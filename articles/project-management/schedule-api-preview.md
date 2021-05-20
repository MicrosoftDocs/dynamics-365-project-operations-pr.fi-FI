---
title: Aikataulutuksen ohjelmointirajapintojen avulla voit suorittaa toimintoja aikataulutusentiteettien kanssa
description: Tässä aiheessa on tietoja ja esimerkkejä aikataulun ohjelmointirajapintojen käyttämisestä.
author: sigitac
manager: Annbe
ms.date: 04/27/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: e03f4e6c49a835206b23cade3fabe3fd26693441
ms.sourcegitcommit: 3d78338773929121d17ec3386f6cb67bfb2272cc
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/27/2021
ms.locfileid: "5950800"
---
# <a name="use-schedule-apis-to-perform-operations-with-scheduling-entities"></a><span data-ttu-id="a28f5-103">Aikataulutuksen ohjelmointirajapintojen avulla voit suorittaa toimintoja aikataulutusentiteettien kanssa</span><span class="sxs-lookup"><span data-stu-id="a28f5-103">Use Schedule APIs to perform operations with Scheduling entities</span></span>

<span data-ttu-id="a28f5-104">_**Koskee:** Project Operationsin resurssiin / muuhun kuin resurssiin perustuvia skenaarioita, Lite-käyttöönotto-kaupasta proformalaskutukseen_</span><span class="sxs-lookup"><span data-stu-id="a28f5-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

> [!IMPORTANT] 
> <span data-ttu-id="a28f5-105">Kaikki tai osa tässä aiheessa käsitellyistä toiminnoista ovat saatavilla esiversiojulkaisun osana.</span><span class="sxs-lookup"><span data-stu-id="a28f5-105">Some or all of the functionality noted in this topic is available as part of a preview release.</span></span> <span data-ttu-id="a28f5-106">Sisältö ja toiminnot voivat muuttua.</span><span class="sxs-lookup"><span data-stu-id="a28f5-106">The content and the functionality are subject to change.</span></span> 

## <a name="scheduling-entities"></a><span data-ttu-id="a28f5-107">Aikataulutusentiteetit</span><span class="sxs-lookup"><span data-stu-id="a28f5-107">Scheduling entities</span></span>

<span data-ttu-id="a28f5-108">Aikatalujen ohjelmointirajapinnat antavat mahdollisuuden luoda, päivittää ja poistaa toimintoja **Eikataulutusentiteettien** avulla.</span><span class="sxs-lookup"><span data-stu-id="a28f5-108">Schedule APIs provide the ability to perform create, update, and delete operations with **Scheduling entities**.</span></span> <span data-ttu-id="a28f5-109">Näitä entiteettejä hallitaan verkkopohjaisessa Projectissa aikataulutusytimen kautta.</span><span class="sxs-lookup"><span data-stu-id="a28f5-109">These entities are managed through the Scheduling engine in Project for the web.</span></span> <span data-ttu-id="a28f5-110">Luonti-, päivitys- ja poisto-operaatioita **Aikataulutusentiteettien avulla** rajoitettiin aiemmissa Dynamics 365 Project Operations -julkaisuissa.</span><span class="sxs-lookup"><span data-stu-id="a28f5-110">Create, update, and delete operations with **Scheduling entities** were restricted in earlier Dynamics 365 Project Operations releases.</span></span>

<span data-ttu-id="a28f5-111">Seuraavassa taulukossa on täydellinen luettelo **Aikataulutusentiteeteistä**.</span><span class="sxs-lookup"><span data-stu-id="a28f5-111">The following table provides a full list of the **Scheduling entities**.</span></span>

| <span data-ttu-id="a28f5-112">Entiteetin nimi</span><span class="sxs-lookup"><span data-stu-id="a28f5-112">Entity name</span></span>  | <span data-ttu-id="a28f5-113">Entiteetin looginen nimi</span><span class="sxs-lookup"><span data-stu-id="a28f5-113">Entity logical name</span></span> |
| --- | --- |
| <span data-ttu-id="a28f5-114">Project</span><span class="sxs-lookup"><span data-stu-id="a28f5-114">Project</span></span> | <span data-ttu-id="a28f5-115">msdyn_project</span><span class="sxs-lookup"><span data-stu-id="a28f5-115">msdyn_project</span></span> |
| <span data-ttu-id="a28f5-116">Projektin tehtävä</span><span class="sxs-lookup"><span data-stu-id="a28f5-116">Project Task</span></span>  | <span data-ttu-id="a28f5-117">msdyn_projecttask</span><span class="sxs-lookup"><span data-stu-id="a28f5-117">msdyn_projecttask</span></span>  |
| <span data-ttu-id="a28f5-118">Projektitehtävän riippuvuus</span><span class="sxs-lookup"><span data-stu-id="a28f5-118">Project Task Dependency</span></span>  | <span data-ttu-id="a28f5-119">msdyn_projecttaskdependency</span><span class="sxs-lookup"><span data-stu-id="a28f5-119">msdyn_projecttaskdependency</span></span>  |
| <span data-ttu-id="a28f5-120">Resurssien delegointi</span><span class="sxs-lookup"><span data-stu-id="a28f5-120">Resource Assignment</span></span> | <span data-ttu-id="a28f5-121">msdyn_resourceassignment</span><span class="sxs-lookup"><span data-stu-id="a28f5-121">msdyn_resourceassignment</span></span> |
| <span data-ttu-id="a28f5-122">Projektin joukko</span><span class="sxs-lookup"><span data-stu-id="a28f5-122">Project Bucket</span></span>  | <span data-ttu-id="a28f5-123">msdyn_projectbucket</span><span class="sxs-lookup"><span data-stu-id="a28f5-123">msdyn_projectbucket</span></span> |
| <span data-ttu-id="a28f5-124">Projektiryhmän jäsen</span><span class="sxs-lookup"><span data-stu-id="a28f5-124">Project Team Member</span></span> | <span data-ttu-id="a28f5-125">msdyn_projectteam</span><span class="sxs-lookup"><span data-stu-id="a28f5-125">msdyn_projectteam</span></span> |

## <a name="operationset"></a><span data-ttu-id="a28f5-126">OperationSet</span><span class="sxs-lookup"><span data-stu-id="a28f5-126">OperationSet</span></span>

<span data-ttu-id="a28f5-127">OperationSet on työyksikkörakenne, jota voidaan käyttää, kun useita aikatauluihin vaikuttavia pyyntöjä on käsiteltävä tapahtumassa.</span><span class="sxs-lookup"><span data-stu-id="a28f5-127">OperationSet is a unit-of-work pattern that can be used when several schedule impacting requests must be processed within a transaction.</span></span>

## <a name="schedule-apis"></a><span data-ttu-id="a28f5-128">Aikataulutuksen ohjelmointirajapinnat</span><span class="sxs-lookup"><span data-stu-id="a28f5-128">Schedule APIs</span></span>

<span data-ttu-id="a28f5-129">Seuraavassa on luettelo nykyisistä aikataulun ohjelmointirajapinnoista.</span><span class="sxs-lookup"><span data-stu-id="a28f5-129">The following is a list of current Schedule APIs.</span></span>

- <span data-ttu-id="a28f5-130">**msdyn_CreateProjectV1**: Tämän ohjelmointirajapinnan avulla voidaan luoda projekti.</span><span class="sxs-lookup"><span data-stu-id="a28f5-130">**msdyn_CreateProjectV1**: This API can be used to create a project.</span></span> <span data-ttu-id="a28f5-131">Projekti ja projektin oletussäilö luodaan heti.</span><span class="sxs-lookup"><span data-stu-id="a28f5-131">The project and default project bucket is created immediately.</span></span>
- <span data-ttu-id="a28f5-132">**msdyn_CreateTeamMemberV1**: Tämän ohjelmointirajapinnan avulla voidaan luoda projektiryhmän jäsen.</span><span class="sxs-lookup"><span data-stu-id="a28f5-132">**msdyn_CreateTeamMemberV1**: This API can be used to create a project team member.</span></span> <span data-ttu-id="a28f5-133">Ryhmän jäsentietue luodaan heti.</span><span class="sxs-lookup"><span data-stu-id="a28f5-133">The team member record is created immediately.</span></span>
- <span data-ttu-id="a28f5-134">**msdyn_CreateOperationSetV1**: Tämän ohjelmointirajapinnan avulla voidaan aikatauluttaa useita pyyntöjä, jotka on suoritettava tapahtumassa.</span><span class="sxs-lookup"><span data-stu-id="a28f5-134">**msdyn_CreateOperationSetV1**: This API can be used to schedule several requests that must be performed within a transaction.</span></span>
- <span data-ttu-id="a28f5-135">**msdyn_PSSCreateV1**: Tämän ohjelmointirajapinnan avulla voidaan luoda entiteetti.</span><span class="sxs-lookup"><span data-stu-id="a28f5-135">**msdyn_PSSCreateV1**: This API can be used to create an entity.</span></span> <span data-ttu-id="a28f5-136">Entiteetti voi olla mikä tahansa luontitoimintoa tukeva aikataulutusentiteetti.</span><span class="sxs-lookup"><span data-stu-id="a28f5-136">The entity can be any of the Scheduling entities that support the create operation.</span></span>
- <span data-ttu-id="a28f5-137">**msdyn_PSSUpdateV1**: Tämän ohjelmointirajapinnan avulla voidaan päivittää entiteetti.</span><span class="sxs-lookup"><span data-stu-id="a28f5-137">**msdyn_PSSUpdateV1**: This API can be used to update an entity.</span></span> <span data-ttu-id="a28f5-138">Entiteetti voi olla mikä tahansa päivitystoimintoa tukeva aikataulutusentiteetti.</span><span class="sxs-lookup"><span data-stu-id="a28f5-138">The entity can be any of the Scheduling entities that support the update operation.</span></span>
- <span data-ttu-id="a28f5-139">**msdyn_PSSDeleteV1**: Tämän ohjelmointirajapinnan avulla voidaan poistaa entiteetti.</span><span class="sxs-lookup"><span data-stu-id="a28f5-139">**msdyn_PSSDeleteV1**: This API can be used to delete an entity.</span></span> <span data-ttu-id="a28f5-140">Entiteetti voi olla mikä tahansa poistotoimintoa tukeva aikataulutusentiteetti.</span><span class="sxs-lookup"><span data-stu-id="a28f5-140">The entity can be any of the Scheduling entities that support the delete operation.</span></span>
- <span data-ttu-id="a28f5-141">**msdyn_ExecuteOperationSetV1**: Tämän ohjelmointirajapinnan avulla suoritetaan kaikki toiminnot tietyn toimintojoukon sisällä.</span><span class="sxs-lookup"><span data-stu-id="a28f5-141">**msdyn_ExecuteOperationSetV1**: This API is used to execute all of the operations within the given operation set.</span></span>

## <a name="using-schedule-apis-with-operationset"></a><span data-ttu-id="a28f5-142">Aikataulutuksen ohjelmointirajapintojen käyttäminen OperationSetin kanssa</span><span class="sxs-lookup"><span data-stu-id="a28f5-142">Using Schedule APIs with OperationSet</span></span>

<span data-ttu-id="a28f5-143">Koska tietueet, joissa on sekä **CreateProjectV1** että **CreateTeamMemberV1** luodaan välittömästi, näitä ohjelmointirajapintoja ei voida käyttää suoraan **OperationSet** issä.</span><span class="sxs-lookup"><span data-stu-id="a28f5-143">Because records with both **CreateProjectV1** and **CreateTeamMemberV1** are created immediately, these APIs can't be used in the **OperationSet** directly.</span></span> <span data-ttu-id="a28f5-144">Ohjelmointirajapinnan avulla voit kuitenkin luoda tarvittavat tietueet, luoda **OperationSet** in, ja käyttää sitten näitä aiemmin luotuja tietueita **OperationSet** issä.</span><span class="sxs-lookup"><span data-stu-id="a28f5-144">However, you can use the API to create needed records, create an **OperationSet**, and then use these pre-created records in the **OperationSet**.</span></span>

## <a name="supported-operations"></a><span data-ttu-id="a28f5-145">Tuetut toiminnot</span><span class="sxs-lookup"><span data-stu-id="a28f5-145">Supported operations</span></span>

