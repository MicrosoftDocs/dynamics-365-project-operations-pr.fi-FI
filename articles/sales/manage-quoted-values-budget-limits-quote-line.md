---
title: Projektin tarjousrivien yleiskatsaus
description: Tässä aiheessa on tietoja projektin tarjousrivien käytöstä projektityöhön.
author: rumant
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.custom: intro-internal
ms.openlocfilehash: c0a4d2d4b9e958ba14badda5a945e0522abba336c82128bfe7539663e0b90f1e
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/06/2021
ms.locfileid: "6997917"
---
# <a name="project-quote-lines-overview"></a>Projektin tarjousrivien yleiskatsaus

_**Käytetään:** Project Operationsin resursseihin ja ei-varastoitaviin perustuvissa skenaarioissa_

Projektipohjaiset tarjousrivit on suunniteltu auttamaan projektityön arvioinnissa. Projektipohjaisen tarjousrivin rakennetta laajennetaan projektiarvioihin seuraavin käsittein:

- Laskutustapa
- Projektin yhdistämismääritys
- Sisältyvät tapahtumaluokat
- Ei-ylitettävä rajoitus
- Veloitettavuusasetus
- Arvio tarjousrivin tietojen avulla
- Tarjousrivin asiakkaat

Seuraavassa taulukossa on tietoja projektipohjaisen tarjousrivin **Yleiset**-välilehden kentistä. Näiden kenttien avulla voit määrittää perustan projektityön yksityiskohtaiselle alhaalta ylöspäin -arvioinnille.

