---
title: Alihankinnan aikarivit
description: Tässä aiheessa selostetaan, miten tallennetaan alihankinnan aikarivit ja ajan ostaminen toimittajilta.
author: rumant
ms.date: 08/05/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: c1adc1e88369e9f60548ed69b5950070d5f10c57
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/14/2022
ms.locfileid: "8595678"
---
# <a name="subcontract-lines-for-time"></a>Alihankinnan aikarivit

[!include [banner](../../includes/dataverse-preview.md)]

_**Käytetään:** Lite-käyttöönotto – kauppa proformalaskutukseen_

Alihankinta Dynamics 365 Project Operationsissa voi sisältää alihankinnan aikarivin. Alihankinnan aikarivien avulla projektipäällikkö voi ostaa toimittajalta resurssiaikaa projektitehtävien suorittamiseksi ja resurssivaatimusten täyttämiseksi.

Luo Project Operationsissa alihankinnan aikarivi seuraavien vaiheiden mukaisesti.

1. Valitse siirtymisruudusta **Alihankinnat** ja avaa alihankinta.
2. Valitse **Alihankintarivit**-välilehdessä **Uusi** luodaksesi uuden alihankintarivin.
3. Valitse **Pikaluonti**-sivun **Tapahtumaluokka**-kentässä **Aika**.
4. Syötä muut kenttätiedot ja valitse **Tallenna**.

  Seuraavassa taulukossa on tietoja kentistä **Alihankintarivi**-sivulla ja **Pikaluonti**-sivulla.

| **Kenttä** | **Kuvaus** | **Toiminnallinen vaikutus** |
| --- | --- | --- |
| Nimi | Alihankintarivin nimi tunnistamisen helpottamiseksi. | Tämä näkyy kaikkien hakujen ensimmäisenä sarakkeena alihankintarivien perusteella. |
| Kuvaus | Lyhyt kuvaus alihankintarivillä ostettavista palveluista. |Ei ole |
| Rivityyppi |   Tämän kentän oletusarvo on **Määräpohjainen**.| Ei ole |
| Laskutustapa | Tämä on asetusjoukko, joka edustaa kahta pääsopimusmallia, joita Project Operations tukee: **Kiinteä hinta** ja **Aika ja materiaali**. | Valitun laskutustavan perusteella välitavoitteeseen perustuva laskuaikataulu on käytettävissä alihankintariveillä, joilla on kiinteähintainen laskutustapa. |
| Tapahtumaluokka | Oletusarvo on **Aika**. | Tämä osoittaa, että alihankintariviä käytetään alihankinnan ajan oston kirjaamiseen. |
| Rooli | Valitse niiden alihankinnan resurssien rooli, joiden aikaa ostetaan. | Alihankintaresurssien suorittama rooli määrittää oston kustannukset. |
| Pyydetty alku | Anna päivämäärä, jona alihankintaresurssit on oltava käytössä, jotta työ voidaan aloittaa. | Tämän avulla voidaan valita projektihinnasto alihankintaan liitetyistä projektihinnastoista. Alihankintarivin roolin kustannus on peräisin tästä hinnastosta. |
| Pyydetty loppu | Anna päivämäärä, jona alihankintaresurssin tehtävä päättyy. | Tätä käytetään varoitusten näyttämiseen, kun projektipäällikkö käyttää kapasiteettia resurssivaatimuksiin, jotka tapahtuvat kyseisen päivämäärän jälkeen. |
| Tilattu määrä | Määritä toimittajalta ostettavan roolin tuntien määrä. | Tätä käytetään varoitusten näyttämiseen, kun projektipäällikkö ylikäyttää tätä kapasiteettia resurssivaatimuksiin. |
| Yksikköryhmä | Oletusarvo on **Aika-yksikköryhmä**, eikä sitä voi muuttaa. | Ei ole|
| Yksikkö | Tämän kentän oletusarvo on tuntien perusyksikkö kohteesta **Aika-yksikköryhmä**. Voit muuttaa tätä arvoa, jos haluat ostaa minkä tahansa **Aika-yksikköryhmä**-yksikön, kuten päivän tai viikon. | **Roolin** ja **Yksikön** yhdistelmää käytetään alihankintarivin yksikköhinnan oletusarvona tai laskettuna arvona. |
| Yksikköhinta | Yksikköhinnan oletusarvo käyttää **Roolin** ja **Yksikön** yhdistelmää projektihinnastosta, joka soveltuu alihankintarivin **Pyydetty alkaminen** -päivämäärään. | Kun soveltuvassa projektin hinnastossa hinta on määritetty eri yksikköön kuin alihankintarivillä, järjestelmä laskee yksikköhinnan yksikkömuunnoksen avulla. |
| Välisumma |    Tämä on vain luku -kenttä, joka lasketaan muodossa määrä x yksikköhinta, jos sekä määrä- että yksikköhinta-arvot on syötetty. Jos joko määrä, yksikköhinta tai molemmat ovat tyhjät, voit syöttää arvon kenttään. | Ei ole|
| Arvonlisävero |   Anna arvonlisäveron summa. |Ei ole |
| Loppusumma | Alihankintarivin kokonaissumma verot mukaan lukien. Tämä kenttä lasketaan muodossa välisumma + arvonlisävero.|Ei ole |

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
