---
title: Synkronoi projektiarvioita suoraan Project Service Automationista Finance and Operationsiin
description: Tässä aiheessa kuvataan malleja ja niiden pohjana olevat tehtävät, joita käytetään projektien työaika-arvioiden ja projektien kustannusarvioiden synkronoimiseen suoraan Microsoft Dynamics 365 Project Service Automationista Dynamics 365 Financeen.
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
ms.openlocfilehash: 336de474c859d30d1ec07ae34bf0c3d578faeef1
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/16/2020
ms.locfileid: "4075476"
---
# <a name="synchronize-project-estimates-directly-from-project-service-automation-to-finance-and-operations"></a><span data-ttu-id="7b84d-103">Synkronoi projektiarvioita suoraan Project Service Automationista Finance and Operationsiin</span><span class="sxs-lookup"><span data-stu-id="7b84d-103">Synchronize project estimates directly from Project Service Automation to Finance and Operations</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="7b84d-104">Tässä aiheessa kuvataan malleja ja niiden pohjana olevat tehtävät, joita käytetään projektien työaika-arvioiden ja projektien kustannusarvioiden synkronoimiseen suoraan Dynamics 365 Project Service Automationista Dynamics 365 Financeen.</span><span class="sxs-lookup"><span data-stu-id="7b84d-104">This topic describes the templates and underlying tasks that are used to synchronize project hour estimates and project expense estimates directly from Dynamics 365 Project Service Automation to Dynamics 365 Finance.</span></span>

> [!NOTE]
> - <span data-ttu-id="7b84d-105">Projektitehtävien integrointi, kulutapahtumien luokat, työaika-arviot, kuluarviot ja toimintojen lukitus ovat käytettävissä versiossa 8.0.</span><span class="sxs-lookup"><span data-stu-id="7b84d-105">Project task integration, expense transaction categories, hour estimates, expense estimates, and functionality locking is available in version 8.0.</span></span>
> - <span data-ttu-id="7b84d-106">Toteutuneiden arvojen integrointi on käytettävissä alkaen versiosta 8.0.1 tai myöhempi.</span><span class="sxs-lookup"><span data-stu-id="7b84d-106">Actuals integration is available in version 8.0.1 or later.</span></span>

## <a name="data-flow-for-project-service-automation-to-finance"></a><span data-ttu-id="7b84d-107">Tietovuo Project Service Automationista Financeen</span><span class="sxs-lookup"><span data-stu-id="7b84d-107">Data flow for Project Service Automation to Finance</span></span>

<span data-ttu-id="7b84d-108">Project Service Automationin integrointiratkaisua Financeen käyttää tietojen integrointitoimintoa tietojen synkronointiin Project Service Automationin ja Financen eri esiintymien välillä.</span><span class="sxs-lookup"><span data-stu-id="7b84d-108">The Project Service Automation to Finance integration solution uses the Data integration feature to synchronize data across instances of Project Service Automation and Finance.</span></span> <span data-ttu-id="7b84d-109">Tietojen integrointitoiminnossa käytettävissä olevat integrointimallit mahdollistavat projektien työaika-arvioiden ja projektien kuluarvioiden tietovuon Project Service Automationista Financeen.</span><span class="sxs-lookup"><span data-stu-id="7b84d-109">The integration templates that are available with the Data integration feature enable the flow of data about project hour estimates and project expense estimates from Project Service Automation to Finance.</span></span>

<span data-ttu-id="7b84d-110">Seuraavassa kuvassa on esitetty, miten tiedot synkronoidaan Project Service Automationin ja Financen välillä.</span><span class="sxs-lookup"><span data-stu-id="7b84d-110">The following illustration shows how the data is synchronized between Project Service Automation and Finance.</span></span>

<span data-ttu-id="7b84d-111">[![Tietovuo Project Service Automationin Financeen integroinnissa](./media/ProjectEstimatesFlow.png)](./media/ProjectEstimatesFlow.png)</span><span class="sxs-lookup"><span data-stu-id="7b84d-111">[![Data flow for Project Service Automation integration with Finance](./media/ProjectEstimatesFlow.png)](./media/ProjectEstimatesFlow.png)</span></span>

## <a name="project-hour-estimates"></a><span data-ttu-id="7b84d-112">Projektin työmäärä-arviot</span><span class="sxs-lookup"><span data-stu-id="7b84d-112">Project hour estimates</span></span>

