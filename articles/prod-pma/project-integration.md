---
title: Microsoft Project Client -integraatio
description: Projektin aikataulun suunnitteleminen ja ylläpitäminen voi olla haastavaa, joten projektipäälliköiden on käytettävä työkaluja, joiden avulla he voivat hallita tätä tehtävää. Microsoft Project Clientiin integrointi tukee projektin työrakenteen avaamista ja hallintaa.
author: Yowelle
manager: AnnBe
ms.date: 12/11/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjWbsTemplate
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2017-12-04
ms.dyn365.ops.version: 7.2999999999999998
ms.openlocfilehash: e93d23559d1f3aca9022cd97dae3b0726bb5ca05
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5289320"
---
# <a name="microsoft-project-client-integration"></a><span data-ttu-id="28762-104">Microsoft Project Client -integraatio</span><span class="sxs-lookup"><span data-stu-id="28762-104">Microsoft Project client integration</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="28762-105">Projektin aikataulun suunnitteleminen ja ylläpitäminen voi olla haastavaa, joten projektipäälliköiden on käytettävä työkaluja, joiden avulla he voivat hallita tätä tehtävää.</span><span class="sxs-lookup"><span data-stu-id="28762-105">Planning and maintaining a project schedule can be complex, so project managers need to use tools that help them manage this task.</span></span> <span data-ttu-id="28762-106">Microsoft Project Clientiin integrointi tukee projektin työrakenteen avaamista ja hallintaa.</span><span class="sxs-lookup"><span data-stu-id="28762-106">Integration with Microsoft Project Client provides support to open and manage a project work breakdown structure.</span></span> <span data-ttu-id="28762-107">Projektipäällikkö voi julkaista muutokset takaisin Dynamics 365 Finance -projektin työrakenteeseen.</span><span class="sxs-lookup"><span data-stu-id="28762-107">The project manager can publish any changes back to the Dynamics 365 Finance project work breakdown structure.</span></span>

> [!NOTE]
> <span data-ttu-id="28762-108">Jos käytössä on heinäkuun päivitys (versio 10.0.4), on asennettava tietokannat 4054797 ja 4055884.</span><span class="sxs-lookup"><span data-stu-id="28762-108">If you are using the July update (version 10.0.4), you must install KB 4054797 and 4055884.</span></span>

## <a name="configure-the-microsoft-project-client-add-in"></a><span data-ttu-id="28762-109">Microsoft Project Client -lisäosan määrittäminen</span><span class="sxs-lookup"><span data-stu-id="28762-109">Configure the Microsoft Project Client add-in</span></span>
<span data-ttu-id="28762-110">Microsoft Project Clientiin integroinnin käyttöönottoa varten on asennettava Microsoft Dynamics 365 -lisäosa käyttäjän Microsoft Project -asiakassovellusta.</span><span class="sxs-lookup"><span data-stu-id="28762-110">To enable the integration with Microsoft Project Client, a Microsoft Dynamics 365 add-in is required to be installed in the user’s client Microsoft Project application.</span></span> <span data-ttu-id="28762-111">Tämä tehdään avaamalla **Projektinhallinnan työtila**.</span><span class="sxs-lookup"><span data-stu-id="28762-111">This is done by opening the **Project management workspace**.</span></span>

<span data-ttu-id="28762-112">•   Valitse **Määritä projektin asiakaslisäosa** työtilan osassa **Linkit** > **Määritys**.</span><span class="sxs-lookup"><span data-stu-id="28762-112">•   Click **Configure project client add-in** from the **Links** > **Setup** section of the workspace.</span></span>

<span data-ttu-id="28762-113">•   Valitse **Avaa** ja sitten kehotteesta **Suorita**.</span><span class="sxs-lookup"><span data-stu-id="28762-113">•   Click **Open**, then click **Run** when prompted.</span></span>

