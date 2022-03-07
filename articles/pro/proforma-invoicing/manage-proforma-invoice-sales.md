---
title: Proformamuotoisen projektilaskun hallinta
description: Tässä aiheessa on tietoja proformamuotoisten projektipohjaisten parissa työskentelystä.
author: rumant
ms.date: 04/05/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: f14cf9d5ee25247500180081b8f407ee311db481a5ef5eac330e75d45baba54a
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/06/2021
ms.locfileid: "6997422"
---
# <a name="manage-a-proforma-project-invoice"></a>Proformamuotoisen projektilaskun hallinta 

_**Käytetään:** Lite-käyttöönotto – kauppa proformalaskutukseen_

Dynamics 365 Project Operationsissa proformalaskut muodostetaan Dynamics 365 Salesin laskujen laajennuksena. Salasin ja Project Operationsin laskutusprosessissa on kuitenkin monenlaisia eroja. Project Operationsissa ei voi esimerkiksi luoda uutta laskua **Laskuluettelo**-sivulla, vaikka se on mahdollista Salesissa. Nämä erot ja laajennukset ovat käytössä siksi, että voidaan tukea sellaisten projektien laskutusprosesseja, jotka eroavat tyypillisestä myyntitilauksen laskusta.

> [!IMPORTANT]
> Näiden erojen vuoksi Salesin ja Project Operationsin laskuja ei voi käyttää toistensa vaihtoehtoina.

## <a name="invoice-header"></a>Laskun otsikko

Project Operationsin proformalaskun otsikossa on seuraavat tiedot.

| Field | Sijainti | Kuvaus | Loppupään vaikutus |
| --- | --- | --- | --- |
| **Laskun tunnus** | **Yhteenveto**-välilehti | Tämä tunnus luodaan automaattisesti, kun proformalasku luodaan. Lukittu vain luku -muotoinen kenttä, jota ei voi muokata. | Tätä kenttää käytetään kunkin proformalaskun viitteenä. |
| **Nimi** | **Yhteenveto**-välilehti | Arvoksi määritetään oletusarvoisesti projektisopimuksen nimi. Käyttäjä voi muokata tätä kenttää. | &nbsp;  |
| **Valuutta** | **Yhteenveto**-välilehti | Arvoksi määritetään oletusarvoisesti projektisopimuksen valuutta. Lukittu vain luku -muotoinen kenttä, jota ei voi muokata. |&nbsp; |
| **Hinnasto** | **Yhteenveto**-välilehti | Arvoksi määritetään oletusarvoisesti projektisopimuksen hinnasto. Lukittu vain luku -muotoinen kenttä, jota ei voi muokata. | &nbsp; |
| **Mahdollisuus** | **Yhteenveto**-välilehti | Viittaus linkitettyyn mahdollisuuteen. Lukittu vain luku -muotoinen kenttä, jota ei voi muokata. | &nbsp;  |
| **Palvelusopimus** | **Yhteenveto**-välilehti | Viittaus linkitettyyn projektisopimukseen. Lukittu vain luku -muotoinen kenttä, jota ei voi muokata. | &nbsp; |
| **Asiakas** | **Yhteenveto**-välilehti | Viittaus linkitettyyn projektisopimukseen. Lukittu vain luku -muotoinen kenttä, jota ei voi muokata. |&nbsp;  |
| **Kuvaus** | **Yhteenveto**-välilehti | Laskua kuvaava tekstikenttä. Käyttäjä voi muokata tätä kenttää. | &nbsp; |
| **Laskutusosoite**- ja liittyvät kentät | **Yhteenveto-välilehti** | Oletusarvot määritetään projektisopimuksen asiakkaasta. Käyttäjä voi muokata tätä kenttää.  | &nbsp; |
| **Tila** | **Yhteenveto**-välilehti | Määrittää seuraavat vaihtoehdot: **Aktiivinen**, **Suljettu**, **Maksettu** ja **Peruutettu**. Käyttäjä voi muokata. | Project Operations ei tue seuraavia tietoja: **Suljettu** ja **Peruutettu**. </br> Tilaksi määritetään **Aktiivinen**, kun lasku luodaan. </br>**Maksettu**-tila on syytä määrittää vastan, kun lasku on vahvistettu. |
| **Projektin laskun tila** | **Yhteenveto**-välilehti | Määrittää seuraavat vaihtoehdot: **Luonnos**, **Tarkistettavana** ja **Vahvistettu**. Käyttäjä voi muokata. | Laskua voi muokata sekä **Luonnos**- että **Tarkistettavana**-tilassa. Laskua ei voi muokata sen jälkeen, kun se on vahvistettu. |
| **Eritelty summa** | **Yhteenveto**-välilehti | Kaikkien laskurivien yhteenlaskettu summa ennakoiden ja vähennysten jälkeen. Lukittu vain luku -muotoinen kenttä, jota ei voi muokata. | Lopullinen summa lasketaan tämän kentän avulla. |
| **Alennus (%)** | **Yhteenveto**-välilehti | Tätä kenttää voi muokata antamalla alennusprosentti. Project Operations -toiminnot eivät tue tätä kenttää. | Tämä kenttää ei tueta. |
| **Alennussumma** | **Yhteenveto**-välilehti | Tätä kenttää voi muokata antamalla alennussumma. Project Operations -toiminnot eivät tue tätä kenttää. | Tämä kenttää ei tueta. |
| **Summa ilman rahtikuluja** | **Yhteenveto-välilehti** | Laskun kokonaissumma alennusten jälkeen. Lukittu vain luku -muotoinen kenttä, jota ei voi muokata. | Lopullinen summa lasketaan tämän kentän avulla. |
| **Rahti** | **Yhteenveto**-välilehti | Tätä kenttää voi muokata antamalla rahti. Project Operations -toiminnot eivät tue tätä kenttää. | Tämä kenttää ei tueta. |
| **Vero yhteensä** | **Yhteenveto**-välilehti | Laskun kaikkien laskurivien vero yhteensä. Lukittu vain luku -muotoinen kenttä, jota ei voi muokata. | Ei mitään. |
| **Loppusumma** | **Yhteenveto**-välilehti | Yhteenlaskettu summa alennusten ja verojen jälkeen. | Yhteenlaskettu summa on summa, joka asiakkaan on maksettava. |
## <a name="project-based-invoice-lines"></a>Projektipohjaiset laskurivit

