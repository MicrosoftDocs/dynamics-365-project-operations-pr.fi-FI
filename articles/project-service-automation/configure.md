---
title: Project Service Automationin määrittäminen
description: Ohjeet Project Servicen määrittämiseen
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: 56ba0b8d-808c-48d6-965f-abd74b49c2b4
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 52be4705e6ef983dcf421df5d1bfb5c6de8e9a30
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/24/2020
ms.locfileid: "3751158"
---
# <a name="configure-project-service"></a><span data-ttu-id="fcff7-103">Määritä Project Service</span><span class="sxs-lookup"><span data-stu-id="fcff7-103">Configure Project Service</span></span>

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="fcff7-104">Ennen kuin voit käyttää [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] -ratkaisun [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] -automatisointitoimintoja asiakkuuksien, projektien ja resurssien hallintaan, sinun on suoritettava muutamia määritysvaiheita ja varmistettava että [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] -ratkaisu vastaa yrityksesi tarpeita.</span><span class="sxs-lookup"><span data-stu-id="fcff7-104">Before you can use the [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] automation capabilities in [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] to manage your accounts, projects, and resources, you need to complete a few configuration steps to ensure the [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] solution matches your organization’s needs.</span></span> <span data-ttu-id="fcff7-105">Näihin vaiheisiin kuuluu:</span><span class="sxs-lookup"><span data-stu-id="fcff7-105">These steps include:</span></span>  
  
-   <span data-ttu-id="fcff7-106">[Määritä aikayksiköt](../project-service/set-up-time-units.md).</span><span class="sxs-lookup"><span data-stu-id="fcff7-106">[Set up time units](../project-service/set-up-time-units.md).</span></span> <span data-ttu-id="fcff7-107">Määritä aikayksiköt tuoteluetteloon, jota aiot käyttää projektien aikataulutuksen ja laskutuksen pohjana.</span><span class="sxs-lookup"><span data-stu-id="fcff7-107">Configure the time units in the product catalog that you’ll use as a base for scheduling and billing your projects.</span></span>  
  
-   <span data-ttu-id="fcff7-108">[Määritä valuutat ja vaihtokurssit](../project-service/set-up-currencies-exchange-rates.md).</span><span class="sxs-lookup"><span data-stu-id="fcff7-108">[Set up currencies and exchange rates](../project-service/set-up-currencies-exchange-rates.md).</span></span> <span data-ttu-id="fcff7-109">Määritä projekteissa käytettävät valuutat.</span><span class="sxs-lookup"><span data-stu-id="fcff7-109">Set up the currencies to use for your projects.</span></span>  
  
-   <span data-ttu-id="fcff7-110">[Luo organisaatioyksiköt](../project-service/create-organizational-units.md).</span><span class="sxs-lookup"><span data-stu-id="fcff7-110">[Create organizational units](../project-service/create-organizational-units.md).</span></span> <span data-ttu-id="fcff7-111">Määritä ryhmät, joiden avulla yritys jakaa liiketoimintansa joko maantieteellisesti,  liiketoimintaominaisuuksien tai muun loogisen jaon mukaan.</span><span class="sxs-lookup"><span data-stu-id="fcff7-111">Set up the groups that your company uses to divide its business, whether by geography, business function, or other logical division.</span></span>  
  
-   <span data-ttu-id="fcff7-112">[Määritä laskutustiheydet](../project-service/set-up-invoice-frequencies.md).</span><span class="sxs-lookup"><span data-stu-id="fcff7-112">[Set up invoice frequencies](../project-service/set-up-invoice-frequencies.md).</span></span> <span data-ttu-id="fcff7-113">Määritä aikajaksot, joita haluat käyttää asiakkaiden laskutuksessa.</span><span class="sxs-lookup"><span data-stu-id="fcff7-113">Set up time periods that you want to use for billing your clients.</span></span>  
  
-   <span data-ttu-id="fcff7-114">[Määritä tapahtumaluokat](../project-service/configure-transaction-categories.md).</span><span class="sxs-lookup"><span data-stu-id="fcff7-114">[Configure transaction categories](../project-service/configure-transaction-categories.md).</span></span> <span data-ttu-id="fcff7-115">Määritä tapahtumaluokat, joissa konsultit voivat periä laskutettavia ja muita kuin laskutettavia kuluja.</span><span class="sxs-lookup"><span data-stu-id="fcff7-115">Set up transaction categories your consultants can charge their billable and unbillable expenses to.</span></span>  
  
