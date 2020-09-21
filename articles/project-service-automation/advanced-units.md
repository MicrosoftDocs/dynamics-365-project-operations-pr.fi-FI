---
title: Yksikköryhmät ja yksiköt
description: Tässä aiheessa on tietoja yksikköryhmistä ja yksiköistä.
author: rumant
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/05/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: b5422be3-5bfc-4ee2-b19a-4eca68813ff2
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: fc2dde2d9471f8585c190a65f3ad9b32de75af86
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/24/2020
ms.locfileid: "3751278"
---
# <a name="unit-groups-and-units"></a><span data-ttu-id="d597c-103">Yksikköryhmät ja yksiköt</span><span class="sxs-lookup"><span data-stu-id="d597c-103">Unit groups and units</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="d597c-104">Yksikköryhmät ja yksiköt Microsoft Dynamics 365:n perusentiteettejä.</span><span class="sxs-lookup"><span data-stu-id="d597c-104">Unit groups and units are basic entities in Microsoft Dynamics 365.</span></span> <span data-ttu-id="d597c-105">Yksikkö on yksittäinen mittayksikkö ja useita yksikköjä voidaan ryhmitellä yksikköryhmiksi.</span><span class="sxs-lookup"><span data-stu-id="d597c-105">A unit is a single unit of measure, and multiple units can be grouped into unit groups.</span></span> <span data-ttu-id="d597c-106">Yksikköryhmää kutsutaan joskus yksikköaikatauluksi Dynamics 365:n käyttöliittymässä (UI).</span><span class="sxs-lookup"><span data-stu-id="d597c-106">A unit group is sometimes referred to as a unit schedule in the Dynamics 365 user interface (UI).</span></span> 

<span data-ttu-id="d597c-107">Seuraavassa on esimerkkejä yksiköistä ja yksikköryhmistä:</span><span class="sxs-lookup"><span data-stu-id="d597c-107">Here are some examples of units and unit groups:</span></span>
 
- <span data-ttu-id="d597c-108">**Yksikköryhmä**: Etäisyys</span><span class="sxs-lookup"><span data-stu-id="d597c-108">**Unit group**: Distance</span></span> 
    - <span data-ttu-id="d597c-109">**Yksiköt**: Maili, Kilometri jne.</span><span class="sxs-lookup"><span data-stu-id="d597c-109">**Units**: Mile, Kilometer, and so on.</span></span>
- <span data-ttu-id="d597c-110">**Yksikköryhmä**: Aika</span><span class="sxs-lookup"><span data-stu-id="d597c-110">**Unit group**: Time</span></span>
    - <span data-ttu-id="d597c-111">**Yksiköt**: Tunti, Päivä, Viikko jne.</span><span class="sxs-lookup"><span data-stu-id="d597c-111">**Units**: Hour, day, week, and so on.</span></span> 

<span data-ttu-id="d597c-112">Kun useita yksikköjä määritetään yksikköryhmäksi, niiden välille on myös määritettävä muuntokerroin määrittämällä ensimmäinen määritettävä yksikkö yksikköryhmän oletusyksiköksi tai ensisijaiseksi yksiköksi.</span><span class="sxs-lookup"><span data-stu-id="d597c-112">When you set up multiple units in a unit group, you must also set up a conversion factor between them by designating the first unit that you set up as the default or primary unit for the unit group.</span></span> 

<span data-ttu-id="d597c-113">Jos esimerkiksi **Aika**-yksikköryhmässä ensimmäisenä yksikkönä määritetään **Tunti**, järjestelmä määrittää yksikön **Tunti** oletusyksiköksi.</span><span class="sxs-lookup"><span data-stu-id="d597c-113">For example, in a **Time** unit group, if you set up **Hour** as the first unit, the system designates **Hour** as the default unit.</span></span> <span data-ttu-id="d597c-114">Jos seuraavana yksikkönä määritetään **Päivä**, on määritettävä muuntokerroin yksikköjen **Päivä** ja **Tunti** välille.</span><span class="sxs-lookup"><span data-stu-id="d597c-114">If the next unit that you set up is **Day**, you must set up a conversion factor for **Day** to **Hour**.</span></span> <span data-ttu-id="d597c-115">Jos sitten kolmantena yksikkönä määritetään **Viikko**, on määritettävä muuntokerroin yksikköjen **Viikko** ja joko **Päivä** tai **Tunti** välille.</span><span class="sxs-lookup"><span data-stu-id="d597c-115">If you then add **Week** as a third unit, you must set up a conversion factor for **Week** in terms of **Day** or **Hour**.</span></span> 