## <a name="open-and-edit-an-existing-draft-work-breakdown-structure-in-microsoft-project-client"></a><span data-ttu-id="28762-114">Olemassa olevan työrakenneluonnoksen avaaminen ja muokkaus Microsoft Project Clientissä</span><span class="sxs-lookup"><span data-stu-id="28762-114">Open and edit an existing draft work breakdown structure in Microsoft Project Client</span></span>
<span data-ttu-id="28762-115">Jos Dynamics 365 Financessa olevalle projektille on jo luotu työrakenne, se voidaan avata o luodulle projektille on luotu työn erittely rakenne, työerittely rakenne voidaan avata Microsoft Project Client -sovelluksessa, jos työrakenne on luonnostilassa.</span><span class="sxs-lookup"><span data-stu-id="28762-115">If a project in Dynamics 365 Finance already has a work breakdown structure created, the work breakdown structure can be opened in the Microsoft Project Client application if the work breakdown structure is in a draft status.</span></span> <span data-ttu-id="28762-116">Avaa **Projekti**-sivulta valitsemalla **Avaa Microsoft Projectissa** -linkki **Suunnitelma**-välilehdestä. Tämä sivu voidaan avata myös Microsoft Project Client -sovelluksesta valitsemalla **Avaa** **Microsoft Dynamics 365** -välilehdestä. Valitse luettelosta **Oikeushenkilö** ja **Projekti**.</span><span class="sxs-lookup"><span data-stu-id="28762-116">To open from the **Project** page, click **Open in Microsoft Project** link from the **Plan** tab. This page can also be opened from within the Microsoft Project Client application by clicking **Open** in the **Microsoft Dynamics 365** tab. Select the **Legal entity** and **Project** from the list.</span></span>

> [!NOTE]
> <span data-ttu-id="28762-117">Jos käytät Internet Explorer -selainta, sinun on valittava **Tallenna** avataksesi manuaalisesti tiedoston lataussijainnista.</span><span class="sxs-lookup"><span data-stu-id="28762-117">If you're using Internet Explorer as your browser, you will need to click **Save** to manually open from the location that the file is downloaded to.</span></span> <span data-ttu-id="28762-118">Tai **Tallenna ja avaa** avataksesi tidoston Microsoft Project Clientissa.</span><span class="sxs-lookup"><span data-stu-id="28762-118">Or, click **Save and open** to open the file in Microsoft Project Client.</span></span> <span data-ttu-id="28762-119">Älä nimeä tiedostoa uudelleen tallennettaessa.</span><span class="sxs-lookup"><span data-stu-id="28762-119">Do not rename the file name when saving.</span></span>

<span data-ttu-id="28762-120">Ennen kuin teet tiedostoon muutoksia Microsoft Project Client -ohjelmalla, sinun on kuitattava se ulos. Valitse **Kuittaa ulos** **Microsoft Dynamics 365** -välilehdessä. Tämä estää muita käyttäjiä muokkaamasta työrakennetta Financessa samalla.</span><span class="sxs-lookup"><span data-stu-id="28762-120">Before making any edits to the file using Microsoft Project Client, you need to check it out. Click **Check out** in the **Microsoft Dynamics 365** tab. This will prevent other users from editing the work breakdown structure from within Finance at the same time.</span></span> <span data-ttu-id="28762-121">Jos haluat julkaista työrakenteen muokkaamisen jälkeen, valitse **Kuittaa sisään** **Microsoft Dynamics 365** -välilehdessä.</span><span class="sxs-lookup"><span data-stu-id="28762-121">To publish the work breakdown structure after completing any edits, click **Check in** on the **Microsoft Dynamics 365** tab.</span></span>

<span data-ttu-id="28762-122">Jos projektiin on jo lisätty projektiryhmä Financessa, resurssiluetteloon täytetään ryhmän jäsenet.</span><span class="sxs-lookup"><span data-stu-id="28762-122">If a project team has already been added to the project in Finance, the resource list will be populated with the team members.</span></span> <span data-ttu-id="28762-123">Jos projektiryhmää ei ole vielä lisätty projektiin, voit valita resursseja ja luoda ryhmän Microsoft Project Client -ohjelmassa napsauttamalla **Resurssit**-painiketta **Microsoft Dynamics 365** -välilehdessä.</span><span class="sxs-lookup"><span data-stu-id="28762-123">If a project team has not yet been added to the project, you can select resources and build the team within Microsoft Project Client by clicking the **Resources** button on the **Microsoft Dynamics 365** tab.</span></span> 

<span data-ttu-id="28762-124">Seuraavat tiedot synkronoidaan takaisin Financeen osana sisäänkuittausprosessia:</span><span class="sxs-lookup"><span data-stu-id="28762-124">The following data will be synced back to Finance as part of the check-in process:</span></span>

