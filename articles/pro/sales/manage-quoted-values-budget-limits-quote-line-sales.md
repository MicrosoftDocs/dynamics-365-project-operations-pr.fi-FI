---
title: Projektipohjaisten tarjousrivien yleiskatsaus
description: Tässä aiheessa on tietoja projektipohjaisten tarjousrivien käyttämisestä projektityöhön.
author: rumant
ms.date: 03/30/2021
ms.topic: overview
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 0a9661d9b91ffeece4c66b129846632b30ebebc8
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/14/2022
ms.locfileid: "8591078"
---
# <a name="project-based-quote-lines-overview"></a>Projektipohjaisten tarjousrivien yleiskatsaus 

_**Koskee:** Lite-käyttöönotto - kaupasta proformalaskutukseen, Project Operationsin resurssiin/ei-varastointiin perustuvia skenaarioita_

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
| Nimi | Sen tarjousrivin nimi, joka auttaa tunnistamaan arvioitavan tarjouksen erillisen osan. | Kopioidaan tästä tarjousrivistä luotuun projektisopimusriviin, kun tarjous on voitettu. |
| Laskutustapa | Kun mahdollisuudesta luodaan tarjous, tämä arvo kopioidaan mahdollisuusrivin vastaavasta kentästä. Tässä kentässä on kaksi pääasiallista palvelusopimusmallia, joita Dynamics 365 Project Operationsissa tuetaan:</br>- Kiinteä hinta</br>- Aika ja materiaali.| Tämä arvo kopioidaan projektisopimusriville, joka luodaan tältä tarjousriviltä, kun tarjous on voitettu. |
| Project | Tämän valinnaisen kentän avulla voit määrittää projektin, jota käytetään tämän tehtävän töiden toimittamiseen. Kun projekti yhdistetään tarjousriviin, se auttaa määrittämään laskutettavia tehtäviä ja tuomaan projektipohjaisen arvion tarjousriviin tarjousrivin tietoina. Kun projektia ei ole yhdistetty projektipohjaiseen tarjousriviin, arvio tulisi luoda manuaalisesti luomalla kukin tarjousrivin tieto. | Tämä arvo kopioidaan projektisopimusriville, joka luodaan tältä tarjousriviltä, kun tarjous on voitettu.|
| Sisällytettävät tehtävät | Ilmaisee, käytetäänkö tätä tarjousriviä valitussa projektissa kaikkiin projektitehtäviin vai vain joihinkin niistä. Tällä kentällä on seuraavat mahdolliset arvot:</br>- Kaikki projektitehtävät</br>- Vain valitut projektitehtävät</br>Tässä kentässä oleva tyhjä arvo vastaa **Kaikki projektitehtävät** -vaihtoehtoa. | Kun projektisivulla valitaan **Vain valitut projektitehtävät**, **Tehtävän laskutuksen asetukset** -välilehdessä voidaan valita tiettyjä tehtäviä, jotka liitetään tähän tarjousriviin. Tämä arvo kopioidaan projektisopimusriville, joka luodaan tältä tarjousriviltä, kun tarjous on voitettu. |
| Sisällytä aika | **Kyllä**/**Ei** -arvo ilmaisee, sisällytetäänkö valitun projektin aikatapahtumat tai työvoimakustannukset arvioon tällä tarjousrivillä. **Ei**-arvo osoittaa, että aikatapahtumia tai työvoimakustannuksia ei sisällytetä tämän tarjousrivin arvioon. **Kyllä**-arvo osoittaa, että aikatapahtumat ja työvoimakustannukset sisällytetään tämän tarjousrivin arvioon. | Tämä arvo kopioidaan projektisopimusriville, joka luodaan tältä tarjousriviltä, kun tarjous on voitettu. |
| Sisällytä kulu | **Kyllä**/**Ei** -arvo ilmaisee, sisällytetäänkö valitun projektin kulukustannukset arvioon tällä tarjousrivillä. **Ei**-arvo osoittaa, että kulujen kustannuksia ei sisällytetä tämän tarjousrivin arvioon. **Kyllä**-arvo osoittaa, että kulujen kustannukset sisällytetään tämän tarjousrivin arvioon. | Tämä arvo kopioidaan projektisopimusriville, joka luodaan tältä tarjousriviltä, kun tarjous on voitettu. |
| Sisällytä materiaali | **Kyllä**/**Ei** -arvo ilmaisee, sisällytetäänkö valitun projektin materiaalikustannukset arvioon tällä tarjousrivillä. **Ei**-arvo ilmaisee, että materiaalikustannuksia ei sisällytetä arvioon tällä tarjousrivillä. **Kyllä**-arvo ilmaisee, että materiaalikustannukset sisällytetään arvioon tällä tarjousrivillä. | Tämä arvo kopioidaan projektisopimusriville, joka luodaan tältä tarjousriviltä, kun tarjous on voitettu. |
| Sisällytä maksu | **Kyllä**/**Ei** -arvo ilmaisee, sisällytetäänkö valitun projektin maksut arvioon tällä tarjousrivillä. **Ei**-arvo osoittaa, että maksuja ei sisällytetä tämän tarjousrivin arvioon. **Kyllä**-arvo osoittaa, että maksut sisällytetään tämän tarjousrivin arvioon. | Tämä arvo kopioidaan projektisopimusriville, joka luodaan tältä tarjousriviltä, kun tarjous on voitettu. |
| Tarjottu summa | Tämä on summa, joka annetaan tarjouksena asiakkaalle projektipohjaisella tarjousrivillä ennustetusta työstä. Kun mahdollisuudesta luodaan tarjous, tämä arvo kopioidaan mahdollisuusrivin **Asiakkaan budjetti** -kentästä. Kun projektipohjaisella tarjousrivillä on rivitiedot, tämä kenttä on lukittu muokkaukselta, ja se on summattu tarjousrivin tietojen summista. | Tämä arvo kopioidaan projektisopimusriville, joka luodaan tältä tarjousriviltä, kun tarjous on voitettu. |
| Arvioitu vero | Tämä on muokattava kenttä, jolla käyttäjä voi lisätä arvioidun verosumman tarjousriville. Kun projektipohjaisella tarjousrivillä on rivitiedot, tämä kenttä on lukittu muokkaukselta, ja se on summattu tarjousrivin tietojen verosummista. | Tämä arvo kopioidaan projektisopimusriville, joka luodaan tältä tarjousriviltä, kun tarjous on voitettu. |
| Tarjouksen summa veron jälkeen | Tämä kenttä on tarjousrivin summa veron jälkeen, ja se on vain luku -tilassa. Tämän kentän summa lasketaan seuraavasti: *Tarjouksen summa + vero*. | Tämä arvo kopioidaan projektisopimusriville, joka luodaan tältä tarjousriviltä, kun tarjous on voitettu. |
| Ei-ylitettävä rajoitus | Tätä kenttää voi muokata, ja se on käytettävissä vain projektipohjaisilla tarjousriveillä, joilla on **Aika ja materiaali** -laskutusmenetelmä. | Tämä arvo kopioidaan projektisopimusriville, joka luodaan tältä tarjousriviltä, kun tarjous on voitettu. |
| Asiakasbudjetti | Tämä kenttä on muokattava ja se kopioidaan kopioidaan mahdollisuusrivin vastaavasta kentästä, josa tarjous luotiin mahdollisuudesta. | Tämä arvo kopioidaan projektisopimusriville, joka luodaan tältä tarjousriviltä, kun tarjous on voitettu. |


