---
title: Alihankinnan kululuokkarivit
description: Tässä artikkelissa käsitellään sitä, miten kulujen alihankintarivejä voidaan kirjata ja käyttää kenttiä toimittajilta ostetun ajan kirjaamiseen.
author: rumant
ms.date: 08/06/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 0b02a8aa0fce7bcb52374c0755d4bb85db16dad3
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8921022"
---
#  <a name="subcontract-lines-for-expense-categories"></a>Alihankinnan kululuokkarivit

[!include [banner](../../includes/dataverse-preview.md)]

_**Käytetään:** Lite-käyttöönotto – kauppa proformalaskutukseen_

Alihankinta Dynamics 365 Project Operationsissa voi sisältää rivin kululuokkia varten. Kululuokkien alihankintarivien avulla projektipäällikkö voi ostaa toimittajilta palvelujen tai tuotteiden luokkia, jotka he voivat veloittaa projektista.

Luo Project Operationsissa alihankinnan kululuokkarivi seuraavien vaiheiden mukaisesti.

1. Valitse siirtymisruudussa **Alihankinnat** ja avaa sitten alihankinta, jota haluat käsitellä.
2. Valitse **Alihankintarivit**-välilehdessä **Uusi** luodaksesi uuden rivin.
3. **Pikaluonti** -sivun **Tapahtumaluokka**-kentässä valitse **Kulu** ja syötä tai valitse muut tarvittavat kenttätiedot.

Seuraavassa taulukossa on tietoja kentistä **Alihankintarivi**-tietosivulla ja **Pikaluonti**-sivulla.

| **Kenttä** | **Kuvaus** | **Toiminnallinen vaikutus** |
| --- | --- | --- |
| Nimi | Alihankintarivin nimi tunnistamisen helpottamiseksi. | Tämä näkyy kaikkien hakujen ensimmäisenä sarakkeena alihankintarivien perusteella. |
| Kuvaus | Alihankintarivillä ostettavien kululuokkien lyhyt kuvaus. | Ei ole |
|Rivityyppi | Tämän kentän oletusarvo on **Määräpohjainen**. |Ei ole |
| Laskutustapa | Tämä on asetusjoukko, joka edustaa kahta pääsopimusmallia, joita Project Operations tukee: **Kiinteä hinta** ja **Aika ja materiaali**. | Välitavoitteeseen perustuva laskuaikataulu on käytettävissä alihankintariveillä, jos kiinteähintainen laskutustapa on valittuna. |
| Tapahtumaluokka | Tämän kentän oletusarvo on **Aika**. Jos haluat luoda alihankintarivejä tuotteiden ostamista varten, määritä **Tapahtumaluokka**-kenttä arvoon **Kulu**.  | Tämä osoittaa, että alihankintariviä käytetään projektissa käytettävien kululuokkien ostojen kirjaamista varten. |
| Tapahtumakategoria | Näyttää luettelon järjestelmän aktiivisista tapahtumaluokista. |Ei ole |
| Pyydetty alku | Määritä päivämäärä, jona ostoluokkien on oltava käytettävissä toimittajalta. | Pyydettyä alkamista käytetään projektin hinnaston valitsemiseen alihankintaan liitetyistä projektihinnastoista. Alihankintarivin luokan kustannus on peräisin tästä hinnastosta. |
| Pyydetty loppu | Anna päivämäärä, jona ostoluokkia ei enää tarvita. | Tätä käytetään varoitusten näyttämiseen, kun projektipäällikkö liittää tämän alihankintarivin projektin tiettyihin kuluarvioihin, jotka ovat pakollisia tämän päivämäärän jälkeen. |
| Tilattu määrä | Toimittajalta ostettavan luokan määrä. | Tätä käytetään varoitusten näyttämiseen, kun projektipäällikkö ylikäyttää tätä määrää.|
| Yksikköryhmä | Oletusarvo perustuu oletusyksikköryhmään, joka on määritetty valitulle luokalle. |Ei ole |
| Yksikkö | Oletusarvo perustuu oletusyksikköön, joka on määritetty valitulle luokalle.  | **Luokan** ja **Yksikön** yhdistelmää käytetään alihankintarivin yksikköhinnan oletusarvona tai laskettuna arvona.  |
| Yksikköhinta | Oletusarvo käyttää **Luokan** ja **Yksikön** yhdistelmää luokkahinnoista, jotka liittyvät projektihinnastoon, joka soveltuu alihankintarivin pyydettyyn alkamiseen. |Ei ole |
| Välisumma | Tämä on vain luku -kenttä, joka lasketaan muodossa määrä x yksikköhinta, jos sekä määrä- että yksikköhinta-arvot on syötetty. Jos jompikumpi tai molemmat kentät ovat tyhjiä, voit syöttää tähän kenttään arvon. |Ei ole |
| Arvonlisävero | Anna arvonlisäveron summa. |Ei ole |
| Loppusumma | Alihankintarivin kokonaissumma verot mukaan lukien. Tämä kenttä lasketaan muodossa välisumma + arvonlisävero. |Ei ole |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
