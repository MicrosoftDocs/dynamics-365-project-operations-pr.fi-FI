---
title: Aikataulutustilat
description: Tässä aiheessa on tietoja aikataulutustiloista.
author: ruhercul
manager: AnnBe
ms.date: 05/04/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: fe54944999617b248ff925148a78601dd4be7aca
ms.sourcegitcommit: c45ceda833b30ad39861f5bcd3ba1bbfff11fe7a
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/04/2021
ms.locfileid: "5981431"
---
# <a name="scheduling-modes"></a><span data-ttu-id="ba9ee-103">Aikataulutustilat</span><span class="sxs-lookup"><span data-stu-id="ba9ee-103">Scheduling modes</span></span>

<span data-ttu-id="ba9ee-104">_**Koskee:** Project Operationsin resurssiin / muuhun kuin resurssiin perustuvia skenaarioita, Lite-käyttöönotto-kaupasta proformalaskutukseen_</span><span class="sxs-lookup"><span data-stu-id="ba9ee-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="ba9ee-105">Dynamics 365 Project Operations tarjoaa organisaatioille mahdollisuuden määritellä, miten ne hallitsevat tehtävien keskeisten muuttujien muutoksia työrakenteessa.</span><span class="sxs-lookup"><span data-stu-id="ba9ee-105">Dynamics 365 Project Operations provides the ability for organizations to define how they manage changes to key variables in tasks within the work breakdown structure.</span></span> <span data-ttu-id="ba9ee-106">Projektipäälliköt voivat organisaation tarpeiden perusteella tehdä muutoksia aikataulutustilaan projektia luodessaan.</span><span class="sxs-lookup"><span data-stu-id="ba9ee-106">Based on the specific needs of the organization, Project Managers can make changes to the scheduling mode when a project is created.</span></span>

<span data-ttu-id="ba9ee-107">Project Operationsissa on käytettävissä kolme aikataulutustilaa:</span><span class="sxs-lookup"><span data-stu-id="ba9ee-107">There are three scheduling modes available in Project Operations:</span></span>

  - <span data-ttu-id="ba9ee-108">Kiinteä kesto (tämä on oletustila)</span><span class="sxs-lookup"><span data-stu-id="ba9ee-108">Fixed duration (this is the default mode)</span></span>
  - <span data-ttu-id="ba9ee-109">Kiinteä työ</span><span class="sxs-lookup"><span data-stu-id="ba9ee-109">Fixed work</span></span>
  - <span data-ttu-id="ba9ee-110">Kiinteät yksiköt</span><span class="sxs-lookup"><span data-stu-id="ba9ee-110">Fixed units</span></span>

<span data-ttu-id="ba9ee-111">Tietyn aikataulutustilan määrityksen vaikutukset määräytyvät seuraavan kaavan mukaan:</span><span class="sxs-lookup"><span data-stu-id="ba9ee-111">The values impacted by the definition of a specific scheduling mode are determined by the following formula:</span></span>

  <span data-ttu-id="ba9ee-112">Työmäärä (*työ*) = Kesto x yksiköt</span><span class="sxs-lookup"><span data-stu-id="ba9ee-112">Effort (*Work*) = Duration x Units</span></span>

<span data-ttu-id="ba9ee-113">Kun määrität projektin aikataulutustilan, määrität yhden näistä arvoista, joita ei voi muuttaa.</span><span class="sxs-lookup"><span data-stu-id="ba9ee-113">When you define a project’s scheduling mode, you are setting one of these values, which then can't be changed.</span></span> <span data-ttu-id="ba9ee-114">Jos tämä arvo pidetään asetinarvona, arvoksi tulee prioriteetti, joka ilmoittaa, että järjestelmä ei halua muuttaa arvoa, kun muut arvot muuttuvat.</span><span class="sxs-lookup"><span data-stu-id="ba9ee-114">Holding this value as a constant places a priority on that value, which notifies the system not to change it when the other two values change.</span></span> <span data-ttu-id="ba9ee-115">Seuraavassa taulukossa on tietoja tietyn tilan valitsemisen vaikutuksista.</span><span class="sxs-lookup"><span data-stu-id="ba9ee-115">The following table provides information about the impacts of selecting a specific mode.</span></span>

