---
title: Kohdenna resurssi tehtävälle
description: Tässä aiheessa on tietoja resurssien kohdentamisesta tehtäville.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 9/27/2019
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 77f13d1e96b76dfea241fbf7a67d5676582f0235
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/16/2020
ms.locfileid: "4075537"
---
# <a name="assign-a-resource-to-a-task"></a><span data-ttu-id="3c172-103">Kohdenna resurssi tehtävälle</span><span class="sxs-lookup"><span data-stu-id="3c172-103">Assign a resource to a task</span></span>

<span data-ttu-id="3c172-104">Microsoft Dynamics 365 Project Service Automationissa resursseja voi kohdentaa tehtävälle kolmella eri tavalla.</span><span class="sxs-lookup"><span data-stu-id="3c172-104">There are three ways to assign a resource to a task in Microsoft Dynamics 365 Project Service Automation.</span></span>

## <a name="book-a-resource-as-a-team-member-and-then-assign-the-resource-to-a-task"></a><span data-ttu-id="3c172-105">Resurssin varaaminen ryhmän jäseneksi ja resurssin kohdentaminen tehtävälle</span><span class="sxs-lookup"><span data-stu-id="3c172-105">Book a resource as a team member, and then assign the resource to a task</span></span>

<span data-ttu-id="3c172-106">Voit lisätä resurssin projektiryhmään ja kohdentaa resurssin projektiaikataulun tehtäville.</span><span class="sxs-lookup"><span data-stu-id="3c172-106">You can add a resource to the project team, and then assign the resource to tasks in the project schedule.</span></span>

1. <span data-ttu-id="3c172-107">Lisää uusi ryhmän jäsen **Ryhmän jäsen** -välilehdelle valitsemalla **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="3c172-107">On the **Team Member** tab, add a new team member by selecting **New**.</span></span> 

2. <span data-ttu-id="3c172-108">Näkyviin tulee **Ryhmän jäsenen pikaluonti** -paneeli, jossa voit valita varattavissa olevan resurssin nimen ja määrittää sen roolin.</span><span class="sxs-lookup"><span data-stu-id="3c172-108">The **Team Member Quick Create** panel opens, where you can select the bookable resource name and set a role.</span></span> 

    <span data-ttu-id="3c172-109">Valitse jokin seuraavista resurssin varauksen kohdennustavoista:</span><span class="sxs-lookup"><span data-stu-id="3c172-109">Select one of the following allocation methods for the resource’s booking:</span></span>

    - <span data-ttu-id="3c172-110">**Täysi kapasiteetti** varaa resurssin täyden kapasiteetin tietyn alku- ja loppupäivämäärän välille.</span><span class="sxs-lookup"><span data-stu-id="3c172-110">**Full Capacity** books the resource’s full capacity for the specified from and to dates.</span></span>
    - <span data-ttu-id="3c172-111">**Kapasiteettiprosentti** varaa resurssin kapasiteettiprosentin perusteella tietyn alku- ja loppupäivämäärän välille.</span><span class="sxs-lookup"><span data-stu-id="3c172-111">**Percentage Capacity** books the resource for a percentage of the resource's capacity for the specified from and to dates.</span></span>
    - <span data-ttu-id="3c172-112">**Tuntien mukaan – jaa tasaisesti** varaa resurssin tietyille tunneille. Tunnit jaetaan tasan päivää kohti tietyn alku- ja loppupäivämäärän väliselle ajalle.</span><span class="sxs-lookup"><span data-stu-id="3c172-112">**By Hours Distribute Evenly** books the resource for a specified number of hours, distributing them evenly per day over the specified from and to dates.</span></span>
    - <span data-ttu-id="3c172-113">**Tuntien mukaan – etupainotteinen** varaa resurssin tietyille tunneille. Päiväkohtaiset tunnit jaetaan etupainotteisesti tietyn alku- ja loppupäivämäärän väliselle ajalle.</span><span class="sxs-lookup"><span data-stu-id="3c172-113">**By Hours Front Load** books the resource for a specified number of hours, front-loading the per-day hours over the specified from and to dates.</span></span>
    - <span data-ttu-id="3c172-114">**Ei mitään** -vaihtoehto lisää ryhmään resurssin, mutta ei luo varauksia, jotka käyttävät resurssin kapasiteettia.</span><span class="sxs-lookup"><span data-stu-id="3c172-114">**None** adds the resource to the team but doesn’t create any bookings that absorb their capacity.</span></span>

3. <span data-ttu-id="3c172-115">Valitse tehtävän **Aikataulut** -ruudukossa resurssin solun **Resurssi** -kuvake ja valitse sitten **Ryhmän jäsenet** -kohdasta juuri lisätty ryhmän jäsen.</span><span class="sxs-lookup"><span data-stu-id="3c172-115">On the **Schedule** grid for a task, select the **Resource** icon in the resource cell, and then under **Team Members** , select the team member you just added.</span></span> 

