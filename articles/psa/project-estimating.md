---
title: Projektin kustannukset ja tuotto
description: Tässä aiheessa on tietoja projektin kustannusten ja tuoton arvioinnista.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 282950c0ee21f430a2f20b21128830891c76c84a
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/28/2020
ms.locfileid: "4127964"
---
# <a name="project-costs-and-revenue"></a><span data-ttu-id="17618-103">Projektin kustannukset ja tuotto</span><span class="sxs-lookup"><span data-stu-id="17618-103">Project costs and revenue</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="17618-104">Projektin arviot tarjoavat taloudellisen näkymän työhän, joka on arvioitu ja aikataulutettu projektin aikataulussa.</span><span class="sxs-lookup"><span data-stu-id="17618-104">Project estimates provide the financial view for work that is estimated and scheduled in the project schedule.</span></span> <span data-ttu-id="17618-105">**Arviot**-välilehti **Projektit**-sivulla näyttää suunnittelemasi työn kustannus- ja tuottovaikutukset.</span><span class="sxs-lookup"><span data-stu-id="17618-105">The **Estimates** tab on the **Projects** page shows the cost and revenue impact of the work that you’re planning.</span></span> <span data-ttu-id="17618-106">Se sisältää myös tietoja monista esimääritetyistä dimensioista.</span><span class="sxs-lookup"><span data-stu-id="17618-106">It also provides information about many predefined dimensions.</span></span> 

> ![Arviot-välilehti](media/project-5.png)

## <a name="cost-and-sales-values-of-the-project"></a><span data-ttu-id="17618-108">Projektin kustannus- ja myyntiarvot</span><span class="sxs-lookup"><span data-stu-id="17618-108">Cost and sales values of the project</span></span>

<span data-ttu-id="17618-109">Hinnastot määrittävät projektin roolien kustannukset ja laskutushinnan.</span><span class="sxs-lookup"><span data-stu-id="17618-109">Price lists define the cost and bill rates for roles in a project.</span></span> <span data-ttu-id="17618-110">Voit määrittää työn kustannus- ja tuottovaikutuksen työtehtävän nimeen liitettyjen roolien sekä tehtävään määritetyn nimetyn resurssin perusteella.</span><span class="sxs-lookup"><span data-stu-id="17618-110">You can determine the cost and revenue impact of the work, based on the roles that are associated with the position name and the named resource that is assigned to a task.</span></span> <span data-ttu-id="17618-111">Jos on tehtäviä, joihin ei ole osoitettu tekijöitä (yleisiä tai nimettyjä), et voi saada kustannus- tai myyntiarvioita.</span><span class="sxs-lookup"><span data-stu-id="17618-111">If there are tasks that don't have any assignments (generic or named), you can’t get cost or sales estimates.</span></span> <span data-ttu-id="17618-112">Kustannus- ja myyntiarvot ottavat huomioon hinnastoissa määritellyn päivämäärän.</span><span class="sxs-lookup"><span data-stu-id="17618-112">Cost and sales values consider the date that is defined in the price lists.</span></span>

### <a name="default-cost-price"></a><span data-ttu-id="17618-113">Kustannusten oletushinta</span><span class="sxs-lookup"><span data-stu-id="17618-113">Default cost price</span></span>  

<span data-ttu-id="17618-114">Jokainen projekti kuuluu organisaatioon.</span><span class="sxs-lookup"><span data-stu-id="17618-114">Every project belongs to an organization.</span></span> <span data-ttu-id="17618-115">Tämä organisaatio näkyy projektin **Hankintayksikkö** -kentässä.</span><span class="sxs-lookup"><span data-stu-id="17618-115">This organization is shown in the **Contracting Unit** field in the project.</span></span> <span data-ttu-id="17618-116">Hankintayksikköön liitettyä hinnastoa käytetään yksikkökustannushinnan määrittämiseksi.</span><span class="sxs-lookup"><span data-stu-id="17618-116">The price list that is associated with the contracting unit is used to determine the unit cost price.</span></span> <span data-ttu-id="17618-117">OIkeiden kustannushintojen määrittämiseksi rooleille sitä päivämäärää varten, joka on määritelty arvioriveillä, etsi roolin, yksikön ja organisaation yksikön yhdistelmää kustannushinnastosta.</span><span class="sxs-lookup"><span data-stu-id="17618-117">To determine the correct cost prices on roles for the date that is defined on estimate lines, search for the combination of role, unit, and organizational unit in the cost price list.</span></span> 

