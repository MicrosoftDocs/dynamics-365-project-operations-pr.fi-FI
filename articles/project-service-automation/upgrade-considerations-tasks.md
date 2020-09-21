---
title: Työrakenteen päivitykseen liittyvät seikat
description: Tässä aihe on tietoja työrakenteen päivittämisestä Project Service Automation 2.x:n ja 3.x:n välillä.
manager: kfend
ms.service: business-applications
ms.custom:
- dyn365-projectservice
ms.date: 10/18/2019
ms.topic: article
ms.prod: ''
ms.technology: Dynamics 365 Project Service Automation 2.x
author: ruhercul
ms.assetid: 9e43d5b5-ca5d-41f5-9012-c48f8e3080f9
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 9aa35dd8784bfa55737b0836e653afd0442b80c2
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/24/2020
ms.locfileid: "3751211"
---
# <a name="upgrade-considerations-for-the-work-breakdown-structure"></a><span data-ttu-id="281b3-103">Työrakenteen päivitykseen liittyvät seikat</span><span class="sxs-lookup"><span data-stu-id="281b3-103">Upgrade considerations for the work breakdown structure</span></span>
<span data-ttu-id="281b3-104">Tässä aihe on tietoja työrakenteen päivittämisestä Project Service Automation 2.x:n ja 3.x:n välillä.</span><span class="sxs-lookup"><span data-stu-id="281b3-104">This topic provides information about upgrading the work breakdown structure from Project Service Automation 2.x to 3.x.</span></span> <span data-ttu-id="281b3-105">Tämä aihe määrittää project Service Automation (PSA) -projektin terveen tilan, jota päivityksen onnistuminen edellyttää.</span><span class="sxs-lookup"><span data-stu-id="281b3-105">This topic defines the healthy state of a project in Project Service Automation (PSA) that is required for a successful upgrade.</span></span> <span data-ttu-id="281b3-106">Siinä on myös tietoja yleisistä estoehdoista, jotka aiheuttavat päivityksen epäonnistumisen.</span><span class="sxs-lookup"><span data-stu-id="281b3-106">There is also information about the common blocking conditions that will cause upgrade to fail.</span></span> <span data-ttu-id="281b3-107">Lisätietoja projektitehtävien ja niiden toimintojen määrittämisestä projektiaikataulussa on aiheessa [Projektiaikataulut](project-creating.md).</span><span class="sxs-lookup"><span data-stu-id="281b3-107">For more information about defining project tasks and their functions within a project schedule, see [Project schedules](project-creating.md).</span></span>

## <a name="key-entities"></a><span data-ttu-id="281b3-108">Avainentiteetit</span><span class="sxs-lookup"><span data-stu-id="281b3-108">Key entities</span></span>
<span data-ttu-id="281b3-109">Seuraavat entiteetit vaaditaan tarkkaa työrakennetta varten, jossa on jo resursseja:</span><span class="sxs-lookup"><span data-stu-id="281b3-109">For an accurate work breakdown structure that is already loaded with resources, the following entities are required:</span></span>

- [<span data-ttu-id="281b3-110">Projekti</span><span class="sxs-lookup"><span data-stu-id="281b3-110">Project</span></span>](../developer/entities/msdyn_project.md)
- [<span data-ttu-id="281b3-111">Projektiryhmä</span><span class="sxs-lookup"><span data-stu-id="281b3-111">Project Team</span></span>](../developer/entities/msdyn_projectteam.md)
- [<span data-ttu-id="281b3-112">Projektin tehtävä</span><span class="sxs-lookup"><span data-stu-id="281b3-112">Project Task</span></span>](../developer/entities/msdyn_projecttask.md)
- [<span data-ttu-id="281b3-113">Resurssimääritykset</span><span class="sxs-lookup"><span data-stu-id="281b3-113">Resource Assignments</span></span>](../developer/entities/msdyn_resourceassignment.md)
- [<span data-ttu-id="281b3-114">Projektitehtävän riippuvuus</span><span class="sxs-lookup"><span data-stu-id="281b3-114">Project Task Dependency</span></span>](../developer/entities/msdyn_projecttaskdependency.md)
- [<span data-ttu-id="281b3-115">Varattavissa olevat resurssit</span><span class="sxs-lookup"><span data-stu-id="281b3-115">Bookable Resources</span></span>](../developer/entities/bookableresource.md)

