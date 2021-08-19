---
title: Projektisopimukset
description: Tässä aiheessa on esimerkkejä projektisopimuksista, joita voi luoda erityyppisille projekteille ja rahoituslähteille, sekä siitä, miten voit hallita palvelusopimuksia ja laskuttaa projektiasiakkaita.
author: Yowelle
ms.date: 11/03/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ProjProjectContractsListPage, ProjProjectsListPage
audience: Application User, IT Pro
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 23561
ms.assetid: bfd18d9b-d9a6-4e21-bc95-bf4af45f617f
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1b92668c38071e8b1afdee9a79fd4a25190248ada30380bfb79054a6dc587f95
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/06/2021
ms.locfileid: "7001022"
---
# <a name="project-contracts"></a>Projektisopimukset

[!include [banner](../includes/banner.md)]

Tässä artikkelissa on esimerkkejä projektisopimuksista, joita voi luoda erityyppisille projekteille ja rahoituslähteille, sekä siitä, miten voit hallita palvelusopimuksia ja laskuttaa projektiasiakkaita.

Projektisopimukselle luotavan projektin tyyppi määrittää menetelmän, jota käytetään projektiasiakkaiden laskutukseen. Voit muuttaa projektisopimusta ja siihen liittyvää projektia, mutta et voi muuttaa projektityyppiä. 

Projektisopimuksen avulla voit laskuttaa yhtä tai useampaa projektia samalla kertaa. Projektisopimus auttaa myös takaamaan yhdenmukaisen laskutusmenettelyn jokaiselle projektirakenteen aliprojektille. 

Kaikki laskutettavat projektit on liitettävä projektisopimukseen. Projektisopimuksen asetukset koskevat kaikkia kyseiseen projektisopimukseen liittyviä projekteja ja aliprojekteja. 

Projektisopimuksessa voi määrittää yhden tai useamman rahoituslähteen. Siksi voit jakaa laskutuksen useiden rahoittajien kesken, määrittää rahoitusrajat siten, että rahoituslähteitä ei laskuteta enempää kuin määritetty summa, ja määrittää kulujen maksujen rahoitussäännöt.

## <a name="funding-for-project-contracts"></a>Projektisopimusten rahoitus
Jotkin projektisopimukset määrittävät, että useat osapuolet jakavat vastuun projektikustannusten rahoittamisesta. Seuraavassa on joitakin esimerkkejä.

-   Suuri asiakas, jolla on useita osastoja, pyytää, että projektin rahoittaminen jaetaan osaston mukaan.
-   Yritys jakaa suuren projektin kustannukset ulkoisen organisaation kanssa.
-   Tiehanketta rahoittaa kaksi kuntaa.
-   Siltaprojektia rahoittaa julkinen avustus ja yksityinen yritys.

Dynamics 365 Financessa voit jakaa yksittäisen tapahtuman tai koko projektin laskutuksen useiden asiakkaiden, apurahojen tai organisaatioiden kesken. 

Projekteissa, joissa on useita rahoittajia, kaikkia edistyneen rahoitusprojektin rahoittamiseen osallistuvia osapuolia kutsutaan rahoituslähteiksi. Kun asiakas, organisaatio tai apuraha on määritetty rahoituslähteeksi, se voidaan delegoida yhteen tai useampaan rahoitussääntöön. Rahoitussäännöt sisältävät ehdot, jotka määrittävät, miten maksut kohdistetaan projektin eri rahoituslähteisiin. 

Koska esimerkiksi ostoehdotuksissa ja ostotilauksissa näkyviä varastonimikkeitä ei voi jakaa, kustannusten määrää ei voi jakaa useiden rahoituslähteiden kesken jakelun aikana. Tämän vuoksi rahoituslähteen arvo on 0 (nolla), kunnes varasto-ongelma on kirjattu. Kun varastokysymys kirjataan, kustannusten summa jaetaan projektin tilin jakelusääntöjen mukaan.

Seuraavassa on joitakin vaiheita, joilla voit helpottaa laskutuksen jakamista useiden rahoituslähteiden kesken:

