---
title: Konsernin sisäisen projektilaskutuksen määrittäminen
description: Tämä aihe osoittaa, miten projektilaskutus määritetään kahden yrityksen välille organisaatiossa.
author: Yowelle
ms.date: 07/29/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: VendTable, InterCompanyTradingRelationSetupVendor, SysDataAreaSelectLookup, ProjParameters, ProjPosting, ProjTransferPrice
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ad25aba492b7902ddd8955be87f88f96f6d4508f
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/10/2021
ms.locfileid: "6001197"
---
# <a name="configure-intercompany-project-invoicing"></a><span data-ttu-id="4c8c9-103">Konsernin sisäisen projektilaskutuksen määrittäminen</span><span class="sxs-lookup"><span data-stu-id="4c8c9-103">Configure intercompany project invoicing</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="4c8c9-104">Tämä aihe osoittaa, miten projektilaskutus määritetään kahden yrityksen välille organisaatiossa.</span><span class="sxs-lookup"><span data-stu-id="4c8c9-104">This topic shows how to set up project invoicing between two companies in your organization.</span></span> <span data-ttu-id="4c8c9-105">Tämä tehtävä käyttää USSI-tietojoukkoa.</span><span class="sxs-lookup"><span data-stu-id="4c8c9-105">This task uses the USSI data set.</span></span>

