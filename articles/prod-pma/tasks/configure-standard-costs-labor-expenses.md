---
title: Työn ja kulujen vakiokustannusten määrittäminen
description: Tässä aiheessa kerrotaan, miten projektin työn ja kulujen vakiokustannukset määritetään.
author: Yowelle
ms.date: 08/02/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ProjCostPriceHour, ProjSalesPriceHour, ProjCostPriceExpense, ProjSalesPriceCost
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 517e5ae776cff18aec81e5446a7aaedfba61ac0c
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/10/2021
ms.locfileid: "6011007"
---
# <a name="configure-standard-costs-for-labor-and-expenses"></a><span data-ttu-id="75c1a-103">Työn ja kulujen vakiokustannusten määrittäminen</span><span class="sxs-lookup"><span data-stu-id="75c1a-103">Configure standard costs for labor and expenses</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="75c1a-104">Tässä aiheessa kerrotaan, miten projektin työn ja kulujen vakiokustannukset määritetään.</span><span class="sxs-lookup"><span data-stu-id="75c1a-104">This topic explains how to set up standard costs for labor and expenses for a project.</span></span> <span data-ttu-id="75c1a-105">Tämä tehtävä käyttää USSI-tietojoukkoa.</span><span class="sxs-lookup"><span data-stu-id="75c1a-105">This task uses the USSI data set.</span></span>

