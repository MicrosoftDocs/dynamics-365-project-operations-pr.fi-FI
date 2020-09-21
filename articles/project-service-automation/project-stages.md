---
title: Projektin vaiheet
description: Tässä aiheessa on tietoja projektin vaiheista.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: 983c25a0-ed21-4151-a109-b385a88285fa
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 70aa057e127df7ba925e84f5d056a06a4cc8833e
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/24/2020
ms.locfileid: "3751149"
---
# <a name="project-stages"></a><span data-ttu-id="42019-103">Projektin vaiheet</span><span class="sxs-lookup"><span data-stu-id="42019-103">Project stages</span></span> 

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="42019-104">Project-vaiheet päivitetään vastaamaan projektin tilaa sen edetessä.</span><span class="sxs-lookup"><span data-stu-id="42019-104">Project stages are updated to reflect the state of the project as it progresses.</span></span> <span data-ttu-id="42019-105">Oletusarvoinen liiketoimintaprosessi päivittää automaattisesti joitakin projektin vaiheista, kun taas toiset projektipäällikkö päivittää manuaalisesti.</span><span class="sxs-lookup"><span data-stu-id="42019-105">The default business process flow automatically updates some stages of the project while others are manually updated by the project manager.</span></span> 

<span data-ttu-id="42019-106">Seuraavat vaiheet määritetään oletusarvoisessa BPF:ssä:</span><span class="sxs-lookup"><span data-stu-id="42019-106">The following stages are defined in the default BPF:</span></span>

- <span data-ttu-id="42019-107">Uusi</span><span class="sxs-lookup"><span data-stu-id="42019-107">New</span></span>
- <span data-ttu-id="42019-108">Tarjous</span><span class="sxs-lookup"><span data-stu-id="42019-108">Quote</span></span>
- <span data-ttu-id="42019-109">Suunnittelu</span><span class="sxs-lookup"><span data-stu-id="42019-109">Plan</span></span>
- <span data-ttu-id="42019-110">Toimitus</span><span class="sxs-lookup"><span data-stu-id="42019-110">Deliver</span></span>
- <span data-ttu-id="42019-111">Valmistuminen</span><span class="sxs-lookup"><span data-stu-id="42019-111">Complete</span></span>
- <span data-ttu-id="42019-112">Sulje</span><span class="sxs-lookup"><span data-stu-id="42019-112">Close</span></span> 

## <a name="new"></a><span data-ttu-id="42019-113">Uusi</span><span class="sxs-lookup"><span data-stu-id="42019-113">New</span></span>

<span data-ttu-id="42019-114">Kun luot projektin, projektin vaiheeksi on määritetty **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="42019-114">When you create a project, the project stage is set to **New**.</span></span> <span data-ttu-id="42019-115">Jos projekti on luotu mallista, siinä voi olla aikataulu, arvio ja ryhmän tiedot.</span><span class="sxs-lookup"><span data-stu-id="42019-115">If the project was created from a template, it might have schedule, estimate, and team data.</span></span> <span data-ttu-id="42019-116">Muussa tapauksessa se on vain luonnos projektista, ja muut osat on syötettävä.</span><span class="sxs-lookup"><span data-stu-id="42019-116">Otherwise, it's just an outline of the project, and the remaining components must be entered.</span></span>

## <a name="quote"></a><span data-ttu-id="42019-117">Tarjous</span><span class="sxs-lookup"><span data-stu-id="42019-117">Quote</span></span>

<span data-ttu-id="42019-118">Kun liität projektin tarjoukseen tai luot sen tarjouksesta, projektivaiheeksi on määritetty **Tarjous**, ja arvioidut aloitus- ja päättymispäivät päivitetään myös.</span><span class="sxs-lookup"><span data-stu-id="42019-118">When you associate a project with a quote, or when you create a project from a quote, the project stage is set to **Quote**, and the estimated start and end dates are updated.</span></span> <span data-ttu-id="42019-119">Kun projekti on **Tarjous**-vaiheessa, **Myynti**-välilehti **Projektikohde**-sivulla näyttää tarjouksen tiedot.</span><span class="sxs-lookup"><span data-stu-id="42019-119">While the project is in the **Quote** stage, the **Sales** tab on the **Project Entity** page shows details of the quote.</span></span>

## <a name="plan"></a><span data-ttu-id="42019-120">Suunnittelu</span><span class="sxs-lookup"><span data-stu-id="42019-120">Plan</span></span>

<span data-ttu-id="42019-121">Kun projektiin liittyvä tarjous voittaa ja valmistelu etenee **Sopimus**-vaiheeseen, päivitetään projektin vaiheeksi **Suunnittelu**.</span><span class="sxs-lookup"><span data-stu-id="42019-121">When you win a quote that is associated with a project, and the project is moved to the **Contract** phase, the project stage is updated to **Plan**.</span></span> <span data-ttu-id="42019-122">Kun projekti on **Suunnittelu**-vaiheessa, **Projektikohde**-sivulla näytetään sopimuksen tiedot.</span><span class="sxs-lookup"><span data-stu-id="42019-122">While the project is in the **Plan** stage, the **Project Entity** page shows details of the contract.</span></span>

## <a name="deliver"></a><span data-ttu-id="42019-123">Toimitus</span><span class="sxs-lookup"><span data-stu-id="42019-123">Deliver</span></span>

<span data-ttu-id="42019-124">Kun projektisuunnitelma valmistuu ja olet valmis aloittamaan projektin, projektipäällikön on päivitettävä projekti vaihe **Toimitettavaksi** osoittamaan, että projekti on käynnistynyt.</span><span class="sxs-lookup"><span data-stu-id="42019-124">When the project plan is completed, and you're ready to start the project, the project manager should update the project stage to **Deliver** to show that the project has started.</span></span>

## <a name="complete"></a><span data-ttu-id="42019-125">Valmistuminen</span><span class="sxs-lookup"><span data-stu-id="42019-125">Complete</span></span> 

<span data-ttu-id="42019-126">Kun projektin työ on valmis, projektipäällikkö voi päivittää vaiheen **valmistuneeksi**.</span><span class="sxs-lookup"><span data-stu-id="42019-126">When the work for the project is completed, the project manager can update the stage to **Complete**.</span></span> <span data-ttu-id="42019-127">Kun projektipäällikkö päivittää projektin vaiheen **valmiiksi**, se osoittaa, että työ on 100 prosenttisesti valmiina, mutta että projekti on avoinna niin, että odottavat aika- tai kulukirjaukset voidaan kirjata.</span><span class="sxs-lookup"><span data-stu-id="42019-127">By updating the project stage to **Complete**, the project manager indicates that the work is 100-percent completed, but that the project is being kept open so that any pending time or expense entries can be recorded.</span></span>

## <a name="close"></a><span data-ttu-id="42019-128">Sulje</span><span class="sxs-lookup"><span data-stu-id="42019-128">Close</span></span>

<span data-ttu-id="42019-129">Kun kaikki tapahtumat on kirjattu projektille, projektipäällikkö voi päivittää vaiheen **suljetuksi**.</span><span class="sxs-lookup"><span data-stu-id="42019-129">When all transactions are recorded for the project, the project manager can update the stage to **Close**.</span></span> <span data-ttu-id="42019-130">Tässä vaiheessa tapahtumia ei voi tallentaa, ja projekti on määritetty vain luku -tilaan.</span><span class="sxs-lookup"><span data-stu-id="42019-130">At that point, no transactions can be recorded, and the project is set to read-only.</span></span>
