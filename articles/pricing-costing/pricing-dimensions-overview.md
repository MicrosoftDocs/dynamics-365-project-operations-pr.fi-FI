---
title: Hinnoitteludimensioiden yleiskatsaus
description: Tämä aihe tarjoaa tietoja Dynamics 365 Project Operationsin hinnoitteludimensioista.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: fe2ab3a1b12c00e346e27709d66b5a0cb81a3b56
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/28/2020
ms.locfileid: "3898212"
---
# <a name="pricing-dimensions-overview"></a><span data-ttu-id="1235a-103">Hinnoitteludimensioiden yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="1235a-103">Pricing dimensions overview</span></span>

<span data-ttu-id="1235a-104">_**Koskee:** Project Operationsin resurssiin / muuhun kuin resurssiin perustuvia skenaarioita, Lite-käyttöönotto-kaupasta proformalaskutukseen_</span><span class="sxs-lookup"><span data-stu-id="1235a-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="1235a-105">Henkilöresursseissa hinnoittelun ja kustannusten määrittämiseen käytettävät dimensiot jaetaan kahteen luokkaan:</span><span class="sxs-lookup"><span data-stu-id="1235a-105">The dimensions that are used in human resources to set up pricing and costs fall into two categories:</span></span>

- <span data-ttu-id="1235a-106">Henkilöt</span><span class="sxs-lookup"><span data-stu-id="1235a-106">People</span></span>
- <span data-ttu-id="1235a-107">Suunniteltu työ</span><span class="sxs-lookup"><span data-stu-id="1235a-107">Planned work</span></span>

<span data-ttu-id="1235a-108">Tämän vuoksi käytettävissä on seuraavat kaksi hinnoitteludimensioarvoa:</span><span class="sxs-lookup"><span data-stu-id="1235a-108">Because of this, there are two types of pricing dimension values available:</span></span>

- <span data-ttu-id="1235a-109">**Asetusjoukot**: Dimensioita, jotka ovat arvojoukon kiinteitä luettelointeja.</span><span class="sxs-lookup"><span data-stu-id="1235a-109">**Option sets**: Dimensions that are fixed enumerations for a set of values.</span></span>
- <span data-ttu-id="1235a-110">**Entiteettiperusteiset arvot**: Dimensioita, jotka voivat olla vaihtelevia arvojoukkoja.</span><span class="sxs-lookup"><span data-stu-id="1235a-110">**Entity-based values**: Dimensions that can be a varied set of values.</span></span>

## <a name="pricing-dimensions"></a><span data-ttu-id="1235a-111">Hinnoitteludimensiot</span><span class="sxs-lookup"><span data-stu-id="1235a-111">Pricing dimensions</span></span>

<span data-ttu-id="1235a-112">Dynamics 365 Project Operations sisältää hinnoitteludimensioiden oletusjoukon.</span><span class="sxs-lookup"><span data-stu-id="1235a-112">Dynamics 365 Project Operations ships with a default set of pricing dimensions.</span></span> <span data-ttu-id="1235a-113">Hinnoitteludimensioita voi tarkastella siirtymällä kohtaan **Project Operations** > **Parametrit**.</span><span class="sxs-lookup"><span data-stu-id="1235a-113">You can view these pricing dimensions by going to **Project Operations** > **Parameters**.</span></span> <span data-ttu-id="1235a-114">Varmista parametritietueen **Summaperusteiset hinnoitteludimensiot** -välilehdellä, että roolin **msdyn_resourcecategory** ja resursoivan organisaatioyksikön **msdyn_organizationalunit** kenttien **Sovelletaan myyntiin** ja **Sovelletaan kustannuksiin** arvona on **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="1235a-114">In the parameter record, on the **Amount-based pricing dimensions** tab, verify that the role, **msdyn_resourcecategory** and resourcing organizational unit, **msdyn_organizationalunit** have the fields **Applicable to sales** and **Applicable to cost** set to **Yes**.</span></span> <span data-ttu-id="1235a-115">Näiden käytössä olevien kenttien avulla voit määrittää jokaisen roolin ja organisaatioyksikön hinnan ja kustannuksen.</span><span class="sxs-lookup"><span data-stu-id="1235a-115">With these fields enabled, you can set up the price and cost for each role and organizational unit combination.</span></span>

<span data-ttu-id="1235a-116">Jos sinun on määritettävä resurssiesi hintoja tai kustannuksia lisämääritteitä käyttäen, voit luoda mukautettuja kenttiä, entiteettejä ja dimensioita.</span><span class="sxs-lookup"><span data-stu-id="1235a-116">If you need to price or cost for your resources using additional attributes, you can create customized fields, entities, and dimensions.</span></span>

