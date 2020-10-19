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
# <a name="set-up-expense-categories"></a><span data-ttu-id="868d1-103">Kululuokkien määrittäminen</span><span class="sxs-lookup"><span data-stu-id="868d1-103">Set up expense categories</span></span>

<span data-ttu-id="868d1-104">_**Käytetään:** Project Operationsin resursseihin ja ei-varastoitaviin perustuvissa skenaarioissa_</span><span class="sxs-lookup"><span data-stu-id="868d1-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="868d1-105">Kun työntekijät luovat kuluraportteja, kukin heidän tallentamansa kulu on liitettävä kululuokkaan.</span><span class="sxs-lookup"><span data-stu-id="868d1-105">When employees create expense reports, each expense that they record must be associated with an expense category.</span></span> <span data-ttu-id="868d1-106">Kululuokat johdetaan jaetuista luokista, jotka voidaan jakaa organisaation yritysten kesken.</span><span class="sxs-lookup"><span data-stu-id="868d1-106">Expense categories are derived from shared categories that can be shared across the legal entities in your organization.</span></span> <span data-ttu-id="868d1-107">Nämä kululuokat voidaan jakaa myös muilla alueilla sen mukaan, miten organisaatio on määritetty.</span><span class="sxs-lookup"><span data-stu-id="868d1-107">Depending on how your organization is defined, these expense categories can also be shared in other areas.</span></span> <span data-ttu-id="868d1-108">Organisaation määritelmän ja käyttöönottoryhmän ohjeiden perusteella sinun täytyy määrittää, käytetäänkö kulujen hallinnassa käytettäviä luokkia vain kulujen hallinnassa vai pitäisikö ne jakaa muilla alueilla.</span><span class="sxs-lookup"><span data-stu-id="868d1-108">Based on the definition of your organization and guidance from the implementation team, you must determine whether the categories that are used in Expense management will be used only in Expense management or should be shared in other areas.</span></span>

> [!NOTE]
> <span data-ttu-id="868d1-109">Nämä luokat voidaan jakaa projektinhallinnan ja kirjanpidon ja kulujen hallinnan välillä tai projektinhallinnan ja kirjanpidon sekä tuotannon välillä.</span><span class="sxs-lookup"><span data-stu-id="868d1-109">These categories can be shared between Project management and accounting and Expense management, or between Project management and accounting and Production.</span></span> <span data-ttu-id="868d1-110">Niitä ei kuitenkaan voi jakaa kulujen hallinnan ja tuotannon välillä.</span><span class="sxs-lookup"><span data-stu-id="868d1-110">However, they can't be shared between Expense management and Production.</span></span>

<span data-ttu-id="868d1-111">Ennen määritysprosessin aloittamista on tehtävä seuraavat päätökset kullekin kululuokalle:</span><span class="sxs-lookup"><span data-stu-id="868d1-111">Before you can begin the setup process, the following decisions must be made for each expense category:</span></span>

