---
title: Projektin kululuokkien synkronointi talous- ja toimintosovellusten ja Project Service Automationin välillä
description: Tässä artikkelissa käsitellään malleja ja taustalla olevia tehtäviä, joilla projektin kululuokat synkronoidaan Microsoft Dynamics 365 Financen ja Dynamics 365 Project Service Automationin välillä.
author: Yowelle
ms.date: 07/20/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: johnmichalak
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 8.0.0
ms.openlocfilehash: 630c4fa7a159aa46b46984736080cd007d519a6c
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8927232"
---
# <a name="synchronize-project-expense-categories-between-finance-and-operations-and-project-service-automation"></a>Projektin kululuokkien synkronointi talous- ja toimintosovellusten ja Project Service Automationin välillä

[!include[banner](../includes/banner.md)]

Tässä artikkelissa käsitellään malleja ja taustalla olevia tehtäviä, joilla projektin kululuokat synkronoidaan Dynamics 365 Financen ja Dynamics 365 Project Service Automationin välillä.

> [!NOTE]
> - Projektitehtävien integrointi, kulutapahtumien luokat, työaika-arviot, kuluarviot ja toimintojen lukitus ovat käytettävissä versiossa 8.0.
> - Toteutuneiden arvojen integrointi on käytettävissä alkaen versiosta 8.0.1 tai myöhempi.
> - Jos käytössäsi on Enterprise Edition 7.3.0, kun olet asentanut tietokannan 4132657 ja tietokannan 4132660, voit integroida malleja projektitehtävien, kulutapahtumien luokkien, tuntiarvioiden, kuluarvioiden ja toteutuneiden arvojen sekä toimintojen lukitsemisen määrittämiseksi. Jos sinun on nollattava kirjanpidollinen jako, suosittelemme myös tietokannan 4131710 asentamista.

## <a name="data-flow-for-project-service-automation-and-finance"></a>Tietovuo Project Service Automationille ja Financelle

Project Service Automationin ja Financen integrointiratkaisua käyttää tietojen integrointitoimintoa tietojen synkronointiin Project Service Automationin ja Financen eri esiintymien välillä. Tietojen integrointitoiminnossa käytettävissä olevat integrointimallit mahdollistavat projektien liiketapahtumaluokkien tietovuon Financen ja Project Service Automationin välillä.

Jos projektin kululuokkia hallitaan Financessa, integrointi tehdään ensin Financesta Project Service Automationiin. Projektin kululuokkien integrointitunnukset päivitetään sitten Project Service Automationista Financeen synkronoimalla.

Jos projektin kululuokkia hallitaan Project Service Automationissa, integrointi tehdään ensin Project Service Automationista Financeen. Projektiluokat täytyy jo määrittää Financessa ennen synkronointia Project Service Automationista. Synkronoi sitten Financesta takaisin Project Service Automationiin ja sitten Project Service Automation -palvelusta Financeen uudelleen. Näin varmistetaan, että luokat on linkitetty eikä kaksoiskappaleita luoda.

> [!NOTE]
> Yleensä projektin kululuokkia hallitaan Financessa. Jos niitä ei kuitenkaan ole tai jos kululuokkia on jo luotu Project Service Automationissa, sinun on ensin synkronoitava käyttämällä projektin kulutapahtumaluokkia (PSA to Fin ja OPS). Synkronoi sitten käyttämällä projektin kulutapahtumaluokkamallia (FIN ja Ops PSA). Suorita sitten synkronointi Project Service Automationista Financeen vielä yhden kerran.
>
> Jos synkronoit ensin Project Service Automationista, seuraavien vaatimusten on täytyttävä Financessa, ennen kuin synkronointi suoritetaan:
>
> - Project Service Automationissa määritettyä projektiluokkaa vastaavan jaetun luokan on oltava käytössä, ja sen on oltava otettu käyttöön sekä **Projektissa** että **Kulussa**.
> - Kullakin Financen yrityksellä, johon on integroituva, on oltava seuraavat projektiluokat:
>
>     - **Projektiluokka** on olemassa. 
>     - **Käytä kuluina** -asetus on käytössä.
>     - **Aktiivinen kirjauskansiossa** on käytössä.
>     - **Tapahtumatyypiksi** on määritetty **Kulu**.

Seuraavassa kuvassa on esitetty, miten tiedot synkronoidaan Project Service Automationin ja Financen välillä.

[![Tietovuo Project Service Automationin Financeen integroinnissa.](./media/ProjectExpenseCategoriesFlow.png)](./media/ProjectExpenseCategoriesFlow.png)