-   Määritä, että kaikki projektiin lisätyt tapahtumat käyttävät samaa myyntivaluuttaa kuin projektisopimus.
-   Määritä rahoitusrajat, jotta rahoituslähdettä ei laskuteta enempää kuin määritetty summa projektia kohti.
-   Määritä rahoitussäännöt ja rahoitusrajat kullekin työntekijälle, nimikkeelle, luokalle, luokkaryhmälle ja tapahtumatyypille (tai kaikille tapahtumatyypeille).
-   Valitse valinnaiset alkamis- ja päättymispäivämäärät, kun haluat määrittää ajanjakson, jolloin kukin rahoitussääntö on voimassa.
-   Määritä prosenttiosuus, josta kukin rahoituslähde on vastuussa.
-   Määritä, mikä rahoituslähde on vastuussa rahoituksen kohdistuslaskelmien aiheuttamista pyöristyseroista.
-   Määritä säännöt, jotka määrittävät, miten projektin kustannukset laskutetaan ulkoisilta asiakkailta ja veloitetaan sisäisistä organisaatioista.
-   Voit kirjata tapahtumia pidossa olevaan rahoitustiliin, kunnes saat lisärahoitusta tai päätät maksaa kustannukset sisäisesti.

Voit määrittää tapahtumaan liitettävän veroryhmän, kun projektia haetaan veroryhmämääritykseksi. Jos veroryhmämääritystä ei ole tehty projektitasolla, projektisopimusta haetaan.

### <a name="example-multiple-funding-sources-simple"></a>Esimerkki: useita rahoituslähteitä (yksinkertainen)

Seuraavassa taulukossa on esitetty skenaarioita, joissa hallitaan rahoituksen jakamista useiden rahoituslähteiden kesken. Nämä skenaariot perustuvat seuraaviin oletuksiin:

-   Prioriteettiasetukset otetaan huomioon varojen kohdentamisessa, ennen kuin muita rahoitussäännön ehtoja käytetään.
-   Kauden d määrittämiseen ei ole määritetty päivämääräaluetta, kun rahoitussääntö on voimassa.

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<tbody>
<tr class="odd">
<td><strong>Skenaario</strong></td>
<td><strong>Rahoituslähde</strong></td>
<td><strong>Kohdistusprosentti</strong></td>
<td><strong>Kohdistuksen prioriteetti</strong></td>
</tr>
<tr class="even">
<td>Jos haluat kohdistaa kustannukset yhteen rahoituslähteeseen, kunnes sen varat ovat loppuneet, kohdista kustannukset toiseen rahoituslähteeseen, kunnes sen varat ovat loppuneet, ja varaa lopuksi loput kustannukset kolmannelle rahoituslähteelle.</td>
<td><ul>
<li>Rahoituslähde　1</li>
<li>Rahoituslähde　2</li>
<li>Rahoituslähde　3</li>
</ul></td>
<td><ul>
<li>100%</li>
<li>100%</li>
<li>100%</li>
</ul></td>
<td><ul>
<li>1</li>
<li>2</li>
<li>3</li>
</ul></td>
</tr>
<tr class="odd">
<td>Haluat kohdistaa 75 prosenttia kustannuksista yhteen rahoituslähteeseen ja 25 prosenttia toiseen rahoituslähteeseen. Kun jompikumpi näistä rahoituslähteistä on täyttynyt, haluat maksaa jäljellä olevat kustannukset kolmannesta rahoituslähteestä.</td>
<td><ul>
<li>Rahoituslähde　1</li>
<li>Rahoituslähde　2</li>
<li>Rahoituslähde　3</li>
</ul></td>
<td><ul>
<li>75 %</li>
<li>25 %</li>
<li>100%</li>
</ul></td>
<td><ul>
<li>1</li>
<li>1</li>
<li>2</li>
</ul></td>
</tr>
<tr class="even">
<td>Haluat kohdistaa 75 prosenttia kustannuksista yhteen rahoituslähteeseen ja 25 prosenttia toiseen rahoituslähteeseen. Kun jompikumpi näistä rahoituslähteistä on täyttynyt, haluat jakaa jäljellä olevat kustannukset kolmannen rahoituslähteen ja neljännen rahoituslähteen välillä.</td>
<td><ul>
<li>Rahoituslähde　1</li>
<li>Rahoituslähde　2</li>
<li>Rahoituslähde　3</li>
<li>Rahoituslähde　4</li>
</ul></td>
<td><ul>
<li>75 %</li>
<li>25 %</li>
<li>50 %</li>
<li>50 %</li>
</ul></td>
<td><ul>
<li>1</li>
<li>1</li>
<li>2</li>
<li>2</li>
</ul></td>
</tr>
<tr class="odd">
<td>Haluat kohdistaa ensimmäiset 25 prosenttia kustannuksista yhteen rahoituslähteeseen ja loput toiseen rahoituslähteeseen.</td>
<td><ul>
<li>Rahoituslähde　1</li>
<li>Rahoituslähde　2</li>
</ul></td>
<td><ul>
<li>25 %</li>
<li>100%</li>
</ul></td>
<td><ul>
<li>1</li>
<li>2</li>
</ul></td>
</tr>
</tbody>
</table>

