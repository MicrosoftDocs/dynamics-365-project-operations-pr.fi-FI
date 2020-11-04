---
title: Nimettyjen varattavissa olevien resurssien varaaminen projektiryhmälle ja tehtävien kohdennus
description: Tässä aiheessa on tietoja miten nimetyt resurssit varataan projektiryhmille ja miten ne kohdennetaan tehtäville.
author: JohnPBurrows
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 11/28/2018
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
ms.openlocfilehash: defc92e701ae6baf9d54f41dca123a09ef834c35
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/16/2020
ms.locfileid: "4075467"
---
# <a name="book-named-bookable-resources-to-a-project-team-and-assign-tasks"></a><span data-ttu-id="2c4a0-103">Nimettyjen varattavissa olevien resurssien varaaminen projektiryhmälle ja tehtävien kohdennus</span><span class="sxs-lookup"><span data-stu-id="2c4a0-103">Book named bookable resources to a project team and assign tasks</span></span> 

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="2c4a0-104">Voit lisätä nimetyn resurssin projektiryhmään varaamalla sen suoraan ryhmään.</span><span class="sxs-lookup"><span data-stu-id="2c4a0-104">You can  add a named resource to your project team by booking them directly onto the team.</span></span> <span data-ttu-id="2c4a0-105">Toimi seuraavien vaiheiden mukaisesti.</span><span class="sxs-lookup"><span data-stu-id="2c4a0-105">To do this, complete the following steps.</span></span>

1. <span data-ttu-id="2c4a0-106">Siirry Project Service Automationissa kohtaan **Projektit** ja avaa projekti, jota varten teet varausta.</span><span class="sxs-lookup"><span data-stu-id="2c4a0-106">In  Project Service Automation, go to **Projects** , and select the open the project that you are booking for.</span></span>
2. <span data-ttu-id="2c4a0-107">Napsauta **Projekti** -sivun **Tyhmä** -välilehdessä **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="2c4a0-107">On the **Project** page, on the **Team** tab, click **New**.</span></span> 

![Ryhmän jäsenen lisääminen ryhmävälilehdestä](media/RM-how-to-1.png)

3. <span data-ttu-id="2c4a0-109">Valitse varattavissa oleva resurssi **Projektiryhmän jäsenen pikaluonti** -valintaikkunassa.</span><span class="sxs-lookup"><span data-stu-id="2c4a0-109">In the **Quick Create Project Team Member** dialog box, select the bookable resource.</span></span> <span data-ttu-id="2c4a0-110">**Rooli** -kenttä täytetään resurssin oletusroolilla, jos sillä sellainen on.</span><span class="sxs-lookup"><span data-stu-id="2c4a0-110">The **Role** field will populate with the resource's default role if they have one assigned.</span></span> <span data-ttu-id="2c4a0-111">Voit muuttaa roolia tarvittaessa.</span><span class="sxs-lookup"><span data-stu-id="2c4a0-111">You can change the role if needed.</span></span> 
4. <span data-ttu-id="2c4a0-112">Valitse alkamis- ja päättymispäivä resurssin tarpeelle ja valitse resurssin kapasiteetin kohdennustapa.</span><span class="sxs-lookup"><span data-stu-id="2c4a0-112">Select the from and to dates that the resource will be needed and select the allocation method of the resource's capacity.</span></span> 
5. <span data-ttu-id="2c4a0-113">Jos haluat ryhmän jäsenen olevan projektin hyväksyjä, valitse **Projektin hyväksyjä** -kentässä **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="2c4a0-113">If you want the team member to be a project approver, select **Yes** in the **Project Approver** field.</span></span> <span data-ttu-id="2c4a0-114">Tämä tarkoittaa, että ryhmän jäsen voi tässä projektissa hyväksyä toimitettuja aika- ja kulumerkintöjä.</span><span class="sxs-lookup"><span data-stu-id="2c4a0-114">This will mean that the team member can approve submitted time and expense entries for this project.</span></span> 
6. <span data-ttu-id="2c4a0-115">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="2c4a0-115">Click **Save**.</span></span>

![Ryhmän jäsenen lisääminen pikaluontilomakkeessa](media/RM-how-to-2.png)


