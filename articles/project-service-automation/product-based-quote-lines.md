---
title: Tuotepohjaiset tarjousrivit
description: Tässä aiheessa on tietoja tuotepohjaisista tarjousriveistä.
author: rumant
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/06/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: 76b90c95-1b3a-4704-a13f-9d7099b83f4c
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: d8bb36fbfe8d01aa26faf5515ca218ad836126b7
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/24/2020
ms.locfileid: "3751155"
---
# <a name="product-based-quote-lines"></a><span data-ttu-id="da003-103">Tuotepohjaiset tarjousrivit</span><span class="sxs-lookup"><span data-stu-id="da003-103">Product-based quote lines</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]


<span data-ttu-id="da003-104">Dynamics 365 Project Service Automationissa voidaan luoda tuotepohjaisia tarjousrivejä.</span><span class="sxs-lookup"><span data-stu-id="da003-104">You can create product-based quote lines in Dynamics 365 Project Service Automation.</span></span> <span data-ttu-id="da003-105">Tuotepohjaiset tarjousrivit voivat olla käsin lisättyjä rivejä tai ne voivat olla tuoteluettelon nimikkeitä.</span><span class="sxs-lookup"><span data-stu-id="da003-105">Product-based quote lines can be "write-in" lines, or they can be items from the product catalog.</span></span>

## <a name="product-catalog"></a><span data-ttu-id="da003-106">Tuoteluettelo</span><span class="sxs-lookup"><span data-stu-id="da003-106">Product catalog</span></span>

<span data-ttu-id="da003-107">Dynamics 365 -tuoteluettelossa olevilla tuotteilla on oletusarvoinen yksikkö ja yksikköryhmä.</span><span class="sxs-lookup"><span data-stu-id="da003-107">The products in a Dynamics 365 product catalog have a default unit and unit group.</span></span> <span data-ttu-id="da003-108">Jos useilla tuotteilla on sama määritejoukko, voit luoda tuoteperheen, jolla on myös kyseiset määritteet.</span><span class="sxs-lookup"><span data-stu-id="da003-108">If several products share the same set of attributes, you can create a product family that also has those attributes.</span></span> <span data-ttu-id="da003-109">Kaikki tuoteperheen tuotteet perivät saman määritejoukon.</span><span class="sxs-lookup"><span data-stu-id="da003-109">All the products in one product family inherit the same set of attributes.</span></span>

<span data-ttu-id="da003-110">Tässä esimerkissä yritys myy tilauskäyttöoikeuksia erilaisille ohjelmistoille.</span><span class="sxs-lookup"><span data-stu-id="da003-110">For example, a company sells subscription licenses for a variety of software.</span></span> <span data-ttu-id="da003-111">Kaikilla tilausohjelmistoilla on seuraavat kaksi määritettä:</span><span class="sxs-lookup"><span data-stu-id="da003-111">All subscription software has the following two attributes:</span></span>

- <span data-ttu-id="da003-112">käyttäjämäärä</span><span class="sxs-lookup"><span data-stu-id="da003-112">Number of users</span></span> 
- <span data-ttu-id="da003-113">Tilausten kesto (kuukausina)</span><span class="sxs-lookup"><span data-stu-id="da003-113">Subscription duration (in months)</span></span>

<span data-ttu-id="da003-114">Hyvä tapa ylläpitää tällaista luetteloa on luoda tuoteperhe nimellä **Tilausohjelmisto**, jolla on määritteinä **Käyttäjämäärä** ja **Tilausten kesto**.</span><span class="sxs-lookup"><span data-stu-id="da003-114">A good way to maintain this type of catalog is to create a product family that is named **Subscription Software**, and that has **Number of users** and **Subscription duration** as attributes.</span></span> <span data-ttu-id="da003-115">Tämän jälkeen **Tilausohjelmisto**-tuoteperheeseen voidaan lisätä yksittäisiä tuotteita, kuten **Dynamics 365 Sales** tai **Dynamics 365 Field Service**.</span><span class="sxs-lookup"><span data-stu-id="da003-115">You can then add individual products, such as **Dynamics 365 Sales** or **Dynamics 365 Field Service** to the **Subscription Software** product family.</span></span>

