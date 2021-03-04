---
title: Viikoittaisen ajan syöttämisen mukauttaminen
description: Tässä aiheessa on tietoja yrityksen käytäntöjä tukevien mukautettujen liiketoimintasääntöjen toteuttamisesta.
author: stsporen
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 07/09/2019
ms.topic: article
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
ms.openlocfilehash: a34244884bc81da74ae3bf550bde6f982d04abd3
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/10/2021
ms.locfileid: "5149629"
---
# <a name="customize-weekly-time-entry"></a>Viikoittaisen ajan syöttämisen mukauttaminen 

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Microsoft esitteli Microsoft Dynamics 365 Project Service Automation versiossa 3.3 uudenaikaisen ruudukon, jonka avulla projektin resurssit voivat nopeasti syöttää aikaa jopa viikko kerrallaan. Uusi viikoittainen ajansyöttöruudukko voi näyttää tapahtumien summat päivämäärän, rivin tai viikon mukaan. Resurssit voivat luoda kopioita aikakirjauksista viikon sisällä, ja myös kopioida useita kerrallaan edellisiltä viikoilta. Järjestelmän mukauttajat voivat mukauttaa näkymää lisäämällä kenttiä, lisäämällä hakuja muihin entiteetteihin ja toteuttamalla mukautettuja liiketoimintasääntöjä, jotka tukevat organisaation käytäntöjä.

Ajan syöttö ja uusi viikoittainen aikaruudukko ovat käytettävissä sivustokartan kautta. Ei-laajennettava mukautettu ajansyöttökokemus, joka oli osa aiempia PSA-versioita, on korvattu laajennettavalla viikoittaisella aikakirjausruudukolla ja vaihtoehtoisella käyttökokemuksella vain luku -ruudukossa ja kalenterissa. Tämän muutoksen vuoksi käyttäjät voivat syöttää aikaa viikoittaisissa summissa.

## <a name="page-layout"></a>Sivun asettelu
Uusi viikoittainen ajansyöttöruudukko on mukautettu ohjausobjekti, jolla on työkalurivi ja kaksi pääosaa, **Dimensiot** ja **Kesto**. Työkalurivillä on painike, joka koskee vain tätä mukautettua ohjausobjektia ajansyöttöruudukkoa varten. Sivun yläosassa olevan toimintoruudun painikkeita käytetään kuitenkin kolmenlaisten ajansyöttöohjausobjektien tyyppeihin: viikoittaisen ajan syötön ohjausobjektiin, vain luku -ohjausobjektiin ja kalenteriohjausobjektiin.

### <a name="dimensions"></a>Dimensiot
**Dimensiot** -osassa näkyvät sarakeotsikoina kaikki ne dimensiot, joihin aikaa voidaan lisätä. Seuraavien dimensioiden tuki on sisäänrakennettu:

- Projekti
- Projektin tehtävä
- Rooli
- Tyyppi
- Merkinnän tila

**Dimensiot** -osa ei salli tekstiin sidottua muokkausta. Tätä osaa tukee näkymä, jonka avulla mukautetut kentät voidaan lisätä viikoittaiseen ajansyöttöruudukkoon. Lisätietoja mukautettujen kenttien lisäämisestä on jäljempänä tässä aihe kohdassa "Laajennettavuus".

### <a name="duration"></a>Kesto
Kesto-osassa näkyvät viikonpäivät sarakeotsikoina. Tässä osassa voi muokata tekstiin sidotusti. Kun ajansyöttörivi on luotu ja siinä on tarvittavat dimensiot, käyttäjät voivat nopeasti syöttää tekstiin sidotusti, sen aikamäärän, jonka he käyttivät näihin dimensioihin.