Project Operationsissa jokaisella projektisopimusrivillä on aina yksi laskurivi. Laskurivi luodaan, vaikka todellisia arvoja ei olisi. Proformalaskurivillä on seuraavat tiedot.

| Field | Sijainti | Kuvaus | Loppupään vaikutus |
| --- | --- | --- | --- |
| **Laskun tunnus** | **Yleiset**-välilehti | Viittaus laskun tunnukseen. Lukittu vain luku -muotoinen kenttä, jota ei voi muokata. | Laskun tunnuksen linkin avulla voi siirtyä takaisin laskun otsikkoon. |
| **Nimi** | **Yleiset**-välilehti | Laskurivin nimi määritetään oletusarvoisesti sopimusrivin nimestä. Käyttäjä voi muokata tätä kenttää. | &nbsp; |
| **Project** | **Yleiset**-välilehti | Liittyvän projektin sopimusrivillä oleva projekti. Lukittu vain luku -muotoinen kenttä, jota ei voi muokata. | Projektiin voi siirtyä projektin linkin avulla. |
| **Laskutustapa** | **Yleiset**-välilehti | Liittyvän projektin sopimusrivillä oleva laskutustapa. Lukittu vain luku -muotoinen kenttä, jota ei voi muokata. | &nbsp; |
| **Sopimusrivin summa** | **Yleiset**-välilehti | Liittyvän projektin sopimusrivillä olevan sopimuksen summa. Lukittu vain luku -muotoinen kenttä, jota ei voi muokata. | &nbsp; |
| **Laskutettu päivämäärään** | **Yleiset**-välilehti | Tämän laskun kaikkien laskurivien tietojen yhteenlasketut summat. Lukittu vain luku -muotoinen kenttä, jota ei voi muokata. | &nbsp; |
| **Summa** | **Yleiset**-välilehti | Tämän laskun kaikkien veloitettavien laskurivien tietojen yhteenlasketut summat. Lukittu vain luku -muotoinen kenttä, jota ei voi muokata. | Laskun otsikon lopullinen summa lasketaan tämän kentän avulla. |
| **Vero** | **Yleiset**-välilehti | Tämän laskurivin kaikkien laskurivin tietojen yhteenlasketut verosummat. Lukittu vain luku -muotoinen kenttä, jota ei voi muokata. | Laskun otsikon lopullinen verosumma lasketaan tämän kentän avulla. |
| **Koko summa** | **Yleiset**-välilehti | Tämän laskurivin kaikkien veloitettavien laskurivin tietojen yhteenlasketut kokonaissummat (**vero + summat)**. Lukittu vain luku -muotoinen kenttä, jota ei voi muokata. | Laskun otsikon lopullinen summa lasketaan tämän kentän avulla. |


