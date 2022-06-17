---
title: Päivärahakulut
description: Tässä artikkelissa on tietoja päivärahakulujen käsittelystä.
author: suvaidya
ms.date: 03/18/2022
ms.topic: article
ms.prod: ''
ms.search.form: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.search.region: ''
ms.author: suvaidya
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 0d2f95b677720726049d7d010e9738ad8c513802
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8923184"
---
# <a name="per-diem-expenses"></a>Päivärahakulut

> [!IMPORTANT] 
> Tässä artikkelissa käsitellyt toiminnot ovat kohdennettujen käyttäjien käytettävissä ennakkoversion osana.

Päivärahamaksu on kiinteä, ennalta määritetty päivämaksu, jonka yritys maksaa työntekijöilleen työmatkojen aikana majoitus-, ateria- ja satunnaiskuluista. Yritys maksaa tämän korvauksen työntekijöille sen sijaan, että maksaisi todelliset matkakulut. Työntekijät voivat käyttää **Satunnaiset/muut**-päivärahaa tärkeissä tapaamisissa tippien, huonepalvelun, pesulan tai siivouspalveluiden korvaukseen. Päivärahan suuruus voi vaihdella sen mukaan, ottaako työntekijä yhdistetyn majoitus- ja ateriakustannuksen vai vain ateria- ja satunnaiskustannukset.

Päivärahahinnat voivat perustua vuodenaikaan, matkustuspaikkaan tai molempiin. Kun luot päivärahasäännön, voit määrittää, mikä prosenttiosuus päivärahasta pidätetään, jos työntekijällä on käytettävissään ilmaisia aterioita tai palveluita. Voit myös määrittää työtuntien vähimmäismäärän ja enimmäismäärän, jonka perusteella päivärahaa voi käyttää työntekijän matkoilla.

Päiväraha lasketaan päiväkohtaisena kokonaiskorvauksena miinus työntekijälle ateria-alennus (ilmaisien aterioiden hinta).

## <a name="configure-per-diems"></a>Päivärahojen määrittäminen

Voit määrittää päivärahakulut seuraavasti.

1. Siirry kohteeseen **Kulujen hallinta** \> **Määritys** \> **Yleiset** \> **Kulujen hallintaparametrit**.
2. Valitse **Päiväraha**-välilehden **Laske ateriavähennys käyttäen:** -kentässä, kuinka päivärahat lasketaan:

    - **Matkakohtainen ateriatyyppi** – Laske päiväraha kirjatun ateriatyypin (aamiainen, lounas tai päivällinen) mukaan ja ateria-alennuksen mukaan, joka määritetään kullekin ateriatyypille päivärahalle matkan keston ajalle.
    - **Päiväkohtainen ateriatyyppi** – Laske päiväraha kirjatun ateriatyypin mukaan ja ateria-alennuksen mukaan, joka määritetään kullekin ateriatyypille päivärahalle päivää kohti.
    - **Aterioiden määrä päivässä** – Laske päiväraha päivittäin syötettyjen aterioiden määrän ja päivittäin tarjottujen aterioiden määrän ateria-alennuksen perusteella.

3. Siirry kohteeseen **Kulujen hallinta** \> **Määritys** \> **Laskelmat ja koodit** \> **Päiväraha – sijainnit**.
4. Lisää sijainteja, joissa voi käyttää päivärahoja.
5. Valitse kullekin lisättävälle sijainnille **Päivärahat**-välilehdessä päivärahan suuruus ja valuutta, jotka ovat kelvollisia majoitus-, ateria- ja muihin kuluihin alkamis- ja päättymispäivän välillä. Jos haluat määrittää päivärahan suuruudet ja valuutat siirry kohtaan **Kulujen hallinta** \> **Määritys** \> **Laskelmat ja koodit** \> **Päivärahat**.

## <a name="per-diems-in-the-reimagined-expense-interface"></a>Päivärahat uudistetussa kulujen käyttöliittymässä

Uudistettu **Kulujen hallinta** -työtila tukee päivärahaominaisuutta Microsoft Dynamics 365 Finance -versiossa 10.0.25 ja myöhemmissä versioissa.

Ota päivärahat käyttöön seuraavasti.