<span data-ttu-id="d597c-116">Seuraavassa kuvassa esitetään esimerkkimääritys yksikölle **Päivä**, jossa **Määrä**-kentässä näkyy päivässä olevien tuntien määrä, ja yksikölle **Viikko**, jossa **Määrä**-kentässä näkyy viikossa olevien päivien määrä.</span><span class="sxs-lookup"><span data-stu-id="d597c-116">The following image shows an example setup for the **Day** unit, where the **Quantity** field shows the number of hours that are in a day, and **Week**, where the **Quantity** field show the number of days that are in a week.</span></span>

> ![Yksikköryhmä: tietosivu](media/advanced-2.png)

## <a name="using-units-and-unit-groups"></a><span data-ttu-id="d597c-118">Yksikköjen ja yksikköryhmien käyttö</span><span class="sxs-lookup"><span data-stu-id="d597c-118">Using units and unit groups</span></span>

<span data-ttu-id="d597c-119">Dynamics 365 Project Service Automation käyttää yksikköjä ja yksikköryhmiä käsitelläkseen sekä kulujen että ajan arvioiden ja merkintöjen käsittelyyn.</span><span class="sxs-lookup"><span data-stu-id="d597c-119">Dynamics 365 Project Service Automation uses units and unit groups to process estimates and entries for both expenses and time.</span></span> 

<span data-ttu-id="d597c-120">Kulujen osalta kullakin kululuokalla on oletusarvoinen yksikköryhmänsä ja yksikkönsä.</span><span class="sxs-lookup"><span data-stu-id="d597c-120">For expenses, each expense category has a default unit group and unit.</span></span> <span data-ttu-id="d597c-121">Nämä arvot otetaan oletusarvoiksi kululuokkien hinnastomerkinnöille.</span><span class="sxs-lookup"><span data-stu-id="d597c-121">These values are entered as default values on price list entries for expense categories.</span></span> 

<span data-ttu-id="d597c-122">Sinulla voi olla esimerkiksi **Kilometrikorvaus**-niminen kululuokka.</span><span class="sxs-lookup"><span data-stu-id="d597c-122">For example, you have an expense category that is named **Mileage**.</span></span> <span data-ttu-id="d597c-123">Sillä on **Etäisyys**-niminen yksikköryhmä ja oletusyksikkö nimeltä **Maili**.</span><span class="sxs-lookup"><span data-stu-id="d597c-123">It has a unit group that is named **Distance** and a default unit that is named **Mile**.</span></span> <span data-ttu-id="d597c-124">Jos määrität **Etäisyys**-yksikköryhmän siten, että siinä on kaksi yksikköä (**Maili** ja **Kilometri**), voit määrittää yhden hinnaston **Kilometrikorvaus**-luokalle kaksi hintaa: mailikohtainen hinta ja kilometrikohtainen hinta.</span><span class="sxs-lookup"><span data-stu-id="d597c-124">If you set up the **Distance** unit group so that it has two units (**Mile** and **Kilometer**), you can set two prices for the **Mileage** category on one price list: price per mile and price per kilometer.</span></span>

