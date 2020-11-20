---
title: Käyttöönottotyypin määritys
description: Tässä aiheessa on tietoja Project Operationsin oikean käyttöönottotyypin valinnasta omalle yrityksellesi.
author: stsporen
manager: Annbe
ms.date: 11/05/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: e9d3a5d8e6e1daafac72a3b4c0380b679d1869bd
ms.sourcegitcommit: 14aa380759214713d9bf560f5a7f619b7f4bd5b8
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/05/2020
ms.locfileid: "4401214"
---
# <a name="determine-your-deployment-type"></a><span data-ttu-id="1e8c8-103">Käyttöönottotyypin määritys</span><span class="sxs-lookup"><span data-stu-id="1e8c8-103">Determine your deployment type</span></span>

<span data-ttu-id="1e8c8-104">_**Koskee:** Project Operationsin resurssiin / muuhun kuin resurssiin perustuvia skenaarioita, Lite-käyttöönotto-kaupasta proformalaskutukseen_</span><span class="sxs-lookup"><span data-stu-id="1e8c8-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

> [!IMPORTANT]
> <span data-ttu-id="1e8c8-105">Kun olet ostanut käyttöoikeuden, voit määrittää Dynamics 365 Project Operationsin parhaan asennusmallin [ohjatun asennusvuon avulla](https://aka.ms/provisionprojectoperations).</span><span class="sxs-lookup"><span data-stu-id="1e8c8-105">After you purchase the license, start here to determine the best deployment model of Dynamics 365 Project Operations using the [Guided installation flow](https://aka.ms/provisionprojectoperations).</span></span>
> <span data-ttu-id="1e8c8-106">Kun olet tehnyt ohjatun asennusvuon, sinut ohjataan oikeaan hallintaportaaliin, jotta asennus viimeistellään.</span><span class="sxs-lookup"><span data-stu-id="1e8c8-106">After you have finshed the Guided installation flow, you will be directed to the correct management portal to complete your installation.</span></span> <span data-ttu-id="1e8c8-107">Katso asennuksen viimeistelemisen tiedot.</span><span class="sxs-lookup"><span data-stu-id="1e8c8-107">See the deployment details to complete the installation.</span></span>


## <a name="existing-customers-of-dynamics-using-dynamics-365-project-service-automation"></a><span data-ttu-id="1e8c8-108">Olemassa olevat Dynamics-asiakkaat, jotka käyttvät Dynamics 365 Project Service Automationia</span><span class="sxs-lookup"><span data-stu-id="1e8c8-108">Existing customers of Dynamics using Dynamics 365 Project Service Automation</span></span>
<span data-ttu-id="1e8c8-109">Project Operations sisältää Project Service Automationin mukana toimitetut toiminnot.</span><span class="sxs-lookup"><span data-stu-id="1e8c8-109">Project Operations includes the capabilities that shipped with Project Service Automation.</span></span> <span data-ttu-id="1e8c8-110">Näille asiakkaille julkaistaan päivityspolku vuoden 2021 1. julkaisuaallossa.</span><span class="sxs-lookup"><span data-stu-id="1e8c8-110">An upgrade path will be released for these customers in the 2021 release wave 1.</span></span>

## <a name="existing-customers-of-dynamics-365-finance-using-project-management-and-accounting"></a><span data-ttu-id="1e8c8-111">Olemassa olevat Dynamics 365 Finance-asiakkaat, jotka käyttävät Projektinhallinta ja kirjanpito -moduulia</span><span class="sxs-lookup"><span data-stu-id="1e8c8-111">Existing customers of Dynamics 365 Finance using Project management and accounting</span></span> 

<span data-ttu-id="1e8c8-112">Nykyiset projektin hallinta- ja kirjanpitotoimintoja käyttävät Finance-asiakkaat voivat jatkoa käyttöä entiseen tapaan.</span><span class="sxs-lookup"><span data-stu-id="1e8c8-112">Existing customers of Finance who use the Project management and accounting functionality can continue to use it as is.</span></span> <span data-ttu-id="1e8c8-113">Katso [Project Operations varastoitavien/tuotantotilausten skenaarioissa](#pma).</span><span class="sxs-lookup"><span data-stu-id="1e8c8-113">See [Project Operations for stocked/production order scenarios](#pma).</span></span>


## <a name="deployment-types"></a><span data-ttu-id="1e8c8-114">Käyttöönottotyypit</span><span class="sxs-lookup"><span data-stu-id="1e8c8-114">Deployment types</span></span>
<span data-ttu-id="1e8c8-115">Project Operations tukee useita eri toteutusvaihtoehtoja tarpeidesi mukaan.</span><span class="sxs-lookup"><span data-stu-id="1e8c8-115">Project Operations supports multiple deployment options to match your requirements.</span></span> <span data-ttu-id="1e8c8-116">Olitpa uusi tai nykyinen Dynamics 365 -asiakas, Project Operations voit tukea tarpeitasi.</span><span class="sxs-lookup"><span data-stu-id="1e8c8-116">Whether you're a new or existing Dynamics 365 customer, Project Operations can support your needs.</span></span>

<span data-ttu-id="1e8c8-117">[Käyttöönottokyselyn](https://aka.ms/provisionprojectoperations) avulla voit määrittää oikean käyttöönottotavan.</span><span class="sxs-lookup"><span data-stu-id="1e8c8-117">Our [Deployment questionnaire](https://aka.ms/provisionprojectoperations) will help you determine the right deployment.</span></span> <span data-ttu-id="1e8c8-118">Tulokset opastavat sinua kohti jotakin seuraavista käyttöönottotyypeistä:</span><span class="sxs-lookup"><span data-stu-id="1e8c8-118">The results will guide you toward one of the following deployment types:</span></span>

- [<span data-ttu-id="1e8c8-119">Lite-käyttöönotto – kauppa proformalaskutukseen</span><span class="sxs-lookup"><span data-stu-id="1e8c8-119">Lite deployment – deal to proforma invoicing</span></span>](#lite)
- [<span data-ttu-id="1e8c8-120">Project Operations resurssien ja ei-varastoitavien skenaarioissa</span><span class="sxs-lookup"><span data-stu-id="1e8c8-120">Project Operations for resource/non-stocked scenarios</span></span>](#integrated)
- [<span data-ttu-id="1e8c8-121">Project Operations varastoitavien/tuotantotilausten skenaarioissa</span><span class="sxs-lookup"><span data-stu-id="1e8c8-121">Project Operations for stocked/production order scenarios</span></span>](#pma)

<span data-ttu-id="1e8c8-122">Project Operations tukee varastoitu/tuotantotilaus-skenaarioita ja ei-varastoitavia/resurssipohjaisia skenaarioita samassa ympäristössä yritystason määritysten avulla.</span><span class="sxs-lookup"><span data-stu-id="1e8c8-122">Project Operations support stocked/production order scenarios and non-stocked/resource-based scenarios on the same environment through legal entity-level configurations.</span></span> <span data-ttu-id="1e8c8-123">Contoso voi esimerkiksi käyttää Yhdysvaltojen tuotantolaitoksen varasto-/tuotantotilaustoimintoja (Yritys = Contoso Manufacturing United States).</span><span class="sxs-lookup"><span data-stu-id="1e8c8-123">For example, Contoso can use the stocked/production order capabilities in their US manufacturing facility (Legal entity = Contoso Manufacturing United States).</span></span> <span data-ttu-id="1e8c8-124">Contoso voi käyttää Contoso Robotics Arms huoltotilan ei-varastoitavien/resurssipohjaisten ominaisuuksien käyttöä Isossa-Britanniassa (yritys = Contoso Robotics United Kingdom).</span><span class="sxs-lookup"><span data-stu-id="1e8c8-124">Contoso can use the non-stocked/resource-based capabilities in their Contoso Robotics Arms servicing facility in UK (Legal entity = Contoso Robotics United Kingdom).</span></span>

### <a name="lite-deployment---deal-to-proforma-invoicing"></a><a  name="lite"></a><span data-ttu-id="1e8c8-125">Lite-käyttöönotto – kauppa proformalaskutukseen</span><span class="sxs-lookup"><span data-stu-id="1e8c8-125">Lite deployment - deal to proforma invoicing</span></span>

<span data-ttu-id="1e8c8-126">Lite-käyttöönotossa on seuraavat ominaisuudet:</span><span class="sxs-lookup"><span data-stu-id="1e8c8-126">The lite deployment includes the following capabilities:</span></span>

- <span data-ttu-id="1e8c8-127">Dynamics 365 Sales -sovelluksen kokemuksia laajentava projektien myyntiprosessi</span><span class="sxs-lookup"><span data-stu-id="1e8c8-127">Sales process for projects that extends Dynamics 365 Sales application experiences</span></span>
- <span data-ttu-id="1e8c8-128">Projektin suunnittelu Microsoft Project -verkkoversion avulla</span><span class="sxs-lookup"><span data-stu-id="1e8c8-128">Project planning using Microsoft Project for the Web</span></span>
- <span data-ttu-id="1e8c8-129">Moniulotteinen hinnoittelu</span><span class="sxs-lookup"><span data-stu-id="1e8c8-129">Multi-dimensional pricing</span></span>
- <span data-ttu-id="1e8c8-130">Yhdistetty resurssien hallinta</span><span class="sxs-lookup"><span data-stu-id="1e8c8-130">Unified resource management</span></span>
- <span data-ttu-id="1e8c8-131">Aikaseuranta</span><span class="sxs-lookup"><span data-stu-id="1e8c8-131">Time tracking</span></span>
- <span data-ttu-id="1e8c8-132">Peruskulu</span><span class="sxs-lookup"><span data-stu-id="1e8c8-132">Basic expense</span></span>
- <span data-ttu-id="1e8c8-133">Proformalaskutus ja asiakkaille suunnattu laskutus</span><span class="sxs-lookup"><span data-stu-id="1e8c8-133">Proforma and customer-facing invoicing</span></span> 

#### <a name="deployment-steps"></a><span data-ttu-id="1e8c8-134">Käyttöönotto-ohjeet</span><span class="sxs-lookup"><span data-stu-id="1e8c8-134">Deployment steps</span></span>
<span data-ttu-id="1e8c8-135">Määritä paras Project Operationsin käyttöönottomalli käyttämällä [Käyttöönottokyselyä](https://aka.ms/provisionprojectoperations).</span><span class="sxs-lookup"><span data-stu-id="1e8c8-135">Determine the best deployment model of Project Operations using the [Deployment questionnaire](https://aka.ms/provisionprojectoperations).</span></span>

<span data-ttu-id="1e8c8-136">Lisätietoja tälle käyttöönotolle: [Esiversiotilauksiin rekisteröityminen](lite-preview-subscription-sign-up.md) ja [Uuden ympäristön valmistelu](lite-deployment.md).</span><span class="sxs-lookup"><span data-stu-id="1e8c8-136">For this deployment, see [Sign-up for preview subscriptions](lite-preview-subscription-sign-up.md) and [Provision new environment](lite-deployment.md).</span></span> 


### <a name="project-operations-for-resourcenon-stocked-scenarios"></a><a name="integrated"></a><span data-ttu-id="1e8c8-137">Project Operations resurssien ja ei-varastoitavien skenaarioissa</span><span class="sxs-lookup"><span data-stu-id="1e8c8-137">Project Operations for resource/non-stocked scenarios</span></span>
<span data-ttu-id="1e8c8-138">Project Operations tarjoaa resurssien/ei-varastoitavien skenaarioille seuraavat ominaisuudet:</span><span class="sxs-lookup"><span data-stu-id="1e8c8-138">The Project Operations for resource/non-stocked scenarios includes the following capabilities:</span></span>
 
- <span data-ttu-id="1e8c8-139">Dynamics 365 Sales -sovellusta laajentava projektien myyntiprosessi</span><span class="sxs-lookup"><span data-stu-id="1e8c8-139">Sales process for projects that extends the Dynamics 365 Sales application</span></span>
- <span data-ttu-id="1e8c8-140">Projektin suunnittelu Microsoft Project -verkkoversion avulla</span><span class="sxs-lookup"><span data-stu-id="1e8c8-140">Project planning using Microsoft Project for the Web</span></span>
- <span data-ttu-id="1e8c8-141">Moniulotteinen hinnoittelu</span><span class="sxs-lookup"><span data-stu-id="1e8c8-141">Multi-dimensional pricing</span></span>
- <span data-ttu-id="1e8c8-142">Yhdistetty resurssien hallinta</span><span class="sxs-lookup"><span data-stu-id="1e8c8-142">Unified resource management</span></span>
- <span data-ttu-id="1e8c8-143">Aikaseuranta</span><span class="sxs-lookup"><span data-stu-id="1e8c8-143">Time tracking</span></span>
- <span data-ttu-id="1e8c8-144">Peruskulu</span><span class="sxs-lookup"><span data-stu-id="1e8c8-144">Basic expense</span></span>
- <span data-ttu-id="1e8c8-145">Koko kulu</span><span class="sxs-lookup"><span data-stu-id="1e8c8-145">Full expense</span></span>
- <span data-ttu-id="1e8c8-146">Kuittien OCR</span><span class="sxs-lookup"><span data-stu-id="1e8c8-146">Receipt OCR</span></span>
- <span data-ttu-id="1e8c8-147">Proformalaskutus ja asiakkaille suunnattu laskutus</span><span class="sxs-lookup"><span data-stu-id="1e8c8-147">Proforma and customer-facing invoicing</span></span> 
- <span data-ttu-id="1e8c8-148">Projektien tuloutus</span><span class="sxs-lookup"><span data-stu-id="1e8c8-148">Revenue recognition for projects</span></span>

#### <a name="deployment-steps"></a><span data-ttu-id="1e8c8-149">Käyttöönotto-ohjeet</span><span class="sxs-lookup"><span data-stu-id="1e8c8-149">Deployment steps</span></span>
<span data-ttu-id="1e8c8-150">Määritä paras Project Operationsin käyttöönottomalli käyttämällä [Käyttöönottokyselyä](https://aka.ms/provisionprojectoperations).</span><span class="sxs-lookup"><span data-stu-id="1e8c8-150">Determine the best deployment model of Project Operations using the [Deployment questionnaire](https://aka.ms/provisionprojectoperations).</span></span>

<span data-ttu-id="1e8c8-151">Lisätietoja tälle käyttöönotolle: [Esiversiotilauksiin rekisteröityminen](resource-sign-up-preview-subscription.md) ja [Uuden ympäristön valmistelu](resource-provision-new-environment.md).</span><span class="sxs-lookup"><span data-stu-id="1e8c8-151">For this deployment, see [Sign-up for preview subscriptions](resource-sign-up-preview-subscription.md) and [Provision new environment](resource-provision-new-environment.md).</span></span> 


### <a name="project-operations-for-stockedproduction-order-scenarios"></a><a name="pma"></a><span data-ttu-id="1e8c8-152">Project Operations varastoitavien/tuotantotilausten skenaarioissa</span><span class="sxs-lookup"><span data-stu-id="1e8c8-152">Project Operations for stocked/production order scenarios</span></span>

- <span data-ttu-id="1e8c8-153">Projektin suunnittelu työrakenteen avulla</span><span class="sxs-lookup"><span data-stu-id="1e8c8-153">Project planning using WBS</span></span>
- <span data-ttu-id="1e8c8-154">Resurssienhallinta</span><span class="sxs-lookup"><span data-stu-id="1e8c8-154">Resource Management</span></span>
- <span data-ttu-id="1e8c8-155">Aikaseuranta</span><span class="sxs-lookup"><span data-stu-id="1e8c8-155">Time Tracking</span></span>
- <span data-ttu-id="1e8c8-156">Koko kulu</span><span class="sxs-lookup"><span data-stu-id="1e8c8-156">Full Expense</span></span>
- <span data-ttu-id="1e8c8-157">Kuittien OCR</span><span class="sxs-lookup"><span data-stu-id="1e8c8-157">Receipt OCR</span></span>
- <span data-ttu-id="1e8c8-158">Täysi laskutus</span><span class="sxs-lookup"><span data-stu-id="1e8c8-158">Full Invoicing</span></span>
- <span data-ttu-id="1e8c8-159">Tuoton kirjaaminen</span><span class="sxs-lookup"><span data-stu-id="1e8c8-159">Revenue Recognition</span></span>
- <span data-ttu-id="1e8c8-160">Tuotantotilaukset</span><span class="sxs-lookup"><span data-stu-id="1e8c8-160">Production Orders</span></span>
- <span data-ttu-id="1e8c8-161">Materiaalien tuki</span><span class="sxs-lookup"><span data-stu-id="1e8c8-161">Materials support</span></span>

#### <a name="deployment-steps"></a><span data-ttu-id="1e8c8-162">Käyttöönotto-ohjeet</span><span class="sxs-lookup"><span data-stu-id="1e8c8-162">Deployment steps</span></span>
<span data-ttu-id="1e8c8-163">Määritä paras Project Operationsin käyttöönottomalli käyttämällä [Käyttöönottokyselyä](https://aka.ms/provisionprojectoperations).</span><span class="sxs-lookup"><span data-stu-id="1e8c8-163">Determine the best deployment model of Project Operations using the [Deployment questionnaire](https://aka.ms/provisionprojectoperations).</span></span>

<span data-ttu-id="1e8c8-164">Lisätietoja tälle käyttöönotolle: [Esiversiotilauksiin rekisteröityminen](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/dev-tools/sign-up-preview-subscription?toc=/dynamics365/finance/toc.json) ja [Uuden ympäristön valmistelu](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment?toc=/dynamics365/finance/toc.json).</span><span class="sxs-lookup"><span data-stu-id="1e8c8-164">For this deployment, see [Sign-up for preview subscriptions](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/dev-tools/sign-up-preview-subscription?toc=/dynamics365/finance/toc.json) and [Provision new environment](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment?toc=/dynamics365/finance/toc.json).</span></span> 

