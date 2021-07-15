---
title: Hinnoittelu- ja kustannusdimensioiden aloitussivu
description: Tämä aihe sisältää yleiskatsauksen hinnoitteludimensioihin.
author: rumant
ms.custom:
- dyn365-projectservice
- intro-internal
ms.date: 10/01/2020
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 5c8c28839f5e7b3259afbea4ab400d0c4fca95fd
ms.sourcegitcommit: 0fafe022731f0e1e8693382ff906e3f8541d34ca
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 07/07/2021
ms.locfileid: "6368877"
---
# <a name="pricing-and-costing-dimensions-home-page"></a><span data-ttu-id="a69c6-103">Hinnoittelu- ja kustannusdimensioiden aloitussivu</span><span class="sxs-lookup"><span data-stu-id="a69c6-103">Pricing and costing dimensions home page</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="a69c6-104">Seuraavat määritteet vaikuttavat dimensioihin, joita käytetään työn hinnoittelun ja kustannuslaskennan määritykseen projektipohjaisissa organisaatioissa:</span><span class="sxs-lookup"><span data-stu-id="a69c6-104">The dimensions used to set labor pricing and costing in project-based organizations are influenced by the following attributes:</span></span>

- <span data-ttu-id="a69c6-105">Käyttäjät, jotka tekevät töitä kokemuksensa, roolinsa tai maantieteellisen sijaintinsa mukaan</span><span class="sxs-lookup"><span data-stu-id="a69c6-105">People doing work similar to their experience, role, or geography</span></span>
- <span data-ttu-id="a69c6-106">Työ, joka on suoritettava samalla tavalla monimutkaisuuden tai vuorokauden ajan suhteen</span><span class="sxs-lookup"><span data-stu-id="a69c6-106">Work to be performed similar to its complexity or time of day</span></span>

<span data-ttu-id="a69c6-107">Kun otetaan huomioon näiden töiden ja työn suorittamiseen tarvittavien henkilöiden tyypilliset määritteet, Project Service Automationissa on kahdentyyppisiä hinnoitteludimensioarvoja:</span><span class="sxs-lookup"><span data-stu-id="a69c6-107">Given the typical nature of these attrubutes of the work and the people required to perform the work, there are two types of pricing dimension values available in Project Service Automation:</span></span> 

- <span data-ttu-id="a69c6-108">**Asetusjoukot** – Määritteet, jotka ovat arvojoukon kiinteitä luettelointeja.</span><span class="sxs-lookup"><span data-stu-id="a69c6-108">**Option sets** - Attributes that are fixed enumerations for a set of values.</span></span>
- <span data-ttu-id="a69c6-109">**Entiteettipohjaiset arvot** – Määritteet, joilla voi olla vaihteleva joukko arvoja, jotka ovat rajallisia mutta voivat muuttua ajan myötä.</span><span class="sxs-lookup"><span data-stu-id="a69c6-109">**Entity-based values** - Attributes that can have a varied set of values that are finite but can change over time.</span></span>

## <a name="pricing-dimensions"></a><span data-ttu-id="a69c6-110">Hinnoitteludimensiot</span><span class="sxs-lookup"><span data-stu-id="a69c6-110">Pricing dimensions</span></span>

<span data-ttu-id="a69c6-111">PSA sisältää oletusjoukon hinnoitteludimensioita.</span><span class="sxs-lookup"><span data-stu-id="a69c6-111">PSA ships with a default set of pricing dimensions.</span></span> <span data-ttu-id="a69c6-112">Niitä voi tarkastella siirtymällä kohtaan **Project Service** > **Parametrit**.</span><span class="sxs-lookup"><span data-stu-id="a69c6-112">You can view these by going to **Project Service** > **Parameters**.</span></span> <span data-ttu-id="a69c6-113">Varmista parametritietueen **Summaperusteiset hinnoitteludimensiot** -välilehdellä, että roolin **msdyn_resourcecategory** ja resursoivan organisaatioyksikön **msdyn_organizationalunit** kenttien **Sovelletaan myyntiin** ja **Sovelletaan kustannuksiin** arvona on **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="a69c6-113">In the parameter record, on the **Amount-based pricing dimensions** tab, verify that the role, **msdyn_resourcecategory** and resourcing organizational unit, **msdyn_organizationalunit** have the fields **Applicable to sales** and **Applicable to cost** set to **Yes**.</span></span> <span data-ttu-id="a69c6-114">Tällöin voit määrittää jokaisen roolin ja organisaatioyksikön hinnan ja kustannuksen.</span><span class="sxs-lookup"><span data-stu-id="a69c6-114">This will allow you to set up the price and cost for each role and organizational unit combination.</span></span>

