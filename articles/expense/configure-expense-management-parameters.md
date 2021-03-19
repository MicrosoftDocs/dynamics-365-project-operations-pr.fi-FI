---
title: Kulujen hallintaparametrien määrittäminen
description: Tässä aiheessa kuvataan parametreja, joilla hallitaan yleistä toimintaa kulujen hallinnassa.
author: suvaidya
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: suvaidya
ms.openlocfilehash: 93cb95ffc0348a1ad1905fbf308477d18e589185
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5276659"
---
# <a name="configure-expense-management-parameters"></a>Kulujen hallintaparametrien määrittäminen

_**Käytetään:** Project Operationsin resursseihin ja ei-varastoitaviin perustuvissa skenaarioissa_

Tässä aiheessa kuvataan parametreja, joilla hallitaan yleistä toimintaa kulujen hallinnassa.

## <a name="general"></a>Yleistiedot

| Field                                                    | Kuvaus |
|----------------------------------------------------------|-------------|
| Kilometrikorvauksen vakiohinta                                 | Anna kilometrikulujen korvausprosentti. Tämä hinta kerrotaan kululle syötetyllä kilometrikorvaukella, joka laskee matkakululle korvattavan summan. |
| Tarkista kulun tarkoitus                                 | Ota tämä asetus käyttöön, jos haluat rajoittaa käyttäjät aiemmin luotuun arvojoukkoon, joka on määritetty **Kuluraportin tarkoitus** -kentän avulla, kun he luovat kuluraportteja. |
| Henkilökohtaiset kulut, jotka maksaa                                | Valitse henkilö, joka on vastuussa kaikkien luottokorttitapahtumien summien maksuista, jotka on luokiteltu henkilökohtaisiksi. |
| Näytä koko kuluraportti porauksen aikana               | Valitse tämä vaihtoehto, jos haluat näyttää kuluraportin kaikki kulut, kun alkuperäisen asiakirjan tietoja tarkastellaan tietyn tositteen perusteella, joka luotiin kuluraportin kirjaamisen yhteydessä. |
| Matkan valtuutus etukäteen on pakollista                 | Valitse tämä vaihtoehto, jos haluat edellyttää, että matkaehdotus lähetetään ja hyväksytään, ennen kuin työntekijä voi lähettää kuluraportin. |
| Salli jakeluiden muokkaaminen ennen kirjausta            | Valitse, voidaanko kuluraportin jakaumia muokata ennen sen kirjaamista. |
| Kulun hallintakäytäntöjen arvioiminen                     | Valitse, milloin kulut arvioidaan, jotta voidaan määrittää, onko kulukäytäntöä rikottu. Kuluja voidaan arvioida rikkomusten varalta, kun kulutapahtuma syötetään ja tallennetaan tai kun kulu lähetetään hyväksyttäväksi. Tarvittavien kuittien käytäntösäännöt arvioidaan, kun kulurivi tallennetaan. |
| Salli konserniyritysten väliset kulurivit                         | Valitse, voidaanko muiden yritysen kuluja syöttää kuluraporttiin. |
| Salli luottokorttikulujen vaihtokurssin muokkaaminen | Valitse tämä vaihtoehto, jos haluat, että käyttäjä voi muokata tuotujen luottokorttikulujen vaihtokurssia. |
| Näytettävät monitasoiset hierarkiakentät                  | Valitse, mitkä hyväksyjän kentät näytetään, kun työnkulun delegointityypiksi on määritetty hierarkia, ja **Hierarkia**-valinta on määritetty käyttämään hyväksyntähierarkiaa, kulujen monitasoista hyväksyntää. Kun monitasoista hyväksyntähierarkiaa käytetään työnkulussa, valitut kentät näkyvät kuluraportissa, ja niitä voi muokata. |
| Anna työntekijän luottokortin numero                        | Valitse, voidaanko 15 merkin tai 16 merkin numero kirjoittaa ja tallentaa yön tekijän **Luottokortit**-sivun **Kortin tunnus** -kenttään. |
| Tarkista matkaehdotuksen tarkoitus                      | Ota tämä asetus käyttöön, jos haluat rajoittaa käyttäjät aiemmin luotuun arvojoukkoon, joka on määritetty **Kuluraportin tarkoitus** -kentän avulla, kun he luovat matkaehdotuksia. |

## <a name="financial"></a>Rahoitustoiminta

