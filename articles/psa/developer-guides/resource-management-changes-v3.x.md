---
title: Resurssien hallinnan muutokset (Project Service Automation 3.x)
description: Tässä aiheessa on tietoja resurssien hallinnan muutoksista.
author: makk
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 03/18/2019
ms.topic: article
ms.service: business-applications
ms.author: makk
audience: admin
search.audienceType:
- admin
- customizer
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 94f9adc67163254486387a1ce59d5d3e8e93c335
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/10/2021
ms.locfileid: "5148639"
---
# <a name="resource-management-changes-project-service-automation-3x"></a><span data-ttu-id="185d6-103">Resurssien hallinnan muutokset (Project Service Automation 3.x)</span><span class="sxs-lookup"><span data-stu-id="185d6-103">Resource management changes (Project Service Automation 3.x)</span></span>

[!include [banner](../../includes/psa-now-project-operations.md)]

<span data-ttu-id="185d6-104">Tämän aiheen osissa on tietoja muutoksista, joita on tehty resurssien hallinnan alueelle Dynamics 365 Project Service Automation versiossa 3. x.</span><span class="sxs-lookup"><span data-stu-id="185d6-104">The sections of this topic provide information about the changes that have been made to the Resource management area of Dynamics 365 Project Service Automation version 3.x.</span></span>

## <a name="project-estimates"></a><span data-ttu-id="185d6-105">Projektin arviot</span><span class="sxs-lookup"><span data-stu-id="185d6-105">Project estimates</span></span>

<span data-ttu-id="185d6-106">Sen sijaan, että perustuisivat **msdyn\_projecttask** -entiteettiin (**Projektitehtävä**), projektin arviot perustuvat **msdyn\_resourceassignment** -entiteettiin (**Resurssin kohdentaminent**).</span><span class="sxs-lookup"><span data-stu-id="185d6-106">Instead of being based on the **msdyn\_projecttask** entity (**Project Task**), project estimates are based on the **msdyn\_resourceassignment** entity (**Resource Assignment**).</span></span> <span data-ttu-id="185d6-107">Resurssien kohdennuksista on tullut "totuuden lähde" tehtävien aikatauluttamista ja hinnoittelua varten.</span><span class="sxs-lookup"><span data-stu-id="185d6-107">Resource assignments have become the "source of truth" for task scheduling and pricing.</span></span>

## <a name="line-tasks"></a><span data-ttu-id="185d6-108">Rivitehtävät</span><span class="sxs-lookup"><span data-stu-id="185d6-108">Line tasks</span></span>

<span data-ttu-id="185d6-109">PSA 3. x:ssä rivitehtävät ovat vanhentuneet (vanhentunut).</span><span class="sxs-lookup"><span data-stu-id="185d6-109">In PSA 3.x, line tasks are obsolete (deprecated).</span></span> <span data-ttu-id="185d6-110">Määritykset osoittavat nyt koko tehtävään rivitehtävien sijaan.</span><span class="sxs-lookup"><span data-stu-id="185d6-110">Assignments now point to the whole task instead of the line tasks.</span></span>

<span data-ttu-id="185d6-111">Seuraavasta esimerkistä näkyy, miten tehtävä, jonka nimi on "Testitehtävä", on määritetty ryhmän jäsenille A ja B PSA:N aiemmissa versioissa ja PSA 3. x:ssä.</span><span class="sxs-lookup"><span data-stu-id="185d6-111">The following example shows how a task that is named "Test task" is assigned to team members A and B in earlier versions of PSA and in PSA 3.x.</span></span>

- <span data-ttu-id="185d6-112">**Ennen PSA 3. x:ää:**</span><span class="sxs-lookup"><span data-stu-id="185d6-112">**Before PSA 3.x:**</span></span>

    - <span data-ttu-id="185d6-113">Testitehtävä</span><span class="sxs-lookup"><span data-stu-id="185d6-113">Test task</span></span>

        - <span data-ttu-id="185d6-114">Testitehtävä – Rivitehtävä 1</span><span class="sxs-lookup"><span data-stu-id="185d6-114">Test task – Line task 1</span></span>

            - <span data-ttu-id="185d6-115">Kohdennus A:lle</span><span class="sxs-lookup"><span data-stu-id="185d6-115">Assignment to A</span></span>

        - <span data-ttu-id="185d6-116">Testitehtävä – Rivitehtävä 2</span><span class="sxs-lookup"><span data-stu-id="185d6-116">Test task – Line task 2</span></span>

            - <span data-ttu-id="185d6-117">Kohdennus B:lle</span><span class="sxs-lookup"><span data-stu-id="185d6-117">Assignment to B</span></span>

