---
title: Projektiarvioiden tuonti projektipohjaiselle tarjousriville – lite
description: Tässä aiheessa on tietoja siitä, miten projektin arviot tuodaan tarjousriville.
author: rumant
ms.date: 10/09/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: a5ac7827f3499aafb63f6bc0b8580ca52e883f272464532bd353170a12b3ae55
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/06/2021
ms.locfileid: "6986127"
---
# <a name="import-estimates-for-a-project-to-a-project-based-quote-line"></a>Projektiarvioiden tuonti projektipohjaiselle tarjousriville 

_**Koskee:** Lite-käyttöönotto - kaupasta proformalaskutukseen, Project Operationsin resurssiin/ei-varastointiin perustuvia skenaarioita_

Jos projekti luodaan myyntiä edeltävän vaiheen aikana, voit valita, tuodaanko taloudellinen arvio projektista projektipohjaiselle tarjousriville.

1. Varmista, että projektipohjaisella tarjousrivillä on projektin tiedot **Projekti**-kentässä.
2. Valitse **Tarjousrivin tiedot** -välilehdessä **Tuo projektiarviosta**.
3. Valitse avautuvassa valintaikkunasivussa jokin seuraavista yhteenvetovaihtoehdoista.

  - **Tapahtumaluokka**
  - **Luokka**
  - **Rooli** 
  - **Projektitehtävä**

Valinnan perusteella kopioidaan projektista kaikkien tähän tarjousriviin sisältyvien tapahtumaluokkien arvio. Voit tarkistaa sisällytettävät tapahtumaluokat valitsemalla **Yleiset**-välilehden projektipohjaiselta tarjousriviltä ja tarkistamalla arvot **Sisällytä aika**, **Sisällytä kulut**, **Sisällytä materiaalit** ja **Sisällytä maksut**.  Voit tarkistaa sisällytettävät tehtävät valitsemalla tarjousriviltä **laskutettavat tehtävät** -välilehden.

Näiden tehtävien ja tapahtumaluokkien yhdistelmien arviot tuodaan tarjousriviin sen mukaan, mitä tehtäviä liittyy.

Kun tuot arvioita, järjestelmä määrittää hinnoittelun oletusarvon tarjoukseen liitettyjen projektihinnastojen ja projektipohjaisen tarjousrivin laskutustyypin perusteella. Jos projektipohjaiseen tarjousriviin on määritetty tehtävä, rooli tai luokka ei-laskutettavana, tuodun arviorivin arvoksi tulee ei-laskutettava eikä sitä lasketa mukaan tarjousrivin tarjotun arvon kanssa.

Kun tarjousrivillä on rivitiedot, tarjousrivin **Tarjouksen arvo**- ja **Arvioitu vero** -kentät on lasketaan yhteen, eikä niitä voi muokata.

Kun useita summausasetuksia valitaan, järjestelmä yrittää laskea yhteen kaikkien valittujen vaihtoehtojen mukaan. Tuloksena on, että tuotujen tarjousrivien tulos on suurempi kuin jos valitsit vain yhden summausasetuksen.

Jos projektilla oli esimerkiksi seuraavat arviorivit kuluja varten.

| Tehtävä | Luokka | Päivämäärä | Määrä | Yksikköhinta | Summa |
| --- | --- | --- | --- | --- | --- |
| Tehtävä A | Lentoliput | 1.10.2020 | 4 | 400 | 1600 |
| Tehtävä B | Hotelli | 1.10.2020 | 4 | 200 | 800 |
| Tehtävä C | Hotelli | 1.11.2020 | 2 | 200 | 400 |

Kun käyttäjä valitsee summauksen tapahtumaluokan mukaan, seuraavat tiedot tuodaan.

| Tehtävä | Luokka | Päivä | Määrä | Yksikköhinta | Summa |
| --- | --- | --- | --- | --- | --- |
|||1.10.2020 | 3.34 | 840 | 2800 |

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


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
