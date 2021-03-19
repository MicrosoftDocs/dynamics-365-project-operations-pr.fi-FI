---
title: Synkronoi projektitehtäviä suoraan Project Service Automationista Finance and Operationsiin
description: Tässä aiheessa kuvataan malli ja sen pohjana oleva tehtävä, jota käytetään projektitehtävien synkronoimiseen suoraan Microsoft Dynamics 365 Project Service Automationista Dynamics 365 Financeen.
author: Yowelle
manager: AnnBe
ms.date: 07/20/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.3.0
ms.openlocfilehash: 7cc9ee9de576549c132e14c333a1000c22a55236
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5288915"
---
# <a name="synchronize-project-tasks-directly-from-project-service-automation-to-finance-and-operations"></a><span data-ttu-id="88f05-103">Synkronoi projektitehtäviä suoraan Project Service Automationista Finance and Operationsiin</span><span class="sxs-lookup"><span data-stu-id="88f05-103">Synchronize project tasks directly from Project Service Automation to Finance and Operations</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="88f05-104">Tässä aiheessa kuvataan malli ja sen pohjana oleva tehtävä, jota käytetään projektitehtävien synkronoimiseen suoraan Dynamics 365 Project Service Automationista Dynamics 365 Financeen.</span><span class="sxs-lookup"><span data-stu-id="88f05-104">This topic describes the template and underlying task that are used to synchronize project tasks directly from Dynamics 365 Project Service Automation to Dynamics 365 Finance.</span></span>

> [!NOTE]
> - <span data-ttu-id="88f05-105">Projektitehtävien integrointi, kulutapahtumien luokat, työaika-arviot, kuluarviot ja toimintojen lukitus ovat käytettävissä versiossa 8.0.</span><span class="sxs-lookup"><span data-stu-id="88f05-105">Project task integration, expense transaction categories, hour estimates, expense estimates, and functionality locking are available in version 8.0.</span></span>
> - <span data-ttu-id="88f05-106">Jos käytössäsi on Enterprise Edition 7.3.0, kun olet asentanut tietokannan 4132657 ja tietokannan 4132660, voit integroida malleja projektitehtävien, kulutapahtumien luokkien, tuntiarvioiden, kuluarvioiden ja toteutuneiden arvojen sekä toimintojen lukitsemisen määrittämiseksi.</span><span class="sxs-lookup"><span data-stu-id="88f05-106">If you're using Enterprise edition 7.3.0, after you install KB 4132657 and KB 4132660, you will be able to use the templates to integrate project tasks, expense transaction categories, hour estimates, expense estimates, and actuals, and to configure functionality locking.</span></span> <span data-ttu-id="88f05-107">Jos sinun on nollattava kirjanpidollinen jako, suosittelemme myös tietokannan 4131710 asentamista.</span><span class="sxs-lookup"><span data-stu-id="88f05-107">If you must reset the accounting distributions, we recommended that you also install KB 4131710.</span></span>
> - <span data-ttu-id="88f05-108">Toteutuneiden arvojen integrointi on käytettävissä alkaen versiosta 8.0.1 tai myöhempi.</span><span class="sxs-lookup"><span data-stu-id="88f05-108">Actuals integration is available in version 8.0.1 or later.</span></span>

## <a name="data-flow-for-project-service-automation-to-finance"></a><span data-ttu-id="88f05-109">Tietovuo Project Service Automationista Financeen</span><span class="sxs-lookup"><span data-stu-id="88f05-109">Data flow for Project Service Automation to Finance</span></span>