## <a name="adding-product-catalog-items-to-a-project-quote"></a><span data-ttu-id="da003-116">Tuoteluettelon nimikkeiden lisääminen projektitarjoukseen</span><span class="sxs-lookup"><span data-stu-id="da003-116">Adding product catalog items to a project quote</span></span>

<span data-ttu-id="da003-117">Projektitarjouksen ja projektisopimuksen sivuilla on osioita kahdenlaisille riveille: projektiperusteisille ja tuoteperusteisille riveille.</span><span class="sxs-lookup"><span data-stu-id="da003-117">Project quote and project contract pages have sections for two types of lines: project-based lines and product-based lines.</span></span> <span data-ttu-id="da003-118">Tuoteperusteisten rivien osalta Dynamics 365:ttä käytetään nimikkeiden lisäämiseen tuoteluettelosta tarjoukseen.</span><span class="sxs-lookup"><span data-stu-id="da003-118">For product-based lines, Dynamics 365 is used to add items from a product catalog to a quote.</span></span> <span data-ttu-id="da003-119">Tarjous- tai projektisopimusrivin avattava luettelo sisältää kaikki tarjoukseen tai projektisopimukseen liitetyn tuotehinnaston tuotteet ja yksiköt.</span><span class="sxs-lookup"><span data-stu-id="da003-119">The drop-down list on the quote line or project contract line includes all the products and units in the product price list that is attached to the quote or project contract.</span></span> <span data-ttu-id="da003-120">Voit myös lisätä tuotteita, jotka eivät sisälly tarjouksen tuotehinnastoon.</span><span class="sxs-lookup"><span data-stu-id="da003-120">You can also add products that aren't part of quote's product price list.</span></span>

<span data-ttu-id="da003-121">Lisäksi voit valita tuotteita muista hinnastoista tai voit valita tuotteita suoraan tuoteluettelosta.</span><span class="sxs-lookup"><span data-stu-id="da003-121">Additionally, you can select products from other price lists, or you can select products directly from the product catalog.</span></span> <span data-ttu-id="da003-122">Kun valitset tuotteita suoraan tuoteluettelosta, kyseisen tuotteen oletushinnastoa käytetään tuotteen myyntihinnan määrittämiseen.</span><span class="sxs-lookup"><span data-stu-id="da003-122">When you select products directly from a product catalog, the default price list of that product is used to get the product's sales price.</span></span> <span data-ttu-id="da003-123">Jos oletushinnastoa ei ole määritetty, hinnaksi määritetään 0 (nolla).</span><span class="sxs-lookup"><span data-stu-id="da003-123">If a default price list isn't set, the price is set to 0 (zero).</span></span>

<span data-ttu-id="da003-124">Jos tarjousrivi perustuu tuoteluetteloon, voit korvata myyntihinnan suoraan tarjousrivillä.</span><span class="sxs-lookup"><span data-stu-id="da003-124">If a quote line is based on a product catalog, you can override the sales price directly on the quote line.</span></span> <span data-ttu-id="da003-125">Huomaa, että Dynamics 365:n tarjousrivillä on **Hinnoittelu**-kenttä.</span><span class="sxs-lookup"><span data-stu-id="da003-125">Note that a quote line in Dynamics 365 has a **Pricing** field.</span></span> <span data-ttu-id="da003-126">Käytettävissä on kaksi arvoa:</span><span class="sxs-lookup"><span data-stu-id="da003-126">Two values are available:</span></span>

