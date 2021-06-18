---
title: Todelliset arvot
description: Tässä aiheessa on tietoja Microsoft Dynamics 365 Project Operationsin todellisten arvojen käsittelystä.
author: rumant
ms.date: 04/01/2021
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: ''
ms.search.industry: ''
ms.author: rumant
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 78c7a9486d0338adfd7770447f21d17509e654f7
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/10/2021
ms.locfileid: "5996607"
---
# <a name="actuals"></a>Todelliset arvot 

_**Koskee:** Project Operationsin resurssiin/ei-varastointiin perustuvia skenaarioita, Lite-käyttöönotto - kaupasta proformalaskutukseen_

Toteutuneet arvot edustavat projektin arvioitua ja hyväksyttyä taloudellista ja aikataulun edistymistä. Ne luodaan ajan, kulujen, materiaalin käyttömerkintöjen, kirjausten ja laskujen hyväksynnän tuloksena.

## <a name="journal-lines-and-time-submission"></a>Kirjauskansion rivit ja ajan lähetys

Lisätietoja ajan syöttämisestä on ohjeaiheessa [Ajan syöttämisen yleiskatsaus](../time/time-entry-overview.md).

### <a name="time-and-materials"></a>Aika ja materiaalit

Kun lähetetty ajankohta linkitetään projektiin, joka on yhdistetty aika- ja materiaalisopimusriviin, järjestelmä luo kaksi kirjausriviä, joista toinen on kustannukselle ja toinen laskuttamattomalle myynnille.

### <a name="fixed-price"></a>Kiinteähintainen

Kun lähetetään sellaiseen projektiin linkitetty aikamerkintä, joka on yhdistetty kiinteähintaiseen sopimusriviin, järjestelmä luo kirjauskansion rivi kustannusta varten.

### <a name="default-pricing"></a>Oletushinnoittelu

Oletushintojen luonnin logiikka on kirjauskansion rivillä. Aikamerkinnän kenttien arvot kopioidaan kirjauskansion riville. Nämä arvot sisältävät tapahtumapäivämäärän, sopimusriviin yhdistetyn projektin ja valuuttatuloksen asianmukaisessa hinnastossa.

