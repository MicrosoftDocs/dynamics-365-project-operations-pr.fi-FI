---
title: Synkronoi projektikulujen luokat Finance and Operationsin ja Project Service Automationin välillä
description: Tässä aiheessa kuvataan malleja ja sen pohjana olevia tehtäviä, jota käytetään projektin kululuokkien synkronoimiseen suoraan Microsoft Dynamics 365 Financen ja Dynamics 365 Project Service Automationin välillä.
author: KimANelson
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
ms.assetid: 7dd914dc-1913-45eb-8a67-e897b00089fa
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 8.0.0
ms.openlocfilehash: 757fe1dbc804b986fc3334ebae7254a3f0491f59
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/24/2020
ms.locfileid: "3751203"
---
# <a name="synchronize-project-expense-categories-between-finance-and-operations-and-project-service-automation"></a><span data-ttu-id="b9d7b-103">Synkronoi projektikulujen luokat Finance and Operationsin ja Project Service Automationin välillä</span><span class="sxs-lookup"><span data-stu-id="b9d7b-103">Synchronize project expense categories between Finance and Operations and Project Service Automation</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="b9d7b-104">Tässä aiheessa kuvataan malleja ja sen pohjana olevia tehtäviä, jota käytetään projektin kululuokkien synkronoimiseen suoraan Dynamics 365 Financen ja Dynamics 365 Project Service Automationin välillä.</span><span class="sxs-lookup"><span data-stu-id="b9d7b-104">This topic describes the templates and underlying tasks that are used to synchronize project expense categories between Dynamics 365 Finance and Dynamics 365 Project Service Automation.</span></span>

> [!NOTE]
> - <span data-ttu-id="b9d7b-105">Projektitehtävien integrointi, kulutapahtumien luokat, työaika-arviot, kuluarviot ja toimintojen lukitus ovat käytettävissä versiossa 8.0.</span><span class="sxs-lookup"><span data-stu-id="b9d7b-105">Project task integration, expense transaction categories, hour estimates, expense estimates, and functionality locking are available in version 8.0.</span></span>
> - <span data-ttu-id="b9d7b-106">Toteutuneiden arvojen integrointi on käytettävissä alkaen versiosta 8.0.1 tai myöhempi.</span><span class="sxs-lookup"><span data-stu-id="b9d7b-106">Actuals integration is available in version 8.0.1 or later.</span></span>
> - <span data-ttu-id="b9d7b-107">Jos käytössäsi on Enterprise Edition 7.3.0, kun olet asentanut tietokannan 4132657 ja tietokannan 4132660, voit integroida malleja projektitehtävien, kulutapahtumien luokkien, tuntiarvioiden, kuluarvioiden ja toteutuneiden arvojen sekä toimintojen lukitsemisen määrittämiseksi.</span><span class="sxs-lookup"><span data-stu-id="b9d7b-107">If you're using Enterprise edition 7.3.0, after you install KB 4132657 and KB 4132660, you will be able to use the templates to integrate project tasks, expense transaction categories, hour estimates, expense estimates, and actuals, and to configure functionality locking.</span></span> <span data-ttu-id="b9d7b-108">Jos sinun on nollattava kirjanpidollinen jako, suosittelemme myös tietokannan 4131710 asentamista.</span><span class="sxs-lookup"><span data-stu-id="b9d7b-108">If you must reset the accounting distributions, we recommend that you also install KB 4131710.</span></span>

## <a name="data-flow-for-project-service-automation-and-finance"></a><span data-ttu-id="b9d7b-109">Tietovuo Project Service Automationille ja Financelle</span><span class="sxs-lookup"><span data-stu-id="b9d7b-109">Data flow for Project Service Automation and Finance</span></span>