### <a name="template-and-tasks"></a><span data-ttu-id="7b84d-113">Malli ja tehtävät</span><span class="sxs-lookup"><span data-stu-id="7b84d-113">Template and tasks</span></span>

<span data-ttu-id="7b84d-114">Jos haluat käyttää käytettävissä olevia malleja, valitse Microsoft Power Appsin hallintakeskuksessa **Projektit** ja sitten oikeassa yläkulmassa **Uusi projekti** valitaksesi julkisia malleja.</span><span class="sxs-lookup"><span data-stu-id="7b84d-114">To access the available templates, in the Microsoft Power Apps admin center, select **Projects** , and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="7b84d-115">Seuraavaa mallia ja pohjana olevia tehtäviä käytetään projektien työaika-arvioiden synkronoimiseen Project Service Automationista Financeen:</span><span class="sxs-lookup"><span data-stu-id="7b84d-115">The following template and underlying tasks are used to synchronize project hour estimates from Project Service Automation to Finance:</span></span>

- <span data-ttu-id="7b84d-116">**Tietojen integroinnin mallin nimi:** Projektin työaika-arviot (PSA:sta Fin:iin ja Ops:iin)</span><span class="sxs-lookup"><span data-stu-id="7b84d-116">**Name of the template in Data integration:** Project hour estimates (PSA to Fin and Ops)</span></span>
- <span data-ttu-id="7b84d-117">**Projektin tehtävien nimet:**</span><span class="sxs-lookup"><span data-stu-id="7b84d-117">**Name of the tasks in the project:**</span></span>

    - <span data-ttu-id="7b84d-118">Tapahtumasuhteet</span><span class="sxs-lookup"><span data-stu-id="7b84d-118">Transaction relationships</span></span>
    - <span data-ttu-id="7b84d-119">Kulujen arviot</span><span class="sxs-lookup"><span data-stu-id="7b84d-119">Expense estimates</span></span>

### <a name="entity-set"></a><span data-ttu-id="7b84d-120">Entiteettijoukko</span><span class="sxs-lookup"><span data-stu-id="7b84d-120">Entity set</span></span>

| <span data-ttu-id="7b84d-121">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="7b84d-121">Project Service Automation</span></span> | <span data-ttu-id="7b84d-122">Rahoitus</span><span class="sxs-lookup"><span data-stu-id="7b84d-122">Finance</span></span>                                       |
|----------------------------|-----------------------------------------------|
| <span data-ttu-id="7b84d-123">Projektitehtävät</span><span class="sxs-lookup"><span data-stu-id="7b84d-123">Project tasks</span></span>              | <span data-ttu-id="7b84d-124">Projektien työaika-arvioiden integrointientiteetti</span><span class="sxs-lookup"><span data-stu-id="7b84d-124">Integration entity for project hour estimates</span></span> |

### <a name="entity-flow"></a><span data-ttu-id="7b84d-125">Entiteettivuo</span><span class="sxs-lookup"><span data-stu-id="7b84d-125">Entity flow</span></span>

<span data-ttu-id="7b84d-126">Projektien työaika-arvioita hallitaan Project Service Automationissa, ja ne synkronoidaan Financeen työaikaennusteina.</span><span class="sxs-lookup"><span data-stu-id="7b84d-126">Project hour estimates are managed in Project Service Automation, and they are synchronized to Finance as project hour forecasts.</span></span>

### <a name="prerequisites"></a><span data-ttu-id="7b84d-127">Edellytykset</span><span class="sxs-lookup"><span data-stu-id="7b84d-127">Prerequisites</span></span>

<span data-ttu-id="7b84d-128">Ennen kuin projektien työaika-arvioita voidaan suorittaa, on synkronoitava projektit, projektitehtävät ja projektien kulutapahtumaluokat.</span><span class="sxs-lookup"><span data-stu-id="7b84d-128">Before synchronization of project hour estimates can occur, you must synchronize projects, project tasks, and project expense transaction categories.</span></span>

### <a name="power-query"></a><span data-ttu-id="7b84d-129">Power Query</span><span class="sxs-lookup"><span data-stu-id="7b84d-129">Power Query</span></span>

<span data-ttu-id="7b84d-130">Projektien työaika-arviomallissa on käytettävä Microsoft Power Query for Exceliä seuraavien tehtävien suorittamiseen:</span><span class="sxs-lookup"><span data-stu-id="7b84d-130">In the project hour estimates template, you must use Microsoft Power Query for Excel to complete these tasks:</span></span>