| <span data-ttu-id="a28f5-146">Aikataulutusentiteetti</span><span class="sxs-lookup"><span data-stu-id="a28f5-146">Scheduling entity</span></span> | <span data-ttu-id="a28f5-147">Luo</span><span class="sxs-lookup"><span data-stu-id="a28f5-147">Create</span></span> | <span data-ttu-id="a28f5-148">Päivitys</span><span class="sxs-lookup"><span data-stu-id="a28f5-148">Update</span></span> | <span data-ttu-id="a28f5-149">Delete</span><span class="sxs-lookup"><span data-stu-id="a28f5-149">Delete</span></span> | <span data-ttu-id="a28f5-150">Tärkeitä huomioon otettavia seikkoja</span><span class="sxs-lookup"><span data-stu-id="a28f5-150">Important considerations</span></span> |
| --- | --- | --- | --- | --- |
<span data-ttu-id="a28f5-151">Projektitehtävä</span><span class="sxs-lookup"><span data-stu-id="a28f5-151">Project task</span></span> | <span data-ttu-id="a28f5-152">Kyllä</span><span class="sxs-lookup"><span data-stu-id="a28f5-152">Yes</span></span> | <span data-ttu-id="a28f5-153">Kyllä</span><span class="sxs-lookup"><span data-stu-id="a28f5-153">Yes</span></span> | <span data-ttu-id="a28f5-154">Kyllä</span><span class="sxs-lookup"><span data-stu-id="a28f5-154">Yes</span></span> | <span data-ttu-id="a28f5-155">Ei ole</span><span class="sxs-lookup"><span data-stu-id="a28f5-155">None</span></span> |
| <span data-ttu-id="a28f5-156">Projektitehtävän riippuvuus</span><span class="sxs-lookup"><span data-stu-id="a28f5-156">Project task dependency</span></span> | <span data-ttu-id="a28f5-157">Kyllä</span><span class="sxs-lookup"><span data-stu-id="a28f5-157">Yes</span></span> | <span data-ttu-id="a28f5-158">Kyllä</span><span class="sxs-lookup"><span data-stu-id="a28f5-158">Yes</span></span> | | <span data-ttu-id="a28f5-159">Projektitehtävän riippuvuustietueita ei päivitetä.</span><span class="sxs-lookup"><span data-stu-id="a28f5-159">Project task dependency records aren't updated.</span></span> <span data-ttu-id="a28f5-160">Sen sijaan voidaan poistaa vanha tietue ja luoda uusi tietue.</span><span class="sxs-lookup"><span data-stu-id="a28f5-160">Instead, an old record can be deleted and a new record can be created.</span></span> |
| <span data-ttu-id="a28f5-161">Resurssien delegointi</span><span class="sxs-lookup"><span data-stu-id="a28f5-161">Resource assignment</span></span> | <span data-ttu-id="a28f5-162">Kyllä</span><span class="sxs-lookup"><span data-stu-id="a28f5-162">Yes</span></span> | <span data-ttu-id="a28f5-163">Kyllä</span><span class="sxs-lookup"><span data-stu-id="a28f5-163">Yes</span></span> | | <span data-ttu-id="a28f5-164">Toimintoja, joilla on seuraavat kentät, ei tueta: **BookableResourceID**, **Effort**, **EffortCompleted**, **EffortRemaining** ja **PlannedWork**.</span><span class="sxs-lookup"><span data-stu-id="a28f5-164">Operations with the following fields aren't supported: **BookableResourceID**, **Effort**, **EffortCompleted**, **EffortRemaining**, and **PlannedWork**.</span></span> <span data-ttu-id="a28f5-165">Resurssien määritystietueita ei päivitetä.</span><span class="sxs-lookup"><span data-stu-id="a28f5-165">Resource assignment records aren't updated.</span></span> <span data-ttu-id="a28f5-166">Sen sijaan voidaan poistaa vanha tietue ja luoda uusi tietue.</span><span class="sxs-lookup"><span data-stu-id="a28f5-166">Instead, the old record can be deleted and a new record can be created.</span></span> |
| <span data-ttu-id="a28f5-167">Projektin säilö</span><span class="sxs-lookup"><span data-stu-id="a28f5-167">Project bucket</span></span> | <span data-ttu-id="a28f5-168">–</span><span class="sxs-lookup"><span data-stu-id="a28f5-168">N/A</span></span> | <span data-ttu-id="a28f5-169">–</span><span class="sxs-lookup"><span data-stu-id="a28f5-169">N/A</span></span> | <span data-ttu-id="a28f5-170">–</span><span class="sxs-lookup"><span data-stu-id="a28f5-170">N/A</span></span> | <span data-ttu-id="a28f5-171">Oletussäilö luodaan **CreateProjectV1** -ohjelmointirajapinnan avulla.</span><span class="sxs-lookup"><span data-stu-id="a28f5-171">The default bucket is created using the **CreateProjectV1** API.</span></span> |
| <span data-ttu-id="a28f5-172">Projektiryhmän jäsen</span><span class="sxs-lookup"><span data-stu-id="a28f5-172">Project team member</span></span> | <span data-ttu-id="a28f5-173">Kyllä</span><span class="sxs-lookup"><span data-stu-id="a28f5-173">Yes</span></span> | <span data-ttu-id="a28f5-174">Kyllä</span><span class="sxs-lookup"><span data-stu-id="a28f5-174">Yes</span></span> | <span data-ttu-id="a28f5-175">Kyllä</span><span class="sxs-lookup"><span data-stu-id="a28f5-175">Yes</span></span> | <span data-ttu-id="a28f5-176">Käytä luontioperaatiolle **CreateTeamMemberV1** -ohjelmointirajapintaa.</span><span class="sxs-lookup"><span data-stu-id="a28f5-176">For the create operation, use the **CreateTeamMemberV1** API.</span></span> |
| <span data-ttu-id="a28f5-177">Project</span><span class="sxs-lookup"><span data-stu-id="a28f5-177">Project</span></span> | <span data-ttu-id="a28f5-178">Kyllä</span><span class="sxs-lookup"><span data-stu-id="a28f5-178">Yes</span></span> | <span data-ttu-id="a28f5-179">Kyllä</span><span class="sxs-lookup"><span data-stu-id="a28f5-179">Yes</span></span> | <span data-ttu-id="a28f5-180">–</span><span class="sxs-lookup"><span data-stu-id="a28f5-180">N/A</span></span> | <span data-ttu-id="a28f5-181">Toimintoja, joilla on seuraavat kentät, ei tueta **StateCode**, **BulkGenerationStatus**, **GlobalRevisionToken**, **CalendarID**, **Effort**, **EffortCompleted**, **EffortRemaining**, **Progress**, **Finish**, **TaskEarliestStart** ja **Duration**.</span><span class="sxs-lookup"><span data-stu-id="a28f5-181">Operations with the following fields aren't supported: **StateCode**, **BulkGenerationStatus**, **GlobalRevisionToken**, **CalendarID**, **Effort**, **EffortCompleted**, **EffortRemaining**, **Progress**, **Finish**, **TaskEarliestStart**, and **Duration**.</span></span> |

<span data-ttu-id="a28f5-182">Näitä ohjelmointirajapintoja voidaan kutsua entiteettiobjekteilla, jotka sisältävät mukautettuja kenttiä.</span><span class="sxs-lookup"><span data-stu-id="a28f5-182">These APIs can be called with entity objects that include custom fields.</span></span>

<span data-ttu-id="a28f5-183">Tunnusominaisuus on valinnainen.</span><span class="sxs-lookup"><span data-stu-id="a28f5-183">The ID property is optional.</span></span> <span data-ttu-id="a28f5-184">Jos se on annettu, järjestelmä yrittää käyttää sitä ja antaa poikkeuksen, jos sitä ei voi käyttää.</span><span class="sxs-lookup"><span data-stu-id="a28f5-184">If it's provided, the system attempts to use it and throws an exception if it can't be used.</span></span> <span data-ttu-id="a28f5-185">Jos sitä ei ole annettu, järjestelmä luo sen.</span><span class="sxs-lookup"><span data-stu-id="a28f5-185">If it isn't provided, the system will generate it.</span></span>

## <a name="restricted-fields"></a><span data-ttu-id="a28f5-186">Rajoitetut kentät</span><span class="sxs-lookup"><span data-stu-id="a28f5-186">Restricted fields</span></span>

<span data-ttu-id="a28f5-187">Seuraavissa taulukoissa määritetään kentät, joita ei voi **luoda** ja **muokata**.</span><span class="sxs-lookup"><span data-stu-id="a28f5-187">The following tables define the fields that are restricted from **Create** and **Edit.**</span></span>

### <a name="project-task"></a><span data-ttu-id="a28f5-188">Projektitehtävä</span><span class="sxs-lookup"><span data-stu-id="a28f5-188">Project task</span></span>

