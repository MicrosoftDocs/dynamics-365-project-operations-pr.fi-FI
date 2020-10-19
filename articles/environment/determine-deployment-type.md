---
title: Käyttöönottotyypit
description: Tässä aiheessa on tietoja Project Operationsin oikean käyttöönottotyypin valinnasta omalle yrityksellesi.
author: stsporen
manager: Annbe
ms.date: 10/02/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: c3cf378caae4510482a8ee6771bf2e6decfe3b48
ms.sourcegitcommit: b9d8bf00239815f31686e9b28998ac684fd2fca4
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/02/2020
ms.locfileid: "3948838"
---
# <a name="deployment-types"></a><span data-ttu-id="fe51a-103">Käyttöönottotyypit</span><span class="sxs-lookup"><span data-stu-id="fe51a-103">Deployment types</span></span>

<span data-ttu-id="fe51a-104">_**Koskee:** Project Operationsin resurssiin / muuhun kuin resurssiin perustuvia skenaarioita, Lite-käyttöönotto-kaupasta proformalaskutukseen_</span><span class="sxs-lookup"><span data-stu-id="fe51a-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

> [!IMPORTANT]
> <span data-ttu-id="fe51a-105">Kun olet ostanut käyttöoikeuden, voit määrittää Dynamics 365 Project Operationsin parhaan asennusmallin [ohjatun asennusvuon avulla](https://aka.ms/provisionprojectoperations).</span><span class="sxs-lookup"><span data-stu-id="fe51a-105">After you purchase the license, start here to determine the best deployment model of Dynamics 365 Project Operations using the [Guided installation flow](https://aka.ms/provisionprojectoperations).</span></span>
> <span data-ttu-id="fe51a-106">Kun olet tehnyt ohjatun asennusvuon, sinut ohjataan oikeaan hallintaportaaliin, jotta asennus viimeistellään.</span><span class="sxs-lookup"><span data-stu-id="fe51a-106">After you have finshed the Guided installation flow, you will be directed to the correct management portal to complete your installation.</span></span> <span data-ttu-id="fe51a-107">Asennuksen viimeistelemisen tiedot ovat alla.</span><span class="sxs-lookup"><span data-stu-id="fe51a-107">See the deployment details below to complete the installation.</span></span>


## <a name="existing-customers-of-dynamics-using-dynamics-365-project-service-automation"></a><span data-ttu-id="fe51a-108">Olemassa olevat Dynamics-asiakkaat, jotka käyttvät Dynamics 365 Project Service Automationia</span><span class="sxs-lookup"><span data-stu-id="fe51a-108">Existing customers of Dynamics using Dynamics 365 Project Service Automation</span></span>
<span data-ttu-id="fe51a-109">Project Operations sisältää Project Service Automationin mukana toimitetut toiminnot.</span><span class="sxs-lookup"><span data-stu-id="fe51a-109">Project Operations includes the capabilities that shipped with Project Service Automation.</span></span> <span data-ttu-id="fe51a-110">Näille asiakkaille julkaistaan tulevaisuudessa päivityspolku.</span><span class="sxs-lookup"><span data-stu-id="fe51a-110">An upgrade path will be released for these customers in the future.</span></span>

## <a name="existing-customers-of-dynamics-365-finance-using-project-management-and-accounting"></a><span data-ttu-id="fe51a-111">Olemassa olevat Dynamics 365 Finance-asiakkaat, jotka käyttävät Projektinhallinta ja kirjanpito -moduulia</span><span class="sxs-lookup"><span data-stu-id="fe51a-111">Existing customers of Dynamics 365 Finance using Project management and accounting</span></span> 

<span data-ttu-id="fe51a-112">Finance-asiakkaat, jotka käyttävät Projektinhallinta- ja kirjanpito -toimintoa, voivat jatkaa käyttöä sellaisenaan.</span><span class="sxs-lookup"><span data-stu-id="fe51a-112">Existing customers of Finance who use the Project management and accounting functionality can continue use this as is.</span></span> <span data-ttu-id="fe51a-113">Katso [Project Operations varastoitavien/tuotantotilausten skenaarioissa](#pma).</span><span class="sxs-lookup"><span data-stu-id="fe51a-113">See [Project Operations for stocked/production order scenarios](#pma).</span></span>

<span data-ttu-id="fe51a-114">Project Operations tukee useita eri toteutusvaihtoehtoja tarpeidesi mukaan.</span><span class="sxs-lookup"><span data-stu-id="fe51a-114">Project Operations supports multiple deployment options to match your requirements.</span></span> <span data-ttu-id="fe51a-115">Olitpa uusi tai nykyinen Dynamics 365 -asiakas, Project Operations voit tukea tarpeitasi.</span><span class="sxs-lookup"><span data-stu-id="fe51a-115">Whether you are a new or existing Dynamics 365 customer, Project Operations can support your needs.</span></span>

<span data-ttu-id="fe51a-116">[Käyttöönottokyselyn](https://aka.ms/provisionprojectoperations) avulla voit määrittää oikean käyttöönottotavan.</span><span class="sxs-lookup"><span data-stu-id="fe51a-116">Our [Deployment questionnaire](https://aka.ms/provisionprojectoperations) will help you determine the right deployment.</span></span> <span data-ttu-id="fe51a-117">Tulokset opastavat sinua kohti jotakin seuraavista käyttöönottotyypeistä:</span><span class="sxs-lookup"><span data-stu-id="fe51a-117">The results will guide you toward one of the following deployment types:</span></span>

- [<span data-ttu-id="fe51a-118">Lite-käyttöönotto – kauppa proformalaskutukseen</span><span class="sxs-lookup"><span data-stu-id="fe51a-118">Lite deployment – deal to proforma invoicing</span></span>](#lite)
- [<span data-ttu-id="fe51a-119">Project Operations resurssien ja ei-varastoitavien skenaarioissa</span><span class="sxs-lookup"><span data-stu-id="fe51a-119">Project Operations for resource/non-stocked scenarios</span></span>](#integrated)
- [<span data-ttu-id="fe51a-120">Project Operations varastoitavien/tuotantotilausten skenaarioissa</span><span class="sxs-lookup"><span data-stu-id="fe51a-120">Project Operations for stocked/production order scenarios</span></span>](#pma)

<span data-ttu-id="fe51a-121">Project Operations tukee varastoitu/tuotantotilaus-skenaarioita ja ei-varastoitavia/resurssipohjaisia skenaarioita samassa ympäristössä yritystason määritysten avulla.</span><span class="sxs-lookup"><span data-stu-id="fe51a-121">Project Operations support stocked/production order scenarios and non-stocked/resource-based scenarios on the same environment through legal entity-level configurations.</span></span> <span data-ttu-id="fe51a-122">Esimerkiksi Contoso voi hyödyntää Yhdysvaltain tuotantolaitoksessa (oikeushenkilö = Contoso Manufacturing United States) ja varastoitavien/tuotannon ominaisuuksia, ja ei-varastoitavien/resurssipohjaisten ominaisuuksia Yhdistyneiden kuningaskuntien Contoso Robotics Arms -palvelulaitoksessa (oikeushenkilö = Contoso Robotics United Kingdom).</span><span class="sxs-lookup"><span data-stu-id="fe51a-122">For example, Contoso can leverage stocked/production order capabilities in their US manufacturing facility (Legal entity = Contoso Manufacturing United States) and non-stocked/resource-based capabilities in their Contoso Robotics Arms servicing facility in UK (Legal entity = Contoso Robotics United Kingdom).</span></span>

## <a name="a-namelitelite-deployment---deal-to-proforma-invoicing"></a><span data-ttu-id="fe51a-123"><a name="lite"><a/>Lite-käyttöönotto – kauppa proformalaskutukseen</span><span class="sxs-lookup"><span data-stu-id="fe51a-123"><a name="lite"><a/>Lite deployment - deal to proforma invoicing</span></span>
<span data-ttu-id="fe51a-124">Lite-käyttöönotossa on seuraavat ominaisuudet:</span><span class="sxs-lookup"><span data-stu-id="fe51a-124">The lite deployment includes the following capabilities:</span></span>

- <span data-ttu-id="fe51a-125">Projektin suunnittelu Microsoft Project -verkkoversion avulla</span><span class="sxs-lookup"><span data-stu-id="fe51a-125">Project planning using Microsoft Project for the Web</span></span>
- <span data-ttu-id="fe51a-126">Moniulotteinen hinnoittelu</span><span class="sxs-lookup"><span data-stu-id="fe51a-126">Multi-dimensional pricing</span></span>
- <span data-ttu-id="fe51a-127">Yhdistetty resurssien hallinta</span><span class="sxs-lookup"><span data-stu-id="fe51a-127">Unified Resource Management</span></span>
- <span data-ttu-id="fe51a-128">Aikaseuranta</span><span class="sxs-lookup"><span data-stu-id="fe51a-128">Time Tracking</span></span>
- <span data-ttu-id="fe51a-129">Peruskulu</span><span class="sxs-lookup"><span data-stu-id="fe51a-129">Basic Expense</span></span>
- <span data-ttu-id="fe51a-130">Laskuehdotus</span><span class="sxs-lookup"><span data-stu-id="fe51a-130">Invoice Proposal</span></span>

### <a name="deployment-steps"></a><span data-ttu-id="fe51a-131">Käyttöönotto-ohjeet:</span><span class="sxs-lookup"><span data-stu-id="fe51a-131">Deployment steps:</span></span>
<span data-ttu-id="fe51a-132">Määritä paras Project Operationsin käyttöönottomalli käyttämällä [Käyttöönottokyselyä](https://aka.ms/provisionprojectoperations).</span><span class="sxs-lookup"><span data-stu-id="fe51a-132">Determine the best deployment model of Project Operations using the [Deployment questionnaire](https://aka.ms/provisionprojectoperations).</span></span>

<span data-ttu-id="fe51a-133">Lisätietoja tälle käyttöönotolle: [Esiversiotilauksiin rekisteröityminen](lite-preview-subscription-sign-up.md) ja [Uuden ympäristön valmistelu](lite-deployment.md).</span><span class="sxs-lookup"><span data-stu-id="fe51a-133">For this deployment, see [Sign-up for preview subscriptions](lite-preview-subscription-sign-up.md) and [Provision new environment](lite-deployment.md).</span></span> 


## <a name="a-nameintegratedproject-operations-for-resourcenon-stocked-scenarios"></a><span data-ttu-id="fe51a-134"><a name="integrated"><a/>Project Operations resurssien ja ei-varastoitavien skenaarioissa</span><span class="sxs-lookup"><span data-stu-id="fe51a-134"><a name="integrated"><a/>Project Operations for resource/non-stocked scenarios</span></span>
<span data-ttu-id="fe51a-135">Project Operations tarjoaa resurssien/ei-varastoitavien skenaarioille seuraavat ominaisuudet:</span><span class="sxs-lookup"><span data-stu-id="fe51a-135">The Project Operations for resource/non-stocked scenarios includes the following capabilities:</span></span>
  
- <span data-ttu-id="fe51a-136">Projektin suunnittelu Microsoft Project -verkkoversion avulla</span><span class="sxs-lookup"><span data-stu-id="fe51a-136">Project planning using Microsoft Project for the Web</span></span>
- <span data-ttu-id="fe51a-137">Moniulotteinen hinnoittelu</span><span class="sxs-lookup"><span data-stu-id="fe51a-137">Multi-dimensional pricing</span></span>
- <span data-ttu-id="fe51a-138">Yhdistetty resurssien hallinta</span><span class="sxs-lookup"><span data-stu-id="fe51a-138">Unified Resource Management</span></span>
- <span data-ttu-id="fe51a-139">Aikaseuranta</span><span class="sxs-lookup"><span data-stu-id="fe51a-139">Time Tracking</span></span>
- <span data-ttu-id="fe51a-140">Peruskulu</span><span class="sxs-lookup"><span data-stu-id="fe51a-140">Basic Expense</span></span>
- <span data-ttu-id="fe51a-141">Koko kulu</span><span class="sxs-lookup"><span data-stu-id="fe51a-141">Full Expense</span></span>
- <span data-ttu-id="fe51a-142">Kuittien OCR</span><span class="sxs-lookup"><span data-stu-id="fe51a-142">Receipt OCR</span></span>
- <span data-ttu-id="fe51a-143">Täysi laskutus</span><span class="sxs-lookup"><span data-stu-id="fe51a-143">Full Invoicing</span></span>
- <span data-ttu-id="fe51a-144">Tuoton kirjaaminen</span><span class="sxs-lookup"><span data-stu-id="fe51a-144">Revenue Recognition</span></span>

### <a name="deployment-steps"></a><span data-ttu-id="fe51a-145">Käyttöönotto-ohjeet:</span><span class="sxs-lookup"><span data-stu-id="fe51a-145">Deployment steps:</span></span>
<span data-ttu-id="fe51a-146">Määritä paras Project Operationsin käyttöönottomalli käyttämällä [Käyttöönottokyselyä](https://aka.ms/provisionprojectoperations).</span><span class="sxs-lookup"><span data-stu-id="fe51a-146">Determine the best deployment model of Project Operations using the [Deployment questionnaire](https://aka.ms/provisionprojectoperations).</span></span>

<span data-ttu-id="fe51a-147">Lisätietoja tälle käyttöönotolle: [Esiversiotilauksiin rekisteröityminen](resource-sign-up-preview-subscription.md) ja [Uuden ympäristön valmistelu](resource-provision-new-environment.md).</span><span class="sxs-lookup"><span data-stu-id="fe51a-147">For this deployment, see [Sign-up for preview subscriptions](resource-sign-up-preview-subscription.md) and [Provision new environment](resource-provision-new-environment.md).</span></span> 


## <a name="project-operations-for-stockedproduction-order-scenarios"></a><a name="pma"></a><span data-ttu-id="fe51a-148">Project Operations varastoitavien/tuotantotilausten skenaarioissa</span><span class="sxs-lookup"><span data-stu-id="fe51a-148">Project Operations for stocked/production order scenarios</span></span>

- <span data-ttu-id="fe51a-149">Projektin suunnittelu työrakenteen avulla</span><span class="sxs-lookup"><span data-stu-id="fe51a-149">Project planning using WBS</span></span>
- <span data-ttu-id="fe51a-150">Resurssienhallinta</span><span class="sxs-lookup"><span data-stu-id="fe51a-150">Resource Management</span></span>
- <span data-ttu-id="fe51a-151">Aikaseuranta</span><span class="sxs-lookup"><span data-stu-id="fe51a-151">Time Tracking</span></span>
- <span data-ttu-id="fe51a-152">Koko kulu</span><span class="sxs-lookup"><span data-stu-id="fe51a-152">Full Expense</span></span>
- <span data-ttu-id="fe51a-153">Kuittien OCR</span><span class="sxs-lookup"><span data-stu-id="fe51a-153">Receipt OCR</span></span>
- <span data-ttu-id="fe51a-154">Täysi laskutus</span><span class="sxs-lookup"><span data-stu-id="fe51a-154">Full Invoicing</span></span>
- <span data-ttu-id="fe51a-155">Tuoton kirjaaminen</span><span class="sxs-lookup"><span data-stu-id="fe51a-155">Revenue Recognition</span></span>
- <span data-ttu-id="fe51a-156">Tuotantotilaukset</span><span class="sxs-lookup"><span data-stu-id="fe51a-156">Production Orders</span></span>
- <span data-ttu-id="fe51a-157">Materiaalien tuki</span><span class="sxs-lookup"><span data-stu-id="fe51a-157">Materials support</span></span>

### <a name="deployment-steps"></a><span data-ttu-id="fe51a-158">Käyttöönotto-ohjeet:</span><span class="sxs-lookup"><span data-stu-id="fe51a-158">Deployment steps:</span></span>
<span data-ttu-id="fe51a-159">Määritä paras Project Operationsin käyttöönottomalli käyttämällä [Käyttöönottokyselyä](https://aka.ms/provisionprojectoperations).</span><span class="sxs-lookup"><span data-stu-id="fe51a-159">Determine the best deployment model of Project Operations using the [Deployment questionnaire](https://aka.ms/provisionprojectoperations).</span></span>

<span data-ttu-id="fe51a-160">Lisätietoja tälle käyttöönotolle: [Esiversiotilauksiin rekisteröityminen](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/dev-tools/sign-up-preview-subscription?toc=/dynamics365/finance/toc.json) ja [Uuden ympäristön valmistelu](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment?toc=/dynamics365/finance/toc.json).</span><span class="sxs-lookup"><span data-stu-id="fe51a-160">For this deployment, see [Sign-up for preview subscriptions](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/dev-tools/sign-up-preview-subscription?toc=/dynamics365/finance/toc.json) and [Provision new environment](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment?toc=/dynamics365/finance/toc.json).</span></span> 