## <a name="validation-rules-for-fields-on-the-general-tab-of-project-based-quote-lines"></a>Projektipohjaisten tarjousrivien Yleiset-välilehden kenttien tarkistussäännöt

**Sääntö 1**: Jos **Sisällytetyt tehtävät** -kenttä on tyhjä tai jos sen arvo on **Kaikki projektitehtävät**, projekti sisällytetään tarjousriviin.

**Sääntö 2**: Jos **Sisällytetyt tehtävät** -kenttä on tyhjä tai jos sen arvo on **Kaikki projektitehtävät**, projekti ja tietty tapahtumaluokka voidaan sisällyttää vain yhteen tarjouksen projektipohjaiseen tarjousriviin.

**Sääntö 3**: Jos **Sisällytetyt tehtävät** -kenttä on tyhjä tai jos sen arvo on **Vain valitut projektitehtävät**, projekti ja tietty tapahtumaluokka voidaan sisällyttää useille tarjouksen projektipohjaisille tarjousriveille.

**Sääntö 4**: Jos mahdollisuudella on useita tarjouksia, eri tarjouksista voi olla tarjousrivejä, jotka kaikki viittaavat samaan projektiin ja sisältävät saman tapahtumaluokan.

**Sääntö 5**: Jos tarjoukset eivät kuulu samaan mahdollisuuteen, ne eivät voi sisältää samaa projektia ja tapahtumaluokkaa.

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="59" valign="top">
                <p>
                    <strong>Mahdollisuus</strong>
                </p>
            </td>
            <td width="39" valign="top">
                <p>
                    <strong>Tarjous</strong>
                </p>
            </td>
            <td width="40" valign="top">
                <p>
                    <strong>Tarjousrivi</strong>
                </p>
            </td>
            <td width="41" valign="top">
                <p>
                    <strong>Project</strong>
                </p>
            </td>
            <td width="77" valign="top">
                <p>
                    <strong>Sisällytettävät tehtävät</strong>
                </p>
            </td>
            <td width="45" valign="top">
                <p>
                    <strong>Sisällytä aika</strong>
                </p>
            </td>
            <td width="46" valign="top">
                <p>
                    <strong>Sisällytä kulu</strong>
                </p>
            </td>
            <td width="43" valign="top">
                <p>
                    <strong>Sisällytä materiaali</strong>
                </p>
            </td>
            <td width="41" valign="top">
                <p>
                    <strong>Sisällytä</strong>
                </p>
                <p>
                    <strong>Maksu</strong>
                </p>
            </td>
            <td width="49" valign="top">
                <p>
                    <strong>Kelpaa / ei kelpaa</strong>
                </p>
            </td>
            <td width="200" valign="top">
                <p>
                    <strong>Syy</strong>
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
O1 </p>
            </td>
            <td width="39" valign="top">
                <p>