- <span data-ttu-id="185d6-118">**PSA 3.x:**</span><span class="sxs-lookup"><span data-stu-id="185d6-118">**PSA 3.x:**</span></span>

    - <span data-ttu-id="185d6-119">Testitehtävä</span><span class="sxs-lookup"><span data-stu-id="185d6-119">Test task</span></span>

        - <span data-ttu-id="185d6-120">Kohdennus A:lle</span><span class="sxs-lookup"><span data-stu-id="185d6-120">Assignment to A</span></span>
        - <span data-ttu-id="185d6-121">Kohdennus B:lle</span><span class="sxs-lookup"><span data-stu-id="185d6-121">Assignment to B</span></span>

## <a name="unassigned-assignment"></a><span data-ttu-id="185d6-122">Kohdentamaton kohdennus</span><span class="sxs-lookup"><span data-stu-id="185d6-122">Unassigned assignment</span></span>

<span data-ttu-id="185d6-123">PSA 3.x:ssä kohdentamaton kohdennus on sellainen kohdennus, joka on kohdennettu ryhmän jäsenelle **NULL** ja resurssille **NULL**.</span><span class="sxs-lookup"><span data-stu-id="185d6-123">In PSA 3.x, an unassigned assignment is an assignment that is assigned to a **NULL** team member and a **NULL** resource.</span></span> <span data-ttu-id="185d6-124">Kohdentamattomia kohdennuksia voi tapahtua muutamissa tapauksissa:</span><span class="sxs-lookup"><span data-stu-id="185d6-124">Unassigned assignments can occur in a couple of scenarios:</span></span>

- <span data-ttu-id="185d6-125">Jos tehtävä on luotu, mutta sitä ei ole vielä kohdennettu millekään ryhmän jäsenelle, kohdentamaton kohdennus luodaan aina.</span><span class="sxs-lookup"><span data-stu-id="185d6-125">If a task has been created, but it hasn't yet been assigned to any team member, an unassigned assignment is always created.</span></span> 
- <span data-ttu-id="185d6-126">Jos kaikki tehtävään kohdennetut henkilöt poistetaan, kohdentamaton kohdennus luodaan uudelleen kyseiselle tehtävälle.</span><span class="sxs-lookup"><span data-stu-id="185d6-126">If all assignees on a task are removed, an unassigned assignment is re-created for that task.</span></span>

## <a name="scheduling-fields-on-the-project-task-entity"></a><span data-ttu-id="185d6-127">Projekti tehtävä -entiteetin aikataulutuskentät</span><span class="sxs-lookup"><span data-stu-id="185d6-127">Scheduling fields on the Project Task entity</span></span>

<span data-ttu-id="185d6-128">Kentät **msdyn\_projecttask**-entiteetissä ovat vanhentuneet tai siirretty **msdyn\_resourceassignment**-entiteettiin, tai niihin viitataan nyt **msdyn\_projectteam**-entiteetissä (**Projektiryhmän jäsen**).</span><span class="sxs-lookup"><span data-stu-id="185d6-128">The fields on the **msdyn\_projecttask** entity have been deprecated or moved to the **msdyn\_resourceassignment** entity, or they are now referenced from the **msdyn\_projectteam** entity (**Project Team Member**).</span></span>

