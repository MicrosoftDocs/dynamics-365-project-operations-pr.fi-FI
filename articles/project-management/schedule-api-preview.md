---
title: Aikataulutuksen ohjelmointirajapintojen avulla voit suorittaa toimintoja aikataulutusentiteettien kanssa
description: Tässä aiheessa on tietoja ja esimerkkejä aikataulun ohjelmointirajapintojen käyttämisestä.
author: sigitac
manager: Annbe
ms.date: 04/07/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: a50a2c6220bb49de8146d0758019827e120e0526
ms.sourcegitcommit: 8ff9fe396db6dec581c21cd6bb9acc2691c815b0
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/07/2021
ms.locfileid: "5868125"
---
# <a name="use-schedule-apis-to-perform-operations-with-scheduling-entities"></a><span data-ttu-id="29a1d-103">Aikataulutuksen ohjelmointirajapintojen avulla voit suorittaa toimintoja aikataulutusentiteettien kanssa</span><span class="sxs-lookup"><span data-stu-id="29a1d-103">Use Schedule APIs to perform operations with Scheduling entities</span></span>

<span data-ttu-id="29a1d-104">_**Koskee:** Project Operationsin resurssiin / muuhun kuin resurssiin perustuvia skenaarioita, Lite-käyttöönotto-kaupasta proformalaskutukseen_</span><span class="sxs-lookup"><span data-stu-id="29a1d-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

> [!IMPORTANT] 
> <span data-ttu-id="29a1d-105">Kaikki tai osa tässä aiheessa käsitellyistä toiminnoista ovat saatavilla esiversiojulkaisun osana.</span><span class="sxs-lookup"><span data-stu-id="29a1d-105">Some or all of the functionality noted in this topic is available as part of a preview release.</span></span> <span data-ttu-id="29a1d-106">Sisältö ja toiminnot voivat muuttua.</span><span class="sxs-lookup"><span data-stu-id="29a1d-106">The content and the functionality are subject to change.</span></span> 

## <a name="scheduling-entities"></a><span data-ttu-id="29a1d-107">Aikataulutusentiteetit</span><span class="sxs-lookup"><span data-stu-id="29a1d-107">Scheduling entities</span></span>

<span data-ttu-id="29a1d-108">Aikatalujen ohjelmointirajapinnat antavat mahdollisuuden luoda, päivittää ja poistaa toimintoja **Eikataulutusentiteettien** avulla.</span><span class="sxs-lookup"><span data-stu-id="29a1d-108">Schedule APIs provide the ability to perform create, update, and delete operations with **Scheduling entities**.</span></span> <span data-ttu-id="29a1d-109">Näitä entiteettejä hallitaan verkkopohjaisessa Projectissa aikataulutusytimen kautta.</span><span class="sxs-lookup"><span data-stu-id="29a1d-109">These entities are managed through the Scheduling engine in Project for the web.</span></span> <span data-ttu-id="29a1d-110">Luonti-, päivitys- ja poisto-operaatioita **Aikataulutusentiteettien avulla** rajoitettiin aiemmissa Dynamics 365 Project Operations -julkaisuissa.</span><span class="sxs-lookup"><span data-stu-id="29a1d-110">Create, update, and delete operations with **Scheduling entities** were restricted in earlier Dynamics 365 Project Operations releases.</span></span>

<span data-ttu-id="29a1d-111">Seuraavassa taulukossa on täydellinen luettelo **Aikataulutusentiteeteistä**.</span><span class="sxs-lookup"><span data-stu-id="29a1d-111">The following table provides a full list of the **Scheduling entities**.</span></span>