### <a name="example-multiple-funding-sources-complex"></a>Esimerkki: useita rahoituslähteitä (monimutkainen)

Käytössäsi on kolme rahoituslähdettä, joita haluat käyttää seuraavassa tilauksessa:

1.  Käytä rahoituslähdettä 2 ja rahoituslähdettä 3 samalla tavalla, kunnes rahoituslähde 2 on täyttynyt.
2.  Käytä edelleen rahoituslähdettä 3, kunnes se on käytetty loppuun.
3.  Käytä rahoituslähdettä 1, kun rahoituslähde 3 on täyttynyt.

Tämän tavoitteen saavuttamiseksi sinun on toimittava seuraavasti:

-   Määritä rahoituslähteen 2 ja rahoituslähteen 3 rahoitusrajat niiden summien osalta.
-   Luo seuraavat rahoitussäännöt:
    -   Sääntö 1 (prioriteetti 1): kohdistaa 50 prosenttia tapahtumista rahoituslähteeseen 2 ja 50 prosenttia rahoituslähteeseen 3.
    -   Sääntö 2 (prioriteetti 2): Varaa 100 prosenttia tapahtumista, jotka rahoitetaan lähteestä 3.
    -   Sääntö 3 (prioriteetti 3): Varaa 100 prosenttia tapahtumista, jotka rahoitetaan lähteestä 1.

Tämä asetus toimii, koska tapahtumia verrataan sääntöihin ja rajoituksiin ja määritetään, koskeeko jokin niistä tapahtumaa. Jos tapahtumalle ei ole erityisiä sääntöjä tai rajoituksia, käytetään Kaikki tapahtumat -sääntöä. Kaikki tapahtumat -sääntö vastaa kaikkia tapahtumia. 

Jos löytyi sääntö, joka vastaa jotakin tapahtumaa, säännössä määritettyä prosenttiosuutta käytetään ensin, mutta vasta kun vastaavat arvot on tarkistettu. Jos rajoitus on täyttynyt ja rahoituslähteen varat ovat loppuneet, rahoitusrajaan liittyvä rahoitussääntö jätetään huomiotta ja ohjelma tarkistaa seuraavan säännön. 

Joissakin tapauksissa vain osa tapahtumasta voidaan kohdistaa sääntöön. Tämä voi johtua siitä, että tapahtuman kohdistuksena saavutetaan raja. Tässä tapauksessa vain tietty summa kohdistetaan kyseisen säännön mukaan, kuten 50 prosenttia kuhunkin rahoituslähteeseen. Tämä koskee sääntöä 1, joka on kuvattu aiemmin tässä osassa. Loppuosa kohdistetaan järjestyksessä seuraavan säännön mukaan. 