## <a name="pricing-human-resource-time"></a><span data-ttu-id="1235a-117">Henkilöresurssin ajan hinnoitteleminen</span><span class="sxs-lookup"><span data-stu-id="1235a-117">Pricing human resource time</span></span>
<span data-ttu-id="1235a-118">Organisaation tapa hinnoitella henkilöresurssien aika on usein tärkeä strateginen näkökohta, joka vaikuttaa suoraan organisaation kannattavuuteen.</span><span class="sxs-lookup"><span data-stu-id="1235a-118">How an organization prices human resource time is often an important strategic consideration that directly affects the organization's profitability.</span></span> <span data-ttu-id="1235a-119">Tee yhteistyötä talousryhmän ja ammattialan päälliköiden kanssa, kun organisaatiosi on valmis päättämään, miten se haluaa määrittää henkilöresurssien ajan laskutus- ja kustannushinnat.</span><span class="sxs-lookup"><span data-stu-id="1235a-119">Work with the finance teams and practice heads when your organization is ready to identify how it wants to set up bill and cost rates for human resource time.</span></span>

<span data-ttu-id="1235a-120">Muita hinnoittelussa huomioitavia seikkoja ovat se, käytetäänkö sellaisia kenttiä tai entiteettejä uudelleen, jotka eivät tällä hetkellä ole hinnoitteludimensioita mutta soveltuvat organisaation hinnoitteludimensioiksi.</span><span class="sxs-lookup"><span data-stu-id="1235a-120">Other considerations for pricing include whether to re-use fields or entities that are not currently pricing dimensions but apply as a pricing dimension for your organization.</span></span> <span data-ttu-id="1235a-121">Mahdollisia dimensioita ovat esimerkiksi kentät **Tapahtumaluokka** (**msdyn_transactioncategory**) ja **Varattavissa oleva resurssi** (**bookableresource**).</span><span class="sxs-lookup"><span data-stu-id="1235a-121">Fields like **Transaction Category** (**msdyn_transactioncategory**) and **Bookable Resource** (**bookableresource**) are examples of candidate dimensions.</span></span> 

<span data-ttu-id="1235a-122">Mieti, pitäisikö hinnoitteludimension olla taulukko vai asetusjoukko.</span><span class="sxs-lookup"><span data-stu-id="1235a-122">Consider whether your pricing dimension should be a table or an option set.</span></span> <span data-ttu-id="1235a-123">Jos odotettavissa on muutoksia dimension arvioihin, jotka ylittävät 10 tai 12, ja tarvitset lisämääritteitä kyseisille arvoille, voit luoda entiteetin asetusjoukon sijaan.</span><span class="sxs-lookup"><span data-stu-id="1235a-123">If you foresee changes to the values of a dimension which will exceed 10 or 12 and you need additional attributes on these values, you could create an entity rather than an option set.</span></span> <span data-ttu-id="1235a-124">Asetusjoukon ylläpitotoimiin, kuten arvojen lisäämiseen, tarvitaan järjestelmänvalvoja tai kehittäjä, kun taas useimmat käyttäjät pystyvät lisäämään uusia rivejä taulukkoon.</span><span class="sxs-lookup"><span data-stu-id="1235a-124">Maintaining an option set, such as adding or removing values, requires an admin or developer whereas adding new rows to a table can be done by most users.</span></span>

<span data-ttu-id="1235a-125">Seuraavassa esimerkissä esitetään laskutushintoja, jotka määritetään roolin ja sen resursoivan organisaatioyksikön perusteella, johon resurssi kuuluu.</span><span class="sxs-lookup"><span data-stu-id="1235a-125">The following example shows bill rates that are set up based on the role and the resourcing org unit to which the resource belongs.</span></span> <span data-ttu-id="1235a-126">Kustannushinnat perustuvat yleensä työntekijän ja hänen organisaatioyksikkönsä palkkaluokkiin.</span><span class="sxs-lookup"><span data-stu-id="1235a-126">Cost rates are typically based on the salary band of the employee and the org unit that they belong to.</span></span> <span data-ttu-id="1235a-127">Tässä esimerkissä laskutushinnan ja kustannushinnan taulukot näyttävät seuraavalta.</span><span class="sxs-lookup"><span data-stu-id="1235a-127">In this example, the bill rate and cost rate tables will look like the following.</span></span>

<span data-ttu-id="1235a-128">**Esimerkkilaskutushinnat**</span><span class="sxs-lookup"><span data-stu-id="1235a-128">**Sample bill rates**</span></span>

