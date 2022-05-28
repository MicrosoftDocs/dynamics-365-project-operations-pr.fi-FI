---
title: Proformamuotoisen projektipohjaisen laskun hallinta
description: Tässä aiheessa on tietoja proformamuotoisten projektipohjaisten laskujen hallinnasta ja niiden parissa työskentelystä.
author: rumant
ms.date: 04/05/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: c61b0d887ae35988f1765d40de0447aa5fd7efd4
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/14/2022
ms.locfileid: "8593746"
---
# <a name="manage-a-proforma-project-based-invoice"></a>Proformamuotoisen projektipohjaisen laskun hallinta

_**Käytetään:** Project Operationsin resursseihin ja ei-varastoitaviin perustuvissa skenaarioissa_

Dynamics 365 Project Operationsissa proformalaskut muodostetaan Dynamics 365 Salesin laskujen laajennuksena. Salasin ja Project Operationsin laskutusprosessissa on kuitenkin monenlaisia eroja. Project Operationsissa ei voi esimerkiksi luoda uutta laskua **Laskuluettelo**-sivulla, vaikka se on mahdollista Salesissa. Nämä erot ja laajennukset ovat käytössä siksi, että voidaan tukea sellaisten projektien laskutusprosesseja, jotka eroavat tyypillisestä myyntitilauksen laskusta.

> [!IMPORTANT]
> Näiden erojen vuoksi Salesin ja Project Operationsin laskuja ei voi käyttää toistensa vaihtoehtoina.

## <a name="invoice-header"></a>Laskun otsikko

Project Operationsin proformalaskun otsikossa on seuraavat tiedot.

| Kenttä | Sijainti | Kuvaus |
| --- | --- | --- | 
| **Laskun tunnus** | **Yhteenveto**-välilehti | Tämä tunnus luodaan automaattisesti, kun proformalasku luodaan. Lukittu vain luku -muotoinen kenttä, jota ei voi muokata. Tätä kenttää käytetään kunkin proformalaskun viitteenä. |
| **Nimi** | **Yhteenveto**-välilehti | Arvoksi määritetään oletusarvoisesti projektisopimuksen nimi. Tätä kenttää voi muokata. | 
| **Valuutta** | **Yhteenveto**-välilehti | Arvoksi määritetään oletusarvoisesti projektisopimuksen valuutta. Lukittu vain luku -muotoinen kenttä, jota ei voi muokata. |
| **Hinnasto** | **Yhteenveto**-välilehti | Arvoksi määritetään oletusarvoisesti projektisopimuksen hinnasto. Lukittu vain luku -muotoinen kenttä, jota ei voi muokata. | 
| **Mahdollisuus** | **Yhteenveto**-välilehti | Viittaus linkitettyyn mahdollisuuteen. Lukittu vain luku -muotoinen kenttä, jota ei voi muokata. | 
| **Palvelusopimus** | **Yhteenveto**-välilehti | Viittaus linkitettyyn projektisopimukseen. Lukittu vain luku -muotoinen kenttä, jota ei voi muokata. | 
| **Asiakas** | **Yhteenveto**-välilehti | Viittaus linkitettyyn projektisopimukseen. Lukittu vain luku -muotoinen kenttä, jota ei voi muokata. |
| **Kuvaus** | **Yhteenveto**-välilehti | Laskua kuvaava tekstikenttä. Tätä kenttää voi muokata. | 
| **Laskutusosoite**- ja liittyvät kentät | **Yhteenveto-välilehti** | Oletusarvot määritetään projektisopimuksen asiakkaasta. Tätä kenttää voi muokata.  | 
| **Tila** | **Yhteenveto**-välilehti | Määrittää seuraavat vaihtoehdot: **Aktiivinen**, **Suljettu**, **Maksettu** ja **Peruutettu**, ja sitä voi muokata. Project Operations ei tue seuraavia tietoja: **Suljettu** ja **Peruutettu**. </br> Tilaksi määritetään **Aktiivinen**, kun lasku luodaan. </br>**Maksettu**-tila on syytä määrittää vastan, kun lasku on vahvistettu.  | 
| **Projektin laskun tila** | **Yhteenveto**-välilehti | Määrittää seuraavat vaihtoehdot: **Luonnos**, **Tarkistuksessa**, **Vahvistettu**, ja sitä voi muokata. Laskua voi muokata sekä **Luonnos**- että **Tarkistettavana**-tilassa. Laskua ei voi muokata sen jälkeen, kun se on vahvistettu. | 
| **Eritelty summa** | **Yhteenveto**-välilehti | Kaikkien laskurivien yhteenlaskettu summa ennakoiden ja vähennysten jälkeen. Lukittu vain luku -muotoinen kenttä, jota ei voi muokata.  Lopullinen summa lasketaan tämän kentän avulla. | 
| **Alennus (%)** | **Yhteenveto**-välilehti | Tätä kenttää voi muokata antamalla alennusprosentti. Project Operations -toiminnot eivät tue tätä kenttää. Tämä kenttää ei tueta.|  
| **Alennussumma** | **Yhteenveto**-välilehti | Tätä kenttää voi muokata antamalla alennussumma. Project Operations -toiminnot eivät tue tätä kenttää. Tämä kenttää ei tueta. |  
| **Summa ilman rahtikuluja** | **Yhteenveto-välilehti** | Laskun kokonaissumma alennusten jälkeen. Lukittu vain luku -muotoinen kenttä, jota ei voi muokata. Lopullinen summa lasketaan tämän kentän avulla.  | 
| **Rahti** | **Yhteenveto**-välilehti | Tätä kenttää voi muokata antamalla rahti. Project Operations -toiminnot eivät tue tätä kenttää. Tämä kenttää ei tueta. |
| **Vero yhteensä** | **Yhteenveto**-välilehti | Laskun kaikkien laskurivien vero yhteensä. Lukittu vain luku -muotoinen kenttä, jota ei voi muokata. | 
| **Loppusumma** | **Yhteenveto**-välilehti | Yhteenlaskettu summa alennusten ja verojen jälkeen. Yhteenlaskettu summa on summa, joka asiakkaan on maksettava. | 

