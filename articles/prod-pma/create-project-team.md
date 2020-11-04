---
title: Luo projektiryhmä
description: Tässä aiheessa on tietoja projektiryhmien luomisesta ja hallinnasta.
author: Yowelle
manager: AnnBe
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: kdwns
ms.search.scope: Core, Operations
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a7eb9101352afd27b527bf6b8acc6f92198f44ea
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/16/2020
ms.locfileid: "4075513"
---
# <a name="create-a-project-team"></a><span data-ttu-id="9fee4-103">Projektitiimin luominen</span><span class="sxs-lookup"><span data-stu-id="9fee4-103">Create a project team</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9fee4-104">Jotta projektipäällikkö voisi käyttää aiemmin projektissa määritettyjä rooleja, hänen on osoitettava roolit projektille.</span><span class="sxs-lookup"><span data-stu-id="9fee4-104">To use the roles that were previously set up in a project, a project manager must associate the roles with the project.</span></span> <span data-ttu-id="9fee4-105">Projektille voidaan osoittaa useita rooleja.</span><span class="sxs-lookup"><span data-stu-id="9fee4-105">Multiple roles can be assigned for a project.</span></span> <span data-ttu-id="9fee4-106">Sekaannusten välttämiseksi näille rooleille määritetään automaattisesti otsikko varauksen aikana.</span><span class="sxs-lookup"><span data-stu-id="9fee4-106">To prevent confusion, these roles are automatically labeled during reservation.</span></span> <span data-ttu-id="9fee4-107">Jos projektipäällikkö tarvitsee kolmea ohjelmistosuunnittelijaa, luodaan automaattisesti kolme ohjelmistosuunnittelijan roolia, joiden otsikot ovat **ohjelmistosuunnittelija 1** , **ohjelmistosuunnittelija 2** ja **ohjelmistosuunnittelija 3**.</span><span class="sxs-lookup"><span data-stu-id="9fee4-107">For example, if the project manager requires three software engineers, three Software engineer roles that have **software engineer 1** , **software engineer 2** , and **software engineer 3** as their labels are automatically generated.</span></span> <span data-ttu-id="9fee4-108">Jos roolille on aiemmin määritetty rooliominaisuudet, niitä käytetään suodattimena resurssin haun aikana.</span><span class="sxs-lookup"><span data-stu-id="9fee4-108">If role characteristics were previously set for the role, they are applied as a filter during searches for a resource.</span></span> <span data-ttu-id="9fee4-109">Lisäominaisuuksia voidaan lisätä tarpeen mukaan haun tarkentamiseksi.</span><span class="sxs-lookup"><span data-stu-id="9fee4-109">Additional characteristics can be added as required to further refine the search.</span></span>

<span data-ttu-id="9fee4-110">Näkymäasetuksia voi myös mukauttaa paremman kuvan antamiseksi resurssien käytettävyydestä.</span><span class="sxs-lookup"><span data-stu-id="9fee4-110">View settings can also be customized to give a better view of resource availability.</span></span> <span data-ttu-id="9fee4-111">Käytettävyys voidaan esittää tunneittain, viikoittain, kuukausittain, neljännesvuosittain ja vuosittain.</span><span class="sxs-lookup"><span data-stu-id="9fee4-111">There are options to show hourly, daily, weekly, monthly, quarterly, and annual availability.</span></span> <span data-ttu-id="9fee4-112">Myös resurssien käytettävissä oleva ja jäljellä oleva kapasiteetti voidaan näyttää.</span><span class="sxs-lookup"><span data-stu-id="9fee4-112">There is also an option to show available and remaining capacity on resources.</span></span> <span data-ttu-id="9fee4-113">Tästä vaihtoehdosta on hyötyä ajanhallinnassa, kun arvioit aktiviteetteihin käytettävissä olevaa aikaa tai resurssien käytettävyyttä.</span><span class="sxs-lookup"><span data-stu-id="9fee4-113">This option is useful for time management, when you're estimating available time for activities or resource availability.</span></span>

