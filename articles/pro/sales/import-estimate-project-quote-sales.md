---
title: Projektiarvioiden tuonti projektipohjaiselle tarjousriville
description: Tässä aiheessa on tietoja siitä, miten projektin arviot tuodaan tarjousriville.
author: rumant
manager: Annbe
ms.date: 10/09/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 224c2265cfcc38dfc2ed74664d38c095feefaca7
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/16/2020
ms.locfileid: "4075250"
---
# <a name="importing-estimates-for-a-project-to-a-project-based-quote-line"></a><span data-ttu-id="dd2f0-103">Projektiarvioiden tuonti projektipohjaiselle tarjousriville</span><span class="sxs-lookup"><span data-stu-id="dd2f0-103">Importing estimates for a project to a project-based quote line</span></span>

<span data-ttu-id="dd2f0-104">_**Käytetään:** Lite-käyttöönotto – kauppa proformalaskutukseen_</span><span class="sxs-lookup"><span data-stu-id="dd2f0-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="dd2f0-105">Jos projekti luodaan myyntiä edeltävän vaiheen aikana, voit valita, tuodaanko taloudellinen arvio projektista projektipohjaiselle tarjousriville.</span><span class="sxs-lookup"><span data-stu-id="dd2f0-105">If a project is created during the pre-sales stage, you can select to import the financial estimate from the project to the project-based quote line.</span></span>

1. <span data-ttu-id="dd2f0-106">Varmista, että projektipohjaisella tarjousrivillä on projektin tiedot **Projekti** -kentässä.</span><span class="sxs-lookup"><span data-stu-id="dd2f0-106">Make sure that the project-based quote line has the project information in the **Project** field.</span></span>
2. <span data-ttu-id="dd2f0-107">Valitse **Tarjousrivin tiedot** -välilehdessä **Tuo projektiarviosta**.</span><span class="sxs-lookup"><span data-stu-id="dd2f0-107">On the **Quote line details** tab, select **Import from Project Estimation**.</span></span>
3. <span data-ttu-id="dd2f0-108">Valitse avautuvassa valintaikkunasivussa jokin seuraavista yhteenvetovaihtoehdoista.</span><span class="sxs-lookup"><span data-stu-id="dd2f0-108">On the dialog page opens, select one of the following summarization options.</span></span>

  - <span data-ttu-id="dd2f0-109">**Tapahtumaluokka**</span><span class="sxs-lookup"><span data-stu-id="dd2f0-109">**Transaction class**</span></span>
  - <span data-ttu-id="dd2f0-110">**Luokka**</span><span class="sxs-lookup"><span data-stu-id="dd2f0-110">**Category**</span></span>
  - <span data-ttu-id="dd2f0-111">**Rooli**</span><span class="sxs-lookup"><span data-stu-id="dd2f0-111">**Role**</span></span> 
  - <span data-ttu-id="dd2f0-112">**Projektitehtävä**</span><span class="sxs-lookup"><span data-stu-id="dd2f0-112">**Project task**</span></span>

<span data-ttu-id="dd2f0-113">Valinnan perusteella kopioidaan projektista kaikkien tähän tarjousriviin sisältyvien tapahtumaluokkien arvio.</span><span class="sxs-lookup"><span data-stu-id="dd2f0-113">Based on your selection, the estimate from the project for all transaction classes included on this quote line are copied over.</span></span> <span data-ttu-id="dd2f0-114">Jos haluat tarkistaa, mitä tapahtumaluokkia on mukana, valitse projektipohjaisen tarjousrivin **Yleiset** -välilehti ja tarkista arvot **Sisällytä aika** , **Sisällytä kulut** ja **Sisällytä maksut**.</span><span class="sxs-lookup"><span data-stu-id="dd2f0-114">To check what transaction classes are included, select the **General** tab on the project-based quote line, and check the values for **Include Time** , **Include Expenses** , and **Include Fees**.</span></span>  <span data-ttu-id="dd2f0-115">Voit tarkistaa sisällytettävät tehtävät valitsemalla tarjousriviltä **laskutettavat tehtävät** -välilehden.</span><span class="sxs-lookup"><span data-stu-id="dd2f0-115">To check what tasks are included, select the **Chargeable Tasks** tab on the quote line.</span></span>

