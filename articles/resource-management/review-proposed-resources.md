---
title: Ehdotettujen resurssien tarkasteleminen
description: Tässä aiheessa on tietoja projektiresurssien ehdottamisesta.
author: ruhercul
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
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
ms.openlocfilehash: ad5cbdeb5fe05e6115eb024833a8d58b626ea4c9
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/16/2020
ms.locfileid: "4075315"
---
# <a name="review-proposed-resources"></a><span data-ttu-id="a8ff5-103">Ehdotettujen resurssien tarkasteleminen</span><span class="sxs-lookup"><span data-stu-id="a8ff5-103">Review proposed resources</span></span>

<span data-ttu-id="a8ff5-104">_**Koskee:** Project Operationsin resurssiin / muuhun kuin resurssiin perustuvia skenaarioita, Lite-käyttöönotto-kaupasta proformalaskutukseen_</span><span class="sxs-lookup"><span data-stu-id="a8ff5-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="a8ff5-105">Resurssipäälliköt voivat ehdottaa resurssia projektipäällikölle resurssipyynnön avulla.</span><span class="sxs-lookup"><span data-stu-id="a8ff5-105">Resource managers can propose a resource to the project manager by using a resource request.</span></span>

1. <span data-ttu-id="a8ff5-106">Valitse pyyntöruudukosta tai itse pyynnöstä **Etsi resursseja**.</span><span class="sxs-lookup"><span data-stu-id="a8ff5-106">From the request grid or the request itself, select **Find Resources**.</span></span>
2. <span data-ttu-id="a8ff5-107">Valitse resurssi **Aikatauluavustaja** -sivulta, ja valitse sen jälkeen **Luo resurssivaraus** -ruudusta **Varaustila** -kentästä **Varaa**.</span><span class="sxs-lookup"><span data-stu-id="a8ff5-107">On the **Schedule Assistant** page, select the resource, and then, in the **Create Resource Booking** pane, in the **Booking Status** field, select **Book**.</span></span>

<span data-ttu-id="a8ff5-108">Seuraavat tilapäivitykset toteutuvat:</span><span class="sxs-lookup"><span data-stu-id="a8ff5-108">The following status updates occur:</span></span>

- <span data-ttu-id="a8ff5-109">**Aikatauluavustaja** -sivulla tilailmaisimet päivittyvät ilmaisemaan, että varaus on ehdotettu eikä sitova.</span><span class="sxs-lookup"><span data-stu-id="a8ff5-109">On the **Schedule Assistant** page, the status indicators are updated to indicate that the booking is proposed, not hard-booked.</span></span>
- <span data-ttu-id="a8ff5-110">Resurssipyynnössä tilaksi vaihtuu **Tarvitsee tarkistusta**.</span><span class="sxs-lookup"><span data-stu-id="a8ff5-110">On the resource request, the status is changed to **Needs Review**.</span></span>
- <span data-ttu-id="a8ff5-111">Projektin **Ryhmä** -välilehdellä yleisen ryhmän jäsenen **Pyyntötilan** arvoksi vaihtuu **Tarvitsee tarkistusta**.</span><span class="sxs-lookup"><span data-stu-id="a8ff5-111">On the **Team** tab of the project, the generic team member's **Request Status** value is changed to **Needs Review**.</span></span>

<span data-ttu-id="a8ff5-112">Projektipäällikkö voi joko hyväksyä tai hylätä ehdotuksen.</span><span class="sxs-lookup"><span data-stu-id="a8ff5-112">The project manager can either accept or reject the proposal.</span></span>

<span data-ttu-id="a8ff5-113">Kun resurssipäälliköt käsittelevät resurssipyyntöjä, he voivat käyttää mitä tahansa seuraavista tavoista:</span><span class="sxs-lookup"><span data-stu-id="a8ff5-113">When resource managers process resource requests, they can use any of the following approaches:</span></span>

