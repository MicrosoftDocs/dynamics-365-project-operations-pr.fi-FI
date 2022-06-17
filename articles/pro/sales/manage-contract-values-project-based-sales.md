---
title: Projektipohjaisten sopimusrivien yleiskatsaus
description: Tässä artikkelissa on tietoja projektipohjaisten sopimusrivien käyttämisestä.
author: rumant
ms.date: 10/28/2020
ms.topic: overview
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: d32edac6537a4b0f51e9d2f72cb4a7342606d2c5
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8931418"
---
# <a name="project-based-contract-lines-overview"></a>Projektipohjaisten sopimusrivien yleiskatsaus

_**Koskee:** Project Operationsin resurssiin / muuhun kuin resurssiin perustuvia skenaarioita, Lite-käyttöönotto-kaupasta proformalaskutukseen_

Dynamics 365 Project Operationsin projektipohjaiset sopimusrivit on suunniteltu sisältämään sitoumuksen projektityön tiettyjen komponenttien arvio- ja laskutussopimukset. Projektipohjaisen sopimusrivin rakenne on laajennettu projektin arviointi- ja laskutusskenaarioihin seuraavien käsitteiden avulla:

- Laskutustapa
- Projektin ja tehtävän yhdistäminen
- Sisältyvät tapahtumaluokat
- Ei-ylitettävä rajoitus
- Veloitettavuusasetus
- Sopimusrivin tietoja käyttävät arviot
- Sopimusrivin asiakkaat

Seuraavassa taulukossa on projektipohjaisten sopimusrivien **Yleiset**-välilehden kenttiä, joilla määritetään tarkka ja perusteellinen pohja projektipohjaisen työn arvio- ja laskutussopimuksille.