| <span data-ttu-id="a28f5-189">**Looginen nimi**</span><span class="sxs-lookup"><span data-stu-id="a28f5-189">**Logical name**</span></span>                       | <span data-ttu-id="a28f5-190">**Voidaan luoda**</span><span class="sxs-lookup"><span data-stu-id="a28f5-190">**Can create**</span></span> | <span data-ttu-id="a28f5-191">**Voidaan muokata**</span><span class="sxs-lookup"><span data-stu-id="a28f5-191">**Can edit**</span></span>     |
|----------------------------------------|----------------|------------------|
| <span data-ttu-id="a28f5-192">msdyn_actualcost</span><span class="sxs-lookup"><span data-stu-id="a28f5-192">msdyn_actualcost</span></span>                       | <span data-ttu-id="a28f5-193">ei</span><span class="sxs-lookup"><span data-stu-id="a28f5-193">no</span></span>             | <span data-ttu-id="a28f5-194">ei</span><span class="sxs-lookup"><span data-stu-id="a28f5-194">no</span></span>               |
| <span data-ttu-id="a28f5-195">msdyn_actualcost_base</span><span class="sxs-lookup"><span data-stu-id="a28f5-195">msdyn_actualcost_base</span></span>                  | <span data-ttu-id="a28f5-196">ei</span><span class="sxs-lookup"><span data-stu-id="a28f5-196">no</span></span>             | <span data-ttu-id="a28f5-197">ei</span><span class="sxs-lookup"><span data-stu-id="a28f5-197">no</span></span>               |
| <span data-ttu-id="a28f5-198">msdyn_actualend</span><span class="sxs-lookup"><span data-stu-id="a28f5-198">msdyn_actualend</span></span>                        | <span data-ttu-id="a28f5-199">ei</span><span class="sxs-lookup"><span data-stu-id="a28f5-199">no</span></span>             | <span data-ttu-id="a28f5-200">ei</span><span class="sxs-lookup"><span data-stu-id="a28f5-200">no</span></span>               |
| <span data-ttu-id="a28f5-201">msdyn_actualsales</span><span class="sxs-lookup"><span data-stu-id="a28f5-201">msdyn_actualsales</span></span>                      | <span data-ttu-id="a28f5-202">ei</span><span class="sxs-lookup"><span data-stu-id="a28f5-202">no</span></span>             | <span data-ttu-id="a28f5-203">ei</span><span class="sxs-lookup"><span data-stu-id="a28f5-203">no</span></span>               |
| <span data-ttu-id="a28f5-204">msdyn_actualsales_base</span><span class="sxs-lookup"><span data-stu-id="a28f5-204">msdyn_actualsales_base</span></span>                 | <span data-ttu-id="a28f5-205">ei</span><span class="sxs-lookup"><span data-stu-id="a28f5-205">no</span></span>             | <span data-ttu-id="a28f5-206">ei</span><span class="sxs-lookup"><span data-stu-id="a28f5-206">no</span></span>               |
| <span data-ttu-id="a28f5-207">msdyn_actualstart</span><span class="sxs-lookup"><span data-stu-id="a28f5-207">msdyn_actualstart</span></span>                      | <span data-ttu-id="a28f5-208">ei</span><span class="sxs-lookup"><span data-stu-id="a28f5-208">no</span></span>             | <span data-ttu-id="a28f5-209">ei</span><span class="sxs-lookup"><span data-stu-id="a28f5-209">no</span></span>               |
| <span data-ttu-id="a28f5-210">msdyn_costatcompleteestimate</span><span class="sxs-lookup"><span data-stu-id="a28f5-210">msdyn_costatcompleteestimate</span></span>           | <span data-ttu-id="a28f5-211">ei</span><span class="sxs-lookup"><span data-stu-id="a28f5-211">no</span></span>             | <span data-ttu-id="a28f5-212">ei</span><span class="sxs-lookup"><span data-stu-id="a28f5-212">no</span></span>               |
| <span data-ttu-id="a28f5-213">msdyn_costatcompleteestimate_base</span><span class="sxs-lookup"><span data-stu-id="a28f5-213">msdyn_costatcompleteestimate_base</span></span>      | <span data-ttu-id="a28f5-214">ei</span><span class="sxs-lookup"><span data-stu-id="a28f5-214">no</span></span>             | <span data-ttu-id="a28f5-215">ei</span><span class="sxs-lookup"><span data-stu-id="a28f5-215">no</span></span>               |
| <span data-ttu-id="a28f5-216">msdyn_costconsumptionpercentage</span><span class="sxs-lookup"><span data-stu-id="a28f5-216">msdyn_costconsumptionpercentage</span></span>        | <span data-ttu-id="a28f5-217">ei</span><span class="sxs-lookup"><span data-stu-id="a28f5-217">no</span></span>             | <span data-ttu-id="a28f5-218">ei</span><span class="sxs-lookup"><span data-stu-id="a28f5-218">no</span></span>               |
| <span data-ttu-id="a28f5-219">msdyn_effortcompleted</span><span class="sxs-lookup"><span data-stu-id="a28f5-219">msdyn_effortcompleted</span></span>                  | <span data-ttu-id="a28f5-220">ei</span><span class="sxs-lookup"><span data-stu-id="a28f5-220">no</span></span>             | <span data-ttu-id="a28f5-221">ei</span><span class="sxs-lookup"><span data-stu-id="a28f5-221">no</span></span>               |
| <span data-ttu-id="a28f5-222">msdyn_effortestimateatcomplete</span><span class="sxs-lookup"><span data-stu-id="a28f5-222">msdyn_effortestimateatcomplete</span></span>         | <span data-ttu-id="a28f5-223">ei</span><span class="sxs-lookup"><span data-stu-id="a28f5-223">no</span></span>             | <span data-ttu-id="a28f5-224">ei</span><span class="sxs-lookup"><span data-stu-id="a28f5-224">no</span></span>               |
| <span data-ttu-id="a28f5-225">msdyn_iscritical</span><span class="sxs-lookup"><span data-stu-id="a28f5-225">msdyn_iscritical</span></span>                       | <span data-ttu-id="a28f5-226">ei</span><span class="sxs-lookup"><span data-stu-id="a28f5-226">no</span></span>             | <span data-ttu-id="a28f5-227">ei</span><span class="sxs-lookup"><span data-stu-id="a28f5-227">no</span></span>               |
| <span data-ttu-id="a28f5-228">msdyn_iscriticalname</span><span class="sxs-lookup"><span data-stu-id="a28f5-228">msdyn_iscriticalname</span></span>                   | <span data-ttu-id="a28f5-229">ei</span><span class="sxs-lookup"><span data-stu-id="a28f5-229">no</span></span>             | <span data-ttu-id="a28f5-230">ei</span><span class="sxs-lookup"><span data-stu-id="a28f5-230">no</span></span>               |
| <span data-ttu-id="a28f5-231">msdyn_ismanual</span><span class="sxs-lookup"><span data-stu-id="a28f5-231">msdyn_ismanual</span></span>                         | <span data-ttu-id="a28f5-232">ei</span><span class="sxs-lookup"><span data-stu-id="a28f5-232">no</span></span>             | <span data-ttu-id="a28f5-233">ei</span><span class="sxs-lookup"><span data-stu-id="a28f5-233">no</span></span>               |
| <span data-ttu-id="a28f5-234">msdyn_ismanualname</span><span class="sxs-lookup"><span data-stu-id="a28f5-234">msdyn_ismanualname</span></span>                     | <span data-ttu-id="a28f5-235">ei</span><span class="sxs-lookup"><span data-stu-id="a28f5-235">no</span></span>             | <span data-ttu-id="a28f5-236">ei</span><span class="sxs-lookup"><span data-stu-id="a28f5-236">no</span></span>               |
| <span data-ttu-id="a28f5-237">msdyn_ismilestone</span><span class="sxs-lookup"><span data-stu-id="a28f5-237">msdyn_ismilestone</span></span>                      | <span data-ttu-id="a28f5-238">ei</span><span class="sxs-lookup"><span data-stu-id="a28f5-238">no</span></span>             | <span data-ttu-id="a28f5-239">ei</span><span class="sxs-lookup"><span data-stu-id="a28f5-239">no</span></span>               |
| <span data-ttu-id="a28f5-240">msdyn_ismilestonename</span><span class="sxs-lookup"><span data-stu-id="a28f5-240">msdyn_ismilestonename</span></span>                  | <span data-ttu-id="a28f5-241">ei</span><span class="sxs-lookup"><span data-stu-id="a28f5-241">no</span></span>             | <span data-ttu-id="a28f5-242">ei</span><span class="sxs-lookup"><span data-stu-id="a28f5-242">no</span></span>               |
| <span data-ttu-id="a28f5-243">msdyn_LinkStatus</span><span class="sxs-lookup"><span data-stu-id="a28f5-243">msdyn_LinkStatus</span></span>                       | <span data-ttu-id="a28f5-244">ei</span><span class="sxs-lookup"><span data-stu-id="a28f5-244">no</span></span>             | <span data-ttu-id="a28f5-245">ei</span><span class="sxs-lookup"><span data-stu-id="a28f5-245">no</span></span>               |
| <span data-ttu-id="a28f5-246">msdyn_linkstatusname</span><span class="sxs-lookup"><span data-stu-id="a28f5-246">msdyn_linkstatusname</span></span>                   | <span data-ttu-id="a28f5-247">ei</span><span class="sxs-lookup"><span data-stu-id="a28f5-247">no</span></span>             | <span data-ttu-id="a28f5-248">ei</span><span class="sxs-lookup"><span data-stu-id="a28f5-248">no</span></span>               |
| <span data-ttu-id="a28f5-249">msdyn_msprojectclientid</span><span class="sxs-lookup"><span data-stu-id="a28f5-249">msdyn_msprojectclientid</span></span>                | <span data-ttu-id="a28f5-250">ei</span><span class="sxs-lookup"><span data-stu-id="a28f5-250">no</span></span>             | <span data-ttu-id="a28f5-251">ei</span><span class="sxs-lookup"><span data-stu-id="a28f5-251">no</span></span>               |
| <span data-ttu-id="a28f5-252">msdyn_plannedcost</span><span class="sxs-lookup"><span data-stu-id="a28f5-252">msdyn_plannedcost</span></span>                      | <span data-ttu-id="a28f5-253">ei</span><span class="sxs-lookup"><span data-stu-id="a28f5-253">no</span></span>             | <span data-ttu-id="a28f5-254">ei</span><span class="sxs-lookup"><span data-stu-id="a28f5-254">no</span></span>               |
| <span data-ttu-id="a28f5-255">msdyn_plannedcost_base</span><span class="sxs-lookup"><span data-stu-id="a28f5-255">msdyn_plannedcost_base</span></span>                 | <span data-ttu-id="a28f5-256">ei</span><span class="sxs-lookup"><span data-stu-id="a28f5-256">no</span></span>             | <span data-ttu-id="a28f5-257">ei</span><span class="sxs-lookup"><span data-stu-id="a28f5-257">no</span></span>               |
| <span data-ttu-id="a28f5-258">msdyn_plannedsales</span><span class="sxs-lookup"><span data-stu-id="a28f5-258">msdyn_plannedsales</span></span>                     | <span data-ttu-id="a28f5-259">ei</span><span class="sxs-lookup"><span data-stu-id="a28f5-259">no</span></span>             | <span data-ttu-id="a28f5-260">ei</span><span class="sxs-lookup"><span data-stu-id="a28f5-260">no</span></span>               |
| <span data-ttu-id="a28f5-261">msdyn_plannedsales_base</span><span class="sxs-lookup"><span data-stu-id="a28f5-261">msdyn_plannedsales_base</span></span>                | <span data-ttu-id="a28f5-262">ei</span><span class="sxs-lookup"><span data-stu-id="a28f5-262">no</span></span>             | <span data-ttu-id="a28f5-263">ei</span><span class="sxs-lookup"><span data-stu-id="a28f5-263">no</span></span>               |
| <span data-ttu-id="a28f5-264">msdyn_pluginprocessingdata</span><span class="sxs-lookup"><span data-stu-id="a28f5-264">msdyn_pluginprocessingdata</span></span>             | <span data-ttu-id="a28f5-265">ei</span><span class="sxs-lookup"><span data-stu-id="a28f5-265">no</span></span>             | <span data-ttu-id="a28f5-266">ei</span><span class="sxs-lookup"><span data-stu-id="a28f5-266">no</span></span>               |
| <span data-ttu-id="a28f5-267">msdyn_progress</span><span class="sxs-lookup"><span data-stu-id="a28f5-267">msdyn_progress</span></span>                         | <span data-ttu-id="a28f5-268">ei</span><span class="sxs-lookup"><span data-stu-id="a28f5-268">no</span></span>             | <span data-ttu-id="a28f5-269">ei (kyllä P4W:lle)</span><span class="sxs-lookup"><span data-stu-id="a28f5-269">no (yes for P4W)</span></span> |
| <span data-ttu-id="a28f5-270">msdyn_remainingcost</span><span class="sxs-lookup"><span data-stu-id="a28f5-270">msdyn_remainingcost</span></span>                    | <span data-ttu-id="a28f5-271">ei</span><span class="sxs-lookup"><span data-stu-id="a28f5-271">no</span></span>             | <span data-ttu-id="a28f5-272">ei</span><span class="sxs-lookup"><span data-stu-id="a28f5-272">no</span></span>               |
| <span data-ttu-id="a28f5-273">msdyn_remainingcost_base</span><span class="sxs-lookup"><span data-stu-id="a28f5-273">msdyn_remainingcost_base</span></span>               | <span data-ttu-id="a28f5-274">ei</span><span class="sxs-lookup"><span data-stu-id="a28f5-274">no</span></span>             | <span data-ttu-id="a28f5-275">ei</span><span class="sxs-lookup"><span data-stu-id="a28f5-275">no</span></span>               |
| <span data-ttu-id="a28f5-276">msdyn_remainingsales</span><span class="sxs-lookup"><span data-stu-id="a28f5-276">msdyn_remainingsales</span></span>                   | <span data-ttu-id="a28f5-277">ei</span><span class="sxs-lookup"><span data-stu-id="a28f5-277">no</span></span>             | <span data-ttu-id="a28f5-278">ei</span><span class="sxs-lookup"><span data-stu-id="a28f5-278">no</span></span>               |
| <span data-ttu-id="a28f5-279">msdyn_remainingsales_base</span><span class="sxs-lookup"><span data-stu-id="a28f5-279">msdyn_remainingsales_base</span></span>              | <span data-ttu-id="a28f5-280">ei</span><span class="sxs-lookup"><span data-stu-id="a28f5-280">no</span></span>             | <span data-ttu-id="a28f5-281">ei</span><span class="sxs-lookup"><span data-stu-id="a28f5-281">no</span></span>               |
| <span data-ttu-id="a28f5-282">msdyn_requestedhours</span><span class="sxs-lookup"><span data-stu-id="a28f5-282">msdyn_requestedhours</span></span>                   | <span data-ttu-id="a28f5-283">ei</span><span class="sxs-lookup"><span data-stu-id="a28f5-283">no</span></span>             | <span data-ttu-id="a28f5-284">ei</span><span class="sxs-lookup"><span data-stu-id="a28f5-284">no</span></span>               |
| <span data-ttu-id="a28f5-285">msdyn_resourcecategory</span><span class="sxs-lookup"><span data-stu-id="a28f5-285">msdyn_resourcecategory</span></span>                 | <span data-ttu-id="a28f5-286">ei</span><span class="sxs-lookup"><span data-stu-id="a28f5-286">no</span></span>             | <span data-ttu-id="a28f5-287">ei</span><span class="sxs-lookup"><span data-stu-id="a28f5-287">no</span></span>               |
| <span data-ttu-id="a28f5-288">msdyn_resourcecategoryname</span><span class="sxs-lookup"><span data-stu-id="a28f5-288">msdyn_resourcecategoryname</span></span>             | <span data-ttu-id="a28f5-289">ei</span><span class="sxs-lookup"><span data-stu-id="a28f5-289">no</span></span>             | <span data-ttu-id="a28f5-290">ei</span><span class="sxs-lookup"><span data-stu-id="a28f5-290">no</span></span>               |
| <span data-ttu-id="a28f5-291">msdyn_resourceorganizationalunitid</span><span class="sxs-lookup"><span data-stu-id="a28f5-291">msdyn_resourceorganizationalunitid</span></span>     | <span data-ttu-id="a28f5-292">ei</span><span class="sxs-lookup"><span data-stu-id="a28f5-292">no</span></span>             | <span data-ttu-id="a28f5-293">ei</span><span class="sxs-lookup"><span data-stu-id="a28f5-293">no</span></span>               |
| <span data-ttu-id="a28f5-294">msdyn_resourceorganizationalunitidname</span><span class="sxs-lookup"><span data-stu-id="a28f5-294">msdyn_resourceorganizationalunitidname</span></span> | <span data-ttu-id="a28f5-295">ei</span><span class="sxs-lookup"><span data-stu-id="a28f5-295">no</span></span>             | <span data-ttu-id="a28f5-296">ei</span><span class="sxs-lookup"><span data-stu-id="a28f5-296">no</span></span>               |
| <span data-ttu-id="a28f5-297">msdyn_salesconsumptionpercentage</span><span class="sxs-lookup"><span data-stu-id="a28f5-297">msdyn_salesconsumptionpercentage</span></span>       | <span data-ttu-id="a28f5-298">ei</span><span class="sxs-lookup"><span data-stu-id="a28f5-298">no</span></span>             | <span data-ttu-id="a28f5-299">ei</span><span class="sxs-lookup"><span data-stu-id="a28f5-299">no</span></span>               |
| <span data-ttu-id="a28f5-300">msdyn_salesestimateatcomplete</span><span class="sxs-lookup"><span data-stu-id="a28f5-300">msdyn_salesestimateatcomplete</span></span>          | <span data-ttu-id="a28f5-301">ei</span><span class="sxs-lookup"><span data-stu-id="a28f5-301">no</span></span>             | <span data-ttu-id="a28f5-302">ei</span><span class="sxs-lookup"><span data-stu-id="a28f5-302">no</span></span>               |
| <span data-ttu-id="a28f5-303">msdyn_salesestimateatcomplete_base</span><span class="sxs-lookup"><span data-stu-id="a28f5-303">msdyn_salesestimateatcomplete_base</span></span>     | <span data-ttu-id="a28f5-304">ei</span><span class="sxs-lookup"><span data-stu-id="a28f5-304">no</span></span>             | <span data-ttu-id="a28f5-305">ei</span><span class="sxs-lookup"><span data-stu-id="a28f5-305">no</span></span>               |
| <span data-ttu-id="a28f5-306">msdyn_salesvariance</span><span class="sxs-lookup"><span data-stu-id="a28f5-306">msdyn_salesvariance</span></span>                    | <span data-ttu-id="a28f5-307">ei</span><span class="sxs-lookup"><span data-stu-id="a28f5-307">no</span></span>             | <span data-ttu-id="a28f5-308">ei</span><span class="sxs-lookup"><span data-stu-id="a28f5-308">no</span></span>               |
| <span data-ttu-id="a28f5-309">msdyn_salesvariance_base</span><span class="sxs-lookup"><span data-stu-id="a28f5-309">msdyn_salesvariance_base</span></span>               | <span data-ttu-id="a28f5-310">ei</span><span class="sxs-lookup"><span data-stu-id="a28f5-310">no</span></span>             | <span data-ttu-id="a28f5-311">ei</span><span class="sxs-lookup"><span data-stu-id="a28f5-311">no</span></span>               |
| <span data-ttu-id="a28f5-312">msdyn_scheduleddurationminutes</span><span class="sxs-lookup"><span data-stu-id="a28f5-312">msdyn_scheduleddurationminutes</span></span>         | <span data-ttu-id="a28f5-313">ei</span><span class="sxs-lookup"><span data-stu-id="a28f5-313">no</span></span>             | <span data-ttu-id="a28f5-314">ei</span><span class="sxs-lookup"><span data-stu-id="a28f5-314">no</span></span>               |
| <span data-ttu-id="a28f5-315">msdyn_scheduledend</span><span class="sxs-lookup"><span data-stu-id="a28f5-315">msdyn_scheduledend</span></span>                     | <span data-ttu-id="a28f5-316">ei</span><span class="sxs-lookup"><span data-stu-id="a28f5-316">no</span></span>             | <span data-ttu-id="a28f5-317">ei</span><span class="sxs-lookup"><span data-stu-id="a28f5-317">no</span></span>               |
| <span data-ttu-id="a28f5-318">msdyn_scheduledstart</span><span class="sxs-lookup"><span data-stu-id="a28f5-318">msdyn_scheduledstart</span></span>                   | <span data-ttu-id="a28f5-319">ei</span><span class="sxs-lookup"><span data-stu-id="a28f5-319">no</span></span>             | <span data-ttu-id="a28f5-320">ei</span><span class="sxs-lookup"><span data-stu-id="a28f5-320">no</span></span>               |
| <span data-ttu-id="a28f5-321">msdyn_schedulevariance</span><span class="sxs-lookup"><span data-stu-id="a28f5-321">msdyn_schedulevariance</span></span>                 | <span data-ttu-id="a28f5-322">ei</span><span class="sxs-lookup"><span data-stu-id="a28f5-322">no</span></span>             | <span data-ttu-id="a28f5-323">ei</span><span class="sxs-lookup"><span data-stu-id="a28f5-323">no</span></span>               |
| <span data-ttu-id="a28f5-324">msdyn_skipupdateestimateline</span><span class="sxs-lookup"><span data-stu-id="a28f5-324">msdyn_skipupdateestimateline</span></span>           | <span data-ttu-id="a28f5-325">ei</span><span class="sxs-lookup"><span data-stu-id="a28f5-325">no</span></span>             | <span data-ttu-id="a28f5-326">ei</span><span class="sxs-lookup"><span data-stu-id="a28f5-326">no</span></span>               |
| <span data-ttu-id="a28f5-327">msdyn_skipupdateestimatelinename</span><span class="sxs-lookup"><span data-stu-id="a28f5-327">msdyn_skipupdateestimatelinename</span></span>       | <span data-ttu-id="a28f5-328">ei</span><span class="sxs-lookup"><span data-stu-id="a28f5-328">no</span></span>             | <span data-ttu-id="a28f5-329">ei</span><span class="sxs-lookup"><span data-stu-id="a28f5-329">no</span></span>               |
| <span data-ttu-id="a28f5-330">msdyn_summary</span><span class="sxs-lookup"><span data-stu-id="a28f5-330">msdyn_summary</span></span>                          | <span data-ttu-id="a28f5-331">ei</span><span class="sxs-lookup"><span data-stu-id="a28f5-331">no</span></span>             | <span data-ttu-id="a28f5-332">ei</span><span class="sxs-lookup"><span data-stu-id="a28f5-332">no</span></span>               |
| <span data-ttu-id="a28f5-333">msdyn_varianceofcost</span><span class="sxs-lookup"><span data-stu-id="a28f5-333">msdyn_varianceofcost</span></span>                   | <span data-ttu-id="a28f5-334">ei</span><span class="sxs-lookup"><span data-stu-id="a28f5-334">no</span></span>             | <span data-ttu-id="a28f5-335">ei</span><span class="sxs-lookup"><span data-stu-id="a28f5-335">no</span></span>               |
| <span data-ttu-id="a28f5-336">msdyn_varianceofcost_base</span><span class="sxs-lookup"><span data-stu-id="a28f5-336">msdyn_varianceofcost_base</span></span>              | <span data-ttu-id="a28f5-337">ei</span><span class="sxs-lookup"><span data-stu-id="a28f5-337">no</span></span>             | <span data-ttu-id="a28f5-338">ei</span><span class="sxs-lookup"><span data-stu-id="a28f5-338">no</span></span>               |