| <span data-ttu-id="d597c-125">Kululuokka</span><span class="sxs-lookup"><span data-stu-id="d597c-125">Expense category</span></span>  | <span data-ttu-id="d597c-126">Yksikköryhmä</span><span class="sxs-lookup"><span data-stu-id="d597c-126">Unit group</span></span>  | <span data-ttu-id="d597c-127">Yksikkö</span><span class="sxs-lookup"><span data-stu-id="d597c-127">Unit</span></span>      | <span data-ttu-id="d597c-128">Hinnoittelutapa</span><span class="sxs-lookup"><span data-stu-id="d597c-128">Pricing method</span></span>  | <span data-ttu-id="d597c-129">Yksikköhinta</span><span class="sxs-lookup"><span data-stu-id="d597c-129">Price per unit</span></span>  |
|-------------------|---------------|-----------|-------------------|-------------------|
| <span data-ttu-id="d597c-130">Kilometrikorvaus</span><span class="sxs-lookup"><span data-stu-id="d597c-130">Mileage</span></span>           | <span data-ttu-id="d597c-131">Etäisyys</span><span class="sxs-lookup"><span data-stu-id="d597c-131">Distance</span></span>      | <span data-ttu-id="d597c-132">Maili</span><span class="sxs-lookup"><span data-stu-id="d597c-132">Mile</span></span>      | <span data-ttu-id="d597c-133">Yksikköhinta</span><span class="sxs-lookup"><span data-stu-id="d597c-133">Price per unit</span></span>    | <span data-ttu-id="d597c-134">10 USD</span><span class="sxs-lookup"><span data-stu-id="d597c-134">10 USD</span></span>            |
| <span data-ttu-id="d597c-135">Kilometrikorvaus</span><span class="sxs-lookup"><span data-stu-id="d597c-135">Mileage</span></span>           | <span data-ttu-id="d597c-136">Etäisyys</span><span class="sxs-lookup"><span data-stu-id="d597c-136">Distance</span></span>      | <span data-ttu-id="d597c-137">Kilometri</span><span class="sxs-lookup"><span data-stu-id="d597c-137">Kilometer</span></span> | <span data-ttu-id="d597c-138">Yksikköhinta</span><span class="sxs-lookup"><span data-stu-id="d597c-138">Price per unit</span></span>    |  <span data-ttu-id="d597c-139">6 USD</span><span class="sxs-lookup"><span data-stu-id="d597c-139">6 USD</span></span>            |

<span data-ttu-id="d597c-140">Kun lisäät projektiin kulun, järjestelmä määrittää hinnan kyseisen kulun luokan ja yksikön yhdistelmän perusteella.</span><span class="sxs-lookup"><span data-stu-id="d597c-140">When you enter an expense on a project, the system determines the price through the combination of the category and the unit on the expense.</span></span> 

| <span data-ttu-id="d597c-141">Kulun kuvaus</span><span class="sxs-lookup"><span data-stu-id="d597c-141">Expense description</span></span>        | <span data-ttu-id="d597c-142">Kululuokka</span><span class="sxs-lookup"><span data-stu-id="d597c-142">Expense category</span></span>  | <span data-ttu-id="d597c-143">Yksikkö</span><span class="sxs-lookup"><span data-stu-id="d597c-143">Unit</span></span>  | <span data-ttu-id="d597c-144">Määrä</span><span class="sxs-lookup"><span data-stu-id="d597c-144">Quantity</span></span>  | <span data-ttu-id="d597c-145">Yksikköhinta</span><span class="sxs-lookup"><span data-stu-id="d597c-145">Unit price</span></span>   |
|----------------------------|---------------------|-------|-----------|----------------|
| <span data-ttu-id="d597c-146">Asiakkaan toimipaikkaan ajaminen</span><span class="sxs-lookup"><span data-stu-id="d597c-146">Drive to client location</span></span> | <span data-ttu-id="d597c-147">Kilometrikorvaus</span><span class="sxs-lookup"><span data-stu-id="d597c-147">Mileage</span></span>             | <span data-ttu-id="d597c-148">Maili</span><span class="sxs-lookup"><span data-stu-id="d597c-148">Mile</span></span>  | <span data-ttu-id="d597c-149">10</span><span class="sxs-lookup"><span data-stu-id="d597c-149">10</span></span>        | <span data-ttu-id="d597c-150">10 USD</span><span class="sxs-lookup"><span data-stu-id="d597c-150">10 USD</span></span>         |

<span data-ttu-id="d597c-151">Aikaa varten jokaisella hinnasto-otsikolla on **Oletusaikayksikkö**-kenttä.</span><span class="sxs-lookup"><span data-stu-id="d597c-151">For time, each price list header has a **Default Time Unit** field.</span></span> <span data-ttu-id="d597c-152">Arvo määritetään, kun hinnasto-otsikko luodaan.</span><span class="sxs-lookup"><span data-stu-id="d597c-152">The value is set when you create the price list header.</span></span> <span data-ttu-id="d597c-153">Tämän jälkeen kyseistä yksikköä käytetään kaikkien hinnaston rooliperusteisten hintojen määrittämisessä.</span><span class="sxs-lookup"><span data-stu-id="d597c-153">This unit is then used to set all role-based prices on that price list.</span></span>