## <a name="create-a-new-time-entry"></a>Uuden aikamerkinnän luominen
Jos haluat luoda uuden aikamerkinnän ajansyöttöruudukkoon, valitse **Uusi**. **Aikamerkinnän pikaluonti** -valintaikkuna aukeaa. Tässä valintaikkunassa käyttäjät voivat valita aikamerkinnänpäivä määrän ja kirjoittaa sitten **Projektin**, **Projektitehtävän**, **Roolin** ja **Keston** dimensioiden tiedot minuutteina, tunteina tai päivinä kirjoittamalla **h**, **m** tai **d** sekä numeron. Käyttäjät voivat myös kirjoittaa aikamerkinnälle kuvauksen ja kommentteja, jotka voidaan jakaa ulkoisesti. Kun käyttäjät tallentavat muutokset, arvot, jotka he ovat antaneet dimensioille, näkyvät **Dimensiot**-osassa. Kesto, jonka he syöttivät **Kesto**-kenttään näkyy päivälle, jota varten aikakirjaus luotiin.

Järjestelmänäkymät tukevat valintakenttiä. Kun käyttäjä on esimerkiksi syöttänyt projektin, **Projektitehtävä**-kenttä asetetaan oletuksena **Kopioi**-näkymään. Jos haluat luoda aikamerkintöjä tehtäville, joita ei ole kohdennettu käyttäjälle, valitse **Vaihda näkymää** -valintaruudussa, ja valitse sen jälkeen **Kaikki aktiiviset projektitehtävät** -näkymä.

## <a name="edit-a-time-entry"></a>Aikamerkinnän muokkaus
Joidenkin ajansyöttösivun kenttien, kuten **Kuvauksen** ja **Ulkoisten huomautusten**, tietoja ei näytetä viikoittaisessa ajansyöttöruudukossa. Sen sijaan näytetään pieni kolmionmuotoinen osoitin niissä kestosoluissa, joilla on näitä lisätietoja. Valitse solu, ja valitse sen jälkeen **Muokkaa tietoja** nähdäksesi tiedot **Pikamuokkaus**-ruudussa. Tietyn aikamerkinnäin, joka ei ole osa viikoittaista ajansyöttöruudukkoa, tietojen päivittämistä tai muokkaamista varten käyttäjien on avattava **Pikamuokkaus**-ruutu.

## <a name="copy-a-time-entry-row"></a>Aikamerkintärivin kopioiminen
Kun ensimmäinen aikamerkintärivi on luotu, käyttäjät voivat valita **Kopioi rivi** -toiminnon kopioidakseen koko rivin uudelle riville. Kun rivi kopioidaan tällä tavalla, myös dimensiot ja kestot kopioidaan. Käyttäjät voivat myös valita **Muokkaa riviä** päivittääkseen dimension arvot ja kestot **Kesto**-osassa.

## <a name="open-a-time-entry"></a>Aikamerkinnän avaaminen
Mahdollisimman optimaalisen ja nopean syötön tukemiseksi näkyvimpiin kenttiin viikoittainen ajansyöttöruudukko näyttää valittujen dimensioiden ja ajan kestojen alijoukon. Jos haluat nähdä kaikki yksittäisen aikamerkinnän tiedot, valitse **Muokkaa merkintää** -kohdassa **Avaa**,

## <a name="submit-a-time-entry"></a>Lähetä aikamerkintä
Käyttäjät voivat lähettää yksittäisen aikamerkinnän tai aikamerkintäryhmän valitsemalla joukon soluja tai koko ajansyöttörivin ja valitsemalla sitten **Lähetä**. Lähetetyt aikamerkinnät näkyvät merkintöinä, jotka odottavat hyväksyntää hyväksyjien **Hyväksyntä**-sivulla. Kun aikamerkinnät on lähetetty onnistuneesti, niitä ei voi muokata.

## <a name="recall-a-time-entry"></a>Peruuta aikamerkintä
Voit peruuttaa lähettämiäsi aikamerkintöjä. Voit peruuttaa yksittäisen aikamerkinnän, ryhmän aikamerkintöjä tai kokonaisen aikamerkintärivin. Peruutetut aikamerkinnät ovar resurssien editoitavissa.

## <a name="time-entry-status"></a>Aikamerkinnän tila
Uudet aikamerkinnät saavat automaattisesti tilan **Luonnos**. Kun aikamerkintä lähetetään, tilaksi päivittyy **Lähetetty**. Kun lähetetty aikamerkintä hyväksytään, tilaksi päivittyy **Hyväksytty**. Jos aikamerkintä hylätään, sen tilaksi päivittyy **Palautettu**, ja merkintä on käytettävissä korjausta ja uudelleenlähettämistä varten. Vain aikamerkintöjä, joiden tila on **Luonnos**, voidaan poistaa.

