---
title: Käyttöönottotyypin määritys
description: Tässä aiheessa on tietoja Project Operationsin oikean käyttöönottotyypin valinnasta omalle yrityksellesi.
author: stsporen
ms.date: 03/15/2021
ms.topic: article
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: ad700a84edd6c39609bc5b4f09ca74af3059a0dd
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/10/2021
ms.locfileid: "5997102"
---
# <a name="determine-your-deployment-type"></a><span data-ttu-id="a670b-103">Käyttöönottotyypin määritys</span><span class="sxs-lookup"><span data-stu-id="a670b-103">Determine your deployment type</span></span>

<span data-ttu-id="a670b-104">_**Koskee:** Project Operationsin resurssiin / muuhun kuin resurssiin perustuvia skenaarioita, Lite-käyttöönotto-kaupasta proformalaskutukseen_</span><span class="sxs-lookup"><span data-stu-id="a670b-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

> [!IMPORTANT]
> <span data-ttu-id="a670b-105">Kun olet ostanut lisenssin, aloita tästä ja selvitä Dynamics 365 Project Operations -palvelun paras käyttöönottomalli käyttämällä  [ohjattua asennustyökulkua](https://aka.ms/provisionprojectoperations).</span><span class="sxs-lookup"><span data-stu-id="a670b-105">After you purchase the license, start here to determine the best deployment model of Dynamics 365 Project Operations using the [Guided installation flow](https://aka.ms/provisionprojectoperations).</span></span>
> <span data-ttu-id="a670b-106">Kun olet tehnyt ohjatun asennusvuon, sinut ohjataan oikeaan hallintaportaaliin, jotta asennus viimeistellään.</span><span class="sxs-lookup"><span data-stu-id="a670b-106">After you have finshed the Guided installation flow, you will be directed to the correct management portal to complete your installation.</span></span> <span data-ttu-id="a670b-107">Katso asennuksen viimeistelemisen tiedot.</span><span class="sxs-lookup"><span data-stu-id="a670b-107">See the deployment details to complete the installation.</span></span>


## <a name="existing-customers-of-dynamics-using-dynamics-365-project-service-automation"></a><span data-ttu-id="a670b-108">Olemassa olevat Dynamics-asiakkaat, jotka käyttvät Dynamics 365 Project Service Automationia</span><span class="sxs-lookup"><span data-stu-id="a670b-108">Existing customers of Dynamics using Dynamics 365 Project Service Automation</span></span>
<span data-ttu-id="a670b-109">Project Operations sisältää Project Service Automationin mukana toimitetut toiminnot.</span><span class="sxs-lookup"><span data-stu-id="a670b-109">Project Operations includes the capabilities that shipped with Project Service Automation.</span></span> <span data-ttu-id="a670b-110">Näille asiakkaille julkaistaan päivityspolku vuoden 2021 1. julkaisuaallossa.</span><span class="sxs-lookup"><span data-stu-id="a670b-110">An upgrade path will be released for these customers in the 2021 release wave 1.</span></span>

## <a name="existing-customers-of-dynamics-365-finance-using-project-management-and-accounting"></a><span data-ttu-id="a670b-111">Olemassa olevat Dynamics 365 Finance-asiakkaat, jotka käyttävät Projektinhallinta ja kirjanpito -moduulia</span><span class="sxs-lookup"><span data-stu-id="a670b-111">Existing customers of Dynamics 365 Finance using Project management and accounting</span></span> 

<span data-ttu-id="a670b-112">Nykyiset projektin hallinta- ja kirjanpitotoimintoja käyttävät Finance-asiakkaat voivat jatkoa käyttöä entiseen tapaan.</span><span class="sxs-lookup"><span data-stu-id="a670b-112">Existing customers of Finance who use the Project management and accounting functionality can continue to use it as is.</span></span> <span data-ttu-id="a670b-113">Katso [Project Operations varastoitavien/tuotantotilausten skenaarioissa](#pma).</span><span class="sxs-lookup"><span data-stu-id="a670b-113">See [Project Operations for stocked/production order scenarios](#pma).</span></span>


## <a name="deployment-regions"></a><span data-ttu-id="a670b-114">Käyttöönottoalueet</span><span class="sxs-lookup"><span data-stu-id="a670b-114">Deployment regions</span></span>
<span data-ttu-id="a670b-115">Lisätietoja Project Operationsin käyttöönottoa tukevien alueiden määrittämisestä on kohdassa [Dynamics 365:n ja Power Platformin maantieteellinen saatavuusraportti](https://dynamics.microsoft.com/en-us/geographic-availability/).</span><span class="sxs-lookup"><span data-stu-id="a670b-115">To determine which regions support Project Operations deployment, see [Geographical availability for Dynamics 365 and Power Platform report](https://dynamics.microsoft.com/en-us/geographic-availability/).</span></span> <span data-ttu-id="a670b-116">Jos haluat nähdä tuetut alueet, valitse **Näytä raportti** ja laajenna **Dynamics 365 > Operation Apps > Dynamics 365 Project Operations**.</span><span class="sxs-lookup"><span data-stu-id="a670b-116">Select **View Report**, and expand **Dynamics 365 > Operations Apps > Dynamics 365 Project Operations** to view the supported regions.</span></span>

## <a name="deployment-types"></a><span data-ttu-id="a670b-117">Käyttöönottotyypit</span><span class="sxs-lookup"><span data-stu-id="a670b-117">Deployment types</span></span>
<span data-ttu-id="a670b-118">Project Operations tukee useita eri toteutusvaihtoehtoja tarpeidesi mukaan.</span><span class="sxs-lookup"><span data-stu-id="a670b-118">Project Operations supports multiple deployment options to match your requirements.</span></span> <span data-ttu-id="a670b-119">Olitpa uusi tai nykyinen Dynamics 365 -asiakas, Project Operations voit tukea tarpeitasi.</span><span class="sxs-lookup"><span data-stu-id="a670b-119">Whether you're a new or existing Dynamics 365 customer, Project Operations can support your needs.</span></span>

<span data-ttu-id="a670b-120">[Käyttöönottokyselyn](https://aka.ms/provisionprojectoperations) avulla voit määrittää oikean käyttöönottotavan.</span><span class="sxs-lookup"><span data-stu-id="a670b-120">Our [Deployment questionnaire](https://aka.ms/provisionprojectoperations) will help you determine the right deployment.</span></span> <span data-ttu-id="a670b-121">Tulokset opastavat sinua kohti jotakin seuraavista käyttöönottotyypeistä:</span><span class="sxs-lookup"><span data-stu-id="a670b-121">The results will guide you toward one of the following deployment types:</span></span>

- [<span data-ttu-id="a670b-122">Lite-käyttöönotto – kauppa proformalaskutukseen</span><span class="sxs-lookup"><span data-stu-id="a670b-122">Lite deployment – deal to proforma invoicing</span></span>](#lite)
- [<span data-ttu-id="a670b-123">Project Operations resurssien ja ei-varastoitavien skenaarioissa</span><span class="sxs-lookup"><span data-stu-id="a670b-123">Project Operations for resource/non-stocked scenarios</span></span>](#integrated)
- [<span data-ttu-id="a670b-124">Project Operations varastoitavien/tuotantotilausten skenaarioissa</span><span class="sxs-lookup"><span data-stu-id="a670b-124">Project Operations for stocked/production order scenarios</span></span>](#pma)

<span data-ttu-id="a670b-125">Project Operations tukee varastoitu/tuotantotilaus-skenaarioita ja ei-varastoitavia/resurssipohjaisia skenaarioita samassa ympäristössä yritystason määritysten avulla.</span><span class="sxs-lookup"><span data-stu-id="a670b-125">Project Operations support stocked/production order scenarios and non-stocked/resource-based scenarios on the same environment through legal entity-level configurations.</span></span> <span data-ttu-id="a670b-126">Esimerkiksi Contoso voi käyttää varastossa olevaa/tuotantotilaus-ominaisuuksia Yhdysvaltain tuotantolaitoksellaan (Yritys = Contoso Manufacturing United States).</span><span class="sxs-lookup"><span data-stu-id="a670b-126">For example, Contoso can use the stocked/production order capabilities in their US manufacturing facility (Legal entity = Contoso Manufacturing United States).</span></span> <span data-ttu-id="a670b-127">Contoso voi käyttää ei-varastoituita tai resurssipohjaisia ominaisuuksia Contoso Robotics Arms -huoltolaitoksellaan Yhdistyneessä kuningaskunnassa (Yritys = Contoso Robotics United Kingdom).</span><span class="sxs-lookup"><span data-stu-id="a670b-127">Contoso can use the non-stocked/resource-based capabilities in their Contoso Robotics Arms servicing facility in UK (Legal entity = Contoso Robotics United Kingdom).</span></span>

### <a name="lite-deployment---deal-to-proforma-invoicing"></a><a  name="lite"></a><span data-ttu-id="a670b-128">Lite-käyttöönotto – kauppa proformalaskutukseen</span><span class="sxs-lookup"><span data-stu-id="a670b-128">Lite deployment - deal to proforma invoicing</span></span>

<span data-ttu-id="a670b-129">Lite-käyttöönotossa on seuraavat ominaisuudet:</span><span class="sxs-lookup"><span data-stu-id="a670b-129">The lite deployment includes the following capabilities:</span></span>

- <span data-ttu-id="a670b-130">Dynamics 365 Sales -sovelluksen kokemuksia laajentava projektien myyntiprosessi</span><span class="sxs-lookup"><span data-stu-id="a670b-130">Sales process for projects that extends Dynamics 365 Sales application experiences</span></span>
- <span data-ttu-id="a670b-131">Projektin suunnittelu Microsoft Project -verkkoversion avulla</span><span class="sxs-lookup"><span data-stu-id="a670b-131">Project planning using Microsoft Project for the Web</span></span>
- <span data-ttu-id="a670b-132">Moniulotteinen hinnoittelu</span><span class="sxs-lookup"><span data-stu-id="a670b-132">Multi-dimensional pricing</span></span>
- <span data-ttu-id="a670b-133">Yhdistetty resurssien hallinta</span><span class="sxs-lookup"><span data-stu-id="a670b-133">Unified resource management</span></span>
- <span data-ttu-id="a670b-134">Aikaseuranta</span><span class="sxs-lookup"><span data-stu-id="a670b-134">Time tracking</span></span>
- <span data-ttu-id="a670b-135">Peruskulu</span><span class="sxs-lookup"><span data-stu-id="a670b-135">Basic expense</span></span>
- <span data-ttu-id="a670b-136">Projektipäällikön tarkistusten ja muokkausten proformalaskutus</span><span class="sxs-lookup"><span data-stu-id="a670b-136">Proforma invoicing for Project manager's review and edits</span></span> 

#### <a name="deployment-steps"></a><span data-ttu-id="a670b-137">Käyttöönotto-ohjeet</span><span class="sxs-lookup"><span data-stu-id="a670b-137">Deployment steps</span></span>
<span data-ttu-id="a670b-138">Määritä paras Project Operationsin käyttöönottomalli käyttämällä [Käyttöönottokyselyä](https://aka.ms/provisionprojectoperations).</span><span class="sxs-lookup"><span data-stu-id="a670b-138">Determine the best deployment model of Project Operations using the [Deployment questionnaire](https://aka.ms/provisionprojectoperations).</span></span>

<span data-ttu-id="a670b-139">Lisätietoja tälle käyttöönotolle: [Esiversiotilauksiin rekisteröityminen](lite-preview-subscription-sign-up.md) ja [Uuden ympäristön valmistelu](lite-deployment.md).</span><span class="sxs-lookup"><span data-stu-id="a670b-139">For this deployment, see [Sign-up for preview subscriptions](lite-preview-subscription-sign-up.md) and [Provision new environment](lite-deployment.md).</span></span> 


### <a name="project-operations-for-resourcenon-stocked-scenarios"></a><a name="integrated"></a><span data-ttu-id="a670b-140">Project Operations resurssien ja ei-varastoitavien skenaarioissa</span><span class="sxs-lookup"><span data-stu-id="a670b-140">Project Operations for resource/non-stocked scenarios</span></span>
<span data-ttu-id="a670b-141">Project Operations tarjoaa resurssien/ei-varastoitavien skenaarioille seuraavat ominaisuudet:</span><span class="sxs-lookup"><span data-stu-id="a670b-141">The Project Operations for resource/non-stocked scenarios includes the following capabilities:</span></span>
 
- <span data-ttu-id="a670b-142">Dynamics 365 Sales -sovellusta laajentava projektien myyntiprosessi</span><span class="sxs-lookup"><span data-stu-id="a670b-142">Sales process for projects that extends the Dynamics 365 Sales application</span></span>
- <span data-ttu-id="a670b-143">Projektin suunnittelu Microsoft Project -verkkoversion avulla</span><span class="sxs-lookup"><span data-stu-id="a670b-143">Project planning using Microsoft Project for the Web</span></span>
- <span data-ttu-id="a670b-144">Moniulotteinen hinnoittelu</span><span class="sxs-lookup"><span data-stu-id="a670b-144">Multi-dimensional pricing</span></span>
- <span data-ttu-id="a670b-145">Yhdistetty resurssien hallinta</span><span class="sxs-lookup"><span data-stu-id="a670b-145">Unified resource management</span></span>
- <span data-ttu-id="a670b-146">Aikaseuranta</span><span class="sxs-lookup"><span data-stu-id="a670b-146">Time tracking</span></span>
- <span data-ttu-id="a670b-147">Peruskulu</span><span class="sxs-lookup"><span data-stu-id="a670b-147">Basic expense</span></span>
- <span data-ttu-id="a670b-148">Koko kulu</span><span class="sxs-lookup"><span data-stu-id="a670b-148">Full expense</span></span>
- <span data-ttu-id="a670b-149">Kuittien OCR</span><span class="sxs-lookup"><span data-stu-id="a670b-149">Receipt OCR</span></span>
- <span data-ttu-id="a670b-150">Proformalaskutus ja asiakkaille suunnattu laskutus</span><span class="sxs-lookup"><span data-stu-id="a670b-150">Proforma and customer-facing invoicing</span></span> 
- <span data-ttu-id="a670b-151">Projektien tuloutus</span><span class="sxs-lookup"><span data-stu-id="a670b-151">Revenue recognition for projects</span></span>

#### <a name="deployment-steps"></a><span data-ttu-id="a670b-152">Käyttöönotto-ohjeet</span><span class="sxs-lookup"><span data-stu-id="a670b-152">Deployment steps</span></span>
<span data-ttu-id="a670b-153">Määritä paras Project Operationsin käyttöönottomalli käyttämällä [Käyttöönottokyselyä](https://aka.ms/provisionprojectoperations).</span><span class="sxs-lookup"><span data-stu-id="a670b-153">Determine the best deployment model of Project Operations using the [Deployment questionnaire](https://aka.ms/provisionprojectoperations).</span></span>

<span data-ttu-id="a670b-154">Lisätietoja tälle käyttöönotolle: [Esiversiotilauksiin rekisteröityminen](resource-sign-up-preview-subscription.md) ja [Uuden ympäristön valmistelu](resource-provision-new-environment.md).</span><span class="sxs-lookup"><span data-stu-id="a670b-154">For this deployment, see [Sign-up for preview subscriptions](resource-sign-up-preview-subscription.md) and [Provision new environment](resource-provision-new-environment.md).</span></span> 


### <a name="project-operations-for-stockedproduction-order-scenarios"></a><a name="pma"></a><span data-ttu-id="a670b-155">Project Operations varastoitavien/tuotantotilausten skenaarioissa</span><span class="sxs-lookup"><span data-stu-id="a670b-155">Project Operations for stocked/production order scenarios</span></span>

- <span data-ttu-id="a670b-156">Projektin suunnittelu työrakenteen avulla</span><span class="sxs-lookup"><span data-stu-id="a670b-156">Project planning using WBS</span></span>
- <span data-ttu-id="a670b-157">Resurssien hallinta</span><span class="sxs-lookup"><span data-stu-id="a670b-157">Resource management</span></span>
- <span data-ttu-id="a670b-158">Aikaseuranta</span><span class="sxs-lookup"><span data-stu-id="a670b-158">Time tracking</span></span>
- <span data-ttu-id="a670b-159">Koko kulu</span><span class="sxs-lookup"><span data-stu-id="a670b-159">Full expense</span></span>
- <span data-ttu-id="a670b-160">Kuittien OCR</span><span class="sxs-lookup"><span data-stu-id="a670b-160">Receipt OCR</span></span>
- <span data-ttu-id="a670b-161">Täysi laskutus</span><span class="sxs-lookup"><span data-stu-id="a670b-161">Full invoicing</span></span>
- <span data-ttu-id="a670b-162">Tuoton tunnistus</span><span class="sxs-lookup"><span data-stu-id="a670b-162">Revenue recognition</span></span>
- <span data-ttu-id="a670b-163">Tuotantotilaukset</span><span class="sxs-lookup"><span data-stu-id="a670b-163">Production orders</span></span>
- <span data-ttu-id="a670b-164">Varastomateriaalien tuki varastojen avulla</span><span class="sxs-lookup"><span data-stu-id="a670b-164">Stocked materials support with inventory</span></span>

#### <a name="deployment-steps"></a><span data-ttu-id="a670b-165">Käyttöönotto-ohjeet</span><span class="sxs-lookup"><span data-stu-id="a670b-165">Deployment steps</span></span>
<span data-ttu-id="a670b-166">Määritä paras Project Operationsin käyttöönottomalli käyttämällä [Käyttöönottokyselyä](https://aka.ms/provisionprojectoperations).</span><span class="sxs-lookup"><span data-stu-id="a670b-166">Determine the best deployment model of Project Operations using the [Deployment questionnaire](https://aka.ms/provisionprojectoperations).</span></span>

<span data-ttu-id="a670b-167">Lisätietoja tälle käyttöönotolle: [Esiversiotilauksiin rekisteröityminen](/dynamics365/fin-ops-core/dev-itpro/dev-tools/sign-up-preview-subscription?toc=%2fdynamics365%2ffinance%2ftoc.json) ja [Uuden ympäristön valmistelu](/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment?toc=%2fdynamics365%2ffinance%2ftoc.json).</span><span class="sxs-lookup"><span data-stu-id="a670b-167">For this deployment, see [Sign-up for preview subscriptions](/dynamics365/fin-ops-core/dev-itpro/dev-tools/sign-up-preview-subscription?toc=%2fdynamics365%2ffinance%2ftoc.json) and [Provision new environment](/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment?toc=%2fdynamics365%2ffinance%2ftoc.json).</span></span> 



[!INCLUDE[footer-include](../includes/footer-banner.md)]