<span data-ttu-id="17618-118">Jotta niiden kustannushinnat voidaan laskea, kaikki tehtävät on kohdennettava resurssille.</span><span class="sxs-lookup"><span data-stu-id="17618-118">So that their cost prices can be calculated, all tasks must be assigned to a resource.</span></span> <span data-ttu-id="17618-119">Kaikkien kohdentamattomien tehtävien kustannushinta on 0,00.</span><span class="sxs-lookup"><span data-stu-id="17618-119">Any uwnassigned tasks will have a cost price of 0.00.</span></span>

<span data-ttu-id="17618-120">Jos roolien, yksiköiden ja organisaatioyksiköiden yhdistelmä ei palauta kustannushintaa hankintayksikön hinnastosta, järjestelmä ohittaa yksikön.</span><span class="sxs-lookup"><span data-stu-id="17618-120">If the combination of role, unit, and organizational unit doesn't return a cost price from the contracting unit's price list, the system ignores the unit.</span></span> <span data-ttu-id="17618-121">Se hakee sen sijaan vain roolien ja organisaatioyksiköiden yhdistelmän.</span><span class="sxs-lookup"><span data-stu-id="17618-121">Instead, it searches for the combination of just role and organizational unit.</span></span> <span data-ttu-id="17618-122">Jos kustannushinta löytyy, käytetään muuntokertoimia muuntamaan se yksiköksi, jonka valitsit arviorivillä.</span><span class="sxs-lookup"><span data-stu-id="17618-122">If a cost price is found, conversion factors are used to convert it to the unit that you selected on the estimate line.</span></span>

<span data-ttu-id="17618-123">Jos roolin ja organisaatioyksikön yhdistelmä ei palauta kustannushintaa, järjestelmä ohittaa organisaatioyksikön.</span><span class="sxs-lookup"><span data-stu-id="17618-123">If the combination of role and organizational unit doesn't return a cost price, the system ignores the organizational unit.</span></span> <span data-ttu-id="17618-124">Se hakee sen sijaan roolien ja yksiköiden yhdistelmän, joka määrittää oletushinnan (mahdollisen muunnoksen jälkeen).</span><span class="sxs-lookup"><span data-stu-id="17618-124">Instead, it searches for the combination of role and unit to set the default price (after any conversion is applied).</span></span>

<span data-ttu-id="17618-125">Jos järjestelmä ei löydä roolille hintaa, kustannushinta arviorivillä asetetaan oletusarvoon **0,00**.</span><span class="sxs-lookup"><span data-stu-id="17618-125">If the system doesn't find a price for the role, the cost price on the estimate line is set to a default value of **0.00**.</span></span> <span data-ttu-id="17618-126">Kaikki projektin kustannusarvioriveillä olevat kustannussummat ovat hankintayksikön valuutassa.</span><span class="sxs-lookup"><span data-stu-id="17618-126">All cost amounts on the project cost estimate lines are recorded in the currency of the contracting unit.</span></span>

> [!NOTE]
> <span data-ttu-id="17618-127">Microsoft Dynamics 365 tallentaa kustannussummat oletusarvoisesti perusvaluutassasi.</span><span class="sxs-lookup"><span data-stu-id="17618-127">By default, Microsoft Dynamics 365 stores cost amounts in your base currency.</span></span> <span data-ttu-id="17618-128">**Arviot**-välilehdellä näytettävät kustannussummat ovat kuitenkin hankintayksikön valuutassa.</span><span class="sxs-lookup"><span data-stu-id="17618-128">However, the cost amounts that are shown on the **Estimates** tab are in the currency of the contracting unit.</span></span>  

