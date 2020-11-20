---
title: Projektipohjaisten sopimusrivien yleiskatsaus – lite
description: Tässä aiheessa on tietoja tuotepohjaisista sopimusriveistä.
author: rumant
manager: Annbe
ms.date: 10/07/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: eb09140eae5383b882db73195d0360a836ece791
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/30/2020
ms.locfileid: "4177867"
---
# <a name="product-based-contract-lines-overview---lite"></a><span data-ttu-id="93adf-103">Projektipohjaisten sopimusrivien yleiskatsaus – lite</span><span class="sxs-lookup"><span data-stu-id="93adf-103">Product-based contract lines overview - lite</span></span>

<span data-ttu-id="93adf-104">_**Käytetään:** Lite-käyttöönotto – kauppa proformalaskutukseen_</span><span class="sxs-lookup"><span data-stu-id="93adf-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="93adf-105">Voit luoda tuotepohjaisia sopimusrivejä Dynamics 365 Project Operationsissa.</span><span class="sxs-lookup"><span data-stu-id="93adf-105">You can create product-based contract lines in Dynamics 365 Project Operations.</span></span> <span data-ttu-id="93adf-106">Tuotepohjaiset sopimusrivit voivat olla käsin lisättyjä rivejä tai ne voivat olla tuoteluettelon nimikkeitä.</span><span class="sxs-lookup"><span data-stu-id="93adf-106">Product-based contract lines can be manually created lines, or they can be items from the product catalog.</span></span>

## <a name="product-catalog"></a><span data-ttu-id="93adf-107">Tuoteluettelo</span><span class="sxs-lookup"><span data-stu-id="93adf-107">Product catalog</span></span>

<span data-ttu-id="93adf-108">Tuoteluettelossa olevilla tuotteilla on oletusarvoinen yksikkö ja yksikköryhmä.</span><span class="sxs-lookup"><span data-stu-id="93adf-108">The products in the product catalog have a default unit and unit group.</span></span> <span data-ttu-id="93adf-109">Jos useilla tuotteilla on sama määritejoukko, voit luoda tuoteperheen, jolla on myös kyseiset määritteet.</span><span class="sxs-lookup"><span data-stu-id="93adf-109">If several products share the same set of attributes, you can create a product family that also has those attributes.</span></span> <span data-ttu-id="93adf-110">Kaikki tuoteperheen tuotteet perivät saman määritejoukon.</span><span class="sxs-lookup"><span data-stu-id="93adf-110">All the products in one product family inherit the same set of attributes.</span></span>

<span data-ttu-id="93adf-111">Tässä esimerkissä yritys myy tilauskäyttöoikeuksia erilaisille ohjelmistoille.</span><span class="sxs-lookup"><span data-stu-id="93adf-111">For example, a company sells subscription licenses for different kinds of software.</span></span> <span data-ttu-id="93adf-112">Kaikilla tilausohjelmistoilla on seuraavat kaksi määritettä:</span><span class="sxs-lookup"><span data-stu-id="93adf-112">All subscription software has the following two attributes:</span></span>

- <span data-ttu-id="93adf-113">Käyttäjien määrä</span><span class="sxs-lookup"><span data-stu-id="93adf-113">Number of users</span></span>
- <span data-ttu-id="93adf-114">Tilausten kesto (kuukausina)</span><span class="sxs-lookup"><span data-stu-id="93adf-114">Subscription duration (in months)</span></span>

<span data-ttu-id="93adf-115">Jos haluat ylläpitää tämäntyyppistä luetteloa, luo tuoteperhe, jonka nimi on **tilausohjelmisto**.</span><span class="sxs-lookup"><span data-stu-id="93adf-115">To maintain this type of catalog, create a product family that is named **Subscription Software**.</span></span> <span data-ttu-id="93adf-116">Lisää tuoteperheeseen määritteet **käyttäjien määrä** ja **tilausten kesto**.</span><span class="sxs-lookup"><span data-stu-id="93adf-116">Add the attributes, **Number of users** and **Subscription duration** to the product family.</span></span> <span data-ttu-id="93adf-117">Lisää sitten yksittäiset tuotteet **tilausohjelmisto**-tuoteperheeseen.</span><span class="sxs-lookup"><span data-stu-id="93adf-117">Then, add individual products to the **Subscription Software** product family.</span></span>

## <a name="add-product-catalog-items-to-a-project-contract"></a><span data-ttu-id="93adf-118">Lisää tuoteluettelon nimikkeet projektisopimukseen</span><span class="sxs-lookup"><span data-stu-id="93adf-118">Add product catalog items to a project Contract</span></span>