| <span data-ttu-id="185d6-129">Vanhentunut kenttä kohteessa msdyn\_projecttask (Projektitehtävä)</span><span class="sxs-lookup"><span data-stu-id="185d6-129">Deprecated field on msdyn\_projecttask (Project Task)</span></span> | <span data-ttu-id="185d6-130">Uusi kenttä kohteessa msdyn\_resourceassignment (Resurssin kohdennus)</span><span class="sxs-lookup"><span data-stu-id="185d6-130">New field on msdyn\_resourceassignment (Resource Assignment)</span></span> | <span data-ttu-id="185d6-131">Kommentti</span><span class="sxs-lookup"><span data-stu-id="185d6-131">Comment</span></span> |
|---|---|---|
| <span data-ttu-id="185d6-132">msdyn\_assignedresources</span><span class="sxs-lookup"><span data-stu-id="185d6-132">msdyn\_assignedresources</span></span> | <span data-ttu-id="185d6-133">Ei ole</span><span class="sxs-lookup"><span data-stu-id="185d6-133">None</span></span> | |
| <span data-ttu-id="185d6-134">msdyn\_assignedteammembers</span><span class="sxs-lookup"><span data-stu-id="185d6-134">msdyn\_assignedteammembers</span></span> | <span data-ttu-id="185d6-135">Ei ole</span><span class="sxs-lookup"><span data-stu-id="185d6-135">None</span></span> | |
| <span data-ttu-id="185d6-136">msdyn\_numberofresources</span><span class="sxs-lookup"><span data-stu-id="185d6-136">msdyn\_numberofresources</span></span> | <span data-ttu-id="185d6-137">Ei ole</span><span class="sxs-lookup"><span data-stu-id="185d6-137">None</span></span> | |
| <span data-ttu-id="185d6-138">msdyn\_scheduledhours</span><span class="sxs-lookup"><span data-stu-id="185d6-138">msdyn\_scheduledhours</span></span> | <span data-ttu-id="185d6-139">Ei ole</span><span class="sxs-lookup"><span data-stu-id="185d6-139">None</span></span> | |
| <span data-ttu-id="185d6-140">msdyn\_effortcontour</span><span class="sxs-lookup"><span data-stu-id="185d6-140">msdyn\_effortcontour</span></span> | <span data-ttu-id="185d6-141">msdyn\_plannedwork</span><span class="sxs-lookup"><span data-stu-id="185d6-141">msdyn\_plannedwork</span></span> | <span data-ttu-id="185d6-142">JavaScript Object Notation (JSON) -tietorakenteen, joka on tallennettu kenttään, muoto on muuttunut.</span><span class="sxs-lookup"><span data-stu-id="185d6-142">The format of the JavaScript Object Notation (JSON) data structure that is stored in the field has been changed.</span></span> |

## <a name="schedule-contour"></a><span data-ttu-id="185d6-143">Aikataulun muoto</span><span class="sxs-lookup"><span data-stu-id="185d6-143">Schedule contour</span></span>

<span data-ttu-id="185d6-144">Aikataulun muoto on tallennettu **Suunniteltu työ** -kenttään (**msdyn\_plannedwork**) jokaisessa **Resurssin kohdennus** -entiteetissä (**msdyn\_resourceassignment**).</span><span class="sxs-lookup"><span data-stu-id="185d6-144">The schedule contour is stored in the **Planned Work** field (**msdyn\_plannedwork**) of each **Resource Assignment** entity (**msdyn\_resourceassignment**).</span></span>

### <a name="structure"></a><span data-ttu-id="185d6-145">Rakenne</span><span class="sxs-lookup"><span data-stu-id="185d6-145">Structure</span></span>

<span data-ttu-id="185d6-146">Aikataulu muodon uusi rakenne koostuu joustavista aikaviipaleista, jotka on määritetty kullekin aikataulun päivälle.</span><span class="sxs-lookup"><span data-stu-id="185d6-146">The new structure of the schedule contour consists of flexible time slices that are defined for each day of the schedule.</span></span> <span data-ttu-id="185d6-147">Kullakin aikaviipaleella on seuraavat ominaisuudet:</span><span class="sxs-lookup"><span data-stu-id="185d6-147">Each time slice has the following properties:</span></span>