- <span data-ttu-id="a8ff5-114">Ehdota useita resursseja kysynnän tyydyttämiseksi, jos yhtään resurssia ei ole käytettävissä tarvittavien tuntien suorittamiseen.</span><span class="sxs-lookup"><span data-stu-id="a8ff5-114">Propose multiple resources to satisfy the demand if no single resource is available to fulfill the required hours.</span></span> <span data-ttu-id="a8ff5-115">Ehdotetut tunnit jaetaan sitten useiden resurssien kesken, jotka voivat täyttää vaaditut tunnit.</span><span class="sxs-lookup"><span data-stu-id="a8ff5-115">Proposed hours are then split among multiple resources that can satisfy the required hours.</span></span> <span data-ttu-id="a8ff5-116">Tässä skenaariossa tunnit eivät voi olla päällekkäisiä.</span><span class="sxs-lookup"><span data-stu-id="a8ff5-116">In this scenario, the hours can't overlap.</span></span>
- <span data-ttu-id="a8ff5-117">Ehdota vähemmän resursseja kuin on tarpeen.</span><span class="sxs-lookup"><span data-stu-id="a8ff5-117">Propose fewer resources than are required.</span></span> <span data-ttu-id="a8ff5-118">Tässä skenaariossa ehdotettu resurssikapasiteetti on pienempi kuin vaadittu pyytäjän määrittämä aika.</span><span class="sxs-lookup"><span data-stu-id="a8ff5-118">In this scenario, the proposed resource capacity is less than the required hours that the requestor specified.</span></span> <span data-ttu-id="a8ff5-119">Tämän vuoksi, kun pyytäjän on hyväksynyt ehdotetut resurssit, järjestelmä luo täyttämättömän resurssivaatimuksen, joka tallentaa jäljelle jäävän kysynnän.</span><span class="sxs-lookup"><span data-stu-id="a8ff5-119">Therefore, when the requestor accepts the proposed resources, an unfulfilled resource requirement is created to capture the remaining demand.</span></span>
- <span data-ttu-id="a8ff5-120">Varaa useita resursseja kysynnän tyydyttämiseksi, jos yhtään resurssia ei ole käytettävissä tarvittavien tuntien suorittamiseen.</span><span class="sxs-lookup"><span data-stu-id="a8ff5-120">Book multiple resources to satisfy the demand if no single resource is available to complete the work.</span></span>
- <span data-ttu-id="a8ff5-121">Varaa vähemmän resursseja kuin on tarpeen.</span><span class="sxs-lookup"><span data-stu-id="a8ff5-121">Book fewer resources than are required.</span></span> <span data-ttu-id="a8ff5-122">Tässä skenaariossa varatut tunnit ovat vähemmän kuin tarvittavat tunnit.</span><span class="sxs-lookup"><span data-stu-id="a8ff5-122">In this scenario, the booked hours are fewer than the required hours.</span></span> <span data-ttu-id="a8ff5-123">Järjestelmä opastaa varaamaan resursseja varauksen sijaan, jotta pyytäjä voi tarkistaa ja seurata jäljellä olevaa kysyntää.</span><span class="sxs-lookup"><span data-stu-id="a8ff5-123">The system guides you to propose resources instead of bookings, so that the requestor can verify and keep track of remaining demand.</span></span>

## <a name="billable-utilization"></a><span data-ttu-id="a8ff5-124">Laskutettava käyttöaste</span><span class="sxs-lookup"><span data-stu-id="a8ff5-124">Billable utilization</span></span>

