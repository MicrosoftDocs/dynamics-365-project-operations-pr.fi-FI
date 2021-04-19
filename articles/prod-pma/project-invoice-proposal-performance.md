---
title: Projektin laskuehdotusten suorituskyky
description: Tässä aiheessa on tietoja projektin laskuehdotusten suorituskykyparannuksista.
author: Yowelle
manager: AnnBe
ms.date: 03/05/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
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
ms.openlocfilehash: 78c924cba8107471a5f8e6d6a38265890d32d72b
ms.sourcegitcommit: 2350c6f3728067a8298adde640e6fdd5984eb077
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/10/2021
ms.locfileid: "5573555"
---
# <a name="project-invoice-proposal-performance"></a><span data-ttu-id="f67d8-103">Projektin laskuehdotusten suorituskyky</span><span class="sxs-lookup"><span data-stu-id="f67d8-103">Project invoice proposal performance</span></span>

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

<span data-ttu-id="f67d8-104">Kun luot uuden laskuehdotukseen, suorituskykyongelmia voi ilmetä projektien ja aliprojektien määrän kasvaessa.</span><span class="sxs-lookup"><span data-stu-id="f67d8-104">When you create a new invoice proposal you might encounter performance issues as the number of projects and subprojects increase.</span></span> <span data-ttu-id="f67d8-105">Suorituskyvyn parantamiseksi käytettävissä on ominaisuus, joka vähentää uusien laskuehdotusten luomiseen lähetettyjä projektitapahtumia varten tarvittavaa aikaa.</span><span class="sxs-lookup"><span data-stu-id="f67d8-105">To improve performance, a feature is available that reduces the time needed to create a new invoice proposal for posted project transactions.</span></span>

## <a name="enable-project-invoice-proposal-performance-enhancement"></a><span data-ttu-id="f67d8-106">Projektin laskuehdotusten suorituskyvyn parantamisen käyttöönotto</span><span class="sxs-lookup"><span data-stu-id="f67d8-106">Enable project invoice proposal performance enhancement</span></span>
<span data-ttu-id="f67d8-107">Ota projektin laskuehdotusten suorituskyvyn parantamistoiminto käyttöön toimimalla seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="f67d8-107">To enable the project invoice proposal performance enhancement feature, complete the following steps.</span></span>

1.  <span data-ttu-id="f67d8-108">Siirry kohteeseen **Ominaisuuksien hallinta** > **Kaikki**.</span><span class="sxs-lookup"><span data-stu-id="f67d8-108">Go to **Feature management** > **All**.</span></span> <span data-ttu-id="f67d8-109">Etsi ominaisuusluettelosta **Projektin laskuehdotusten suorituskyvyn parantaminen**.</span><span class="sxs-lookup"><span data-stu-id="f67d8-109">In the feature list, locate **Project invoice proposal performance enhancement**.</span></span>
2.  <span data-ttu-id="f67d8-110">Valitse **Ota käyttöön nyt**.</span><span class="sxs-lookup"><span data-stu-id="f67d8-110">Select **Enable now**.</span></span>
3.  <span data-ttu-id="f67d8-111">Päivitä selain ja luo sitten uusi laskuehdotus.</span><span class="sxs-lookup"><span data-stu-id="f67d8-111">Refresh your browser, and then create a new invoice proposal.</span></span>

## <a name="turn-off-project-invoice-proposal-performance-enhancement"></a><span data-ttu-id="f67d8-112">Projektin laskuehdotusten suorituskyvyn parantamisen poistaminen käytöstä</span><span class="sxs-lookup"><span data-stu-id="f67d8-112">Turn off project invoice proposal performance enhancement</span></span>
<span data-ttu-id="f67d8-113">Poista projektin laskuehdotusten suorituskyvyn parantamistoiminto käytöstä suorittamalla seuraavat vaiheet.</span><span class="sxs-lookup"><span data-stu-id="f67d8-113">Complete the following steps to turn off the project invoice proposal performance enhancement.</span></span>

1.  <span data-ttu-id="f67d8-114">Siirry kohteeseen **Ominaisuuksien hallinta** > **Kaikki**.</span><span class="sxs-lookup"><span data-stu-id="f67d8-114">Go to **Feature management** > **All**.</span></span> <span data-ttu-id="f67d8-115">Etsi ominaisuusluettelosta **Projektin laskuehdotusten suorituskyvyn parantaminen**.</span><span class="sxs-lookup"><span data-stu-id="f67d8-115">In the feature list, locate **Project invoice proposal performance enhancement**.</span></span>
2.  <span data-ttu-id="f67d8-116">Valitse **Poista käytöstä**.</span><span class="sxs-lookup"><span data-stu-id="f67d8-116">Select **Disable**.</span></span>
3.  <span data-ttu-id="f67d8-117">Päivitä selain.</span><span class="sxs-lookup"><span data-stu-id="f67d8-117">Refresh your browser.</span></span>

> [!NOTE]
> <span data-ttu-id="f67d8-118">Laskuehdotusten suorituskykyä ei voi ottaa käyttöön, kun laskutussäännöt on otettu käyttöön tai eräprosesseja suoritetaan.</span><span class="sxs-lookup"><span data-stu-id="f67d8-118">Invoice proposal performance can't be applied when billing rules are enabled or batch processes are running.</span></span>
