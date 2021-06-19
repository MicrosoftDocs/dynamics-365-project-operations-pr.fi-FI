---
title: Hinnoitteludimension poistaminen käytöstä
description: Tässä aiheessa on tietoja hinnoitteludimensioiden käytöstäpoistosta.
author: rumant
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 7b7c1d1b3363c0d158fcf6fda532822354b852a3
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/10/2021
ms.locfileid: "6004527"
---
# <a name="turning-off-a-pricing-dimension"></a><span data-ttu-id="512e7-103">Hinnoitteludimension poistaminen käytöstä</span><span class="sxs-lookup"><span data-stu-id="512e7-103">Turning off a pricing dimension</span></span>

<span data-ttu-id="512e7-104">_**Koskee:** Project Operationsin resurssiin / muuhun kuin resurssiin perustuvia skenaarioita, Lite-käyttöönotto-kaupasta proformalaskutukseen_</span><span class="sxs-lookup"><span data-stu-id="512e7-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="512e7-105">Hinnoittelustrategiaa on ehkä tarkistettava ja päivitettävä muutaman vuoden välein.</span><span class="sxs-lookup"><span data-stu-id="512e7-105">You may need to review and update your pricing strategy every few years.</span></span> <span data-ttu-id="512e7-106">Tekemäsi päivitykset voivat edellyttää, että poistat aiemmin luodun hinnoitteludimension käytöstä ja luot uuden.</span><span class="sxs-lookup"><span data-stu-id="512e7-106">Any updates you make might require that you turn off an existing pricing dimension and create a new one.</span></span> <span data-ttu-id="512e7-107">Olet esimerkiksi ehkä aiemmin hinnoitellut **Roolin** mukaan, mutta olet nyt päättänyt, että hinta määräytyy **Työkokemuksen** perusteella.</span><span class="sxs-lookup"><span data-stu-id="512e7-107">For example, you may have previously priced by **Role**, but now you have decided to price by **Work Experience**.</span></span> <span data-ttu-id="512e7-108">Tämä voi edellyttää, **Roolin** hinnoitteludimensioista ja lisäät **Työkokemuksen** uutena hinnoitteludimensiona.</span><span class="sxs-lookup"><span data-stu-id="512e7-108">This may require you to turn off **Role** as a pricing dimension and create **Work Experience** as a new pricing dimension.</span></span> 

<span data-ttu-id="512e7-109">Hinnoitteludimension poistaminen käytöstä, riippumatta siitä onko se valmiina oleva vai mukautettu, voidaan tehdä asettamalla **Sovelletaan kustannuksiin** ja **Sovelletaan myyntiin** -kenttien arvoksi hinnoitteludimensiossa **Ei**.</span><span class="sxs-lookup"><span data-stu-id="512e7-109">Turning off a pricing dimension, regardless if it is out-of-the-box or custom, can be done by setting the **Applicable to Cost** and **Applicable to Sales** fields of the Pricing Dimension to **No**.</span></span>

<span data-ttu-id="512e7-110">Jos näin tehdään, näyttöön saattaa tulla seuraava virhesanoma: **Hinnoitteludimensiota ei voi päivittää tai poistaa, jos liittyviä hintatietueita on olemassa.**</span><span class="sxs-lookup"><span data-stu-id="512e7-110">However, when you do this, you might receive the error message, **Pricing dimension cannot be updated or deleted if there are associated price records.**</span></span>

![Liiketoimintaprosessivirhe on todennäköinen, kun hinnoitteludimensio poistetaan käytöstä](media/Business-Process-Error.png)

<span data-ttu-id="512e7-112">Tämä virhesanoma ilmaisee, että käytöstä poistettavalle dimensiolle on aiemmin määritetty hintatietueita.</span><span class="sxs-lookup"><span data-stu-id="512e7-112">This error message indicates that there are price records that were previously set up for the dimension that is being turned off.</span></span> <span data-ttu-id="512e7-113">Kaikki **Roolihinta** ja **Rooolihinnan korotus** -tietueet, jotka viittaavat dimensioon tulee poistaa ennen kuin dimension sovellettavuudeksi voidaan asettaa **Ei**.</span><span class="sxs-lookup"><span data-stu-id="512e7-113">All **Role Price** and **Role Price Markup** records that refer to a dimension must be deleted before the dimension’s applicability can be to set to **No**.</span></span> <span data-ttu-id="512e7-114">Tämä sääntö koskee sekä valmiita hinnoitteludimensioita että mahdollisesti luotuja mukautettuja hinnoitteludimensioita.</span><span class="sxs-lookup"><span data-stu-id="512e7-114">This rule applies to both out-of-the-box pricing dimensions and any custom pricing dimensions that you may have created.</span></span> <span data-ttu-id="512e7-115">Tämän vahvistuksen syy on se, että kullakin **Roolihinta**-tietueella on oltava ainutlaatuinen dimensioyhdistelmä.</span><span class="sxs-lookup"><span data-stu-id="512e7-115">The reason for this validation is because each **Role Price** record must have a unique combination of dimensions.</span></span> <span data-ttu-id="512e7-116">Esimerkiksi hinnastossa nimeltä **US Cost Rates 2018** on seuraavat **Roolihinta**-rivit.</span><span class="sxs-lookup"><span data-stu-id="512e7-116">For example, on a price list called **US Cost Rates 2018**, you have the following **Role price** rows.</span></span> 