## <a name="view-rejection-comments"></a>Hylkäystä koskevien huomautusten tarkastelu
Kun hyväksyjä hylkää aikamerkinnän, hyväksyjä voi lisätä hylkäyshuomautuksia, jotka auttavat resurssia ymmärtämään hylkäyksen syyn. Jos haluat tarkastella aikamerkinnän hylkäyshuomautuksia, valitse **Avaa merkintä**. Hylkäyshuomautukset näkyvät aikajanalla. Resurssi voi vastata hylkäyshuomautuksiin aikajanalla ennen kuin hän lähettää merkinnän uudelleen.

## <a name="copy-week"></a>Kopioi viikko
Kun joitakin aikamerkintöjä on luotu, käyttäjät voivat valita **Kopioi viikko** luodakseen useita aikamerkintöjä lisää kerralla. **Kopioi**-valintaikkuna avautuu. Käytä **Lähdejakso**-kenttäryhmässä **Alkamispäivä**- ja **Päättymispäivä**-kenttiä sen päivämäärävälin määrittelemiseksi, jolta aikamerkinnät kopioidaan. Määritä **Kohdejakso**-osassa **Alkamispäivä**-kentässä päivämäärä, jolle luodaan aikamerkintöjä. Valitse sitten **Kopioi**. Kohdejaksolle määritellylle päivämäärälle luodaan kopio aikamerkinnöistä lähdejakson vastaavalta viikonpäivältä. Esimerkiksi edellisen viikon maanantain aikakirjaus kopioidaan sen viikon maanantaille, joka on määritetty kohdejaksossa.

## <a name="import"></a>Tuonti
Samaa perusprosessia käytetään tuotaessa varauksista, kohdennuksista ja vaihdoista. Käyttäjät voivat määrittää päivämäärävälin, josta varaukset tuodaan. Tämän jälkeen heidän täytyy valita erikseen ne varaukset, jotka kopioidaan aikamerkintäluonnoksiksi. Edellisessä versiossa ehdotetut ajankohdat tulivat näkyviin ruudukossa ja kalenterissa, ja ne menetettiin, kun istunto päivitettiin.

## <a name="extensibility"></a>Laajennettavuus
### <a name="add-custom-fields-that-have-lookups-to-other-entities"></a>Sellaisten mukautettujen kenttien lisääminen, joilla on hakuja muihin kohteisiin
Mukautetun kentän lisäämisessä viikoittaiseen ajansyöttöruudukkoon on kolme päävaihetta.

1.  Lisää mukautettu kenttä pikaluonti-valintaikkunaan.
2.  Määritä ruudukko näyttämään mukautettu kenttä.
3.  Lisää mukautettu kenttä joko rivin muokkaamisen tai solun muokkauksen työnkulkuun tarpeen mukaan.

Varmista myös, että uudella kentällä on tarpeelliset kelpoisuustarkistukset rivin tai solun muokkauksen työnkulussa. Tässä vaiheessa kenttä täytyy lukita aikamerkinnän tilan perusteella.

#### <a name="add-the-custom-field-to-the-quick-create-dialog-box"></a>Lisää mukautettu kenttä pikaluonti-valintaikkunaan.
Lisää mukautettu kenttä Aikamerkinnän pikaluonti -valintaikkunaan. Tämä tehdään, jotta käyttäjät voivat määrittää sille arvon, kun he lisäävät aikamerkintöjä käyttämällä **Uusi** -painiketta.

#### <a name="configure-the-grid-to-show-the-custom-field"></a>Määritä ruudukko näyttämään mukautettu kenttä.
Mukautettu kenttä voidaan lisätä viikoittaiseen ajansyöttöruudukkoon kahdella eri tavalla. Ensimmäinen vaihtoehto on mukauttaa **Omat viikoittaiset aikamerkinnät** -näkymää lisäämällä siihen mukautettu kenttä. Voit valita mukautetun kentän sijainnin ja koon ruudukossa muokkaamalla näitä näkymän ominaisuuksia.

