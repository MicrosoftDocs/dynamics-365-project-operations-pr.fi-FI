---
title: Yksikköryhmät ja yksiköt
description: Tässä aiheessa on tietoja yksikköryhmistä ja yksiköistä.
author: rumant
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 03/05/2019
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 45e4a95b429cd9d1f174653bd28cf567f690676d
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5291615"
---
# <a name="unit-groups-and-units"></a><span data-ttu-id="916f8-103">Yksikköryhmät ja yksiköt</span><span class="sxs-lookup"><span data-stu-id="916f8-103">Unit groups and units</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="916f8-104">Yksikköryhmät ja yksiköt Microsoft Dynamics 365:n perusentiteettejä.</span><span class="sxs-lookup"><span data-stu-id="916f8-104">Unit groups and units are basic entities in Microsoft Dynamics 365.</span></span> <span data-ttu-id="916f8-105">Yksikkö on yksittäinen mittayksikkö ja useita yksikköjä voidaan ryhmitellä yksikköryhmiksi.</span><span class="sxs-lookup"><span data-stu-id="916f8-105">A unit is a single unit of measure, and multiple units can be grouped into unit groups.</span></span> <span data-ttu-id="916f8-106">Yksikköryhmää kutsutaan joskus yksikköaikatauluksi Dynamics 365:n käyttöliittymässä (UI).</span><span class="sxs-lookup"><span data-stu-id="916f8-106">A unit group is sometimes referred to as a unit schedule in the Dynamics 365 user interface (UI).</span></span> 

<span data-ttu-id="916f8-107">Seuraavassa on esimerkkejä yksiköistä ja yksikköryhmistä:</span><span class="sxs-lookup"><span data-stu-id="916f8-107">Here are some examples of units and unit groups:</span></span>
 
- <span data-ttu-id="916f8-108">**Yksikköryhmä**: Etäisyys</span><span class="sxs-lookup"><span data-stu-id="916f8-108">**Unit group**: Distance</span></span> 
    - <span data-ttu-id="916f8-109">**Yksiköt**: Maili, Kilometri jne.</span><span class="sxs-lookup"><span data-stu-id="916f8-109">**Units**: Mile, Kilometer, and so on.</span></span>
- <span data-ttu-id="916f8-110">**Yksikköryhmä**: Aika</span><span class="sxs-lookup"><span data-stu-id="916f8-110">**Unit group**: Time</span></span>
    - <span data-ttu-id="916f8-111">**Yksiköt**: Tunti, Päivä, Viikko jne.</span><span class="sxs-lookup"><span data-stu-id="916f8-111">**Units**: Hour, day, week, and so on.</span></span> 

<span data-ttu-id="916f8-112">Kun useita yksikköjä määritetään yksikköryhmäksi, niiden välille on myös määritettävä muuntokerroin määrittämällä ensimmäinen määritettävä yksikkö yksikköryhmän oletusyksiköksi tai ensisijaiseksi yksiköksi.</span><span class="sxs-lookup"><span data-stu-id="916f8-112">When you set up multiple units in a unit group, you must also set up a conversion factor between them by designating the first unit that you set up as the default or primary unit for the unit group.</span></span> 

<span data-ttu-id="916f8-113">Jos esimerkiksi **Aika**-yksikköryhmässä ensimmäisenä yksikkönä määritetään **Tunti**, järjestelmä määrittää yksikön **Tunti** oletusyksiköksi.</span><span class="sxs-lookup"><span data-stu-id="916f8-113">For example, in a **Time** unit group, if you set up **Hour** as the first unit, the system designates **Hour** as the default unit.</span></span> <span data-ttu-id="916f8-114">Jos seuraavana yksikkönä määritetään **Päivä**, on määritettävä muuntokerroin yksikköjen **Päivä** ja **Tunti** välille.</span><span class="sxs-lookup"><span data-stu-id="916f8-114">If the next unit that you set up is **Day**, you must set up a conversion factor for **Day** to **Hour**.</span></span> <span data-ttu-id="916f8-115">Jos sitten kolmantena yksikkönä määritetään **Viikko**, on määritettävä muuntokerroin yksikköjen **Viikko** ja joko **Päivä** tai **Tunti** välille.</span><span class="sxs-lookup"><span data-stu-id="916f8-115">If you then add **Week** as a third unit, you must set up a conversion factor for **Week** in terms of **Day** or **Hour**.</span></span> 

