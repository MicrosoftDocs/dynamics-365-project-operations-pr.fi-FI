---
title: Projektin edistyminen ja toteutuneet kustannukset
description: Tässä aiheessa on tietoja siitä, miten projektin edistymistä ja kustannusten toteutumista voidaan seurata.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: 0d742164-5469-421d-8917-63160a81f651
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 8aa5814938129f30885d8161a7c86197ab013364
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/24/2020
ms.locfileid: "3751233"
---
# <a name="project-progress-and-cost-consumption"></a><span data-ttu-id="c8a7e-103">Projektin edistyminen ja toteutuneet kustannukset</span><span class="sxs-lookup"><span data-stu-id="c8a7e-103">Project progress and cost consumption</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="c8a7e-104">Tarve seurata aikataulun edistymistä vaihtelee toimialoittain.</span><span class="sxs-lookup"><span data-stu-id="c8a7e-104">The need to track progress against a schedule varies by industry.</span></span> <span data-ttu-id="c8a7e-105">Joillakin toimialoilla seurataan yksityiskohtaisella tasolla, kun taas muilla toimi loilla seurataan korkeammalla tasolla.</span><span class="sxs-lookup"><span data-stu-id="c8a7e-105">Some industries track at a granular level, whereas other industries track at a higher level.</span></span> <span data-ttu-id="c8a7e-106">Tässä aiheessa kerrotaan, miten voit aikatauluttaa oman organisaatiosi tarpeiden mukaan.</span><span class="sxs-lookup"><span data-stu-id="c8a7e-106">This topic shows how to schedule in order to meet your organization's requirements.</span></span>

## <a name="effort-tracking-view"></a><span data-ttu-id="c8a7e-107">Työmäärän seurantanäkymä</span><span class="sxs-lookup"><span data-stu-id="c8a7e-107">Effort tracking view</span></span>

<span data-ttu-id="c8a7e-108">**Työn seuranta** -näkymä seuraa tehtävien edistymistä aikataulussa.</span><span class="sxs-lookup"><span data-stu-id="c8a7e-108">The **Effort tracking** view tracks the progress of tasks in the schedule.</span></span> <span data-ttu-id="c8a7e-109">Se vertailee tehtävään käytettyjä toteutuneita työtunteja tehtävälle suunniteltuihin työtunteihin.</span><span class="sxs-lookup"><span data-stu-id="c8a7e-109">It compares the actual effort hours that have been spent on a task to the planned effort hours for that task.</span></span> <span data-ttu-id="c8a7e-110">PSA laskee seurantamittarit seuraavien kaavojen avulla:</span><span class="sxs-lookup"><span data-stu-id="c8a7e-110">PSA uses the following formulas to calculate the tracking metrics:</span></span>

- <span data-ttu-id="c8a7e-111">Edistymisprosentti = Todellinen tähän päivämäärään saakka käytetty työmäärä ÷ Tehtävälle suunniteltu työmäärä</span><span class="sxs-lookup"><span data-stu-id="c8a7e-111">Progress percentage = Actual effort spent to date ÷ Planned effort for the task</span></span> 
- <span data-ttu-id="c8a7e-112">Valmistumisarvio (ETC) = Suunniteltu työmäärä – Tähän päivämäärään saakka käytetty työmäärä</span><span class="sxs-lookup"><span data-stu-id="c8a7e-112">Estimate to complete (ETC) = Planned effort – Actual effort spent to date</span></span> 
- <span data-ttu-id="c8a7e-113">Arvio valmistumisen hetkellä (EAC) = Jäljellä oleva työmäärä + Tähän päivämäärään saakka käytetty työmäärä</span><span class="sxs-lookup"><span data-stu-id="c8a7e-113">Estimate at complete (EAC) = Remaining effort + Actual effort spent to date</span></span> 
- <span data-ttu-id="c8a7e-114">Ennustettu työmäärän varianssi = Suunniteltu työmäärä – EAC</span><span class="sxs-lookup"><span data-stu-id="c8a7e-114">Projected effort variance = Planned effort – EAC</span></span>