<span data-ttu-id="dd2f0-116">Näiden tehtävien ja tapahtumaluokkien yhdistelmien arviot tuodaan tarjousriviin sen mukaan, mitä tehtäviä liittyy.</span><span class="sxs-lookup"><span data-stu-id="dd2f0-116">Depending on the Tasks associated and Included transaction classes, the estimates for those task and transaction class combinations are imported to the quote line.</span></span>

<span data-ttu-id="dd2f0-117">Kun tuot arvioita, järjestelmä määrittää hinnoittelun oletusarvon tarjoukseen liitettyjen projektihinnastojen ja projektipohjaisen tarjousrivin laskutustyypin perusteella.</span><span class="sxs-lookup"><span data-stu-id="dd2f0-117">When you import estimates, the system will default the pricing based on the project price lists attached to the quote and the billing type set up on the project-based quote line.</span></span> <span data-ttu-id="dd2f0-118">Jos projektipohjaiseen tarjousriviin on määritetty tehtävä, rooli tai luokka ei-laskutettavana, tuodun arviorivin arvoksi tulee ei-laskutettava eikä sitä lasketa mukaan tarjousrivin tarjotun arvon kanssa.</span><span class="sxs-lookup"><span data-stu-id="dd2f0-118">If a task, role, or category is set up on the project-based quote line as non-chargeable, the imported estimate line will set as non-chargeable and won't add up to the quoted value of quote line.</span></span>

<span data-ttu-id="dd2f0-119">Kun tarjousrivillä on rivitiedot, tarjousrivin **Tarjouksen arvo** - ja **Arvioitu vero** -kentät on lasketaan yhteen, eikä niitä voi muokata.</span><span class="sxs-lookup"><span data-stu-id="dd2f0-119">When a quote line has line details, the **Quote Value** and the **Estimated Tax** fields on the quote line are summarized and can't be edited.</span></span>

<span data-ttu-id="dd2f0-120">Kun useita summausasetuksia valitaan, järjestelmä yrittää laskea yhteen kaikkien valittujen vaihtoehtojen mukaan.</span><span class="sxs-lookup"><span data-stu-id="dd2f0-120">When multiple summarization options are selected, the system attempts to summarize by all selected options.</span></span> <span data-ttu-id="dd2f0-121">Tuloksena on, että tuotujen tarjousrivien tulos on suurempi kuin jos valitsit vain yhden summausasetuksen.</span><span class="sxs-lookup"><span data-stu-id="dd2f0-121">The result is that the output of imported quote lines will be more than if you selected only one summarization option.</span></span>

<span data-ttu-id="dd2f0-122">Jos projektilla oli esimerkiksi seuraavat arviorivit kuluja varten.</span><span class="sxs-lookup"><span data-stu-id="dd2f0-122">For example, if the project had the following estimate lines for expenses.</span></span>

