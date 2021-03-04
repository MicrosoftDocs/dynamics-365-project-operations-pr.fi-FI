---
title: Projektin edistyminen ja toteutuneet kustannukset
description: Tässä aiheessa on tietoja projektin edistymisen ja kustannusten toteutumisen seurannasta.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 08/21/2020
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
ms.openlocfilehash: 0b69cee49e028b98bbb32e4a7e7aedf5479527dc
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/10/2021
ms.locfileid: "5148009"
---
# <a name="project-progress-and-cost-consumption"></a><span data-ttu-id="38165-103">Projektin edistyminen ja toteutuneet kustannukset</span><span class="sxs-lookup"><span data-stu-id="38165-103">Project progress and cost consumption</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="38165-104">Tarve seurata aikataulun edistymistä vaihtelee toimialoittain.</span><span class="sxs-lookup"><span data-stu-id="38165-104">The need to track progress against a schedule varies by industry.</span></span> <span data-ttu-id="38165-105">Joillakin toimialoilla seurataan yksityiskohtaisella tasolla, kun taas muilla toimi loilla seurataan korkeammalla tasolla.</span><span class="sxs-lookup"><span data-stu-id="38165-105">Some industries track at a granular level, whereas other industries track at a higher level.</span></span> <span data-ttu-id="38165-106">Tässä aiheessa kerrotaan, miten voit aikatauluttaa oman organisaatiosi tarpeiden mukaan.</span><span class="sxs-lookup"><span data-stu-id="38165-106">This topic shows how to schedule in order to meet your organization's requirements.</span></span>

## <a name="effort-tracking-view"></a><span data-ttu-id="38165-107">Työmäärän seurantanäkymä</span><span class="sxs-lookup"><span data-stu-id="38165-107">Effort tracking view</span></span>

<span data-ttu-id="38165-108">**Työn seuranta** -näkymä seuraa tehtävien edistymistä aikataulussa.</span><span class="sxs-lookup"><span data-stu-id="38165-108">The **Effort tracking** view tracks the progress of tasks in the schedule.</span></span> <span data-ttu-id="38165-109">Tehtävään käytettyjä työtunteja verrataan tehtävälle suunniteltuihin työtunteihin.</span><span class="sxs-lookup"><span data-stu-id="38165-109">It compares the actual effort hours spent on a task to the task's planned effort hours.</span></span> <span data-ttu-id="38165-110">Project Service Automation laskee seurantamittarit seuraavien kaavojen avulla:</span><span class="sxs-lookup"><span data-stu-id="38165-110">Project Service Automation uses the following formulas to calculate the tracking metrics:</span></span>

<span data-ttu-id="38165-111">Tehtävän luonnissa aluksi: suunniteltujen kustannusten arvoksi tulee arvioidut kustannukset valmistuessa.</span><span class="sxs-lookup"><span data-stu-id="38165-111">Initially on the task creation: Planned cost will be set to the Estimated cost at complete.</span></span> <span data-ttu-id="38165-112">Kun todelliset arvot on tallennettu tehtävään, Seuranta-näkymässä suoritetaan seuraava laskenta työmäärää varten</span><span class="sxs-lookup"><span data-stu-id="38165-112">Once Actuals are recorded on the task, the following will be calculation on the Tracking view for Effort</span></span>

- <span data-ttu-id="38165-113">Edistymisprosentti = Tähän päivämäärään saakka käytetty työmäärä ÷ Arvio valmistumisen hetkellä (EAC)</span><span class="sxs-lookup"><span data-stu-id="38165-113">Progress percentage = Actual effort spent to date ÷ Estimate at complete (EAC)</span></span> 
- <span data-ttu-id="38165-114">Valmistumisarvio (ETC) = Arvio valmistuessa (EAC) – Tähän mennessä käytetty todellinen työmäärä</span><span class="sxs-lookup"><span data-stu-id="38165-114">Estimate to complete (ETC) = Estimate at complete (EAC)  – Actual effort spent to date</span></span> 
- <span data-ttu-id="38165-115">EAC = Jäljellä oleva työmäärä + Tähän päivämäärään saakka käytetty työmäärä</span><span class="sxs-lookup"><span data-stu-id="38165-115">EAC = Remaining effort + Actual effort spent to date</span></span> 
- <span data-ttu-id="38165-116">Ennustettu työmäärän varianssi = Suunniteltu työmäärä – EAC</span><span class="sxs-lookup"><span data-stu-id="38165-116">Projected effort variance = Planned effort – EAC</span></span>