<span data-ttu-id="d597c-154">**Tarjouksen aika** -kentän arviorivit voidaan ilmaista missä tahansa aikayksikössä.</span><span class="sxs-lookup"><span data-stu-id="d597c-154">Estimate lines for the **Time on Quote** field can be expressed in any unit of time.</span></span> <span data-ttu-id="d597c-155">Projektien arvioriveissä ja projektien merkinnöissä kuitenkin voidaan käyttää vain **Tunti**-aikayksikköä.</span><span class="sxs-lookup"><span data-stu-id="d597c-155">However, estimate lines on projects and time entries for projects can use only the **Hour** unit of time.</span></span> <span data-ttu-id="d597c-156">Jos aikamerkinnän tai arviorivin yksikkö ei vastaa hinnaston yksikköä kyseistä roolia varten, järjestelmä muuntaa hinnan niiksi yksiköiksi, jotka on määritetty projektiarviossa tai projektin todellisessa tapahtumassa.</span><span class="sxs-lookup"><span data-stu-id="d597c-156">If the unit on the time entry or estimate line doesn't match the unit on the price list line for that role, the system converts the price to the units that are defined in the project estimate or the project actual transaction.</span></span>

<span data-ttu-id="d597c-157">Seuraavassa esimerkissä esitetään, miten PSA käyttää yksikköryhmiä, yksikköjä ja muuntokertoimia.</span><span class="sxs-lookup"><span data-stu-id="d597c-157">The following example shows how PSA uses the unit group, units, and conversion factors.</span></span>
- <span data-ttu-id="d597c-158">Yksiköt</span><span class="sxs-lookup"><span data-stu-id="d597c-158">Units</span></span>

   - <span data-ttu-id="d597c-159">**Yksikköryhmä**: Aika</span><span class="sxs-lookup"><span data-stu-id="d597c-159">**Unit group**: Time</span></span> 
   - <span data-ttu-id="d597c-160">**Yksiköt**: Tunti</span><span class="sxs-lookup"><span data-stu-id="d597c-160">**Units**: Hour</span></span> 
    
    - <span data-ttu-id="d597c-161">**Päivä** – Muuntokerroin: 8 tuntia</span><span class="sxs-lookup"><span data-stu-id="d597c-161">**Day** - Conversion factor: 8 hours</span></span>       
    - <span data-ttu-id="d597c-162">**Viikko** – Muuntokerroin: 40 tuntia</span><span class="sxs-lookup"><span data-stu-id="d597c-162">**Week** - Conversion factor: 40 hours</span></span>  
        
- <span data-ttu-id="d597c-163">Projektin A hinnastomääritys:</span><span class="sxs-lookup"><span data-stu-id="d597c-163">Price list setup on Project A:</span></span>

    - <span data-ttu-id="d597c-164">**Nimi**: UK:n myyntihinnat 2016</span><span class="sxs-lookup"><span data-stu-id="d597c-164">**Name**: UK sales prices 2016</span></span> 
    - <span data-ttu-id="d597c-165">**Oletusaikayksikkö**: Päivä</span><span class="sxs-lookup"><span data-stu-id="d597c-165">**Default time unit**: Day</span></span> 
    - <span data-ttu-id="d597c-166">**Valuutta**: GBP</span><span class="sxs-lookup"><span data-stu-id="d597c-166">**Currency**: GBP</span></span>

