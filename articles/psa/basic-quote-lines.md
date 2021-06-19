---
title: Tarjoukset ja tarjousrivit
description: Tässä aiheessa on tietoja tarjouksista ja tarjousriveistä.
author: rumant
ms.custom:
- dyn365-projectservice
ms.date: 3/01/2019
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
ms.openlocfilehash: a46ec93744067205e1aa8c99dba52967a1780957
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/10/2021
ms.locfileid: "6014914"
---
# <a name="quotes-and-quote-lines"></a>Tarjoukset ja tarjousrivit

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Dynamics 365 Project Service Automationissa on kahdenlaisia tarjouksia: projektitarjouksia ja myyntitarjouksia. Nämä tarjoukset eroavat toisistaan seuraavasti:

- Myyntitarjouksessa rivinimikkeille on vain yksi ruudukko. Projektitarjouksessa rivinimikkeille on kaksi ruudukkoa: yksi projektiriveille ja yksi tuoteriveille.
- Myyntitarjous tukee aktivointeja ja muutoksia. Projektitarjous ei tue näitä prosesseja.
- Myyntitarjoukseen voi liittää useita tilauksia. Projektitarjoukseen voi liittää vain yhden projektisopimuksen.
- Voit voittaa myyntitarjouksen ja pitää siihen liittyvän mahdollisuuden avoimena. Kun projektitarjous on voitettu, siihen liittyvä mahdollisuus suljetaan.
- Myyntitarjous ei sisällä kaikkia projektitarjouksessa olevia kenttiä ja konsepteja. Kenttiä ovat esimerkiksi **Sopimusyksikkö**, **Asiakaspäällikkö** ja **Laskutusyhteyshenkilön nimi**.  
- Myyntitarjouksille ja projektitarjouksille määritetään myös asetusjoukkoperusteinen kenttä nimeltään **Tyyppi**. Myyntitarjouksessa tällä kentällä on arvo **Nimikepohjainen**. Projektitarjouksessa sen arvo on **Työpohjainen**.

Tässä aiheessa keskitytään projektitarjousten tietoihin.

PSA:ssa projektitarjouksella voi olla useita rivinimikkeitä tai tarjousrivejä. Itse asiassa projektitarjouksella on kaksi ruudukkoa. Yksi ruudukko on yksityiskohtaiset arviot mahdollistavia projektiperusteisia kenttiä varten. Toinen ruudukko on sellaisia tuoteperusteisia rivejä varten, jossa käytetään yksinkertaista yksikköhintaa ja määräperusteista lähestymistapaa.

- **Projektipohjainen** – Summa (tarjouksen arvo) määritetään, kun olet arvioinut vaadittavan työmäärän. Voit arvioida työtä korkealla tasolla tai voit arvioida sen suoraan rivitietoina kunkin tarjousrivin alla. Lopuksi voit arvioida työn alhaalta-ylöspäin-arviointien perusteella käyttämällä projektia ja projektisuunnitelmaa. Projektipohjaisia tarjousrivejä esiintyy vain projektipohjaisissa tarjouksissa, jotka luodaan Project Service Automationilla. Tällainen tarjousrivi on muokattu Microsoft Dynamics 365:n myynneissä käytettävissä olevien käsin lisättävien tarjousrivien muoto.
- **Tuotepohjainen** – Summa (tarjouksen arvo) määritetään myytävien yksiköiden määrän ja tuotteen yksikkömyyntihinnan perusteella. Tuotepohjaisen rivin tuote voi olla peräisin myynnin tuoteluettelosta tai voit määrittää tuotteen itse. Tällainen tarjousrivi on käytettävissä myös PSA:lla luotavissa projektipohjaisissa tarjouksissa.

Tarjouksen summa lasketaan kaikista tuotepohjaisista ja projektipohjaisista riveistä.

> [!NOTE]
> PSA:ssa ei tarvita tarjouksia ja tarjousrivejä. Voit aloittaa projektiprosessin projektisopimuksella (myyty projekti). Mahdollisuus on kuitenkin aina pakollinen riippumatta siitä, aloitetaanko tarjouksella vai projektisopimuksella.

## <a name="project-based-quote-lines"></a>Projektipohjaiset tarjousrivit

PSA:ssa projektipohjaisella tarjousrivillä on seuraavat laskutusmenetelmät:

- Aika ja materiaalit
- Kiinteähintainen

### <a name="time-and-material"></a>Aika ja materiaalit

