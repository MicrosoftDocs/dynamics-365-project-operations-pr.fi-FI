---
title: Hinnoitteludimensioiden yleiskatsaus
description: Tämä aihe tarjoaa tietoja Dynamics 365 Project Operationsin hinnoitteludimensioista.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
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
ms.openlocfilehash: 6b1ebdc97ec4704ba256acb521c0f2e7c474940b
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/16/2020
ms.locfileid: "4075455"
---
# <a name="pricing-dimensions-overview"></a><span data-ttu-id="8d0da-103">Hinnoitteludimensioiden yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="8d0da-103">Pricing dimensions overview</span></span>

<span data-ttu-id="8d0da-104">_**Koskee:** Project Operationsin resurssiin / muuhun kuin resurssiin perustuvia skenaarioita, Lite-käyttöönotto-kaupasta proformalaskutukseen_</span><span class="sxs-lookup"><span data-stu-id="8d0da-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="8d0da-105">Henkilöresursseissa hinnoittelun ja kustannusten määrittämiseen käytettävät dimensiot jaetaan kahteen luokkaan:</span><span class="sxs-lookup"><span data-stu-id="8d0da-105">The dimensions that are used in human resources to set up pricing and costs fall into two categories:</span></span>

- <span data-ttu-id="8d0da-106">Henkilöt</span><span class="sxs-lookup"><span data-stu-id="8d0da-106">People</span></span>
- <span data-ttu-id="8d0da-107">Suunniteltu työ</span><span class="sxs-lookup"><span data-stu-id="8d0da-107">Planned work</span></span>

<span data-ttu-id="8d0da-108">Tämän vuoksi käytettävissä on seuraavat kaksi hinnoitteludimensioarvoa:</span><span class="sxs-lookup"><span data-stu-id="8d0da-108">Because of this, there are two types of pricing dimension values available:</span></span>

- <span data-ttu-id="8d0da-109">**Asetusjoukot** : Dimensioita, jotka ovat arvojoukon kiinteitä luettelointeja.</span><span class="sxs-lookup"><span data-stu-id="8d0da-109">**Option sets** : Dimensions that are fixed enumerations for a set of values.</span></span>
- <span data-ttu-id="8d0da-110">**Entiteettiperusteiset arvot** : Dimensioita, jotka voivat olla vaihtelevia arvojoukkoja.</span><span class="sxs-lookup"><span data-stu-id="8d0da-110">**Entity-based values** : Dimensions that can be a varied set of values.</span></span>

## <a name="pricing-dimensions"></a><span data-ttu-id="8d0da-111">Hinnoitteludimensiot</span><span class="sxs-lookup"><span data-stu-id="8d0da-111">Pricing dimensions</span></span>

<span data-ttu-id="8d0da-112">Dynamics 365 Project Operations sisältää hinnoitteludimensioiden oletusjoukon.</span><span class="sxs-lookup"><span data-stu-id="8d0da-112">Dynamics 365 Project Operations ships with a default set of pricing dimensions.</span></span> <span data-ttu-id="8d0da-113">Hinnoitteludimensioita voi tarkastella siirtymällä kohtaan **Project Operations** > **Parametrit**.</span><span class="sxs-lookup"><span data-stu-id="8d0da-113">You can view these pricing dimensions by going to **Project Operations** > **Parameters**.</span></span> <span data-ttu-id="8d0da-114">Varmista parametritietueen **Summaperusteiset hinnoitteludimensiot** -välilehdellä, että roolin **msdyn_resourcecategory** ja resursoivan organisaatioyksikön **msdyn_organizationalunit** kenttien **Sovelletaan myyntiin** ja **Sovelletaan kustannuksiin** arvona on **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="8d0da-114">In the parameter record, on the **Amount-based pricing dimensions** tab, verify that the role, **msdyn_resourcecategory** and resourcing organizational unit, **msdyn_organizationalunit** have the fields **Applicable to sales** and **Applicable to cost** set to **Yes**.</span></span> <span data-ttu-id="8d0da-115">Näiden käytössä olevien kenttien avulla voit määrittää jokaisen roolin ja organisaatioyksikön hinnan ja kustannuksen.</span><span class="sxs-lookup"><span data-stu-id="8d0da-115">With these fields enabled, you can set up the price and cost for each role and organizational unit combination.</span></span>

<span data-ttu-id="8d0da-116">Jos sinun on määritettävä resurssiesi hintoja tai kustannuksia lisämääritteitä käyttäen, voit luoda mukautettuja kenttiä, entiteettejä ja dimensioita.</span><span class="sxs-lookup"><span data-stu-id="8d0da-116">If you need to price or cost for your resources using additional attributes, you can create customized fields, entities, and dimensions.</span></span>

