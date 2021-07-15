---
title: Projektiaikataulun ohjelmointirajapintojen käyttö toimintojen suorittamiseen aikataulutusentiteeteillä
description: Tässä aiheessa on tietoja ja esimerkkejä projektiaikataulun ohjelmointirajapintojen käyttämisestä.
author: sigitac
ms.date: 06/22/2021
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 4915261c08a3271a919e04084e92a14b297c1b35
ms.sourcegitcommit: 2f16c2bc7c8350676a6a380c61fffa9958db6a0b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/22/2021
ms.locfileid: "6293223"
---
# <a name="use-project-schedule-apis-to-perform-operations-with-scheduling-entities"></a><span data-ttu-id="ab429-103">Projektiaikataulun ohjelmointirajapintojen käyttö toimintojen suorittamiseen aikataulutusentiteeteillä</span><span class="sxs-lookup"><span data-stu-id="ab429-103">Use Project schedule APIs to perform operations with Scheduling entities</span></span>

<span data-ttu-id="ab429-104">_**Koskee:** Project Operationsin resurssiin / muuhun kuin resurssiin perustuvia skenaarioita, Lite-käyttöönotto-kaupasta proformalaskutukseen_</span><span class="sxs-lookup"><span data-stu-id="ab429-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

> [!IMPORTANT] 
> <span data-ttu-id="ab429-105">Kaikki tai osa tässä aiheessa käsitellyistä toiminnoista ovat saatavilla esiversiojulkaisun osana.</span><span class="sxs-lookup"><span data-stu-id="ab429-105">Some or all of the functionality noted in this topic is available as part of a preview release.</span></span> <span data-ttu-id="ab429-106">Sisältö ja toiminnot voivat muuttua.</span><span class="sxs-lookup"><span data-stu-id="ab429-106">The content and the functionality are subject to change.</span></span> 

## <a name="scheduling-entities"></a><span data-ttu-id="ab429-107">Aikataulutusentiteetit</span><span class="sxs-lookup"><span data-stu-id="ab429-107">Scheduling entities</span></span>

<span data-ttu-id="ab429-108">Projektiaikataulun ohjelmointirajapintojen avulla voi luoda, päivittää ja poistaa toimintoja **aikataulutusentiteettien** avulla.</span><span class="sxs-lookup"><span data-stu-id="ab429-108">Project schedule APIs provide the ability to perform create, update, and delete operations with **Scheduling entities**.</span></span> <span data-ttu-id="ab429-109">Näitä entiteettejä hallitaan verkkopohjaisessa Projectissa aikataulutusytimen kautta.</span><span class="sxs-lookup"><span data-stu-id="ab429-109">These entities are managed through the Scheduling engine in Project for the web.</span></span> <span data-ttu-id="ab429-110">Luonti-, päivitys- ja poisto-operaatioita **Aikataulutusentiteettien avulla** rajoitettiin aiemmissa Dynamics 365 Project Operations -julkaisuissa.</span><span class="sxs-lookup"><span data-stu-id="ab429-110">Create, update, and delete operations with **Scheduling entities** were restricted in earlier Dynamics 365 Project Operations releases.</span></span>

<span data-ttu-id="ab429-111">Seuraavassa taulukossa on täydellinen luettelo Projektiaikataulu -entiteeteistä.</span><span class="sxs-lookup"><span data-stu-id="ab429-111">The following table provides a full list of the Project schedule entities.</span></span>

| <span data-ttu-id="ab429-112">Entiteetin nimi</span><span class="sxs-lookup"><span data-stu-id="ab429-112">Entity name</span></span>  | <span data-ttu-id="ab429-113">Entiteetin looginen nimi</span><span class="sxs-lookup"><span data-stu-id="ab429-113">Entity logical name</span></span> |
| --- | --- |
| <span data-ttu-id="ab429-114">Project</span><span class="sxs-lookup"><span data-stu-id="ab429-114">Project</span></span> | <span data-ttu-id="ab429-115">msdyn_project</span><span class="sxs-lookup"><span data-stu-id="ab429-115">msdyn_project</span></span> |
| <span data-ttu-id="ab429-116">Projektin tehtävä</span><span class="sxs-lookup"><span data-stu-id="ab429-116">Project Task</span></span>  | <span data-ttu-id="ab429-117">msdyn_projecttask</span><span class="sxs-lookup"><span data-stu-id="ab429-117">msdyn_projecttask</span></span>  |
| <span data-ttu-id="ab429-118">Projektitehtävän riippuvuus</span><span class="sxs-lookup"><span data-stu-id="ab429-118">Project Task Dependency</span></span>  | <span data-ttu-id="ab429-119">msdyn_projecttaskdependency</span><span class="sxs-lookup"><span data-stu-id="ab429-119">msdyn_projecttaskdependency</span></span>  |
| <span data-ttu-id="ab429-120">Resurssien delegointi</span><span class="sxs-lookup"><span data-stu-id="ab429-120">Resource Assignment</span></span> | <span data-ttu-id="ab429-121">msdyn_resourceassignment</span><span class="sxs-lookup"><span data-stu-id="ab429-121">msdyn_resourceassignment</span></span> |
| <span data-ttu-id="ab429-122">Projektin joukko</span><span class="sxs-lookup"><span data-stu-id="ab429-122">Project Bucket</span></span>  | <span data-ttu-id="ab429-123">msdyn_projectbucket</span><span class="sxs-lookup"><span data-stu-id="ab429-123">msdyn_projectbucket</span></span> |
| <span data-ttu-id="ab429-124">Projektiryhmän jäsen</span><span class="sxs-lookup"><span data-stu-id="ab429-124">Project Team Member</span></span> | <span data-ttu-id="ab429-125">msdyn_projectteam</span><span class="sxs-lookup"><span data-stu-id="ab429-125">msdyn_projectteam</span></span> |

## <a name="operationset"></a><span data-ttu-id="ab429-126">OperationSet</span><span class="sxs-lookup"><span data-stu-id="ab429-126">OperationSet</span></span>

<span data-ttu-id="ab429-127">OperationSet on työyksikkörakenne, jota voidaan käyttää, kun useita aikatauluihin vaikuttavia pyyntöjä on käsiteltävä tapahtumassa.</span><span class="sxs-lookup"><span data-stu-id="ab429-127">OperationSet is a unit-of-work pattern that can be used when several schedule impacting requests must be processed within a transaction.</span></span>

## <a name="project-schedule-apis"></a><span data-ttu-id="ab429-128">Projektiaikataulujen ohjelmointirajapinnat</span><span class="sxs-lookup"><span data-stu-id="ab429-128">Project schedule APIs</span></span>

<span data-ttu-id="ab429-129">Seuraavassa on luettelo nykyisistä Projektiaikataulun ohjelmointirajapinnoista.</span><span class="sxs-lookup"><span data-stu-id="ab429-129">The following is a list of current Project schedule APIs.</span></span>

- <span data-ttu-id="ab429-130">**msdyn_CreateProjectV1**: Tämän ohjelmointirajapinnan avulla voidaan luoda projekti.</span><span class="sxs-lookup"><span data-stu-id="ab429-130">**msdyn_CreateProjectV1**: This API can be used to create a project.</span></span> <span data-ttu-id="ab429-131">Projekti ja projektin oletussäilö luodaan heti.</span><span class="sxs-lookup"><span data-stu-id="ab429-131">The project and default project bucket is created immediately.</span></span>
- <span data-ttu-id="ab429-132">**msdyn_CreateTeamMemberV1**: Tämän ohjelmointirajapinnan avulla voidaan luoda projektiryhmän jäsen.</span><span class="sxs-lookup"><span data-stu-id="ab429-132">**msdyn_CreateTeamMemberV1**: This API can be used to create a project team member.</span></span> <span data-ttu-id="ab429-133">Ryhmän jäsentietue luodaan heti.</span><span class="sxs-lookup"><span data-stu-id="ab429-133">The team member record is created immediately.</span></span>
- <span data-ttu-id="ab429-134">**msdyn_CreateOperationSetV1**: Tämän ohjelmointirajapinnan avulla voidaan aikatauluttaa useita pyyntöjä, jotka on suoritettava tapahtumassa.</span><span class="sxs-lookup"><span data-stu-id="ab429-134">**msdyn_CreateOperationSetV1**: This API can be used to schedule several requests that must be performed within a transaction.</span></span>
- <span data-ttu-id="ab429-135">**msdyn_PSSCreateV1**: Tämän ohjelmointirajapinnan avulla voidaan luoda entiteetti.</span><span class="sxs-lookup"><span data-stu-id="ab429-135">**msdyn_PSSCreateV1**: This API can be used to create an entity.</span></span> <span data-ttu-id="ab429-136">Entiteetti voi olla mikä tahansa luontitoimintoa tukeva projektin aikataulutusentiteetti.</span><span class="sxs-lookup"><span data-stu-id="ab429-136">The entity can be any of the Project scheduling entities that support the create operation.</span></span>
- <span data-ttu-id="ab429-137">**msdyn_PSSUpdateV1**: Tämän ohjelmointirajapinnan avulla voidaan päivittää entiteetti.</span><span class="sxs-lookup"><span data-stu-id="ab429-137">**msdyn_PSSUpdateV1**: This API can be used to update an entity.</span></span> <span data-ttu-id="ab429-138">Entiteetti voi olla mikä tahansa päivitystoimintoa tukeva projektin aikataulutusentiteetti.</span><span class="sxs-lookup"><span data-stu-id="ab429-138">The entity can be any of the Project scheduling entities that support the update operation.</span></span>
- <span data-ttu-id="ab429-139">**msdyn_PSSDeleteV1**: Tämän ohjelmointirajapinnan avulla voidaan poistaa entiteetti.</span><span class="sxs-lookup"><span data-stu-id="ab429-139">**msdyn_PSSDeleteV1**: This API can be used to delete an entity.</span></span> <span data-ttu-id="ab429-140">Entiteetti voi olla mikä tahansa poistotoimintoa tukeva projektin aikataulutusentiteetti.</span><span class="sxs-lookup"><span data-stu-id="ab429-140">The entity can be any of the Project scheduling entities that support the delete operation.</span></span>
- <span data-ttu-id="ab429-141">**msdyn_ExecuteOperationSetV1**: Tämän ohjelmointirajapinnan avulla suoritetaan kaikki toiminnot tietyn toimintojoukon sisällä.</span><span class="sxs-lookup"><span data-stu-id="ab429-141">**msdyn_ExecuteOperationSetV1**: This API is used to execute all of the operations within the given operation set.</span></span>

## <a name="using-project-schedule-apis-with-operationset"></a><span data-ttu-id="ab429-142">Projektiaikataulun ohjelmointirajapintojen käyttäminen OperationSetin kanssa</span><span class="sxs-lookup"><span data-stu-id="ab429-142">Using Project schedule APIs with OperationSet</span></span>

<span data-ttu-id="ab429-143">Koska tietueet, joissa on sekä **CreateProjectV1** että **CreateTeamMemberV1** luodaan välittömästi, näitä ohjelmointirajapintoja ei voida käyttää suoraan **OperationSet** issä.</span><span class="sxs-lookup"><span data-stu-id="ab429-143">Because records with both **CreateProjectV1** and **CreateTeamMemberV1** are created immediately, these APIs can't be used in the **OperationSet** directly.</span></span> <span data-ttu-id="ab429-144">Ohjelmointirajapinnan avulla voit kuitenkin luoda tarvittavat tietueet, luoda **OperationSet** in, ja käyttää sitten näitä aiemmin luotuja tietueita **OperationSet** issä.</span><span class="sxs-lookup"><span data-stu-id="ab429-144">However, you can use the API to create needed records, create an **OperationSet**, and then use these pre-created records in the **OperationSet**.</span></span>

## <a name="supported-operations"></a><span data-ttu-id="ab429-145">Tuetut toiminnot</span><span class="sxs-lookup"><span data-stu-id="ab429-145">Supported operations</span></span>