<span data-ttu-id="38165-117">Project Service Automation näyttää tehtävän työmäärän varianssin ennusteen.</span><span class="sxs-lookup"><span data-stu-id="38165-117">Project Service Automation shows a projection of the effort variance on the task.</span></span> <span data-ttu-id="38165-118">Jos EAC on suunniteltua työmäärää enemmän, tehtävän ennustetaan vaativan enemmän aikaa kuin alunperin oli suunniteltu.</span><span class="sxs-lookup"><span data-stu-id="38165-118">If the EAC is more than the planned effort, the task is projected to take more time than was originally planned.</span></span> <span data-ttu-id="38165-119">Siksi se on myöhässä.</span><span class="sxs-lookup"><span data-stu-id="38165-119">Therefore, it's behind schedule.</span></span> <span data-ttu-id="38165-120">Jos EAC on suunniteltua työmäärää vähemmän, tehtävän ennustetaan vaativan vähemmän aikaa kuin alunperin oli suunniteltu.</span><span class="sxs-lookup"><span data-stu-id="38165-120">If the EAC is less than the planned effort, the task is projected to take less time than was originally planned.</span></span> <span data-ttu-id="38165-121">Siksi se on edellä aikataulusta.</span><span class="sxs-lookup"><span data-stu-id="38165-121">Therefore, it's ahead of schedule.</span></span>

## <a name="reprojecting-effort"></a><span data-ttu-id="38165-122">Työmäärän uudelleenprojisoiminen</span><span class="sxs-lookup"><span data-stu-id="38165-122">Reprojecting effort</span></span>

<span data-ttu-id="38165-123">On tavallista, että projektipäällikkö muuttaa tehtävän alkuperäisiä arvioita.</span><span class="sxs-lookup"><span data-stu-id="38165-123">It's common for a project manager to revise the original estimates on a task.</span></span> <span data-ttu-id="38165-124">Projektin uudelleenprojisoinnit ovat projektipäällikön arvioita, joissa otetaan huomioon projektin tämänhetkinen tila.</span><span class="sxs-lookup"><span data-stu-id="38165-124">Project reprojections are a project manager's perception of estimates, given the current state of a project.</span></span> <span data-ttu-id="38165-125">Microsoft ei suosittele perusaikataulun numeroiden muuttamista, koska projektin perusaikataulu on projektin aikataulun ja kustannusarvioiden virallinen lähde, ja projektin kaikki sidosryhmät ovat hyväksyneet sen.</span><span class="sxs-lookup"><span data-stu-id="38165-125">However, we don't recommend that project managers change the baseline numbers, because the project baseline represents the established source of truth for the project's schedule and cost estimate, and all project stakeholders have agreed to it.</span></span>

<span data-ttu-id="38165-126">Projektipäällikkö voi projisoida tehtävien työmäärää uudelleen seuraavilla kahdella tavalla:</span><span class="sxs-lookup"><span data-stu-id="38165-126">There are two ways that a project manager can reproject effort on tasks:</span></span>

- <span data-ttu-id="38165-127">Korvaa oletusarvoinen ETC uudella arviolla tehtävän todellisesta jäljellä olevasta työstä.</span><span class="sxs-lookup"><span data-stu-id="38165-127">Override the default ETC with a new estimate of the actual remaining effort on the task.</span></span> 
- <span data-ttu-id="38165-128">Korvaa oletusarvoinen edistymisprosentti uudella arviolla tehtävän todellisesta edistymisestä.</span><span class="sxs-lookup"><span data-stu-id="38165-128">Override the default progress percentage with a new estimate of the true progress on the task.</span></span>