## <a name="invoice-line-details"></a>Laskurivin tiedot

Jokainen projektilaskun laskurivi sisältää laskurivin tiedot. Nämä rivitiedot liittyvät laskuttamattomaan toteutuneeseen myyntiin ja niihin sopimusriviin liittyviin välitavoitteisiin, joihin laskurivi viittaa. Kaikissa näissä tapahtumissa on merkintä **Valmis laskuttamista varten**.

**Aika- ja materiaalilasku** -rivillä laskun tiedot on ryhmitelty ryhmiin **Laskutettava**, **Ei-laskutettava** ja **Ilmainen** sivulla **Laskurivi**. **Veloitettavan laskurivin** tiedot listään laskurivin kokonaissummaan. **Ilmaiset** ja **Ei-laskutettavat toteutuneet arvot** eivät täsmää laskurivin kokonaissummaan.

**Kiinteähintainen lasku** -riviä varten laskurivin tiedot luodaan välitavoitteista, jotka on merkitty **Valmis laskutettavaksi** liittyvällä sopimusrivillä. Kun laskurivin tiedot on luotu välitavoitteesta, välitavoitteen laskutustilaksi päivitetään **Asiakaslasku luotu**.

### <a name="edit-invoice-line-details"></a>Laskurivin tietojen muokkaaminen

Seuraavat kentät ovat käytettävissä laskun rivin tiedossa, joka perustuu laskuttamattomaan toteutuneeseen myyntiin:

