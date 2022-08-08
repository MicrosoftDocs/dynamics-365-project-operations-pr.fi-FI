---
title: Heinäkuun 2022 uudet ominaisuudet – Project Operations resurri/ei-varastoitavien skenaarioissa
description: Tässä artikkelissa on tietoja Microsoft Dynamics 365 Project Operationsin resursseihin ja ei-varastoitaviin perustuvissa skenaarioissa heinäkuussa 2022 julkaistussa versiossa saatavilla olevista laatupäivityksistä.
author: ramagadu
ms.date: 07/19/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: ramagadu
ms.openlocfilehash: cbee9281d2fae485a3ebcd38bb884a2b2322f8d1
ms.sourcegitcommit: 66e376675e6df8efc86fa84ec24e9aad6a980304
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 07/21/2022
ms.locfileid: "9183890"
---
# <a name="whats-new-july-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>Heinäkuun 2022 uudet ominaisuudet – Project Operations resurri/ei-varastoitavien skenaarioissa

_**Käytetään:** Project Operationsin resursseihin ja ei-varastoitaviin perustuvissa skenaarioissa_

Tämä artikkeli koskee seuraavia Microsoft Dynamics 365 Project Operationsin osia ja versioita:

- Project Operations Dataversessa ympäristöversio 4.44.0.22
- Projektinhallinta ja kirjanpito Dynamics 365 Finance -ympäristön versiossa 10.0.28

## <a name="project-operations-dual-write-maps-updates"></a>Project Operationsin kaksoiskirjoituskarttojen päivitys

Tässä versiossa ei ole päivityksiä Project Operationsin kaksoiskirjoituskartoille. Project Operationsin kaksoiskirjoituskarttojen luettelo ja versiot ovat kohdassa [Project Operationsin kaksi kaksoiskirjoituskarttojen versiot](../environment/resource-dual-write-maps.md).