| Field                                                                                    | Kuvaus |
|------------------------------------------------------------------------------------------|-------------|
| Kirjanpidon päiväkirjan nimi                                                                | Valitse sen kirjanpidon kirjauskansion nimi, jolle hyväksytyt kuluraportit kirjataan. |
| Ota käyttöön veronpalautus kuluista                                                        | Valitse tämä vaihtoehto, jos haluat ottaa kulujen veronpalautuksen käyttöön niihin oikeuttavissa kuluissa. Tätä vaihtoehtoa ei voi valita, jos Yhdysvaltojen arvonlisävero ja käyttöverosäännöt on otettu käyttöön. |
| Käteisennakko maksujen kirjaaminen heti                                                           | Valitse tämä vaihtoehto, jos haluat kirjata hyväksytyn käteisennakon, kun maksu- ja siirtoprosessi on valmis. Jos tätä vaihtoehtoa ei ole valittu, maksu- ja siirtoprosessi luo kirjaamattoman yleisen kirjauskansion. |
| Korkaa kirjanpitopäivämäärä kirjauksen aikana                                                   | Valitse tämä vaihtoehto, jos haluat päivittää kirjauspäivämäärän kulujen kirjaamisen yhteydessä, jos nykyinen kausi on pidossa tai suljettu. Kirjanpitopäiväksi tulee seuraava avoin kausi. |
| Salli tapahtumien ryhmittely maksutavassa määritetyn vastatilin perusteella       | Valitse tämä vaihtoehto, jos haluat tehdä yhteenvedon kuluraportin kulutapahtumista kulujen maksutavassa määritetyn vastatilin perusteella. |
| Sisällytetty vero                                                                             | Valitse tämä vaihtoehto, jos haluat lisätä arvonlisäveron oletusarvoisesti kulusummaan. |
| Vapauta varaukset matkustusehdotusten sulkemisen yhteydessä                                      | Valitse tämä vaihtoehto, jos haluat vapauttaa varatut varat, kun hyväksytty matkustusehdotus suljetaan. |
| Salli matka ehdotuksen lähettäminen budjetin ylittyessä budjettirekisterissä ja projektibudjetissa | Valitse tämä vaihtoehto, jos haluat, että työntekijät voivat lähettää matkustusehdotuksia hyväksyttäväksi, vaikka ne ylittäisivät joko budjettirekisterissä määritetyn sallitun budjetin tai projektin sallitun budjetin. |
| Salli kuluraportin lähettäminen budjetin ylittyessä budjettirekisterissä ja projektibudjetissa     | Valitse tämä vaihtoehto, jos haluat, että työntekijät voivat lähettää kuluraportteja hyväksyttäväksi, vaikka ne ylittäisivät joko budjettirekisterissä määritetyn sallitun budjetin tai projektin sallitun budjetin. |
| Salli kuluraportin hyväksyminen vain budjetin ylittyessä budjettirekisterissä                 | Valitse tämä vaihtoehto, jos haluat sallia hyväksyjien hyväksyä kuluraportit, jotka ylittävät budjettirekisterissä määritetyn sallitun budjetin. |

## <a name="per-diem"></a>Päiväraha