<span data-ttu-id="c8a7e-115">PSA näyttää tehtävän työmäärän varianssin ennusteen.</span><span class="sxs-lookup"><span data-stu-id="c8a7e-115">PSA shows a projection of the effort variance on the task.</span></span> <span data-ttu-id="c8a7e-116">Jos EAC on suunniteltua työmäärää enemmän, tehtävän ennustetaan vaativan enemmän aikaa kuin alunperin oli suunniteltu.</span><span class="sxs-lookup"><span data-stu-id="c8a7e-116">If the EAC is more than the planned effort, the task is projected to take more time than was originally planned.</span></span> <span data-ttu-id="c8a7e-117">Siksi se on myöhässä.</span><span class="sxs-lookup"><span data-stu-id="c8a7e-117">Therefore, it's behind schedule.</span></span> <span data-ttu-id="c8a7e-118">Jos EAC on suunniteltua työmäärää vähemmän, tehtävän ennustetaan vaativan vähemmän aikaa kuin alunperin oli suunniteltu.</span><span class="sxs-lookup"><span data-stu-id="c8a7e-118">If the EAC is less than the planned effort, the task is projected to take less time than was originally planned.</span></span> <span data-ttu-id="c8a7e-119">Siksi se on edellä aikataulusta.</span><span class="sxs-lookup"><span data-stu-id="c8a7e-119">Therefore, it's ahead of schedule.</span></span>

## <a name="re-projecting-effort"></a><span data-ttu-id="c8a7e-120">Työmäärän uudelleenprojisoiminen</span><span class="sxs-lookup"><span data-stu-id="c8a7e-120">Re-projecting effort</span></span>

<span data-ttu-id="c8a7e-121">On tavallista, että projektipäällikkö muuttaa tehtävän alkuperäisiä arvioita.</span><span class="sxs-lookup"><span data-stu-id="c8a7e-121">It's common for a project manager to revise the original estimates on a task.</span></span> <span data-ttu-id="c8a7e-122">Projektin ennusteet ovat projektipäällikön arvioita, joissa otetaan huomioon projektin tämänhetkinen tila.</span><span class="sxs-lookup"><span data-stu-id="c8a7e-122">Project re-projections are a project manager's perception of estimates, given the current state of a project.</span></span> <span data-ttu-id="c8a7e-123">Microsoft ei suosittele perusaikataulun numeroiden muuttamista, koska projektin perusaikataulu on projektin aikataulun ja kustannusarvioiden virallinen lähde, ja projektin kaikki sidosryhmät ovat hyväksyneet sen.</span><span class="sxs-lookup"><span data-stu-id="c8a7e-123">However, we don't recommend that project managers change the baseline numbers, because the project baseline represents the established source of truth for the project's schedule and cost estimate, and all project stakeholders have agreed to it.</span></span>

<span data-ttu-id="c8a7e-124">Projektipäällikkö voi projisoida tehtävien työmäärää uudelleen seuraavilla kahdella tavalla:</span><span class="sxs-lookup"><span data-stu-id="c8a7e-124">There are two ways that a project manager can re-project effort on tasks:</span></span>

- <span data-ttu-id="c8a7e-125">Korvaa oletusarvoinen ETC uudella arviolla tehtävän todellisesta jäljellä olevasta työstä.</span><span class="sxs-lookup"><span data-stu-id="c8a7e-125">Override the default ETC with a new estimate of the actual remaining effort on the task.</span></span> 
- <span data-ttu-id="c8a7e-126">Korvaa oletusarvoinen edistymisprosentti uudella arviolla tehtävän todellisesta edistymisestä.</span><span class="sxs-lookup"><span data-stu-id="c8a7e-126">Override the default progress percentage with a new estimate of the true progress on the task.</span></span>

