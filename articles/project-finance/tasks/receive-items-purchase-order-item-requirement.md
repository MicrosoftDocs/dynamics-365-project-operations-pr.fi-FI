---
title: Nimikkeiden vastaanotto nimiketarpeeseen perustuvan ostotilauksen perusteella
description: Tässä aiheessa kerrotaan, miten voidaan vastaanottaa nimikkeitä nimiketarpeeseen perustuvan ostotilauksen perusteella.
author: KimANelson
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
ms.assetid: c61e3a5e-da3d-4f4c-87fa-03dea19f6936
ms.author: knelson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c5ed287aa24aff647ef1dc625f9e9f5f086ee662
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/24/2020
ms.locfileid: "3751110"
---
# <a name="receive-items-on-purchase-order-from-item-requirement"></a><span data-ttu-id="71b23-103">Nimikkeiden vastaanotto nimiketarpeeseen perustuvan ostotilauksen perusteella</span><span class="sxs-lookup"><span data-stu-id="71b23-103">Receive items on purchase order from item requirement</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="71b23-104">Tässä aiheessa kerrotaan, miten voidaan vastaanottaa nimikkeitä nimiketarpeeseen perustuvan ostotilauksen perusteella.</span><span class="sxs-lookup"><span data-stu-id="71b23-104">This topic explains how to receive items on a purchase order from an item requirement.</span></span>

<span data-ttu-id="71b23-105">Kun käytät nimiketarvetta nimiketapahtuman sijaan, voit suunnitella toimituksen toteutettavaksi juuri ennen nimikkeen todellista käyttöä, luoda ostotilauksen, lisätä nimikkeen kauppasopimuskehykseen ja lisätä nimiketarpeen tuotannon suunnitteluun.</span><span class="sxs-lookup"><span data-stu-id="71b23-105">By using an item requirement instead of an item transaction, you can plan for delivery just before the item is actually used, create a purchase order, include the item in the trade-agreement framework, and include the item requirement in production planning.</span></span> 

<span data-ttu-id="71b23-106">Tämä tehtävä käyttää USSI-tietojoukkoa.</span><span class="sxs-lookup"><span data-stu-id="71b23-106">This task uses the USSI data set.</span></span>

1. <span data-ttu-id="71b23-107">Valitse siirtymisruudussa **Moduulit > Projektinhallinta ja kirjanpito > Projektit > Kaikki projektit**.</span><span class="sxs-lookup"><span data-stu-id="71b23-107">In the navigation pane, go to **Modules > Project management and accounting > Projects > All projects**.</span></span>
2. <span data-ttu-id="71b23-108">Valitse luettelossa halutun rivin linkki.</span><span class="sxs-lookup"><span data-stu-id="71b23-108">In the list, select the link in the desired row.</span></span>
3. <span data-ttu-id="71b23-109">Valitse toimintoruudussa **Suunnittelu**.</span><span class="sxs-lookup"><span data-stu-id="71b23-109">On the Action Pane, select **Plan**.</span></span>
4. <span data-ttu-id="71b23-110">Valitse **Nimiketarpeet**.</span><span class="sxs-lookup"><span data-stu-id="71b23-110">Select **Item requirements**.</span></span>
5. <span data-ttu-id="71b23-111">Valitse **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="71b23-111">Select **New**.</span></span>
6. <span data-ttu-id="71b23-112">Syötä riville arvo tai valitse siltä arvo **Nimikenumero**-kentässä.</span><span class="sxs-lookup"><span data-stu-id="71b23-112">In the new row, enter or select a value in the **Item number** field.</span></span>
7. <span data-ttu-id="71b23-113">Kirjoita **Määrä**-kenttään numero.</span><span class="sxs-lookup"><span data-stu-id="71b23-113">In the **Quantity** field, enter a number.</span></span>
8. <span data-ttu-id="71b23-114">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="71b23-114">Select **Save**.</span></span>
9. <span data-ttu-id="71b23-115">Valitse toimintoruudussa **Hallitse**.</span><span class="sxs-lookup"><span data-stu-id="71b23-115">On the Action Pane, select **Manage**.</span></span>
10. <span data-ttu-id="71b23-116">Valitse **Funktiot**.</span><span class="sxs-lookup"><span data-stu-id="71b23-116">Select **Functions**.</span></span>
11. <span data-ttu-id="71b23-117">Valitse **Luo uusi ostotilaus**.</span><span class="sxs-lookup"><span data-stu-id="71b23-117">Select **Create purchase order**.</span></span>
12. <span data-ttu-id="71b23-118">Valitse **Sisällytä kaikki** -valintaruutu.</span><span class="sxs-lookup"><span data-stu-id="71b23-118">Select the **Include all** check box.</span></span>
13. <span data-ttu-id="71b23-119">Kirjoita tai valitse arvo **Toimittajatili** -kenttään.</span><span class="sxs-lookup"><span data-stu-id="71b23-119">In the **Vendor account** field, enter or select a value.</span></span>
14. <span data-ttu-id="71b23-120">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="71b23-120">Select **OK**.</span></span>
15. <span data-ttu-id="71b23-121">Siirry siirtymisruudussa kohtaan **Moduulit > Ostoreskontra > Ostotilaukset > Kaikki ostotilaukset**.</span><span class="sxs-lookup"><span data-stu-id="71b23-121">In the navigation pane, go to **Modules > Accounts payable > Purchase orders > All purchase orders**.</span></span>
16. <span data-ttu-id="71b23-122">Valitse luettelossa halutun rivin linkki.</span><span class="sxs-lookup"><span data-stu-id="71b23-122">In the list, select the link in the desired row.</span></span>
17. <span data-ttu-id="71b23-123">Valitse toimintoruudussa **Osta**.</span><span class="sxs-lookup"><span data-stu-id="71b23-123">On the Action Pane, select **Purchase**.</span></span>
18. <span data-ttu-id="71b23-124">Valitse **Vahvista**.</span><span class="sxs-lookup"><span data-stu-id="71b23-124">Select **Confirm**.</span></span>
19. <span data-ttu-id="71b23-125">Valitse toimintoruudussa **Vastaanota**.</span><span class="sxs-lookup"><span data-stu-id="71b23-125">On the Action Pane, select **Receive**.</span></span>
20. <span data-ttu-id="71b23-126">Valitse **Tuoteresepti**.</span><span class="sxs-lookup"><span data-stu-id="71b23-126">Select **Product receipt**.</span></span>
21. <span data-ttu-id="71b23-127">Kirjoita arvo **Tuoteresepti**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="71b23-127">In the **Product receipt** field, type a value.</span></span>
22. <span data-ttu-id="71b23-128">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="71b23-128">Select **OK**.</span></span>

