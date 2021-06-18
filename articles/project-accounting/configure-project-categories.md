---
title: Projektiluokkien määrittäminen
description: Tässä aiheessa on tietoja projektiluokkien määrityksestä.
author: sigitac
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: d82302f12ba75a92f2de0e9746ad7e61ce0cdc6b
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/10/2021
ms.locfileid: "5995167"
---
# <a name="configure-project-categories"></a><span data-ttu-id="60f28-103">Projektiluokkien määrittäminen</span><span class="sxs-lookup"><span data-stu-id="60f28-103">Configure project categories</span></span>

<span data-ttu-id="60f28-104">_**Käytetään:** Project Operationsin resursseihin ja ei-varastoitaviin perustuvissa skenaarioissa_</span><span class="sxs-lookup"><span data-stu-id="60f28-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="60f28-105">Project Operations tarjoaa tehokkaat ominaisuudet tuottojen ja kulujen luokittelemiseen projekteissa.</span><span class="sxs-lookup"><span data-stu-id="60f28-105">Project Operations offers robust capabilities for categorizing revenue and expenses on projects.</span></span> <span data-ttu-id="60f28-106">Luokat antavat mahdollisuuden raportoida ja analysoida projektitapahtumia sekä edistää kirjauksia pääkirjanpitoon.</span><span class="sxs-lookup"><span data-stu-id="60f28-106">Categories provide the ability to report on and analyze project transactions, and drive posting to the general ledger.</span></span>

<span data-ttu-id="60f28-107">Seuraavassa kaaviossa on kuvattu tapahtumaluokkien, jaettujen luokkien ja projektiluokkien väliset vastaavuudet.</span><span class="sxs-lookup"><span data-stu-id="60f28-107">The following diagram illustrates the correlation between transaction categories, shared categories, and project categories.</span></span> 

<span data-ttu-id="60f28-108">Tapahtumaluokat ovat projektitapahtumien perusryhmittely.</span><span class="sxs-lookup"><span data-stu-id="60f28-108">Transaction categories are the basic grouping for project transactions.</span></span> <span data-ttu-id="60f28-109">Kyseisessä ryhmittelyssä on joukko jaettuja luokkia, jotka voidaan jakaa eri sovelluksissa ja moduuleissa.</span><span class="sxs-lookup"><span data-stu-id="60f28-109">Within that grouping, there is a set of shared categories that can be shared across applications and modules.</span></span> <span data-ttu-id="60f28-110">Tarkemmalla tasolla projektiluokat ovat kaikkein täsmällisimpiä luokkia.</span><span class="sxs-lookup"><span data-stu-id="60f28-110">Getting even further into specifics, project categories are the most granular level of categories.</span></span> <span data-ttu-id="60f28-111">Projektiluokat ovat yritys-, moduuli- ja sovelluskohtaisia.</span><span class="sxs-lookup"><span data-stu-id="60f28-111">Project categories are specific to legal entity, module, and application.</span></span>

![Tapahtumaluokkien, jaettujen luokkien ja projektiluokkien väliset vastaavuudet](media/project-categories.png)

## <a name="transaction-categories"></a><span data-ttu-id="60f28-113">Tapahtumaluokat</span><span class="sxs-lookup"><span data-stu-id="60f28-113">Transaction categories</span></span>

<span data-ttu-id="60f28-114">Tapahtumaluokat edustavat projektitapahtumien perusryhmittelyä, eivätkä ne ole yritys- tai tapahtumakohtaisia.</span><span class="sxs-lookup"><span data-stu-id="60f28-114">Transaction categories represent the basic grouping for project transactions and are not company or transaction type-specific.</span></span> <span data-ttu-id="60f28-115">Esimerkiksi Contoso Robotics käyttää Design-, Matkustaminen-, Asennus- ja Palvelutapahtuma-luokkia projektitapahtumien ryhmittelemiseen.</span><span class="sxs-lookup"><span data-stu-id="60f28-115">For example, Contoso Robotics uses Design, Travel, Installation, and Service Transaction categories to group Project transactions.</span></span>

<span data-ttu-id="60f28-116">Tapahtumaluokat määritetään Project Operations -moduulissa.</span><span class="sxs-lookup"><span data-stu-id="60f28-116">Transaction categories are defined in the Project Operations module.</span></span> 
1. <span data-ttu-id="60f28-117">Avaa lomake siirtymällä kohtaan **Asetukset** \>**Tapahtumaluokat**.</span><span class="sxs-lookup"><span data-stu-id="60f28-117">Go to **Settings** \> **Transaction Categories** to open the form.</span></span> 
2. <span data-ttu-id="60f28-118">Voit luoda uuden tapahtumaluokan joko valitsemalla **Uusi** tai valitsemalla **Tuo Excelistä**.</span><span class="sxs-lookup"><span data-stu-id="60f28-118">Create a new transaction category either by selecting **New** or by selecting **Import from Excel**.</span></span>

## <a name="shared-categories"></a><span data-ttu-id="60f28-119">Jaetut luokat</span><span class="sxs-lookup"><span data-stu-id="60f28-119">Shared categories</span></span>

