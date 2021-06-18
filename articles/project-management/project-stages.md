---
title: Projektin vaiheet
description: Tässä aiheessa on tietoja Microsoft Dynamics Project Operationsin projektivaiheista.
author: ruhercul
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 079c3d2d16cf802d2b9ecc779577e6e390d92ddc
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/10/2021
ms.locfileid: "5996922"
---
# <a name="project-stages"></a><span data-ttu-id="79d46-103">Projektin vaiheet</span><span class="sxs-lookup"><span data-stu-id="79d46-103">Project stages</span></span>

<span data-ttu-id="79d46-104">_**Koskee:** Project Operationsin resurssiin / muuhun kuin resurssiin perustuvia skenaarioita, Lite-käyttöönotto-kaupasta proformalaskutukseen_</span><span class="sxs-lookup"><span data-stu-id="79d46-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="79d46-105">Projektin vaiheet suunnitellaan vastaamaan projektin tilaa sen edetessä.</span><span class="sxs-lookup"><span data-stu-id="79d46-105">Project stages are designed to reflect the state of the project as it progresses.</span></span> <span data-ttu-id="79d46-106">Mukautusten avulla vaiheet voidaan päivittää automaattisesti käyttämällä liiketoimintaprosesseja, Power Automatea tai laajennuksia.</span><span class="sxs-lookup"><span data-stu-id="79d46-106">Customizations can be used to automatically update the stages with business process flows, Power Automate, or plug-in extensions.</span></span>

<span data-ttu-id="79d46-107">Seuraavat vaiheet määritetään oletusliiketoimintaprosessissa:</span><span class="sxs-lookup"><span data-stu-id="79d46-107">The following stages are defined in the default business process flow:</span></span>

- <span data-ttu-id="79d46-108">Uusi</span><span class="sxs-lookup"><span data-stu-id="79d46-108">New</span></span>
- <span data-ttu-id="79d46-109">Tarjous</span><span class="sxs-lookup"><span data-stu-id="79d46-109">Quote</span></span>
- <span data-ttu-id="79d46-110">Palvelupaketti</span><span class="sxs-lookup"><span data-stu-id="79d46-110">Plan</span></span>
- <span data-ttu-id="79d46-111">Toimita</span><span class="sxs-lookup"><span data-stu-id="79d46-111">Deliver</span></span>
- <span data-ttu-id="79d46-112">Täydellinen</span><span class="sxs-lookup"><span data-stu-id="79d46-112">Complete</span></span>
- <span data-ttu-id="79d46-113">Sulje</span><span class="sxs-lookup"><span data-stu-id="79d46-113">Close</span></span> 

## <a name="new"></a><span data-ttu-id="79d46-114">Uusi</span><span class="sxs-lookup"><span data-stu-id="79d46-114">New</span></span>

<span data-ttu-id="79d46-115">Kun luot projektin, projektin vaiheeksi on määritetty **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="79d46-115">When you create a project, the project stage is set to **New**.</span></span> <span data-ttu-id="79d46-116">Jos projekti on luotu mallista, siinä voi olla aikataulu, arvio ja ryhmän tiedot.</span><span class="sxs-lookup"><span data-stu-id="79d46-116">If the project was created from a template, it might have schedule, estimate, and team data.</span></span> <span data-ttu-id="79d46-117">Muussa tapauksessa se on luonnos projektista, ja muut osat on syötettävä.</span><span class="sxs-lookup"><span data-stu-id="79d46-117">Otherwise, it's an outline of the project, and the remaining components must be entered.</span></span>

## <a name="quote"></a><span data-ttu-id="79d46-118">Tarjous</span><span class="sxs-lookup"><span data-stu-id="79d46-118">Quote</span></span>