<span data-ttu-id="c8a7e-127">Kukin näistä lähestymistavoista aiheuttaa tehtävän ETC:n, EAC:n ja edistymisprosentin sekä ennustetun työmäärän varianssin uudelleenlaskennan.</span><span class="sxs-lookup"><span data-stu-id="c8a7e-127">Each of these approaches cause a recalculation of the task's ETC, EAC, and progress percentage, and the projected effort variance on a task.</span></span> <span data-ttu-id="c8a7e-128">Myös yhteenvetotehtävien EAC, ETC ja edistymisprosentti lasketaan uudelleen, ja uusi työmäärän varianssin arvo tuotetaan.</span><span class="sxs-lookup"><span data-stu-id="c8a7e-128">The EAC, ETC, and progress percentage on the summary tasks are also recalculated, and produce a new projection of effort variance.</span></span>

## <a name="re-projection-of-effort-on-summary-tasks"></a><span data-ttu-id="c8a7e-129">Yhteenvetotehtävien työmäärän uudelleenprojisointi</span><span class="sxs-lookup"><span data-stu-id="c8a7e-129">Re-projection of effort on summary tasks</span></span>

<span data-ttu-id="c8a7e-130">Yhteenvetotehtävien tai säiliötehtävien työmäärä voidaan projisoida uudelleen.</span><span class="sxs-lookup"><span data-stu-id="c8a7e-130">Effort on summary tasks or container tasks can be re-projected.</span></span> <span data-ttu-id="c8a7e-131">Riippumatta siitä, uudelleenprojisoiko käyttäjä käyttäen yhteenvetotehtävien jäljellä olevaa työmäärää vai edistymisprosenttia, seuraava laskentajoukko aloitetaan:</span><span class="sxs-lookup"><span data-stu-id="c8a7e-131">Regardless of whether the user re-projects by using the remaining effort or the progress percentage on the summary tasks, the following set of calculations begins:</span></span>

- <span data-ttu-id="c8a7e-132">EAC, ETC ja tehtävän edistymisprosentti lasketaan.</span><span class="sxs-lookup"><span data-stu-id="c8a7e-132">The EAC, ETC, and progress percentage on the task are calculated.</span></span>
- <span data-ttu-id="c8a7e-133">Uusi EAC jaetaan alitehtäviin samassa suhteessa kuin alkuperäinen EAC oli tehtävässä.</span><span class="sxs-lookup"><span data-stu-id="c8a7e-133">The new EAC is distributed down to the child tasks in the same proportion as the original EAC was on the task.</span></span>
- <span data-ttu-id="c8a7e-134">Jokaisen yksittäisen tehtävän EAC aina lehtisolmutehtäviin asti lasketaan.</span><span class="sxs-lookup"><span data-stu-id="c8a7e-134">The new EAC on each of the individualt tasks down to the leaf node tasks is calculated.</span></span> 
- <span data-ttu-id="c8a7e-135">Alitehtävien, joihin vaikutus ulottuu lehtisolmuissa, ETC ja edistymisprosentti lasketaan uudelleen EAC:n arvoon perustuen.</span><span class="sxs-lookup"><span data-stu-id="c8a7e-135">The affected child tasks down to the leaf nodes have their ETC and progress percentage recalculated based on the EAC value.</span></span> <span data-ttu-id="c8a7e-136">Tuloksena on uusi projektio tehtävän työmäärän varianssista.</span><span class="sxs-lookup"><span data-stu-id="c8a7e-136">This results in a new projection for the effort variance of the task.</span></span> 
- <span data-ttu-id="c8a7e-137">Yhteenvetotehtävien EAC:t lasketaan uudelleen aina juurisolmuun asti.</span><span class="sxs-lookup"><span data-stu-id="c8a7e-137">The EACs of the summary tasks all the way to the root node are recalculated.</span></span>

### <a name="cost-tracking-view"></a><span data-ttu-id="c8a7e-138">Kustannusten seurannan näkymä</span><span class="sxs-lookup"><span data-stu-id="c8a7e-138">Cost tracking view</span></span> 

