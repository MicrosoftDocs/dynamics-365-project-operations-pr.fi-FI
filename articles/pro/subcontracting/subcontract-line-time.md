---
title: Alihankinnan aikarivit
description: Tässä aiheessa selostetaan, miten tallennetaan alihankinnan aikarivit ja ajan ostaminen toimittajilta.
author: rumant
ms.date: 08/05/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 10ebe0fcc86b4652ac01e28108361df1f768b61d
ms.sourcegitcommit: 80aa1e8070f0cb4992ac408fc05bdffe47cee931
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/13/2021
ms.locfileid: "7323862"
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

| **Kenttä** | **Kuvaus** |
| --- | --- |
| Nimi | Alihankintarivin nimi. |
| Kuvaus | Lyhyt kuvaus alihankintarivillä ostettavista palveluista. | 
| Rivityyppi | Tämä kenttä on oletusarvo.  |
| Laskutustapa | Valitse laskutustapa. Viitatun alihankintarivin laskutustavan perusteella välitavoitteeseen perustuva laskuaikataulu tulee käytettäväksi kiinteähintaiselle laskutustavalle. |
| Tapahtumaluokka | Tämä kenttä on oletusarvo, joka osoittaa, käytetäänkö alihankintariviä tallentamaan ajan ostamista alihankkijalta. |
| Rooli | Niiden alihankintaresurssien, joiden aikaa ostetaan, rooli. Alihankintaresursseille määritetty rooli määrittää oston kustannukset. |
| Pyydetty alku | Päivämäärä, jolloin alihankkijaresurssit tarvitaan, jotta työt voidaan aloittaa. Pyydettyä alkua käytetään myös projektin hinnaston valitsemiseen projektin hinnastoista, jotka on liitetty alihankkijaan. Tämän jälkeen alihankintarivillä oleva roolin kustannus tulee oletusarvona tästä hinnastosta. |
| Pyydetty loppu | Päivämäärä, jolloin alihankkijaresurssien käyttäminen päättyy. Tätä päivämäärää käytetään varoitusten näyttämiseen, kun projektipäällikkö käyttää tätä kapasiteettia tehtäviin, jotka tapahtuvat kyseisen päivämäärän jälkeen. |
| Tilattu määrä | Toimittajalta ostettavien roolituntien määrä. Tätä arvoa käytetään varoitusten näyttämiseen, kun projektipäällikkö ylittää tämän kapasiteetin resurssivaatimukset täyttääkseen. |
| Yksikköryhmä | Tämä kenttä käyttää Aika-yksikköryhmän oletusarvoa, eikä sitä voi muuttaa.  |
| Yksikkö | Tämä kenttä käyttää Aika-yksikköryhmän tuntiperusyksikön oletusarvoa. Voit muuttaa tätä arvoa, jos haluat ostaa minkä tahansa Aika-yksikköryhmän yksikön, kuten päivän tai viikon. Roolin ja yksikön yhdistelmää käytetään alihankintarivin yksikköhinnan laskemiseen. |
| Yksikköhinta | Yksikköhinnan oletusarvo tulee käyttämällä roolin ja yksikön yhdistelmää projektin hintaluettelosta, joka soveltuu alihankintarivin pyydettyyn alkamispäivään. Kun soveltuvassa projektin hinnastossa hinta on määritetty eri yksikköön kuin alihankintarivillä, järjestelmä laskee yksikköhinnan yksikkömuunnoksen avulla. |
| Välisumma | Tämä on vain luku -kenttä, joka lasketaan automaattisesti muodossa **Määrä x Yksikköhinta**, jos sekä määrän että yksikköhinnan arvot on syötetty. Jos joko määrä, yksikköhinta tai molemmat ovat tyhjät, voit syöttää arvon kenttään. |
| Arvonlisävero |  Anna arvonlisäveron summa. |
| Loppusumma | Mukaan tulee alihankintarivin kokonaissumma verot mukaan lukien. |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
