---
title: Tarjoukset - keskeiset käsitteet
description: Tässä aiheessa on tietoja Project Operations -sovelluksen projekti- ja myyntitarjouksista.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: rumant
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 488c57527e6cc153093014438453001170f311dc
ms.sourcegitcommit: df30839484ef278675c5c712af0f7ba66ed9cdd3
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/17/2021
ms.locfileid: "5663681"
---
# <a name="concepts-unique-to-project-based-quotes"></a>Projektipohjaisten tarjousten yksilölliset käsitteet

_**Koskee:** Project Operationsin resurssiin / muuhun kuin resurssiin perustuvia skenaarioita, Lite-käyttöönotto-kaupasta proformalaskutukseen_

Dynamics 365 Project Operationsissa on kahdenlaisia tarjouksia: projekti- ja myyntitarjouksia. Nämä kaksi tarjoustyyppiä eroavat toisistaan seuraavasti:

- **Rivinimikkeiden ruudukot**: Myyntitarjouksessa rivinimikkeille on vain yksi ruudukko. Projektitarjouksessa rivinimikkeille on kaksi ruudukkoa. Yksi ruudukko on projektiriveille ja toinen tuoteriveille.
- **Aktivointi ja muokkaukset**: Myyntitarjoukset tukevat aktivointia ja muokkauksia. Projektitarjous ei tue näitä prosesseja.
- **Liitetyt tarjoukset**: Myyntitarjoukseen voi liittää useita tilauksia. Projektitarjoukseen voi liittää vain yhden projektisopimuksen.
- **Tarjouksen voittaminen**: Kun voitat myyntitarjouksen, siihen liittyvä mahdollisuus voi säilyä avoimena. Kun projektitarjous on voitettu, siihen liittyvä mahdollisuus suljetaan.
- **Kentät ja käsitteet**: Myyntitarjous ei sisällä kaikkia projektitarjouksen kenttiä ja käsitteitä. Kenttiä ovat esimerkiksi **Sopimusyksikkö**, **Asiakaspäällikkö** ja **Laskutusyhteyshenkilön nimi**.  
- **Tyyppi**: Myynti- ja projektitarjouksille määritetään myös asetusjoukkoperusteinen kenttä, jonka nimi on **Tyyppi**. Myyntitarjouksessa tällä kentällä on arvo **Nimikepohjainen**. Projektitarjouksessa sen arvo on **Työpohjainen**.

Tässä aiheessa keskitytään projektitarjousten tietoihin.

Project Operations -sovelluksessa projektitarjouksella voi olla useita rivinimikkeitä tai tarjousrivejä. Itse asiassa projektitarjouksella on kaksi ruudukkoa. Yksi ruudukko on yksityiskohtaiset arviot mahdollistavia projektiperusteisia kenttiä varten. Toinen ruudukko on sellaisia tuoteperusteisia rivejä varten, jossa käytetään yksinkertaista yksikköhintaa ja määräperusteista lähestymistapaa.

- **Projektipohjainen**: Summa-arvo määritetään, kun olet arvioinut vaadittavan työmäärän. Voit arvioida työn korkealla tasolla, suoraan kunkin tarjousrivin alapuolella, tai käyttämällä projektia ja projektisuunnitelmaa alhaalta ylöspäin. Projektipohjaisia tarjousrivejä esiintyy vain projektipohjaisissa tarjouksissa, jotka luodaan Project Operations -sovelluksen avulla. Tällainen tarjousrivi on muokattu Microsoft Dynamics 365:n myynneissä käytettävissä olevien käsin lisättävien tarjousrivien muoto.

- **Tuotepohjainen**: Summa-arvo määritetään myytyjen yksiköiden määrän ja tuotteen yksikkömyyntihinnan perusteella. Tuotepohjaisen rivin tuote voi olla peräisin myynnin tuoteluettelosta tai voit määrittää tuotteen itse. Tällainen tarjousrivi on käytettävissä myös Project Operations -sovelluksella luotavissa projektipohjaisissa tarjouksissa.

Tarjouksen summa lasketaan kaikista tuotepohjaisista ja projektipohjaisista riveistä.

> [!NOTE]
> Project Operations -sovelluksessa ei tarvita tarjouksia ja tarjousrivejä. Voit aloittaa projektiprosessin projektisopimuksella (myyty projekti). Mahdollisuus on kuitenkin aina pakollinen riippumatta siitä, aloitetaanko tarjouksella vai projektisopimuksella.

## <a name="project-based-quote-lines"></a>Projektipohjaiset tarjousrivit

Project Operations -sovelluksen projektipohjaisella tarjousrivillä on seuraavat laskutusmenetelmät:

- Aika ja materiaalit
- Kiinteähintainen

### <a name="time-and-material"></a>Aika ja materiaalit

