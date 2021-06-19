---
title: Projektin kopioiminen
description: Tässä aiheessa on tietoja projektien kopioimisesta Dynamics 365 Project Operationsissa.
author: ruhercul
ms.date: 05/21/2021
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: c3055ab5b8c07faa2bc9167956d283e2a66029dd
ms.sourcegitcommit: 173f2b1f4e063c440a5f78d76d456c62aadbd89e
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/24/2021
ms.locfileid: "6091250"
---
# <a name="copy-a-project"></a><span data-ttu-id="f4b4b-103">Projektin kopioiminen</span><span class="sxs-lookup"><span data-stu-id="f4b4b-103">Copy a project</span></span>

<span data-ttu-id="f4b4b-104">_**Koskee:** Project Operationsin resurssiin / muuhun kuin resurssiin perustuvia skenaarioita, Lite-käyttöönotto-kaupasta proformalaskutukseen_</span><span class="sxs-lookup"><span data-stu-id="f4b4b-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="f4b4b-105">Dynamics 365 Project Operationsin avulla voit nopeasti luoda uusia projekteja valitsemalla **Projektit**-lomakkeessa **Kopioi projekti**.</span><span class="sxs-lookup"><span data-stu-id="f4b4b-105">With Dynamics 365 Project Operations, you can quickly build new projects by selecting **Copy Project** on the **Projects** form.</span></span> <span data-ttu-id="f4b4b-106">Jos haluat kopioida projektin, avaa kopioitava projekti ja valitse sitten **Kopioi projekti**.</span><span class="sxs-lookup"><span data-stu-id="f4b4b-106">To copy a project, open the project you want to copy, and then select **Copy project**.</span></span> <span data-ttu-id="f4b4b-107">Toiminto kopioi seuraavat tiedot:</span><span class="sxs-lookup"><span data-stu-id="f4b4b-107">The action will copy the following:</span></span>

- <span data-ttu-id="f4b4b-108">Projektin ominaisuudet</span><span class="sxs-lookup"><span data-stu-id="f4b4b-108">Project properties</span></span> 
- <span data-ttu-id="f4b4b-109">Työrakenne</span><span class="sxs-lookup"><span data-stu-id="f4b4b-109">Work breakdown structure</span></span>
- <span data-ttu-id="f4b4b-110">Projektiryhmän jäsenet</span><span class="sxs-lookup"><span data-stu-id="f4b4b-110">Project team members</span></span>
- <span data-ttu-id="f4b4b-111">Projektin arviot</span><span class="sxs-lookup"><span data-stu-id="f4b4b-111">Project estimates</span></span>
- <span data-ttu-id="f4b4b-112">Projektin kuluarviot</span><span class="sxs-lookup"><span data-stu-id="f4b4b-112">Project expense estimates</span></span>
- <span data-ttu-id="f4b4b-113">Projektin materiaaliarviot</span><span class="sxs-lookup"><span data-stu-id="f4b4b-113">Project material estimates</span></span>

## <a name="project-properties"></a><span data-ttu-id="f4b4b-114">Projektin ominaisuudet</span><span class="sxs-lookup"><span data-stu-id="f4b4b-114">Project properties</span></span>

<span data-ttu-id="f4b4b-115">Kun projekti kopioidaan, seuraavien kenttien arvot kopioidaan:</span><span class="sxs-lookup"><span data-stu-id="f4b4b-115">When the project is copied, the values in the following fields are copied:</span></span>

- <span data-ttu-id="f4b4b-116">Nimi</span><span class="sxs-lookup"><span data-stu-id="f4b4b-116">Name</span></span>
- <span data-ttu-id="f4b4b-117">Kuvaus</span><span class="sxs-lookup"><span data-stu-id="f4b4b-117">Description</span></span>
- <span data-ttu-id="f4b4b-118">Asiakas</span><span class="sxs-lookup"><span data-stu-id="f4b4b-118">Customer</span></span>
- <span data-ttu-id="f4b4b-119">Kalenterimalli</span><span class="sxs-lookup"><span data-stu-id="f4b4b-119">Calendar Template</span></span>
- <span data-ttu-id="f4b4b-120">Valuutta</span><span class="sxs-lookup"><span data-stu-id="f4b4b-120">Currency</span></span>
- <span data-ttu-id="f4b4b-121">Sopimusyksikkö</span><span class="sxs-lookup"><span data-stu-id="f4b4b-121">Contracting Unit</span></span>
- <span data-ttu-id="f4b4b-122">Projektipäällikkö</span><span class="sxs-lookup"><span data-stu-id="f4b4b-122">Project Manager</span></span>
- <span data-ttu-id="f4b4b-123">Tila</span><span class="sxs-lookup"><span data-stu-id="f4b4b-123">Status</span></span>
- <span data-ttu-id="f4b4b-124">Koko projektin tila</span><span class="sxs-lookup"><span data-stu-id="f4b4b-124">Overall Project Status</span></span>
- <span data-ttu-id="f4b4b-125">Kommentit</span><span class="sxs-lookup"><span data-stu-id="f4b4b-125">Comments</span></span>
- <span data-ttu-id="f4b4b-126">Arviot</span><span class="sxs-lookup"><span data-stu-id="f4b4b-126">Estimates</span></span>
- <span data-ttu-id="f4b4b-127">Arvioitu aloituspäivä: Tämä on päivämäärä, jolloin projekti luodaan kopiosta.</span><span class="sxs-lookup"><span data-stu-id="f4b4b-127">Estimated Start Date: This is the date that the project is created from the copy.</span></span>
- <span data-ttu-id="f4b4b-128">Arvioitu päättymispäivä: Tätä päivämäärää säädetään kopiosta luodun uuden projektin aloituspäivän perusteella.</span><span class="sxs-lookup"><span data-stu-id="f4b4b-128">Estimated Finish Date: This date is adjusted based on the start date of the new project that was made from the copy.</span></span>
- <span data-ttu-id="f4b4b-129">Työmäärä (tuntia)</span><span class="sxs-lookup"><span data-stu-id="f4b4b-129">Effort (Hours)</span></span>
- <span data-ttu-id="f4b4b-130">Arvioidut työvoimakustannukset</span><span class="sxs-lookup"><span data-stu-id="f4b4b-130">Estimated Labor Cost</span></span>
- <span data-ttu-id="f4b4b-131">Arvioidut kulujen kustannukset</span><span class="sxs-lookup"><span data-stu-id="f4b4b-131">Estimated Expense Cost</span></span>
- <span data-ttu-id="f4b4b-132">Arvioidut materiaalikustannukset</span><span class="sxs-lookup"><span data-stu-id="f4b4b-132">Estimated Material Cost</span></span>

