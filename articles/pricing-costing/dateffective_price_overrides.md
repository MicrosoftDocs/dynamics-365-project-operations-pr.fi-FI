---
title: Päivämääräperusteiset hinnan ohitukset
description: Tässä artikkelissa selostetaan, miten hinnaston tietyille hinnoille määritetään korvaavat hinnat.
author: rumant
ms.date: 09/01/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 41af5176c0809c9621fc0fa946a04492da7d152b
ms.sourcegitcommit: 37293b0b28f072deafc00112ddbbea91c48a7802
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/08/2022
ms.locfileid: "9445966"
---
# <a name="date-effective-price-overrides"></a>Päivämääräperusteiset hinnan ohitukset 

_**Koskee:** Project Operationsin resurssiin / muuhun kuin resurssiin perustuvia skenaarioita, Lite-käyttöönotto-kaupasta proformalaskutukseen_

*Päivämääräperusteiset hinnan ohitukset* antavat tavan korvata tai muuttaa hinnastossa tiettyjä hintoja. Esimerkiksi vakiohintaluettelo on voimassa 1.1.2022–31.12.2022. Tässä hinnastossa on hinnat monelle roolille. **Verkkoteknikko**-roolille määritetty hinta on 100 dollaria (USD) tunnissa. Kun verkkoteknikko kirjaa ajan aikavälillä 1.1.2022–31.12.2022, aika hinnoitellaan 100 USD tunnissa. 1.10.2022 hintaa on oikaistava *vain* **Verkkoteknikko**-roolille 100 USD -hinnasta hintaan 110 USD tunnissa. **Päivämääräperusteiset hinnan ohitukset** -ominaisuuden avulla voit määrittää tämän muutoksen korvaavaksi hinnaksi tämän roolin hinnan riville. Siksi koko hinnastoa ei tarvitse kopioida ja vain yhden rivin hintaa muuttaa.

## <a name="date-effective-price-overrides-for-labor-pricing"></a>Päivämääräperusteiset hinnan ohitukset työn hinnoittelulle

Kun määritetään päivämääräperusteiset hinnan ohitukset projektin työajalle, prosessiin sisältyy kaksi perusvaihetta.

1. Ota käyttöön **Päivämääräperusteiset hinnan ohitukset** -ominaisuus.
1. Määritä päivämääräperusteinen hinnan ohitus.

### <a name="enable-the-date-effective-price-overrides-feature"></a>Ota käyttöön Päivämääräperusteiset hinnan ohitukset -ominaisuus

> [!NOTE]
> Kun **Päivämääräperusteiset hinnan ohitukset** -ominaisuus on otettu käyttöön, sitä ei voi poistaa käytöstä.

Voit ottaa **Päivämääräperusteiset hinnan ohitukset** -ominaisuuden käyttöön seuraavasti.

1. Siirry kohtaan **Asetukset** \> **Parametrit**.
1. Avaa **Parametrit**-tietue.
1. Valitse Toimintoruudun **Ominaisuuksien hallinta** -välilehdessä **Ota käyttöön päivämääräperusteiset hinnan ohitukset**.
1. Valitse vahvistusikkunassa **OK**.
1. Päivitä selain hetken kuluttua. Päivämääräperusteiset hinnan ohitukset -ominaisuuksien pitäisi nyt olla käytettävissä. Nämä ominaisuudet on otettu käyttöön, jos **Ota käyttöön päivämääräperusteiset hinnan ohitukset** ei enää näy toimintoruudussa.

### <a name="set-up-a-date-effective-price-override"></a>Määritä päivämääräperusteinen hinnan ohitus

Päivämääräperusteisia hinnan ohituksia voidaan määrittää **Kustannus**-, **Myynti**- tai **Osto**-hinnastoissa.

> [!NOTE]
>**Päivämääräperusteiset hinnan ohitukset** -ominaisuuden käyttäytymisessä on tällä hetkellä seuraavat rajoitukset:
>
> - Vain roolin hinnat ja roolin hinnankorotukset tukevat **Päivämääräperusteiset hinnan ohitukset** -ominaisuutta Project Operationsissa.
> - Kun hinnasto kopioidaan **Hinnaston tiedot** -sivun **Kopioi**-toiminnon avulla ja kun luot projektihinnastoa vakiohinnastosta tai mukautetusta hinnastosta palvelusopimuksen luonnin aikana, päivämääräperusteisia hinnan ohituksia **ei** kopioida lähdehintaluettelosta.

Voit määrittää päivämääräperusteisen hinnan ohituksen roolihinnalle tai roolihinnan korotukselle seuraavasti.

