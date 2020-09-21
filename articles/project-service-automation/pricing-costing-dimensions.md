---
title: Hinnoittelu- ja kustannusdimensioiden aloitussivu
description: Tämä aihe sisältää yleiskatsauksen hinnoitteludimensioihin.
author: rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 11/19/2018
ms.topic: article
ms.prod: Project Service
ms.service: business-applications
ms.assetid: 425d7bb8-9015-4f67-b9c9-cf3602e9afe8
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
ms.openlocfilehash: 2379d0d2e038f28a1a8df87a851e9bf7db7fe33f
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/24/2020
ms.locfileid: "3751156"
---
# <a name="pricing-and-costing-dimensions-home-page"></a><span data-ttu-id="525e4-103">Hinnoittelu- ja kustannusdimensioiden aloitussivu</span><span class="sxs-lookup"><span data-stu-id="525e4-103">Pricing and costing dimensions home page</span></span>

<span data-ttu-id="525e4-104">Henkilöresursseissa hinnoittelun ja kustannusten määrittämiseen käytettävät dimensiot jaetaan kahteen luokkaan:</span><span class="sxs-lookup"><span data-stu-id="525e4-104">The dimensions that are used in human resources to set up pricing and costs fall into two categories:</span></span>

- <span data-ttu-id="525e4-105">Henkilöt</span><span class="sxs-lookup"><span data-stu-id="525e4-105">People</span></span>
- <span data-ttu-id="525e4-106">Suunniteltu työ</span><span class="sxs-lookup"><span data-stu-id="525e4-106">Planned work</span></span>

<span data-ttu-id="525e4-107">Tämän vuoksi Project Service Automationissa (PSA:ssa) on käytettävissä kahdenlaisia hinnoitteludimensioarvoja:</span><span class="sxs-lookup"><span data-stu-id="525e4-107">Because of this, there are two types of pricing dimension values available in Project Service Automation (PSA):</span></span> 

- <span data-ttu-id="525e4-108">**Asetusjoukot** – Dimensioita, jotka ovat arvojoukon kiinteitä luettelointeja.</span><span class="sxs-lookup"><span data-stu-id="525e4-108">**Option sets** - Dimensions that are fixed enumerations for a set of values.</span></span>
- <span data-ttu-id="525e4-109">**Entiteettiperusteiset arvot** – Dimensioita, jotka voivat olla vaihtelevia arvojoukkoja.</span><span class="sxs-lookup"><span data-stu-id="525e4-109">**Entity-based values** - Dimensions that can be a varied set of values.</span></span>

## <a name="pricing-dimensions"></a><span data-ttu-id="525e4-110">Hinnoitteludimensiot</span><span class="sxs-lookup"><span data-stu-id="525e4-110">Pricing dimensions</span></span>

<span data-ttu-id="525e4-111">PSA sisältää oletusjoukon hinnoitteludimensioita.</span><span class="sxs-lookup"><span data-stu-id="525e4-111">PSA ships with a default set of pricing dimensions.</span></span> <span data-ttu-id="525e4-112">Niitä voi tarkastella siirtymällä kohtaan **Project Service** > **Parametrit**.</span><span class="sxs-lookup"><span data-stu-id="525e4-112">You can view these by going to **Project Service** > **Parameters**.</span></span> <span data-ttu-id="525e4-113">Varmista parametritietueen **Summaperusteiset hinnoitteludimensiot** -välilehdellä, että roolin **msdyn_resourcecategory** ja resursoivan organisaatioyksikön **msdyn_organizationalunit** kenttien **Sovelletaan myyntiin** ja **Sovelletaan kustannuksiin** arvona on **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="525e4-113">In the parameter record, on the **Amount-based pricing dimensions** tab, verify that the role, **msdyn_resourcecategory** and resourcing organizational unit, **msdyn_organizationalunit** have the fields **Applicable to sales** and **Applicable to cost** set to **Yes**.</span></span> <span data-ttu-id="525e4-114">Tällöin voit määrittää jokaisen roolin ja organisaatioyksikön hinnan ja kustannuksen.</span><span class="sxs-lookup"><span data-stu-id="525e4-114">This will allow you to set up the price and cost for each role and organizational unit combination.</span></span>

