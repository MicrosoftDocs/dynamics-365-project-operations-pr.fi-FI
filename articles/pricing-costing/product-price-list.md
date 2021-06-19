---
title: Tuotehinnastot
description: Tässä aiheessa on tietoja luettelon hinnoittelun hinnastoista, joita käytetään projektitarjouksissa ja sopimuksissa.
author: rumant
ms.date: 04/05/2021
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: rumant
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 02d274725983e50adc35a4cae1ac60c35be346a4
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/10/2021
ms.locfileid: "6004932"
---
# <a name="product-price-lists"></a><span data-ttu-id="998d8-103">Tuotehinnastot</span><span class="sxs-lookup"><span data-stu-id="998d8-103">Product price lists</span></span>

<span data-ttu-id="998d8-104">_**Käytetään:** Lite-käyttöönotto – kauppa proformalaskutukseen_</span><span class="sxs-lookup"><span data-stu-id="998d8-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

 <span data-ttu-id="998d8-105">Project Operationsissa **Tuotehinnastot** ja niihin liittyvät hinnastonimikkeen entiteetit tukevat tuotteiden hinnoittelutoimintoja tuotepohjaisilla tarjous- ja sopimusriveillä.</span><span class="sxs-lookup"><span data-stu-id="998d8-105">In Project Operations, **Product price lists** and related price list item entities support functionality for pricing products on product-based quote and contract lines.</span></span> <span data-ttu-id="998d8-106">Projektihinnastojen hinnastonimiketietueita käytetään projekteissa käytetyille tuotteille.</span><span class="sxs-lookup"><span data-stu-id="998d8-106">For products used on projects, the price list item records for project price lists are used.</span></span> 

<span data-ttu-id="998d8-107">Tuotteet olisi määritettävä siten, että niillä on tuoteluettelossa oletusarvoiset kustannusluettelot ja hinnastot.</span><span class="sxs-lookup"><span data-stu-id="998d8-107">Products should be set up so that they have default cost and price lists in the product catalog.</span></span> <span data-ttu-id="998d8-108">Oletusarvoisten kustannus- ja luettelohintojen määrittämisessä on käytettävä luettelohintaa, vakiokustannusta ja päivän hintaa.</span><span class="sxs-lookup"><span data-stu-id="998d8-108">Use the list price, standard cost, and current cost to configure default cost and list prices.</span></span> <span data-ttu-id="998d8-109">Oletusarvoisia luettelohintoja käytetään tarjousrivillä tai projektisopimusrivillä vain, kun järjestelmä ei löydä tarjouksen tai projektisopimuksen tuotehinnastosta hinnastoriviä tuotteelle.</span><span class="sxs-lookup"><span data-stu-id="998d8-109">The default list prices are used on a quote line or a project contract line only when the system can't find a price list line for that product in the product price list for the quote or project contract.</span></span>

<span data-ttu-id="998d8-110">Tuoteluettelon rivien kustannushintaa voi muuttaa tarjousten välillä.</span><span class="sxs-lookup"><span data-stu-id="998d8-110">The cost price of product catalog lines can be changed between quotes.</span></span> <span data-ttu-id="998d8-111">Tämä ominaisuus on tärkeä, koska jos kustannuksia ei seurata tarkasti, projektisitoumusten toiminnallista voittoa ei voi määrittää.</span><span class="sxs-lookup"><span data-stu-id="998d8-111">This capability is important, because if you don't accurately track costs, you can't determine operational profits on project engagements.</span></span> <span data-ttu-id="998d8-112">Oletusarvoisesti kustannushintana käytetään tuotteen vakiokustannusta.</span><span class="sxs-lookup"><span data-stu-id="998d8-112">By default, the standard cost of the product is used as the cost price.</span></span> <span data-ttu-id="998d8-113">Tarjousrivin oletusarvoista kustannushintaa voidaan kuitenkin päivittää, jos asianomaiselle tarjoukselle on olemassa eri kustannushinta.</span><span class="sxs-lookup"><span data-stu-id="998d8-113">However, the default cost price can be updated on the quote line if there's a different cost price for that quote.</span></span>