## <a name="project-based-invoice-lines"></a>Projektipohjaiset laskurivit

Project Operationsissa jokaisella projektisopimusrivillä on aina yksi laskurivi. Laskurivi luodaan, vaikka todellisia arvoja ei olisi. Proformalaskurivillä on seuraavat tiedot.

| Kenttä | Sijainti | Kuvaus | 
| --- | --- | --- |
| **Laskun tunnus** | **Yleiset**-välilehti | Viittaus laskun tunnukseen. Lukittu vain luku -muotoinen kenttä, jota ei voi muokata. Laskun tunnuksen linkin avulla voi siirtyä takaisin laskun otsikkoon. | 
| **Nimi** | **Yleiset**-välilehti | Laskurivin nimi määritetään oletusarvoisesti sopimusrivin nimestä. Tätä kenttää voi muokata. |
| **Project** | **Yleiset**-välilehti | Liittyvän projektin sopimusrivillä oleva projekti. Lukittu vain luku -muotoinen kenttä, jota ei voi muokata. Projektiin voi siirtyä projektin linkin avulla. | 
| **Laskutustapa** | **Yleiset**-välilehti | Liittyvän projektin sopimusrivillä oleva laskutustapa. Lukittu vain luku -muotoinen kenttä, jota ei voi muokata. |
| **Sopimusrivin summa** | **Yleiset**-välilehti | Liittyvän projektin sopimusrivillä olevan sopimuksen summa. Lukittu vain luku -muotoinen kenttä, jota ei voi muokata. | 
| **Laskutettu päivämäärään** | **Yleiset**-välilehti | Tämän laskun kaikkien laskurivien tietojen yhteenlasketut summat. Lukittu vain luku -muotoinen kenttä, jota ei voi muokata. | 
| **Summa** | **Yleiset**-välilehti | Tämän laskun kaikkien veloitettavien laskurivien tietojen yhteenlasketut summat. Lukittu vain luku -muotoinen kenttä, jota ei voi muokata. Laskun otsikon lopullinen summa lasketaan tämän kentän avulla. | 
| **Vero** | **Yleiset**-välilehti | Tämän laskurivin kaikkien laskurivin tietojen yhteenlasketut verosummat. Lukittu vain luku -muotoinen kenttä, jota ei voi muokata. Laskun otsikon lopullinen verosumma lasketaan tämän kentän avulla. | 
| **Koko summa** | **Yleiset**-välilehti | Tämän laskurivin kaikkien veloitettavien laskurivin tietojen yhteenlasketut kokonaissummat (**vero + summat)**. Lukittu vain luku -muotoinen kenttä, jota ei voi muokata. Laskun otsikon lopullinen summa lasketaan tämän kentän avulla. |