![Näyttökuva Project Service -parametreista, joissa Sovelletaan myyntiin on korostettu](media/PS-OOB-parameters.png)

> [!IMPORTANT]
> <span data-ttu-id="525e4-116">Jos olet käyttänyt valmiita roolin ja organisaatioyksikön kenttiä hinnoitteludimensioina ennen PSA;n versiota 3, muutoksia ei ole havaittavissa.</span><span class="sxs-lookup"><span data-stu-id="525e4-116">If you have been the using out-of-the box fields of role and organizational unit as pricing dimensions prior to version 3 of PSA, there will not be any observable change.</span></span> <span data-ttu-id="525e4-117">Voit jatkaa Project Servicen käyttöä tavalliseen tapaan.</span><span class="sxs-lookup"><span data-stu-id="525e4-117">You can continue to use Project Service as usual.</span></span> 

<span data-ttu-id="525e4-118">Jos sinun on määritettävä resurssiesi hintoja tai kustannuksia lisämääritteitä käyttäen, voit luoda mukautettuja kenttiä, entiteettejä ja dimensioita.</span><span class="sxs-lookup"><span data-stu-id="525e4-118">If you need to price or cost for your resources using additional attributes, you can create customized fields, entities, and dimensions.</span></span> <span data-ttu-id="525e4-119">Lisätietoja saat seuraavista aiheista, mutta ota huomioon, että sinun on suoritettava toimenpidesarja alla näkyvässä järjestyksessä:</span><span class="sxs-lookup"><span data-stu-id="525e4-119">For more information, see the following topics, however note that you must complete the procedures in the order listed below:</span></span>

- [<span data-ttu-id="525e4-120">Mukautettujen kenttien ja entiteettien luominen</span><span class="sxs-lookup"><span data-stu-id="525e4-120">Create custom fields and entities</span></span>](create-custom-fields-entities.md)
- [<span data-ttu-id="525e4-121">Mukautettujen kenttien lisääminen hinta- ja tapahtumaentiteetteihin</span><span class="sxs-lookup"><span data-stu-id="525e4-121">Add custom fields to price setup and transactional entities</span></span>](field-references.md)
- [<span data-ttu-id="525e4-122">Mukautettujen kenttien määrittäminen hinnoitteludimensioiksi </span><span class="sxs-lookup"><span data-stu-id="525e4-122">Set up custom fields as pricing dimensions</span></span>](set-up-pricing-dimensions.md)
- [<span data-ttu-id="525e4-123">Päivitä laajennusmääritteet sisältämään uudet hinnoitteludimensiot</span><span class="sxs-lookup"><span data-stu-id="525e4-123">Update plug-in attributes to include new pricing dimensions</span></span>](update-plug-in-attributes.md)

## <a name="pricing-human-resource-time"></a><span data-ttu-id="525e4-124">Henkilöresurssin ajan hinnoitteleminen</span><span class="sxs-lookup"><span data-stu-id="525e4-124">Pricing human resource time</span></span>
<span data-ttu-id="525e4-125">Organisaation tapa hinnoitella henkilöresurssien aika on usein tärkeä strateginen näkökohta, joka vaikuttaa suoraan organisaation kannattavuuteen.</span><span class="sxs-lookup"><span data-stu-id="525e4-125">How an organization prices human resource time is often an important strategic consideration that directly affects the organization's profitability.</span></span> <span data-ttu-id="525e4-126">Tee yhteistyötä talousryhmän ja ammattialan päälliköiden kanssa, kun organisaatiosi on valmis päättämään, miten se haluaa määrittää henkilöresurssien ajan laskutus- ja kustannushinnat.</span><span class="sxs-lookup"><span data-stu-id="525e4-126">Work with the finance teams and practice heads when your organization is ready to identify how it wants to set up bill and cost rates for human resource time.</span></span>