## <a name="project-expense-category-synchronization-from-finance-to-project-service-automation"></a>Projektikululuokkien synkronointi Financen ja Project Service Automationin välillä

### <a name="template-and-task"></a>Malli ja tehtävä

Jos haluat käyttää mallia, valitse Microsoft Power Appsin hallintakeskuksessa **Projektit** ja sitten oikeassa yläkulmassa **Uusi projekti** valitaksesi julkisia malleja.

Seuraavaa mallia ja pohjana olevaa tehtävää käytetään projektien kululuokkien synkronoimiseen Financesta Project Service Automationiin:

- **Tietojen integrointimallin nimi:** Projektin kuluarviotapahtumien luokat (Fin ja Ops to PSA:han)
- **Projektin tehtävän nimi:** Synkronoi luokat PSA-järjestelmään

### <a name="entity-set"></a>Entiteettijoukko

| Rahoitus                           | Project Service Automation |
|-----------------------------------|----------------------------|
| Luokkien integroinnin entiteetti | Tapahtumaluokat     |

### <a name="entity-flow"></a>Entiteettivuo

Projektien kululuokkia hallitaan Financessa ja ne synkronoidaan Project Service Automationiin tapahtumaluokkina.

### <a name="power-query"></a>Power Query

Tapahtumaluokan laskutustyyppi on määritettävä Microsoft Power Query for Excelillä, kun synkronointi tehdään Project Service Automationiin. Projektin kulutapahtumaluokat (FIN ja Ops to PSA) -malli sisältää oletussarakkeen ja -yhdistämismäärityksen. Jos luot oman mallin, tämä ehtosarake on lisättävä Power Queryyn. Toimi seuraavasti.

1. Napsauttamalla nuolta voit avata projektikululuokat tehtävänyhdistämismäärityksen projektin kulutapahtumaluokissa (FIN ja Ops to PSA) -mallin.
2. Napsauta **Kyselyn ja suodatuksen lisäasetukset** avataksesi Power Queryn.
2. Valitse **Lisää ehdollinen sarake**.
3. Syötä uudelle sarakkeelle nimi, kuten **Laskutustyyppi**.
4. Kirjoita seuraava ehto: **if CATEGORYID not equal to null then 19235001, Otherwise null**.
5. Valitse **OK** sarakkeessa.
6. Varmista, että yhdistät tämän uuden sarakkeen yhdistämissivulle.

Seuraavassa kuvissa on esimerkki mallitehtävien yhdistämismäärityksissä tietojen integroinnissa. Yhdistämismäärityksessä näytetään kenttätiedot, jotka synkronoidaan Financesta Project Service Automationiin.

[![Projektikululuokka Project Service Automationin malliyhdistämiseen.](./media/ProjectExpenseCategoriesToPSAMapping.jpg)](./media/ProjectExpenseCategoriesToPSAMapping.jpg)

## <a name="project-expense-category-synchronization-from-project-service-automation-to-finance"></a>Projektikululuokkien synkronointi Project Service Automationista Financeen

### <a name="template-and-task"></a>Malli ja tehtävä

Seuraavaa mallia ja pohjana olevaa tehtävää käytetään projektien kululuokkien synkronoimiseen Project Service Automationista Financeen:

- **Tietojen integrointimallin nimi:** Projektin kuluarviotapahtumien luokat (PSA to Fin and Ops)
- **Projektin tehtävän nimi:** Synkronoi luokat Fin Ops -järjestelmään

### <a name="entity-set"></a>Entiteettijoukko

| Project Service Automation | Rahoitus                           |
|----------------------------|-----------------------------------|
| Tapahtumaluokat     | Luokkien integroinnin entiteetti |

### <a name="entity-flow"></a>Entiteettivuo

Projektien kululuokkia hallitaan Financessa ja ne synkronoidaan Project Service Automationiin tapahtumaluokkina. Synkronointi takaisin Financeen päivittää Finance-projektiluokan Project Service Automationin integraatiotunnuksella.

### <a name="template-mapping-in-data-integration"></a>Mallien yhdistämismääritys tietojen integroinnissa

Seuraavassa kuvissa on esimerkki mallitehtävien yhdistämismäärityksissä tietojen integroinnissa.

> [!NOTE]
> Yhdistämismäärityksessä näytetään kenttätiedot, jotka synkronoidaan Project Service Automationista Financeen.

[![Project Service Automationista Financen malliyhdistämiseen.](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)


[!INCLUDE[footer-include](../includes/footer-banner.md)]