<span data-ttu-id="a8ff5-125">Resursseilla voi olla tavoite laskutettavalle käytölle.</span><span class="sxs-lookup"><span data-stu-id="a8ff5-125">Resources can have a target billable utilization.</span></span> <span data-ttu-id="a8ff5-126">Tämä tavoitekäyttö määritetään joko resurssinoletusroolin ominaisuudeksi tai se määritellään yksittäisen varattavan resurssin tietueessa.</span><span class="sxs-lookup"><span data-stu-id="a8ff5-126">This target utilization is either defined as an attribute on a resource's default role or set on the record of the individual bookable resource.</span></span> <span data-ttu-id="a8ff5-127">Käytön laskennat perustuvat todellisiin tunteihin, jotka resurssit ovat raportoineet hyväksyttyjen aikakirjausten kautta.</span><span class="sxs-lookup"><span data-stu-id="a8ff5-127">Utilization calculations are based on the actual hours that resources have reported by using approved time entries.</span></span>

<span data-ttu-id="a8ff5-128">Käytön laskennassa käytetään seuraavia kaavoja:</span><span class="sxs-lookup"><span data-stu-id="a8ff5-128">The following formulas are used to calculate utilization:</span></span>

- <span data-ttu-id="a8ff5-129">Lakutettava käyttö = Laskutettavat todelliset tunnit ÷ Resurssin kapasiteetti</span><span class="sxs-lookup"><span data-stu-id="a8ff5-129">Billable utilization = Chargeable actual hours ÷ Resource capacity</span></span>
- <span data-ttu-id="a8ff5-130">Ei-laskutettava käyttö = Todellinen aika, jonka laskutustyyppi ID = Ei-laskutettava, Täydentävä tai Ei käytettävissä ÷ Resurssin kapasiteetti</span><span class="sxs-lookup"><span data-stu-id="a8ff5-130">Non-billable utilization = Actual time with billing type ID = Non-chargeable, Complementary, or Not available ÷ Resource capacity</span></span>
- <span data-ttu-id="a8ff5-131">Sisäinen = Todellinen aika ilman myyntisopimusta ÷ Resurssin kapasiteetti</span><span class="sxs-lookup"><span data-stu-id="a8ff5-131">Internal = Actual time with no sales contract ÷ Resource capacity</span></span>
- <span data-ttu-id="a8ff5-132">Resurssin kapasiteetti = Resurssin työtunnit – Poissa toimistosta – Muut kuin työpäivät</span><span class="sxs-lookup"><span data-stu-id="a8ff5-132">Resource capacity = Resource work hours – Out-of-office – Non-working days</span></span>

<span data-ttu-id="a8ff5-133">**Resurssien käyttöaste** -näkymä on **Resurssit** -ruudussa.</span><span class="sxs-lookup"><span data-stu-id="a8ff5-133">You can find the **Resource Utilization** view in the **Resources** pane.</span></span>

<span data-ttu-id="a8ff5-134">Kukin ruudukon solu kuvaa resurssin laskutettavaa käyttöprosenttia kauden, esimerkiksi päivän, viikon tai kuukauden, aikana.</span><span class="sxs-lookup"><span data-stu-id="a8ff5-134">Each cell in the grid represents the billable utilization percentage of the resource in a period, such as a day, week, or month.</span></span> <span data-ttu-id="a8ff5-135">Solujen värittämiseen käytetään seuraavia kaavoja:</span><span class="sxs-lookup"><span data-stu-id="a8ff5-135">The following formulas are used to color the cells:</span></span>

- <span data-ttu-id="a8ff5-136">**Vihreä:** Laskutettava käyttö \>= Resurssin tavoitekäyttö</span><span class="sxs-lookup"><span data-stu-id="a8ff5-136">**Green:** Billable utilization \>= Resource target utilization</span></span>
- <span data-ttu-id="a8ff5-137">**Keltainen:** Tavoitekäyttö – 20 \<= Laskutettava käyttö \< Tavoitekäyttö</span><span class="sxs-lookup"><span data-stu-id="a8ff5-137">**Yellow:** Target utilization – 20 \<= Billable utilization \< Target utilization</span></span>
- <span data-ttu-id="a8ff5-138">**Punainen:** Laskutettava käyttö \< Tavoitekäyttö – 20</span><span class="sxs-lookup"><span data-stu-id="a8ff5-138">**Red:** Billable utilization \< Target utilization – 20</span></span>