<span data-ttu-id="2c4a0-117">Voit nyt kohdentaa varatun resurssin projektin tehtäville.</span><span class="sxs-lookup"><span data-stu-id="2c4a0-117">You can now assign the booked resource to tasks on the project.</span></span> <span data-ttu-id="2c4a0-118">Napsauta **Projekti** -sivulla **Aikataulut** -välilehteä kohdentaaksesi tehtäviä uudelle resurssille.</span><span class="sxs-lookup"><span data-stu-id="2c4a0-118">On the **Project** page, click the **Schedule** tab to assign tasks to the new resource.</span></span> <span data-ttu-id="2c4a0-119">Tehtäväruudukon **Resurssit** -kentästä käynnistettävä resurssinvalitsin näyttää ne ryhmän jäsenet, jotka voidaan valita.</span><span class="sxs-lookup"><span data-stu-id="2c4a0-119">The resource picker that is launched from the **Resources** field in the task grid will show the team members that you can select.</span></span>

![Ryhmän jäsenen kohdentaminen aikataulutaulukossa olevalle tehtävälle.](media/RM-how-to-3.png)

<span data-ttu-id="2c4a0-121">Project Service Automationin (PSA) versiossa 3 resurssivaraukset ja tehtäväkohdennukset eivät ole tiiviissä yhteydessä toisiinsa.</span><span class="sxs-lookup"><span data-stu-id="2c4a0-121">In version 3 for Project Service Automation (PSA), resource bookings and task assignments are not tightly coupled.</span></span> <span data-ttu-id="2c4a0-122">Tämä tarkoittaa, että voit aikataulun resurssinvalitsinta käyttäessäsi kohdentaa ryhmän jäsenille tehtäviä, joiden tuntimäärä ylittää heidän varaustensa projektissa kattaman tuntimäärän.</span><span class="sxs-lookup"><span data-stu-id="2c4a0-122">This means that when you use the resource picker in the schedule, you can assign tasks to team members for more hours than their bookings cover on the project.</span></span>
<span data-ttu-id="2c4a0-123">Voit tarkastella ryhmän jäsenen varausten ja kohdennusten välisiä eroja **Ryhmä** - tai **Resurssin täsmäytys** -välilehdellä. Voit myös täsmäyttää resurssien varauksia ja kohdennuksia yksityiskohtaisemmalla tasolla.</span><span class="sxs-lookup"><span data-stu-id="2c4a0-123">You can see the differences between team member bookings and assignments on the **Team** tab or on the **Resource Reconciliation** tab. You can also reconcile the differences between bookings and assignments for resources at a more detailed level.</span></span>

![Resurssin täsmäytys -välilehti](media/RM-how-to-4.png)

<span data-ttu-id="2c4a0-125">Voit myös käyttää **Aikataulut** -välilehden resurssinvalitsinta etsiäksesi ja valitaksesi varattavissa olevia resursseja, jotka eivät vielä kuulu projektiryhmään.</span><span class="sxs-lookup"><span data-stu-id="2c4a0-125">You can also use the resource picker on the **Schedule** tab to search for and select bookable resources that are not already part of the project team.</span></span> <span data-ttu-id="2c4a0-126">Nämä näkyvät resurssinvalitsimessa nimellä **Muut resurssit**.</span><span class="sxs-lookup"><span data-stu-id="2c4a0-126">These are shown in the resource picker as **Other Resources**.</span></span>

![Ryhmään kuulumattoman resurssin kohdentaminen tehtävälle](media/RM-how-to-5.png)

<span data-ttu-id="2c4a0-128">Kun teet näin, resurssi lisätään projektiryhmään ja se kohdennetaan tehtävällä, mutta varauksia ei luoda.</span><span class="sxs-lookup"><span data-stu-id="2c4a0-128">When you do this, the resource is added to the project team and assigned to the task, but no bookings are generated.</span></span>

![Ryhmän jäsen, jolla on kohdennuksia muttei varauksia](media/RM-how-to-6.png)

<span data-ttu-id="2c4a0-130">Voit käyttää **Täsmäytys** -välilehden varauksenlaajennustoimintoa tai kohtaa **aikataulutaulukko** varataksesi resurssin kapasiteettia projektille.</span><span class="sxs-lookup"><span data-stu-id="2c4a0-130">You can use the **Reconciliation** tab’s extend booking capability or the **Schedule Board** to book the resource’s capacity to the project.</span></span>

![Ryhmän jäsenen varausten laajentaminen resurssin täsmäyksen välilehdessä](media/RM-how-to-7.png)

<span data-ttu-id="2c4a0-132">Kun ryhmän jäsen on varattu projektillesi, voit käyttää niiden varausten hallitsemiseen varausten ylläpitoa tai aikataulutaulukkoa.</span><span class="sxs-lookup"><span data-stu-id="2c4a0-132">After a team member is booked on your project, you can use maintain bookings or use the Schedule Board directly to manage their bookings.</span></span>