| <span data-ttu-id="29a1d-112">Entiteetin nimi</span><span class="sxs-lookup"><span data-stu-id="29a1d-112">Entity name</span></span>  | <span data-ttu-id="29a1d-113">Entiteetin looginen nimi</span><span class="sxs-lookup"><span data-stu-id="29a1d-113">Entity logical name</span></span> |
| --- | --- |
| <span data-ttu-id="29a1d-114">Project</span><span class="sxs-lookup"><span data-stu-id="29a1d-114">Project</span></span> | <span data-ttu-id="29a1d-115">msdyn_project</span><span class="sxs-lookup"><span data-stu-id="29a1d-115">msdyn_project</span></span> |
| <span data-ttu-id="29a1d-116">Projektin tehtävä</span><span class="sxs-lookup"><span data-stu-id="29a1d-116">Project Task</span></span>  | <span data-ttu-id="29a1d-117">msdyn_projecttask</span><span class="sxs-lookup"><span data-stu-id="29a1d-117">msdyn_projecttask</span></span>  |
| <span data-ttu-id="29a1d-118">Projektitehtävän riippuvuus</span><span class="sxs-lookup"><span data-stu-id="29a1d-118">Project Task Dependency</span></span>  | <span data-ttu-id="29a1d-119">msdyn_projecttaskdependency</span><span class="sxs-lookup"><span data-stu-id="29a1d-119">msdyn_projecttaskdependency</span></span>  |
| <span data-ttu-id="29a1d-120">Resurssien delegointi</span><span class="sxs-lookup"><span data-stu-id="29a1d-120">Resource Assignment</span></span> | <span data-ttu-id="29a1d-121">msdyn_resourceassignment</span><span class="sxs-lookup"><span data-stu-id="29a1d-121">msdyn_resourceassignment</span></span> |
| <span data-ttu-id="29a1d-122">Projektin joukko</span><span class="sxs-lookup"><span data-stu-id="29a1d-122">Project Bucket</span></span>  | <span data-ttu-id="29a1d-123">msdyn_projectbucket</span><span class="sxs-lookup"><span data-stu-id="29a1d-123">msdyn_projectbucket</span></span> |
| <span data-ttu-id="29a1d-124">Projektiryhmän jäsen</span><span class="sxs-lookup"><span data-stu-id="29a1d-124">Project Team Member</span></span> | <span data-ttu-id="29a1d-125">msdyn_projectteam</span><span class="sxs-lookup"><span data-stu-id="29a1d-125">msdyn_projectteam</span></span> |

## <a name="operationset"></a><span data-ttu-id="29a1d-126">OperationSet</span><span class="sxs-lookup"><span data-stu-id="29a1d-126">OperationSet</span></span>

<span data-ttu-id="29a1d-127">OperationSet on työyksikkörakenne, jota voidaan käyttää, kun useita aikatauluihin vaikuttavia pyyntöjä on käsiteltävä tapahtumassa.</span><span class="sxs-lookup"><span data-stu-id="29a1d-127">OperationSet is a unit-of-work pattern that can be used when several schedule impacting requests must be processed within a transaction.</span></span>

## <a name="schedule-apis"></a><span data-ttu-id="29a1d-128">Aikataulutuksen ohjelmointirajapinnat</span><span class="sxs-lookup"><span data-stu-id="29a1d-128">Schedule APIs</span></span>

<span data-ttu-id="29a1d-129">Seuraavassa on luettelo nykyisistä aikataulun ohjelmointirajapinnoista.</span><span class="sxs-lookup"><span data-stu-id="29a1d-129">The following is a list of current Schedule APIs.</span></span>

