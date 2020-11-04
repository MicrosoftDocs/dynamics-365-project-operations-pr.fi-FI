---
title: Käyttöönottotyypin määritys
description: Tässä aiheessa on tietoja Project Operationsin oikean käyttöönottotyypin valinnasta omalle yrityksellesi.
author: stsporen
manager: Annbe
ms.date: 10/07/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 564f2878553fe3904a7c47c7e80a3b57c763a3b2
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/16/2020
ms.locfileid: "4075352"
---
# <a name="determine-your-deployment-type"></a><span data-ttu-id="4f311-103">Käyttöönottotyypin määritys</span><span class="sxs-lookup"><span data-stu-id="4f311-103">Determine your deployment type</span></span>

<span data-ttu-id="4f311-104">_**Koskee:** Project Operationsin resurssiin / muuhun kuin resurssiin perustuvia skenaarioita, Lite-käyttöönotto-kaupasta proformalaskutukseen_</span><span class="sxs-lookup"><span data-stu-id="4f311-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

> [!IMPORTANT]
> <span data-ttu-id="4f311-105">Kun olet ostanut käyttöoikeuden, voit määrittää Dynamics 365 Project Operationsin parhaan asennusmallin [ohjatun asennusvuon avulla](https://aka.ms/provisionprojectoperations).</span><span class="sxs-lookup"><span data-stu-id="4f311-105">After you purchase the license, start here to determine the best deployment model of Dynamics 365 Project Operations using the [Guided installation flow](https://aka.ms/provisionprojectoperations).</span></span>
> <span data-ttu-id="4f311-106">Kun olet tehnyt ohjatun asennusvuon, sinut ohjataan oikeaan hallintaportaaliin, jotta asennus viimeistellään.</span><span class="sxs-lookup"><span data-stu-id="4f311-106">After you have finshed the Guided installation flow, you will be directed to the correct management portal to complete your installation.</span></span> <span data-ttu-id="4f311-107">Katso asennuksen viimeistelemisen tiedot.</span><span class="sxs-lookup"><span data-stu-id="4f311-107">See the deployment details to complete the installation.</span></span>


## <a name="existing-customers-of-dynamics-using-dynamics-365-project-service-automation"></a><span data-ttu-id="4f311-108">Olemassa olevat Dynamics-asiakkaat, jotka käyttvät Dynamics 365 Project Service Automationia</span><span class="sxs-lookup"><span data-stu-id="4f311-108">Existing customers of Dynamics using Dynamics 365 Project Service Automation</span></span>
<span data-ttu-id="4f311-109">Project Operations sisältää Project Service Automationin mukana toimitetut toiminnot.</span><span class="sxs-lookup"><span data-stu-id="4f311-109">Project Operations includes the capabilities that shipped with Project Service Automation.</span></span> <span data-ttu-id="4f311-110">Näille asiakkaille julkaistaan tulevaisuudessa päivityspolku.</span><span class="sxs-lookup"><span data-stu-id="4f311-110">An upgrade path will be released for these customers in the future.</span></span>

## <a name="existing-customers-of-dynamics-365-finance-using-project-management-and-accounting"></a><span data-ttu-id="4f311-111">Olemassa olevat Dynamics 365 Finance-asiakkaat, jotka käyttävät Projektinhallinta ja kirjanpito -moduulia</span><span class="sxs-lookup"><span data-stu-id="4f311-111">Existing customers of Dynamics 365 Finance using Project management and accounting</span></span> 

<span data-ttu-id="4f311-112">Finance-asiakkaat, jotka käyttävät Projektinhallinta- ja kirjanpito -toimintoa, voivat jatkaa käyttöä sellaisenaan.</span><span class="sxs-lookup"><span data-stu-id="4f311-112">Existing customers of Finance who use the Project management and accounting functionality can continue to use this as is.</span></span> <span data-ttu-id="4f311-113">Katso [Project Operations varastoitavien/tuotantotilausten skenaarioissa](#pma).</span><span class="sxs-lookup"><span data-stu-id="4f311-113">See [Project Operations for stocked/production order scenarios](#pma).</span></span>


## <a name="deployment-types"></a><span data-ttu-id="4f311-114">Käyttöönottotyypit</span><span class="sxs-lookup"><span data-stu-id="4f311-114">Deployment types</span></span>
<span data-ttu-id="4f311-115">Project Operations tukee useita eri toteutusvaihtoehtoja tarpeidesi mukaan.</span><span class="sxs-lookup"><span data-stu-id="4f311-115">Project Operations supports multiple deployment options to match your requirements.</span></span> <span data-ttu-id="4f311-116">Olitpa uusi tai nykyinen Dynamics 365 -asiakas, Project Operations voit tukea tarpeitasi.</span><span class="sxs-lookup"><span data-stu-id="4f311-116">Whether you're a new or existing Dynamics 365 customer, Project Operations can support your needs.</span></span>

<span data-ttu-id="4f311-117">[Käyttöönottokyselyn](https://aka.ms/provisionprojectoperations) avulla voit määrittää oikean käyttöönottotavan.</span><span class="sxs-lookup"><span data-stu-id="4f311-117">Our [Deployment questionnaire](https://aka.ms/provisionprojectoperations) will help you determine the right deployment.</span></span> <span data-ttu-id="4f311-118">Tulokset opastavat sinua kohti jotakin seuraavista käyttöönottotyypeistä:</span><span class="sxs-lookup"><span data-stu-id="4f311-118">The results will guide you toward one of the following deployment types:</span></span>

- [<span data-ttu-id="4f311-119">Lite-käyttöönotto – kauppa proformalaskutukseen</span><span class="sxs-lookup"><span data-stu-id="4f311-119">Lite deployment – deal to proforma invoicing</span></span>](#lite)
- [<span data-ttu-id="4f311-120">Project Operations resurssien ja ei-varastoitavien skenaarioissa</span><span class="sxs-lookup"><span data-stu-id="4f311-120">Project Operations for resource/non-stocked scenarios</span></span>](#integrated)
- [<span data-ttu-id="4f311-121">Project Operations varastoitavien/tuotantotilausten skenaarioissa</span><span class="sxs-lookup"><span data-stu-id="4f311-121">Project Operations for stocked/production order scenarios</span></span>](#pma)

<span data-ttu-id="4f311-122">Project Operations tukee varastoitu/tuotantotilaus-skenaarioita ja ei-varastoitavia/resurssipohjaisia skenaarioita samassa ympäristössä yritystason määritysten avulla.</span><span class="sxs-lookup"><span data-stu-id="4f311-122">Project Operations support stocked/production order scenarios and non-stocked/resource-based scenarios on the same environment through legal entity-level configurations.</span></span> <span data-ttu-id="4f311-123">Contoso voi esimerkiksi käyttää Yhdysvaltojen tuotantolaitoksen varasto-/tuotantotilaustoimintoja (Yritys = Contoso Manufacturing United States).</span><span class="sxs-lookup"><span data-stu-id="4f311-123">For example, Contoso can use the stocked/production order capabilities in their US manufacturing facility (Legal entity = Contoso Manufacturing United States).</span></span> <span data-ttu-id="4f311-124">Contoso voi käyttää Contoso Robotics Arms huoltotilan ei-varastoitavien/resurssipohjaisten ominaisuuksien käyttöä Isossa-Britanniassa (yritys = Contoso Robotics United Kingdom).</span><span class="sxs-lookup"><span data-stu-id="4f311-124">Contoso can use the non-stocked/resource-based capabilities in their Contoso Robotics Arms servicing facility in UK (Legal entity = Contoso Robotics United Kingdom).</span></span>

### <a name="lite-deployment---deal-to-proforma-invoicing"></a><a  name="lite"></a><span data-ttu-id="4f311-125">Lite-käyttöönotto – kauppa proformalaskutukseen</span><span class="sxs-lookup"><span data-stu-id="4f311-125">Lite deployment - deal to proforma invoicing</span></span>

<span data-ttu-id="4f311-126">Lite-käyttöönotossa on seuraavat ominaisuudet:</span><span class="sxs-lookup"><span data-stu-id="4f311-126">The lite deployment includes the following capabilities:</span></span>

- <span data-ttu-id="4f311-127">Projektin suunnittelu Microsoft Project -verkkoversion avulla</span><span class="sxs-lookup"><span data-stu-id="4f311-127">Project planning using Microsoft Project for the Web</span></span>
- <span data-ttu-id="4f311-128">Moniulotteinen hinnoittelu</span><span class="sxs-lookup"><span data-stu-id="4f311-128">Multi-dimensional pricing</span></span>
- <span data-ttu-id="4f311-129">Yhdistetty resurssien hallinta</span><span class="sxs-lookup"><span data-stu-id="4f311-129">Unified Resource Management</span></span>
- <span data-ttu-id="4f311-130">Aikaseuranta</span><span class="sxs-lookup"><span data-stu-id="4f311-130">Time Tracking</span></span>
- <span data-ttu-id="4f311-131">Peruskulu</span><span class="sxs-lookup"><span data-stu-id="4f311-131">Basic Expense</span></span>
- <span data-ttu-id="4f311-132">Laskuehdotus</span><span class="sxs-lookup"><span data-stu-id="4f311-132">Invoice Proposal</span></span>

#### <a name="deployment-steps"></a><span data-ttu-id="4f311-133">Käyttöönotto-ohjeet</span><span class="sxs-lookup"><span data-stu-id="4f311-133">Deployment steps</span></span>
<span data-ttu-id="4f311-134">Määritä paras Project Operationsin käyttöönottomalli käyttämällä [Käyttöönottokyselyä](https://aka.ms/provisionprojectoperations).</span><span class="sxs-lookup"><span data-stu-id="4f311-134">Determine the best deployment model of Project Operations using the [Deployment questionnaire](https://aka.ms/provisionprojectoperations).</span></span>

<span data-ttu-id="4f311-135">Lisätietoja tälle käyttöönotolle: [Esiversiotilauksiin rekisteröityminen](lite-preview-subscription-sign-up.md) ja [Uuden ympäristön valmistelu](lite-deployment.md).</span><span class="sxs-lookup"><span data-stu-id="4f311-135">For this deployment, see [Sign-up for preview subscriptions](lite-preview-subscription-sign-up.md) and [Provision new environment](lite-deployment.md).</span></span> 


### <a name="project-operations-for-resourcenon-stocked-scenarios"></a><a name="integrated"></a><span data-ttu-id="4f311-136">Project Operations resurssien ja ei-varastoitavien skenaarioissa</span><span class="sxs-lookup"><span data-stu-id="4f311-136">Project Operations for resource/non-stocked scenarios</span></span>
<span data-ttu-id="4f311-137">Project Operations tarjoaa resurssien/ei-varastoitavien skenaarioille seuraavat ominaisuudet:</span><span class="sxs-lookup"><span data-stu-id="4f311-137">The Project Operations for resource/non-stocked scenarios includes the following capabilities:</span></span>
  
- <span data-ttu-id="4f311-138">Projektin suunnittelu Microsoft Project -verkkoversion avulla</span><span class="sxs-lookup"><span data-stu-id="4f311-138">Project planning using Microsoft Project for the Web</span></span>
- <span data-ttu-id="4f311-139">Moniulotteinen hinnoittelu</span><span class="sxs-lookup"><span data-stu-id="4f311-139">Multi-dimensional pricing</span></span>
- <span data-ttu-id="4f311-140">Yhdistetty resurssien hallinta</span><span class="sxs-lookup"><span data-stu-id="4f311-140">Unified Resource Management</span></span>
- <span data-ttu-id="4f311-141">Aikaseuranta</span><span class="sxs-lookup"><span data-stu-id="4f311-141">Time Tracking</span></span>
- <span data-ttu-id="4f311-142">Peruskulu</span><span class="sxs-lookup"><span data-stu-id="4f311-142">Basic Expense</span></span>
- <span data-ttu-id="4f311-143">Koko kulu</span><span class="sxs-lookup"><span data-stu-id="4f311-143">Full Expense</span></span>
- <span data-ttu-id="4f311-144">Kuittien OCR</span><span class="sxs-lookup"><span data-stu-id="4f311-144">Receipt OCR</span></span>
- <span data-ttu-id="4f311-145">Täysi laskutus</span><span class="sxs-lookup"><span data-stu-id="4f311-145">Full Invoicing</span></span>
- <span data-ttu-id="4f311-146">Tuoton kirjaaminen</span><span class="sxs-lookup"><span data-stu-id="4f311-146">Revenue Recognition</span></span>

#### <a name="deployment-steps"></a><span data-ttu-id="4f311-147">Käyttöönotto-ohjeet</span><span class="sxs-lookup"><span data-stu-id="4f311-147">Deployment steps</span></span>
<span data-ttu-id="4f311-148">Määritä paras Project Operationsin käyttöönottomalli käyttämällä [Käyttöönottokyselyä](https://aka.ms/provisionprojectoperations).</span><span class="sxs-lookup"><span data-stu-id="4f311-148">Determine the best deployment model of Project Operations using the [Deployment questionnaire](https://aka.ms/provisionprojectoperations).</span></span>

<span data-ttu-id="4f311-149">Lisätietoja tälle käyttöönotolle: [Esiversiotilauksiin rekisteröityminen](resource-sign-up-preview-subscription.md) ja [Uuden ympäristön valmistelu](resource-provision-new-environment.md).</span><span class="sxs-lookup"><span data-stu-id="4f311-149">For this deployment, see [Sign-up for preview subscriptions](resource-sign-up-preview-subscription.md) and [Provision new environment](resource-provision-new-environment.md).</span></span> 


### <a name="project-operations-for-stockedproduction-order-scenarios"></a><a name="pma"></a><span data-ttu-id="4f311-150">Project Operations varastoitavien/tuotantotilausten skenaarioissa</span><span class="sxs-lookup"><span data-stu-id="4f311-150">Project Operations for stocked/production order scenarios</span></span>

- <span data-ttu-id="4f311-151">Projektin suunnittelu työrakenteen avulla</span><span class="sxs-lookup"><span data-stu-id="4f311-151">Project planning using WBS</span></span>
- <span data-ttu-id="4f311-152">Resurssienhallinta</span><span class="sxs-lookup"><span data-stu-id="4f311-152">Resource Management</span></span>
- <span data-ttu-id="4f311-153">Aikaseuranta</span><span class="sxs-lookup"><span data-stu-id="4f311-153">Time Tracking</span></span>
- <span data-ttu-id="4f311-154">Koko kulu</span><span class="sxs-lookup"><span data-stu-id="4f311-154">Full Expense</span></span>
- <span data-ttu-id="4f311-155">Kuittien OCR</span><span class="sxs-lookup"><span data-stu-id="4f311-155">Receipt OCR</span></span>
- <span data-ttu-id="4f311-156">Täysi laskutus</span><span class="sxs-lookup"><span data-stu-id="4f311-156">Full Invoicing</span></span>
- <span data-ttu-id="4f311-157">Tuoton kirjaaminen</span><span class="sxs-lookup"><span data-stu-id="4f311-157">Revenue Recognition</span></span>
- <span data-ttu-id="4f311-158">Tuotantotilaukset</span><span class="sxs-lookup"><span data-stu-id="4f311-158">Production Orders</span></span>
- <span data-ttu-id="4f311-159">Materiaalien tuki</span><span class="sxs-lookup"><span data-stu-id="4f311-159">Materials support</span></span>

#### <a name="deployment-steps"></a><span data-ttu-id="4f311-160">Käyttöönotto-ohjeet</span><span class="sxs-lookup"><span data-stu-id="4f311-160">Deployment steps</span></span>
<span data-ttu-id="4f311-161">Määritä paras Project Operationsin käyttöönottomalli käyttämällä [Käyttöönottokyselyä](https://aka.ms/provisionprojectoperations).</span><span class="sxs-lookup"><span data-stu-id="4f311-161">Determine the best deployment model of Project Operations using the [Deployment questionnaire](https://aka.ms/provisionprojectoperations).</span></span>

<span data-ttu-id="4f311-162">Lisätietoja tälle käyttöönotolle: [Esiversiotilauksiin rekisteröityminen](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/dev-tools/sign-up-preview-subscription?toc=/dynamics365/finance/toc.json) ja [Uuden ympäristön valmistelu](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment?toc=/dynamics365/finance/toc.json).</span><span class="sxs-lookup"><span data-stu-id="4f311-162">For this deployment, see [Sign-up for preview subscriptions](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/dev-tools/sign-up-preview-subscription?toc=/dynamics365/finance/toc.json) and [Provision new environment](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment?toc=/dynamics365/finance/toc.json).</span></span> 

