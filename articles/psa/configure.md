---
title: Project Service Automationin määrittäminen
description: Ohjeet Project Servicen määrittämiseen
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
ms.openlocfilehash: 8a219ef0166565a550a7836ffeae37ffd514a001
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/28/2020
ms.locfileid: "4129179"
---
# <a name="configure-project-service"></a><span data-ttu-id="2e233-103">Määritä Project Service</span><span class="sxs-lookup"><span data-stu-id="2e233-103">Configure Project Service</span></span>

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="2e233-104">Ennen kuin voit käyttää [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] -ratkaisun [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] -automatisointitoimintoja asiakkuuksien, projektien ja resurssien hallintaan, sinun on suoritettava muutamia määritysvaiheita ja varmistettava että [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] -ratkaisu vastaa yrityksesi tarpeita.</span><span class="sxs-lookup"><span data-stu-id="2e233-104">Before you can use the [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] automation capabilities in [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] to manage your accounts, projects, and resources, you need to complete a few configuration steps to ensure the [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] solution matches your organization’s needs.</span></span> <span data-ttu-id="2e233-105">Näihin vaiheisiin kuuluu:</span><span class="sxs-lookup"><span data-stu-id="2e233-105">These steps include:</span></span>  
  
-   <span data-ttu-id="2e233-106">[Määritä aikayksiköt](../psa/set-up-time-units.md).</span><span class="sxs-lookup"><span data-stu-id="2e233-106">[Set up time units](../psa/set-up-time-units.md).</span></span> <span data-ttu-id="2e233-107">Määritä aikayksiköt tuoteluetteloon, jota aiot käyttää projektien aikataulutuksen ja laskutuksen pohjana.</span><span class="sxs-lookup"><span data-stu-id="2e233-107">Configure the time units in the product catalog that you’ll use as a base for scheduling and billing your projects.</span></span>  
  
-   <span data-ttu-id="2e233-108">[Määritä valuutat ja vaihtokurssit](../psa/set-up-currencies-exchange-rates.md).</span><span class="sxs-lookup"><span data-stu-id="2e233-108">[Set up currencies and exchange rates](../psa/set-up-currencies-exchange-rates.md).</span></span> <span data-ttu-id="2e233-109">Määritä projekteissa käytettävät valuutat.</span><span class="sxs-lookup"><span data-stu-id="2e233-109">Set up the currencies to use for your projects.</span></span>  
  
-   <span data-ttu-id="2e233-110">[Luo organisaatioyksiköt](../psa/create-organizational-units.md).</span><span class="sxs-lookup"><span data-stu-id="2e233-110">[Create organizational units](../psa/create-organizational-units.md).</span></span> <span data-ttu-id="2e233-111">Määritä ryhmät, joiden avulla yritys jakaa liiketoimintansa joko maantieteellisesti,  liiketoimintaominaisuuksien tai muun loogisen jaon mukaan.</span><span class="sxs-lookup"><span data-stu-id="2e233-111">Set up the groups that your company uses to divide its business, whether by geography, business function, or other logical division.</span></span>  
  
-   <span data-ttu-id="2e233-112">[Määritä laskutustiheydet](../psa/set-up-invoice-frequencies.md).</span><span class="sxs-lookup"><span data-stu-id="2e233-112">[Set up invoice frequencies](../psa/set-up-invoice-frequencies.md).</span></span> <span data-ttu-id="2e233-113">Määritä aikajaksot, joita haluat käyttää asiakkaiden laskutuksessa.</span><span class="sxs-lookup"><span data-stu-id="2e233-113">Set up time periods that you want to use for billing your clients.</span></span>  
  
-   <span data-ttu-id="2e233-114">[Määritä tapahtumaluokat](../psa/configure-transaction-categories.md).</span><span class="sxs-lookup"><span data-stu-id="2e233-114">[Configure transaction categories](../psa/configure-transaction-categories.md).</span></span> <span data-ttu-id="2e233-115">Määritä tapahtumaluokat, joissa konsultit voivat periä laskutettavia ja muita kuin laskutettavia kuluja.</span><span class="sxs-lookup"><span data-stu-id="2e233-115">Set up transaction categories your consultants can charge their billable and unbillable expenses to.</span></span>  
  
