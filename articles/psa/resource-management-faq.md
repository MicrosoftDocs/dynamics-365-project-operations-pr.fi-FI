---
title: Resurssienhallinta UKK
description: Tässä aiheessa on vastauksia usein kysyttyihin kysymyksiin resurssienhallinnasta.
author: ruhercul
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
ms.openlocfilehash: 25e069beaffc9081a5516449d55b5c9304c23b0f
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/10/2021
ms.locfileid: "6008757"
---
# <a name="resource-management-faq"></a><span data-ttu-id="4f192-103">Resurssienhallinta UKK</span><span class="sxs-lookup"><span data-stu-id="4f192-103">Resource management FAQ</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

## <a name="what-is-the-difference-between-a-team-member-and-a-resource-requirement"></a><span data-ttu-id="4f192-104">Mitä eroa on ryhmän jäsenellä ja resurssitarpeella?</span><span class="sxs-lookup"><span data-stu-id="4f192-104">What is the difference between a team member and a resource requirement?</span></span>

<span data-ttu-id="4f192-105">Projektiryhmän jäsen voidaan kohdentaa tehtäviin, varata tai ylivarata ja määrittää hyväksyjäksi.</span><span class="sxs-lookup"><span data-stu-id="4f192-105">A project team member can be assigned to tasks, booked or overbooked, and set as an approver.</span></span> <span data-ttu-id="4f192-106">Resurssivaatimus voi olla olemassa ilman projektiryhmän jäsentä alustavana kysyntähuomautuksena.</span><span class="sxs-lookup"><span data-stu-id="4f192-106">A resource requirement can exist without a project team member, as a draft note of demand.</span></span> 

## <a name="what-is-the-difference-between-proposed-and-soft-booked-hours"></a><span data-ttu-id="4f192-107">Mitä eroa on ehdotetuilla ja alustavasti varatuilla tunneilla?</span><span class="sxs-lookup"><span data-stu-id="4f192-107">What is the difference between proposed and soft-booked hours?</span></span>

<span data-ttu-id="4f192-108">Ehdotetut tunnit ja alustavasti varatut tunnit eroavat näkyvyydessä.</span><span class="sxs-lookup"><span data-stu-id="4f192-108">Proposed hours and soft-booked hours differ in visibility.</span></span> <span data-ttu-id="4f192-109">Ehdotetut tunnit näkyvät vain resurssi -ja projektipäällikköille, jotka ovat luoneen kysynnän resurssipyynnön avulla.</span><span class="sxs-lookup"><span data-stu-id="4f192-109">Proposed hours are visible only to resource managers and the project manager who initiated the demand by using a resource request.</span></span> <span data-ttu-id="4f192-110">Alustavasti varatut tunnit näkyvät kaikille, joilla on pääsy aikataulutaulukkoon.</span><span class="sxs-lookup"><span data-stu-id="4f192-110">Soft-booked hours are visible to anyone who has access to the Schedule Board.</span></span>

## <a name="how-can-i-see-the-soft-booked-hours-for-resources-on-a-team"></a><span data-ttu-id="4f192-111">Miten voin nähdä ryhmän resurssien alustavasti varatut tunnit?</span><span class="sxs-lookup"><span data-stu-id="4f192-111">How can I see the soft-booked hours for resources on a team?</span></span>

<span data-ttu-id="4f192-112">Alustavia varauksia voidaan tehdä resurssitarvetta varattaessa.</span><span class="sxs-lookup"><span data-stu-id="4f192-112">Soft bookings can made when you book a resource requirement.</span></span> <span data-ttu-id="4f192-113">Resurssit, jotka on alustavasti varattu projektiryhmään, näkyvät ryhmän jäseninä, joilla on alustavasti varattuja tunteja.</span><span class="sxs-lookup"><span data-stu-id="4f192-113">Resources that are soft-booked on a project team appear as team members who have soft-booked hours.</span></span> <span data-ttu-id="4f192-114">Ne näkyvät myös aikataulutaulukossa.</span><span class="sxs-lookup"><span data-stu-id="4f192-114">They also appear on the Schedule Board.</span></span>

