---
title: Projektipohjaisten mahdollisuuksien hallinta
description: Tässä aiheessa on tietoja projekteihin liittyvien mahdollisuuksien käyttämisestä.
author: rumant
manager: Annbe
ms.date: 10/21/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 5ce9ad1458d338d63469c3d6fddb98b9cbbced31
ms.sourcegitcommit: 3d78338773929121d17ec3386f6cb67bfb2272cc
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/27/2021
ms.locfileid: "5948371"
---
# <a name="manage-project-based-opportunities"></a><span data-ttu-id="59986-103">Projektipohjaisten mahdollisuuksien hallinta</span><span class="sxs-lookup"><span data-stu-id="59986-103">Manage project-based opportunities</span></span>

<span data-ttu-id="59986-104">_**Koskee:** Project Operationsin resurssiin / muuhun kuin resurssiin perustuvia skenaarioita, Lite-käyttöönotto-kaupasta proformalaskutukseen_</span><span class="sxs-lookup"><span data-stu-id="59986-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="59986-105">Projektipohjaisten yritysten toimitustoiminnot on yleensä jaettu useisiin maihin ja maantieteellisille alueille.</span><span class="sxs-lookup"><span data-stu-id="59986-105">Project-based companies typically have their operations for delivery spread across multiple countries and geographies.</span></span> <span data-ttu-id="59986-106">Projektin toteutuksen ja toimituksen kustannukset voivat vaihdella sen mukaan, mikä paikkatieto tai divisioona hallitsee toimitusta.</span><span class="sxs-lookup"><span data-stu-id="59986-106">The cost of the project execution and delivery can vary  based on which geography or division manages the delivery.</span></span> <span data-ttu-id="59986-107">Tämä puolestaan voi vaikuttaa kaupan marginaaliin.</span><span class="sxs-lookup"><span data-stu-id="59986-107">In turn, this can impact the margins of the deal.</span></span> <span data-ttu-id="59986-108">Projektiin perustuvien palvelujen toimittamiseen liittyy yleensä suuria määriä henkilöresurssien aikaa, huomattavia matkakuluja, materiaalikustannuksia ja muita kuluja.</span><span class="sxs-lookup"><span data-stu-id="59986-108">Delivery of project-based services typically involves large quantities of human resource time, considerable expenses for travel, material costs, and other expenses.</span></span>

<span data-ttu-id="59986-109">Dynamics 365 Project Operationsin projektipohjaiset mahdollisuudet on suunniteltu sisältämään Dynamics 365 Salesin laajennuksia.</span><span class="sxs-lookup"><span data-stu-id="59986-109">Project-based opportunities in Dynamics 365 Project Operations are designed with extensions to Dynamics 365 Sales.</span></span> <span data-ttu-id="59986-110">Aihe sisältää tietoja projektipohjaisten yritysten tarvitsemista lisätoiminnoista eri kentissä ja liiketoimintalogiikasta, joilla hallitaan projektipohjaisia mahdollisuuksia.</span><span class="sxs-lookup"><span data-stu-id="59986-110">The topic provides details about the different fields and business logic included in the additional functionality that is required by project-based companies to manage project-based opportunities.</span></span>

## <a name="view-all-project-based-opportunities"></a><span data-ttu-id="59986-111">Näytä kaikki projektipohjaiset mahdollisuudet</span><span class="sxs-lookup"><span data-stu-id="59986-111">View all project-based opportunities</span></span>

<span data-ttu-id="59986-112">Luettelo kaikista projektipohjaisista mahdollisuuksista näkyy **mahdollisuus**-luettelosivulla.</span><span class="sxs-lookup"><span data-stu-id="59986-112">A list of all the project-based opportunities can be seen from the **Opportunity** list page.</span></span> 

1. <span data-ttu-id="59986-113">Siirry kohtaan **Myynti** > **Mahdollisuudet**.</span><span class="sxs-lookup"><span data-stu-id="59986-113">Go to **Sales** > **Opportunities**.</span></span>
2. <span data-ttu-id="59986-114">Valitse **Näkymien vaihtajasta** muut suodatetut näkymät mahdollisuuksista.</span><span class="sxs-lookup"><span data-stu-id="59986-114">Use the **View switcher** to select other filtered views of the opportunities.</span></span> <span data-ttu-id="59986-115">Voit luoda omia näkymiä, joissa on mukautettuja suodatusehtoja, näiden näkymien ja siirtymisvaihtoehtojen määrittämistä varten.</span><span class="sxs-lookup"><span data-stu-id="59986-115">You can create your own views with custom filter criteria to configure these views and navigation options.</span></span>

<span data-ttu-id="59986-116">Tämän luettelosivun tai tietosivun avulla voit luoda tai poistaa projektimahdollisuuksia.</span><span class="sxs-lookup"><span data-stu-id="59986-116">Project Opportunities can be created or deleted from this list page or the detail page.</span></span>

