---
title: Resurssienhallinta UKK
description: Tässä aiheessa on vastauksia usein kysyttyihin kysymyksiin resurssienhallinnasta.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/28/2019
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
ms.openlocfilehash: 395aa57d73e5d4a0c9c827c79bf4e7ef229c3981
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/16/2020
ms.locfileid: "4075559"
---
# <a name="resource-management-faq"></a><span data-ttu-id="ede8f-103">Resurssienhallinta UKK</span><span class="sxs-lookup"><span data-stu-id="ede8f-103">Resource management FAQ</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

## <a name="what-is-the-difference-between-a-team-member-and-a-resource-requirement"></a><span data-ttu-id="ede8f-104">Mitä eroa on ryhmän jäsenellä ja resurssitarpeella?</span><span class="sxs-lookup"><span data-stu-id="ede8f-104">What is the difference between a team member and a resource requirement?</span></span>

<span data-ttu-id="ede8f-105">Projektiryhmän jäsen voidaan kohdentaa tehtäviin, varata tai ylivarata ja määrittää hyväksyjäksi.</span><span class="sxs-lookup"><span data-stu-id="ede8f-105">A project team member can be assigned to tasks, booked or overbooked, and set as an approver.</span></span> <span data-ttu-id="ede8f-106">Resurssivaatimus voi olla olemassa ilman projektiryhmän jäsentä alustavana kysyntähuomautuksena.</span><span class="sxs-lookup"><span data-stu-id="ede8f-106">A resource requirement can exist without a project team member, as a draft note of demand.</span></span> 

## <a name="what-is-the-difference-between-proposed-and-soft-booked-hours"></a><span data-ttu-id="ede8f-107">Mitä eroa on ehdotetuilla ja alustavasti varatuilla tunneilla?</span><span class="sxs-lookup"><span data-stu-id="ede8f-107">What is the difference between proposed and soft-booked hours?</span></span>

<span data-ttu-id="ede8f-108">Ehdotetut tunnit ja alustavasti varatut tunnit eroavat näkyvyydessä.</span><span class="sxs-lookup"><span data-stu-id="ede8f-108">Proposed hours and soft-booked hours differ in visibility.</span></span> <span data-ttu-id="ede8f-109">Ehdotetut tunnit näkyvät vain resurssi -ja projektipäällikköille, jotka ovat luoneen kysynnän resurssipyynnön avulla.</span><span class="sxs-lookup"><span data-stu-id="ede8f-109">Proposed hours are visible only to resource managers and the project manager who initiated the demand by using a resource request.</span></span> <span data-ttu-id="ede8f-110">Alustavasti varatut tunnit näkyvät kaikille, joilla on pääsy aikataulutaulukkoon.</span><span class="sxs-lookup"><span data-stu-id="ede8f-110">Soft-booked hours are visible to anyone who has access to the Schedule Board.</span></span>

## <a name="how-can-i-see-the-soft-booked-hours-for-resources-on-a-team"></a><span data-ttu-id="ede8f-111">Miten voin nähdä ryhmän resurssien alustavasti varatut tunnit?</span><span class="sxs-lookup"><span data-stu-id="ede8f-111">How can I see the soft-booked hours for resources on a team?</span></span>

<span data-ttu-id="ede8f-112">Alustavia varauksia voidaan tehdä resurssitarvetta varattaessa.</span><span class="sxs-lookup"><span data-stu-id="ede8f-112">Soft bookings can made when you book a resource requirement.</span></span> <span data-ttu-id="ede8f-113">Resurssit, jotka on alustavasti varattu projektiryhmään, näkyvät ryhmän jäseninä, joilla on alustavasti varattuja tunteja.</span><span class="sxs-lookup"><span data-stu-id="ede8f-113">Resources that are soft-booked on a project team appear as team members who have soft-booked hours.</span></span> <span data-ttu-id="ede8f-114">Ne näkyvät myös aikataulutaulukossa.</span><span class="sxs-lookup"><span data-stu-id="ede8f-114">They also appear on the Schedule Board.</span></span>

