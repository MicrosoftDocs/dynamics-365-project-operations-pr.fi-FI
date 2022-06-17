---
title: Projektipohjaisten sopimusrivien käyttäminen
description: Tässä artikkelissa on tietoja projektipohjaisista sopimusriveistä.
author: rumant
ms.date: 10/28/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 055c34c96eec0f4eee1b8e17d989d22c4752787d
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8931970"
---
# <a name="work-with-projectbased-contract-lines"></a>Projektipohjaisten sopimusrivien käyttäminen

Dynamics 365 Project Operationsin projektipohjaiset sopimusrivit on suunniteltu sisältämään sitoumuksen projektityön tiettyjen komponenttien arvio- ja laskutussopimukset. Projektipohjaisen sopimusrivin rakenne on laajennettu projektin arviointi- ja laskutusskenaarioihin seuraavien käsitteiden avulla:

- Laskutustapa
- Projektin ja tehtävän yhdistäminen
- Sisältyvät tapahtumaluokat
- Ei-ylitettävä rajoitus
- Veloitettavuusasetus
- Sopimusrivin tietoja käyttävät arviot
- Sopimusrivin asiakkaat

Projektipohjaisten sopimusrivien **Yleiset**-välilehdessä on seuraavat kentät. Näiden kenttien avulla voidaan määrittää tarkka ja perusteellinen pohja projektipohjaisen työn arvio- ja laskutussopimuksille.

| Field | Kuvaus | Loppupään vaikutus |
| --- | --- | --- |
| **Nimi** | Sen sopimusrivin nimi, joka määrittää sopimuksen arvioitavan komponentin. Jos projektisopimus on luotu tarjouksesta, tämä arvo kopioidaan vastaavasta projektipohjaisen tarjousrivin arvosta. | Tämän kentän arvo kopioidaan tältä projektiriviltä luodulle projektin laskuriville, kun lasku luodaan. |
| **Laskutustapa** | Jos projektisopimus on luotu tarjouksesta, tämä arvo kopioidaan vastaavasta tarjousrivin kentästä. Tämä asetusjoukko ilmaisee kaksi tärkeintä Project Operationsin tukemaa sopimusmallia:</br>- **Kiinteä hinta**</br>- **Aika ja materiaalit** | Varsinainen tapahtuma käsitellään viitatun sopimusrivin laskutustavan perusteella. Jos sen sopimusrivin, johon todellinen arvo viittaa, laskutustapana on aika ja materiaali, kustannus ja laskuttamaton todellisen myynnin tietue luodaan. Jos sen sopimusrivin, johon todellinen arvo viittaa, laskutustapa on kiinteä hinta, vain todellinen kustannus luodaan. |
| **Project** | Tämän kentän avulla voi määrittää projektin, jonka avulla toimitetaan tämän sitoumuksen työ. | Tämän kentän arvoa käytetään yhdessä **Sisällytettävät tehtävät**- ja **Sisällytettävät tapahtumaluokat** -kenttien kanssa selvittämään sopimusriviviittaus todellisen arvon tai arvion rivitietueessa. |
| **Sisällytä aika** | Merkintä ilmaisee, sisältääkö tämä sopimusrivi valitun projekti aikatapahtumat tai työkustannukset. **Ei**-arvo ilmaisee, että aikatapahtumia tai työkustannuksia ei sisällytetä sopimusriville. **Kyllä**-arvo ilmaisee, että ne sisällytetään. | Tämän kentän arvoa käytetään yhdessä projektin kanssa selvittämään sopimusriviviittaus todellisen arvon tai arvion rivitietueessa. |
| **Sisällytä kulu** | Merkintä ilmaisee, sisällytetäänkö valitun projekti kulukustannukset tälle sopimusriville. **Ei**-arvo ilmaisee, että kulukustannuksia ei sisällytetä sopimusriville. **Kyllä**-arvo ilmaisee, että se sisällytetään. | Tämän kentän arvoa käytetään yhdessä projektin kanssa selvittämään sopimusriviviittaus todellisen arvon tai arvion rivitietueessa. |
| **Sisällytä maksu** | Merkintä ilmaisee, sisällytetäänkö valitun projekti maksut tälle sopimusriville. **Ei**-arvo ilmaisee, että maksuja ei sisällytetä sopimusriville. **Kyllä**-arvo ilmaisee, että ne sisällytetään. | Tämän kentän arvoa käytetään yhdessä projektin kanssa selvittämään sopimusriviviittaus todellisen arvon tai arvion rivitietueessa. |
| **Palvelusopimuksen summa** | Kiinteähintaisella sopimusrivillä tämä on sovittu arvo, joka asiakkaalle laskutetaan kaikesta tähän sopimusriviin liitetyistä työkomponenteista. Ajan ja materiaalin sopimusrivillä tämä summa on arvio siitä, mitä asiakkaalle laskutetaan kaikesta tähän sopimusriviin liitetyistä työkomponenteista. Jos projektisopimus on luotu tarjouksesta, tämä arvo kopioidaan vastaavan tarjousrivin kentästä. Jos projektipohjaisella sopimusrivillä on tietoja, kenttä on lukittu eikä sitä voi muokata ja sen arvo saadaan sopimusrivin tietojen summasta. | Jos sopimusrivillä on rivitietoja, tätä arvoa voi muokata muuttamalla rivitietojen summia. Kiinteähintaisella sopimusrivillä tämän arvon avulla luodaan summa ennen veroja säännöllisinä välitavoitteiden laskutusajankohtina. |
| **Arvioitu vero** | Käyttäjä voi muokata tätä kenttää antamalla arvioidun verosumman sopimusrivillä. Jos projektipohjaisella sopimusrivillä on tietoja, kenttä on lukittu eikä sitä voi muokata ja sen arvo saadaan sopimusrivin tietojen verosummasta. | Jos sopimusrivillä on rivitietoja, tätä arvoa voi muokata muuttamalla rivitietojen verosummia. Kiinteähintaisella sopimusrivillä tämän arvon avulla luodaan vero säännöllisinä välitavoitteiden laskutusajankohtina. |
| **Palvelusopimuksen summa veron jälkeen** | Sopimusrivin summa veron jälkeen. Tämä kenttä on vain luku -muotoinen, ja se lasketaan kaavalla **Palvelusopimuksen summa + Vero**. | Kiinteähintaisella sopimusrivillä tämän arvon avulla luodaan säännölliset välitavoitteiden laskutukset. |
| **Ei-ylitettävä rajoitus** | Käyttäjä voi muokata tätä kenttää, ja se on käytettävissä vain niissä projektipohjaisilla sopimusriveillä, joissa on laskutustapana aika ja materiaali. | Käyttäjä voi muokata tätä kenttää. Kun ajan tai kulun todellinen arvo käyttää viittauksen tämän sopimusrivin aikaa ja materiaalia, todellisen arvon summaa verrataan tämän sopimusrivin ei-ylitettävään rajoitukseen sen jälkeen, kun jo kulutetut ja varatut summat on otettu huomioon. |
| **Asiakasbudjetti** | Tätä kenttää voi muokata ja se kopioidaan tarjousrivin vastaavasta kentästä, jos palvelusopimus on luotu tarjouksesta. | Tämä kenttä on tarkoitettu vain tiedoksi eikä se vaikuta muihin toimintoihin. |