> [!NOTE]
> <span data-ttu-id="f4b4b-133">Projektin kopiointi on pitkäkestoinen toiminto.</span><span class="sxs-lookup"><span data-stu-id="f4b4b-133">Copy project is a long running operation.</span></span> <span data-ttu-id="f4b4b-134">Myös projektitietueet, niihin liittyvät määritteet ja monet asiaan liittyvät entiteetit kopioidaan.</span><span class="sxs-lookup"><span data-stu-id="f4b4b-134">Project records, their relevant attributes, and many related entities are also copied.</span></span> <span data-ttu-id="f4b4b-135">Koska toiminto on pitkäkestoinen, kohdeprojektin sivu lukitaan kopioinnin alkamisen jälkeen muokkausten estämiseksi, kunnes kopiointitoiminto on valmis.</span><span class="sxs-lookup"><span data-stu-id="f4b4b-135">Because of the long running nature of the operation, after the copy starts, the target project page is locked for editing until the copy operation is complete.</span></span>

## <a name="work-breakdown-structure"></a><span data-ttu-id="f4b4b-136">Työrakenne</span><span class="sxs-lookup"><span data-stu-id="f4b4b-136">Work breakdown structure</span></span>

<span data-ttu-id="f4b4b-137">Kun projekti kopioidaan, koko resursseillä täytetty työrakenne kopioidaan.</span><span class="sxs-lookup"><span data-stu-id="f4b4b-137">When the project is copied, the entire resource-loaded work breakdown structure is copied.</span></span> <span data-ttu-id="f4b4b-138">Nimetyt resurssit korvataan yleisillä resursseilla.</span><span class="sxs-lookup"><span data-stu-id="f4b4b-138">Named resources are replaced with generic resources.</span></span> <span data-ttu-id="f4b4b-139">Jos nimettyjen resurssien työaika ei ole sama kuin yleisellä resurssilla, aikataulu lasketaan uudelleen ja tehtävien kestot voivat muuttua.</span><span class="sxs-lookup"><span data-stu-id="f4b4b-139">If the named resources don't have the same working hours as the generic resource, the schedule will be recalculated and task durations may change.</span></span>

## <a name="project-team-members"></a><span data-ttu-id="f4b4b-140">Projektiryhmän jäsenet</span><span class="sxs-lookup"><span data-stu-id="f4b4b-140">Project team members</span></span>

<span data-ttu-id="f4b4b-141">Kun projektiryhmä kopioidaan lähdeprojektista, yleiset resurssit kopioidaan.</span><span class="sxs-lookup"><span data-stu-id="f4b4b-141">When a project team is copied from the source project, the generic resources are copied.</span></span> <span data-ttu-id="f4b4b-142">Yleisten resurssien kohdennukset myös säilytetään sellaisina, kuin ne olivat lähdeprojektissa.</span><span class="sxs-lookup"><span data-stu-id="f4b4b-142">Generic resource assignments are also maintained as they were in the source project.</span></span> <span data-ttu-id="f4b4b-143">Nimetyt resurssit muunnetaan yleisiksi ryhmän jäseniksi.</span><span class="sxs-lookup"><span data-stu-id="f4b4b-143">Named resources will be converted to generic team members.</span></span>

## <a name="estimates"></a><span data-ttu-id="f4b4b-144">Arviot</span><span class="sxs-lookup"><span data-stu-id="f4b4b-144">Estimates</span></span>

<span data-ttu-id="f4b4b-145">Kun projekti kopioidaan, resurssien, kulujen ja materiaaliarvioiden rivit kopioidaan lähdeprojektista.</span><span class="sxs-lookup"><span data-stu-id="f4b4b-145">When the project is copied, resource, expense and material estimate lines are copied from the source project.</span></span> 

<span data-ttu-id="f4b4b-146">Lisätietoja projektin kopioinnin ohjelmallisesta käyttämisestä on ohjeaiheessa [Projektimallien kehittäminen projektin kopioinnin avulla](dev-copy-project.md).</span><span class="sxs-lookup"><span data-stu-id="f4b4b-146">For information on how to programmatically access Copy Project, see [Develop project templates with Copy Project](dev-copy-project.md).</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
