---
title: Resurssien hallinnan muutokset (Project Service Automation 3.x)
description: Tässä aiheessa on tietoja resurssien hallinnan muutoksista.
author: makk
ms.custom:
- dyn365-projectservice
ms.date: 03/18/2019
ms.topic: article
ms.author: makk
audience: admin
search.audienceType:
- admin
- customizer
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: e888d55b93c40e08e51bd4480853fec37f2b6333
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/10/2021
ms.locfileid: "6007812"
---
# <a name="resource-management-changes-project-service-automation-3x"></a><span data-ttu-id="31f47-103">Resurssien hallinnan muutokset (Project Service Automation 3.x)</span><span class="sxs-lookup"><span data-stu-id="31f47-103">Resource management changes (Project Service Automation 3.x)</span></span>

[!include [banner](../../includes/psa-now-project-operations.md)]

<span data-ttu-id="31f47-104">Tämän aiheen osissa on tietoja muutoksista, joita on tehty resurssien hallinnan alueelle Dynamics 365 Project Service Automation versiossa 3. x.</span><span class="sxs-lookup"><span data-stu-id="31f47-104">The sections of this topic provide information about the changes that have been made to the Resource management area of Dynamics 365 Project Service Automation version 3.x.</span></span>

## <a name="project-estimates"></a><span data-ttu-id="31f47-105">Projektin arviot</span><span class="sxs-lookup"><span data-stu-id="31f47-105">Project estimates</span></span>

<span data-ttu-id="31f47-106">Sen sijaan, että perustuisivat **msdyn\_projecttask** -entiteettiin (**Projektitehtävä**), projektin arviot perustuvat **msdyn\_resourceassignment** -entiteettiin (**Resurssin kohdentaminent**).</span><span class="sxs-lookup"><span data-stu-id="31f47-106">Instead of being based on the **msdyn\_projecttask** entity (**Project Task**), project estimates are based on the **msdyn\_resourceassignment** entity (**Resource Assignment**).</span></span> <span data-ttu-id="31f47-107">Resurssien kohdennuksista on tullut "totuuden lähde" tehtävien aikatauluttamista ja hinnoittelua varten.</span><span class="sxs-lookup"><span data-stu-id="31f47-107">Resource assignments have become the "source of truth" for task scheduling and pricing.</span></span>

## <a name="line-tasks"></a><span data-ttu-id="31f47-108">Rivitehtävät</span><span class="sxs-lookup"><span data-stu-id="31f47-108">Line tasks</span></span>

<span data-ttu-id="31f47-109">PSA 3. x:ssä rivitehtävät ovat vanhentuneet (vanhentunut).</span><span class="sxs-lookup"><span data-stu-id="31f47-109">In PSA 3.x, line tasks are obsolete (deprecated).</span></span> <span data-ttu-id="31f47-110">Määritykset osoittavat nyt koko tehtävään rivitehtävien sijaan.</span><span class="sxs-lookup"><span data-stu-id="31f47-110">Assignments now point to the whole task instead of the line tasks.</span></span>

<span data-ttu-id="31f47-111">Seuraavasta esimerkistä näkyy, miten tehtävä, jonka nimi on "Testitehtävä", on määritetty ryhmän jäsenille A ja B PSA:N aiemmissa versioissa ja PSA 3. x:ssä.</span><span class="sxs-lookup"><span data-stu-id="31f47-111">The following example shows how a task that is named "Test task" is assigned to team members A and B in earlier versions of PSA and in PSA 3.x.</span></span>

- <span data-ttu-id="31f47-112">**Ennen PSA 3. x:ää:**</span><span class="sxs-lookup"><span data-stu-id="31f47-112">**Before PSA 3.x:**</span></span>

    - <span data-ttu-id="31f47-113">Testitehtävä</span><span class="sxs-lookup"><span data-stu-id="31f47-113">Test task</span></span>

        - <span data-ttu-id="31f47-114">Testitehtävä – Rivitehtävä 1</span><span class="sxs-lookup"><span data-stu-id="31f47-114">Test task – Line task 1</span></span>

            - <span data-ttu-id="31f47-115">Kohdennus A:lle</span><span class="sxs-lookup"><span data-stu-id="31f47-115">Assignment to A</span></span>

        - <span data-ttu-id="31f47-116">Testitehtävä – Rivitehtävä 2</span><span class="sxs-lookup"><span data-stu-id="31f47-116">Test task – Line task 2</span></span>

            - <span data-ttu-id="31f47-117">Kohdennus B:lle</span><span class="sxs-lookup"><span data-stu-id="31f47-117">Assignment to B</span></span>