| Field | Kuvaus | Loppupään vaikutus |
| --- | --- | --- |
| **Laskurivi** | Viittaus **laskurivin tunnukseen**. Lukittu vain luku -muotoinen kenttä, jota ei voi muokata. | Tämän linkin avulla voi siirtyä takaisin laskun otsikkoon. |
| **Kuvaus** | Laskurivin tiedon kuvaus. Määritetään oletusarvoisesti **Aikamerkintä**-kohdan **Sisäiset kommentit** -kentästä ja **Kulumerkintä**-kohdan **Kuvaus**-kentästä. Käyttäjä voi muokata kenttää.| &nbsp; |
| **Ulkoinen kuvaus** | Laskurivin tiedon kuvaus. Määritetään oletusarvoisesti **Aikamerkintä**-kohdan **Ulkoiset kommentit** -kentästä ja **Kulumerkintä**-kohdan **Kuvaus**-kentästä. Käyttäjä voi muokata kenttää. | Tällä kuvauksella voidaan määrittää, mitä asiakkaalle lähetettävään laskuun tulostetaan. Project Operationsin proformalaskussa ei ole kaikkia tarvittavia toimintoja laskun tulostusasetusten määrittämiseen. |
| **Aloituspäivämäärä** | Määritetään oletusarvoisesti lähteen todellisesta arvosta. Lukittu vain luku -muotoinen kenttä, jota ei voi muokata. | Tätä kenttää voi muokata uudessa laskurivin tiedossa, joka ei perustu lähteen todelliseen arvoon. |
| **Project** | Määritetään oletusarvoisesti lähteen todellisesta arvosta. Lukittu vain luku -muotoinen kenttä, jota ei voi muokata. | Arvoksi määritetään oletusarvoisesti liittyvällä sopimusrivillä oleva projekti. |
| **Tehtävä** | Määritetään oletusarvoisesti lähteen todellisesta arvosta. Lukittu vain luku -muotoinen kenttä, jota ei voi muokata. | Kenttää voi muokata uudessa laskurivin tiedossa, joka ei perustu lähteen todelliseen arvoon. Avattava luettelo sisältää kaikki liittyvään projektin sopimusriviin liitetyt tehtävät.  |
| **Tapahtumaluokka** | Määritetään oletusarvoisesti lähteen todellisesta arvosta. Lukittu vain luku -muotoinen kenttä, jota ei voi muokata. | Kenttää voi muokata uudessa laskurivin tiedossa, joka ei perustu toteutuneeseen lähteeseen. |
| **Rooli** | Määritetään oletusarvoisesti lähteen todellisesta arvosta. Lukittu vain luku -muotoinen kenttä, jota ei voi muokata. | Kenttää voi muokata uudessa laskurivin tiedossa, joka ei perustu lähteen todelliseen arvoon. |
| **Varattavissa oleva resurssi** | Määritetään oletusarvoisesti lähteen todellisesta arvosta. Lukittu vain luku -muotoinen kenttä, jota ei voi muokata. | Kenttää voi muokata uudessa laskurivin tiedossa, joka ei perustu toteutuneeseen lähteeseen. |
| **Resursointiyksikkö** | Määritetään oletusarvoisesti lähteen todellisesta arvosta. Lukittu vain luku -muotoinen kenttä, jota ei voi muokata. | Kenttää voi muokata uudessa laskurivin tiedossa, joka ei perustu lähteen todelliseen arvoon. |
| **Määrä** | Määritetään oletusarvoisesti lähteen todellisesta arvosta. Lukittu vain luku -muotoinen kenttä, jota ei voi muokata. | Kenttää voi muokata uudessa laskurivin tiedossa, joka ei perustu lähteen todelliseen arvoon. |
| **Yksikön aikataulutus** | Ajan laskurivin tiedoksi on aina määritetty aika, eikä sitä voi muokata. Kulujen arvo määritetään oletusarvoisesti lähteen toteutuneesta kulusta. Lukittu vain luku -muotoinen kenttä, jota ei voi muokata. | Uuden laskurivin tiedon arvoksi määritetään oletusarvoisesti **Aika**, kun perusteena ei ole todellinen arvo. |
| **Yksikkö** | Määritetään oletusarvoisesti lähteen todellisesta arvosta. Lukittu vain luku -muotoinen kenttä, jota ei voi muokata. | Kenttää voi muokata uudessa laskurivin tiedossa, joka ei perustu lähteen todelliseen arvoon |
| **Hinta** | Määritetään oletusarvoisesti lähteen todellisesta arvosta. Lukittu vain luku -muotoinen kenttä, jota ei voi muokata. | Kenttää voi muokata uudessa laskurivin tiedossa, joka ei perustu lähteen todelliseen arvoon. Jos arvoa ei anneta, se määritetään oletusarvoksi **Tallenna**-valinnan jälkeen. |
| **Valuutta** | Määritetään oletusarvoisesti lähteen todellisesta arvosta. Lukittu vain luku -muotoinen kenttä, jota ei voi muokata. | Arvo määritetään oletusarvoisesti laskun otsikosta, kun uusi laskun tieto luodaan ilman, että perustuu todelliseen arvoon.  Lukittu vain luku -muotoinen kenttä, jota ei voi muokata. |
| **Summa** | Määritetään oletusarvoisesti lähteen todellisesta arvosta. Lukittu vain luku -muotoinen kenttä, jota ei voi muokata. | Lasketaan kaavalla **Määrä \* Hinta**, jos uusi laskun tieto luodaan ilman, että sen perusteena on todellinen arvo. Arvo lasketaan **Tallenna**-valinnan jälkeen. Lukittu vain luku -muotoinen kenttä, jota ei voi muokata. |
| **Vero** | Määritetään oletusarvoisesti lähteen todellisesta arvosta. Käyttäjä voi muokata kenttää | Käyttäjä voi muokata kenttää luotaessa uutta laskurivin tietoa ilman, että perustuu todelliseen arvoon. |
| **Koko summa** | Laskennallinen kenttä, joka lasketaan kaavalla **Summa + Vero**. Lukittu vain luku -muotoinen kenttä, jota ei voi muokata. | &nbsp; |
| **Laskutustyyppi** | Määritetään oletusarvoisesti lähteen todellisesta arvosta. Käyttäjä voi muokata kenttää. | Kun **Veloitettava** valitaan, rivi lisätään laskurivin kokonaissummaan. **Ilmainen** ja **Ei-veloitettava** jättävät rivin pois laskurivin kokonaissummasta. |
| **Valitse tuote** | Määritetään oletusarvoisesti lähteen todellisesta arvosta, tämä on vain luku -kenttä. | Kun luot uuden laskun rivin tiedot ilman taustalla olevaa todellista arvoa, tätä kenttää voi muokata. |
| **Tuote** | Määritetään oletusarvoisesti lähteen todellisesta arvosta, tämä on vain luku -kenttä. | Kun luot uuden laskurivin tiedot ilman varsinaista taustaa, tätä kenttää voidaan muokata, jos **Valitse tuote** -kentän arvoksi on määritetty **Aiemmin luotu tuote**. |
| **Tuotteen nimi** | Määritetään oletusarvoisesti lähteen todellisesta arvosta, tämä on vain luku -kenttä. | Uudessa laskurivin tiedossa, jossa tuotetunnus on valittu luettelosta, tämä kenttä on tuotteen nimi. Käsin luotaville tuotteille tämä kenttä on käsin luotava nimi. |
| **Käsin lisätty kuvaus** | Määritetään oletusarvoisesti lähteen todellisesta arvosta, tämä kenttä on muotoa vain luku. | Kun luot uuden laskurivin tiedot ilman taustalla olevaa todellista arvoa, voit lisätä tuotteelle kuvauksen. |
| **Tapahtumatyyppi** | Määritetään oletusarvoisesti lähteen todellisesta arvosta. Lukittu vain luku -muotoinen kenttä, jota ei voi muokata. | Arvoksi määritetään oletusarvoisesti **Laskutettu myynti**, ja se on lukittu, kun luodaan uusi **Laskurivin tieto**, joka ei perustu todelliseen arvoon.  |
| **Tapahtumaluokka** | Määritetään oletusarvoisesti lähteen todellisesta arvosta. Lukittu vain luku -muotoinen kenttä, jota ei voi muokata. | Määritetään oletusarvon mukaan riippuen siitä, valitseeko käyttäjä luotavaksi **Aika**-, **Kulu**-, **Materiaali**- vai **Maksu**-tyyppisen laskurivin tiedon luodessaan uuden **Laskurivin tiedon** ilman taustalla olevaa todellista arvoa. Muokkaus estetty lukituksella. |