<span data-ttu-id="916f8-116">Seuraavassa kuvassa esitetään esimerkkimääritys yksikölle **Päivä**, jossa **Määrä**-kentässä näkyy päivässä olevien tuntien määrä, ja yksikölle **Viikko**, jossa **Määrä**-kentässä näkyy viikossa olevien päivien määrä.</span><span class="sxs-lookup"><span data-stu-id="916f8-116">The following image shows an example setup for the **Day** unit, where the **Quantity** field shows the number of hours that are in a day, and **Week**, where the **Quantity** field show the number of days that are in a week.</span></span>

> ![Yksikköryhmä: tietosivu](media/advanced-2.png)

## <a name="using-units-and-unit-groups"></a><span data-ttu-id="916f8-118">Yksikköjen ja yksikköryhmien käyttö</span><span class="sxs-lookup"><span data-stu-id="916f8-118">Using units and unit groups</span></span>

<span data-ttu-id="916f8-119">Dynamics 365 Project Service Automation käyttää yksikköjä ja yksikköryhmiä käsitelläkseen sekä kulujen että ajan arvioiden ja merkintöjen käsittelyyn.</span><span class="sxs-lookup"><span data-stu-id="916f8-119">Dynamics 365 Project Service Automation uses units and unit groups to process estimates and entries for both expenses and time.</span></span> 

<span data-ttu-id="916f8-120">Kulujen osalta kullakin kululuokalla on oletusarvoinen yksikköryhmänsä ja yksikkönsä.</span><span class="sxs-lookup"><span data-stu-id="916f8-120">For expenses, each expense category has a default unit group and unit.</span></span> <span data-ttu-id="916f8-121">Nämä arvot otetaan oletusarvoiksi kululuokkien hinnastomerkinnöille.</span><span class="sxs-lookup"><span data-stu-id="916f8-121">These values are entered as default values on price list entries for expense categories.</span></span> 

<span data-ttu-id="916f8-122">Sinulla voi olla esimerkiksi **Kilometrikorvaus**-niminen kululuokka.</span><span class="sxs-lookup"><span data-stu-id="916f8-122">For example, you have an expense category that is named **Mileage**.</span></span> <span data-ttu-id="916f8-123">Sillä on **Etäisyys**-niminen yksikköryhmä ja oletusyksikkö nimeltä **Maili**.</span><span class="sxs-lookup"><span data-stu-id="916f8-123">It has a unit group that is named **Distance** and a default unit that is named **Mile**.</span></span> <span data-ttu-id="916f8-124">Jos määrität **Etäisyys**-yksikköryhmän siten, että siinä on kaksi yksikköä (**Maili** ja **Kilometri**), voit määrittää yhden hinnaston **Kilometrikorvaus**-luokalle kaksi hintaa: mailikohtainen hinta ja kilometrikohtainen hinta.</span><span class="sxs-lookup"><span data-stu-id="916f8-124">If you set up the **Distance** unit group so that it has two units (**Mile** and **Kilometer**), you can set two prices for the **Mileage** category on one price list: price per mile and price per kilometer.</span></span>

