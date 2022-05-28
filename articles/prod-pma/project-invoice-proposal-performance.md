---
title: Projektin laskuehdotusten suorituskyky
description: Tässä aiheessa on tietoja projektin laskuehdotusten suorituskykyparannuksista.
author: Yowelle
ms.date: 06/16/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: johnmichalak
ms.custom: 23561
ms.assetid: bfd18d9b-d9a6-4e21-bc95-bf4af45f617f
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 20121-03-05
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: e707b0d9b379df59726271b5a0441ac04e269b9a
ms.sourcegitcommit: 2c2a5a11d446adec2f21030ab77a053d7e2da28e
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/04/2022
ms.locfileid: "8683442"
---
# <a name="project-invoice-proposal-performance"></a>Projektin laskuehdotusten suorituskyky

[!include [banner](../includes/banner.md)]

Kun luot uuden laskuehdotukseen, suorituskykyongelmia voi ilmetä projektien ja aliprojektien määrän kasvaessa. Suorituskyvyn parantamiseksi käytettävissä on ominaisuus, joka vähentää uusien laskuehdotusten luomiseen lähetettyjä projektitapahtumia varten tarvittavaa aikaa.

## <a name="enable-project-invoice-proposal-performance-enhancement"></a>Projektin laskuehdotusten suorituskyvyn parantamisen käyttöönotto
Ota projektin laskuehdotusten suorituskyvyn parantamistoiminto käyttöön toimimalla seuraavasti.

1.  Siirry kohteeseen **Ominaisuuksien hallinta** > **Kaikki**. Etsi ominaisuusluettelosta **Projektin laskuehdotusten suorituskyvyn parantaminen**.
2.  Valitse **Ota käyttöön nyt**.
3.  Päivitä selain ja luo sitten uusi laskuehdotus.

## <a name="turn-off-project-invoice-proposal-performance-enhancement"></a>Projektin laskuehdotusten suorituskyvyn parantamisen poistaminen käytöstä
Poista projektin laskuehdotusten suorituskyvyn parantamistoiminto käytöstä suorittamalla seuraavat vaiheet.

1.  Siirry kohteeseen **Ominaisuuksien hallinta** > **Kaikki**. Etsi ominaisuusluettelosta **Projektin laskuehdotusten suorituskyvyn parantaminen**.
2.  Valitse **Poista käytöstä**.
3.  Päivitä selain.

> [!NOTE]
> Laskuehdotusten suorituskykyä ei voi ottaa käyttöön, kun laskutussäännöt on otettu käyttöön.
> 
> Kun luot laskuehdotuksia eräprosessina, alitehtävien määrä jaetaan enimmäismäärään laskutettavia tapahtumia koskevien palvelusopimusten määrän perusteella huolimatta siitä, mitä olet syöttänyt. Jos esimerkiksi määrität **3** laskuehdotusten eräluonnin alitehtävien määräksi ja laskutettavia tapahtumia on vain kaksi, vain kaksi alitehtävää luodaan.