| <span data-ttu-id="ab429-146">Aikataulutusentiteetti</span><span class="sxs-lookup"><span data-stu-id="ab429-146">Scheduling entity</span></span> | <span data-ttu-id="ab429-147">Luo</span><span class="sxs-lookup"><span data-stu-id="ab429-147">Create</span></span> | <span data-ttu-id="ab429-148">Päivitys</span><span class="sxs-lookup"><span data-stu-id="ab429-148">Update</span></span> | <span data-ttu-id="ab429-149">Delete</span><span class="sxs-lookup"><span data-stu-id="ab429-149">Delete</span></span> | <span data-ttu-id="ab429-150">Tärkeitä huomioon otettavia seikkoja</span><span class="sxs-lookup"><span data-stu-id="ab429-150">Important considerations</span></span> |
| --- | --- | --- | --- | --- |
<span data-ttu-id="ab429-151">Projektitehtävä</span><span class="sxs-lookup"><span data-stu-id="ab429-151">Project task</span></span> | <span data-ttu-id="ab429-152">Kyllä</span><span class="sxs-lookup"><span data-stu-id="ab429-152">Yes</span></span> | <span data-ttu-id="ab429-153">Kyllä</span><span class="sxs-lookup"><span data-stu-id="ab429-153">Yes</span></span> | <span data-ttu-id="ab429-154">Kyllä</span><span class="sxs-lookup"><span data-stu-id="ab429-154">Yes</span></span> | <span data-ttu-id="ab429-155">Ei ole</span><span class="sxs-lookup"><span data-stu-id="ab429-155">None</span></span> |
| <span data-ttu-id="ab429-156">Projektitehtävän riippuvuus</span><span class="sxs-lookup"><span data-stu-id="ab429-156">Project task dependency</span></span> | <span data-ttu-id="ab429-157">Kyllä</span><span class="sxs-lookup"><span data-stu-id="ab429-157">Yes</span></span> | <span data-ttu-id="ab429-158">Kyllä</span><span class="sxs-lookup"><span data-stu-id="ab429-158">Yes</span></span> | | <span data-ttu-id="ab429-159">Projektitehtävän riippuvuustietueita ei päivitetä.</span><span class="sxs-lookup"><span data-stu-id="ab429-159">Project task dependency records aren't updated.</span></span> <span data-ttu-id="ab429-160">Sen sijaan voidaan poistaa vanha tietue ja luoda uusi tietue.</span><span class="sxs-lookup"><span data-stu-id="ab429-160">Instead, an old record can be deleted and a new record can be created.</span></span> |
| <span data-ttu-id="ab429-161">Resurssien delegointi</span><span class="sxs-lookup"><span data-stu-id="ab429-161">Resource assignment</span></span> | <span data-ttu-id="ab429-162">Kyllä</span><span class="sxs-lookup"><span data-stu-id="ab429-162">Yes</span></span> | <span data-ttu-id="ab429-163">Kyllä</span><span class="sxs-lookup"><span data-stu-id="ab429-163">Yes</span></span> | | <span data-ttu-id="ab429-164">Toimintoja, joilla on seuraavat kentät, ei tueta: **BookableResourceID**, **Effort**, **EffortCompleted**, **EffortRemaining** ja **PlannedWork**.</span><span class="sxs-lookup"><span data-stu-id="ab429-164">Operations with the following fields aren't supported: **BookableResourceID**, **Effort**, **EffortCompleted**, **EffortRemaining**, and **PlannedWork**.</span></span> <span data-ttu-id="ab429-165">Resurssien määritystietueita ei päivitetä.</span><span class="sxs-lookup"><span data-stu-id="ab429-165">Resource assignment records aren't updated.</span></span> <span data-ttu-id="ab429-166">Sen sijaan voidaan poistaa vanha tietue ja luoda uusi tietue.</span><span class="sxs-lookup"><span data-stu-id="ab429-166">Instead, the old record can be deleted and a new record can be created.</span></span> |
| <span data-ttu-id="ab429-167">Projektin säilö</span><span class="sxs-lookup"><span data-stu-id="ab429-167">Project bucket</span></span> | <span data-ttu-id="ab429-168">–</span><span class="sxs-lookup"><span data-stu-id="ab429-168">N/A</span></span> | <span data-ttu-id="ab429-169">–</span><span class="sxs-lookup"><span data-stu-id="ab429-169">N/A</span></span> | <span data-ttu-id="ab429-170">–</span><span class="sxs-lookup"><span data-stu-id="ab429-170">N/A</span></span> | <span data-ttu-id="ab429-171">Oletussäilö luodaan **CreateProjectV1** -ohjelmointirajapinnan avulla.</span><span class="sxs-lookup"><span data-stu-id="ab429-171">The default bucket is created using the **CreateProjectV1** API.</span></span> |
| <span data-ttu-id="ab429-172">Projektiryhmän jäsen</span><span class="sxs-lookup"><span data-stu-id="ab429-172">Project team member</span></span> | <span data-ttu-id="ab429-173">Kyllä</span><span class="sxs-lookup"><span data-stu-id="ab429-173">Yes</span></span> | <span data-ttu-id="ab429-174">Kyllä</span><span class="sxs-lookup"><span data-stu-id="ab429-174">Yes</span></span> | <span data-ttu-id="ab429-175">Kyllä</span><span class="sxs-lookup"><span data-stu-id="ab429-175">Yes</span></span> | <span data-ttu-id="ab429-176">Käytä luontioperaatiolle **CreateTeamMemberV1** -ohjelmointirajapintaa.</span><span class="sxs-lookup"><span data-stu-id="ab429-176">For the create operation, use the **CreateTeamMemberV1** API.</span></span> |
| <span data-ttu-id="ab429-177">Project</span><span class="sxs-lookup"><span data-stu-id="ab429-177">Project</span></span> | <span data-ttu-id="ab429-178">Kyllä</span><span class="sxs-lookup"><span data-stu-id="ab429-178">Yes</span></span> | <span data-ttu-id="ab429-179">Kyllä</span><span class="sxs-lookup"><span data-stu-id="ab429-179">Yes</span></span> | <span data-ttu-id="ab429-180">–</span><span class="sxs-lookup"><span data-stu-id="ab429-180">N/A</span></span> | <span data-ttu-id="ab429-181">Toimintoja, joilla on seuraavat kentät, ei tueta **StateCode**, **BulkGenerationStatus**, **GlobalRevisionToken**, **CalendarID**, **Effort**, **EffortCompleted**, **EffortRemaining**, **Progress**, **Finish**, **TaskEarliestStart** ja **Duration**.</span><span class="sxs-lookup"><span data-stu-id="ab429-181">Operations with the following fields aren't supported: **StateCode**, **BulkGenerationStatus**, **GlobalRevisionToken**, **CalendarID**, **Effort**, **EffortCompleted**, **EffortRemaining**, **Progress**, **Finish**, **TaskEarliestStart**, and **Duration**.</span></span> |

<span data-ttu-id="ab429-182">Näitä ohjelmointirajapintoja voidaan kutsua entiteettiobjekteilla, jotka sisältävät mukautettuja kenttiä.</span><span class="sxs-lookup"><span data-stu-id="ab429-182">These APIs can be called with entity objects that include custom fields.</span></span>

<span data-ttu-id="ab429-183">Tunnusominaisuus on valinnainen.</span><span class="sxs-lookup"><span data-stu-id="ab429-183">The ID property is optional.</span></span> <span data-ttu-id="ab429-184">Jos se on annettu, järjestelmä yrittää käyttää sitä ja antaa poikkeuksen, jos sitä ei voi käyttää.</span><span class="sxs-lookup"><span data-stu-id="ab429-184">If it's provided, the system attempts to use it and throws an exception if it can't be used.</span></span> <span data-ttu-id="ab429-185">Jos sitä ei ole annettu, järjestelmä luo sen.</span><span class="sxs-lookup"><span data-stu-id="ab429-185">If it isn't provided, the system will generate it.</span></span>

## <a name="restricted-fields"></a><span data-ttu-id="ab429-186">Rajoitetut kentät</span><span class="sxs-lookup"><span data-stu-id="ab429-186">Restricted fields</span></span>

<span data-ttu-id="ab429-187">Seuraavissa taulukoissa määritetään kentät, joita ei voi **luoda** ja **muokata**.</span><span class="sxs-lookup"><span data-stu-id="ab429-187">The following tables define the fields that are restricted from **Create** and **Edit.**</span></span>

### <a name="project-task"></a><span data-ttu-id="ab429-188">Projektitehtävä</span><span class="sxs-lookup"><span data-stu-id="ab429-188">Project task</span></span>