<span data-ttu-id="88f05-110">Project Service Automationin integrointiratkaisua Financeen käyttää tietojen integrointitoimintoa tietojen synkronointiin Project Service Automationin ja Financen eri esiintymien välillä.</span><span class="sxs-lookup"><span data-stu-id="88f05-110">The Project Service Automation to Finance integration solution uses the Data integration feature to synchronize data across instances of Project Service Automation and Finance.</span></span> <span data-ttu-id="88f05-111">Tietojen integrointitoiminnossa käytettävissä oleva integrointimalli mahdollistavaa projektitehtävien tietovuon Project Service Automationista Financeen.</span><span class="sxs-lookup"><span data-stu-id="88f05-111">The integration template that is available with the Data integration feature enables the flow of data about project tasks from Project Service Automation to Finance.</span></span>

<span data-ttu-id="88f05-112">Seuraavassa kuvassa on esitetty, miten tiedot synkronoidaan Project Service Automationin ja Financen välillä.</span><span class="sxs-lookup"><span data-stu-id="88f05-112">The following illustration shows how the data is synchronized between Project Service Automation and Finance.</span></span>

<span data-ttu-id="88f05-113">[![Tietovuo Project Service Automationin Financeen integroinnissa](./media/ProjectTasksFlow.png)](./media/ProjectTasksFlow.png)</span><span class="sxs-lookup"><span data-stu-id="88f05-113">[![Data flow for Project Service Automation integration with Finance](./media/ProjectTasksFlow.png)](./media/ProjectTasksFlow.png)</span></span>

## <a name="template-and-task"></a><span data-ttu-id="88f05-114">Malli ja tehtävä</span><span class="sxs-lookup"><span data-stu-id="88f05-114">Template and task</span></span>

<span data-ttu-id="88f05-115">Jos haluat käyttää mallia, valitse Microsoft Power Appsin hallintakeskuksessa **Projektit** ja sitten oikeassa yläkulmassa **Uusi projekti** valitaksesi julkisia malleja.</span><span class="sxs-lookup"><span data-stu-id="88f05-115">To access the template, in the Microsoft Power Apps admin center, select **Projects**, and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="88f05-116">Seuraavaa mallia ja pohjana olevaa tehtävää käytetään projektitehtävien synkronoimiseen Project Service Automationista Financeen:</span><span class="sxs-lookup"><span data-stu-id="88f05-116">The following template and underlying task are used to synchronize project tasks from Project Service Automation to Finance:</span></span>

- <span data-ttu-id="88f05-117">**Tietojen integroinnin mallin nimi:** Projektitehtävät (PSA:sta Fin:iin ja Ops:iin)</span><span class="sxs-lookup"><span data-stu-id="88f05-117">**Name of the template in Data integration:** Project tasks (PSA to Fin and Ops)</span></span>
- <span data-ttu-id="88f05-118">**Projektin tehtävän nimi:** Projektitehtävä</span><span class="sxs-lookup"><span data-stu-id="88f05-118">**Name of the task in the project:** Project tasks</span></span>

<span data-ttu-id="88f05-119">Ennen kuin projektitehtäviä voi synkronoitava, on synkronoitava projektisopimukset ja projektit.</span><span class="sxs-lookup"><span data-stu-id="88f05-119">Before synchronization of project tasks can occur, you must synchronize project contracts and projects.</span></span>

## <a name="entity-set"></a><span data-ttu-id="88f05-120">Entiteettijoukko</span><span class="sxs-lookup"><span data-stu-id="88f05-120">Entity set</span></span>

| <span data-ttu-id="88f05-121">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="88f05-121">Project Service Automation</span></span> | <span data-ttu-id="88f05-122">Rahoitus</span><span class="sxs-lookup"><span data-stu-id="88f05-122">Finance</span></span>                             |
|----------------------------|-------------------------------------|
| <span data-ttu-id="88f05-123">Projektitehtävät</span><span class="sxs-lookup"><span data-stu-id="88f05-123">Project Tasks</span></span>              | <span data-ttu-id="88f05-124">Projektitehtävän integroinnin entiteetti</span><span class="sxs-lookup"><span data-stu-id="88f05-124">Integration entity for project task</span></span> |