Toinen vaihtoehto on luoda uusi mukautettu ajansyöttönäkymä ja määrittää se oletusnäkymäksi. Tässä näkymässä tulisi olla kentät **Kuvaus** ja **Ulkoiset huomautukset** niiden sarakkeiden lisäksi, joita haluat ruudukkoon. Voit valita mukautetun kentän sijainnin, koon ja oletuslajittelujärjestyksen ruudukossa muokkaamalla näitä näkymän ominaisuuksia. Määritä seuraavaksi tämän näkymän mukautettu ohjausobjekti siten, että se on **Ajansyöttöruudukon** ohjausobjekti. Lisää tämä ohjausobjekti näkymään ja valitse se verkolle, puhelimelle ja tabletille. Määritä seuraavaksi viikoittaisen ajansyöttöruudukon parametrit. Aseta **Alkamispäivä**-kentäksi **msdyn_date**, aseta **Kesto**-kentäksi **msdyn_duration** ja aseta **Tila**-kentäksi **msdyn_entrystatus**. Oletusnäkymälle **Vain luku -tilaluettelo** -kentäksi on asetettu **192350002,192350003,192350004**, **Rivinmuokkauksen työnkulku** -kentäksi on asetettu **msdyn_timeentryrowedit** ja **Solunmuokkauksen työnkulku** -kentäksi on asetettu **msdyn_timeentryedit**. Voit mukauttaa näitä kenttiä, jos haluat lisätä tai poistaa vain luku -tilan tai käyttää toista tehtäväpohjaista kokemusta (TBX) rivien tai solujen muokkaamiseen. Nämä kentät on sidottava staattiseen arvoon.

#### <a name="add-the-custom-field-to-the-appropriate-edit-task-flow"></a>Mukautetun kentän lisääminen asianmukaiseen muokkaus työnkulkuun
Muokkaamiseen käytettävät TBX-sivut löytyvät **Prosessit**-kohdasta. Oletussivut ovat **Project Service - Aikamerkintärivin muokkaus** ja **Project Service - Aikamerkinnän muokkaus**. Voit joko muokata näitä oletussivuja tai luoda uusia mukautettuja TBX-sivuja.

> [!NOTE] 
> Molemmat vaihtoehdot poistavat joitakin valmiina olevia suodattimia entiteeteistä **Projekti** ja **Projektitehtävä**, joten kaikki valintanäkymät ovat näkyvissä näille entiteeteille. Vain merkitykselliset valintanäkymät ovat näkyvissä valmiina.

Sinun täytyy määrittää mukautetulle kentälle asianmukainen työnkulku. Jos olet lisännyt kentän ruudukkoon, sen pitäisi todennäköisesti siirtyä siihen rivimuokkauksen työnkulkuun, jota käytetään kentissä, jotka koskevat koko aikamerkintäriviä Jos mukautetulla kentällä on ainutkertainen arvo joka päivä, kuten mukautetulla kentällä **Päättymisaika**, sen pitäisi siirtyä solunmuokkauksen työnkulkuun.

Jos haluat lisätä mukautetun kentän työnkulkuun, vedä **Kenttä**-elementti asianmukaiseen kohtaan sivulla ja valitse sitten sen ominaisuudet. Määritä **Lähde**-ominaisuudeksi **Aikamerkintä** ja aseta **Tietokenttä**-ominaisuus muokatulle kentälle. **Kenttä**-ominaisuus määrittää TBX-sivun näyttönimen. Valitse **Käytä** tallentaaksesi kenttään tekemäsi muutokset. Valitse sitten **Päivitä** tallentaaksesi sivulle tekemäsi muutokset.

Jos haluat käyttää uutta mukautettua TBX-sivua, luo uusi prosessi. Määritä luokaksi **Liiketoimintaprosessin kulku**, aseta entiteetiksi **Aikakirjaus**, ja aseta liiketoimintaprosessityypiksi **Aja prosessi työnkulkuna**. **Ominaisuuksissa** **Sivun nimi** -ominaisuuden tulisi olla asetettu sivun näyttönimeksi. Lisää kaikki tarvittavat kentät TBX-sivulle. Tallenna ja aktivoi prosessi ja päivitä sitten kyseisen tehtävänkulun mukautetun ohjausobjektin ominaisuus prosessin **Nimen** arvoksi.

