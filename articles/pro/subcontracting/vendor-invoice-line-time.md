---
title: Toimittajan laskurivit ajalle
description: Tässä artikkelissa käsitellään alihankkijoiden syöttämien aikakustannusten kirjaamista toimittajan laskuriveille.
author: rumant
ms.date: 03/15/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 0b81d2884580e9054457906627c1f9101f435524
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8927538"
---
# <a name="vendor-invoice-lines-for-time"></a>Toimittajan laskurivit ajalle

[!include [banner](../../includes/dataverse-preview.md)]

_**Käytetään:** Lite-käyttöönotto – kauppa proformalaskutukseen_

Microsoft Dynamics 365 Project Operationsissa toimittajan laskussa voi olla toimittajan laskurivejä aikaa varten. Projektipäälliköt voivat kirjata projektien alihankkijoiden ajan kustannukset toimittajan aikalaskurivien avulla.

Toimittajan aikalaskurivit voivat viitata ajan alihankkijariviin tai sitten ei. Jos toimittajan aikalaskurivi viittaa alihankintasopimukseen, projektipäälliköt voivat yhdistää ja tarkistaa ajat, joita toimittajan laskurivi laskuttaa ostettujen alihankkijoiden ajan käytölle ja jotka projektipäälliköt ovat hyväksyneet projektille.

Seuraavassa taulukossa on tietoja toimittajan aikalaskurivien kentistä.

| Field | Description | Toiminnallinen vaikutus |
| --- | --- | --- |
| Name | Toimittajan laskurivin nimi tunnistamisen helpottamiseksi. | Tämä nimi näkyy kaikkien toimittajan laskuriveihin perustuvien valintojen ensimmäisenä sarakkeena. |
| Description | Lyhyt kuvaus palveluista, joita toimittaja laskuttaa toimittajan laskurivillä. | Ei mikään |
| Alihankinta | Alihankinta, jossa palvelut tilattiin alun perin. | Kun toimittajan laskulle valitaan alihankinta, kaikki toimittajan laskurivit perivät tämän valinnan. Toimittajan laskussa ei voi olla toimittajan laskurivejä, jotka viittaavat eri alihankintoihin. |
| Alihankintarivi | Alihankintarivi, jossa palvelut tilattiin alun perin. Valittavissa olevien alihankintarivien luettelo rajoittuu valitun alihankkijan riveihin. | Kun toimittajan laskurivillä valitaan ajalle alihankkijarivi, **projekti**-, **rooli**- ja **varattavissa oleva resurssi**-kenttien oletusarvot syötetään alihankkijarivin vastaavista kentistä. Jos valitulla alihankkijarivillä on arvoja **Projekti**-, **Rooli**- ja **Varattava**-kentissä, toimittajan laskurivin vastaavien kenttien arvot eivät voi erota näistä arvoista. |
| Tapahtuman päivä | Päivämäärä, jona toimittajan laskurivin todellinen kustannus kirjataan projektiin. | Ei mikään |
| Tapahtumaluokka | Oletusarvo on **Aika**. | Arvo **Aika** ilmaisee, että toimittajan laskun riviä käytetään kirjaamaan alihankkijan ajan laskun summan. |
| Project | Sen projektin nimi, jossa laskutettavat palvelut on käytetty. | Tämä kenttä on pakollinen, eikä sitä voi jättää tyhjäksi. |
| Tehtävä | Sen projektitehtävän nimi, jossa laskutettavat palvelut on käytetty. Tämä kenttä on käytettävissä vain, jos projekti on valittu. Projektitehtävän valinta on valinnainen. | Jos tämä kenttä jätetään tyhjäksi, projektipäällikkö voi yhdistää toimittajan laskurivin alihankkijan resurssien kirjaamaan aikaan, jota on käytetty mihin tahansa projektin tehtävään. Jos toimittajan laskurivillä ei ole viittausta alihankkijariviin ja tämä kenttä jätetään tyhjäksi, toimittajan laskurivin luomaa kustannusta ei linkitetä laskuttamattoman myynnin toteutuneisiin arvoihin. Tässä tapauksessa jos tehtäväpohjainen laskutus on määritetty, kustannuksia ei ehkä voi laskuttaa loppuasiakkaalta. |
| Rooli | Niiden alihankinnan resurssien rooli, joiden aikaa laskutetaan. | Tämä kenttä määrittää roolin, joka suoritetaan alihankkijaresursseilla, joiden aika laskutetaan toimittajan laskussa. |
| Varattavissa oleva resurssi | Sen alihankkijan nimi, jonka aikaa laskutetaan. Varattavissa olevan resurssin valinta on valinnainen. | Jos tämä kenttä jätetään tyhjäksi, projektipäällikkö voi yhdistää toimittajan laskurivin sen resurssien kirjaamaan aikaan, joka kuuluu toimittajaan toimittajan laskurivillä. |
| Määrä | Anna aika tunteina, jotka toimittaja laskuttaa laskurivillä. |Ei mikään |
| Yksikköryhmä | Oletusarvo on **Aika-yksikköryhmä**, eikä sitä voi muuttaa. | Ei mikään |
| Yksikkö | Oletusarvo on tuntien perusyksikkö kohteesta Aika-yksikköryhmä. Voit muuttaa tätä arvoa, jos haluat ostaa minkä tahansa Aika-yksikköryhmä-yksikön, kuten päivän tai viikon. | **Rooli**- ja **Yksikkö**-arvojen yhdistelmää käytetään toimittajan laskurivin **yksikköhinnan** oletusarvona tai laskettuna arvona. |
| Yksikköhinta | Oletusyksikköhinta käyttää projektihintaluettelon **Rooli**- ja **Yksikkö**-arvojen yhdistelmää, jota käytetään toimittajan laskurivin tapahtumapäivämäärään. | Jos soveltuvan projektihinnaston hinta on määritetty yksikköön, joka eroaa toimittajan laskurivin yksiköstä, järjestelmä laskee yksikköhinnan yksikkömuunnoksen avulla. |
| Välisumma | Tämä on vain luku -kenttä, joka lasketaan muodossa *määrä* &times; *yksikköhinta*, jos sekä **määrä**- että **yksikköhinta**-arvot on syötetty. Jos jompikumpi tai molemmat kentät ovat tyhjiä, voit syöttää tähän kenttään arvon. | Ei mikään |
| Arvonlisävero | Anna arvonlisäveron summa. | Ei mikään |
| Loppusumma | Toimittajan laskurivin kokonaissumma verot mukaan lukien. Tämä kenttä lasketaan muodossa *välisumma*  +  *arvonlisävero*. | Ei mikään |

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