| <span data-ttu-id="ba9ee-116">**Tässä tehtävässä**</span><span class="sxs-lookup"><span data-stu-id="ba9ee-116">**In this task**</span></span>             | <span data-ttu-id="ba9ee-117">**Jos muutat yksiköitä**</span><span class="sxs-lookup"><span data-stu-id="ba9ee-117">**If you revise units**</span></span>   | <span data-ttu-id="ba9ee-118">**Jos muutat kestoa**</span><span class="sxs-lookup"><span data-stu-id="ba9ee-118">**If you revise duration**</span></span> | <span data-ttu-id="ba9ee-119">**Jos muutat työmäärää**</span><span class="sxs-lookup"><span data-stu-id="ba9ee-119">**If you revise effort**</span></span>  |
|----------------------|---------------------------|----------------------------|---------------------------|
| <span data-ttu-id="ba9ee-120">Kiinteät yksikkötehtävät</span><span class="sxs-lookup"><span data-stu-id="ba9ee-120">Fixed units task</span></span>     | <span data-ttu-id="ba9ee-121">Kesto lasketaan uudelleen.</span><span class="sxs-lookup"><span data-stu-id="ba9ee-121">Duration is recalculated.</span></span> | <span data-ttu-id="ba9ee-122">Työmäärä lasketaan uudelleen.</span><span class="sxs-lookup"><span data-stu-id="ba9ee-122">Effort is recalculated.</span></span>    | <span data-ttu-id="ba9ee-123">Kesto lasketaan uudelleen.</span><span class="sxs-lookup"><span data-stu-id="ba9ee-123">Duration is recalculated.</span></span> |
| <span data-ttu-id="ba9ee-124">Kiinteän työmäärän tehtävä</span><span class="sxs-lookup"><span data-stu-id="ba9ee-124">Fixed effort task</span></span>    | <span data-ttu-id="ba9ee-125">Kesto lasketaan uudelleen.</span><span class="sxs-lookup"><span data-stu-id="ba9ee-125">Duration is recalculated.</span></span> | <span data-ttu-id="ba9ee-126">Yksiköt lasketaan uudelleen.</span><span class="sxs-lookup"><span data-stu-id="ba9ee-126">Units are recalculated.</span></span>    | <span data-ttu-id="ba9ee-127">Kesto lasketaan uudelleen.</span><span class="sxs-lookup"><span data-stu-id="ba9ee-127">Duration is recalculated.</span></span> |
| <span data-ttu-id="ba9ee-128">Kiinteän keston tehtävä</span><span class="sxs-lookup"><span data-stu-id="ba9ee-128">Fixed duration task</span></span>  | <span data-ttu-id="ba9ee-129">Työmäärä lasketaan uudelleen.</span><span class="sxs-lookup"><span data-stu-id="ba9ee-129">Effort is recalculated.</span></span>   | <span data-ttu-id="ba9ee-130">Työmäärä lasketaan uudelleen.</span><span class="sxs-lookup"><span data-stu-id="ba9ee-130">Effort is recalculated.</span></span>    | <span data-ttu-id="ba9ee-131">Yksiköt lasketaan uudelleen.</span><span class="sxs-lookup"><span data-stu-id="ba9ee-131">Units are recalculated.</span></span>   |