### <a name="project-task-dependency"></a><span data-ttu-id="a28f5-339">Projektitehtävän riippuvuus</span><span class="sxs-lookup"><span data-stu-id="a28f5-339">Project task dependency</span></span>

| <span data-ttu-id="a28f5-340">**Looginen nimi**</span><span class="sxs-lookup"><span data-stu-id="a28f5-340">**Logical name**</span></span>              | <span data-ttu-id="a28f5-341">**Voidaan luoda**</span><span class="sxs-lookup"><span data-stu-id="a28f5-341">**Can create**</span></span> | <span data-ttu-id="a28f5-342">**Voidaan muokata**</span><span class="sxs-lookup"><span data-stu-id="a28f5-342">**Can edit**</span></span> |
|-------------------------------|----------------|--------------|
| <span data-ttu-id="a28f5-343">msdyn_linktype</span><span class="sxs-lookup"><span data-stu-id="a28f5-343">msdyn_linktype</span></span>                | <span data-ttu-id="a28f5-344">ei</span><span class="sxs-lookup"><span data-stu-id="a28f5-344">no</span></span>             | <span data-ttu-id="a28f5-345">ei</span><span class="sxs-lookup"><span data-stu-id="a28f5-345">no</span></span>           |
| <span data-ttu-id="a28f5-346">msdyn_linktypename</span><span class="sxs-lookup"><span data-stu-id="a28f5-346">msdyn_linktypename</span></span>            | <span data-ttu-id="a28f5-347">ei</span><span class="sxs-lookup"><span data-stu-id="a28f5-347">no</span></span>             | <span data-ttu-id="a28f5-348">ei</span><span class="sxs-lookup"><span data-stu-id="a28f5-348">no</span></span>           |
| <span data-ttu-id="a28f5-349">msdyn_predecessortask</span><span class="sxs-lookup"><span data-stu-id="a28f5-349">msdyn_predecessortask</span></span>         | <span data-ttu-id="a28f5-350">kyllä</span><span class="sxs-lookup"><span data-stu-id="a28f5-350">yes</span></span>            | <span data-ttu-id="a28f5-351">ei</span><span class="sxs-lookup"><span data-stu-id="a28f5-351">no</span></span>           |
| <span data-ttu-id="a28f5-352">msdyn_predecessortaskname</span><span class="sxs-lookup"><span data-stu-id="a28f5-352">msdyn_predecessortaskname</span></span>     | <span data-ttu-id="a28f5-353">kyllä</span><span class="sxs-lookup"><span data-stu-id="a28f5-353">yes</span></span>            | <span data-ttu-id="a28f5-354">ei</span><span class="sxs-lookup"><span data-stu-id="a28f5-354">no</span></span>           |
| <span data-ttu-id="a28f5-355">msdyn_project</span><span class="sxs-lookup"><span data-stu-id="a28f5-355">msdyn_project</span></span>                 | <span data-ttu-id="a28f5-356">kyllä</span><span class="sxs-lookup"><span data-stu-id="a28f5-356">yes</span></span>            | <span data-ttu-id="a28f5-357">ei</span><span class="sxs-lookup"><span data-stu-id="a28f5-357">no</span></span>           |
| <span data-ttu-id="a28f5-358">msdyn_projectname</span><span class="sxs-lookup"><span data-stu-id="a28f5-358">msdyn_projectname</span></span>             | <span data-ttu-id="a28f5-359">kyllä</span><span class="sxs-lookup"><span data-stu-id="a28f5-359">yes</span></span>            | <span data-ttu-id="a28f5-360">ei</span><span class="sxs-lookup"><span data-stu-id="a28f5-360">no</span></span>           |
| <span data-ttu-id="a28f5-361">msdyn_projecttaskdependencyid</span><span class="sxs-lookup"><span data-stu-id="a28f5-361">msdyn_projecttaskdependencyid</span></span> | <span data-ttu-id="a28f5-362">kyllä</span><span class="sxs-lookup"><span data-stu-id="a28f5-362">yes</span></span>            | <span data-ttu-id="a28f5-363">ei</span><span class="sxs-lookup"><span data-stu-id="a28f5-363">no</span></span>           |
| <span data-ttu-id="a28f5-364">msdyn_successortask</span><span class="sxs-lookup"><span data-stu-id="a28f5-364">msdyn_successortask</span></span>           | <span data-ttu-id="a28f5-365">kyllä</span><span class="sxs-lookup"><span data-stu-id="a28f5-365">yes</span></span>            | <span data-ttu-id="a28f5-366">ei</span><span class="sxs-lookup"><span data-stu-id="a28f5-366">no</span></span>           |
| <span data-ttu-id="a28f5-367">msdyn_successortaskname</span><span class="sxs-lookup"><span data-stu-id="a28f5-367">msdyn_successortaskname</span></span>       | <span data-ttu-id="a28f5-368">kyllä</span><span class="sxs-lookup"><span data-stu-id="a28f5-368">yes</span></span>            | <span data-ttu-id="a28f5-369">ei</span><span class="sxs-lookup"><span data-stu-id="a28f5-369">no</span></span>           |

### <a name="resource-assignment"></a><span data-ttu-id="a28f5-370">Resurssien delegointi</span><span class="sxs-lookup"><span data-stu-id="a28f5-370">Resource assignment</span></span>