- <span data-ttu-id="29a1d-130">**msdyn_CreateProjectV1**: Tämän ohjelmointirajapinnan avulla voidaan luoda projekti.</span><span class="sxs-lookup"><span data-stu-id="29a1d-130">**msdyn_CreateProjectV1**: This API can be used to create a project.</span></span> <span data-ttu-id="29a1d-131">Projekti ja projektin oletussäilö luodaan heti.</span><span class="sxs-lookup"><span data-stu-id="29a1d-131">The project and default project bucket is created immediately.</span></span>
- <span data-ttu-id="29a1d-132">**msdyn_CreateTeamMemberV1**: Tämän ohjelmointirajapinnan avulla voidaan luoda projektiryhmän jäsen.</span><span class="sxs-lookup"><span data-stu-id="29a1d-132">**msdyn_CreateTeamMemberV1**: This API can be used to create a project team member.</span></span> <span data-ttu-id="29a1d-133">Ryhmän jäsentietue luodaan heti.</span><span class="sxs-lookup"><span data-stu-id="29a1d-133">The team member record is created immediately.</span></span>
- <span data-ttu-id="29a1d-134">**msdyn_CreateOperationSetV1**: Tämän ohjelmointirajapinnan avulla voidaan aikatauluttaa useita pyyntöjä, jotka on suoritettava tapahtumassa.</span><span class="sxs-lookup"><span data-stu-id="29a1d-134">**msdyn_CreateOperationSetV1**: This API can be used to schedule several requests that must be performed within a transaction.</span></span>
- <span data-ttu-id="29a1d-135">**msdyn_PSSCreateV1**: Tämän ohjelmointirajapinnan avulla voidaan luoda entiteetti.</span><span class="sxs-lookup"><span data-stu-id="29a1d-135">**msdyn_PSSCreateV1**: This API can be used to create an entity.</span></span> <span data-ttu-id="29a1d-136">Entiteetti voi olla mikä tahansa luontitoimintoa tukeva aikataulutusentiteetti.</span><span class="sxs-lookup"><span data-stu-id="29a1d-136">The entity can be any of the Scheduling entities that support the create operation.</span></span>
- <span data-ttu-id="29a1d-137">**msdyn_PSSUpdateV1**: Tämän ohjelmointirajapinnan avulla voidaan päivittää entiteetti.</span><span class="sxs-lookup"><span data-stu-id="29a1d-137">**msdyn_PSSUpdateV1**: This API can be used to update an entity.</span></span> <span data-ttu-id="29a1d-138">Entiteetti voi olla mikä tahansa päivitystoimintoa tukeva aikataulutusentiteetti.</span><span class="sxs-lookup"><span data-stu-id="29a1d-138">The entity can be any of the Scheduling entities that support the update operation.</span></span>
- <span data-ttu-id="29a1d-139">**msdyn_PSSDeleteV1**: Tämän ohjelmointirajapinnan avulla voidaan poistaa entiteetti.</span><span class="sxs-lookup"><span data-stu-id="29a1d-139">**msdyn_PSSDeleteV1**: This API can be used to delete an entity.</span></span> <span data-ttu-id="29a1d-140">Entiteetti voi olla mikä tahansa poistotoimintoa tukeva aikataulutusentiteetti.</span><span class="sxs-lookup"><span data-stu-id="29a1d-140">The entity can be any of the Scheduling entities that support the delete operation.</span></span>
- <span data-ttu-id="29a1d-141">**msdyn_ExecuteOperationSetV1**: Tämän ohjelmointirajapinnan avulla suoritetaan kaikki toiminnot tietyn toimintojoukon sisällä.</span><span class="sxs-lookup"><span data-stu-id="29a1d-141">**msdyn_ExecuteOperationSetV1**: This API is used to execute all of the operations within the given operation set.</span></span>

## <a name="using-schedule-apis-with-operationset"></a><span data-ttu-id="29a1d-142">Aikataulutuksen ohjelmointirajapintojen käyttäminen OperationSetin kanssa</span><span class="sxs-lookup"><span data-stu-id="29a1d-142">Using Schedule APIs with OperationSet</span></span>

<span data-ttu-id="29a1d-143">Koska tietueet, joissa on sekä **CreateProjectV1** että **CreateTeamMemberV1** luodaan välittömästi, näitä ohjelmointirajapintoja ei voida käyttää suoraan **OperationSet** issä.</span><span class="sxs-lookup"><span data-stu-id="29a1d-143">Because records with both **CreateProjectV1** and **CreateTeamMemberV1** are created immediately, these APIs can't be used in the **OperationSet** directly.</span></span> <span data-ttu-id="29a1d-144">Ohjelmointirajapinnan avulla voit kuitenkin luoda tarvittavat tietueet, luoda **OperationSet** in, ja käyttää sitten näitä aiemmin luotuja tietueita **OperationSet** issä.</span><span class="sxs-lookup"><span data-stu-id="29a1d-144">However, you can use the API to create needed records, create an **OperationSet**, and then use these pre-created records in the **OperationSet**.</span></span>

## <a name="supported-operations"></a><span data-ttu-id="29a1d-145">Tuetut toiminnot</span><span class="sxs-lookup"><span data-stu-id="29a1d-145">Supported operations</span></span>