<span data-ttu-id="9fee4-114">Projektipäällikkö voi valita sivulla roolin ja sitten, jos vaatimuksen täyttävä resurssi on käytettävissä, päättää varata resurssin täyttämään kyseinen rooli.</span><span class="sxs-lookup"><span data-stu-id="9fee4-114">The project manager can select a role on the page and then, if there is an available resource that fits the requirement, select to reserve a resource to fill the role.</span></span> <span data-ttu-id="9fee4-115">Huomaa, että resursseja ei tarvitse varata tässä kohtaa suunnitteluvaihetta.</span><span class="sxs-lookup"><span data-stu-id="9fee4-115">Note that the resources don't have to be reserved at this point in the planning stage.</span></span> <span data-ttu-id="9fee4-116">Kun luot työrakennemallin, voit korvata roolit projektin henkilöresursseilla.</span><span class="sxs-lookup"><span data-stu-id="9fee4-116">When you create a WBS, you can replace roles with staffed resources for the project.</span></span> <span data-ttu-id="9fee4-117">Jos roolit korvataan työrakenteessa henkilöresursseilla, resurssien määritys päivittää automaattisesti projektitiimiluettelon ja aikataulutuksen.</span><span class="sxs-lookup"><span data-stu-id="9fee4-117">If roles are replaced with staffed resources in the WBS, the resource setup automatically updates the project team listing and scheduling.</span></span>

<span data-ttu-id="9fee4-118">[![Projektitiimin luettelo, joka sisältää sekä roolit että todelliset resurssit](./media/projectresourcing03-1024x368.jpg)](./media/projectresourcing03.jpg)</span><span class="sxs-lookup"><span data-stu-id="9fee4-118">[![Project team listing that includes both roles and actual resources](./media/projectresourcing03-1024x368.jpg)](./media/projectresourcing03.jpg)</span></span> 

<span data-ttu-id="9fee4-119">Projektipäälliköllä on useita vaihtoehtoja resurssin varaamiseen projektia varten, kuten **Jäljellä oleva kapasiteetti** , **Koko kapasiteetti** , **Prosenttiosuus kapasiteetista** ja **Työtuntien määritys**.</span><span class="sxs-lookup"><span data-stu-id="9fee4-119">The project manager has various options for booking a resource for a project, such as **Remaining capacity** , **Full capacity** , **Capacity percentage** , and **Specify hours**.</span></span> <span data-ttu-id="9fee4-120">Nämä varausvaihtoehdot voidaan peruuttaa milloin tahansa, jos resurssiosoitukset muuttuvat.</span><span class="sxs-lookup"><span data-stu-id="9fee4-120">These booking options can be canceled at any time if resource assignments change.</span></span> <span data-ttu-id="9fee4-121">Kahdenlaisia varauksia tuetaan:</span><span class="sxs-lookup"><span data-stu-id="9fee4-121">Two types of booking are supported:</span></span>

- <span data-ttu-id="9fee4-122">**Sitova varaus** – Resurssin varaus on hyväksytty ja vahvistettu työskentelemään kiinnityksessä määritetyn keston ajan.</span><span class="sxs-lookup"><span data-stu-id="9fee4-122">**Hard Book** – The resource reservation was approved and confirmed to work on the engagement for the specified duration.</span></span>
- <span data-ttu-id="9fee4-123">**Alustava** – Resurssin varaukset on alustettavasti määritetty työskentelemään kiinnityksessä määritetyn keston ajan.</span><span class="sxs-lookup"><span data-stu-id="9fee4-123">**Soft book** – The resource reservations was tentatively set to work on the engagement for the specified duration.</span></span>

<span data-ttu-id="9fee4-124">Seuraava menettely selittää, miten projektitiimi luodaan.</span><span class="sxs-lookup"><span data-stu-id="9fee4-124">The following procedure explains how to create a project team.</span></span>

## <a name="create-a-project-team"></a><span data-ttu-id="9fee4-125">Projektitiimin luominen</span><span class="sxs-lookup"><span data-stu-id="9fee4-125">Create a project team</span></span>