<span data-ttu-id="28762-125">•   Tehtävän nimi</span><span class="sxs-lookup"><span data-stu-id="28762-125">•   Task name</span></span>

<span data-ttu-id="28762-126">•   Alkamispäivä</span><span class="sxs-lookup"><span data-stu-id="28762-126">•   Start date</span></span>

<span data-ttu-id="28762-127">•   Päättymispäivä</span><span class="sxs-lookup"><span data-stu-id="28762-127">•   Finish date</span></span>

<span data-ttu-id="28762-128">•   Edeltäjät</span><span class="sxs-lookup"><span data-stu-id="28762-128">•   Predecessors</span></span>

<span data-ttu-id="28762-129">•   Resurssinimet</span><span class="sxs-lookup"><span data-stu-id="28762-129">•   Resource names</span></span>

<span data-ttu-id="28762-130">•   Luokka</span><span class="sxs-lookup"><span data-stu-id="28762-130">•   Category</span></span>

<span data-ttu-id="28762-131">•   Resurssiluokka</span><span class="sxs-lookup"><span data-stu-id="28762-131">•   Resource category</span></span>

<span data-ttu-id="28762-132">•   Työajat</span><span class="sxs-lookup"><span data-stu-id="28762-132">•   Work hours</span></span>

<span data-ttu-id="28762-133">•   Muistiinpanot</span><span class="sxs-lookup"><span data-stu-id="28762-133">•   Notes</span></span>

<span data-ttu-id="28762-134">•   Prioriteetti</span><span class="sxs-lookup"><span data-stu-id="28762-134">•   Priority</span></span>

> [!NOTE]
> <span data-ttu-id="28762-135">Jos lisäät Microsoft Project Client -tiedostoon muita sarakkeita, niitä ei tallenneta tiedostoon eikä niitä näytetä, kun tiedosto avataan uudelleen.</span><span class="sxs-lookup"><span data-stu-id="28762-135">If you add any other columns to your Microsoft Project Client file, they will not be saved to the file and will not be displayed when the file is opened again.</span></span>

## <a name="create-the-work-breakdown-structure-for-an-existing-project-using-microsoft-project-client"></a><span data-ttu-id="28762-136">Työrakenteen luominen olemassa olevalle projektille Microsoft Project Client -ohjelmalla</span><span class="sxs-lookup"><span data-stu-id="28762-136">Create the work breakdown structure for an existing project using Microsoft Project Client</span></span>
<span data-ttu-id="28762-137">Voit luoda uuden työrakenteen Microsoft Project Client -ohjelmalla seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="28762-137">To create a new work breakdown structure using Microsoft Project Client, follow these steps:</span></span>


1.  <span data-ttu-id="28762-138">Avaa Microsoft Project Client.</span><span class="sxs-lookup"><span data-stu-id="28762-138">Open Microsoft Project Client.</span></span>

2.  <span data-ttu-id="28762-139">Valitse **Microsoft Dynamics 365** -välilehdessä **Avaa**.</span><span class="sxs-lookup"><span data-stu-id="28762-139">On the **Microsoft Dynamics 365** tab, click **Open**.</span></span>

3.  <span data-ttu-id="28762-140">Valitse projektin **Oikeushenkilö**.</span><span class="sxs-lookup"><span data-stu-id="28762-140">Select the **Legal entity** for the project.</span></span>

4.  <span data-ttu-id="28762-141">Valitse **Projekti**.</span><span class="sxs-lookup"><span data-stu-id="28762-141">Select the **Project**.</span></span>

5.  <span data-ttu-id="28762-142">Valitse **Microsoft Dynamics 365** -välilehdessä **Kuitta ulos**.</span><span class="sxs-lookup"><span data-stu-id="28762-142">Click **Check out** on the **Microsoft Dynamics 365** tab.</span></span>

6.  <span data-ttu-id="28762-143">Kun olet valmis julkaisemaan Financeen, valitse **Microsoft Dynamics 365** -välilehdessä **Kuittaa sisään**.</span><span class="sxs-lookup"><span data-stu-id="28762-143">When ready to publish to Finance, click **Check in** on the **Microsoft Dynamics 365** tab.</span></span>

