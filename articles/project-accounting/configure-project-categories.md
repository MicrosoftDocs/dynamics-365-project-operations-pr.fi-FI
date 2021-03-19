---
title: Projektiluokkien määrittäminen
description: Tässä aiheessa on tietoja projektiluokkien määrityksestä.
author: sigitac
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: b7adf61a82714a0148d9c8b1d2b2b37fd611c1cf
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5287504"
---
# <a name="configure-project-categories"></a><span data-ttu-id="770cf-103">Projektiluokkien määrittäminen</span><span class="sxs-lookup"><span data-stu-id="770cf-103">Configure project categories</span></span>

<span data-ttu-id="770cf-104">_**Käytetään:** Project Operationsin resursseihin ja ei-varastoitaviin perustuvissa skenaarioissa_</span><span class="sxs-lookup"><span data-stu-id="770cf-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="770cf-105">Project Operations tarjoaa tehokkaat ominaisuudet tuottojen ja kulujen luokittelemiseen projekteissa.</span><span class="sxs-lookup"><span data-stu-id="770cf-105">Project Operations offers robust capabilities for categorizing revenue and expenses on projects.</span></span> <span data-ttu-id="770cf-106">Luokat antavat mahdollisuuden raportoida ja analysoida projektitapahtumia sekä edistää kirjauksia pääkirjanpitoon.</span><span class="sxs-lookup"><span data-stu-id="770cf-106">Categories provide the ability to report on and analyze project transactions, and drive posting to the general ledger.</span></span>

<span data-ttu-id="770cf-107">Seuraavassa kaaviossa on kuvattu tapahtumaluokkien, jaettujen luokkien ja projektiluokkien väliset vastaavuudet.</span><span class="sxs-lookup"><span data-stu-id="770cf-107">The following diagram illustrates the correlation between transaction categories, shared categories, and project categories.</span></span> 

<span data-ttu-id="770cf-108">Tapahtumaluokat ovat projektitapahtumien perusryhmittely.</span><span class="sxs-lookup"><span data-stu-id="770cf-108">Transaction categories are the basic grouping for project transactions.</span></span> <span data-ttu-id="770cf-109">Kyseisessä ryhmittelyssä on joukko jaettuja luokkia, jotka voidaan jakaa eri sovelluksissa ja moduuleissa.</span><span class="sxs-lookup"><span data-stu-id="770cf-109">Within that grouping, there is a set of shared categories that can be shared across applications and modules.</span></span> <span data-ttu-id="770cf-110">Tarkemmalla tasolla projektiluokat ovat kaikkein täsmällisimpiä luokkia.</span><span class="sxs-lookup"><span data-stu-id="770cf-110">Getting even further into specifics, project categories are the most granular level of categories.</span></span> <span data-ttu-id="770cf-111">Projektiluokat ovat yritys-, moduuli- ja sovelluskohtaisia.</span><span class="sxs-lookup"><span data-stu-id="770cf-111">Project categories are specific to legal entity, module, and application.</span></span>

![Tapahtumaluokkien, jaettujen luokkien ja projektiluokkien väliset vastaavuudet](media/project-categories.png)

## <a name="transaction-categories"></a><span data-ttu-id="770cf-113">Tapahtumaluokat</span><span class="sxs-lookup"><span data-stu-id="770cf-113">Transaction categories</span></span>

<span data-ttu-id="770cf-114">Tapahtumaluokat edustavat projektitapahtumien perusryhmittelyä, eivätkä ne ole yritys- tai tapahtumakohtaisia.</span><span class="sxs-lookup"><span data-stu-id="770cf-114">Transaction categories represent the basic grouping for project transactions and are not company or transaction type-specific.</span></span> <span data-ttu-id="770cf-115">Contoso Robotics käyttää esimerkiksi Suunnittelu-, Matka-, Asennus- ja Palvelu -tapahtumaluokkia projektitapahtumien ryhmittelyssä.</span><span class="sxs-lookup"><span data-stu-id="770cf-115">For example, Contoso Robotics uses Design, Travel, Installation, and Service Transaction categories to group Project transactions.</span></span>

<span data-ttu-id="770cf-116">Tapahtumaluokat määritetään Project Operations -moduulissa.</span><span class="sxs-lookup"><span data-stu-id="770cf-116">Transaction categories are defined in the Project Operations module.</span></span> 
1. <span data-ttu-id="770cf-117">Avaa lomake siirtymällä kohtaan **Asetukset** \>**Tapahtumaluokat**.</span><span class="sxs-lookup"><span data-stu-id="770cf-117">Go to **Settings** \> **Transaction Categories** to open the form.</span></span> 
2. <span data-ttu-id="770cf-118">Voit luoda uuden tapahtumaluokan joko valitsemalla **Uusi** tai valitsemalla **Tuo Excelistä**.</span><span class="sxs-lookup"><span data-stu-id="770cf-118">Create a new transaction category either by selecting **New** or by selecting **Import from Excel**.</span></span>

## <a name="shared-categories"></a><span data-ttu-id="770cf-119">Jaetut luokat</span><span class="sxs-lookup"><span data-stu-id="770cf-119">Shared categories</span></span>