## <a name="validation-rule-for-the-options-on-the-general-tab-of-project-based-contract-lines"></a>Projektipohjaisten sopimusrivien Yleiset-välilehden asetusten vahvistussääntö

Sääntö: projekti ja tietty tapahtumaluokka voidaan sisällyttää vain yhdelle sopimuksen projektipohjaiselle sopimusriville.

| Sopimus | Palvelusopimuksen rivi | Project | Sisällytä aika | Sisällytä kulu | Sisällytä maksu | Kelpaa / ei kelpaa | Syy                                                                                                                                                                                                  |
|----------|---------------|---------|--------------|-----------------|-------------|-----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| S1       | SR1           | K1      | Kyllä          | Kyllä             | Kyllä         | Ei kelpaa       | Rikkoo sääntöä. Projektin P1 aika, kulu ja maksut sisältyvät kummallekin sopimusriville SR1 ja SR2.                                                                                       |
| S1       | SR2           | K1      | Kyllä          | Kyllä             | Kyllä         | Ei kelpaa       | Rikkoo sääntöä. Projektin P1 aika, kulu ja maksut sisältyvät kummallekin sopimusriville SR1 ja SR2.                                                                                       |
| S1       | SR1           | K1      | Kyllä          | No              | Kyllä         | Ei kelpaa       | Rikkoo sääntöä. Projektin P1 aika ja maksut sisältyvät kummallekin sopimusriville SR1 ja SR2.                                                                                                   |
| S1       | SR2           | K1      | Kyllä          | Kyllä             | Kyllä         | Ei kelpaa       | Rikkoo sääntöä. Projektin P1 aika ja maksut sisältyvät kummallekin sopimusriville SR1 ja SR2.                                                                                                   |
| S1       | SR1           | K1      | Kyllä          | No              | Kyllä         | Kelvollinen           | SR1 sisältää projektin P1 ajan ja maksut. SR2 sisältää projektin P1 kulun. </br>   Siinä, mitä kummallekin sopimusriville sisällytetään, ei ole päällekkäisyyttä, joten kelpaa.  |
| S1       | SR2           | K1      | No           | Kyllä             | No          | Kelvollinen           | SR1 sisältää projektin P1 ajan ja maksut. SR2 sisältää projektin P1 kulun. </br>   Siinä, mitä kummallekin sopimusriville sisällytetään, ei ole päällekkäisyyttä, joten kelpaa.  |
| S1       | SR1           | K1      | Kyllä          | Kyllä             | Kyllä         | Ei kelpaa       | Rikkoo sääntöä. Projektin P1 aika, kulu ja maksut sisältyvät kahden sopimuksen riveille.                                                                                               |
| SR2      | SR2           | K1      | Kyllä          | Kyllä             | Kyllä         | Ei kelpaa       | Rikkoo sääntöä. Projektin P1 aika, kulu ja maksut sisältyvät kahden sopimuksen riveille.                                                                                               |


[!INCLUDE[footer-include](../includes/footer-banner.md)]