Seuraavat kentät ovat käytettävissä laskurivin tiedossa, joka perustuu välitavoitteeseen:

| Field | Kuvaus | Loppupään vaikutus |
| --- | --- | --- |
| **Laskurivi** | Viittaus **laskurivin tunnukseen**. Lukittu vain luku -muotoinen kenttä, jota ei voi muokata. | Linkin avulla voi siirtyä takaisin laskun otsikkoon. |
| **Kuvaus** | Laskurivin tiedon kuvaus. Arvo määritetään oletusarvoisesti lähteen välitavoitteen kuvauksesta. | &nbsp; |
|**Ulkoinen kuvaus** | Sen laskurivin tiedon kuvaus, joka on määritetty oletusarvoisesti lähteen välitavoitteen kuvauksesta. | Tämän kentän avulla voidaan määrittää, mitä asiakkaalle lähetettävään laskuun tulostetaan. Project Operationsin proformalaskussa ei ole kaikkia tarvittavia toimintoja laskun tulostusasetusten määrittämiseen. |
| **Aloituspäivämäärä** | Arvo määritetään oletusarvoisesti lähteen välitavoitteen **Välitavoite**-päivämäärästä. Lukittu vain luku -muotoinen kenttä, jota ei voi muokata. | &nbsp; |
| **Project** | Määritetään oletusarvoisesti lähteen välitavoitteesta. Lukittu vain luku -muotoinen kenttä, jota ei voi muokata. | &nbsp; |
| **Tehtävä** | Määritetään oletusarvoisesti lähteen välitavoitteesta. Lukittu vain luku -muotoinen kenttä, jota ei voi muokata. | &nbsp; |
| **Tapahtumaluokka** | Lukittu vain luku -muotoinen kenttä, jota ei voi muokata. | &nbsp; |
| **Rooli** | Lukittu vain luku -muotoinen kenttä, jota ei voi muokata. | &nbsp; |
| **Varattavissa oleva resurssi** | Lukittu vain luku -muotoinen kenttä, jota ei voi muokata. | &nbsp; |
| **Resursointiyksikkö** | Lukittu vain luku -muotoinen kenttä, jota ei voi muokata. | &nbsp; |
| **Yksikön aikataulutus** | Lukittu vain luku -muotoinen kenttä, jota ei voi muokata. | &nbsp; |
| **Yksikkö** | Lukittu vain luku -muotoinen kenttä, jota ei voi muokata. | &nbsp; |
| **Hinta** | Arvo määritetään oletusarvoisesti lähteen välitavoitteen summasta. Lukittu vain luku -muotoinen kenttä, jota ei voi muokata. | &nbsp; |
| **Valuutta** | Määritetään oletusarvoisesti lähteen välitavoitteesta. Lukittu vain luku -muotoinen kenttä, jota ei voi muokata. |&nbsp; |
| **Summa** | Arvo määritetään oletusarvoisesti lähteen välitavoitteen summasta. Lukittu vain luku -muotoinen kenttä, jota ei voi muokata. | &nbsp; |
| **Vero** | Arvo määritetään oletusarvoisesti lähteen välitavoitteen verosummasta. Lukittu vain luku -muotoinen kenttä, jota ei voi muokata. | &nbsp; |
| **Koko summa** | Arvo määritetään oletusarvoisesti lähteen välitavoitteen koko summasta. Käyttäjä voi muokata kenttää | &nbsp; |
| **Laskutustyyppi** | Arvo määritetään oletusarvoisesti aina **Veloitettava**. Lukittu vain luku -muotoinen kenttä, jota ei voi muokata. | &nbsp; |
| **Tapahtumatyyppi** | Määritetään oletusarvoisesti lähteen välitavoitteesta. Lukittu vain luku -muotoinen kenttä, jota ei voi muokata. | &nbsp; |
| **Tapahtumaluokka** | Määritetään oletusarvoisesti lähteen välitavoitteesta. Lukittu vain luku -muotoinen kenttä, jota ei voi muokata. | &nbsp; |