- <span data-ttu-id="31f47-118">**PSA 3.x:**</span><span class="sxs-lookup"><span data-stu-id="31f47-118">**PSA 3.x:**</span></span>

    - <span data-ttu-id="31f47-119">Testitehtävä</span><span class="sxs-lookup"><span data-stu-id="31f47-119">Test task</span></span>

        - <span data-ttu-id="31f47-120">Kohdennus A:lle</span><span class="sxs-lookup"><span data-stu-id="31f47-120">Assignment to A</span></span>
        - <span data-ttu-id="31f47-121">Kohdennus B:lle</span><span class="sxs-lookup"><span data-stu-id="31f47-121">Assignment to B</span></span>

## <a name="unassigned-assignment"></a><span data-ttu-id="31f47-122">Kohdentamaton kohdennus</span><span class="sxs-lookup"><span data-stu-id="31f47-122">Unassigned assignment</span></span>

<span data-ttu-id="31f47-123">PSA 3.x:ssä kohdentamaton kohdennus on sellainen kohdennus, joka on kohdennettu ryhmän jäsenelle **NULL** ja resurssille **NULL**.</span><span class="sxs-lookup"><span data-stu-id="31f47-123">In PSA 3.x, an unassigned assignment is an assignment that is assigned to a **NULL** team member and a **NULL** resource.</span></span> <span data-ttu-id="31f47-124">Kohdentamattomia kohdennuksia voi tapahtua muutamissa tapauksissa:</span><span class="sxs-lookup"><span data-stu-id="31f47-124">Unassigned assignments can occur in a couple of scenarios:</span></span>

- <span data-ttu-id="31f47-125">Jos tehtävä on luotu, mutta sitä ei ole vielä kohdennettu millekään ryhmän jäsenelle, kohdentamaton kohdennus luodaan aina.</span><span class="sxs-lookup"><span data-stu-id="31f47-125">If a task has been created, but it hasn't yet been assigned to any team member, an unassigned assignment is always created.</span></span> 
- <span data-ttu-id="31f47-126">Jos kaikki tehtävään kohdennetut henkilöt poistetaan, kohdentamaton kohdennus luodaan uudelleen kyseiselle tehtävälle.</span><span class="sxs-lookup"><span data-stu-id="31f47-126">If all assignees on a task are removed, an unassigned assignment is re-created for that task.</span></span>

## <a name="scheduling-fields-on-the-project-task-entity"></a><span data-ttu-id="31f47-127">Projekti tehtävä -entiteetin aikataulutuskentät</span><span class="sxs-lookup"><span data-stu-id="31f47-127">Scheduling fields on the Project Task entity</span></span>

<span data-ttu-id="31f47-128">Kentät **msdyn\_projecttask**-entiteetissä ovat vanhentuneet tai siirretty **msdyn\_resourceassignment**-entiteettiin, tai niihin viitataan nyt **msdyn\_projectteam**-entiteetissä (**Projektiryhmän jäsen**).</span><span class="sxs-lookup"><span data-stu-id="31f47-128">The fields on the **msdyn\_projecttask** entity have been deprecated or moved to the **msdyn\_resourceassignment** entity, or they are now referenced from the **msdyn\_projectteam** entity (**Project Team Member**).</span></span>

