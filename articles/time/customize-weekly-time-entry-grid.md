---
title: Aikamerkintöjen laajentaminen
description: Tässä aiheesa on tietoja siitä, miten kehittäjät voivat laajentaa aikamerkinnän ohjausobjektia.
author: stsporen
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 93f411ad7c86beefcc35e7799a03987dacdcd62b
ms.sourcegitcommit: 5a29adce48133e09f051929e8544d6c2c93c025d
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/02/2020
ms.locfileid: "3930876"
---
# <a name="extending-time-entries"></a>Aikamerkintöjen laajentaminen

_**Koskee:** Project Operationsin resurssiin / muuhun kuin resurssiin perustuvia skenaarioita, Lite-käyttöönotto-kaupasta proformalaskutukseen_

Dynamics 365 Project Operations sisältää laajennettavan ja mukautetun aikamerkinnän ohjausobjektin. Tämä ohjausobjekti sisältää seuraavat ominaisuudet:

- Syötä aika vaaka suunnassa koko viikolle
- Summat päivän, rivin tai viikon mukaan
- Rivien tai viikkojen kopioiminen
- Aikamerkintä muodossa HH:mm tai HH.hh (muuntaa automaattisesti muotoon to HH.hh)
- Tuonti delegoinneista, varauksista tai tapaamisista