- <span data-ttu-id="185d6-148">**Aloitus** – päivän työajan alkamisaika projektikalenterin mukaan.</span><span class="sxs-lookup"><span data-stu-id="185d6-148">**Start** – The start of the working hours for the day, according to the project calendar.</span></span>
- <span data-ttu-id="185d6-149">**Lopetus** – päivän työajan päättymisaika projektikalenterin mukaan.</span><span class="sxs-lookup"><span data-stu-id="185d6-149">**End** – The end of the working hours for the day, according to the project calendar.</span></span>
- <span data-ttu-id="185d6-150">**Tunnit** – päivälle määritettyjen tuntien määrä.</span><span class="sxs-lookup"><span data-stu-id="185d6-150">**Hours** – The number of hours that are assigned on the day.</span></span>

<span data-ttu-id="185d6-151">**Esimerkki**</span><span class="sxs-lookup"><span data-stu-id="185d6-151">**Example**</span></span>

<span data-ttu-id="185d6-152">Tässä esimerkissä käytetään projektikalenteria, jossa työpäivä on UTC-8 aikavyöhykkeellä klo 9.00-17.00.</span><span class="sxs-lookup"><span data-stu-id="185d6-152">This example uses a project calendar where the workday is from 9 AM to 5 PM in the UTC-8 time zone.</span></span>

```json
[{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":8},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":8},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":2}]
```

### <a name="auto-scheduling-and-manual-scheduling"></a><span data-ttu-id="185d6-153">Automaattinen aikataulutus ja manuaalinen aikataulutus</span><span class="sxs-lookup"><span data-stu-id="185d6-153">Auto-scheduling and manual scheduling</span></span>

<span data-ttu-id="185d6-154">Jos tehtävä on aikataulutettu automaattisesti, tunnit on ladattu etualalle ja tehtävän kesto voi pienentyä.</span><span class="sxs-lookup"><span data-stu-id="185d6-154">If a task is auto-scheduled, the hours are front-loaded, and the task duration might be reduced.</span></span>

<span data-ttu-id="185d6-155">**Esimerkki**</span><span class="sxs-lookup"><span data-stu-id="185d6-155">**Example**</span></span>

<span data-ttu-id="185d6-156">Seuraava tehtävä on ajoitettu automaattisesti 18 tunniksi kolmen päivän ajaksi (3. joulukuuta 2018 - 5. joulukuuta 2018).</span><span class="sxs-lookup"><span data-stu-id="185d6-156">The following task is auto-scheduled for 18 hours over three days (December 3, 2018, to December 5, 2018).</span></span>

```json
[{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":8},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":8},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":2}]
```

<span data-ttu-id="185d6-157">Jos tehtävä on aikataulutettu manuaalisesti, tunnit jaetaan tasaisesti kaikille päivämäärille.</span><span class="sxs-lookup"><span data-stu-id="185d6-157">If a task is manually scheduled, the hours are evenly distributed to all the dates.</span></span>

<span data-ttu-id="185d6-158">**Esimerkki**</span><span class="sxs-lookup"><span data-stu-id="185d6-158">**Example**</span></span>

<span data-ttu-id="185d6-159">Seuraava tehtävä on ajoitettu manuaalisesti 18 tunniksi kolmen päivän ajaksi (3. joulukuuta 2018 - 5. joulukuuta 2018).</span><span class="sxs-lookup"><span data-stu-id="185d6-159">The following task is manually scheduled for 18 hours over three days (December 3, 2018, to December 5, 2018).</span></span>

```json
[{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":6},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":6},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":6}]
```

### <a name="assignment-unit"></a><span data-ttu-id="185d6-160">Kohdennusyksikkö</span><span class="sxs-lookup"><span data-stu-id="185d6-160">Assignment unit</span></span>

<span data-ttu-id="185d6-161">Kohdennusyksikkö on vanhentunut PSA 3.x:ssä.</span><span class="sxs-lookup"><span data-stu-id="185d6-161">The assignment unit has been deprecated in PSA 3.x.</span></span> <span data-ttu-id="185d6-162">Tehtävien työtunnit jaetaan nyt yhtä päivää kohden kaikkien määritettyjen resurssien kesken.</span><span class="sxs-lookup"><span data-stu-id="185d6-162">The task effort hours are now equally divided, per day, among all the assigned resources.</span></span>

<span data-ttu-id="185d6-163">**Esimerkki**</span><span class="sxs-lookup"><span data-stu-id="185d6-163">**Example**</span></span>