<span data-ttu-id="79d46-119">Kun liität projektin tarjoukseen tai luot sen tarjouksesta, projektivaiheeksi on määritetty **Tarjous**, ja arvioidut aloitus- ja päättymispäivät päivitetään myös.</span><span class="sxs-lookup"><span data-stu-id="79d46-119">When you associate a project with a quote, or when you create a project from a quote, the project stage is set to **Quote**, and the estimated start and end dates are updated.</span></span> <span data-ttu-id="79d46-120">Kun projekti on **Tarjous**-vaiheessa, **Myynti**-välilehti **Projektikohde**-sivulla näyttää tarjouksen tiedot.</span><span class="sxs-lookup"><span data-stu-id="79d46-120">While the project is in the **Quote** stage, the **Sales** tab on the **Project Entity** page shows details of the quote.</span></span>

## <a name="plan"></a><span data-ttu-id="79d46-121">Suunnittelu</span><span class="sxs-lookup"><span data-stu-id="79d46-121">Plan</span></span>

<span data-ttu-id="79d46-122">Kun projektiin liittyvä tarjous voittaa ja valmistelu etenee **Sopimus**-vaiheeseen, päivitetään projektin vaiheeksi **Suunnittelu**.</span><span class="sxs-lookup"><span data-stu-id="79d46-122">When you win a quote that is associated with a project, and the project is moved to the **Contract** phase, the project stage is updated to **Plan**.</span></span> <span data-ttu-id="79d46-123">Kun projekti on **Suunnittelu**-vaiheessa, **Projektikohde**-sivulla näytetään sopimuksen tiedot.</span><span class="sxs-lookup"><span data-stu-id="79d46-123">While the project is in the **Plan** stage, the **Project Entity** page shows details of the contract.</span></span>

## <a name="deliver"></a><span data-ttu-id="79d46-124">Toimitus</span><span class="sxs-lookup"><span data-stu-id="79d46-124">Deliver</span></span>

<span data-ttu-id="79d46-125">Kun projektisuunnitelma valmistuu ja olet valmis aloittamaan projektin, projektipäällikön on päivitettävä projekti vaihe **Toimitettavaksi** osoittamaan, että projekti on käynnistynyt.</span><span class="sxs-lookup"><span data-stu-id="79d46-125">When the project plan is completed, and you're ready to start the project, the project manager should update the project stage to **Deliver** to show that the project has started.</span></span>

## <a name="complete"></a><span data-ttu-id="79d46-126">Valmistuminen</span><span class="sxs-lookup"><span data-stu-id="79d46-126">Complete</span></span> 

<span data-ttu-id="79d46-127">Kun projektin työ on valmis, projektipäällikkö voi päivittää vaiheen **valmistuneeksi**.</span><span class="sxs-lookup"><span data-stu-id="79d46-127">When the work for the project is completed, the project manager can update the stage to **Complete**.</span></span> <span data-ttu-id="79d46-128">Kun projektipäällikkö päivittää projektin vaiheen **valmiiksi**, se osoittaa, että työ on 100 prosenttisesti valmiina, mutta että projekti on avoinna niin, että odottavat aika- tai kulukirjaukset voidaan kirjata.</span><span class="sxs-lookup"><span data-stu-id="79d46-128">By updating the project stage to **Complete**, the project manager indicates that the work is 100-percent completed, but that the project is being kept open so that any pending time or expense entries can be recorded.</span></span>

## <a name="close"></a><span data-ttu-id="79d46-129">Sulje</span><span class="sxs-lookup"><span data-stu-id="79d46-129">Close</span></span>

<span data-ttu-id="79d46-130">Kun kaikki tapahtumat on kirjattu projektille, projektipäällikkö voi päivittää vaiheen **suljetuksi**.</span><span class="sxs-lookup"><span data-stu-id="79d46-130">When all transactions are recorded for the project, the project manager can update the stage to **Close**.</span></span> <span data-ttu-id="79d46-131">Tässä vaiheessa tapahtumia ei voi tallentaa, ja projekti on määritetty vain luku -tilaan.</span><span class="sxs-lookup"><span data-stu-id="79d46-131">At that point, no transactions can be recorded, and the project is set to read-only.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]