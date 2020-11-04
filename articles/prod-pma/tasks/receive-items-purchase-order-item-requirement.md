---
title: Nimikkeiden vastaanotto nimiketarpeeseen perustuvan ostotilauksen perusteella
description: Tässä aiheessa kerrotaan, miten voidaan vastaanottaa nimikkeitä nimiketarpeeseen perustuvan ostotilauksen perusteella.
author: Yowelle
manager: AnnBe
ms.date: 08/06/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage, ProjTable, ProjSalesItemReq, InventItemIdLookupSimple, PurchCreateFromSalesOrder, VendAccountItemLookup, PurchTable, PurchEditLines
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a5b3622458da957ed150311f6ea75d5f1444d5f1
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/16/2020
ms.locfileid: "4075515"
---
# <a name="receive-items-on-purchase-order-from-item-requirement"></a><span data-ttu-id="e6099-103">Nimikkeiden vastaanotto nimiketarpeeseen perustuvan ostotilauksen perusteella</span><span class="sxs-lookup"><span data-stu-id="e6099-103">Receive items on purchase order from item requirement</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="e6099-104">Tässä aiheessa kerrotaan, miten voidaan vastaanottaa nimikkeitä nimiketarpeeseen perustuvan ostotilauksen perusteella.</span><span class="sxs-lookup"><span data-stu-id="e6099-104">This topic explains how to receive items on a purchase order from an item requirement.</span></span>

<span data-ttu-id="e6099-105">Kun käytät nimiketarvetta nimiketapahtuman sijaan, voit suunnitella toimituksen toteutettavaksi juuri ennen nimikkeen todellista käyttöä, luoda ostotilauksen, lisätä nimikkeen kauppasopimuskehykseen ja lisätä nimiketarpeen tuotannon suunnitteluun.</span><span class="sxs-lookup"><span data-stu-id="e6099-105">By using an item requirement instead of an item transaction, you can plan for delivery just before the item is actually used, create a purchase order, include the item in the trade-agreement framework, and include the item requirement in production planning.</span></span> 

<span data-ttu-id="e6099-106">Tämä tehtävä käyttää USSI-tietojoukkoa.</span><span class="sxs-lookup"><span data-stu-id="e6099-106">This task uses the USSI data set.</span></span>

1. <span data-ttu-id="e6099-107">Valitse siirtymisruudussa **Moduulit > Projektinhallinta ja kirjanpito > Projektit > Kaikki projektit**.</span><span class="sxs-lookup"><span data-stu-id="e6099-107">In the navigation pane, go to **Modules > Project management and accounting > Projects > All projects**.</span></span>
2. <span data-ttu-id="e6099-108">Valitse luettelossa halutun rivin linkki.</span><span class="sxs-lookup"><span data-stu-id="e6099-108">In the list, select the link in the desired row.</span></span>
3. <span data-ttu-id="e6099-109">Valitse toimintoruudussa **Suunnittelu**.</span><span class="sxs-lookup"><span data-stu-id="e6099-109">On the Action Pane, select **Plan**.</span></span>
4. <span data-ttu-id="e6099-110">Valitse **Nimiketarpeet**.</span><span class="sxs-lookup"><span data-stu-id="e6099-110">Select **Item requirements**.</span></span>
5. <span data-ttu-id="e6099-111">Valitse **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="e6099-111">Select **New**.</span></span>
6. <span data-ttu-id="e6099-112">Syötä riville arvo tai valitse siltä arvo **Nimikenumero** -kentässä.</span><span class="sxs-lookup"><span data-stu-id="e6099-112">In the new row, enter or select a value in the **Item number** field.</span></span>
7. <span data-ttu-id="e6099-113">Kirjoita **Määrä** -kenttään numero.</span><span class="sxs-lookup"><span data-stu-id="e6099-113">In the **Quantity** field, enter a number.</span></span>
8. <span data-ttu-id="e6099-114">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="e6099-114">Select **Save**.</span></span>
9. <span data-ttu-id="e6099-115">Valitse toimintoruudussa **Hallitse**.</span><span class="sxs-lookup"><span data-stu-id="e6099-115">On the Action Pane, select **Manage**.</span></span>
10. <span data-ttu-id="e6099-116">Valitse **Funktiot**.</span><span class="sxs-lookup"><span data-stu-id="e6099-116">Select **Functions**.</span></span>
11. <span data-ttu-id="e6099-117">Valitse **Luo uusi ostotilaus**.</span><span class="sxs-lookup"><span data-stu-id="e6099-117">Select **Create purchase order**.</span></span>
12. <span data-ttu-id="e6099-118">Valitse **Sisällytä kaikki** -valintaruutu.</span><span class="sxs-lookup"><span data-stu-id="e6099-118">Select the **Include all** check box.</span></span>
13. <span data-ttu-id="e6099-119">Kirjoita tai valitse arvo **Toimittajatili** -kenttään.</span><span class="sxs-lookup"><span data-stu-id="e6099-119">In the **Vendor account** field, enter or select a value.</span></span>
14. <span data-ttu-id="e6099-120">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="e6099-120">Select **OK**.</span></span>
15. <span data-ttu-id="e6099-121">Siirry siirtymisruudussa kohtaan **Moduulit > Ostoreskontra > Ostotilaukset > Kaikki ostotilaukset**.</span><span class="sxs-lookup"><span data-stu-id="e6099-121">In the navigation pane, go to **Modules > Accounts payable > Purchase orders > All purchase orders**.</span></span>
16. <span data-ttu-id="e6099-122">Valitse luettelossa halutun rivin linkki.</span><span class="sxs-lookup"><span data-stu-id="e6099-122">In the list, select the link in the desired row.</span></span>
17. <span data-ttu-id="e6099-123">Valitse toimintoruudussa **Osta**.</span><span class="sxs-lookup"><span data-stu-id="e6099-123">On the Action Pane, select **Purchase**.</span></span>
18. <span data-ttu-id="e6099-124">Valitse **Vahvista**.</span><span class="sxs-lookup"><span data-stu-id="e6099-124">Select **Confirm**.</span></span>
19. <span data-ttu-id="e6099-125">Valitse toimintoruudussa **Vastaanota**.</span><span class="sxs-lookup"><span data-stu-id="e6099-125">On the Action Pane, select **Receive**.</span></span>
20. <span data-ttu-id="e6099-126">Valitse **Tuoteresepti**.</span><span class="sxs-lookup"><span data-stu-id="e6099-126">Select **Product receipt**.</span></span>
21. <span data-ttu-id="e6099-127">Kirjoita arvo **Tuoteresepti** -kenttään.</span><span class="sxs-lookup"><span data-stu-id="e6099-127">In the **Product receipt** field, type a value.</span></span>
22. <span data-ttu-id="e6099-128">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="e6099-128">Select **OK**.</span></span>

