---
title: Ehdotettujen resurssien tarkasteleminen
description: Tässä aiheessa on tietoja projektiresurssien ehdottamisesta.
author: ruhercul
manager: AnnBe
ms.date: 11/05/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: ruhercul
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: fa0515b9d6a0023c05c37d2bcfa6a403f48927cb
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5279269"
---
# <a name="review-proposed-resources"></a><span data-ttu-id="a510e-103">Ehdotettujen resurssien tarkasteleminen</span><span class="sxs-lookup"><span data-stu-id="a510e-103">Review proposed resources</span></span>

<span data-ttu-id="a510e-104">_**Koskee:** Project Operationsin resurssiin / muuhun kuin resurssiin perustuvia skenaarioita, Lite-käyttöönotto-kaupasta proformalaskutukseen_</span><span class="sxs-lookup"><span data-stu-id="a510e-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="a510e-105">Resurssipäälliköt voivat ehdottaa resurssia projektipäällikölle resurssipyynnön avulla.</span><span class="sxs-lookup"><span data-stu-id="a510e-105">Resource managers can propose a resource to the project manager by using a resource request.</span></span>

1. <span data-ttu-id="a510e-106">Valitse pyyntöruudukosta tai itse pyynnöstä **Etsi resursseja**.</span><span class="sxs-lookup"><span data-stu-id="a510e-106">From the request grid or the request itself, select **Find Resources**.</span></span>
2. <span data-ttu-id="a510e-107">Valitse resurssi **Aikatauluavustaja**-sivulta, ja valitse sen jälkeen **Luo resurssivaraus** -ruudusta **Varaustila**-kentästä **Varaa**.</span><span class="sxs-lookup"><span data-stu-id="a510e-107">On the **Schedule Assistant** page, select the resource, and then, in the **Create Resource Booking** pane, in the **Booking Status** field, select **Book**.</span></span>

<span data-ttu-id="a510e-108">Seuraavat tilapäivitykset toteutuvat:</span><span class="sxs-lookup"><span data-stu-id="a510e-108">The following status updates occur:</span></span>

- <span data-ttu-id="a510e-109">**Aikatauluavustaja** -sivulla tilailmaisimet päivittyvät ilmaisemaan, että varaus on ehdotettu eikä sitova.</span><span class="sxs-lookup"><span data-stu-id="a510e-109">On the **Schedule Assistant** page, the status indicators are updated to indicate that the booking is proposed, not hard-booked.</span></span>
- <span data-ttu-id="a510e-110">Resurssipyynnössä tilaksi vaihtuu **Tarvitsee tarkistusta**.</span><span class="sxs-lookup"><span data-stu-id="a510e-110">On the resource request, the status is changed to **Needs Review**.</span></span>
- <span data-ttu-id="a510e-111">Projektin **Ryhmä**-välilehdellä yleisen ryhmän jäsenen **Pyyntötilan** arvoksi vaihtuu **Tarvitsee tarkistusta**.</span><span class="sxs-lookup"><span data-stu-id="a510e-111">On the **Team** tab of the project, the generic team member's **Request Status** value is changed to **Needs Review**.</span></span>

<span data-ttu-id="a510e-112">Projektipäällikkö voi joko hyväksyä tai hylätä ehdotuksen.</span><span class="sxs-lookup"><span data-stu-id="a510e-112">The project manager can either accept or reject the proposal.</span></span>

<span data-ttu-id="a510e-113">Kun resurssipäälliköt käsittelevät resurssipyyntöjä, he voivat käyttää mitä tahansa seuraavista tavoista:</span><span class="sxs-lookup"><span data-stu-id="a510e-113">When resource managers process resource requests, they can use any of the following approaches:</span></span>

- <span data-ttu-id="a510e-114">Ehdota useita resursseja kysynnän tyydyttämiseksi, jos yhtään resurssia ei ole käytettävissä tarvittavien tuntien suorittamiseen.</span><span class="sxs-lookup"><span data-stu-id="a510e-114">Propose multiple resources to satisfy the demand if no single resource is available to fulfill the required hours.</span></span> <span data-ttu-id="a510e-115">Ehdotetut tunnit jaetaan sitten useiden resurssien kesken, jotka voivat täyttää vaaditut tunnit.</span><span class="sxs-lookup"><span data-stu-id="a510e-115">Proposed hours are then split among multiple resources that can satisfy the required hours.</span></span> <span data-ttu-id="a510e-116">Tässä skenaariossa tunnit eivät voi olla päällekkäisiä.</span><span class="sxs-lookup"><span data-stu-id="a510e-116">In this scenario, the hours can't overlap.</span></span>
- <span data-ttu-id="a510e-117">Ehdota vähemmän resursseja kuin on tarpeen.</span><span class="sxs-lookup"><span data-stu-id="a510e-117">Propose fewer resources than are required.</span></span> <span data-ttu-id="a510e-118">Tässä skenaariossa ehdotettu resurssikapasiteetti on pienempi kuin vaadittu pyytäjän määrittämä aika.</span><span class="sxs-lookup"><span data-stu-id="a510e-118">In this scenario, the proposed resource capacity is less than the required hours that the requestor specified.</span></span> <span data-ttu-id="a510e-119">Tämän vuoksi, kun pyytäjän on hyväksynyt ehdotetut resurssit, järjestelmä luo täyttämättömän resurssivaatimuksen, joka tallentaa jäljelle jäävän kysynnän.</span><span class="sxs-lookup"><span data-stu-id="a510e-119">Therefore, when the requestor accepts the proposed resources, an unfulfilled resource requirement is created to capture the remaining demand.</span></span>
- <span data-ttu-id="a510e-120">Varaa useita resursseja kysynnän tyydyttämiseksi, jos yhtään resurssia ei ole käytettävissä tarvittavien tuntien suorittamiseen.</span><span class="sxs-lookup"><span data-stu-id="a510e-120">Book multiple resources to satisfy the demand if no single resource is available to complete the work.</span></span>
- <span data-ttu-id="a510e-121">Varaa vähemmän resursseja kuin on tarpeen.</span><span class="sxs-lookup"><span data-stu-id="a510e-121">Book fewer resources than are required.</span></span> <span data-ttu-id="a510e-122">Tässä skenaariossa varatut tunnit ovat vähemmän kuin tarvittavat tunnit.</span><span class="sxs-lookup"><span data-stu-id="a510e-122">In this scenario, the booked hours are fewer than the required hours.</span></span> <span data-ttu-id="a510e-123">Järjestelmä opastaa varaamaan resursseja varauksen sijaan, jotta pyytäjä voi tarkistaa ja seurata jäljellä olevaa kysyntää.</span><span class="sxs-lookup"><span data-stu-id="a510e-123">The system guides you to propose resources instead of bookings, so that the requestor can verify and keep track of remaining demand.</span></span>