## <a name="pricing-human-resource-time"></a><span data-ttu-id="8d0da-117">Henkilöresurssin ajan hinnoitteleminen</span><span class="sxs-lookup"><span data-stu-id="8d0da-117">Pricing human resource time</span></span>
<span data-ttu-id="8d0da-118">Organisaation tapa hinnoitella henkilöresurssien aika on usein tärkeä strateginen näkökohta, joka vaikuttaa suoraan organisaation kannattavuuteen.</span><span class="sxs-lookup"><span data-stu-id="8d0da-118">How an organization prices human resource time is often an important strategic consideration that directly affects the organization's profitability.</span></span> <span data-ttu-id="8d0da-119">Tee yhteistyötä talousryhmän ja ammattialan päälliköiden kanssa, kun organisaatiosi on valmis päättämään, miten se haluaa määrittää henkilöresurssien ajan laskutus- ja kustannushinnat.</span><span class="sxs-lookup"><span data-stu-id="8d0da-119">Work with the finance teams and practice heads when your organization is ready to identify how it wants to set up bill and cost rates for human resource time.</span></span>

<span data-ttu-id="8d0da-120">Muita hinnoittelussa huomioitavia seikkoja ovat se, käytetäänkö sellaisia kenttiä tai entiteettejä uudelleen, jotka eivät tällä hetkellä ole hinnoitteludimensioita mutta soveltuvat organisaation hinnoitteludimensioiksi.</span><span class="sxs-lookup"><span data-stu-id="8d0da-120">Other considerations for pricing include whether to re-use fields or entities that are not currently pricing dimensions but apply as a pricing dimension for your organization.</span></span> <span data-ttu-id="8d0da-121">Mahdollisia dimensioita ovat esimerkiksi kentät **Tapahtumaluokka** ( **msdyn_transactioncategory** ) ja **Varattavissa oleva resurssi** ( **bookableresource** ).</span><span class="sxs-lookup"><span data-stu-id="8d0da-121">Fields like **Transaction Category** ( **msdyn_transactioncategory** ) and **Bookable Resource** ( **bookableresource** ) are examples of candidate dimensions.</span></span> 

<span data-ttu-id="8d0da-122">Mieti, pitäisikö hinnoitteludimension olla taulukko vai asetusjoukko.</span><span class="sxs-lookup"><span data-stu-id="8d0da-122">Consider whether your pricing dimension should be a table or an option set.</span></span> <span data-ttu-id="8d0da-123">Jos odotettavissa on muutoksia dimension arvioihin, jotka ylittävät 10 tai 12, ja tarvitset lisämääritteitä kyseisille arvoille, voit luoda entiteetin asetusjoukon sijaan.</span><span class="sxs-lookup"><span data-stu-id="8d0da-123">If you foresee changes to the values of a dimension which will exceed 10 or 12 and you need additional attributes on these values, you could create an entity rather than an option set.</span></span> <span data-ttu-id="8d0da-124">Asetusjoukon ylläpitotoimiin, kuten arvojen lisäämiseen, tarvitaan järjestelmänvalvoja tai kehittäjä, kun taas useimmat käyttäjät pystyvät lisäämään uusia rivejä taulukkoon.</span><span class="sxs-lookup"><span data-stu-id="8d0da-124">Maintaining an option set, such as adding or removing values, requires an admin or developer whereas adding new rows to a table can be done by most users.</span></span>

<span data-ttu-id="8d0da-125">Seuraavassa esimerkissä esitetään laskutushintoja, jotka määritetään roolin ja sen resursoivan organisaatioyksikön perusteella, johon resurssi kuuluu.</span><span class="sxs-lookup"><span data-stu-id="8d0da-125">The following example shows bill rates that are set up based on the role and the resourcing org unit to which the resource belongs.</span></span> <span data-ttu-id="8d0da-126">Kustannushinnat perustuvat yleensä työntekijän ja hänen organisaatioyksikkönsä palkkaluokkiin.</span><span class="sxs-lookup"><span data-stu-id="8d0da-126">Cost rates are typically based on the salary band of the employee and the org unit that they belong to.</span></span> <span data-ttu-id="8d0da-127">Tässä esimerkissä laskutushinnan ja kustannushinnan taulukot näyttävät seuraavalta.</span><span class="sxs-lookup"><span data-stu-id="8d0da-127">In this example, the bill rate and cost rate tables will look like the following.</span></span>

<span data-ttu-id="8d0da-128">**Esimerkkilaskutushinnat**</span><span class="sxs-lookup"><span data-stu-id="8d0da-128">**Sample bill rates**</span></span>