<span data-ttu-id="281b3-116">Voit määrittää työrakenteen, jossa on resurssit, tekemällä seuraavat toimet:</span><span class="sxs-lookup"><span data-stu-id="281b3-116">To define a resource loaded work breakdown structure, you must complete the following steps:</span></span>

1. <span data-ttu-id="281b3-117">Luo uusi projekti.</span><span class="sxs-lookup"><span data-stu-id="281b3-117">Create a new project.</span></span> <span data-ttu-id="281b3-118">Lisätietoja uuden projektin luomisesta on aiheessa [msdyn_project](../developer/entities/msdyn_project.md).</span><span class="sxs-lookup"><span data-stu-id="281b3-118">For more information about how to create a new project, see [msdyn_project](../developer/entities/msdyn_project.md).</span></span>
2. <span data-ttu-id="281b3-119">Luo yksi tai useampia tehtäviä.</span><span class="sxs-lookup"><span data-stu-id="281b3-119">Create one or more tasks.</span></span> <span data-ttu-id="281b3-120">Lisätietoja tehtävän luomisesta on aiheessa [msdyn_projecttask](../developer/entities/msdyn_projecttask.md).</span><span class="sxs-lookup"><span data-stu-id="281b3-120">For more information about how to create a task, see [msdyn_projecttask](../developer/entities/msdyn_projecttask.md).</span></span>
3. <span data-ttu-id="281b3-121">Määritä tehtäväriippuvuudet.</span><span class="sxs-lookup"><span data-stu-id="281b3-121">Define the task dependencies.</span></span> <span data-ttu-id="281b3-122">Lisätietoja on kohdassa [projektitehtävien riippuvuus](../developer/entities/msdyn_projecttaskdependency.md).</span><span class="sxs-lookup"><span data-stu-id="281b3-122">For more information, see [Project Task Dependency](../developer/entities/msdyn_projecttaskdependency.md).</span></span>
4. <span data-ttu-id="281b3-123">Kohdenna projektiryhmän jäsenet projektiin.</span><span class="sxs-lookup"><span data-stu-id="281b3-123">Assign project team members to the project.</span></span> <span data-ttu-id="281b3-124">Lisätietoja on aiheessa [msdyn_projectteam](../developer/entities/msdyn_projectteam.md).</span><span class="sxs-lookup"><span data-stu-id="281b3-124">For more information, see [msdyn_projectteam](../developer/entities/msdyn_projectteam.md).</span></span>
5. <span data-ttu-id="281b3-125">Kohdenna projektiryhmän jäsenet tehtäviin.</span><span class="sxs-lookup"><span data-stu-id="281b3-125">Assign project team members to the tasks.</span></span> <span data-ttu-id="281b3-126">Lisätietoja on aiheessa [msdyn_resourceassignment](../developer/entities/msdyn_resourceassignment.md).</span><span class="sxs-lookup"><span data-stu-id="281b3-126">For more information, see [msdyn_resourceassignment](../developer/entities/msdyn_resourceassignment.md).</span></span>

## <a name="project-team-relationships"></a><span data-ttu-id="281b3-127">Projektiryhmän suhteet</span><span class="sxs-lookup"><span data-stu-id="281b3-127">Project team relationships</span></span>

<span data-ttu-id="281b3-128">Onnistuneen päivityksen varmistamiseksi seuraavat suhteet on säilytettävä oikein:</span><span class="sxs-lookup"><span data-stu-id="281b3-128">To ensure a successful upgrade, the following relationships must be correctly maintained:</span></span>
- <span data-ttu-id="281b3-129">Kaikkien projektiryhmän jäsenten on oltava liitettyinä varattavissa olevaan resurssiin.</span><span class="sxs-lookup"><span data-stu-id="281b3-129">All project team members must be associated with a bookable resource.</span></span>
- <span data-ttu-id="281b3-130">Kaikkien projektiryhmän jäsenten on oltava liitettyinä samaan projektiin.</span><span class="sxs-lookup"><span data-stu-id="281b3-130">All project team members must be associated with the same project.</span></span> 

## <a name="project-task-relationships"></a><span data-ttu-id="281b3-131">Projektitehtävän suhteet</span><span class="sxs-lookup"><span data-stu-id="281b3-131">Project task relationships</span></span>
<span data-ttu-id="281b3-132">Onnistuneen päivityksen varmistamiseksi seuraavat suhteet on säilytettävä oikein:</span><span class="sxs-lookup"><span data-stu-id="281b3-132">To ensure a successful upgrade, the following relationships must be correctly maintained:</span></span>