## <a name="business-process-flow-for-project-based-deals"></a><span data-ttu-id="59986-117">Projektiin perustuvien tarjousten liiketoimintaprosessi</span><span class="sxs-lookup"><span data-stu-id="59986-117">Business process flow for project-based deals</span></span>

<span data-ttu-id="59986-118">Seuraavat liiketoimintaprosessit ovat tuettuja Project Operationsin projektipohjaisille sopimuksille:</span><span class="sxs-lookup"><span data-stu-id="59986-118">The following business process flows are supported for project-based deals in Project Operations:</span></span>

- <span data-ttu-id="59986-119">Liidistä mahdollisuudeksi -liiketoimintaprosessi</span><span class="sxs-lookup"><span data-stu-id="59986-119">Lead to Opportunity business process</span></span>
- <span data-ttu-id="59986-120">Mahdollisuuden myynti prosessi</span><span class="sxs-lookup"><span data-stu-id="59986-120">Opportunity sales process</span></span>

### <a name="lead-to-opportunity-business-process"></a><span data-ttu-id="59986-121">Liidistä mahdollisuudeksi -liiketoimintaprosessi</span><span class="sxs-lookup"><span data-stu-id="59986-121">Lead to opportunity business process</span></span> 
<span data-ttu-id="59986-122">Liidistä mahdollisuudeksi -liiketoimintaprosessi tukee seuraavia vaiheita:</span><span class="sxs-lookup"><span data-stu-id="59986-122">The lead to opportunity business process supports the following stages:</span></span>

| <span data-ttu-id="59986-123">Vaihe</span><span class="sxs-lookup"><span data-stu-id="59986-123">Stage</span></span> | <span data-ttu-id="59986-124">Yhdistetty entiteetti</span><span class="sxs-lookup"><span data-stu-id="59986-124">Mapped entity</span></span> | <span data-ttu-id="59986-125">Toiminnallisuus</span><span class="sxs-lookup"><span data-stu-id="59986-125">Functionality</span></span> |
| --- | --- | --- |
| <span data-ttu-id="59986-126">Hyväksy</span><span class="sxs-lookup"><span data-stu-id="59986-126">Qualify</span></span> | <span data-ttu-id="59986-127">Liidi</span><span class="sxs-lookup"><span data-stu-id="59986-127">Lead</span></span> | <span data-ttu-id="59986-128">Hyväksy liidi, jotta luodaan asiakkuus, yhteyshenkilö ja mahdollisuus.</span><span class="sxs-lookup"><span data-stu-id="59986-128">Qualify the lead to create an account, contact, and an opportunity.</span></span> |
| <span data-ttu-id="59986-129">Kehitä</span><span class="sxs-lookup"><span data-stu-id="59986-129">Develop</span></span> | <span data-ttu-id="59986-130">Mahdollisuus</span><span class="sxs-lookup"><span data-stu-id="59986-130">Opportunity</span></span> | <span data-ttu-id="59986-131">Kehitä mahdollisuutta lisäämällä tietoja liittyvistä töistä, keskeisistä sidosryhmistä ja kilpailijoista.</span><span class="sxs-lookup"><span data-stu-id="59986-131">Develop the opportunity to add more information on the work involved, key stakeholders, and competition.</span></span> |
| <span data-ttu-id="59986-132">Ehdota</span><span class="sxs-lookup"><span data-stu-id="59986-132">Propose</span></span> | <span data-ttu-id="59986-133">Mahdollisuus</span><span class="sxs-lookup"><span data-stu-id="59986-133">Opportunity</span></span> | <span data-ttu-id="59986-134">Laadi ehdotus ja hanki hyväksyntä sisäiseltä tarkistusryhmältä.</span><span class="sxs-lookup"><span data-stu-id="59986-134">Develop the proposal and get approval from the internal review team.</span></span> |
| <span data-ttu-id="59986-135">Sulje</span><span class="sxs-lookup"><span data-stu-id="59986-135">Close</span></span> | <span data-ttu-id="59986-136">Mahdollisuus</span><span class="sxs-lookup"><span data-stu-id="59986-136">Opportunity</span></span> | <span data-ttu-id="59986-137">Kun mahdollisuus voitetaan, sopimus suljetaan.</span><span class="sxs-lookup"><span data-stu-id="59986-137">Win the opportunity to close the deal.</span></span> |

### <a name="opportunity-sales-process"></a><span data-ttu-id="59986-138">Mahdollisuuden myynti prosessi</span><span class="sxs-lookup"><span data-stu-id="59986-138">Opportunity sales process</span></span>
<span data-ttu-id="59986-139">Project Operationsin mahdollisuuden myyntiprosessi on laajennusmahdollisuus myyntiprosessin liiketoimintavirtaan myyntisovelluksessa.</span><span class="sxs-lookup"><span data-stu-id="59986-139">The Opportunity sales process in Project Operations is an extension to the Opportunity sales process business flow in the Sales application.</span></span> <span data-ttu-id="59986-140">Tämä liiketoimintaprosessi on suunniteltu siten, että se tukee seuraavia projektipohjaisen mahdollisuuden vaiheita.</span><span class="sxs-lookup"><span data-stu-id="59986-140">This business process is designed out-of-the-box to support the following stages in a project-based opportunity.</span></span>