<span data-ttu-id="770cf-120">Dynamics 365 luokittelee kulut eri sovelluksissa, kuten Dynamics 365 Financessa, Dynamics 365 Supply Chainissa ja Dynamics 365 Project Operationsissa, käyttämällä Jaetut luokat -käsitettä.</span><span class="sxs-lookup"><span data-stu-id="770cf-120">Dynamics 365 uses the Shared categories concept to categorize expenses in different applications, such as Dynamics 365 Finance, Dynamics 365 Supply Chain, and Dynamics 365 Project Operations.</span></span> <span data-ttu-id="770cf-121">Kullekin luodulle tapahtumaluokalle Project Operations luo automaattisesti neljä toisiinsa liittyvää jaettua luokkaa: Tunnit, Kulut, Maksut ja Nimike.</span><span class="sxs-lookup"><span data-stu-id="770cf-121">For each Transaction category created, Project Operations automatically creates four related Shared categories: Hours, Expense, Fees, and Item.</span></span> <span data-ttu-id="770cf-122">Voit tarkastella ja muokata jaettuja luokkia siirtymällä kohtaan **Projektinhallinta ja kirjanpito** \> **Asetukset** \> **Luokat** \> **Jaetut luokat**.</span><span class="sxs-lookup"><span data-stu-id="770cf-122">You can review and adjust the shared categories by going to **Project management and accounting** \> **Setup** \> **Categories** \> **Shared Categories**.</span></span>

## <a name="project-categories"></a><span data-ttu-id="770cf-123">Projektiluokat</span><span class="sxs-lookup"><span data-stu-id="770cf-123">Project categories</span></span>

<span data-ttu-id="770cf-124">Projektiluokat edustavat kaikkein tarkimpia luokkamäärityksiä, ja projektin kirjanpitäjän täytyy määrittää ne erikseen ja kullekin yritykselle.</span><span class="sxs-lookup"><span data-stu-id="770cf-124">Project categories represent most granular level of category configuration and must be configured separately, and for each company, by a Project accountant.</span></span>

1. <span data-ttu-id="770cf-125">Siirry kohtaan **Projektinhallinta ja kirjanpito** \> **Asetukset** \> **Luokat** \> **Projektiluokat**.</span><span class="sxs-lookup"><span data-stu-id="770cf-125">Go to **Project Management and Accounting** \> **Setup** \> **Categories** \> **Project categories**.</span></span>
2. <span data-ttu-id="770cf-126">Valitse **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="770cf-126">Select **New**.</span></span>
3. <span data-ttu-id="770cf-127">Valitse edellisessä osassa luodun jaetun luokan **Luokan tunnus**.</span><span class="sxs-lookup"><span data-stu-id="770cf-127">Select the **Category ID** of the Shared category you created in the previous section.</span></span> <span data-ttu-id="770cf-128">Project Operationsin avulla voi käyttää vain niitä jaettuja luokkia, jotka liittyvät tapahtumaluokkiin.</span><span class="sxs-lookup"><span data-stu-id="770cf-128">Project Operations allows using only those shared categories that are associated with transaction categories.</span></span>
4. <span data-ttu-id="770cf-129">Valitse luokan ryhmä.</span><span class="sxs-lookup"><span data-stu-id="770cf-129">Select a category group.</span></span>

## <a name="category-groups"></a><span data-ttu-id="770cf-130">Luokaryhmät</span><span class="sxs-lookup"><span data-stu-id="770cf-130">Category groups</span></span>

<span data-ttu-id="770cf-131">Luokkayhmien avulla voidaan jakaa ominaisuuksia, ensisijaisesti kirjausprofiileja, toisiinsa liittyvien projektiluokkien välillä.</span><span class="sxs-lookup"><span data-stu-id="770cf-131">Category groups are used to share properties, primarily posting profiles, between related Project categories.</span></span> <span data-ttu-id="770cf-132">Kullakin tapahtumatyypillä on oltava vähintään yksi luokkaryhmä, ja kullekin projektiluokalle on määritetty ryhmä.</span><span class="sxs-lookup"><span data-stu-id="770cf-132">There must be at least one category group for each transaction type and each project category is assigned a group.</span></span>

<span data-ttu-id="770cf-133">Project Operationsin kirjausmääritykset määräytyvät projektin kustannus- ja tuottoprofiilin sääntöjen, projektiluokkien ja luokkaryhmien mukaan.</span><span class="sxs-lookup"><span data-stu-id="770cf-133">The posting specifications in Project Operations are defined by the project cost and revenue profile rules, project categories, and category groups.</span></span> <span data-ttu-id="770cf-134">Voit määrittää luokkaryhmiä siirtymällä kohtaan **Projektinhallinta ja kirjanpito** \> **Asetukset** \> **Luokat** \> **Luokkaryhmät**.</span><span class="sxs-lookup"><span data-stu-id="770cf-134">You can set up category groups by going to **Project management and accounting** \> **Setup** \> **Categories** \> **Category groups**.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]