- <span data-ttu-id="7b84d-131">Määritä sen oletusarvoisen ennustemallin tunnus, jota käytetään, kun integrointi luo uusia työaikaennusteita.</span><span class="sxs-lookup"><span data-stu-id="7b84d-131">Set the default forecast model ID that will be used when the integration creates new hour forecasts.</span></span>
- <span data-ttu-id="7b84d-132">Suodata kaikki ne tehtävän resurssikohtaiset tietueet, jotka aiheuttavat työaikaennusteisiin integroinnin epäonnistumisen.</span><span class="sxs-lookup"><span data-stu-id="7b84d-132">Filter out any resource-specific records in the task that will fail the integration into hour forecasts.</span></span>
- <span data-ttu-id="7b84d-133">Suodata tyhjät tapahtumaluokkarivit pois.</span><span class="sxs-lookup"><span data-stu-id="7b84d-133">Filter out any empty transaction category rows.</span></span> <span data-ttu-id="7b84d-134">Jos tätä tehtävää ei suoriteta, saattaa esiintyä virheellisiä työaikaennusteita.</span><span class="sxs-lookup"><span data-stu-id="7b84d-134">Failure to complete this task might result in incorrect hour forecasts.</span></span>

#### <a name="set-the-default-forecast-model-id"></a><span data-ttu-id="7b84d-135">Määritä oletusarvoisen ennustemallin tunnus</span><span class="sxs-lookup"><span data-stu-id="7b84d-135">Set the default forecast model ID</span></span>

<span data-ttu-id="7b84d-136">Päivitä oletusarvoisen ennustemallin tunnus mallissa avaamalla yhdistämismäärityksen valitsemalla **Yhdistämismääritys** -nuoli.</span><span class="sxs-lookup"><span data-stu-id="7b84d-136">To update the default forecast model ID in the template, click the **Map** arrow to open the mapping.</span></span> <span data-ttu-id="7b84d-137">Valitse sitten **Tarkka kysely ja suodatus** -linkki.</span><span class="sxs-lookup"><span data-stu-id="7b84d-137">Then select the **Advanced Query and Filtering** link.</span></span>

- <span data-ttu-id="7b84d-138">Jos käytät oletusarvoisten projektien työaika-arvioiden (PSA:sta Fin:iin ja Ops:iin) mallia, valitse **Sovelletut vaiheet** -luettelossa **Lisätty ehto**.</span><span class="sxs-lookup"><span data-stu-id="7b84d-138">If you're using the default Project hour estimates (PSA to Fin and Ops) template, select the **Inserted Condition** in the list of **Applied Steps**.</span></span> <span data-ttu-id="7b84d-139">Korvaa **Toiminto** -kirjauksessa **O\_forecast** sen ennustemallin tunnuksella, jota käytetään integroinnissa.</span><span class="sxs-lookup"><span data-stu-id="7b84d-139">In the **Function** entry, replace **O\_forecast** with the name of the forecast model ID that should be used with the integration.</span></span> <span data-ttu-id="7b84d-140">Oletusmallilla on esittelytiedoista peräisin oleva ennustemallin tunnus.</span><span class="sxs-lookup"><span data-stu-id="7b84d-140">The default template has a forecast model ID from the demo data.</span></span>
- <span data-ttu-id="7b84d-141">Jos olet luomassa uutta mallia, tämä sarake on lisättävä.</span><span class="sxs-lookup"><span data-stu-id="7b84d-141">If you're creating a new template, you must add this column.</span></span> <span data-ttu-id="7b84d-142">Valitse Power Queryssä **Lisää ehdollinen sarake** ja kirjoita uuden sarakkeen nimi, Kuten **Mallitunnus**.</span><span class="sxs-lookup"><span data-stu-id="7b84d-142">In Power Query, select **Add Conditional Column** , and enter a name for the new column, such as **ModelID**.</span></span> <span data-ttu-id="7b84d-143">Kirjoita sarakkeen ehto, silloin jos projektitehtävä ei ole tyhjäarvo, sitten \<enter the forecast model ID\>; muuten tyhjäarvo.</span><span class="sxs-lookup"><span data-stu-id="7b84d-143">Enter the condition for the column, where, if Project task is not null, then \<enter the forecast model ID\>; else null.</span></span>