1. Etsi ja valitse **Ominaisuuksien hallinta** -työtilan luettelosta **Uudistetut kuluraportit** -ominaisuus ja valitse sitten **Ota käyttöön nyt**.
2. Etsi ja valitse luettelosta **Päiväraha uudistetut kuluraporttien käyttöliittymässä** -ominaisuus ja valitse sitten **Ota käyttöön nyt**.

## <a name="how-the-feature-works"></a>Miten ominaisuus toimii

Tässä osassa on esimerkkejä kolmesta määritysskenaariosta. Esimerkiksi **Laske ateriavähennys käyttäen:** -kentän arvoksi määritetään eri arvo. Kaikissa kolmessa esimerkissä maksettava kokonaissumma on sama, kunnes ateria-alennus otetaan käyttöön. Tämän jälkeen maksettava kokonaissumma on erilainen kussakin esimerkissä.

Jos haluat luoda päivärahakulun, jota käytetään kaikissa kolmessa esimerkissä, toimi seuraavasti.

1. Valitse **Työtilat** \> **Kulujen hallinta**.
2. Valitse joko **Uusi kuluraportti** tai valitse aikaisemmin luotu kuluraportti.
3. Lisää uusi kulu. Valitse **Luokka**-kentässä **Päiväraha**. Valitse matkasi sijainti sekä sen alkamis- ja päättymispäivät. Majoitus-, ateria- ja satunnaiskulujen (muut kulut) päiväraha lasketaan valitulle sijainnille määritetyn päivärahan perusteella.

    Voit esimerkiksi valita sijainniksi **Redmond (USA)**. Tämän sijainnin päivämaksu on 150 dollaria (150 USD) majoitukseen, ateriaan USD 75 ja USD 5 satunnaisiin kuluihin. Alkamispäivä on 10.1. ja päättymispäivä on 14.1. Siksi valittu kesto on viisi päivää, kun valittu määritys on kalenteripäivät ajan kanssa, ja valittu aika alkaa ja päättyy klo 00:00 alkamis- ja päättymispäivänä. Tässä ovat laskelmat:

    - Maksettavaa yhteensä = 5 × (150 + 75 + 5) = 5 × 230 = 1 150 USD
    - Aterioiden ja satunnaisten osuus kokonaissummasta = 5 × (75 + 5) = 400 USD

Jos matkan aikana tarjottiin aamiainen, lounas ja ruoka, ateriat on vähennettävä ateria-alennuksena.

### <a name="example-1-per-diem-where-meal-reductions-are-based-on-meal-type-per-trip"></a>Esimerkki 1: Päiväraha, jossa ateriavähennykset perustuvat matkakohtaiseen ateriatyyppiin

Tässä esimerkissä ateriavähennys on 30 prosenttia aamupalalle, lounaalle 30 prosenttia ja päivälliselle 40 prosenttia. **Kulujen hallinnan parametrit** -sivun **Laske ateriavähennys käyttäen:** -kentän arvoksi määritetään **Matkakohtainen ateriatyyppi**. Tässä ovat laskelmat, jos työntekijälle on tarjottu kolme aamupalaa, kaksi lounasta ja nolla päivällistä:

- Ateriavähennys = (3 × \[75 × 30 %\]) + (2 × \[75 × 30 %\]) + 0 = (3 × 22,50) + (2 × 22,50) + 0 = 67,50 + 45 + 0 = 112,50 USD
- Ateriat ja satunnaiset kulut = 400 - 112,50 = 287,50 USD
- Maksettava kokonaissumma = kokonaiskorvaus – ateriavähennys 1 150 - 112,50 = 1 037,50 USD

![Päivärahakulu, jossa ateriavähennys perustuu matkakohtaiseen ateriatyyppiin.](media/1-meal-type-per-trip.png)

### <a name="example-2-per-diem-where-meal-reductions-are-based-on-meal-type-per-day"></a>Esimerkki 2: Päiväraha, jossa ateriavähennykset perustuvat päiväkohtaiseen ateriatyyppiin

Tässä esimerkissä ateriavähennys on 30 prosenttia aamupalalle, lounaalle 30 prosenttia ja päivälliselle 40 prosenttia. **Kulujen hallinnan parametrit** -sivun **Laske ateriavähennys käyttäen:** -kentän arvoksi määritetään **Päiväkohtainen ateriatyyppi**. Tyhjennä tällöin **Kulun muokkaaminen** -valintaikkunan **Ateria**-ruudukosta valintaruudut, jotka ilmaisevat, mitkä ateriat on tarjottu matkasi aikana.

