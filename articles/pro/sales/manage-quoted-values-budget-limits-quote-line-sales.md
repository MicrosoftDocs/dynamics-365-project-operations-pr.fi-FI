---
title: Projektipohjaisten tarjousrivien yleiskatsaus – lite
description: Tässä aiheessa on tietoja projektipohjaisten tarjousrivien käyttämisestä projektityöhön. (Pro)
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: be1663c0d226fa19fe4b9df566e16d215f1fc08e
ms.sourcegitcommit: f6f86e80dfef15a7b5f9174b55dddf410522f7c8
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/31/2020
ms.locfileid: "4181088"
---
# <a name="project-based-quote-lines-overview---lite"></a>Projektipohjaisten tarjousrivien yleiskatsaus – lite

_**Käytetään:** Lite-käyttöönotto – kauppa proformalaskutukseen_

Projektipohjaiset tarjousrivit on suunniteltu auttamaan projektityön arvioinnissa. Projektipohjaisen tarjousrivin rakennetta laajennetaan projektiarvioihin seuraavin käsittein:

- Laskutustapa
- Projektin ja tehtävän yhdistäminen
- Sisältyvät tapahtumaluokat
- Ei-ylitettävä rajoitus
- Veloitettavuusasetus
- Arvio tarjousrivin tietojen avulla
- Tarjousrivin asiakkaat

Seuraavassa taulukossa on tietoja projektipohjaisen tarjousrivin **Yleiset**-välilehden kentistä. Näiden kenttien avulla voit määrittää perustan projektityön yksityiskohtaiselle alhaalta ylöspäin -arvioinnille.

