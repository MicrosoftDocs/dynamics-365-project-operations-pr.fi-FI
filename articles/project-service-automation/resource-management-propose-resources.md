---
title: Projektiresurssien ehdottaminen
description: Tässä aiheessa on tietoja projektiresurssien ehdottamisesta.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/28/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: bdb0dcb2-4421-4ee1-b97d-89a8cdefbd8d
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 3a7f7c15c3c7a3c39f2b7b9eeb88b9cf0cfdc220
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/24/2020
ms.locfileid: "3751253"
---
# <a name="propose-project-resources"></a><span data-ttu-id="b2e88-103">Projektiresurssien ehdottaminen</span><span class="sxs-lookup"><span data-stu-id="b2e88-103">Propose project resources</span></span>

<span data-ttu-id="b2e88-104">Resurssipäälliköt voivat ehdottaa resurssia projektipäällikölle resurssipyynnön avulla.</span><span class="sxs-lookup"><span data-stu-id="b2e88-104">Resource managers can propose a resource to the project manager by using a resource request.</span></span>

1. <span data-ttu-id="b2e88-105">Valitse pyyntöruudukosta tai itse pyynnöstä **Etsi resursseja**.</span><span class="sxs-lookup"><span data-stu-id="b2e88-105">From the request grid or the request itself, select **Find Resources**.</span></span>
2. <span data-ttu-id="b2e88-106">Valitse resurssi **Aikatauluavustaja**-sivulta, ja valitse sen jälkeen **Luo resurssivaraus** -ruudusta **Varaustila**-kentästä **Varaa**.</span><span class="sxs-lookup"><span data-stu-id="b2e88-106">On the **Schedule Assistant** page, select the resource, and then, in the **Create Resource Booking** pane, in the **Booking Status** field, select **Book**.</span></span>

    ![Ehdotettu resurssi valittu](media/Resource-Management-image62.png)

<span data-ttu-id="b2e88-108">Seuraavat tilapäivitykset toteutuvat:</span><span class="sxs-lookup"><span data-stu-id="b2e88-108">The following status updates occur:</span></span>

- <span data-ttu-id="b2e88-109">**Aikatauluavustaja** -sivulla tilailmaisimet päivittyvät ilmaisemaan, että varaus on ehdotettu eikä sitova.</span><span class="sxs-lookup"><span data-stu-id="b2e88-109">On the **Schedule Assistant** page, the status indicators are updated to indicate that the booking is proposed, not hard-booked.</span></span>

    ![Ehdotetun varauksen tilailmaisimet Aikatauluavustaja -sivulla](media/Resource-Management-image63.png)

- <span data-ttu-id="b2e88-111">Resurssipyynnössä tilaksi vaihtuu **Tarvitsee tarkistusta**.</span><span class="sxs-lookup"><span data-stu-id="b2e88-111">On the resource request, the status is changed to **Needs Review**.</span></span>

    ![Resurssipyynnön tilaksi vaihtuu Tarvitsee tarkistusta.](media/Resource-Management-image64.png)

- <span data-ttu-id="b2e88-113">Projektin **Ryhmä**-välilehdellä yleisen ryhmän jäsenen**Pyyntötilan** arvoksi vaihtuu **Tarvitsee tarkistusta**.</span><span class="sxs-lookup"><span data-stu-id="b2e88-113">On the **Team** tab of the project, the generic team member's **Request Status** value is changed to **Needs Review**.</span></span>

    ![Yleisen ryhmän jäsenen pyyntötila vaihtuu tilaksi Tarvitsee tarkistusta Ryhmä-välilehdellä.](media/Resource-Management-image48.png)

<span data-ttu-id="b2e88-115">Projektipäällikkö voi joko hyväksyä tai hylätä ehdotuksen.</span><span class="sxs-lookup"><span data-stu-id="b2e88-115">The project manager can either accept or reject the proposal.</span></span>

