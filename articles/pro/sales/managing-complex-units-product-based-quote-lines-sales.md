---
title: Monimutkaisten yksiköiden, kuten käyttäjäkohtaisten ja kuukausikohtaisten yksiköiden, hallinta tuotepohjaisilla tarjousriveillä – lite
description: Tässä aiheessa on tietoja monimutkaisten yksiköiden hallinnasta tuotepohjaisilla tarjousriveillä
author: rumant
manager: Annbe
ms.date: 10/06/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 2ee46da2f663ef4f5f8fc7f9f89b6fcfd09a1798
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/30/2020
ms.locfileid: "4175572"
---
# <a name="managing-complex-units-such-as-per-user-per-month-for-product-based-quote-lines---lite"></a><span data-ttu-id="67d29-103">Monimutkaisten yksiköiden, kuten käyttäjäkohtaisten ja kuukausikohtaisten yksiköiden, hallinta tuotepohjaisilla tarjousriveillä – lite</span><span class="sxs-lookup"><span data-stu-id="67d29-103">Managing complex units such as per-user, per-month for product-based quote lines - lite</span></span>

<span data-ttu-id="67d29-104">_**Käytetään:** Lite-käyttöönotto – kauppa proformalaskutukseen_</span><span class="sxs-lookup"><span data-stu-id="67d29-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="67d29-105">Dynamics 365 Project Operationsissa käytetään määräkertoimia tukemaan tilausperusteisten tuotteiden myyntiä.</span><span class="sxs-lookup"><span data-stu-id="67d29-105">Dynamics 365 Project Operations uses quantity factors to support the sale of subscription-based products.</span></span> <span data-ttu-id="67d29-106">Tilausperusteisten tuotteiden osalta tarjouksen tai projektisopimuksen rivin määrä ilmaistaan käyttäjäkuukausien lukumääränä.</span><span class="sxs-lookup"><span data-stu-id="67d29-106">For subscription-based products, the quantity on the quote or project contract line is expressed as the number of user-months.</span></span>

<span data-ttu-id="67d29-107">Yleensä tilausohjelmiston hinta tallennetaan luetteloon käyttäjäkohtaisena kuukausihintana.</span><span class="sxs-lookup"><span data-stu-id="67d29-107">Usually, the price of subscription software is stored in the catalog as the price per user per month.</span></span> <span data-ttu-id="67d29-108">Myyntiprosessin aikana tarjousrivillä oleva hinta on yleensä se käyttäjäkohtainen kuukausihinta, jonka IT-myyjä on neuvotellut ja josta hän on antanut alennusta.</span><span class="sxs-lookup"><span data-stu-id="67d29-108">During the sales process, the price on the quote line is usually the per-user, per-month price that was negotiated and discounted by the IT sales agent.</span></span> <span data-ttu-id="67d29-109">Kullakin kaupalla on eri määrä käyttäjiä ja eri määrä tilauskuukausia.</span><span class="sxs-lookup"><span data-stu-id="67d29-109">Each deal has a different number of users and a different number of subscription months.</span></span> <span data-ttu-id="67d29-110">Tarjousrivin summan laskemiseen käytettävä määrä perustuu käyttäjämäärän ja tilauskuukausien määrään kertolaskuun.</span><span class="sxs-lookup"><span data-stu-id="67d29-110">The quantity used to compute the quote line is a product of the number of users and the number of subscription months.</span></span>

<span data-ttu-id="67d29-111">Tällaisen myynnin tukemista varten Project Operationsissa on otettu käyttöön määräkertoimien konsepti.</span><span class="sxs-lookup"><span data-stu-id="67d29-111">To support this type of sale, Project Operations introduced the concept of quantity factors.</span></span> <span data-ttu-id="67d29-112">Määräkertoimet perustuvat Dynamics 365:n tuotemääritteisiin.</span><span class="sxs-lookup"><span data-stu-id="67d29-112">Quantity factors rely on the product attributes in Dynamics 365.</span></span> <span data-ttu-id="67d29-113">Kun määrität tuotteelle tiettyjä ominaisuuksia, voit Project Operationsissa valita osan näistä määritteistä tai ne kaikki määräkertoimiksi.</span><span class="sxs-lookup"><span data-stu-id="67d29-113">When you configure specific properties for a product, Project Operations lets you flag a subset, or all of the properties, as quantity factors.</span></span>