1. Avaa sen hinnaston sivu, johon haluat määrittää päivämääräperusteisen hinnan ohituksen.
1. Valitse **Roolin hinnat** -välilehti. Tässä välilehdessä on luettelo kaikista hinnastossa olevista **Roolin hinta** -tietueista.
1. Valitse **Roolin hinta** -tietue, johon haluat määrittää uuden päivämääräperusteisen hinnan ohituksen, ja avaa sitten **Roolin hinnan tiedot** -sivu kaksoisnapauttamalla (tai kaksoisnapsauttamalla) **Roolin hinta**.
1. Valitse **Päivämääräperusteiset hinnan ohitukset** -välilehti. Tämän välilehden ruudukossa näkyvät kaikki valitun **Roolihinta**-tietueen päivämääräperusteiset hinnan ohitukset.
1. Valitse ruudukon yläpuolella olevasta työkaluriviltä **Uusi roolihinnan ohitus**. **Uusi roolihinnan ohitus** -liukusäädin avautuu.
1. Määritä hinnan ohituksen voimassaolon aloituspäivä, yksikkö ja uusi hinta. Valitse sitten **Tallenna** ja sulje lomake.

> [!NOTE]
> - Roolihinnan tai roolihinnan korotuksen päivämääräperusteiset hinnan ohitukset koskevat samaa hinnoitteludimension arvojen yhdistelmää, jotka ovat ylätason **Roolin hinta**- tai **Roolihinnan korotus** -rivillä.
> - **Voimassaolo alkaen** -kentässä valitun päivämäärän on oltava ylätason hinnaston voimassaolopäivien sisällä. Hinnan korvaaminen tulee voimaan päivämääränä, joka on valittu **Voimassaolo alkaen** -kentässä, ja sitä käytetään päähintaluettelon päättymispäivään asti. Jos määrität samalle roolihinnalle toisen päivämääräperusteisen hinnan ohituksen, ensimmäinen hinnan ohitus tulee voimaan päivämääränä, joka on valittu **Voimassaolo alkaen** -kentässä, ja se on voimassa toisen ohituksen alkuun asti.

## <a name="examples"></a>Esimerkkejä

### <a name="example-1-determining-date-effectivity-for-a-role-price-that-has-role-price-overrides"></a>Esimerkki 1: Päivämäärävoimassaolon määrittäminen roolihinnalle, jolla on roolihinnan ohituksia

Seuraavassa esimerkissä näytetään, miten päivämäärävoimassaolo määritetään tietylle roolin hinnalle, jolle on määritetty roolin hinnan ohitukset.

**Hinnasto A: 1.1.–30.6.**

*Roolin hinta*

| Roolin hinta | Yksikkö | Hinta | Vaikutus saapuvien tapahtumien hinnoitteluun |
|---|---|---|---|
| Verkkoteknikko | Tunti | 100 | Tätä hintaa käytetään tapahtumissa, joissa tapahtumapäivä on välillä 1.1.–14.3. |

*Roolin hinnan ohitus*

| Voimassa alkaen | Yksikkö | Hinta | Vaikutus saapuvien tapahtumien hinnoitteluun |
|---|---|---|---|
| Maaliskuu 15 | Tunti | 110 | Tätä hintaa käytetään tapahtumissa, joissa tapahtumapäivä on välillä 15.3.–30.3. |
| Huhtikuu 1 | Tunti | 120 | Tätä hintaa käytetään tapahtumissa, joissa tapahtumapäivä on välillä 1.4.–30.6. |

### <a name="example-2-determining-date-effectivity-for-a-role-price-markup-that-has-role-price-markup-overrides"></a>Esimerkki 2: Päivämäärävoimassaolon määrittäminen roolihinnan korotukselle, jolla on roolihinnan korotuksen ohituksia

Seuraavassa esimerkissä näytetään, miten päivämäärävoimassaolo määritetään tietylle roolin hinnankorotukselle, jolle on määritetty roolin hinnankorotuksen ohitukset.

**Hinnasto A: 1.1.–30.6.**

*Roolin hinta*

| Roolin hinta | Työaika | Yksikkö | Hinta | Vaikutus saapuvien tapahtumien hinnoitteluun |
|---|---|---|---|---|
| Verkkoteknikko | Normaali | Tunti | 100 | Tätä hintaa käytetään tapahtumissa, joissa tapahtumapäivä on välillä 1.1.–14.3. |

*Roolin hinnankorotus*

| Organisaatioyksikkö | Työaika | Hinnankorotus-% |
|---|---|---|
| Contoso US | Ylityö | 10 % |

*Roolin hinnankorotuksen ohitus*

| Voimassa alkaen | Hinta | Vaikutus saapuvien tapahtumien hinnoitteluun |
|---|---|---|
| Maaliskuu 15 | 20 % | Tätä hinnankorotusprosenttia käytetään tapahtumissa, joissa tapahtumapäivä on välillä 15.3.–30.3. |
| Huhtikuu 1 | 25 % | Tätä hinnankorotusta käytetään tapahtumissa, joissa tapahtumapäivä on välillä 1.4.–30.6. |

[!INCLUDE[footer-include](../includes/footer-banner.md)]
