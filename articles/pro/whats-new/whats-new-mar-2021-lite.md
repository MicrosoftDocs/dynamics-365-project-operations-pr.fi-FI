---
title: Maaliskuun 2021 Project Operations Lite -käyttöönoton uudet ominaisuudet
description: Tässä aiheessa on tietoja Project Operations Lite -käyttöönoton maaliskuun 2021 version päivityksessä olevista laatupäivityksistä.
author: sigitac
manager: tfehr
ms.date: 03/03/2021
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: bd1518ef8f5645bace63a222b92cfd16d9c19a21
ms.sourcegitcommit: f78087174a8512199a1bcbd7e8610bbc80e64801
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/04/2021
ms.locfileid: "5499994"
---
# <a name="whats-new-march-2021---project-operations-lite-deployment"></a><span data-ttu-id="fd655-103">Maaliskuun 2021 Project Operations Lite -käyttöönoton uudet ominaisuudet</span><span class="sxs-lookup"><span data-stu-id="fd655-103">What's new March 2021 - Project Operations lite deployment</span></span>

<span data-ttu-id="fd655-104">_Käytetään: Lite-käyttöönotto – kauppa proformalaskutukseen_</span><span class="sxs-lookup"><span data-stu-id="fd655-104">_Applies To: Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="fd655-105">Tämä aihe koskee seuraavia Dynamics 365 Project Operationsin komponentteja ja versioita:</span><span class="sxs-lookup"><span data-stu-id="fd655-105">This topic applies to the following Dynamics 365 Project Operations components and versions:</span></span>

- <span data-ttu-id="fd655-106">Project Operations Dataverse-ympäristön versiossa 4.8.0.91</span><span class="sxs-lookup"><span data-stu-id="fd655-106">Project Operations on Dataverse environment version 4.8.0.91</span></span> 

## <a name="quality-updates"></a><span data-ttu-id="fd655-107">Laatupäivitykset</span><span class="sxs-lookup"><span data-stu-id="fd655-107">Quality updates</span></span>

