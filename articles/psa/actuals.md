---
title: Toteutuneiden yleiskatsaus
description: Tässä artikkelissa on tietoja projektin todellisista arvoista.
author: rumant
ms.custom:
- dyn365-projectservice
- intro-internal
ms.date: 08/03/2020
ms.topic: overview
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.reviewer: johnmichalak
ms.openlocfilehash: 35282e6c51fff28dbbb0a5a7de760788416ed0e4
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8929072"
---
# <a name="actuals-overview"></a>Toteutuneiden yleiskatsaus

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Todelliset arvot vastaavat työmäärää, joka projektissa on suoritettu. Projektin todelliset arvot voidaan jäljittää lähdeasiakirjoihinsa. Lähdeasiakirjoja ovat aika, kulu, kirjauskansioviennit ja myös laskut.

![Projektin todellisten arvojen jäljittäminen lähdeasiakirjoihin.](media/basic-guide-18.png)

## <a name="submitting-a-time-entry"></a>Aikamerkinnän lähettäminen

Kun PSA:ssa lähetetään sellaisen projektin aikamerkintä, joka on yhdistetty aika ja materiaalit -sopimusriviin, luodaan kaksi kirjauskansion riviä. Yksi rivi on kustannusta ja toinen laskuttamatonta myyntiä varten. Kun lähetetään sellaisen projektin aikamerkintä, joka on yhdistetty kiinteähintaiseen sopimusriviin, luodaan kirjauskansion rivi vain kustannusta varten. 

Oletushintojen antamisen logiikka on kirjauskansion rivillä. Kaikkien aikamerkinnän kenttien arvot kopioidaan kirjauskansion riville. Nämä kentät sisältävät tapahtuman päiväyksen, sopimusriviin yhdistetyn projektin ja valuuttatuloksen asianmukaisessa hinnastossa. 

Oletushintoihin vaikuttavat kentät, kuten **Rooli** ja **Organisaatioyksiköt** varmistavat, että kirjauskansion riville täytetään oletusarvoisesti asianmukainen hinta. Jos lisäät aikamerkintään muokatun kentän ja haluat, että kentän arvo välitetään todellisiin arvoihin, luo kenttä Todelliset arvot -entiteettiin ja käytä kenttien yhdistämistä kopioidaksesi kentän aikamerkinnästä todelliseen arvoon.

## <a name="submitting-an-expense-entry"></a>Kulumerkinnän lähettäminen

Kun PSA:ssa lähetetään sellaisen projektin kulumerkintä, joka on yhdistetty aika ja materiaalit -sopimusriviin, luodaan kaksi kirjauskansion riviä. Yksi rivi on kustannusta ja toinen laskuttamatonta myyntiä varten. Kun lähetetään sellaisen projektin kulumerkintä, joka on yhdistetty kiinteähintaiseen sopimusriviin, luodaan kirjauskansion rivi vain kustannusta varten.

Kulujen oletushintojen antamisen logiikka perustuu kululuokkaan, joka valitaan **Kulumerkintä**-sivulla. Oikean hinnaston määrittämisessä käytetään tapahtuman päiväystä, sopimusriviin yhdistettyä projektia ja valuuttaa. Itse hinnan osalta käyttäjän antama summa asetetaan oletusarvoisesti suoraan siihen liittyvien kulujen kirjauskansion kustannus- ja myyntirivien arvoksi.

Nykyisessä PSA:n versiossa, luokkaperusteista merkintää yksikkökohtaisista kulumerkintöjen oletushinnoista ei ole käytettävissä.

## <a name="using-entry-journals-to-record-costs"></a>Kirjauskansioiden käyttö kustannusten tallentamiseen

PSA:ssa kirjauskansioihin voi tallentaa kustannuksia tai tuottoja materiaali-, maksu-, aika-, kulu- ja verotapahtumaluokkiin. Kirjauskansiossa on otsikko, rivejä ja **Vahvista**-toiminto. Seuraavassa on skenaarioita, joissa saatetaan käyttää kirjauskansiota:

- Sinun on tallennettava projektin materiaalien todellisia kustannuksia ja myyntejä.
- Sinun on siirrettävä tapahtumien todellisia arvoja toisesta järjestelmästä PSA:han.
- Sinun on tallennettava toisessa järjestelmässä aiheutuneita kustannuksia, kuten hankinta- tai alihankintakustannuksia.

> [!IMPORTANT]
> Toteutuneiden luonti kirjauskansioiden avulla sopii vain sellaiselle käyttäjälle, joka on täysin tietoinen siitä, mikä kirjanpitovaikutus toteutuneilla on projektiin. Syynä on se, että sovellus ei tarkista kirjauskansion rivityyppiä tai kirjauskansion rivillä annettua liittyvää hinnoittelua. Tämän kirjauskansiotyypin vaikutuksen vuoksi onkin harkittava riittävän tarkasti, kenelle tämän kirjauskansion luontioikeus annetaan.     


## <a name="recording-actuals-based-on-project-events"></a>Todellisten arvojen tallentaminen projektitapahtumien perusteella

PSA tallentaa projektin aikana esiintyvät taloudelliset tapahtumat. Nämä tapahtumat kirjataan muodossa **Todelliset arvot**. Seuraavissa taulukoissa esitetään todellisten arvojen eri tyypit, jotka luodaan sen perusteella, onko projekti aika ja materiaalit -projekti vai kiinteähintainen projekti, onko se myyntiä edeltävässä vaiheessa vai onko se sisäinen projekti.

**Resurssi kuuluu samaan organisaatioyksikköön kuin projektin sopimusyksikkö**

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

**Resurssi kuuluu muuhun organisaatioyksikköön kuin projektin sopimusyksikköön**

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