## <a name="how-do-i-change-the-required-hours-and-the-start-and-end-dates-for-a-resource-generic-or-named-that-i-booked"></a><span data-ttu-id="ede8f-115">Kuinka voin muuttaa vaaditut tunnit ja aloitus- ja lopetuspäivämäärät resurssille (yleiselle tai nimetylle), jonka varasin?</span><span class="sxs-lookup"><span data-stu-id="ede8f-115">How do I change the required hours, and the start and end dates, for a resource (generic or named) that I booked?</span></span>

<span data-ttu-id="ede8f-116">Kun resurssit on varattu, valitse **Ylläpidä varauksia** tehdäksesi tarvittavat muutokset.</span><span class="sxs-lookup"><span data-stu-id="ede8f-116">After resources are booked, select **Maintain Bookings** to make any changes that are required.</span></span>

## <a name="what-resources-types-does-project-service-automation-support"></a><span data-ttu-id="ede8f-117">Mitä resurssityyppejä Project Service Automation tukee?</span><span class="sxs-lookup"><span data-stu-id="ede8f-117">What resources types does Project Service Automation support?</span></span>

<span data-ttu-id="ede8f-118">**Käyttäjä** ja **Yhteyshenkilö** ovat ainoita resurssityyppejä, joita tuetaan ohjelmassa Dynamics 365 Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="ede8f-118">**User** and **Contact** are the only resource types that are supported in Dynamics 365 Project Service Automation.</span></span> <span data-ttu-id="ede8f-119">Vaikka onkin mahdollista luoda muuntyyppisiä resursseja (esimerkiksi **Välineitä** ja **Ryhmiä** ), niitä varten ei tueta mitään päästä päähän -käyttötapauksia.</span><span class="sxs-lookup"><span data-stu-id="ede8f-119">Although you can create other types of resources (for example, **Equipment** and **Group** ), no end-to-end use case is supported for them.</span></span>

## <a name="what-is-the-difference-between-an-assignment-and-a-booking"></a><span data-ttu-id="ede8f-120">Mitä eroa on kohdennuksella ja varauksella?</span><span class="sxs-lookup"><span data-stu-id="ede8f-120">What is the difference between an assignment and a booking?</span></span>

<span data-ttu-id="ede8f-121">Kohdennukset ovat resurssien kohdennuksia projektitehtäviin projektiaikataulussa.</span><span class="sxs-lookup"><span data-stu-id="ede8f-121">Assignments are the assignment of resources to project tasks in the project schedule.</span></span> <span data-ttu-id="ede8f-122">Resurssit voivat olla joko todellisia tai yleisiä resursseja.</span><span class="sxs-lookup"><span data-stu-id="ede8f-122">The resources can be either real or generic resources.</span></span> <span data-ttu-id="ede8f-123">Varaukset ovat resurssien sitovia tai alustavia jakoja projekteihin.</span><span class="sxs-lookup"><span data-stu-id="ede8f-123">Bookings are the hard or soft allocation of resources to a project.</span></span> <span data-ttu-id="ede8f-124">Sitovat varaukset kuluttavat resurssin kapasiteettia.</span><span class="sxs-lookup"><span data-stu-id="ede8f-124">Hard bookings consume a resource's capacity.</span></span> <span data-ttu-id="ede8f-125">Ihannetapauksessa todellisille resursseilla varausten ja kohdennusten tulisi olla ristiriidattomia, koska niissä ei ole eroja.</span><span class="sxs-lookup"><span data-stu-id="ede8f-125">Ideally, for real resources, the bookings and assignments should agree, because they don't differ.</span></span> <span data-ttu-id="ede8f-126">PSA ei kuitenkaan pakota tähän yhteensopivuuteen.</span><span class="sxs-lookup"><span data-stu-id="ede8f-126">However, PSA doesn't enforce this agreement.</span></span> <span data-ttu-id="ede8f-127">Täsmäytysnäkymä näyttää projektipäällikölle kohteet, joissa resurssin varaukset ja kohdennukset eivät täsmää.</span><span class="sxs-lookup"><span data-stu-id="ede8f-127">The Reconciliation view shows a project manager places where a resource's bookings and assignments don't agree.</span></span>