| <span data-ttu-id="dd2f0-123">Tehtävä</span><span class="sxs-lookup"><span data-stu-id="dd2f0-123">Task</span></span> | <span data-ttu-id="dd2f0-124">Luokka</span><span class="sxs-lookup"><span data-stu-id="dd2f0-124">Category</span></span> | <span data-ttu-id="dd2f0-125">Päivämäärä</span><span class="sxs-lookup"><span data-stu-id="dd2f0-125">Date</span></span> | <span data-ttu-id="dd2f0-126">Määrä</span><span class="sxs-lookup"><span data-stu-id="dd2f0-126">Quantity</span></span> | <span data-ttu-id="dd2f0-127">Yksikköhinta</span><span class="sxs-lookup"><span data-stu-id="dd2f0-127">Unit price</span></span> | <span data-ttu-id="dd2f0-128">Summa</span><span class="sxs-lookup"><span data-stu-id="dd2f0-128">Amount</span></span> |
| --- | --- | --- | --- | --- | --- |
| <span data-ttu-id="dd2f0-129">Tehtävä A</span><span class="sxs-lookup"><span data-stu-id="dd2f0-129">Task A</span></span> | <span data-ttu-id="dd2f0-130">Lentoliput</span><span class="sxs-lookup"><span data-stu-id="dd2f0-130">Airfare</span></span> | <span data-ttu-id="dd2f0-131">1.10.2020</span><span class="sxs-lookup"><span data-stu-id="dd2f0-131">10/1/2020</span></span> | <span data-ttu-id="dd2f0-132">4</span><span class="sxs-lookup"><span data-stu-id="dd2f0-132">4</span></span> | <span data-ttu-id="dd2f0-133">400</span><span class="sxs-lookup"><span data-stu-id="dd2f0-133">400</span></span> | <span data-ttu-id="dd2f0-134">1600</span><span class="sxs-lookup"><span data-stu-id="dd2f0-134">1600</span></span> |
| <span data-ttu-id="dd2f0-135">Tehtävä B</span><span class="sxs-lookup"><span data-stu-id="dd2f0-135">Task B</span></span> | <span data-ttu-id="dd2f0-136">Hotelli</span><span class="sxs-lookup"><span data-stu-id="dd2f0-136">Hotel</span></span> | <span data-ttu-id="dd2f0-137">1.10.2020</span><span class="sxs-lookup"><span data-stu-id="dd2f0-137">10/1/2020</span></span> | <span data-ttu-id="dd2f0-138">4</span><span class="sxs-lookup"><span data-stu-id="dd2f0-138">4</span></span> | <span data-ttu-id="dd2f0-139">200</span><span class="sxs-lookup"><span data-stu-id="dd2f0-139">200</span></span> | <span data-ttu-id="dd2f0-140">800</span><span class="sxs-lookup"><span data-stu-id="dd2f0-140">800</span></span> |
| <span data-ttu-id="dd2f0-141">Tehtävä C</span><span class="sxs-lookup"><span data-stu-id="dd2f0-141">Task C</span></span> | <span data-ttu-id="dd2f0-142">Hotelli</span><span class="sxs-lookup"><span data-stu-id="dd2f0-142">Hotel</span></span> | <span data-ttu-id="dd2f0-143">1.11.2020</span><span class="sxs-lookup"><span data-stu-id="dd2f0-143">11/1/2020</span></span> | <span data-ttu-id="dd2f0-144">2</span><span class="sxs-lookup"><span data-stu-id="dd2f0-144">2</span></span> | <span data-ttu-id="dd2f0-145">200</span><span class="sxs-lookup"><span data-stu-id="dd2f0-145">200</span></span> | <span data-ttu-id="dd2f0-146">400</span><span class="sxs-lookup"><span data-stu-id="dd2f0-146">400</span></span> |

<span data-ttu-id="dd2f0-147">Kun käyttäjä valitsee summauksen tapahtumaluokan mukaan, seuraavat tiedot tuodaan.</span><span class="sxs-lookup"><span data-stu-id="dd2f0-147">When the user selects to summarize by Transaction class, the following information will be imported.</span></span>

| <span data-ttu-id="dd2f0-148">Tehtävä</span><span class="sxs-lookup"><span data-stu-id="dd2f0-148">Task</span></span> | <span data-ttu-id="dd2f0-149">Luokka</span><span class="sxs-lookup"><span data-stu-id="dd2f0-149">Category</span></span> | <span data-ttu-id="dd2f0-150">Päivä</span><span class="sxs-lookup"><span data-stu-id="dd2f0-150">Date</span></span> | <span data-ttu-id="dd2f0-151">Määrä</span><span class="sxs-lookup"><span data-stu-id="dd2f0-151">Quantity</span></span> | <span data-ttu-id="dd2f0-152">Yksikköhinta</span><span class="sxs-lookup"><span data-stu-id="dd2f0-152">Unit price</span></span> | <span data-ttu-id="dd2f0-153">Summa</span><span class="sxs-lookup"><span data-stu-id="dd2f0-153">Amount</span></span> |
| --- | --- | --- | --- | --- | --- |
|||<span data-ttu-id="dd2f0-154">1.10.2020</span><span class="sxs-lookup"><span data-stu-id="dd2f0-154">10/1/2020</span></span> | <span data-ttu-id="dd2f0-155">3.34</span><span class="sxs-lookup"><span data-stu-id="dd2f0-155">3.34</span></span> | <span data-ttu-id="dd2f0-156">840</span><span class="sxs-lookup"><span data-stu-id="dd2f0-156">840</span></span> | <span data-ttu-id="dd2f0-157">2800</span><span class="sxs-lookup"><span data-stu-id="dd2f0-157">2800</span></span> |