<span data-ttu-id="b9d7b-110">Project Service Automationin ja Financen integrointiratkaisua käyttää tietojen integrointitoimintoa tietojen synkronointiin Project Service Automationin ja Financen eri esiintymien välillä.</span><span class="sxs-lookup"><span data-stu-id="b9d7b-110">The Project Service Automation and Finance integration solution uses the Data integration feature to synchronize data across instances of Project Service Automation and Finance.</span></span> <span data-ttu-id="b9d7b-111">Tietojen integrointitoiminnossa käytettävissä olevat integrointimallit mahdollistavat projektien liiketapahtumaluokkien tietovuon Financen ja Project Service Automationin välillä.</span><span class="sxs-lookup"><span data-stu-id="b9d7b-111">The integration templates that are available with the Data integration feature enable the flow of data about project expense transaction categories between Finance and Project Service Automation.</span></span>

<span data-ttu-id="b9d7b-112">Jos projektin kululuokkia hallitaan Financessa, integrointi tehdään ensin Financesta Project Service Automationiin.</span><span class="sxs-lookup"><span data-stu-id="b9d7b-112">If the project expense categories are mastered in Finance, the integration flow is first from Finance to Project Service Automation.</span></span> <span data-ttu-id="b9d7b-113">Projektin kululuokkien integrointitunnukset päivitetään sitten Project Service Automationista Financeen synkronoimalla.</span><span class="sxs-lookup"><span data-stu-id="b9d7b-113">The integration IDs of the project expense categories are then updated through synchronization from Project Service Automation to Finance.</span></span>

<span data-ttu-id="b9d7b-114">Jos projektin kululuokkia hallitaan Project Service Automationissa, integrointi tehdään ensin Project Service Automationista Financeen.</span><span class="sxs-lookup"><span data-stu-id="b9d7b-114">If the project expense categories are mastered in Project Service Automation, the integration flow is first from Project Service Automation to Finance.</span></span> <span data-ttu-id="b9d7b-115">Projektiluokat täytyy jo määrittää Financessa ennen synkronointia Project Service Automationista.</span><span class="sxs-lookup"><span data-stu-id="b9d7b-115">The project categories must already be configured in Finance before the synchronization from Project Service Automation.</span></span> <span data-ttu-id="b9d7b-116">Synkronoi sitten Financesta takaisin Project Service Automationiin ja sitten Project Service Automation -palvelusta Financeen uudelleen.</span><span class="sxs-lookup"><span data-stu-id="b9d7b-116">Then synchronize from Finance back to Project Service Automation, and then from Project Service Automation to Finance again.</span></span> <span data-ttu-id="b9d7b-117">Näin varmistetaan, että luokat on linkitetty eikä kaksoiskappaleita luoda.</span><span class="sxs-lookup"><span data-stu-id="b9d7b-117">In this way, you help guarantee that the categories are linked, and that no duplicates are created.</span></span>

