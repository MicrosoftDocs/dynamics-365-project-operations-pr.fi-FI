---
title: Kululuokkien toimittajan laskurivit
description: Tässä aiheessa kerrotaan, miten toimittajan laskurivit tallennetaan kululuokkiin.
author: rumant
ms.date: 03/25/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 209460680c9e5c2e39f98ba5c48aa18992775db1
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/14/2022
ms.locfileid: "8579532"
---
# <a name="vendor-invoice-lines-for-expense-categories"></a>Kululuokkien toimittajan laskurivit

[!include [banner](../../includes/dataverse-preview.md)]

_**Käytetään:** Lite-käyttöönotto – kauppa proformalaskutukseen_

Microsoft Dynamics 365 Project Operationsissa toimittajan laskussa voi olla toimittajan laskurivejä kululuokkia varten. Projektipäälliköt voivat kirjata kululuokkiin toimittajan laskurivien avulla kululuokiksi hankittujen palvelujen kustannukset.

Kululuokkien toimittajan laskurivit voivat viitata kululuokkien alihankkijariviin tai sitten ei. Jos kululuokkien toimittajan laskurivi viittaa alihankkijaan, projektipäälliköt voivat yhdistää ja tarkistaa kulut, joita toimittajan laskurivi laskuttaa kuluille, jotka on tallennettu näihin kululuokkiin ja jotka projektipäälliköt ovat hyväksyneet projektiin.

Seuraavassa taulukossa on tietoja kululuokkien toimittajan laskurivien kentistä.

| Field | Description | Toiminnallinen vaikutus |
| --- | --- | --- |
| Name | Toimittajan laskurivin nimi tunnistamisen helpottamiseksi. | Tämä nimi näkyy kaikkien toimittajan laskuriveihin perustuvien valintojen ensimmäisenä sarakkeena. |
| Description | Lyhyt kuvaus palveluista, joita toimittaja laskuttaa toimittajan laskurivillä. | Ei mikään |
| Alihankinta | Alihankinta, jossa palvelut tilattiin alun perin. | Kun toimittajan laskulle valitaan alihankinta, kaikki toimittajan laskurivit perivät tämän valinnan. Toimittajan laskussa ei voi olla toimittajan laskurivejä, jotka viittaavat eri alihankintoihin. |
| Alihankintarivi | Alihankintarivi, jossa palvelut tilattiin alun perin. Valittavissa olevien alihankintarivien luettelo rajoittuu valitun alihankkijan riveihin. | Kun toimittajan laskurivillä valitaan kululuokille alihankkijarivi, **projekti**-, **tehtävä**- ja **tapahtumaluokka**-kenttien oletusarvot syötetään alihankkijarivin vastaavista kentistä. Jos valitulla alihankkijarivillä on arvoja **Projekti**-, **Projektitehtävä**- ja **Tapahtumaluokka**-kentissä, toimittajan laskurivin vastaavien kenttien arvot eivät voi erota näistä arvoista. |
| Tapahtuman päivä | Päivämäärä, jona toimittajan laskurivin todellinen kustannus kirjataan projektiin. |Ei mikään |
| Tapahtumaluokka | Valitse **Kulu**, jos haluat kirjata toimittajan laskun kululuokkaa varten. | Arvo **Kulu** ilmaisee, että toimittajan laskun riviä käytetään kirjaamaan kululuokkina hankituille palveluille laskun summan. |
| Project | Sen projektin nimi, jossa laskutettavat palvelut on käytetty. | Tämä kenttä on pakollinen, eikä sitä voi jättää tyhjäksi. |
| Tehtävä | Sen projektitehtävän nimi, jossa laskutettavat palvelut on käytetty. Tämä kenttä on käytettävissä vain, jos projekti on valittu. Projektitehtävän valinta on valinnainen. | Jos tämä kenttä jätetään tyhjäksi, projektipäällikkö voi yhdistää toimittajan laskurivin kuluihin, jotka on tallennettu mihin tahansa projektin tehtävään. Jos toimittajan laskurivillä ei ole viittausta alihankkijariviin ja tämä kenttä jätetään tyhjäksi, toimittajan laskurivin luomaa kustannusta ei linkitetä laskuttamattoman myynnin toteutuneisiin arvoihin. Tässä tapauksessa jos tehtäväpohjainen laskutus on määritetty, kustannuksia ei ehkä voi laskuttaa loppuasiakkaalta. |
| Tapahtumaluokka | Laskutettava tapahtumaluokka. Valitulle tapahtumaluokalle on luotava vastaava kululuokka. | **Tapahtumaluokka**- ja **Yksikkö**-arvojen yhdistelmää käytetään toimittajan laskurivin **yksikköhinnan** oletusarvona tai laskettuna arvona. |
| Määrä | Kirjoita määrä, jonka toimittaja laskuttaa laskurivillä. |Ei mikään|
| Yksikköryhmä | Oletusarvon syöttö perustuu valitun tapahtumaluokan yksikköryhmään. | Ei mikään |
| Yksikkö | Oletusarvo on valitun yksikköryhmän perusyksikkö. Voit muuttaa tätä arvoa, jos haluat ostaa minkä tahansa yksikköryhmän yksikön. | **Tapahtumaluokka**- ja **Yksikkö**-arvojen yhdistelmää käytetään toimittajan laskurivin **yksikköhinnan** oletusarvona tai laskettuna arvona. |
| Yksikköhinta | Oletusyksikköhinta käyttää projektihintaluettelon **Tapahtumaluokka**- ja **Yksikkö**-arvojen yhdistelmää, jota käytetään toimittajan laskurivin tapahtumapäivämäärään. | Jos soveltuvan projektihinnaston hinta on määritetty yksikköön, joka eroaa toimittajan laskurivin yksiköstä, järjestelmä laskee yksikköhinnan yksikkömuunnoksen avulla. |
| Välisumma | Tämä on vain luku -kenttä, joka lasketaan muodossa *määrä* &times; *yksikköhinta*, jos sekä **määrä**- että **yksikköhinta**-arvot on syötetty. Jos jompikumpi tai molemmat kentät ovat tyhjiä, voit syöttää tähän kenttään arvon.| Ei mikään |
| Arvonlisävero | Anna arvonlisäveron summa. | Ei mikään |
| Loppusumma | Toimittajan laskurivin kokonaissumma verot mukaan lukien. Tämä kenttä lasketaan muodossa *välisumma*  +  *arvonlisävero*. | Ei mikään |

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