<span data-ttu-id="dd2f0-158">Kun käyttäjä valitsee summauksen tapahtumaluokan ja luokan mukaan, seuraavat tiedot tuodaan.</span><span class="sxs-lookup"><span data-stu-id="dd2f0-158">When the user selects to summarize by Transaction class and Category, the following information will be imported.</span></span>

| <span data-ttu-id="dd2f0-159">Tehtävä</span><span class="sxs-lookup"><span data-stu-id="dd2f0-159">Task</span></span> | <span data-ttu-id="dd2f0-160">Luokka</span><span class="sxs-lookup"><span data-stu-id="dd2f0-160">Category</span></span> | <span data-ttu-id="dd2f0-161">Päivä</span><span class="sxs-lookup"><span data-stu-id="dd2f0-161">Date</span></span> | <span data-ttu-id="dd2f0-162">Määrä</span><span class="sxs-lookup"><span data-stu-id="dd2f0-162">Quantity</span></span> | <span data-ttu-id="dd2f0-163">Yksikköhinta</span><span class="sxs-lookup"><span data-stu-id="dd2f0-163">Unit price</span></span> | <span data-ttu-id="dd2f0-164">Summa</span><span class="sxs-lookup"><span data-stu-id="dd2f0-164">Amount</span></span> |
| --- | --- | --- | --- | --- | --- |
| <span data-ttu-id="dd2f0-165">Tehtävä A</span><span class="sxs-lookup"><span data-stu-id="dd2f0-165">Task A</span></span> | <span data-ttu-id="dd2f0-166">Lentoliput</span><span class="sxs-lookup"><span data-stu-id="dd2f0-166">Airfare</span></span> | <span data-ttu-id="dd2f0-167">1.10.2020</span><span class="sxs-lookup"><span data-stu-id="dd2f0-167">10/1/2020</span></span> | <span data-ttu-id="dd2f0-168">4</span><span class="sxs-lookup"><span data-stu-id="dd2f0-168">4</span></span> | <span data-ttu-id="dd2f0-169">400</span><span class="sxs-lookup"><span data-stu-id="dd2f0-169">400</span></span> | <span data-ttu-id="dd2f0-170">1600</span><span class="sxs-lookup"><span data-stu-id="dd2f0-170">1600</span></span> |
| | <span data-ttu-id="dd2f0-171">Hotelli</span><span class="sxs-lookup"><span data-stu-id="dd2f0-171">Hotel</span></span> | <span data-ttu-id="dd2f0-172">1.10.2020</span><span class="sxs-lookup"><span data-stu-id="dd2f0-172">10/1/2020</span></span> | <span data-ttu-id="dd2f0-173">6</span><span class="sxs-lookup"><span data-stu-id="dd2f0-173">6</span></span> | <span data-ttu-id="dd2f0-174">200</span><span class="sxs-lookup"><span data-stu-id="dd2f0-174">200</span></span> | <span data-ttu-id="dd2f0-175">1200</span><span class="sxs-lookup"><span data-stu-id="dd2f0-175">1200</span></span> |

<span data-ttu-id="dd2f0-176">Kun käyttäjä valitsee summauksen tapahtumaluokan, luokan ja lehtisolmutehtävän mukaan, seuraavat tiedot tuodaan.</span><span class="sxs-lookup"><span data-stu-id="dd2f0-176">When the user selects to summarize by Transaction class, Category and Leaf Node Task, the following information will be imported.</span></span> <span data-ttu-id="dd2f0-177">Huomaa, että tämä tulos on sama kuin mitä projektissa oli.</span><span class="sxs-lookup"><span data-stu-id="dd2f0-177">Notice that this result is the same as what was on the project.</span></span>

