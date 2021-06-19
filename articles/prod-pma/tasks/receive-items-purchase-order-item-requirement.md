---
title: Nimikkeiden vastaanotto nimiketarpeeseen perustuvan ostotilauksen perusteella
description: Tässä aiheessa kerrotaan, miten voidaan vastaanottaa nimikkeitä nimiketarpeeseen perustuvan ostotilauksen perusteella.
author: Yowelle
ms.date: 08/06/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ProjProjectsListPage, ProjTable, ProjSalesItemReq, InventItemIdLookupSimple, PurchCreateFromSalesOrder, VendAccountItemLookup, PurchTable, PurchEditLines
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0e0c4a75f1d86538cc773af1f7c0ae3c83ef0ad5
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/10/2021
ms.locfileid: "6011682"
---
# <a name="receive-items-on-purchase-order-from-item-requirement"></a><span data-ttu-id="18636-103">Nimikkeiden vastaanotto nimiketarpeeseen perustuvan ostotilauksen perusteella</span><span class="sxs-lookup"><span data-stu-id="18636-103">Receive items on purchase order from item requirement</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="18636-104">Tässä aiheessa kerrotaan, miten voidaan vastaanottaa nimikkeitä nimiketarpeeseen perustuvan ostotilauksen perusteella.</span><span class="sxs-lookup"><span data-stu-id="18636-104">This topic explains how to receive items on a purchase order from an item requirement.</span></span>

<span data-ttu-id="18636-105">Kun käytät nimiketarvetta nimiketapahtuman sijaan, voit suunnitella toimituksen toteutettavaksi juuri ennen nimikkeen todellista käyttöä, luoda ostotilauksen, lisätä nimikkeen kauppasopimuskehykseen ja lisätä nimiketarpeen tuotannon suunnitteluun.</span><span class="sxs-lookup"><span data-stu-id="18636-105">By using an item requirement instead of an item transaction, you can plan for delivery just before the item is actually used, create a purchase order, include the item in the trade-agreement framework, and include the item requirement in production planning.</span></span> 

<span data-ttu-id="18636-106">Tämä tehtävä käyttää USSI-tietojoukkoa.</span><span class="sxs-lookup"><span data-stu-id="18636-106">This task uses the USSI data set.</span></span>

1. <span data-ttu-id="18636-107">Valitse siirtymisruudussa **Moduulit > Projektinhallinta ja kirjanpito > Projektit > Kaikki projektit**.</span><span class="sxs-lookup"><span data-stu-id="18636-107">In the navigation pane, go to **Modules > Project management and accounting > Projects > All projects**.</span></span>
2. <span data-ttu-id="18636-108">Valitse luettelossa halutun rivin linkki.</span><span class="sxs-lookup"><span data-stu-id="18636-108">In the list, select the link in the desired row.</span></span>
3. <span data-ttu-id="18636-109">Valitse toimintoruudussa **Suunnittelu**.</span><span class="sxs-lookup"><span data-stu-id="18636-109">On the Action Pane, select **Plan**.</span></span>
4. <span data-ttu-id="18636-110">Valitse **Nimiketarpeet**.</span><span class="sxs-lookup"><span data-stu-id="18636-110">Select **Item requirements**.</span></span>
5. <span data-ttu-id="18636-111">Valitse **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="18636-111">Select **New**.</span></span>
6. <span data-ttu-id="18636-112">Syötä riville arvo tai valitse siltä arvo **Nimikenumero**-kentässä.</span><span class="sxs-lookup"><span data-stu-id="18636-112">In the new row, enter or select a value in the **Item number** field.</span></span>
7. <span data-ttu-id="18636-113">Kirjoita **Määrä**-kenttään numero.</span><span class="sxs-lookup"><span data-stu-id="18636-113">In the **Quantity** field, enter a number.</span></span>
8. <span data-ttu-id="18636-114">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="18636-114">Select **Save**.</span></span>
9. <span data-ttu-id="18636-115">Valitse toimintoruudussa **Hallitse**.</span><span class="sxs-lookup"><span data-stu-id="18636-115">On the Action Pane, select **Manage**.</span></span>
10. <span data-ttu-id="18636-116">Valitse **Funktiot**.</span><span class="sxs-lookup"><span data-stu-id="18636-116">Select **Functions**.</span></span>
11. <span data-ttu-id="18636-117">Valitse **Luo uusi ostotilaus**.</span><span class="sxs-lookup"><span data-stu-id="18636-117">Select **Create purchase order**.</span></span>
12. <span data-ttu-id="18636-118">Valitse **Sisällytä kaikki** -valintaruutu.</span><span class="sxs-lookup"><span data-stu-id="18636-118">Select the **Include all** check box.</span></span>
13. <span data-ttu-id="18636-119">Kirjoita tai valitse arvo **Toimittajatili** -kenttään.</span><span class="sxs-lookup"><span data-stu-id="18636-119">In the **Vendor account** field, enter or select a value.</span></span>
14. <span data-ttu-id="18636-120">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="18636-120">Select **OK**.</span></span>
15. <span data-ttu-id="18636-121">Siirry siirtymisruudussa kohtaan **Moduulit > Ostoreskontra > Ostotilaukset > Kaikki ostotilaukset**.</span><span class="sxs-lookup"><span data-stu-id="18636-121">In the navigation pane, go to **Modules > Accounts payable > Purchase orders > All purchase orders**.</span></span>
16. <span data-ttu-id="18636-122">Valitse luettelossa halutun rivin linkki.</span><span class="sxs-lookup"><span data-stu-id="18636-122">In the list, select the link in the desired row.</span></span>
17. <span data-ttu-id="18636-123">Valitse toimintoruudussa **Osta**.</span><span class="sxs-lookup"><span data-stu-id="18636-123">On the Action Pane, select **Purchase**.</span></span>
18. <span data-ttu-id="18636-124">Valitse **Vahvista**.</span><span class="sxs-lookup"><span data-stu-id="18636-124">Select **Confirm**.</span></span>
19. <span data-ttu-id="18636-125">Valitse toimintoruudussa **Vastaanota**.</span><span class="sxs-lookup"><span data-stu-id="18636-125">On the Action Pane, select **Receive**.</span></span>
20. <span data-ttu-id="18636-126">Valitse **Tuoteresepti**.</span><span class="sxs-lookup"><span data-stu-id="18636-126">Select **Product receipt**.</span></span>
21. <span data-ttu-id="18636-127">Kirjoita arvo **Tuoteresepti**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="18636-127">In the **Product receipt** field, type a value.</span></span>
22. <span data-ttu-id="18636-128">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="18636-128">Select **OK**.</span></span>



[!INCLUDE[footer-include](../../includes/footer-banner.md)]