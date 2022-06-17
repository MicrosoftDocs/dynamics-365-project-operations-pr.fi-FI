---
title: Toimittajan laskurivit tuotteille
description: Tässä artikkelissa käsitellään sitä,, miten toimittajan laskurivit voidaan kirjata tuotteille ja kirjata tuoteostot toimittajilta eri kenttiin.
author: rumant
ms.date: 03/25/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 206dd36a1a1e7141678da27d76a99561ac89044b
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8931372"
---
# <a name="vendor-invoice-lines-for-products"></a>Toimittajan laskurivit tuotteille

[!include [banner](../../includes/dataverse-preview.md)]

_**Käytetään:** Lite-käyttöönotto – kauppa proformalaskutukseen_

Microsoft Dynamics 365 Project Operationsin toimittajan laskussa voi olla toimittajan laskurivejä tuotteille (joita kutsutaan myös materiaaleiksi). Projektipäälliköt voivat kirjata projekteissa ostettujen tuotteiden kustannukset toimittajan tuotelaskurivien avulla.

Toimittajan tuotelaskurivit voivat viitata materiaalien alihankkijariviin tai sitten ei. Jos toimittajan tuotelaskurivi viittaa alihankintasopimukseen, projektipäälliköt voivat yhdistää ja tarkistaa tuotteet, joita toimittajan laskurivi laskuttaa ostettujen tuotteiden käytölle ja jotka projektipäälliköt ovat hyväksyneet.

Seuraavassa taulukossa on tietoja toimittajan tuotelaskurivien kentistä.

| Field | Description | Toiminnallinen vaikutus |
| --- | --- | --- |
| Name | Toimittajan laskurivin nimi tunnistamisen helpottamiseksi. | Tämä nimi näkyy kaikkien toimittajan laskuriveihin perustuvien valintojen ensimmäisenä sarakkeena. |
| Description | Lyhyt kuvaus tuotteista, joita toimittaja laskuttaa toimittajan laskurivillä. | Ei mikään |
| Alihankinta | Alihankintasopimus, jossa tuotteet tilattiin alun perin. | Kun toimittajan laskulle valitaan alihankinta, kaikki toimittajan laskurivit perivät tämän valinnan. Toimittajan laskussa ei voi olla toimittajan laskurivejä, jotka viittaavat eri alihankintoihin. |
| Alihankintasopimusrivi | Alihankintasopimusrivi, jossa tuotteet tilattiin alun perin. Valittavissa olevien alihankintarivien luettelo rajoittuu valitun alihankkijan riveihin. | Kun toimittajan laskurivillä valitaan tuotteille alihankintasopimusrivi, **projekti**-, **tehtävä**- ja **tuote**-kenttien oletusarvot syötetään alihankkijarivin vastaavista kentistä. Jos valitulla alihankkijarivillä on arvoja **Projekti**-, **Tehtävä**- ja **Tuote**-kentissä, toimittajan laskurivin vastaavien kenttien arvot eivät voi erota näistä arvoista. |
| Tapahtuman päivä | Päivämäärä, jona toimittajan laskurivin todellinen kustannus kirjataan projektiin. | Ei mikään|
| Tapahtumaluokka | Kun tuotteita laskutetaan, tämän kentän arvoksi tulee määrittää **Materiaali**. | Arvo **Materiaali** ilmaisee, että toimittajan laskun riviä käytetään kirjaamaan ostetuille tuotteille laskun summan. |
| Project | Sen projektin nimi, jossa laskutettavat tuotteet on käytetty. | Tämä kenttä on pakollinen, eikä sitä voi jättää tyhjäksi. |
| Tehtävä | Sen projektitehtävän nimi, jossa laskutettavat tuotteet on käytetty. Tämä kenttä on käytettävissä vain, jos projekti on valittu. Projektitehtävän valinta on valinnainen. | Jos tämä kenttä jätetään tyhjäksi, projektipäällikkö voi yhdistää toimittajan laskurivin ostettuun tuotteeseen, jota on käytetty mihin tahansa projektin tehtävään. Jos toimittajan laskurivillä ei ole viittausta alihankkijariviin ja tämä kenttä jätetään tyhjäksi, toimittajan laskurivin luomaa kustannusta ei linkitetä laskuttamattoman myynnin toteutuneisiin arvoihin. Tässä tapauksessa jos tehtäväpohjainen laskutus on määritetty, kustannuksia ei voi laskuttaa loppuasiakkaalta. |
| Valitse tuote | Valitse, onko laskutettava tuote tuoteluettelossa vai onko se käsin lisätty tuote. | Oletusarvo kirjoitetaan alihankkijariviltä, kun alihankkijarivi valitaan. |
| Tuote | Valitse tuote luettelosta. Jos tuote on käsin lisätty tuote, anna tuotteen nimi. | Tähän kenttään kirjoitettaan nykyisten tuotteiden oletusostohinnat. |
| Määrä | Kirjoita materiaalin määrä, jonka toimittaja laskuttaa tällä laskurivillä. | Ei mikään |
| Yksikköryhmä | Valitse sen yksikön yksikköryhmä, jossa laskutettava määrä ilmaistaan. | Ei mikään |
| Yksikkö | Oletusarvo on valitun yksikköryhmän perusyksikkö. Voit muuttaa tätä arvoa, jos haluat maksaa valitun yksikköryhmän missä tahansa yksikössä. | **Tuote**- ja **Yksikkö**-arvojen yhdistelmää käytetään toimittajan laskurivin **yksikköhinnan** oletusarvona tai laskettuna arvona. |
| Yksikköhinta | Oletusyksikköhinta käyttää projektihintaluettelon **Tuote**- ja **Yksikkö**-arvojen yhdistelmää, jota käytetään toimittajan laskurivin tapahtumapäivämäärään. | Ei mikään |
| Välisumma | Tämä on vain luku -kenttä, joka lasketaan muodossa *määrä* &times; *yksikköhinta*, jos sekä **määrä**- että **yksikköhinta**-arvot on syötetty. Jos jompikumpi tai molemmat kentät ovat tyhjiä, voit syöttää tähän kenttään arvon. | Ei mikään |
| Arvonlisävero | Anna arvonlisäveron summa. | Ei mikään |
| Loppusumma | Toimittajan laskurivin kokonaissumma verot mukaan lukien. Tämä kenttä lasketaan muodossa *välisumma*  +  *arvonlisävero*. | Ei mikään |

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