<span data-ttu-id="c8a7e-139">**Kustannusten seuranta** -näkymä vertaa tehtävän toteutuneita kustannuksia tehtävälle suunniteltuihin kustannuksiin.</span><span class="sxs-lookup"><span data-stu-id="c8a7e-139">The **Cost tracking** view compares the actual cost that was spent on a task to the planned cost on a task.</span></span> 

> [!NOTE]
> <span data-ttu-id="c8a7e-140">Tämä näkymä näyttää vain työvoimakustannukset, eikä se sisällä kuluarvioiden kustannuksia.</span><span class="sxs-lookup"><span data-stu-id="c8a7e-140">This view shows only labor costs and doesn’t include costs from the expense estimates.</span></span> 

<span data-ttu-id="c8a7e-141">PSA laskee seurantamittarit seuraavien kaavojen avulla:</span><span class="sxs-lookup"><span data-stu-id="c8a7e-141">PSA uses the following formulas to calculate the tracking metrics:</span></span>

- <span data-ttu-id="c8a7e-142">Toteutuneiden kustannusten prosenttiosuus = Toteutuneet kustannukset tähän päivämäärään asti ÷ Tehtävän suunnitellut kustannukset</span><span class="sxs-lookup"><span data-stu-id="c8a7e-142">Percentage of cost consumed = Actual cost spent to date ÷ Planned cost for the task</span></span>
- <span data-ttu-id="c8a7e-143">Kustannukset valmistuessa (CTC) = Suunnitellut kustannukset – Tähän päivämäärään saakka toteutuneet kustannukset</span><span class="sxs-lookup"><span data-stu-id="c8a7e-143">Cost to complete (CTC) = Planned cost – Actual cost spent to date</span></span>
- <span data-ttu-id="c8a7e-144">EAC = CTC + Toteutuneet kustannukset tähän päivämäärään saakka</span><span class="sxs-lookup"><span data-stu-id="c8a7e-144">EAC = CTC + Actual cost spent to date</span></span>
- <span data-ttu-id="c8a7e-145">Arvioitujen kustannusten varianssi = Suunnitellut kustannukset – EAC</span><span class="sxs-lookup"><span data-stu-id="c8a7e-145">Projected cost variance = Planned cost – EAC</span></span>

<span data-ttu-id="c8a7e-146">Kustannusten varianssin ennuste näytetään tehtävässä.</span><span class="sxs-lookup"><span data-stu-id="c8a7e-146">A projection of the cost variance is shown on the task.</span></span> <span data-ttu-id="c8a7e-147">Jos EAC on suunniteltuja kustannuksia enemmän, tehtävän ennustetaan maksavan enemmän kuin alunperin oli suunniteltu.</span><span class="sxs-lookup"><span data-stu-id="c8a7e-147">If the EAC is more than the planned cost, the task is projected to cost more than was originally planned.</span></span> <span data-ttu-id="c8a7e-148">Siksi se on suuntautunut budjetin ylittämiseen.</span><span class="sxs-lookup"><span data-stu-id="c8a7e-148">Therefore, it's trending over budget.</span></span> <span data-ttu-id="c8a7e-149">Jos EAC on suunniteltuja kustannuksia vähemmän, tehtävän ennustetaan maksavan vähemmän kuin alunperin oli suunniteltu.</span><span class="sxs-lookup"><span data-stu-id="c8a7e-149">If the EAC is less than the planned cost, the task is projected to cost less than was originally planned.</span></span> <span data-ttu-id="c8a7e-150">Siksi se on suuntautunut budjetin alittamiseen.</span><span class="sxs-lookup"><span data-stu-id="c8a7e-150">Therefore, it's trending under budget.</span></span>

## <a name="project-managers-re-projection-of-cost"></a><span data-ttu-id="c8a7e-151">Projektipäällikön kustannusten uudelleenprojektio</span><span class="sxs-lookup"><span data-stu-id="c8a7e-151">Project manager’s re-projection of cost</span></span>