## <a name="invoice-line-details"></a>Laskurivin tiedot

Jokainen projektilaskun laskurivi sisältää laskurivin tiedot. Nämä rivitiedot liittyvät laskuttamattomaan toteutuneeseen myyntiin ja niihin sopimusriviin liittyviin välitavoitteisiin, joihin laskurivi viittaa. Kaikissa näissä tapahtumissa on merkintä **Valmis laskuttamista varten**.

**Aika- ja materiaalilasku** -rivillä laskun tiedot on ryhmitelty ryhmiin **Laskutettava**, **Ei-laskutettava** ja **Ilmainen** sivulla **Laskurivi**. **Veloitettavan laskurivin** tiedot listään laskurivin kokonaissummaan. **Ilmaisia** ja **ei-veloitettavia toteutuneita** ei lisätä laskurivin kokonaissummaan.

**Kiinteähintainen lasku** -riviä varten laskurivin tiedot luodaan välitavoitteista, jotka on merkitty **Valmis laskutettavaksi** liittyvällä sopimusrivillä. Kun laskurivin tiedot on luotu välitavoitteesta, välitavoitteen laskutustilaksi päivitetään **Asiakaslasku luotu**.

### <a name="edit-invoice-line-details"></a>Laskurivin tietojen muokkaaminen

Seuraavat kentät ovat käytettävissä laskun rivin tiedossa, joka perustuu laskuttamattomaan toteutuneeseen myyntiin.