Aika ja materiaalit -laskutusmenetelmä perustuu käyttöön. Kun valitset tämän laskutusmenetelmän, asiakasta laskutetaan, kun projektista aiheutuu kustannuksia. Laskuja luodaan päivämääräperusteisin väliajoin. Myyntiprosessin aikana aika ja materiaalit -komponentin tarjoushinta on vain arvio lopullisista kustannuksista asiakkaalle. Toimittaja ei sitoudu suorittamaan projektia loppuun tarkalla tarjoushinnalla. Aika ja materiaalit -komponentit lisäävät asiakkaan riskiä. Asiakkaat voivat haluta neuvotella ylimääräisistä ylärajalausekkeista minimoidakseen riskinsä. PSA ei tue ylärajalausekkeiden asettamista.

### <a name="fixed-price"></a>Kiinteähintainen

Kiinteähintaisessa laskutusmenetelmässä toimittaja sitoutuu toimittamaan projektin asiakkaalle kiinteillä kustannuksilla. Asiakkaalta laskutetaan kiinteähintaisen tuoterivin tarjoushinta riippumatta kustannuksista, jotka toimittajalle aiheutuvat kyseisen tarjousrivin toimittamisesta. Kiinteähintaisen tarjousrivin arvo laskutetaan jollakin seuraavista tavoista: 

- Kertasummana projektin alussa tai lopussa tai kun projektin välitavoite on saavutettu. 
- Päivämääräperusteisin väliajoin maksettavina tasasuurina tarjousrivin kiinteää arvoa vastaavina erinä. Näitä maksueriä kutsutaan jaksoittaisiksi välitavoitteiksi.
- Maksuerinä, joiden rahallinen arvo vastaa työn edistymistä tai tiettyjä projektissa saavutettavia välitavoitteita. Tässä tapauksessa maksuerien suuruudet voivat vaihdella, mutta niiden on yhdessä vastattava tarjousrivin kiinteää arvoa.

PSA tukee kaikkia kolmea laskutussuunnitelmatyyppiä kiinteähintaisissa tarjousriveissä.

## <a name="transaction-classification"></a>Tapahtuman luokittelu

Asiantuntijapalveluja myyvät organisaatiot tekevät asiakkailleen tarjouksia ja laskuttavat niitä yleensä tapahtuman luokittelun perusteella. PSA:ssa kustannuksia edustavat seuraavat tapahtumaluokat:

- **Aika** – Tämä luokka edustaa työn tai henkilöresurssien ajan kustannuksia projektissa.
- **Kulu**: – Tämä luokka edustaa kaikkia muita projektin kuluja. Koska kuluja voidaan luokitella laajasti, useimmat organisaatiot luovat alaluokkia, kuten matka-, autonvuokraus-, hotelli- tai toimistotarvikekulut.
- **Maksu** – Tämä luokka edustaa erilaisia yleiskuluja, sakkoja ja muita asioita, jotka veloitetaan asiakkaalta. 
- **Vero** – Tämä luokka edustaa veromääriä, jotka käyttäjät lisäävät syöttäessään kuluja.
- **Materiaalitapahtuma** – Tämä luokka edustaa vahvistetun projektilaskun tuoterivien todellisia arvoja.
- **Välitavoite** – Tätä luokkaa käytetään PSA:n kiinteähintaisessa laskutuslogiikassa.

Kullekin tarjousriville voidaan kohdentaa yksi tai useampi tällainen tapahtumaluokka. Kun tarjous on voitettu, tapahtumaluokan ja tarjousrivin välinen yhdistämismääritys siirretään sopimusriville.
 
> ![Näyttökuva tapahtumatyyppien yhdistämismäärityksestä tarjous- ja sopimusriveihin](media/basic-guide-5.png)
  
Tarjous voi sisältää esimerkiksi seuraavat kaksi tarjousriviä: 
- Konsultointityö, jossa käytetään aika ja materiaalit -laskutusmenetelmää, jossa voidaan soveltaa tapahtumaluokkia Aika ja Maksu. Esimerkiksi kaikki esimerkkiprojektin **Dynamics AX:n käyttöönotto** aika- ja maksutapahtumat laskutetaan asiakkaalta käytetyn ajan ja käytettyjen materiaalien perusteella. 
- Tähän liittyvät matkakulut, joissa käytetään kiinteähintaisen laskutuksen menetelmää. Esimerkiksi kaikki esimerkkiprojektin **Dynamics AX:n käyttöönotto** matkakulut laskutetaan kiinteänä rahasummana.

> [!NOTE]
> Tarjous- tai sopimusriviin kohdennetun projektin ja tapahtumaluokkien **Aika**, **Kulu** ja **Maksu** yhdistelmän on oltava yksilöllinen. Jos sama projektin ja tapahtumaluokkien yhdistelmä kohdennetaan useammalle sopimus- tai tarjousriville, PSA ei toimi oikein.

## <a name="billing-types"></a>Laskutustyypit

**Laskutustyyppi** -kenttä määrittää PSA:n veloitettavuuskonseptin. Se on asetusjoukko, jolla on seuraavat mahdolliset arvot:

- **Veloitettava** – Tämän roolin/luokan kulut ovat suoria kuluja, jotka edistävät projektin toteutusta, ja asiakas maksaa kyseisestä työstä. Maksu voi olla aika- ja materiaaliperusteinen tai kiinteähintainen. Kyseisen ajan käyttävä työntekijä saa kuitenkin vastaavan saldon laskutettavaan käytettyyn aikaansa.
- **Ei-veloitettava** – Tämän roolin/luokan kulut katsotaan suoriksi kuluiksi, jotka edistävät projektin toteutusta, vaikka asiakas ei tätä tunnusta eikä maksa kyseisestä työstä. Kyseisen ajan käyttävä työntekijä ei saa laskutettavaa käytettyä aikaa.
- **Ilmainen** – Tämän roolin/luokan kulut katsotaan suoriksi kuluiksi, jotka edistävät projektin toteutusta, ja asiakas tunnustaa tämän. Kyseisen ajan käyttävä työntekijä saa laskutettavaa käytettyä aikaa. Näitä kuluja ei kuitenkaan veloiteta asiakkaalta.
- **Ei käytettävissä** – Tällä vaihtoehdolla seurataan sellaisista sisäisistä projekteista aiheutuvia kuluja, jotka eivät edellytä tuottojen seurantaa.

## <a name="invoice-schedule"></a>Laskutusaikataulu

Laskutusaikataulu on sarja projektin laskutuksen päivämääriä. Voit luoda laskutusaikataulun PSA:n tarjousriville. Kullakin tarjousrivillä voi olla oma laskutusaikataulunsa. Laskutusaikataulun luonnissa on annettava seuraavat määritearvot:

- Laskutuksen aloituspäivä 
- Toimituspäivä, joka edustaa projektin laskutuksen päättymispäivää
- Laskutustiheys

PSA käyttää näitä kolmea määritearvoa luodakseen alustavan päivämääräjoukon laskutuksen luomiselle.

## <a name="invoice-frequency"></a>Laskutustiheys

Laskutustiheys on entiteetti, joka tallentaa laskujen luonnin tiheyden ilmaisemisessa auttavia määritearvoja. Seuraavat määritteet ilmaisevat tai määrittävät laskutustiheyden entiteettiä:

- **Jakso** – Kahden viikon ja viikon jaksoja tuetaan. 
- **Suorituksia jaksossa** – Viikon ja kahden viikon jaksoille voi määrittää vain yhden suorituksen jaksoa kohden. Kuukauden jaksoille voidaan määrittää 1–4 suoritusta jaksossa. 
- **Suorituspäivät** – Päivät, joina laskutus suoritetaan. Tämä määrite voidaan määrittää kahdella tavalla:
  - **Arkipäivät** – Voit esimerkiksi määrittää, että laskutus suoritetaan joka maanantai tai joka toinen maanantai. Asiakkaat, joiden on määritettävä laskutus suoritettavaksi arkipäivänä, saattavat suosia tällaista määritystä. 
  - **Kalenteripäivät** – Voit esimerkiksi määrittää, että laskutus suoritetaan jokaisen kuukauden 7. ja 21. päivänä. Jotkut organisaatiot saattavat suosia tällaista määritystä, koska se auttaa takaamaan, että laskutus suoritetaan kiinteällä aikataululla jokaisena kuukautena.
  
### <a name="invoice-schedule-for-a-fixed-price-quote-line"></a>Kiinteähintaisen tarjousrivin laskutusaikataulu

Kiinteähintaisessa tarjousrivissä voit käyttää **Laskutusaikataulu**-ruudukkoa luodaksesi laskutuksen välitavoitteita, jotka vastaavat tarjousrivin arvoa.

- Voit luoda tasan jaettuja laskutuksen välitavoitteita valitsemalla laskutusvälin, antamalla laskutuksen aloituspäivän tarjousrivissä ja valitsemalla tarjoukselle arvon **Pyydetty suorituspäivä** tarjousotsikon **Yhteenveto**-osassa. Valitse sitten **Luo jaksoittaiset välitavoitteet** luodaksesi tasaisesti jaettuja välitavoitteita valitun laskutusvälin perusteella. 
- Voit luoda kertasummaisen laskutuksen välitavoitteen luomalla välitavoitteen ja määrittämällä tarjousrivin aroksi välitavoitteen summan.
- Voit luoda tiettyihin projektisuunnitelman tehtäviin perustuvia laskutuksen välitavoitteita luomalla välitavoitteen ja yhdistämällä sen projektiaikataulun elementtiin laskutuksen välitavoitteen käyttöliittymässä.


[!INCLUDE[footer-include](../includes/footer-banner.md)]