| Field                                 | Kuvaus |
|---------------------------------------|-------------|
| Päivärahan vähimmäistunnit            | Määritä vähimmäistuntien oletusmäärä, joka työntekijän on työskenneltävä päivässä, jotta hän voi saada matkakulujen päivä rahaa. Tätä arvoa käytetään oletusarvona vain päivärahatasojen **Vähimmäistunnit**-kentässä. |
| Ateriaprosentti                          | Määritä niiden aterioiden korvauksen oletusprosenttiosuus, joita käytetään matkustamiseen liittyvän kulun ensimmäisenä ja viimeisenä päivänä silloin, kun **Laske ateriavähennys** -kentän arvoksi on määritetty joko **Ateriatyyppi päivässä** tai **Aterioiden määrä päivässä**. Ensimmäisen ja viimeisen päivän työpäivä voi olla tavallista arkipäivää lyhyempi. Tämän vuoksi päivärahasummat voivat poiketa vakiosummasta. Jos prosenttiarvoksi on määritetty **0** (nolla), ensimmäisen ja viimeisen päivän vähennykset ovat 0,00. |
| Hotelliprosentti                         | Määritä niiden hotellien oletusprosenttiosuus, joita käytetään matkustamiseen liittyvän kulun ensimmäisinä ja viimeisinä päivinä. Ensimmäisen ja viimeisen päivän työpäivä voi olla tavallista arkipäivää lyhyempi. Tämän vuoksi päivärahasummat voivat poiketa vakiosummasta. Jos prosenttiarvoksi on määritetty **0** (nolla), ensimmäisen ja viimeisen päivän vähennykset ovat 0,00. |
| Muu prosentti                         | Määritä niiden muiden kulujen oletusprosenttiosuus, joita käytetään matkustamiseen liittyvän kulun ensimmäisinä ja viimeisinä päivinä. Ensimmäisen ja viimeisen päivän työpäivä voi olla tavallista arkipäivää lyhyempi. Tämän vuoksi päivärahasummat voivat poiketa vakiosummasta. Jos prosenttiarvoksi on määritetty **0** (nolla), ensimmäisen ja viimeisen päivän vähennykset ovat 0,00. |
| Aamiaisen prosenttiosuuden vähennys | Anna prosentti, jonka verran päivärahaa vähennetään aamiaisen osalta. Jos esimerkiksi työntekijä saa ilmaisen aamiaisen, haluat ehkä vähentää päivärahan määrää 10 prosentilla. |
| Lounaan prosenttiosuuden vähennys     | Anna prosentti, jonka verran päivärahaa vähennetään lounaan osalta. Jos esimerkiksi työntekijä saa ilmaisen lounaan, haluat ehkä vähentää päivärahan määrää 15 prosentilla. |
| Päivällisen prosenttiosuuden vähennys    | Anna prosentti, jonka verran päivärahaa vähennetään päivällisen osalta. Jos esimerkiksi työntekijä saa ilmaisen päivällisen, haluat ehkä vähentää päivärahan määrää 25 prosentilla. |
| Laske ateriavähennys           | Määritä, miten järjestelmä laskee päivärahan ateriavähennyksen, valitsemalla, perustuuko vähennys matka- tai päiväkohtaiseen ateriatyyppiin vai perustuuko se aterioiden määrään, joka on sallittu päivässä. |
| Päivärahan pyöristys                     | Valitse päivärahakulujen pyöristystyyppi. Jos valitset normaalin pyöristyksen, kaikki päivärahakulut, joiden määrä on 0,50 tai yli, pyöristetään ylöspäin lukuun 1,00, ja kaikki päivärahakulut, joiden summa on pienempi kuin 0,50, pyöristetään alaspäin lukuun 0,00. |
| Päivärahalaskelman peruste          | Valitse, perustuvatko päivärahasummat kalenteripäivään vai 24 tunnin jaksoon. |

## <a name="fax-cover-pages"></a>Faksaa kansilehdet

| Field                          | Kuvaus |
|--------------------------------|-------------|
| Ohjeet                   | Kirjoita ohjeet, joita työntekijöiden on noudatettava, kun he luovat kansilehden faksiin, jota käytetään kuluraporttiin liittyvien kuittien lähettämiseen. Jos haluat lisätä kielikohtaisen tekstin, joka näkyy käyttäjän kielen mukaan, valitse **Käännökset**. |
| Käyttäjätunnus (viivakooditiedot) | Valitse tämä vaihtoehto, jos haluat tallentaa työntekijän yksilöivän tunnisteen viivakoodiin, jota käytetään faksin kansilehdellä. |
| Viivakoodi                       | Valitse faksin kansilehdellä käytettävä viivakoodi. Viivakoodeja 39 ja 128 tuetaan kulujen hallinnassa. |

## <a name="anti-corruption"></a>Korruption vastainen

| Field                                 | Kuvaus |
|---------------------------------------|-------------|
| Näytä korruption vastainen todistus   | Valitse tämä vaihtoehto, jos haluat näyttää korruption vastaisen tekstin, kun kuluraportti luodaan. Tällöin voidaan ottaa käyttöön tietyt kululuokat, jotka edellyttävät, että kuluraporttiin valitaan korruption vastainen todistus. Esimerkiksi hallituksen virallisiin kuluihin liittyvä lahjaluokka voi edellyttää, että työntekijä vahvistaa, että kulu vastaa hallituksen virkamiehiin liittyvää käytäntöä. |
| Korruption vastainen sanoma lähettäjälle | Kirjoita teksti, joka näytetään kuluraporttia luovalle työntekijälle. Jos haluat lisätä kielikohtaisen tekstin, joka näkyy käyttäjän kielen mukaan, valitse **Käännökset**. |
| Korruption vastainen sanoma hyväksyjälle  | Kirjoita teksti, joka näytetään hyväksyjälle, kun kuluraportti luodaan. Jos haluat lisätä kielikohtaisen tekstin, joka näkyy käyttäjän kielen mukaan, valitse **Käännökset**. |


[!INCLUDE[footer-include](../includes/footer-banner.md)]