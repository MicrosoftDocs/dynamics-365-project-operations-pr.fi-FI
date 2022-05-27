---
title: Kulujen erittely
description: Tässä aiheessa selitetään, miten kulut eritellään käyttäen uudistettua kulutyötilaa.
author: suvaidya
ms.date: 12/16/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: suvaidya
ms.openlocfilehash: 34b11c6bd8be729957973a60fccccc2dd32c2669
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/14/2022
ms.locfileid: "8574518"
---
# <a name="expense-itemization"></a>Kulujen erittely

[!include [banner](../includes/banner.md)]

_**Käytetään:** Project Operationsin resursseihin ja ei-varastoitaviin perustuvissa skenaarioissa_

Organisaatiot edellyttävät usein, että työntekijät antavat yksityiskohtaisen erittelyn matkoista aiheutuvista kuluista. Esimerkiksi hotellilasku voi sisältää useita eriteltyjä rivejä, jotka koskevat huoneen hintaa, veroja, pysäköintiä tai muita kuluja, joita on kertynyt vierailupäivien aikana. Ruokailukuluihin liittyen saatetaan vaatia, että kulut ilmoitetaan tarkemmin esimerkiksi aamiaisen, lounaan ja päivällisen osalta. Organisaation tarpeista riippumatta kukin kululuokka voidaan määrittää kuvaamaan alaluokkia tai rivinimikkeitä, joista kulu koostuu. Erittelyä on aina tuettu **kulujen hallinnassa**, mutta **uudistettu kulujen** työtila antaa mahdollisuuden vielä tehokkaampaan erittelyyn, kun **Erittele toistuvat kulut nopeasti** -ominaisuus on otettu käyttöön.  

## <a name="enable-quick-itemization"></a>Ota käyttöön nopea erittely 

Voit käyttää **Erittele toistuvat kulut nopeasti** -ominaisuutta toistuvien kulujen nopeaan erittelyyn. Samalla vältät tarpeen syöttää päivittäiset kulut aina erikseen. Ota nopea erittely käyttöön seuraavasti.

1. Siirry **Ominaisuuksien hallinta** -työtilaan. Hae ja valitse ominaisuuksien luettelosta **Uudistetut kuluraportit**. 
2. Valitse **Ota käyttöön nyt**. 
3. Hae ja valitse ominaisuuksien luettelosta **Erittele toistuvat kulut nopeasti**.
4. Valitse **Ota käyttöön nyt**. 

## <a name="itemization-grid"></a>Erittelyruudukko 

Jos kululuokka sisältää alaluokkia tai komponentteja, jotka muodostavat kulun, se voidaan eritellä. Erittele kulu valitsemalla kulurivi kuluraportista ja valitse sitten **Kulun tiedot** -ruudusta **Toiminnot** > **Erittele**. **Erittely**-liukusäädin tuo esiin ruudukon ja kentät. Seuraavassa taulukossa on esimerkki kustakin ruudukon kentästä ja siitä, miten kenttä hahmonnetaan kuluraportissa. 

|     Field          |     Description                                                                                  |     Esimerkki:              |
|--------------------|--------------------------------------------------------------------------------------------------|--------------------------|
|     Alakategoria    |     Kululuokkatyypin **Hotelli** alla määritetty alaluokkaluettelo.             |     Huoneen päivähinta      |
|     Alkamispäivä     |     Päivämäärä, jolloin kulunimike aiheutui ensimmäisen kerran.                                           |     13.9.2021           |
|     Päivähinta     |     Kulunimikkeelle aiheutunut summa.                                                    |     200                  |
|     Määrä       |     Kuinka monta kertaa veloitus toistetaan keskeytyksettä.                       |     3                    |

![Erittele kulu.](media/Itemization%20screen%201.png)

Kun olet tallentanut erittelyn, näet määritetylle summalle yksittäisen eritellyn rivin erittelyruudukossa. Jokainen rivi alkaa ruudukossa määritetystä päivämäärästä.

![Eritelty raportti.](media/Itemization%20screen%202.png)