<span data-ttu-id="38165-129">Kukin näistä lähestymistavoista aiheuttaa tehtävän ETC:n, EAC:n ja edistymisprosentin sekä ennustetun työmäärän varianssin uudelleenlaskennan.</span><span class="sxs-lookup"><span data-stu-id="38165-129">Each of these approaches cause a recalculation of the task's ETC, EAC, and progress percentage, and the projected effort variance on a task.</span></span> <span data-ttu-id="38165-130">Myös yhteenvetotehtävien EAC, ETC ja edistymisprosentti lasketaan uudelleen, ja uusi työmäärän varianssin arvo tuotetaan.</span><span class="sxs-lookup"><span data-stu-id="38165-130">The EAC, ETC, and progress percentage on the summary tasks are also recalculated, and produce a new projection of effort variance.</span></span>

## <a name="reprojection-of-effort-on-summary-tasks"></a><span data-ttu-id="38165-131">Yhteenvetotehtävien työmäärän uudelleenprojisointi</span><span class="sxs-lookup"><span data-stu-id="38165-131">Reprojection of effort on summary tasks</span></span>

<span data-ttu-id="38165-132">Yhteenvetotehtävien tai säiliötehtävien työmäärä voidaan projisoida uudelleen.</span><span class="sxs-lookup"><span data-stu-id="38165-132">Effort on summary tasks or container tasks can be reprojected.</span></span> <span data-ttu-id="38165-133">Riippumatta siitä, uudelleenprojisoiko käyttäjä käyttäen yhteenvetotehtävien jäljellä olevaa työmäärää vai edistymisprosenttia, seuraava laskentajoukko aloitetaan:</span><span class="sxs-lookup"><span data-stu-id="38165-133">Regardless of whether the user reprojects by using the remaining effort or the progress percentage on the summary tasks, the following set of calculations begins:</span></span>

- <span data-ttu-id="38165-134">EAC, ETC ja tehtävän edistymisprosentti lasketaan.</span><span class="sxs-lookup"><span data-stu-id="38165-134">The EAC, ETC, and progress percentage on the task are calculated.</span></span>
- <span data-ttu-id="38165-135">Uusi EAC jaetaan alitehtäviin samassa suhteessa kuin alkuperäinen EAC oli tehtävässä.</span><span class="sxs-lookup"><span data-stu-id="38165-135">The new EAC is distributed down to the child tasks in the same proportion as the original EAC was on the task.</span></span>
- <span data-ttu-id="38165-136">Jokaisen yksittäisen tehtävän valmistumisen kustannusarvio lasketaan lehtisolmutehtäviin asti.</span><span class="sxs-lookup"><span data-stu-id="38165-136">The new EAC on each of the individual tasks down to the leaf node tasks is calculated.</span></span> 
- <span data-ttu-id="38165-137">Alitehtävien, joihin vaikutus ulottuu lehtisolmuissa, ETC ja edistymisprosentti lasketaan uudelleen EAC:n arvoon perustuen.</span><span class="sxs-lookup"><span data-stu-id="38165-137">The affected child tasks down to the leaf nodes have their ETC and progress percentage recalculated based on the EAC value.</span></span> <span data-ttu-id="38165-138">Tuloksena on uusi projektio tehtävän työmäärän varianssista.</span><span class="sxs-lookup"><span data-stu-id="38165-138">This results in a new projection for the effort variance of the task.</span></span> 
- <span data-ttu-id="38165-139">Yhteenvetotehtävien EAC:t lasketaan uudelleen aina juurisolmuun asti.</span><span class="sxs-lookup"><span data-stu-id="38165-139">The EACs of the summary tasks all the way to the root node are recalculated.</span></span>

### <a name="cost-tracking-view"></a><span data-ttu-id="38165-140">Kustannusten seurannan näkymä</span><span class="sxs-lookup"><span data-stu-id="38165-140">Cost tracking view</span></span> 

<span data-ttu-id="38165-141">**Kustannusten seuranta** -näkymä vertaa tehtävän toteutuneita kustannuksia suunniteltuihin kustannuksiin.</span><span class="sxs-lookup"><span data-stu-id="38165-141">The **Cost tracking** view compares the actual cost that was spent on a task to the planned cost.</span></span> 