| <span data-ttu-id="a28f5-371">**Looginen nimi**</span><span class="sxs-lookup"><span data-stu-id="a28f5-371">**Logical name**</span></span>             | <span data-ttu-id="a28f5-372">**Voidaan luoda**</span><span class="sxs-lookup"><span data-stu-id="a28f5-372">**Can create**</span></span> | <span data-ttu-id="a28f5-373">**Voidaan muokata**</span><span class="sxs-lookup"><span data-stu-id="a28f5-373">**Can edit**</span></span> |
|------------------------------|----------------|--------------|
| <span data-ttu-id="a28f5-374">msdyn_bookableresourceid</span><span class="sxs-lookup"><span data-stu-id="a28f5-374">msdyn_bookableresourceid</span></span>     | <span data-ttu-id="a28f5-375">kyllä</span><span class="sxs-lookup"><span data-stu-id="a28f5-375">yes</span></span>            | <span data-ttu-id="a28f5-376">ei</span><span class="sxs-lookup"><span data-stu-id="a28f5-376">no</span></span>           |
| <span data-ttu-id="a28f5-377">msdyn_bookableresourceidname</span><span class="sxs-lookup"><span data-stu-id="a28f5-377">msdyn_bookableresourceidname</span></span> | <span data-ttu-id="a28f5-378">kyllä</span><span class="sxs-lookup"><span data-stu-id="a28f5-378">yes</span></span>            | <span data-ttu-id="a28f5-379">ei</span><span class="sxs-lookup"><span data-stu-id="a28f5-379">no</span></span>           |
| <span data-ttu-id="a28f5-380">msdyn_bookingstatusid</span><span class="sxs-lookup"><span data-stu-id="a28f5-380">msdyn_bookingstatusid</span></span>        | <span data-ttu-id="a28f5-381">ei</span><span class="sxs-lookup"><span data-stu-id="a28f5-381">no</span></span>             | <span data-ttu-id="a28f5-382">ei</span><span class="sxs-lookup"><span data-stu-id="a28f5-382">no</span></span>           |
| <span data-ttu-id="a28f5-383">msdyn_bookingstatusidname</span><span class="sxs-lookup"><span data-stu-id="a28f5-383">msdyn_bookingstatusidname</span></span>    | <span data-ttu-id="a28f5-384">ei</span><span class="sxs-lookup"><span data-stu-id="a28f5-384">no</span></span>             | <span data-ttu-id="a28f5-385">ei</span><span class="sxs-lookup"><span data-stu-id="a28f5-385">no</span></span>           |
| <span data-ttu-id="a28f5-386">msdyn_committype</span><span class="sxs-lookup"><span data-stu-id="a28f5-386">msdyn_committype</span></span>             | <span data-ttu-id="a28f5-387">ei</span><span class="sxs-lookup"><span data-stu-id="a28f5-387">no</span></span>             | <span data-ttu-id="a28f5-388">ei</span><span class="sxs-lookup"><span data-stu-id="a28f5-388">no</span></span>           |
| <span data-ttu-id="a28f5-389">msdyn_committypename</span><span class="sxs-lookup"><span data-stu-id="a28f5-389">msdyn_committypename</span></span>         | <span data-ttu-id="a28f5-390">ei</span><span class="sxs-lookup"><span data-stu-id="a28f5-390">no</span></span>             | <span data-ttu-id="a28f5-391">ei</span><span class="sxs-lookup"><span data-stu-id="a28f5-391">no</span></span>           |
| <span data-ttu-id="a28f5-392">msdyn_effort</span><span class="sxs-lookup"><span data-stu-id="a28f5-392">msdyn_effort</span></span>                 | <span data-ttu-id="a28f5-393">ei</span><span class="sxs-lookup"><span data-stu-id="a28f5-393">no</span></span>             | <span data-ttu-id="a28f5-394">ei</span><span class="sxs-lookup"><span data-stu-id="a28f5-394">no</span></span>           |
| <span data-ttu-id="a28f5-395">msdyn_effortcompleted</span><span class="sxs-lookup"><span data-stu-id="a28f5-395">msdyn_effortcompleted</span></span>        | <span data-ttu-id="a28f5-396">ei</span><span class="sxs-lookup"><span data-stu-id="a28f5-396">no</span></span>             | <span data-ttu-id="a28f5-397">ei</span><span class="sxs-lookup"><span data-stu-id="a28f5-397">no</span></span>           |
| <span data-ttu-id="a28f5-398">msdyn_effortremaining</span><span class="sxs-lookup"><span data-stu-id="a28f5-398">msdyn_effortremaining</span></span>        | <span data-ttu-id="a28f5-399">ei</span><span class="sxs-lookup"><span data-stu-id="a28f5-399">no</span></span>             | <span data-ttu-id="a28f5-400">ei</span><span class="sxs-lookup"><span data-stu-id="a28f5-400">no</span></span>           |
| <span data-ttu-id="a28f5-401">msdyn_finish</span><span class="sxs-lookup"><span data-stu-id="a28f5-401">msdyn_finish</span></span>                 | <span data-ttu-id="a28f5-402">ei</span><span class="sxs-lookup"><span data-stu-id="a28f5-402">no</span></span>             | <span data-ttu-id="a28f5-403">ei</span><span class="sxs-lookup"><span data-stu-id="a28f5-403">no</span></span>           |
| <span data-ttu-id="a28f5-404">msdyn_plannedcost</span><span class="sxs-lookup"><span data-stu-id="a28f5-404">msdyn_plannedcost</span></span>            | <span data-ttu-id="a28f5-405">ei</span><span class="sxs-lookup"><span data-stu-id="a28f5-405">no</span></span>             | <span data-ttu-id="a28f5-406">ei</span><span class="sxs-lookup"><span data-stu-id="a28f5-406">no</span></span>           |
| <span data-ttu-id="a28f5-407">msdyn_plannedcost_base</span><span class="sxs-lookup"><span data-stu-id="a28f5-407">msdyn_plannedcost_base</span></span>       | <span data-ttu-id="a28f5-408">ei</span><span class="sxs-lookup"><span data-stu-id="a28f5-408">no</span></span>             | <span data-ttu-id="a28f5-409">ei</span><span class="sxs-lookup"><span data-stu-id="a28f5-409">no</span></span>           |
| <span data-ttu-id="a28f5-410">msdyn_plannedcostcontour</span><span class="sxs-lookup"><span data-stu-id="a28f5-410">msdyn_plannedcostcontour</span></span>     | <span data-ttu-id="a28f5-411">ei</span><span class="sxs-lookup"><span data-stu-id="a28f5-411">no</span></span>             | <span data-ttu-id="a28f5-412">ei</span><span class="sxs-lookup"><span data-stu-id="a28f5-412">no</span></span>           |
| <span data-ttu-id="a28f5-413">msdyn_plannedsales</span><span class="sxs-lookup"><span data-stu-id="a28f5-413">msdyn_plannedsales</span></span>           | <span data-ttu-id="a28f5-414">ei</span><span class="sxs-lookup"><span data-stu-id="a28f5-414">no</span></span>             | <span data-ttu-id="a28f5-415">ei</span><span class="sxs-lookup"><span data-stu-id="a28f5-415">no</span></span>           |
| <span data-ttu-id="a28f5-416">msdyn_plannedsales_base</span><span class="sxs-lookup"><span data-stu-id="a28f5-416">msdyn_plannedsales_base</span></span>      | <span data-ttu-id="a28f5-417">ei</span><span class="sxs-lookup"><span data-stu-id="a28f5-417">no</span></span>             | <span data-ttu-id="a28f5-418">ei</span><span class="sxs-lookup"><span data-stu-id="a28f5-418">no</span></span>           |
| <span data-ttu-id="a28f5-419">msdyn_plannedsalescontour</span><span class="sxs-lookup"><span data-stu-id="a28f5-419">msdyn_plannedsalescontour</span></span>    | <span data-ttu-id="a28f5-420">ei</span><span class="sxs-lookup"><span data-stu-id="a28f5-420">no</span></span>             | <span data-ttu-id="a28f5-421">ei</span><span class="sxs-lookup"><span data-stu-id="a28f5-421">no</span></span>           |
| <span data-ttu-id="a28f5-422">msdyn_plannedwork</span><span class="sxs-lookup"><span data-stu-id="a28f5-422">msdyn_plannedwork</span></span>            | <span data-ttu-id="a28f5-423">ei</span><span class="sxs-lookup"><span data-stu-id="a28f5-423">no</span></span>             | <span data-ttu-id="a28f5-424">ei</span><span class="sxs-lookup"><span data-stu-id="a28f5-424">no</span></span>           |
| <span data-ttu-id="a28f5-425">msdyn_projectid</span><span class="sxs-lookup"><span data-stu-id="a28f5-425">msdyn_projectid</span></span>              | <span data-ttu-id="a28f5-426">kyllä</span><span class="sxs-lookup"><span data-stu-id="a28f5-426">yes</span></span>            | <span data-ttu-id="a28f5-427">ei</span><span class="sxs-lookup"><span data-stu-id="a28f5-427">no</span></span>           |
| <span data-ttu-id="a28f5-428">msdyn_projectidname</span><span class="sxs-lookup"><span data-stu-id="a28f5-428">msdyn_projectidname</span></span>          | <span data-ttu-id="a28f5-429">ei</span><span class="sxs-lookup"><span data-stu-id="a28f5-429">no</span></span>             | <span data-ttu-id="a28f5-430">ei</span><span class="sxs-lookup"><span data-stu-id="a28f5-430">no</span></span>           |
| <span data-ttu-id="a28f5-431">msdyn_projectteamid</span><span class="sxs-lookup"><span data-stu-id="a28f5-431">msdyn_projectteamid</span></span>          | <span data-ttu-id="a28f5-432">ei</span><span class="sxs-lookup"><span data-stu-id="a28f5-432">no</span></span>             | <span data-ttu-id="a28f5-433">ei</span><span class="sxs-lookup"><span data-stu-id="a28f5-433">no</span></span>           |
| <span data-ttu-id="a28f5-434">msdyn_projectteamidname</span><span class="sxs-lookup"><span data-stu-id="a28f5-434">msdyn_projectteamidname</span></span>      | <span data-ttu-id="a28f5-435">ei</span><span class="sxs-lookup"><span data-stu-id="a28f5-435">no</span></span>             | <span data-ttu-id="a28f5-436">ei</span><span class="sxs-lookup"><span data-stu-id="a28f5-436">no</span></span>           |
| <span data-ttu-id="a28f5-437">msdyn_start</span><span class="sxs-lookup"><span data-stu-id="a28f5-437">msdyn_start</span></span>                  | <span data-ttu-id="a28f5-438">ei</span><span class="sxs-lookup"><span data-stu-id="a28f5-438">no</span></span>             | <span data-ttu-id="a28f5-439">ei</span><span class="sxs-lookup"><span data-stu-id="a28f5-439">no</span></span>           |
| <span data-ttu-id="a28f5-440">msdyn_taskid</span><span class="sxs-lookup"><span data-stu-id="a28f5-440">msdyn_taskid</span></span>                 | <span data-ttu-id="a28f5-441">ei</span><span class="sxs-lookup"><span data-stu-id="a28f5-441">no</span></span>             | <span data-ttu-id="a28f5-442">ei</span><span class="sxs-lookup"><span data-stu-id="a28f5-442">no</span></span>           |
| <span data-ttu-id="a28f5-443">msdyn_taskidname</span><span class="sxs-lookup"><span data-stu-id="a28f5-443">msdyn_taskidname</span></span>             | <span data-ttu-id="a28f5-444">ei</span><span class="sxs-lookup"><span data-stu-id="a28f5-444">no</span></span>             | <span data-ttu-id="a28f5-445">ei</span><span class="sxs-lookup"><span data-stu-id="a28f5-445">no</span></span>           |
| <span data-ttu-id="a28f5-446">msdyn_userresourceid</span><span class="sxs-lookup"><span data-stu-id="a28f5-446">msdyn_userresourceid</span></span>         | <span data-ttu-id="a28f5-447">ei</span><span class="sxs-lookup"><span data-stu-id="a28f5-447">no</span></span>             | <span data-ttu-id="a28f5-448">ei</span><span class="sxs-lookup"><span data-stu-id="a28f5-448">no</span></span>           |

### <a name="project-team-member"></a><span data-ttu-id="a28f5-449">Projektiryhmän jäsen</span><span class="sxs-lookup"><span data-stu-id="a28f5-449">Project team member</span></span>