![Näyttökuva Project Service -parametreista, joissa Sovelletaan myyntiin on korostettu](media/PS-OOB-parameters.png)

> [!IMPORTANT]
> <span data-ttu-id="a69c6-116">Jos olet käyttänyt valmiita roolin ja organisaatioyksikön kenttiä hinnoitteludimensioina ennen PSA;n versiota 3, muutoksia ei ole havaittavissa.</span><span class="sxs-lookup"><span data-stu-id="a69c6-116">If you have been the using out-of-the box fields of role and organizational unit as pricing dimensions prior to version 3 of PSA, there will not be any observable change.</span></span> <span data-ttu-id="a69c6-117">Voit jatkaa Project Servicen käyttöä tavalliseen tapaan.</span><span class="sxs-lookup"><span data-stu-id="a69c6-117">You can continue to use Project Service as usual.</span></span> 

<span data-ttu-id="a69c6-118">Jos sinun on määritettävä resurssiesi hintoja tai kustannuksia lisämääritteitä käyttäen, voit luoda mukautettuja kenttiä, entiteettejä ja dimensioita.</span><span class="sxs-lookup"><span data-stu-id="a69c6-118">If you need to price or cost for your resources using additional attributes, you can create customized fields, entities, and dimensions.</span></span> <span data-ttu-id="a69c6-119">Lisätietoja saat seuraavista aiheista, mutta ota huomioon, että sinun on suoritettava toimenpidesarja alla näkyvässä järjestyksessä:</span><span class="sxs-lookup"><span data-stu-id="a69c6-119">For more information, see the following topics, however note that you must complete the procedures in the order listed below:</span></span>

- [<span data-ttu-id="a69c6-120">Mukautettujen kenttien ja entiteettien luominen</span><span class="sxs-lookup"><span data-stu-id="a69c6-120">Create custom fields and entities</span></span>](create-custom-fields-entities.md)
- [<span data-ttu-id="a69c6-121">Mukautettujen kenttien lisääminen hinta- ja tapahtumaentiteetteihin</span><span class="sxs-lookup"><span data-stu-id="a69c6-121">Add custom fields to price setup and transactional entities</span></span>](field-references.md)
- [<span data-ttu-id="a69c6-122">Mukautettujen kenttien määrittäminen hinnoitteludimensioiksi </span><span class="sxs-lookup"><span data-stu-id="a69c6-122">Set up custom fields as pricing dimensions</span></span>](set-up-pricing-dimensions.md)
- [<span data-ttu-id="a69c6-123">Päivitä laajennusmääritteet sisältämään uudet hinnoitteludimensiot</span><span class="sxs-lookup"><span data-stu-id="a69c6-123">Update plug-in attributes to include new pricing dimensions</span></span>](update-plug-in-attributes.md)

## <a name="pricing-human-resource-time"></a><span data-ttu-id="a69c6-124">Henkilöresurssin ajan hinnoitteleminen</span><span class="sxs-lookup"><span data-stu-id="a69c6-124">Pricing human resource time</span></span>
<span data-ttu-id="a69c6-125">Organisaation tapa hinnoitella henkilöresurssien aika on usein tärkeä strateginen näkökohta, joka vaikuttaa suoraan organisaation kannattavuuteen.</span><span class="sxs-lookup"><span data-stu-id="a69c6-125">How an organization prices human resource time is often an important strategic consideration that directly affects the organization's profitability.</span></span> <span data-ttu-id="a69c6-126">Tee yhteistyötä talousryhmän ja ammattialan päälliköiden kanssa, kun organisaatiosi on valmis päättämään, miten se haluaa määrittää henkilöresurssien ajan laskutus- ja kustannushinnat.</span><span class="sxs-lookup"><span data-stu-id="a69c6-126">Work with the finance teams and practice heads when your organization is ready to identify how it wants to set up bill and cost rates for human resource time.</span></span>