> [!NOTE]
> <span data-ttu-id="38165-142">Tämä näkymä näyttää vain työvoimakustannukset, eikä se sisällä kuluarvioiden kustannuksia.</span><span class="sxs-lookup"><span data-stu-id="38165-142">This view shows only labor costs and doesn’t include costs from the expense estimates.</span></span> 

<span data-ttu-id="38165-143">Project Service Automation laskee seurantamittarit seuraavien kaavojen avulla:</span><span class="sxs-lookup"><span data-stu-id="38165-143">Project Service Automation uses the following formulas to calculate the tracking metrics:</span></span>

<span data-ttu-id="38165-144">Kun tehtävä luodaan, suunnitellut kustannukset ovat samat kuin arvioidut kustannukset valmistuessa.</span><span class="sxs-lookup"><span data-stu-id="38165-144">When a task is created, the planned cost is equal to the estimated cost at complete.</span></span> <span data-ttu-id="38165-145">Kun todelliset arvot on tallennettu tehtävään, **Seuranta**-näkymässä suoritetaan seuraava laskenta kustannusta varten:</span><span class="sxs-lookup"><span data-stu-id="38165-145">After actuals are recorded on the task, the following is calculated on the **Tracking** view for cost:</span></span>

 - <span data-ttu-id="38165-146">Toteutuneiden kustannusten prosenttiosuus = Toteutuneet kustannukset tähän päivämäärään asti ÷ Tehtävän arvioidut kustannukset valmistuessa</span><span class="sxs-lookup"><span data-stu-id="38165-146">Percentage of cost consumed = Actual cost spent to date ÷ Estimated cost at complete for the task</span></span>
 - <span data-ttu-id="38165-147">Kustannukset valmistuessa (CTC) = Arvioidut kustannukset valmistuessa – Tähän päivämäärään saakka toteutuneet kustannukset</span><span class="sxs-lookup"><span data-stu-id="38165-147">Cost to complete (CTC) = Estimated cost at complete – Actual cost spent to date</span></span>
 - <span data-ttu-id="38165-148">Kustannukset valmistuessa = CTC + Tähän päivämäärään saakka toteutuneet kustannukset</span><span class="sxs-lookup"><span data-stu-id="38165-148">Estimated cost at complete = CTC + Actual cost spent to date</span></span>
 - <span data-ttu-id="38165-149">Arvioidun kustannuksen varianssi = Suunniteltu kustannus – arvioidut kustannukset valmistuessa</span><span class="sxs-lookup"><span data-stu-id="38165-149">Projected cost variance = Planned cost – Estimated cost at complete</span></span>

<span data-ttu-id="38165-150">Kustannusten varianssin ennuste näytetään tehtävässä.</span><span class="sxs-lookup"><span data-stu-id="38165-150">A projection of the cost variance is shown on the task.</span></span> <span data-ttu-id="38165-151">Jos arvioitu kustannus valmistuessa on suunniteltuja kustannuksia enemmän, tehtävän ennustetaan maksavan enemmän kuin alunperin oli suunniteltu.</span><span class="sxs-lookup"><span data-stu-id="38165-151">If the estimated cost at complete is more than the planned cost, the task is projected to cost more than was originally planned.</span></span> <span data-ttu-id="38165-152">Siksi se on suuntautunut budjetin ylittämiseen.</span><span class="sxs-lookup"><span data-stu-id="38165-152">Therefore, it's trending over budget.</span></span> <span data-ttu-id="38165-153">Jos arvioitu kustannus valmistuessa on suunniteltuja kustannuksia vähemmän, tehtävän ennustetaan maksavan vähemmän kuin alunperin oli suunniteltu ja suunta on alle budjetin.</span><span class="sxs-lookup"><span data-stu-id="38165-153">If the Estimated cost at complete is less than the planned cost, the task is projected to cost less than was originally planned and is trending under budget.</span></span>

## <a name="project-managers-reprojection-of-cost"></a><span data-ttu-id="38165-154">Projektipäällikön kustannusten uudelleenprojektio</span><span class="sxs-lookup"><span data-stu-id="38165-154">Project manager’s reprojection of cost</span></span>