| <span data-ttu-id="ab429-189">**Looginen nimi**</span><span class="sxs-lookup"><span data-stu-id="ab429-189">**Logical name**</span></span>                       | <span data-ttu-id="ab429-190">**Voidaan luoda**</span><span class="sxs-lookup"><span data-stu-id="ab429-190">**Can create**</span></span> | <span data-ttu-id="ab429-191">**Voidaan muokata**</span><span class="sxs-lookup"><span data-stu-id="ab429-191">**Can edit**</span></span>     |
|----------------------------------------|----------------|------------------|
| <span data-ttu-id="ab429-192">msdyn_actualcost</span><span class="sxs-lookup"><span data-stu-id="ab429-192">msdyn_actualcost</span></span>                       | <span data-ttu-id="ab429-193">ei</span><span class="sxs-lookup"><span data-stu-id="ab429-193">no</span></span>             | <span data-ttu-id="ab429-194">ei</span><span class="sxs-lookup"><span data-stu-id="ab429-194">no</span></span>               |
| <span data-ttu-id="ab429-195">msdyn_actualcost_base</span><span class="sxs-lookup"><span data-stu-id="ab429-195">msdyn_actualcost_base</span></span>                  | <span data-ttu-id="ab429-196">ei</span><span class="sxs-lookup"><span data-stu-id="ab429-196">no</span></span>             | <span data-ttu-id="ab429-197">ei</span><span class="sxs-lookup"><span data-stu-id="ab429-197">no</span></span>               |
| <span data-ttu-id="ab429-198">msdyn_actualend</span><span class="sxs-lookup"><span data-stu-id="ab429-198">msdyn_actualend</span></span>                        | <span data-ttu-id="ab429-199">ei</span><span class="sxs-lookup"><span data-stu-id="ab429-199">no</span></span>             | <span data-ttu-id="ab429-200">ei</span><span class="sxs-lookup"><span data-stu-id="ab429-200">no</span></span>               |
| <span data-ttu-id="ab429-201">msdyn_actualsales</span><span class="sxs-lookup"><span data-stu-id="ab429-201">msdyn_actualsales</span></span>                      | <span data-ttu-id="ab429-202">ei</span><span class="sxs-lookup"><span data-stu-id="ab429-202">no</span></span>             | <span data-ttu-id="ab429-203">ei</span><span class="sxs-lookup"><span data-stu-id="ab429-203">no</span></span>               |
| <span data-ttu-id="ab429-204">msdyn_actualsales_base</span><span class="sxs-lookup"><span data-stu-id="ab429-204">msdyn_actualsales_base</span></span>                 | <span data-ttu-id="ab429-205">ei</span><span class="sxs-lookup"><span data-stu-id="ab429-205">no</span></span>             | <span data-ttu-id="ab429-206">ei</span><span class="sxs-lookup"><span data-stu-id="ab429-206">no</span></span>               |
| <span data-ttu-id="ab429-207">msdyn_actualstart</span><span class="sxs-lookup"><span data-stu-id="ab429-207">msdyn_actualstart</span></span>                      | <span data-ttu-id="ab429-208">ei</span><span class="sxs-lookup"><span data-stu-id="ab429-208">no</span></span>             | <span data-ttu-id="ab429-209">ei</span><span class="sxs-lookup"><span data-stu-id="ab429-209">no</span></span>               |
| <span data-ttu-id="ab429-210">msdyn_costatcompleteestimate</span><span class="sxs-lookup"><span data-stu-id="ab429-210">msdyn_costatcompleteestimate</span></span>           | <span data-ttu-id="ab429-211">ei</span><span class="sxs-lookup"><span data-stu-id="ab429-211">no</span></span>             | <span data-ttu-id="ab429-212">ei</span><span class="sxs-lookup"><span data-stu-id="ab429-212">no</span></span>               |
| <span data-ttu-id="ab429-213">msdyn_costatcompleteestimate_base</span><span class="sxs-lookup"><span data-stu-id="ab429-213">msdyn_costatcompleteestimate_base</span></span>      | <span data-ttu-id="ab429-214">ei</span><span class="sxs-lookup"><span data-stu-id="ab429-214">no</span></span>             | <span data-ttu-id="ab429-215">ei</span><span class="sxs-lookup"><span data-stu-id="ab429-215">no</span></span>               |
| <span data-ttu-id="ab429-216">msdyn_costconsumptionpercentage</span><span class="sxs-lookup"><span data-stu-id="ab429-216">msdyn_costconsumptionpercentage</span></span>        | <span data-ttu-id="ab429-217">ei</span><span class="sxs-lookup"><span data-stu-id="ab429-217">no</span></span>             | <span data-ttu-id="ab429-218">ei</span><span class="sxs-lookup"><span data-stu-id="ab429-218">no</span></span>               |
| <span data-ttu-id="ab429-219">msdyn_effortcompleted</span><span class="sxs-lookup"><span data-stu-id="ab429-219">msdyn_effortcompleted</span></span>                  | <span data-ttu-id="ab429-220">ei</span><span class="sxs-lookup"><span data-stu-id="ab429-220">no</span></span>             | <span data-ttu-id="ab429-221">ei</span><span class="sxs-lookup"><span data-stu-id="ab429-221">no</span></span>               |
| <span data-ttu-id="ab429-222">msdyn_effortestimateatcomplete</span><span class="sxs-lookup"><span data-stu-id="ab429-222">msdyn_effortestimateatcomplete</span></span>         | <span data-ttu-id="ab429-223">ei</span><span class="sxs-lookup"><span data-stu-id="ab429-223">no</span></span>             | <span data-ttu-id="ab429-224">ei</span><span class="sxs-lookup"><span data-stu-id="ab429-224">no</span></span>               |
| <span data-ttu-id="ab429-225">msdyn_iscritical</span><span class="sxs-lookup"><span data-stu-id="ab429-225">msdyn_iscritical</span></span>                       | <span data-ttu-id="ab429-226">ei</span><span class="sxs-lookup"><span data-stu-id="ab429-226">no</span></span>             | <span data-ttu-id="ab429-227">ei</span><span class="sxs-lookup"><span data-stu-id="ab429-227">no</span></span>               |
| <span data-ttu-id="ab429-228">msdyn_iscriticalname</span><span class="sxs-lookup"><span data-stu-id="ab429-228">msdyn_iscriticalname</span></span>                   | <span data-ttu-id="ab429-229">ei</span><span class="sxs-lookup"><span data-stu-id="ab429-229">no</span></span>             | <span data-ttu-id="ab429-230">ei</span><span class="sxs-lookup"><span data-stu-id="ab429-230">no</span></span>               |
| <span data-ttu-id="ab429-231">msdyn_ismanual</span><span class="sxs-lookup"><span data-stu-id="ab429-231">msdyn_ismanual</span></span>                         | <span data-ttu-id="ab429-232">ei</span><span class="sxs-lookup"><span data-stu-id="ab429-232">no</span></span>             | <span data-ttu-id="ab429-233">ei</span><span class="sxs-lookup"><span data-stu-id="ab429-233">no</span></span>               |
| <span data-ttu-id="ab429-234">msdyn_ismanualname</span><span class="sxs-lookup"><span data-stu-id="ab429-234">msdyn_ismanualname</span></span>                     | <span data-ttu-id="ab429-235">ei</span><span class="sxs-lookup"><span data-stu-id="ab429-235">no</span></span>             | <span data-ttu-id="ab429-236">ei</span><span class="sxs-lookup"><span data-stu-id="ab429-236">no</span></span>               |
| <span data-ttu-id="ab429-237">msdyn_ismilestone</span><span class="sxs-lookup"><span data-stu-id="ab429-237">msdyn_ismilestone</span></span>                      | <span data-ttu-id="ab429-238">ei</span><span class="sxs-lookup"><span data-stu-id="ab429-238">no</span></span>             | <span data-ttu-id="ab429-239">ei</span><span class="sxs-lookup"><span data-stu-id="ab429-239">no</span></span>               |
| <span data-ttu-id="ab429-240">msdyn_ismilestonename</span><span class="sxs-lookup"><span data-stu-id="ab429-240">msdyn_ismilestonename</span></span>                  | <span data-ttu-id="ab429-241">ei</span><span class="sxs-lookup"><span data-stu-id="ab429-241">no</span></span>             | <span data-ttu-id="ab429-242">ei</span><span class="sxs-lookup"><span data-stu-id="ab429-242">no</span></span>               |
| <span data-ttu-id="ab429-243">msdyn_LinkStatus</span><span class="sxs-lookup"><span data-stu-id="ab429-243">msdyn_LinkStatus</span></span>                       | <span data-ttu-id="ab429-244">ei</span><span class="sxs-lookup"><span data-stu-id="ab429-244">no</span></span>             | <span data-ttu-id="ab429-245">ei</span><span class="sxs-lookup"><span data-stu-id="ab429-245">no</span></span>               |
| <span data-ttu-id="ab429-246">msdyn_linkstatusname</span><span class="sxs-lookup"><span data-stu-id="ab429-246">msdyn_linkstatusname</span></span>                   | <span data-ttu-id="ab429-247">ei</span><span class="sxs-lookup"><span data-stu-id="ab429-247">no</span></span>             | <span data-ttu-id="ab429-248">ei</span><span class="sxs-lookup"><span data-stu-id="ab429-248">no</span></span>               |
| <span data-ttu-id="ab429-249">msdyn_msprojectclientid</span><span class="sxs-lookup"><span data-stu-id="ab429-249">msdyn_msprojectclientid</span></span>                | <span data-ttu-id="ab429-250">ei</span><span class="sxs-lookup"><span data-stu-id="ab429-250">no</span></span>             | <span data-ttu-id="ab429-251">ei</span><span class="sxs-lookup"><span data-stu-id="ab429-251">no</span></span>               |
| <span data-ttu-id="ab429-252">msdyn_plannedcost</span><span class="sxs-lookup"><span data-stu-id="ab429-252">msdyn_plannedcost</span></span>                      | <span data-ttu-id="ab429-253">ei</span><span class="sxs-lookup"><span data-stu-id="ab429-253">no</span></span>             | <span data-ttu-id="ab429-254">ei</span><span class="sxs-lookup"><span data-stu-id="ab429-254">no</span></span>               |
| <span data-ttu-id="ab429-255">msdyn_plannedcost_base</span><span class="sxs-lookup"><span data-stu-id="ab429-255">msdyn_plannedcost_base</span></span>                 | <span data-ttu-id="ab429-256">ei</span><span class="sxs-lookup"><span data-stu-id="ab429-256">no</span></span>             | <span data-ttu-id="ab429-257">ei</span><span class="sxs-lookup"><span data-stu-id="ab429-257">no</span></span>               |
| <span data-ttu-id="ab429-258">msdyn_plannedsales</span><span class="sxs-lookup"><span data-stu-id="ab429-258">msdyn_plannedsales</span></span>                     | <span data-ttu-id="ab429-259">ei</span><span class="sxs-lookup"><span data-stu-id="ab429-259">no</span></span>             | <span data-ttu-id="ab429-260">ei</span><span class="sxs-lookup"><span data-stu-id="ab429-260">no</span></span>               |
| <span data-ttu-id="ab429-261">msdyn_plannedsales_base</span><span class="sxs-lookup"><span data-stu-id="ab429-261">msdyn_plannedsales_base</span></span>                | <span data-ttu-id="ab429-262">ei</span><span class="sxs-lookup"><span data-stu-id="ab429-262">no</span></span>             | <span data-ttu-id="ab429-263">ei</span><span class="sxs-lookup"><span data-stu-id="ab429-263">no</span></span>               |
| <span data-ttu-id="ab429-264">msdyn_pluginprocessingdata</span><span class="sxs-lookup"><span data-stu-id="ab429-264">msdyn_pluginprocessingdata</span></span>             | <span data-ttu-id="ab429-265">ei</span><span class="sxs-lookup"><span data-stu-id="ab429-265">no</span></span>             | <span data-ttu-id="ab429-266">ei</span><span class="sxs-lookup"><span data-stu-id="ab429-266">no</span></span>               |
| <span data-ttu-id="ab429-267">msdyn_progress</span><span class="sxs-lookup"><span data-stu-id="ab429-267">msdyn_progress</span></span>                         | <span data-ttu-id="ab429-268">ei</span><span class="sxs-lookup"><span data-stu-id="ab429-268">no</span></span>             | <span data-ttu-id="ab429-269">ei (kyllä P4W:lle)</span><span class="sxs-lookup"><span data-stu-id="ab429-269">no (yes for P4W)</span></span> |
| <span data-ttu-id="ab429-270">msdyn_remainingcost</span><span class="sxs-lookup"><span data-stu-id="ab429-270">msdyn_remainingcost</span></span>                    | <span data-ttu-id="ab429-271">ei</span><span class="sxs-lookup"><span data-stu-id="ab429-271">no</span></span>             | <span data-ttu-id="ab429-272">ei</span><span class="sxs-lookup"><span data-stu-id="ab429-272">no</span></span>               |
| <span data-ttu-id="ab429-273">msdyn_remainingcost_base</span><span class="sxs-lookup"><span data-stu-id="ab429-273">msdyn_remainingcost_base</span></span>               | <span data-ttu-id="ab429-274">ei</span><span class="sxs-lookup"><span data-stu-id="ab429-274">no</span></span>             | <span data-ttu-id="ab429-275">ei</span><span class="sxs-lookup"><span data-stu-id="ab429-275">no</span></span>               |
| <span data-ttu-id="ab429-276">msdyn_remainingsales</span><span class="sxs-lookup"><span data-stu-id="ab429-276">msdyn_remainingsales</span></span>                   | <span data-ttu-id="ab429-277">ei</span><span class="sxs-lookup"><span data-stu-id="ab429-277">no</span></span>             | <span data-ttu-id="ab429-278">ei</span><span class="sxs-lookup"><span data-stu-id="ab429-278">no</span></span>               |
| <span data-ttu-id="ab429-279">msdyn_remainingsales_base</span><span class="sxs-lookup"><span data-stu-id="ab429-279">msdyn_remainingsales_base</span></span>              | <span data-ttu-id="ab429-280">ei</span><span class="sxs-lookup"><span data-stu-id="ab429-280">no</span></span>             | <span data-ttu-id="ab429-281">ei</span><span class="sxs-lookup"><span data-stu-id="ab429-281">no</span></span>               |
| <span data-ttu-id="ab429-282">msdyn_requestedhours</span><span class="sxs-lookup"><span data-stu-id="ab429-282">msdyn_requestedhours</span></span>                   | <span data-ttu-id="ab429-283">ei</span><span class="sxs-lookup"><span data-stu-id="ab429-283">no</span></span>             | <span data-ttu-id="ab429-284">ei</span><span class="sxs-lookup"><span data-stu-id="ab429-284">no</span></span>               |
| <span data-ttu-id="ab429-285">msdyn_resourcecategory</span><span class="sxs-lookup"><span data-stu-id="ab429-285">msdyn_resourcecategory</span></span>                 | <span data-ttu-id="ab429-286">ei</span><span class="sxs-lookup"><span data-stu-id="ab429-286">no</span></span>             | <span data-ttu-id="ab429-287">ei</span><span class="sxs-lookup"><span data-stu-id="ab429-287">no</span></span>               |
| <span data-ttu-id="ab429-288">msdyn_resourcecategoryname</span><span class="sxs-lookup"><span data-stu-id="ab429-288">msdyn_resourcecategoryname</span></span>             | <span data-ttu-id="ab429-289">ei</span><span class="sxs-lookup"><span data-stu-id="ab429-289">no</span></span>             | <span data-ttu-id="ab429-290">ei</span><span class="sxs-lookup"><span data-stu-id="ab429-290">no</span></span>               |
| <span data-ttu-id="ab429-291">msdyn_resourceorganizationalunitid</span><span class="sxs-lookup"><span data-stu-id="ab429-291">msdyn_resourceorganizationalunitid</span></span>     | <span data-ttu-id="ab429-292">ei</span><span class="sxs-lookup"><span data-stu-id="ab429-292">no</span></span>             | <span data-ttu-id="ab429-293">ei</span><span class="sxs-lookup"><span data-stu-id="ab429-293">no</span></span>               |
| <span data-ttu-id="ab429-294">msdyn_resourceorganizationalunitidname</span><span class="sxs-lookup"><span data-stu-id="ab429-294">msdyn_resourceorganizationalunitidname</span></span> | <span data-ttu-id="ab429-295">ei</span><span class="sxs-lookup"><span data-stu-id="ab429-295">no</span></span>             | <span data-ttu-id="ab429-296">ei</span><span class="sxs-lookup"><span data-stu-id="ab429-296">no</span></span>               |
| <span data-ttu-id="ab429-297">msdyn_salesconsumptionpercentage</span><span class="sxs-lookup"><span data-stu-id="ab429-297">msdyn_salesconsumptionpercentage</span></span>       | <span data-ttu-id="ab429-298">ei</span><span class="sxs-lookup"><span data-stu-id="ab429-298">no</span></span>             | <span data-ttu-id="ab429-299">ei</span><span class="sxs-lookup"><span data-stu-id="ab429-299">no</span></span>               |
| <span data-ttu-id="ab429-300">msdyn_salesestimateatcomplete</span><span class="sxs-lookup"><span data-stu-id="ab429-300">msdyn_salesestimateatcomplete</span></span>          | <span data-ttu-id="ab429-301">ei</span><span class="sxs-lookup"><span data-stu-id="ab429-301">no</span></span>             | <span data-ttu-id="ab429-302">ei</span><span class="sxs-lookup"><span data-stu-id="ab429-302">no</span></span>               |
| <span data-ttu-id="ab429-303">msdyn_salesestimateatcomplete_base</span><span class="sxs-lookup"><span data-stu-id="ab429-303">msdyn_salesestimateatcomplete_base</span></span>     | <span data-ttu-id="ab429-304">ei</span><span class="sxs-lookup"><span data-stu-id="ab429-304">no</span></span>             | <span data-ttu-id="ab429-305">ei</span><span class="sxs-lookup"><span data-stu-id="ab429-305">no</span></span>               |
| <span data-ttu-id="ab429-306">msdyn_salesvariance</span><span class="sxs-lookup"><span data-stu-id="ab429-306">msdyn_salesvariance</span></span>                    | <span data-ttu-id="ab429-307">ei</span><span class="sxs-lookup"><span data-stu-id="ab429-307">no</span></span>             | <span data-ttu-id="ab429-308">ei</span><span class="sxs-lookup"><span data-stu-id="ab429-308">no</span></span>               |
| <span data-ttu-id="ab429-309">msdyn_salesvariance_base</span><span class="sxs-lookup"><span data-stu-id="ab429-309">msdyn_salesvariance_base</span></span>               | <span data-ttu-id="ab429-310">ei</span><span class="sxs-lookup"><span data-stu-id="ab429-310">no</span></span>             | <span data-ttu-id="ab429-311">ei</span><span class="sxs-lookup"><span data-stu-id="ab429-311">no</span></span>               |
| <span data-ttu-id="ab429-312">msdyn_scheduleddurationminutes</span><span class="sxs-lookup"><span data-stu-id="ab429-312">msdyn_scheduleddurationminutes</span></span>         | <span data-ttu-id="ab429-313">ei</span><span class="sxs-lookup"><span data-stu-id="ab429-313">no</span></span>             | <span data-ttu-id="ab429-314">ei</span><span class="sxs-lookup"><span data-stu-id="ab429-314">no</span></span>               |
| <span data-ttu-id="ab429-315">msdyn_scheduledend</span><span class="sxs-lookup"><span data-stu-id="ab429-315">msdyn_scheduledend</span></span>                     | <span data-ttu-id="ab429-316">ei</span><span class="sxs-lookup"><span data-stu-id="ab429-316">no</span></span>             | <span data-ttu-id="ab429-317">ei</span><span class="sxs-lookup"><span data-stu-id="ab429-317">no</span></span>               |
| <span data-ttu-id="ab429-318">msdyn_scheduledstart</span><span class="sxs-lookup"><span data-stu-id="ab429-318">msdyn_scheduledstart</span></span>                   | <span data-ttu-id="ab429-319">ei</span><span class="sxs-lookup"><span data-stu-id="ab429-319">no</span></span>             | <span data-ttu-id="ab429-320">ei</span><span class="sxs-lookup"><span data-stu-id="ab429-320">no</span></span>               |
| <span data-ttu-id="ab429-321">msdyn_schedulevariance</span><span class="sxs-lookup"><span data-stu-id="ab429-321">msdyn_schedulevariance</span></span>                 | <span data-ttu-id="ab429-322">ei</span><span class="sxs-lookup"><span data-stu-id="ab429-322">no</span></span>             | <span data-ttu-id="ab429-323">ei</span><span class="sxs-lookup"><span data-stu-id="ab429-323">no</span></span>               |
| <span data-ttu-id="ab429-324">msdyn_skipupdateestimateline</span><span class="sxs-lookup"><span data-stu-id="ab429-324">msdyn_skipupdateestimateline</span></span>           | <span data-ttu-id="ab429-325">ei</span><span class="sxs-lookup"><span data-stu-id="ab429-325">no</span></span>             | <span data-ttu-id="ab429-326">ei</span><span class="sxs-lookup"><span data-stu-id="ab429-326">no</span></span>               |
| <span data-ttu-id="ab429-327">msdyn_skipupdateestimatelinename</span><span class="sxs-lookup"><span data-stu-id="ab429-327">msdyn_skipupdateestimatelinename</span></span>       | <span data-ttu-id="ab429-328">ei</span><span class="sxs-lookup"><span data-stu-id="ab429-328">no</span></span>             | <span data-ttu-id="ab429-329">ei</span><span class="sxs-lookup"><span data-stu-id="ab429-329">no</span></span>               |
| <span data-ttu-id="ab429-330">msdyn_summary</span><span class="sxs-lookup"><span data-stu-id="ab429-330">msdyn_summary</span></span>                          | <span data-ttu-id="ab429-331">ei</span><span class="sxs-lookup"><span data-stu-id="ab429-331">no</span></span>             | <span data-ttu-id="ab429-332">ei</span><span class="sxs-lookup"><span data-stu-id="ab429-332">no</span></span>               |
| <span data-ttu-id="ab429-333">msdyn_varianceofcost</span><span class="sxs-lookup"><span data-stu-id="ab429-333">msdyn_varianceofcost</span></span>                   | <span data-ttu-id="ab429-334">ei</span><span class="sxs-lookup"><span data-stu-id="ab429-334">no</span></span>             | <span data-ttu-id="ab429-335">ei</span><span class="sxs-lookup"><span data-stu-id="ab429-335">no</span></span>               |
| <span data-ttu-id="ab429-336">msdyn_varianceofcost_base</span><span class="sxs-lookup"><span data-stu-id="ab429-336">msdyn_varianceofcost_base</span></span>              | <span data-ttu-id="ab429-337">ei</span><span class="sxs-lookup"><span data-stu-id="ab429-337">no</span></span>             | <span data-ttu-id="ab429-338">ei</span><span class="sxs-lookup"><span data-stu-id="ab429-338">no</span></span>               |

