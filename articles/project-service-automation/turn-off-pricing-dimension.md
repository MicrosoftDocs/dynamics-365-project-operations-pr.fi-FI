---
title: Hinnoitteludimension poistaminen käytöstä
description: Tämä aihe näyttää, miten hinnoitteludimensiot määritetään Project Service -ratkaisussa.
author: Rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 11/06/2018
ms.topic: article
ms.prod: Project Service
ms.service: business-applications
ms.assetid: 689e5a8d-e39a-471d-a6c4-7e2fc3bb5590
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
ms.openlocfilehash: 5cf2cd86fb1eba50c8e08b2bd624669ab0b1deb3
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/24/2020
ms.locfileid: "3751213"
---
# <a name="turn-off-a-pricing-dimension"></a><span data-ttu-id="a22ac-103">Hinnoitteludimension poistaminen käytöstä</span><span class="sxs-lookup"><span data-stu-id="a22ac-103">Turn off a pricing dimension</span></span>

<span data-ttu-id="a22ac-104">Hinnoittelustrategiaa on ehkä tarkistettava ja päivitettävä muutaman vuoden välein.</span><span class="sxs-lookup"><span data-stu-id="a22ac-104">You may need to review and update your pricing strategy every few years.</span></span> <span data-ttu-id="a22ac-105">Tekemäsi päivitykset voivat edellyttää, että poistat aiemmin luodun hinnoitteludimension käytöstä ja luot uuden.</span><span class="sxs-lookup"><span data-stu-id="a22ac-105">Any updates you make might require that you turn off an existing pricing dimension and create a new one.</span></span> <span data-ttu-id="a22ac-106">Olet esimerkiksi ehkä aiemmin hinnoitellut **Roolin** mukaan, mutta olet nyt päättänyt, että hinta määräytyy **Työkokemuksen** perusteella.</span><span class="sxs-lookup"><span data-stu-id="a22ac-106">For example, you may have previously priced by **Role**, but now you have decided to price by **Work Experience**.</span></span> <span data-ttu-id="a22ac-107">Tämä voi edellyttää, **Roolin** hinnoitteludimensioista ja lisäät **Työkokemuksen** uutena hinnoitteludimensiona.</span><span class="sxs-lookup"><span data-stu-id="a22ac-107">This may require you to turn off **Role** as a pricing dimension and create **Work Expereince** as a new pricing dimension.</span></span> 

<span data-ttu-id="a22ac-108">Hinnoitteludimension poistaminen käytöstä, riippumatta siitä onko se valmiina oleva vai mukautettu, voidaan tehdä asettamalla **Sovelletaan kustannuksiin** ja **Sovelletaan myyntiin** -kenttien arvoksi hinnoitteludimensiossa **Ei**.</span><span class="sxs-lookup"><span data-stu-id="a22ac-108">Turning off a pricing dimension, regardless if it is out-of-the-box or custom, can be done by setting the **Applicable to Cost** and **Applicable to Sales** fields of the Pricing Dimension to **No**.</span></span>

<span data-ttu-id="a22ac-109">Kun teet näin, näyttöön voi kuitenkin tulla seuraava virhesanoma.</span><span class="sxs-lookup"><span data-stu-id="a22ac-109">However, when you do this, you might receive the following error message.</span></span>

![Liiketoimintaprosessivirhe on todennäköinen, kun hinnoitteludimensio poistetaan käytöstä](media/Business-Process-Error.png)


<span data-ttu-id="a22ac-111">Tämä virhesanoma ilmaisee, että käytöstä poistettavalle dimensiolle on aiemmin määritetty hintatietueita.</span><span class="sxs-lookup"><span data-stu-id="a22ac-111">This error message indicates that there are price records that were previously set up for the dimension that is being turned off.</span></span> <span data-ttu-id="a22ac-112">Kaikki **Roolihinta** ja **Rooolihinnan korotus** -tietueet, jotka viittaavat dimensioon tulee poistaa ennen kuin dimension sovellettavuudeksi voidaan asettaa **Ei**.</span><span class="sxs-lookup"><span data-stu-id="a22ac-112">All **Role Price** and **Role Price Markup** records that refer to a dimension must be deleted before the dimension’s applicability can be to set to **No**.</span></span> <span data-ttu-id="a22ac-113">Tämä sääntö koskee sekä valmiita hinnoitteludimensioita että mahdollisesti luotuja mukautettuja hinnoitteludimensioita.</span><span class="sxs-lookup"><span data-stu-id="a22ac-113">This rule applies to both out-of-the-box pricing dimensions and any custom pricing dimensions that you may have created.</span></span> <span data-ttu-id="a22ac-114">Tämän vahvistuksen syy on se, että Project Service -palvelussa on rajoitus, jonka mukaan kullakin **Roolihinta**-tietueella on oltava ainutlaatuinen dimensioyhdistelmä.</span><span class="sxs-lookup"><span data-stu-id="a22ac-114">The reason for this validation is because Project Service has a constraint that each **Role Price** record must have a unique combination of dimensions.</span></span> <span data-ttu-id="a22ac-115">Esimerkiksi hinnastossa nimeltä **US Cost Rates 2018** on seuraavat **Roolihinta**-rivit.</span><span class="sxs-lookup"><span data-stu-id="a22ac-115">For example, on a price list called **US Cost Rates 2018**, you have the following **Role price** rows.</span></span> 