Tässä ovat esimerkiksi laskelmat, jos aamiainen on tarjottu matkan kolmen ensimmäisen päivän ajan:

- Päivittäinen ateriavähennys kolmen ensimmäisen päivän aikana = 75 × 30 % = 22,50 USD
- Alennus yhteensä = 3 × 22,50 = 67,50 USD
- Ateriat ja satunnaiset kulut päiville 1–3 = 75–22,50 = 57,50 USD
- Ateriat ja satunnaiset yhteensä = viiden päivän ateria- ja satunnaiskulujen summa = 400 - 67,50 = 332,50 USD
- Maksettava kokonaissumma = kokonaissumma – ateriavähennys 1 150 - 67,50 = 1 082,50 USD

![Päivärahakulu, jossa ateriavähennys perustuu päiväkohtaiseen ateriatyyppiin.](media/2-meal-type-per-day.png)

### <a name="example-3-per-diem-where-meal-reductions-are-based-on-number-of-meals-per-day"></a>Esimerkki 3: Päiväraha, jossa ateriavähennykset perustuvat päiväkohtaiseen aterioiden määrään

Tässä esimerkissä ateria-alennus lasketaan päivittäin tarjottujen aterioiden määrän perusteella (eli kun **Laske ateriavähennys käyttäen:** -kentän arvoksi **Kulujen hallintaparametrit** -sivulla on määritetty **Aterioiden määrä päivässä**). Tyhjennä **Kulun muokkaaminen** -valintaikkunan **Ateria**-ruudukosta valintaruudut, jotka ilmaisevat, mitkä ateriat on tarjottu.
Tässä tapauksessa ateriavähennys perustuu vain tarjottujen aterioiden määrään, ei ateriatyypin (aamiainen/ lounas/päivällinen) mukaan.

Seuraavassa on laskelmat, joiden mukaan päiväraha on 150 USD majoitukselle, 75 USD aterioille ja 5 USD satunnaisille kuluille:

- **Maksettavaa yhteensä** = 5 × (150 + 75 + 5) = 5 × 230 = 1 150 USD
- **Yksi ateria:** Ateriavähennys = 20 % = 15 USD
- **Kaksi ateriaa:** Ateriavähennys = 50 % = 37,50 USD
- **Kolme ateriaa:** Ateriavähennys = 100 % = 75 USD

Seuraavassa on **ateria- ja satunnaislisän** laskelmat, joihin sisältyy 5 USD satunnaisia kuluja varten:

- Päivä 1 – Kaksi ateriaa tarjottu = (75 - 37,50) + 5 = 37,50 + 5 = 42,50 USD
- Päivä 2 – Kaksi ateriaa tarjottu = (75 - 37,50) + 5 = 37,50 + 5 = 42,50 USD
- Päivä 3 – Yksi ateria tarjottu = (75 - 15) + 5 = 60 + 5 = 65 USD
- Päivä 4 – Nolla ateriaa tarjottu = (75 - 0) + 5 = 75 + 5 = 80 USD
- Päivä 5 – Kolme ateriaa tarjottu = (75 - 75) + 5 = 0 + 5 = 5 USD

- Ateriat ja satunnaiset kulut yhteensä = ateriat ja satunnaiset päivä 1+ päivä 2 +päivä 3+päivä 4+ päivä 5 = 235 USD
- Ateriavähennys yhteensä = ateriavähennys päivä 1+ päivä 2 + päivä 3 + päivä 4 + päivä 5= 37,5+ 37,5+ 15 + 0+ 75 = 165 USD
- Maksettava kokonaissumma = kokonaiskorvaus – kokonaisateriavähennys 1 150 - 165 = 985 USD

![Päivärahakulu, jossa ateriavähennys perustuu päiväkohtaiseen aterioiden määrään.](media/3-number-of-meals-per-day.png)

> [!NOTE]
> Finance-versiosta 10.0.23 eteenpäin et voi uudistetussa kulujen käyttöliittymässä luoda päivärahakuluja, jotka ovat päällekkäisiä päivämääriltään. Jos yrität sitä, saat virhesanoman.