Aika ja materiaalit -laskutusmenetelmä perustuu käyttöön. Kun valitset tämän laskutusmenetelmän, asiakasta laskutetaan, kun projektista aiheutuu kustannuksia. Laskuja luodaan päivämääräperusteisin väliajoin. Myyntiprosessin aikana aika ja materiaalit -komponentin tarjoushinta on vain arvio lopullisista kustannuksista asiakkaalle. Toimittaja ei sitoudu suorittamaan projektia loppuun tarkalla tarjoushinnalla. Aika ja materiaalit -komponentit lisäävät asiakkaan riskiä. Asiakkaat voivat haluta neuvotella ylimääräisistä ylärajalausekkeista minimoidakseen riskinsä. Project Operations ei tue ylärajalausekkeiden asettamista.

### <a name="fixed-price"></a>Kiinteähintainen

Kiinteähintaisessa laskutusmenetelmässä toimittaja sitoutuu toimittamaan projektin asiakkaalle kiinteillä kustannuksilla. Asiakkaalta laskutetaan kiinteähintaisen tuoterivin tarjoushinta riippumatta kustannuksista, jotka toimittajalle aiheutuvat kyseisen tarjousrivin toimittamisesta. Kiinteähintaisen tarjousrivin arvo laskutetaan jollakin seuraavista tavoista: 

- Kertasummana projektin alussa tai lopussa tai kun projektin välitavoite on saavutettu. 
- Päivämääräperusteisin väliajoin maksettavina tasasuurina tarjousrivin kiinteää arvoa vastaavina erinä. Näitä maksueriä kutsutaan jaksoittaisiksi välitavoitteiksi.
- Maksuerinä, joiden rahallinen arvo vastaa työn edistymistä tai tiettyjä projektissa saavutettavia välitavoitteita. Tässä tapauksessa maksuerien suuruudet voivat vaihdella, mutta niiden on yhdessä vastattava tarjousrivin kiinteää arvoa.

Project Operations tukee kaikkia kolmea laskutussuunnitelmatyyppiä kiinteähintaisissa tarjousriveissä.

## <a name="transaction-classification"></a>Tapahtuman luokittelu

Asiantuntijapalveluja myyvät organisaatiot tekevät asiakkailleen tarjouksia ja laskuttavat niitä yleensä tapahtuman luokittelun perusteella. Kustannuksia edustavat seuraavat tapahtumaluokat:

- **Aika**: Tämä luokka edustaa työn tai henkilöresurssien ajan kustannuksia projektissa.
- **Kulu**: Tämä luokka edustaa kaikkia muita projektin kuluja. Koska kuluja voidaan luokitella laajasti, useimmat organisaatiot luovat alaluokkia, kuten matka-, autonvuokraus-, hotelli- tai toimistotarvikekulut.
- **Maksu**: Tämä luokka edustaa erilaisia yleiskuluja, sakkoja ja muita asioita, jotka veloitetaan asiakkaalta. 
- **Vero**: Tämä luokka edustaa veromääriä, jotka käyttäjät lisäävät syöttäessään kuluja.
- **Materiaalitapahtuma**: Tämä luokka edustaa vahvistetun projektilaskun tuoterivien todellisia arvoja.
- **Välitavoite**: Tätä luokkaa käytetään kiinteähintaisessa laskutuslogiikassa.

Kullekin tarjousriville voidaan kohdentaa yksi tai useampi tällainen tapahtumaluokka. Kun tarjous on voitettu, tapahtumaluokan ja tarjousrivin välinen yhdistämismääritys siirretään sopimusriville.
  
Tarjous voi sisältää esimerkiksi seuraavat kaksi tarjousriviä: 

- Konsultointityö, jossa käytetään aika ja materiaalit -laskutusmenetelmää, jossa voidaan soveltaa tapahtumaluokkia Aika ja Maksu. Esimerkiksi kaikki esimerkkiprojektin **Dynamics AX:n käyttöönotto** aika- ja maksutapahtumat laskutetaan asiakkaalta käytetyn ajan ja käytettyjen materiaalien perusteella. 
- Tähän liittyvät matkakulut, joissa käytetään kiinteähintaisen laskutuksen menetelmää. Esimerkiksi kaikki esimerkkiprojektin **Dynamics AX:n käyttöönotto** matkakulut laskutetaan kiinteänä rahasummana.

> [!NOTE]
> Tarjous- tai sopimusriviin kohdennetun projektin ja tapahtumaluokkien **Aika**, **Kulu** ja **Maksu** yhdistelmän on oltava yksilöllinen. Jos sama projektin ja tapahtumaluokkien yhdistelmä kohdennetaan useammalle sopimus- tai tarjousriville, Project Operations ei toimi oikein.

## <a name="billing-types"></a>Laskutustyypit