| <span data-ttu-id="916f8-125">Kululuokka</span><span class="sxs-lookup"><span data-stu-id="916f8-125">Expense category</span></span>  | <span data-ttu-id="916f8-126">Yksikköryhmä</span><span class="sxs-lookup"><span data-stu-id="916f8-126">Unit group</span></span>  | <span data-ttu-id="916f8-127">Yksikkö</span><span class="sxs-lookup"><span data-stu-id="916f8-127">Unit</span></span>      | <span data-ttu-id="916f8-128">Hinnoittelutapa</span><span class="sxs-lookup"><span data-stu-id="916f8-128">Pricing method</span></span>  | <span data-ttu-id="916f8-129">Yksikköhinta</span><span class="sxs-lookup"><span data-stu-id="916f8-129">Price per unit</span></span>  |
|-------------------|---------------|-----------|-------------------|-------------------|
| <span data-ttu-id="916f8-130">Kilometrikorvaus</span><span class="sxs-lookup"><span data-stu-id="916f8-130">Mileage</span></span>           | <span data-ttu-id="916f8-131">Etäisyys</span><span class="sxs-lookup"><span data-stu-id="916f8-131">Distance</span></span>      | <span data-ttu-id="916f8-132">Maili</span><span class="sxs-lookup"><span data-stu-id="916f8-132">Mile</span></span>      | <span data-ttu-id="916f8-133">Yksikköhinta</span><span class="sxs-lookup"><span data-stu-id="916f8-133">Price per unit</span></span>    | <span data-ttu-id="916f8-134">10 USD</span><span class="sxs-lookup"><span data-stu-id="916f8-134">10 USD</span></span>            |
| <span data-ttu-id="916f8-135">Kilometrikorvaus</span><span class="sxs-lookup"><span data-stu-id="916f8-135">Mileage</span></span>           | <span data-ttu-id="916f8-136">Etäisyys</span><span class="sxs-lookup"><span data-stu-id="916f8-136">Distance</span></span>      | <span data-ttu-id="916f8-137">Kilometri</span><span class="sxs-lookup"><span data-stu-id="916f8-137">Kilometer</span></span> | <span data-ttu-id="916f8-138">Yksikköhinta</span><span class="sxs-lookup"><span data-stu-id="916f8-138">Price per unit</span></span>    |  <span data-ttu-id="916f8-139">6 USD</span><span class="sxs-lookup"><span data-stu-id="916f8-139">6 USD</span></span>            |

<span data-ttu-id="916f8-140">Kun lisäät projektiin kulun, järjestelmä määrittää hinnan kyseisen kulun luokan ja yksikön yhdistelmän perusteella.</span><span class="sxs-lookup"><span data-stu-id="916f8-140">When you enter an expense on a project, the system determines the price through the combination of the category and the unit on the expense.</span></span> 

| <span data-ttu-id="916f8-141">Kulun kuvaus</span><span class="sxs-lookup"><span data-stu-id="916f8-141">Expense description</span></span>        | <span data-ttu-id="916f8-142">Kululuokka</span><span class="sxs-lookup"><span data-stu-id="916f8-142">Expense category</span></span>  | <span data-ttu-id="916f8-143">Yksikkö</span><span class="sxs-lookup"><span data-stu-id="916f8-143">Unit</span></span>  | <span data-ttu-id="916f8-144">Määrä</span><span class="sxs-lookup"><span data-stu-id="916f8-144">Quantity</span></span>  | <span data-ttu-id="916f8-145">Yksikköhinta</span><span class="sxs-lookup"><span data-stu-id="916f8-145">Unit price</span></span>   |
|----------------------------|---------------------|-------|-----------|----------------|
| <span data-ttu-id="916f8-146">Asiakkaan toimipaikkaan ajaminen</span><span class="sxs-lookup"><span data-stu-id="916f8-146">Drive to client location</span></span> | <span data-ttu-id="916f8-147">Kilometrikorvaus</span><span class="sxs-lookup"><span data-stu-id="916f8-147">Mileage</span></span>             | <span data-ttu-id="916f8-148">Maili</span><span class="sxs-lookup"><span data-stu-id="916f8-148">Mile</span></span>  | <span data-ttu-id="916f8-149">10</span><span class="sxs-lookup"><span data-stu-id="916f8-149">10</span></span>        | <span data-ttu-id="916f8-150">10 USD</span><span class="sxs-lookup"><span data-stu-id="916f8-150">10 USD</span></span>         |

<span data-ttu-id="916f8-151">Aikaa varten jokaisella hinnasto-otsikolla on **Oletusaikayksikkö**-kenttä.</span><span class="sxs-lookup"><span data-stu-id="916f8-151">For time, each price list header has a **Default Time Unit** field.</span></span> <span data-ttu-id="916f8-152">Arvo määritetään, kun hinnasto-otsikko luodaan.</span><span class="sxs-lookup"><span data-stu-id="916f8-152">The value is set when you create the price list header.</span></span> <span data-ttu-id="916f8-153">Tämän jälkeen kyseistä yksikköä käytetään kaikkien hinnaston rooliperusteisten hintojen määrittämisessä.</span><span class="sxs-lookup"><span data-stu-id="916f8-153">This unit is then used to set all role-based prices on that price list.</span></span>