## <a name="price-list-items"></a><span data-ttu-id="998d8-114">Hinnaston nimikkeet</span><span class="sxs-lookup"><span data-stu-id="998d8-114">Price list items</span></span>

<span data-ttu-id="998d8-115">Voit lisätä tuotteita tuoteluettelosta eri hinnastoihin.</span><span class="sxs-lookup"><span data-stu-id="998d8-115">You can add products from a product catalog to different price lists.</span></span> <span data-ttu-id="998d8-116">Tuotteiden hinnastorivit viittaavat aina tiettyyn yksikköön.</span><span class="sxs-lookup"><span data-stu-id="998d8-116">Price list lines for products always reference a specific unit.</span></span> <span data-ttu-id="998d8-117">Hinnaston nimikkeisiin kuuluvan tuotteen hinnoittelu voidaan määrittää valuuttamääräisesti.</span><span class="sxs-lookup"><span data-stu-id="998d8-117">Pricing for a product on price list items can be configured as a currency amount.</span></span> <span data-ttu-id="998d8-118">Vaihtoehtoisesti se voidaan määrittää luettelohinnan, päivän hinnan tai vakiokustannuksen funktioksi.</span><span class="sxs-lookup"><span data-stu-id="998d8-118">Alternatively, it can be configured as a function of the list price, current cost, or standard cost.</span></span>

<span data-ttu-id="998d8-119">Hinnoittelutoiminto tukee erilaisia pyöristysvaihtoehtoja, kun tuotteiden hinnat määritetään luettelohinnan, vakiokustannuksen tai päivän hinnan funktioiksi.</span><span class="sxs-lookup"><span data-stu-id="998d8-119">Pricing functionality supports various rounding options when product prices are configured as a function of the list price, standard cost, or current cost.</span></span> <span data-ttu-id="998d8-120">Useiden hinnoittelutapojen ja pyöristysvaihtoehtojen hyödyntämisen lisäksi voit yhdistää hinnaston nimikkeisiin alennusluetteloja.</span><span class="sxs-lookup"><span data-stu-id="998d8-120">In addition to taking advantage of multiple pricing methods and rounding options, you can associate discount lists with price list items.</span></span> 

 
## <a name="default-product-price-list"></a><span data-ttu-id="998d8-121">Oletusarvoinen tuotehinnasto</span><span class="sxs-lookup"><span data-stu-id="998d8-121">Default product price list</span></span>
<span data-ttu-id="998d8-122">Kussakin asiakastietueessa on **Oletushinnasto**-kenttä, jossa voit määrittää hinnaston, jossa käytetään asiakkaan valuuttaa.</span><span class="sxs-lookup"><span data-stu-id="998d8-122">Each customer record has a **Default Price List** field, where you can specify a price list that matches the currency of the customer.</span></span> <span data-ttu-id="998d8-123">Tähän kenttään ei lisätä automaattisesti oletusarvoa.</span><span class="sxs-lookup"><span data-stu-id="998d8-123">A default value isn't automatically entered in this field.</span></span> <span data-ttu-id="998d8-124">Kun tietyn asiakkaan kanssa on tehty mukautettu hinnoittelusopimus, voit käyttää tätä kenttää lisätäksesi hinnaston kyseiselle asiakkaalle.</span><span class="sxs-lookup"><span data-stu-id="998d8-124">When a custom pricing agreement with a specific customer exists, you can use this field to associate a price list with that customer.</span></span>