| <span data-ttu-id="512e7-117">Vakio-otsikko</span><span class="sxs-lookup"><span data-stu-id="512e7-117">Standard Title</span></span>         | <span data-ttu-id="512e7-118">Organisaatioyksikkö</span><span class="sxs-lookup"><span data-stu-id="512e7-118">Org Unit</span></span>    |<span data-ttu-id="512e7-119">Yksikkö</span><span class="sxs-lookup"><span data-stu-id="512e7-119">Unit</span></span>   |<span data-ttu-id="512e7-120">Hinta</span><span class="sxs-lookup"><span data-stu-id="512e7-120">Price</span></span>  |<span data-ttu-id="512e7-121">Valuutta</span><span class="sxs-lookup"><span data-stu-id="512e7-121">Currency</span></span>  |
| -----------------------|-------------|-------|-------|----------|
| <span data-ttu-id="512e7-122">Järjestelmäinsinööri</span><span class="sxs-lookup"><span data-stu-id="512e7-122">Systems Engineer</span></span>|<span data-ttu-id="512e7-123">Contoso US</span><span class="sxs-lookup"><span data-stu-id="512e7-123">Contoso US</span></span>|<span data-ttu-id="512e7-124">tunti</span><span class="sxs-lookup"><span data-stu-id="512e7-124">Hour</span></span>| <span data-ttu-id="512e7-125">100</span><span class="sxs-lookup"><span data-stu-id="512e7-125">100</span></span>|<span data-ttu-id="512e7-126">USD</span><span class="sxs-lookup"><span data-stu-id="512e7-126">USD</span></span>|
| <span data-ttu-id="512e7-127">Vanhempi järjestelmäinsinööri</span><span class="sxs-lookup"><span data-stu-id="512e7-127">Senior Systems Engineer</span></span>|<span data-ttu-id="512e7-128">Contoso US</span><span class="sxs-lookup"><span data-stu-id="512e7-128">Contoso US</span></span>|<span data-ttu-id="512e7-129">tunti</span><span class="sxs-lookup"><span data-stu-id="512e7-129">Hour</span></span>| <span data-ttu-id="512e7-130">150</span><span class="sxs-lookup"><span data-stu-id="512e7-130">150</span></span>| <span data-ttu-id="512e7-131">USD</span><span class="sxs-lookup"><span data-stu-id="512e7-131">USD</span></span>|


<span data-ttu-id="512e7-132">Kun poistat käytöstä **Vakio-otsikon** hinnoitteludimensiona, ja hinnoittelumoottori etsii hintaa, se käyttää ainoastaan **Organisaatioyksikkö**-arvoa syötekontekstista.</span><span class="sxs-lookup"><span data-stu-id="512e7-132">When you turn off **Standard Title** as the pricing dimension, and the pricing engine searches for a price, it will only use the **Org Unit** value from the input context.</span></span> <span data-ttu-id="512e7-133">Jos syötekontekstin **Organisaatioyksikkö** on ”Contoso US”, lopputulos ei ole deterministinen, koska molemmat rivit täyttävät ehdon.</span><span class="sxs-lookup"><span data-stu-id="512e7-133">If the **Org Unit** of the input context is “Contoso US”, the result will be non-deterministic because both the rows will match.</span></span> <span data-ttu-id="512e7-134">Jotta tämä skenaario voidaan välttää, järjestelmä tarkistaa **Roolihinta**-tietueita luotaessa, että dimensioiden yhdistelmä on ainutlaatuinen.</span><span class="sxs-lookup"><span data-stu-id="512e7-134">To avoid this scenario, when you create **Role Price** records, the system validates that the combination of dimensions is unique.</span></span> <span data-ttu-id="512e7-135">Jos dimensio on poistettu käytöstä sen jälkeen kun **Roolihinta**-tietueita on luotu, tätä rajoitetta voidaan rikkoa.</span><span class="sxs-lookup"><span data-stu-id="512e7-135">If the dimension is turned off after the **Role Price** records are created, this constraint can be violated.</span></span> <span data-ttu-id="512e7-136">Siksi on tarpeen, että ennen kuin poistat dimension käytöstä, poistat kaikki ne **Roolihinta**- ja **Roolihinnan korotus** -rivit, joilla on käytetty tätä dimension arvoa.</span><span class="sxs-lookup"><span data-stu-id="512e7-136">Therefore, it is required that before you turn off a dimension, you delete all **Role Price** and **Role Price Markup** rows that have that dimension value populated.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]