| <span data-ttu-id="59986-141">Vaihe</span><span class="sxs-lookup"><span data-stu-id="59986-141">Stage</span></span> | <span data-ttu-id="59986-142">Yhdistetty entiteetti</span><span class="sxs-lookup"><span data-stu-id="59986-142">Mapped entity</span></span> | <span data-ttu-id="59986-143">Toiminnallisuus</span><span class="sxs-lookup"><span data-stu-id="59986-143">Functionality</span></span> |
| --- | --- | --- |
| <span data-ttu-id="59986-144">Hyväksy</span><span class="sxs-lookup"><span data-stu-id="59986-144">Qualify</span></span> | <span data-ttu-id="59986-145">Mahdollisuus</span><span class="sxs-lookup"><span data-stu-id="59986-145">Opportunity</span></span> | <span data-ttu-id="59986-146">Hyväksy liidi, jotta luodaan asiakkuus, yhteyshenkilö ja mahdollisuus.</span><span class="sxs-lookup"><span data-stu-id="59986-146">Qualify the lead to create an account, contact, and an opportunity.</span></span> |
| <span data-ttu-id="59986-147">Ehdota</span><span class="sxs-lookup"><span data-stu-id="59986-147">Propose</span></span> | <span data-ttu-id="59986-148">Tarjous</span><span class="sxs-lookup"><span data-stu-id="59986-148">Quote</span></span> | <span data-ttu-id="59986-149">Laadi ehdotus ja käyttämällä projektitarjouksia ja hanki hyväksyntä sisäiseltä tarkistusryhmältä.</span><span class="sxs-lookup"><span data-stu-id="59986-149">Develop the proposal using project quotes and get approval from the internal review team.</span></span> |
| <span data-ttu-id="59986-150">Sopimus</span><span class="sxs-lookup"><span data-stu-id="59986-150">Contract</span></span> | <span data-ttu-id="59986-151">Projektin palvelusopimus</span><span class="sxs-lookup"><span data-stu-id="59986-151">Project Contract</span></span> | <span data-ttu-id="59986-152">Voita tarjous, joka luo palvelusopimuksen ja aloittaa projektin toteutuksen ja toimituksen.</span><span class="sxs-lookup"><span data-stu-id="59986-152">Win the quote to create the contract and begin execution and delivery on the project.</span></span> |
| <span data-ttu-id="59986-153">Sulje</span><span class="sxs-lookup"><span data-stu-id="59986-153">Close</span></span> | <span data-ttu-id="59986-154">Projektin palvelusopimus</span><span class="sxs-lookup"><span data-stu-id="59986-154">Project Contract</span></span> | <span data-ttu-id="59986-155">Viimeistele työn onnistuminen ja sulje projektisopimus.</span><span class="sxs-lookup"><span data-stu-id="59986-155">Finish the work successfully and close the project contract.</span></span> |

> [!NOTE]
> <span data-ttu-id="59986-156">Jos projektipohjainen sopimus on käynnistetty liidistä, mahdollisuus liiketoimintaprosessiin on etusijalla.</span><span class="sxs-lookup"><span data-stu-id="59986-156">If your project-based deal started with a Lead, the Lead to Opportunity business process takes precedence.</span></span>
>
> <span data-ttu-id="59986-157">Jos projektipohjainen sopimus on käynnistetty mahdollisuudesta, mahdollisuuden myyntiprosessiin on etusijalla.</span><span class="sxs-lookup"><span data-stu-id="59986-157">If your project-based deal started with an Opportunity, the Opportunity sales process takes precedence.</span></span>

<span data-ttu-id="59986-158">Voit muokata tuote liiketoimintaprosessin työnkulkua tai luoda omia liiketoimintaprosessien työnkulkuja, joilla voit seurata myyntiprosessia tarpeen mukaan.</span><span class="sxs-lookup"><span data-stu-id="59986-158">You can edit the product business process flow or create your own business process flows to track your sales process as needed.</span></span> <span data-ttu-id="59986-159">Lisätietoja liiketoimintaprosesseista on aiheessa [liiketoimintaprosessin kulun yleiskatsaus](/dynamics365/customerengagement/on-premises/customize/business-process-flows-overview).</span><span class="sxs-lookup"><span data-stu-id="59986-159">For more information about the business process flow, see [Business process flows overview](/dynamics365/customerengagement/on-premises/customize/business-process-flows-overview).</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]