| Field | Kuvaus | Loppupään vaikutus |
| --- | --- | --- |
| **Nimi** | Sopimusrivin nimi. Se määrittää sopimuksen arvioitavan komponentin. Jos projektisopimus on luotu tarjouksesta, tämä arvo kopioidaan vastaavasta projektipohjaisen tarjousrivin arvosta. | Nimi kopioidaan tältä sopimusriviltä luodulle projektin laskuriville, kun lasku luodaan. |
| **Laskutustapa** | Jos projektisopimus on luotu tarjouksesta, tämä arvo kopioidaan vastaavasta tarjousrivin kentästä. Tämä asetusjoukko ilmaisee kaksi tärkeintä Project Operationsin tukemaa sopimusmallia:</br>- **Kiinteä hinta**</br>- **Aika ja materiaalit** | Varsinainen tapahtuma käsitellään viitatun sopimusrivin laskutustavan perusteella. Jos sen sopimusrivin, johon todellinen arvo viittaa, laskutustapana on aika ja materiaali, kustannusten ja laskuttamaton todellisen myynnin tietueet luodaan. Jos sen sopimusrivin, johon todellinen arvo viittaa, laskutustapa on kiinteä hinta, vain todellinen kustannus luodaan. |
| **Project** | Tämän kentän avulla voi määrittää projektin, jonka avulla toimitetaan tämän sitoumuksen työ. | Arvoa käytetään yhdessä **Sisällytetyt tehtävät** - ja **Sisällytetyt tapahtumaluokat** -arvojen kanssa, kun sopimusriviviittaus ratkaistaan toteutuneiden tai arviorivitietueiden perusteella. |
| **Sisällytettävät tehtävät** | Ilmaisee, sisältääkö tämä sopimusrivi valitun projektin kaikki projektitehtävät vai vain tehtävien alijoukon. Tällä asetusjoukolla on seuraavat mahdolliset arvot:</br>- **Kaikki projektitehtävät**</br>- **Vain valitut projektitehtävät**. Tyhjä arvo tässä kentässä vastaa vaihtoehdon **Kaikki projektitehtävät** valintaa. | Jos **Vain valitut tehtävät** valitaan, voi valita tietyt tehtävät ja liittää ne tähän sopimusriviin **Projekti**-sivun **Tehtävän laskutuksen asetukset** -välilehdessä. Tätä arvoa käytetään yhdessä **Projekti**- ja **Sisällytettävät tapahtumaluokat** -luokkien kanssa selvittämään sopimusriviviittaus todellisen arvon tai arvion rivitietueessa. |
| **Sisällytä aika** | **Kyllä**/**Ei** -arvo ilmaisee, sisällytetäänkö valitun projektin aikatapahtumat tai työvoimakustannukset tähän sopimusriviin. **Ei**-arvo ilmaisee, että aikatapahtumia tai työkustannuksia ei sisällytetä sopimusriville. **Kyllä**-arvo ilmaisee, että ne sisällytetään. | Tätä arvoa käytetään yhdessä projektin kanssa, kun palvelusopimusrivin viittaus ratkaistaan toteutuneita tai arviorivitietueita varten. |
| **Sisällytä kulu** | **Kyllä**/**Ei** -arvo ilmaisee, sisällytetäänkö valitun projektin kulutapahtumat tähän sopimusriviin. **Ei**-arvo ilmaisee, että kulukustannuksia ei sisällytetä sopimusriville. **Kyllä**-arvo ilmaisee, että se sisällytetään. | Tätä arvoa käytetään yhdessä projektin kanssa, kun palvelusopimusrivin viittaus ratkaistaan toteutuneita tai arviorivitietueita varten. |
| **Sisällytä materiaalit** | **Kyllä**/**Ei** -arvo ilmaisee, sisällytetäänkö valitun projektin materiaalikustannukset tähän sopimusriviin. **Ei**-arvo ilmaisee, että materiaalikustannuksia ei sisällytetä tähän sopimusriviin. **Kyllä**-arvo ilmaisee, että se sisällytetään. | Tätä arvoa käytetään yhdessä projektin kanssa, kun palvelusopimusrivin viittaus ratkaistaan toteutuneita tai arviorivitietueita varten. |
| **Sisällytä maksu** | **Kyllä**/**Ei** -arvo ilmaisee, sisällytetäänkö valitun projektin maksut tähän sopimusriviin. **Ei**-arvo ilmaisee, että maksuja ei sisällytetä sopimusriville. **Kyllä**-arvo ilmaisee, että ne sisällytetään. | Tätä arvoa käytetään yhdessä projektin kanssa, kun palvelusopimusrivin viittaus ratkaistaan toteutuneita tai arviorivitietueita varten. |
| **Palvelusopimuksen summa** | Kiinteähintaisella sopimusrivillä tämä summa on sovittu arvo, joka asiakkaalle laskutetaan kaikesta tähän sopimusriviin liitetyistä työkomponenteista. Ajan ja materiaalin sopimusrivillä tämä summa on arvio siitä, mitä asiakkaalle laskutetaan kaikesta tähän sopimusriviin liitetyistä työkomponenteista. Jos projektisopimus on luotu tarjouksesta, tämä arvo kopioidaan vastaavan tarjousrivin kentästä. Jos projektipohjaisella sopimusrivillä on tietoja, kenttä on lukittu eikä sitä voi muokata ja sen arvo saadaan sopimusrivin tietojen summasta. | Jos sopimusrivillä on rivitietoja, tätä arvoa voi muokata muuttamalla rivitietojen summia. Kiinteähintaisella sopimusrivillä tämän arvon avulla luodaan summa ennen veroja säännöllisinä välitavoitteiden laskutusajankohtina. |
| **Arvioitu vero** | Käyttäjä voi muokata tätä kenttää antamalla arvioidun verosumman sopimusrivillä. Jos projektipohjaisella sopimusrivillä on tietoja, kenttä on lukittu eikä sitä voi muokata ja sen arvo saadaan sopimusrivin tietojen verosummasta. | Jos sopimusrivillä on rivitietoja, tätä arvoa voi muokata muuttamalla rivitietojen verosummia. Kiinteähintaisella sopimusrivillä tämän arvon avulla luodaan vero säännöllisinä välitavoitteiden laskutusajankohtina. |
| **Palvelusopimuksen summa veron jälkeen** | Sopimusrivin summa veron jälkeen. Tämä kenttä on vain luku -muotoinen, ja se lasketaan kaavalla **Palvelusopimuksen summa + Vero**. | Kiinteähintaisella sopimusrivillä tämän arvon avulla luodaan säännölliset välitavoitteiden laskutukset. |
| **Ei-ylitettävä rajoitus** | Käyttäjä voi muokata tätä kenttää, ja se on käytettävissä vain niillä projektipohjaisilla sopimusriveillä, joissa on laskutustavaksi on määritetty aika ja materiaali. | Käyttäjä voi muokata tätä kenttää. Kun ajan tai materiaalin todellinen arvo käyttää viittauksena tämän sopimusrivin aikaa ja materiaalia, todellisen arvon summaa verrataan tämän sopimusrivin ei-ylitettävään rajoitukseen sopimusrivillä. Tämä arviointi on valmis, kun jo käytetyt ja varatut summat on otettu huomioon. |
| **Asiakasbudjetti** | Tätä kenttää voi muokata ja se kopioidaan tarjousrivin vastaavasta kentästä, jos palvelusopimus on luotu tarjouksesta. | Tämä kenttä on tarkoitettu vain tiedoksi eikä se vaikuta muihin toimintoihin. |