| <span data-ttu-id="31f47-129">Vanhentunut kenttä kohteessa msdyn\_projecttask (Projektitehtävä)</span><span class="sxs-lookup"><span data-stu-id="31f47-129">Deprecated field on msdyn\_projecttask (Project Task)</span></span> | <span data-ttu-id="31f47-130">Uusi kenttä kohteessa msdyn\_resourceassignment (Resurssin kohdennus)</span><span class="sxs-lookup"><span data-stu-id="31f47-130">New field on msdyn\_resourceassignment (Resource Assignment)</span></span> | <span data-ttu-id="31f47-131">Kommentti</span><span class="sxs-lookup"><span data-stu-id="31f47-131">Comment</span></span> |
|---|---|---|
| <span data-ttu-id="31f47-132">msdyn\_assignedresources</span><span class="sxs-lookup"><span data-stu-id="31f47-132">msdyn\_assignedresources</span></span> | <span data-ttu-id="31f47-133">Ei ole</span><span class="sxs-lookup"><span data-stu-id="31f47-133">None</span></span> | |
| <span data-ttu-id="31f47-134">msdyn\_assignedteammembers</span><span class="sxs-lookup"><span data-stu-id="31f47-134">msdyn\_assignedteammembers</span></span> | <span data-ttu-id="31f47-135">Ei ole</span><span class="sxs-lookup"><span data-stu-id="31f47-135">None</span></span> | |
| <span data-ttu-id="31f47-136">msdyn\_numberofresources</span><span class="sxs-lookup"><span data-stu-id="31f47-136">msdyn\_numberofresources</span></span> | <span data-ttu-id="31f47-137">Ei ole</span><span class="sxs-lookup"><span data-stu-id="31f47-137">None</span></span> | |
| <span data-ttu-id="31f47-138">msdyn\_scheduledhours</span><span class="sxs-lookup"><span data-stu-id="31f47-138">msdyn\_scheduledhours</span></span> | <span data-ttu-id="31f47-139">Ei ole</span><span class="sxs-lookup"><span data-stu-id="31f47-139">None</span></span> | |
| <span data-ttu-id="31f47-140">msdyn\_effortcontour</span><span class="sxs-lookup"><span data-stu-id="31f47-140">msdyn\_effortcontour</span></span> | <span data-ttu-id="31f47-141">msdyn\_plannedwork</span><span class="sxs-lookup"><span data-stu-id="31f47-141">msdyn\_plannedwork</span></span> | <span data-ttu-id="31f47-142">JavaScript Object Notation (JSON) -tietorakenteen, joka on tallennettu kenttään, muoto on muuttunut.</span><span class="sxs-lookup"><span data-stu-id="31f47-142">The format of the JavaScript Object Notation (JSON) data structure that is stored in the field has been changed.</span></span> |

## <a name="schedule-contour"></a><span data-ttu-id="31f47-143">Aikataulun muoto</span><span class="sxs-lookup"><span data-stu-id="31f47-143">Schedule contour</span></span>

<span data-ttu-id="31f47-144">Aikataulun muoto on tallennettu **Suunniteltu työ** -kenttään (**msdyn\_plannedwork**) jokaisessa **Resurssin kohdennus** -entiteetissä (**msdyn\_resourceassignment**).</span><span class="sxs-lookup"><span data-stu-id="31f47-144">The schedule contour is stored in the **Planned Work** field (**msdyn\_plannedwork**) of each **Resource Assignment** entity (**msdyn\_resourceassignment**).</span></span>

### <a name="structure"></a><span data-ttu-id="31f47-145">Rakenne</span><span class="sxs-lookup"><span data-stu-id="31f47-145">Structure</span></span>

<span data-ttu-id="31f47-146">Aikataulu muodon uusi rakenne koostuu joustavista aikaviipaleista, jotka on määritetty kullekin aikataulun päivälle.</span><span class="sxs-lookup"><span data-stu-id="31f47-146">The new structure of the schedule contour consists of flexible time slices that are defined for each day of the schedule.</span></span> <span data-ttu-id="31f47-147">Kullakin aikaviipaleella on seuraavat ominaisuudet:</span><span class="sxs-lookup"><span data-stu-id="31f47-147">Each time slice has the following properties:</span></span>

