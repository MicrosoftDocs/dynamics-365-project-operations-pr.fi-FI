---
title: Projektin vaihetyypit
description: Tässä aiheessa on tietoja projektin vaiheista.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 06/19/2020
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 3503b17e54fc0b321582c30ce534e4cb3f497a5f
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5283679"
---
# <a name="project-stage-types"></a><span data-ttu-id="08a1f-103">Projektin vaihetyypit</span><span class="sxs-lookup"><span data-stu-id="08a1f-103">Project stage types</span></span> 

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="08a1f-104">Projektin vaiheet suunnitellaan vastaamaan projektin tilaa sen edetessä.</span><span class="sxs-lookup"><span data-stu-id="08a1f-104">Project stages are designed to reflect the state of the project as it progresses.</span></span> <span data-ttu-id="08a1f-105">Mukautusten avulla vaiheet voidaan päivittää automaattisesti käyttämällä liiketoimintaprosesseja, Power Automatea tai laajennuksia.</span><span class="sxs-lookup"><span data-stu-id="08a1f-105">Customizations can be used to automatically update the stages with business process flows, Power Automate, or plug-in extensions.</span></span>

<span data-ttu-id="08a1f-106">Seuraavat vaiheet määritetään oletusarvoisessa BPF:ssä:</span><span class="sxs-lookup"><span data-stu-id="08a1f-106">The following stages are defined in the default BPF:</span></span>

- <span data-ttu-id="08a1f-107">Uusi</span><span class="sxs-lookup"><span data-stu-id="08a1f-107">New</span></span>
- <span data-ttu-id="08a1f-108">Tarjous</span><span class="sxs-lookup"><span data-stu-id="08a1f-108">Quote</span></span>
- <span data-ttu-id="08a1f-109">Suunnittelu</span><span class="sxs-lookup"><span data-stu-id="08a1f-109">Plan</span></span>
- <span data-ttu-id="08a1f-110">Toimitus</span><span class="sxs-lookup"><span data-stu-id="08a1f-110">Deliver</span></span>
- <span data-ttu-id="08a1f-111">Valmistuminen</span><span class="sxs-lookup"><span data-stu-id="08a1f-111">Complete</span></span>
- <span data-ttu-id="08a1f-112">Sulje</span><span class="sxs-lookup"><span data-stu-id="08a1f-112">Close</span></span> 

## <a name="new"></a><span data-ttu-id="08a1f-113">Uusi</span><span class="sxs-lookup"><span data-stu-id="08a1f-113">New</span></span>

<span data-ttu-id="08a1f-114">Kun luot projektin, projektin vaiheeksi on määritetty **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="08a1f-114">When you create a project, the project stage is set to **New**.</span></span> <span data-ttu-id="08a1f-115">Jos projekti on luotu mallista, siinä voi olla aikataulu, arvio ja ryhmän tiedot.</span><span class="sxs-lookup"><span data-stu-id="08a1f-115">If the project was created from a template, it might have schedule, estimate, and team data.</span></span> <span data-ttu-id="08a1f-116">Muussa tapauksessa se on vain luonnos projektista, ja muut osat on syötettävä.</span><span class="sxs-lookup"><span data-stu-id="08a1f-116">Otherwise, it's just an outline of the project, and the remaining components must be entered.</span></span>

## <a name="quote"></a><span data-ttu-id="08a1f-117">Tarjous</span><span class="sxs-lookup"><span data-stu-id="08a1f-117">Quote</span></span>

<span data-ttu-id="08a1f-118">Kun liität projektin tarjoukseen tai luot sen tarjouksesta, projektivaiheeksi on määritetty **Tarjous**, ja arvioidut aloitus- ja päättymispäivät päivitetään myös.</span><span class="sxs-lookup"><span data-stu-id="08a1f-118">When you associate a project with a quote, or when you create a project from a quote, the project stage is set to **Quote**, and the estimated start and end dates are updated.</span></span> <span data-ttu-id="08a1f-119">Kun projekti on **Tarjous**-vaiheessa, **Myynti**-välilehti **Projektikohde**-sivulla näyttää tarjouksen tiedot.</span><span class="sxs-lookup"><span data-stu-id="08a1f-119">While the project is in the **Quote** stage, the **Sales** tab on the **Project Entity** page shows details of the quote.</span></span>

## <a name="plan"></a><span data-ttu-id="08a1f-120">Suunnittelu</span><span class="sxs-lookup"><span data-stu-id="08a1f-120">Plan</span></span>

<span data-ttu-id="08a1f-121">Kun projektiin liittyvä tarjous voittaa ja valmistelu etenee **Sopimus**-vaiheeseen, päivitetään projektin vaiheeksi **Suunnittelu**.</span><span class="sxs-lookup"><span data-stu-id="08a1f-121">When you win a quote that is associated with a project, and the project is moved to the **Contract** phase, the project stage is updated to **Plan**.</span></span> <span data-ttu-id="08a1f-122">Kun projekti on **Suunnittelu**-vaiheessa, **Projektikohde**-sivulla näytetään sopimuksen tiedot.</span><span class="sxs-lookup"><span data-stu-id="08a1f-122">While the project is in the **Plan** stage, the **Project Entity** page shows details of the contract.</span></span>

## <a name="deliver"></a><span data-ttu-id="08a1f-123">Toimitus</span><span class="sxs-lookup"><span data-stu-id="08a1f-123">Deliver</span></span>

<span data-ttu-id="08a1f-124">Kun projektisuunnitelma valmistuu ja olet valmis aloittamaan projektin, projektipäällikön on päivitettävä projekti vaihe **Toimitettavaksi** osoittamaan, että projekti on käynnistynyt.</span><span class="sxs-lookup"><span data-stu-id="08a1f-124">When the project plan is completed, and you're ready to start the project, the project manager should update the project stage to **Deliver** to show that the project has started.</span></span>

## <a name="complete"></a><span data-ttu-id="08a1f-125">Valmistuminen</span><span class="sxs-lookup"><span data-stu-id="08a1f-125">Complete</span></span> 

<span data-ttu-id="08a1f-126">Kun projektin työ on valmis, projektipäällikkö voi päivittää vaiheen **valmistuneeksi**.</span><span class="sxs-lookup"><span data-stu-id="08a1f-126">When the work for the project is completed, the project manager can update the stage to **Complete**.</span></span> <span data-ttu-id="08a1f-127">Kun projektipäällikkö päivittää projektin vaiheen **valmiiksi**, se osoittaa, että työ on 100 prosenttisesti valmiina, mutta että projekti on avoinna niin, että odottavat aika- tai kulukirjaukset voidaan kirjata.</span><span class="sxs-lookup"><span data-stu-id="08a1f-127">By updating the project stage to **Complete**, the project manager indicates that the work is 100-percent completed, but that the project is being kept open so that any pending time or expense entries can be recorded.</span></span>

## <a name="close"></a><span data-ttu-id="08a1f-128">Sulje</span><span class="sxs-lookup"><span data-stu-id="08a1f-128">Close</span></span>

<span data-ttu-id="08a1f-129">Kun kaikki tapahtumat on kirjattu projektille, projektipäällikkö voi päivittää vaiheen **suljetuksi**.</span><span class="sxs-lookup"><span data-stu-id="08a1f-129">When all transactions are recorded for the project, the project manager can update the stage to **Close**.</span></span> <span data-ttu-id="08a1f-130">Tässä vaiheessa tapahtumia ei voi tallentaa, ja projekti on määritetty vain luku -tilaan.</span><span class="sxs-lookup"><span data-stu-id="08a1f-130">At that point, no transactions can be recorded, and the project is set to read-only.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]