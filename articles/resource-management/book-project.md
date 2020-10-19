---
title: Projektin varaaminen
description: Tässä aiheessa on tietoja resurssin varaamisesta projektiin.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 19128264ed3db7efeeba948155f0ddbdc806c2a0
ms.sourcegitcommit: 56c42d7f5995a674426a1c2a81bae897dceb391c
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/01/2020
ms.locfileid: "3908085"
---
# <a name="book-to-a-project"></a><span data-ttu-id="5076a-103">Projektin varaaminen</span><span class="sxs-lookup"><span data-stu-id="5076a-103">Book to a project</span></span>

<span data-ttu-id="5076a-104">_**Koskee:** Project Operationsin resurssiin / muuhun kuin resurssiin perustuvia skenaarioita, Lite-käyttöönotto-kaupasta proformalaskutukseen_</span><span class="sxs-lookup"><span data-stu-id="5076a-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="5076a-105">Joskus projektipäällikön tai resurssipäällikön on kohdistettava resurssi projektiin, jossa ei ole määritetty tiettyä vaatimusta yleiselle ryhmän jäsenelle.</span><span class="sxs-lookup"><span data-stu-id="5076a-105">There are times where a Project manager or Resource manager will need to allocate a resource to project without a specific requirement being defined from a generic team member.</span></span> <span data-ttu-id="5076a-106">Tämä voidaan saavuttaa kolmella eri tavalla.</span><span class="sxs-lookup"><span data-stu-id="5076a-106">This can be achieved in one of three ways.</span></span>

- <span data-ttu-id="5076a-107">Varaa ryhmän jäsenen ruudukosta</span><span class="sxs-lookup"><span data-stu-id="5076a-107">Book from the team member grid</span></span>
- <span data-ttu-id="5076a-108">Varaus aikataulutaulukosta</span><span class="sxs-lookup"><span data-stu-id="5076a-108">Book from the schedule board</span></span>
- <span data-ttu-id="5076a-109">Varaa **Projekti**-lomakkeesta</span><span class="sxs-lookup"><span data-stu-id="5076a-109">Book from the **Project** form</span></span>

## <a name="book-from-the-team-member-grid"></a><span data-ttu-id="5076a-110">Varaa ryhmän jäsenen ruudukosta</span><span class="sxs-lookup"><span data-stu-id="5076a-110">Book from the team member grid</span></span>

<span data-ttu-id="5076a-111">Jos organisaatiosi toimii resussien hybridikohdistustilassa, projektipäällikkö voi varata resurssin suoraan projektiin suorittamalla seuraavat vaiheet.</span><span class="sxs-lookup"><span data-stu-id="5076a-111">If your organization is operating in hybrid Resource allocation mode, the Project manager can book a resource directly to the project by completing the following steps.</span></span>

1. <span data-ttu-id="5076a-112">Siirry projektista tiimin jäsenen ruudukkoon ja valitse **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="5076a-112">From the project, go to the team member grid and select **New**.</span></span>
2. <span data-ttu-id="5076a-113">Määritä toimen nimi ja resurssin rooli.</span><span class="sxs-lookup"><span data-stu-id="5076a-113">Define the position name and the role of the resource.</span></span>
3. <span data-ttu-id="5076a-114">Valitse varattavissa oleva resurssi käytettävissä olevasta valintaluettelosta.</span><span class="sxs-lookup"><span data-stu-id="5076a-114">Select the bookable resource from the available lookup.</span></span>
4. <span data-ttu-id="5076a-115">Kun olet valinnut resurssin, määritä seuraavat kentän tiedot resurssin varaamiseen:</span><span class="sxs-lookup"><span data-stu-id="5076a-115">After you select the resource, define the following field information to book the resource:</span></span>

    - <span data-ttu-id="5076a-116">Alkamispäivä</span><span class="sxs-lookup"><span data-stu-id="5076a-116">Start date</span></span>
    - <span data-ttu-id="5076a-117">Päättymispäivä</span><span class="sxs-lookup"><span data-stu-id="5076a-117">Finish date</span></span>
    - <span data-ttu-id="5076a-118">Kohdistustapa</span><span class="sxs-lookup"><span data-stu-id="5076a-118">Allocation method</span></span>
    - <span data-ttu-id="5076a-119">Tunnit, jos soveltuu</span><span class="sxs-lookup"><span data-stu-id="5076a-119">Hours, if applicable</span></span>
    - <span data-ttu-id="5076a-120">Projektin hyväksyjä</span><span class="sxs-lookup"><span data-stu-id="5076a-120">Project approver</span></span>

6. <span data-ttu-id="5076a-121">Valitse **Tallenna ja sulje**</span><span class="sxs-lookup"><span data-stu-id="5076a-121">Select **Save and Close**</span></span>

## <a name="book-from-the-schedule-board"></a><span data-ttu-id="5076a-122">Varaus aikataulutaulukosta</span><span class="sxs-lookup"><span data-stu-id="5076a-122">Book from the schedule board</span></span>