1. <span data-ttu-id="4c8c9-106">Siirry siirtymisruudussa kohtaan **Moduulit > Ostoreskontra > Toimittajat > Kaikki toimittajat**.</span><span class="sxs-lookup"><span data-stu-id="4c8c9-106">In the navigation pane, go to **Modules > Accounts payable > Vendors > All vendors**.</span></span>
2. <span data-ttu-id="4c8c9-107">Etsi ja valitse **Kaikki toimittajat** -luettelosta haluamasi tietue.</span><span class="sxs-lookup"><span data-stu-id="4c8c9-107">In the **All vendors** list, find and select the desired record.</span></span>
3. <span data-ttu-id="4c8c9-108">Valitse toimintoruudussa **Yleiset**.</span><span class="sxs-lookup"><span data-stu-id="4c8c9-108">On the Action Pane, select **General**.</span></span>
4. <span data-ttu-id="4c8c9-109">Valitse **Konsernin sisäinen**.</span><span class="sxs-lookup"><span data-stu-id="4c8c9-109">Select **Intercompany**.</span></span>
5. <span data-ttu-id="4c8c9-110">Määritä **Aktiivinen**-kohdan arvoksi **Kyllä**, jos haluat ottaa käyttöön konserniyritysten välisen kaupan.</span><span class="sxs-lookup"><span data-stu-id="4c8c9-110">Set **Active** to **Yes** to enable intercompany trading.</span></span>
6. <span data-ttu-id="4c8c9-111">Kirjoita tai valitse arvo **Asiakasyritys**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="4c8c9-111">In the **Customer company** field, enter or select a value.</span></span>
7. <span data-ttu-id="4c8c9-112">Kirjoita tai valitse arvo **Oma tili** -kenttään.</span><span class="sxs-lookup"><span data-stu-id="4c8c9-112">In the **My account** field, enter or select a value.</span></span>
8. <span data-ttu-id="4c8c9-113">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="4c8c9-113">Select **Save**.</span></span>
9. <span data-ttu-id="4c8c9-114">Sulje sivut palataksesi kotisivulle.</span><span class="sxs-lookup"><span data-stu-id="4c8c9-114">Close the pages to return to the home page.</span></span>
10. <span data-ttu-id="4c8c9-115">Valitse siirtymisruudussa **Moduulit > Projektinhallinta ja kirjanpito > Määritys > Projektinhallinnan ja kirjanpidon parametrit**.</span><span class="sxs-lookup"><span data-stu-id="4c8c9-115">In the navigation pane, go to **Modules > Project management and accounting > Setup > Project management and accounting parameters**.</span></span>
11. <span data-ttu-id="4c8c9-116">Valitse **Konsernin sisäinen** -välilehti.</span><span class="sxs-lookup"><span data-stu-id="4c8c9-116">Select the **Intercompany** tab.</span></span>
12. <span data-ttu-id="4c8c9-117">Jos haluat ottaa käyttöön konsernin sisäisten resurssien aikataulutuksen ja tuntilomakkeet, siirrä liukusäädin kohtaan **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="4c8c9-117">Move the slider to **Yes** to enable intercompany resource scheduling and timesheets.</span></span>
13. <span data-ttu-id="4c8c9-118">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="4c8c9-118">In the list, mark the selected row.</span></span>
14. <span data-ttu-id="4c8c9-119">Valitse **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="4c8c9-119">Select **New**.</span></span>
15. <span data-ttu-id="4c8c9-120">Kirjoita tai valitse arvo **Lainaava yritys** -kenttään.</span><span class="sxs-lookup"><span data-stu-id="4c8c9-120">In the **Borrowing legal entity** field, enter or select a value.</span></span>
16. <span data-ttu-id="4c8c9-121">Valitse **Jaksota tuotot** -valintaruutu.</span><span class="sxs-lookup"><span data-stu-id="4c8c9-121">Select the **Accrue revenue** check box.</span></span>
17. <span data-ttu-id="4c8c9-122">Kirjoita tai valitse arvo **Oletusaikaraporttiluokka**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="4c8c9-122">In the **Default timesheet category** field, enter or select a value.</span></span>
18. <span data-ttu-id="4c8c9-123">Kirjoita tai valitse arvo **Oletuskululuokka**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="4c8c9-123">In the **Default expense category** field, enter or select a value.</span></span>
19. <span data-ttu-id="4c8c9-124">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="4c8c9-124">Select **Save**.</span></span>
20. <span data-ttu-id="4c8c9-125">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="4c8c9-125">Close the page.</span></span>
21. <span data-ttu-id="4c8c9-126">Valitse siirtymisruudussa **Moduulit > Projektinhallinta ja kirjanpito > Määritys > Kirjaus > Kirjanpidon asetukset**.</span><span class="sxs-lookup"><span data-stu-id="4c8c9-126">In the navigation pane, go to **Modules > Project management and accounting > Setup > Posting > Ledger posting setup**.</span></span>
22. <span data-ttu-id="4c8c9-127">Valitse vaihtoehto **Kirjanpitotilityypit**-kentässä.</span><span class="sxs-lookup"><span data-stu-id="4c8c9-127">In the **Ledger account types** field, select an option.</span></span>
23. <span data-ttu-id="4c8c9-128">Valitse **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="4c8c9-128">Select **New**.</span></span>
24. <span data-ttu-id="4c8c9-129">Määritä uuden rivin **Päätili**-kentässä haluamasi arvot.</span><span class="sxs-lookup"><span data-stu-id="4c8c9-129">In the **Main account** field of the new row, specify the desired values.</span></span>
25. <span data-ttu-id="4c8c9-130">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="4c8c9-130">Select **Save**.</span></span>
26. <span data-ttu-id="4c8c9-131">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="4c8c9-131">Close the page.</span></span>
27. <span data-ttu-id="4c8c9-132">Valitse siirtymisruudussa **Moduulit > Projektinhallinta ja kirjanpito > Määritys > Hinnat > Siirtohinta**.</span><span class="sxs-lookup"><span data-stu-id="4c8c9-132">In the navigation pane, go to **Modules > Project management and accounting > Setup > Prices > Transfer price**.</span></span>
28. <span data-ttu-id="4c8c9-133">Valitse **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="4c8c9-133">Select **New**.</span></span>
29. <span data-ttu-id="4c8c9-134">Kirjoita päivämäärä **Voimaantulopäivä**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="4c8c9-134">In the **Effective date** field, enter a date.</span></span>
30. <span data-ttu-id="4c8c9-135">Kirjoita tai valitse arvo **Lainaava yritys** -kenttään.</span><span class="sxs-lookup"><span data-stu-id="4c8c9-135">In the **Borrowing legal entity** field, enter or select a value.</span></span>
31. <span data-ttu-id="4c8c9-136">Valitse **Siirtohintamalli**-kentässä vaihtoehto.</span><span class="sxs-lookup"><span data-stu-id="4c8c9-136">In the **Transfer price model** field, select an option.</span></span>
32. <span data-ttu-id="4c8c9-137">Kirjoita **Hinnoittelu**-kenttään numero.</span><span class="sxs-lookup"><span data-stu-id="4c8c9-137">In the **Pricing** field, enter a number.</span></span>
33. <span data-ttu-id="4c8c9-138">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="4c8c9-138">Select **Save**.</span></span>



[!INCLUDE[footer-include](../../includes/footer-banner.md)]