-   <span data-ttu-id="fcff7-116">[Määritä kululuokat](../project-service/configure-expense-categories.md).</span><span class="sxs-lookup"><span data-stu-id="fcff7-116">[Configure expense categories](../project-service/configure-expense-categories.md).</span></span> <span data-ttu-id="fcff7-117">Määritä luokat, joissa konsultit voivat periä laskutettavia ja muita kuin laskutettavia kuluja.</span><span class="sxs-lookup"><span data-stu-id="fcff7-117">Set up the categories your consultants can charge their billable and unbillable expenses to.</span></span>  
  
-   <span data-ttu-id="fcff7-118">[Tuoteluettelon nimikkeiden luominen](../project-service/create-product-catalog-items.md).</span><span class="sxs-lookup"><span data-stu-id="fcff7-118">[Create product catalog items](../project-service/create-product-catalog-items.md).</span></span> <span data-ttu-id="fcff7-119">Lisää tuoteluetteloon myytäviä tuotteita, kuten ohjelmiston käyttöoikeudet.</span><span class="sxs-lookup"><span data-stu-id="fcff7-119">Add the products you sell, such as software licenses, to the product catalog.</span></span>  
  
-   <span data-ttu-id="fcff7-120">[Hinnaston luominen](../project-service/create-price-list.md).</span><span class="sxs-lookup"><span data-stu-id="fcff7-120">[Create a price list](../project-service/create-price-list.md).</span></span> <span data-ttu-id="fcff7-121">Määritä erilliset hinnastot sen mukaan, kuinka paljon veloitat asiakkaalta jokaisesta projektin edellyttämästä roolista.</span><span class="sxs-lookup"><span data-stu-id="fcff7-121">Configure different price lists, depending on how much you want to charge your clients for each role their project requires.</span></span>  
  
-   <span data-ttu-id="fcff7-122">[Resurssien määrittäminen](../project-service/set-up-resources.md).</span><span class="sxs-lookup"><span data-stu-id="fcff7-122">[Set up resources](../project-service/set-up-resources.md).</span></span> <span data-ttu-id="fcff7-123">Lisää taitoja, pätevyyksiä, resurssin rooleja ja muita resurssitietoja, joita tarvitset projekteissa.</span><span class="sxs-lookup"><span data-stu-id="fcff7-123">Add the skills, proficiencies, resource roles, and other resource information that you’ll need for your projects.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="fcff7-124">Katso myös</span><span class="sxs-lookup"><span data-stu-id="fcff7-124">See Also</span></span>  
 <span data-ttu-id="fcff7-125">[Project Service Automationin yleiskatsaus](../project-service/overview.md) </span><span class="sxs-lookup"><span data-stu-id="fcff7-125">[Overview of Project Service Automation](../project-service/overview.md) </span></span>  
 <span data-ttu-id="fcff7-126">[Project Service Automationin määrittäminen](../project-service/configure.md) </span><span class="sxs-lookup"><span data-stu-id="fcff7-126">[Configure Project Service Automation](../project-service/configure.md) </span></span>  
 <span data-ttu-id="fcff7-127">[Asiakaspäällikön opas](../project-service/account-manager-guide.md) </span><span class="sxs-lookup"><span data-stu-id="fcff7-127">[Account Manager Guide](../project-service/account-manager-guide.md) </span></span>  
 <span data-ttu-id="fcff7-128">[Projektipäällikön opas](../project-service/project-manager-guide.md) </span><span class="sxs-lookup"><span data-stu-id="fcff7-128">[Project Manager Guide](../project-service/project-manager-guide.md) </span></span>  
 <span data-ttu-id="fcff7-129">[Resurssipäällikön opas](../project-service/resource-manager-guide.md) </span><span class="sxs-lookup"><span data-stu-id="fcff7-129">[Resource Manager Guide](../project-service/resource-manager-guide.md) </span></span>  
 [<span data-ttu-id="fcff7-130">Aika-, kulu- ja yhteistyöopas</span><span class="sxs-lookup"><span data-stu-id="fcff7-130">Time, Expense, and Collaboration Guid</span></span>](../project-service/time-expense-collaboration-guide.md)
