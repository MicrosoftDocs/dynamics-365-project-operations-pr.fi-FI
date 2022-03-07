---
title: Kulujen hallintaparametrit
description: Seuraavat parametrit ohjaavat käyttäytymistä kulunhallinnassa.
author: KimANelson
ms.date: 01/12/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TrvParameters
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: suvaidya
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: 2ef48f844656ff5197ae1731fb3f9bdf91a1a906b16f35bb2124469743a9e954
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/06/2021
ms.locfileid: "6991347"
---
# <a name="expense-management-parameters"></a>Kulujen hallintaparametrit


Parametrit ohjaavat yleistä käyttäytymistä kulunhallinnassa.

### <a name="general"></a>Yleistiedot

| **Field**                                                | **Kuvaus**                                                 |
|----------------------------------------------------------|---------------------------------------------------------------------|
| **Kilometrikorvauksen vakiohinta**                             | Anna kilometrikulujen korvausprosentti. Hinta kerrotaan kululle syötetyllä kilometrikorvauksella, joka laskee matkakululle korvattavan summan.                       |
|**Henkilökohtaiset kulut, jotka maksaa**                             | Valitse henkilö, joka on vastuussa kaikkien henkilökohtaisiksi luokiteltujen luottokorttitapahtumien summien maksuista.                                                                                                     |
|**Näytä koko kuluraportti porauksen aikana**               | Valitse tämä vaihtoehto, jos haluat näyttää kuluraportin kaikki kulut, kun alkuperäisen asiakirjan tietoja tarkastellaan tietyn tositteen perusteella, joka luotiin kuluraportin kirjaamisen yhteydessä.              |
|**Matkan valtuutus etukäteen on pakollista**                 | Valitse tämä vaihtoehto, jos haluat edellyttää, että matkaehdotus lähetetään ja hyväksytään, ennen kuin työntekijä voi lähettää kuluraportin.                                                                    |
|**Salli jakeluiden muokkaaminen ennen kirjausta**            | Valitse, voidaanko kuluraportin jakaumia muokata ennen sen kirjaamista.                                                                                                                 |
|**Kulun hallintakäytäntöjen arvioiminen**                     | Valitse, milloin kulut arvioidaan, jotta voidaan määrittää, onko kulukäytäntöä rikottu. Kuluja voidaan tarkastaa rikkomusten varalta, kun kulutapahtuma syötetään ja tallennetaan tai kun kulu lähetetään hyväksyttäväksi. Tarvittavien kuittien käytäntösäännöt tarkastetaan, kun kulurivi tallennetaan.                   |
|**Salli konserniyritysten väliset kulurivit**                         | Valitse, sallitaanko muiden yritysten kulujen syöttäminen kuluraportin sisällä.                                                                                                          |
|**Salli luottokorttikulujen vaihtokurssin muokkaaminen** | Valitse tämä vaihtoehto, jos haluat, että käyttäjä voi muokata tuotujen luottokorttikulujen vaihtokurssia.                                                                        |
|**Näytettävät monitasoiset hierarkiakentät**                  | Valitse näytettävät hyväksyjäkentät, kun kuluraportin työnkulun määritystyypiksi on asetettu hierarkia ja hierarkian valinta on asetettu käyttämään kulujen monitasoista hyväksyntähierarkiaa. Kun työnkulkuun käytetään monitasoista hyväksyntähierarkiaa, valitut kentät näytetään ja niitä voidaan muokata kuluraportissa. |
|**Anna työntekijän luottokortin numero (heinäkuun 2017 päivitys)**     | Valitse, voidaanko 15 tai 16 merkin numero kirjoittaa ja tallentaa työntekijän **Luottokortit**-sivun **Kortin tunnus** -kenttään.                                                                          |

### <a name="financial"></a>Rahoitustoiminta

