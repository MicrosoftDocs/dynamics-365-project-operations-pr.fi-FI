---
title: Projektikalenterien määrittäminen
description: Tässä aiheessa on tietoja siitä, miten kalenterimallia käytetään projektissa projektin aikataulun seuraamiseen.
author: ruhercul
manager: AnnBe
ms.date: 02/05/2021
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
ms.openlocfilehash: 1d5642d7a2246dc878b2bc4f504f138b71d29a69
ms.sourcegitcommit: c45ceda833b30ad39861f5bcd3ba1bbfff11fe7a
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/04/2021
ms.locfileid: "5981296"
---
# <a name="define-project-calendars"></a><span data-ttu-id="d7007-103">Projektikalenterien määrittäminen</span><span class="sxs-lookup"><span data-stu-id="d7007-103">Define project calendars</span></span>

<span data-ttu-id="d7007-104">_**Koskee:** Project Operationsin resurssiin / muuhun kuin resurssiin perustuvia skenaarioita, Lite-käyttöönotto-kaupasta proformalaskutukseen_</span><span class="sxs-lookup"><span data-stu-id="d7007-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="d7007-105">Projektia voi luoda ja hallita käyttämällä projektissa kalenterimallia.</span><span class="sxs-lookup"><span data-stu-id="d7007-105">To create and manage a project, you must apply a calendar template to the project.</span></span> <span data-ttu-id="d7007-106">Kalenterimalli määrittää seuraavat projektimääritteet:</span><span class="sxs-lookup"><span data-stu-id="d7007-106">The calendar template defines the following project attributes:</span></span>

- <span data-ttu-id="d7007-107">Työaika, mukaan lukien alkamis- ja päättymisaika</span><span class="sxs-lookup"><span data-stu-id="d7007-107">Working hours, including start and end time</span></span>
- <span data-ttu-id="d7007-108">Työpäivät</span><span class="sxs-lookup"><span data-stu-id="d7007-108">Working days</span></span>
- <span data-ttu-id="d7007-109">Kalenteripoikkeukset, kuten muut kuin työpäivät</span><span class="sxs-lookup"><span data-stu-id="d7007-109">Calendar exceptions such as non-working days</span></span>

<span data-ttu-id="d7007-110">Projektiin käytettävä kalenterimalli on kopio organisaation asetuksissa määritetystä kalenterimallista.</span><span class="sxs-lookup"><span data-stu-id="d7007-110">The calendar template that's applied to a project is a copy of the calendar template defined in your organization’s settings.</span></span>

> [!NOTE]
> <span data-ttu-id="d7007-111">Jos muutat kalenterimallia, muutokset eivät leviä projektin työaikaan.</span><span class="sxs-lookup"><span data-stu-id="d7007-111">If you change the calendar template, those changes don't propagate to the working hours of the project.</span></span> <span data-ttu-id="d7007-112">Jotta projektin työaikaa voidaan muuttaa, on otettava käyttöön uusi malli.</span><span class="sxs-lookup"><span data-stu-id="d7007-112">To change the working hours of the project, a new template must be applied.</span></span>

<span data-ttu-id="d7007-113">Organisaation kalenterimallin luomiselle on kaksi tärkeää avainvaatimusta:</span><span class="sxs-lookup"><span data-stu-id="d7007-113">To create a calendar template for your organization, there are two key requirements:</span></span>

- <span data-ttu-id="d7007-114">Määritä mallin haluttu työaika käyttämällä uutta tai aiemmin luotua varattavissa olevaa resurssia.</span><span class="sxs-lookup"><span data-stu-id="d7007-114">Define the desired working hours of the template using a new or existing bookable resource.</span></span>
- <span data-ttu-id="d7007-115">Luo uusi kalenterimalli ja liitä malli varattavaan resurssiin.</span><span class="sxs-lookup"><span data-stu-id="d7007-115">Create a new calendar template and associate the template with the bookable resource.</span></span>

<span data-ttu-id="d7007-116">**Määritä mallin työaika**</span><span class="sxs-lookup"><span data-stu-id="d7007-116">**Define the working hours of the template**</span></span>

1. <span data-ttu-id="d7007-117">Siirry kohtaan **Resurssit** \> **Resurssit**.</span><span class="sxs-lookup"><span data-stu-id="d7007-117">Go to **Resources** \> **Resources**.</span></span>
2. <span data-ttu-id="d7007-118">Luo uusi resurssi, jota haluat käyttää kalenterimallissa, tai valitse aiemmin luotu resurssi.</span><span class="sxs-lookup"><span data-stu-id="d7007-118">Create a new resource to reference in the calendar template, or select an existing resource.</span></span>
3. <span data-ttu-id="d7007-119">Valitse **resurssin työaika** -välilehti ja noudata ohjeita kohdasta [Resurssin työaikojen määrittäminen](https://docs.microsoft.com/dynamics365/field-service/set-work-hours-resource) kalenterisääntöjen määrittämiseksi.</span><span class="sxs-lookup"><span data-stu-id="d7007-119">Select the **Work Hours** tab of the resource and complete the instructions in [Set work hours for a resource](https://docs.microsoft.com/dynamics365/field-service/set-work-hours-resource) to configure the calendar rules.</span></span>

<span data-ttu-id="d7007-120">**Luo uusi kalenterimalli**</span><span class="sxs-lookup"><span data-stu-id="d7007-120">**Create a new calendar template**</span></span>

1. <span data-ttu-id="d7007-121">Valitse **Asetukset** \> **Kalenterimalli**.</span><span class="sxs-lookup"><span data-stu-id="d7007-121">Go to **Settings** \> **Calendar Template**.</span></span>
2. <span data-ttu-id="d7007-122">Valitse **Uusi** ja kirjoita nimi, kuvaus ja malliresurssi.</span><span class="sxs-lookup"><span data-stu-id="d7007-122">Select **New**, and enter a name, description, and template resource.</span></span>

> [!NOTE]
> <span data-ttu-id="d7007-123">Kun resurssiin viitataan kalenterimallissa, kalenterimalliin liitetään resurssin kalenterin kopio.</span><span class="sxs-lookup"><span data-stu-id="d7007-123">When a resource is referenced in a calendar template, a copy of the resource’s calendar is associated with the calendar template.</span></span> <span data-ttu-id="d7007-124">Jos kopioidun mallin työajat muuttuvat, nämä muutokset eivät levitä kalenterimalliin.</span><span class="sxs-lookup"><span data-stu-id="d7007-124">If the working hours of the copied template change, those changes will not propagate to the calendar template.</span></span>

<span data-ttu-id="d7007-125">Voit nyt liittää työmallin projektin kalenterimalliin.</span><span class="sxs-lookup"><span data-stu-id="d7007-125">You can now associate the work template with a project calendar template.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]

