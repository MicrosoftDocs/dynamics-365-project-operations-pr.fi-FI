---
title: Arvion tuonti projektipohjaiselle sopimusriville
description: Tässä artikkelissa on tietoja siitä, miten projektin arviot tuodaan sopimusriville.
author: rumant
ms.date: 10/19/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: d4a298cbcb8d13447c0f6e264d2aa85ad7ed43bf
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8915088"
---
# <a name="import-an-estimate-to-a-project-based-contract-line"></a>Arvion tuonti projektipohjaiselle sopimusriville

_**Käytetään:** Project Operationsin resursseihin ja ei-varastoitaviin perustuvissa skenaarioissa_

Voit tuoda arvioita projektista projektipohjaiselle sopimusriville Dynamics 365 Project Operations -sovelluksessa.

1. Tarkista, että projektipohjaisen sopimusrivin **Projekti**-kenttä on täytetty.
2. Valitse **Sopimusrivin tiedot** -välilehdessä aliruudukossa **Tuo projektiarviosta**. Näkyviin tulee keskustelusivu, jossa on yhteenvetovaihtoehtoja. Saatavilla olevat yhteenvedon vaihtoehdot ovat **tapahtumaluokka**, **luokka**, **rooli** ja **projektitehtävä**. Yhteenvedon valintojen perusteella kopioidaan projektin arvio kaikista tämän sopimusrivin sisältämistä tapahtumaluokista. 
3. Jos haluat tarkistaa, mitä tapahtumaluokkia on mukana, valitse sopimusrivin **Yleiset**-välilehti ja tarkista arvot kentissä **Sisällytä aika**, **Sisällytä kulut** ja **Sisällytä maksut**.

Kun tuot arvioita, sovellus olettaa hinnoittelun sopimukseen liitettyjen projektin hinnastojen ja sopimusriville määritetyn laskutustyypin perusteella. Jos rooli tai luokka on määritetty sopimusriville ei-laskutettavaksi, tuodun arvion rivi tälle roolille tai luokalle on veloittamaton eikä se lisää sopimusrivin sopimuksen arvoa.

Kun sopimusrivillä on rivitiedot, sopimusrivin **sopimuksen arvo**- ja **Arvioitu vero** -kentät on lasketaan yhteen, eikä niitä voi muokata.

Kun useita summausasetuksia valitaan, järjestelmä yrittää laskea yhteen kaikkien valittujen vaihtoehtojen mukaan. Yhteenvedon tuotos johtaa enemmän tuotuihin sopimusriveihin kuin jos valitset vain yhden yhteenvedon vaihtoehdon.

Jos projektilla oli esimerkiksi seuraavat arviorivit kuluja varten:

| Tehtävä | Luokka | Päivämäärä | Määrä | Yksikköhinta | Summa |
| --- | --- | --- | --- | --- | --- |
| Tehtävä A | Lentoliput | 1.10.2020 | 4 | 400 | 1600 |
| Tehtävä B | Hotelli | 1.10.2020 | 4 | 200 | 800 |
| Tehtävä C | Hotelli | 1.11.2020 | 2 | 200 | 400 |

Kun käyttäjä valitsee summauksen **tapahtumaluokan** mukaan, seuraavat tiedot tuodaan:

| Tehtävä | Luokka | Päivämäärä | Määrä | Yksikköhinta | Summa |
| --- | --- | --- | --- | --- | --- |
| &nbsp;  | &nbsp;  | 1.10.2020 | 3.34 | 840 | 2800 |

Kun käyttäjä valitsee summauksen **tapahtumaluokan** ja **luokan** mukaan, seuraavat tiedot tuodaan:

| Tehtävä | Luokka | Päivämäärä | Määrä | Yksikköhinta | Summa |
| --- | --- | --- | --- | --- | --- |
| Tehtävä A | Lentoliput | 1.10.2020 | 4 | 400 | 1600 |
| &nbsp;  | Hotelli | 1.10.2020 | 6 | 200 | 1200 |

Kun käyttäjä valitsee summauksen **tapahtumaluokan**, **luokan** ja **lehtisolmutehtävän** mukaan, seuraavat tiedot tuodaan. Huomaa, että tämä tulos on sama kuin mitä projektissa oli:

| Tehtävä | Luokka | Päivämäärä | Määrä | Yksikköhinta | Summa |
| --- | --- | --- | --- | --- | --- |
| Tehtävä A | Lentoliput | 1.10.2020 | 4 | 400 | 1600 |
| Tehtävä B | Hotelli | 1.10.2020 | 4 | 200 | 800 |
| Tehtävä C | Hotelli | 1.11.2020 | 2 | 200 | 400 |


[!INCLUDE[footer-include](../includes/footer-banner.md)]