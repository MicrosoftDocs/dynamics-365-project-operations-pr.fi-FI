---
title: Arvion tuonti projektipohjaiselle sopimusriville – lite
description: Tässä aiheessa on tietoja siitä, miten projektin rahoitusarviot tuodaan sopimusriville.
author: rumant
ms.date: 10/19/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: fb85d835789da82f22ae007addb6757ab3c166180992e4ce3a5c85606be6671d
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/06/2021
ms.locfileid: "6997242"
---
# <a name="import-an-estimate-to-a-project-based-contract-line---lite"></a>Arvion tuonti projektipohjaiselle sopimusriville – lite

_**Käytetään:** Lite-käyttöönotto – kauppa proformalaskutukseen_

Voit tuoda arvioita projektista projektipohjaiselle sopimusriville Dynamics 365 Project Operations -sovelluksessa.

1. Tarkista, että projektipohjaisen sopimusrivin **Projekti**-kenttä on täytetty.
2. Valitse **Sopimusrivin tiedot** -välilehdessä aliruudukossa **Tuo projektiarviosta**. Näkyviin tulee keskustelusivu, jossa on yhteenvetovaihtoehtoja. Yhteenvedon vaihtoehdot ovat **tapahtumaluokka**, **luokka**, **rooli** ja **projektitehtävä**.
3. Yhteenvedon valinnan perusteella kopioidaan projektista kaikkien tähän sopimusriviin sisältyvien tapahtumaluokkien ja tehtävien arvio. Jos haluat tarkistaa, mitä tapahtumaluokkia on mukana, valitse projektipohjaisen sopimusrivin **Yleiset**-välilehti ja tarkista arvot kentissä **Sisällytä aika**, **Sisällytä kulut** ja **Sisällytä maksut**. 
4. Voit katsoa sisällytettävät tehtävät valitsemalla sopimusriviltä **laskutettavat tehtävät** -välilehden. Perustuen liitettyihin tehtäviin, joiden kentän **Mukana olevat tapahtumaluokat** -asetukseksi on valittu **Kyllä**, kaikki näiden tehtävien ja tapahtumaluokkien yhdistelmien arviot tuodaan sopimusriville.

Kun tuot arvioita, järjestelmä olettaa hinnoittelun sopimukseen liitettyjen projektihintojen ja sopimusrivin laskutustyypin määrityksen perusteella. Jos tehtävä, rooli tai luokka on määritetty sopimusriville ei-laskutettavaksi, tuodun arvion rivi on veloittamaton eikä se lisää sopimusrivin sopimuksen arvoa.

Kun sopimusrivillä on rivitiedot, sopimusrivin **sopimuksen arvo**- ja **Arvioitu vero** -kentät on lasketaan yhteen, eikä niitä voi muokata.

Kun useita summausasetuksia valitaan, järjestelmä yrittää laskea yhteen kaikkien valittujen vaihtoehtojen mukaan. Yhteenvedon tuotos johtaa enemmän tuotuihin sopimusriveihin kuin jos valitset vain yhden yhteenvedon vaihtoehdon.

Jos projektilla on esimerkiksi seuraavat arviorivit kuluja varten:

| Tehtävä | Luokka | Päivämäärä | Määrä | Yksikköhinta | Summa |
| --- | --- | --- | --- | --- | --- |
| Tehtävä A | Lentoliput | 1.10.2020 | 4 | 400 | 1600 |
| Tehtävä B | Hotelli | 1.10.2020 | 4 | 200 | 800 |
| Tehtävä C | Hotelli | 1.11.2020 | 2 | 200 | 400 |

Kun käyttäjä valitsee summauksen **tapahtumaluokan** mukaan, seuraavat tiedot tuodaan:

| Tehtävä | Luokka | Päivämäärä | Määrä | Yksikköhinta | Summa |
| --- | --- | --- | --- | --- | --- |
| &nbsp; | &nbsp; | 1.10.2020 | 3.34 | 840 | 2800 |

Kun käyttäjä valitsee summauksen **tapahtumaluokan** ja **luokan** mukaan, seuraavat tiedot tuodaan:

| Tehtävä | Luokka | Päivämäärä | Määrä | Yksikköhinta | Summa |
| --- | --- | --- | --- | --- | --- |
| Tehtävä A | Lentoliput | 1.10.2020 | 4 | 400 | 1600 |
| &nbsp;| Hotelli | 1.10.2020 | 6 | 200 | 1200 |

Kun käyttäjä valitsee summauksen **tapahtumaluokan**, **luokan** ja **lehtisolmutehtävän** mukaan, seuraavat tiedot tuodaan. Huomaa, että tämä tulos on sama kuin mitä projektissa on:

| Tehtävä | Luokka | Päivämäärä | Määrä | Yksikköhinta | Summa |
| --- | --- | --- | --- | --- | --- |
| Tehtävä A | Lentoliput | 1.10.2020 | 4 | 400 | 1600 |
| Tehtävä B | Hotelli | 1.10.2020 | 4 | 200 | 800 |
| Tehtävä C | Hotelli | 1.11.2020 | 2 | 200 | 400 |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]