| Kenttä | Kuvaus |
| --- | --- | 
| **Laskurivi** | Viittaus **laskurivin tunnukseen**. Tätä kenttää on vain luku -muotoa, eikä sitä voi muokata. Tämän linkin avulla voi siirtyä takaisin laskun otsikkoon. | 
| **Kuvaus** | Laskurivin tiedon kuvaus. Määritetään oletusarvoisesti **Aikamerkintä**-kohdan **Sisäiset kommentit** -kentästä ja **Kulumerkintä**-kohdan **Kuvaus**-kentästä. Kenttää voi muokata.| 
| **Ulkoinen kuvaus** | Laskurivin tiedon kuvaus. Määritetään oletusarvoisesti **Aikamerkintä**-kohdan **Ulkoiset kommentit** -kentästä ja **Kulumerkintä**-kohdan **Kuvaus**-kentästä. Kenttää voi muokata. Tällä kuvauksella voidaan määrittää, mitä asiakkaalle lähetettävään laskuun tulostetaan. Project Operationsin proformalaskussa ei ole kaikkia tarvittavia toimintoja laskun tulostusasetusten määrittämiseen. | 
| **Aloituspäivämäärä** | Tämä on vain luku -kenttä, joka määritetään oletusarvoisesti lähteen todellisesta arvosta. |
| **Project** | Tämä on vain luku -kenttä, joka määritetään oletusarvoisesti lähteen todellisesta arvosta projektiin liittyvällä sopimusrivillä. |  
| **Tehtävä** | Määritetään oletusarvoisesti lähteen todellisesta arvosta. Lukittu vain luku -muotoinen kenttä, jota ei voi muokata. |
| **Tapahtumaluokka** | Määritetään oletusarvoisesti lähteen todellisesta arvosta. Lukittu vain luku -muotoinen kenttä, jota ei voi muokata. | 
| **Rooli** | Määritetään oletusarvoisesti lähteen todellisesta arvosta. Lukittu vain luku -muotoinen kenttä, jota ei voi muokata. |  
| **Varattavissa oleva resurssi** | Määritetään oletusarvoisesti lähteen todellisesta arvosta. Lukittu vain luku -muotoinen kenttä, jota ei voi muokata. | 
| **Resursoiva yritys** | Määritetään oletusarvoisesti lähteen todellisesta arvosta. Lukittu vain luku -muotoinen kenttä, jota ei voi muokata. | 
| **Resursointiyksikkö** | Määritetään oletusarvoisesti lähteen todellisesta arvosta. Lukittu vain luku -muotoinen kenttä, jota ei voi muokata. | 
| **Määrä** | Määritetään oletusarvoisesti lähteen todellisesta arvosta. Lukittu vain luku -muotoinen kenttä, jota ei voi muokata. |  
| **Yksikön aikataulutus** | Ajan laskurivin tiedoksi on aina määritetty aika, eikä sitä voi muokata. Kulujen arvo määritetään oletusarvoisesti lähteen toteutuneesta kulusta. Lukittu vain luku -muotoinen kenttä, jota ei voi muokata. | 
| **Yksikkö** | Määritetään oletusarvoisesti lähteen todellisesta arvosta. Lukittu vain luku -muotoinen kenttä, jota ei voi muokata. |  
| **Hinta** | Määritetään oletusarvoisesti lähteen todellisesta arvosta. Lukittu vain luku -muotoinen kenttä, jota ei voi muokata. |
| **Valuutta** | Määritetään oletusarvoisesti lähteen todellisesta arvosta. Lukittu vain luku -muotoinen kenttä, jota ei voi muokata. | 
| **Summa** | Määritetään oletusarvoisesti lähteen todellisesta arvosta. Lukittu vain luku -muotoinen kenttä, jota ei voi muokata. | 
| **Vero** | Määritetään oletusarvoisesti lähteen todellisesta arvosta. Kenttää voi muokata.| 
| **Koko summa** | Laskennallinen kenttä, joka lasketaan kaavalla **Summa + Vero**. Lukittu vain luku -muotoinen kenttä, jota ei voi muokata. | 
| **Laskutustyyppi** | Määritetään oletusarvoisesti lähteen todellisesta arvosta. Kenttää voi muokata. Kun **Veloitettava** valitaan, rivi lisätään laskurivin kokonaissummaan. **Ilmainen** ja **Ei-veloitettava** jättävät rivin pois laskurivin kokonaissummasta.| 
| **Valitse tuote** | Määritetään oletusarvoisesti lähteen todellisesta arvosta. Lukittu vain luku -muotoinen kenttä, jota ei voi muokata. |
| **Tuote** | Määritetään oletusarvoisesti lähteen todellisesta arvosta. Lukittu vain luku -muotoinen kenttä, jota ei voi muokata. | 
| **Tuotteen nimi** | Määritetään oletusarvoisesti lähteen todellisesta arvosta. Lukittu vain luku -muotoinen kenttä, jota ei voi muokata. |  
| **Käsin lisätty kuvaus** | Määritetään oletusarvoisesti lähteen todellisesta arvosta. Lukittu vain luku -muotoinen kenttä, jota ei voi muokata. |
| **Tapahtumatyyppi** | Tämä on vain luku -kenttä, joka määritetään oletusarvoisesti lähteen todellisesta arvosta **Laskutettuihin myynteihin**. |  
| **Tapahtumaluokka** | Määritetään oletusarvoisesti lähteen todellisesta arvosta. Lukittu vain luku -muotoinen kenttä, jota ei voi muokata. | 

Seuraavat kentät ovat käytettävissä laskurivin tiedossa, joka perustuu välitavoitteeseen.