## <a name="entity-flow"></a><span data-ttu-id="88f05-125">Entiteettivuo</span><span class="sxs-lookup"><span data-stu-id="88f05-125">Entity flow</span></span>

<span data-ttu-id="88f05-126">Projektitehtäviä hallitaan Project Service Automationissa, ja ne synkronoidaan Financeen projektiaktiviteetteina.</span><span class="sxs-lookup"><span data-stu-id="88f05-126">Project tasks are managed in Project Service Automation, and they are synchronized to Finance as project activities.</span></span>

## <a name="prerequisites-and-mapping-setup"></a><span data-ttu-id="88f05-127">Edellytykset ja yhdistämismääritykset</span><span class="sxs-lookup"><span data-stu-id="88f05-127">Prerequisites and mapping setup</span></span>

<span data-ttu-id="88f05-128">Ennen kuin projektitehtäviä voi synkronoitava, on synkronoitava projektisopimukset ja projektit.</span><span class="sxs-lookup"><span data-stu-id="88f05-128">Before synchronization of project tasks can occur, you must synchronize project contracts and projects.</span></span>

## <a name="power-query"></a><span data-ttu-id="88f05-129">Power Query</span><span class="sxs-lookup"><span data-stu-id="88f05-129">Power Query</span></span>

<span data-ttu-id="88f05-130">Sinun on käytettävä Microsoft Power Query for Excel -isäosaa suodattamaan tietoja, jos seuraava ehto täyttyy:</span><span class="sxs-lookup"><span data-stu-id="88f05-130">You must use Microsoft Power Query for Excel to filter data if this condition is met:</span></span>

- <span data-ttu-id="88f05-131">Projektitehtävässä on resurssikohtaisia tietueita.</span><span class="sxs-lookup"><span data-stu-id="88f05-131">You have resource-specific records in a project task.</span></span>

<span data-ttu-id="88f05-132">Jos sinun on käytettävä Power Queryä, noudata seuraavaa ohjetta:</span><span class="sxs-lookup"><span data-stu-id="88f05-132">If you must use Power Query, follow this guideline:</span></span>

- <span data-ttu-id="88f05-133">Projektitehtävien (PSA:sta Fin:iin ja Ops:iin) on oletussuodatin, joka jättää resurssikohtaiset tietueet pois projektitehtävästä määrittämällä **IsLineTask**-suodattimen arvoksi **Epätosi**.</span><span class="sxs-lookup"><span data-stu-id="88f05-133">The Project tasks (PSA to Fin and Ops) template has a default filter that excludes resource-specific records from a project task by setting the filter on **IsLineTask** to **False**.</span></span> <span data-ttu-id="88f05-134">Jos luot oman mallin, tämä suodatin on lisättävä.</span><span class="sxs-lookup"><span data-stu-id="88f05-134">If you create your own template, you must add this filter.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="88f05-135">Mallien yhdistämismääritys tietojen integroinnissa</span><span class="sxs-lookup"><span data-stu-id="88f05-135">Template mapping in Data integration</span></span>

<span data-ttu-id="88f05-136">Seuraavassa kuvissa on esimerkki mallitehtävien yhdistämismäärityksestä tietojen integroinnissa.</span><span class="sxs-lookup"><span data-stu-id="88f05-136">The following illustration shows an example of the template task mappings in Data integration.</span></span> <span data-ttu-id="88f05-137">Yhdistämismäärityksessä näytetään kenttätiedot, jotka synkronoidaan Project Service Automationista Financeen.</span><span class="sxs-lookup"><span data-stu-id="88f05-137">The mapping shows the field information that will be synchronized from Project Service Automation to Finance.</span></span>

<span data-ttu-id="88f05-138">[![Yhdistelmämääritysmalli](./media/ProjectTasksMapping.png)](./media/ProjectTasksMapping.png)</span><span class="sxs-lookup"><span data-stu-id="88f05-138">[![Template mapping](./media/ProjectTasksMapping.png)](./media/ProjectTasksMapping.png)</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]