## <a name="how-do-i-change-the-required-hours-and-the-start-and-end-dates-for-a-resource-generic-or-named-that-i-booked"></a><span data-ttu-id="4f192-115">Kuinka voin muuttaa vaaditut tunnit ja aloitus- ja lopetuspäivämäärät resurssille (yleiselle tai nimetylle), jonka varasin?</span><span class="sxs-lookup"><span data-stu-id="4f192-115">How do I change the required hours, and the start and end dates, for a resource (generic or named) that I booked?</span></span>

<span data-ttu-id="4f192-116">Kun resurssit on varattu, valitse **Ylläpidä varauksia** tehdäksesi tarvittavat muutokset.</span><span class="sxs-lookup"><span data-stu-id="4f192-116">After resources are booked, select **Maintain Bookings** to make any changes that are required.</span></span>

## <a name="what-resources-types-does-project-service-automation-support"></a><span data-ttu-id="4f192-117">Mitä resurssityyppejä Project Service Automation tukee?</span><span class="sxs-lookup"><span data-stu-id="4f192-117">What resources types does Project Service Automation support?</span></span>

<span data-ttu-id="4f192-118">**Käyttäjä** ja **Yhteyshenkilö** ovat ainoita resurssityyppejä, joita tuetaan ohjelmassa Dynamics 365 Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="4f192-118">**User** and **Contact** are the only resource types that are supported in Dynamics 365 Project Service Automation.</span></span> <span data-ttu-id="4f192-119">Vaikka onkin mahdollista luoda muuntyyppisiä resursseja (esimerkiksi **Välineitä** ja **Ryhmiä**), niitä varten ei tueta mitään päästä päähän -käyttötapauksia.</span><span class="sxs-lookup"><span data-stu-id="4f192-119">Although you can create other types of resources (for example, **Equipment** and **Group**), no end-to-end use case is supported for them.</span></span>

## <a name="what-is-the-difference-between-an-assignment-and-a-booking"></a><span data-ttu-id="4f192-120">Mitä eroa on kohdennuksella ja varauksella?</span><span class="sxs-lookup"><span data-stu-id="4f192-120">What is the difference between an assignment and a booking?</span></span>

<span data-ttu-id="4f192-121">Kohdennukset ovat resurssien kohdennuksia projektitehtäviin projektiaikataulussa.</span><span class="sxs-lookup"><span data-stu-id="4f192-121">Assignments are the assignment of resources to project tasks in the project schedule.</span></span> <span data-ttu-id="4f192-122">Resurssit voivat olla joko todellisia tai yleisiä resursseja.</span><span class="sxs-lookup"><span data-stu-id="4f192-122">The resources can be either real or generic resources.</span></span> <span data-ttu-id="4f192-123">Varaukset ovat resurssien sitovia tai alustavia jakoja projekteihin.</span><span class="sxs-lookup"><span data-stu-id="4f192-123">Bookings are the hard or soft allocation of resources to a project.</span></span> <span data-ttu-id="4f192-124">Sitovat varaukset kuluttavat resurssin kapasiteettia.</span><span class="sxs-lookup"><span data-stu-id="4f192-124">Hard bookings consume a resource's capacity.</span></span> <span data-ttu-id="4f192-125">Ihannetapauksessa todellisille resursseilla varausten ja kohdennusten tulisi olla ristiriidattomia, koska niissä ei ole eroja.</span><span class="sxs-lookup"><span data-stu-id="4f192-125">Ideally, for real resources, the bookings and assignments should agree, because they don't differ.</span></span> <span data-ttu-id="4f192-126">PSA ei kuitenkaan pakota tähän yhteensopivuuteen.</span><span class="sxs-lookup"><span data-stu-id="4f192-126">However, PSA doesn't enforce this agreement.</span></span> <span data-ttu-id="4f192-127">Täsmäytysnäkymä näyttää projektipäällikölle kohteet, joissa resurssin varaukset ja kohdennukset eivät täsmää.</span><span class="sxs-lookup"><span data-stu-id="4f192-127">The Reconciliation view shows a project manager places where a resource's bookings and assignments don't agree.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]