### <a name="add-new-option-set-values"></a>Lisää uusia asetusjoukkoarvoja
Jos haluat lisätä asetusjoukkoarvoja valmiina olevaan kentään, avaa kentän muokkaussivu ja valitse sen jälkeen **Kirjoita**-kohdassa **Muokkaa** asetusjoukon vieressä. Lisää seuraavaksi uusi asetus, jolla on mukautettu selite ja väri. Jos haluat lisätä uuden aikamerkinnän tilan, valmiin kentän nimi on  **Merkinnän tila**, ei **Tila**.

### <a name="designate-a-new-time-entry-status-as-read-only"></a>Uuden aikakirjaustilan määrittäminen vain luku -tilaan
Jos haluat määrittää uuden aikamerkinnän tilaksi vain luku, lisää uuden aikamerkinnän arvo (numero, ei selite) **Vain luku -tilaluettelo** -ominaisuuteen. Ajansyöttöruudukon muokattava osa lukitaan riveille, joilla on uusi tila.
Lisää seuraavaksi liiketoimintasäännöt lukitaksesi kaikki kentät **Aikamerkintärivin muokkaus** -ja **Aikamerkinnän muokkaus** -TBX-sivuilla. Pääset sivujen liiketoimintasääntöihin avaamalla sivun liiketoimintaprosessieditorin ja valitsemalla sitten **Liiketoimintasäännöt**. Voit lisätä uuden tilan aiemmin luotujen liiketoimintasääntöjen ehtoon tai voit lisätä uuden liiketoimintasäännön uutta tilaa varten.

### <a name="add-custom-validation-rules"></a>Mukautettujen vahvistussääntöjen lisääminen
Viikoittaiseen ajansyöttöruudukkokokemukseen voidaan lisätä kahden tyyppisiä vahvistussääntöjä: • Asiakaspuolen liiketoimintasäännöt, jotka toimivat pikaluonnin valintaruuduissa ja TBX-sivuilla •   Palvelinpuolen lisäosavahvistuksia, joita sovelletaan kaikkiin ajansyötön päivityksiin

#### <a name="business-rules"></a>Liiketoimintasäännöt
Liiketoimintasääntöjen avulla voit lukita ja vapauttaa kenttiä, kirjoittaa oletusarvoja kenttiin ja määrittää vahvistuksia, jotka edellyttävät tietoja vain nykyisestä ajansyöttötietueesta. Pääset TBX-sivun liiketoimintasääntöihin avaamalla sivun liiketoimintaprosessieditorin ja valitsemalla sitten **Liiketoimintasäännöt**. Voit sitten muokata aiemmin luotuja liiketoimintasääntöjä tai lisätä uuden liiketoimintasäännön. Voit käyttää liiketoimintasääntöä ajamaan JavaScriptiä luodaksesi vielä mukautetumpia vahvistuksia.

#### <a name="plug-in-validations"></a>Laajennusvahvistukset
Käytä laajennusvahvistuksia kaikkiin vahvistuksiin, jotka edellyttävät enemmän kontekstia kuin on käytettävissä yksittäisessä aikakirjaustietueessa, tai kaikkiin vahvistuksiin, jotka haluat suorittaa tekstisidonnaisina päivityksinä ruudukossa. Viimeistele vahvistus luomalla mukautettu laajennus **Aikakirjaus**-entiteettiin.

> [!IMPORTANT] 
> Tällä hetkellä tunnettu ongelma TBX-sivuilla estää käyttäjiä korjaamasta tietoja ja uudelleenvalitsemista Valmis, kun päivitys epäonnistuu laajennuksen tarkistuksessa. Voit kiertää ongelman määrittämällä liiketoimintasäännön vahvistuksia, jotka estävät tilanteen mahdollisimman hyvin.


[!INCLUDE[footer-include](../includes/footer-banner.md)]