## <a name="replace-the-existing-work-breakdown-structure-for-an-existing-project-using-microsoft-project-client"></a><span data-ttu-id="28762-144">Olemassa olevan työrakenteen korvaaminen olemassa olevalle projektille Microsoft Project Client -ohjelmalla</span><span class="sxs-lookup"><span data-stu-id="28762-144">Replace the existing work breakdown structure for an existing project using Microsoft Project Client</span></span>
<span data-ttu-id="28762-145">Voit luoda uuden työrakenteen Microsoft Project Client -ohjelmalla ja korvata olemassa olevan projektin olemassa olevan työrakenteen seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="28762-145">To create a new work breakdown structure using Microsoft Project Client and replace an existing work breakdown structure for an existing project, follow these steps:</span></span>

1.  <span data-ttu-id="28762-146">Avaa Microsoft Project Client.</span><span class="sxs-lookup"><span data-stu-id="28762-146">Open the Microsoft Project Client.</span></span>

2.  <span data-ttu-id="28762-147">Luo aikataulu Microsoft Project Client -ohjelmassa.</span><span class="sxs-lookup"><span data-stu-id="28762-147">Create the schedule in Microsoft Project Client.</span></span>

3.  <span data-ttu-id="28762-148">Valitse **Microsoft Dynamics 365** -välilehdessä **Tallenna muutokset** > **Korvaa olemassa oleva projekti**.</span><span class="sxs-lookup"><span data-stu-id="28762-148">On the **Microsoft Dynamics 365** tab, click **Save changes** > **Replace existing project**.</span></span>

4.  <span data-ttu-id="28762-149">Valitse projektin **Oikeushenkilö**.</span><span class="sxs-lookup"><span data-stu-id="28762-149">Select the **Legal entity** for the project.</span></span>

5.  <span data-ttu-id="28762-150">Valitse **Projekti**.</span><span class="sxs-lookup"><span data-stu-id="28762-150">Select the **Project**.</span></span>

6.  <span data-ttu-id="28762-151">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="28762-151">Click **OK**.</span></span>

## <a name="create-a-new-project-from-within-microsoft-project-client"></a><span data-ttu-id="28762-152">Uuden projektin luominen Microsoft Project Client -ohjelmassa</span><span class="sxs-lookup"><span data-stu-id="28762-152">Create a new project from within Microsoft Project Client</span></span>


1.  <span data-ttu-id="28762-153">Avaa Microsoft Project Client.</span><span class="sxs-lookup"><span data-stu-id="28762-153">Open the Microsoft Project Client.</span></span>

2.  <span data-ttu-id="28762-154">Luo aikataulu Microsoft Project Client -ohjelmassa.</span><span class="sxs-lookup"><span data-stu-id="28762-154">Create the schedule in Microsoft Project Client.</span></span>

3.  <span data-ttu-id="28762-155">Valitse **Microsoft Dynamics 365** -välilehdessä **Tallenna muutokset** > **Tallenna uuteen projektiin**.</span><span class="sxs-lookup"><span data-stu-id="28762-155">On the **Microsoft Dynamics 365** tab, click **Save changes** > **Save to new Project**.</span></span>

4.  <span data-ttu-id="28762-156">Valitse projektin **Oikeushenkilö**.</span><span class="sxs-lookup"><span data-stu-id="28762-156">Select the **Legal entity** for the project.</span></span>

5.  <span data-ttu-id="28762-157">Syötä **Projektitunnus** tarvittaessa.</span><span class="sxs-lookup"><span data-stu-id="28762-157">Enter the **Project ID**, if necessary.</span></span>

6.  <span data-ttu-id="28762-158">Syötä **Projektin nimi**.</span><span class="sxs-lookup"><span data-stu-id="28762-158">Enter the **Project name**.</span></span>

7.  <span data-ttu-id="28762-159">Valitse **Projektityyppi**, **Projektiryhmä** ja **Projektisopimuksen tunnus**.</span><span class="sxs-lookup"><span data-stu-id="28762-159">Select the **Project type**, **Project group** and the **Project contract ID**.</span></span> <span data-ttu-id="28762-160">Voit vaihtoehtoisesti luoda uuden projektisopimuksen valitsemalla **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="28762-160">Alternatively, you can create a new project contract by clicking **New**.</span></span>

8.  <span data-ttu-id="28762-161">Valitse resursoinnissa käytettävä **kalenteri**.</span><span class="sxs-lookup"><span data-stu-id="28762-161">Select the **Calendar** to be used for resourcing.</span></span>

11. <span data-ttu-id="28762-162">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="28762-162">Click **OK**.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]