### <a name="default-sales-price"></a><span data-ttu-id="17618-129">Oletusmyyntihinta</span><span class="sxs-lookup"><span data-stu-id="17618-129">Default sales price</span></span> 

<span data-ttu-id="17618-130">Myyntihinnaston määrittää joko se myyntikohde, johon projekti on liitetty, tai projektin asiakas.</span><span class="sxs-lookup"><span data-stu-id="17618-130">The sales price list is determined by either the sales entity that the project is attached to or the project customer.</span></span> <span data-ttu-id="17618-131">Kun projektiin liittyy myyntikohde, kuten mahdollisuus, tarjous tai sopimus, myyntikohteen myyntihinnan määrittää tarjoukseen tai sopimukseen liittyvä hinnasto.</span><span class="sxs-lookup"><span data-stu-id="17618-131">When a sales entity, such as opportunity, quote, or contract, is associated with the project, the sales entity's sales price is determined by the price list that is associated with the quote or contract.</span></span> <span data-ttu-id="17618-132">Jos tarjouksessa tai sopimuksessa on mukautettu hinnasto, sitä käytetään oletusmyyntihinnastona projektin arvioille.</span><span class="sxs-lookup"><span data-stu-id="17618-132">If the quote or contract has a custom price list, that price list is used as the default sales price list for project estimates.</span></span> <span data-ttu-id="17618-133">Jos myyntikohteiden kanssa ei ole yhteyttä, parametrien oletusmyyntihinnastoa käytetään projektin oletusmyyntihinnastona, jota vastaa projektissa määritetty asiakasvaluutta.</span><span class="sxs-lookup"><span data-stu-id="17618-133">If there is no association with sales entities, the default sales price list from the parameters is used as the project's default sales price list matched by the customer currency that is defined on the project.</span></span>

<span data-ttu-id="17618-134">Kullakin arviorivillä on siihen liittyvä resurssiyksikkö.</span><span class="sxs-lookup"><span data-stu-id="17618-134">Each estimate line has a resourcing unit that is associated with it.</span></span> <span data-ttu-id="17618-135">Resurssiyksikkö osoittaa organisaatioyksikön, josta resurssit on varattu, jotta tehtävä voidaan suorittaa loppuun.</span><span class="sxs-lookup"><span data-stu-id="17618-135">The resourcing unit indicates the organizational unit that resources are booked from to complete the task.</span></span> <span data-ttu-id="17618-136">Määrittääksesi myyntihinnan liitetyille rooleille etsi roolin, yksikön ja resurssiyksikön yhdistelmää myyntihinnastossa.</span><span class="sxs-lookup"><span data-stu-id="17618-136">To determine the sales price for the associated roles, search for the combination of role, unit, and resourcing unit in the sales price list.</span></span> <span data-ttu-id="17618-137">Jos tehtävässä ei ole kohdennuksia, tehtävän myyntihinta on 0,00.</span><span class="sxs-lookup"><span data-stu-id="17618-137">If there are no assignments on the task, the sales price for the task is 0.00.</span></span>

<span data-ttu-id="17618-138">Jos roolin, yksikön ja resurssiyksikön yhdistelmä ei palauta kustannushintaa myyntihinnastosta, järjestelmä ohittaa yksikön.</span><span class="sxs-lookup"><span data-stu-id="17618-138">If the combination of role, unit, and resourcing unit doesn't return a sales price from the sales price list, the system ignores the unit.</span></span> <span data-ttu-id="17618-139">Se hakee sen sijaan vain roolin ja resurssiyksikön yhdistelmän.</span><span class="sxs-lookup"><span data-stu-id="17618-139">Instead, it searches for the combination of just role and resourcing unit.</span></span> <span data-ttu-id="17618-140">Jos myyntihinta löytyy, käytetään muuntokertoimia muuntamaan se yksiköksi, jonka valitsit myynnin arviorivillä.</span><span class="sxs-lookup"><span data-stu-id="17618-140">If a sales price is found, conversion factors are used to convert it to the unit that you selected on the sales estimate line.</span></span> 