> [!NOTE]
> <span data-ttu-id="3c172-116">Resurssin varatut tunnit ja kohdennetut tunnit näkyvät sekä **Ryhmän jäsen** - että **Täsmäytys** -välilehdessä.</span><span class="sxs-lookup"><span data-stu-id="3c172-116">On the **Team Member** and **Reconciliation** tabs, the resource shows booked and assigned hours.</span></span> <span data-ttu-id="3c172-117">Tuntien pitäisi olla samat, mutta se ei ole pakollista, koska varaukset ja kohdennukset eivät ole tiiviissä yhteydessä toisiinsa.</span><span class="sxs-lookup"><span data-stu-id="3c172-117">The hours should be the same, but it isn't required as bookings and assignments are not tightly coupled.</span></span> <span data-ttu-id="3c172-118">**Täsmäytys** -välilehti sisältää tietoja, jos tuntien määrät eivät ole samat. Näin voi käydä, jos esimerkiksi resurssille kohdennettuja tunteja on enemmän kuin varattuja tunteja.</span><span class="sxs-lookup"><span data-stu-id="3c172-118">The **Reconciliation** tab gives you details when they are different, such as when you assign a resource more hours than you have booked.</span></span> <span data-ttu-id="3c172-119">Tarvittaessa voit korjata tietoja laajentamalla resurssin varauksia tai muuttamalla kohdennusta.</span><span class="sxs-lookup"><span data-stu-id="3c172-119">If needed, you can correct the information by extending the resource's bookings or changing the assignment.</span></span>

## <a name="create-a-generic-team-member-through-task-assignment"></a><span data-ttu-id="3c172-120">Yleisen ryhmän jäsenen luominen tehtäväkohdennuksen kautta</span><span class="sxs-lookup"><span data-stu-id="3c172-120">Create a generic team member through task assignment</span></span>

<span data-ttu-id="3c172-121">Kun luot yleisen ryhmän jäsenen tehtäväkohdennuksella, luot ensin paikkamerkin tai yleisen resurssin, joka kuvaa sen nimetyn resurssin ominaisuudet, jonka haluat lopulta suorittavan tehtäviä.</span><span class="sxs-lookup"><span data-stu-id="3c172-121">When you create a generic team member through task assignment, you create a placeholder or generic resource that describes the characteristics of the named resource you ultimately want to work on the tasks.</span></span> <span data-ttu-id="3c172-122">Tämän jälkeen voit luoda tarpeen (tai lähettää pyynnön käyttämällä tarvetta), jota käytetään nimetyn resurssin haussa ja varauksessa.</span><span class="sxs-lookup"><span data-stu-id="3c172-122">You then generate a requirement (or submit a request using the requirement) that is used to search for and book the named resource.</span></span>

1. <span data-ttu-id="3c172-123">Valitse tehtävän **Aikataulut** -ruudukossa **Resurssi** -kuvake resurssin solussa.</span><span class="sxs-lookup"><span data-stu-id="3c172-123">On the **Schedule** grid for a task, select the **Resource** icon in the resource cell.</span></span>

2. <span data-ttu-id="3c172-124">Kirjoita nimi, joka toimii resurssin nimen paikkamerkkinä.</span><span class="sxs-lookup"><span data-stu-id="3c172-124">Type a name to serve as the placeholder resource’s name.</span></span> <span data-ttu-id="3c172-125">Esimerkiksi ohjelmapäällikkö.</span><span class="sxs-lookup"><span data-stu-id="3c172-125">For example, Program Manager.</span></span>

3. <span data-ttu-id="3c172-126">Valitse **Luo** ja määritä yleisen resurssin rooli kentässä **Projektiryhmän jäsenen pikaluonti**.</span><span class="sxs-lookup"><span data-stu-id="3c172-126">Select **Create** , and in the **Quick Create Project Team Member** field, set the role for the generic resource.</span></span>

4. <span data-ttu-id="3c172-127">Voit jatkaa tehtävien delegoimista tälle paikkamerkin resurssille valitsemalla tehtävälle resurssin **Resurssinvalitsin** -kohdasta.</span><span class="sxs-lookup"><span data-stu-id="3c172-127">You can continue to assign tasks to this placeholder resource by selecting the resource on the **Resource Selector** for the task.</span></span> <span data-ttu-id="3c172-128">Ne löytyvät **Ryhmän jäsenet** -kohdasta.</span><span class="sxs-lookup"><span data-stu-id="3c172-128">They’re listed under **Team Members**.</span></span>

