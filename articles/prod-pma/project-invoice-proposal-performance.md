---
title: Projektin laskuehdotusten suorituskyky
description: Tässä artikkelissa on tietoja projektin laskuehdotusten suorituskykyparannuksista.
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
ms.openlocfilehash: 70069778b7d4326cb23d6bb36e2c78a33da12573
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8927186"
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