| <span data-ttu-id="fd655-108">**Ominaisuusalue**</span><span class="sxs-lookup"><span data-stu-id="fd655-108">**Feature area**</span></span> | <span data-ttu-id="fd655-109">**Viitenumero**</span><span class="sxs-lookup"><span data-stu-id="fd655-109">**Reference number**</span></span> | <span data-ttu-id="fd655-110">**Laatupäivitys**</span><span class="sxs-lookup"><span data-stu-id="fd655-110">**Quality update**</span></span> |
| --- | --- | --- |
| <span data-ttu-id="fd655-111">Laskutus ja hinnoittelu</span><span class="sxs-lookup"><span data-stu-id="fd655-111">Billing and pricing</span></span> | <span data-ttu-id="fd655-112">2133873</span><span class="sxs-lookup"><span data-stu-id="fd655-112">2133873</span></span> | <span data-ttu-id="fd655-113">Korjattiin **Yksikön myyntihinnan** valuuttasymbolin näkymä **Kuluarviot**-ruudukossa.</span><span class="sxs-lookup"><span data-stu-id="fd655-113">Fixed the display of **Unit Sales Price** currency symbol in the **Expense Estimates** grid.</span></span> |
| <span data-ttu-id="fd655-114">Laskutus ja hinnoittelu</span><span class="sxs-lookup"><span data-stu-id="fd655-114">Billing and pricing</span></span> | <span data-ttu-id="fd655-115">2174616</span><span class="sxs-lookup"><span data-stu-id="fd655-115">2174616</span></span> | <span data-ttu-id="fd655-116">Kun tarjous voitetaan, sopimuksen mukautettuun hinnastoon viitataan sopimusrivin tiedoissa, jotka kopioidaan tarjouksesta.</span><span class="sxs-lookup"><span data-stu-id="fd655-116">When a quote is won, the contract custom pricelist is referenced on contract line details that are copied from the quote.</span></span> |
| <span data-ttu-id="fd655-117">Mahdollisuuksien hallinta</span><span class="sxs-lookup"><span data-stu-id="fd655-117">Opportunity Management</span></span> | <span data-ttu-id="fd655-118">2167475</span><span class="sxs-lookup"><span data-stu-id="fd655-118">2167475</span></span> | <span data-ttu-id="fd655-119">Korjauslaskun kiinteä verosumma, josta laskuttamaton todellinen tapahtuma on peräisin.</span><span class="sxs-lookup"><span data-stu-id="fd655-119">Fixed tax amount in the correction invoice that originated an unbilled actual entry.</span></span> |
| <span data-ttu-id="fd655-120">Mahdollisuuksien hallinta</span><span class="sxs-lookup"><span data-stu-id="fd655-120">Opportunity Management</span></span> | <span data-ttu-id="fd655-121">2176285</span><span class="sxs-lookup"><span data-stu-id="fd655-121">2176285</span></span> | <span data-ttu-id="fd655-122">Verosummaa ei saa kopioida myyntisopimuksen/tarjousrivin tiedoista kustannuksen sopimuksen/tarjouksen rivin tietoihin.</span><span class="sxs-lookup"><span data-stu-id="fd655-122">Tax amount must not be copied from sales contract/quote line details to cost contract/quote line details.</span></span> |
| <span data-ttu-id="fd655-123">Mahdollisuuksien hallinta</span><span class="sxs-lookup"><span data-stu-id="fd655-123">Opportunity Management</span></span> | <span data-ttu-id="fd655-124">2188079</span><span class="sxs-lookup"><span data-stu-id="fd655-124">2188079</span></span> | <span data-ttu-id="fd655-125">Jaettua laskutussääntöä ei saa luoda sopimuksille, jotka eivät perustu työhön.</span><span class="sxs-lookup"><span data-stu-id="fd655-125">Split billing rule must not be created for contracts that are not work-based.</span></span> |
| <span data-ttu-id="fd655-126">Suunnittelu ja seuranta</span><span class="sxs-lookup"><span data-stu-id="fd655-126">Planning and Tracking</span></span> | <span data-ttu-id="fd655-127">2138853</span><span class="sxs-lookup"><span data-stu-id="fd655-127">2138853</span></span> | <span data-ttu-id="fd655-128">Projektin kopiointitoiminto päivitettiin. Tämä varmistaa, että tehtäviin viittaavat kuluarviorivit kopioidaan kohdeprojektiin.</span><span class="sxs-lookup"><span data-stu-id="fd655-128">Project copy function updated to ensure expense estimate lines that reference tasks are copied to the destination project.</span></span> |
| <span data-ttu-id="fd655-129">Suunnittelu ja seuranta</span><span class="sxs-lookup"><span data-stu-id="fd655-129">Planning and Tracking</span></span> | <span data-ttu-id="fd655-130">2173259</span><span class="sxs-lookup"><span data-stu-id="fd655-130">2173259</span></span> | <span data-ttu-id="fd655-131">Kopioi projekti -toiminto päivitettiin. Näin varmistetaan, että se ei näytä **Kopioidaan työrakennetta** -virhesanomaa tietyissä skenaarioissa.</span><span class="sxs-lookup"><span data-stu-id="fd655-131">Project copy function updated to ensure it doesn't display the **Copying WBS** error message in certain scenarios.</span></span> |
| <span data-ttu-id="fd655-132">Aika ja kulu</span><span class="sxs-lookup"><span data-stu-id="fd655-132">Time and Expense</span></span> | <span data-ttu-id="fd655-133">2148910</span><span class="sxs-lookup"><span data-stu-id="fd655-133">2148910</span></span> | <span data-ttu-id="fd655-134">Korjattiin näyttöongelma, jossa **Muokkaa merkintää** -sivu näkyi **Aikamerkintä**-ruudukossa.</span><span class="sxs-lookup"><span data-stu-id="fd655-134">Fixed display issue with the **Edit Entry** page in the **Time Entry** grid.</span></span> |
| <span data-ttu-id="fd655-135">Aika ja kulu</span><span class="sxs-lookup"><span data-stu-id="fd655-135">Time and Expense</span></span> | <span data-ttu-id="fd655-136">2159798</span><span class="sxs-lookup"><span data-stu-id="fd655-136">2159798</span></span> | <span data-ttu-id="fd655-137">Ohjausobjekteja on tarkennettu, jotta varmistettaisiin, että hyväksyttyjä kulumerkintöjä ei voi muokata.</span><span class="sxs-lookup"><span data-stu-id="fd655-137">Tightened controls to ensure approved expense entries can't be edited.</span></span> |