<span data-ttu-id="525e4-127">Muita hinnoittelussa huomioitavia seikkoja ovat se, käytetäänkö sellaisia kenttiä tai entiteettejä uudelleen, jotka eivät tällä hetkellä ole hinnoitteludimensioita mutta soveltuvat organisaation hinnoitteludimensioiksi.</span><span class="sxs-lookup"><span data-stu-id="525e4-127">Other considerations for pricing include whether to re-use fields or entities that are not currently pricing dimensions but apply as a pricing dimension for your organization.</span></span> <span data-ttu-id="525e4-128">Mahdollisia dimensioita ovat esimerkiksi kentät **Tapahtumaluokka** (**msdyn_transactioncategory**) ja **Varattavissa oleva resurssi** (**bookableresource**).</span><span class="sxs-lookup"><span data-stu-id="525e4-128">Fields like **Transaction Category** (**msdyn_transactioncategory**) and **Bookable Resource** (**bookableresource**) are examples of candidate dimensions.</span></span> 

<span data-ttu-id="525e4-129">On myös päätettävä, pitäisikö hinnoitteludimension olla taulukko vai asetusjoukko.</span><span class="sxs-lookup"><span data-stu-id="525e4-129">You should also consider whether your pricing dimension should be a table or an option set.</span></span> <span data-ttu-id="525e4-130">Jos odotettavissa on muutoksia dimension arvioihin, jotka ylittävät 10 tai 12, ja tarvitset lisämääritteitä kyseisille arvoille, voit luoda entiteetin asetusjoukon sijaan.</span><span class="sxs-lookup"><span data-stu-id="525e4-130">If you foresee changes to the values of a dimension which will exceed 10 or 12 and you need additional attributes on these values, you could create an entity rather than an option set.</span></span> <span data-ttu-id="525e4-131">Asetusjoukon ylläpitotoimiin, kuten arvojen lisäämiseen, tarvitaan järjestelmänvalvoja tai kehittäjä, kun taas useimmat käyttäjät pystyvät lisäämään uusia rivejä taulukkoon.</span><span class="sxs-lookup"><span data-stu-id="525e4-131">Maintaining an option set, such as adding or removing values, requires an admin or developer whereas adding new rows to a table can be done by most users.</span></span>

<span data-ttu-id="525e4-132">Seuraavassa esimerkissä esitetään laskutushintoja, jotka määritetään roolin ja sen resursoivan organisaatioyksikön perusteella, johon resurssi kuuluu.</span><span class="sxs-lookup"><span data-stu-id="525e4-132">The following example shows bill rates that are set up based on the role and the resourcing org unit to which the resource belongs.</span></span> <span data-ttu-id="525e4-133">Kustannushinnat perustuvat yleensä työntekijän ja hänen organisaatioyksikkönsä palkkaluokkiin.</span><span class="sxs-lookup"><span data-stu-id="525e4-133">Cost rates are typically based on the salary band of the employee and the org unit that they belong to.</span></span> <span data-ttu-id="525e4-134">Tässä esimerkissä laskutushinnan ja kustannushinnan taulukot näyttävät seuraavalta.</span><span class="sxs-lookup"><span data-stu-id="525e4-134">In this example, the bill rate and cost rate tables will look like the following.</span></span>

<span data-ttu-id="525e4-135">**Esimerkkilaskutushinnat**</span><span class="sxs-lookup"><span data-stu-id="525e4-135">**Sample bill rates**</span></span>