VN1 </p>
            </td>
            <td width="40" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="41" valign="top">
                <p>
K1 </p>
            </td>
            <td width="77" valign="top">
                <p>
Tyhjä </p>
            </td>
            <td width="45" valign="top">
                <p>
Kyllä </p>
            </td>
            <td width="46" valign="top">
                <p>
Kyllä </p>
            </td>
            <td width="43" valign="top">
                <p>
Kyllä </p>
            </td>
            <td width="41" valign="top">
                <p>
Kyllä </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
Ei kelpaa </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
Säännön 2 rikkominen. P1-projektin aika, kulu ja maksut sisältyvät tarjousriveille QL1 ja QL2 </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
O1 </p>
            </td>
            <td width="39" valign="top">
                <p>
VN1 </p>
            </td>
            <td width="40" valign="top">
                <p>
QL2 </p>
            </td>
            <td width="41" valign="top">
                <p>
K1 </p>
            </td>
            <td width="77" valign="top">
                <p>
Tyhjä </p>
            </td>
            <td width="45" valign="top">
                <p>
Kyllä </p>
            </td>
            <td width="46" valign="top">
                <p>
Kyllä </p>
            </td>
            <td width="43" valign="top">
                <p>
Kyllä </p>
            </td>
            <td width="41" valign="top">
                <p>
Kyllä </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
O1 </p>
            </td>
            <td width="39" valign="top">
                <p>
VN1 </p>
            </td>
            <td width="40" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="41" valign="top">
                <p>
K1 </p>
            </td>
            <td width="77" valign="top">
                <p>
Tyhjä </p>
            </td>
            <td width="45" valign="top">
                <p>
Kyllä </p>
            </td>
            <td width="46" valign="top">
                <p>
No </p>
            </td>
            <td width="43" valign="top">
                <p>
Kyllä </p>
            </td>
            <td width="41" valign="top">
                <p>
Kyllä </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
Ei kelpaa </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
Säännön 2 rikkominen. P1-projektin aika, materiaali ja maksut sisältyvät tarjousriveille QL1 ja QL2 </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
O1 </p>
            </td>
            <td width="39" valign="top">
                <p>
VN1 </p>
            </td>
            <td width="40" valign="top">
                <p>