Seuraavassa taulukossa tutkitaan yksityiskohtaisesti skenaariota.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><strong>Kohdistus</strong></td>
<td><strong>Tiedot</strong></td>
</tr>
<tr class="even">
<td>Rahoitussäännöt</td>
<td><ul>
<li>Sääntö 1 (prioriteetti 1): kaikki tapahtumat. Kohdista rahoituslähteelle 2 50 % ja rahoituslähteelle 3 50 %.</li>
<li>Sääntö 2 (prioriteetti 2): kaikki tapahtumat. Kohdista rahoituslähteelle 3 100 %.</li>
<li>Sääntö 3 (prioriteetti 2): kaikki tapahtumat. Kohdista rahoituslähteelle 1 100 %.</li>
</ul></td>
</tr>
<tr class="odd">
<td>Rahoitusrajat</td>
<td><ul>
<li>Rahoituslähde 1 raja = 10 000,00</li>
<li>Rahoituslähde 2 raja = 500,00</li>
<li>Rahoituslähde 3 raja = 750,00</li>
</ul></td>
</tr>
<tr class="even">
<td>Tapahtuma 1</td>
<td><strong>Tapahtumamäärä:</strong> 100,00<strong>Rahoitus:</strong> Tapahtuma maksetaan vain säännön 1 mukaisesti, koska tapahtuma on kokonaan maksettu sen jälkeen, kun sääntö 1 on otettu käyttöön. Tapahtuma rahoitetaan tasapuolisesti rahoituslähteen 2 ja rahoituslähteen 3 välillä.
<ul>
<li>Rahoituslähde 2: 50,00</li>
<li>Rahoituslähde 3: 50,00</li>
</ul></td>
</tr>
<tr class="odd">
<td>Tapahtuma 2</td>
<td><strong>Tapahtumamäärä:</strong>5 000,00<strong>Rahoitus:</strong> Tapahtuma maksetaan kaikkien kolmen säännön mukaisesti. <strong>Sääntö 1</strong>
<ul>
<li>Rahoituslähde 2: 450,00</li>
<li>Rahoituslähde 3: 450,00</li>
</ul>
<strong>Sääntö 2</strong>
<ul>
<li>Rahoituslähde 3: 250,00 (= 750,00 – 50,00 – 450,00)</li>
</ul>
<strong>Sääntö 3</strong>
<ul>
<li>Rahoituslähde1: 3 850,00 (= 5 000,00 – 450,00 – 450,00 – 250,00)</li>
</ul></td>
</tr>
<tr class="even">
<td>Kullekin rahoituslähteelle jaetut varat yhteensä</td>
<td><ul>
<li>Rahoituslähde 1: 3 850,00</li>
<li>Rahoituslähde 2: 500,00</li>
<li>Rahoituslähde 3: 750,00</li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="billing-rules"></a>Laskutussäännöt
Kun neuvottelemme projektisopimuksesta asiakkaan kanssa, voit määrittää, miten ja milloin voit laskuttaa asiakasta projektin töistä. Kun olet määrittänyt projektisopimuksen ja projektin, voit määrittää projektille laskutussäännöt. Laskutussäännöt perustuvat projektisopimuksessa määritettyihin projektin ehtoihin. Luotettavat laskutussäännöt määräytyvät sen mukaan, mitkä projektisopimuksen ehdot ja projektityyppi, kuten aika ja materiaali tai kiinteämääräinen hinta, liitetään laskutussääntöön. Voit luoda projektisopimukselle useamman kuin yhden laskutussäännön. Voit myös delegoida laskutussäännön useisiin projekteihin, jotka liittyvät samaan projektisopimukseen ja joilla on samankaltaiset laskutusehdot. 

Voit määrittää seuraavan tyyppisiä laskutussääntöjä:

-   **Toimitusyksikkö** – Laskuta asiakasta, kun toimitusyksikkö on valmis. Palvelusopimuksessa määritetään toimitusyksiköt.
-   **Edistyminen** – Laskuta asiakasta, kun olet suorittanut määritetyn prosenttiosuuden projektista. Voit määrittää laskutussäännön, joka laskee automaattisesti valmiin työn prosenttiosuuden, tai voit laskea valmiin työn prosenttimäärän ja asiakkaan laskutettavan summan manuaalisesti.
-   **Välitavoite** – Laskuta asiakasta projektin välitavoitteen koko määrästä, kun välitavoite saavutetaan.
-   **Maksu**: Laskuta palveluistasi asiakas- ja hallinnointipalkkio, joka on yleensä prosenttiosuus palvelujen kustannuksista.
-   **Aika ja materiaali** – Laskuta asiakasta projektissa käytettävän ajan ja materiaalin arvosta.

Voit määrittää kaikentyyppisille laskutussäännöille säilytysprosentin, joka vähennetään asiakaslaskuista, kunnes projekti saavuttaa sovitun vaiheen. Maksun säilytysprosentti määritetään projektisopimuksessa. Summa lasketaan myyntilaskun rivien yhteisarvon perusteella ja vähennetään siitä. 

**Ajan ja materiaalin** sekä **Edistymisen** laskutussääntöjen avulla voit määrittää laskutettavia luokkia. Laskutettavat luokat ilmaisevat tapahtumat, jotka tulisi sisällyttää myyntilaskuihin. 

Kun olet valmis laskuttamaan asiakasta, projektin laskutettava summa lasketaan laskutussääntöjen perusteella, ja projektin laskuehdotus luodaan. 

Seuraavissa osissa on esimerkkejä siitä, miten projektin laskutussääntöjä määritetään ja hallitaan.

### <a name="example-create-a-billing-rule-that-is-based-on-the-number-of-units-delivered"></a>Esimerkki: Luo laskutussääntö, joka perustuu toimitettujen yksiköiden määrään