<span data-ttu-id="b2e88-116">Kun resurssipäälliköt käsittelevät resurssipyyntöjä, he voivat käyttää mitä tahansa seuraavista tavoista:</span><span class="sxs-lookup"><span data-stu-id="b2e88-116">When resource managers process resource requests, they can use any of the following approaches:</span></span>

- <span data-ttu-id="b2e88-117">Ehdota useita resursseja kysynnän tyydyttämiseksi, jos yhtään resurssia ei ole käytettävissä tarvittavien tuntien suorittamiseen.</span><span class="sxs-lookup"><span data-stu-id="b2e88-117">Propose multiple resources to satisfy the demand if no single resource is available to fulfill the required hours.</span></span> <span data-ttu-id="b2e88-118">Ehdotetut tunnit jaetaan sitten useiden resurssien kesken, jotka voivat täyttää vaaditut tunnit.</span><span class="sxs-lookup"><span data-stu-id="b2e88-118">Proposed hours are then split among multiple resources that can satisfy the required hours.</span></span> <span data-ttu-id="b2e88-119">Tässä skenaariossa tunnit eivät voi olla päällekkäisiä.</span><span class="sxs-lookup"><span data-stu-id="b2e88-119">In this scenario, the hours can't overlap.</span></span>
- <span data-ttu-id="b2e88-120">Ehdota vähemmän resursseja kuin on tarpeen.</span><span class="sxs-lookup"><span data-stu-id="b2e88-120">Propose fewer resources than are required.</span></span> <span data-ttu-id="b2e88-121">Tässä skenaariossa ehdotettu resurssikapasiteetti on pienempi kuin vaadittu pyytäjän määrittämä aika.</span><span class="sxs-lookup"><span data-stu-id="b2e88-121">In this scenario, the proposed resource capacity is less than the required hours that the requestor specified.</span></span> <span data-ttu-id="b2e88-122">Tämän vuoksi, kun pyytäjän on hyväksynyt ehdotetut resurssit, järjestelmä luo täyttämättömän resurssivaatimuksen, joka tallentaa jäljelle jäävän kysynnän.</span><span class="sxs-lookup"><span data-stu-id="b2e88-122">Therefore, when the requestor accepts the proposed resources, an unfulfilled resource requirement is created to capture the remaining demand.</span></span>
- <span data-ttu-id="b2e88-123">Varaa useita resursseja kysynnän tyydyttämiseksi, jos yhtään resurssia ei ole käytettävissä tarvittavien tuntien suorittamiseen.</span><span class="sxs-lookup"><span data-stu-id="b2e88-123">Book multiple resources to satisfy the demand if no single resource is available to complete the work.</span></span>
- <span data-ttu-id="b2e88-124">Varaa vähemmän resursseja kuin on tarpeen.</span><span class="sxs-lookup"><span data-stu-id="b2e88-124">Book fewer resources than are required.</span></span> <span data-ttu-id="b2e88-125">Tässä skenaariossa varatut tunnit ovat vähemmän kuin tarvittavat tunnit.</span><span class="sxs-lookup"><span data-stu-id="b2e88-125">In this scenario, the booked hours are fewer than the required hours.</span></span> <span data-ttu-id="b2e88-126">Järjestelmä opastaa varaamaan resursseja varauksen sijaan, jotta pyytäjä voi tarkistaa ja seurata jäljellä olevaa kysyntää.</span><span class="sxs-lookup"><span data-stu-id="b2e88-126">The system guides you to propose resources instead of bookings, so that the requestor can verify and keep track of remaining demand.</span></span>

## <a name="billable-utilization"></a><span data-ttu-id="b2e88-127">Laskutettava käyttöaste</span><span class="sxs-lookup"><span data-stu-id="b2e88-127">Billable utilization</span></span>