<span data-ttu-id="998d8-125">Entiteetit Mahdollisuus, Tarjous ja Projektisopimukset lisäävät oletusarvoisia tuotehinnastoja seuraavassa järjestyksessä.</span><span class="sxs-lookup"><span data-stu-id="998d8-125">The Opportunity, Quote, and Project Contract entities use the following order to enter default product price lists.</span></span> <span data-ttu-id="998d8-126">Samaa järjestystä käytetään projektihinnastoissa.</span><span class="sxs-lookup"><span data-stu-id="998d8-126">The same order is used for project price lists.</span></span>

1.  <span data-ttu-id="998d8-127">Tarjous</span><span class="sxs-lookup"><span data-stu-id="998d8-127">Quote</span></span>
2.  <span data-ttu-id="998d8-128">Mahdollisuus</span><span class="sxs-lookup"><span data-stu-id="998d8-128">Opportunity</span></span>
3.  <span data-ttu-id="998d8-129">Asiakas</span><span class="sxs-lookup"><span data-stu-id="998d8-129">Customer</span></span>
4.  <span data-ttu-id="998d8-130">Yleiset asetukset</span><span class="sxs-lookup"><span data-stu-id="998d8-130">Global settings</span></span> 

<span data-ttu-id="998d8-131">Oletusarvoisesti tarjousrivin **Tuote**-rivillä luetellaan kaikki tarjouksen tuotehinnaston aktiiviset tuotteet.</span><span class="sxs-lookup"><span data-stu-id="998d8-131">By default, the **Product** field on the quote line lists all the active products in the product price list of the quote.</span></span> <span data-ttu-id="998d8-132">Jos tuote ei ole aktiivinen tai jos se on tuoteluonnos, se ei näy luettelossa, vaikka se olisi hinnastossa.</span><span class="sxs-lookup"><span data-stu-id="998d8-132">If a product has been inactivated, or if it's a draft product, it isn't listed, even if it's in the price list.</span></span> 

<span data-ttu-id="998d8-133">Tuoteluettelon rivit lisätään laskuriveinä ensimmäiselle projektisopimusat varten luodulle laskulle.</span><span class="sxs-lookup"><span data-stu-id="998d8-133">Product catalog lines are added as invoice lines on the first invoice that is created for a project contract.</span></span> <span data-ttu-id="998d8-134">Nämä laskurivit voidaan poistaa laskuluonnoksessa.</span><span class="sxs-lookup"><span data-stu-id="998d8-134">On a draft invoice, those invoice lines can be deleted.</span></span> <span data-ttu-id="998d8-135">Tällöin rivit tulevat näkyviin myöhemmässä laskussa, kunnes ne on laskutettu tai kunnes lasku on lähetetty asiakkaalle.</span><span class="sxs-lookup"><span data-stu-id="998d8-135">In that case, the lines will appear on a subsequent invoice until they are invoiced, or until the invoice is sent to the customer.</span></span> <span data-ttu-id="998d8-136">Tuotteen laskurivin osittaista määrää ei voi laskuttaa.</span><span class="sxs-lookup"><span data-stu-id="998d8-136">You can't invoice a partial quantity of a product invoice line.</span></span> <span data-ttu-id="998d8-137">Kun projektisopimuksen tuoterivit laskutetaan, luodaan todellisia arvoja.</span><span class="sxs-lookup"><span data-stu-id="998d8-137">When the product lines from the project contract are invoiced, actuals are created.</span></span> <span data-ttu-id="998d8-138">Näitä todellisia arvoja ei kuitenkaan linkitetä niihin liittyvään projektientiteettiin.</span><span class="sxs-lookup"><span data-stu-id="998d8-138">However, those actuals aren't linked to the related project entity.</span></span> <span data-ttu-id="998d8-139">Toisin sanoen tuoteperusteiset projektisopimusrivit ovat riippumattomia projektiperusteisesta käytöstä.</span><span class="sxs-lookup"><span data-stu-id="998d8-139">In other words, product-based project contract lines are independent of any project-based use.</span></span> 


[!INCLUDE[footer-include](../includes/footer-banner.md)]
