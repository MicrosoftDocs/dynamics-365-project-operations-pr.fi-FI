---
title: Projektiluokkien määrittäminen
description: Tässä aiheessa on tietoja projektiluokkien määrityksestä.
author: sigitac
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 84033182ce047d230724409eef9bc6afcaefd2b4
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/28/2020
ms.locfileid: "3895962"
---
# <a name="configure-project-categories"></a><span data-ttu-id="f010b-103">Projektiluokkien määrittäminen</span><span class="sxs-lookup"><span data-stu-id="f010b-103">Configure project categories</span></span>

<span data-ttu-id="f010b-104">_**Käytetään:** Project Operationsin resursseihin ja ei-varastoitaviin perustuvissa skenaarioissa_</span><span class="sxs-lookup"><span data-stu-id="f010b-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="f010b-105">Project Operations tarjoaa tehokkaat ominaisuudet tuottojen ja kulujen luokittelemiseen projekteissa.</span><span class="sxs-lookup"><span data-stu-id="f010b-105">Project Operations offers robust capabilities for categorizing revenue and expenses on projects.</span></span> <span data-ttu-id="f010b-106">Luokat antavat mahdollisuuden raportoida ja analysoida projektitapahtumia sekä edistää kirjauksia pääkirjanpitoon.</span><span class="sxs-lookup"><span data-stu-id="f010b-106">Categories provide the ability to report on and analyze project transactions, and drive posting to the general ledger.</span></span>

<span data-ttu-id="f010b-107">Seuraavassa kaaviossa on kuvattu tapahtumaluokkien, jaettujen luokkien ja projektiluokkien väliset vastaavuudet.</span><span class="sxs-lookup"><span data-stu-id="f010b-107">The following diagram illustrates the correlation between transaction categories, shared categories, and project categories.</span></span> 

<span data-ttu-id="f010b-108">Tapahtumaluokat ovat projektitapahtumien perusryhmittely.</span><span class="sxs-lookup"><span data-stu-id="f010b-108">Transaction categories are the basic grouping for project transactions.</span></span> <span data-ttu-id="f010b-109">Kyseisessä ryhmittelyssä on joukko jaettuja luokkia, jotka voidaan jakaa eri sovelluksissa ja moduuleissa.</span><span class="sxs-lookup"><span data-stu-id="f010b-109">Within that grouping, there is a set of shared categories that can be shared across applications and modules.</span></span> <span data-ttu-id="f010b-110">Tarkemmalla tasolla projektiluokat ovat kaikkein täsmällisimpiä luokkia.</span><span class="sxs-lookup"><span data-stu-id="f010b-110">Getting even further into specifics, project categories are the most granular level of categories.</span></span> <span data-ttu-id="f010b-111">Projektiluokat ovat yritys-, moduuli- ja sovelluskohtaisia.</span><span class="sxs-lookup"><span data-stu-id="f010b-111">Project categories are specific to legal entity, module, and application.</span></span>

![Tapahtumaluokkien, jaettujen luokkien ja projektiluokkien väliset vastaavuudet](media/project-categories.png)

## <a name="transaction-categories"></a><span data-ttu-id="f010b-113">Tapahtumaluokat</span><span class="sxs-lookup"><span data-stu-id="f010b-113">Transaction categories</span></span>

<span data-ttu-id="f010b-114">Tapahtumaluokat edustavat projektitapahtumien perusryhmittelyä, eivätkä ne ole yritys- tai tapahtumakohtaisia.</span><span class="sxs-lookup"><span data-stu-id="f010b-114">Transaction categories represent the basic grouping for project transactions and are not company or transaction type-specific.</span></span> <span data-ttu-id="f010b-115">Contoso Robotics käyttää esimerkiksi Suunnittelu-, Matka-, Asennus- ja Palvelu -tapahtumaluokkia projektitapahtumien ryhmittelyssä.</span><span class="sxs-lookup"><span data-stu-id="f010b-115">For example, Contoso Robotics uses Design, Travel, Installation, and Service Transaction categories to group Project transactions.</span></span>

<span data-ttu-id="f010b-116">Tapahtumaluokat määritetään Project Operations -moduulissa.</span><span class="sxs-lookup"><span data-stu-id="f010b-116">Transaction categories are defined in the Project Operations module.</span></span> 
1. <span data-ttu-id="f010b-117">Avaa lomake siirtymällä kohtaan **Asetukset** \>**Tapahtumaluokat**.</span><span class="sxs-lookup"><span data-stu-id="f010b-117">Go to **Settings** \> **Transaction Categories** to open the form.</span></span> 
2. <span data-ttu-id="f010b-118">Voit luoda uuden tapahtumaluokan joko valitsemalla **Uusi** tai valitsemalla **Tuo Excelistä**.</span><span class="sxs-lookup"><span data-stu-id="f010b-118">Create a new transaction category either by selecting **New** or by selecting **Import from Excel**.</span></span>

## <a name="shared-categories"></a><span data-ttu-id="f010b-119">Jaetut luokat</span><span class="sxs-lookup"><span data-stu-id="f010b-119">Shared categories</span></span>