| Kenttä | Kuvaus |
| --- | --- | 
| **Laskurivi** | Viittaus **laskurivin tunnukseen**. Lukittu vain luku -muotoinen kenttä, jota ei voi muokata. Linkin avulla voi siirtyä takaisin laskun otsikkoon.  | 
| **Kuvaus** | Laskurivin tiedon kuvaus. Arvo määritetään oletusarvoisesti lähteen välitavoitteen kuvauksesta. | 
|**Ulkoinen kuvaus** | Sen laskurivin tiedon kuvaus, joka on määritetty oletusarvoisesti lähteen välitavoitteen kuvauksesta. Tämän kentän avulla voidaan määrittää, mitä asiakkaalle lähetettävään laskuun tulostetaan. Project Operationsin proformalaskussa ei ole kaikkia tarvittavia toimintoja laskun tulostusasetusten määrittämiseen. | 
| **Aloituspäivämäärä** | Arvo määritetään oletusarvoisesti lähteen välitavoitteen **Välitavoite**-päivämäärästä. Lukittu vain luku -muotoinen kenttä, jota ei voi muokata. | 
| **Project** | Määritetään oletusarvoisesti lähteen välitavoitteesta. Lukittu vain luku -muotoinen kenttä, jota ei voi muokata. |
| **Tehtävä** | Määritetään oletusarvoisesti lähteen välitavoitteesta. Lukittu vain luku -muotoinen kenttä, jota ei voi muokata. | 
| **Tapahtumaluokka** | Lukittu vain luku -muotoinen kenttä, jota ei voi muokata. |
| **Rooli** | Lukittu vain luku -muotoinen kenttä, jota ei voi muokata. | 
| **Varattavissa oleva resurssi** | Lukittu vain luku -muotoinen kenttä, jota ei voi muokata. | 
| **Resursointiyksikkö** | Lukittu vain luku -muotoinen kenttä, jota ei voi muokata. | 
| **Yksikön aikataulutus** | Lukittu vain luku -muotoinen kenttä, jota ei voi muokata. | 
| **Yksikkö** | Lukittu vain luku -muotoinen kenttä, jota ei voi muokata. | 
| **Hinta** | Arvo määritetään oletusarvoisesti lähteen välitavoitteen summasta. Lukittu vain luku -muotoinen kenttä, jota ei voi muokata. |
| **Valuutta** | Määritetään oletusarvoisesti lähteen välitavoitteesta. Lukittu vain luku -muotoinen kenttä, jota ei voi muokata. |
| **Summa** | Arvo määritetään oletusarvoisesti lähteen välitavoitteen summasta. Lukittu vain luku -muotoinen kenttä, jota ei voi muokata. | 
| **Vero** | Arvo määritetään oletusarvoisesti lähteen välitavoitteen verosummasta. Lukittu vain luku -muotoinen kenttä, jota ei voi muokata. |
| **Koko summa** | Arvo määritetään oletusarvoisesti lähteen välitavoitteen koko summasta. Kenttää voi muokata. | 
| **Laskutustyyppi** | Arvo määritetään oletusarvoisesti aina **Veloitettava**. Lukittu vain luku -muotoinen kenttä, jota ei voi muokata. |
| **Tapahtumatyyppi** | Määritetään oletusarvoisesti lähteen välitavoitteesta. Lukittu vain luku -muotoinen kenttä, jota ei voi muokata. | 
| **Tapahtumaluokka** | Määritetään oletusarvoisesti lähteen välitavoitteesta. Lukittu vain luku -muotoinen kenttä, jota ei voi muokata. | 

## <a name="refresh-invoice-transactions"></a>Laskutapahtumien päivittäminen

Jos todellisia arvoja saadaan laskun luomisen jälkeen, nämä todelliset arvot voidaan sisällyttää laskuun.

1. Lisää tietoihin **keskeneräisen laskutuksen näkymässä** merkintä **Valmis laskuttamista varten**.   
2. Avaa proformalaskuluonnos ja valitse **Toiminnot**-valintanauhasta **Päivitä laskurivin tapahtumat**.

  Laskurivin tiedot luodaan toteutuneille arvoille, jotka on päivätty menneisyyteen ja merkitty **Valmiina laskutettavaksi**, mutta joita ei ole laskussa.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