## <a name="validation-rules-for-the-options-on-the-general-tab-of-project-based-contract-lines"></a>Projektipohjaisten sopimusrivien Yleiset-välilehden asetusten vahvistussäännöt

Sääntö 1: jos **Sisällytettävät tehtävät** -kenttä on tyhjä tai sen määrityksenä on **Kaikki projektitehtävät**, kaikki projektin tehtävät sisällytetään sopimusrivillä.

Sääntö 2: jos **Sisällytettävät tehtävät** -kenttä on tyhjä tai sen määrityksenä on **Kaikki projektitehtävät**, projekti ja tietty tapahtumaluokka voidaan sisällyttää vain yhdelle sopimuksen projektipohjaiselle sopimusriville.

Sääntö 3: jos **Sisällytettävät tehtävät** -kenttä on tyhjä tai sen määrityksenä on **Vain valitut projektitehtävät**, projekti ja tietty tapahtumaluokka voidaan sisällyttää useille sopimuksen projektipohjaisille sopimusriveille.

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="43" valign="top">
                <p>
                    <strong>Sopimus</strong>
                </p>
            </td>
            <td width="65" valign="top">
                <p>
                    <strong>Palvelusopimuksen rivi</strong>
                </p>
            </td>
            <td width="42" valign="top">
                <p>
                    <strong>Project</strong>
                </p>
            </td>
            <td width="67" valign="top">
                <p>
                    <strong>Sisällytettävät tehtävät</strong>
                </p>
            </td>
            <td width="48" valign="top">
                <p>
                    <strong>Sisällytä aika</strong>
                </p>
            </td>
            <td width="48" valign="top">
                <p>
                    <strong>Sisällytä kulu</strong>
                </p>
            </td>
            <td width="42" valign="top">
                <p>
                    <strong>Sisällytä materiaalit</strong>
                </p>
            </td>
            <td width="42" valign="top">
                <p>
                    <strong>Sisällytä</strong>
                </p>
                <p>
                    <strong>Maksu</strong>
                </p>
            </td>
            <td width="53" valign="top">
                <p>
                    <strong>Kelpaa / ei kelpaa</strong>
                </p>
            </td>
            <td width="250" valign="top">
                <p>
                    <strong>Syy</strong>
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
S1 </p>
            </td>
            <td width="65" valign="top">
                <p>
SR1 </p>
            </td>
            <td width="42" valign="top">
                <p>
K1 </p>
            </td>
            <td width="67" valign="top">
                <p>
Tyhjä </p>
            </td>
            <td width="48" valign="top">
                <p>
Kyllä </p>
            </td>
            <td width="48" valign="top">
                <p>
Kyllä </p>
            </td>
            <td width="42" valign="top">
                <p>
Kyllä </p>
            </td>
            <td width="42" valign="top">
                <p>
Kyllä </p>
            </td>
            <td width="53" rowspan="2" valign="top">
                <p>
