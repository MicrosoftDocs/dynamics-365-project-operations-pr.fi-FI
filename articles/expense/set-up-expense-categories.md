---
title: Kululuokkien määrittäminen
description: Tässä aiheessa on tietoja siitä, miten kuluraporttien kululuokkia ja jaettuja luokkia määritetään.
author: suvaidya
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: suvaidya
ms.openlocfilehash: f051d70f3dfe3b241dc0a206c0cdfda000f87c76
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/28/2020
ms.locfileid: "3896682"
---
# <a name="set-up-expense-categories"></a>Kululuokkien määrittäminen

_**Käytetään:** Project Operationsin resursseihin ja ei-varastoitaviin perustuvissa skenaarioissa_

Kun työntekijät luovat kuluraportteja, kukin heidän tallentamansa kulu on liitettävä kululuokkaan. Kululuokat johdetaan jaetuista luokista, jotka voidaan jakaa organisaation yritysten kesken. Nämä kululuokat voidaan jakaa myös muilla alueilla sen mukaan, miten organisaatio on määritetty. Organisaation määritelmän ja käyttöönottoryhmän ohjeiden perusteella sinun täytyy määrittää, käytetäänkö kulujen hallinnassa käytettäviä luokkia vain kulujen hallinnassa vai pitäisikö ne jakaa muilla alueilla.

> [!NOTE]
> Nämä luokat voidaan jakaa projektinhallinnan ja kirjanpidon ja kulujen hallinnan välillä tai projektinhallinnan ja kirjanpidon sekä tuotannon välillä. Niitä ei kuitenkaan voi jakaa kulujen hallinnan ja tuotannon välillä.

Ennen määritysprosessin aloittamista on tehtävä seuraavat päätökset kullekin kululuokalle:

- Mikä on kululuokka? Esimerkkeinä voidaan mainita luokat lennoille, hotellille tai kilometrikorvauksille.
- Voiko kululuokkaa käyttää myös projektinhallinnassa ja kirjanpidossa? Jos voi käyttää, on tehtävä myös seuraavat päätökset:

    - Mitä kustannustilejä käytetään seuraaviin kuluihin?

        - Kustannus
        - Palkanlaskennan kohdistus
        - KET-kustannusarvo
        - Kustannusnimike
        - KET-kustannuksen arvonimike
        - Jaksotettu tappio
        - KET – jaksotettu tappio

    - Mitä tuottotilejä käytetään seuraavissa tuottolähteissä?

        - Laskutettu tuotto
        - Jaksotetun tuoton myyntiarvo
        - KET – myynnin arvo
        - Jaksotettu tuotto – tuotanto
        - KET – tuotanto
        - Jaksotettu tuotto – voitto
        - KET – voitto
        - Jaksotettu tuotto – tilaus
        - KET – tilaus

- Mikä on kulutyyppi?
- Mikä on kululuokan oletusmaksutapa?
- Onko kululuokan kulut eriteltävä?
- Mikä on kululuokan oletuspäätili?
- Mikä on kululuokan nimikkeen oletusarvonlisäveroryhmä?
- Sallitaanko kululuokalle muita maksutapoja? Jos sallitaan, mitä ne ovat?
- Onko kululuokassa aliluokkia? Jos aliluokkia on, on tehtävä myös seuraavat päätökset:

    - Jätetäänkö jotkin aliluokat pois veronpalautuksesta?
    - Mikä on aliluokkien nimikkeen arvonlisäveroryhmä?
