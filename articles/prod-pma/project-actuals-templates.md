---
title: Synkronoi projektin todelliset arvot suoraan Project Service Automationista projekti-integraation kirjauskansioon kirjausta varten Finance and Operationsissa
description: Tässä aiheessa kuvataan malleja ja sen pohjana olevia tehtäviä, jota käytetään projektin toteutuneita arvoja synkronoimiseen suoraan Microsoft Dynamics 365 Project Service Automationista Finance and Operationsen.
author: Yowelle
manager: AnnBe
ms.date: 07/20/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.3.0
ms.openlocfilehash: cff62e739e88dc45e7c3d1ea044875f0600f2bc1
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/16/2020
ms.locfileid: "4075480"
---
# <a name="synchronize-project-actuals-directly-from-project-service-automation-to-the-project-integration-journal-for-posting-in-finance-and-operations"></a>Synkronoi projektin todelliset arvot suoraan Project Service Automationista projekti-integraation kirjauskansioon kirjausta varten Finance and Operationsissa

[!include[banner](../includes/banner.md)]

Tässä aiheessa kuvataan malleja ja sen pohjana olevia tehtäviä, jota käytetään projektin toteutuneita arvoja synkronoimiseen suoraan Dynamics 365 Project Service Automationista Dynamics 365 Financeen.

Malli synkronoi Project Service Automationin tapahtumat Financen väliaikaiseen taulukkoon. Kun synkronointi on valmis, tiedot **on tuotava** väliaikaisesta taulukosta integrointipäiväkirjaan.

> [!NOTE]
> - Projektin toteutuneet -integrointi on käytettävissä alkaen versiosta 8.0.1.
> - Jos käytössäsi on Enterprise Edition 7.3.0, kun olet asentanut tietokannan 4132657 ja tietokannan 4132660, voit integroida malleja projektitehtävien, kulutapahtumien luokkien, tuntiarvioiden, kuluarvioiden ja toteutuneiden arvojen sekä toimintojen lukitsemisen määrittämiseksi. Jos sinun on nollattava kirjanpidollinen jako, suosittelemme myös tietokannan 4131710 asentamista.
> - Jos käytössäsi on versio 7.3.0 ja tuot maksutapahtumia Project Service Automationin kautta, sinun täytyy asentaa tietokanta 4345320, jotta voit lisätä kyseiset maksut projektilaskuun.
> - Jos olet syöttämässä arvonlisäverosummia aika- tai kulutapahtumille Project Service Automationissa, sinun täytyy asentaa Project Service Automation Update 7. Muussa tapauksessa veron toteutuneita arvoja ei linkitetä niihin liittyviin ajan tai kulujen todellisiin arvoihin, eikä niitä synkronoida Financeen. Pyydä lisätietoja tukitiimiltä.

## <a name="data-flow-for-project-service-automation-to-finance"></a>Tietovuo Project Service Automationista Financeen

Project Service Automationin integrointiratkaisua Financeen käyttää tietojen integrointitoimintoa tietojen synkronointiin Project Service Automationin ja Financen eri esiintymien välillä. Tietojen integrointitoiminnossa käytettävissä olevat integrointimallit mahdollistavat projektin toteutuneiden arvojen työnkulun Project Service Automationista Financeen.

Seuraavassa kuvassa on esitetty, miten tiedot synkronoidaan Project Service Automationin ja Financen välillä.

[![Työnkulku Project Service Automationin integroinnissa Finance and Operationsiin](./media/ProjectActualsFlow.jpg)](./media/ProjectActualsFlow.jpg)

## <a name="project-actuals-from-project-service-automation"></a>Projektin toteutuneet arvot Project Service Automationista

### <a name="template-and-tasks"></a>Malli ja tehtävät

Jos haluat käyttää käytettävissä olevia malleja, valitse Microsoft Power Appsin hallintakeskuksessa **Projektit** ja sitten oikeassa yläkulmassa **Uusi projekti** valitaksesi julkisia malleja.

Seuraavaa mallia ja pohjana olevia tehtäviä käytetään projektin toteutuneiden arvojen synkronoimiseen Project Service Automationista Financeen:

- **Tietojen integroinnin mallin nimi:** Projektin toteutuneet arvot (PSA:sta Fin:iin ja Ops:iin)
- **Projektin tehtävien nimet:**

    - Todelliset arvot
    - TransactionConnections