| <span data-ttu-id="29a1d-146">Aikataulutusentiteetti</span><span class="sxs-lookup"><span data-stu-id="29a1d-146">Scheduling entity</span></span> | <span data-ttu-id="29a1d-147">Luo</span><span class="sxs-lookup"><span data-stu-id="29a1d-147">Create</span></span> | <span data-ttu-id="29a1d-148">Päivitys</span><span class="sxs-lookup"><span data-stu-id="29a1d-148">Update</span></span> | <span data-ttu-id="29a1d-149">Delete</span><span class="sxs-lookup"><span data-stu-id="29a1d-149">Delete</span></span> | <span data-ttu-id="29a1d-150">Tärkeitä huomioon otettavia seikkoja</span><span class="sxs-lookup"><span data-stu-id="29a1d-150">Important considerations</span></span> |
| --- | --- | --- | --- | --- |
<span data-ttu-id="29a1d-151">Projektitehtävä</span><span class="sxs-lookup"><span data-stu-id="29a1d-151">Project task</span></span> | <span data-ttu-id="29a1d-152">Kyllä</span><span class="sxs-lookup"><span data-stu-id="29a1d-152">Yes</span></span> | <span data-ttu-id="29a1d-153">Kyllä</span><span class="sxs-lookup"><span data-stu-id="29a1d-153">Yes</span></span> | <span data-ttu-id="29a1d-154">Kyllä</span><span class="sxs-lookup"><span data-stu-id="29a1d-154">Yes</span></span> | <span data-ttu-id="29a1d-155">Ei ole</span><span class="sxs-lookup"><span data-stu-id="29a1d-155">None</span></span> |
| <span data-ttu-id="29a1d-156">Projektitehtävän riippuvuus</span><span class="sxs-lookup"><span data-stu-id="29a1d-156">Project task dependency</span></span> | <span data-ttu-id="29a1d-157">Kyllä</span><span class="sxs-lookup"><span data-stu-id="29a1d-157">Yes</span></span> | <span data-ttu-id="29a1d-158">Kyllä</span><span class="sxs-lookup"><span data-stu-id="29a1d-158">Yes</span></span> | | <span data-ttu-id="29a1d-159">Projektitehtävän riippuvuustietueita ei päivitetä.</span><span class="sxs-lookup"><span data-stu-id="29a1d-159">Project task dependency records aren't updated.</span></span> <span data-ttu-id="29a1d-160">Sen sijaan voidaan poistaa vanha tietue ja luoda uusi tietue.</span><span class="sxs-lookup"><span data-stu-id="29a1d-160">Instead, an old record can be deleted and a new record can be created.</span></span> |
| <span data-ttu-id="29a1d-161">Resurssien delegointi</span><span class="sxs-lookup"><span data-stu-id="29a1d-161">Resource assignment</span></span> | <span data-ttu-id="29a1d-162">Kyllä</span><span class="sxs-lookup"><span data-stu-id="29a1d-162">Yes</span></span> | <span data-ttu-id="29a1d-163">Kyllä</span><span class="sxs-lookup"><span data-stu-id="29a1d-163">Yes</span></span> | | <span data-ttu-id="29a1d-164">Toimintoja, joilla on seuraavat kentät, ei tueta: **BookableResourceID**, **Effort**, **EffortCompleted**, **EffortRemaining** ja **PlannedWork**.</span><span class="sxs-lookup"><span data-stu-id="29a1d-164">Operations with the following fields aren't supported: **BookableResourceID**, **Effort**, **EffortCompleted**, **EffortRemaining**, and **PlannedWork**.</span></span> <span data-ttu-id="29a1d-165">Resurssien määritystietueita ei päivitetä.</span><span class="sxs-lookup"><span data-stu-id="29a1d-165">Resource assignment records aren't updated.</span></span> <span data-ttu-id="29a1d-166">Sen sijaan voidaan poistaa vanha tietue ja luoda uusi tietue.</span><span class="sxs-lookup"><span data-stu-id="29a1d-166">Instead, the old record can be deleted and a new record can be created.</span></span> |
| <span data-ttu-id="29a1d-167">Projektin säilö</span><span class="sxs-lookup"><span data-stu-id="29a1d-167">Project bucket</span></span> | <span data-ttu-id="29a1d-168">–</span><span class="sxs-lookup"><span data-stu-id="29a1d-168">N/A</span></span> | <span data-ttu-id="29a1d-169">–</span><span class="sxs-lookup"><span data-stu-id="29a1d-169">N/A</span></span> | <span data-ttu-id="29a1d-170">–</span><span class="sxs-lookup"><span data-stu-id="29a1d-170">N/A</span></span> | <span data-ttu-id="29a1d-171">Oletussäilö luodaan **CreateProjectV1** -ohjelmointirajapinnan avulla.</span><span class="sxs-lookup"><span data-stu-id="29a1d-171">The default bucket is created using the **CreateProjectV1** API.</span></span> |
| <span data-ttu-id="29a1d-172">Projektiryhmän jäsen</span><span class="sxs-lookup"><span data-stu-id="29a1d-172">Project team member</span></span> | <span data-ttu-id="29a1d-173">Kyllä</span><span class="sxs-lookup"><span data-stu-id="29a1d-173">Yes</span></span> | <span data-ttu-id="29a1d-174">Kyllä</span><span class="sxs-lookup"><span data-stu-id="29a1d-174">Yes</span></span> | <span data-ttu-id="29a1d-175">Kyllä</span><span class="sxs-lookup"><span data-stu-id="29a1d-175">Yes</span></span> | <span data-ttu-id="29a1d-176">Käytä luontioperaatiolle **CreateTeamMemberV1** -ohjelmointirajapintaa.</span><span class="sxs-lookup"><span data-stu-id="29a1d-176">For the create operation, use the **CreateTeamMemberV1** API.</span></span> |
| <span data-ttu-id="29a1d-177">Project</span><span class="sxs-lookup"><span data-stu-id="29a1d-177">Project</span></span> | <span data-ttu-id="29a1d-178">Kyllä</span><span class="sxs-lookup"><span data-stu-id="29a1d-178">Yes</span></span> | <span data-ttu-id="29a1d-179">Kyllä</span><span class="sxs-lookup"><span data-stu-id="29a1d-179">Yes</span></span> | <span data-ttu-id="29a1d-180">–</span><span class="sxs-lookup"><span data-stu-id="29a1d-180">N/A</span></span> | <span data-ttu-id="29a1d-181">Toimintoja, joilla on seuraavat kentät, ei tueta **StateCode**, **BulkGenerationStatus**, **GlobalRevisionToken**, **CalendarID**, **Effort**, **EffortCompleted**, **EffortRemaining**, **Progress**, **Finish**, **TaskEarliestStart** ja **Duration**.</span><span class="sxs-lookup"><span data-stu-id="29a1d-181">Operations with the following fields aren't supported: **StateCode**, **BulkGenerationStatus**, **GlobalRevisionToken**, **CalendarID**, **Effort**, **EffortCompleted**, **EffortRemaining**, **Progress**, **Finish**, **TaskEarliestStart**, and **Duration**.</span></span> |