| <span data-ttu-id="525e4-136">Rooli</span><span class="sxs-lookup"><span data-stu-id="525e4-136">Role</span></span>        | <span data-ttu-id="525e4-137">Organisaatioyksikkö</span><span class="sxs-lookup"><span data-stu-id="525e4-137">Org Unit</span></span>    |<span data-ttu-id="525e4-138">Yksikkö</span><span class="sxs-lookup"><span data-stu-id="525e4-138">Unit</span></span>      |<span data-ttu-id="525e4-139">Hinta</span><span class="sxs-lookup"><span data-stu-id="525e4-139">Price</span></span>      |<span data-ttu-id="525e4-140">Valuutta</span><span class="sxs-lookup"><span data-stu-id="525e4-140">Currency</span></span>  |
| ------------|-------------|----------|----------:|----------|
| <span data-ttu-id="525e4-141">Kehittäjä</span><span class="sxs-lookup"><span data-stu-id="525e4-141">Developer</span></span>   | <span data-ttu-id="525e4-142">Contoso US</span><span class="sxs-lookup"><span data-stu-id="525e4-142">Contoso US</span></span>  |<span data-ttu-id="525e4-143">Hour</span><span class="sxs-lookup"><span data-stu-id="525e4-143">Hour</span></span> | <span data-ttu-id="525e4-144">200</span><span class="sxs-lookup"><span data-stu-id="525e4-144">200</span></span>|<span data-ttu-id="525e4-145">USD</span><span class="sxs-lookup"><span data-stu-id="525e4-145">USD</span></span>     |
| <span data-ttu-id="525e4-146">Kehittäjä</span><span class="sxs-lookup"><span data-stu-id="525e4-146">Developer</span></span>   | <span data-ttu-id="525e4-147">Contoso India</span><span class="sxs-lookup"><span data-stu-id="525e4-147">Contoso India</span></span> |<span data-ttu-id="525e4-148">Hour</span><span class="sxs-lookup"><span data-stu-id="525e4-148">Hour</span></span>|   <span data-ttu-id="525e4-149">112</span><span class="sxs-lookup"><span data-stu-id="525e4-149">112</span></span>|<span data-ttu-id="525e4-150">USD</span><span class="sxs-lookup"><span data-stu-id="525e4-150">USD</span></span>     |


<span data-ttu-id="525e4-151">**Esimerkkikustannushinnat**</span><span class="sxs-lookup"><span data-stu-id="525e4-151">**Sample cost rates**</span></span>

| <span data-ttu-id="525e4-152">Palkkaluokat</span><span class="sxs-lookup"><span data-stu-id="525e4-152">Salary Band</span></span>     | <span data-ttu-id="525e4-153">Organisaatioyksikkö</span><span class="sxs-lookup"><span data-stu-id="525e4-153">Org Unit</span></span>    |<span data-ttu-id="525e4-154">Yksikkö</span><span class="sxs-lookup"><span data-stu-id="525e4-154">Unit</span></span>      |<span data-ttu-id="525e4-155">Hinta</span><span class="sxs-lookup"><span data-stu-id="525e4-155">Price</span></span>      |<span data-ttu-id="525e4-156">Valuutta</span><span class="sxs-lookup"><span data-stu-id="525e4-156">Currency</span></span>  |
| ----------------|-------------|----------|----------:|----------|
| <span data-ttu-id="525e4-157">Oma company_Band1</span><span class="sxs-lookup"><span data-stu-id="525e4-157">My company_Band1</span></span> | <span data-ttu-id="525e4-158">Contoso US</span><span class="sxs-lookup"><span data-stu-id="525e4-158">Contoso US</span></span>  |<span data-ttu-id="525e4-159">Hour</span><span class="sxs-lookup"><span data-stu-id="525e4-159">Hour</span></span> | <span data-ttu-id="525e4-160">145</span><span class="sxs-lookup"><span data-stu-id="525e4-160">145</span></span>|<span data-ttu-id="525e4-161">USD</span><span class="sxs-lookup"><span data-stu-id="525e4-161">USD</span></span>     |
| <span data-ttu-id="525e4-162">Oma company_Band2</span><span class="sxs-lookup"><span data-stu-id="525e4-162">My company_Band2</span></span> | <span data-ttu-id="525e4-163">Contoso India</span><span class="sxs-lookup"><span data-stu-id="525e4-163">Contoso India</span></span> |<span data-ttu-id="525e4-164">Hour</span><span class="sxs-lookup"><span data-stu-id="525e4-164">Hour</span></span>|   <span data-ttu-id="525e4-165">67</span><span class="sxs-lookup"><span data-stu-id="525e4-165">67</span></span>|<span data-ttu-id="525e4-166">USD</span><span class="sxs-lookup"><span data-stu-id="525e4-166">USD</span></span>     |