- <span data-ttu-id="31f47-148">**Aloitus** – päivän työajan alkamisaika projektikalenterin mukaan.</span><span class="sxs-lookup"><span data-stu-id="31f47-148">**Start** – The start of the working hours for the day, according to the project calendar.</span></span>
- <span data-ttu-id="31f47-149">**Lopetus** – päivän työajan päättymisaika projektikalenterin mukaan.</span><span class="sxs-lookup"><span data-stu-id="31f47-149">**End** – The end of the working hours for the day, according to the project calendar.</span></span>
- <span data-ttu-id="31f47-150">**Tunnit** – päivälle määritettyjen tuntien määrä.</span><span class="sxs-lookup"><span data-stu-id="31f47-150">**Hours** – The number of hours that are assigned on the day.</span></span>

<span data-ttu-id="31f47-151">**Esimerkki**</span><span class="sxs-lookup"><span data-stu-id="31f47-151">**Example**</span></span>

<span data-ttu-id="31f47-152">Tässä esimerkissä käytetään projektikalenteria, jossa työpäivä on UTC-8 aikavyöhykkeellä klo 9.00-17.00.</span><span class="sxs-lookup"><span data-stu-id="31f47-152">This example uses a project calendar where the workday is from 9 AM to 5 PM in the UTC-8 time zone.</span></span>

```json
[{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":8},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":8},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":2}]
```

### <a name="auto-scheduling-and-manual-scheduling"></a><span data-ttu-id="31f47-153">Automaattinen aikataulutus ja manuaalinen aikataulutus</span><span class="sxs-lookup"><span data-stu-id="31f47-153">Auto-scheduling and manual scheduling</span></span>

<span data-ttu-id="31f47-154">Jos tehtävä on aikataulutettu automaattisesti, tunnit on ladattu etualalle ja tehtävän kesto voi pienentyä.</span><span class="sxs-lookup"><span data-stu-id="31f47-154">If a task is auto-scheduled, the hours are front-loaded, and the task duration might be reduced.</span></span>

<span data-ttu-id="31f47-155">**Esimerkki**</span><span class="sxs-lookup"><span data-stu-id="31f47-155">**Example**</span></span>

<span data-ttu-id="31f47-156">Seuraava tehtävä on ajoitettu automaattisesti 18 tunniksi kolmen päivän ajaksi (3. joulukuuta 2018 - 5. joulukuuta 2018).</span><span class="sxs-lookup"><span data-stu-id="31f47-156">The following task is auto-scheduled for 18 hours over three days (December 3, 2018, to December 5, 2018).</span></span>

```json
[{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":8},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":8},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":2}]
```

<span data-ttu-id="31f47-157">Jos tehtävä on aikataulutettu manuaalisesti, tunnit jaetaan tasaisesti kaikille päivämäärille.</span><span class="sxs-lookup"><span data-stu-id="31f47-157">If a task is manually scheduled, the hours are evenly distributed to all the dates.</span></span>

<span data-ttu-id="31f47-158">**Esimerkki**</span><span class="sxs-lookup"><span data-stu-id="31f47-158">**Example**</span></span>

<span data-ttu-id="31f47-159">Seuraava tehtävä on ajoitettu manuaalisesti 18 tunniksi kolmen päivän ajaksi (3. joulukuuta 2018 - 5. joulukuuta 2018).</span><span class="sxs-lookup"><span data-stu-id="31f47-159">The following task is manually scheduled for 18 hours over three days (December 3, 2018, to December 5, 2018).</span></span>

```json
[{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":6},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":6},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":6}]
```

### <a name="assignment-unit"></a><span data-ttu-id="31f47-160">Kohdennusyksikkö</span><span class="sxs-lookup"><span data-stu-id="31f47-160">Assignment unit</span></span>

<span data-ttu-id="31f47-161">Kohdennusyksikkö on vanhentunut PSA 3.x:ssä.</span><span class="sxs-lookup"><span data-stu-id="31f47-161">The assignment unit has been deprecated in PSA 3.x.</span></span> <span data-ttu-id="31f47-162">Tehtävien työtunnit jaetaan nyt yhtä päivää kohden kaikkien määritettyjen resurssien kesken.</span><span class="sxs-lookup"><span data-stu-id="31f47-162">The task effort hours are now equally divided, per day, among all the assigned resources.</span></span>

<span data-ttu-id="31f47-163">**Esimerkki**</span><span class="sxs-lookup"><span data-stu-id="31f47-163">**Example**</span></span>

