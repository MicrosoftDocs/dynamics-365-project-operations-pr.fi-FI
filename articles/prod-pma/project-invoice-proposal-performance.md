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
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 23561
ms.assetid: bfd18d9b-d9a6-4e21-bc95-bf4af45f617f
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 20121-03-05
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 8b6df8baf1013720778308ce536b037dec4775f040d2925a47508fb373900f81
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/06/2021
ms.locfileid: "7005702"
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