<span data-ttu-id="c8a7e-152">Kun työmäärä projektoidaan uudelleen, CTC, EAC, kustannusten toteutumisprosentti ja ennustettu kustannusten varianssi lasketaan kaikki uudelleen **Kustannusten seuranta** -näkymässä.</span><span class="sxs-lookup"><span data-stu-id="c8a7e-152">When effort is re-projected, the CTC, EAC, percentage of cost consumed, and projected cost variance are all recalculated in the **Cost tracking** view.</span></span>

## <a name="project-status-summary"></a><span data-ttu-id="c8a7e-153">Projektin tilan yhteenveto</span><span class="sxs-lookup"><span data-stu-id="c8a7e-153">Project status summary</span></span>

<span data-ttu-id="c8a7e-154">Seurantatiedot **Työmäärän seuranta**- ja **Kustannusten seuranta** -näkymissä näyttävät edistymisen ja toteutuneet kustannukset projektin juurisolmun, yhteenvetotehtävien ja lehtisolmujen tasoilla.</span><span class="sxs-lookup"><span data-stu-id="c8a7e-154">Tracking data in the **Effort tracking** and **Cost tracking** views shows the progress and cost consumption at the project root node, summary tasks, and leaf node tasks levels.</span></span> <span data-ttu-id="c8a7e-155">**Tila**-osio **Projektikohde**-sivulla näyttää yhteenvedon projektitason tilasta.</span><span class="sxs-lookup"><span data-stu-id="c8a7e-155">The **Status** section on the **Project entity** page shows a summary of project-level status.</span></span>

## <a name="status-summary-fields"></a><span data-ttu-id="c8a7e-156">Tilan yhteenvetokentät</span><span class="sxs-lookup"><span data-stu-id="c8a7e-156">Status summary fields</span></span>

<span data-ttu-id="c8a7e-157">**Projektin kokonaistila** -kenttä on muokattava kenttä, joka näyttää projektin kokonaistilan.</span><span class="sxs-lookup"><span data-stu-id="c8a7e-157">The **Overall project status** field is an editable field that shows the overall status of the project.</span></span> <span data-ttu-id="c8a7e-158">Se käyttää värikoodausta, kuten vihreää, keltaista ja punaista, osoittamaan lisääntyvää riskiä.</span><span class="sxs-lookup"><span data-stu-id="c8a7e-158">It uses color-coding, such as green, yellow, and red, to indicate increasing risk.</span></span> <span data-ttu-id="c8a7e-159">**Kommentit** -kentän avulla projektipäällikkö voi syöttää tilaan liittyviä kommentteja.</span><span class="sxs-lookup"><span data-stu-id="c8a7e-159">The **Comments** field lets the project manager enter specific comments about the status.</span></span> <span data-ttu-id="c8a7e-160">**Tila päivitetty** -kenttää ei voi muokata, ja sen arvo on aik leima, joka ilmaisee, milloin tila on viimeksi päivitetty.</span><span class="sxs-lookup"><span data-stu-id="c8a7e-160">The **Status updated on** field is not editable and the value is a timestamp that indicates when the status was last updated.</span></span>

<span data-ttu-id="c8a7e-161">**Aikataulun tehokkuus** - ja **Kustannustehokkuus**-kentät määritetään seurantapäivänä.</span><span class="sxs-lookup"><span data-stu-id="c8a7e-161">The **Schedule performance** and **Cost performance** fields are set from the tracking date.</span></span> <span data-ttu-id="c8a7e-162">Kun aikataulun ja kustannusten varianssi juurisolmussa **Työmäärän seuranta** -näkymässä ovat positiivisia, voit asettaa näiden kenttien arvoksi **Edellä**.</span><span class="sxs-lookup"><span data-stu-id="c8a7e-162">When the schedule and cost variance for the root node in the **Effort tracking** view are positive, you can set these fields to **Ahead**.</span></span> <span data-ttu-id="c8a7e-163">Kun pääsolmun aikataulun ja kustasten varianssi juurisolmussa on negatiivinen, voit määrittää niiden arvoksi **Jäljessä**.</span><span class="sxs-lookup"><span data-stu-id="c8a7e-163">When the schedule and cost variance for the root node are negative, you can set them to **Behind**.</span></span>