<span data-ttu-id="185d6-164">Tässä esimerkissä tehtävälle on määritetty kaksi resurssia, ja se ajoitetaan automaattisesti 36 tunniksi kolmen päivän ajaksi (3. joulukuuta 2018 - 5. joulukuuta 2018).</span><span class="sxs-lookup"><span data-stu-id="185d6-164">In this example, the task is is assigned to two resources and is auto-scheduled for 36 hours over three days (December 3, 2018, to December 5, 2018).</span></span>

- <span data-ttu-id="185d6-165">Kohdennus 1:</span><span class="sxs-lookup"><span data-stu-id="185d6-165">Assignment 1:</span></span>

    ```json
    [{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":8},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":8},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":2}]
    ```

- <span data-ttu-id="185d6-166">Kohdennus 2:</span><span class="sxs-lookup"><span data-stu-id="185d6-166">Assignment 2:</span></span>

    ```json
    [{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":8},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":8},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":2}]
    ```

## <a name="pricing-dimensions"></a><span data-ttu-id="185d6-167">Hinnoitteludimensiot</span><span class="sxs-lookup"><span data-stu-id="185d6-167">Pricing dimensions</span></span>

<span data-ttu-id="185d6-168">PSA 3.x:ssa resurssikohtaiset hinnoitteludimensiokentät (kuten **Rooli** ja **Organisaatioyksikkö**) on poistettu **msdyn\_projecttask**-entiteetistä.</span><span class="sxs-lookup"><span data-stu-id="185d6-168">In PSA 3.x, resource-specific pricing dimension fields (such as **Role** and **Organizational Unit**) have been removed from the **msdyn\_projecttask** entity.</span></span> <span data-ttu-id="185d6-169">Nämä kentät ovat nyt saatavilla vastaavassa projektiryhmän jäsenessä (**msdyn\_projectteam**) resurssikohdennuksessa (**msdyn\_resourceassignment**), kun projektin arviot on luotu.</span><span class="sxs-lookup"><span data-stu-id="185d6-169">These fields can now be retrieved from the corresponding project team member (**msdyn\_projectteam**) of the resource assignment (**msdyn\_resourceassignment**) when project estimates are generated.</span></span> <span data-ttu-id="185d6-170">Uusi kenttä, **msdyn\_organizationalunit**, on lisätty **msdyn\_projectteam**-entiteettiin.</span><span class="sxs-lookup"><span data-stu-id="185d6-170">A new field, **msdyn\_organizationalunit**, has been added to the **msdyn\_projectteam** entity.</span></span>

| <span data-ttu-id="185d6-171">Vanhentunut kenttä kohteessa msdyn\_projecttask (Projektitehtävä)</span><span class="sxs-lookup"><span data-stu-id="185d6-171">Deprecated field on msdyn\_projecttask (Project Task)</span></span> | <span data-ttu-id="185d6-172">Kenttä kohteesta msdyn\_projectteam (Projektiryhmän jäsen), jota käytetään sen tilalla</span><span class="sxs-lookup"><span data-stu-id="185d6-172">Field from msdyn\_projectteam (Project Team Member) that is used instead</span></span> |
|---|---|
| <span data-ttu-id="185d6-173">msdyn\_resourcecategory</span><span class="sxs-lookup"><span data-stu-id="185d6-173">msdyn\_resourcecategory</span></span> | <span data-ttu-id="185d6-174">msdyn\_resourcecategory</span><span class="sxs-lookup"><span data-stu-id="185d6-174">msdyn\_resourcecategory</span></span> |
| <span data-ttu-id="185d6-175">msdyn\_organizationalunit</span><span class="sxs-lookup"><span data-stu-id="185d6-175">msdyn\_organizationalunit</span></span> | <span data-ttu-id="185d6-176">msdyn\_organizationalunit</span><span class="sxs-lookup"><span data-stu-id="185d6-176">msdyn\_organizationalunit</span></span> |

## <a name="contours"></a><span data-ttu-id="185d6-177">Muodot</span><span class="sxs-lookup"><span data-stu-id="185d6-177">Contours</span></span>