<span data-ttu-id="17618-141">Jos roolin, yksikön ja resurssiyksikön yhdistelmä ei palauta myyntihintaa myyntihinnastosta, järjestelmä ohittaa resurssiyksikön.</span><span class="sxs-lookup"><span data-stu-id="17618-141">If the combination of role and resourcing unit doesn't return a sales price from the sales price list, the system ignores the resourcing unit.</span></span> <span data-ttu-id="17618-142">Se hakee sen sijaan roolien ja yksiköiden yhdistelmän, joka määrittää oletushinnan (mahdollisen muunnoksen jälkeen).</span><span class="sxs-lookup"><span data-stu-id="17618-142">Instead, it searches for the combination of role and unit to set the default price (after any conversion is applied).</span></span>

<span data-ttu-id="17618-143">Jos järjestelmä ei löydä roolille hintaa, myyntihinta arviorivillä asetetaan oletusarvoon **0,00**.</span><span class="sxs-lookup"><span data-stu-id="17618-143">If the system doesn't find a price for the role, the sales price on the estimate line is set to a default value of **0.00**.</span></span>

<span data-ttu-id="17618-144">**Arviot**-välilehdellä on ruudukkonäkymä, jossa näkyvät arviorivit.</span><span class="sxs-lookup"><span data-stu-id="17618-144">The **Estimates** tab has a grid view that shows estimate lines.</span></span> <span data-ttu-id="17618-145">Ruudukossa on yksikkö-, kokonaiskustannushinta- ja kokonaismyyntihinta-sarakkeet, jotka on esitetty seuraavassa kuvassa.</span><span class="sxs-lookup"><span data-stu-id="17618-145">The grid includes columns for the unit, total cost price, and total sales price, as shown in the following illustration.</span></span> 

> ![Arviot-välilehden ruudukkonäkymä](media/project-6.png)

## <a name="time-phased-view-of-project-estimates"></a><span data-ttu-id="17618-147">Projektin arvioiden aikavaiheistettu näkymä</span><span class="sxs-lookup"><span data-stu-id="17618-147">Time-phased view of project estimates</span></span>

<span data-ttu-id="17618-148">Projektiarvioiden aikajaksoittain tarkasteltavaan näkymään on määritetty valitsemasi aikajanan arviotiedot, jotka näkyvät aikajanalla ruudukkonäkymässä.</span><span class="sxs-lookup"><span data-stu-id="17618-148">The time-phased view of project estimates shows the estimate data from the grid view across the timeline, in a time scale that you select.</span></span> <span data-ttu-id="17618-149">Oletusarvoisesti arviotiedot siirretään **Rooli**-dimensioon.</span><span class="sxs-lookup"><span data-stu-id="17618-149">By default, the estimate data is pivoted on the **Role** dimension.</span></span>

> ![Projektin arvioiden aikavaiheistettu näkymä](media/project-7.png)

## <a name="allocating-estimated-effort-based-on-the-task-mode"></a><span data-ttu-id="17618-151">Arvioidun työmäärän kohdennus tehtävätilaan perustuen</span><span class="sxs-lookup"><span data-stu-id="17618-151">Allocating estimated effort based on the task mode</span></span>

<span data-ttu-id="17618-152">Aikajaksotetussa näkymässä jaat kokonaistyömäärän, joka on arvioitu tehtävälle, kohdentamalla työmäärätunnit yksikköaikajaksolle valitulla aikajanalla.</span><span class="sxs-lookup"><span data-stu-id="17618-152">In the time-phased view, you distribute the total effort that is estimated for the task by allocating effort hours per unit time period in the selected time scale.</span></span> <span data-ttu-id="17618-153">Tehtävätila määrittää, kuinka työmäärä kohdennetaan tehtävän keston ajalle.</span><span class="sxs-lookup"><span data-stu-id="17618-153">The task mode determines how effort is allocated across the duration of the task.</span></span> <span data-ttu-id="17618-154">Kaksi kohdistustapaa ovat **Tasainen** ja **Työtunteihin perustuva**.</span><span class="sxs-lookup"><span data-stu-id="17618-154">The two kinds of allocation are **Even** and **Work hours–based**.</span></span>