| **Kenttä** | **Kuvaus** | **Loppupään vaikutus** |
| --- | --- | --- |
| Nimi | Tarjousrivin nimi, jonka avulla voit määrittää arvioidun tarjouksen erillisen osan. | Kopioidaan tästä tarjousrivistä luotuun projektisopimusriviin, kun tarjous on voitettu. |
| Laskutustapa | Kun mahdollisuudesta luodaan tarjous, tämä arvo kopioidaan mahdollisuusrivin vastaavasta kentästä. Tässä kentässä on kaksi pääasiallista palvelusopimusmallia, joita Dynamics 365 Project Operationsissa tuetaan:</br>– Kiinteä hinta</br>– Aika ja materiaali.| Tämän kentän arvo kopioidaan tästä tarjousrivistä luotuun projektisopimusriviin, kun tarjous on voitettu. |
| Project | Tämän valinnaisen kentän avulla voit määrittää projektin, jota käytetään tämän tehtävän töiden toimittamiseen. Kun projekti yhdistetään tarjousriviin, se auttaa määrittämään laskutettavia tehtäviä ja tuomaan projektipohjaisen arvion tarjousriviin tarjousrivin tietoina. Kun projektia ei ole yhdistetty projektipohjaiseen tarjousriviin, arvio tulisi luoda manuaalisesti luomalla kukin tarjousrivin tieto. | Tämän kentän arvo kopioidaan tästä tarjousrivistä luotuun projektisopimusriviin, kun tarjous on voitettu. |
| Sisällytä aika | **Kyllä**/**Ei**-merkintä osoittaa, onko valitun projektin aikatapahtumat tai työvoimakustannukset sisällytettävä tämän tarjousrivin arvioon. **Ei**-arvo osoittaa, että aikatapahtumia tai työvoimakustannuksia ei sisällytetä tämän tarjousrivin arvioon. **Kyllä**-arvo osoittaa, että aikatapahtumat ja työvoimakustannukset sisällytetään tämän tarjousrivin arvioon. | Tämän kentän arvo kopioidaan tästä tarjousrivistä luotuun projektisopimusriviin, kun tarjous on voitettu. |
| Sisällytä kulu | **Kyllä**/**Ei**-merkintä osoittaa, onko valitun projektin kulujen kustannukset sisällytettävä tämän tarjousrivin arvioon. **Ei**-arvo osoittaa, että kulujen kustannuksia ei sisällytetä tämän tarjousrivin arvioon. **Kyllä**-arvo osoittaa, että kulujen kustannukset sisällytetään tämän tarjousrivin arvioon. | Tämän kentän arvo kopioidaan tästä tarjousrivistä luotuun projektisopimusriviin, kun tarjous on voitettu. |
| Sisällytä maksu | **Kyllä**/**Ei**-merkintä osoittaa, onko valitun projektin maksut sisällytettävä tämän tarjousrivin arvioon. **Ei**-arvo osoittaa, että maksuja ei sisällytetä tämän tarjousrivin arvioon. **Kyllä**-arvo osoittaa, että maksut sisällytetään tämän tarjousrivin arvioon. | Tämän kentän arvo kopioidaan tästä tarjousrivistä luotuun projektisopimusriviin, kun tarjous on voitettu. |
| Tarjottu summa | Tämä on summa, joka tarjotaan asiakkaalle kaikista tähän projektipohjaiseen tarjousriviin ennustetuista töistä. Kun mahdollisuudesta luodaan tarjous, tämä arvo kopioidaan mahdollisuusrivin **Asiakkaan budjetti** -kentästä. Kun projektipohjaisella tarjousrivillä on rivitiedot, tämä kenttä on lukittu muokkaukselta, ja se on summattu tarjousrivin tietojen summista. | Tämän kentän arvo kopioidaan tästä tarjousrivistä luotuun projektisopimusriviin, kun tarjous on voitettu. |
| Arvioitu vero | Tämä on muokattava kenttä, jolla käyttäjä voi lisätä arvioidun verosumman tarjousriville. Kun projektipohjaisella tarjousrivillä on rivitiedot, tämä kenttä on lukittu muokkaukselta, ja se on summattu tarjousrivin tietojen verosummista. | Tämän kentän arvo kopioidaan tästä tarjousrivistä luotuun projektisopimusriviin, kun tarjous on voitettu. |
| Tarjouksen summa veron jälkeen | Tämä kenttä on tarjousrivin summa veron jälkeen, ja se on vain luku -tilassa. Tämän kentän summa lasketaan seuraavasti: *Tarjouksen summa + vero*. | Tämän kentän arvo kopioidaan tästä tarjousrivistä luotuun projektisopimusriviin, kun tarjous on voitettu. |
| Ei-ylitettävä rajoitus | Tätä kenttää voi muokata, ja se on käytettävissä vain projektipohjaisilla tarjousriveillä, joilla on **Aika ja materiaali** -laskutusmenetelmä. | Tämän kentän arvo kopioidaan tästä tarjousrivistä luotuun projektisopimusriviin, kun tarjous on voitettu. |
| Asiakasbudjetti | Tämä kenttä on muokattava ja se kopioidaan kopioidaan mahdollisuusrivin vastaavasta kentästä, josa tarjous luotiin mahdollisuudesta. | Tämän kentän arvo kopioidaan tästä tarjousrivistä luotuun projektisopimusriviin, kun tarjous on voitettu. |

## <a name="validation-rules-for-fields-on-the-general-tab-of-project-based-quote-lines"></a>Projektipohjaisten tarjousrivien Yleiset-välilehden kenttien tarkistussäännöt

**Sääntö 1**: Valitun projektin tietty tapahtumaluokka voidaan sisällyttää vain yhteen tarjouksen projektipohjaiseen tarjousriviin.

**Sääntö 2**: Jos mahdollisuudella on useita tarjouksia, eri tarjouksista voi olla tarjousrivejä, jotka kaikki viittaavat samaan projektiin ja sisältävät saman tapahtumaluokan.

**Sääntö 3**: Jos tarjoukset eivät kuulu samaan mahdollisuuteen, ne eivät voi sisältää samaa projektia ja tapahtumaluokkaa.

<table border="1" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="61" valign="top">
                <p>
                    <strong>Mahdollisuus</strong>
                </p>
            </td>
            <td width="41" valign="top">
                <p>
                    <strong>Tarjous</strong>
                </p>
            </td>
            <td width="42" valign="top">
                <p>
                    <strong>Tarjousrivi</strong>
                </p>
            </td>
            <td width="42" valign="top">
                <p>
                    <strong>Project</strong>
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
                    <strong>Sisällytä</strong>
                </p>
                <p>
                    <strong>maksu</strong>
                </p>
            </td>
            <td width="54" valign="top">
                <p>
                    <strong>Kelpaa / ei kelpaa</strong>
                </p>
            </td>
            <td width="308" valign="top">
                <p>
                    <strong>Syy</strong>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O1 </p>
            </td>
            <td width="41" valign="top">
                <p>
VN1 </p>
            </td>
            <td width="42" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
K1 </p>
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
            <td width="54" rowspan="2" valign="top">
                <p>
Ei kelpaa </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
Säännön 1 rikkominen. P1-projektin aika, kulu ja maksut sisältyvät molemmille tarjousriveille (QL1 ja QL2).
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O1 </p>
            </td>
            <td width="41" valign="top">
                <p>
VN1 </p>
            </td>
            <td width="42" valign="top">
                <p>
QL2 </p>
            </td>
            <td width="42" valign="top">
                <p>
K1 </p>
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
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="308" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O1 </p>
            </td>
            <td width="41" valign="top">
                <p>
VN1 </p>
            </td>
            <td width="42" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
K1 </p>
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
            <td width="54" rowspan="2" valign="top">
                <p>
Ei kelpaa </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
Säännön 1 rikkominen. P1-projektin aika ja maksut sisältyvät molemmille tarjousriveille (QL1 ja QL2).
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O1 </p>
            </td>
            <td width="41" valign="top">
                <p>
VN1 </p>
            </td>
            <td width="42" valign="top">
                <p>
QL2 </p>
            </td>
            <td width="42" valign="top">
                <p>
K1 </p>
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
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="308" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O1 </p>
            </td>
            <td width="41" valign="top">
                <p>
VN1 </p>
            </td>
            <td width="42" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
K1 </p>
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
            <td width="54" rowspan="2" valign="top">
                <p>
Kelvollinen </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                 <p>
P1-projektin aika ja maksut sisältyvät riville QL1.
Kulu P1-projektissa sisältyy riville QL2.
Kullekin tarjousriville lisätyissä kohteissa ei ole päällekkäisyyttä, joten tämä on kelvollinen.
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O1 </p>
            </td>
            <td width="41" valign="top">
                <p>
VN1 </p>
            </td>
            <td width="42" valign="top">
                <p>
QL2 </p>
            </td>
            <td width="42" valign="top">
                <p>
K1 </p>
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
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="308" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O1 </p>
            </td>
            <td width="41" valign="top">
                <p>
VN1 </p>
            </td>
            <td width="42" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
K1 </p>
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
            <td width="54" rowspan="2" valign="top">
                <p>
Ei kelpaa </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
Säännön 1 rikkominen yllä </p>
                <p>
Q1 sisältää koko P1-projektin ajan, kulut ja maksut.
                </p>
                <p>
QL2 sisältää koko projektin P1 ajan, kulut ja maksut, ja se on päällekkäinen riville Q1 sisällytettyjen kohteiden kanssa.
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O1 </p>
            </td>
            <td width="41" valign="top">
                <p>
VN1 </p>
            </td>
            <td width="42" valign="top">
                <p>
QL2 </p>
            </td>
            <td width="42" valign="top">
                <p>
K1 </p>
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
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="308" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O1 </p>
            </td>
            <td width="41" valign="top">
                <p>
VN1 </p>
            </td>
            <td width="42" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
K1 </p>
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
            <td width="54" valign="top">
                <p>
Kelvollinen </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
Säännön 2 mukaan Q1 ja Q2 ovat saman mahdollisuuden kaksi tarjousta, joten ne voivat molemmat arvioida projektin samoja osia.
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O1 </p>
            </td>
            <td width="41" valign="top">
                <p>
VN2 </p>
            </td>
            <td width="42" valign="top">
                <p>
QL1 kohteessa Q2 </p>
            </td>
            <td width="42" valign="top">
                <p>
K1 </p>
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
            <td width="54" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="308" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O1 </p>
            </td>
            <td width="41" valign="top">
                <p>
VN1 </p>
            </td>
            <td width="42" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
K1 </p>
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
            <td width="54" valign="top">
                <p>
Kelvollinen </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
Säännön 3 mukaan Q1 ja Q2 ovat eri mahdollisuuksien kaksi tarjousta, joten ne eivät voi arvioida saman projektin samoja osia.
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O2 </p>
            </td>
            <td width="41" valign="top">
                <p>
VN1 </p>
            </td>
            <td width="42" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
K1 </p>
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
            <td width="54" valign="top">
                <p>
Ei kelpaa </p>
            </td>
        </tr>
    </tbody>
</table>



[!INCLUDE[footer-include](../includes/footer-banner.md)]