| <span data-ttu-id="dd2f0-178">Tehtävä</span><span class="sxs-lookup"><span data-stu-id="dd2f0-178">Task</span></span> | <span data-ttu-id="dd2f0-179">Luokka</span><span class="sxs-lookup"><span data-stu-id="dd2f0-179">Category</span></span> | <span data-ttu-id="dd2f0-180">Päivä</span><span class="sxs-lookup"><span data-stu-id="dd2f0-180">Date</span></span> | <span data-ttu-id="dd2f0-181">Määrä</span><span class="sxs-lookup"><span data-stu-id="dd2f0-181">Quantity</span></span> | <span data-ttu-id="dd2f0-182">Yksikköhinta</span><span class="sxs-lookup"><span data-stu-id="dd2f0-182">Unit price</span></span> | <span data-ttu-id="dd2f0-183">Summa</span><span class="sxs-lookup"><span data-stu-id="dd2f0-183">Amount</span></span> |
| --- | --- | --- | --- | --- | --- |
| <span data-ttu-id="dd2f0-184">Tehtävä A</span><span class="sxs-lookup"><span data-stu-id="dd2f0-184">Task A</span></span> | <span data-ttu-id="dd2f0-185">Lentoliput</span><span class="sxs-lookup"><span data-stu-id="dd2f0-185">Airfare</span></span> | <span data-ttu-id="dd2f0-186">1.10.2020</span><span class="sxs-lookup"><span data-stu-id="dd2f0-186">10/1/2020</span></span> | <span data-ttu-id="dd2f0-187">4</span><span class="sxs-lookup"><span data-stu-id="dd2f0-187">4</span></span> | <span data-ttu-id="dd2f0-188">400</span><span class="sxs-lookup"><span data-stu-id="dd2f0-188">400</span></span> | <span data-ttu-id="dd2f0-189">1600</span><span class="sxs-lookup"><span data-stu-id="dd2f0-189">1600</span></span> |
| <span data-ttu-id="dd2f0-190">Tehtävä B</span><span class="sxs-lookup"><span data-stu-id="dd2f0-190">Task B</span></span> | <span data-ttu-id="dd2f0-191">Hotelli</span><span class="sxs-lookup"><span data-stu-id="dd2f0-191">Hotel</span></span> | <span data-ttu-id="dd2f0-192">1.10.2020</span><span class="sxs-lookup"><span data-stu-id="dd2f0-192">10/1/2020</span></span> | <span data-ttu-id="dd2f0-193">4</span><span class="sxs-lookup"><span data-stu-id="dd2f0-193">4</span></span> | <span data-ttu-id="dd2f0-194">200</span><span class="sxs-lookup"><span data-stu-id="dd2f0-194">200</span></span> | <span data-ttu-id="dd2f0-195">800</span><span class="sxs-lookup"><span data-stu-id="dd2f0-195">800</span></span> |
| <span data-ttu-id="dd2f0-196">Tehtävä C</span><span class="sxs-lookup"><span data-stu-id="dd2f0-196">Task C</span></span> | <span data-ttu-id="dd2f0-197">Hotelli</span><span class="sxs-lookup"><span data-stu-id="dd2f0-197">Hotel</span></span> | <span data-ttu-id="dd2f0-198">1.11.2020</span><span class="sxs-lookup"><span data-stu-id="dd2f0-198">11/1/2020</span></span> | <span data-ttu-id="dd2f0-199">2</span><span class="sxs-lookup"><span data-stu-id="dd2f0-199">2</span></span> | <span data-ttu-id="dd2f0-200">200</span><span class="sxs-lookup"><span data-stu-id="dd2f0-200">200</span></span> | <span data-ttu-id="dd2f0-201">400</span><span class="sxs-lookup"><span data-stu-id="dd2f0-201">400</span></span> |