### <a name="project-task-dependency"></a><span data-ttu-id="ab429-339">Projektitehtävän riippuvuus</span><span class="sxs-lookup"><span data-stu-id="ab429-339">Project task dependency</span></span>

| <span data-ttu-id="ab429-340">**Looginen nimi**</span><span class="sxs-lookup"><span data-stu-id="ab429-340">**Logical name**</span></span>              | <span data-ttu-id="ab429-341">**Voidaan luoda**</span><span class="sxs-lookup"><span data-stu-id="ab429-341">**Can create**</span></span> | <span data-ttu-id="ab429-342">**Voidaan muokata**</span><span class="sxs-lookup"><span data-stu-id="ab429-342">**Can edit**</span></span> |
|-------------------------------|----------------|--------------|
| <span data-ttu-id="ab429-343">msdyn_linktype</span><span class="sxs-lookup"><span data-stu-id="ab429-343">msdyn_linktype</span></span>                | <span data-ttu-id="ab429-344">ei</span><span class="sxs-lookup"><span data-stu-id="ab429-344">no</span></span>             | <span data-ttu-id="ab429-345">ei</span><span class="sxs-lookup"><span data-stu-id="ab429-345">no</span></span>           |
| <span data-ttu-id="ab429-346">msdyn_linktypename</span><span class="sxs-lookup"><span data-stu-id="ab429-346">msdyn_linktypename</span></span>            | <span data-ttu-id="ab429-347">ei</span><span class="sxs-lookup"><span data-stu-id="ab429-347">no</span></span>             | <span data-ttu-id="ab429-348">ei</span><span class="sxs-lookup"><span data-stu-id="ab429-348">no</span></span>           |
| <span data-ttu-id="ab429-349">msdyn_predecessortask</span><span class="sxs-lookup"><span data-stu-id="ab429-349">msdyn_predecessortask</span></span>         | <span data-ttu-id="ab429-350">kyllä</span><span class="sxs-lookup"><span data-stu-id="ab429-350">yes</span></span>            | <span data-ttu-id="ab429-351">ei</span><span class="sxs-lookup"><span data-stu-id="ab429-351">no</span></span>           |
| <span data-ttu-id="ab429-352">msdyn_predecessortaskname</span><span class="sxs-lookup"><span data-stu-id="ab429-352">msdyn_predecessortaskname</span></span>     | <span data-ttu-id="ab429-353">kyllä</span><span class="sxs-lookup"><span data-stu-id="ab429-353">yes</span></span>            | <span data-ttu-id="ab429-354">ei</span><span class="sxs-lookup"><span data-stu-id="ab429-354">no</span></span>           |
| <span data-ttu-id="ab429-355">msdyn_project</span><span class="sxs-lookup"><span data-stu-id="ab429-355">msdyn_project</span></span>                 | <span data-ttu-id="ab429-356">kyllä</span><span class="sxs-lookup"><span data-stu-id="ab429-356">yes</span></span>            | <span data-ttu-id="ab429-357">ei</span><span class="sxs-lookup"><span data-stu-id="ab429-357">no</span></span>           |
| <span data-ttu-id="ab429-358">msdyn_projectname</span><span class="sxs-lookup"><span data-stu-id="ab429-358">msdyn_projectname</span></span>             | <span data-ttu-id="ab429-359">kyllä</span><span class="sxs-lookup"><span data-stu-id="ab429-359">yes</span></span>            | <span data-ttu-id="ab429-360">ei</span><span class="sxs-lookup"><span data-stu-id="ab429-360">no</span></span>           |
| <span data-ttu-id="ab429-361">msdyn_projecttaskdependencyid</span><span class="sxs-lookup"><span data-stu-id="ab429-361">msdyn_projecttaskdependencyid</span></span> | <span data-ttu-id="ab429-362">kyllä</span><span class="sxs-lookup"><span data-stu-id="ab429-362">yes</span></span>            | <span data-ttu-id="ab429-363">ei</span><span class="sxs-lookup"><span data-stu-id="ab429-363">no</span></span>           |
| <span data-ttu-id="ab429-364">msdyn_successortask</span><span class="sxs-lookup"><span data-stu-id="ab429-364">msdyn_successortask</span></span>           | <span data-ttu-id="ab429-365">kyllä</span><span class="sxs-lookup"><span data-stu-id="ab429-365">yes</span></span>            | <span data-ttu-id="ab429-366">ei</span><span class="sxs-lookup"><span data-stu-id="ab429-366">no</span></span>           |
| <span data-ttu-id="ab429-367">msdyn_successortaskname</span><span class="sxs-lookup"><span data-stu-id="ab429-367">msdyn_successortaskname</span></span>       | <span data-ttu-id="ab429-368">kyllä</span><span class="sxs-lookup"><span data-stu-id="ab429-368">yes</span></span>            | <span data-ttu-id="ab429-369">ei</span><span class="sxs-lookup"><span data-stu-id="ab429-369">no</span></span>           |

### <a name="resource-assignment"></a><span data-ttu-id="ab429-370">Resurssien delegointi</span><span class="sxs-lookup"><span data-stu-id="ab429-370">Resource assignment</span></span>

| <span data-ttu-id="ab429-371">**Looginen nimi**</span><span class="sxs-lookup"><span data-stu-id="ab429-371">**Logical name**</span></span>             | <span data-ttu-id="ab429-372">**Voidaan luoda**</span><span class="sxs-lookup"><span data-stu-id="ab429-372">**Can create**</span></span> | <span data-ttu-id="ab429-373">**Voidaan muokata**</span><span class="sxs-lookup"><span data-stu-id="ab429-373">**Can edit**</span></span> |
|------------------------------|----------------|--------------|
| <span data-ttu-id="ab429-374">msdyn_bookableresourceid</span><span class="sxs-lookup"><span data-stu-id="ab429-374">msdyn_bookableresourceid</span></span>     | <span data-ttu-id="ab429-375">kyllä</span><span class="sxs-lookup"><span data-stu-id="ab429-375">yes</span></span>            | <span data-ttu-id="ab429-376">ei</span><span class="sxs-lookup"><span data-stu-id="ab429-376">no</span></span>           |
| <span data-ttu-id="ab429-377">msdyn_bookableresourceidname</span><span class="sxs-lookup"><span data-stu-id="ab429-377">msdyn_bookableresourceidname</span></span> | <span data-ttu-id="ab429-378">kyllä</span><span class="sxs-lookup"><span data-stu-id="ab429-378">yes</span></span>            | <span data-ttu-id="ab429-379">ei</span><span class="sxs-lookup"><span data-stu-id="ab429-379">no</span></span>           |
| <span data-ttu-id="ab429-380">msdyn_bookingstatusid</span><span class="sxs-lookup"><span data-stu-id="ab429-380">msdyn_bookingstatusid</span></span>        | <span data-ttu-id="ab429-381">ei</span><span class="sxs-lookup"><span data-stu-id="ab429-381">no</span></span>             | <span data-ttu-id="ab429-382">ei</span><span class="sxs-lookup"><span data-stu-id="ab429-382">no</span></span>           |
| <span data-ttu-id="ab429-383">msdyn_bookingstatusidname</span><span class="sxs-lookup"><span data-stu-id="ab429-383">msdyn_bookingstatusidname</span></span>    | <span data-ttu-id="ab429-384">ei</span><span class="sxs-lookup"><span data-stu-id="ab429-384">no</span></span>             | <span data-ttu-id="ab429-385">ei</span><span class="sxs-lookup"><span data-stu-id="ab429-385">no</span></span>           |
| <span data-ttu-id="ab429-386">msdyn_committype</span><span class="sxs-lookup"><span data-stu-id="ab429-386">msdyn_committype</span></span>             | <span data-ttu-id="ab429-387">ei</span><span class="sxs-lookup"><span data-stu-id="ab429-387">no</span></span>             | <span data-ttu-id="ab429-388">ei</span><span class="sxs-lookup"><span data-stu-id="ab429-388">no</span></span>           |
| <span data-ttu-id="ab429-389">msdyn_committypename</span><span class="sxs-lookup"><span data-stu-id="ab429-389">msdyn_committypename</span></span>         | <span data-ttu-id="ab429-390">ei</span><span class="sxs-lookup"><span data-stu-id="ab429-390">no</span></span>             | <span data-ttu-id="ab429-391">ei</span><span class="sxs-lookup"><span data-stu-id="ab429-391">no</span></span>           |
| <span data-ttu-id="ab429-392">msdyn_effort</span><span class="sxs-lookup"><span data-stu-id="ab429-392">msdyn_effort</span></span>                 | <span data-ttu-id="ab429-393">ei</span><span class="sxs-lookup"><span data-stu-id="ab429-393">no</span></span>             | <span data-ttu-id="ab429-394">ei</span><span class="sxs-lookup"><span data-stu-id="ab429-394">no</span></span>           |
| <span data-ttu-id="ab429-395">msdyn_effortcompleted</span><span class="sxs-lookup"><span data-stu-id="ab429-395">msdyn_effortcompleted</span></span>        | <span data-ttu-id="ab429-396">ei</span><span class="sxs-lookup"><span data-stu-id="ab429-396">no</span></span>             | <span data-ttu-id="ab429-397">ei</span><span class="sxs-lookup"><span data-stu-id="ab429-397">no</span></span>           |
| <span data-ttu-id="ab429-398">msdyn_effortremaining</span><span class="sxs-lookup"><span data-stu-id="ab429-398">msdyn_effortremaining</span></span>        | <span data-ttu-id="ab429-399">ei</span><span class="sxs-lookup"><span data-stu-id="ab429-399">no</span></span>             | <span data-ttu-id="ab429-400">ei</span><span class="sxs-lookup"><span data-stu-id="ab429-400">no</span></span>           |
| <span data-ttu-id="ab429-401">msdyn_finish</span><span class="sxs-lookup"><span data-stu-id="ab429-401">msdyn_finish</span></span>                 | <span data-ttu-id="ab429-402">ei</span><span class="sxs-lookup"><span data-stu-id="ab429-402">no</span></span>             | <span data-ttu-id="ab429-403">ei</span><span class="sxs-lookup"><span data-stu-id="ab429-403">no</span></span>           |
| <span data-ttu-id="ab429-404">msdyn_plannedcost</span><span class="sxs-lookup"><span data-stu-id="ab429-404">msdyn_plannedcost</span></span>            | <span data-ttu-id="ab429-405">ei</span><span class="sxs-lookup"><span data-stu-id="ab429-405">no</span></span>             | <span data-ttu-id="ab429-406">ei</span><span class="sxs-lookup"><span data-stu-id="ab429-406">no</span></span>           |
| <span data-ttu-id="ab429-407">msdyn_plannedcost_base</span><span class="sxs-lookup"><span data-stu-id="ab429-407">msdyn_plannedcost_base</span></span>       | <span data-ttu-id="ab429-408">ei</span><span class="sxs-lookup"><span data-stu-id="ab429-408">no</span></span>             | <span data-ttu-id="ab429-409">ei</span><span class="sxs-lookup"><span data-stu-id="ab429-409">no</span></span>           |
| <span data-ttu-id="ab429-410">msdyn_plannedcostcontour</span><span class="sxs-lookup"><span data-stu-id="ab429-410">msdyn_plannedcostcontour</span></span>     | <span data-ttu-id="ab429-411">ei</span><span class="sxs-lookup"><span data-stu-id="ab429-411">no</span></span>             | <span data-ttu-id="ab429-412">ei</span><span class="sxs-lookup"><span data-stu-id="ab429-412">no</span></span>           |
| <span data-ttu-id="ab429-413">msdyn_plannedsales</span><span class="sxs-lookup"><span data-stu-id="ab429-413">msdyn_plannedsales</span></span>           | <span data-ttu-id="ab429-414">ei</span><span class="sxs-lookup"><span data-stu-id="ab429-414">no</span></span>             | <span data-ttu-id="ab429-415">ei</span><span class="sxs-lookup"><span data-stu-id="ab429-415">no</span></span>           |
| <span data-ttu-id="ab429-416">msdyn_plannedsales_base</span><span class="sxs-lookup"><span data-stu-id="ab429-416">msdyn_plannedsales_base</span></span>      | <span data-ttu-id="ab429-417">ei</span><span class="sxs-lookup"><span data-stu-id="ab429-417">no</span></span>             | <span data-ttu-id="ab429-418">ei</span><span class="sxs-lookup"><span data-stu-id="ab429-418">no</span></span>           |
| <span data-ttu-id="ab429-419">msdyn_plannedsalescontour</span><span class="sxs-lookup"><span data-stu-id="ab429-419">msdyn_plannedsalescontour</span></span>    | <span data-ttu-id="ab429-420">ei</span><span class="sxs-lookup"><span data-stu-id="ab429-420">no</span></span>             | <span data-ttu-id="ab429-421">ei</span><span class="sxs-lookup"><span data-stu-id="ab429-421">no</span></span>           |
| <span data-ttu-id="ab429-422">msdyn_plannedwork</span><span class="sxs-lookup"><span data-stu-id="ab429-422">msdyn_plannedwork</span></span>            | <span data-ttu-id="ab429-423">ei</span><span class="sxs-lookup"><span data-stu-id="ab429-423">no</span></span>             | <span data-ttu-id="ab429-424">ei</span><span class="sxs-lookup"><span data-stu-id="ab429-424">no</span></span>           |
| <span data-ttu-id="ab429-425">msdyn_projectid</span><span class="sxs-lookup"><span data-stu-id="ab429-425">msdyn_projectid</span></span>              | <span data-ttu-id="ab429-426">kyllä</span><span class="sxs-lookup"><span data-stu-id="ab429-426">yes</span></span>            | <span data-ttu-id="ab429-427">ei</span><span class="sxs-lookup"><span data-stu-id="ab429-427">no</span></span>           |
| <span data-ttu-id="ab429-428">msdyn_projectidname</span><span class="sxs-lookup"><span data-stu-id="ab429-428">msdyn_projectidname</span></span>          | <span data-ttu-id="ab429-429">ei</span><span class="sxs-lookup"><span data-stu-id="ab429-429">no</span></span>             | <span data-ttu-id="ab429-430">ei</span><span class="sxs-lookup"><span data-stu-id="ab429-430">no</span></span>           |
| <span data-ttu-id="ab429-431">msdyn_projectteamid</span><span class="sxs-lookup"><span data-stu-id="ab429-431">msdyn_projectteamid</span></span>          | <span data-ttu-id="ab429-432">ei</span><span class="sxs-lookup"><span data-stu-id="ab429-432">no</span></span>             | <span data-ttu-id="ab429-433">ei</span><span class="sxs-lookup"><span data-stu-id="ab429-433">no</span></span>           |
| <span data-ttu-id="ab429-434">msdyn_projectteamidname</span><span class="sxs-lookup"><span data-stu-id="ab429-434">msdyn_projectteamidname</span></span>      | <span data-ttu-id="ab429-435">ei</span><span class="sxs-lookup"><span data-stu-id="ab429-435">no</span></span>             | <span data-ttu-id="ab429-436">ei</span><span class="sxs-lookup"><span data-stu-id="ab429-436">no</span></span>           |
| <span data-ttu-id="ab429-437">msdyn_start</span><span class="sxs-lookup"><span data-stu-id="ab429-437">msdyn_start</span></span>                  | <span data-ttu-id="ab429-438">ei</span><span class="sxs-lookup"><span data-stu-id="ab429-438">no</span></span>             | <span data-ttu-id="ab429-439">ei</span><span class="sxs-lookup"><span data-stu-id="ab429-439">no</span></span>           |
| <span data-ttu-id="ab429-440">msdyn_taskid</span><span class="sxs-lookup"><span data-stu-id="ab429-440">msdyn_taskid</span></span>                 | <span data-ttu-id="ab429-441">ei</span><span class="sxs-lookup"><span data-stu-id="ab429-441">no</span></span>             | <span data-ttu-id="ab429-442">ei</span><span class="sxs-lookup"><span data-stu-id="ab429-442">no</span></span>           |
| <span data-ttu-id="ab429-443">msdyn_taskidname</span><span class="sxs-lookup"><span data-stu-id="ab429-443">msdyn_taskidname</span></span>             | <span data-ttu-id="ab429-444">ei</span><span class="sxs-lookup"><span data-stu-id="ab429-444">no</span></span>             | <span data-ttu-id="ab429-445">ei</span><span class="sxs-lookup"><span data-stu-id="ab429-445">no</span></span>           |
| <span data-ttu-id="ab429-446">msdyn_userresourceid</span><span class="sxs-lookup"><span data-stu-id="ab429-446">msdyn_userresourceid</span></span>         | <span data-ttu-id="ab429-447">ei</span><span class="sxs-lookup"><span data-stu-id="ab429-447">no</span></span>             | <span data-ttu-id="ab429-448">ei</span><span class="sxs-lookup"><span data-stu-id="ab429-448">no</span></span>           |

