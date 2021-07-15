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
ms.openlocfilehash: 5a14acf51d277b16896d64c4b12ee00bfb326910
ms.sourcegitcommit: 3a4b181be08ef0428104d72b54a3e61ac2782f14
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/17/2021
ms.locfileid: "6269786"
---
# <a name="project-invoice-proposal-performance"></a><span data-ttu-id="fa99b-103">Projektin laskuehdotusten suorituskyky</span><span class="sxs-lookup"><span data-stu-id="fa99b-103">Project invoice proposal performance</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="fa99b-104">Kun luot uuden laskuehdotukseen, suorituskykyongelmia voi ilmetä projektien ja aliprojektien määrän kasvaessa.</span><span class="sxs-lookup"><span data-stu-id="fa99b-104">When you create a new invoice proposal you might encounter performance issues as the number of projects and subprojects increase.</span></span> <span data-ttu-id="fa99b-105">Suorituskyvyn parantamiseksi käytettävissä on ominaisuus, joka vähentää uusien laskuehdotusten luomiseen lähetettyjä projektitapahtumia varten tarvittavaa aikaa.</span><span class="sxs-lookup"><span data-stu-id="fa99b-105">To improve performance, a feature is available that reduces the time needed to create a new invoice proposal for posted project transactions.</span></span>

## <a name="enable-project-invoice-proposal-performance-enhancement"></a><span data-ttu-id="fa99b-106">Projektin laskuehdotusten suorituskyvyn parantamisen käyttöönotto</span><span class="sxs-lookup"><span data-stu-id="fa99b-106">Enable project invoice proposal performance enhancement</span></span>
<span data-ttu-id="fa99b-107">Ota projektin laskuehdotusten suorituskyvyn parantamistoiminto käyttöön toimimalla seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="fa99b-107">To enable the project invoice proposal performance enhancement feature, complete the following steps.</span></span>

1.  <span data-ttu-id="fa99b-108">Siirry kohteeseen **Ominaisuuksien hallinta** > **Kaikki**.</span><span class="sxs-lookup"><span data-stu-id="fa99b-108">Go to **Feature management** > **All**.</span></span> <span data-ttu-id="fa99b-109">Etsi ominaisuusluettelosta **Projektin laskuehdotusten suorituskyvyn parantaminen**.</span><span class="sxs-lookup"><span data-stu-id="fa99b-109">In the feature list, locate **Project invoice proposal performance enhancement**.</span></span>
2.  <span data-ttu-id="fa99b-110">Valitse **Ota käyttöön nyt**.</span><span class="sxs-lookup"><span data-stu-id="fa99b-110">Select **Enable now**.</span></span>
3.  <span data-ttu-id="fa99b-111">Päivitä selain ja luo sitten uusi laskuehdotus.</span><span class="sxs-lookup"><span data-stu-id="fa99b-111">Refresh your browser, and then create a new invoice proposal.</span></span>

## <a name="turn-off-project-invoice-proposal-performance-enhancement"></a><span data-ttu-id="fa99b-112">Projektin laskuehdotusten suorituskyvyn parantamisen poistaminen käytöstä</span><span class="sxs-lookup"><span data-stu-id="fa99b-112">Turn off project invoice proposal performance enhancement</span></span>
<span data-ttu-id="fa99b-113">Poista projektin laskuehdotusten suorituskyvyn parantamistoiminto käytöstä suorittamalla seuraavat vaiheet.</span><span class="sxs-lookup"><span data-stu-id="fa99b-113">Complete the following steps to turn off the project invoice proposal performance enhancement.</span></span>

1.  <span data-ttu-id="fa99b-114">Siirry kohteeseen **Ominaisuuksien hallinta** > **Kaikki**.</span><span class="sxs-lookup"><span data-stu-id="fa99b-114">Go to **Feature management** > **All**.</span></span> <span data-ttu-id="fa99b-115">Etsi ominaisuusluettelosta **Projektin laskuehdotusten suorituskyvyn parantaminen**.</span><span class="sxs-lookup"><span data-stu-id="fa99b-115">In the feature list, locate **Project invoice proposal performance enhancement**.</span></span>
2.  <span data-ttu-id="fa99b-116">Valitse **Poista käytöstä**.</span><span class="sxs-lookup"><span data-stu-id="fa99b-116">Select **Disable**.</span></span>
3.  <span data-ttu-id="fa99b-117">Päivitä selain.</span><span class="sxs-lookup"><span data-stu-id="fa99b-117">Refresh your browser.</span></span>

> [!NOTE]
> <span data-ttu-id="fa99b-118">Laskuehdotusten suorituskykyä ei voi ottaa käyttöön, kun laskutussäännöt on otettu käyttöön.</span><span class="sxs-lookup"><span data-stu-id="fa99b-118">Invoice proposal performance can't be applied when billing rules are enabled.</span></span>
> 
> <span data-ttu-id="fa99b-119">Kun luot laskuehdotuksia eräprosessina, alitehtävien määrä jaetaan enimmäismäärään laskutettavia tapahtumia koskevien palvelusopimusten määrän perusteella huolimatta siitä, mitä olet syöttänyt.</span><span class="sxs-lookup"><span data-stu-id="fa99b-119">During the batch process to create invoice proposals, the number of subtasks will split the tasks to a maximum number based on the number of contracts with invoiceable transactions, regardless of what you have entered.</span></span> <span data-ttu-id="fa99b-120">Jos esimerkiksi määrität **3** laskuehdotusten eräluonnin alitehtävien määräksi ja laskutettavia tapahtumia on vain kaksi, vain kaksi alitehtävää luodaan.</span><span class="sxs-lookup"><span data-stu-id="fa99b-120">For example, if you enter **3** for the number of subtasks for invoice proposal creation in batch, and there are only two contracts with invoiceable transactions, only two subtasks are created.</span></span>
