---
title: Ryhmän jäsenten ylläpitäminen
description: Tässä aiheessa on tietoja nimettyjen resurssien varaamisesta projektiryhmille ja niiden kohdentamisesta tehtäville.
author: ruhercul
manager: AnnBe
ms.date: 10/05/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 60b6788d881518502d314e9ee5daf6bbc0ae8764
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5286829"
---
# <a name="maintain-team-members"></a><span data-ttu-id="8adbc-103">Ryhmän jäsenten ylläpitäminen</span><span class="sxs-lookup"><span data-stu-id="8adbc-103">Maintain team members</span></span>

<span data-ttu-id="8adbc-104">_**Koskee:** Project Operationsin resurssiin / muuhun kuin resurssiin perustuvia skenaarioita, Lite-käyttöönotto-kaupasta proformalaskutukseen_</span><span class="sxs-lookup"><span data-stu-id="8adbc-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="8adbc-105">Voit lisätä nimetyn resurssin projektiryhmään varaamalla sen suoraan ryhmään.</span><span class="sxs-lookup"><span data-stu-id="8adbc-105">You can add a named resource to your project team by booking them directly to the team.</span></span>

1. <span data-ttu-id="8adbc-106">Siirry Dynamics 365 Project Operationsissa kohtaan **Projektit** ja avaa projekti, jota varten teet varausta.</span><span class="sxs-lookup"><span data-stu-id="8adbc-106">In Dynamics 365 Project Operations, go to **Projects**, and select the open the project that you're booking for.</span></span>
2. <span data-ttu-id="8adbc-107">Valitse **Projekti**-sivun **Ryhmä**-välilehdessä **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="8adbc-107">On the **Project** page, on the **Team** tab, select **New**.</span></span> 
3. <span data-ttu-id="8adbc-108">Valitse varattavissa oleva resurssi **Projektiryhmän jäsenen pikaluonti** -valintaikkunassa.</span><span class="sxs-lookup"><span data-stu-id="8adbc-108">In the **Quick Create Project Team Member** dialog box, select the bookable resource.</span></span> <span data-ttu-id="8adbc-109">**Rooli**-kenttä täytetään resurssin oletusroolilla, jos sillä sellainen on.</span><span class="sxs-lookup"><span data-stu-id="8adbc-109">The **Role** field will populate with the resource's default role if they have one assigned.</span></span> <span data-ttu-id="8adbc-110">Voit muuttaa roolia.</span><span class="sxs-lookup"><span data-stu-id="8adbc-110">You can change the role.</span></span> 
4. <span data-ttu-id="8adbc-111">Valitse alkamis- ja päättymispäivä resurssin tarpeelle ja valitse resurssin kapasiteetin kohdennustapa.</span><span class="sxs-lookup"><span data-stu-id="8adbc-111">Select the from and to dates that the resource will be needed, and select the allocation method of the resource's capacity.</span></span> 
5. <span data-ttu-id="8adbc-112">Jos haluat ryhmän jäsenen olevan projektin hyväksyjä, valitse **Projektin hyväksyjä** -kentässä **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="8adbc-112">In the **Project Approver** field, select **Yes** if you want the team member to be a project approver.</span></span> <span data-ttu-id="8adbc-113">Ryhmän jäsen voi tässä projektissa hyväksyä toimitettuja aika- ja kulumerkintöjä.</span><span class="sxs-lookup"><span data-stu-id="8adbc-113">The team member can approve submitted time and expense entries for this project.</span></span> 
6. <span data-ttu-id="8adbc-114">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="8adbc-114">Select **Save**.</span></span>

