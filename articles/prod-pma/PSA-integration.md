---
title: Project Service Automationin yleiskatsaus
description: Tässä aiheessa on tietoja Dynamics 365 Project Service Automationin Dynamics 365 Financeen integroinnin ratkaisusta.
author: ruhercul
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: ruhercul
ms.search.scope: Core, Operations
ms.custom: intro-internal
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: ruhercul
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1c756caec6cd7eda8f891446d3e8309aca3b2482
ms.sourcegitcommit: 0fafe022731f0e1e8693382ff906e3f8541d34ca
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 07/07/2021
ms.locfileid: "6369615"
---
# <a name="project-service-automation-overview"></a><span data-ttu-id="236ff-103">Project Service Automationin yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="236ff-103">Project Service Automation overview</span></span>

[!include[banner](../includes/banner.md)]
[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="236ff-104">Project Service Automationin integrointiratkaisua Financeen käyttää tietojen integrointitoimintoa tietojen synkronointiin Dynamics 365 Financen ja Dynamics 365 Project Service Automationin eri esiintymien välillä Common Data Servicen kautta.</span><span class="sxs-lookup"><span data-stu-id="236ff-104">The Project Service Automation to Finance integration solution uses the Data integration feature to synchronize data across instances of Dynamics 365 Finance and Dynamics 365 Project Service Automation via Common Data Service.</span></span> <span data-ttu-id="236ff-105">Tietojen integrointitoiminnossa käytettävissä olevat integrointimallit mahdollistaa projektien, projektisopimusten, projektisopimusten rivien, projektisopimusten rivien välitavoitteiden, projektitehtävien, kulutapahtumaluokkien, työaika-arvioiden ja kuluarvioiden vuon Project Service Automationista Financeen.</span><span class="sxs-lookup"><span data-stu-id="236ff-105">The integration templates that are available with the Data integration feature enable the flow of projects, project contracts, project contract lines, project contract line milestones, project tasks, expense transaction categories, hour estimates, and expense estimates from Project Service Automation to Finance.</span></span>

> [!NOTE]
> - <span data-ttu-id="236ff-106">Jos käytössäsi on versio 7.3.0, sinun täytyy asentaa tietokanta 4074835.</span><span class="sxs-lookup"><span data-stu-id="236ff-106">If you're using version 7.3.0, you must install KB 4074835.</span></span> <span data-ttu-id="236ff-107">Sen jälkeen voit integroida kiinteähintaisia projekteja.</span><span class="sxs-lookup"><span data-stu-id="236ff-107">You will then be able to integrate fixed price projects.</span></span>
> - <span data-ttu-id="236ff-108">Jos käytössäsi on versio 7.3.0 ja tuot maksutapahtumia Project Service Automationin kautta, sinun täytyy asentaa tietokanta 4345320, jotta voit lisätä kyseiset maksut projektilaskuun.</span><span class="sxs-lookup"><span data-stu-id="236ff-108">If you're using version 7.3.0, and you are bringing fee transactions over from Project Service Automation, you must install KB 4345320 in order to include those fees in the project invoice.</span></span>
> - <span data-ttu-id="236ff-109">Jos käytät versiota 8.0 voit käyttää projektitehtävien integrointia, kulutapahtumien luokkia, työaika-arvioita, kuluarvioita ja toimintojen lukitusta.</span><span class="sxs-lookup"><span data-stu-id="236ff-109">If you're using version 8.0, you will be able to use project task integration, expense transaction categories, hour estimates, expense estimates, and functionality locking.</span></span>
> - <span data-ttu-id="236ff-110">Jos käytössäsi on versio 8.0.1 tai uudempi, voit synkronoida toteutuneet.</span><span class="sxs-lookup"><span data-stu-id="236ff-110">If you're using version 8.0.1 or later, you will be able to synchronize actuals.</span></span>

<span data-ttu-id="236ff-111">Ennen kuin voit integroida Project Service Automation Financeen, sinun täytyy määrittää Project Service Automation -integroinnin parametrit.</span><span class="sxs-lookup"><span data-stu-id="236ff-111">Before you can integrate Project Service Automation Finance, you must configure the Project Service Automation integration parameters.</span></span> <span data-ttu-id="236ff-112">Lisätietoja [Project Service Automation -integroinnin parametrit](PSA-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="236ff-112">For more information, see [Project Service Automation integration parameters](PSA-parameters.md).</span></span>

<span data-ttu-id="236ff-113">Tämä integrointiratkaisu mahdollistaa suoran synkronoinnin seuraavissa tilanteissa:</span><span class="sxs-lookup"><span data-stu-id="236ff-113">This integration solution enables direct synchronization in the following scenarios:</span></span>

- <span data-ttu-id="236ff-114">Projektisopimusten ylläpitäminen Project Service Automationissa ja suora synkronointi Project Service Autiomationista Financeen.</span><span class="sxs-lookup"><span data-stu-id="236ff-114">Maintain project contracts in Project Service Automation, and synchronize them directly from Project Service Automation to Finance.</span></span>
- <span data-ttu-id="236ff-115">Projektien luominen Project Service Automationissa ja suora synkronointi Project Service Autiomationista Financeen.</span><span class="sxs-lookup"><span data-stu-id="236ff-115">Create projects in Project Service Automation, and synchronize them directly from Project Service Automation to Finance.</span></span>
- <span data-ttu-id="236ff-116">Projektisopimusten rivien ylläpitäminen Project Service Automationissa ja suora synkronointi Project Service Autiomationista Financeen.</span><span class="sxs-lookup"><span data-stu-id="236ff-116">Maintain project contract lines in Project Service Automation, and synchronize them directly from Project Service Automation to Finance.</span></span>
- <span data-ttu-id="236ff-117">Projektisopimusten rivien välitavoitteiden ylläpitäminen Project Service Automationissa ja suora synkronointi Project Service Autiomationista Financeen.</span><span class="sxs-lookup"><span data-stu-id="236ff-117">Maintain project contract line milestones in Project Service Automation, and synchronize them directly from Project Service Automation to Finance.</span></span>
- <span data-ttu-id="236ff-118">Projektitehtävien ylläpitäminen Project Service Automationissa ja suora synkronointi Project Service Autiomationista Financeen.</span><span class="sxs-lookup"><span data-stu-id="236ff-118">Maintain project tasks in Project Service Automation, and synchronize them directly from Project Service Automation to Finance.</span></span>
- <span data-ttu-id="236ff-119">Kulutapahtumaluokkien ylläpitäminen Financesta ja suora synkronointi Financesta Project Service Autiomationiin.</span><span class="sxs-lookup"><span data-stu-id="236ff-119">Maintain expense transaction categories in Finance, and synchronize them directly from Finance to Project Service Automation.</span></span>
- <span data-ttu-id="236ff-120">Projektien työaikaennusteiden luominen Project Service Automationissa ja suora synkronointi Project Service Autiomationista Financeen.</span><span class="sxs-lookup"><span data-stu-id="236ff-120">Create project hour estimates in Project Service Automation, and synchronize them directly from Project Service Automation to Finance.</span></span>
- <span data-ttu-id="236ff-121">Projektien kuluennusteiden luominen Project Service Automationissa ja suora synkronointi Project Service Autiomationista Financeen.</span><span class="sxs-lookup"><span data-stu-id="236ff-121">Create project expense estimates in Project Service Automation, and synchronize them directly from Project Service Automation to Finance.</span></span>
- <span data-ttu-id="236ff-122">Projektin toteutuneiden työaikojen, kulujen ja maksujen luominen Project Service Automationissa ja projektitapahtumien luominen Project Service Automationin integroinnin kirjauskansioon, jotta ne voidaan kirjata Financeen.</span><span class="sxs-lookup"><span data-stu-id="236ff-122">Create project time, expense, and fee actuals in Project Service Automation, and create project transactions in the Project Service Automation integration journal so that they can be posted in Finance.</span></span>

## <a name="data-synchronization"></a><span data-ttu-id="236ff-123">Tietojen synkronointi</span><span class="sxs-lookup"><span data-stu-id="236ff-123">Data synchronization</span></span>

<span data-ttu-id="236ff-124">Seuraavassa kuvassa on esitetty, miten tiedot synkronoidaan osana integrointia Project Service Automationin ja Financen välillä.</span><span class="sxs-lookup"><span data-stu-id="236ff-124">The following illustration shows how data is synchronized as part of the integration between Project Service Automation and Finance.</span></span>

> [!NOTE]
> <span data-ttu-id="236ff-125">Kaikki mallit eivät ole tällä hetkellä käytettävissä.</span><span class="sxs-lookup"><span data-stu-id="236ff-125">Not all templates are currently available.</span></span> <span data-ttu-id="236ff-126">Mallit julkaistaan, kun ne ovat valmiit.</span><span class="sxs-lookup"><span data-stu-id="236ff-126">Templates will be released as they are completed.</span></span>

<span data-ttu-id="236ff-127">[![Project Service Automationin integrointi Financeen](./media/PSA-integration.png)](./media/PSA-integration.png)</span><span class="sxs-lookup"><span data-stu-id="236ff-127">[![Project Service Automation integration with Finance](./media/PSA-integration.png)](./media/PSA-integration.png)</span></span>

## <a name="system-requirements-for-finance"></a><span data-ttu-id="236ff-128">Financen järjestelmävaatimukset</span><span class="sxs-lookup"><span data-stu-id="236ff-128">System requirements for Finance</span></span>

<span data-ttu-id="236ff-129">Jotta voit käyttää Project Service Automationin Financeen integroinnin ratkaisua, sinun on asennettava Enterprise Edition 7.3 ja Platform Update 12 tai uudempi.</span><span class="sxs-lookup"><span data-stu-id="236ff-129">To use the Project Service Automation to Finance integration solution, you must install Enterprise edition 7.3 with Platform update 12 or later.</span></span>

## <a name="system-requirements-for-project-service-automation"></a><span data-ttu-id="236ff-130">Project Service Automationin järjestelmävaatimukset</span><span class="sxs-lookup"><span data-stu-id="236ff-130">System requirements for Project Service Automation</span></span>

<span data-ttu-id="236ff-131">Jotta voit käyttää Project Service Automationin Financeen integroinnin ratkaisua, sinun on asennettava seuraavat osat:</span><span class="sxs-lookup"><span data-stu-id="236ff-131">To use the Project Service Automation to Finance integration solution, you must install the following components:</span></span>

- <span data-ttu-id="236ff-132">Dynamics 365 Project Service Automation -versio 9.0.0.0 tai uudempi</span><span class="sxs-lookup"><span data-stu-id="236ff-132">Dynamics 365 Project Service Automation version 9.0.0.0 or later</span></span>
- <span data-ttu-id="236ff-133">Dynamics 365 Salesin Prospect to Cash -ratkaisun versio 1.14.0.0 (v14) tai uudempi</span><span class="sxs-lookup"><span data-stu-id="236ff-133">Prospect to cash solution for Dynamics 365 Sales, version 1.14.0.0 (v14) or later</span></span>
- <span data-ttu-id="236ff-134">Dynamics 365 Project Service Automationin Project Service Automationista Financeen versio 1.0.0.0 tai uudempi</span><span class="sxs-lookup"><span data-stu-id="236ff-134">Project Service Automation to Finance solution for Dynamics 365 Project Service Automation version 1.0.0.0 or later</span></span>

## <a name="install-the-project-service-automation-to-finance-integration-solution-in-your-project-service-automation-instance"></a><span data-ttu-id="236ff-135">Project Service Automationista Financeen integroinnin ratkaisun asentaminen Project Service Automationin esiintymään</span><span class="sxs-lookup"><span data-stu-id="236ff-135">Install the Project Service Automation to Finance integration solution in your Project Service Automation instance</span></span>

<span data-ttu-id="236ff-136">Lataa Project Service Automationista Financeen integroinnin ratkaisu [Microsoft Download Centeristä](https://www.microsoft.com/download/details.aspx?id=57016) ja noudata ratkaisuun sisältyviä ohjeita.</span><span class="sxs-lookup"><span data-stu-id="236ff-136">Download the Project Service Automation to Finance integration solution from [Microsoft Download Center](https://www.microsoft.com/download/details.aspx?id=57016), and follow the instructions that are included with the solution.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]