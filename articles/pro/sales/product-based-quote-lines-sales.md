---
title: Tuotepohjaisten tarjousrivien yleiskatsaus – lite
description: Tässä aiheessa on tietoja tuotepohjaisten tarjousrivien käyttämisestä.
author: rumant
ms.date: 10/30/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 5cc3a97194e01b14de054a93a6268c1f0c24bc25
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/10/2021
ms.locfileid: "5994447"
---
# <a name="product-based-quote-lines-overview---lite"></a><span data-ttu-id="c5aae-103">Tuotepohjaisten tarjousrivien yleiskatsaus – lite</span><span class="sxs-lookup"><span data-stu-id="c5aae-103">Product-based quote lines overview - lite</span></span>

<span data-ttu-id="c5aae-104">_**Käytetään:** Lite-käyttöönotto – kauppa proformalaskutukseen_</span><span class="sxs-lookup"><span data-stu-id="c5aae-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="c5aae-105">Dynamics 365 Project Operationsissa voidaan luoda tuotepohjaisia tarjousrivejä.</span><span class="sxs-lookup"><span data-stu-id="c5aae-105">You can create product-based quote lines in Dynamics 365 Project Operations.</span></span> <span data-ttu-id="c5aae-106">Tuotepohjaiset tarjousrivit voidaan lisätä manuaalisesti, tai ne voivat olla tuoteluettelon nimikkeitä.</span><span class="sxs-lookup"><span data-stu-id="c5aae-106">Product-based quote lines can be manually added, or they can be items from the product catalog.</span></span>

## <a name="product-catalog"></a><span data-ttu-id="c5aae-107">Tuoteluettelo</span><span class="sxs-lookup"><span data-stu-id="c5aae-107">Product catalog</span></span>

<span data-ttu-id="c5aae-108">Kullakin tuoteluettelon tuotteella on oletusarvoinen yksikkö ja yksikköryhmä.</span><span class="sxs-lookup"><span data-stu-id="c5aae-108">Each product in the product catalog has a default unit and unit group.</span></span> <span data-ttu-id="c5aae-109">Jos useilla tuotteilla on sama määritejoukko, voit luoda tuoteperheen, jotka jakavat nämä määritteet.</span><span class="sxs-lookup"><span data-stu-id="c5aae-109">If multiple products share the same set of attributes, you can create a product family that share those attributes.</span></span> 

<span data-ttu-id="c5aae-110">Tässä esimerkissä yritys myy tilauskäyttöoikeuksia erilaisille ohjelmistoille.</span><span class="sxs-lookup"><span data-stu-id="c5aae-110">For example, a company sells subscription licenses for different kinds of software.</span></span> <span data-ttu-id="c5aae-111">Kaikilla tilausohjelmistoilla on seuraavat kaksi määritettä:</span><span class="sxs-lookup"><span data-stu-id="c5aae-111">All subscription software has the following two attributes:</span></span>

- <span data-ttu-id="c5aae-112">Käyttäjien määrä</span><span class="sxs-lookup"><span data-stu-id="c5aae-112">Number of users</span></span>
- <span data-ttu-id="c5aae-113">Tilausten kesto mitataan kuukausina</span><span class="sxs-lookup"><span data-stu-id="c5aae-113">A subscription duration measured in months</span></span>

<span data-ttu-id="c5aae-114">Tällaista luetteloa ylläpidetään luomalla **Tilausohjelmisto**-niminen tuoteperhe ja lisäämällä käyttäjien määrä ja tilauksen kesto määritteinä.</span><span class="sxs-lookup"><span data-stu-id="c5aae-114">To maintain this type of catalog, create a product family named **Subscription Software** and add the number of users and the subscription duration as attributes.</span></span> <span data-ttu-id="c5aae-115">Seuraavaksi voit lisätä yksittäisiä tuotteita **Tilausohjelmisto**-tuoteperheeseen.</span><span class="sxs-lookup"><span data-stu-id="c5aae-115">Next, you can add individual products to the **Subscription Software** product family.</span></span>

## <a name="add-product-catalog-items-to-a-project-quote"></a><span data-ttu-id="c5aae-116">Tuoteluettelon nimikkeiden lisääminen projektitarjoukseen</span><span class="sxs-lookup"><span data-stu-id="c5aae-116">Add product catalog items to a project quote</span></span>