| **Kenttä**                                                            | **Kuvaus**     |
|----------------------------------------------------------------------|------------------------------------|
|**Kirjanpidon päiväkirjan nimi**                                         | Valitse sen kirjanpidon kirjauskansion nimi, jolle hyväksytyt kuluraportit kirjataan.            |
|**Ota käyttöön veronpalautus kuluista**                                  | Valitse tämä vaihtoehto, jos haluat ottaa kulujen veronpalautuksen käyttöön niihin oikeuttavissa kuluissa. Tätä vaihtoehtoa ei voi ottaa käyttöön, jos Yhdysvaltojen arvonlisävero ja käyttöverosäännöt on otettu käyttöön.      |
|**Käteisennakko maksujen kirjaaminen heti**                                     | Valitse tämä vaihtoehto, jos haluat kirjata hyväksytyn käteisennakon, kun maksu- ja siirtoprosessi on valmis. Jos tätä vaihtoehtoa ei ole valittu, maksu- ja siirtoprosessi luo kirjaamattoman yleisen kirjauskansion. |
|**Korkaa kirjanpitopäivämäärä kirjauksen aikana**                             | Valitse tämä vaihtoehto, jos haluat päivittää kirjauspäivämäärän kulujen kirjaamisen yhteydessä, jos nykyinen kausi on pidossa tai suljettu. Kirjanpitopäiväksi tulee seuraava avoin kausi.   |
|**Salli tapahtumien ryhmittely maksutavassa määritetyn vastatilin perusteella**      | Valitse tämä vaihtoehto, jos haluat tehdä yhteenvedon kuluraportin kulutapahtumista kulujen maksutavassa määritetyn vastatilin perusteella.   
|**Sisällytetty vero**                                                   | Valitse tämä vaihtoehto, jos haluat lisätä arvonlisäveron oletusarvoisesti kulusummaan.             |
|**Vapauta varaukset matkustusehdotusten sulkemisen yhteydessä**            | Valitse tämä vaihtoehto, jos haluat vapauttaa varatut varat, kun hyväksytty matkustusehdotus suljetaan.                                                                                   |
|**Salli matka ehdotuksen lähettäminen budjetin ylittyessä budjettirekisterissä ja projektibudjetissa** | Valitse tämä vaihtoehto, jos haluat, että työntekijät voivat lähettää hyväksyttäväksi matkustusehdotuksia, jotka ylittäisivät joko budjettirekisterissä määritetyn sallitun budjetin tai projektin sallitun budjetin.            |
|**Salli kuluraportin lähettäminen budjetin ylittyessä budjettirekisterissä ja projektibudjetissa**    | Valitse tämä vaihtoehto, jos haluat, että työntekijät voivat lähettää hyväksyttäväksi kuluraportteja, jotka ylittäisivät joko budjettirekisterissä määritetyn sallitun budjetin tai projektin sallitun budjetin.                |
|**Salli kuluraportin hyväksyminen vain budjetin ylittyessä budjettirekisterissä**                | Valitse tämä vaihtoehto, jos haluat sallia hyväksyjien hyväksyä kuluraportit, jotka ylittävät budjettirekisterissä määritetyn sallitun budjetin.                                                                       |

### <a name="per-diem"></a>Päiväraha

| **Field**                             | **Kuvaus**             |
|---------------------------------------|--------------------------------------------------------------------------------------|
|**Päivärahan vähimmäistunnit**           | Määritä vähimmäistuntien oletusmäärä, joka työntekijän on työskenneltävä päivässä, jotta hän voi saada matkakulujen päivä rahaa.  Tätä arvoa käytetään vain oletusarvona päivärahatasojen Vähimmäistunnit-kentässä.                                                                                      |
|**Ateriaprosentti**                          | Määritä niiden aterioiden korvauksen oletusprosenttiosuus, joita käytetään matkustamiseen liittyvän kulun ensimmäisenä ja viimeisenä päivänä silloin, kun **Laske ateriavähennys** -kentän arvoksi on määritetty joko **Ateriatyyppi päivässä** tai **Aterioiden määrä päivässä**. Ensimmäisen ja viimeisen päivän työpäivä voi olla tavallista arkipäivää lyhyempi. Tämän vuoksi nämä päivärahasummat voivat poiketa vakiosummasta. Jos prosenttiarvoksi on määritetty 0, ensimmäisen ja viimeisen päivän vähennykset ovat 0,00. |
|**Hotelliprosentti**                        | Määritä niiden hotellien oletusprosenttiosuus, joita käytetään matkustamiseen liittyvän kulun ensimmäisinä ja viimeisinä päivinä. Ensimmäisen ja viimeisen päivän työpäivä voi olla tavallista arkipäivää lyhyempi. Tämän vuoksi nämä päivärahasummat voivat poiketa vakiosummasta. Jos prosenttiarvoksi on määritetty 0, ensimmäisen ja viimeisen päivän vähennykset ovat 0,00.                                              |
|**Muu prosentti**                        | Määritä niiden muiden kulujen oletusprosenttiosuus, joita käytetään matkustamiseen liittyvän kulun ensimmäisinä ja viimeisinä päivinä. Ensimmäisen ja viimeisen päivän työpäivä voi olla tavallista arkipäivää lyhyempi. Tämän vuoksi nämä päivärahasummat voivat poiketa vakiosummasta. Jos prosenttiarvoksi on määritetty 0, ensimmäisen ja viimeisen päivän vähennykset ovat 0,00.                                                                                                     |
|**Aamiaisen prosenttiosuuden vähennys** | Anna prosentti, jonka verran päivärahaa vähennetään aamiaisen osalta. Jos esimerkiksi työntekijä saa ilmaisen aamiaisen, haluat ehkä vähentää päivärahan määrää 10 prosentilla.                               |
|**Lounaan prosenttiosuuden vähennys**    | Anna prosentti, jonka verran päivärahaa vähennetään lounaan osalta. Jos esimerkiksi työntekijä saa ilmaisen lounaan, haluat ehkä vähentää päivärahan määrää 15 prosentilla.                                       |
|**Päivällisen prosenttiosuuden vähennys**   | Anna prosentti, jonka verran päivärahaa vähennetään päivällisen osalta. Jos esimerkiksi työntekijä saa ilmaisen päivällisen, haluat ehkä vähentää päivärahan määrää 25 prosentilla.                                     |
|**Laske ateriavähennys**         | Valitse, miten järjestelmä laskee päivärahan ateriavähennyksen, valitsemalla, perustuuko vähennys matka- tai päiväkohtaiseen ateriatyyppiin vai perustuuko vähennys aterioiden määrään, joka on sallittu päivässä.|
|**Päivärahan pyöristys**                  | Valitse päivärahakulujen pyöristystyyppi. Jos valitset normaalin pyöristyksen, kaikki päivärahakulut, joiden määrä on 0,50 tai yli, pyöristetään ylöspäin lukuun 1,00, ja kaikki päivärahakulut, joiden summa on pienempi kuin 0,50, pyöristetään alaspäin lukuun 0,00.                                                                                              |
|**Päivärahalaskelman peruste**         | Valitse, perustuvatko päivärahasummat kalenteripäivään vai 24 tunnin jaksoon.       |