Aikamerkintöjen laajentaminen on mahdollista kahdella alueella:
- [Mukautettujen aikamerkintöjen lisääminen omaan käyttöön](#add)
- [Viikoitteiasen aikamerkinnän ohjausobjektin mukauttaminen](#customize)

## <a name="add-custom-time-entries-for-your-own-use"></a><a name="add"></a>Mukautettujen aikamerkintöjen lisääminen omaan käyttöön.

Aikamerkinnät ovat perusentiteetti, joka on suunniteltu käytettäväksi useissa skenaarioissa. Huhtikuun 2020 1. julkaisuaallossa TESA-ydinratkaisu otettiin käyttöön, joka tarjoaa **Asetukset**-entiteetin ja uuden **Aikamerkinnän käyttäjä** -käyttöoikeusroolin. Myös uudet kentät, **msdyn_start** ja **msdyn_end**, joilla on suora suhde kenttään **msdyn_duration**, oli sisällytetty mukaan. Uusi entiteetti, käyttöoikeusrooli ja kentät mahdollistavat yhtenäisemmän lähetysmistavan aikamerkintöihin useiden tuotteiden välillä.


### <a name="time-source-entity"></a>Ajan lähde -entiteetti
| Field | Kuvaus | 
|-------|------------|
| Nimi  | Ajan lähde -merkinnän nimeä käytettiin valinta-arvona aikamerkinnän luonnin aikana. |
| Ajan oletuslähde [Time Source: isdefault] | Oletusarvon mukaan vain yksi aikalähde voidaan merkitä oletusaikalähteeksi. Tämä ominaisuus sallii merkintöjen oletusarvoksi aikalähteen, jos sellaista ei ole määritetty. |
|Aikalähteen tyyppi [Time Source: sourcetype] | Lähdetyyppi on asetus (aikamerkinnän lähdetyyppi), joka sallii aikalähteen liittämisen sovellukseen. Tähän asetusjoukkoon lisätään lisäarvoja, kun uusia sovelluksia lisätään. Huomaa, että Microsoft varaa arvot, jotka ovat suurempia kuin 190 000 000.|


### <a name="time-entries-and-the-time-source-entity"></a>Aikamerkinnät ja Ajan lähde -entiteetti
Kukun aikamerkintä liitetään aikalähteen tietueeseen. Tämä tietue määrittää, miten ja mitkä sovellukset käsittelevät aikamerkinnän.

Aikamerkinnät ovat aina yksi yhtenäinen aikalohko, johon on linkitetty alku, loppu ja kesto.

Logiikka päivittää aikamerkinnän tietueen automaattisesti seuraavissa tilanteissa:

- Jos kaksi seuraavista kolmesta kentästä on käytettävissä, kolmas lasketaan automaattisesti 

    - **msdyn_start**
    - **msdyn_end**
    - **msdyn_duration**

- Kentät **msdyn_start** ja **msdyn_end** ovat aikavyöhykeriippuvaisia.
- Aikamerkinnät, jotka on luotu vain **msdyn_date** ja **msdyn_duration** määrittämällä, alkavat keskiyöllä, ja **msdyn_start** ja **msdyn_end** päivittyvät vastaavasti.

#### <a name="time-entry-types"></a>Aikamerkinnän tyypit

Aikamerkinnän tietueisiin on liitetty tyyppi, joka määrittää käyttäytymisen liitetyn sovelluksen lähetystyönkulussa.

|Label | Arvo|
|-----|-----|
|Tauolla   |192,355,000|
|Matka | 192,355,001|
|Ylityö   | 192,354,320|
|Työ   | 192,350,000|
|Poissaolo    | 192,350,001|
|Loma   | 192,350,002|



## <a name="customize-the-weekly-time-entry-control"></a><a name="customize"></a>Viikoittaisen aikamerkinnän ohjausobjektin mukauttaminen
Sovelluskehittäjät voivat lisätä muita kenttiä ja hakuja muihin kohteisiin sekä ottaa käyttöön mukautettuja liiketoimintasääntöjä liiketoimintaskenaarioiden tueksi.

### <a name="add-custom-fields-with-lookups-to-other-entities"></a>Sellaisten mukautettujen kenttien lisääminen, joilla on hakuja muihin kohteisiin
Mukautetun kentän lisäämisessä viikoittaiseen ajansyöttöruudukkoon on kolme päävaihetta.

- Lisää mukautettu kenttä pikaluonti-valintaikkunaan.
- Määritä ruudukko näyttämään mukautettu kenttä.
- Lisää mukautettu kenttä joko rivin muokkaamisen tai solun muokkauksen työnkulkuun.

Varmista myös, että uudella kentällä on tarpeelliset kelpoisuustarkistukset rivin tai solun muokkauksen työnkulussa. Tässä vaiheessa kenttä täytyy lukita aikamerkinnän tilan perusteella.

#### <a name="add-the-custom-field-to-the-quick-create-dialog-box"></a>Lisää mukautettu kenttä pikaluonti-valintaikkunaan.
Lisää mukautettu kenttä **Aikamerkinnän pikaluonti** -valintaikkunaan. Käyttäjät voivat kirjoittaa arvon, kun he lisäävät aikamerkintöjä valitsemalla **Uusi**.

#### <a name="configure-the-grid-to-show-the-custom-field"></a>Määritä ruudukko näyttämään mukautettu kenttä.
Mukautettu kenttä voidaan lisätä viikoittaiseen ajansyöttöruudukkoon kahdella eri tavalla:

  - Näkymän mukauttaminen ja mukautetun kentän lisääminen
  - Uuden mukautetun oletusaikamerkinnän luominen 


**Näkymän mukauttaminen ja mukautetun kentän lisääminen**

Voit mukauttaa **Omat viikoittaiset aikamerkinnät** -näkymää lisäämällä siihen mukautetun kentän. Voit valita mukautetun kentän sijainnin ja koon ruudukossa muokkaamalla näitä näkymän ominaisuuksia.

**Uuden mukautetun oletusaikamerkinnän luominen** 

Tässä näkymässä tulisi olla kentät **Kuvaus** ja **Ulkoiset huomautukset** niiden sarakkeiden lisäksi, joita haluat ruudukkoon. 

1. Valitse mukautetun kentän sijainti, koko ja oletuslajittelujärjestys ruudukossa muokkaamalla näitä näkymän ominaisuuksia. 
2. Määritä tämän näkymän mukautettu ohjausobjekti siten, että se on **Ajansyöttöruudukon** ohjausobjekti. 
3. Lisää tämä ohjausobjekti näkymään ja valitse se verkolle, puhelimelle ja tabletille. 
4. Määritä viikoittaisen ajansyöttöruudukon parametrit. Aseta **Alkamispäivä**-kentäksi **msdyn_date**, aseta **Kesto**-kentäksi **msdyn_duration** ja aseta **Tila**-kentäksi **msdyn_entrystatus**. 
5. Oletusnäkymälle **Vain luku -tilaluettelo** -kentäksi on asetettu **192350002,192350003,192350004**, **Rivinmuokkauksen työnkulku** -kentäksi on asetettu **msdyn_timeentryrowedit** ja **Solunmuokkauksen työnkulku** -kentäksi on asetettu **msdyn_timeentryedit**. 
6. Voit mukauttaa näitä kenttiä, jos haluat lisätä tai poistaa vain luku -tilan tai käyttää toista tehtäväpohjaista kokemusta (TBX) rivien tai solujen muokkaamiseen. Nämä kentät on sidottava staattiseen arvoon.


> [!NOTE] 
> Molemmat vaihtoehdot poistavat joitakin valmiina olevia suodattimia entiteeteistä **Projekti** ja **Projektitehtävä**, joten kaikki valintanäkymät ovat näkyvissä näille entiteeteille. Vain merkitykselliset valintanäkymät ovat näkyvissä valmiina.
Sinun täytyy määrittää mukautetulle kentälle asianmukainen työnkulku. Jos olet lisännyt kentän ruudukkoon, sen pitäisi todennäköisesti siirtyä siihen rivimuokkauksen työnkulkuun, jota käytetään kentissä, jotka koskevat koko aikamerkintäriviä Jos mukautetulla kentällä on ainutkertainen arvo joka päivä, kuten mukautetulla kentällä **Päättymisaika**, sen pitäisi siirtyä solunmuokkauksen työnkulkuun.

Jos haluat lisätä mukautetun kentän työnkulkuun, vedä **Kenttä**-elementti asianmukaiseen kohtaan sivulla ja valitse sitten kentän ominaisuudet. Määritä **Lähde**-ominaisuudeksi **Aikamerkintä** ja aseta **Tietokenttä**-ominaisuus muokatulle kentälle. **Kenttä**-ominaisuus määrittää TBX-sivun näyttönimen. Valitse **Käytä**, jos haluat tallentaa muutokset kenttään, ja valitse sitten **Päivitä**, jos haluat tallentaa muutokset sivulla.

Jos haluat käyttää uutta mukautettua TBX-sivua, luo uusi prosessi. Määritä luokaksi **Liiketoimintaprosessin kulku**, aseta entiteetiksi **Aikakirjaus**, ja aseta liiketoimintaprosessityypiksi **Aja prosessi työnkulkuna**. **Ominaisuuksissa** **Sivun nimi** -ominaisuuden tulisi olla asetettu sivun näyttönimeksi. Lisää kaikki tarvittavat kentät TBX-sivulle. Tallenna ja aktivoi prosessi ja päivitä sitten kyseisen tehtävänkulun mukautetun ohjausobjektin ominaisuus prosessin **Nimen** arvoksi.

### <a name="add-new-option-set-values"></a>Lisää uusia asetusjoukkoarvoja
Jos haluat lisätä asetusjoukkoarvoja valmiina olevaan kentään, avaa kentän muokkaussivu ja valitse sen jälkeen **Kirjoita**-kohdassa **Muokkaa** asetusjoukon vieressä. Lisää seuraavaksi uusi asetus, jolla on mukautettu selite ja väri. Jos haluat lisätä uuden aikamerkinnän tilan, valmiin kentän nimi on  **Merkinnän tila**, ei **Tila**.

### <a name="designate-a-new-time-entry-status-as-read-only"></a>Uuden aikakirjaustilan määrittäminen vain luku -tilaan
Jos haluat määrittää uuden aikamerkinnän tilaksi vain luku, lisää uuden aikamerkinnän arvo **Vain luku -tilaluettelo** -ominaisuuteen. Ajansyöttöruudukon muokattava osa lukitaan riveille, joilla on uusi tila.
Lisää seuraavaksi liiketoimintasäännöt lukitaksesi kaikki kentät **Aikamerkintärivin muokkaus** -ja **Aikamerkinnän muokkaus** -TBX-sivuilla. Pääset sivujen liiketoimintasääntöihin avaamalla sivun liiketoimintaprosessieditorin ja valitsemalla sitten **Liiketoimintasäännöt**. Voit lisätä uuden tilan aiemmin luotujen liiketoimintasääntöjen ehtoon tai voit lisätä uuden liiketoimintasäännön uutta tilaa varten.

### <a name="add-custom-validation-rules"></a>Mukautettujen vahvistussääntöjen lisääminen
Voit lisätä viikoittaiseen aikamerkinnän ruudukkokokemukseen kahdentyyppisiä tarkistussääntöjä:

- Asiakaspuolen liiketoimintasäännöt, jotka toimivat pikaluontivalintaikkunoissa ja TBX-sivuilla.
- Palvelinpuolen laajennuksen tarkistukset, jotka koskevat kaikkia aikamerkinnän päivityksiä.

#### <a name="business-rules"></a>Liiketoimintasäännöt
Liiketoimintasääntöjen avulla voit lukita ja vapauttaa kenttiä, kirjoittaa oletusarvoja kenttiin ja määrittää vahvistuksia, jotka edellyttävät tietoja vain nykyisestä ajansyöttötietueesta. Pääset TBX-sivun liiketoimintasääntöihin avaamalla sivun liiketoimintaprosessieditorin ja valitsemalla sitten **Liiketoimintasäännöt**. Voit sitten muokata aiemmin luotuja liiketoimintasääntöjä tai lisätä uuden liiketoimintasäännön. Voit käyttää liiketoimintasääntöä ajamaan JavaScriptiä luodaksesi vielä mukautetumpia vahvistuksia.

#### <a name="plug-in-validations"></a>Laajennusvahvistukset
Käytä laajennusvahvistuksia kaikkiin vahvistuksiin, jotka edellyttävät enemmän kontekstia kuin on käytettävissä yksittäisessä aikakirjaustietueessa, tai kaikkiin vahvistuksiin, jotka haluat suorittaa tekstisidonnaisina päivityksinä ruudukossa. Viimeistele vahvistus luomalla mukautettu laajennus **Aikakirjaus**-entiteettiin.