<span data-ttu-id="916f8-154">**Tarjouksen aika** -kentän arviorivit voidaan ilmaista missä tahansa aikayksikössä.</span><span class="sxs-lookup"><span data-stu-id="916f8-154">Estimate lines for the **Time on Quote** field can be expressed in any unit of time.</span></span> <span data-ttu-id="916f8-155">Projektien arvioriveissä ja projektien merkinnöissä kuitenkin voidaan käyttää vain **Tunti**-aikayksikköä.</span><span class="sxs-lookup"><span data-stu-id="916f8-155">However, estimate lines on projects and time entries for projects can use only the **Hour** unit of time.</span></span> <span data-ttu-id="916f8-156">Jos aikamerkinnän tai arviorivin yksikkö ei vastaa hinnaston yksikköä kyseistä roolia varten, järjestelmä muuntaa hinnan niiksi yksiköiksi, jotka on määritetty projektiarviossa tai projektin todellisessa tapahtumassa.</span><span class="sxs-lookup"><span data-stu-id="916f8-156">If the unit on the time entry or estimate line doesn't match the unit on the price list line for that role, the system converts the price to the units that are defined in the project estimate or the project actual transaction.</span></span>

<span data-ttu-id="916f8-157">Seuraavassa esimerkissä esitetään, miten PSA käyttää yksikköryhmiä, yksikköjä ja muuntokertoimia.</span><span class="sxs-lookup"><span data-stu-id="916f8-157">The following example shows how PSA uses the unit group, units, and conversion factors.</span></span>
- <span data-ttu-id="916f8-158">Yksiköt</span><span class="sxs-lookup"><span data-stu-id="916f8-158">Units</span></span>

   - <span data-ttu-id="916f8-159">**Yksikköryhmä**: Aika</span><span class="sxs-lookup"><span data-stu-id="916f8-159">**Unit group**: Time</span></span> 
   - <span data-ttu-id="916f8-160">**Yksiköt**: Tunti</span><span class="sxs-lookup"><span data-stu-id="916f8-160">**Units**: Hour</span></span> 
    
    - <span data-ttu-id="916f8-161">**Päivä** – Muuntokerroin: 8 tuntia</span><span class="sxs-lookup"><span data-stu-id="916f8-161">**Day** - Conversion factor: 8 hours</span></span>       
    - <span data-ttu-id="916f8-162">**Viikko** – Muuntokerroin: 40 tuntia</span><span class="sxs-lookup"><span data-stu-id="916f8-162">**Week** - Conversion factor: 40 hours</span></span>  
        
- <span data-ttu-id="916f8-163">Projektin A hinnastomääritys:</span><span class="sxs-lookup"><span data-stu-id="916f8-163">Price list setup on Project A:</span></span>

    - <span data-ttu-id="916f8-164">**Nimi**: UK:n myyntihinnat 2016</span><span class="sxs-lookup"><span data-stu-id="916f8-164">**Name**: UK sales prices 2016</span></span> 
    - <span data-ttu-id="916f8-165">**Oletusaikayksikkö**: Päivä</span><span class="sxs-lookup"><span data-stu-id="916f8-165">**Default time unit**: Day</span></span> 
    - <span data-ttu-id="916f8-166">**Valuutta**: GBP</span><span class="sxs-lookup"><span data-stu-id="916f8-166">**Currency**: GBP</span></span>

| <span data-ttu-id="916f8-167">Rooli</span><span class="sxs-lookup"><span data-stu-id="916f8-167">Role</span></span>      | <span data-ttu-id="916f8-168">Yksikköryhmä</span><span class="sxs-lookup"><span data-stu-id="916f8-168">Unit group</span></span> | <span data-ttu-id="916f8-169">Yksikkö</span><span class="sxs-lookup"><span data-stu-id="916f8-169">Unit</span></span> | <span data-ttu-id="916f8-170">Organisaatioyksikkö</span><span class="sxs-lookup"><span data-stu-id="916f8-170">Organizational unit</span></span> | <span data-ttu-id="916f8-171">Hinta</span><span class="sxs-lookup"><span data-stu-id="916f8-171">Price</span></span>   |
|-----------|------------|------|---------------------|---------|
| <span data-ttu-id="916f8-172">Kehittäjä</span><span class="sxs-lookup"><span data-stu-id="916f8-172">Developer</span></span> | <span data-ttu-id="916f8-173">Time</span><span class="sxs-lookup"><span data-stu-id="916f8-173">Time</span></span>       | <span data-ttu-id="916f8-174">Day</span><span class="sxs-lookup"><span data-stu-id="916f8-174">Day</span></span>  | <span data-ttu-id="916f8-175">Contoso UK</span><span class="sxs-lookup"><span data-stu-id="916f8-175">Contoso UK</span></span>          | <span data-ttu-id="916f8-176">800 GBP</span><span class="sxs-lookup"><span data-stu-id="916f8-176">800 GBP</span></span> |