| <span data-ttu-id="a28f5-450">**Looginen nimi**</span><span class="sxs-lookup"><span data-stu-id="a28f5-450">**Logical name**</span></span>                                 | <span data-ttu-id="a28f5-451">**Voidaan luoda**</span><span class="sxs-lookup"><span data-stu-id="a28f5-451">**Can create**</span></span> | <span data-ttu-id="a28f5-452">**Voidaan muokata**</span><span class="sxs-lookup"><span data-stu-id="a28f5-452">**Can edit**</span></span> |
|--------------------------------------------------|----------------|--------------|
| <span data-ttu-id="a28f5-453">msdyn_calendarid</span><span class="sxs-lookup"><span data-stu-id="a28f5-453">msdyn_calendarid</span></span>                                 | <span data-ttu-id="a28f5-454">ei</span><span class="sxs-lookup"><span data-stu-id="a28f5-454">no</span></span>             | <span data-ttu-id="a28f5-455">ei</span><span class="sxs-lookup"><span data-stu-id="a28f5-455">no</span></span>           |
| <span data-ttu-id="a28f5-456">msdyn_creategenericteammemberwithrequirementname</span><span class="sxs-lookup"><span data-stu-id="a28f5-456">msdyn_creategenericteammemberwithrequirementname</span></span> | <span data-ttu-id="a28f5-457">ei</span><span class="sxs-lookup"><span data-stu-id="a28f5-457">no</span></span>             | <span data-ttu-id="a28f5-458">ei</span><span class="sxs-lookup"><span data-stu-id="a28f5-458">no</span></span>           |
| <span data-ttu-id="a28f5-459">msdyn_deletestatus</span><span class="sxs-lookup"><span data-stu-id="a28f5-459">msdyn_deletestatus</span></span>                               | <span data-ttu-id="a28f5-460">ei</span><span class="sxs-lookup"><span data-stu-id="a28f5-460">no</span></span>             | <span data-ttu-id="a28f5-461">ei</span><span class="sxs-lookup"><span data-stu-id="a28f5-461">no</span></span>           |
| <span data-ttu-id="a28f5-462">msdyn_deletestatusname</span><span class="sxs-lookup"><span data-stu-id="a28f5-462">msdyn_deletestatusname</span></span>                           | <span data-ttu-id="a28f5-463">ei</span><span class="sxs-lookup"><span data-stu-id="a28f5-463">no</span></span>             | <span data-ttu-id="a28f5-464">ei</span><span class="sxs-lookup"><span data-stu-id="a28f5-464">no</span></span>           |
| <span data-ttu-id="a28f5-465">msdyn_effort</span><span class="sxs-lookup"><span data-stu-id="a28f5-465">msdyn_effort</span></span>                                     | <span data-ttu-id="a28f5-466">ei</span><span class="sxs-lookup"><span data-stu-id="a28f5-466">no</span></span>             | <span data-ttu-id="a28f5-467">ei</span><span class="sxs-lookup"><span data-stu-id="a28f5-467">no</span></span>           |
| <span data-ttu-id="a28f5-468">msdyn_effortcompleted</span><span class="sxs-lookup"><span data-stu-id="a28f5-468">msdyn_effortcompleted</span></span>                            | <span data-ttu-id="a28f5-469">ei</span><span class="sxs-lookup"><span data-stu-id="a28f5-469">no</span></span>             | <span data-ttu-id="a28f5-470">ei</span><span class="sxs-lookup"><span data-stu-id="a28f5-470">no</span></span>           |
| <span data-ttu-id="a28f5-471">msdyn_effortremaining</span><span class="sxs-lookup"><span data-stu-id="a28f5-471">msdyn_effortremaining</span></span>                            | <span data-ttu-id="a28f5-472">ei</span><span class="sxs-lookup"><span data-stu-id="a28f5-472">no</span></span>             | <span data-ttu-id="a28f5-473">ei</span><span class="sxs-lookup"><span data-stu-id="a28f5-473">no</span></span>           |
| <span data-ttu-id="a28f5-474">msdyn_finish</span><span class="sxs-lookup"><span data-stu-id="a28f5-474">msdyn_finish</span></span>                                     | <span data-ttu-id="a28f5-475">ei</span><span class="sxs-lookup"><span data-stu-id="a28f5-475">no</span></span>             | <span data-ttu-id="a28f5-476">ei</span><span class="sxs-lookup"><span data-stu-id="a28f5-476">no</span></span>           |
| <span data-ttu-id="a28f5-477">msdyn_hardbookedhours</span><span class="sxs-lookup"><span data-stu-id="a28f5-477">msdyn_hardbookedhours</span></span>                            | <span data-ttu-id="a28f5-478">ei</span><span class="sxs-lookup"><span data-stu-id="a28f5-478">no</span></span>             | <span data-ttu-id="a28f5-479">ei</span><span class="sxs-lookup"><span data-stu-id="a28f5-479">no</span></span>           |
| <span data-ttu-id="a28f5-480">msdyn_hours</span><span class="sxs-lookup"><span data-stu-id="a28f5-480">msdyn_hours</span></span>                                      | <span data-ttu-id="a28f5-481">ei</span><span class="sxs-lookup"><span data-stu-id="a28f5-481">no</span></span>             | <span data-ttu-id="a28f5-482">ei</span><span class="sxs-lookup"><span data-stu-id="a28f5-482">no</span></span>           |
| <span data-ttu-id="a28f5-483">msdyn_markedfordeletiontimer</span><span class="sxs-lookup"><span data-stu-id="a28f5-483">msdyn_markedfordeletiontimer</span></span>                     | <span data-ttu-id="a28f5-484">ei</span><span class="sxs-lookup"><span data-stu-id="a28f5-484">no</span></span>             | <span data-ttu-id="a28f5-485">ei</span><span class="sxs-lookup"><span data-stu-id="a28f5-485">no</span></span>           |
| <span data-ttu-id="a28f5-486">msdyn_markedfordeletiontimestamp</span><span class="sxs-lookup"><span data-stu-id="a28f5-486">msdyn_markedfordeletiontimestamp</span></span>                 | <span data-ttu-id="a28f5-487">ei</span><span class="sxs-lookup"><span data-stu-id="a28f5-487">no</span></span>             | <span data-ttu-id="a28f5-488">ei</span><span class="sxs-lookup"><span data-stu-id="a28f5-488">no</span></span>           |
| <span data-ttu-id="a28f5-489">msdyn_msprojectclientid</span><span class="sxs-lookup"><span data-stu-id="a28f5-489">msdyn_msprojectclientid</span></span>                          | <span data-ttu-id="a28f5-490">ei</span><span class="sxs-lookup"><span data-stu-id="a28f5-490">no</span></span>             | <span data-ttu-id="a28f5-491">ei</span><span class="sxs-lookup"><span data-stu-id="a28f5-491">no</span></span>           |
| <span data-ttu-id="a28f5-492">msdyn_percentage</span><span class="sxs-lookup"><span data-stu-id="a28f5-492">msdyn_percentage</span></span>                                 | <span data-ttu-id="a28f5-493">ei</span><span class="sxs-lookup"><span data-stu-id="a28f5-493">no</span></span>             | <span data-ttu-id="a28f5-494">ei</span><span class="sxs-lookup"><span data-stu-id="a28f5-494">no</span></span>           |
| <span data-ttu-id="a28f5-495">msdyn_requiredhours</span><span class="sxs-lookup"><span data-stu-id="a28f5-495">msdyn_requiredhours</span></span>                              | <span data-ttu-id="a28f5-496">ei</span><span class="sxs-lookup"><span data-stu-id="a28f5-496">no</span></span>             | <span data-ttu-id="a28f5-497">ei</span><span class="sxs-lookup"><span data-stu-id="a28f5-497">no</span></span>           |
| <span data-ttu-id="a28f5-498">msdyn_softbookedhours</span><span class="sxs-lookup"><span data-stu-id="a28f5-498">msdyn_softbookedhours</span></span>                            | <span data-ttu-id="a28f5-499">ei</span><span class="sxs-lookup"><span data-stu-id="a28f5-499">no</span></span>             | <span data-ttu-id="a28f5-500">ei</span><span class="sxs-lookup"><span data-stu-id="a28f5-500">no</span></span>           |
| <span data-ttu-id="a28f5-501">msdyn_start</span><span class="sxs-lookup"><span data-stu-id="a28f5-501">msdyn_start</span></span>                                      | <span data-ttu-id="a28f5-502">ei</span><span class="sxs-lookup"><span data-stu-id="a28f5-502">no</span></span>             | <span data-ttu-id="a28f5-503">ei</span><span class="sxs-lookup"><span data-stu-id="a28f5-503">no</span></span>           |

### <a name="project"></a><span data-ttu-id="a28f5-504">Project</span><span class="sxs-lookup"><span data-stu-id="a28f5-504">Project</span></span>