### <a name="fax-cover-pages"></a>Faksaa kansilehdet

| **Field**                      | **Kuvaus**            |
|--------------------------------|-----------------------------------------------------------------------------|
| **Ohjeet**                   | Kirjoita ohjeet, joita työntekijöiden on noudatettava, kun he luovat kansilehden faksiin, jota käytetään kuluraporttiin liittyvien kuittien lähettämiseen. Jos haluat lisätä kielikohtaisen tekstin, joka näkyy käyttäjän kielen mukaan, paina **Käännökset**-painiketta. |
|**Käyttäjätunnus (viivakooditiedot)** | Valitse tämä vaihtoehto, jos haluat tallentaa työntekijän yksilöivän tunnisteen viivakoodiin, jota käytetään faksin kansilehdellä.                 |
|**Viivakoodi**                      | Valitse faksin kansilehdellä käytettävä viivakoodi. Kulujen hallinta tukee viivakoodeja 39 ja 128.               |

### <a name="anti-corruption"></a>Korruption vastainen

|                 <strong>Kenttä</strong>                 |                                                                                                                                                                                            <strong>Kuvaus</strong>                                                                                                                                                                                             |
|--------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|  <strong>Näytä korruption vastainen todistus</strong>  | Valitse tämä vaihtoehto, jos haluat näyttää korruption vastaisen tekstin, kun uusi kuluraportti luodaan. Tällöin voidaan ottaa käyttöön tietyt kululuokat, jotka edellyttävät, että kuluraporttiin valitaan korruption vastainen todistus. Esimerkiksi hallituksen virallisiin kuluihin liittyvä lahjaluokka voi edellyttää, että työntekijä vahvistaa, että kulu vastaa hallituksen virkamiehiin liittyvää käytäntöä. |
| <strong>Korruption vastainen sanoma lähettäjälle</strong> |                                                                                             Kirjoita teksti, joka näytetään työntekijälle uutta kuluraporttia luotaessa. Jos haluat lisätä kielikohtaisen tekstin, joka näkyy käyttäjän kielen mukaan, paina<strong>Käännökset</strong>-painiketta.                                                                                             |
| <strong>Korruption vastainen sanoma hyväksyjälle</strong>  |                                                                                             Kirjoita teksti, joka näytetään hyväksyjälle uutta kuluraporttia luotaessa. Jos haluat lisätä kielikohtaisen tekstin, joka näkyy käyttäjän kielen mukaan, paina<strong>Käännökset</strong>-painiketta.                                                                                             |



[!INCLUDE[footer-include](../includes/footer-banner.md)]