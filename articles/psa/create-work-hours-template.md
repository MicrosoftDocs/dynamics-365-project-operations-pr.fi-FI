---
title: Työtuntimallien luominen
description: Ohjeita työtuntimallin luomisesta Project Servicessä.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
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
ms.openlocfilehash: 525f601ad6fee902cb6d5c128b596cc2d33f30c4
ms.sourcegitcommit: c45ceda833b30ad39861f5bcd3ba1bbfff11fe7a
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/04/2021
ms.locfileid: "5981251"
---
# <a name="create-a-work-hours-template-project-service"></a><span data-ttu-id="063ad-103">Luo työtuntimalli (Project Service)</span><span class="sxs-lookup"><span data-stu-id="063ad-103">Create a work hours template (Project Service)</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="063ad-104">Projektia voi luoda ja hallita käyttämällä projektissa kalenterimallia.</span><span class="sxs-lookup"><span data-stu-id="063ad-104">To create and manage a project, you must apply a calendar template to the project.</span></span> <span data-ttu-id="063ad-105">Kalenterimalli määrittää seuraavat projektimääritteet:</span><span class="sxs-lookup"><span data-stu-id="063ad-105">The calendar template defines the following project attributes:</span></span>

- <span data-ttu-id="063ad-106">Työaika, mukaan lukien alkamis- ja päättymisaika</span><span class="sxs-lookup"><span data-stu-id="063ad-106">Working hours, including start and end time</span></span>
- <span data-ttu-id="063ad-107">Työpäivät</span><span class="sxs-lookup"><span data-stu-id="063ad-107">Working days</span></span>
- <span data-ttu-id="063ad-108">Kalenteripoikkeukset, kuten muut kuin työpäivät</span><span class="sxs-lookup"><span data-stu-id="063ad-108">Calendar exceptions such as non-working days</span></span>

<span data-ttu-id="063ad-109">Projektiin käytettävä kalenterimalli on kopio organisaation asetuksissa määritetystä kalenterimallista.</span><span class="sxs-lookup"><span data-stu-id="063ad-109">The calendar template that's applied to a project is a copy of the calendar template defined in your organization’s settings.</span></span>

> [!NOTE]
> <span data-ttu-id="063ad-110">Jos muutat kalenterimallia, muutokset eivät leviä projektin työaikaan.</span><span class="sxs-lookup"><span data-stu-id="063ad-110">If you change the calendar template, those changes don't propagate to the working hours of the project.</span></span> <span data-ttu-id="063ad-111">Jotta projektin työaikaa voidaan muuttaa, on otettava käyttöön uusi malli.</span><span class="sxs-lookup"><span data-stu-id="063ad-111">To change the working hours of the project, a new template must be applied.</span></span>

<span data-ttu-id="063ad-112">Organisaation kalenterimallin luomiselle on kaksi tärkeää avainvaatimusta:</span><span class="sxs-lookup"><span data-stu-id="063ad-112">To create a calendar template for your organization, there are two key requirements:</span></span>

- <span data-ttu-id="063ad-113">Määritä mallin haluttu työaika käyttämällä uutta tai aiemmin luotua varattavissa olevaa resurssia.</span><span class="sxs-lookup"><span data-stu-id="063ad-113">Define the desired working hours of the template using a new or existing bookable resource.</span></span>
- <span data-ttu-id="063ad-114">Luo uusi kalenterimalli ja liitä malli varattavaan resurssiin.</span><span class="sxs-lookup"><span data-stu-id="063ad-114">Create a new calendar template and associate the template with the bookable resource.</span></span>

<span data-ttu-id="063ad-115">**Määritä mallin työaika**</span><span class="sxs-lookup"><span data-stu-id="063ad-115">**Define the working hours of the template**</span></span>

1. <span data-ttu-id="063ad-116">Siirry kohtaan **Resurssit** \> **Resurssit**.</span><span class="sxs-lookup"><span data-stu-id="063ad-116">Go to **Resources** \> **Resources**.</span></span>
2. <span data-ttu-id="063ad-117">Luo uusi resurssi, jota haluat käyttää kalenterimallissa, tai valitse aiemmin luotu resurssi.</span><span class="sxs-lookup"><span data-stu-id="063ad-117">Create a new resource to reference in the calendar template, or select an existing resource.</span></span>
3. <span data-ttu-id="063ad-118">Valitse **resurssin työaika** -välilehti ja noudata ohjeita kohdasta [Resurssin työaikojen määrittäminen](https://docs.microsoft.com/dynamics365/field-service/set-work-hours-resource) kalenterisääntöjen määrittämiseksi.</span><span class="sxs-lookup"><span data-stu-id="063ad-118">Select the **Work Hours** tab of the resource and complete the instructions in [Set work hours for a resource](https://docs.microsoft.com/dynamics365/field-service/set-work-hours-resource) to configure the calendar rules.</span></span>

<span data-ttu-id="063ad-119">**Luo uusi kalenterimalli**</span><span class="sxs-lookup"><span data-stu-id="063ad-119">**Create a new calendar template**</span></span>

1. <span data-ttu-id="063ad-120">Valitse **Asetukset** \> **Kalenterimalli**.</span><span class="sxs-lookup"><span data-stu-id="063ad-120">Go to **Settings** \> **Calendar Template**.</span></span>
2. <span data-ttu-id="063ad-121">Valitse **Uusi** ja kirjoita nimi, kuvaus ja malliresurssi.</span><span class="sxs-lookup"><span data-stu-id="063ad-121">Select **New**, and enter a name, description, and template resource.</span></span>


> [!NOTE]
> <span data-ttu-id="063ad-122">Kun resurssiin viitataan kalenterimallissa, kalenterimalliin liitetään resurssin kalenterin kopio.</span><span class="sxs-lookup"><span data-stu-id="063ad-122">When a resource is referenced in a calendar template, a copy of the resource’s calendar is associated with the calendar template.</span></span> <span data-ttu-id="063ad-123">Jos kopioidun mallin työajat muuttuvat, nämä muutokset eivät levitä kalenterimalliin.</span><span class="sxs-lookup"><span data-stu-id="063ad-123">If the working hours of the copied template change, those changes will not propagate to the calendar template.</span></span>


### <a name="see-also"></a><span data-ttu-id="063ad-124">Katso myös</span><span class="sxs-lookup"><span data-stu-id="063ad-124">See Also</span></span>  
 [<span data-ttu-id="063ad-125">Resurssien määrittäminen</span><span class="sxs-lookup"><span data-stu-id="063ad-125">Set up resources</span></span>](../psa/set-up-resources.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