<span data-ttu-id="29a1d-182">Näitä ohjelmointirajapintoja voidaan kutsua entiteettiobjekteilla, jotka sisältävät mukautettuja kenttiä.</span><span class="sxs-lookup"><span data-stu-id="29a1d-182">These APIs can be called with entity objects that include custom fields.</span></span>

<span data-ttu-id="29a1d-183">Tunnusominaisuus on valinnainen.</span><span class="sxs-lookup"><span data-stu-id="29a1d-183">The ID property is optional.</span></span> <span data-ttu-id="29a1d-184">Jos se on annettu, järjestelmä yrittää käyttää sitä ja antaa poikkeuksen, jos sitä ei voi käyttää.</span><span class="sxs-lookup"><span data-stu-id="29a1d-184">If it's provided, the system attempts to use it and throws an exception if it can't be used.</span></span> <span data-ttu-id="29a1d-185">Jos sitä ei ole annettu, järjestelmä luo sen.</span><span class="sxs-lookup"><span data-stu-id="29a1d-185">If it isn't provided, the system will generate it.</span></span>

## <a name="limitations-and-known-issues"></a><span data-ttu-id="29a1d-186">Rajoitukset ja tunnetut ongelmat</span><span class="sxs-lookup"><span data-stu-id="29a1d-186">Limitations and known issues</span></span>
<span data-ttu-id="29a1d-187">Seuraavassa on luettelo rajoituksista ja tunnetuista ongelmista:</span><span class="sxs-lookup"><span data-stu-id="29a1d-187">The following is a list of limitations and known issues:</span></span>

- <span data-ttu-id="29a1d-188">Aikataulutuksen ohjelmointirajapintoja voivat käyttää vain **käyttäjät, joilla on Microsoft Project -lisenssi.**</span><span class="sxs-lookup"><span data-stu-id="29a1d-188">Schedule APIs can only be used by **Users with Microsoft Project License.**</span></span> <span data-ttu-id="29a1d-189">Niitä eivät voi käyttää:</span><span class="sxs-lookup"><span data-stu-id="29a1d-189">They can't be used by:</span></span>
    - <span data-ttu-id="29a1d-190">Sovelluksen käyttäjät</span><span class="sxs-lookup"><span data-stu-id="29a1d-190">Application users</span></span>
    - <span data-ttu-id="29a1d-191">Järjestelmäkäyttäjät</span><span class="sxs-lookup"><span data-stu-id="29a1d-191">System users</span></span>
    - <span data-ttu-id="29a1d-192">Integrointikäyttäjät</span><span class="sxs-lookup"><span data-stu-id="29a1d-192">Integration users</span></span>
    - <span data-ttu-id="29a1d-193">Muut käyttäjät, joilla ei ole tarvittavaa lisenssiä</span><span class="sxs-lookup"><span data-stu-id="29a1d-193">Other users that don't have the required license</span></span>