<span data-ttu-id="60f28-120">Dynamics 365 luokittelee kulut eri sovelluksissa, kuten Dynamics 365 Financessa, Dynamics 365 Supply Chainissa ja Dynamics 365 Project Operationsissa, käyttämällä Jaetut luokat -käsitettä.</span><span class="sxs-lookup"><span data-stu-id="60f28-120">Dynamics 365 uses the Shared categories concept to categorize expenses in different applications, such as Dynamics 365 Finance, Dynamics 365 Supply Chain, and Dynamics 365 Project Operations.</span></span> <span data-ttu-id="60f28-121">Kullekin luodulle tapahtumaluokalle Project Operations luo automaattisesti neljä toisiinsa liittyvää jaettua luokkaa: Tunnit, Kulut, Maksut ja Nimike.</span><span class="sxs-lookup"><span data-stu-id="60f28-121">For each Transaction category created, Project Operations automatically creates four related Shared categories: Hours, Expense, Fees, and Item.</span></span> <span data-ttu-id="60f28-122">Voit tarkastella ja muokata jaettuja luokkia siirtymällä kohtaan **Projektinhallinta ja kirjanpito** \> **Asetukset** \> **Luokat** \> **Jaetut luokat**.</span><span class="sxs-lookup"><span data-stu-id="60f28-122">You can review and adjust the shared categories by going to **Project management and accounting** \> **Setup** \> **Categories** \> **Shared Categories**.</span></span>

## <a name="project-categories"></a><span data-ttu-id="60f28-123">Projektiluokat</span><span class="sxs-lookup"><span data-stu-id="60f28-123">Project categories</span></span>

<span data-ttu-id="60f28-124">Projektiluokat edustavat kaikkein tarkimpia luokkamäärityksiä, ja projektin kirjanpitäjän täytyy määrittää ne erikseen ja kullekin yritykselle.</span><span class="sxs-lookup"><span data-stu-id="60f28-124">Project categories represent most granular level of category configuration and must be configured separately, and for each company, by a Project accountant.</span></span>

1. <span data-ttu-id="60f28-125">Siirry kohtaan **Projektinhallinta ja kirjanpito** \> **Asetukset** \> **Luokat** \> **Projektiluokat**.</span><span class="sxs-lookup"><span data-stu-id="60f28-125">Go to **Project Management and Accounting** \> **Setup** \> **Categories** \> **Project categories**.</span></span>
2. <span data-ttu-id="60f28-126">Valitse **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="60f28-126">Select **New**.</span></span>
3. <span data-ttu-id="60f28-127">Valitse edellisessä osassa luodun jaetun luokan **Luokan tunnus**.</span><span class="sxs-lookup"><span data-stu-id="60f28-127">Select the **Category ID** of the Shared category you created in the previous section.</span></span> <span data-ttu-id="60f28-128">Project Operationsin avulla voi käyttää vain niitä jaettuja luokkia, jotka liittyvät tapahtumaluokkiin.</span><span class="sxs-lookup"><span data-stu-id="60f28-128">Project Operations allows using only those shared categories that are associated with transaction categories.</span></span>
4. <span data-ttu-id="60f28-129">Valitse luokan ryhmä.</span><span class="sxs-lookup"><span data-stu-id="60f28-129">Select a category group.</span></span>

## <a name="category-groups"></a><span data-ttu-id="60f28-130">Luokaryhmät</span><span class="sxs-lookup"><span data-stu-id="60f28-130">Category groups</span></span>

<span data-ttu-id="60f28-131">Luokkayhmien avulla voidaan jakaa ominaisuuksia, ensisijaisesti kirjausprofiileja, toisiinsa liittyvien projektiluokkien välillä.</span><span class="sxs-lookup"><span data-stu-id="60f28-131">Category groups are used to share properties, primarily posting profiles, between related Project categories.</span></span> <span data-ttu-id="60f28-132">Kullakin tapahtumatyypillä on oltava vähintään yksi luokkaryhmä, ja kullekin projektiluokalle on määritetty ryhmä.</span><span class="sxs-lookup"><span data-stu-id="60f28-132">There must be at least one category group for each transaction type and each project category is assigned a group.</span></span>

<span data-ttu-id="60f28-133">Project Operationsin kirjausmääritykset määräytyvät projektin kustannus- ja tuottoprofiilin sääntöjen, projektiluokkien ja luokkaryhmien mukaan.</span><span class="sxs-lookup"><span data-stu-id="60f28-133">The posting specifications in Project Operations are defined by the project cost and revenue profile rules, project categories, and category groups.</span></span> <span data-ttu-id="60f28-134">Voit määrittää luokkaryhmiä siirtymällä kohtaan **Projektinhallinta ja kirjanpito** \> **Asetukset** \> **Luokat** \> **Luokkaryhmät**.</span><span class="sxs-lookup"><span data-stu-id="60f28-134">You can set up category groups by going to **Project management and accounting** \> **Setup** \> **Categories** \> **Category groups**.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]