5. <span data-ttu-id="3c172-129">Kun olet kohdentanut yleisen resurssin, valitse se **Ryhmä** -välilehdessä ja valitse sitten **Luo tarve** luodaksesi resurssitarpeen yleiselle resurssille.</span><span class="sxs-lookup"><span data-stu-id="3c172-129">When you’re done assigning the generic resource, select the generic resource on the **Team** tab, and then select **Generate Requirement** to create a resource requirement for the generic resource.</span></span>

6. <span data-ttu-id="3c172-130">Valitse yleisen resurssin **Varaa** -kohta.</span><span class="sxs-lookup"><span data-stu-id="3c172-130">Select **Book** for the generic resource.</span></span> <span data-ttu-id="3c172-131">Tämän jälkeen voit etsiä aikataulutaulukon avulla todellisen resurssin ja varata sen.</span><span class="sxs-lookup"><span data-stu-id="3c172-131">You can then use the Schedule board to find and book a real resource.</span></span> <span data-ttu-id="3c172-132">Voit myös lähettää tarpeen resurssipäällikön tekemälle toteutukselle.</span><span class="sxs-lookup"><span data-stu-id="3c172-132">You can also submit the requirement for fulfillment by a resource manager.</span></span>

7. <span data-ttu-id="3c172-133">Kun yleinen resurssi toteutetaan nimetyn resurssin kanssa, yleinen resurssi poistetaan ryhmästä ja yleisen resurssin tehtävän delegoinnit delegoidaan nimetylle resurssille, joka toteutti yleisen resurssin resurssitarpeen.</span><span class="sxs-lookup"><span data-stu-id="3c172-133">When the generic resource is fulfilled with a named resource, the generic resource is removed from the team and the task assignments for the generic resource are assigned to the named resource that fulfilled the generic resource’s resource requirement.</span></span>

## <a name="assign-a-named-resource-from-the-list-of-all-bookable-resources"></a><span data-ttu-id="3c172-134">Nimetyn resurssin kohdentaminen kaikkien varattavissa olevien resurssien luettelosta</span><span class="sxs-lookup"><span data-stu-id="3c172-134">Assign a named resource from the list of all bookable resources</span></span>

<span data-ttu-id="3c172-135">**Resurssinvalitsin** -kohdan hakuruudun avulla voit hakea kaikki varattavissa olevat resurssit ja kohdentaa ne tehtävälle.</span><span class="sxs-lookup"><span data-stu-id="3c172-135">You can use the search box in the **Resource Selector** to search all bookable resources and assign them to a task.</span></span>

<span data-ttu-id="3c172-136">Tällä tavoin kohdennetut resurssit lisätään ryhmään ilman varauksia.</span><span class="sxs-lookup"><span data-stu-id="3c172-136">Resources assigned this way are added to the team without any bookings.</span></span> <span data-ttu-id="3c172-137">tämä vastaa ryhmän jäsenen lisäämistä ja Ei mitään -kohdennusmenetelmän valitsemista.</span><span class="sxs-lookup"><span data-stu-id="3c172-137">This is similar to adding a team member and selecting None as the allocation method.</span></span> <span data-ttu-id="3c172-138">Resurssi näkyy **Ryhmä** - ja **Täsmäytys** -välilehdessä resurssina, jolla on vain kohdennuksia. Sillä on varausvaje.</span><span class="sxs-lookup"><span data-stu-id="3c172-138">The resource is displayed in the **Team** and **Reconciliation** tabs as resources with only assignments and a booking deficit.</span></span> <span data-ttu-id="3c172-139">Varaa ne, jos haluat käyttää niitä.</span><span class="sxs-lookup"><span data-stu-id="3c172-139">Book them if you want to use their availability.</span></span>

1. <span data-ttu-id="3c172-140">Valitse tehtävän **Aikataulut** -ruudukossa **Resurssi** -kuvake resurssin solussa.</span><span class="sxs-lookup"><span data-stu-id="3c172-140">On the **Schedule** grid for a task, select the **Resource** icon in the resource cell.</span></span>

2. <span data-ttu-id="3c172-141">Aloita kirjoittamalla nimi.</span><span class="sxs-lookup"><span data-stu-id="3c172-141">Start typing a name.</span></span> <span data-ttu-id="3c172-142">Nimen hakutulokset näkyvät **Muut resurssit** -kohdan kohdassa **Resurssinvalitsin**.</span><span class="sxs-lookup"><span data-stu-id="3c172-142">The search results for the name are displayed in the **Resource Selector** under **Other Resources**.</span></span>

3. <span data-ttu-id="3c172-143">Valitse resurssi, jonka haluat kohdentaa tehtävälle.</span><span class="sxs-lookup"><span data-stu-id="3c172-143">Select the resource that you want to assign to the task.</span></span>