<span data-ttu-id="31f47-164">Tässä esimerkissä tehtävälle on määritetty kaksi resurssia, ja se ajoitetaan automaattisesti 36 tunniksi kolmen päivän ajaksi (3. joulukuuta 2018 - 5. joulukuuta 2018).</span><span class="sxs-lookup"><span data-stu-id="31f47-164">In this example, the task is is assigned to two resources and is auto-scheduled for 36 hours over three days (December 3, 2018, to December 5, 2018).</span></span>

- <span data-ttu-id="31f47-165">Kohdennus 1:</span><span class="sxs-lookup"><span data-stu-id="31f47-165">Assignment 1:</span></span>

    ```json
    [{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":8},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":8},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":2}]
    ```

- <span data-ttu-id="31f47-166">Kohdennus 2:</span><span class="sxs-lookup"><span data-stu-id="31f47-166">Assignment 2:</span></span>

    ```json
    [{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":8},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":8},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":2}]
    ```

## <a name="pricing-dimensions"></a><span data-ttu-id="31f47-167">Hinnoitteludimensiot</span><span class="sxs-lookup"><span data-stu-id="31f47-167">Pricing dimensions</span></span>

<span data-ttu-id="31f47-168">PSA 3.x:ssa resurssikohtaiset hinnoitteludimensiokentät (kuten **Rooli** ja **Organisaatioyksikkö**) on poistettu **msdyn\_projecttask**-entiteetistä.</span><span class="sxs-lookup"><span data-stu-id="31f47-168">In PSA 3.x, resource-specific pricing dimension fields (such as **Role** and **Organizational Unit**) have been removed from the **msdyn\_projecttask** entity.</span></span> <span data-ttu-id="31f47-169">Nämä kentät ovat nyt saatavilla vastaavassa projektiryhmän jäsenessä (**msdyn\_projectteam**) resurssikohdennuksessa (**msdyn\_resourceassignment**), kun projektin arviot on luotu.</span><span class="sxs-lookup"><span data-stu-id="31f47-169">These fields can now be retrieved from the corresponding project team member (**msdyn\_projectteam**) of the resource assignment (**msdyn\_resourceassignment**) when project estimates are generated.</span></span> <span data-ttu-id="31f47-170">Uusi kenttä, **msdyn\_organizationalunit**, on lisätty **msdyn\_projectteam**-entiteettiin.</span><span class="sxs-lookup"><span data-stu-id="31f47-170">A new field, **msdyn\_organizationalunit**, has been added to the **msdyn\_projectteam** entity.</span></span>

| <span data-ttu-id="31f47-171">Vanhentunut kenttä kohteessa msdyn\_projecttask (Projektitehtävä)</span><span class="sxs-lookup"><span data-stu-id="31f47-171">Deprecated field on msdyn\_projecttask (Project Task)</span></span> | <span data-ttu-id="31f47-172">Kenttä kohteesta msdyn\_projectteam (Projektiryhmän jäsen), jota käytetään sen tilalla</span><span class="sxs-lookup"><span data-stu-id="31f47-172">Field from msdyn\_projectteam (Project Team Member) that is used instead</span></span> |
|---|---|
| <span data-ttu-id="31f47-173">msdyn\_resourcecategory</span><span class="sxs-lookup"><span data-stu-id="31f47-173">msdyn\_resourcecategory</span></span> | <span data-ttu-id="31f47-174">msdyn\_resourcecategory</span><span class="sxs-lookup"><span data-stu-id="31f47-174">msdyn\_resourcecategory</span></span> |
| <span data-ttu-id="31f47-175">msdyn\_organizationalunit</span><span class="sxs-lookup"><span data-stu-id="31f47-175">msdyn\_organizationalunit</span></span> | <span data-ttu-id="31f47-176">msdyn\_organizationalunit</span><span class="sxs-lookup"><span data-stu-id="31f47-176">msdyn\_organizationalunit</span></span> |

## <a name="contours"></a><span data-ttu-id="31f47-177">Muodot</span><span class="sxs-lookup"><span data-stu-id="31f47-177">Contours</span></span>