### <a name="time-entry"></a><span data-ttu-id="916f8-177">Aikamerkintä</span><span class="sxs-lookup"><span data-stu-id="916f8-177">Time entry</span></span>

<span data-ttu-id="916f8-178">Seuraavassa taulukossa esitetään kolmen tunnin projektin tuloksena oleva PSA:n luoma myyntipuolen tapahtuma.</span><span class="sxs-lookup"><span data-stu-id="916f8-178">The following table shows the resulting sales-side transaction created by PSA for a three hour project.</span></span>


| <span data-ttu-id="916f8-179">Projekti</span><span class="sxs-lookup"><span data-stu-id="916f8-179">Project</span></span>   | <span data-ttu-id="916f8-180">Tehtävä</span><span class="sxs-lookup"><span data-stu-id="916f8-180">Task</span></span>    | <span data-ttu-id="916f8-181">Rooli</span><span class="sxs-lookup"><span data-stu-id="916f8-181">Role</span></span>      | <span data-ttu-id="916f8-182">Määrä</span><span class="sxs-lookup"><span data-stu-id="916f8-182">Quantity</span></span> | <span data-ttu-id="916f8-183">Yksikkö</span><span class="sxs-lookup"><span data-stu-id="916f8-183">Unit</span></span>  | <span data-ttu-id="916f8-184">Yksikköhinta</span><span class="sxs-lookup"><span data-stu-id="916f8-184">Unit price</span></span> | <span data-ttu-id="916f8-185">Laskuttamattoman myynnin summa</span><span class="sxs-lookup"><span data-stu-id="916f8-185">Unbilled sales amount</span></span> |
|-----------|---------|-----------|----------|-------|------------|-----------------------|
| <span data-ttu-id="916f8-186">Projekti A</span><span class="sxs-lookup"><span data-stu-id="916f8-186">Project A</span></span> | <span data-ttu-id="916f8-187">Suunnittele</span><span class="sxs-lookup"><span data-stu-id="916f8-187">Design</span></span>  | <span data-ttu-id="916f8-188">Kehittäjä</span><span class="sxs-lookup"><span data-stu-id="916f8-188">Developer</span></span> | <span data-ttu-id="916f8-189">3</span><span class="sxs-lookup"><span data-stu-id="916f8-189">3</span></span>        | <span data-ttu-id="916f8-190">Hour</span><span class="sxs-lookup"><span data-stu-id="916f8-190">Hour</span></span>  | <span data-ttu-id="916f8-191">100 GBP</span><span class="sxs-lookup"><span data-stu-id="916f8-191">100 GBP</span></span>    | <span data-ttu-id="916f8-192">300 GBP</span><span class="sxs-lookup"><span data-stu-id="916f8-192">300 GBP</span></span>               |

## <a name="time-unit-faq"></a><span data-ttu-id="916f8-193">Aikayksikön usein kysytyt kysymykset</span><span class="sxs-lookup"><span data-stu-id="916f8-193">Time unit FAQ</span></span>