> [!NOTE]
> <span data-ttu-id="b9d7b-118">Yleensä projektin kululuokkia hallitaan Financessa.</span><span class="sxs-lookup"><span data-stu-id="b9d7b-118">Typically, the project expense categories are mastered in Finance.</span></span> <span data-ttu-id="b9d7b-119">Jos niitä ei kuitenkaan ole tai jos kululuokkia on jo luotu Project Service Automationissa, sinun on ensin synkronoitava käyttämällä projektin kulutapahtumaluokkia (PSA to Fin ja OPS).</span><span class="sxs-lookup"><span data-stu-id="b9d7b-119">However, if they aren't, or if expense categories have already been created in Project Service Automation, you must first synchronize by using the Project expense transaction categories (PSA to Fin and Ops) template.</span></span> <span data-ttu-id="b9d7b-120">Synkronoi sitten käyttämällä projektin kulutapahtumaluokkamallia (FIN ja Ops PSA).</span><span class="sxs-lookup"><span data-stu-id="b9d7b-120">Then synchronize by using the Project expense transaction categories (Fin and Ops to PSA) template.</span></span> <span data-ttu-id="b9d7b-121">Suorita sitten synkronointi Project Service Automationista Financeen vielä yhden kerran.</span><span class="sxs-lookup"><span data-stu-id="b9d7b-121">You should then run the synchronization from Project Service Automation to Finance one more time.</span></span>
>
> <span data-ttu-id="b9d7b-122">Jos synkronoit ensin Project Service Automationista, seuraavien vaatimusten on täytyttävä Financessa, ennen kuin synkronointi suoritetaan:</span><span class="sxs-lookup"><span data-stu-id="b9d7b-122">If you synchronize first from Project Service Automation, the following requirements must be met in Finance before the synchronization is run:</span></span>
>
> - <span data-ttu-id="b9d7b-123">Project Service Automationissa määritettyä projektiluokkaa vastaavan jaetun luokan on oltava käytössä, ja sen on oltava otettu käyttöön sekä **Projektissa** että **Kulussa**.</span><span class="sxs-lookup"><span data-stu-id="b9d7b-123">The shared category that matches the project category that is set up in Project Service Automation must exist, and it must be enabled for both **Project** and **Expense**.</span></span>
> - <span data-ttu-id="b9d7b-124">Kullakin Financen yrityksellä, johon on integroituva, on oltava seuraavat projektiluokat:</span><span class="sxs-lookup"><span data-stu-id="b9d7b-124">For each Finance legal entity that must be integrated with, the following project categories must exist:</span></span>
>
>     - <span data-ttu-id="b9d7b-125">**Projektiluokka** on olemassa.</span><span class="sxs-lookup"><span data-stu-id="b9d7b-125">**Project category** exists.</span></span> 
>     - <span data-ttu-id="b9d7b-126">**Käytä kuluina** -asetus on käytössä.</span><span class="sxs-lookup"><span data-stu-id="b9d7b-126">**Use in Expense** is enabled.</span></span>
>     - <span data-ttu-id="b9d7b-127">**Aktiivinen kirjauskansiossa** on käytössä.</span><span class="sxs-lookup"><span data-stu-id="b9d7b-127">**Active in journal** is enabled.</span></span>
>     - <span data-ttu-id="b9d7b-128">**Tapahtumatyypiksi** on määritetty **Kulu**.</span><span class="sxs-lookup"><span data-stu-id="b9d7b-128">**Transaction type** is set to **Expense**.</span></span>

<span data-ttu-id="b9d7b-129">Seuraavassa kuvassa on esitetty, miten tiedot synkronoidaan Project Service Automationin ja Financen välillä.</span><span class="sxs-lookup"><span data-stu-id="b9d7b-129">The following illustration shows how the data is synchronized between Project Service Automation and Finance.</span></span>

<span data-ttu-id="b9d7b-130">[![Tietovuo Project Service Automationin Financeen integroinnissa](./media/ProjectExpenseCategoriesFlow.png)](./media/ProjectExpenseCategoriesFlow.png)</span><span class="sxs-lookup"><span data-stu-id="b9d7b-130">[![Data flow for Project Service Automation integration with Finance](./media/ProjectExpenseCategoriesFlow.png)](./media/ProjectExpenseCategoriesFlow.png)</span></span>

## <a name="project-expense-category-synchronization-from-finance-to-project-service-automation"></a><span data-ttu-id="b9d7b-131">Projektikululuokkien synkronointi Financen ja Project Service Automationin välillä</span><span class="sxs-lookup"><span data-stu-id="b9d7b-131">Project expense category synchronization from Finance to Project Service Automation</span></span>

### <a name="template-and-task"></a><span data-ttu-id="b9d7b-132">Malli ja tehtävä</span><span class="sxs-lookup"><span data-stu-id="b9d7b-132">Template and task</span></span>