<span data-ttu-id="b2e88-128">Resursseilla voi olla tavoite laskutettavalle käytölle.</span><span class="sxs-lookup"><span data-stu-id="b2e88-128">Resources can have a target billable utilization.</span></span> <span data-ttu-id="b2e88-129">Tämä tavoitekäyttö määritetään joko resurssinoletusroolin ominaisuudeksi tai se määritellään yksittäisen varattavan resurssin tietueessa.</span><span class="sxs-lookup"><span data-stu-id="b2e88-129">This target utilization is either defined as an attribute on a resource's default role or set on the record of the individual bookable resource.</span></span> <span data-ttu-id="b2e88-130">Käytön laskennat perustuvat todellisiin tunteihin, jotka resurssit ovat raportoineet hyväksyttyjen aikakirjausten kautta.</span><span class="sxs-lookup"><span data-stu-id="b2e88-130">Utilization calculations are based on the actual hours that resources have reported by using approved time entries.</span></span>

<span data-ttu-id="b2e88-131">Käytön laskennassa käytetään seuraavia kaavoja:</span><span class="sxs-lookup"><span data-stu-id="b2e88-131">The following formulas are used to calculate utilization:</span></span>

- <span data-ttu-id="b2e88-132">Lakutettava käyttö = Laskutettavat todelliset tunnit ÷ Resurssin kapasiteetti</span><span class="sxs-lookup"><span data-stu-id="b2e88-132">Billable utilization = Chargeable actual hours ÷ Resource capacity</span></span>
- <span data-ttu-id="b2e88-133">Ei-laskutettava käyttö = Todellinen aika, jonka laskutustyyppi ID = Ei-laskutettava, Täydentävä tai Ei käytettävissä ÷ Resurssin kapasiteetti</span><span class="sxs-lookup"><span data-stu-id="b2e88-133">Non-billable utilization = Actual time with billing type ID = Non-chargeable, Complementary, or Not available ÷ Resource capacity</span></span>
- <span data-ttu-id="b2e88-134">Sisäinen = Todellinen aika ilman myyntisopimusta ÷ Resurssin kapasiteetti</span><span class="sxs-lookup"><span data-stu-id="b2e88-134">Internal = Actual time with no sales contract ÷ Resource capacity</span></span>
- <span data-ttu-id="b2e88-135">Resurssin kapasiteetti = Resurssin työtunnit – Poissa toimistosta – Muut kuin työpäivät</span><span class="sxs-lookup"><span data-stu-id="b2e88-135">Resource capacity = Resource work hours – Out-of-office – Non-working days</span></span>

<span data-ttu-id="b2e88-136">**Resurssien käyttöaste** -näkymä on **Resurssit**-ruudussa.</span><span class="sxs-lookup"><span data-stu-id="b2e88-136">You can find the **Resource Utilization** view in the **Resources** pane.</span></span>

![Resurssien käyttöaste -näkymä](media/Resource-Management-image65.png)

<span data-ttu-id="b2e88-138">Kukin ruudukon solu kuvaa resurssin laskutettavaa käyttöprosenttia kauden, esimerkiksi päivän, viikon tai kuukauden, aikana.</span><span class="sxs-lookup"><span data-stu-id="b2e88-138">Each cell in the grid represents the billable utilization percentage of the resource in a period, such as a day, week, or month.</span></span> <span data-ttu-id="b2e88-139">Solujen värittämiseen käytetään seuraavia kaavoja:</span><span class="sxs-lookup"><span data-stu-id="b2e88-139">The following formulas are used to color the cells:</span></span>

- <span data-ttu-id="b2e88-140">**Vihreä:** Laskutettava käyttö \>= Resurssin tavoitekäyttö</span><span class="sxs-lookup"><span data-stu-id="b2e88-140">**Green:** Billable utilization \>= Resource target utilization</span></span>
- <span data-ttu-id="b2e88-141">**Keltainen:** Tavoitekäyttö – 20 \<= Laskutettava käyttö \< Tavoitekäyttö</span><span class="sxs-lookup"><span data-stu-id="b2e88-141">**Yellow:** Target utilization – 20 \<= Billable utilization \< Target utilization</span></span>
- <span data-ttu-id="b2e88-142">**Punainen:** Laskutettava käyttö \< Tavoitekäyttö – 20</span><span class="sxs-lookup"><span data-stu-id="b2e88-142">**Red:** Billable utilization \< Target utilization – 20</span></span>