#### <a name="filter-out-resource-specific-records"></a><span data-ttu-id="7b84d-144">Resurssikohtaisten tietueiden pois suodattaminen</span><span class="sxs-lookup"><span data-stu-id="7b84d-144">Filter out resource-specific records</span></span>

<span data-ttu-id="7b84d-145">Projektien työaikaennusteiden (PSA:sta Fin:iin ja Ops:iin) mallissa on oletussuodatin, joka poistaa kaikki resurssikohtaiset tietueet.</span><span class="sxs-lookup"><span data-stu-id="7b84d-145">The Project hour estimates (PSA to Fin and Ops) template has a default filter that removes any resource-specific records.</span></span> <span data-ttu-id="7b84d-146">Jos luot oman mallin, tämä suodatin on lisättävä.</span><span class="sxs-lookup"><span data-stu-id="7b84d-146">If you create your own template, you must add this filter.</span></span> <span data-ttu-id="7b84d-147">Valitse **Tarkka kysely ja suodatus** -linkki suodattaaksesi **msdyn\_islinetask** -saraketta siten, että vain tietueet, joiden arvo on **Epätosi** ovat mukana.</span><span class="sxs-lookup"><span data-stu-id="7b84d-147">Select the **Advanced Query and Filtering** link to filter on the **msdyn\_islinetask** column so that only **False** records are included.</span></span>

#### <a name="filter-out-empty-transaction-category-rows"></a><span data-ttu-id="7b84d-148">Tyhjien tapahtumaluokkarivien pois suodattaminen</span><span class="sxs-lookup"><span data-stu-id="7b84d-148">Filter out empty transaction category rows</span></span>

<span data-ttu-id="7b84d-149">Sinun on lisättävä suodatin poistaaksesi kaikki rivit, joilla on tyhjiä tapahtumaluokkia.</span><span class="sxs-lookup"><span data-stu-id="7b84d-149">You must add a filter to remove any rows that have empty transaction categories.</span></span> <span data-ttu-id="7b84d-150">Tämä tehtävä on pakollinen riippumatta siitä, käytätkö oletusmallia vai luotko oman mallin.</span><span class="sxs-lookup"><span data-stu-id="7b84d-150">This task is required, regardless of whether you're using the default template or creating your own template.</span></span> <span data-ttu-id="7b84d-151">Tämä suodatin poistaa Project Service Automationista kaikki yhteenvetorivit, jotka saattavat aiheuttaa virheitä Financen työaikaennusteissa.</span><span class="sxs-lookup"><span data-stu-id="7b84d-151">This filter removes any summary rows from Project Service Automation that might cause the hour forecasts in Finance to be incorrect.</span></span> <span data-ttu-id="7b84d-152">Valitse **Tarkka kysely ja suodatus** -linkki suodattaaksesi tyhjät tietueet sarakkeessa **msdyn\_transactioncategory\_value**.</span><span class="sxs-lookup"><span data-stu-id="7b84d-152">Select **Advanced Query and Filtering** link to filter out null records in the **msdyn\_transactioncategory\_value** column.</span></span>

### <a name="template-mapping-in-data-integration"></a><span data-ttu-id="7b84d-153">Mallien yhdistämismääritys tietojen integroinnissa</span><span class="sxs-lookup"><span data-stu-id="7b84d-153">Template mapping in Data integration</span></span>

<span data-ttu-id="7b84d-154">Seuraavassa kuvissa on esimerkki mallitehtävien yhdistämismäärityksissä tietojen integroinnissa.</span><span class="sxs-lookup"><span data-stu-id="7b84d-154">The following illustration shows an example of the template task mapping in Data integration.</span></span> <span data-ttu-id="7b84d-155">Yhdistämismäärityksessä näytetään kenttätiedot, jotka synkronoidaan Project Service Automationista Financeen.</span><span class="sxs-lookup"><span data-stu-id="7b84d-155">The mapping shows the field information that will be synchronized from Project Service Automation to Finance.</span></span>