| <span data-ttu-id="8d0da-129">Rooli</span><span class="sxs-lookup"><span data-stu-id="8d0da-129">Role</span></span>        | <span data-ttu-id="8d0da-130">Organisaatioyksikkö</span><span class="sxs-lookup"><span data-stu-id="8d0da-130">Org Unit</span></span>    |<span data-ttu-id="8d0da-131">Yksikkö</span><span class="sxs-lookup"><span data-stu-id="8d0da-131">Unit</span></span>      |<span data-ttu-id="8d0da-132">Hinta</span><span class="sxs-lookup"><span data-stu-id="8d0da-132">Price</span></span>      |<span data-ttu-id="8d0da-133">Valuutta</span><span class="sxs-lookup"><span data-stu-id="8d0da-133">Currency</span></span>  |
| ------------|-------------|----------|----------:|----------|
| <span data-ttu-id="8d0da-134">Kehittäjä</span><span class="sxs-lookup"><span data-stu-id="8d0da-134">Developer</span></span>   | <span data-ttu-id="8d0da-135">Contoso US</span><span class="sxs-lookup"><span data-stu-id="8d0da-135">Contoso US</span></span>  |<span data-ttu-id="8d0da-136">Hour</span><span class="sxs-lookup"><span data-stu-id="8d0da-136">Hour</span></span> | <span data-ttu-id="8d0da-137">200</span><span class="sxs-lookup"><span data-stu-id="8d0da-137">200</span></span>|<span data-ttu-id="8d0da-138">USD</span><span class="sxs-lookup"><span data-stu-id="8d0da-138">USD</span></span>     |
| <span data-ttu-id="8d0da-139">Kehittäjä</span><span class="sxs-lookup"><span data-stu-id="8d0da-139">Developer</span></span>   | <span data-ttu-id="8d0da-140">Contoso India</span><span class="sxs-lookup"><span data-stu-id="8d0da-140">Contoso India</span></span> |<span data-ttu-id="8d0da-141">Hour</span><span class="sxs-lookup"><span data-stu-id="8d0da-141">Hour</span></span>|   <span data-ttu-id="8d0da-142">112</span><span class="sxs-lookup"><span data-stu-id="8d0da-142">112</span></span>|<span data-ttu-id="8d0da-143">USD</span><span class="sxs-lookup"><span data-stu-id="8d0da-143">USD</span></span>     |


<span data-ttu-id="8d0da-144">**Esimerkkikustannushinnat**</span><span class="sxs-lookup"><span data-stu-id="8d0da-144">**Sample cost rates**</span></span>

| <span data-ttu-id="8d0da-145">Palkkaluokat</span><span class="sxs-lookup"><span data-stu-id="8d0da-145">Salary Band</span></span>     | <span data-ttu-id="8d0da-146">Organisaatioyksikkö</span><span class="sxs-lookup"><span data-stu-id="8d0da-146">Org Unit</span></span>    |<span data-ttu-id="8d0da-147">Yksikkö</span><span class="sxs-lookup"><span data-stu-id="8d0da-147">Unit</span></span>      |<span data-ttu-id="8d0da-148">Hinta</span><span class="sxs-lookup"><span data-stu-id="8d0da-148">Price</span></span>      |<span data-ttu-id="8d0da-149">Valuutta</span><span class="sxs-lookup"><span data-stu-id="8d0da-149">Currency</span></span>  |
| ----------------|-------------|----------|----------:|----------|
| <span data-ttu-id="8d0da-150">Oma company_Band1</span><span class="sxs-lookup"><span data-stu-id="8d0da-150">My company_Band1</span></span> | <span data-ttu-id="8d0da-151">Contoso US</span><span class="sxs-lookup"><span data-stu-id="8d0da-151">Contoso US</span></span>  |<span data-ttu-id="8d0da-152">Hour</span><span class="sxs-lookup"><span data-stu-id="8d0da-152">Hour</span></span> | <span data-ttu-id="8d0da-153">145</span><span class="sxs-lookup"><span data-stu-id="8d0da-153">145</span></span>|<span data-ttu-id="8d0da-154">USD</span><span class="sxs-lookup"><span data-stu-id="8d0da-154">USD</span></span>     |
| <span data-ttu-id="8d0da-155">Oma company_Band2</span><span class="sxs-lookup"><span data-stu-id="8d0da-155">My company_Band2</span></span> | <span data-ttu-id="8d0da-156">Contoso India</span><span class="sxs-lookup"><span data-stu-id="8d0da-156">Contoso India</span></span> |<span data-ttu-id="8d0da-157">Hour</span><span class="sxs-lookup"><span data-stu-id="8d0da-157">Hour</span></span>|   <span data-ttu-id="8d0da-158">67</span><span class="sxs-lookup"><span data-stu-id="8d0da-158">67</span></span>|<span data-ttu-id="8d0da-159">USD</span><span class="sxs-lookup"><span data-stu-id="8d0da-159">USD</span></span>     |