<span data-ttu-id="a69c6-127">Muita hinnoittelussa huomioitavia seikkoja ovat se, käytetäänkö sellaisia kenttiä tai entiteettejä uudelleen, jotka eivät tällä hetkellä ole hinnoitteludimensioita mutta soveltuvat organisaation hinnoitteludimensioiksi.</span><span class="sxs-lookup"><span data-stu-id="a69c6-127">Other considerations for pricing include whether to re-use fields or entities that are not currently pricing dimensions but apply as a pricing dimension for your organization.</span></span> <span data-ttu-id="a69c6-128">Mahdollisia dimensioita ovat esimerkiksi kentät **Tapahtumaluokka** (**msdyn_transactioncategory**) ja **Varattavissa oleva resurssi** (**bookableresource**).</span><span class="sxs-lookup"><span data-stu-id="a69c6-128">Fields like **Transaction Category** (**msdyn_transactioncategory**) and **Bookable Resource** (**bookableresource**) are examples of candidate dimensions.</span></span> 

<span data-ttu-id="a69c6-129">Mieti, pitäisikö hinnoitteludimension olla taulukko vai asetusjoukko.</span><span class="sxs-lookup"><span data-stu-id="a69c6-129">Consider whether your pricing dimension should be a table or an option set.</span></span> <span data-ttu-id="a69c6-130">Jos odotettavissa on muutoksia dimension arvoihin, jotka ylittävät 10 tai 12, ja tarvitset lisämääritteitä kyseisille arvoille, luo entiteetti asetusjoukon sijaan.</span><span class="sxs-lookup"><span data-stu-id="a69c6-130">If you foresee changes to the values of a dimension which will exceed 10 or 12 and you need additional attributes on these values, create an entity rather than an option set.</span></span> <span data-ttu-id="a69c6-131">Asetusjoukon ylläpitotoimiin, kuten arvojen lisäämiseen, tarvitaan järjestelmänvalvoja tai kehittäjä, kun taas useimmat yrityskäyttäjät pystyvät lisäämään uusia rivejä taulukkoon.</span><span class="sxs-lookup"><span data-stu-id="a69c6-131">Maintaining an option set, such as adding or removing values, requires an admin or developer whereas adding new rows to a table can be done by most business users.</span></span>

<span data-ttu-id="a69c6-132">Seuraavassa esimerkissä esitetään laskutushintoja, jotka määritetään roolin ja sen resursoivan organisaatioyksikön perusteella, johon resurssi kuuluu.</span><span class="sxs-lookup"><span data-stu-id="a69c6-132">The following example shows bill rates that are set up based on the role and the resourcing org unit to which the resource belongs.</span></span> <span data-ttu-id="a69c6-133">Kustannushinnat perustuvat yleensä työntekijän ja hänen organisaatioyksikkönsä palkkaluokkiin.</span><span class="sxs-lookup"><span data-stu-id="a69c6-133">Cost rates are typically based on the salary band of the employee and the org unit that they belong to.</span></span> <span data-ttu-id="a69c6-134">Tässä esimerkissä laskutushinnan ja kustannushinnan taulukot näyttävät seuraavalta.</span><span class="sxs-lookup"><span data-stu-id="a69c6-134">In this example, the bill rate and cost rate tables will look like the following.</span></span>

<span data-ttu-id="a69c6-135">**Esimerkkilaskutushinnat**</span><span class="sxs-lookup"><span data-stu-id="a69c6-135">**Sample bill rates**</span></span>