## <a name="resource-availability"></a><span data-ttu-id="a510e-124">Resurssin käytettävyys</span><span class="sxs-lookup"><span data-stu-id="a510e-124">Resource availability</span></span>

<span data-ttu-id="a510e-125">On tärkeää, että resurssipäälliköt voivat tarkastella resurssien saatavuutta ja päivittää varauksia.</span><span class="sxs-lookup"><span data-stu-id="a510e-125">It's critical that resource managers be able to view the availability of resources and update bookings.</span></span> <span data-ttu-id="a510e-126">Joissakin tapauksissa ei ole virallista kysyntää (resurssipyyntöä), mutta resurssipäällikön on vastattava suunnittelemattomaan kysyntään, joka tulee esimerkiksi sähköpostitse, puhelimitse tai pikaviestin kautta.</span><span class="sxs-lookup"><span data-stu-id="a510e-126">In some cases, there is no formal demand (resource request), but a resource manager must respond to an unplanned demand that comes through channels such as an email, phone call, or instant message.</span></span> <span data-ttu-id="a510e-127">Resurssipäälliköt käyttävät aikataulutaulukkoa resurssien ja varausten päivittämiseen.</span><span class="sxs-lookup"><span data-stu-id="a510e-127">Resource managers use the Schedule Board to update resources and bookings.</span></span>

<span data-ttu-id="a510e-128">Resurssin työaikaa käytetään perusteena resurssin saatavuuden laskennassa.</span><span class="sxs-lookup"><span data-stu-id="a510e-128">Resource work hours are used as the basis for calculating the availability of a resource.</span></span> <span data-ttu-id="a510e-129">Resurssivaraukset kuluttavat resurssien kapasiteettia.</span><span class="sxs-lookup"><span data-stu-id="a510e-129">Resource bookings consume the capacity of the resources.</span></span>

<span data-ttu-id="a510e-130">Aikataulutaulukko käyttää värejä ja varjostusta, kun se näyttää varauksia, saatavuutta ja ylivarauksia sekä varausten tilan.</span><span class="sxs-lookup"><span data-stu-id="a510e-130">The Schedule Board uses colors and shading to show bookings, availability, and overbookings, and also the status of bookings.</span></span> <span data-ttu-id="a510e-131">Aikataulutaulukon asetusten avulla voit näyttää selitteen.</span><span class="sxs-lookup"><span data-stu-id="a510e-131">A setting in the Schedule Board settings lets you show a legend.</span></span>

<span data-ttu-id="a510e-132">Jos yksittäisen varattavan resurssin vieressä näkyy oikealle osoittava nuoli aikataulutaulukossa, resurssi voidaan laajentaa niin, että siinä näkyvät sen työn tiedot, johon resurssi on varattu.</span><span class="sxs-lookup"><span data-stu-id="a510e-132">If a right-pointing arrow appears next to an individual bookable resource on the Schedule Board, the resource can be expanded to show details of the work that the resource is booked on.</span></span>

<span data-ttu-id="a510e-133">Koska Dynamics 365 Project Operations käyttää Universal Resource Scheduling -moottoria, jos sinulla on myös Dynamics 365 Field Service asennettuna,voit katsella resurssivarausten tietoja projekteille, työtilauksille ja mille tahansa muille kohteille, joihin olet laajentanut aikatauluttamisen.</span><span class="sxs-lookup"><span data-stu-id="a510e-133">Because Dynamics 365 Project Operations uses the Universal Resource Scheduling engine, if you also have Dynamics 365 Field Service installed, you can view the details of resource bookings for projects, work orders, and any other entities that you've extended scheduling to.</span></span>

<span data-ttu-id="a510e-134">Jos haluat tarkastella lisätietoja yksittäisestä resurssista, avaa resurssikortti napsauttamalla sitä hiiren kakkospainikkeella.</span><span class="sxs-lookup"><span data-stu-id="a510e-134">To view more details about an individual resource, right-click it to open the resource card.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]