| <span data-ttu-id="1235a-129">Rooli</span><span class="sxs-lookup"><span data-stu-id="1235a-129">Role</span></span>        | <span data-ttu-id="1235a-130">Organisaatioyksikkö</span><span class="sxs-lookup"><span data-stu-id="1235a-130">Org Unit</span></span>    |<span data-ttu-id="1235a-131">Yksikkö</span><span class="sxs-lookup"><span data-stu-id="1235a-131">Unit</span></span>      |<span data-ttu-id="1235a-132">Hinta</span><span class="sxs-lookup"><span data-stu-id="1235a-132">Price</span></span>      |<span data-ttu-id="1235a-133">Valuutta</span><span class="sxs-lookup"><span data-stu-id="1235a-133">Currency</span></span>  |
| ------------|-------------|----------|----------:|----------|
| <span data-ttu-id="1235a-134">Kehittäjä</span><span class="sxs-lookup"><span data-stu-id="1235a-134">Developer</span></span>   | <span data-ttu-id="1235a-135">Contoso US</span><span class="sxs-lookup"><span data-stu-id="1235a-135">Contoso US</span></span>  |<span data-ttu-id="1235a-136">Hour</span><span class="sxs-lookup"><span data-stu-id="1235a-136">Hour</span></span> | <span data-ttu-id="1235a-137">200</span><span class="sxs-lookup"><span data-stu-id="1235a-137">200</span></span>|<span data-ttu-id="1235a-138">USD</span><span class="sxs-lookup"><span data-stu-id="1235a-138">USD</span></span>     |
| <span data-ttu-id="1235a-139">Kehittäjä</span><span class="sxs-lookup"><span data-stu-id="1235a-139">Developer</span></span>   | <span data-ttu-id="1235a-140">Contoso India</span><span class="sxs-lookup"><span data-stu-id="1235a-140">Contoso India</span></span> |<span data-ttu-id="1235a-141">Hour</span><span class="sxs-lookup"><span data-stu-id="1235a-141">Hour</span></span>|   <span data-ttu-id="1235a-142">112</span><span class="sxs-lookup"><span data-stu-id="1235a-142">112</span></span>|<span data-ttu-id="1235a-143">USD</span><span class="sxs-lookup"><span data-stu-id="1235a-143">USD</span></span>     |


<span data-ttu-id="1235a-144">**Esimerkkikustannushinnat**</span><span class="sxs-lookup"><span data-stu-id="1235a-144">**Sample cost rates**</span></span>

| <span data-ttu-id="1235a-145">Palkkaluokat</span><span class="sxs-lookup"><span data-stu-id="1235a-145">Salary Band</span></span>     | <span data-ttu-id="1235a-146">Organisaatioyksikkö</span><span class="sxs-lookup"><span data-stu-id="1235a-146">Org Unit</span></span>    |<span data-ttu-id="1235a-147">Yksikkö</span><span class="sxs-lookup"><span data-stu-id="1235a-147">Unit</span></span>      |<span data-ttu-id="1235a-148">Hinta</span><span class="sxs-lookup"><span data-stu-id="1235a-148">Price</span></span>      |<span data-ttu-id="1235a-149">Valuutta</span><span class="sxs-lookup"><span data-stu-id="1235a-149">Currency</span></span>  |
| ----------------|-------------|----------|----------:|----------|
| <span data-ttu-id="1235a-150">Oma company_Band1</span><span class="sxs-lookup"><span data-stu-id="1235a-150">My company_Band1</span></span> | <span data-ttu-id="1235a-151">Contoso US</span><span class="sxs-lookup"><span data-stu-id="1235a-151">Contoso US</span></span>  |<span data-ttu-id="1235a-152">Hour</span><span class="sxs-lookup"><span data-stu-id="1235a-152">Hour</span></span> | <span data-ttu-id="1235a-153">145</span><span class="sxs-lookup"><span data-stu-id="1235a-153">145</span></span>|<span data-ttu-id="1235a-154">USD</span><span class="sxs-lookup"><span data-stu-id="1235a-154">USD</span></span>     |
| <span data-ttu-id="1235a-155">Oma company_Band2</span><span class="sxs-lookup"><span data-stu-id="1235a-155">My company_Band2</span></span> | <span data-ttu-id="1235a-156">Contoso India</span><span class="sxs-lookup"><span data-stu-id="1235a-156">Contoso India</span></span> |<span data-ttu-id="1235a-157">Hour</span><span class="sxs-lookup"><span data-stu-id="1235a-157">Hour</span></span>|   <span data-ttu-id="1235a-158">67</span><span class="sxs-lookup"><span data-stu-id="1235a-158">67</span></span>|<span data-ttu-id="1235a-159">USD</span><span class="sxs-lookup"><span data-stu-id="1235a-159">USD</span></span>     |