| <span data-ttu-id="a28f5-505">**Looginen nimi**</span><span class="sxs-lookup"><span data-stu-id="a28f5-505">**Logical name**</span></span>                       | <span data-ttu-id="a28f5-506">**Voidaan luoda**</span><span class="sxs-lookup"><span data-stu-id="a28f5-506">**Can create**</span></span> | <span data-ttu-id="a28f5-507">**Voidaan muokata**</span><span class="sxs-lookup"><span data-stu-id="a28f5-507">**Can edit**</span></span> |
|----------------------------------------|----------------|--------------|
| <span data-ttu-id="a28f5-508">msdyn_actualexpensecost</span><span class="sxs-lookup"><span data-stu-id="a28f5-508">msdyn_actualexpensecost</span></span>                | <span data-ttu-id="a28f5-509">ei</span><span class="sxs-lookup"><span data-stu-id="a28f5-509">no</span></span>             | <span data-ttu-id="a28f5-510">ei</span><span class="sxs-lookup"><span data-stu-id="a28f5-510">no</span></span>           |
| <span data-ttu-id="a28f5-511">msdyn_actualexpensecost_base</span><span class="sxs-lookup"><span data-stu-id="a28f5-511">msdyn_actualexpensecost_base</span></span>           | <span data-ttu-id="a28f5-512">ei</span><span class="sxs-lookup"><span data-stu-id="a28f5-512">no</span></span>             | <span data-ttu-id="a28f5-513">ei</span><span class="sxs-lookup"><span data-stu-id="a28f5-513">no</span></span>           |
| <span data-ttu-id="a28f5-514">msdyn_actuallaborcost</span><span class="sxs-lookup"><span data-stu-id="a28f5-514">msdyn_actuallaborcost</span></span>                  | <span data-ttu-id="a28f5-515">ei</span><span class="sxs-lookup"><span data-stu-id="a28f5-515">no</span></span>             | <span data-ttu-id="a28f5-516">ei</span><span class="sxs-lookup"><span data-stu-id="a28f5-516">no</span></span>           |
| <span data-ttu-id="a28f5-517">msdyn_actuallaborcost_base</span><span class="sxs-lookup"><span data-stu-id="a28f5-517">msdyn_actuallaborcost_base</span></span>             | <span data-ttu-id="a28f5-518">ei</span><span class="sxs-lookup"><span data-stu-id="a28f5-518">no</span></span>             | <span data-ttu-id="a28f5-519">ei</span><span class="sxs-lookup"><span data-stu-id="a28f5-519">no</span></span>           |
| <span data-ttu-id="a28f5-520">msdyn_actualsales</span><span class="sxs-lookup"><span data-stu-id="a28f5-520">msdyn_actualsales</span></span>                      | <span data-ttu-id="a28f5-521">ei</span><span class="sxs-lookup"><span data-stu-id="a28f5-521">no</span></span>             | <span data-ttu-id="a28f5-522">ei</span><span class="sxs-lookup"><span data-stu-id="a28f5-522">no</span></span>           |
| <span data-ttu-id="a28f5-523">msdyn_actualsales_base</span><span class="sxs-lookup"><span data-stu-id="a28f5-523">msdyn_actualsales_base</span></span>                 | <span data-ttu-id="a28f5-524">ei</span><span class="sxs-lookup"><span data-stu-id="a28f5-524">no</span></span>             | <span data-ttu-id="a28f5-525">ei</span><span class="sxs-lookup"><span data-stu-id="a28f5-525">no</span></span>           |
| <span data-ttu-id="a28f5-526">msdyn_contractlineproject</span><span class="sxs-lookup"><span data-stu-id="a28f5-526">msdyn_contractlineproject</span></span>              | <span data-ttu-id="a28f5-527">kyllä</span><span class="sxs-lookup"><span data-stu-id="a28f5-527">yes</span></span>            | <span data-ttu-id="a28f5-528">ei</span><span class="sxs-lookup"><span data-stu-id="a28f5-528">no</span></span>           |
| <span data-ttu-id="a28f5-529">msdyn_contractorganizationalunitid</span><span class="sxs-lookup"><span data-stu-id="a28f5-529">msdyn_contractorganizationalunitid</span></span>     | <span data-ttu-id="a28f5-530">kyllä</span><span class="sxs-lookup"><span data-stu-id="a28f5-530">yes</span></span>            | <span data-ttu-id="a28f5-531">ei</span><span class="sxs-lookup"><span data-stu-id="a28f5-531">no</span></span>           |
| <span data-ttu-id="a28f5-532">msdyn_contractorganizationalunitidname</span><span class="sxs-lookup"><span data-stu-id="a28f5-532">msdyn_contractorganizationalunitidname</span></span> | <span data-ttu-id="a28f5-533">kyllä</span><span class="sxs-lookup"><span data-stu-id="a28f5-533">yes</span></span>            | <span data-ttu-id="a28f5-534">ei</span><span class="sxs-lookup"><span data-stu-id="a28f5-534">no</span></span>           |
| <span data-ttu-id="a28f5-535">msdyn_costconsumption</span><span class="sxs-lookup"><span data-stu-id="a28f5-535">msdyn_costconsumption</span></span>                  | <span data-ttu-id="a28f5-536">ei</span><span class="sxs-lookup"><span data-stu-id="a28f5-536">no</span></span>             | <span data-ttu-id="a28f5-537">ei</span><span class="sxs-lookup"><span data-stu-id="a28f5-537">no</span></span>           |
| <span data-ttu-id="a28f5-538">msdyn_costestimateatcomplete</span><span class="sxs-lookup"><span data-stu-id="a28f5-538">msdyn_costestimateatcomplete</span></span>           | <span data-ttu-id="a28f5-539">ei</span><span class="sxs-lookup"><span data-stu-id="a28f5-539">no</span></span>             | <span data-ttu-id="a28f5-540">ei</span><span class="sxs-lookup"><span data-stu-id="a28f5-540">no</span></span>           |
| <span data-ttu-id="a28f5-541">msdyn_costestimateatcomplete_base</span><span class="sxs-lookup"><span data-stu-id="a28f5-541">msdyn_costestimateatcomplete_base</span></span>      | <span data-ttu-id="a28f5-542">ei</span><span class="sxs-lookup"><span data-stu-id="a28f5-542">no</span></span>             | <span data-ttu-id="a28f5-543">ei</span><span class="sxs-lookup"><span data-stu-id="a28f5-543">no</span></span>           |
| <span data-ttu-id="a28f5-544">msdyn_costvariance</span><span class="sxs-lookup"><span data-stu-id="a28f5-544">msdyn_costvariance</span></span>                     | <span data-ttu-id="a28f5-545">ei</span><span class="sxs-lookup"><span data-stu-id="a28f5-545">no</span></span>             | <span data-ttu-id="a28f5-546">ei</span><span class="sxs-lookup"><span data-stu-id="a28f5-546">no</span></span>           |
| <span data-ttu-id="a28f5-547">msdyn_costvariance_base</span><span class="sxs-lookup"><span data-stu-id="a28f5-547">msdyn_costvariance_base</span></span>                | <span data-ttu-id="a28f5-548">ei</span><span class="sxs-lookup"><span data-stu-id="a28f5-548">no</span></span>             | <span data-ttu-id="a28f5-549">ei</span><span class="sxs-lookup"><span data-stu-id="a28f5-549">no</span></span>           |
| <span data-ttu-id="a28f5-550">msdyn_duration</span><span class="sxs-lookup"><span data-stu-id="a28f5-550">msdyn_duration</span></span>                         | <span data-ttu-id="a28f5-551">ei</span><span class="sxs-lookup"><span data-stu-id="a28f5-551">no</span></span>             | <span data-ttu-id="a28f5-552">ei</span><span class="sxs-lookup"><span data-stu-id="a28f5-552">no</span></span>           |
| <span data-ttu-id="a28f5-553">msdyn_effort</span><span class="sxs-lookup"><span data-stu-id="a28f5-553">msdyn_effort</span></span>                           | <span data-ttu-id="a28f5-554">ei</span><span class="sxs-lookup"><span data-stu-id="a28f5-554">no</span></span>             | <span data-ttu-id="a28f5-555">ei</span><span class="sxs-lookup"><span data-stu-id="a28f5-555">no</span></span>           |
| <span data-ttu-id="a28f5-556">msdyn_effortcompleted</span><span class="sxs-lookup"><span data-stu-id="a28f5-556">msdyn_effortcompleted</span></span>                  | <span data-ttu-id="a28f5-557">ei</span><span class="sxs-lookup"><span data-stu-id="a28f5-557">no</span></span>             | <span data-ttu-id="a28f5-558">ei</span><span class="sxs-lookup"><span data-stu-id="a28f5-558">no</span></span>           |
| <span data-ttu-id="a28f5-559">msdyn_effortestimateatcompleteeac</span><span class="sxs-lookup"><span data-stu-id="a28f5-559">msdyn_effortestimateatcompleteeac</span></span>      | <span data-ttu-id="a28f5-560">ei</span><span class="sxs-lookup"><span data-stu-id="a28f5-560">no</span></span>             | <span data-ttu-id="a28f5-561">ei</span><span class="sxs-lookup"><span data-stu-id="a28f5-561">no</span></span>           |
| <span data-ttu-id="a28f5-562">msdyn_effortremaining</span><span class="sxs-lookup"><span data-stu-id="a28f5-562">msdyn_effortremaining</span></span>                  | <span data-ttu-id="a28f5-563">ei</span><span class="sxs-lookup"><span data-stu-id="a28f5-563">no</span></span>             | <span data-ttu-id="a28f5-564">ei</span><span class="sxs-lookup"><span data-stu-id="a28f5-564">no</span></span>           |
| <span data-ttu-id="a28f5-565">msdyn_finish</span><span class="sxs-lookup"><span data-stu-id="a28f5-565">msdyn_finish</span></span>                           | <span data-ttu-id="a28f5-566">kyllä</span><span class="sxs-lookup"><span data-stu-id="a28f5-566">yes</span></span>            | <span data-ttu-id="a28f5-567">kyllä</span><span class="sxs-lookup"><span data-stu-id="a28f5-567">yes</span></span>          |
| <span data-ttu-id="a28f5-568">msdyn_globalrevisiontoken</span><span class="sxs-lookup"><span data-stu-id="a28f5-568">msdyn_globalrevisiontoken</span></span>              | <span data-ttu-id="a28f5-569">ei</span><span class="sxs-lookup"><span data-stu-id="a28f5-569">no</span></span>             | <span data-ttu-id="a28f5-570">ei</span><span class="sxs-lookup"><span data-stu-id="a28f5-570">no</span></span>           |
| <span data-ttu-id="a28f5-571">msdyn_islinkedtomsprojectclient</span><span class="sxs-lookup"><span data-stu-id="a28f5-571">msdyn_islinkedtomsprojectclient</span></span>        | <span data-ttu-id="a28f5-572">ei</span><span class="sxs-lookup"><span data-stu-id="a28f5-572">no</span></span>             | <span data-ttu-id="a28f5-573">ei</span><span class="sxs-lookup"><span data-stu-id="a28f5-573">no</span></span>           |
| <span data-ttu-id="a28f5-574">msdyn_islinkedtomsprojectclientname</span><span class="sxs-lookup"><span data-stu-id="a28f5-574">msdyn_islinkedtomsprojectclientname</span></span>    | <span data-ttu-id="a28f5-575">ei</span><span class="sxs-lookup"><span data-stu-id="a28f5-575">no</span></span>             | <span data-ttu-id="a28f5-576">ei</span><span class="sxs-lookup"><span data-stu-id="a28f5-576">no</span></span>           |
| <span data-ttu-id="a28f5-577">msdyn_linkeddocumenturl</span><span class="sxs-lookup"><span data-stu-id="a28f5-577">msdyn_linkeddocumenturl</span></span>                | <span data-ttu-id="a28f5-578">ei</span><span class="sxs-lookup"><span data-stu-id="a28f5-578">no</span></span>             | <span data-ttu-id="a28f5-579">ei</span><span class="sxs-lookup"><span data-stu-id="a28f5-579">no</span></span>           |
| <span data-ttu-id="a28f5-580">msdyn_msprojectdocument</span><span class="sxs-lookup"><span data-stu-id="a28f5-580">msdyn_msprojectdocument</span></span>                | <span data-ttu-id="a28f5-581">ei</span><span class="sxs-lookup"><span data-stu-id="a28f5-581">no</span></span>             | <span data-ttu-id="a28f5-582">ei</span><span class="sxs-lookup"><span data-stu-id="a28f5-582">no</span></span>           |
| <span data-ttu-id="a28f5-583">msdyn_msprojectdocumentname</span><span class="sxs-lookup"><span data-stu-id="a28f5-583">msdyn_msprojectdocumentname</span></span>            | <span data-ttu-id="a28f5-584">ei</span><span class="sxs-lookup"><span data-stu-id="a28f5-584">no</span></span>             | <span data-ttu-id="a28f5-585">ei</span><span class="sxs-lookup"><span data-stu-id="a28f5-585">no</span></span>           |
| <span data-ttu-id="a28f5-586">msdyn_plannedexpensecost</span><span class="sxs-lookup"><span data-stu-id="a28f5-586">msdyn_plannedexpensecost</span></span>               | <span data-ttu-id="a28f5-587">ei</span><span class="sxs-lookup"><span data-stu-id="a28f5-587">no</span></span>             | <span data-ttu-id="a28f5-588">ei</span><span class="sxs-lookup"><span data-stu-id="a28f5-588">no</span></span>           |
| <span data-ttu-id="a28f5-589">msdyn_plannedexpensecost_base</span><span class="sxs-lookup"><span data-stu-id="a28f5-589">msdyn_plannedexpensecost_base</span></span>          | <span data-ttu-id="a28f5-590">ei</span><span class="sxs-lookup"><span data-stu-id="a28f5-590">no</span></span>             | <span data-ttu-id="a28f5-591">ei</span><span class="sxs-lookup"><span data-stu-id="a28f5-591">no</span></span>           |
| <span data-ttu-id="a28f5-592">msdyn_plannedlaborcost</span><span class="sxs-lookup"><span data-stu-id="a28f5-592">msdyn_plannedlaborcost</span></span>                 | <span data-ttu-id="a28f5-593">ei</span><span class="sxs-lookup"><span data-stu-id="a28f5-593">no</span></span>             | <span data-ttu-id="a28f5-594">ei</span><span class="sxs-lookup"><span data-stu-id="a28f5-594">no</span></span>           |
| <span data-ttu-id="a28f5-595">msdyn_plannedlaborcost_base</span><span class="sxs-lookup"><span data-stu-id="a28f5-595">msdyn_plannedlaborcost_base</span></span>            | <span data-ttu-id="a28f5-596">ei</span><span class="sxs-lookup"><span data-stu-id="a28f5-596">no</span></span>             | <span data-ttu-id="a28f5-597">ei</span><span class="sxs-lookup"><span data-stu-id="a28f5-597">no</span></span>           |
| <span data-ttu-id="a28f5-598">msdyn_plannedsales</span><span class="sxs-lookup"><span data-stu-id="a28f5-598">msdyn_plannedsales</span></span>                     | <span data-ttu-id="a28f5-599">ei</span><span class="sxs-lookup"><span data-stu-id="a28f5-599">no</span></span>             | <span data-ttu-id="a28f5-600">ei</span><span class="sxs-lookup"><span data-stu-id="a28f5-600">no</span></span>           |
| <span data-ttu-id="a28f5-601">msdyn_plannedsales_base</span><span class="sxs-lookup"><span data-stu-id="a28f5-601">msdyn_plannedsales_base</span></span>                | <span data-ttu-id="a28f5-602">ei</span><span class="sxs-lookup"><span data-stu-id="a28f5-602">no</span></span>             | <span data-ttu-id="a28f5-603">ei</span><span class="sxs-lookup"><span data-stu-id="a28f5-603">no</span></span>           |
| <span data-ttu-id="a28f5-604">msdyn_progress</span><span class="sxs-lookup"><span data-stu-id="a28f5-604">msdyn_progress</span></span>                         | <span data-ttu-id="a28f5-605">ei</span><span class="sxs-lookup"><span data-stu-id="a28f5-605">no</span></span>             | <span data-ttu-id="a28f5-606">ei</span><span class="sxs-lookup"><span data-stu-id="a28f5-606">no</span></span>           |
| <span data-ttu-id="a28f5-607">msdyn_remainingcost</span><span class="sxs-lookup"><span data-stu-id="a28f5-607">msdyn_remainingcost</span></span>                    | <span data-ttu-id="a28f5-608">ei</span><span class="sxs-lookup"><span data-stu-id="a28f5-608">no</span></span>             | <span data-ttu-id="a28f5-609">ei</span><span class="sxs-lookup"><span data-stu-id="a28f5-609">no</span></span>           |
| <span data-ttu-id="a28f5-610">msdyn_remainingcost_base</span><span class="sxs-lookup"><span data-stu-id="a28f5-610">msdyn_remainingcost_base</span></span>               | <span data-ttu-id="a28f5-611">ei</span><span class="sxs-lookup"><span data-stu-id="a28f5-611">no</span></span>             | <span data-ttu-id="a28f5-612">ei</span><span class="sxs-lookup"><span data-stu-id="a28f5-612">no</span></span>           |
| <span data-ttu-id="a28f5-613">msdyn_remainingsales</span><span class="sxs-lookup"><span data-stu-id="a28f5-613">msdyn_remainingsales</span></span>                   | <span data-ttu-id="a28f5-614">ei</span><span class="sxs-lookup"><span data-stu-id="a28f5-614">no</span></span>             | <span data-ttu-id="a28f5-615">ei</span><span class="sxs-lookup"><span data-stu-id="a28f5-615">no</span></span>           |
| <span data-ttu-id="a28f5-616">msdyn_remainingsales_base</span><span class="sxs-lookup"><span data-stu-id="a28f5-616">msdyn_remainingsales_base</span></span>              | <span data-ttu-id="a28f5-617">ei</span><span class="sxs-lookup"><span data-stu-id="a28f5-617">no</span></span>             | <span data-ttu-id="a28f5-618">ei</span><span class="sxs-lookup"><span data-stu-id="a28f5-618">no</span></span>           |
| <span data-ttu-id="a28f5-619">msdyn_replaylogheader</span><span class="sxs-lookup"><span data-stu-id="a28f5-619">msdyn_replaylogheader</span></span>                  | <span data-ttu-id="a28f5-620">ei</span><span class="sxs-lookup"><span data-stu-id="a28f5-620">no</span></span>             | <span data-ttu-id="a28f5-621">ei</span><span class="sxs-lookup"><span data-stu-id="a28f5-621">no</span></span>           |
| <span data-ttu-id="a28f5-622">msdyn_salesconsumption</span><span class="sxs-lookup"><span data-stu-id="a28f5-622">msdyn_salesconsumption</span></span>                 | <span data-ttu-id="a28f5-623">ei</span><span class="sxs-lookup"><span data-stu-id="a28f5-623">no</span></span>             | <span data-ttu-id="a28f5-624">ei</span><span class="sxs-lookup"><span data-stu-id="a28f5-624">no</span></span>           |
| <span data-ttu-id="a28f5-625">msdyn_salesestimateatcompleteeac</span><span class="sxs-lookup"><span data-stu-id="a28f5-625">msdyn_salesestimateatcompleteeac</span></span>       | <span data-ttu-id="a28f5-626">ei</span><span class="sxs-lookup"><span data-stu-id="a28f5-626">no</span></span>             | <span data-ttu-id="a28f5-627">ei</span><span class="sxs-lookup"><span data-stu-id="a28f5-627">no</span></span>           |
| <span data-ttu-id="a28f5-628">msdyn_salesestimateatcompleteeac_base</span><span class="sxs-lookup"><span data-stu-id="a28f5-628">msdyn_salesestimateatcompleteeac_base</span></span>  | <span data-ttu-id="a28f5-629">ei</span><span class="sxs-lookup"><span data-stu-id="a28f5-629">no</span></span>             | <span data-ttu-id="a28f5-630">ei</span><span class="sxs-lookup"><span data-stu-id="a28f5-630">no</span></span>           |
| <span data-ttu-id="a28f5-631">msdyn_salesvariance</span><span class="sxs-lookup"><span data-stu-id="a28f5-631">msdyn_salesvariance</span></span>                    | <span data-ttu-id="a28f5-632">ei</span><span class="sxs-lookup"><span data-stu-id="a28f5-632">no</span></span>             | <span data-ttu-id="a28f5-633">ei</span><span class="sxs-lookup"><span data-stu-id="a28f5-633">no</span></span>           |
| <span data-ttu-id="a28f5-634">msdyn_salesvariance_base</span><span class="sxs-lookup"><span data-stu-id="a28f5-634">msdyn_salesvariance_base</span></span>               | <span data-ttu-id="a28f5-635">ei</span><span class="sxs-lookup"><span data-stu-id="a28f5-635">no</span></span>             | <span data-ttu-id="a28f5-636">ei</span><span class="sxs-lookup"><span data-stu-id="a28f5-636">no</span></span>           |
| <span data-ttu-id="a28f5-637">msdyn_scheduleperformance</span><span class="sxs-lookup"><span data-stu-id="a28f5-637">msdyn_scheduleperformance</span></span>              | <span data-ttu-id="a28f5-638">ei</span><span class="sxs-lookup"><span data-stu-id="a28f5-638">no</span></span>             | <span data-ttu-id="a28f5-639">ei</span><span class="sxs-lookup"><span data-stu-id="a28f5-639">no</span></span>           |
| <span data-ttu-id="a28f5-640">msdyn_scheduleperformancename</span><span class="sxs-lookup"><span data-stu-id="a28f5-640">msdyn_scheduleperformancename</span></span>          | <span data-ttu-id="a28f5-641">ei</span><span class="sxs-lookup"><span data-stu-id="a28f5-641">no</span></span>             | <span data-ttu-id="a28f5-642">ei</span><span class="sxs-lookup"><span data-stu-id="a28f5-642">no</span></span>           |
| <span data-ttu-id="a28f5-643">msdyn_schedulevariance</span><span class="sxs-lookup"><span data-stu-id="a28f5-643">msdyn_schedulevariance</span></span>                 | <span data-ttu-id="a28f5-644">ei</span><span class="sxs-lookup"><span data-stu-id="a28f5-644">no</span></span>             | <span data-ttu-id="a28f5-645">ei</span><span class="sxs-lookup"><span data-stu-id="a28f5-645">no</span></span>           |
| <span data-ttu-id="a28f5-646">msdyn_taskearlieststart</span><span class="sxs-lookup"><span data-stu-id="a28f5-646">msdyn_taskearlieststart</span></span>                | <span data-ttu-id="a28f5-647">ei</span><span class="sxs-lookup"><span data-stu-id="a28f5-647">no</span></span>             | <span data-ttu-id="a28f5-648">ei</span><span class="sxs-lookup"><span data-stu-id="a28f5-648">no</span></span>           |
| <span data-ttu-id="a28f5-649">msdyn_teamsize</span><span class="sxs-lookup"><span data-stu-id="a28f5-649">msdyn_teamsize</span></span>                         | <span data-ttu-id="a28f5-650">ei</span><span class="sxs-lookup"><span data-stu-id="a28f5-650">no</span></span>             | <span data-ttu-id="a28f5-651">ei</span><span class="sxs-lookup"><span data-stu-id="a28f5-651">no</span></span>           |
| <span data-ttu-id="a28f5-652">msdyn_teamsize_date</span><span class="sxs-lookup"><span data-stu-id="a28f5-652">msdyn_teamsize_date</span></span>                    | <span data-ttu-id="a28f5-653">ei</span><span class="sxs-lookup"><span data-stu-id="a28f5-653">no</span></span>             | <span data-ttu-id="a28f5-654">ei</span><span class="sxs-lookup"><span data-stu-id="a28f5-654">no</span></span>           |
| <span data-ttu-id="a28f5-655">msdyn_teamsize_state</span><span class="sxs-lookup"><span data-stu-id="a28f5-655">msdyn_teamsize_state</span></span>                   | <span data-ttu-id="a28f5-656">ei</span><span class="sxs-lookup"><span data-stu-id="a28f5-656">no</span></span>             | <span data-ttu-id="a28f5-657">ei</span><span class="sxs-lookup"><span data-stu-id="a28f5-657">no</span></span>           |
| <span data-ttu-id="a28f5-658">msdyn_totalactualcost</span><span class="sxs-lookup"><span data-stu-id="a28f5-658">msdyn_totalactualcost</span></span>                  | <span data-ttu-id="a28f5-659">ei</span><span class="sxs-lookup"><span data-stu-id="a28f5-659">no</span></span>             | <span data-ttu-id="a28f5-660">ei</span><span class="sxs-lookup"><span data-stu-id="a28f5-660">no</span></span>           |
| <span data-ttu-id="a28f5-661">msdyn_totalactualcost_base</span><span class="sxs-lookup"><span data-stu-id="a28f5-661">msdyn_totalactualcost_base</span></span>             | <span data-ttu-id="a28f5-662">ei</span><span class="sxs-lookup"><span data-stu-id="a28f5-662">no</span></span>             | <span data-ttu-id="a28f5-663">ei</span><span class="sxs-lookup"><span data-stu-id="a28f5-663">no</span></span>           |
| <span data-ttu-id="a28f5-664">msdyn_totalplannedcost</span><span class="sxs-lookup"><span data-stu-id="a28f5-664">msdyn_totalplannedcost</span></span>                 | <span data-ttu-id="a28f5-665">ei</span><span class="sxs-lookup"><span data-stu-id="a28f5-665">no</span></span>             | <span data-ttu-id="a28f5-666">ei</span><span class="sxs-lookup"><span data-stu-id="a28f5-666">no</span></span>           |
| <span data-ttu-id="a28f5-667">msdyn_totalplannedcost_base</span><span class="sxs-lookup"><span data-stu-id="a28f5-667">msdyn_totalplannedcost_base</span></span>            | <span data-ttu-id="a28f5-668">ei</span><span class="sxs-lookup"><span data-stu-id="a28f5-668">no</span></span>             | <span data-ttu-id="a28f5-669">ei</span><span class="sxs-lookup"><span data-stu-id="a28f5-669">no</span></span>           |