| <span data-ttu-id="a69c6-136">Rooli</span><span class="sxs-lookup"><span data-stu-id="a69c6-136">Role</span></span>        | <span data-ttu-id="a69c6-137">Organisaatioyksikkö</span><span class="sxs-lookup"><span data-stu-id="a69c6-137">Org Unit</span></span>    |<span data-ttu-id="a69c6-138">Yksikkö</span><span class="sxs-lookup"><span data-stu-id="a69c6-138">Unit</span></span>      |<span data-ttu-id="a69c6-139">Hinta</span><span class="sxs-lookup"><span data-stu-id="a69c6-139">Price</span></span>      |<span data-ttu-id="a69c6-140">Valuutta</span><span class="sxs-lookup"><span data-stu-id="a69c6-140">Currency</span></span>  |
| ------------|-------------|----------|----------:|----------|
| <span data-ttu-id="a69c6-141">Kehittäjä</span><span class="sxs-lookup"><span data-stu-id="a69c6-141">Developer</span></span>   | <span data-ttu-id="a69c6-142">Contoso US</span><span class="sxs-lookup"><span data-stu-id="a69c6-142">Contoso US</span></span>  |<span data-ttu-id="a69c6-143">tunti</span><span class="sxs-lookup"><span data-stu-id="a69c6-143">Hour</span></span> | <span data-ttu-id="a69c6-144">200</span><span class="sxs-lookup"><span data-stu-id="a69c6-144">200</span></span>|<span data-ttu-id="a69c6-145">USD</span><span class="sxs-lookup"><span data-stu-id="a69c6-145">USD</span></span>     |
| <span data-ttu-id="a69c6-146">Kehittäjä</span><span class="sxs-lookup"><span data-stu-id="a69c6-146">Developer</span></span>   | <span data-ttu-id="a69c6-147">Contoso India</span><span class="sxs-lookup"><span data-stu-id="a69c6-147">Contoso India</span></span> |<span data-ttu-id="a69c6-148">tunti</span><span class="sxs-lookup"><span data-stu-id="a69c6-148">Hour</span></span>|   <span data-ttu-id="a69c6-149">112</span><span class="sxs-lookup"><span data-stu-id="a69c6-149">112</span></span>|<span data-ttu-id="a69c6-150">USD</span><span class="sxs-lookup"><span data-stu-id="a69c6-150">USD</span></span>     |


<span data-ttu-id="a69c6-151">**Esimerkkikustannushinnat**</span><span class="sxs-lookup"><span data-stu-id="a69c6-151">**Sample cost rates**</span></span>

| <span data-ttu-id="a69c6-152">Palkkaluokat</span><span class="sxs-lookup"><span data-stu-id="a69c6-152">Salary Band</span></span>     | <span data-ttu-id="a69c6-153">Organisaatioyksikkö</span><span class="sxs-lookup"><span data-stu-id="a69c6-153">Org Unit</span></span>    |<span data-ttu-id="a69c6-154">Yksikkö</span><span class="sxs-lookup"><span data-stu-id="a69c6-154">Unit</span></span>      |<span data-ttu-id="a69c6-155">Hinta</span><span class="sxs-lookup"><span data-stu-id="a69c6-155">Price</span></span>      |<span data-ttu-id="a69c6-156">Valuutta</span><span class="sxs-lookup"><span data-stu-id="a69c6-156">Currency</span></span>  |
| ----------------|-------------|----------|----------:|----------|
| <span data-ttu-id="a69c6-157">Oma company_Band1</span><span class="sxs-lookup"><span data-stu-id="a69c6-157">My company_Band1</span></span> | <span data-ttu-id="a69c6-158">Contoso US</span><span class="sxs-lookup"><span data-stu-id="a69c6-158">Contoso US</span></span>  |<span data-ttu-id="a69c6-159">tunti</span><span class="sxs-lookup"><span data-stu-id="a69c6-159">Hour</span></span> | <span data-ttu-id="a69c6-160">145</span><span class="sxs-lookup"><span data-stu-id="a69c6-160">145</span></span>|<span data-ttu-id="a69c6-161">USD</span><span class="sxs-lookup"><span data-stu-id="a69c6-161">USD</span></span>     |
| <span data-ttu-id="a69c6-162">Oma company_Band2</span><span class="sxs-lookup"><span data-stu-id="a69c6-162">My company_Band2</span></span> | <span data-ttu-id="a69c6-163">Contoso India</span><span class="sxs-lookup"><span data-stu-id="a69c6-163">Contoso India</span></span> |<span data-ttu-id="a69c6-164">tunti</span><span class="sxs-lookup"><span data-stu-id="a69c6-164">Hour</span></span>|   <span data-ttu-id="a69c6-165">67</span><span class="sxs-lookup"><span data-stu-id="a69c6-165">67</span></span>|<span data-ttu-id="a69c6-166">USD</span><span class="sxs-lookup"><span data-stu-id="a69c6-166">USD</span></span>     |


[!INCLUDE[footer-include](../includes/footer-banner.md)]