<span data-ttu-id="ba9ee-132">Lisätietoja tietyn tilan vaikutuksista on ohjeaiheessa [Tehtävätyypin muuttaminen tarkempaa aikataulutusta varten](https://support.microsoft.com/en-us/office/change-the-task-type-for-more-accurate-scheduling-b0b969ad-45bc-4e9e-8967-435587548a72).</span><span class="sxs-lookup"><span data-stu-id="ba9ee-132">For more information about the implications of a given mode, see [Change the task type for more accurate scheduling](https://support.microsoft.com/en-us/office/change-the-task-type-for-more-accurate-scheduling-b0b969ad-45bc-4e9e-8967-435587548a72).</span></span> <span data-ttu-id="ba9ee-133">Aiheessa **Työ**-termiä käytetään **Työmäärä**-termin sijaan.</span><span class="sxs-lookup"><span data-stu-id="ba9ee-133">In the topic, the term **Work** is used instead of **Effort**.</span></span>

## <a name="change-the-organizations-scheduling-mode"></a><span data-ttu-id="ba9ee-134">Organisaation aikataulutustilan muuttaminen</span><span class="sxs-lookup"><span data-stu-id="ba9ee-134">Change the organization’s scheduling mode</span></span>

<span data-ttu-id="ba9ee-135">Määritä organisaation aikataulutustila seuraavien vaiheiden mukaisesti.</span><span class="sxs-lookup"><span data-stu-id="ba9ee-135">Complete the following steps to define the scheduling mode of an organization.</span></span>

1. <span data-ttu-id="ba9ee-136">Siirry kohtaan **Asetukset** \> **Yleiset** \> **Parametrit** ja valitse sitten projektin parametri.</span><span class="sxs-lookup"><span data-stu-id="ba9ee-136">Go to **Settings** \> **General** \> **Parameters**, and then select the project parameter.</span></span> 
2. <span data-ttu-id="ba9ee-137">Valitse **Projektin parametrit** -sivulla organisaation oletusajoitustila ja määritä sitten projektipäällikölle mahdollisuus ohittaa asetus uutta projektia luotaessa.</span><span class="sxs-lookup"><span data-stu-id="ba9ee-137">On the **Project Parameters** page, select the default scheduling mode for the organization, and then define ability for the Project manager to override the setting when creating a new project.</span></span>

## <a name="change-the-scheduling-mode-setting-on-a-project"></a><span data-ttu-id="ba9ee-138">Projektin aikataulutustilan asetuksen muuttaminen</span><span class="sxs-lookup"><span data-stu-id="ba9ee-138">Change the scheduling mode setting on a project</span></span>

<span data-ttu-id="ba9ee-139">Jos organisaatio sallii projektipäällikön ohittaa oletusajoitustilan, projektipäällikkö voi tehdä muutoksen uutta projektia luodessaan.</span><span class="sxs-lookup"><span data-stu-id="ba9ee-139">If an organization allows the Project manager to override the default scheduling mode, the Project manager can make that change when they create a new project.</span></span> <span data-ttu-id="ba9ee-140">Kun projekti on tallennettu, ajoitustilaa ei voi kuitenkaan muuttaa.</span><span class="sxs-lookup"><span data-stu-id="ba9ee-140">However, after the project has been saved, the scheduling mode can't be changed.</span></span>

## <a name="copied-projects"></a><span data-ttu-id="ba9ee-141">Kopioidut projektit</span><span class="sxs-lookup"><span data-stu-id="ba9ee-141">Copied projects</span></span>

<span data-ttu-id="ba9ee-142">Koska projekti luodaan, kun kopiointitoiminto suoritetaan, projektipäällikkö ei voi asettaa ajoitustilaa.</span><span class="sxs-lookup"><span data-stu-id="ba9ee-142">Because a project is created when the copy project action is taken, the Project manager can't set the scheduling mode.</span></span> <span data-ttu-id="ba9ee-143">Kohdeprojektin oletusarvo on aina organisaatiotasolla määritetty tila.</span><span class="sxs-lookup"><span data-stu-id="ba9ee-143">The destination project will always default to the mode defined at the organizational level.</span></span>

## <a name="copied-tasks"></a><span data-ttu-id="ba9ee-144">Kopioidut tehtävät</span><span class="sxs-lookup"><span data-stu-id="ba9ee-144">Copied tasks</span></span>

<span data-ttu-id="ba9ee-145">Kun tehtävä kopioidaan projektista toiseen, tehtävä perii kohdeprojektin aikataulutustilan.</span><span class="sxs-lookup"><span data-stu-id="ba9ee-145">When a task is copied from one project to another, the task inherits the scheduling mode of the destination project.</span></span>