<span data-ttu-id="8adbc-115">Voit nyt kohdentaa varatun resurssin projektin tehtäville.</span><span class="sxs-lookup"><span data-stu-id="8adbc-115">You can now assign the booked resource to tasks on the project.</span></span> <span data-ttu-id="8adbc-116">Valitse **Projekti** -sivulla **Aikataulut**-välilehteä kohdentaaksesi tehtäviä uudelle resurssille.</span><span class="sxs-lookup"><span data-stu-id="8adbc-116">On the **Project** page, on the **Schedule** tab, assign tasks to the new resource.</span></span> <span data-ttu-id="8adbc-117">Tehtäväruudukon **Resurssit**-kentästä käynnistettävä resurssinvalitsin näyttää ne ryhmän jäsenet, jotka voidaan valita.</span><span class="sxs-lookup"><span data-stu-id="8adbc-117">The resource picker that is launched from the **Resources** field in the task grid will show the team members that you can select.</span></span>


<span data-ttu-id="8adbc-118">Project Operationsissa resurssivaraukset ja tehtävän delegoinnit eivät ole tiukasti sidottuja.</span><span class="sxs-lookup"><span data-stu-id="8adbc-118">In Project Operations, resource bookings and task assignments aren't tightly coupled.</span></span> <span data-ttu-id="8adbc-119">Voit aikataulun resurssinvalitsinta käyttäessäsi kohdentaa ryhmän jäsenille tehtäviä, joiden tuntimäärä ylittää heidän varaustensa projektissa kattaman tuntimäärän.</span><span class="sxs-lookup"><span data-stu-id="8adbc-119">When you use the resource picker in the schedule, you can assign tasks to team members for more hours than their bookings cover on the project.</span></span>

<span data-ttu-id="8adbc-120">Ryhmän jäsenen varausten ja delgointien väliset erot näkyvät **Ryhmä**- ja **Resurssin täsmäytys** -välilehdissä.</span><span class="sxs-lookup"><span data-stu-id="8adbc-120">The differences between team member bookings and assignments are shown on the **Team** and **Resource Reconciliation** tabs.</span></span> <span data-ttu-id="8adbc-121">Voit myös täsmäyttää resurssien varausten ja delegointien väliset erot yksityiskohtaisella tasolla.</span><span class="sxs-lookup"><span data-stu-id="8adbc-121">You can also reconcile the differences between bookings and assignments for resources at a more detailed level.</span></span>

<span data-ttu-id="8adbc-122">Käytä **Aikataulut**-välilehden resurssinvalitsinta etsiäksesi ja valitaksesi varattavissa olevia resursseja, jotka eivät vielä kuulu projektiryhmään.</span><span class="sxs-lookup"><span data-stu-id="8adbc-122">Use the resource picker on the **Schedule** tab to search for and select bookable resources that are not already part of the project team.</span></span> <span data-ttu-id="8adbc-123">Nämä resurssit näkyvät resurssinvalitsimessa nimellä **Muut resurssit**.</span><span class="sxs-lookup"><span data-stu-id="8adbc-123">These resources are shown in the resource picker as **Other Resources**.</span></span>

<span data-ttu-id="8adbc-124">Kun teet valinnan, resurssi lisätään projektiryhmään ja se kohdennetaan tehtävällä, mutta varauksia ei luoda.</span><span class="sxs-lookup"><span data-stu-id="8adbc-124">When you make a selection, the resource is added to the project team and assigned to the task, but no bookings are generated.</span></span>

<span data-ttu-id="8adbc-125">Voit käyttää **Täsmäytys**-välilehden varauksenlaajennustoimintoa tai kohtaa **aikataulutaulukko** varataksesi resurssin kapasiteettia projektille.</span><span class="sxs-lookup"><span data-stu-id="8adbc-125">You can use the **Reconciliation** tab’s extend booking capability or the **Schedule Board** to book the resource’s capacity to the project.</span></span>

<span data-ttu-id="8adbc-126">Kun ryhmän jäsen on varattu projektillesi, voit käyttää niiden varausten hallitsemiseen **Ylläpidä varauksia** -toimintoa tai **aikataulutaulukkoa**.</span><span class="sxs-lookup"><span data-stu-id="8adbc-126">After a team member is booked on your project, you can use **Maintain bookings** or the **Schedule Board** directly to manage their bookings.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]