| <span data-ttu-id="d597c-167">Rooli</span><span class="sxs-lookup"><span data-stu-id="d597c-167">Role</span></span>      | <span data-ttu-id="d597c-168">Yksikköryhmä</span><span class="sxs-lookup"><span data-stu-id="d597c-168">Unit group</span></span> | <span data-ttu-id="d597c-169">Yksikkö</span><span class="sxs-lookup"><span data-stu-id="d597c-169">Unit</span></span> | <span data-ttu-id="d597c-170">Organisaatioyksikkö</span><span class="sxs-lookup"><span data-stu-id="d597c-170">Organizational unit</span></span> | <span data-ttu-id="d597c-171">Hinta</span><span class="sxs-lookup"><span data-stu-id="d597c-171">Price</span></span>   |
|-----------|------------|------|---------------------|---------|
| <span data-ttu-id="d597c-172">Kehittäjä</span><span class="sxs-lookup"><span data-stu-id="d597c-172">Developer</span></span> | <span data-ttu-id="d597c-173">Time</span><span class="sxs-lookup"><span data-stu-id="d597c-173">Time</span></span>       | <span data-ttu-id="d597c-174">Day</span><span class="sxs-lookup"><span data-stu-id="d597c-174">Day</span></span>  | <span data-ttu-id="d597c-175">Contoso UK</span><span class="sxs-lookup"><span data-stu-id="d597c-175">Contoso UK</span></span>          | <span data-ttu-id="d597c-176">800 GBP</span><span class="sxs-lookup"><span data-stu-id="d597c-176">800 GBP</span></span> |

### <a name="time-entry"></a><span data-ttu-id="d597c-177">Aikamerkintä</span><span class="sxs-lookup"><span data-stu-id="d597c-177">Time entry</span></span>

<span data-ttu-id="d597c-178">Seuraavassa taulukossa esitetään kolmen tunnin projektin tuloksena oleva PSA:n luoma myyntipuolen tapahtuma.</span><span class="sxs-lookup"><span data-stu-id="d597c-178">The following table shows the resulting sales-side transaction created by PSA for a three hour project.</span></span>


| <span data-ttu-id="d597c-179">Projekti</span><span class="sxs-lookup"><span data-stu-id="d597c-179">Project</span></span>   | <span data-ttu-id="d597c-180">Tehtävä</span><span class="sxs-lookup"><span data-stu-id="d597c-180">Task</span></span>    | <span data-ttu-id="d597c-181">Rooli</span><span class="sxs-lookup"><span data-stu-id="d597c-181">Role</span></span>      | <span data-ttu-id="d597c-182">Määrä</span><span class="sxs-lookup"><span data-stu-id="d597c-182">Quantity</span></span> | <span data-ttu-id="d597c-183">Yksikkö</span><span class="sxs-lookup"><span data-stu-id="d597c-183">Unit</span></span>  | <span data-ttu-id="d597c-184">Yksikköhinta</span><span class="sxs-lookup"><span data-stu-id="d597c-184">Unit price</span></span> | <span data-ttu-id="d597c-185">Laskuttamattoman myynnin summa</span><span class="sxs-lookup"><span data-stu-id="d597c-185">Unbilled sales amount</span></span> |
|-----------|---------|-----------|----------|-------|------------|-----------------------|
| <span data-ttu-id="d597c-186">Projekti A</span><span class="sxs-lookup"><span data-stu-id="d597c-186">Project A</span></span> | <span data-ttu-id="d597c-187">Suunnittele</span><span class="sxs-lookup"><span data-stu-id="d597c-187">Design</span></span>  | <span data-ttu-id="d597c-188">Kehittäjä</span><span class="sxs-lookup"><span data-stu-id="d597c-188">Developer</span></span> | <span data-ttu-id="d597c-189">3</span><span class="sxs-lookup"><span data-stu-id="d597c-189">3</span></span>        | <span data-ttu-id="d597c-190">Hour</span><span class="sxs-lookup"><span data-stu-id="d597c-190">Hour</span></span>  | <span data-ttu-id="d597c-191">100 GBP</span><span class="sxs-lookup"><span data-stu-id="d597c-191">100 GBP</span></span>    | <span data-ttu-id="d597c-192">300 GBP</span><span class="sxs-lookup"><span data-stu-id="d597c-192">300 GBP</span></span>               |

## <a name="time-unit-faq"></a><span data-ttu-id="d597c-193">Aikayksikön usein kysytyt kysymykset</span><span class="sxs-lookup"><span data-stu-id="d597c-193">Time unit FAQ</span></span>