Ei kelpaa </p>
            </td>
            <td width="250" rowspan="2" valign="top">
                <p>
Säännön 2 rikkominen. P1-projektin aika, kulut, materiaalit ja maksut sisältyvät sekä sopimusriveille CL1 että CL2.
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
S1 </p>
            </td>
            <td width="65" valign="top">
                <p>
SR2 </p>
            </td>
            <td width="42" valign="top">
                <p>
K1 </p>
            </td>
            <td width="67" valign="top">
                <p>
Tyhjä </p>
            </td>
            <td width="48" valign="top">
                <p>
Kyllä </p>
            </td>
            <td width="48" valign="top">
                <p>
Kyllä </p>
            </td>
            <td width="42" valign="top">
                <p>
Kyllä </p>
            </td>
            <td width="42" valign="top">
                <p>
Kyllä </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
            </td>
            <td width="65" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="67" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="53" valign="top">
            </td>
            <td width="250" valign="top">
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
S1 </p>
            </td>
            <td width="65" valign="top">
                <p>
SR1 </p>
            </td>
            <td width="42" valign="top">
                <p>
K1 </p>
            </td>
            <td width="67" valign="top">
                <p>
Tyhjä </p>
            </td>
            <td width="48" valign="top">
                <p>
Kyllä </p>
            </td>
            <td width="48" valign="top">
                <p>
No </p>
            </td>
            <td width="42" valign="top">
                <p>
Kyllä </p>
            </td>
            <td width="42" valign="top">
                <p>
Kyllä </p>
            </td>
            <td width="53" rowspan="2" valign="top">
                <p>
Ei kelpaa </p>
            </td>
            <td width="250" rowspan="2" valign="top">
                <p>
Säännön 2 rikkominen. P1-projektin aika, materiaalit ja maksut sisältyvät sekä sopimusriveille CL1 että CL2.
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
S1 </p>
            </td>
            <td width="65" valign="top">
                <p>
SR2 </p>
            </td>
            <td width="42" valign="top">
                <p>
K1 </p>
            </td>
            <td width="67" valign="top">
                <p>
Tyhjä </p>
            </td>
            <td width="48" valign="top">
                <p>
Kyllä </p>
            </td>
            <td width="48" valign="top">
                <p>
Kyllä </p>
            </td>
            <td width="42" valign="top">
                <p>
Kyllä </p>
            </td>
            <td width="42" valign="top">
                <p>
Kyllä </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
            </td>
            <td width="65" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="67" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="53" valign="top">
            </td>
            <td width="250" valign="top">
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
S1 </p>
            </td>
            <td width="65" valign="top">
                <p>
SR1 </p>
            </td>
            <td width="42" valign="top">
                <p>
K1 </p>
            </td>
            <td width="67" valign="top">
                <p>
Tyhjä </p>
            </td>
            <td width="48" valign="top">
                <p>
Kyllä </p>
            </td>
            <td width="48" valign="top">
                <p>
No </p>
            </td>
            <td width="42" valign="top">
                <p>
Kyllä </p>
            </td>
            <td width="42" valign="top">
                <p>
Kyllä </p>
            </td>
            <td width="53" rowspan="2" valign="top">
                <p>
Kelvollinen </p>
            </td>
            <td width="250" rowspan="2" valign="top">
                <p>
P1-projektin aika, materiaalit ja maksut sisältyvät CL1:een.
                </p>
                <ul>
                    <li>
Kulu P1-projektissa sisältyy riville CL2.
                    </li>
                </ul>
                <p>
Sopimusriveillä ei ole päällekkäisyyksiä, joten ne ovat kelvollisia.
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
S1 </p>
            </td>
            <td width="65" valign="top">
                <p>
SR2 </p>
            </td>
            <td width="42" valign="top">
                <p>
K1 </p>
            </td>
            <td width="67" valign="top">
                <p>
Tyhjä </p>
            </td>
            <td width="48" valign="top">
                <p>
No </p>
            </td>
            <td width="48" valign="top">
                <p>
Kyllä </p>
            </td>
            <td width="42" valign="top">
                <p>