- <span data-ttu-id="281b3-133">Liittyvät tehtävät on liitettävä samaan projektiin.</span><span class="sxs-lookup"><span data-stu-id="281b3-133">Any related tasks must be associated with the same project.</span></span>
- <span data-ttu-id="281b3-134">Jokaisella rivitehtävällä on oltava päätehtävä.</span><span class="sxs-lookup"><span data-stu-id="281b3-134">Every line task must have a parent task.</span></span>
- <span data-ttu-id="281b3-135">Jokaisella tehtävällä on oltava projekti.</span><span class="sxs-lookup"><span data-stu-id="281b3-135">Every task must have a parent project.</span></span>

### <a name="valid-conditions"></a><span data-ttu-id="281b3-136">Kelvolliset ehdot</span><span class="sxs-lookup"><span data-stu-id="281b3-136">Valid conditions</span></span>

- <span data-ttu-id="281b3-137">Kaikkien tehtävien keston on oltava suurempi tai yhtä suuri kuin (> =) 1 tunti ja alle 1 800 000 minuuttia (1 250 päivää). \*</span><span class="sxs-lookup"><span data-stu-id="281b3-137">All task durations must be greater than or equal to (>=) one hour and less than 1,800,000 minutes (1,250 days).\*</span></span>
- <span data-ttu-id="281b3-138">Kaikilla tehtävillä on oltava alkamispäivä aikaisintaan 2000/01/01. \*</span><span class="sxs-lookup"><span data-stu-id="281b3-138">All tasks must have a start date no earlier than 2000/01/01.\*</span></span>
- <span data-ttu-id="281b3-139">Kaikilla tehtävillä on oltava alkamispäivä viimeistään 17 vuoden kuluttua nykyisestä päivästä. \*</span><span class="sxs-lookup"><span data-stu-id="281b3-139">All tasks must have a start date no later than 17 years from the present day.\*</span></span>
- <span data-ttu-id="281b3-140">Kaikkien tehtävien alkamispäivän on oltava aiemmin tai samana päivänä kuin niiden päättymispäivä.</span><span class="sxs-lookup"><span data-stu-id="281b3-140">All tasks must have a start date earlier or equal to their finish date.</span></span>
- <span data-ttu-id="281b3-141">Kaikilla tapahtumatyypeillä luokissa (Kulu, Materiaali, Vero ja Aika) on oltava arvot **Oletusyksikkö** ja **Yksikköryhmä**.</span><span class="sxs-lookup"><span data-stu-id="281b3-141">All transaction types on classifications (Expense, Material, Tax, and Time) must have values for **Default Unit** and **Unit Group**.</span></span>
- <span data-ttu-id="281b3-142">Päivämäärämuotoja, joissa on kirjaimia, on vältettävä.</span><span class="sxs-lookup"><span data-stu-id="281b3-142">Date formats with letters should be avoided.</span></span>

### <a name="potential-mitigation-steps"></a><span data-ttu-id="281b3-143">Mahdolliset korjaavien toimien vaiheet</span><span class="sxs-lookup"><span data-stu-id="281b3-143">Potential mitigation steps</span></span>
- <span data-ttu-id="281b3-144">Erikoishaku-toiminnon avulla voit määrittää projektitehtävät, jotka eivät sisällä projektitunnusta.</span><span class="sxs-lookup"><span data-stu-id="281b3-144">Use Advanced Find to identify Project tasks that do not contain a Project ID.</span></span>
- <span data-ttu-id="281b3-145">Erikoishaku-toiminnon avulla voit määrittää projektitehtävät, joiden ajoitettu kesto on suurempi kuin 1 800 000.</span><span class="sxs-lookup"><span data-stu-id="281b3-145">Use Advanced Find to identify Project tasks where the scheduled duration is greater than > 1,800,000.</span></span>
- <span data-ttu-id="281b3-146">Ennen kuin teet muutoksia tietoihin, tutki entiteettiin liittyviä mukautuksia, jotka ovat voineet saada tiedot huonoon tilaan.</span><span class="sxs-lookup"><span data-stu-id="281b3-146">Prior to making any data changes, you should investigate any customizations associated with the entity that may have led to getting the data into a bad state.</span></span> <span data-ttu-id="281b3-147">Nämä mukautukset on selvitettävä, ennen kuin jatkat mitään tietoihin liittyviä päivityksiä.</span><span class="sxs-lookup"><span data-stu-id="281b3-147">These customizations should be addressed before proceeding with any data-related updates.</span></span>
- <span data-ttu-id="281b3-148">Jos tunnistetut tehtävät on määritetty orvoiksi, harkitse näiden tehtävien poistamista, jos niitä ei tarvita, tai niiden liitettämistä oikeaan pääprojektiin.</span><span class="sxs-lookup"><span data-stu-id="281b3-148">For the identified tasks that have been orphaned, consider deleting these tasks if they are not needed or if they should be associated with the correct parent project.</span></span>
- <span data-ttu-id="281b3-149">Jos tehtävän kesto on suurempi kuin 1 250 päivää, kannattaa lisätä useita tehtäviä, jotka kuvaavat kokonaiskestoa, jos mahdollista.</span><span class="sxs-lookup"><span data-stu-id="281b3-149">For any tasks where the duration is greater than 1,250 days, consider adding multiple tasks to represent the total duration, if feasible.</span></span>

