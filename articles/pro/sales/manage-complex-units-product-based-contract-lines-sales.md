---
title: Tuotepohjaisten sopimusrivien monitasoisten yksiköiden hallinta – lite
description: Tässä aiheessa on tietoja tilauspohjaisten tuotteiden myynnin tukemisesta.
author: rumant
ms.date: 10/28/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 86da5a96919438e883b56fc8ecfe765f70a789ff
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/10/2021
ms.locfileid: "6003177"
---
# <a name="manage-complex-units-for-product-based-contract-lines---lite"></a><span data-ttu-id="f49a3-103">Tuotepohjaisten sopimusrivien monitasoisten yksiköiden hallinta – lite</span><span class="sxs-lookup"><span data-stu-id="f49a3-103">Manage complex units for product-based contract lines - lite</span></span>

<span data-ttu-id="f49a3-104">_**Käytetään:** Lite-käyttöönotto – kauppa proformalaskutukseen_</span><span class="sxs-lookup"><span data-stu-id="f49a3-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="f49a3-105">Dynamics 365 Project Operationsissa käytetään määräkertoimia tukemaan tilausperusteisten tuotteiden myyntiä.</span><span class="sxs-lookup"><span data-stu-id="f49a3-105">Dynamics 365 Project Operations uses quantity factors to support the sale of subscription-based products.</span></span> <span data-ttu-id="f49a3-106">Tilausperusteisten tuotteiden osalta sopimuksen tai projektin sopimusrivin määrä ilmaistaan käyttäjäkuukausien lukumääränä.</span><span class="sxs-lookup"><span data-stu-id="f49a3-106">For subscription-based products, the quantity on the contract or project contract line is expressed as the number of user-months.</span></span>

<span data-ttu-id="f49a3-107">Tilausohjelmiston hinta tallennetaan luetteloon käyttäjäkohtaisena kuukausihintana.</span><span class="sxs-lookup"><span data-stu-id="f49a3-107">The price of subscription software is stored in the catalog as the price per-user, per-month.</span></span> <span data-ttu-id="f49a3-108">Myyntiprosessin aikana sopimusrivillä oleva hinta on yleensä se käyttäjäkohtainen kuukausihinta, jonka myyjä on neuvotellut ja josta hän on antanut alennusta.</span><span class="sxs-lookup"><span data-stu-id="f49a3-108">During the sales process, the price on the contract line is usually the per-user, per-month price that was negotiated and discounted by the sales agent.</span></span> <span data-ttu-id="f49a3-109">Kullakin kaupalla on eri määrä käyttäjiä ja eri määrä tilauskuukausia.</span><span class="sxs-lookup"><span data-stu-id="f49a3-109">Each deal has a different number of users and a different number of subscription months.</span></span> <span data-ttu-id="f49a3-110">Sopimusrivin summan laskemiseen käytettävä määrä perustuu käyttäjämäärään ja tilauskuukausien määrään.</span><span class="sxs-lookup"><span data-stu-id="f49a3-110">The quantity used to calculate the amount of the contract line is a product of the number of users and the number of subscription months.</span></span>

<span data-ttu-id="f49a3-111">Tällaisen myynnin tukemista varten Project Operations tukee *määräkertoimien* käsitettä.</span><span class="sxs-lookup"><span data-stu-id="f49a3-111">To support this type of sale, Project Operations supports the concept of *quantity factors*.</span></span> <span data-ttu-id="f49a3-112">Määräkertoimet perustuvat tuotemääritteisiin.</span><span class="sxs-lookup"><span data-stu-id="f49a3-112">Quantity factors rely on product attributes.</span></span> <span data-ttu-id="f49a3-113">Kun määrität tuotteelle tiettyjä ominaisuuksia, voit valita osan näistä määritteistä tai ne kaikki määräkertoimiksi.</span><span class="sxs-lookup"><span data-stu-id="f49a3-113">When you configure specific properties for a product, you can flag a subset of those properties, or all the properties, as quantity factors.</span></span>

<span data-ttu-id="f49a3-114">Project Operations varmistaa, että määräkertoimiksi valitaan vain numeerisia ominaisuuksia tai tuoteominaisuuksia joilla on numeerinen tietotyyppi.</span><span class="sxs-lookup"><span data-stu-id="f49a3-114">Project Operations validates that only numeric properties or product properties that have a numeric data type are flagged as quantity factors.</span></span> <span data-ttu-id="f49a3-115">Kun tuote, johon on määritetty määräkertoimia, lisätään sopimusriville, **Määrä**-kenttä muuttuu vain luku -muotoiseksi.</span><span class="sxs-lookup"><span data-stu-id="f49a3-115">When a product with configured quantity factors is added to a contract line, the **Quantity** field  becomes read-only.</span></span> <span data-ttu-id="f49a3-116">Kun olet määrittänyt arvot tuoteominaisuuksille, jotka ovat määräkertoimia, Project Operations laskee sopimusrivin määrän.</span><span class="sxs-lookup"><span data-stu-id="f49a3-116">After you enter values for product properties that are quantity factors, Project Operations calculates the quantity of the contract line.</span></span>