## <a name="limitations-and-known-issues"></a><span data-ttu-id="a28f5-670">Rajoitukset ja tunnetut ongelmat</span><span class="sxs-lookup"><span data-stu-id="a28f5-670">Limitations and known issues</span></span>
<span data-ttu-id="a28f5-671">Seuraavassa on luettelo rajoituksista ja tunnetuista ongelmista:</span><span class="sxs-lookup"><span data-stu-id="a28f5-671">The following is a list of limitations and known issues:</span></span>

- <span data-ttu-id="a28f5-672">Aikataulutuksen ohjelmointirajapintoja voivat käyttää vain **käyttäjät, joilla on Microsoft Project -lisenssi.**</span><span class="sxs-lookup"><span data-stu-id="a28f5-672">Schedule APIs can only be used by **Users with Microsoft Project License.**</span></span> <span data-ttu-id="a28f5-673">Niitä eivät voi käyttää:</span><span class="sxs-lookup"><span data-stu-id="a28f5-673">They can't be used by:</span></span>
    - <span data-ttu-id="a28f5-674">Sovelluksen käyttäjät</span><span class="sxs-lookup"><span data-stu-id="a28f5-674">Application users</span></span>
    - <span data-ttu-id="a28f5-675">Järjestelmäkäyttäjät</span><span class="sxs-lookup"><span data-stu-id="a28f5-675">System users</span></span>
    - <span data-ttu-id="a28f5-676">Integrointikäyttäjät</span><span class="sxs-lookup"><span data-stu-id="a28f5-676">Integration users</span></span>
    - <span data-ttu-id="a28f5-677">Muut käyttäjät, joilla ei ole tarvittavaa lisenssiä</span><span class="sxs-lookup"><span data-stu-id="a28f5-677">Other users that don't have the required license</span></span>
- <span data-ttu-id="a28f5-678">Kussakin **OperationSet** issä voi olla enintään 100 toimintoa.</span><span class="sxs-lookup"><span data-stu-id="a28f5-678">Each **OperationSet** can only have a maximum of 100 operations.</span></span>
- <span data-ttu-id="a28f5-679">Kullakin käyttäjällä voi olla enintään 10 avointa **OperationSet** iä.</span><span class="sxs-lookup"><span data-stu-id="a28f5-679">Each user can only have a maximum of 10 open **OperationSets**.</span></span>
- <span data-ttu-id="a28f5-680">Project Operations tukee tällä hetkellä projektissa enintään 500 tehtävää.</span><span class="sxs-lookup"><span data-stu-id="a28f5-680">Project Operations currently supports a maximum of 500 total tasks on a project.</span></span>
- <span data-ttu-id="a28f5-681">**OperationSet**-virheen tila- ja virhelokit eivät ole tällä hetkellä käytettävissä.</span><span class="sxs-lookup"><span data-stu-id="a28f5-681">**OperationSet** failure status and failure logs aren't currently available.</span></span>
- <span data-ttu-id="a28f5-682">Aikataulutuksen ohjelmointirajapinnat ovat julkisessa esiversiossa.</span><span class="sxs-lookup"><span data-stu-id="a28f5-682">Schedule APIs are in Public preview.</span></span> <span data-ttu-id="a28f5-683">Microsoft ei tue näiden ohjelmointirajapintojen käyttöä tuotantoympäristössä.</span><span class="sxs-lookup"><span data-stu-id="a28f5-683">Using these APIs in a Production environment isn't supported by Microsoft.</span></span>
- [<span data-ttu-id="a28f5-684">Projektien ja tehtävien rajoitukset ja rajat</span><span class="sxs-lookup"><span data-stu-id="a28f5-684">Limits and boundaries on projects and tasks</span></span>](/project-for-the-web/project-for-the-web-limits-and-boundaries)

## <a name="error-handling"></a><span data-ttu-id="a28f5-685">Virheen käsittely</span><span class="sxs-lookup"><span data-stu-id="a28f5-685">Error handling</span></span>

   - <span data-ttu-id="a28f5-686">Voit tarkastella toimintojoukoista luotuja virheitä kohdassa **Asetukset** \> **Aikatauluta integrointi** \> **Toimintojoukot**.</span><span class="sxs-lookup"><span data-stu-id="a28f5-686">To review errors generated from the Operation Sets, go to **Settings** \> **Schedule Integration** \> **Operations Sets**.</span></span>
   - <span data-ttu-id="a28f5-687">Voit tarkastella projektin aikataulutuspalvelun luomia virheitä valitsemalla **Asetukset** \> **Aikataulutuksen integrointi** \> **PSS-virhelokit**.</span><span class="sxs-lookup"><span data-stu-id="a28f5-687">To review errors generated from the Project Scheduling Service, go to **Settings** \> **Schedule Integration** \> **PSS Error Logs**.</span></span>

## <a name="sample-scenario"></a><span data-ttu-id="a28f5-688">Näyteskenaario</span><span class="sxs-lookup"><span data-stu-id="a28f5-688">Sample scenario</span></span>

<span data-ttu-id="a28f5-689">Tässä skenaariossa luodaan projekti, ryhmän jäsen, neljä tehtävää ja kaksi resurssivarausta.</span><span class="sxs-lookup"><span data-stu-id="a28f5-689">In this scenario, you will create a project, a team member, four tasks, and two resource assignments.</span></span> <span data-ttu-id="a28f5-690">Seuraavaksi päivität yhden tehtävän, päivität projektin, poistat yhden tehtävän, poistat yhden resurssin määrityksen ja luot riippuvuuden.</span><span class="sxs-lookup"><span data-stu-id="a28f5-690">Next, you will update one task, update the project, delete one task, delete one resource assignment, and create a task dependency.</span></span>

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

## <a name="additional-samples"></a><span data-ttu-id="a28f5-691">Muita näytteitä</span><span class="sxs-lookup"><span data-stu-id="a28f5-691">Additional samples</span></span>

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
