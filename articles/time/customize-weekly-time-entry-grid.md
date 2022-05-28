---
title: Aikamerkintöjen laajentaminen
description: Tässä aiheesa on tietoja siitä, miten kehittäjät voivat laajentaa aikamerkinnän ohjausobjektia.
author: stsporen
ms.date: 01/27/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: 6b91aecd76950d2bd37192d634c80ea98d08034e
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/14/2022
ms.locfileid: "8582982"
---
# <a name="extending-time-entries"></a>Aikamerkintöjen laajentaminen

_**Koskee:** Project Operationsin resurssiin / muuhun kuin resurssiin perustuvia skenaarioita, Lite-käyttöönotto-kaupasta proformalaskutukseen_

Dynamics 365 Project Operations sisältää laajennettavan ajansyötön mukautetun ohjausobjektin. Tämä ohjausobjekti sisältää seuraavat ominaisuudet:

- Syötä aika vaaka suunnassa koko viikolle
- Summat päivän, rivin tai viikon mukaan
- Rivien tai viikkojen kopioiminen
- Aikamerkintä muodossa HH:mm tai HH.hh (muuntaa automaattisesti muotoon to HH.hh)
- Tuonti delegoinneista, varauksista tai tapaamisista

Aikamerkintöjen laajentaminen on mahdollista kahdella alueella:
- [Mukautettujen aikamerkintöjen lisääminen omaan käyttöön](#add)
- [Viikoitteiasen aikamerkinnän ohjausobjektin mukauttaminen](#customize)

## <a name="add-custom-time-entries-for-your-own-use"></a><a name="add"></a>Mukautettujen aikamerkintöjen lisääminen omaan käyttöön

Aikamerkinnät ovat perusentiteetti, jota käytetään useissa skenaarioissa. Huhtikuussa 2020 julkaisuaalto 1:ssä TESA-ydinratkaisu otettiin käyttöön. TESAssa on **asetukset**-entiteetti ja uusi **aikamerkinnän käyttäjä** -käyttöoikeusrooli. Myös uudet kentät, **msdyn_start** ja **msdyn_end**, joilla on suora suhde kenttään **msdyn_duration**, oli sisällytetty mukaan. Uusi entiteetti, käyttöoikeusrooli ja kentät mahdollistavat yhtenäisemmän lähetysmistavan aikamerkintöihin useiden tuotteiden välillä.


### <a name="time-source-entity"></a>Ajan lähde -entiteetti
| Field | Kuvaus | 
|-------|------------|
| Nimi  | Ajan lähde -merkinnän nimeä käytettiin valinta-arvona, kun luotiin aikamerkintöjä. |
| Ajan oletuslähde [Time Source: isdefault] | Oletusarvon mukaan vain yksi aikalähde voidaan merkitä oletukseksi. Tämä sallii merkintöjen oletusarvoksi aikalähteen, jos sellaista ei ole määritetty. |
|Aikalähteen tyyppi [Time Source: sourcetype] | Lähdetyyppi on asetus (aikamerkinnän lähdetyyppi), joka sallii aikalähteen liittämisen sovellukseen. Microsoft varaa arvot, jotka ovat suurempia kuin 190 000 000.|


### <a name="time-entries-and-the-time-source-entity"></a>Aikamerkinnät ja Ajan lähde -entiteetti
Kukun aikamerkintä liitetään aikalähteen tietueeseen. Tämä tietue määrittää, mitkä sovellukset käsittelevät aikamerkinnän ja miten.

Aikamerkinnät ovat aina yksi yhtenäinen aikalohko, johon on linkitetty alku, loppu ja kesto.

Logiikka päivittää aikamerkinnän tietueen automaattisesti seuraavissa tilanteissa:

- Jos kaksi seuraavista kolmesta kentästä on käytettävissä, kolmas lasketaan automaattisesti: 

    - **msdyn_start**
    - **msdyn_end**
    - **msdyn_duration**

- Kentät **msdyn_start** ja **msdyn_end** ovat tietoisia aikavyöhykkeestä.
- Aikamerkinnät, jotka on luotu vain **msdyn_date**- ja **msdyn_duration**-määrityksillä, alkavat keskiyöllä. **msdyn_start**- ja **msdyn_end**-kentät päivittyvät vastaavasti.

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

1. Lisää mukautettu kenttä **Pikaluonti**-valintaikkunaan.
2. Määritä ruudukko näyttämään mukautettu kenttä.
3. Lisää mukautettu kenttä **rivinmuokkaus**- tai **aikamerkinnän muokkaus** -sivulle tarpeen mukaan.

Varmista, että uudella kentällä on tarpeelliset kelpoisuustarkistukset **rivinmuokkauksen** tai **aikamerkinnän muokkauksen** sivulla. Tässä tehtävässä kenttä täytyy lukita aikamerkinnän tilan perusteella.

Kun lisäät mukautetun kentän **Aikamerkintä**-ruudukkoon ja luot sitten aikamerkinnät suoraan ruudukkoon, näiden merkintöjen mukautettu kenttä määritetään automaattisesti niin, että se vastaa riviä. 

### <a name="add-the-custom-field-to-the-quick-create-dialog-box"></a>Lisää mukautettu kenttä Pikaluonti-valintaikkunaan
Lisää mukautettu kenttä **Aikamerkinnän pikaluonti** -valintaikkunaan. Käyttäjät voivat kirjoittaa arvon, kun he lisäävät aikamerkintöjä valitsemalla **Uusi**.

### <a name="configure-the-grid-to-show-the-custom-field"></a>Määritä ruudukko näyttämään mukautettu kenttä.
Mukautettu kenttä voidaan lisätä **viikoittaiseen ajansyöttö** -ruudukkoon kahdella eri tavalla.

- Mukauta **Omat viikoittaiset aikamerkinnät** -näkymää lisäämällä siihen mukautetun kentän. Voit määrittää mukautetun kentän sijainnin ja koon ruudukossa muokkaamalla näitä näkymän ominaisuuksia.
- Luo uusi mukautettu ajansyöttönäkymä ja määritä se oletusnäkymäksi. Tässä näkymässä tulisi olla kentät **Kuvaus** ja **Ulkoiset huomautukset** niiden sarakkeiden lisäksi, joita haluat ruudukkoon. Voit määrittää mukautetun kentän sijainnin, koon ja oletuslajittelujärjestyksen ruudukossa muokkaamalla näitä näkymän ominaisuuksia. Määritä seuraavaksi tämän näkymän mukautettu ohjausobjekti siten, että se on **Ajansyöttöruudukon** ohjausobjekti. Lisää tämä ohjausobjekti näkymään ja valitse se **verkolle**, **puhelimelle** ja **tabletille**. Määritä seuraavaksi **viikoittaisen ajansyöttö** -ruudukon parametrit. Aseta **Alkamispäivä**-kentäksi **msdyn\_date**, aseta **Kesto**-kentäksi **msdyn\_duration** ja aseta **Tila**-kentäksi **msdyn\_entrystatus**. **Vain luku -tilaluettelo** -kentän arvoksi on määritetty **192350002 (hyväksytty)**, **192350003 (lähetetty)**, or **192350004 (Palautusta pyydetty)**.

### <a name="add-the-custom-field-to-the-appropriate-edit-page"></a>Mukautetun kentän lisääminen asianmukaiseen muokkaussivuun
Sivut, joilla muokataan aikakirjauksia tai aikamerkintärivejä, löytyvät kohdasta **Lomakkeet**. Ruudukon **Muokkaa merkintää** -painike avaa **Muokkaa merkintää** -sivun ja **Muokkaa riviä** -painike avaa **Rivin muokkaus** -sivun. Voit muokata näitä sivuja niin, että niissä on mukautettuja kenttiä.

Molemmat vaihtoehdot poistavat joitakin valmiina olevia suodattimia entiteeteistä **Projekti** ja **Projektitehtävä**, joten kaikki valintanäkymät ovat näkyvissä näille entiteeteille. Vain merkitykselliset valintanäkymät ovat näkyvissä valmiina.

Sinun täytyy määrittää mukautetulle kentälle asianmukainen sivu. Jos olet lisännyt kentän ruudukkoon, sen pitäisi todennäköisesti siirtyä siihen **Rivin muokkaus** -sivuun, jota käytetään kentissä, jotka koskevat koko aikamerkintäriviä Jos mukautetulla kentällä on ainutkertainen arvo rivillä joka päivä (kuten mukautetulla kentällä Päättymisaika), sen pitäisi siirtyä **aikamerkinnän muokkaus** -sivulle.

Jos haluat lisätä mukautetun kentän sivuun, vedä **Kenttä**-elementti asianmukaiseen kohtaan sivulla ja valitse sitten sen ominaisuudet.

### <a name="add-new-option-set-values"></a>Lisää uusia asetusjoukkoarvoja
Jos haluat lisätä asetusjoukon arvot käyttövalmiiseen kenttään, toimi seuraavasti.

1. Avaa kentän muokkaussivu ja valitse sen jälkeen **Kirjoita**-kohdassa **Muokkaa** asetusjoukon vieressä.
2. Lisää uusi asetus, jolla on mukautettu selite ja väri. Jos haluat lisätä uuden aikamerkinnän tilan, valmiin kentän nimi on **Merkinnän tila**.

### <a name="designate-a-new-time-entry-status-as-read-only"></a>Uuden aikakirjaustilan määrittäminen vain luku -tilaan
Jos haluat määrittää uuden aikamerkinnän tilaksi vain luku, lisää uuden aikamerkinnän arvo **Vain luku -tilaluettelo** -ominaisuuteen. Muista lisätä numeroa, älä otsikkoa. Ajansyöttöruudukon muokattava osa lukitaan nyt riveille, joilla on uusi tila. Jos haluat määrittää **Vain luku -tilaluettelo** -ominaisuuden eri **aikamerkinnän** näkymissä, lisää **ajan merkintä** -ruudukko näkymän **Mukautetut ohjausobjektit** -osaan ja määritä parametrit tarpeen mukaan.

Lisää seuraavaksi liiketoimintasäännöt lukitaksesi kaikki kentät **Rivin muokkaus** -ja **Aikamerkinnän muokkaus** -sivuilla. Pääset sivujen liiketoimintasääntöihin avaamalla kunkin sivun lomake-editorin ja valitsemalla sitten **Liiketoimintasäännöt**. Voit lisätä uuden tilan aiemmin luotujen liiketoimintasääntöjen ehtoon tai voit lisätä uuden liiketoimintasäännön uutta tilaa varten.

### <a name="add-custom-validation-rules"></a>Mukautettujen vahvistussääntöjen lisääminen
Voit lisätä kahdentyyppisiä tarkistussääntöjä **viikoittaiseen ajanmerkinnän** ruudukkokokemukseen:

- Sivuilla toimivat asiakaspuolen liiketoimintasäännöt
- Palvelinpuolen laajennuksen tarkistukset, jotka koskevat kaikkia aikamerkinnän päivityksiä

#### <a name="client-side-business-rules"></a>Asiakaspuolen liiketoimintasäännöt
Liiketoimintasääntöjen avulla voit lukita ja vapauttaa kenttiä, kirjoittaa oletusarvoja kenttiin ja määrittää vahvistuksia, jotka edellyttävät tietoja vain nykyisestä ajansyöttötietueesta. Pääset sivun liiketoimintasääntöihin avaamalla lomake-editorin ja valitsemalla sitten **Liiketoimintasäännöt**. Voit sitten muokata aiemmin luotuja liiketoimintasääntöjä tai lisätä uuden liiketoimintasäännön.

#### <a name="server-side-plug-in-validations"></a>Palvelinpuolen laajennuksen vahvistukset
Käytä laajennusvahvistuksia kaikkiin vahvistuksiin, jotka edellyttävät enemmän kontekstia kuin on käytettävissä yksittäisessä aikakirjaustietueessa. Käytä niitä myös kaikkiin vahvistuksiin, jotka haluat suorittaa tekstisidonnaisina päivityksinä ruudukossa. Viimeistele vahvistukset luomalla mukautettu laajennus **Aikakirjaus**-entiteettiin.

### <a name="limits"></a>Rajoitukset
Tällä hetkellä **ajan syöttö** -ruudukon kokorajoitus on 500 riviä. Jos rivejä on yli 500, ylimääräisiä rivejä ei näy. Tätä kokorajoitusta ei voi suurentaa.

### <a name="copying-time-entries"></a>Aikamerkintöjen kopiointi
Voit määrittää aikamerkinnän aikana kopioitavien kenttien luettelon käyttämällä **Näytä kopiointiajan syöttö** -sarakkeita. **Päivämäärä** ja **kesto** ovat pakollisia kenttiä, eikä niitä pitäisi poistaa näkymästä.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