<span data-ttu-id="f010b-120">Dynamics 365 käyttää jaettujen luokkien käsitettä kulujen luokittelemiseen eri sovelluksissa, kuten Dynamics 365 Finance, Dynamics 365 Supply Chain ja Dynamics 365 Project Operations.</span><span class="sxs-lookup"><span data-stu-id="f010b-120">Dynamics 365 uses the Shared categories concept to categorize expenses in different applications, such as Dynamics 365 Finance, Dynamics 365 Supply Chain, and Dynamics 365 Project Operations.</span></span> <span data-ttu-id="f010b-121">Kullekin luodulle tapahtumaluokalle Project Operations luo automaattisesti neljä toisiinsa liittyvää jaettua luokkaa: Tunnit, Kulut, Maksut ja Nimike.</span><span class="sxs-lookup"><span data-stu-id="f010b-121">For each Transaction category created, Project Operations automatically creates four related Shared categories: Hours, Expense, Fees, and Item.</span></span> <span data-ttu-id="f010b-122">Voit tarkastella ja muokata jaettuja luokkia siirtymällä kohtaan **Projektinhallinta ja kirjanpito** \> **Asetukset** \> **Luokat** \> **Jaetut luokat**.</span><span class="sxs-lookup"><span data-stu-id="f010b-122">You can review and adjust the shared categories by going to **Project management and accounting** \> **Setup** \> **Categories** \> **Shared Categories**.</span></span>

## <a name="project-categories"></a><span data-ttu-id="f010b-123">Projektiluokat</span><span class="sxs-lookup"><span data-stu-id="f010b-123">Project categories</span></span>

<span data-ttu-id="f010b-124">Projektiluokat edustavat kaikkein tarkimpia luokkamäärityksiä, ja projektin kirjanpitäjän täytyy määrittää ne erikseen ja kullekin yritykselle.</span><span class="sxs-lookup"><span data-stu-id="f010b-124">Project categories represent most granular level of category configuration and must be configured separately, and for each company, by a Project accountant.</span></span>

1. <span data-ttu-id="f010b-125">Siirry kohtaan **Projektinhallinta ja kirjanpito** \> **Asetukset** \> **Luokat** \> **Projektiluokat**.</span><span class="sxs-lookup"><span data-stu-id="f010b-125">Go to **Project Management and Accounting** \> **Setup** \> **Categories** \> **Project categories**.</span></span>
2. <span data-ttu-id="f010b-126">Valitse **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="f010b-126">Select **New**.</span></span>
3. <span data-ttu-id="f010b-127">Valitse edellisessä osassa luodun jaetun luokan **Luokan tunnus**.</span><span class="sxs-lookup"><span data-stu-id="f010b-127">Select the **Category ID** of the Shared category you created in the previous section.</span></span> <span data-ttu-id="f010b-128">Project Operationsin avulla voi käyttää vain niitä jaettuja luokkia, jotka liittyvät tapahtumaluokkiin.</span><span class="sxs-lookup"><span data-stu-id="f010b-128">Project Operations allows using only those shared categories that are associated with transaction categories.</span></span>
4. <span data-ttu-id="f010b-129">Valitse luokan ryhmä.</span><span class="sxs-lookup"><span data-stu-id="f010b-129">Select a category group.</span></span>

## <a name="category-groups"></a><span data-ttu-id="f010b-130">Luokaryhmät</span><span class="sxs-lookup"><span data-stu-id="f010b-130">Category groups</span></span>

<span data-ttu-id="f010b-131">Luokkayhmien avulla voidaan jakaa ominaisuuksia, ensisijaisesti kirjausprofiileja, toisiinsa liittyvien projektiluokkien välillä.</span><span class="sxs-lookup"><span data-stu-id="f010b-131">Category groups are used to share properties, primarily posting profiles, between related Project categories.</span></span> <span data-ttu-id="f010b-132">Kullakin tapahtumatyypillä on oltava vähintään yksi luokkaryhmä, ja kullekin projektiluokalle on määritetty ryhmä.</span><span class="sxs-lookup"><span data-stu-id="f010b-132">There must be at least one category group for each transaction type and each project category is assigned a group.</span></span>

<span data-ttu-id="f010b-133">Project Operationsin kirjausmääritykset määräytyvät projektin kustannus- ja tuottoprofiilin sääntöjen, projektiluokkien ja luokkaryhmien mukaan.</span><span class="sxs-lookup"><span data-stu-id="f010b-133">The posting specifications in Project Operations are defined by the project cost and revenue profile rules, project categories, and category groups.</span></span> <span data-ttu-id="f010b-134">Voit määrittää luokkaryhmiä siirtymällä kohtaan **Projektinhallinta ja kirjanpito** \> **Asetukset** \> **Luokat** \> **Luokkaryhmät**.</span><span class="sxs-lookup"><span data-stu-id="f010b-134">You can set up category groups by going to **Project management and accounting** \> **Setup** \> **Categories** \> **Category groups**.</span></span>