<span data-ttu-id="b9d7b-133">Jos haluat käyttää mallia, valitse Microsoft Power Appsin hallintakeskuksessa **Projektit** ja sitten oikeassa yläkulmassa **Uusi projekti** valitaksesi julkisia malleja.</span><span class="sxs-lookup"><span data-stu-id="b9d7b-133">To access the template, in the Microsoft Power Apps admin center, select **Projects**, and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="b9d7b-134">Seuraavaa mallia ja pohjana olevaa tehtävää käytetään projektien kululuokkien synkronoimiseen Financesta Project Service Automationiin:</span><span class="sxs-lookup"><span data-stu-id="b9d7b-134">The following template and underlying task are used to synchronize project expense categories from Finance to Project Service Automation:</span></span>

- <span data-ttu-id="b9d7b-135">**Tietojen integrointimallin nimi:** Projektin kuluarviotapahtumien luokat (Fin ja Ops to PSA:han)</span><span class="sxs-lookup"><span data-stu-id="b9d7b-135">**Name of the template in Data integration:** Project expense transaction categories (Fin and Ops to PSA)</span></span>
- <span data-ttu-id="b9d7b-136">**Projektin tehtävän nimi:** Synkronoi luokat PSA-järjestelmään</span><span class="sxs-lookup"><span data-stu-id="b9d7b-136">**Name of the task in the project:** Sync categories to PSA</span></span>

### <a name="entity-set"></a><span data-ttu-id="b9d7b-137">Entiteettijoukko</span><span class="sxs-lookup"><span data-stu-id="b9d7b-137">Entity set</span></span>

| <span data-ttu-id="b9d7b-138">Rahoitus</span><span class="sxs-lookup"><span data-stu-id="b9d7b-138">Finance</span></span>                           | <span data-ttu-id="b9d7b-139">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="b9d7b-139">Project Service Automation</span></span> |
|-----------------------------------|----------------------------|
| <span data-ttu-id="b9d7b-140">Luokkien integroinnin entiteetti</span><span class="sxs-lookup"><span data-stu-id="b9d7b-140">Integration entity for categories</span></span> | <span data-ttu-id="b9d7b-141">Tapahtumaluokat</span><span class="sxs-lookup"><span data-stu-id="b9d7b-141">Transaction categories</span></span>     |

### <a name="entity-flow"></a><span data-ttu-id="b9d7b-142">Entiteettivuo</span><span class="sxs-lookup"><span data-stu-id="b9d7b-142">Entity flow</span></span>

<span data-ttu-id="b9d7b-143">Projektien kululuokkia hallitaan Financessa ja ne synkronoidaan Project Service Automationiin tapahtumaluokkina.</span><span class="sxs-lookup"><span data-stu-id="b9d7b-143">Project expense categories are managed in Finance, and they are synchronized to Project Service Automation as transaction categories.</span></span>

### <a name="power-query"></a><span data-ttu-id="b9d7b-144">Power Query</span><span class="sxs-lookup"><span data-stu-id="b9d7b-144">Power Query</span></span>

<span data-ttu-id="b9d7b-145">Kun synkronoit Project Service Automationin, sinun täytyy käyttää Microsoft Power Query for Exceliä, kun haluat määrittää laskutustyypin tapahtumaluokalle.</span><span class="sxs-lookup"><span data-stu-id="b9d7b-145">When you're synchronizing to Project Service Automation, you must use Microsoft Power Query for Excel to set the billing type on the transaction category.</span></span> <span data-ttu-id="b9d7b-146">Projektin kulutapahtumaluokat (FIN ja Ops to PSA) -malli sisältää oletussarakkeen ja -yhdistämismäärityksen.</span><span class="sxs-lookup"><span data-stu-id="b9d7b-146">The Project expense transaction categories (Fin and Ops to PSA) template provides a default column and mapping.</span></span> <span data-ttu-id="b9d7b-147">Jos luot oman mallin, ehdollinen sarake on lisättävä Power Queryyn.</span><span class="sxs-lookup"><span data-stu-id="b9d7b-147">If you create your own template, you must add a conditional column in Power Query.</span></span> <span data-ttu-id="b9d7b-148">Toimi seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="b9d7b-148">Follow these steps.</span></span>