No </p>
            </td>
            <td width="42" valign="top">
                <p>
No </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
            </td>
            <td width="65" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="67" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="53" valign="top">
            </td>
            <td width="250" valign="top">
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
S1 </p>
            </td>
            <td width="65" valign="top">
                <p>
SR1 </p>
            </td>
            <td width="42" valign="top">
                <p>
K1 </p>
            </td>
            <td width="67" valign="top">
                <p>
Vain valitut tehtävät </p>
            </td>
            <td width="48" valign="top">
                <p>
Kyllä </p>
            </td>
            <td width="48" valign="top">
                <p>
Kyllä </p>
            </td>
            <td width="42" valign="top">
                <p>
Kyllä </p>
            </td>
            <td width="42" valign="top">
                <p>
Kyllä </p>
            </td>
            <td width="53" rowspan="2" valign="top">
                <p>
Ei kelpaa </p>
            </td>
            <td width="250" rowspan="2" valign="top">
                <p>
Rikkoo sääntöä 2 </p>
                <p>
C1 sisältää projektin P1 tehtävien alijoukon ajan, materiaalit, kulut ja maksut.
                </p>
                <p>
CL2 sisältää koko projektin P1 ajan, materiaalit, kulut ja maksut, joten se on päällekkäinen C1:n kanssa.
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
S1 </p>
            </td>
            <td width="65" valign="top">
                <p>
SR2 </p>
            </td>
            <td width="42" valign="top">
                <p>
K1 </p>
            </td>
            <td width="67" valign="top">
                <p>
Tyhjä </p>
            </td>
            <td width="48" valign="top">
                <p>
Kyllä </p>
            </td>
            <td width="48" valign="top">
                <p>
Kyllä </p>
            </td>
            <td width="42" valign="top">
                <p>
Kyllä </p>
            </td>
            <td width="42" valign="top">
                <p>
Kyllä </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
            </td>
            <td width="65" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="67" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="53" valign="top">
            </td>
            <td width="250" valign="top">
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
S1 </p>
            </td>
            <td width="65" valign="top">
                <p>
SR1 </p>
            </td>
            <td width="42" valign="top">
                <p>
K1 </p>
            </td>
            <td width="67" valign="top">
                <p>
Vain valitut tehtävät </p>
            </td>
            <td width="48" valign="top">
                <p>
Kyllä </p>
            </td>
            <td width="48" valign="top">
                <p>
Kyllä </p>
            </td>
            <td width="42" valign="top">
                <p>
Kyllä </p>
            </td>
            <td width="42" valign="top">
                <p>
Kyllä </p>
            </td>
            <td width="53" rowspan="2" valign="top">
                <p>
Kelvollinen </p>
            </td>
            <td width="250" rowspan="2" valign="top">
                <p>
Säännön 3 perusteella </p>
                <p>
C1 sisältää projektin P1 tehtävien alijoukon ajan, kulut, materiaalit, ja maksut.
                </p>
                <p>
CL2 sisältää projektin P1 tehtävien alijoukon ajan, kulut, materiaalit, ja maksut.
                </p>
                <p>
Ainoa lisätarkistus koskee CL1-tehtävien alijoukkoa, joka eroaa CL2:n tehtävien alijoukosta. Näin voidaan varmistaa, että CL2-tehtävissä ei ole päällekkäisiä tehtäviä. Järjestelmä suorittaa tämän, kun tehtävät on liitetty.
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
S1 </p>
            </td>
            <td width="65" valign="top">
                <p>
SR2 </p>
            </td>
            <td width="42" valign="top">
                <p>
K1 </p>
            </td>
            <td width="67" valign="top">
                <p>
Vain valitut tehtävät </p>
            </td>
            <td width="48" valign="top">
                <p>
Kyllä </p>
            </td>
            <td width="48" valign="top">
                <p>
Kyllä </p>
            </td>
            <td width="42" valign="top">
                <p>
Kyllä </p>
            </td>
            <td width="42" valign="top">
                <p>
Kyllä </p>
            </td>
        </tr>
    </tbody>
</table>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