1. <span data-ttu-id="9fee4-126">Valitse **Kaikki projektit** -luettelosivulta projekti ja valitse sitten **Muokkaa**.</span><span class="sxs-lookup"><span data-stu-id="9fee4-126">On the **All projects** list page, select a project, and then select **Edit**.</span></span>
2. <span data-ttu-id="9fee4-127">Syötä **Projektitiimi ja aikataulutus** -välilehden **Aikataulun päättymispäivä** -kenttään aikataulun alkamispäivä plus yksi kuukausi.</span><span class="sxs-lookup"><span data-stu-id="9fee4-127">On the **Project team and scheduling** tab, in the **Schedule end date** field, enter the schedule start date plus one month.</span></span> <span data-ttu-id="9fee4-128">Jos aikataulu esimerkiksi alkaa 24. kesäkuuta 2017 (24.6.2017), syötä **24.7.2017**.</span><span class="sxs-lookup"><span data-stu-id="9fee4-128">For example, if the schedule start date is June 24, 2017 (24/06/2017), enter **24/07/2017**.</span></span>
3. <span data-ttu-id="9fee4-129">Valitse **Lisää**.</span><span class="sxs-lookup"><span data-stu-id="9fee4-129">Select **Add**.</span></span>
4. <span data-ttu-id="9fee4-130">Valitse **Lisää rooleja projektiin** -ruudun **Rooli** -kentässä **Projektipäällikkö**.</span><span class="sxs-lookup"><span data-stu-id="9fee4-130">In the **Add roles to the project** pane, in the **Role** field, select **Senior Project Manager**.</span></span>
5. <span data-ttu-id="9fee4-131">Valitse **Vaadittavat pätevyydet**.</span><span class="sxs-lookup"><span data-stu-id="9fee4-131">Select **Required competencies**.</span></span>
6. <span data-ttu-id="9fee4-132">**Valitse ominaisuudet** -sivulla ovat oletusarvoisesti valittuna ne ominaisuudet, jotka olet aiemmin määrittänyt projektipäällikön roolille.</span><span class="sxs-lookup"><span data-stu-id="9fee4-132">On the **Choose characteristics** page, the characteristics that you previously set for the Senior project manager role are selected by default.</span></span> <span data-ttu-id="9fee4-133">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="9fee4-133">Select **OK**.</span></span>
7. <span data-ttu-id="9fee4-134">Kirjoita **Lisää rooleja projektiin** -sivun **Resurssien määrä** -kenttään **1**.</span><span class="sxs-lookup"><span data-stu-id="9fee4-134">On the **Add roles to project** page, in the **Number of resources** field, enter **1**.</span></span>
8. <span data-ttu-id="9fee4-135">Haku näyttää **Resurssi** -kentässä kaikki resurssit, joilla on vaadittavat pätevyydet.</span><span class="sxs-lookup"><span data-stu-id="9fee4-135">In the **Resource** field, the lookup shows all resources that have the required competencies.</span></span> <span data-ttu-id="9fee4-136">Valitse **Taneli Kultaranta** ja sitten **Luo**.</span><span class="sxs-lookup"><span data-stu-id="9fee4-136">Select **Daniel Goldschmidt** , and then select **Create**.</span></span>
9. <span data-ttu-id="9fee4-137">Valitse **Projekti** -sivulla **Lisää**.</span><span class="sxs-lookup"><span data-stu-id="9fee4-137">On the **Project** page, select **Add**.</span></span>
10. <span data-ttu-id="9fee4-138">Valitse **Lisää rooleja projektiin** -ruudun **Rooli** -kentässä **Tiiminjäsen**.</span><span class="sxs-lookup"><span data-stu-id="9fee4-138">In the **Add roles to the project** pane, in the **Role** field, select **Team member**.</span></span> <span data-ttu-id="9fee4-139">Syötä **Resurssien määrä** -kenttään **5**.</span><span class="sxs-lookup"><span data-stu-id="9fee4-139">In the **Number of resources** field, enter **5**.</span></span>
11. <span data-ttu-id="9fee4-140">Valitse **Luo**.</span><span class="sxs-lookup"><span data-stu-id="9fee4-140">Select **Create**.</span></span>
12. <span data-ttu-id="9fee4-141">Valitse **Projektit** -sivulla **Täytä resurssi**.</span><span class="sxs-lookup"><span data-stu-id="9fee4-141">On the **Projects** page, select **Fulfill resource**.</span></span>

## <a name="monitor-project-teams"></a><span data-ttu-id="9fee4-142">Projektitiimien seuraaminen</span><span class="sxs-lookup"><span data-stu-id="9fee4-142">Monitor project teams</span></span>
1. <span data-ttu-id="9fee4-143">Valitse **Kaikki projektit** -sivulla **XYZ-päivityksen vaihe 2** -projektin **Projektitunnus** -linkki.</span><span class="sxs-lookup"><span data-stu-id="9fee4-143">On the **All projects** page, select the **Project ID** link for the **XYZ Upgrade Phase 2** project.</span></span>
2. <span data-ttu-id="9fee4-144">Varmista **Projektitiimi ja aikataulutus** -pikavälilehdessä, että luettelossa olevat projektiresurssit ovat oikein.</span><span class="sxs-lookup"><span data-stu-id="9fee4-144">On the **Project team and scheduling** FastTab, verify that the project resources that are listed are correct.</span></span>