- <span data-ttu-id="da003-127">Korvaa hinnoittelu</span><span class="sxs-lookup"><span data-stu-id="da003-127">Override pricing</span></span>  
- <span data-ttu-id="da003-128">Käytä oletusta</span><span class="sxs-lookup"><span data-stu-id="da003-128">Use default</span></span>

<span data-ttu-id="da003-129">Jos määrität tämän kentän arvoksi **Korvaa hinnoittelu**, Dynamics 365 ei määritä oletushintaa.</span><span class="sxs-lookup"><span data-stu-id="da003-129">If you set this field to **Override pricing**, Dynamics 365 doesn't set a default price.</span></span> <span data-ttu-id="da003-130">Tuotteelle on määritettävä hinta tarjousrivillä.</span><span class="sxs-lookup"><span data-stu-id="da003-130">You must enter a price for the product on the quote line.</span></span> <span data-ttu-id="da003-131">Jos kentän arvoksi määritetään **Käytä oletusta**, Dynamics 365 käyttää oletusmyyntihintaa ja lukitsee kentän muokkaamisen estämiseksi.</span><span class="sxs-lookup"><span data-stu-id="da003-131">If you set this field to **Use default**, Dynamics 365 uses the default sales price and locks the field to prevent editing.</span></span>

<span data-ttu-id="da003-132">Kun olet asentanut PSA:n, oletusmyyntihinnat syötetään tarjouksen tuoteperusteisille riveille.</span><span class="sxs-lookup"><span data-stu-id="da003-132">After you install PSA, default sales prices are entered on the product-based lines on a quote.</span></span> <span data-ttu-id="da003-133">**Hinnoittelu** -kentän arvoksi määritetään sitten **Korvaa hinnoittelu**, jotta voit muokata tarjousrivien oletushintaa.</span><span class="sxs-lookup"><span data-stu-id="da003-133">The **Pricing** field is then set to **Override pricing** so that you can edit the default price on the quote lines.</span></span>

> ![Hinnoittelun korvaamisen määritys](media/basic-guide-10.png)
 
## <a name="quantity-factors-for-products"></a><span data-ttu-id="da003-135">Tuotteiden määräkertoimet</span><span class="sxs-lookup"><span data-stu-id="da003-135">Quantity factors for products</span></span>

<span data-ttu-id="da003-136">PSA:ssa käytetään määräkertoimia tukemaan tilausperusteisten tuotteiden myyntiä.</span><span class="sxs-lookup"><span data-stu-id="da003-136">PSA uses quantity factors to support the sale of subscription-based products.</span></span> <span data-ttu-id="da003-137">Tilausperusteisten tuotteiden osalta tarjouksen tai projektisopimuksen rivin määrä ilmaistaan käyttäjäkuukausien lukumääränä.</span><span class="sxs-lookup"><span data-stu-id="da003-137">For subscription-based products, the quantity on the quote or project contract line is expressed as the number of user months.</span></span>

<span data-ttu-id="da003-138">Yleensä tilausohjelmiston hinta tallennetaan luetteloon käyttäjäkohtaisena kuukausihintana.</span><span class="sxs-lookup"><span data-stu-id="da003-138">Usually, the price of subscription software is stored in the catalog as the price per user per month.</span></span> <span data-ttu-id="da003-139">Voit kuitenkin käyttää muitakin aikakuvauksia.</span><span class="sxs-lookup"><span data-stu-id="da003-139">However, you can use other time descriptions instead.</span></span> <span data-ttu-id="da003-140">Myyntiprosessin aikana tarjousrivillä oleva hinta on yleensä se käyttäjäkohtainen kuukausihinta, jonka IT-myyjä on neuvotellut ja josta hän on antanut alennusta.</span><span class="sxs-lookup"><span data-stu-id="da003-140">During the sales process, the price on the quote line is usually the per-user, per-month price that was negotiated and discounted by the IT sales agent.</span></span> <span data-ttu-id="da003-141">Kullakin kaupalla on eri määrä käyttäjiä ja eri määrä tilauskuukausia.</span><span class="sxs-lookup"><span data-stu-id="da003-141">Each deal has a different number of users and a different number of subscription months.</span></span> <span data-ttu-id="da003-142">Tarjousrivin summan laskemiseen käytettävä määrä perustuu käyttäjämäärään ja tilauskuukausien määrään.</span><span class="sxs-lookup"><span data-stu-id="da003-142">The quantity that is used to compute the amount of the quote line is a product of the number of users and the number of subscription months.</span></span>