<span data-ttu-id="31f47-178">Hinnoittelun ja arvioiden muotokentät ovat vanhentuneet **msdyn\_projecttask**-entiteetissä.</span><span class="sxs-lookup"><span data-stu-id="31f47-178">The pricing and estimation contour fields have been deprecated on the **msdyn\_projecttask** entity.</span></span> <span data-ttu-id="31f47-179">Ne on siirretty **msdyn\_resourceassignment**-entiteettiin.</span><span class="sxs-lookup"><span data-stu-id="31f47-179">They have been moved to the **msdyn\_resourceassignment** entity.</span></span>

| <span data-ttu-id="31f47-180">Vanhentunut kenttä kohteessa msdyn\_projecttask (Projektitehtävä)</span><span class="sxs-lookup"><span data-stu-id="31f47-180">Deprecated field on msdyn\_projecttask (Project Task)</span></span> | <span data-ttu-id="31f47-181">Uusi kenttä kohteessa msdyn\_resourceassignment (Resurssin kohdennus)</span><span class="sxs-lookup"><span data-stu-id="31f47-181">New field on msdyn\_resourceassignment (Resource Assignment)</span></span> |
|---|---|
| <span data-ttu-id="31f47-182">msdyn\_costestimatecontour</span><span class="sxs-lookup"><span data-stu-id="31f47-182">msdyn\_costestimatecontour</span></span> | <span data-ttu-id="31f47-183">msdyn\_plannedcostcontour</span><span class="sxs-lookup"><span data-stu-id="31f47-183">msdyn\_plannedcostcontour</span></span> |
| <span data-ttu-id="31f47-184">msdyn\_salesestimatecontour</span><span class="sxs-lookup"><span data-stu-id="31f47-184">msdyn\_salesestimatecontour</span></span> | <span data-ttu-id="31f47-185">msdyn\_plannedsalescontour</span><span class="sxs-lookup"><span data-stu-id="31f47-185">msdyn\_plannedsalescontour</span></span> |

<span data-ttu-id="31f47-186">Seuraavat kentät on lisätty **msdyn\_resourceassignment**-entiteettiin:</span><span class="sxs-lookup"><span data-stu-id="31f47-186">The following fields have been added to the **msdyn\_resourceassignment** entity:</span></span>

* <span data-ttu-id="31f47-187">msdyn\_plannedcost</span><span class="sxs-lookup"><span data-stu-id="31f47-187">msdyn\_plannedcost</span></span>
* <span data-ttu-id="31f47-188">msdyn\_plannedsales</span><span class="sxs-lookup"><span data-stu-id="31f47-188">msdyn\_plannedsales</span></span>

<span data-ttu-id="31f47-189">Seuraavat suunniteltujen, toteutuneiden ja jäljellä olevien kustannusten ja myynnin kentät ovat muuttumattomina **msdyn\_projecttask**-entiteetissä:</span><span class="sxs-lookup"><span data-stu-id="31f47-189">The following fields for planned, actual, and remaining cost and sales are unchanged on the **msdyn\_projecttask** entity:</span></span>

* <span data-ttu-id="31f47-190">msdyn\_plannedcost</span><span class="sxs-lookup"><span data-stu-id="31f47-190">msdyn\_plannedcost</span></span>
* <span data-ttu-id="31f47-191">msdyn\_plannedsales</span><span class="sxs-lookup"><span data-stu-id="31f47-191">msdyn\_plannedsales</span></span>
* <span data-ttu-id="31f47-192">msdyn\_actualcost</span><span class="sxs-lookup"><span data-stu-id="31f47-192">msdyn\_actualcost</span></span>
* <span data-ttu-id="31f47-193">msdyn\_actualsales</span><span class="sxs-lookup"><span data-stu-id="31f47-193">msdyn\_actualsales</span></span>
* <span data-ttu-id="31f47-194">msdyn\_remainingcost</span><span class="sxs-lookup"><span data-stu-id="31f47-194">msdyn\_remainingcost</span></span>
* <span data-ttu-id="31f47-195">msdyn\_remainingsales</span><span class="sxs-lookup"><span data-stu-id="31f47-195">msdyn\_remainingsales</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]