### <a name="does-psa-convert-to-different-units-in-the-case-of-expenses"></a><span data-ttu-id="d597c-194">Muuntaako PSA kulut eri yksiköiksi?</span><span class="sxs-lookup"><span data-stu-id="d597c-194">Does PSA convert to different units in the case of expenses?</span></span>
<span data-ttu-id="d597c-195">Ei.</span><span class="sxs-lookup"><span data-stu-id="d597c-195">No.</span></span> <span data-ttu-id="d597c-196">Yksikköjen muuntaminen toimii vain ajan osalta.</span><span class="sxs-lookup"><span data-stu-id="d597c-196">Unit conversion works only for time.</span></span> <span data-ttu-id="d597c-197">Jos järjestelmä ei kulujen osalta löydä hintaa kululuokan ja yksikön yhdistelmälle, hinnan oletusarvo on 0,00.</span><span class="sxs-lookup"><span data-stu-id="d597c-197">For expenses, if the system can't find a price for the combination of the expense category and unit, the price is set to 0.00 by default.</span></span>

### <a name="why-does-psa-convert-time-units"></a><span data-ttu-id="d597c-198">Miksi PSA muuntaa aikayksikköjä?</span><span class="sxs-lookup"><span data-stu-id="d597c-198">Why does PSA convert time units?</span></span>
<span data-ttu-id="d597c-199">Joissakin maissa tai tietyillä alueilla laskutushinnat on lakisääteisesti ilmaistava päivissä.</span><span class="sxs-lookup"><span data-stu-id="d597c-199">In some countries or regions, there is a legal requirement that bill rates be set up in days.</span></span> <span data-ttu-id="d597c-200">Tarjousmenettelyn aikana hintaneuvottelut ja alennukset toteutetaan käyttämällä kunkin laskutettavan roolin päivähintoja.</span><span class="sxs-lookup"><span data-stu-id="d597c-200">Price negotiation and discounting during the quote cycle is done by using day rates for each billable role.</span></span> <span data-ttu-id="d597c-201">Aikatauluarvio ja aikamerkintä toteutetaan tunneissa.</span><span class="sxs-lookup"><span data-stu-id="d597c-201">Schedule estimation and time entry are done in hours.</span></span> <span data-ttu-id="d597c-202">PSA muuntaa aikayksikköjä tukeakseen tätä eroa.</span><span class="sxs-lookup"><span data-stu-id="d597c-202">To support this difference in time units, PSA converts time units.</span></span>

### <a name="can-time-units-be-changed-on-project-estimates"></a><span data-ttu-id="d597c-203">Voidaanko projektiarvioiden aikayksikköjä muuttaa?</span><span class="sxs-lookup"><span data-stu-id="d597c-203">Can time units be changed on project estimates?</span></span>
<span data-ttu-id="d597c-204">Ei.</span><span class="sxs-lookup"><span data-stu-id="d597c-204">No.</span></span> <span data-ttu-id="d597c-205">Projektiarviot on tällä hetkellä rajoitettu tunteihin eikä tähän voi tehdä muutoksia.</span><span class="sxs-lookup"><span data-stu-id="d597c-205">Schedule estimation is currently restricted to hours and can’t be changed.</span></span>

### <a name="can-units-and-unit-groups-be-edited-deleted-and-added"></a><span data-ttu-id="d597c-206">Voiko yksikköjä ja yksikköryhmiä muokata, poistaa ja lisätä?</span><span class="sxs-lookup"><span data-stu-id="d597c-206">Can units and unit groups be edited, deleted, and added?</span></span>
<span data-ttu-id="d597c-207">Kyllä.</span><span class="sxs-lookup"><span data-stu-id="d597c-207">Yes.</span></span> <span data-ttu-id="d597c-208">**Aika**-yksikköryhmää ja **Tunti**-yksikköä lukuun ottamatta kaikkia yksikköjä voi poistaa tai muokata ja uusia yksikköjä voi lisätä.</span><span class="sxs-lookup"><span data-stu-id="d597c-208">With exception of the **Time** unit group and the **Hour** unit, all units can be deleted or edited, and new units can be added.</span></span> <span data-ttu-id="d597c-209">PSA:ssa **Aika**-yksikköryhmää ja **Tunti**-yksikköä ei voi poistaa.</span><span class="sxs-lookup"><span data-stu-id="d597c-209">In PSA, the **Time** unit group and the **Hour** unit can't be deleted.</span></span> <span data-ttu-id="d597c-210">Niitä voidaan kuitenkin päivittää **Nimi**-kenttää varten käännetyllä tekstillä.</span><span class="sxs-lookup"><span data-stu-id="d597c-210">However, they can be updated with a translated text for the **Name** field.</span></span>
