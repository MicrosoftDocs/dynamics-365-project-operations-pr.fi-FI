---
title: Yksiköt ja yksikköryhmät
description: Tässä aiheessa on tietoja yksikköjen ja yksikköryhmien luomisesta Dynamics 365 Project Operationsissa.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
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
ms.openlocfilehash: 162366f4b7aa678b4e39d9745a657037bf36cbe0
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5277334"
---
# <a name="units-and-unit-groups"></a><span data-ttu-id="70f04-103">Yksiköt ja yksikköryhmät</span><span class="sxs-lookup"><span data-stu-id="70f04-103">Units and unit groups</span></span>

<span data-ttu-id="70f04-104">_**Koskee:** Project Operationsin resurssiin / muuhun kuin resurssiin perustuvia skenaarioita, Lite-käyttöönotto-kaupasta proformalaskutukseen_</span><span class="sxs-lookup"><span data-stu-id="70f04-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="70f04-105">Yksiköt ovat määriä tai mittayksiköitä, joissa tuotteita tai palveluja myydään.</span><span class="sxs-lookup"><span data-stu-id="70f04-105">Units are the quantities or measurements that you sell your products or services in.</span></span> <span data-ttu-id="70f04-106">Jos esimerkiksi myyt puutarhatarvikkeita, siemenien myyntiyksikkönä voi olla paketti, laatikko tai kuormalava.</span><span class="sxs-lookup"><span data-stu-id="70f04-106">For example, if you sell gardening supplies, you might sell seeds in units of packets, boxes, and pallets.</span></span> <span data-ttu-id="70f04-107">Yksikköryhmä on näiden yksiköiden kokoelma.</span><span class="sxs-lookup"><span data-stu-id="70f04-107">A unit group is a collection of these different units.</span></span>

<span data-ttu-id="70f04-108">Jos haluat viimeistellä tämän aiheen vaiheet, varmista, että sinulle on annettu järjestelmänvalvojan tai Sales Professionalin esimiehen rooli tai vastaavat käyttöoikeudet.</span><span class="sxs-lookup"><span data-stu-id="70f04-108">To complete the steps in this topic, make sure that you have been assigned to the System Administrator or Sales Professional Manager role or have equivalent permissions.</span></span>

## <a name="create-a-unit-group"></a><span data-ttu-id="70f04-109">Yksikköryhmän luominen</span><span class="sxs-lookup"><span data-stu-id="70f04-109">Create a unit group</span></span>

1. <span data-ttu-id="70f04-110">Valitse sivustokartassa **Yksiköt**.</span><span class="sxs-lookup"><span data-stu-id="70f04-110">In the site map, select **Units**.</span></span>
2. <span data-ttu-id="70f04-111">Valitse **Uusi** ja syötä **Luo yksikköryhmä** -valintaikkunaan yksikön nimi.</span><span class="sxs-lookup"><span data-stu-id="70f04-111">Select **New**, and in the **Create Unit Group** dialog box, enter the unit name.</span></span>
3. <span data-ttu-id="70f04-112">Anna **Ensisijainen yksikkö** -kenttään pienin yhteinen mittayksikkö, jossa tuotetta myydään.</span><span class="sxs-lookup"><span data-stu-id="70f04-112">In the **Primary unit** field, enter the lowest common unit of measure that the product will be sold in.</span></span> <span data-ttu-id="70f04-113">Voit esimerkiksi syöttää arvon Kappale tai Unssi.</span><span class="sxs-lookup"><span data-stu-id="70f04-113">For example, you might enter "piece" or "ounce".</span></span>
4. <span data-ttu-id="70f04-114">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="70f04-114">Select **OK**.</span></span>

## <a name="add-units-to-a-unit-group"></a><span data-ttu-id="70f04-115">Yksiköiden lisääminen yksikköryhmään</span><span class="sxs-lookup"><span data-stu-id="70f04-115">Add units to a unit group</span></span>

1. <span data-ttu-id="70f04-116">Avaa yksikköryhmä ja valitse **Liittyvät**-välilehdessä **Yksiköt**.</span><span class="sxs-lookup"><span data-stu-id="70f04-116">Open a unit group, and on the **Related** tab, select **Units**.</span></span> <span data-ttu-id="70f04-117">Ensisijainen yksikkö näkyy jo lisättynä.</span><span class="sxs-lookup"><span data-stu-id="70f04-117">You will see that the primary unit is already added.</span></span>
2. <span data-ttu-id="70f04-118">Valitse **Lisää uusi yksikkö** ja syötä **Pikaluonti: Yksikkö** -sivun **Nimi**-kenttään yksikön nimi.</span><span class="sxs-lookup"><span data-stu-id="70f04-118">Select **Add New Unit**, and on the **Quick Create: Unit** page, in the **Name** field, enter the nanem of the unit.</span></span>
3. <span data-ttu-id="70f04-119">Syötä **Määrä**-kenttään yksikön sisältämä määrä.</span><span class="sxs-lookup"><span data-stu-id="70f04-119">In the **QUantity** field, enter the quantity that the unit will contain.</span></span> <span data-ttu-id="70f04-120">Jos laatikossa on esimerkiksi kaksi kappaletta, syötä 2.</span><span class="sxs-lookup"><span data-stu-id="70f04-120">For example, if a box contains two pieces, enter "2".</span></span> 
4. <span data-ttu-id="70f04-121">Valitse **Perusyksikkö**-kentässä perusyksikkö, joka määrittää yksikön pienimmän mittayksikön.</span><span class="sxs-lookup"><span data-stu-id="70f04-121">In the **Base unit** field, select a base unit to establish the lowest unit of measurement for the unit.</span></span> <span data-ttu-id="70f04-122">Voit valita esimerkiksi Kappale.</span><span class="sxs-lookup"><span data-stu-id="70f04-122">For example, you might select "Piece".</span></span>
5. <span data-ttu-id="70f04-123">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="70f04-123">Select **Save**:</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]