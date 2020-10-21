---
title: Tuo projektiarviot projektipohjaiselle tarjousriville
description: Tässä aiheessa on tietoja siitä, miten projektin arviot tuodaan tarjousriville.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 75511f0d7ef1d2d1b3bf5cc598a8f51d0c553939
ms.sourcegitcommit: 56c42d7f5995a674426a1c2a81bae897dceb391c
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/01/2020
ms.locfileid: "3908073"
---
# <a name="import-estimates-for-a-project-to-a-project-based-quote-line"></a>Tuo projektiarviot projektipohjaiselle tarjousriville

_**Koskee:** Project Operationsin resurssiin / muuhun kuin resurssiin perustuvia skenaarioita, Lite-käyttöönotto-kaupasta proformalaskutukseen_


Jos projekti luodaan myyntiä edeltävän vaiheen aikana, voit valita, tuodaanko taloudellinen arvio projektista projektipohjaiselle tarjousriville.

1. Varmista, että projektipohjaisella tarjousrivillä on projektin tiedot **Projekti**-kentässä.
2. Valitse **Tarjousrivin tiedot** -välilehdessä **Tuo projektiarviosta**.
3. Valitse avautuvassa valintaikkunasivussa jokin seuraavista yhteenvetovaihtoehdoista.

  - **Tapahtumaluokka**
  - **Luokka**
  - **Rooli** 
  - **Projektitehtävä**

Valinnan perusteella kopioidaan projektista kaikkien tähän tarjousriviin sisältyvien tapahtumaluokkien arvio. Jos haluat tarkistaa, mitä tapahtumaluokkia on mukana, valitse projektipohjaisen tarjousrivin **Yleiset**-välilehti ja tarkista arvot **Sisällytä aika**, **Sisällytä kulut** ja **Sisällytä maksut**.

Kun tuot arvioita, järjestelmä määrittää hinnoittelun oletusarvon tarjoukseen liitettyjen projektihinnastojen ja projektipohjaisen tarjousrivin laskutustyypin perusteella. Jos projektipohjaiseen tarjousriviin on määritetty rooli tai luokka ei-laskutettavana, tuodun arviorivin arvoksi tulee ei-laskutettava eikä sitä lasketa mukaan tarjousrivin tarjotun arvon kanssa.

Kun tarjousrivillä on rivitiedot, tarjousrivin **Tarjouksen arvo**- ja **Arvioitu vero** -kentät on lasketaan yhteen, eikä niitä voi muokata.

Kun useita summausasetuksia valitaan, summaus yrittää laskea yhteen kaikkien valittujen vaihtoehtojen mukaan. Tämä tarkoittaa sitä, että tuotujen tarjousrivien tulos on suurempi kuin jos valitsit vain yhden summausasetuksen.

Jos projektilla on esimerkiksi seuraavat arviorivit kuluja varten.

| Tehtävä | Luokka | Päivä | Määrä | Yksikköhinta | Summa |
| --- | --- | --- | --- | --- | --- |
| Tehtävä A | Lentoliput | 1.10.2020 | 4 | 400 | 1600 |
| Tehtävä B | Hotelli | 1.10.2020 | 4 | 200 | 800 |
| Tehtävä C | Hotelli | 1.11.2020 | 2 | 200 | 400 |

Kun käyttäjä valitsee summauksen tapahtumaluokan mukaan, seuraavat tiedot tuodaan.

| Tehtävä | Luokka | Päivä | Määrä | Yksikköhinta | Summa |
| --- | --- | --- | --- | --- | --- |
| | | 1.10.2020 | 3.34 | 840 | 2800 |

Kun käyttäjä valitsee summauksen tapahtumaluokan ja luokan mukaan, seuraavat tiedot tuodaan.

| Tehtävä | Luokka | Päivä | Määrä | Yksikköhinta | Summa |
| --- | --- | --- | --- | --- | --- |
| Tehtävä A | Lentoliput | 1.10.2020 | 4 | 400 | 1600 |
| | Hotelli | 1.10.2020 | 6 | 200 | 1200 |

Kun käyttäjä valitsee summauksen tapahtumaluokan, luokan ja lehtisolmutehtävän mukaan, seuraavat tiedot tuodaan. Huomaa, että tämä tulos on sama kuin mitä projektissa oli.

| Tehtävä | Luokka | Päivä | Määrä | Yksikköhinta | Summa |
| --- | --- | --- | --- | --- | --- |
| Tehtävä A | Lentoliput | 1.10.2020 | 4 | 400 | 1600 |
| Tehtävä B | Hotelli | 1.10.2020 | 4 | 200 | 800 |
| Tehtävä C | Hotelli | 1.11.2020 | 2 | 200 | 400 |