<span data-ttu-id="7b84d-156">[![Mallitehtävän yhdistämismääritys tietojen integroinnissa](./media/ProjectHourEstimatesMapping.jpg)](./media/ProjectHourEstimatesMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="7b84d-156">[![Template task mapping in data integration](./media/ProjectHourEstimatesMapping.jpg)](./media/ProjectHourEstimatesMapping.jpg)</span></span>

## <a name="project-expense-estimates"></a><span data-ttu-id="7b84d-157">Projektin kuluarviot</span><span class="sxs-lookup"><span data-stu-id="7b84d-157">Project expense estimates</span></span>

### <a name="template-and-tasks"></a><span data-ttu-id="7b84d-158">Malli ja tehtävät</span><span class="sxs-lookup"><span data-stu-id="7b84d-158">Template and tasks</span></span>

<span data-ttu-id="7b84d-159">Seuraavaa mallia ja pohjana olevia tehtäviä käytetään projektien kuluarvioiden synkronoimiseen Project Service Automationista Financeen:</span><span class="sxs-lookup"><span data-stu-id="7b84d-159">The following template and underlying tasks are used to synchronize project expense estimates from Project Service Automation to Finance:</span></span>

- <span data-ttu-id="7b84d-160">**Tietojen integroinnin mallin nimi:** Projektin kuluarviot (PSA:sta Fin:iin ja Ops:iin)</span><span class="sxs-lookup"><span data-stu-id="7b84d-160">**Name of the template in Data integration:** Project expense estimates (PSA to Fin and Ops)</span></span>
- <span data-ttu-id="7b84d-161">**Projektin tehtävien nimet:**</span><span class="sxs-lookup"><span data-stu-id="7b84d-161">**Name of the tasks in the project:**</span></span>

    - <span data-ttu-id="7b84d-162">Tapahtumasuhteet</span><span class="sxs-lookup"><span data-stu-id="7b84d-162">Transaction relationships</span></span> 
    - <span data-ttu-id="7b84d-163">Kulujen arviot</span><span class="sxs-lookup"><span data-stu-id="7b84d-163">Expense estimates</span></span>

### <a name="entity-set"></a><span data-ttu-id="7b84d-164">Entiteettijoukko</span><span class="sxs-lookup"><span data-stu-id="7b84d-164">Entity set</span></span>

| <span data-ttu-id="7b84d-165">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="7b84d-165">Project Service Automation</span></span> | <span data-ttu-id="7b84d-166">Rahoitus</span><span class="sxs-lookup"><span data-stu-id="7b84d-166">Finance</span></span>                                                  |
|----------------------------|----------------------------------------------------------|
| <span data-ttu-id="7b84d-167">Tapahtuman yhteydet</span><span class="sxs-lookup"><span data-stu-id="7b84d-167">Transaction Connections</span></span>    | <span data-ttu-id="7b84d-168">Projektitapahtuman integrointikohdesuhteet</span><span class="sxs-lookup"><span data-stu-id="7b84d-168">Integration entity for project transaction relationships</span></span> |
| <span data-ttu-id="7b84d-169">Arviorivit</span><span class="sxs-lookup"><span data-stu-id="7b84d-169">Estimate Lines</span></span>             | <span data-ttu-id="7b84d-170">Projektien kuluarvioiden integrointientiteetti</span><span class="sxs-lookup"><span data-stu-id="7b84d-170">Integration entity for project expense estimates</span></span>         |

### <a name="entity-flow"></a><span data-ttu-id="7b84d-171">Entiteettivuo</span><span class="sxs-lookup"><span data-stu-id="7b84d-171">Entity flow</span></span>

<span data-ttu-id="7b84d-172">Projektien kuluarvioita hallitaan Project Service Automationissa, ja ne synkronoidaan Financeen kuluennusteina.</span><span class="sxs-lookup"><span data-stu-id="7b84d-172">Project expense estimates are managed in Project Service Automation, and they are synchronized to Finance as project expense forecasts.</span></span>

### <a name="prerequisites"></a><span data-ttu-id="7b84d-173">Edellytykset</span><span class="sxs-lookup"><span data-stu-id="7b84d-173">Prerequisites</span></span>

<span data-ttu-id="7b84d-174">Ennen kuin projektien kuluarvioita voidaan suorittaa, on synkronoitava projektit, projektitehtävät ja projektien kulutapahtumaluokat.</span><span class="sxs-lookup"><span data-stu-id="7b84d-174">Before synchronization of project expense estimates can occur, you must synchronize projects, project tasks, and project expense transaction categories.</span></span>

### <a name="power-query"></a><span data-ttu-id="7b84d-175">Power Query</span><span class="sxs-lookup"><span data-stu-id="7b84d-175">Power Query</span></span>

<span data-ttu-id="7b84d-176">Projektien kuluarviomallissa on käytettävä Power Queryä seuraavien tehtävien suorittamiseen:</span><span class="sxs-lookup"><span data-stu-id="7b84d-176">In the project expense estimates template, you must use Power Query to complete the following tasks:</span></span>

- <span data-ttu-id="7b84d-177">Suodatus siten, että mukana on vain kuluarviorivitietueita.</span><span class="sxs-lookup"><span data-stu-id="7b84d-177">Filter to include only expense estimate line records.</span></span>
- <span data-ttu-id="7b84d-178">Määritä sen oletusarvoisen ennustemallin tunnus, jota käytetään, kun integrointi luo uusia työaikaennusteita.</span><span class="sxs-lookup"><span data-stu-id="7b84d-178">Set the default forecast model ID that will be used when the integration creates new hour forecasts.</span></span>
- <span data-ttu-id="7b84d-179">Laskutustyyppien muuntaminen.</span><span class="sxs-lookup"><span data-stu-id="7b84d-179">Transform the billing types.</span></span>
- <span data-ttu-id="7b84d-180">Tapahtumatyyppien muuntaminen.</span><span class="sxs-lookup"><span data-stu-id="7b84d-180">Transform the transaction types.</span></span>

#### <a name="filter-to-include-only-expense-estimate-lines"></a><span data-ttu-id="7b84d-181">Suodatus siten, että mukana on vain kuluarviorivejä</span><span class="sxs-lookup"><span data-stu-id="7b84d-181">Filter to include only expense estimate lines</span></span>

<span data-ttu-id="7b84d-182">Projektin kuluarvioiden (PSA:sta Fin:iin ja Ops:iin) -mallissa on oletussuodatin, jonka ansiosta integroinnissa on mukana vain kulurivejä.</span><span class="sxs-lookup"><span data-stu-id="7b84d-182">The Project expense estimates (PSA to Fin and Ops) template has a default filter that includes only expense lines in the integration.</span></span> <span data-ttu-id="7b84d-183">Jos luot oman mallin, tämä suodatin on lisättävä.</span><span class="sxs-lookup"><span data-stu-id="7b84d-183">If you create your own template, you must add this filter.</span></span> <span data-ttu-id="7b84d-184">Valitse **Tapahtumasuhteet** -tehtävä ja avaa siten yhdistämismääritys valitsemalla **Yhdistämismääritys** -nuoli.</span><span class="sxs-lookup"><span data-stu-id="7b84d-184">Select the **Transaction relationships** task, and then click the **Map** arrow to open the mapping.</span></span> <span data-ttu-id="7b84d-185">Valitse **Tarkka kysely ja suodatus** -linkki.</span><span class="sxs-lookup"><span data-stu-id="7b84d-185">Select the **Advanced Query and Filtering** link.</span></span> <span data-ttu-id="7b84d-186">Suodata **msdyn\_transactiontype1** -saraketta siten, että se sisältää vain **msdyn\_estimateline** -kohteita.</span><span class="sxs-lookup"><span data-stu-id="7b84d-186">Filter the **msdyn\_transactiontype1** column so that it includes only **msdyn\_estimateline**.</span></span>

#### <a name="set-the-default-forecast-model-id"></a><span data-ttu-id="7b84d-187">Määritä oletusarvoisen ennustemallin tunnus</span><span class="sxs-lookup"><span data-stu-id="7b84d-187">Set the default forecast model ID</span></span>

<span data-ttu-id="7b84d-188">Päivitä oletusarvoisen ennustemallin tunnus mallissa valitsemalla **Kuluarviot** -tehtävä ja avaamalla sitten yhdistämismääritys valitsemalla **Yhdistämismääritys** -nuoli.</span><span class="sxs-lookup"><span data-stu-id="7b84d-188">To update the default forecast model ID in the template, select the **Expense estimates** task, and then click the **Map** arrow to open the mapping.</span></span> <span data-ttu-id="7b84d-189">Valitse **Tarkka kysely ja suodatus** -linkki.</span><span class="sxs-lookup"><span data-stu-id="7b84d-189">Select the **Advanced Query and Filtering** link.</span></span>

- <span data-ttu-id="7b84d-190">Jos käytät oletusarvoisten projektien kuluarvioiden (PSA:sta Fin:iin ja Ops:iin) mallia, valitse Power Queryssä ensimmäinen **Lisätty ehto** **Sovelletut vaiheet** -osasta.</span><span class="sxs-lookup"><span data-stu-id="7b84d-190">If you're using the default Project expense estimates (PSA to Fin and Ops) template, in Power Query, select the first **Inserted Condition** from the **Applied Steps** section.</span></span> <span data-ttu-id="7b84d-191">Korvaa **Toiminto** -kirjauksessa **O\_forecast** sen ennustemallin tunnuksella, jota käytetään integroinnissa.</span><span class="sxs-lookup"><span data-stu-id="7b84d-191">In the **Function** entry, replace **O\_forecast** with the name of the forecast model ID that should be used with the integration.</span></span> <span data-ttu-id="7b84d-192">Oletusmallilla on esittelytiedoista peräisin oleva ennustemallin tunnus.</span><span class="sxs-lookup"><span data-stu-id="7b84d-192">The default template has a forecast model ID from the demo data.</span></span>
- <span data-ttu-id="7b84d-193">Jos olet luomassa uutta mallia, tämä sarake on lisättävä.</span><span class="sxs-lookup"><span data-stu-id="7b84d-193">If you're creating a new template, you must add this column.</span></span> <span data-ttu-id="7b84d-194">Valitse Power Queryssä **Lisää ehdollinen sarake** ja kirjoita uuden sarakkeen nimi, Kuten **Mallitunnus**.</span><span class="sxs-lookup"><span data-stu-id="7b84d-194">In Power Query, select **Add Conditional Column** , and enter a name for the new column, such as **ModelID**.</span></span> <span data-ttu-id="7b84d-195">Kirjoita sarakkeen ehto, silloin jos arviorivitunnus ei ole tyhjäarvo, sitten \<enter the forecast model ID\>; muuten tyhjäarvo.</span><span class="sxs-lookup"><span data-stu-id="7b84d-195">Enter the condition for the column, where, if Estimate line ID is not null, then \<enter the forecast model ID\>; else null.</span></span>

#### <a name="transform-the-billing-types"></a><span data-ttu-id="7b84d-196">Laskutustyyppien muuntaminen</span><span class="sxs-lookup"><span data-stu-id="7b84d-196">Transform the billing types</span></span>

<span data-ttu-id="7b84d-197">Projektin kuluarviot (PSA:sta Fin:iin ja Ops:iin) -mallissa on ehdollinen sarake, jonka avulla voidaan muuntaa laskutustyyppejä, jotka vastaanotetaan Project Service Automationista integroinnin aikana.</span><span class="sxs-lookup"><span data-stu-id="7b84d-197">The Project expense estimates (PSA to Fin and Ops) template includes a conditional column that is used to transform the billing types that are received from Project Service Automation during the integration.</span></span> <span data-ttu-id="7b84d-198">Jos luot oman mallin, tämä ehdollinen sarake on lisättävä.</span><span class="sxs-lookup"><span data-stu-id="7b84d-198">If you create your own template, you must add this conditional column.</span></span> <span data-ttu-id="7b84d-199">Valitse **Tarkka kysely ja suodatus** -linkki ja valitse sitten **Lisää ehdollinen sarake**.</span><span class="sxs-lookup"><span data-stu-id="7b84d-199">Select the **Advanced Query and Filtering** link and then select **Add Conditional Column**.</span></span> <span data-ttu-id="7b84d-200">Syötä uudelle sarakkeelle nimi, kuten **Laskutustyyppi**.</span><span class="sxs-lookup"><span data-stu-id="7b84d-200">Enter a name for the new column, such as **BillingType**.</span></span> <span data-ttu-id="7b84d-201">Syötä sitten seuraava ehto:</span><span class="sxs-lookup"><span data-stu-id="7b84d-201">Then enter the following condition:</span></span>

<span data-ttu-id="7b84d-202">If **msdyn\_billingtype** = 192350000, then **NonChargeable**</span><span class="sxs-lookup"><span data-stu-id="7b84d-202">If **msdyn\_billingtype** = 192350000, then **NonChargeable**</span></span>  
<span data-ttu-id="7b84d-203">else if **msdyn\_billingtype** = 192350001, then **Chargeable**</span><span class="sxs-lookup"><span data-stu-id="7b84d-203">else if **msdyn\_billingtype** = 192350001, then **Chargeable**</span></span>  
<span data-ttu-id="7b84d-204">else if **msdyn\_billingtype** = 192350002, then **Complimentary**</span><span class="sxs-lookup"><span data-stu-id="7b84d-204">else if **msdyn\_billingtype** = 192350002, then **Complimentary**</span></span>  
<span data-ttu-id="7b84d-205">else **NotAvailable**</span><span class="sxs-lookup"><span data-stu-id="7b84d-205">else **NotAvailable**</span></span>

#### <a name="transform-the-transaction-types"></a><span data-ttu-id="7b84d-206">Tapahtumatyyppien muuntaminen</span><span class="sxs-lookup"><span data-stu-id="7b84d-206">Transform the transaction types</span></span>

<span data-ttu-id="7b84d-207">Projektin kuluarviot (PSA:sta Fin:iin ja Ops:iin) -mallissa on ehdollinen sarake, jonka avulla voidaan muuntaa tapahtumatyyppejä, jotka vastaanotetaan Project Service Automationista integroinnin aikana.</span><span class="sxs-lookup"><span data-stu-id="7b84d-207">The Project expense estimates (PSA to Fin and Ops) template includes a conditional column that is used to transform the transaction types that are received from Project Service Automation during the integration.</span></span> <span data-ttu-id="7b84d-208">Jos luot oman mallin, tämä ehdollinen sarake on lisättävä.</span><span class="sxs-lookup"><span data-stu-id="7b84d-208">If you create your own template, you must add this conditional column.</span></span> <span data-ttu-id="7b84d-209">Valitse **Tarkka kysely ja suodatus** -linkki ja valitse sitten **Lisää ehdollinen sarake**.</span><span class="sxs-lookup"><span data-stu-id="7b84d-209">Select the **Advanced Query and Filtering** link and then select **Add Conditional Column**.</span></span> <span data-ttu-id="7b84d-210">Syötä uudelle sarakkeelle nimi, kuten **Tapahtumatyyppi**.</span><span class="sxs-lookup"><span data-stu-id="7b84d-210">Enter a name for the new column, such as **TransactionType**.</span></span> <span data-ttu-id="7b84d-211">Syötä sitten seuraava ehto:</span><span class="sxs-lookup"><span data-stu-id="7b84d-211">Then enter the following condition:</span></span>

<span data-ttu-id="7b84d-212">If **msdyn\_transactiontypecode** = 192350000, then **Cost**</span><span class="sxs-lookup"><span data-stu-id="7b84d-212">If **msdyn\_transactiontypecode** = 192350000, then **Cost**</span></span>  
<span data-ttu-id="7b84d-213">else if **msdyn\_transactiontypecode** = 192350005, then **Sales**</span><span class="sxs-lookup"><span data-stu-id="7b84d-213">else if **msdyn\_transactiontypecode** = 192350005, then **Sales**</span></span>  
<span data-ttu-id="7b84d-214">else **null**</span><span class="sxs-lookup"><span data-stu-id="7b84d-214">else **null**</span></span>

### <a name="template-mapping-in-data-integration"></a><span data-ttu-id="7b84d-215">Mallien yhdistämismääritys tietojen integroinnissa</span><span class="sxs-lookup"><span data-stu-id="7b84d-215">Template mapping in Data integration</span></span>

<span data-ttu-id="7b84d-216">Seuraavissa kuvissa on esimerkkejä mallitehtävien yhdistämismäärityksestä tietojen integroinnissa.</span><span class="sxs-lookup"><span data-stu-id="7b84d-216">The following illustrations show examples of the template task mappings in Data integration.</span></span> <span data-ttu-id="7b84d-217">Yhdistämismäärityksessä näytetään kenttätiedot, jotka synkronoidaan Project Service Automationista Financeen.</span><span class="sxs-lookup"><span data-stu-id="7b84d-217">The mapping shows the field information that will be synchronized from Project Service Automation to Finance.</span></span>

<span data-ttu-id="7b84d-218">[![Kuluarviotapahtumien mallin yhdistäminen](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="7b84d-218">[![Template mapping of expense estimate transactions](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)</span></span>

<span data-ttu-id="7b84d-219">[![Kuluarvioiden mallin yhdistäminen](./media/ExpenseEstimatesMapping.jpg)](./media/ExpenseEstimatesMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="7b84d-219">[![Template mapping of expense estimates](./media/ExpenseEstimatesMapping.jpg)](./media/ExpenseEstimatesMapping.jpg)</span></span>