### <a name="project-team-member"></a><span data-ttu-id="ab429-449">Projektiryhmän jäsen</span><span class="sxs-lookup"><span data-stu-id="ab429-449">Project team member</span></span>

| <span data-ttu-id="ab429-450">**Looginen nimi**</span><span class="sxs-lookup"><span data-stu-id="ab429-450">**Logical name**</span></span>                                 | <span data-ttu-id="ab429-451">**Voidaan luoda**</span><span class="sxs-lookup"><span data-stu-id="ab429-451">**Can create**</span></span> | <span data-ttu-id="ab429-452">**Voidaan muokata**</span><span class="sxs-lookup"><span data-stu-id="ab429-452">**Can edit**</span></span> |
|--------------------------------------------------|----------------|--------------|
| <span data-ttu-id="ab429-453">msdyn_calendarid</span><span class="sxs-lookup"><span data-stu-id="ab429-453">msdyn_calendarid</span></span>                                 | <span data-ttu-id="ab429-454">ei</span><span class="sxs-lookup"><span data-stu-id="ab429-454">no</span></span>             | <span data-ttu-id="ab429-455">ei</span><span class="sxs-lookup"><span data-stu-id="ab429-455">no</span></span>           |
| <span data-ttu-id="ab429-456">msdyn_creategenericteammemberwithrequirementname</span><span class="sxs-lookup"><span data-stu-id="ab429-456">msdyn_creategenericteammemberwithrequirementname</span></span> | <span data-ttu-id="ab429-457">ei</span><span class="sxs-lookup"><span data-stu-id="ab429-457">no</span></span>             | <span data-ttu-id="ab429-458">ei</span><span class="sxs-lookup"><span data-stu-id="ab429-458">no</span></span>           |
| <span data-ttu-id="ab429-459">msdyn_deletestatus</span><span class="sxs-lookup"><span data-stu-id="ab429-459">msdyn_deletestatus</span></span>                               | <span data-ttu-id="ab429-460">ei</span><span class="sxs-lookup"><span data-stu-id="ab429-460">no</span></span>             | <span data-ttu-id="ab429-461">ei</span><span class="sxs-lookup"><span data-stu-id="ab429-461">no</span></span>           |
| <span data-ttu-id="ab429-462">msdyn_deletestatusname</span><span class="sxs-lookup"><span data-stu-id="ab429-462">msdyn_deletestatusname</span></span>                           | <span data-ttu-id="ab429-463">ei</span><span class="sxs-lookup"><span data-stu-id="ab429-463">no</span></span>             | <span data-ttu-id="ab429-464">ei</span><span class="sxs-lookup"><span data-stu-id="ab429-464">no</span></span>           |
| <span data-ttu-id="ab429-465">msdyn_effort</span><span class="sxs-lookup"><span data-stu-id="ab429-465">msdyn_effort</span></span>                                     | <span data-ttu-id="ab429-466">ei</span><span class="sxs-lookup"><span data-stu-id="ab429-466">no</span></span>             | <span data-ttu-id="ab429-467">ei</span><span class="sxs-lookup"><span data-stu-id="ab429-467">no</span></span>           |
| <span data-ttu-id="ab429-468">msdyn_effortcompleted</span><span class="sxs-lookup"><span data-stu-id="ab429-468">msdyn_effortcompleted</span></span>                            | <span data-ttu-id="ab429-469">ei</span><span class="sxs-lookup"><span data-stu-id="ab429-469">no</span></span>             | <span data-ttu-id="ab429-470">ei</span><span class="sxs-lookup"><span data-stu-id="ab429-470">no</span></span>           |
| <span data-ttu-id="ab429-471">msdyn_effortremaining</span><span class="sxs-lookup"><span data-stu-id="ab429-471">msdyn_effortremaining</span></span>                            | <span data-ttu-id="ab429-472">ei</span><span class="sxs-lookup"><span data-stu-id="ab429-472">no</span></span>             | <span data-ttu-id="ab429-473">ei</span><span class="sxs-lookup"><span data-stu-id="ab429-473">no</span></span>           |
| <span data-ttu-id="ab429-474">msdyn_finish</span><span class="sxs-lookup"><span data-stu-id="ab429-474">msdyn_finish</span></span>                                     | <span data-ttu-id="ab429-475">ei</span><span class="sxs-lookup"><span data-stu-id="ab429-475">no</span></span>             | <span data-ttu-id="ab429-476">ei</span><span class="sxs-lookup"><span data-stu-id="ab429-476">no</span></span>           |
| <span data-ttu-id="ab429-477">msdyn_hardbookedhours</span><span class="sxs-lookup"><span data-stu-id="ab429-477">msdyn_hardbookedhours</span></span>                            | <span data-ttu-id="ab429-478">ei</span><span class="sxs-lookup"><span data-stu-id="ab429-478">no</span></span>             | <span data-ttu-id="ab429-479">ei</span><span class="sxs-lookup"><span data-stu-id="ab429-479">no</span></span>           |
| <span data-ttu-id="ab429-480">msdyn_hours</span><span class="sxs-lookup"><span data-stu-id="ab429-480">msdyn_hours</span></span>                                      | <span data-ttu-id="ab429-481">ei</span><span class="sxs-lookup"><span data-stu-id="ab429-481">no</span></span>             | <span data-ttu-id="ab429-482">ei</span><span class="sxs-lookup"><span data-stu-id="ab429-482">no</span></span>           |
| <span data-ttu-id="ab429-483">msdyn_markedfordeletiontimer</span><span class="sxs-lookup"><span data-stu-id="ab429-483">msdyn_markedfordeletiontimer</span></span>                     | <span data-ttu-id="ab429-484">ei</span><span class="sxs-lookup"><span data-stu-id="ab429-484">no</span></span>             | <span data-ttu-id="ab429-485">ei</span><span class="sxs-lookup"><span data-stu-id="ab429-485">no</span></span>           |
| <span data-ttu-id="ab429-486">msdyn_markedfordeletiontimestamp</span><span class="sxs-lookup"><span data-stu-id="ab429-486">msdyn_markedfordeletiontimestamp</span></span>                 | <span data-ttu-id="ab429-487">ei</span><span class="sxs-lookup"><span data-stu-id="ab429-487">no</span></span>             | <span data-ttu-id="ab429-488">ei</span><span class="sxs-lookup"><span data-stu-id="ab429-488">no</span></span>           |
| <span data-ttu-id="ab429-489">msdyn_msprojectclientid</span><span class="sxs-lookup"><span data-stu-id="ab429-489">msdyn_msprojectclientid</span></span>                          | <span data-ttu-id="ab429-490">ei</span><span class="sxs-lookup"><span data-stu-id="ab429-490">no</span></span>             | <span data-ttu-id="ab429-491">ei</span><span class="sxs-lookup"><span data-stu-id="ab429-491">no</span></span>           |
| <span data-ttu-id="ab429-492">msdyn_percentage</span><span class="sxs-lookup"><span data-stu-id="ab429-492">msdyn_percentage</span></span>                                 | <span data-ttu-id="ab429-493">ei</span><span class="sxs-lookup"><span data-stu-id="ab429-493">no</span></span>             | <span data-ttu-id="ab429-494">ei</span><span class="sxs-lookup"><span data-stu-id="ab429-494">no</span></span>           |
| <span data-ttu-id="ab429-495">msdyn_requiredhours</span><span class="sxs-lookup"><span data-stu-id="ab429-495">msdyn_requiredhours</span></span>                              | <span data-ttu-id="ab429-496">ei</span><span class="sxs-lookup"><span data-stu-id="ab429-496">no</span></span>             | <span data-ttu-id="ab429-497">ei</span><span class="sxs-lookup"><span data-stu-id="ab429-497">no</span></span>           |
| <span data-ttu-id="ab429-498">msdyn_softbookedhours</span><span class="sxs-lookup"><span data-stu-id="ab429-498">msdyn_softbookedhours</span></span>                            | <span data-ttu-id="ab429-499">ei</span><span class="sxs-lookup"><span data-stu-id="ab429-499">no</span></span>             | <span data-ttu-id="ab429-500">ei</span><span class="sxs-lookup"><span data-stu-id="ab429-500">no</span></span>           |
| <span data-ttu-id="ab429-501">msdyn_start</span><span class="sxs-lookup"><span data-stu-id="ab429-501">msdyn_start</span></span>                                      | <span data-ttu-id="ab429-502">ei</span><span class="sxs-lookup"><span data-stu-id="ab429-502">no</span></span>             | <span data-ttu-id="ab429-503">ei</span><span class="sxs-lookup"><span data-stu-id="ab429-503">no</span></span>           |

### <a name="project"></a><span data-ttu-id="ab429-504">Project</span><span class="sxs-lookup"><span data-stu-id="ab429-504">Project</span></span>