<span data-ttu-id="a8ff5-139">Koska **Resurssien käyttöaste** -näkymä perustuu aikataulutaulutaulukkoon, voit suodattaa tuloksia käyttämällä aikataulutaulukon suodatustoimintoja.</span><span class="sxs-lookup"><span data-stu-id="a8ff5-139">Because the **Resource Utilization** view is based on the Schedule Board, you can use the filtering capabilities of the Schedule Board to filter your results.</span></span>

<span data-ttu-id="a8ff5-140">Ruudukko edellyttää, että määrität kohteen käytön joko roolille tai yksittäiselle resurssille.</span><span class="sxs-lookup"><span data-stu-id="a8ff5-140">The grid requires that you set a target utilization on either the role or the individual resource.</span></span> <span data-ttu-id="a8ff5-141">Tämä määritetään kohteessa **Resurssit** \> **Resurssiroolit**.</span><span class="sxs-lookup"><span data-stu-id="a8ff5-141">To do this setup, go to **Resources** \> **Resource roles**.</span></span>

<span data-ttu-id="a8ff5-142">Lisäksi jokaiselle varattavissa olevalle resurssille on määritettävä oletusrooli.</span><span class="sxs-lookup"><span data-stu-id="a8ff5-142">Additionally, a default role must be assigned to each bookable resource.</span></span> <span data-ttu-id="a8ff5-143">Siirry kohtaan **Resurssit** \> **Resurssit**.</span><span class="sxs-lookup"><span data-stu-id="a8ff5-143">Go to **Resources** \> **Resources**.</span></span> <span data-ttu-id="a8ff5-144">Varmista **Project Service** -välilehdellä, että resurssin rooli on määritetty, ja että **Onko oletus** -kentän arvo on **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="a8ff5-144">On the **Project Service** tab, verify that a resource role is defined, and that the **Is Default** field for it is set to **Yes**.</span></span> <span data-ttu-id="a8ff5-145">Voit llisätä muita rooleja, joiden **Onko oletus = Ei**.</span><span class="sxs-lookup"><span data-stu-id="a8ff5-145">You can add additional roles where **Is Default = No**.</span></span> <span data-ttu-id="a8ff5-146">Roolia, jossa **Onko oletus = Kyllä** käytetään määrittämään resurssin käyttöaste tavoitteen mukaisesti.</span><span class="sxs-lookup"><span data-stu-id="a8ff5-146">The role where the **Is Default = Yes** is used to evaluate the resource's utilization against the target for that role.</span></span>

<span data-ttu-id="a8ff5-147">**Project Service** -välilehdellä voit myös määrittää yksittäisen tavoitekäytön resurssille.</span><span class="sxs-lookup"><span data-stu-id="a8ff5-147">On the **Project Service** tab, you can also set an individual target utilization for the resource.</span></span> <span data-ttu-id="a8ff5-148">Käytön laskenta käyttää sen jälkeen tätä tavoitekäyttöastetta määrittääkseen resurssin tavoitteen resurssin oletusroolin tavoitteen asemesta.</span><span class="sxs-lookup"><span data-stu-id="a8ff5-148">The utilization calculation then uses that target utilization to evaluate the resource's target instead of the target of the resource's default role.</span></span>

<span data-ttu-id="a8ff5-149">Resurssin käyttöaste näytetään ainoastaan, jos resurssilla on hyväksyttyä laskutettavaa aikaa sen jakson aikana, joka näkyy ruudukossa.</span><span class="sxs-lookup"><span data-stu-id="a8ff5-149">Utilization is shown for a resource only if that resource has approved, chargeable time during the period that is shown in the grid.</span></span>

## <a name="resource-availability"></a><span data-ttu-id="a8ff5-150">Resurssin käytettävyys</span><span class="sxs-lookup"><span data-stu-id="a8ff5-150">Resource availability</span></span>

