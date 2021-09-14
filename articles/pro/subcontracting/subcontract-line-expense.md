---
title: Alihankinnan kululuokkarivit
description: Tässä aiheessa selitetään, miten voidaan kirjata kulujen alihankintarivejä ja käyttää kenttiä toimittajilta ostetun ajan kirjaamiseen.
author: rumant
ms.date: 08/06/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 9e8e7bb66063dab6db1ac8da1753913aee0ef3fc
ms.sourcegitcommit: 80aa1e8070f0cb4992ac408fc05bdffe47cee931
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/13/2021
ms.locfileid: "7323817"
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

| **Kenttä** |  **Kuvaus** |
| ----------| ---------------- |
| Nimi | Alihankintarivin nimi. |
| Kuvaus | Lyhyt kuvaus alihankintarivillä ostettavista palvelu- tai tuoteluokista. |
| Rivityyppi | Tämän kentän oletusarvo on **Määräpohjainen**.  |
| Laskutustapa | Alihankintarivin laskutustapa. Alihankintarivin laskutustavan perusteella välitavoitteeseen perustuva laskuaikataulu tulee käytettäväksi kiinteähintaiselle laskutustavalle.  |
| Tapahtumaluokka | Tämän kentän oletusarvo on **Aika**. Jos haluat luoda alihankintarivejä tuotteiden ostamista varten, määritä **Tapahtumaluokka**-kenttä arvoon **Kulu**. Kentän arvo osoittaa, että alihankintarivillä tallennetaan projektissa käytettävien tuote- tai palveluluokkien ostot. |
| Tapahtumakategoria | Valitse tapahtumaluokka. |
| Pyydetty alku | Päivämäärä, jolloin ostoluokkien on oltava saatavissa toimittajalta. Pyydettyä alkua käytetään myös projektin hinnaston valitsemiseen projektin hinnastoista, jotka on liitetty alihankkijaan. Tämän jälkeen alihankintarivillä oleva luokan kustannus tulee oletusarvona tästä hinnastosta. |
| Pyydetty loppu | Päivämäärä, jolloin ostoluokkia ei enää tarvita. Tämä päivämäärä kutsuu varoituksen, jos projektipäällikkö liittää tämän alihankintarivin tiettyihin kuluarvioihin projekteissa, jotka on päivätty tämän päivämäärän jälkeen. |
| Tilattu määrä | Toimittajalta ostettavan luokan määrä. Kun projektipäällikkö ylittää ostetun määrän, siitä tulee varoitus.  |
| Yksikköryhmä | Tämän kentän oletusarvo perustuu oletusyksikköryhmään, joka on määritetty valitulle luokalle. |
| Yksikkö | Tämän kentän oletusarvo perustuu valitun luokan oletusyksikköryhmään. Luokan ja yksikön yhdistelmää käytetään alihankintarivin yksikköhinnan oletusarvoksi asettamiseen. |
| Yksikköhinta | Yksikköhinnan kentän arvon oletusarvo tulee käyttämällä luokan ja yksikön yhdistelmää luokkahinnoista, jotka liittyvät projektin hinnastoon, jota voi soveltaa alihankintarivin pyydettyyn alkuun.  |
| Välisumma | Tämä vain luku -kenttä lasketaan automaattisesti määrän yksikköhintana, jos sekä määrän että yksikköhinnan arvot on syötetty. Jos toinen kenttä on tyhjä tai molemmat kentät ovat tyhjät, voit syöttää tähän kenttään arvon manuaalisesti.  |
| Arvonlisävero | Anna arvonlisäveron summa.  |
| Loppusumma | Alihankintarivin kokonaissumma verot mukaan lukien. Tämä kenttä lasketaan muodossa välisumma + arvonlisävero.  |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