### <a name="entity-set"></a>Entiteettijoukko

| Project Service Automation | Rahoitus                                   |
|----------------------------|----------------------------------------------------------|
| Todelliset arvot                    | Projektin toteutuneiden arvojen integroinnin entiteetti                   |
| Tapahtuman yhteydet    | Projektitapahtuman integrointikohdesuhteet |

### <a name="entity-flow"></a>Entiteettivuo

Projektin toteutuneita hallitaan Project Service Automationissa, ja ne synkronoidaan Financeen projektin integroinnin kirjauskansioon. Kirjanpitoa käytetään taloushallinnon oletusdimensioiden ja kirjausasetusten perusteella.

### <a name="prerequisites"></a>Edellytykset

Ennen todellisten arvojen synkronointia sinun täytyy määrittää Project Service Automation -integrointiparametrit ja synkronoida projektit, projektitehtävät ja projektin kulutapahtumien luokat.

### <a name="power-query"></a>Power Query

Projektien toteutuneiden arvojen mallissa on käytettävä Microsoft Power Query for Exceliä seuraavien tehtävien suorittamiseen:

- Muunna tapahtumatyyppi Project Service Automationissa Financen oikeaan tapahtumatyyppiin. Tämä muunnos on jo määritetty projektin toteutuneet arvot (PSA to Fin ja OPS) -mallissa.
- Muunna laskutustyyppi Project Service Automationissa Financen oikeaan laskutustyyppiin. Tämä muunnos on jo määritetty projektin toteutuneet arvot (PSA to Fin ja OPS) -mallissa. Tämän jälkeen laskutustyyppi yhdistetään rivin ominaisuuteen **Project Service Automationin integrointiparametrit** -sivun määritysten perusteella .
- Suodata tiettyihin resurssin organisaatioyksiköihin, jotka on synkronoitava tämän mallin kanssa.
- Jos konserniyritysten välinen aika tai konsernin kulutiedot synkronoidaan rahoittamaan, palvelusopimuksen organisaatioyksikkö on muunnettava oikeaksi yritykseksi entiteetille Financessa. Projektin todelliset arvot (PSA to Fin ja OPS) -mallissa ehdollinen sarake määritetään demotietojen perusteella. Viimeksi lisätty ehdollinen sarake on päivitettävä oikeisiin yrityksiin. Muussa tapauksessa voi tapahtua joko integrointivirhe tai virheellisiä toteutuneita tapahtumia voidaan tuoda Financeen.
- Jos konsernin aikaa tai konsernin sisäisiä kuluja ei synkronoida Financeen, sinun täytyy poistaa mallista viimeksi lisätty ehdollinen sarake. Muussa tapauksessa voi tapahtua joko integrointivirhe tai virheellisiä toteutuneita tapahtumia voidaan tuoda Financeen.

#### <a name="contract-organizational-unit"></a>Sopimusorganisaatioyksikkö
Voit päivittää lisätyn ehdollisen sarakkeen mallissa avaamalla yhdistämismäärityksen valitsemalla **Yhdistämismääritys** -nuoli. Valitse **Tarkka kysely ja suodatus** -linkki avataksesi Power Queryn.

- Jos käytät oletusarvoisten projektien toteutuneiden arvojen (PSA:sta Fin:iin ja Ops:iin) mallia, valitse Power Queryssä ensimmäinen **Lisätty ehto** **Sovelletut vaiheet** -osasta. Korvaa **Toiminto** -kirjauksessa **USSI** sen yrityksen nimellä, jota käytetään integroinnissa. Lisää **Funktio** -merkintään lisäehtoja tarpeen mukaan ja päivitä **Tai** -ehto **USMF** -ohjelmasta oikeaan yritykseen.
- Jos olet luomassa uutta mallia, sinun täytyy lisätä sarake, joka tukee konsernin sisäistä aikaa ja kuluja. Valitse Power Queryssä **Lisää ehdollinen sarake** ja kirjoita uuden sarakkeen nimi, kuten **Yritys**. Kirjoita sarakkeen ehto, silloin jos **msdyn\_contractorganizationalunitid.msdyn\_name** on \<organizational unit\>, sitten \<enter the legal entity\>; muuten tyhjäarvo