-   <span data-ttu-id="2e233-116">[Määritä kululuokat](../psa/configure-expense-categories.md).</span><span class="sxs-lookup"><span data-stu-id="2e233-116">[Configure expense categories](../psa/configure-expense-categories.md).</span></span> <span data-ttu-id="2e233-117">Määritä luokat, joissa konsultit voivat periä laskutettavia ja muita kuin laskutettavia kuluja.</span><span class="sxs-lookup"><span data-stu-id="2e233-117">Set up the categories your consultants can charge their billable and unbillable expenses to.</span></span>  
  
-   <span data-ttu-id="2e233-118">[Tuoteluettelon nimikkeiden luominen](../psa/create-product-catalog-items.md).</span><span class="sxs-lookup"><span data-stu-id="2e233-118">[Create product catalog items](../psa/create-product-catalog-items.md).</span></span> <span data-ttu-id="2e233-119">Lisää tuoteluetteloon myytäviä tuotteita, kuten ohjelmiston käyttöoikeudet.</span><span class="sxs-lookup"><span data-stu-id="2e233-119">Add the products you sell, such as software licenses, to the product catalog.</span></span>  
  
-   <span data-ttu-id="2e233-120">[Hinnaston luominen](../psa/create-price-list.md).</span><span class="sxs-lookup"><span data-stu-id="2e233-120">[Create a price list](../psa/create-price-list.md).</span></span> <span data-ttu-id="2e233-121">Määritä erilliset hinnastot sen mukaan, kuinka paljon veloitat asiakkaalta jokaisesta projektin edellyttämästä roolista.</span><span class="sxs-lookup"><span data-stu-id="2e233-121">Configure different price lists, depending on how much you want to charge your clients for each role their project requires.</span></span>  
  
-   <span data-ttu-id="2e233-122">[Resurssien määrittäminen](../psa/set-up-resources.md).</span><span class="sxs-lookup"><span data-stu-id="2e233-122">[Set up resources](../psa/set-up-resources.md).</span></span> <span data-ttu-id="2e233-123">Lisää taitoja, pätevyyksiä, resurssin rooleja ja muita resurssitietoja, joita tarvitset projekteissa.</span><span class="sxs-lookup"><span data-stu-id="2e233-123">Add the skills, proficiencies, resource roles, and other resource information that you’ll need for your projects.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="2e233-124">Katso myös</span><span class="sxs-lookup"><span data-stu-id="2e233-124">See Also</span></span>  
 <span data-ttu-id="2e233-125">[Project Service Automationin yleiskatsaus](../psa/overview.md) </span><span class="sxs-lookup"><span data-stu-id="2e233-125">[Overview of Project Service Automation](../psa/overview.md) </span></span>  
 <span data-ttu-id="2e233-126">[Project Service Automationin määrittäminen](../psa/configure.md) </span><span class="sxs-lookup"><span data-stu-id="2e233-126">[Configure Project Service Automation](../psa/configure.md) </span></span>  
 <span data-ttu-id="2e233-127">[Asiakaspäällikön opas](../psa/account-manager-guide.md) </span><span class="sxs-lookup"><span data-stu-id="2e233-127">[Account Manager Guide](../psa/account-manager-guide.md) </span></span>  
 <span data-ttu-id="2e233-128">[Projektipäällikön opas](../psa/project-manager-guide.md) </span><span class="sxs-lookup"><span data-stu-id="2e233-128">[Project Manager Guide](../psa/project-manager-guide.md) </span></span>  
 <span data-ttu-id="2e233-129">[Resurssipäällikön opas](../psa/resource-manager-guide.md) </span><span class="sxs-lookup"><span data-stu-id="2e233-129">[Resource Manager Guide](../psa/resource-manager-guide.md) </span></span>  
 [<span data-ttu-id="2e233-130">Aika-, kulu- ja yhteistyöopas</span><span class="sxs-lookup"><span data-stu-id="2e233-130">Time, Expense, and Collaboration Guid</span></span>](../psa/time-expense-collaboration-guide.md)