- <span data-ttu-id="29a1d-194">Kussakin **OperationSet** issä voi olla enintään 100 toimintoa.</span><span class="sxs-lookup"><span data-stu-id="29a1d-194">Each **OperationSet** can only have a maximum of 100 operations.</span></span>
- <span data-ttu-id="29a1d-195">Kullakin käyttäjällä voi olla enintään 10 avointa **OperationSet** iä.</span><span class="sxs-lookup"><span data-stu-id="29a1d-195">Each user can only have a maximum of 10 open **OperationSets**.</span></span>
- <span data-ttu-id="29a1d-196">Project Operations tukee tällä hetkellä projektissa enintään 500 tehtävää.</span><span class="sxs-lookup"><span data-stu-id="29a1d-196">Project Operations currently supports a maximum of 500 total tasks on a project.</span></span>
- <span data-ttu-id="29a1d-197">**OperationSet**-virheen tila- ja virhelokit eivät ole tällä hetkellä käytettävissä.</span><span class="sxs-lookup"><span data-stu-id="29a1d-197">**OperationSet** failure status and failure logs aren't currently available.</span></span>
- <span data-ttu-id="29a1d-198">Aikataulutuksen ohjelmointirajapinnat ovat julkisessa esiversiossa.</span><span class="sxs-lookup"><span data-stu-id="29a1d-198">Schedule APIs are in Public preview.</span></span> <span data-ttu-id="29a1d-199">Microsoft ei tue näiden ohjelmointirajapintojen käyttöä tuotantoympäristössä.</span><span class="sxs-lookup"><span data-stu-id="29a1d-199">Using these APIs in a Production environment isn't supported by Microsoft.</span></span>

## <a name="sample-scenario"></a><span data-ttu-id="29a1d-200">Näyteskenaario</span><span class="sxs-lookup"><span data-stu-id="29a1d-200">Sample scenario</span></span>

<span data-ttu-id="29a1d-201">Tässä skenaariossa luodaan projekti, ryhmän jäsen, neljä tehtävää ja kaksi resurssivarausta.</span><span class="sxs-lookup"><span data-stu-id="29a1d-201">In this scenario, you will create a project, a team member, four tasks, and two resource assignments.</span></span> <span data-ttu-id="29a1d-202">Seuraavaksi päivität yhden tehtävän, päivität projektin, poistat yhden tehtävän, poistat yhden resurssin määrityksen ja luot riippuvuuden.</span><span class="sxs-lookup"><span data-stu-id="29a1d-202">Next, you will update one task, update the project, delete one task, delete one resource assignment, and create a task dependency.</span></span>

```C#
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
var task4 = GetTask("4ZZ";, projectReference);

var assignment1 = GetResourceAssignment("R1", teamMember, task2, project);
var assignment2 = GetResourceAssignment"R2", teamMember, task3, project);

var task1Response = CallPssCreateAction(task1, operationSetId);
var task2Response = CallPssCreateAction(task2, operationSetId);
var task3Response = CallPssCreateAction(task3, operationSetId);
var task4Response = CallPssCreateAction(task4, operationSetId);

varassignment1Response = CallPssCreateAction(assignment1, operationSetId);
varassignment2Response = CallPssCreateAction(assignment2, operationSetId);

task2["msdyn_subject"] = "Updated Task";
var task2UpdateResponse = CallPssUpdateAction(task2, operationSetId);

project["msdyn_subject"] = $"Proj update {DateTime.Now.ToShortTimeString()}";
var projectUpdateResponse = CallPssUpdateAction(project, operationSetId);

var task4DeleteResponse = CallPssDeleteAction(task4.Id.ToString(), task4.LogicalName, operationSetId);

varassignment2DeleteResponse = CallPssDeleteAction(assignment2.Id.ToString(), assignment2.LogicalName, operationSetId);

var dependency1 = GetTaskDependency(project, task2, task3);
var dependency1Response = CallPssCreateAction(dependency1, operationSetId);

CallExecuteOperationSetAction(operationSetId);
Console.WriteLine("Done....");
```