1. <span data-ttu-id="b9d7b-149">Napsauttamalla nuolta voit avata projektikululuokat tehtävänyhdistämismäärityksen projektin kulutapahtumaluokissa (FIN ja Ops to PSA) -mallin.</span><span class="sxs-lookup"><span data-stu-id="b9d7b-149">Click the arrow to open the mapping of the project expense categories task in the Project expense transaction categories (Fin and Ops to PSA) template.</span></span>
2. <span data-ttu-id="b9d7b-150">Napsauta **Tarkka kysely ja suodatus** -linkki avataksesi Power Queryn.</span><span class="sxs-lookup"><span data-stu-id="b9d7b-150">Click the **Advance Query and Filtering** link to open Power Query.</span></span>
2. <span data-ttu-id="b9d7b-151">Valitse **Lisää ehdollinen sarake**.</span><span class="sxs-lookup"><span data-stu-id="b9d7b-151">Select **Add Conditional Column**.</span></span>
3. <span data-ttu-id="b9d7b-152">Syötä uudelle sarakkeelle nimi, kuten **Laskutustyyppi**.</span><span class="sxs-lookup"><span data-stu-id="b9d7b-152">Enter a name for the new column, such as **BillingType**.</span></span>
4. <span data-ttu-id="b9d7b-153">Kirjoita seuraava ehto: **if CATEGORYID not equal to null then 19235001, Otherwise null**.</span><span class="sxs-lookup"><span data-stu-id="b9d7b-153">Enter the following condition: **if CATEGORYID not equal to null then 19235001, Otherwise null**.</span></span>
5. <span data-ttu-id="b9d7b-154">Valitse **OK** sarakkeessa.</span><span class="sxs-lookup"><span data-stu-id="b9d7b-154">Click **OK** on the column.</span></span>
6. <span data-ttu-id="b9d7b-155">Varmista, että yhdistät tämän uuden sarakkeen yhdistämissivulle.</span><span class="sxs-lookup"><span data-stu-id="b9d7b-155">Be sure to map this new column on the mapping page.</span></span>

<span data-ttu-id="b9d7b-156">Seuraavassa kuvissa on esimerkki mallitehtävien yhdistämismäärityksissä tietojen integroinnissa.</span><span class="sxs-lookup"><span data-stu-id="b9d7b-156">The following illustration shows an example of the template task mapping in Data integration.</span></span> <span data-ttu-id="b9d7b-157">Yhdistämismäärityksessä näytetään kenttätiedot, jotka synkronoidaan Financesta Project Service Automationiin.</span><span class="sxs-lookup"><span data-stu-id="b9d7b-157">The mapping shows the field information that will be synchronized from Finance to Project Service Automation.</span></span>