<span data-ttu-id="b2e88-143">Koska **Resurssien käyttöaste** -näkymä perustuu aikataulutaulutaulukkoon, voit suodattaa tuloksia käyttämällä aikataulutaulukon suodatustoimintoja.</span><span class="sxs-lookup"><span data-stu-id="b2e88-143">Because the **Resource Utilization** view is based on the Schedule Board, you can use the filtering capabilities of the Schedule Board to filter your results.</span></span>

<span data-ttu-id="b2e88-144">Ruudukko edellyttää, että määrität kohteen käytön joko roolille tai yksittäiselle resurssille.</span><span class="sxs-lookup"><span data-stu-id="b2e88-144">The grid requires that you set a target utilization on either the role or the individual resource.</span></span> <span data-ttu-id="b2e88-145">Tämä määritetään kohteessa **Resurssit** \> **Resurssiroolit**.</span><span class="sxs-lookup"><span data-stu-id="b2e88-145">To do this setup, go to **Resources** \> **Resource roles**.</span></span>

<span data-ttu-id="b2e88-146">Lisäksi jokaiselle varattavissa olevalle resurssille on määritettävä oletusrooli.</span><span class="sxs-lookup"><span data-stu-id="b2e88-146">Additionally, a default role must be assigned to each bookable resource.</span></span> <span data-ttu-id="b2e88-147">Siirry kohtaan **Resurssit** \> **Resurssit**.</span><span class="sxs-lookup"><span data-stu-id="b2e88-147">Go to **Resources** \> **Resources**.</span></span> <span data-ttu-id="b2e88-148">Varmista **Project Service**-välilehdellä, että resurssin rooli on määritetty, ja että **Onko oletus** -kentän arvo on **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="b2e88-148">On the **Project Service** tab, verify that a resource role is defined, and that the **Is Default** field for it is set to **Yes**.</span></span> <span data-ttu-id="b2e88-149">Voit llisätä muita rooleja, joiden **Onko oletus = Ei**.</span><span class="sxs-lookup"><span data-stu-id="b2e88-149">You can add additional roles where **Is Default = No**.</span></span> <span data-ttu-id="b2e88-150">Roolia, jossa **Onko oletus = Kyllä** käytetään määrittämään resurssin käyttöaste tavoitteen mukaisesti.</span><span class="sxs-lookup"><span data-stu-id="b2e88-150">The role where the **Is Default = Yes** is used to evaluate the resource's utilization against the target for that role.</span></span>

![Oletusrooli asetettu](media/Resource-Management-image67.png)

<span data-ttu-id="b2e88-152">**Project Service** -välilehdellä voit myös määrittää yksittäisen tavoitekäytön resurssille.</span><span class="sxs-lookup"><span data-stu-id="b2e88-152">On the **Project Service** tab, you can also set an individual target utilization for the resource.</span></span> <span data-ttu-id="b2e88-153">Käytön laskenta käyttää sen jälkeen tätä tavoitekäyttöastetta määrittääkseen resurssin tavoitteen resurssin oletusroolin tavoitteen asemesta.</span><span class="sxs-lookup"><span data-stu-id="b2e88-153">The utilization calculation then uses that target utilization to evaluate the resource's target instead of the target of the resource's default role.</span></span>

<span data-ttu-id="b2e88-154">Resurssin käyttöaste näytetään ainoastaan, jos resurssilla on hyväksyttyä laskutettavaa aikaa sen jakson aikana, joka näkyy ruudukossa.</span><span class="sxs-lookup"><span data-stu-id="b2e88-154">Utilization is shown for a resource only if that resource has approved, chargeable time during the period that is shown in the grid.</span></span>

## <a name="resource-availability"></a><span data-ttu-id="b2e88-155">Resurssin käytettävyys</span><span class="sxs-lookup"><span data-stu-id="b2e88-155">Resource availability</span></span>