QL2 </p>
            </td>
            <td width="41" valign="top">
                <p>
K1 </p>
            </td>
            <td width="77" valign="top">
                <p>
Tyhjä </p>
            </td>
            <td width="45" valign="top">
                <p>
Kyllä </p>
            </td>
            <td width="46" valign="top">
                <p>
Kyllä </p>
            </td>
            <td width="43" valign="top">
                <p>
Kyllä </p>
            </td>
            <td width="41" valign="top">
                <p>
Kyllä </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
O1 </p>
            </td>
            <td width="39" valign="top">
                <p>
VN1 </p>
            </td>
            <td width="40" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="41" valign="top">
                <p>
K1 </p>
            </td>
            <td width="77" valign="top">
                <p>
Tyhjä </p>
            </td>
            <td width="45" valign="top">
                <p>
Kyllä </p>
            </td>
            <td width="46" valign="top">
                <p>
No </p>
            </td>
            <td width="43" valign="top">
                <p>
Kyllä </p>
            </td>
            <td width="41" valign="top">
                <p>
Kyllä </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
Kelvollinen </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
P1-projektin aika, materiaali ja maksut sisältyvät QL1:een. <br>
Kulu P1-projektissa sisältyy riville QL2 <br>
Tarjousriveillä ei ole päällekkäisyyksiä, joten ne ovat kelvollisia.
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
O1 </p>
            </td>
            <td width="39" valign="top">
                <p>
VN1 </p>
            </td>
            <td width="40" valign="top">
                <p>
QL2 </p>
            </td>
            <td width="41" valign="top">
                <p>
K1 </p>
            </td>
            <td width="77" valign="top">
                <p>
Tyhjä </p>
            </td>
            <td width="45" valign="top">
                <p>
No </p>
            </td>
            <td width="46" valign="top">
                <p>
Kyllä </p>
            </td>
            <td width="43" valign="top">
                <p>
No </p>
            </td>
            <td width="41" valign="top">
                <p>
No </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
O1 </p>
            </td>
            <td width="39" valign="top">
                <p>
VN1 </p>
            </td>
            <td width="40" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="41" valign="top">
                <p>
K1 </p>
            </td>
            <td width="77" valign="top">
                <p>
Vain valitut tehtävät </p>
            </td>
            <td width="45" valign="top">
                <p>
Kyllä </p>
            </td>
            <td width="46" valign="top">
                <p>
Kyllä </p>
            </td>
            <td width="43" valign="top">
                <p>
Kyllä </p>
            </td>
            <td width="41" valign="top">
                <p>
Kyllä </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
Ei kelpaa </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
Rikkoo sääntöä 2 </p>
                <p>
Q1 sisältää projektin P1 tehtävien alijoukon ajan, materiaalin, kulut ja maksut </p>
                <p>
QL2 sisältää koko projektin P1 ajan, kulut ja maksut, joten se on päällekkäinen Q1:n sisällön kanssa.
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
O1 </p>
            </td>
            <td width="39" valign="top">
                <p>
VN1 </p>
            </td>
            <td width="40" valign="top">
                <p>
QL2 </p>
            </td>
            <td width="41" valign="top">
                <p>
K1 </p>
            </td>
            <td width="77" valign="top">
                <p>
Tyhjä </p>
            </td>
            <td width="45" valign="top">
                <p>
Kyllä </p>
            </td>
            <td width="46" valign="top">
                <p>
Kyllä </p>
            </td>
            <td width="43" valign="top">
                <p>
Kyllä </p>
            </td>
            <td width="41" valign="top">
                <p>
Kyllä </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
O1 </p>
            </td>
            <td width="39" valign="top">
                <p>
VN1 </p>
            </td>
            <td width="40" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="41" valign="top">
                <p>
K1 </p>
            </td>
            <td width="77" valign="top">
                <p>
Vain valitut tehtävät </p>
            </td>
            <td width="45" valign="top">
                <p>
Kyllä </p>
            </td>
            <td width="46" valign="top">
                <p>
Kyllä </p>
            </td>
            <td width="43" valign="top">
                <p>
Kyllä </p>
            </td>
            <td width="41" valign="top">
                <p>
Kyllä </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
Kelvollinen </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
Säännön 3 perusteella, </p>
                <p>