**Laskutustyyppi**-kenttä määrittää veloitettavuuskonseptin. Se on asetusjoukko, jolla on seuraavat mahdolliset arvot:

- **Veloitettava**: Tämän roolin/luokan kulut ovat suoria kuluja, jotka edistävät projektin toteutusta, ja asiakas maksaa kyseisestä työstä. Maksu voi olla aika- ja materiaaliperusteinen tai kiinteähintainen. Kyseisen ajan käyttävä työntekijä saa kuitenkin vastaavan saldon laskutettavaan käytettyyn aikaansa.
- **Ei-veloitettava**: Tämän roolin/luokan kulut katsotaan suoriksi kuluiksi, jotka edistävät projektin toteutusta, vaikka asiakas ei tätä tunnusta eikä maksa kyseisestä työstä. Kyseisen ajan käyttävä työntekijä ei saa laskutettavaa käytettyä aikaa.
- **Ilmainen**: Tämän roolin/luokan kulut katsotaan suoriksi kuluiksi, jotka edistävät projektin toteutusta, ja asiakas tunnustaa tämän. Kyseisen ajan käyttävä työntekijä saa laskutettavaa käytettyä aikaa. Näitä kuluja ei kuitenkaan veloiteta asiakkaalta.
- **Ei käytettävissä**: Tällä vaihtoehdolla seurataan sellaisista sisäisistä projekteista aiheutuvia kuluja, jotka eivät edellytä tuottojen seurantaa.

## <a name="invoice-schedule"></a>Laskutusaikataulu

Laskutusaikataulu on sarja projektin laskutuksen päivämääriä. Voit luoda laskutusaikataulun tarjousriville. Kullakin tarjousrivillä voi olla oma laskutusaikataulunsa. Laskutusaikataulun luonnissa on annettava seuraavat määritearvot:

- Laskutuksen aloituspäivä 
- Toimituspäivä, joka edustaa projektin laskutuksen päättymispäivää
- Laskutustiheys

Näitä kolmea määritearvoa käytetään luotaessa alustava päivämääräjoukko laskutuksen muodostamista varten.

## <a name="invoice-frequency"></a>Laskutustiheys

Laskutustiheys on entiteetti, joka tallentaa laskujen luonnin tiheyden ilmaisemisessa auttavia määritearvoja. Seuraavat määritteet ilmaisevat tai määrittävät laskutustiheyden entiteettiä:

- **Jakso**: Kahden viikon ja viikon jaksoja tuetaan. 
- **Suorituksia jaksossa**: Viikon ja kahden viikon jaksoille voi määrittää vain yhden suorituksen jaksoa kohden. Kuukauden jaksoille voidaan määrittää 1–4 suoritusta jaksossa. 
- **Suorituspäivät**: Päivät, joina laskutus suoritetaan. Tämä määrite voidaan määrittää kahdella tavalla:
  - **Arkipäivät**: Voit esimerkiksi määrittää, että laskutus suoritetaan joka maanantai tai joka toinen maanantai. Asiakkaat, joiden on määritettävä laskutus suoritettavaksi arkipäivänä, saattavat suosia tällaista määritystä. 
  - **Kalenteripäivät**: Voit esimerkiksi määrittää, että laskutus suoritetaan jokaisen kuukauden 7. ja 21. päivänä. Jotkut organisaatiot saattavat suosia tällaista määritystä, koska se auttaa takaamaan, että laskutus suoritetaan kiinteällä aikataululla jokaisena kuukautena.
  
### <a name="invoice-schedule-for-a-fixed-price-quote-line"></a>Kiinteähintaisen tarjousrivin laskutusaikataulu

Kiinteähintaisessa tarjousrivissä voit käyttää **Laskutusaikataulu**-ruudukkoa luodaksesi laskutuksen välitavoitteita, jotka vastaavat tarjousrivin arvoa.

- Voit luoda tasan jaettuja laskutuksen välitavoitteita valitsemalla laskutusvälin, antamalla laskutuksen aloituspäivän tarjousrivissä ja valitsemalla tarjoukselle arvon **Pyydetty suorituspäivä** tarjousotsikon **Yhteenveto**-osassa. Valitse sitten **Luo jaksoittaiset välitavoitteet** luodaksesi tasaisesti jaettuja välitavoitteita valitun laskutusvälin perusteella. 
- Voit luoda kertasummaisen laskutuksen välitavoitteen luomalla välitavoitteen ja määrittämällä tarjousrivin aroksi välitavoitteen summan.
- Voit luoda tiettyihin projektisuunnitelman tehtäviin perustuvia laskutuksen välitavoitteita luomalla välitavoitteen ja yhdistämällä sen projektiaikataulun elementtiin laskutuksen välitavoitteen käyttöliittymässä.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