### <a name="work-hours-based-allocation"></a><span data-ttu-id="17618-155">Työtunteihin perustuva kohdistus</span><span class="sxs-lookup"><span data-stu-id="17618-155">Work hours-based allocation</span></span>
 
<span data-ttu-id="17618-156">Automaattisesti aikatauluttavassa tehtävätilassa asetetaan päivittäiset oletustunnit tehtäväresursseille täydellä työtuntimäärällä.</span><span class="sxs-lookup"><span data-stu-id="17618-156">In auto-scheduling task mode, the daily default hours for task resources are set at the full work hour rate.</span></span> <span data-ttu-id="17618-157">Tämä tominta pätee, kun työmäärä kohdennetaan jakamalla se tehtävän keston ajalle aikavaiheistetussa näkymässä.</span><span class="sxs-lookup"><span data-stu-id="17618-157">This behavior applies when effort is allocated by splitting it across the duration of the task in the time-phased view.</span></span> <span data-ttu-id="17618-158">Jos esimerkiksi arvioit, että tehtävä suoritetaan loppuun yhdellä resurssilla **Päivä**-aikaskaalalla, päivää kohti kohdennettu työmäärä ei ylitä projektin kalenterissa määritettyjä päiväkohtaisia tunteja.</span><span class="sxs-lookup"><span data-stu-id="17618-158">For example, if you estimate that a task will be completed by one resource in the **Day** time scale, the effort that is allocated per day won't exceed the work hours per day that are defined in the project calendar.</span></span> <span data-ttu-id="17618-159">Työmäärän kohdistus varmistaa siksi aina, että resurssit on arvioitu käytettäviksi koko päivän ajan.</span><span class="sxs-lookup"><span data-stu-id="17618-159">Therefore, the effort allocation always makes sure that the resources are estimated to be used for the full day.</span></span>

### <a name="even-allocation"></a><span data-ttu-id="17618-160">Tasainen kohdistus</span><span class="sxs-lookup"><span data-stu-id="17618-160">Even allocation</span></span>

<span data-ttu-id="17618-161">Manuaalisesti ajoitettuun tehtävätilaan ei käytetä työtunteja projektikalenterista.</span><span class="sxs-lookup"><span data-stu-id="17618-161">In manually scheduled task mode, the work hours from the project calendar aren't used.</span></span> <span data-ttu-id="17618-162">Tehtävän ajoitus perustuu sen sijaan käyttäjän syötteisiin.</span><span class="sxs-lookup"><span data-stu-id="17618-162">Instead, the task schedule is based on user input.</span></span> <span data-ttu-id="17618-163">Tällaisille tehtävillä työmäärän kohdistuksella yksikön aikajaksoa kohti valitulla aikaskaalalla ei ole rajoittavia tekijöitä.</span><span class="sxs-lookup"><span data-stu-id="17618-163">For these tasks, the effort allocation per unit time period in the selected time scale doesn't have any limiting factor.</span></span> <span data-ttu-id="17618-164">Tehtävän kokonaistyömäärä jaetaan ja kohdistetaan jokaiselle yksikön aikajaksolle kohti valitulla aikaskaalalla.</span><span class="sxs-lookup"><span data-stu-id="17618-164">The total effort on the task is equally split and allocated for each unit time period in the selected time scale.</span></span> <span data-ttu-id="17618-165">Näin tehtävässä määritetty tehtävätila määrittää työmäärän jakamista tai kohdistusta yksikön aikajaksoa kohti aikavaiheistetuissa arvioissa.</span><span class="sxs-lookup"><span data-stu-id="17618-165">Therefore, the task mode that is defined on the task determines the effort distribution, or the allocation of effort per unit time period in time-phased estimates.</span></span>

## <a name="grouping-and-time-phasing-options"></a><span data-ttu-id="17618-166">Ryhmittely- ja aikavaiheistusasetukset</span><span class="sxs-lookup"><span data-stu-id="17618-166">Grouping and time-phasing options</span></span>