| <span data-ttu-id="ab429-505">**Looginen nimi**</span><span class="sxs-lookup"><span data-stu-id="ab429-505">**Logical name**</span></span>                       | <span data-ttu-id="ab429-506">**Voidaan luoda**</span><span class="sxs-lookup"><span data-stu-id="ab429-506">**Can create**</span></span> | <span data-ttu-id="ab429-507">**Voidaan muokata**</span><span class="sxs-lookup"><span data-stu-id="ab429-507">**Can edit**</span></span> |
|----------------------------------------|----------------|--------------|
| <span data-ttu-id="ab429-508">msdyn_actualexpensecost</span><span class="sxs-lookup"><span data-stu-id="ab429-508">msdyn_actualexpensecost</span></span>                | <span data-ttu-id="ab429-509">ei</span><span class="sxs-lookup"><span data-stu-id="ab429-509">no</span></span>             | <span data-ttu-id="ab429-510">ei</span><span class="sxs-lookup"><span data-stu-id="ab429-510">no</span></span>           |
| <span data-ttu-id="ab429-511">msdyn_actualexpensecost_base</span><span class="sxs-lookup"><span data-stu-id="ab429-511">msdyn_actualexpensecost_base</span></span>           | <span data-ttu-id="ab429-512">ei</span><span class="sxs-lookup"><span data-stu-id="ab429-512">no</span></span>             | <span data-ttu-id="ab429-513">ei</span><span class="sxs-lookup"><span data-stu-id="ab429-513">no</span></span>           |
| <span data-ttu-id="ab429-514">msdyn_actuallaborcost</span><span class="sxs-lookup"><span data-stu-id="ab429-514">msdyn_actuallaborcost</span></span>                  | <span data-ttu-id="ab429-515">ei</span><span class="sxs-lookup"><span data-stu-id="ab429-515">no</span></span>             | <span data-ttu-id="ab429-516">ei</span><span class="sxs-lookup"><span data-stu-id="ab429-516">no</span></span>           |
| <span data-ttu-id="ab429-517">msdyn_actuallaborcost_base</span><span class="sxs-lookup"><span data-stu-id="ab429-517">msdyn_actuallaborcost_base</span></span>             | <span data-ttu-id="ab429-518">ei</span><span class="sxs-lookup"><span data-stu-id="ab429-518">no</span></span>             | <span data-ttu-id="ab429-519">ei</span><span class="sxs-lookup"><span data-stu-id="ab429-519">no</span></span>           |
| <span data-ttu-id="ab429-520">msdyn_actualsales</span><span class="sxs-lookup"><span data-stu-id="ab429-520">msdyn_actualsales</span></span>                      | <span data-ttu-id="ab429-521">ei</span><span class="sxs-lookup"><span data-stu-id="ab429-521">no</span></span>             | <span data-ttu-id="ab429-522">ei</span><span class="sxs-lookup"><span data-stu-id="ab429-522">no</span></span>           |
| <span data-ttu-id="ab429-523">msdyn_actualsales_base</span><span class="sxs-lookup"><span data-stu-id="ab429-523">msdyn_actualsales_base</span></span>                 | <span data-ttu-id="ab429-524">ei</span><span class="sxs-lookup"><span data-stu-id="ab429-524">no</span></span>             | <span data-ttu-id="ab429-525">ei</span><span class="sxs-lookup"><span data-stu-id="ab429-525">no</span></span>           |
| <span data-ttu-id="ab429-526">msdyn_contractlineproject</span><span class="sxs-lookup"><span data-stu-id="ab429-526">msdyn_contractlineproject</span></span>              | <span data-ttu-id="ab429-527">kyllä</span><span class="sxs-lookup"><span data-stu-id="ab429-527">yes</span></span>            | <span data-ttu-id="ab429-528">ei</span><span class="sxs-lookup"><span data-stu-id="ab429-528">no</span></span>           |
| <span data-ttu-id="ab429-529">msdyn_contractorganizationalunitid</span><span class="sxs-lookup"><span data-stu-id="ab429-529">msdyn_contractorganizationalunitid</span></span>     | <span data-ttu-id="ab429-530">kyllä</span><span class="sxs-lookup"><span data-stu-id="ab429-530">yes</span></span>            | <span data-ttu-id="ab429-531">ei</span><span class="sxs-lookup"><span data-stu-id="ab429-531">no</span></span>           |
| <span data-ttu-id="ab429-532">msdyn_contractorganizationalunitidname</span><span class="sxs-lookup"><span data-stu-id="ab429-532">msdyn_contractorganizationalunitidname</span></span> | <span data-ttu-id="ab429-533">kyllä</span><span class="sxs-lookup"><span data-stu-id="ab429-533">yes</span></span>            | <span data-ttu-id="ab429-534">ei</span><span class="sxs-lookup"><span data-stu-id="ab429-534">no</span></span>           |
| <span data-ttu-id="ab429-535">msdyn_costconsumption</span><span class="sxs-lookup"><span data-stu-id="ab429-535">msdyn_costconsumption</span></span>                  | <span data-ttu-id="ab429-536">ei</span><span class="sxs-lookup"><span data-stu-id="ab429-536">no</span></span>             | <span data-ttu-id="ab429-537">ei</span><span class="sxs-lookup"><span data-stu-id="ab429-537">no</span></span>           |
| <span data-ttu-id="ab429-538">msdyn_costestimateatcomplete</span><span class="sxs-lookup"><span data-stu-id="ab429-538">msdyn_costestimateatcomplete</span></span>           | <span data-ttu-id="ab429-539">ei</span><span class="sxs-lookup"><span data-stu-id="ab429-539">no</span></span>             | <span data-ttu-id="ab429-540">ei</span><span class="sxs-lookup"><span data-stu-id="ab429-540">no</span></span>           |
| <span data-ttu-id="ab429-541">msdyn_costestimateatcomplete_base</span><span class="sxs-lookup"><span data-stu-id="ab429-541">msdyn_costestimateatcomplete_base</span></span>      | <span data-ttu-id="ab429-542">ei</span><span class="sxs-lookup"><span data-stu-id="ab429-542">no</span></span>             | <span data-ttu-id="ab429-543">ei</span><span class="sxs-lookup"><span data-stu-id="ab429-543">no</span></span>           |
| <span data-ttu-id="ab429-544">msdyn_costvariance</span><span class="sxs-lookup"><span data-stu-id="ab429-544">msdyn_costvariance</span></span>                     | <span data-ttu-id="ab429-545">ei</span><span class="sxs-lookup"><span data-stu-id="ab429-545">no</span></span>             | <span data-ttu-id="ab429-546">ei</span><span class="sxs-lookup"><span data-stu-id="ab429-546">no</span></span>           |
| <span data-ttu-id="ab429-547">msdyn_costvariance_base</span><span class="sxs-lookup"><span data-stu-id="ab429-547">msdyn_costvariance_base</span></span>                | <span data-ttu-id="ab429-548">ei</span><span class="sxs-lookup"><span data-stu-id="ab429-548">no</span></span>             | <span data-ttu-id="ab429-549">ei</span><span class="sxs-lookup"><span data-stu-id="ab429-549">no</span></span>           |
| <span data-ttu-id="ab429-550">msdyn_duration</span><span class="sxs-lookup"><span data-stu-id="ab429-550">msdyn_duration</span></span>                         | <span data-ttu-id="ab429-551">ei</span><span class="sxs-lookup"><span data-stu-id="ab429-551">no</span></span>             | <span data-ttu-id="ab429-552">ei</span><span class="sxs-lookup"><span data-stu-id="ab429-552">no</span></span>           |
| <span data-ttu-id="ab429-553">msdyn_effort</span><span class="sxs-lookup"><span data-stu-id="ab429-553">msdyn_effort</span></span>                           | <span data-ttu-id="ab429-554">ei</span><span class="sxs-lookup"><span data-stu-id="ab429-554">no</span></span>             | <span data-ttu-id="ab429-555">ei</span><span class="sxs-lookup"><span data-stu-id="ab429-555">no</span></span>           |
| <span data-ttu-id="ab429-556">msdyn_effortcompleted</span><span class="sxs-lookup"><span data-stu-id="ab429-556">msdyn_effortcompleted</span></span>                  | <span data-ttu-id="ab429-557">ei</span><span class="sxs-lookup"><span data-stu-id="ab429-557">no</span></span>             | <span data-ttu-id="ab429-558">ei</span><span class="sxs-lookup"><span data-stu-id="ab429-558">no</span></span>           |
| <span data-ttu-id="ab429-559">msdyn_effortestimateatcompleteeac</span><span class="sxs-lookup"><span data-stu-id="ab429-559">msdyn_effortestimateatcompleteeac</span></span>      | <span data-ttu-id="ab429-560">ei</span><span class="sxs-lookup"><span data-stu-id="ab429-560">no</span></span>             | <span data-ttu-id="ab429-561">ei</span><span class="sxs-lookup"><span data-stu-id="ab429-561">no</span></span>           |
| <span data-ttu-id="ab429-562">msdyn_effortremaining</span><span class="sxs-lookup"><span data-stu-id="ab429-562">msdyn_effortremaining</span></span>                  | <span data-ttu-id="ab429-563">ei</span><span class="sxs-lookup"><span data-stu-id="ab429-563">no</span></span>             | <span data-ttu-id="ab429-564">ei</span><span class="sxs-lookup"><span data-stu-id="ab429-564">no</span></span>           |
| <span data-ttu-id="ab429-565">msdyn_finish</span><span class="sxs-lookup"><span data-stu-id="ab429-565">msdyn_finish</span></span>                           | <span data-ttu-id="ab429-566">kyllä</span><span class="sxs-lookup"><span data-stu-id="ab429-566">yes</span></span>            | <span data-ttu-id="ab429-567">kyllä</span><span class="sxs-lookup"><span data-stu-id="ab429-567">yes</span></span>          |
| <span data-ttu-id="ab429-568">msdyn_globalrevisiontoken</span><span class="sxs-lookup"><span data-stu-id="ab429-568">msdyn_globalrevisiontoken</span></span>              | <span data-ttu-id="ab429-569">ei</span><span class="sxs-lookup"><span data-stu-id="ab429-569">no</span></span>             | <span data-ttu-id="ab429-570">ei</span><span class="sxs-lookup"><span data-stu-id="ab429-570">no</span></span>           |
| <span data-ttu-id="ab429-571">msdyn_islinkedtomsprojectclient</span><span class="sxs-lookup"><span data-stu-id="ab429-571">msdyn_islinkedtomsprojectclient</span></span>        | <span data-ttu-id="ab429-572">ei</span><span class="sxs-lookup"><span data-stu-id="ab429-572">no</span></span>             | <span data-ttu-id="ab429-573">ei</span><span class="sxs-lookup"><span data-stu-id="ab429-573">no</span></span>           |
| <span data-ttu-id="ab429-574">msdyn_islinkedtomsprojectclientname</span><span class="sxs-lookup"><span data-stu-id="ab429-574">msdyn_islinkedtomsprojectclientname</span></span>    | <span data-ttu-id="ab429-575">ei</span><span class="sxs-lookup"><span data-stu-id="ab429-575">no</span></span>             | <span data-ttu-id="ab429-576">ei</span><span class="sxs-lookup"><span data-stu-id="ab429-576">no</span></span>           |
| <span data-ttu-id="ab429-577">msdyn_linkeddocumenturl</span><span class="sxs-lookup"><span data-stu-id="ab429-577">msdyn_linkeddocumenturl</span></span>                | <span data-ttu-id="ab429-578">ei</span><span class="sxs-lookup"><span data-stu-id="ab429-578">no</span></span>             | <span data-ttu-id="ab429-579">ei</span><span class="sxs-lookup"><span data-stu-id="ab429-579">no</span></span>           |
| <span data-ttu-id="ab429-580">msdyn_msprojectdocument</span><span class="sxs-lookup"><span data-stu-id="ab429-580">msdyn_msprojectdocument</span></span>                | <span data-ttu-id="ab429-581">ei</span><span class="sxs-lookup"><span data-stu-id="ab429-581">no</span></span>             | <span data-ttu-id="ab429-582">ei</span><span class="sxs-lookup"><span data-stu-id="ab429-582">no</span></span>           |
| <span data-ttu-id="ab429-583">msdyn_msprojectdocumentname</span><span class="sxs-lookup"><span data-stu-id="ab429-583">msdyn_msprojectdocumentname</span></span>            | <span data-ttu-id="ab429-584">ei</span><span class="sxs-lookup"><span data-stu-id="ab429-584">no</span></span>             | <span data-ttu-id="ab429-585">ei</span><span class="sxs-lookup"><span data-stu-id="ab429-585">no</span></span>           |
| <span data-ttu-id="ab429-586">msdyn_plannedexpensecost</span><span class="sxs-lookup"><span data-stu-id="ab429-586">msdyn_plannedexpensecost</span></span>               | <span data-ttu-id="ab429-587">ei</span><span class="sxs-lookup"><span data-stu-id="ab429-587">no</span></span>             | <span data-ttu-id="ab429-588">ei</span><span class="sxs-lookup"><span data-stu-id="ab429-588">no</span></span>           |
| <span data-ttu-id="ab429-589">msdyn_plannedexpensecost_base</span><span class="sxs-lookup"><span data-stu-id="ab429-589">msdyn_plannedexpensecost_base</span></span>          | <span data-ttu-id="ab429-590">ei</span><span class="sxs-lookup"><span data-stu-id="ab429-590">no</span></span>             | <span data-ttu-id="ab429-591">ei</span><span class="sxs-lookup"><span data-stu-id="ab429-591">no</span></span>           |
| <span data-ttu-id="ab429-592">msdyn_plannedlaborcost</span><span class="sxs-lookup"><span data-stu-id="ab429-592">msdyn_plannedlaborcost</span></span>                 | <span data-ttu-id="ab429-593">ei</span><span class="sxs-lookup"><span data-stu-id="ab429-593">no</span></span>             | <span data-ttu-id="ab429-594">ei</span><span class="sxs-lookup"><span data-stu-id="ab429-594">no</span></span>           |
| <span data-ttu-id="ab429-595">msdyn_plannedlaborcost_base</span><span class="sxs-lookup"><span data-stu-id="ab429-595">msdyn_plannedlaborcost_base</span></span>            | <span data-ttu-id="ab429-596">ei</span><span class="sxs-lookup"><span data-stu-id="ab429-596">no</span></span>             | <span data-ttu-id="ab429-597">ei</span><span class="sxs-lookup"><span data-stu-id="ab429-597">no</span></span>           |
| <span data-ttu-id="ab429-598">msdyn_plannedsales</span><span class="sxs-lookup"><span data-stu-id="ab429-598">msdyn_plannedsales</span></span>                     | <span data-ttu-id="ab429-599">ei</span><span class="sxs-lookup"><span data-stu-id="ab429-599">no</span></span>             | <span data-ttu-id="ab429-600">ei</span><span class="sxs-lookup"><span data-stu-id="ab429-600">no</span></span>           |
| <span data-ttu-id="ab429-601">msdyn_plannedsales_base</span><span class="sxs-lookup"><span data-stu-id="ab429-601">msdyn_plannedsales_base</span></span>                | <span data-ttu-id="ab429-602">ei</span><span class="sxs-lookup"><span data-stu-id="ab429-602">no</span></span>             | <span data-ttu-id="ab429-603">ei</span><span class="sxs-lookup"><span data-stu-id="ab429-603">no</span></span>           |
| <span data-ttu-id="ab429-604">msdyn_progress</span><span class="sxs-lookup"><span data-stu-id="ab429-604">msdyn_progress</span></span>                         | <span data-ttu-id="ab429-605">ei</span><span class="sxs-lookup"><span data-stu-id="ab429-605">no</span></span>             | <span data-ttu-id="ab429-606">ei</span><span class="sxs-lookup"><span data-stu-id="ab429-606">no</span></span>           |
| <span data-ttu-id="ab429-607">msdyn_remainingcost</span><span class="sxs-lookup"><span data-stu-id="ab429-607">msdyn_remainingcost</span></span>                    | <span data-ttu-id="ab429-608">ei</span><span class="sxs-lookup"><span data-stu-id="ab429-608">no</span></span>             | <span data-ttu-id="ab429-609">ei</span><span class="sxs-lookup"><span data-stu-id="ab429-609">no</span></span>           |
| <span data-ttu-id="ab429-610">msdyn_remainingcost_base</span><span class="sxs-lookup"><span data-stu-id="ab429-610">msdyn_remainingcost_base</span></span>               | <span data-ttu-id="ab429-611">ei</span><span class="sxs-lookup"><span data-stu-id="ab429-611">no</span></span>             | <span data-ttu-id="ab429-612">ei</span><span class="sxs-lookup"><span data-stu-id="ab429-612">no</span></span>           |
| <span data-ttu-id="ab429-613">msdyn_remainingsales</span><span class="sxs-lookup"><span data-stu-id="ab429-613">msdyn_remainingsales</span></span>                   | <span data-ttu-id="ab429-614">ei</span><span class="sxs-lookup"><span data-stu-id="ab429-614">no</span></span>             | <span data-ttu-id="ab429-615">ei</span><span class="sxs-lookup"><span data-stu-id="ab429-615">no</span></span>           |
| <span data-ttu-id="ab429-616">msdyn_remainingsales_base</span><span class="sxs-lookup"><span data-stu-id="ab429-616">msdyn_remainingsales_base</span></span>              | <span data-ttu-id="ab429-617">ei</span><span class="sxs-lookup"><span data-stu-id="ab429-617">no</span></span>             | <span data-ttu-id="ab429-618">ei</span><span class="sxs-lookup"><span data-stu-id="ab429-618">no</span></span>           |
| <span data-ttu-id="ab429-619">msdyn_replaylogheader</span><span class="sxs-lookup"><span data-stu-id="ab429-619">msdyn_replaylogheader</span></span>                  | <span data-ttu-id="ab429-620">ei</span><span class="sxs-lookup"><span data-stu-id="ab429-620">no</span></span>             | <span data-ttu-id="ab429-621">ei</span><span class="sxs-lookup"><span data-stu-id="ab429-621">no</span></span>           |
| <span data-ttu-id="ab429-622">msdyn_salesconsumption</span><span class="sxs-lookup"><span data-stu-id="ab429-622">msdyn_salesconsumption</span></span>                 | <span data-ttu-id="ab429-623">ei</span><span class="sxs-lookup"><span data-stu-id="ab429-623">no</span></span>             | <span data-ttu-id="ab429-624">ei</span><span class="sxs-lookup"><span data-stu-id="ab429-624">no</span></span>           |
| <span data-ttu-id="ab429-625">msdyn_salesestimateatcompleteeac</span><span class="sxs-lookup"><span data-stu-id="ab429-625">msdyn_salesestimateatcompleteeac</span></span>       | <span data-ttu-id="ab429-626">ei</span><span class="sxs-lookup"><span data-stu-id="ab429-626">no</span></span>             | <span data-ttu-id="ab429-627">ei</span><span class="sxs-lookup"><span data-stu-id="ab429-627">no</span></span>           |
| <span data-ttu-id="ab429-628">msdyn_salesestimateatcompleteeac_base</span><span class="sxs-lookup"><span data-stu-id="ab429-628">msdyn_salesestimateatcompleteeac_base</span></span>  | <span data-ttu-id="ab429-629">ei</span><span class="sxs-lookup"><span data-stu-id="ab429-629">no</span></span>             | <span data-ttu-id="ab429-630">ei</span><span class="sxs-lookup"><span data-stu-id="ab429-630">no</span></span>           |
| <span data-ttu-id="ab429-631">msdyn_salesvariance</span><span class="sxs-lookup"><span data-stu-id="ab429-631">msdyn_salesvariance</span></span>                    | <span data-ttu-id="ab429-632">ei</span><span class="sxs-lookup"><span data-stu-id="ab429-632">no</span></span>             | <span data-ttu-id="ab429-633">ei</span><span class="sxs-lookup"><span data-stu-id="ab429-633">no</span></span>           |
| <span data-ttu-id="ab429-634">msdyn_salesvariance_base</span><span class="sxs-lookup"><span data-stu-id="ab429-634">msdyn_salesvariance_base</span></span>               | <span data-ttu-id="ab429-635">ei</span><span class="sxs-lookup"><span data-stu-id="ab429-635">no</span></span>             | <span data-ttu-id="ab429-636">ei</span><span class="sxs-lookup"><span data-stu-id="ab429-636">no</span></span>           |
| <span data-ttu-id="ab429-637">msdyn_scheduleperformance</span><span class="sxs-lookup"><span data-stu-id="ab429-637">msdyn_scheduleperformance</span></span>              | <span data-ttu-id="ab429-638">ei</span><span class="sxs-lookup"><span data-stu-id="ab429-638">no</span></span>             | <span data-ttu-id="ab429-639">ei</span><span class="sxs-lookup"><span data-stu-id="ab429-639">no</span></span>           |
| <span data-ttu-id="ab429-640">msdyn_scheduleperformancename</span><span class="sxs-lookup"><span data-stu-id="ab429-640">msdyn_scheduleperformancename</span></span>          | <span data-ttu-id="ab429-641">ei</span><span class="sxs-lookup"><span data-stu-id="ab429-641">no</span></span>             | <span data-ttu-id="ab429-642">ei</span><span class="sxs-lookup"><span data-stu-id="ab429-642">no</span></span>           |
| <span data-ttu-id="ab429-643">msdyn_schedulevariance</span><span class="sxs-lookup"><span data-stu-id="ab429-643">msdyn_schedulevariance</span></span>                 | <span data-ttu-id="ab429-644">ei</span><span class="sxs-lookup"><span data-stu-id="ab429-644">no</span></span>             | <span data-ttu-id="ab429-645">ei</span><span class="sxs-lookup"><span data-stu-id="ab429-645">no</span></span>           |
| <span data-ttu-id="ab429-646">msdyn_taskearlieststart</span><span class="sxs-lookup"><span data-stu-id="ab429-646">msdyn_taskearlieststart</span></span>                | <span data-ttu-id="ab429-647">ei</span><span class="sxs-lookup"><span data-stu-id="ab429-647">no</span></span>             | <span data-ttu-id="ab429-648">ei</span><span class="sxs-lookup"><span data-stu-id="ab429-648">no</span></span>           |
| <span data-ttu-id="ab429-649">msdyn_teamsize</span><span class="sxs-lookup"><span data-stu-id="ab429-649">msdyn_teamsize</span></span>                         | <span data-ttu-id="ab429-650">ei</span><span class="sxs-lookup"><span data-stu-id="ab429-650">no</span></span>             | <span data-ttu-id="ab429-651">ei</span><span class="sxs-lookup"><span data-stu-id="ab429-651">no</span></span>           |
| <span data-ttu-id="ab429-652">msdyn_teamsize_date</span><span class="sxs-lookup"><span data-stu-id="ab429-652">msdyn_teamsize_date</span></span>                    | <span data-ttu-id="ab429-653">ei</span><span class="sxs-lookup"><span data-stu-id="ab429-653">no</span></span>             | <span data-ttu-id="ab429-654">ei</span><span class="sxs-lookup"><span data-stu-id="ab429-654">no</span></span>           |
| <span data-ttu-id="ab429-655">msdyn_teamsize_state</span><span class="sxs-lookup"><span data-stu-id="ab429-655">msdyn_teamsize_state</span></span>                   | <span data-ttu-id="ab429-656">ei</span><span class="sxs-lookup"><span data-stu-id="ab429-656">no</span></span>             | <span data-ttu-id="ab429-657">ei</span><span class="sxs-lookup"><span data-stu-id="ab429-657">no</span></span>           |
| <span data-ttu-id="ab429-658">msdyn_totalactualcost</span><span class="sxs-lookup"><span data-stu-id="ab429-658">msdyn_totalactualcost</span></span>                  | <span data-ttu-id="ab429-659">ei</span><span class="sxs-lookup"><span data-stu-id="ab429-659">no</span></span>             | <span data-ttu-id="ab429-660">ei</span><span class="sxs-lookup"><span data-stu-id="ab429-660">no</span></span>           |
| <span data-ttu-id="ab429-661">msdyn_totalactualcost_base</span><span class="sxs-lookup"><span data-stu-id="ab429-661">msdyn_totalactualcost_base</span></span>             | <span data-ttu-id="ab429-662">ei</span><span class="sxs-lookup"><span data-stu-id="ab429-662">no</span></span>             | <span data-ttu-id="ab429-663">ei</span><span class="sxs-lookup"><span data-stu-id="ab429-663">no</span></span>           |
| <span data-ttu-id="ab429-664">msdyn_totalplannedcost</span><span class="sxs-lookup"><span data-stu-id="ab429-664">msdyn_totalplannedcost</span></span>                 | <span data-ttu-id="ab429-665">ei</span><span class="sxs-lookup"><span data-stu-id="ab429-665">no</span></span>             | <span data-ttu-id="ab429-666">ei</span><span class="sxs-lookup"><span data-stu-id="ab429-666">no</span></span>           |
| <span data-ttu-id="ab429-667">msdyn_totalplannedcost_base</span><span class="sxs-lookup"><span data-stu-id="ab429-667">msdyn_totalplannedcost_base</span></span>            | <span data-ttu-id="ab429-668">ei</span><span class="sxs-lookup"><span data-stu-id="ab429-668">no</span></span>             | <span data-ttu-id="ab429-669">ei</span><span class="sxs-lookup"><span data-stu-id="ab429-669">no</span></span>           |