<span data-ttu-id="93adf-119">Projektisopimuksissa on osioita kahdenlaisille riveille, projektiperusteisille ja tuoteperusteisille riveille.</span><span class="sxs-lookup"><span data-stu-id="93adf-119">Project contracts have sections for two types of lines, project-based and product-based.</span></span> <span data-ttu-id="93adf-120">Tuotepohjaisia rivejä ovat kaikki tuotteet ja yksiköt palvelusopimuksen tuotehinnastossa.</span><span class="sxs-lookup"><span data-stu-id="93adf-120">Product-based lines include all of the products and units in the product price list on the contract.</span></span> <span data-ttu-id="93adf-121">Tuotteita, jotka eivät sisälly sopimuksen tuotehinnastoon, voi lisätä.</span><span class="sxs-lookup"><span data-stu-id="93adf-121">Products that aren't part of contract's product price list can be added.</span></span>

<span data-ttu-id="93adf-122">Voit valita tuotteita muista hinnastoista tai suoraan tuoteluettelosta.</span><span class="sxs-lookup"><span data-stu-id="93adf-122">You can select products from other price lists, or directly from the product catalog.</span></span> <span data-ttu-id="93adf-123">Kun valitset tuotteita suoraan tuoteluettelosta, kyseisen tuotteen oletushinnastoa käytetään tuotteen myyntihinnan määrittämiseen.</span><span class="sxs-lookup"><span data-stu-id="93adf-123">When you select products directly from a product catalog, the default price list of that product is used for the product's sales price.</span></span> <span data-ttu-id="93adf-124">Jos oletushinnastoa ei ole määritetty, hinnaksi määritetään 0 (nolla).</span><span class="sxs-lookup"><span data-stu-id="93adf-124">If a default price list isn't set, the price is set to 0 (zero).</span></span>

<span data-ttu-id="93adf-125">Jos sopimusrivi perustuu tuoteluetteloon, voit korvata myyntihinnan suoraan sopimusrivillä.</span><span class="sxs-lookup"><span data-stu-id="93adf-125">If a contract line is based on a product catalog, you can override the sales price directly on the line.</span></span> <span data-ttu-id="93adf-126">Sopimusrivillä on **hinnoittelu**-kenttä, jolla on kaksi arvoa:</span><span class="sxs-lookup"><span data-stu-id="93adf-126">A contract line has the **Pricing** field with the two values:</span></span>

- <span data-ttu-id="93adf-127">**Korvaa hinnoittelu**</span><span class="sxs-lookup"><span data-stu-id="93adf-127">**Override pricing**</span></span>
- <span data-ttu-id="93adf-128">**Käytä oletusta**</span><span class="sxs-lookup"><span data-stu-id="93adf-128">**Use default**</span></span>

<span data-ttu-id="93adf-129">Jos määrität **Hinnoittelu**-kentän arvoksi **Korvaa hinnoittelu**, oletushintaa ei määritetä.</span><span class="sxs-lookup"><span data-stu-id="93adf-129">If you set the **Pricing** field to **Override pricing**, the default price isn't set.</span></span> <span data-ttu-id="93adf-130">Anna projektin sopimusrivin tuotteen hinta.</span><span class="sxs-lookup"><span data-stu-id="93adf-130">Enter a price for the product on the contract line.</span></span> <span data-ttu-id="93adf-131">Jos määrität kentän arvoksi **Käytä oletusarvoa**, käytetään oletusmyyntihintaa eikä kenttää voi muokata.</span><span class="sxs-lookup"><span data-stu-id="93adf-131">If you set the field to **Use default**, the default sales price is used and the field can't be edited.</span></span>

<span data-ttu-id="93adf-132">Kun olet asentanut Project Operationsin, oletusmyyntihinnat syötetään sopimuksen tuoteperusteisille riveille.</span><span class="sxs-lookup"><span data-stu-id="93adf-132">After you install Project Operations, default sales prices are entered on the product-based lines on a contract.</span></span> <span data-ttu-id="93adf-133">**Hinnoittelu**-kentän arvoksi määritetään **Korvaa hinnoittelu**, jotta voit muokata sopimusrivien oletushintaa.</span><span class="sxs-lookup"><span data-stu-id="93adf-133">The **Pricing** field is set to **Override pricing** so that you can edit the default price on the contract lines.</span></span> <span data-ttu-id="93adf-134">Tämä on Project Operations -kohtainen toiminto, joita käytetään Dynamics 365 Salesin tuotepohjaisiin riveihin.</span><span class="sxs-lookup"><span data-stu-id="93adf-134">This is a Project Operations-specific override to product-based lines behavior in Dynamics 365 Sales.</span></span>
