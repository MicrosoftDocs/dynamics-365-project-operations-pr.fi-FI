---
title: Miten delegoin varattavissa olevan resurssin tehtävälle verkkosovelluksessa
description: Yleiskatsaus tapoihin, joilla varattavissa olevia resursseja voidaan delegoida.
author: JohnPBurrows
manager: kfend
ms.service: business-applications
ms.custom:
- dyn365-projectservice
ms.date: 8/21/2018
ms.topic: article
ms.prod: ''
ms.technology: Dynamics 365 Project Service Automation 2.x on platform version 9.x
ms.assetid: 9db35b39-8dfc-4989-9160-fd841fe0ae5a
ms.author: john.burrows
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 521ea73c948619816d3cd06d72140fcc85366397
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/24/2020
ms.locfileid: "3751271"
---
# <a name="how-do-i-assign-a-bookable-resource-to-a-task-in-the-web-app-project-service-app-v2x"></a><span data-ttu-id="20846-103">Miten delegoin varattavissa olevan resurssin tehtävälle verkkosovelluksessa (Project Service -sovelluksen versio 2.x)?</span><span class="sxs-lookup"><span data-stu-id="20846-103">How do I assign a bookable resource to a task in the web app (Project Service app v2.x)?</span></span>

[!INCLUDE[cc-applies-to-psa-app-1.x-2.x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="20846-104">Resurssin voi delegoida tehtävälle kahdella eri tavalla Project Service -sovelluksessa.</span><span class="sxs-lookup"><span data-stu-id="20846-104">There are two ways to assign a resource to a task in Project Service.</span></span> <span data-ttu-id="20846-105">Voit varata resurssin ryhmän jäsenenä ja delegoida sen sitten tehtävälle.</span><span class="sxs-lookup"><span data-stu-id="20846-105">You can book a resource as a team member and then assign it to a task.</span></span> <span data-ttu-id="20846-106">Vaihtoehtoisesti voit luoda yleisen ryhmän jäsenen roolin tehtävän delegointien kautta, luoda sitten ryhmän ja täyttää taustalla olevat tarpeet nimetyn resurssin avulla.</span><span class="sxs-lookup"><span data-stu-id="20846-106">Or, you can create a generic team member through role assignment on tasks, generate a team, and then fulfill the backing requirements with a named resource.</span></span>

<span data-ttu-id="20846-107">Huomaa, että jos haluat delegoida varattavissa olevan resurssin tehtävälle, varattavissa olevan resurssin ryhmän jäsenellä on oltava riittävästi käytettävissä olevia varauksia.</span><span class="sxs-lookup"><span data-stu-id="20846-107">Note that if you’d like to assign a bookable resource to a task, the bookable resource team member must have enough available bookings.</span></span> <span data-ttu-id="20846-108">Varauksen tilan vahvistustyypin on oltava Sitova varaus ja tilan on oltava Vahvistettu.</span><span class="sxs-lookup"><span data-stu-id="20846-108">The status of the booking must be Commit Type Hard Book and Status Committed.</span></span> <span data-ttu-id="20846-109">Jos resurssilla ei ole riittävästi varauksia, Project Service poistaa delegoinnin ja näyttää seuraavan virhesanoman:</span><span class="sxs-lookup"><span data-stu-id="20846-109">If there aren’t enough bookings for the resource, Project Service removes the assignment and displays the following error message:</span></span>

<span data-ttu-id="20846-110">*Resurssia ei voi delegoida tehtävälle - Seuraaville resursseille ei ole varattu riittävästi tunteja projektissa*</span><span class="sxs-lookup"><span data-stu-id="20846-110">*Unable to assign resource to task - Following resource(s) do not have sufficient hours booked against project*</span></span>

## <a name="book-a-resource-as-a-team-member-and-then-assign-the-resource-to-a-task"></a><span data-ttu-id="20846-111">Varaa resurssi ryhmän jäsenenä ja delegoi resurssi sitten tehtävälle.</span><span class="sxs-lookup"><span data-stu-id="20846-111">Book a resource as a team member and then assign the resource to a task</span></span>

<span data-ttu-id="20846-112">Kun tämä tapa on käytössä resurssi lisätään projektiryhmään. Tämän jälkeen delegoidaan tehtävät projektiaikataulun resurssille.</span><span class="sxs-lookup"><span data-stu-id="20846-112">With this method you add a resource to the project team and then assign tasks to the resource in the project schedule.</span></span> <span data-ttu-id="20846-113">Tämä tehdään seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="20846-113">Here’s how you do this:</span></span>
1.  <span data-ttu-id="20846-114">Lisää uusi ryhmän jäsen ryhmän jäsenen ruudukkoon valitsemalla **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="20846-114">On the team member grid, add a new team member by selecting **New**.</span></span>
2.  <span data-ttu-id="20846-115">Valitse ryhmän jäsenen pikaluontinäytössä varattavissa olevan resurssin nimi ja määritä rooli.</span><span class="sxs-lookup"><span data-stu-id="20846-115">On the Team Member Quick Create screen, select the bookable resource name and set a role.</span></span>
3.  <span data-ttu-id="20846-116">Valitse **alku**- ja **loppupäivämäärät**.</span><span class="sxs-lookup"><span data-stu-id="20846-116">Select the **From** and **To** dates.</span></span>

    > [!div class="mx-imgBorder"] 
    > <span data-ttu-id="20846-117">![Kuvakaappaus ryhmän jäsenen lisäämisestä](media/FAQ-Resources-to-Tasks2-1.png "Kuvakaappaus ryhmän jäsenen lisäämisestä")</span><span class="sxs-lookup"><span data-stu-id="20846-117">![Screenshot of adding team member](media/FAQ-Resources-to-Tasks2-1.png "Screenshot of adding team member")</span></span>
 
4.  <span data-ttu-id="20846-118">Valitse jokin seuraavista resurssin varauksen kohdistustavoista:</span><span class="sxs-lookup"><span data-stu-id="20846-118">Select one of the following allocation methods for booking the resource:</span></span>
    - <span data-ttu-id="20846-119">**Täysi kapasiteetti** varaa resurssin täyden kapasiteetin tietyn alku- ja loppupäivämäärän välille.</span><span class="sxs-lookup"><span data-stu-id="20846-119">**Full Capacity** books the resource’s full capacity for the specified from and to dates.</span></span>
    - <span data-ttu-id="20846-120">**Kapasiteettiprosentti** varaa resurssin kapasiteettiprosentin perusteella tietyn alku- ja loppupäivämäärän välille.</span><span class="sxs-lookup"><span data-stu-id="20846-120">**Percentage Capacity** books the resource for a percentage of the resource's capacity for the specified from and to dates.</span></span>
    - <span data-ttu-id="20846-121">**Tuntien mukaan – jaa tasaisesti** varaa resurssin tietyille tunneille. Aika jaetaan tasan päivää kohti tietyn alku- ja loppupäivämäärän väliselle ajalle.</span><span class="sxs-lookup"><span data-stu-id="20846-121">**By Hours Distribute Evenly** books the resource for a specified number of hours, distributing it evenly per day over the specified from and to dates.</span></span>
    - <span data-ttu-id="20846-122">**Tuntien mukaan – etupainotteinen** varaa resurssin tietyille tunneille. Päiväkohtaiset tunnit jaetaan etupainotteisesti tietyn alku- ja loppupäivämäärän väliselle ajalle.</span><span class="sxs-lookup"><span data-stu-id="20846-122">**By Hours Front Load** books the resource for a specified number of hours, front-loading the per-day hours over the specified from and to dates.</span></span>

    <span data-ttu-id="20846-123">Älä valitse **Ei mitään** -tapaa, koska se lisää resurssin ryhmään, mutta ei luo varauksia, jotka käyttävät resurssin kapasiteettia.</span><span class="sxs-lookup"><span data-stu-id="20846-123">Don’t select **None** because it adds the resource to the team but doesn’t create any bookings that absorb the resource's capacity.</span></span>
5.  <span data-ttu-id="20846-124">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="20846-124">Select **Save**.</span></span>

    <span data-ttu-id="20846-125">Huomaa, että varauksen tunteja on oltava riittävästi, jotta ne kattavat työtunnit ja sen tehtävän päivämäärävälit, jolle tämä resurssi delegoidaan.</span><span class="sxs-lookup"><span data-stu-id="20846-125">Note that the hours of the booking must be enough to cover the effort hours and date ranges of the tasks that you assign this resource to.</span></span> <span data-ttu-id="20846-126">Jos ne eivät vastaa toisiaan, et voi delegoida resurssia tehtävälle.</span><span class="sxs-lookup"><span data-stu-id="20846-126">If they aren’t in alignment, you can’t assign the resource to the task.</span></span>

6.  <span data-ttu-id="20846-127">Valitse tehtävän työrakenteessa resurssin solun avattava luettelo.</span><span class="sxs-lookup"><span data-stu-id="20846-127">On the work breakdown structure (WBS) for the task, click the resource cell dropdown.</span></span> <span data-ttu-id="20846-128">Tee seuraavaksi näin:</span><span class="sxs-lookup"><span data-stu-id="20846-128">Then:</span></span> 

    1. <span data-ttu-id="20846-129">Valitse **Lisää**.</span><span class="sxs-lookup"><span data-stu-id="20846-129">Select **Add**.</span></span>
    2. <span data-ttu-id="20846-130">Valitse **Resurssit**-kohdan alla oleva avattava luettelo ja valitse aiemmin lisäämäsi ryhmän jäsen.</span><span class="sxs-lookup"><span data-stu-id="20846-130">Select the dropdown under **Resources** and select the team member you added above.</span></span>
    3. <span data-ttu-id="20846-131">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="20846-131">Select **OK**.</span></span> <span data-ttu-id="20846-132">Ryhmän jäsen on nyt delegoitu tehtävälle.</span><span class="sxs-lookup"><span data-stu-id="20846-132">The team member is now assigned to the task.</span></span>

    > [!div class="mx-imgBorder"] 
    > <span data-ttu-id="20846-133">![Näyttökuva resurssien lisäämisestä työrakenteen avulla](media/FAQ-Resources-to-Tasks2-2.png "Näyttökuva resurssien lisäämisestä työrakenteen avulla")</span><span class="sxs-lookup"><span data-stu-id="20846-133">![Screenshot of adding resources with WBS](media/FAQ-Resources-to-Tasks2-2.png "Screenshot of adding resources with WBS")</span></span>
 
<span data-ttu-id="20846-134">Ryhmän jäsenen ruudukon Delegoidut tunnit -kohdassa on resurssin delegoitujen tuntien kooste.</span><span class="sxs-lookup"><span data-stu-id="20846-134">On the team member grid, you’ll see the aggregate of the resource’s assigned hours under Assigned Hours.</span></span> <span data-ttu-id="20846-135">Se on yhtä suuri tai pienempi kuin resurssin varatut tunnit.</span><span class="sxs-lookup"><span data-stu-id="20846-135">It will be less than or equal to the booked hours for the resource.</span></span> 

> [!div class="mx-imgBorder"] 
> <span data-ttu-id="20846-136">![Resurssin delegoitujen tuntien näyttökuva](media/FAQ-Resources-to-Tasks2-3.png "Resurssin delegoitujen tuntien näyttökuva")</span><span class="sxs-lookup"><span data-stu-id="20846-136">![Screenshot of assigned hours for a resource](media/FAQ-Resources-to-Tasks2-3.png "Screenshot of assigned hours for a resource")</span></span>
 
<span data-ttu-id="20846-137">Jos tehtävä, jota yrität delegoida resurssille, alkaa resurssin varausten loppupäivämäärän jälkeen, resurssi ei näy avattavassa luettelossa.</span><span class="sxs-lookup"><span data-stu-id="20846-137">If the task you’re attempting to assign to the resource starts after the end date of the resources bookings, the resource won’t appear in the dropdown.</span></span>

<span data-ttu-id="20846-138">Huomaa, että voit delegoida resurssin varattujen tunteja useammille tunneille, jos resurssilla on jäljellä delegoimatonta kapasiteettia.</span><span class="sxs-lookup"><span data-stu-id="20846-138">Note that you can assign a resource to more hours than their booked hours if the resource has some remaining unassigned capacity.</span></span> <span data-ttu-id="20846-139">Tässä tapauksessa resurssi on vain osittain delegoitu varausten perusteella.</span><span class="sxs-lookup"><span data-stu-id="20846-139">In this case the resource will only be partially assigned up to their bookings.</span></span> <span data-ttu-id="20846-140">Näet jäljellä olevat delegoimattomat tehtävän tunnit, kun lisäät työrakenteeseen Resursoimattomat tunnit -sarakkeen.</span><span class="sxs-lookup"><span data-stu-id="20846-140">You can see these remaining unassigned task hours by adding the Unstaffed Hours column to the work breakdown structure.</span></span>

<span data-ttu-id="20846-141">Jos resurssit on delegoitu niiden varatuille tunneille (varattuja tunteja on yhtä paljon kuin delegoituja tunteja), näkyviin tulee seuraava virhesanoma, kun yrität delegoida niille uusia tehtäviä:</span><span class="sxs-lookup"><span data-stu-id="20846-141">If resources are assigned to their booked hours (their booked hours equals their assigned hours), you’ll see the following error message when you attempt to assign them further tasks:</span></span>

<span data-ttu-id="20846-142">*Resurssia ei voi delegoida tehtävälle - Seuraaville resursseille ei ole varattu riittävästi tunteja projektissa.*</span><span class="sxs-lookup"><span data-stu-id="20846-142">*Unable to assign resource to task - Following resource(s) do not have sufficient hours booked against project.*</span></span>

<span data-ttu-id="20846-143">Lisäksi projektipäällikön ryhmän oletusjäsen, joka on lisätty ryhmään projektin luomisen yhteydessä, on lisätty ilman varauksia. Hänelle ei voi delegoida tehtäviä.</span><span class="sxs-lookup"><span data-stu-id="20846-143">Additionally, the default project manager team member that is added to the team when you create the project is added without any bookings and can’t be assigned to any task.</span></span> <span data-ttu-id="20846-144">Ne eivät näy resurssin tehtävien avattavassa luettelossa.</span><span class="sxs-lookup"><span data-stu-id="20846-144">They won’t show up in the resource dropdown for tasks.</span></span>

<span data-ttu-id="20846-145">Jos haluat delegoida tämän resurssin, poista se ryhmästä ja lisää uudelleen käyttämällä jotain muuta kohdistustapaa kuin Ei mitään.</span><span class="sxs-lookup"><span data-stu-id="20846-145">If you want to assign this resource, you need to remove them from the team and then re-add them with an allocation method other than None.</span></span> <span data-ttu-id="20846-146">Jäsenet lisätään ryhmään projektin luontivaiheessa siksi, että projektissa on oletusarvoisesti vähintään yksi projektin hyväksyjä.</span><span class="sxs-lookup"><span data-stu-id="20846-146">The reason they’re added to the team when the project is created is so that a project has at least one project approver by default.</span></span>

## <a name="create-a-generic-team-member-through-role-assignment-on-tasks"></a><span data-ttu-id="20846-147">Yleisen ryhmän jäsenen luominen roolin delegoinnin kautta tehtävissä</span><span class="sxs-lookup"><span data-stu-id="20846-147">Create a generic team member through role assignment on tasks</span></span>

<span data-ttu-id="20846-148">Tämä tapa varmistaa sen, että resursseilla on riittävästi tehtävien varauksia.</span><span class="sxs-lookup"><span data-stu-id="20846-148">This method assures that resources have enough bookings for tasks.</span></span> <span data-ttu-id="20846-149">Luo ensin paikkamerkki tai yleinen resurssi, joka kuvaa sen nimetyn resurssin ominaisuudet, jota haluat käsitellä tehtävissä. Tämä tapahtuu luomalla ryhmä sen jälkeen, kun tehtäville on delegoitu roolit.</span><span class="sxs-lookup"><span data-stu-id="20846-149">First, you create a placeholder or generic resource that describes the characteristics of the named resource you ultimately want to work on the tasks by generating a team after assigning roles to tasks.</span></span> <span data-ttu-id="20846-150">Tämä tehdään seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="20846-150">Here’s how you do this:</span></span>

1. <span data-ttu-id="20846-151">Valitse työrakenteessa tehtävä.</span><span class="sxs-lookup"><span data-stu-id="20846-151">On the work breakdown structure, select a task.</span></span>
2. <span data-ttu-id="20846-152">Valitse resurssin solun avattavan **Delegoitu rooli** -luettelon kuvake.</span><span class="sxs-lookup"><span data-stu-id="20846-152">Select the **Assigned Role** dropdown icon in the resource cell.</span></span>
3. <span data-ttu-id="20846-153">Valitse avattava **Rooli**-luettelo ja valitse yleisen resurssin rooli.</span><span class="sxs-lookup"><span data-stu-id="20846-153">Select the **Role** dropdown and select the role for the generic resource.</span></span>
4. <span data-ttu-id="20846-154">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="20846-154">Select **OK**.</span></span>

    > [!div class="mx-imgBorder"] 
    > <span data-ttu-id="20846-155">![Näyttökuva resurssin lisäämisestä työrakenteen avulla](media/FAQ-Resources-to-Tasks2-4.png "Näyttökuva resurssin lisäämisestä työrakenteen avulla")</span><span class="sxs-lookup"><span data-stu-id="20846-155">![Screenshot of using WBS to add resource](media/FAQ-Resources-to-Tasks2-4.png "Screenshot of using WBS to add resource")</span></span>
 
<span data-ttu-id="20846-156">Kun roolit on delegoitu tehtäville työrakenteessa, valitse **Luo projektiryhmä**.</span><span class="sxs-lookup"><span data-stu-id="20846-156">Once you’ve completed assigning roles to the tasks in the WBS, select **Generate Project Team**.</span></span> <span data-ttu-id="20846-157">Project Service luo vähimmäismäärän yleisen ryhmän jäseniä näiden roolien, resursointiorganisaation yksiköiden ja projektikalenterin perusteella yhdistämällä tehtävien delegoinnit.</span><span class="sxs-lookup"><span data-stu-id="20846-157">Project Service creates the minimum number of generic team members based on the roles, resourcing organization units, and project calendar by aggregating the task assignments.</span></span>

> [!div class="mx-imgBorder"] 
> <span data-ttu-id="20846-158">![Kuvakaappaus projektiryhmän luomisesta](media/FAQ-Resources-to-Tasks2-5.png "Kuvakaappaus projektiryhmän luomisesta")</span><span class="sxs-lookup"><span data-stu-id="20846-158">![Screenshot of generating project team](media/FAQ-Resources-to-Tasks2-5.png "Screenshot of generating project team")</span></span>
 
<span data-ttu-id="20846-159">Ryhmän jäsenen ruudukossa näkyvät yleisen resurssityypin resurssit ja niiden rooli sekä sijainnin nimi.</span><span class="sxs-lookup"><span data-stu-id="20846-159">On the Team Member grid, you’ll see resources of the Generic Resource type with the role and position name.</span></span> <span data-ttu-id="20846-160">Jos roolissa on oltava kaksi resurssia, jotta työ voidaan tehdä valmiiksi, Luo ryhmä -toiminto luo kaksi ryhmän jäsentä ja erottelee ne toisistaan sijainnin nimen avulla.</span><span class="sxs-lookup"><span data-stu-id="20846-160">If two resources are needed for a role to complete the work, the Generate Team feature creates two team members and uses position name to set them apart.</span></span>

> [!div class="mx-imgBorder"] 
> <span data-ttu-id="20846-161">![Näyttökuva kahden yleisen resurssin lisäämisestä](media/FAQ-Resources-to-Tasks2-6.png "Näyttökuva kahden yleisen resurssin lisäämisestä")</span><span class="sxs-lookup"><span data-stu-id="20846-161">![Screenshot of adding two generic resources](media/FAQ-Resources-to-Tasks2-6.png "Screenshot of adding two generic resources")</span></span>
 
<span data-ttu-id="20846-162">Voit avata yleisen ryhmän jäsenen taustalla olevan resurssitarpeen valitsemalla Resurssitarve-kohdan alla olevan linkin.</span><span class="sxs-lookup"><span data-stu-id="20846-162">You can open the backing resource requirement for the generic team member by selecting the link under Resource Requirement.</span></span>

> [!div class="mx-imgBorder"] 
> <span data-ttu-id="20846-163">![Näyttökuva taustalla olevan resurssitarpeen avaamisesta](media/FAQ-Resources-to-Tasks2-7.png "Näyttökuva taustalla olevan resurssitarpeen avaamisesta")</span><span class="sxs-lookup"><span data-stu-id="20846-163">![Screenshot of opening backing resource requirement](media/FAQ-Resources-to-Tasks2-7.png "Screenshot of opening backing resource requirement")</span></span>

<span data-ttu-id="20846-164">Valitse yleisen resurssin **Varaa**-kohta. Tämän jälkeen voit etsiä todellisen resurssin ja varata sen aikataulutaulukon avulla.</span><span class="sxs-lookup"><span data-stu-id="20846-164">Select **Book** for the generic resource, and then you can use the schedule board to find and book a real resource.</span></span> <span data-ttu-id="20846-165">Voit myös lähettää tarpeen resurssipäällikön tekemälle toteutukselle valitsemalla **Lähetä pyyntö**.</span><span class="sxs-lookup"><span data-stu-id="20846-165">You can also submit the requirement for fulfillment by a resource manager by selecting **Submit Request**.</span></span>

<span data-ttu-id="20846-166">Kun yleinen resurssi toteutetaan nimetyn resurssin kanssa, yleinen resurssi poistetaan ryhmästä ja yleisen resurssin tehtävän delegoinnit delegoidaan nimetylle resurssille, joka toteutti yleisen resurssin resurssitarpeen.</span><span class="sxs-lookup"><span data-stu-id="20846-166">When the generic resource is fulfilled with a named resource, the generic resource is removed from the team and the task assignments for the generic resource are assigned to the named resource that fulfilled the generic resource’s resource requirement.</span></span>
 