<span data-ttu-id="17618-167">Aikavaiheistettu näkymä näyttää työmäärän, kustannusten ja myyntiarvioiden jakautumisen päivittäin, viikoittain, kuukausittain tai vuosittain.</span><span class="sxs-lookup"><span data-stu-id="17618-167">The time-phased view shows the distribution of the effort, cost, and sales estimates on a daily, weekly, monthly, or yearly basis.</span></span> <span data-ttu-id="17618-168">Oletusarvoisesti arviotiedot siirretään **Rooli**-dimensioon.</span><span class="sxs-lookup"><span data-stu-id="17618-168">By default, the estimate data is pivoted on the **Role** dimension.</span></span> <span data-ttu-id="17618-169">Voit kuitenkin käyttää **Ryhmittely**-toimintoa ryhmitelläksesi kahden muun dimension avulla: **Luokka** ja **Resurssi**.</span><span class="sxs-lookup"><span data-stu-id="17618-169">However, you can use the **Group By** option to pivot on two other dimensions: **Category** and **Resource**.</span></span>

<span data-ttu-id="17618-170">Voit valita sekä ruudukkonäkymässä että aikavaiheisessa näkymässä näytettävät kentät.</span><span class="sxs-lookup"><span data-stu-id="17618-170">In both the grid view and the time-phased view, you can select which fields are shown.</span></span> <span data-ttu-id="17618-171">Kunkin aikalohkon summat näkyvät projektin alalaidassa.</span><span class="sxs-lookup"><span data-stu-id="17618-171">Totals for each time block are shown at the bottom of the project.</span></span> <span data-ttu-id="17618-172">Ne näyttävät arvioidun kokonaistyömäärän, kustannukset ja myynnin päivälle, viikolle, kuukaudelle tai vuodelle.</span><span class="sxs-lookup"><span data-stu-id="17618-172">They show the total estimated effort, cost, and sales for the day, week, month, or year.</span></span> <span data-ttu-id="17618-173">Oletus kustannushinta ja myyntihinta ovat voimassa.</span><span class="sxs-lookup"><span data-stu-id="17618-173">The default cost price and sales price are date-effective.</span></span> <span data-ttu-id="17618-174">Toisin sanoen ne muuttuvat kunkin resurssin mukaan valitsemasi aikavaiheisen näkymän perusteella.</span><span class="sxs-lookup"><span data-stu-id="17618-174">In other words, they change for each resource, based on the time-phased view that you select.</span></span>

## <a name="expense-estimates"></a><span data-ttu-id="17618-175">Kulujen arviot</span><span class="sxs-lookup"><span data-stu-id="17618-175">Expense estimates</span></span>

<span data-ttu-id="17618-176">**Lisää uusi kuluarvio** -painike ruudukkonäkymässä mahdollistaa sellaisten projektin kulujen kirjaamisen, jotka eivät suoraan liity työvoimaan.</span><span class="sxs-lookup"><span data-stu-id="17618-176">The **Add a New Expense Estimate** button in the grid view lets you record any expenses that are incurred in the project, but that aren't directly related to labor.</span></span> <span data-ttu-id="17618-177">Voit kirjata tietyn tehtävän tai koko projektin kuluarviot.</span><span class="sxs-lookup"><span data-stu-id="17618-177">You can record the expense estimates for a specific task or for the entire project.</span></span> <span data-ttu-id="17618-178">Valitse kul luokat ja alustava päivämäärä, jolloin oletat kulun tapahtuvan.</span><span class="sxs-lookup"><span data-stu-id="17618-178">Select expense categories and the tentative date when you expect to incur the expense.</span></span> <span data-ttu-id="17618-179">Jos liitetyllä kustannushinnastolla ja myyntihinnastolla on oletushinnat (tai hinnankorotuksen prosenttiosuudet määritetään kululuokille), ne asetetaan automaattisesti arvioriville, kun liittäminen tapahtuu.</span><span class="sxs-lookup"><span data-stu-id="17618-179">If the associated cost price list and sales price list have default prices (or if markup percentages are defined for expense categories), they are automatically entered on the estimate line when the association occurs.</span></span>