Organisaatiosi tekee sopimuksen, jonka mukaan asiakkaan työntekijöillä on yhteensä viisi koulutustilaisuutta, joiden kustannus on 10 000 per koulutusjakso. Laskutat asiakasta jokaisen koulutusjakson jälkeen. 

Kun määrität palvelusopimuksen laskutussäännöt, käytä seuraavia arvoja:

-   Toimitusyksikkö on yksi koulutusjakso.
-   Yksikköhinta on 10 000 koulutusjaksoa kohti.
-   Yksiköiden kokonaismäärä on viisi koulutustilaisuutta.

Kun olet suorittanut yhden koulutusjakson, voit luoda 10 000 laskun ensimmäisestä toimitetusta yksiköstä ja lähettää laskun asiakkaalle.

### <a name="example-create-a-billing-rule-that-is-based-on-a-specified-percentage-of-project-completion-manual-calculation"></a>Esimerkki: sellaisen laskutussäännön luominen, joka perustuu tiettyyn prosenttiosuuteen projektin valmistumisesta (manuaalisesta laskennasta)

Organisaatiosi, ohjelmistokonsultointiyritys, tekee asiakkaan kanssa sopimuksen, joka kehittää tuotteen osan, jota asiakas kehittää. Organisaatiosi suostuu toimittamaan ohjelmistokoodin kuuden kuukauden aikana. Asiakas sitoutuu maksamaan organisaatiollesi yhteensä 100 000 työn hinnasta. Voit luoda laskutussäännön, joka laskuttaa asiakasta sopimuksessa määritetyn työn valmistumisprosentin perusteella.

-   Ensimmäisen kuukauden lopussa asiakkaan on selvitettävä valmiin työn prosenttiosuus. Kun asiakas on tarkistanut projektin, hän päättää, että projektista on 15 prosenttia valmis.
-   Voit luoda laskun, jonka summa on 15 000 (15 prosenttia 100 000:sta) ja lähettää sen asiakkaalle.

### <a name="example-create-a-billing-rule-that-is-based-on-a-specified-percentage-of-project-completion-automatic-calculation"></a>Esimerkki: sellaisen laskutussäännön luominen, joka perustuu tiettyyn prosenttiosuuteen projektin valmistumisesta (automaattisesta laskennasta)

Organisaatiosi, ohjelmistokehitysyritys, sitoutuu kehittämään asiakkaalle 30 000 palkanlaskentapaketin. Asiakas sitoutuu maksamaan organisaatiollesi suoritettujen töiden prosenttiosuuden perusteella. Arvioit, että projektin kustannukset ovat 20 000. Projektisopimus määrittää työluokat, joita käytät laskutusprosessissa. Voit määrittää laskutussäännöt, jotka laskevat automaattisesti kullekin luokalle valmiin työn prosenttimäärän laskusummat. Kullekin luokalle määritetään budjetti:

-   **Kehitys** – Kustannukset 15 000 ja liikevaihto 20 000
-   **Asennus** – Kustannukset 5 000 ja liikevaihto 10 000

Kun luot myyntilaskun ensimmäisen kerran, laskun summa lasketaan automaattisesti seuraavien tietojen perusteella:

-   Kuukauden kuluttua projektin työntekijä lähettää projektiraportin. Työntekijän tuntien kustannukset ovat 5 000 kehityksen ja 1 000 asennuksen osalta. Kehitystyöt ovat 33 prosenttisesti valmiina (5 000 todelliset kustannukset/15 000 budjettikustannukset), ja asennustyöt ovat 20 prosenttisesti valmiina (1 000 toteutuneet kustannukset/5 000 budjettikustannukset).
-   Laskun summa 8 667 lasketaan automaattisesti (33 prosenttia 20 000 + 20 prosenttia 10 000).
-   Voit luoda laskun, jonka summa on 8 667 ja lähettää sen asiakkaalle.

### <a name="example-create-a-billing-rule-that-is-based-on-agreed-upon-milestones"></a>Esimerkki: sellaisen laskutussäännön luominen, joka perustuu sovittuihin välitavoitteisiin

Organisaatiosi, liikkeenjohdon konsultointiyritys, sitoutuu tekemään markkinatutkimusta kuluttajatuotteesta, jota asiakas suunnittelee myyvänsä. Asiakas sitoutuu käyttämään palvelujasi kolmen kuukauden ajan maaliskuun alusta ja sitoutuu maksamaan organisaatiollesi 50 000. Projektissa on kolme virstanpylvästä:

-   Välitavoite 1: Kuluttajatietojen kerääminen – 31. maaliskuuta
-   Välitavoite 2: Kuluttajatietojen analysointi – 30. huhtikuuta
-   Välitavoite 3: Tuotteen kannattavuusehdotuksen esittäminen – 31. toukokuuta

Asiakas sitoutuu maksamaan organisaatiollesi 10 000 ensimmäisen välitavoitteen, 20 000 toisen välitavoitteen ja 20 000 kolmannen välitavoitteen osalta. 

Kun määrität projektisopimuksen, sitoudut laskuttamaan asiakasta valmiiden välitavoitteiden perusteella. Laskutussäännön asetuksissa on seuraavat vaiheet:

-   Määritä projektin välitavoitteet.
-   Määritä summa, joka asiakkaalta laskutetaan, kun kukin välitavoite on valmis.

Kun ensimmäinen välitavoite on valmis maaliskuun 31., merkitse välitavoite valmiiksi ja luo sitten lasku, jonka summa on 10 000 ja lähetä se asiakkaalle. Välitavoitteille ei voi luoda laskua, ennen kuin olet merkinnyt välitavoitteen valmiiksi.

### <a name="example-create-a-billing-rule-that-is-based-on-services-plus-a-management-fee"></a>Esimerkki: Luo palveluihin perustuva laskutussääntö ja hallinnointipalkkio

Organisaatiosi, liikkeenjohdon konsultointiyritys, sitoutuu tekemään markkinatutkimusta arvioidakseen asiakkaan, vähittäiskaupan yrityksen kehittämän tuotteen kannattavuutta. Sopimuksen ehdoissa täsmennetään, että tarjoat kolmen johtavan konsulttisi palveluja, jotka suorittavat tutkimuksen ajan ja materiaalien perusteella. Asiakas sitoutuu maksamaan 100 tunnissa, johon lisätään 10 prosentin hallinnointipalkkio projektille veloitettavista konsultointitunneista. 

Kun määrität projektisopimuksen, luo laskutussääntö, joka lisää 10 prosentin hallinnointipalkkion projektista veloitettavien konsultointituntien osalta. 

Kun luot asiakkaalle laskun, asiakkaalta laskutetaan 10 prosentin hallinnointipalkkio sekä konsultointiajan kustannukset. Jos esimerkiksi kolme konsulttia työskenteli projektissa yhteensä 200 tuntia, järjestelmä luo laskun, jonka summa on 22 000 seuraavan laskelman perusteella:

-   200 tuntia 100 tunnilta = 20 000
-   10 prosentin hallinnointimaksu = 2 000
-   Laskun kokonaismäärä = 22 000

Jos maksut verotetaan asiakkaalle ja valitset arvonlisäveroryhmän projektisopimuksessa, arvonlisäveroryhmä syötetään automaattisesti maksujen laskutussääntöön.

### <a name="example-create-a-billing-rule-for-the-value-of-time-and-materials"></a>Esimerkki: laskutussäännön luominen ajan ja materiaalien arvolle

Organisaatiosi, ohjelmistokonsultointiyritys, suostuu toimittamaan asiakkaalle ohjelmistokehitysprojektia varten viisi teknistä konsulttia seuraavan kuuden kuukauden ajaksi. Asiakas sitoutuu maksamaan 150 jokaisesta konsultointitunnista sekä toimistotarvikkeiden kustannuksista. Organisaatiosi lähettää laskun asiakkaalle kunkin kuukauden lopussa. 

Kun määrität projektisopimuksen, sitoudut laskuttamaan asiakasta kuukausittain projektin ajan ja materiaalin perusteella. Voit luoda laskutussäännön, joka sisältää seuraavat tiedot:

-   Sopimuskausi on kuusi kuukautta.
-   Konsultointiajan hinnaksi lasketaan 150 tunnissa.
-   Toimistotarvikkeet laskutetaan kustannustasolla, ja projektin kokonaiskustannukset eivät saa ylittää 10 000.
-   Luot asiakaslaskun kunkin kalenterikuukauden lopussa projektin aikana.

Ensimmäisen kuukauden aikana konsultit kirjaavat projektille yhteensä 800 tuntia. Projektista veloitettavien toimistotarvikkeiden kustannukset ovat 2 000. Tämän vuoksi voit kuukauden lopussa luoda laskun, jonka summa on 122 000. Siihen on laskettu 800 tuntia á 150, sekä 2 000 toimistotarvikkeista.





[!INCLUDE[footer-include](../includes/footer-banner.md)]