<span data-ttu-id="5076a-123">Kun resurssipäällikön pitää varata resurssi suoraan projektiin, hän voi käyttää aikataulutaulukkoa ja projektin tarvetta.</span><span class="sxs-lookup"><span data-stu-id="5076a-123">When a Resource manager needs to book a resource directly to a project, they can use the schedule board and the project requirement.</span></span> <span data-ttu-id="5076a-124">Projektin tarve on resurssitarve, joka on aina käytettävissä varaamista varten.</span><span class="sxs-lookup"><span data-stu-id="5076a-124">The project requirement is a resource requirement that is always available to be booked against.</span></span> <span data-ttu-id="5076a-125">Varaa suoraan projektiin aikataulutaulukosta seuraavalla tavalla.</span><span class="sxs-lookup"><span data-stu-id="5076a-125">To book directly to a project form the schedule board, complete the following steps.</span></span>

1. <span data-ttu-id="5076a-126">Siirry aikataulutaulukkoon ja suodata vasemmanpuoleisella sivulla haluamasi resurssit, joita harkitset tarpeeseen.</span><span class="sxs-lookup"><span data-stu-id="5076a-126">Navigate to the schedule board and on the left page, filter for the resources you are considering for the requirement.</span></span>
2. <span data-ttu-id="5076a-127">Valitse alaruudussa **Projekti**-välilehti, jossa voit tarkastella projektitarpeiden luetteloa.</span><span class="sxs-lookup"><span data-stu-id="5076a-127">In the bottom pane, select the **Project** tab to view a list of project requirements.</span></span>
3. <span data-ttu-id="5076a-128">Vedä tarve resurssin päälle ja määritä seuraavat tiedot:</span><span class="sxs-lookup"><span data-stu-id="5076a-128">Drag the requirement onto a resource and define the following information:</span></span>

    - <span data-ttu-id="5076a-129">Alkamispäivä</span><span class="sxs-lookup"><span data-stu-id="5076a-129">Start date</span></span>
    - <span data-ttu-id="5076a-130">Päättymispäivä</span><span class="sxs-lookup"><span data-stu-id="5076a-130">Finish date</span></span>
    - <span data-ttu-id="5076a-131">Varauksen tila</span><span class="sxs-lookup"><span data-stu-id="5076a-131">Booking status</span></span>
    - <span data-ttu-id="5076a-132">Varaustapa</span><span class="sxs-lookup"><span data-stu-id="5076a-132">Booking method</span></span>
    - <span data-ttu-id="5076a-133">Kesto</span><span class="sxs-lookup"><span data-stu-id="5076a-133">Duration</span></span>

## <a name="book-from-the-project-form"></a><span data-ttu-id="5076a-134">Varaa Projekti-lomakkeesta</span><span class="sxs-lookup"><span data-stu-id="5076a-134">Book from the Project form</span></span>

<span data-ttu-id="5076a-135">Projektipäällikön täytyy ehkä varata resurssi projektiin, mutta vain tietää resurssin ehdot, mutta ei nimeä.</span><span class="sxs-lookup"><span data-stu-id="5076a-135">As a Project manager, you might need to book a resource to a project, but only know the criteria rather than the name of the resource.</span></span> <span data-ttu-id="5076a-136">Suorita seuraavat vaiheet, kun haluat etsiä resurssia käytettävissä olevien määritteiden perusteella ajoitusavustajan avulla.</span><span class="sxs-lookup"><span data-stu-id="5076a-136">Complete the following steps to use the schedule assistant to find a resource based on any available attributes of the resource.</span></span> 

1. <span data-ttu-id="5076a-137">Siirry projektiin ja avaa ajoitusavustaja valitsemalla **Varaa**.</span><span class="sxs-lookup"><span data-stu-id="5076a-137">Navigate to the project and select **Book** to open the Schedule Assistant.</span></span>
2. <span data-ttu-id="5076a-138">Rajaa ehtoja käyttäen ajoitusavustajan vasemmalla puolella olevia suodattimia ja valitse **Hae.**</span><span class="sxs-lookup"><span data-stu-id="5076a-138">Using the filters on the left side of the Schedule Assistant, narrow the criteria and select **Search.**</span></span>
3. <span data-ttu-id="5076a-139">Tuloksissa palautettujen resurssien perusteella voit varata resurssin.</span><span class="sxs-lookup"><span data-stu-id="5076a-139">Based on resources returned in the results, you can book a resource.</span></span>

> [!NOTE]
> <span data-ttu-id="5076a-140">Tämä menetelmä ei luo varauksia resurssille.</span><span class="sxs-lookup"><span data-stu-id="5076a-140">This method doesn't create any bookings for the resource.</span></span> <span data-ttu-id="5076a-141">Sen sijaan se lisää resurssin ryhmään.</span><span class="sxs-lookup"><span data-stu-id="5076a-141">Instead, it adds the resource to the team.</span></span> <span data-ttu-id="5076a-142">Kun ryhmän jäsen on lisätty projektiin, projektipäällikkö voi ylläpitää varauksia tai laajentaa varauksia, jotta tarvittavat varaukset voidaan lisätä resurssiin.</span><span class="sxs-lookup"><span data-stu-id="5076a-142">After the team member has been added to the project, the project manager can use maintain bookings or extend bookings to add the required bookings to the resource.</span></span>