Suorita aina ympäristön kartan uusin versio ja ota käyttöön kaikki taulukkokartat, kun päivität Project Operations Dataverse -ratkaisua ja rahoitusratkaisun versiota. Jotkin ominaisuudet ja toiminnot eivät ehkä toimi oikein, jos kartan uusinta versiota ei ole aktivoitu. Voit tarkastella kartan aktiivista versiota **Kaksoiskirjoitus**-sivun **Versio**-sarakkeessa. Voit aktivoida kartan uuden version valitsemalla **Taulukkokartan versiot**, valitsemalla uusimman version ja tallentamalla sitten valitun version. Jos olet mukauttanut valmista taulukkokarttaa, voit käyttää muutokset uudelleen. Lue lisätietoja kohdasta [Ratkaisun elinkaaren hallinta](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Jos kartan käynnistämisen yhteydessä tulee ongelma, seuraa ohjeita [Puuttuvien taulukkosarakkeiden ongelma kartoissa](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) -osassa kaksoiskirjoituksen vianmääritysoppaassa.

## <a name="quality-updates"></a>Laatupäivitykset

### <a name="project-operations-on-dataverse"></a>Project Operations Dataversessä

| Ominaisuusalue | Viitenumero | Laatupäivitys |
| --- | --- | --- |
| Käyttöönotto ja määritys | 2761472 | Project Operationsin asennusvirhettä käsitellään. |
| Laskutus ja hinnoittelu | 2746940 | Alihankintarivin nimessä voi olla enintään 100 merkkiä. |
| Laskutus ja hinnoittelu | 2739162 | Asiakkaiden on pystyttävä näkemään valintanauhan painikkeet todellisten arvojen ruudukkonäkymässä. |
| Projektin suunnittelu ja seuranta | 2730318 | Projektin aiheen ei-tuettujen merkkien päivitetty tarkistus. |
| Laskutus ja hinnoittelu | 2705361 | Välitavoitteen laskutettu toteutunut myynti on sisällytettävä projektin seurantakenttiin. |
| Laskutus ja hinnoittelu | 2675880 | Estä projektin linkitys sopimusriviin, joka ei perustu työhön. |
| Laskutus ja hinnoittelu | 2664396 | Jos tarjoushinnasto tallennetaan ilman tarjousta, järjestelmässä on oltava virhe, jossa kerrotaan, että tarjous ei voi olla tyhjä. |
| Laskutus ja hinnoittelu | 2184019 | **Tehtäväpohjainen laskutus** -välilehteä ei näytetä projekteissa, joilla ei ole taustasopimusta tai -tarjousta. |

### <a name="project-management-and-accounting-in-finance"></a>Projektinhallinta ja kirjanpito Financessa

Saat lisätietoja tähän päivitykseen liittyvistä virheenkorjauksista kirjautumalla sisään Microsoft Dynamics Lifecycle Services (LCS) -sovellukseen ja tarkastelemalla [Knowledge Base -artikkelia](https://fix.lcs.dynamics.com/Issue/Details?bugId=694438).

## <a name="features-turned-on-by-default-in-upcoming-release"></a>Tulevassa julkaisussa oletusarvoisesti käytössä olevat ominaisuudet

Seuraavassa taulukossa luetellaan ominaisuudet, jotka ovat oletusarvoisesti käytössä versiossa 10.0.29. Useimmat automaattisesti käyttöön otetut ominaisuudet voi ottaa käyttöön [ominaisuuksienhallinnassa](/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview). Tulevaisuudessa jotkin automaattisesti käyttöönotetut ominaisuudet voidaan poistaa ominaisuuksien hallinnasta, ja niistä tulee pakollisia. Tämä muutos varmistaa, että asiakkaat käyttävät nykyistä toiminnallisuutta. Näin parannukset voidaan ottaa käyttöön nykyisessä toiminnallisuudessa, kun ne lisätään. Ominaisuudet otetaan automaattisesti käyttöön korkeintaan kerran vuodessa, jos niitä ei ole määritetty olennaisiksi.

| Ominaisuuden nimi | Käyttöönottopäivämäärä | Ominaisuuden lisäysajankohta | Ominaisuuden tila | Moduuli |
| --- | --- | --- |--- |--- |
| Tuntitapahtuman oikaisun käyttöönotto rahoitussäännön kohdistuksen muutoksen perusteella | 16. syyskuuta 2022 | 7. lokakuuta 2020 | Käytössä oletusarvoisesti | Projektinhallinta ja kirjanpito |
| Projektin ostotilauksen ennakkomaksulaskun peruutusominaisuus | 16. syyskuuta 2022 | 6. lokakuuta 2021 | Käytössä oletusarvoisesti | Projektinhallinta ja kirjanpito |
| Laskun ehdotusrivien poistaminen, kun käytössä on Project Operations resurssipohjaisia tai ei-varastoituja skenaarioita varten | 16. syyskuuta 2022 | 6. lokakuuta 2021 | Käytössä oletusarvoisesti | Projektinhallinta ja kirjanpito |
| Kirjanpidon oikaisu kirjatussa projektitapahtumassa | 16. syyskuuta 2022 | 10. toukokuuta 2020 | Käytössä oletusarvoisesti | Projektinhallinta ja kirjanpito |
| Projektinkirjanpidon oletusasetusten käyttöönotto | 16. syyskuuta 2022 | 19. helmikuuta 2020 | Käytössä oletusarvoisesti | Projektinhallinta ja kirjanpito |
| Projektin useiden sopimusrivien ottaminen käyttöön | 16. syyskuuta 2022 | 29. kesäkuuta 2020 | Käytössä oletusarvoisesti | Projektinhallinta ja kirjanpito |
| Projektin tuntikirjauskansioiden määrittäminen vain luku -muotoon, jos nykyinen hyväksynnän tila ei salli muokkausta | 16. syyskuuta 2022 | 6. lokakuuta 2021 | Käytössä oletusarvoisesti | Projektinhallinta ja kirjanpito |
| Synkronoinnin myyntirivien käyttöönotto ostoriveiltä, kun ostorivit päivitetään ja ostotilauksen muutoksenhallinnan parametri on otettu käyttöön | 16. syyskuuta 2022 | 7. lokakuuta 2020 | Käytössä oletusarvoisesti | Projektinhallinta ja kirjanpito |
| Ota käyttöön Project Operations – Dynamics 365 Customer Engagement | 16. syyskuuta 2022 | 29. kesäkuuta 2020 | Käytössä oletusarvoisesti | Projektinhallinta ja kirjanpito |
| Projektitapahtumien peruutusten korjausominaisuus | 16. syyskuuta 2022 | 13. heinäkuuta 2020 | Käytössä oletusarvoisesti | Projektinhallinta ja kirjanpito |

## <a name="features-that-become-mandatory-in-the-upcoming-release"></a>Ominaisuudet, jotka ovat pakollisia tulevassa versiossa

Seuraavassa taulukossa luetellaan ominaisuudet, jotka ovat pakollisia versiossa 10.0.29 ja sitä uudemmissa versioissa.

| Ominaisuuden nimi | Käyttöönottopäivämäärä | Ominaisuuden lisäysajankohta | Ominaisuuden tila | Moduuli |
| --- | --- | --- | --- | --- |
| Rahoituslähteen vahvistetun arvon laskeminen ilman valuuttakurssin pyöristämistä | 16. syyskuuta 2022 | 14. kesäkuuta 2020 | Pakollinen | Projektinhallinta ja kirjanpito |
| Projektin oikaisun kirjauksen käyttöönotto samalla kirjanpitotilillä kuin alkuperäinen tapahtuma | 16. syyskuuta 2022 | 14. kesäkuuta 2020 | Pakollinen | Projektinhallinta ja kirjanpito |
| Projektisopimuksen vahvistetun summan tiedot | 16. syyskuuta 2022 | 31. elokuuta 2019 | Pakollinen | Projektinhallinta ja kirjanpito |
| Lajittelun käyttöönotto resurssin mukaan projektin laskuehdotuksen luomisen aikana | 16. syyskuuta 2022 | 31. elokuuta 2019 | Pakollinen | Projektinhallinta ja kirjanpito |