<span data-ttu-id="f49a3-117">Esimerkiksi Dynamics 365 Salesilla voi olla seuraavat ominaisuudet:</span><span class="sxs-lookup"><span data-stu-id="f49a3-117">For example, Dynamics 365 Sales might have the following properties:</span></span>

- <span data-ttu-id="f49a3-118">**Käyttäjät**: käyttäjien määrä.</span><span class="sxs-lookup"><span data-stu-id="f49a3-118">**No of users**: The number of users.</span></span>
- <span data-ttu-id="f49a3-119">**Kuukaudet**: tilauskuukausien määrä.</span><span class="sxs-lookup"><span data-stu-id="f49a3-119">**No of Months**: The number of subscription months.</span></span>
- <span data-ttu-id="f49a3-120">**Tuotteen SKU**: tuotteen varastointiyksikkö (SKU).</span><span class="sxs-lookup"><span data-stu-id="f49a3-120">**Product SKU**: The stock keeping unit (SKU) for the product.</span></span>

<span data-ttu-id="f49a3-121">**Käyttäjät**- ja **Kuukaudet**-ominaisuudet voidaan valita määräkertoimiksi muokkaamalla tuoterivin ominaisuuksia.</span><span class="sxs-lookup"><span data-stu-id="f49a3-121">The **No of Users** and **No of Months** properties can be flagged as quantity factors by editing the properties of the product line.</span></span>

<span data-ttu-id="f49a3-122">Määräkertoimia luodaan tuotteen ominaisuuksista seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="f49a3-122">To create quantity factors from product properties, complete the following steps.</span></span>

1. <span data-ttu-id="f49a3-123">Valitse **Project Operationsissa** **Myynti - tuotteet**.</span><span class="sxs-lookup"><span data-stu-id="f49a3-123">On the **Project Operations**, select **Sales-Products**.</span></span>
2. <span data-ttu-id="f49a3-124">Avaa tuote, jolle määräkertoimet on määritettävä.</span><span class="sxs-lookup"><span data-stu-id="f49a3-124">Open the product for which you need to set up quantity factors.</span></span> <span data-ttu-id="f49a3-125">Varmista, että tuotteen ominaisuudet on jo määritetty.</span><span class="sxs-lookup"><span data-stu-id="f49a3-125">Make sure that the product has properties already set up.</span></span>
3. <span data-ttu-id="f49a3-126">Valitse **Projektin tiedot** -sivulla **Määräkertoimet**-välilehti.</span><span class="sxs-lookup"><span data-stu-id="f49a3-126">On the **Project Information** page, select the **Quantity Factors** tab.</span></span>
4. <span data-ttu-id="f49a3-127">Valitse aliruudukossa **+ Uusi kenttälaskenta**.</span><span class="sxs-lookup"><span data-stu-id="f49a3-127">In the subgrid, select **+ New field computation**.</span></span>
5. <span data-ttu-id="f49a3-128">Kirjoita **määräkertoimen** nimi ja valitse ominaisuuden arvo, joka yhdistetään kentän laskentaan.</span><span class="sxs-lookup"><span data-stu-id="f49a3-128">Enter the name of the **Quantity Factor** and select the property value that maps to the field computation.</span></span>
6. <span data-ttu-id="f49a3-129">Tallenna ja sulje lomake.</span><span class="sxs-lookup"><span data-stu-id="f49a3-129">Save and close the form.</span></span>
7. <span data-ttu-id="f49a3-130">Toista vaiheet 2–6 kaikkien niiden ominaisuuksien osalta, jotka yhdessä muodostavat tuotepohjaisen sopimusrivin määrän.</span><span class="sxs-lookup"><span data-stu-id="f49a3-130">Repeat steps 2-6 for all the properties that together will make up the quantity for the product-based contract line.</span></span>

<span data-ttu-id="f49a3-131">Kun määräkertoimet on määritetty ja käyttäjä luo tuotteelle sopimusrivin, sopimusrivin määrä lukitaan.</span><span class="sxs-lookup"><span data-stu-id="f49a3-131">With quantity factors set up, when the user creates a contract line for this product, the quantity of the contract line is locked.</span></span> <span data-ttu-id="f49a3-132">Määrä lasketaan sitten kyseisen sopimusrivin ominaisuusarvojen tuotteena.</span><span class="sxs-lookup"><span data-stu-id="f49a3-132">The quantity is then calculated as a product of the property values for that contract line.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]