<span data-ttu-id="b2e88-156">On tärkeää, että resurssipäälliköt voivat tarkastella resurssien saatavuutta ja päivittää varauksia.</span><span class="sxs-lookup"><span data-stu-id="b2e88-156">It's critical that resource managers be able to view the availability of resources and update bookings.</span></span> <span data-ttu-id="b2e88-157">Joissakin tapauksissa ei ole virallista kysyntää (resurssipyyntöä), mutta resurssipäällikön on vastattava suunnittelemattomaan kysyntään, joka tulee esimerkiksi sähköpostitse, puhelimitse tai pikaviestin kautta.</span><span class="sxs-lookup"><span data-stu-id="b2e88-157">In some cases, there is no formal demand (resource request), but a resource manager must respond to an unplanned demand that comes through channels such as an email, phone call, or instant message.</span></span> <span data-ttu-id="b2e88-158">Resurssipäälliköt käyttävät aikataulutaulukkoa resurssien ja varausten päivittämiseen.</span><span class="sxs-lookup"><span data-stu-id="b2e88-158">Resource managers use the Schedule Board to update resources and bookings.</span></span>

<span data-ttu-id="b2e88-159">Resurssin työaikaa käytetään perusteena resurssin saatavuuden laskennassa.</span><span class="sxs-lookup"><span data-stu-id="b2e88-159">Resource work hours are used as the basis for calculating the availability of a resource.</span></span> <span data-ttu-id="b2e88-160">Resurssivaraukset kuluttavat resurssien kapasiteettia.</span><span class="sxs-lookup"><span data-stu-id="b2e88-160">Resource bookings consume the capacity of the resources.</span></span>

![Aikataulutaulukko](media/Resource-Management-image68.png)

<span data-ttu-id="b2e88-162">Aikataulutaulukko käyttää värejä ja varjostusta, kun se näyttää varauksia, saatavuutta ja ylivarauksia sekä varausten tilan.</span><span class="sxs-lookup"><span data-stu-id="b2e88-162">The Schedule Board uses colors and shading to show bookings, availability, and overbookings, and also the status of bookings.</span></span> <span data-ttu-id="b2e88-163">Aikataulutaulukon asetusten avulla voit näyttää selitteen.</span><span class="sxs-lookup"><span data-stu-id="b2e88-163">A setting in the Schedule Board settings lets you show a legend.</span></span>

<span data-ttu-id="b2e88-164">Jos yksittäisen varattavan resurssin vieressä näkyy oikealle osoittava nuoli aikataulutaulukossa, resurssi voidaan laajentaa niin, että siinä näkyvät sen työn tiedot, johon resurssi on varattu.</span><span class="sxs-lookup"><span data-stu-id="b2e88-164">If a right-pointing arrow appears next to an individual bookable resource on the Schedule Board, the resource can be expanded to show details of the work that the resource is booked on.</span></span>

![Varattava resurssi laajennettuna aikataulutaulukossa](media/Resource-Management-image69.png)

<span data-ttu-id="b2e88-166">Koska Dynamics 365 Project Service Automation käyttää Universal Resource Scheduling -moottoria, jos sinulla on myös Dynamics 365 Field Service asennettuna,voit katsella resurssivarausten tietoja projekteille, työtilauksille ja mille tahansa muille kohteille, joihin olet laajentanut aikatauluttamisen.</span><span class="sxs-lookup"><span data-stu-id="b2e88-166">Because Dynamics 365 Project Service Automation uses the Universal Resource Scheduling engine, if you also have Dynamics 365 Field Service installed, you can view the details of resource bookings for projects, work orders, and any other entities that you've extended scheduling to.</span></span>

![Projektien ja työtilausten resurssivarausten tiedot](media/Resource-Management-image70.png)

<span data-ttu-id="b2e88-168">Jos haluat tarkastella lisätietoja yksittäisestä resurssista, avaa resurssikortti napsauttamalla sitä hiiren kakkospainikkeella.</span><span class="sxs-lookup"><span data-stu-id="b2e88-168">To view more details about an individual resource, right-click it to open the resource card.</span></span>

![Resurssikortti](media/Resource-Management-image71.png)