Q1 sisältää projektin P1 tehtävien alijoukon ajan, materiaalin, kulut ja maksut.
                </p>
                <p>
QL2 sisältää projektin P1 tehtävien alijoukon ajan, materiaalin, kulut, ja maksut.
                </p>
                <p>
Ainoa lisätarkistus koskee QL1-tehtävien alijoukkoa, joka eroaa QL2:n tehtävien alijoukosta. Näin voidaan varmistaa, että QL2-tehtävissä ei ole päällekkäisyyksiä. Järjestelmä suorittaa tämän, kun tehtävät on liitetty.
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
O1 </p>
            </td>
            <td width="39" valign="top">
                <p>
VN1 </p>
            </td>
            <td width="40" valign="top">
                <p>
QL2 </p>
            </td>
            <td width="41" valign="top">
                <p>
K1 </p>
            </td>
            <td width="77" valign="top">
                <p>
Vain valitut tehtävät </p>
            </td>
            <td width="45" valign="top">
                <p>
Kyllä </p>
            </td>
            <td width="46" valign="top">
                <p>
Kyllä </p>
            </td>
            <td width="43" valign="top">
                <p>
Kyllä </p>
            </td>
            <td width="41" valign="top">
                <p>
Kyllä </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
O1 </p>
            </td>
            <td width="39" valign="top">
                <p>
VN1 </p>
            </td>
            <td width="40" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="41" valign="top">
                <p>
K1 </p>
            </td>
            <td width="77" valign="top">
                <p>
Kaikki projektitehtävät tai tyhjä </p>
            </td>
            <td width="45" valign="top">
                <p>
Kyllä </p>
            </td>
            <td width="46" valign="top">
                <p>
Kyllä </p>
            </td>
            <td width="43" valign="top">
                <p>
Kyllä </p>
            </td>
            <td width="41" valign="top">
                <p>
Kyllä </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
Kelvollinen </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
Säännön 5 mukaan Q1 ja Q2 ovat kaksi tarjousta samalle mahdollisuudelle, joten ne voivat arvioida samoja projektin osia.
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
O1 </p>
            </td>
            <td width="39" valign="top">
                <p>
VN2 </p>
            </td>
            <td width="40" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="41" valign="top">
                <p>
K1 </p>
            </td>
            <td width="77" valign="top">
                <p>
Kaikki projektitehtävät tai tyhjä </p>
            </td>
            <td width="45" valign="top">
                <p>
Kyllä </p>
            </td>
            <td width="46" valign="top">
                <p>
Kyllä </p>
            </td>
            <td width="43" valign="top">
                <p>
Kyllä </p>
            </td>
            <td width="41" valign="top">
                <p>
Kyllä </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
O1 </p>
            </td>
            <td width="39" valign="top">
                <p>
VN1 </p>
            </td>
            <td width="40" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="41" valign="top">
                <p>
K1 </p>
            </td>
            <td width="77" valign="top">
                <p>
Kaikki projektitehtävät tai tyhjä </p>
            </td>
            <td width="45" valign="top">
                <p>
Kyllä </p>
            </td>
            <td width="46" valign="top">
                <p>
Kyllä </p>
            </td>
            <td width="43" valign="top">
                <p>
Kyllä </p>
            </td>
            <td width="41" valign="top">
                <p>
Kyllä </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
Ei kelpaa </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
Säännön 4 mukaan Q1 ja Q2 ovat kaksi tarjousta eri mahdollisuudelle, joten ne eivät voi arvioida saman projektin samoja osia.
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
O2 </p>
            </td>
            <td width="39" valign="top">
                <p>
VN1 </p>
            </td>
            <td width="40" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="41" valign="top">
                <p>
K1 </p>
            </td>
            <td width="77" valign="top">
                <p>
Kaikki projektitehtävät tai tyhjä </p>
            </td>
            <td width="45" valign="top">
                <p>
Kyllä </p>
            </td>
            <td width="46" valign="top">
                <p>
Kyllä </p>
            </td>
            <td width="43" valign="top">
                <p>
Kyllä </p>
            </td>
            <td width="41" valign="top">
                <p>
Kyllä </p>
            </td>
        </tr>
    </tbody>
</table>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