<span data-ttu-id="c5aae-117">**Projektitarjous**- ja **Projektisopimus**-sivuilla on oma osa projektipohjaisille riveille ja tuotepohjaisille riveille.</span><span class="sxs-lookup"><span data-stu-id="c5aae-117">The **Project Quote** and **Project Contract** pages have sections for project-based lines and product-based lines.</span></span> <span data-ttu-id="c5aae-118">Tuotepohjaisten rivien tarjous- tai projektisopimusrivin avattava luettelo sisältää kaikki tuotehinnaston tuotteet ja yksiköt.</span><span class="sxs-lookup"><span data-stu-id="c5aae-118">For product-based lines, the drop-down list on the quote line or project contract line includes all the products and units in the product price list.</span></span> <span data-ttu-id="c5aae-119">Voit lisätä myös tuotteita, jotka eivät sisälly tuotehinnastoon.</span><span class="sxs-lookup"><span data-stu-id="c5aae-119">You can also add products that aren't part of the product price list.</span></span>

<span data-ttu-id="c5aae-120">Lisäksi voit valita tuotteita muista hinnastoista tai suoraan tuoteluettelosta.</span><span class="sxs-lookup"><span data-stu-id="c5aae-120">Additionally, you can select products from other price lists or directly from the product catalog.</span></span> <span data-ttu-id="c5aae-121">Kun valitset tuotteita suoraan tuoteluettelosta, kyseisen tuotteen oletushinnastoa käytetään tuotteen myyntihinnan määrittämiseen.</span><span class="sxs-lookup"><span data-stu-id="c5aae-121">When you select products directly from a product catalog, the default price list of that product is used to get the product's sales price.</span></span> <span data-ttu-id="c5aae-122">Jos oletushinnastoa ei ole määritetty, hinnaksi määritetään nolla (0).</span><span class="sxs-lookup"><span data-stu-id="c5aae-122">If a default price list isn't set, the price is set to zero (0).</span></span>

<span data-ttu-id="c5aae-123">Jos tarjousrivi perustuu tuoteluetteloon, voit korvata myyntihinnan suoraan tarjousrivillä.</span><span class="sxs-lookup"><span data-stu-id="c5aae-123">When a quote line is based on a product catalog, you can override the sales price directly on the quote line.</span></span> <span data-ttu-id="c5aae-124">**Hinnoittelu**-kentän tarjousrivillä on kaksi mahdollista arvoa:</span><span class="sxs-lookup"><span data-stu-id="c5aae-124">A quote line in **Pricing** field with two available values:</span></span>

- <span data-ttu-id="c5aae-125">**Ohita hinnoittelu**</span><span class="sxs-lookup"><span data-stu-id="c5aae-125">**Override Pricing**</span></span>
- <span data-ttu-id="c5aae-126">**Käytä oletusta**</span><span class="sxs-lookup"><span data-stu-id="c5aae-126">**Use Default**</span></span>

<span data-ttu-id="c5aae-127">Jos valitset **Ohita hinnoittelu**, oletushintaa ei määritetä.</span><span class="sxs-lookup"><span data-stu-id="c5aae-127">If you select **Override Pricing**, the default price isn't set.</span></span> <span data-ttu-id="c5aae-128">Tuotteelle on sen sijaan annettava hinta tarjousrivillä.</span><span class="sxs-lookup"><span data-stu-id="c5aae-128">Instead, you must enter a price for the product on the quote line.</span></span> <span data-ttu-id="c5aae-129">Jos valitset **Käytä oletusta**, oletusmyyntihintaa käytetään ja kenttä lukitaan, joten sitä ei voi muokata.</span><span class="sxs-lookup"><span data-stu-id="c5aae-129">If you select **Use Default**, the default sales price is used and the field is locked for editing.</span></span>

<span data-ttu-id="c5aae-130">Oletusmyyntihinnat annetaan tarjouksen tuotepohjaisilla riveillä.</span><span class="sxs-lookup"><span data-stu-id="c5aae-130">Default sales prices are entered on the product-based lines of a quote.</span></span> <span data-ttu-id="c5aae-131">**Hinnoittelu** -kentän arvoksi määritetään sitten **Ohita hinnoittelu**, jotta voit muokata tarjousrivien oletushintaa.</span><span class="sxs-lookup"><span data-stu-id="c5aae-131">The **Pricing** field is then set to **Override Pricing** so that you can edit the default price on the quote lines.</span></span> <span data-ttu-id="c5aae-132">Tämä on Project Operations -kohtainen Dynamics 365 Salesin tuotepohjaisen rivitoiminnan ohitus.</span><span class="sxs-lookup"><span data-stu-id="c5aae-132">This is a Project Operations-specific override to the product-based lines behavior in Dynamics 365 Sales.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]