<span data-ttu-id="b9d7b-158">[![Yhdistelmämääritysmalli](./media/ProjectExpenseCategoriesToPSAMapping.jpg)](./media/ProjectExpenseCategoriesToPSAMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="b9d7b-158">[![Template mapping](./media/ProjectExpenseCategoriesToPSAMapping.jpg)](./media/ProjectExpenseCategoriesToPSAMapping.jpg)</span></span>

## <a name="project-expense-category-synchronization-from-project-service-automation-to-finance"></a><span data-ttu-id="b9d7b-159">Projektikululuokkien synkronointi Project Service Automationista Financeen</span><span class="sxs-lookup"><span data-stu-id="b9d7b-159">Project expense category synchronization from Project Service Automation to Finance</span></span>

### <a name="template-and-task"></a><span data-ttu-id="b9d7b-160">Malli ja tehtävä</span><span class="sxs-lookup"><span data-stu-id="b9d7b-160">Template and task</span></span>

<span data-ttu-id="b9d7b-161">Seuraavaa mallia ja pohjana olevaa tehtävää käytetään projektien kululuokkien synkronoimiseen Project Service Automationista Financeen:</span><span class="sxs-lookup"><span data-stu-id="b9d7b-161">The following template and underlying task are used to synchronize project expense categories from Project Service Automation to Finance:</span></span>

- <span data-ttu-id="b9d7b-162">**Tietojen integrointimallin nimi:** Projektin kuluarviotapahtumien luokat (PSA to Fin and Ops)</span><span class="sxs-lookup"><span data-stu-id="b9d7b-162">**Name of the template in Data integration:** Project expense transaction categories (PSA to Fin and Ops)</span></span>
- <span data-ttu-id="b9d7b-163">**Projektin tehtävän nimi:** Synkronoi luokat Fin Ops -järjestelmään</span><span class="sxs-lookup"><span data-stu-id="b9d7b-163">**Name of the task in the project:** Sync categories to Fin Ops</span></span>

### <a name="entity-set"></a><span data-ttu-id="b9d7b-164">Entiteettijoukko</span><span class="sxs-lookup"><span data-stu-id="b9d7b-164">Entity set</span></span>

| <span data-ttu-id="b9d7b-165">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="b9d7b-165">Project Service Automation</span></span> | <span data-ttu-id="b9d7b-166">Rahoitus</span><span class="sxs-lookup"><span data-stu-id="b9d7b-166">Finance</span></span>                           |
|----------------------------|-----------------------------------|
| <span data-ttu-id="b9d7b-167">Tapahtumaluokat</span><span class="sxs-lookup"><span data-stu-id="b9d7b-167">Transaction categories</span></span>     | <span data-ttu-id="b9d7b-168">Luokkien integroinnin entiteetti</span><span class="sxs-lookup"><span data-stu-id="b9d7b-168">Integration entity for categories</span></span> |

### <a name="entity-flow"></a><span data-ttu-id="b9d7b-169">Entiteettivuo</span><span class="sxs-lookup"><span data-stu-id="b9d7b-169">Entity flow</span></span>

<span data-ttu-id="b9d7b-170">Projektien kululuokkia hallitaan Financessa ja ne synkronoidaan Project Service Automationiin tapahtumaluokkina.</span><span class="sxs-lookup"><span data-stu-id="b9d7b-170">Project expense categories are managed in Finance, and they are synchronized to Project Service Automation as transaction categories.</span></span> <span data-ttu-id="b9d7b-171">Synkronointi takaisin Financeen päivittää Finance-projektiluokan Project Service Automationin integraatiotunnuksella.</span><span class="sxs-lookup"><span data-stu-id="b9d7b-171">The synchronization back to Finance updates the project category in Finance with the integration ID from Project Service Automation.</span></span>

### <a name="template-mapping-in-data-integration"></a><span data-ttu-id="b9d7b-172">Mallien yhdistämismääritys tietojen integroinnissa</span><span class="sxs-lookup"><span data-stu-id="b9d7b-172">Template mapping in Data integration</span></span>

<span data-ttu-id="b9d7b-173">Seuraavassa kuvissa on esimerkki mallitehtävien yhdistämismäärityksissä tietojen integroinnissa.</span><span class="sxs-lookup"><span data-stu-id="b9d7b-173">The following illustration shows an example of the template task mapping in Data integration.</span></span>

> [!NOTE]
> <span data-ttu-id="b9d7b-174">Yhdistämismäärityksessä näytetään kenttätiedot, jotka synkronoidaan Project Service Automationista Financeen.</span><span class="sxs-lookup"><span data-stu-id="b9d7b-174">The mapping shows the field information that will be synchronized from Project Service Automation to Finance.</span></span>

<span data-ttu-id="b9d7b-175">[![Yhdistelmämääritysmalli](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="b9d7b-175">[![Template mapping](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)</span></span>