## <a name="limitations-and-known-issues"></a><span data-ttu-id="ab429-670">Rajoitukset ja tunnetut ongelmat</span><span class="sxs-lookup"><span data-stu-id="ab429-670">Limitations and known issues</span></span>
<span data-ttu-id="ab429-671">Seuraavassa on luettelo rajoituksista ja tunnetuista ongelmista:</span><span class="sxs-lookup"><span data-stu-id="ab429-671">The following is a list of limitations and known issues:</span></span>

- <span data-ttu-id="ab429-672">Projektiaikataulun ohjelmointirajapintoja voivat käyttää vain **käyttäjät, joilla on Microsoft Project -lisenssi**.</span><span class="sxs-lookup"><span data-stu-id="ab429-672">Project Schedule APIs can only be used by **Users with Microsoft Project License.**</span></span> <span data-ttu-id="ab429-673">Niitä eivät voi käyttää:</span><span class="sxs-lookup"><span data-stu-id="ab429-673">They can't be used by:</span></span>
    - <span data-ttu-id="ab429-674">Sovelluksen käyttäjät</span><span class="sxs-lookup"><span data-stu-id="ab429-674">Application users</span></span>
    - <span data-ttu-id="ab429-675">Järjestelmäkäyttäjät</span><span class="sxs-lookup"><span data-stu-id="ab429-675">System users</span></span>
    - <span data-ttu-id="ab429-676">Integrointikäyttäjät</span><span class="sxs-lookup"><span data-stu-id="ab429-676">Integration users</span></span>
    - <span data-ttu-id="ab429-677">Muut käyttäjät, joilla ei ole tarvittavaa lisenssiä</span><span class="sxs-lookup"><span data-stu-id="ab429-677">Other users that don't have the required license</span></span>
- <span data-ttu-id="ab429-678">Kussakin **OperationSet** issä voi olla enintään 100 toimintoa.</span><span class="sxs-lookup"><span data-stu-id="ab429-678">Each **OperationSet** can only have a maximum of 100 operations.</span></span>
- <span data-ttu-id="ab429-679">Kullakin käyttäjällä voi olla enintään 10 avointa **OperationSet** iä.</span><span class="sxs-lookup"><span data-stu-id="ab429-679">Each user can only have a maximum of 10 open **OperationSets**.</span></span>
- <span data-ttu-id="ab429-680">Project Operations tukee tällä hetkellä projektissa enintään 500 tehtävää.</span><span class="sxs-lookup"><span data-stu-id="ab429-680">Project Operations currently supports a maximum of 500 total tasks on a project.</span></span>
- <span data-ttu-id="ab429-681">**OperationSet**-virheen tila- ja virhelokit eivät ole tällä hetkellä käytettävissä.</span><span class="sxs-lookup"><span data-stu-id="ab429-681">**OperationSet** failure status and failure logs aren't currently available.</span></span>
- [<span data-ttu-id="ab429-682">Projektien ja tehtävien rajoitukset ja rajat</span><span class="sxs-lookup"><span data-stu-id="ab429-682">Limits and boundaries on projects and tasks</span></span>](/project-for-the-web/project-for-the-web-limits-and-boundaries)