| **Kenttä** | **Kuvaus** | **Loppupään vaikutus** |
| --- | --- | --- |
| Nimi | Tarjousrivin nimi, jonka avulla voit määrittää arvioidun tarjouksen erillisen osan. | Kopioidaan tästä tarjousrivistä luotuun projektisopimusriviin, kun tarjous on voitettu. |
| Laskutustapa | Kun mahdollisuudesta luodaan tarjous, tämä arvo kopioidaan mahdollisuusrivin vastaavasta kentästä. Tämä kenttä sisältää kaksi tärkeintä Dynamics 365 Project Operationsin tukemaa sopimusmallia:</br>– Kiinteä hinta</br>– Aika ja materiaali.| Tämän kentän arvo kopioidaan tästä tarjousrivistä luotuun projektisopimusriviin, kun tarjous on voitettu. |
| Project | Tämän valinnaisen kentän avulla voit määrittää projektin, jota käytetään tämän tehtävän töiden toimittamiseen. Kun projekti yhdistetään tarjousriviin, se auttaa määrittämään laskutettavia tehtäviä ja tuomaan projektipohjaisen arvion tarjousriviin tarjousrivin tietoina. Kun projektia ei ole yhdistetty projektipohjaiseen tarjousriviin, arvio tulisi luoda manuaalisesti luomalla kukin tarjousrivin tieto. | Tämän kentän arvo kopioidaan tästä tarjousrivistä luotuun projektisopimusriviin, kun tarjous on voitettu.|
| Sisällytettävät tehtävät | Ilmaisee, käytetäänkö tätä tarjousriviä valitussa projektissa kaikkiin projektitehtäviin vai vain joihinkin niistä. Tällä kentällä on seuraavat mahdolliset arvot:</br>– Kaikki projektitehtävät</br>– Vain valitut projektitehtävät</br>Tässä kentässä oleva tyhjä arvo vastaa **Kaikki projektitehtävät** -vaihtoehtoa. | Kun **Vain valitut projektitehtävät** valitaan projektisivulla, **Tehtävien laskutuksen asetukset** -välilehdessä voit valita tiettyjä tehtäviä, jotka liitetään tähän tarjousriviin. Tämän kentän arvo kopioidaan tästä tarjousrivistä luotuun projektisopimusriviin, kun tarjous on voitettu. |
| Sisällytä aika | **Kyllä**/**Ei**-merkintä osoittaa, onko valitun projektin aikatapahtumat tai työvoimakustannukset sisällytettävä tämän tarjousrivin arvioon. **Ei**-arvo osoittaa, että aikatapahtumia tai työvoimakustannuksia ei sisällytetä tämän tarjousrivin arvioon. **Kyllä**-arvo osoittaa, että aikatapahtumat ja työvoimakustannukset sisällytetään tämän tarjousrivin arvioon. | Tämän kentän arvo kopioidaan tästä tarjousrivistä luotuun projektisopimusriviin, kun tarjous on voitettu. |
| Sisällytä kulu | **Kyllä**/**Ei**-merkintä osoittaa, onko valitun projektin kulujen kustannukset sisällytettävä tämän tarjousrivin arvioon. **Ei**-arvo osoittaa, että kulujen kustannuksia ei sisällytetä tämän tarjousrivin arvioon. **Kyllä**-arvo osoittaa, että kulujen kustannukset sisällytetään tämän tarjousrivin arvioon. | Tämän kentän arvo kopioidaan tästä tarjousrivistä luotuun projektisopimusriviin, kun tarjous on voitettu. |
| Sisällytä maksu | **Kyllä**/**Ei**-merkintä osoittaa, onko valitun projektin maksut sisällytettävä tämän tarjousrivin arvioon. **Ei**-arvo osoittaa, että maksuja ei sisällytetä tämän tarjousrivin arvioon. **Kyllä**-arvo osoittaa, että maksut sisällytetään tämän tarjousrivin arvioon. | Tämän kentän arvo kopioidaan tästä tarjousrivistä luotuun projektisopimusriviin, kun tarjous on voitettu. |
| Tarjottu summa | Tämä on summa, joka tarjotaan asiakkaalle kaikista tähän projektipohjaiseen tarjousriviin ennustetuista töistä. Kun mahdollisuudesta luodaan tarjous, tämä arvo kopioidaan mahdollisuusrivin **Asiakkaan budjetti** -kentästä. Kun projektipohjaisella tarjousrivillä on rivitiedot, tämä kenttä on lukittu muokkaukselta, ja se on summattu tarjousrivin tietojen summista. | Tämän kentän arvo kopioidaan tästä tarjousrivistä luotuun projektisopimusriviin, kun tarjous on voitettu. |
| Arvioitu vero | Tämä on muokattava kenttä, jolla käyttäjä voi lisätä arvioidun verosumman tarjousriville. Kun projektipohjaisella tarjousrivillä on rivitiedot, tämä kenttä on lukittu muokkaukselta, ja se on summattu tarjousrivin tietojen verosummista. | Tämän kentän arvo kopioidaan tästä tarjousrivistä luotuun projektisopimusriviin, kun tarjous on voitettu. |
| Tarjouksen summa veron jälkeen | Tämä kenttä on tarjousrivin summa veron jälkeen, ja se on vain luku -tilassa. Tämän kentän summa lasketaan seuraavasti: *Tarjouksen summa + vero*. | Tämän kentän arvo kopioidaan tästä tarjousrivistä luotuun projektisopimusriviin, kun tarjous on voitettu. |
| Ei-ylitettävä rajoitus | Tätä kenttää voi muokata, ja se on käytettävissä vain projektipohjaisilla tarjousriveillä, joilla on **Aika ja materiaali** -laskutusmenetelmä. | Tämän kentän arvo kopioidaan tästä tarjousrivistä luotuun projektisopimusriviin, kun tarjous on voitettu. |
| Asiakasbudjetti | Tämä kenttä on muokattava ja se kopioidaan kopioidaan mahdollisuusrivin vastaavasta kentästä, josa tarjous luotiin mahdollisuudesta. | Tämän kentän arvo kopioidaan tästä tarjousrivistä luotuun projektisopimusriviin, kun tarjous on voitettu. |


## <a name="validation-rules-for-fields-on-the-general-tab-of-project-based-quote-lines"></a>Projektipohjaisten tarjousrivien Yleiset-välilehden kenttien tarkistussäännöt

**Sääntö 1**: Jos **Sisällytetyt tehtävät** -kenttä on tyhjä tai jos sen arvo on **Kaikki projektitehtävät**, projekti sisällytetään tarjousriviin.

**Sääntö 2**: Jos **Sisällytetyt tehtävät** -kenttä on tyhjä tai jos sen arvo on **Kaikki projektitehtävät**, projekti ja tietty tapahtumaluokka voidaan sisällyttää vain yhteen tarjouksen projektipohjaiseen tarjousriviin.

**Sääntö 3**: Jos **Sisällytetyt tehtävät** -kenttä on tyhjä tai jos sen arvo on **Vain valitut projektitehtävät**, projekti ja tietty tapahtumaluokka voidaan sisällyttää useille tarjouksen projektipohjaisille tarjousriveille.

**Sääntö 4**: Jos mahdollisuudella on useita tarjouksia, eri tarjouksista voi olla tarjousrivejä, jotka kaikki viittaavat samaan projektiin ja sisältävät saman tapahtumaluokan.

**Sääntö 5**: Jos tarjoukset eivät kuulu samaan mahdollisuuteen, ne eivät voi sisältää samaa projektia ja tapahtumaluokkaa.

<table border="0" cellspacing="0" cellpadding="0">
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
            <td width="90" valign="top">
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
                    <strong>Sisällytä</strong>
                </p>
                <p>
                    <strong>Maksu</strong>
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
            <td width="90" valign="top">
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
            <td width="54" rowspan="2" valign="top">
                <p>
Ei kelpaa </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
Säännön 2 rikkominen. P1-projektin aika, kulu ja maksut sisältyvät molemmille tarjousriveille (QL1 ja QL2).
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
            <td width="90" valign="top">
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
            <td width="90" valign="top">
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
            <td width="90" valign="top">
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
            <td width="54" rowspan="2" valign="top">
                <p>
Ei kelpaa </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
Säännön 2 rikkominen. P1-projektin aika ja maksut sisältyvät molemmille tarjousriveille (QL1 ja QL2).
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
            <td width="90" valign="top">
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
            <td width="90" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="108" valign="top">
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
            <td width="90" valign="top">
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
            <td width="54" rowspan="2" valign="top">
                <p>
Kelvollinen </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                  <p>
P1-projektin aika ja maksut sisältyvät riville QL1.
Kulu P1-projektissa sisältyy riville QL2.
Kullekin tarjousriville lisätyissä kohteissa ei ole päällekkäisyyttä, ja tämä on kelvollinen.
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
            <td width="90" valign="top">
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
            <td width="90" valign="top">
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
            <td width="90" valign="top">
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
            <td width="54" rowspan="2" valign="top">
                <p>
Ei kelpaa </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
Säännön 2 rikkominen yllä </p>
                <p>
Q1 sisältää projektin P1 tehtävien alijoukon ajan, kulut ja maksut.
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
            <td width="90" valign="top">
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
            <td width="90" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="108" valign="top">
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
            <td width="90" valign="top">
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
            <td width="54" rowspan="2" valign="top">
                <p>
Kelvollinen </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
Edellä olevan säännön 3 mukaan </p>
                <p>
Q1 sisältää projektin P1 tehtävien alijoukon ajan, kulut ja maksut.
                </p>
                <p>
QL2 sisältää projektin P1 tehtävien alijoukon ajan, kulut ja maksut.
                </p>
                <p>
Ainoa lisätarkistus on QL1-rivin tehtävien alijoukolle, joka eroaa QL2-rivin tehtävien alijoukosta. Näin varmistetaan, että päällekkäisyyksiä ei ole. Järjestelmä suorittaa tämän, kun tehtävät on liitetty.
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
            <td width="90" valign="top">
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
            <td width="90" valign="top">
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
            <td width="90" valign="top">
                <p>
Kaikki projektitehtävät tai tyhjä </p>
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
Säännön 5 mukaan Q1 ja Q2 ovat saman mahdollisuuden kaksi tarjousta, joten ne voivat molemmat arvioida projektin samoja osia.
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
QL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
K1 </p>
            </td>
            <td width="90" valign="top">
                <p>
Kaikki projektitehtävät tai tyhjä </p>
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
            <td width="90" valign="top">
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
            <td width="90" valign="top">
                <p>
Kaikki projektitehtävät tai tyhjä </p>
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
Säännön 4 mukaan Q1 ja Q2 ovat eri mahdollisuuksien kaksi tarjousta, joten ne eivät voi arvioida saman projektin samoja osia.
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
            <td width="90" valign="top">
                <p>
Kaikki projektitehtävät tai tyhjä </p>
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



[!INCLUDE[footer-include](../../includes/footer-banner.md)]