1. <span data-ttu-id="75c1a-106">Valitse siirtymisruudussa **Moduulit > Projektinhallinta ja kirjanpito > Määritys > Hinnat > Kustannushinta (tunti)**.</span><span class="sxs-lookup"><span data-stu-id="75c1a-106">In the navigation pane, go to **Modules > Project management and accounting > Setup > Prices > Cost price (hour)**.</span></span>
2. <span data-ttu-id="75c1a-107">Valitse **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="75c1a-107">Select **New**.</span></span>
3. <span data-ttu-id="75c1a-108">Kirjoita päivämäärä **Voimaantulopäivä**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="75c1a-108">In the **Effective date** field, enter a date.</span></span>
4. <span data-ttu-id="75c1a-109">Kirjoita **Kustannushinta**-kenttään numero.</span><span class="sxs-lookup"><span data-stu-id="75c1a-109">In the **Cost price** field, enter a number.</span></span> <span data-ttu-id="75c1a-110">Voit määrittää projektiluokalle vakiokustannushinnan tai voit määrittää kustannushinnan työntekijänumeron, projektinumeron, luokan, päivämäärän tai näiden yhdistelmän perusteella.</span><span class="sxs-lookup"><span data-stu-id="75c1a-110">You can set up a standard cost price for the project category, or you can set up a cost price by worker number, project number, category, date, or any combination of these.</span></span> <span data-ttu-id="75c1a-111">Käytettävä kustannushinta on kustannushinta, joka on yksityiskohtaisin.</span><span class="sxs-lookup"><span data-stu-id="75c1a-111">The cost price that is applied is the cost price with the highest level of detail.</span></span>  
5. <span data-ttu-id="75c1a-112">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="75c1a-112">Select **Save**.</span></span>
6. <span data-ttu-id="75c1a-113">Valitse siirtymisruudussa **Moduulit > Projektinhallinta ja kirjanpito > Määritys > Hinnat > Myyntihinta (tunti)**.</span><span class="sxs-lookup"><span data-stu-id="75c1a-113">In the navigation pane, go to **Modules > Project management and accounting > Setup > Prices > Sales price (hour)**.</span></span>
7. <span data-ttu-id="75c1a-114">Valitse **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="75c1a-114">Select **New**.</span></span>
8. <span data-ttu-id="75c1a-115">Kirjoita päivämäärä **Voimaantulopäivä**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="75c1a-115">In the **Effective date** field, enter a date.</span></span>
9. <span data-ttu-id="75c1a-116">Valitse vaihtoehto **Voimassa**-kentässä.</span><span class="sxs-lookup"><span data-stu-id="75c1a-116">In the **Valid for** field, select an option.</span></span>
10. <span data-ttu-id="75c1a-117">Kirjoita **Hinnoittelu**-kenttään numero.</span><span class="sxs-lookup"><span data-stu-id="75c1a-117">In the **Pricing** field, enter a number.</span></span> <span data-ttu-id="75c1a-118">Voit määrittää vakiomyyntihinnan tuntitapahtumille tai projektiluokalle.</span><span class="sxs-lookup"><span data-stu-id="75c1a-118">You can set up a standard sales price for hour transactions or for a project category.</span></span> <span data-ttu-id="75c1a-119">Voit myös määrittää myyntihinnat työntekijänumeron, projektinumeron, luokan, tapahtumapäivän tai minkä tahansa näiden yhdistelmän mukaan.</span><span class="sxs-lookup"><span data-stu-id="75c1a-119">You can also set up sales prices by worker number, project number, category, transaction date, or any combination of these.</span></span> <span data-ttu-id="75c1a-120">Todellinen myyntihinta, jota käytetään, kun työntekijä syöttää tapahtuman tuntikirjauskansioon, on myyntihinta, joka on yksityiskohtaisin.</span><span class="sxs-lookup"><span data-stu-id="75c1a-120">The actual sales price, which is applied when a worker enters a transaction in the Hour journal, is the sales price with the highest level of detail.</span></span> <span data-ttu-id="75c1a-121">Jos esimerkiksi sekä yleinen myyntihinta että työntekijäkohtainen myyntihinta on määritetty, käytetään työntekijäkohtaista myyntihintaa.</span><span class="sxs-lookup"><span data-stu-id="75c1a-121">For example, if both a general sales price and a worker-specific sales price are set up, the worker-specific sales price is used.</span></span>  
11. <span data-ttu-id="75c1a-122">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="75c1a-122">Select **Save**.</span></span>
12. <span data-ttu-id="75c1a-123">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="75c1a-123">Close the page.</span></span>
13. <span data-ttu-id="75c1a-124">Valitse siirtymisruudussa **Moduulit > Projektinhallinta ja kirjanpito > Määritys > Hinnat > Kustannushinta (kulu)**.</span><span class="sxs-lookup"><span data-stu-id="75c1a-124">In the navigation pane, go to **Modules > Project management and accounting > Setup > Prices > Cost price (expense)**.</span></span>
14. <span data-ttu-id="75c1a-125">Valitse **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="75c1a-125">Select **New**.</span></span>
15. <span data-ttu-id="75c1a-126">Kirjoita päivämäärä **Voimaantulopäivä**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="75c1a-126">In the **Effective date** field, enter a date.</span></span>
16. <span data-ttu-id="75c1a-127">Kirjoita **Kustannushinta**-kenttään numero.</span><span class="sxs-lookup"><span data-stu-id="75c1a-127">In the **Cost price** field, enter a number.</span></span> <span data-ttu-id="75c1a-128">Useita kenttiä voidaan täyttää, mutta tämä on tietueen tallentamiseen tarvittava vähimmäismäärä.</span><span class="sxs-lookup"><span data-stu-id="75c1a-128">Multiple fields can be filled in, but this is the minimum needed to save the record.</span></span>  
17. <span data-ttu-id="75c1a-129">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="75c1a-129">Select **Save**.</span></span>
18. <span data-ttu-id="75c1a-130">Valitse siirtymisruudussa **Moduulit > Projektinhallinta ja kirjanpito > Määritys > Hinnat > Myyntihinta (kulu)**.</span><span class="sxs-lookup"><span data-stu-id="75c1a-130">In the navigation pane, go to **Modules > Project management and accounting > Setup > Prices > Sales price (expense)**.</span></span>
19. <span data-ttu-id="75c1a-131">Valitse **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="75c1a-131">Select **New**.</span></span>
20. <span data-ttu-id="75c1a-132">Kirjoita päivämäärä **Voimaantulopäivä**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="75c1a-132">In the **Effective date** field, enter a date.</span></span>
21. <span data-ttu-id="75c1a-133">Valitse vaihtoehto **Voimassa**-kentässä.</span><span class="sxs-lookup"><span data-stu-id="75c1a-133">In the **Valid for** field, select an option.</span></span>
22. <span data-ttu-id="75c1a-134">Kirjoita **Hinnoittelu**-kenttään numero.</span><span class="sxs-lookup"><span data-stu-id="75c1a-134">In the **Pricing** field, enter a number.</span></span> <span data-ttu-id="75c1a-135">Todellinen myyntihinta, jota käytetään, kun työntekijä syöttää tapahtumat kulukirjauskansioon, on myyntihinta, joka on yksityiskohtaisin.</span><span class="sxs-lookup"><span data-stu-id="75c1a-135">The actual sales price, which is applied when a worker enters transactions in an expense journal, is the sales price with the highest level of detail.</span></span> <span data-ttu-id="75c1a-136">Jos esimerkiksi sekä yleinen että työntekijäkohtainen myyntihinta on määritetty, käytetään työntekijäkohtaista myyntihintaa.</span><span class="sxs-lookup"><span data-stu-id="75c1a-136">For example, if both a general and a worker-specific sales price are set up, the worker-specific sales price is used.</span></span>  
23. <span data-ttu-id="75c1a-137">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="75c1a-137">Select **Save**.</span></span>



[!INCLUDE[footer-include](../../includes/footer-banner.md)]