## <a name="error-handling"></a><span data-ttu-id="ab429-683">Virheen käsittely</span><span class="sxs-lookup"><span data-stu-id="ab429-683">Error handling</span></span>

   - <span data-ttu-id="ab429-684">Voit tarkastella toimintojoukoista luotuja virheitä kohdassa **Asetukset** \> **Aikatauluta integrointi** \> **Toimintojoukot**.</span><span class="sxs-lookup"><span data-stu-id="ab429-684">To review errors generated from the Operation Sets, go to **Settings** \> **Schedule Integration** \> **Operations Sets**.</span></span>
   - <span data-ttu-id="ab429-685">Voit tarkastella Projektin aikataulupalvelussa luotuja virheitä valitsemalla **Asetukset** \> **Aikataulun integrointi** \> **PSS-virhelokit**.</span><span class="sxs-lookup"><span data-stu-id="ab429-685">To review errors generated from the Project schedule Service, go to **Settings** \> **Schedule Integration** \> **PSS Error Logs**.</span></span>

## <a name="sample-scenario"></a><span data-ttu-id="ab429-686">Näyteskenaario</span><span class="sxs-lookup"><span data-stu-id="ab429-686">Sample scenario</span></span>

<span data-ttu-id="ab429-687">Tässä skenaariossa luodaan projekti, ryhmän jäsen, neljä tehtävää ja kaksi resurssivarausta.</span><span class="sxs-lookup"><span data-stu-id="ab429-687">In this scenario, you will create a project, a team member, four tasks, and two resource assignments.</span></span> <span data-ttu-id="ab429-688">Seuraavaksi päivität yhden tehtävän, päivität projektin, poistat yhden tehtävän, poistat yhden resurssin määrityksen ja luot riippuvuuden.</span><span class="sxs-lookup"><span data-stu-id="ab429-688">Next, you will update one task, update the project, delete one task, delete one resource assignment, and create a task dependency.</span></span>

```csharp
Entity project = CreateProject();
project.Id = CallCreateProjectAction(project);
var projectReference = project.ToEntityReference();

var teamMember = new Entity("msdyn_projectteam", Guid.NewGuid());
teamMember["msdyn_name"] = $"TM {DateTime.Now.ToShortTimeString()}";
teamMember["msdyn_project"] = projectReference;
var createTeamMemberResponse = CallCreateTeamMemberAction(teamMember);

var description = $"My demo {DateTime.Now.ToShortTimeString()}";
var operationSetId = CallCreateOperationSetAction(project.Id, description);

var task1 = GetTask("1WW", projectReference);
var task2 = GetTask("2XX", projectReference, task1.ToEntityReference());
var task3 = GetTask("3YY", projectReference);
var task4 = GetTask("4ZZ", projectReference);

var assignment1 = GetResourceAssignment("R1", teamMember, task2, project);
var assignment2 = GetResourceAssignment("R2", teamMember, task3, project);

var task1Response = CallPssCreateAction(task1, operationSetId);
var task2Response = CallPssCreateAction(task2, operationSetId);
var task3Response = CallPssCreateAction(task3, operationSetId);
var task4Response = CallPssCreateAction(task4, operationSetId);

var assignment1Response = CallPssCreateAction(assignment1, operationSetId);
var assignment2Response = CallPssCreateAction(assignment2, operationSetId);

task2["msdyn_subject"] = "Updated Task";
var task2UpdateResponse = CallPssUpdateAction(task2, operationSetId);

project["msdyn_subject"] = $"Proj update {DateTime.Now.ToShortTimeString()}";
var projectUpdateResponse = CallPssUpdateAction(project, operationSetId);

var task4DeleteResponse = CallPssDeleteAction(task4.Id.ToString(), task4.LogicalName, operationSetId);

var assignment2DeleteResponse = CallPssDeleteAction(assignment2.Id.ToString(), assignment2.LogicalName, operationSetId);

var dependency1 = GetTaskDependency(project, task2, task3);
var dependency1Response = CallPssCreateAction(dependency1, operationSetId);

CallExecuteOperationSetAction(operationSetId);
Console.WriteLine("Done....");
```

## <a name="additional-samples"></a><span data-ttu-id="ab429-689">Muita näytteitä</span><span class="sxs-lookup"><span data-stu-id="ab429-689">Additional samples</span></span>

```csharp
#region Call actions --- Sample code ----

/// <summary>
/// Calls the action to create an operationSet
/// </summary>
/// <param name="projectId">project id for the operations to be included in this operationSet</param>
/// <param name="description">description of this operationSet</param>
/// <returns>operationSet id</returns>
private string CallCreateOperationSetAction(Guid projectId, string description)
{
    OrganizationRequest operationSetRequest = new OrganizationRequest("msdyn_CreateOperationSetV1");
    operationSetRequest["ProjectId"] = projectId.ToString();
    operationSetRequest["Description"] = description;
    OrganizationResponse response = organizationService.Execute(operationSetRequest);
    return response["OperationSetId"].ToString();
}

/// <summary>
/// Calls the action to create an entity, only Task and Resource Assignment for now
/// </summary>
/// <param name="entity">Task or Resource Assignment</param>
/// <param name="operationSetId">operationSet id</param>
/// <returns>OperationSetResponse</returns>

private OperationSetResponse CallPssCreateAction(Entity entity, string operationSetId)
{
    OrganizationRequest operationSetRequest = new OrganizationRequest("msdyn_PssCreateV1");
    operationSetRequest["Entity"] = entity;
    operationSetRequest["OperationSetId"] = operationSetId;
    return GetOperationSetResponseFromOrgResponse(organizationService.Execute(operationSetRequest));
}

/// <summary>
/// Calls the action to update an entity, only Task for now
/// </summary>
/// <param name="entity">Task or Resource Assignment</param>
/// <param name="operationSetId">operationSet Id</param>
/// <returns>OperationSetResponse</returns>
private OperationSetResponse CallPssUpdateAction(Entity entity, string operationSetId)
{
    OrganizationRequest operationSetRequest = new OrganizationRequest("msdyn_PssUpdateV1");
    operationSetRequest["Entity"] = entity;
    operationSetRequest["OperationSetId"] = operationSetId;
    return GetOperationSetResponseFromOrgResponse(organizationService.Execute(operationSetRequest));
}

/// <summary>
/// Calls the action to update an entity, only Task and Resource Assignment for now
/// </summary>
/// <param name="recordId">Id of the record to be deleted</param>
/// <param name="entityLogicalName">Entity logical name of the record</param>
/// <param name="operationSetId">OperationSet Id</param>
/// <returns>OperationSetResponse</returns>
private OperationSetResponse CallPssDeleteAction(string recordId, string entityLogicalName, string operationSetId)
{
    OrganizationRequest operationSetRequest = new OrganizationRequest("msdyn_PssDeleteV1");
    operationSetRequest["RecordId"] = recordId;
    operationSetRequest["EntityLogicalName"] = entityLogicalName;
    operationSetRequest["OperationSetId"] = operationSetId;
    return GetOperationSetResponseFromOrgResponse(organizationService.Execute(operationSetRequest));
}

/// <summary>
/// Calls the action to execute requests in an operationSet
/// </summary>
/// <param name="operationSetId">operationSet id</param>
/// <returns>OperationSetResponse</returns>
private OperationSetResponse CallExecuteOperationSetAction(string operationSetId)
{
    OrganizationRequest operationSetRequest = new OrganizationRequest("msdyn_ExecuteOperationSetV1");
    operationSetRequest["OperationSetId"] = operationSetId;
    return GetOperationSetResponseFromOrgResponse(organizationService.Execute(operationSetRequest));
}

/// <summary>
/// This can be used to abandon an operationSet that is no longer needed
/// </summary>
/// <param name="operationSetId">operationSet id</param>
/// <returns>OperationSetResponse</returns>
protected OperationSetResponse CallAbandonOperationSetAction(Guid operationSetId)
{
    OrganizationRequest operationSetRequest = new OrganizationRequest("msdyn_AbandonOperationSetV1");
    operationSetRequest["OperationSetId"] = operationSetId.ToString();
    return GetOperationSetResponseFromOrgResponse(organizationService.Execute(operationSetRequest));
}


/// <summary>
/// Calls the action to create a new project
/// </summary>
/// <param name="project">Project</param>
/// <returns>project Id</returns>
private Guid CallCreateProjectAction(Entity project)
{
    OrganizationRequest createProjectRequest = new OrganizationRequest("msdyn_CreateProjectV1");
    createProjectRequest["Project"] = project;
    OrganizationResponse response = organizationService.Execute(createProjectRequest);
    var projectId = Guid.Parse((string)response["ProjectId"]);
    return projectId;
}

/// <summary>
/// Calls the action to create a new project team member
/// </summary>
/// <param name="teamMember">Project team member</param>
/// <returns>project team member Id</returns>
private string CallCreateTeamMemberAction(Entity teamMember)
{
    OrganizationRequest request = new OrganizationRequest("msdyn_CreateTeamMemberV1");
    request["TeamMember"] = teamMember;
    OrganizationResponse response = organizationService.Execute(request);
    return (string)response["TeamMemberId"];
}

private OperationSetResponse GetOperationSetResponseFromOrgResponse(OrganizationResponse orgResponse)
{
    return JsonConvert.DeserializeObject<OperationSetResponse>((string)orgResponse.Results["OperationSetResponse"]);
}

private EntityCollection GetDefaultBucket(EntityReference projectReference)
{
    var columnsToFetch = new ColumnSet("msdyn_project", "msdyn_name");
    var getDefaultBucket = new QueryExpression("msdyn_projectbucket")
    {
        ColumnSet = columnsToFetch,
        Criteria =
        {
            Conditions =
            {
                new ConditionExpression("msdyn_project", ConditionOperator.Equal, projectReference.Id),
                new ConditionExpression("msdyn_name", ConditionOperator.Equal, "Bucket 1")
            }
        }
    };

    return organizationService.RetrieveMultiple(getDefaultBucket);
}

private Entity GetBucket(EntityReference projectReference)
{
    var bucketCollection = GetDefaultBucket(projectReference);
    if (bucketCollection.Entities.Count > 0)
    {
        return bucketCollection[0].ToEntity<Entity>();
    }

    throw new Exception($"Please open project with id {projectReference.Id} in the Dynamics UI and navigate to the Tasks tab");
}

private Entity CreateProject()
{
    var project = new Entity("msdyn_project", Guid.NewGuid());
    project["msdyn_subject"] = $"Proj {DateTime.Now.ToShortTimeString()}";

    return project;
}



private Entity GetTask(string name, EntityReference projectReference, EntityReference parentReference = null)
{
    var task = new Entity("msdyn_projecttask", Guid.NewGuid());
    task["msdyn_project"] = projectReference;
    task["msdyn_subject"] = name;
    task["msdyn_effort"] = 4d;
    task["msdyn_scheduledstart"] = DateTime.Today;
    task["msdyn_scheduledend"] = DateTime.Today.AddDays(5);
    task["msdyn_progress"] = 0.34m;
    task["msdyn_start"] = DateTime.Now.AddDays(1);
    task["msdyn_projectbucket"] = GetBucket(projectReference).ToEntityReference();
    task["msdyn_LinkStatus"] = new OptionSetValue(192350000);

    //Custom field handling
    /*
    task["new_custom1"] = "Just my test";
    task["new_age"] = 98;
    task["new_amount"] = 591.34m;
    task["new_isready"] = new OptionSetValue(100000000);
    */

    if (parentReference == null)
    {
        task["msdyn_outlinelevel"] = 1;
    }
    else
    {
        task["msdyn_parenttask"] = parentReference;
    }

    return task;
}

private Entity GetResourceAssignment(string name, Entity teamMember, Entity task, Entity project)
{
    var assignment = new Entity("msdyn_resourceassignment", Guid.NewGuid());
    assignment["msdyn_projectteamid"] = teamMember.ToEntityReference();
    assignment["msdyn_taskid"] = task.ToEntityReference();
    assignment["msdyn_projectid"] = project.ToEntityReference();
    assignment["msdyn_name"] = name;
    assignment["msdyn_start"] = DateTime.Now;
    assignment["msdyn_finish"] = DateTime.Now;

    return assignment;
}

protected Entity GetTaskDependency(Entity project, Entity predecessor, Entity successor)
{
    var taskDependency = new Entity("msdyn_projecttaskdependency", Guid.NewGuid());
    taskDependency["msdyn_project"] = project.ToEntityReference();
    taskDependency["msdyn_predecessortask"] = predecessor.ToEntityReference();
    taskDependency["msdyn_successortask"] = successor.ToEntityReference();
    taskDependency["msdyn_linktype"] = new OptionSetValue(192350000);

    return taskDependency;
}

#endregion


#region OperationSetResponse DataContract --- Sample code ----

[DataContract]
public class OperationSetResponse
{
[DataMember(Name = "operationSetId")]
public Guid OperationSetId { get; set; }

[DataMember(Name = "operationSetDetailId")]
public Guid OperationSetDetailId { get; set; }

[DataMember(Name = "operationType")]
public string OperationType { get; set; }

[DataMember(Name = "recordId")]
public string RecordId { get; set; }

[DataMember(Name = "correlationId")]
public string CorrelationId { get; set; }
}

#endregion
```