<span data-ttu-id="38165-155">Kun työmäärä projektoidaan uudelleen, CTC, arvioitu kustannus valmistuessa, kustannusten toteutumisprosentti ja ennustettu kustannusten varianssi lasketaan kaikki uudelleen **Kustannusten seuranta** -näkymässä.</span><span class="sxs-lookup"><span data-stu-id="38165-155">When effort is reprojected, the CTC, Estimated cost at complete, percentage of cost consumed, and projected cost variance are all recalculated in the **Cost tracking** view.</span></span>

## <a name="project-status-summary"></a><span data-ttu-id="38165-156">Projektin tilan yhteenveto</span><span class="sxs-lookup"><span data-stu-id="38165-156">Project status summary</span></span>

<span data-ttu-id="38165-157">Seurantatiedot **Työmäärän seuranta**- ja **Kustannusten seuranta** -näkymissä näyttävät edistymisen ja toteutuneet kustannukset projektin juurisolmun, yhteenvetotehtävien ja lehtisolmujen tasoilla.</span><span class="sxs-lookup"><span data-stu-id="38165-157">Tracking data in the **Effort tracking** and **Cost tracking** views shows the progress and cost consumption at the project root node, summary tasks, and leaf node tasks levels.</span></span> <span data-ttu-id="38165-158">**Tila**-osio **Projektikohde**-sivulla näyttää yhteenvedon projektitason tilasta.</span><span class="sxs-lookup"><span data-stu-id="38165-158">The **Status** section on the **Project entity** page shows a summary of project-level status.</span></span>

## <a name="status-summary-fields"></a><span data-ttu-id="38165-159">Tilan yhteenvetokentät</span><span class="sxs-lookup"><span data-stu-id="38165-159">Status summary fields</span></span>

<span data-ttu-id="38165-160">**Projektin kokonaistila** -kenttä on muokattava kenttä, joka näyttää projektin kokonaistilan.</span><span class="sxs-lookup"><span data-stu-id="38165-160">The **Overall project status** field is an editable field that shows the overall status of the project.</span></span> <span data-ttu-id="38165-161">Se käyttää värikoodausta, kuten vihreää, keltaista ja punaista, osoittamaan lisääntyvää riskiä.</span><span class="sxs-lookup"><span data-stu-id="38165-161">It uses color-coding, such as green, yellow, and red, to indicate increasing risk.</span></span> <span data-ttu-id="38165-162">**Kommentit** -kentän avulla projektipäällikkö voi syöttää tilaan liittyviä kommentteja.</span><span class="sxs-lookup"><span data-stu-id="38165-162">The **Comments** field lets the project manager enter specific comments about the status.</span></span> <span data-ttu-id="38165-163">**Tila päivitetty** -kenttää ei voi muokata, ja sen arvo on aik leima, joka ilmaisee, milloin tila on viimeksi päivitetty.</span><span class="sxs-lookup"><span data-stu-id="38165-163">The **Status updated on** field is not editable and the value is a timestamp that indicates when the status was last updated.</span></span>

<span data-ttu-id="38165-164">**Aikataulun tehokkuus** - ja **Kustannustehokkuus**-kentät määritetään seurantapäivänä.</span><span class="sxs-lookup"><span data-stu-id="38165-164">The **Schedule performance** and **Cost performance** fields are set from the tracking date.</span></span> <span data-ttu-id="38165-165">Kun aikataulun ja kustannusten varianssi juurisolmussa **Työmäärän seuranta** -näkymässä ovat positiivisia, voit asettaa näiden kenttien arvoksi **Edellä**.</span><span class="sxs-lookup"><span data-stu-id="38165-165">When the schedule and cost variance for the root node in the **Effort tracking** view are positive, you can set these fields to **Ahead**.</span></span> <span data-ttu-id="38165-166">Kun pääsolmun aikataulun ja kustasten varianssi juurisolmussa on negatiivinen, voit määrittää niiden arvoksi **Jäljessä**.</span><span class="sxs-lookup"><span data-stu-id="38165-166">When the schedule and cost variance for the root node are negative, you can set them to **Behind**.</span></span>