| <span data-ttu-id="a22ac-116">Vakio-otsikko</span><span class="sxs-lookup"><span data-stu-id="a22ac-116">Standard Title</span></span>         | <span data-ttu-id="a22ac-117">Organisaatioyksikkö</span><span class="sxs-lookup"><span data-stu-id="a22ac-117">Org Unit</span></span>    |<span data-ttu-id="a22ac-118">Yksikkö</span><span class="sxs-lookup"><span data-stu-id="a22ac-118">Unit</span></span>   |<span data-ttu-id="a22ac-119">Hinta</span><span class="sxs-lookup"><span data-stu-id="a22ac-119">Price</span></span>  |<span data-ttu-id="a22ac-120">Valuutta</span><span class="sxs-lookup"><span data-stu-id="a22ac-120">Currency</span></span>  |
| -----------------------|-------------|-------|-------|----------|
| <span data-ttu-id="a22ac-121">Järjestelmäinsinööri</span><span class="sxs-lookup"><span data-stu-id="a22ac-121">Systems Engineer</span></span>|<span data-ttu-id="a22ac-122">Contoso US</span><span class="sxs-lookup"><span data-stu-id="a22ac-122">Contoso US</span></span>|<span data-ttu-id="a22ac-123">Hour</span><span class="sxs-lookup"><span data-stu-id="a22ac-123">Hour</span></span>| <span data-ttu-id="a22ac-124">100</span><span class="sxs-lookup"><span data-stu-id="a22ac-124">100</span></span>|<span data-ttu-id="a22ac-125">USD</span><span class="sxs-lookup"><span data-stu-id="a22ac-125">USD</span></span>|
| <span data-ttu-id="a22ac-126">Vanhempi järjestelmäinsinööri</span><span class="sxs-lookup"><span data-stu-id="a22ac-126">Senior Systems Engineer</span></span>|<span data-ttu-id="a22ac-127">Contoso US</span><span class="sxs-lookup"><span data-stu-id="a22ac-127">Contoso US</span></span>|<span data-ttu-id="a22ac-128">Hour</span><span class="sxs-lookup"><span data-stu-id="a22ac-128">Hour</span></span>| <span data-ttu-id="a22ac-129">150</span><span class="sxs-lookup"><span data-stu-id="a22ac-129">150</span></span>| <span data-ttu-id="a22ac-130">USD</span><span class="sxs-lookup"><span data-stu-id="a22ac-130">USD</span></span>|


<span data-ttu-id="a22ac-131">Kun poistat käytöstä **Vakio-otsikon** hinnoitteludimensiona, ja Project Servicen hinnoittelumoottori etsii hintaa, se käyttää ainoastaan **Organisaatioyksikkö**-arvoa syötekontekstista.</span><span class="sxs-lookup"><span data-stu-id="a22ac-131">When you turn off **Standard Title** as the pricing dimension, and the Project Service pricing engine searches for a price, it will only use the **Org Unit** value from the input context.</span></span> <span data-ttu-id="a22ac-132">Jos syötekontekstin **Organisaatioyksikkö** on “Contoso US”, lopputulos ei ole deterministinen, koska molemmat rivit täyttävät ehdon.</span><span class="sxs-lookup"><span data-stu-id="a22ac-132">If the **Org Unit** of the input context is “Contoso US”, the result will be non-deterministic because both the rows will match.</span></span> <span data-ttu-id="a22ac-133">Jotta tämä skenaario voidaan välttää, Project Service tarkistaa **Roolihinta**-tietueita luotaessa, että dimensioiden yhdistelmä on ainutlaatuinen.</span><span class="sxs-lookup"><span data-stu-id="a22ac-133">To avoid this scenario, when you create **Role Price** records, Project Service validates that the combination of dimensions is unique.</span></span> <span data-ttu-id="a22ac-134">Jos dimensio on poistettu käytöstä sen jälkeen kun **Roolihinta**-tietueita on luotu, tätä rajoitetta voidaan rikkoa.</span><span class="sxs-lookup"><span data-stu-id="a22ac-134">If the dimension is turned off after the **Role Price** records are created, this constraint can be violated.</span></span> <span data-ttu-id="a22ac-135">Siksi on tarpeen, että ennen kuin poistat dimension käytöstä, poistat kaikki ne **Roolihinta**- ja **Roolihinnan korotus** -rivit, joilla on käytetty tätä dimension arvoa.</span><span class="sxs-lookup"><span data-stu-id="a22ac-135">Therefore, it is required that before you turn off a dimension, you delete all **Role Price** and **Role Price Markup** rows that have that dimension value populated.</span></span>