- <span data-ttu-id="868d1-112">Mikä on kululuokka?</span><span class="sxs-lookup"><span data-stu-id="868d1-112">What is the expense category?</span></span> <span data-ttu-id="868d1-113">Esimerkkeinä voidaan mainita luokat lennoille, hotellille tai kilometrikorvauksille.</span><span class="sxs-lookup"><span data-stu-id="868d1-113">Examples include categories for flights, hotel, or mileage.</span></span>
- <span data-ttu-id="868d1-114">Voiko kululuokkaa käyttää myös projektinhallinnassa ja kirjanpidossa?</span><span class="sxs-lookup"><span data-stu-id="868d1-114">Can the expense category also be used in Project management and accounting?</span></span> <span data-ttu-id="868d1-115">Jos voi käyttää, on tehtävä myös seuraavat päätökset:</span><span class="sxs-lookup"><span data-stu-id="868d1-115">If it can, you must also make the following decisions:</span></span>

    - <span data-ttu-id="868d1-116">Mitä kustannustilejä käytetään seuraaviin kuluihin?</span><span class="sxs-lookup"><span data-stu-id="868d1-116">Which cost accounts will be used for the following expenses?</span></span>

        - <span data-ttu-id="868d1-117">Kustannus</span><span class="sxs-lookup"><span data-stu-id="868d1-117">Cost</span></span>
        - <span data-ttu-id="868d1-118">Palkanlaskennan kohdistus</span><span class="sxs-lookup"><span data-stu-id="868d1-118">Payroll allocation</span></span>
        - <span data-ttu-id="868d1-119">KET-kustannusarvo</span><span class="sxs-lookup"><span data-stu-id="868d1-119">WIP-cost value</span></span>
        - <span data-ttu-id="868d1-120">Kustannusnimike</span><span class="sxs-lookup"><span data-stu-id="868d1-120">Cost-item</span></span>
        - <span data-ttu-id="868d1-121">KET-kustannuksen arvonimike</span><span class="sxs-lookup"><span data-stu-id="868d1-121">WIP-cost value-item</span></span>
        - <span data-ttu-id="868d1-122">Jaksotettu tappio</span><span class="sxs-lookup"><span data-stu-id="868d1-122">Accrued loss</span></span>
        - <span data-ttu-id="868d1-123">KET – jaksotettu tappio</span><span class="sxs-lookup"><span data-stu-id="868d1-123">WIP-accrued loss</span></span>

    - <span data-ttu-id="868d1-124">Mitä tuottotilejä käytetään seuraavissa tuottolähteissä?</span><span class="sxs-lookup"><span data-stu-id="868d1-124">Which revenue accounts will be used for the following sources of revenue?</span></span>

        - <span data-ttu-id="868d1-125">Laskutettu tuotto</span><span class="sxs-lookup"><span data-stu-id="868d1-125">Invoiced revenue</span></span>
        - <span data-ttu-id="868d1-126">Jaksotetun tuoton myyntiarvo</span><span class="sxs-lookup"><span data-stu-id="868d1-126">Accrued revenue-sales value</span></span>
        - <span data-ttu-id="868d1-127">KET – myynnin arvo</span><span class="sxs-lookup"><span data-stu-id="868d1-127">WIP-sales value</span></span>
        - <span data-ttu-id="868d1-128">Jaksotettu tuotto – tuotanto</span><span class="sxs-lookup"><span data-stu-id="868d1-128">Accrued revenue-production</span></span>
        - <span data-ttu-id="868d1-129">KET – tuotanto</span><span class="sxs-lookup"><span data-stu-id="868d1-129">WIP-production</span></span>
        - <span data-ttu-id="868d1-130">Jaksotettu tuotto – voitto</span><span class="sxs-lookup"><span data-stu-id="868d1-130">Accrued revenue-profit</span></span>
        - <span data-ttu-id="868d1-131">KET – voitto</span><span class="sxs-lookup"><span data-stu-id="868d1-131">WIP-profit</span></span>
        - <span data-ttu-id="868d1-132">Jaksotettu tuotto – tilaus</span><span class="sxs-lookup"><span data-stu-id="868d1-132">Accrued revenue-subscription</span></span>
        - <span data-ttu-id="868d1-133">KET – tilaus</span><span class="sxs-lookup"><span data-stu-id="868d1-133">WIP-subscription</span></span>

- <span data-ttu-id="868d1-134">Mikä on kulutyyppi?</span><span class="sxs-lookup"><span data-stu-id="868d1-134">What is the expense type?</span></span>
- <span data-ttu-id="868d1-135">Mikä on kululuokan oletusmaksutapa?</span><span class="sxs-lookup"><span data-stu-id="868d1-135">What is the default payment method for the expense category?</span></span>
- <span data-ttu-id="868d1-136">Onko kululuokan kulut eriteltävä?</span><span class="sxs-lookup"><span data-stu-id="868d1-136">Do expenses in the expense category have to be itemized?</span></span>
- <span data-ttu-id="868d1-137">Mikä on kululuokan oletuspäätili?</span><span class="sxs-lookup"><span data-stu-id="868d1-137">What is the main default account for the expense category?</span></span>
- <span data-ttu-id="868d1-138">Mikä on kululuokan nimikkeen oletusarvonlisäveroryhmä?</span><span class="sxs-lookup"><span data-stu-id="868d1-138">What is the default item sales tax group for the expense category?</span></span>
- <span data-ttu-id="868d1-139">Sallitaanko kululuokalle muita maksutapoja?</span><span class="sxs-lookup"><span data-stu-id="868d1-139">Are additional payment methods allowed for the expense category?</span></span> <span data-ttu-id="868d1-140">Jos sallitaan, mitä ne ovat?</span><span class="sxs-lookup"><span data-stu-id="868d1-140">If so, what are they?</span></span>
- <span data-ttu-id="868d1-141">Onko kululuokassa aliluokkia?</span><span class="sxs-lookup"><span data-stu-id="868d1-141">Are there subcategories in this expense category?</span></span> <span data-ttu-id="868d1-142">Jos aliluokkia on, on tehtävä myös seuraavat päätökset:</span><span class="sxs-lookup"><span data-stu-id="868d1-142">If there are subcategories, you must also make the following decisions:</span></span>

    - <span data-ttu-id="868d1-143">Jätetäänkö jotkin aliluokat pois veronpalautuksesta?</span><span class="sxs-lookup"><span data-stu-id="868d1-143">Are any of the subcategories excluded from tax recovery?</span></span>
    - <span data-ttu-id="868d1-144">Mikä on aliluokkien nimikkeen arvonlisäveroryhmä?</span><span class="sxs-lookup"><span data-stu-id="868d1-144">What is the item sales tax group of the subcategories?</span></span>