### <a name="template-mapping-in-data-integration"></a>Mallien yhdistämismääritys tietojen integroinnissa

Seuraavassa kuvissa on esimerkki mallitehtävien yhdistämismäärityksessä tietojen integroinnissa. Yhdistämismäärityksessä näytetään kenttätiedot, jotka synkronoidaan Project Service Automationista Financeen.

[![Mallien yhdistäminen ‑ toteutuneet](./media/ActualsMapping.jpg)](./media/ActualsMapping.jpg)

[![Mallien yhdistäminen - tapahtumayhteydet](./media/TransactionConnections.jpg)](./media/TransactionConnections.jpg)

## <a name="import-from-staging-table-after-integration-from-project-service-automation"></a>Tuominen väliaikaisesta taulukosta Project Service Automationin integroinnin jälkeen

Tuonti väliaikaisesta taulusta kausittaisesta prosessista on suoritettava sen jälkeen, kun todellisten tietojen synkronointi on suoritettu Project Service Automationista Financeen. Tämä prosessi tuo projektitapahtumat väliaikaisesta taulukosta Project Service Automationin integroinnin kirjauskansioon, jossa kirjanpitoa käytetään ja tuodut tapahtumat voidaan kirjata. Tämä prosessi kannattaa suorittaa komentojonotilassa. Se voidaan vaihtoehtoisesti määrittää suoritettavaksi toistuvana eränä.

## <a name="update-actuals-from-finance"></a>Päivitä Financen toteutuneet arvot

### <a name="template-and-tasks"></a>Malli ja tehtävät

Seuraavia malleja ja perustehtäviä käytetään, kun kirjataan kirjattujen projektitapahtumien tositenumero ja arvonlisäverot Financesta Project Service Automationiin:

- **Tietojen integroinnin mallin nimi:** Projektin toteutuneiden arvojen päivitys (Fin Opsista PSA:han)
- **Projektin tehtävien nimet:**

    - Todelliset arvot 
    - TransactionConnections

### <a name="entity-set"></a>Entiteettijoukko

| Rahoitus                                                  | Project Service Automation |
|----------------------------------------------------------|----------------------------|
| Projektin toteutuneiden arvojen integroinnin entiteetti                   | Todelliset arvot                    |
| Projektitapahtuman integrointikohdesuhteet | Tapahtuman yhteydet    |

### <a name="entity-flow"></a>Entiteettivuo

Projektin toteutuneita hallitaan Project Service Automationissa, ja ne synkronoidaan Financeen projektin integroinnin kirjauskansioon. Kun toteutuneet on kirjattu Financeen, ne päivitetään Project Service Automationissa käyttämällä Financen tositenumeroa. Jos arvonlisäverot on lisätty Financeen, Project Service Automationissa luodaan uudet veron todelliset arvot.

### <a name="power-query"></a>Power Query

Projektien toteutuneiden arvojen päivitysmallissa on käytettävä Power Queryä seuraavien tehtävien suorittamiseen:

- Muunna Financen tapahtumatyyppi oikeaan tapahtumatyyppiin Project Service Automationissa. Tämä muunnos on jo määritetty projektin toteutuneet arvot (PSA to Fin ja OPS) -päivitysmallissa.
- Muunna laskutustyyppi Financessa Project Service Automationin oikeaan laskutustyyppiin. Tämä muunnos on jo määritetty projektin toteutuneet arvot (PSA to Fin ja OPS) -päivitysmallissa.

### <a name="template-mapping-in-data-integration"></a>Mallien yhdistämismääritys tietojen integroinnissa

Seuraavissa kuvissa on esimerkkejä mallitehtävien yhdistämismäärityksestä tietojen integroinnissa. Yhdistämismäärityksessä näytetään kenttätiedot, jotka synkronoidaan Financesta Project Service Automationiin.

[![Mallien yhdistäminen ‑ toteutuneet päivitys](./media/ActualsUpdateMapping.jpg)](./media/ActualsUpdateMapping.jpg)

[![Mallien yhdistäminen ‑ Tapahtumat päivitys](./media/TransactionConnectionsUpdate.jpg)](./media/TransactionConnectionsUpdate.jpg)


[!INCLUDE[footer-include](../includes/footer-banner.md)]