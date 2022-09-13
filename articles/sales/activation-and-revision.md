---
title: Projektitarjouksen aktivoiminen ja muuttaminen
description: Tässä artikkelissa on tietoja tarjouksen aktivoinnista ja muuttamisesta Microsoft Dynamics 365 Project Operationsissa.
author: rumant
ms.date: 09/01/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: e71102078832ac7d5f8e5edb40cc484df927eda4
ms.sourcegitcommit: 16c9eded66d60d4c654872ff5a0267cccae9ef0e
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/07/2022
ms.locfileid: "9410334"
---
# <a name="activate-and-revise-a-project-quote"></a>Projektitarjouksen aktivoiminen ja muuttaminen

_**Koskee:** Project Operationsin resurssiin / muuhun kuin resurssiin perustuvia skenaarioita, Lite-käyttöönotto-kaupasta proformalaskutukseen_

Aktivointi- ja muuttamisominaisuuksien avulla voit seurata projektipohjaisten tarjousten versiointeja arviointi- ja neuvotteluvaiheiden aikana. Kun tarjousluonnos aktivoidaan, se muuttuu vain luku -tyyppiseksi.

Aktivointi- ja muuttamisominaisuuksien avulla voit suorittaa seuraavat tehtävät:

- Voittaa tai hävitä tarjouksia vasta aktivoinnin jälkeen.
- Muuta tarjousta, jos haluat tehdä muutoksia aiemmin luotuun tarjoukseen tai luoda uuden version.

> [!NOTE]
> Kun tarjousten aktivointi- ja muuttamisominaisuus on otettu käyttöön, sitä ei voi poistaa käytöstä.

Voit ottaa käyttöön projektipohjaisten tarjousten aktivoinnin ja muuttamisen seuraavasti.

1. Siirry kohtaan **Asetukset** \> **Parametrit**.
1. Avaa **Parametrit**-tietue.
1. Valitse toimintoruudun **Ominaisuuksien hallinta** -välilehdessä **Ota käyttöön tarjousten aktivointi ja muutokset**.
1. Valitse vahvistusikkunassa **OK**.
1. Päivitä selain hetken kuluttua. Aktivointi- ja muuttamisominaisuuksien pitäisi nyt olla käytettävissä. Nämä ominaisuudet on otettu käyttöön, jos **Ota käyttöön tarjousten aktivointi ja muutokset** -painike ei enää näy toimintoruudussa.

## <a name="activating-a-quote"></a>Tarjouksen aktivointi

Kun tarjousten aktivointi- ja muutosominaisuus on otettu käyttöön, **Sulje tarjous voitettuna**- ja **Sulje tarjous hävittynä** -painikkeet toimintoruudussa eivät ole käytettävissä projektitarjousluonnoksissa. Ne ovat käytettävissä vasta, kun tarjous on aktivoitu.

Aktivointi edustaa tarjousprosessin sitä vaihetta, kun haluat estää tarjouksen muutokset. Tässä vaiheessa tarjous lähetetään sisäiseen tarkasteluun tai asiakkaalle.

**Sulje tarjous voitettuina**- ja **Sulje tarjous hävittynä** -painikkeet toimintoruudussa ovat käytettävissä aktivoituja tarjouksia varten. Sisäisen tai asiakkaan tarkistuksen tuloksen mukaan voit sulkea aktivoidun tarjouksen näiden painikkeiden avulla. Voit tehdä neuvotteluja ja muutoksia aktivoituihin tarjouksiin valitsemalla **Muuta tarjousta**.

## <a name="revising-a-quote"></a>Tarjouksen muuttaminen

Jos aktivoituun tarjoukseen on tehtävä muutoksia, valitse **Muuta tarjousta**. Tarjous suljetaan ja käytetään syykoodia **Muutettu**. Tämän jälkeen luodaan uusi tarjous, jolla on sama tunnus ja kasvatettu versionumero. Kaikki alkuperäisen tarjouksen tiedot kopioidaan uuteen tarjoukseen. Uusi tarjous on luonnostilassa, ja sitä voi muokata tarpeen mukaan.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