<span data-ttu-id="da003-143">Tällaisen myynnin tukemista varten PSA:ssa on otettu käyttöön määräkertoimien konsepti.</span><span class="sxs-lookup"><span data-stu-id="da003-143">To support this type of sale, PSA introduced the concept of quantity factors.</span></span> <span data-ttu-id="da003-144">Määräkertoimet perustuvat Dynamics 365:n tuotemääritteisiin.</span><span class="sxs-lookup"><span data-stu-id="da003-144">Quantity factors rely on the product attributes in Dynamics 365.</span></span> <span data-ttu-id="da003-145">Kun määrität tuotteelle tiettyjä ominaisuuksia, voit valita osan näistä määritteistä tai ne kaikki määräkertoimiksi.</span><span class="sxs-lookup"><span data-stu-id="da003-145">When you configure specific properties for a product, PSA lets you flag a subset of those properties, or all the properties, as quantity factors.</span></span>

<span data-ttu-id="da003-146">PSA varmistaa, että määräkertoimiksi valitaan vain numeerisia ominaisuuksia tai tuoteominaisuuksia joilla on numeerinen tietotyyppi.</span><span class="sxs-lookup"><span data-stu-id="da003-146">PSA validates that only numeric properties or product properties that have a numeric data type are flagged as quantity factors.</span></span> <span data-ttu-id="da003-147">Kun tarjousriville lisätään tuote, jolle on määritetty määräkertoimia, tarjousrivin **Määrä** -kentästä tulee vain luku -kenttä.</span><span class="sxs-lookup"><span data-stu-id="da003-147">When a product that quantity factors are configured for is added to a quote line, the **Quantity** field on the quote line becomes a read-only field.</span></span> <span data-ttu-id="da003-148">Kun olet määrittänyt arvot tuoteominaisuuksille, jotka ovat määräkertoimia, PSA laskee tarjousrivin määrän.</span><span class="sxs-lookup"><span data-stu-id="da003-148">After you enter values for product properties that are quantity factors, PSA computes the quantity of the quote line.</span></span>

<span data-ttu-id="da003-149">Esimerkiksi Dynamics 365:llä voi olla seuraavat ominaisuudet:</span><span class="sxs-lookup"><span data-stu-id="da003-149">For example, Dynamics 365 might have the following properties:</span></span> 

- <span data-ttu-id="da003-150">**Käyttäjät** – Käyttäjien määrä</span><span class="sxs-lookup"><span data-stu-id="da003-150">**No of users** - The number of users</span></span> 
- <span data-ttu-id="da003-151">**Kuukaudet** – Tilauskuukausien määrä</span><span class="sxs-lookup"><span data-stu-id="da003-151">**No of Months** - The number of subscription months</span></span>
- <span data-ttu-id="da003-152">**Tuote-SKU**</span><span class="sxs-lookup"><span data-stu-id="da003-152">**Product SKU**</span></span> 

<span data-ttu-id="da003-153">Ominaisuudet **Käyttäjät** ja **Kuukaudet** voidaan valita määräkertoimiksi muokkaamalla tuoterivin ominaisuuksia.</span><span class="sxs-lookup"><span data-stu-id="da003-153">Tne **No of Users** and **No of Months** properties can be flagged as quantity factors by editing the properties of the product line.</span></span> 

> ![Ominaisuuksien Käyttäjät ja Kuukaudet valinta määräkertoimiksi](media/basic-guide-11.png)
 