### <a name="create-new-invoice-line-details"></a>Uuden laskurivin tietojen luominen

Ajan ja materiaalin laskuriveillä voi luoda uusia laskurivin tietoja. Näiden laskurivin tietojen perusteena ei ole toteutunut arvo. Ajan ja materiaalin laskurivillä sisällytetyille tapahtumaluokille voi luoda uuden laskurivin tiedon sopimusriville valitsemalla **Uusi**.

## <a name="refresh-invoice-transactions"></a>Laskutapahtumien päivittäminen

Jos todellisia arvoja saadaan laskun luomisen jälkeen, nämä todelliset arvot voidaan sisällyttää laskuun.

1. Lisää tietoihin **keskeneräisen laskutuksen näkymässä** merkintä **Valmis laskuttamista varten**.   
2. Avaa proformalaskun luonnos ja valitse **Toiminnot**-valintanauhassa **Päivitä laskurivin tapahtumat**.

  Tällä tavoin voidaan luoda laskurivin tiedot todelliselle arvolle, jonka päivämäärä on menneisyydessä ja jossa on merkintä **Valmis laskuttamista varten** mutta jota ei ole sisällytetty laskuun.

## <a name="product-based-invoice-lines"></a>Tuotepohjaiset laskurivit

Project Operationsissa tuotteille voi luoda laskurivejä, joita ei käytetä mihinkään projektiin tai joita käytetään kaikissa projekteissa yhdessä projektipohjaisten laskurivien kanssa. Nämä laskurivit luodaan tuotepohjaisina sopimusriveinä, ja ne lisätään tuotepohjaisina laskuriveinä sen jälkeen, kun ne merkitty valmiiksi laskutettaviksi.

Kun tuotepohjaiset laskurivit on lisätty, niitä ei voi muuttaa. Ne voidaan kuitenkin poistaa proformalaskun luonnoksesta.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