Oletushintoihin vaikuttavia kenttiä, kuten **Rooli** ja **Organisaatioyksikkö** käytetään kirjauskansion rivin sopivan hinnan määrittämiseen. Voit lisätä mukautetun kentän ajankohdalle. Jos haluat, että kentän arvo välitettään toteutuneisiin arvoihin, luo kenttä **Toteutuneet**- ja **Kirjausrivi**-taulukoihin. Käytä mukautettua koodia, kun haluat välittää valitun kentän arvon ajan syötöstä toteutuneisiin arvoihin kirjausrivin kautta käyttämällä tapahtumien alkuperää. Lisätietoja tapahtumien alkuperästä ja yhteyksistä on ohjeaiheessa [Toteutuneidenarvojen linkittäminen alkuperäisiin tietueisiin](linkingactuals.md#example-how-transaction-origin-works-with-transaction-connection).

## <a name="journal-lines-and-basic-expense-submission"></a>Kirjauskansiorivit ja peruskulujen lähettäminen

Lisätietoja kulun syöttämisestä on ohjeaiheessa [Kulujen syöttämisen yleiskatsaus](../expense/expense-overview.md).

### <a name="time-and-materials"></a>Aika ja materiaalit

Kun lähetetty perustukulumerkintä linkitetään projektiin, joka on yhdistetty aika- ja materiaalisopimusriviin, järjestelmä luo kaksi kirjausriviä, joista toinen on kustannukselle ja toinen laskuttamattomalle myynnille.

### <a name="fixed-price"></a>Kiinteähintainen

Kun lähetetty peruskulumerkintä on linkitetty projektiin, joka on yhdistetty kiinteähintaiseen sopimusriviin, järjestelmä luo yhden kirjauskansion rivin kustannusta varten.

### <a name="default-pricing"></a>Oletushinnoittelu

Kulujen oletushintojen syöttämiseen liittyvä logiikka perustuu kululuokkaan. Sopivan hinnaston määrittämisessä käytetään tapahtuman päiväystä, sopimusriviin yhdistettyä projektia ja valuuttaa. Oletushintoihin vaikuttavia kenttiä, kuten **Tapahtumaluokka** ja **Yksikkö** käytetään kirjauskansion rivin sopivan hinnan määrittämiseen. Tämä toimii kuitenkin vain, jos hinnaston hinnoittelutapa on **Yksikköhinta**. Jos hinnoittelutapa on **Kustannuksen arvo** tai **Hinnankorotus kustannukselle**, hintaa, joka syötetään, kun kulumerkintä luodaan, käytetään kustannukselle ja myyntikirjauskansion rivi lasketaan hinnoittelutavan perusteella. 

Voit lisätä kulumerkintään mukautetun kentän. Jos haluat, että kentän arvo välitettään toteutuneisiin arvoihin, luo kenttä **Toteutuneet**- ja **Kirjausrivi**-taulukoihin. Käytä mukautettua koodia, kun haluat välittää valitun kentän arvon ajan syötöstä toteutuneisiin arvoihin kirjausrivin kautta käyttämällä tapahtumien alkuperää. Lisätietoja tapahtumien alkuperästä ja yhteyksistä on ohjeaiheessa [Toteutuneidenarvojen linkittäminen alkuperäisiin tietueisiin](linkingactuals.md#example-how-transaction-origin-works-with-transaction-connection).

## <a name="journal-lines-and-material-usage-log-submission"></a>Kirjauskansion rivien ja materiaalin käyttölokien lähettäminen

Lisätietoja kulumerkinnästä on kohdassa [Materiaalin käyttöloki](../material/material-usage-log.md).

### <a name="time-and-materials"></a>Aika ja materiaalit

Kun lähetetty materiaalin käyttölokin kirjaus linkitetään projektiin, joka on yhdistetty ajan ja materiaalien sopimusriviin, järjestelmä luo kaksi kirjauskansion riviä, yhden kustannuksille ja toisen laskuttamattomalle myynnille.

### <a name="fixed-price"></a>Kiinteähintainen

Kun lähetetty materiaalin käyttölokin kirjaus on linkitetty projektiin, joka on yhdistetty kiinteähintaiseen sopimusriviin, järjestelmä luo yhden kirjauskansion rivin kustannusta varten.

### <a name="default-pricing"></a>Oletushinnoittelu

Materiaalin oletushintojen syöttämisen logiikka perustuu tuotteen ja yksikön yhdistelmään. Sopivan hinnaston määrittämisessä käytetään tapahtuman päiväystä, sopimusriviin yhdistettyä projektia ja valuuttaa. Oletushintoihin vaikuttavia kenttiä, kuten **Tuotetunnus** ja **Yksikkö** käytetään kirjauskansion rivin sopivan hinnan määrittämiseen. Tämä koskee kuitenkin vain luettelotuotteita. Lisätyille tuotteille hintaa, joka syötetään, kun materiaalin käyttölokin kirjaus luodaan, käytetään kustannuksen ja myyntihinnan kirjauskansioriveillä. 

Voit lisätä **materiaalin käyttölokin** kirjaukseen mukautetun kentän. Jos haluat, että kentän arvo välitettään toteutuneisiin arvoihin, luo kenttä **Toteutuneet**- ja **Kirjausrivi**-taulukoihin. Käytä mukautettua koodia, kun haluat välittää valitun kentän arvon ajan syötöstä toteutuneisiin arvoihin kirjausrivin kautta käyttämällä tapahtumien alkuperää. Lisätietoja tapahtumien alkuperästä ja yhteyksistä on ohjeaiheessa [Toteutuneidenarvojen linkittäminen alkuperäisiin tietueisiin](linkingactuals.md#example-how-transaction-origin-works-with-transaction-connection).

## <a name="use-entry-journals-to-record-costs"></a>Tapahtumakirjauskansioiden käyttö kustannusten tallentamiseen

Tapahtumakirjauskansioihin voit tallentaa kustannuksia tai tuottoja luokkiin materiaali, maksu, kulu ja verotapahtuma. Kirjauskansioita voi käyttää seuraaviin tarkoituksiin:

- Siirrä tapahtumien todelliset arvot toisesta järjestelmästä Microsoft Dynamics 365 Project Operations -ohjelmaan.
- Tallenna kustannukset, jotka tapahtuivat toisessa järjestelmässä. Nämä kustannukset voivat sisältää hankinta- tai alihankintakustannuksia.

> [!IMPORTANT]
> Sovellus ei tarkista päiväkirjan rivin tyyppiä tai siihen liittyvää hinnoittelua, joka on syötetty päiväkirjan riville. Siksi vain käyttäjä, joka on täysin tietoinen todellisten arvojen kirjanpidollisesta vaikutuksesta projekteihin, voi käyttää tapahtumakirjauskansioita todellisten arvojen luomiseen. Tämän kirjauskansiotyypin vaikutuksen vuoksi sinun on valittava huolellisesti, kenellä on oikeus luoda tapahtumakirjauskansioita.

## <a name="record-actuals-based-on-project-events"></a>Todellisten arvojen tallentaminen projektitapahtumien perusteella

Project Operations tallentaa projektin aikana esiintyvät taloudelliset tapahtumat. Nämä tapahtumat kirjataan muodossa Todelliset arvot. Seuraavissa taulukoissa esitetään todellisten arvojen eri tyypit, jotka luodaan sen perusteella, onko projekti aika ja materiaalit -projekti vai kiinteähintainen projekti, onko se myyntiä edeltävässä vaiheessa vai onko se sisäinen projekti.

### <a name="the-resource-belongs-to-same-organizational-unit-as-the-projects-contracting-unit"></a>Resurssi kuuluu samaan organisaatioyksikköön kuin projektin sopimusyksikkö

<table>
<thead>
<tr>
<th rowspan="3">Tapahtuma</th>
<th colspan="4">Laskutettava tai myyty projekti</th>
<th rowspan="3">Projekti myyntiä edeltävässä vaiheessa</th>
<th rowspan="3">Sisäinen projekti</th>
</tr>
<tr>
<th colspan="2">Aika ja materiaalit</th>
<th colspan="2">Kiinteähintainen</th>
</tr>
<tr>
<th>Todelliset arvot</th>
<th>Tapahtumavaluutta</th>
<th>Kiinteähintainen</th>
<th>Tapahtumavaluutta</th>
</tr>
</thead>
<tbody>
<tr>
<td>Aikamerkintä luodaan.</td>
<td colspan="6">Ei toimintaa Todelliset arvot -entiteetissä</td>
</tr>
<tr>
<td>Aikamerkintä lähetetään.</td>
<td colspan="6">Ei toimintaa Todelliset arvot -entiteetissä</td>
</tr>
<tr>
<td rowspan="2">Aika hyväksytään eikä laskutettavia tunteja muuteta hyväksynnän aikana.</td>
<td>Kulujen todellinen arvo</td>
<td>Sopimusyksikön valuutta</td>
<td rowspan="2">Kulujen todellinen arvo</td>
<td rowspan="2">Sopimusyksikön valuutta
<td rowspan="2">Kulujen todellinen arvo</td>
<td rowspan="2">Kulujen todellinen arvo</td>
</tr>
<tr>
<td>Laskuttamattoman myynnin todellinen arvo – laskutettava</td>
<td>Projektisopimuksen valuutta</td>
</tr>
<tr>
<td rowspan="3">Aika hyväksytään ja laskutettavia tunteja vähennetään hyväksynnän aikana.</td>
<td>Kulujen todellinen arvo</td>
<td>Sopimusyksikön valuutta</td>
<td rowspan="3">Kulujen todellinen arvo</td>
<td rowspan="3">Sopimusyksikön valuutta</td>
<td rowspan="3">Kulujen todellinen arvo</td>
<td rowspan="3">Kulujen todellinen arvo</td>
</tr>
<tr>
<td>Laskuttamattoman myynnin todellinen arvo – laskutetaan uuden määrän perusteella</td>
<td>Projektisopimuksen valuutta</td>
</tr>
<tr>
<td>Laskuttamattoman myynnin todellinen arvo – erotusta ei laskuteta</td>
<td>Projektisopimuksen valuutta</td>
</tr>
<tr>
<td rowspan="2">Lasku vahvistetaan eikä laskutettavia tunteja muuteta.</td>
<td>Laskuttamattoman myynnin palautus</td>
<td>Projektisopimuksen valuutta</td>
<td rowspan="2">Välitavoitteen laskutettu myynti</td>
<td rowspan="2">Projektisopimuksen valuutta</td>
<td rowspan="2">Ei käytettävissä</td>
<td rowspan="2">Ei käytettävissä</td>
</tr>
<tr>
<td>Laskutettu myynti</td>
<td>Projektisopimuksen valuutta</td>
</tr>
<tr>
<td rowspan="3">Lasku vahvistetaan ja laskutettavia tunteja vähennetään.</td>
<td>Laskuttamattoman myynnin palautus</td>
<td>Projektisopimuksen valuutta</td>
<td rowspan="3">Ei käytettävissä</td>
<td rowspan="3">Ei käytettävissä</td>
<td rowspan="3">Ei käytettävissä</td>
<td rowspan="3">Ei käytettävissä</td>
</tr>
<tr>
<td>Laskutettu myynti – laskutetaan uuden määrän perusteella</td>
<td>Projektisopimuksen valuutta</td>
</tr>
<tr>
<td>Laskutettu myynti – erotusta ei laskuteta</td>
<td>Projektisopimuksen valuutta</td>
</tr>
<tr>
<td rowspan="2">Laskua korjataan laskutettavan summan suurentamiseksi.</td>
<td>Laskutettu myynti – palautus</td>
<td>Projektisopimuksen valuutta</td>
<td rowspan="5">
<ul>
<li>Välitavoitteen laskutetun myynnin palautus</li>
<li>Välitavoitteen tila muuttuu tilasta <strong>Laskutettu</strong> tilaan <strong>Valmis laskutukseen</strong></li>
</ul>
</td>
<td rowspan="5">Projektisopimuksen valuutta</td>
<td rowspan="5">Ei käytettävissä</td>
<td rowspan="5">Ei käytettävissä</td>
</tr>
<tr>
<td>Laskutettu myynti</td>
<td>Projektisopimuksen valuutta</td>
</tr>
<tr>
<td rowspan="3">Laskua korjataan laskutettavan summan pienentämiseksi.</td>
<td>Laskutettu myynti – palautus</td>
<td>Projektisopimuksen valuutta</td>
</tr>
<tr>
<td>Uuden määrän laskutettu myynti</td>
<td>Projektisopimuksen valuutta</td>
</tr>
<tr>
<td>Laskuttamaton myynti – erotus laskutetaan</td>
<td>Projektisopimuksen valuutta</td>
</tr>
</tbody>
</table>

### <a name="the-resource-belongs-to-an-organizational-unit-that-differs-from-the-projects-contracting-unit"></a>Resurssi kuuluu muuhun organisaatioyksikköön kuin projektin sopimusyksikköön

<table>
<thead>
<tr>
<th rowspan="3">Tapahtuma</th>
<th colspan="4">Laskutettava tai myyty projekti</th>
<th rowspan="3">Projekti myyntiä edeltävässä vaiheessa</th>
<th rowspan="3">Sisäinen projekti</th>
</tr>
<tr>
<th colspan="2">Aika ja materiaalit</th>
<th colspan="2">Kiinteähintainen</th>
</tr>
<tr>
<th>Todelliset arvot</th>
<th>Tapahtumavaluutta</th>
<th>Kiinteähintainen</th>
<th>Tapahtumavaluutta</th>
</tr>
</thead>
<tbody>
<tr>
<td>Aikamerkintä luodaan.</td>
<td colspan="6">Ei toimintaa Todelliset arvot -entiteetissä</td>
</tr>
<tr>
<td>Aikamerkintä lähetetään.</td>
<td colspan="6">Ei toimintaa Todelliset arvot -entiteetissä</td>
</tr>
<tr>
<td rowspan="4">Aika hyväksytään eikä laskutettavia tunteja muuteta hyväksynnän aikana.</td>
<td>Kulujen todellinen arvo</td>
<td>Sopimusyksikön valuutta</td>
<td rowspan="4">Kulujen todellinen arvo</td>
<td rowspan="4">Sopimusyksikön valuutta</td>
<td rowspan="4">Kulujen todellinen arvo</td>
<td rowspan="4">Kulujen todellinen arvo</td>
</tr>
<tr>
<td>Laskuttamattoman myynnin todellinen arvo – laskutettava</td>
<td>Projektisopimuksen valuutta</td>
</tr>
<tr>
<td>Resursointiyksikön kustannus</td>
<td>Resursointiyksikön valuutta</td>
</tr>
<tr>
<td>Organisaatioiden välinen myynti</td>
<td>Sopimusyksikön valuutta</td>
</tr>
<tr>
<td rowspan="5">Aika hyväksytään ja laskutettavia tunteja vähennetään hyväksynnän aikana.</td>
<td>Kulujen todellinen arvo</td>
<td>Sopimusyksikön valuutta</td>
<td rowspan="5">Kulujen todellinen arvo</td>
<td rowspan="5">Sopimusyksikön valuutta</td>
<td rowspan="5">Kulujen todellinen arvo</td>
<td rowspan="5">Kulujen todellinen arvo</td>
</tr>
<tr>
<td>Resursointiyksikön kustannus</td>
<td>Resursointiyksikön valuutta</td>
</tr>
<tr>
<td>Organisaatioiden välinen myynti</td>
<td>Sopimusyksikön valuutta</td>
</tr>
<tr>
<td>Laskuttamattoman myynnin todellinen arvo – laskutetaan uuden määrän perusteella</td>
<td>Projektisopimuksen valuutta</td>
</tr>
<tr>
<td>Laskuttamattoman myynnin todellinen arvo – erotusta ei laskuteta</td>
<td>Projektisopimuksen valuutta</td>
</tr>
<tr>
<td rowspan="2">Lasku vahvistetaan eikä laskutettavia tunteja muuteta.</td>
<td>Laskuttamattoman myynnin palautus</td>
<td>Projektisopimuksen valuutta</td>
<td rowspan="2">Välitavoitteen laskutettu myynti</td>
<td rowspan="2">Projektisopimuksen valuutta</td>
<td rowspan="2">Ei käytettävissä</td>
<td rowspan="2">Ei käytettävissä</td>
</tr>
<tr>
<td>Laskutettu myynti</td>
<td>Projektisopimuksen valuutta</td>
</tr>
<tr>
<td rowspan="3">Lasku vahvistetaan ja laskutettavia tunteja vähennetään.</td>
<td>Laskuttamattoman myynnin palautus</td>
<td>Projektisopimuksen valuutta</td>
<td rowspan="3">Ei käytettävissä</td>
<td rowspan="3">Ei käytettävissä</td>
<td rowspan="3">Ei käytettävissä</td>
<td rowspan="3">Ei käytettävissä</td>
</tr>
<tr>
<td>Laskutettu myynti – laskutetaan uuden määrän perusteella</td>
<td>Projektisopimuksen valuutta</td>
</tr>
<tr>
<td>Laskutettu myynti – erotusta ei laskuteta</td>
<td>Projektisopimuksen valuutta</td>
</tr>
<tr>
<td rowspan="2">Laskua korjataan laskutettavan summan suurentamiseksi.</td>
<td>Laskutettu myynti – palautus</td>
<td>Projektisopimuksen valuutta</td>
<td rowspan="5">
<ul>
<li>Välitavoitteen laskutetun myynnin palautus</li>
<li>Välitavoitteen tila muuttuu tilasta <strong>Laskutettu</strong> tilaan <strong>Valmis laskutukseen</strong></li>
</ul>
</td>
<td rowspan="5">Projektisopimuksen valuutta</td>
<td rowspan="5">Ei käytettävissä</td>
<td rowspan="5">Ei käytettävissä</td>
</tr>
<tr>
<td>Laskutettu myynti</td>
<td>Projektisopimuksen valuutta</td>
</tr>
<tr>
<td rowspan="3">Laskua korjataan laskutettavan summan pienentämiseksi.</td>
<td>Laskutettu myynti – palautus</td>
<td>Projektisopimuksen valuutta</td>
</tr>
<tr>
<td>Uuden määrän laskutettu myynti</td>
<td>Projektisopimuksen valuutta</td>
</tr>
<tr>
<td>Laskuttamaton myynti – erotus laskutetaan</td>
<td>Projektisopimuksen valuutta</td>
</tr>
</tbody>
</table>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
