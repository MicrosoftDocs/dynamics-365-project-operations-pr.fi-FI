---
title: Projektin ostotilaukset
description: Tässä artikkelissa on kuvattu eri menetelmiä, joiden avulla voit luoda projektille ostotilauksia. Käytettävä menetelmä riippuu ostotilauksen tarkoituksesta sekä siitä, milloin ostetut nimikkeet käytetään ja veloitetaan projektilta.
author: Yowelle
manager: AnnBe
ms.date: 09/14/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 83972
ms.assetid: 247e4d72-610b-4fa5-9873-601ed0f4b2d6
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: bd891aec5bcab66c5801a5d9ca8abbbf632d662d
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/16/2020
ms.locfileid: "4075336"
---
# <a name="purchase-orders-for-a-project"></a><span data-ttu-id="9812b-104">Projektin ostotilaukset</span><span class="sxs-lookup"><span data-stu-id="9812b-104">Purchase orders for a project</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9812b-105">Tässä artikkelissa on kuvattu eri menetelmiä, joiden avulla voit luoda projektille ostotilauksia.</span><span class="sxs-lookup"><span data-stu-id="9812b-105">This article describes the various methods that you can use to create purchase orders for a project.</span></span> <span data-ttu-id="9812b-106">Käytettävä menetelmä riippuu ostotilauksen tarkoituksesta sekä siitä, milloin ostetut nimikkeet käytetään ja veloitetaan projektilta.</span><span class="sxs-lookup"><span data-stu-id="9812b-106">The method that you use depends on the purpose of the purchase order, and when the purchased items are consumed and charged to a project.</span></span>

### <a name="methods-for-creating-a-purchase-order"></a><span data-ttu-id="9812b-107">Ostotilausten luontitavat</span><span class="sxs-lookup"><span data-stu-id="9812b-107">Methods for creating a purchase order</span></span>

<span data-ttu-id="9812b-108">Voit luoda ostotilauksen projektinhallinnassa ja kirjanpidossa jollakin seuraavista menetelmistä.</span><span class="sxs-lookup"><span data-stu-id="9812b-108">You can use one of the following methods to create a purchase order in Project management and accounting.</span></span> <span data-ttu-id="9812b-109">Ostotilauksen tarkoitus määrittää, milloin ostotilaus kulutetaan, ja näin ollen, kun nimikkeitä laskutetaan projektilta.</span><span class="sxs-lookup"><span data-stu-id="9812b-109">The purpose of the purchase order determines when the purchase order is consumed and, therefore, when items are charged to a project.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="9812b-110">Tapa</span><span class="sxs-lookup"><span data-stu-id="9812b-110">Method</span></span></th>
<th><span data-ttu-id="9812b-111">Tarkoitus</span><span class="sxs-lookup"><span data-stu-id="9812b-111">Purpose</span></span></th>
<th><span data-ttu-id="9812b-112">Nimikkeiden kulutus</span><span class="sxs-lookup"><span data-stu-id="9812b-112">Consumption of items</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9812b-113">Uuden ostotilauksen luominen suoraan projektista.</span><span class="sxs-lookup"><span data-stu-id="9812b-113">Create a purchase order directly from a project.</span></span></td>
<td><span data-ttu-id="9812b-114">Käytä tätä menetelmää nimikkeiden ostamiseen ulkoiselta toimittajalta projektin kulutusta varten.</span><span class="sxs-lookup"><span data-stu-id="9812b-114">Use this method to purchase items from an external vendor for consumption on a project.</span></span> <span data-ttu-id="9812b-115">Voit luoda ostotilauksen kahdella tavalla:</span><span class="sxs-lookup"><span data-stu-id="9812b-115">You can create the purchase order in two ways:</span></span>
<ul>
<li><span data-ttu-id="9812b-116">Projektista itsestään.</span><span class="sxs-lookup"><span data-stu-id="9812b-116">From the project itself.</span></span> <span data-ttu-id="9812b-117">Tällöin projekti on jo määritetty ostotilaukselle.</span><span class="sxs-lookup"><span data-stu-id="9812b-117">In this case, the project is already defined for the purchase order.</span></span></li>
<li><span data-ttu-id="9812b-118">Siirtymällä projektin ostotilaukseen.</span><span class="sxs-lookup"><span data-stu-id="9812b-118">By navigating to the project purchase order.</span></span> <span data-ttu-id="9812b-119">Sinun täytyy valita sekä toimittaja että projekti, jolle ostotilaus luodaan.</span><span class="sxs-lookup"><span data-stu-id="9812b-119">You must select both the vendor and the project to create the purchase order for.</span></span></li>
</ul></td>
<td><span data-ttu-id="9812b-120">Nimikkeet kulutetaan, kun toimittajan lasku päivitetään.</span><span class="sxs-lookup"><span data-stu-id="9812b-120">Items are consumed when the vendor invoice is updated.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9812b-121">Ostotilauksen luominen myyntitilauksesta.</span><span class="sxs-lookup"><span data-stu-id="9812b-121">Create a purchase order from a sales order.</span></span></td>
<td><span data-ttu-id="9812b-122">käytä tätä menetelmää nimikkeiden ostamiseen, kun luot myyntitilauksen projektista.</span><span class="sxs-lookup"><span data-stu-id="9812b-122">Use this method to purchase items when you create a sales order from a project.</span></span></td>
<td><span data-ttu-id="9812b-123">Nimikkeet kulutetaan, kun myyntitilaus laskutetaan asiakkaalta.</span><span class="sxs-lookup"><span data-stu-id="9812b-123">Items are consumed when the sales order is invoiced to the customer.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9812b-124">Ostotilauksen luominen nimiketarpeesta.</span><span class="sxs-lookup"><span data-stu-id="9812b-124">Create a purchase order from an item requirement.</span></span></td>
<td><span data-ttu-id="9812b-125">käytä tätä menetelmää nimikkeiden ostamiseen, kun nimiketarpeen projektista.</span><span class="sxs-lookup"><span data-stu-id="9812b-125">Use this method to purchase items when you create an item requirement from a project.</span></span></td>
<td><span data-ttu-id="9812b-126">Nimikkeet kulutetaan, kun nimiketarpeen pakkausluettelo päivitetään.</span><span class="sxs-lookup"><span data-stu-id="9812b-126">Items are consumed when the item requirement packing slip is updated.</span></span></td>
</tr>
</tbody>
</table>

> [!NOTE] 
> <span data-ttu-id="9812b-127">Kun päivität toimittajan laskun tai pakkausluettelon, järjestelmä pyytää päivittämään nimiketarpeen pakkausluettelon.</span><span class="sxs-lookup"><span data-stu-id="9812b-127">When you update the vendor invoice or packing slip, you're prompted to update the packing slip on the item requirement.</span></span>

<span data-ttu-id="9812b-128">Lisätietoja: [Nimikkeiden vastaanotto nimiketarpeeseen perustuvan ostotilauksen perusteella](tasks/receive-items-purchase-order-item-requirement.md).</span><span class="sxs-lookup"><span data-stu-id="9812b-128">For more information, see [Receive items on purchase order from item requirement](tasks/receive-items-purchase-order-item-requirement.md).</span></span>