### <a name="does-psa-convert-to-different-units-in-the-case-of-expenses"></a><span data-ttu-id="916f8-194">Muuntaako PSA kulut eri yksiköiksi?</span><span class="sxs-lookup"><span data-stu-id="916f8-194">Does PSA convert to different units in the case of expenses?</span></span>
<span data-ttu-id="916f8-195">Ei.</span><span class="sxs-lookup"><span data-stu-id="916f8-195">No.</span></span> <span data-ttu-id="916f8-196">Yksikköjen muuntaminen toimii vain ajan osalta.</span><span class="sxs-lookup"><span data-stu-id="916f8-196">Unit conversion works only for time.</span></span> <span data-ttu-id="916f8-197">Jos järjestelmä ei kulujen osalta löydä hintaa kululuokan ja yksikön yhdistelmälle, hinnan oletusarvo on 0,00.</span><span class="sxs-lookup"><span data-stu-id="916f8-197">For expenses, if the system can't find a price for the combination of the expense category and unit, the price is set to 0.00 by default.</span></span>

### <a name="why-does-psa-convert-time-units"></a><span data-ttu-id="916f8-198">Miksi PSA muuntaa aikayksikköjä?</span><span class="sxs-lookup"><span data-stu-id="916f8-198">Why does PSA convert time units?</span></span>
<span data-ttu-id="916f8-199">Joissakin maissa tai tietyillä alueilla laskutushinnat on lakisääteisesti ilmaistava päivissä.</span><span class="sxs-lookup"><span data-stu-id="916f8-199">In some countries or regions, there is a legal requirement that bill rates be set up in days.</span></span> <span data-ttu-id="916f8-200">Tarjousmenettelyn aikana hintaneuvottelut ja alennukset toteutetaan käyttämällä kunkin laskutettavan roolin päivähintoja.</span><span class="sxs-lookup"><span data-stu-id="916f8-200">Price negotiation and discounting during the quote cycle is done by using day rates for each billable role.</span></span> <span data-ttu-id="916f8-201">Aikatauluarvio ja aikamerkintä toteutetaan tunneissa.</span><span class="sxs-lookup"><span data-stu-id="916f8-201">Schedule estimation and time entry are done in hours.</span></span> <span data-ttu-id="916f8-202">PSA muuntaa aikayksikköjä tukeakseen tätä eroa.</span><span class="sxs-lookup"><span data-stu-id="916f8-202">To support this difference in time units, PSA converts time units.</span></span>

### <a name="can-time-units-be-changed-on-project-estimates"></a><span data-ttu-id="916f8-203">Voidaanko projektiarvioiden aikayksikköjä muuttaa?</span><span class="sxs-lookup"><span data-stu-id="916f8-203">Can time units be changed on project estimates?</span></span>
<span data-ttu-id="916f8-204">Ei.</span><span class="sxs-lookup"><span data-stu-id="916f8-204">No.</span></span> <span data-ttu-id="916f8-205">Projektiarviot on tällä hetkellä rajoitettu tunteihin eikä tähän voi tehdä muutoksia.</span><span class="sxs-lookup"><span data-stu-id="916f8-205">Schedule estimation is currently restricted to hours and can’t be changed.</span></span>

### <a name="can-units-and-unit-groups-be-edited-deleted-and-added"></a><span data-ttu-id="916f8-206">Voiko yksikköjä ja yksikköryhmiä muokata, poistaa ja lisätä?</span><span class="sxs-lookup"><span data-stu-id="916f8-206">Can units and unit groups be edited, deleted, and added?</span></span>
<span data-ttu-id="916f8-207">Kyllä.</span><span class="sxs-lookup"><span data-stu-id="916f8-207">Yes.</span></span> <span data-ttu-id="916f8-208">**Aika**-yksikköryhmää ja **Tunti**-yksikköä lukuun ottamatta kaikkia yksikköjä voi poistaa tai muokata ja uusia yksikköjä voi lisätä.</span><span class="sxs-lookup"><span data-stu-id="916f8-208">With exception of the **Time** unit group and the **Hour** unit, all units can be deleted or edited, and new units can be added.</span></span> <span data-ttu-id="916f8-209">PSA:ssa **Aika**-yksikköryhmää ja **Tunti**-yksikköä ei voi poistaa.</span><span class="sxs-lookup"><span data-stu-id="916f8-209">In PSA, the **Time** unit group and the **Hour** unit can't be deleted.</span></span> <span data-ttu-id="916f8-210">Niitä voidaan kuitenkin päivittää **Nimi**-kenttää varten käännetyllä tekstillä.</span><span class="sxs-lookup"><span data-stu-id="916f8-210">However, they can be updated with a translated text for the **Name** field.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]