> [!NOTE]
> <span data-ttu-id="281b3-150">Tähdellä (\*) merkityt kohteet sisältävät rajoituksia, jotka johtuvat siitä, että customer relationship management (CRM) tukee vain 7 320 toistuvuuslaajennusta.</span><span class="sxs-lookup"><span data-stu-id="281b3-150">Items noted with an asterisk (\*) have limits that are due to the fact that customer relationship management (CRM) supports only 7,320 recurrence expansions.</span></span> <span data-ttu-id="281b3-151">Sinun täytyy pysyä tämän rajan alapuolella.</span><span class="sxs-lookup"><span data-stu-id="281b3-151">You must stay below this limit.</span></span>

## <a name="resource-assignment-relationships"></a><span data-ttu-id="281b3-152">Resurssien kohdentamisen suhteet</span><span class="sxs-lookup"><span data-stu-id="281b3-152">Resource Assignment relationships</span></span>
<span data-ttu-id="281b3-153">Onnistuneen päivityksen varmistamiseksi seuraavat suhteet on säilytettävä oikein:</span><span class="sxs-lookup"><span data-stu-id="281b3-153">To ensure a successful upgrade, the following relationships must be correctly maintained:</span></span>

- <span data-ttu-id="281b3-154">Kaikkien työrakenteen resurssikohdennusten on liityttävä samaan projektiin.</span><span class="sxs-lookup"><span data-stu-id="281b3-154">All Resource Assignments in a work breakdown structure must be related to the same project.</span></span>
- <span data-ttu-id="281b3-155">Kaikkien työrakenteen resurssikohdennusten on liityttävä projektiryhmän jäseniin samassa projektissa.</span><span class="sxs-lookup"><span data-stu-id="281b3-155">All Resource Assignments in a work breakdown structure must be associated to project team members in the same project.</span></span>

### <a name="potential-mitigation-steps"></a><span data-ttu-id="281b3-156">Mahdolliset korjaavien toimien vaiheet</span><span class="sxs-lookup"><span data-stu-id="281b3-156">Potential mitigation steps</span></span>
- <span data-ttu-id="281b3-157">Määritä kaikki tehtävät, jotka eivät kuulu edellä mainittuihin ehtoihin.</span><span class="sxs-lookup"><span data-stu-id="281b3-157">Identify all tasks that fall outside the conditions described above.</span></span>  
- <span data-ttu-id="281b3-158">Kaikki resurssivaraukset, jotka eivät ole enää kelvollisia, on poistettava.</span><span class="sxs-lookup"><span data-stu-id="281b3-158">Any Resource Assignments that are no longer valid should be deleted.</span></span>

## <a name="project-task-dependency-relationships"></a><span data-ttu-id="281b3-159">Projektitehtävän riippuvuuksien suhteet</span><span class="sxs-lookup"><span data-stu-id="281b3-159">Project task dependency relationships</span></span>
<span data-ttu-id="281b3-160">Onnistuneen päivityksen varmistamiseksi seuraavat suhteet on säilytettävä oikein:</span><span class="sxs-lookup"><span data-stu-id="281b3-160">To ensure a successful upgrade, the following relationships must be correctly maintained:</span></span>

- <span data-ttu-id="281b3-161">Kaikkien projektitehtäväriippuvuuksien on liityttävä samaan projektiin.</span><span class="sxs-lookup"><span data-stu-id="281b3-161">All project task dependencies must be related to the same project.</span></span>
- <span data-ttu-id="281b3-162">Samaan tehtävän riippuvuuteen ei voi viitata useammin kuin kerran.</span><span class="sxs-lookup"><span data-stu-id="281b3-162">A task can't have the same dependency referenced more than once.</span></span>