<span data-ttu-id="185d6-178">Hinnoittelun ja arvioiden muotokentät ovat vanhentuneet **msdyn\_projecttask**-entiteetissä.</span><span class="sxs-lookup"><span data-stu-id="185d6-178">The pricing and estimation contour fields have been deprecated on the **msdyn\_projecttask** entity.</span></span> <span data-ttu-id="185d6-179">Ne on siirretty **msdyn\_resourceassignment**-entiteettiin.</span><span class="sxs-lookup"><span data-stu-id="185d6-179">They have been moved to the **msdyn\_resourceassignment** entity.</span></span>

| <span data-ttu-id="185d6-180">Vanhentunut kenttä kohteessa msdyn\_projecttask (Projektitehtävä)</span><span class="sxs-lookup"><span data-stu-id="185d6-180">Deprecated field on msdyn\_projecttask (Project Task)</span></span> | <span data-ttu-id="185d6-181">Uusi kenttä kohteessa msdyn\_resourceassignment (Resurssin kohdennus)</span><span class="sxs-lookup"><span data-stu-id="185d6-181">New field on msdyn\_resourceassignment (Resource Assignment)</span></span> |
|---|---|
| <span data-ttu-id="185d6-182">msdyn\_costestimatecontour</span><span class="sxs-lookup"><span data-stu-id="185d6-182">msdyn\_costestimatecontour</span></span> | <span data-ttu-id="185d6-183">msdyn\_plannedcostcontour</span><span class="sxs-lookup"><span data-stu-id="185d6-183">msdyn\_plannedcostcontour</span></span> |
| <span data-ttu-id="185d6-184">msdyn\_salesestimatecontour</span><span class="sxs-lookup"><span data-stu-id="185d6-184">msdyn\_salesestimatecontour</span></span> | <span data-ttu-id="185d6-185">msdyn\_plannedsalescontour</span><span class="sxs-lookup"><span data-stu-id="185d6-185">msdyn\_plannedsalescontour</span></span> |

<span data-ttu-id="185d6-186">Seuraavat kentät on lisätty **msdyn\_resourceassignment**-entiteettiin:</span><span class="sxs-lookup"><span data-stu-id="185d6-186">The following fields have been added to the **msdyn\_resourceassignment** entity:</span></span>

* <span data-ttu-id="185d6-187">msdyn\_plannedcost</span><span class="sxs-lookup"><span data-stu-id="185d6-187">msdyn\_plannedcost</span></span>
* <span data-ttu-id="185d6-188">msdyn\_plannedsales</span><span class="sxs-lookup"><span data-stu-id="185d6-188">msdyn\_plannedsales</span></span>

<span data-ttu-id="185d6-189">Seuraavat suunniteltujen, toteutuneiden ja jäljellä olevien kustannusten ja myynnin kentät ovat muuttumattomina **msdyn\_projecttask**-entiteetissä:</span><span class="sxs-lookup"><span data-stu-id="185d6-189">The following fields for planned, actual, and remaining cost and sales are unchanged on the **msdyn\_projecttask** entity:</span></span>

* <span data-ttu-id="185d6-190">msdyn\_plannedcost</span><span class="sxs-lookup"><span data-stu-id="185d6-190">msdyn\_plannedcost</span></span>
* <span data-ttu-id="185d6-191">msdyn\_plannedsales</span><span class="sxs-lookup"><span data-stu-id="185d6-191">msdyn\_plannedsales</span></span>
* <span data-ttu-id="185d6-192">msdyn\_actualcost</span><span class="sxs-lookup"><span data-stu-id="185d6-192">msdyn\_actualcost</span></span>
* <span data-ttu-id="185d6-193">msdyn\_actualsales</span><span class="sxs-lookup"><span data-stu-id="185d6-193">msdyn\_actualsales</span></span>
* <span data-ttu-id="185d6-194">msdyn\_remainingcost</span><span class="sxs-lookup"><span data-stu-id="185d6-194">msdyn\_remainingcost</span></span>
* <span data-ttu-id="185d6-195">msdyn\_remainingsales</span><span class="sxs-lookup"><span data-stu-id="185d6-195">msdyn\_remainingsales</span></span>