<span data-ttu-id="67d29-114">Project Operations varmistaa, että määräkertoimiksi valitaan vain numeerisia ominaisuuksia tai tuoteominaisuuksia joilla on numeerinen tietotyyppi.</span><span class="sxs-lookup"><span data-stu-id="67d29-114">Project Operations validates that only numeric properties or product properties that have a numeric data type are flagged as quantity factors.</span></span> <span data-ttu-id="67d29-115">Kun lisäät tarjousriviin tuotteen, jolla on määräkertoimia, **Määrä**-kenttä muuttuu vain luku -tilaan.</span><span class="sxs-lookup"><span data-stu-id="67d29-115">When you add a product with quantity factors to a quote line, the **Quantity** field becomes read-only.</span></span> <span data-ttu-id="67d29-116">Kun olet määrittänyt arvot tuoteominaisuuksille, jotka ovat määräkertoimia, Project Operations laskee tarjousrivin määrän.</span><span class="sxs-lookup"><span data-stu-id="67d29-116">After you enter values for product properties that are quantity factors, Project Operations calculates the quantity of the quote line.</span></span>

<span data-ttu-id="67d29-117">Esimerkiksi Dynamics 365 Salesilla voi olla seuraavat ominaisuudet:</span><span class="sxs-lookup"><span data-stu-id="67d29-117">For example, Dynamics 365 Sales might have the following properties:</span></span>

- <span data-ttu-id="67d29-118">**Käyttäjät**: Käyttäjien määrä</span><span class="sxs-lookup"><span data-stu-id="67d29-118">**No of users**: The number of users</span></span>
- <span data-ttu-id="67d29-119">**Kuukaudet**: Tilauskuukausien määrä</span><span class="sxs-lookup"><span data-stu-id="67d29-119">**No of Months**: The number of subscription months</span></span>
- <span data-ttu-id="67d29-120">**Tuote-SKU**</span><span class="sxs-lookup"><span data-stu-id="67d29-120">**Product SKU**</span></span>

<span data-ttu-id="67d29-121">**Käyttäjät**- ja **Kuukaudet**-ominaisuudet voidaan valita määräkertoimiksi muokkaamalla tuoterivin ominaisuuksia.</span><span class="sxs-lookup"><span data-stu-id="67d29-121">You can flag the **No of Users** and **No of Months** properties as quantity factors by editing the properties of the product line.</span></span>

<span data-ttu-id="67d29-122">Voit luoda määräkertoimet tuotteen ominaisuuksista seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="67d29-122">To create Quantity factors from Product properties, follow these steps:</span></span>

1. <span data-ttu-id="67d29-123">Siirry Project Operationsin vasemmassa siirtymisruudussa kohtaan **Myynti** > **Tuotteet**.</span><span class="sxs-lookup"><span data-stu-id="67d29-123">On the Project Operations left navigation pane, go to **Sales** > **Products**.</span></span>
2. <span data-ttu-id="67d29-124">Avaa tuote, jolle on määritettävä määräkertoimet.</span><span class="sxs-lookup"><span data-stu-id="67d29-124">Open the product for which you need to configure quantity factors.</span></span> <span data-ttu-id="67d29-125">Varmista, että tuotteen ominaisuudet on jo määritetty.</span><span class="sxs-lookup"><span data-stu-id="67d29-125">Make sure the product has properties already configured.</span></span>
3. <span data-ttu-id="67d29-126">Valitse tuotteen **Projektitiedot**- sivulla **Määräkertoimet**-välilehti.</span><span class="sxs-lookup"><span data-stu-id="67d29-126">On the **Project Information** page for the Product, select the **Quantity Factors** tab.</span></span>
4. <span data-ttu-id="67d29-127">Valitse aliruudukossa **+ Uusi kenttälaskenta**.</span><span class="sxs-lookup"><span data-stu-id="67d29-127">In the subgrid, select **+ New field computation**.</span></span>
5. <span data-ttu-id="67d29-128">Kirjoita määräkertoimen nimi ja valitse ominaisuuden arvo, joka yhdistetään kentän laskentaan.</span><span class="sxs-lookup"><span data-stu-id="67d29-128">Enter the name of the Quantity factor and select the property value that maps to the field computation.</span></span>
6. <span data-ttu-id="67d29-129">Tallenna ja sulje lomake.</span><span class="sxs-lookup"><span data-stu-id="67d29-129">Save and close the form.</span></span> <span data-ttu-id="67d29-130">Toista nämä vaiheet kaikille ominaisuuksille, joita käytetään tuotepohjaisen tarjousrivin määrän laskennassa.</span><span class="sxs-lookup"><span data-stu-id="67d29-130">Repeat these steps for all properties to use for computing the quantity for the product-based quote line.</span></span>

<span data-ttu-id="67d29-131">Kun luot tuotteelle tuotepohjaisen tarjousrivin, tarjousrivin määrä lukitaan.</span><span class="sxs-lookup"><span data-stu-id="67d29-131">When you create a product-based quote line for a product, the quantity of the quote line will be locked.</span></span> <span data-ttu-id="67d29-132">Määrä lasketaan tuotteena niiden ominaisuusarvojen kertolaskuna, jotka syötetään kyseiselle tarjousriville.</span><span class="sxs-lookup"><span data-stu-id="67d29-132">The quantity will be computed as a product of the property values that you input for that quote line.</span></span>
