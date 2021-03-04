---
title: Arvion tuonti projektipohjaiselle sopimusriville – lite
description: Tässä aiheessa on tietoja siitä, miten projektin rahoitusarviot tuodaan sopimusriville.
author: rumant
manager: Annbe
ms.date: 10/19/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: b462af163fef1bfcbbc4f945df722d4e8a71fb1a
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/30/2020
ms.locfileid: "4177462"
---
# <a name="import-an-estimate-to-a-project-based-contract-line---lite"></a>Arvion tuonti projektipohjaiselle sopimusriville – lite

_**Käytetään:** Lite-käyttöönotto – kauppa proformalaskutukseen_

Dynamics 365 Project Operationsissa voit tuoda arvioita projektista projektipohjaiseen sopimusriviin.

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