## <a name="additional-samples"></a><span data-ttu-id="29a1d-203">Muita näytteitä</span><span class="sxs-lookup"><span data-stu-id="29a1d-203">Additional samples</span></span>

```C#
#region Call actions 

///<summary>
/// Calls the action to create an operationSet
/// </summary>
/// <paramname="projectId">project id for the operations to be included in this operationSet>/param>
/// <paramname="description">description of this operationSet</param>
/// <returns>operationSet id</returns>
privatestring CallCreateOperationSetAction(Guid projectId, string description)
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
/// <paramname="entity">Task or Resource Assignment</param>
/// <paramname="operationSetId">operationSet id</param>
/// <returns>OperationSetResponse</returns>
private OperationSetResponse CallPssCreateAction(Entity entity, string operationSetId)
{
    OrganizationRequest operationSetRequest = new OrganizationRequest("msdyn_PssCreateV1");
    operationSetRequest["Entity"] = entity;
    operationSetRequest["OperationSetId"] = operationSetId;
    return GetOperationSetResponseFromOrgResponse(organizationService.Execute(operationSetRequest));
}

/// <summary<
/// Calls the action to update an entity, only Task for now
/// </summary>
/// <paramname="entity">Task or Resource Assignment</param>
/// <paramname="operationSetId">operationSet Id</param>
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
/// <summary>
/// <paramname="recordId">Id of the record to be deleted</param>
/// <paramname="entityLogicalName">Entity logical name of the record</param>
/// <paramname="operationSetId">OperationSet Id</param>
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
/// <summary>
/// <paramname="operationSetId">operationSet id</param>
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
/// <paramname="operationSetId">operationSet id</param>
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
/// <paramname="project">Project</param>
/// <returns>project Id</returns>
private Guid CallCreateProjectAction(Entity project)
{
    OrganizationRequest createProjectRequest = new OrganizationRequest("msdyn_CreateProjectV1";
    createProjectRequest["Project"] = project;
    OrganizationResponse response = organizationService.Execute(createProjectRequest);
    var projectId = Guid.Parse((string)response["ProjectId"]);

    return projectId;
}

/// <summary>
/// Calls the action to create a new project team member
/// </summary>
/// <paramname="teamMember">Project team member</param>
/// <returns>project team member Id</returns>
privatestring CallCreateTeamMemberAction(Entity teamMember)
{
    OrganizationRequest request = new OrganizationRequest("msdyn_CreateTeamMemberV1");
    request["TeamMember"] = teamMember;
    OrganizationResponse response = organizationService.Execute(request);
    return (string)response["TeamMemberId"];
}

private OperationSetResponse GetOperationSetResponseFromOrgResponse(OrganizationResponse orgResponse)
{
    return JsonConvert.DeserializeObject><OperationSetResponse>
    ((string)orgResponse.Results["OperationSetResponse";]);
}

private EntityCollection GetDefaultBucket(EntityReference projectReference)
{
    var columnsToFetch = new ColumnSet(";msdyn_project", "msdyn_name");
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
    task["msdyn_effort";] = 4d;
    task["msdyn_scheduledstart"] = DateTime.Today;
    task["msdyn_scheduledend"] = DateTime.Today.AddDays(5);
    task["msdyn_progress"] = 0.34m;
    task["msdyn_start"] = DateTime.Now.AddDays(1);
    task["msdyn_projectbucket"] = GetBucket(projectReference).ToEntityReference();
    task["msdyn_LinkStatus"] = new OptionSetValue(192350000);

    //Custom field handling
    /*
        task["new_custom1"] = "Just my test";
        task[";new_age"] = 98;
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
publicclassOperationSetResponse
{
    [DataMember(Name = "operationSetId")]
    public Guid OperationSetId { get; set; }

    [DataMember(Name = "operationSetDetailId")]
    public Guid OperationSetDetailId { get; set; }

    [DataMember(Name = "operationType")]
    publicstring OperationType { get; set; }

    [DataMember(Name = "recordId")]
    publicstring RecordId { get; set; }

    [DataMember(Name = "correlationId")]
    publicstring CorrelationId { get; set; }
}

#endregion
```
