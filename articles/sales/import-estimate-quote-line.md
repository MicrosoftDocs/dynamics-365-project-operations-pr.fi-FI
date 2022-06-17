---
title: Projektiarvioiden tuonti projektin tarjousriville
description: Tässä artikkelissa on tietoja arvioiden tuomisesta projektista projektin tarjousriville.
author: rumant
ms.date: 10/09/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: dc5b6279a2123604291da35c9da2bf63dbe475b7
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8915042"
---
# <a name="import-estimates-for-a-project-to-a-project-quote-line"></a>Projektiarvioiden tuonti projektin tarjousriville

_**Käytetään:** Project Operationsin resursseihin ja ei-varastoitaviin perustuvissa skenaarioissa_


Jos projekti luodaan myyntiä edeltävän vaiheen aikana, voit valita, tuodaanko taloudellinen arvio projektista projektipohjaiselle tarjousriville.

1. Varmista, että projektipohjaisella tarjousrivillä on projektin tiedot **Projekti**-kentässä.
2. Valitse **Tarjousrivin tiedot** -välilehdessä **Tuo projektiarviosta**.
3. Valitse avautuvassa valintaikkunasivussa jokin seuraavista yhteenvetovaihtoehdoista:

  - **Tapahtumaluokka**
  - **Luokka**
  - **Rooli** 
  - **Projektitehtävä**

Valinnan perusteella kopioidaan projektista kaikkien tähän tarjousriviin sisältyvien tapahtumaluokkien arvio. Jos haluat tarkistaa, mitä tapahtumaluokkia on mukana, valitse projektipohjaisen tarjousrivin **Yleiset**-välilehti ja tarkista arvot **Sisällytä aika**, **Sisällytä kulut** ja **Sisällytä maksut**.

Kun tuot arvioita, järjestelmä määrittää hinnoittelun oletusarvon tarjoukseen liitettyjen projektihinnastojen ja projektipohjaisen tarjousrivin laskutustyypin perusteella. Jos projektipohjaiseen tarjousriviin on määritetty rooli tai luokka ei-laskutettavana, tuodun arviorivin arvoksi tulee ei-laskutettava eikä sitä lasketa mukaan tarjousrivin tarjotun arvon kanssa.

Kun tarjousrivillä on rivitiedot, tarjousrivin **Tarjouksen arvo**- ja **Arvioitu vero** -kentät on lasketaan yhteen, eikä niitä voi muokata.

Kun useita summausasetuksia valitaan, järjestelmä yrittää laskea yhteen kaikkien valittujen vaihtoehtojen mukaan. Tuloksena on, että tuotujen tarjousrivien tulos on suurempi kuin jos valitsit vain yhden summausasetuksen.

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


[!INCLUDE[footer-include](../includes/footer-banner.md)]