<span data-ttu-id="a8ff5-151">On tärkeää, että resurssipäälliköt voivat tarkastella resurssien saatavuutta ja päivittää varauksia.</span><span class="sxs-lookup"><span data-stu-id="a8ff5-151">It's critical that resource managers be able to view the availability of resources and update bookings.</span></span> <span data-ttu-id="a8ff5-152">Joissakin tapauksissa ei ole virallista kysyntää (resurssipyyntöä), mutta resurssipäällikön on vastattava suunnittelemattomaan kysyntään, joka tulee esimerkiksi sähköpostitse, puhelimitse tai pikaviestin kautta.</span><span class="sxs-lookup"><span data-stu-id="a8ff5-152">In some cases, there is no formal demand (resource request), but a resource manager must respond to an unplanned demand that comes through channels such as an email, phone call, or instant message.</span></span> <span data-ttu-id="a8ff5-153">Resurssipäälliköt käyttävät aikataulutaulukkoa resurssien ja varausten päivittämiseen.</span><span class="sxs-lookup"><span data-stu-id="a8ff5-153">Resource managers use the Schedule Board to update resources and bookings.</span></span>

<span data-ttu-id="a8ff5-154">Resurssin työaikaa käytetään perusteena resurssin saatavuuden laskennassa.</span><span class="sxs-lookup"><span data-stu-id="a8ff5-154">Resource work hours are used as the basis for calculating the availability of a resource.</span></span> <span data-ttu-id="a8ff5-155">Resurssivaraukset kuluttavat resurssien kapasiteettia.</span><span class="sxs-lookup"><span data-stu-id="a8ff5-155">Resource bookings consume the capacity of the resources.</span></span>

<span data-ttu-id="a8ff5-156">Aikataulutaulukko käyttää värejä ja varjostusta, kun se näyttää varauksia, saatavuutta ja ylivarauksia sekä varausten tilan.</span><span class="sxs-lookup"><span data-stu-id="a8ff5-156">The Schedule Board uses colors and shading to show bookings, availability, and overbookings, and also the status of bookings.</span></span> <span data-ttu-id="a8ff5-157">Aikataulutaulukon asetusten avulla voit näyttää selitteen.</span><span class="sxs-lookup"><span data-stu-id="a8ff5-157">A setting in the Schedule Board settings lets you show a legend.</span></span>

<span data-ttu-id="a8ff5-158">Jos yksittäisen varattavan resurssin vieressä näkyy oikealle osoittava nuoli aikataulutaulukossa, resurssi voidaan laajentaa niin, että siinä näkyvät sen työn tiedot, johon resurssi on varattu.</span><span class="sxs-lookup"><span data-stu-id="a8ff5-158">If a right-pointing arrow appears next to an individual bookable resource on the Schedule Board, the resource can be expanded to show details of the work that the resource is booked on.</span></span>

<span data-ttu-id="a8ff5-159">Koska Dynamics 365 Project Operations käyttää Universal Resource Scheduling -ohjelmaa, jos myös Dynamics 365 Field Service on asennettu,voit katsella resurssivarausten tietoja projekteille, työtilauksille ja mille tahansa muille kohteille, joihin olet laajentanut aikatauluttamisen.</span><span class="sxs-lookup"><span data-stu-id="a8ff5-159">Because Dynamics 365 Project Operations uses the Universal Resource Scheduling engine, if you also have Dynamics 365 Field Service installed, you can view the details of resource bookings for projects, work orders, and any other entities that you've extended scheduling to.</span></span>

<span data-ttu-id="a8ff5-160">Jos haluat tarkastella lisätietoja yksittäisestä resurssista, avaa resurssikortti napsauttamalla sitä hiiren kakkospainikkeella.</span><span class="sxs-lookup"><span data-stu-id="a8ff5-160">To view more details about an individual resource, right-click it to open the resource card.</span></span>

