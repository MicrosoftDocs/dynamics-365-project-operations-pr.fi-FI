---
title: Resurssiarviot
description: Tässä aiheessa on tietoja siitä, miten resurssiarviot lasketaan Project Operationsissa.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 98a61746f172b50bf6fa29cb0d21462cd616f417
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5286514"
---
# <a name="resource-estimates"></a><span data-ttu-id="242c4-103">Resurssiarviot</span><span class="sxs-lookup"><span data-stu-id="242c4-103">Resource estimates</span></span>

<span data-ttu-id="242c4-104">_**Koskee:** Project Operationsin resurssiin / muuhun kuin resurssiin perustuvia skenaarioita, Lite-käyttöönotto-kaupasta proformalaskutukseen_</span><span class="sxs-lookup"><span data-stu-id="242c4-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="242c4-105">Resurssiarviot tulevat työrakenteessa määritetystä aikajaksotetusta työmäärästä, johon sisältyvät sovellettavat hinnoitteludimensiot.</span><span class="sxs-lookup"><span data-stu-id="242c4-105">Resource estimates come from time-phased effort that is defined in the work breakdown structure along with applicable pricing dimensions.</span></span> <span data-ttu-id="242c4-106">Yleensä laskenta on **hinta/tunti kullekin roolille x tuntia**</span><span class="sxs-lookup"><span data-stu-id="242c4-106">Typically, the calculation is **rate/hr for each role x hours.**</span></span> <span data-ttu-id="242c4-107">Kunkin resurssin aikajaksotettu työmäärä tallennetaan resurssin delegointitietueeseen.</span><span class="sxs-lookup"><span data-stu-id="242c4-107">The time-phased effort for each resource is stored in the resource assignment record.</span></span> <span data-ttu-id="242c4-108">Hinnoittelu on tallennetaan ennalta määritettyyn hinnastoon.</span><span class="sxs-lookup"><span data-stu-id="242c4-108">The pricing is stored in a pre-defined price list.</span></span> <span data-ttu-id="242c4-109">Yksikkömuunnosta käytetään sovellettavan hinnaston perusteella.</span><span class="sxs-lookup"><span data-stu-id="242c4-109">Unit conversion is applied based on the applicable price list.</span></span>

![Resurssiarviot](./media/navigation12.png)

## <a name="default-cost-price-and-cost-currency"></a><span data-ttu-id="242c4-111">Kustannushinnan ja kustannusvaluutan oletusarvot</span><span class="sxs-lookup"><span data-stu-id="242c4-111">Default cost price and cost currency</span></span>

<span data-ttu-id="242c4-112">Kustannushinnat määritetään oletusarvona organisaatioyksiköstä.</span><span class="sxs-lookup"><span data-stu-id="242c4-112">Cost prices are defaulted from the Organizational Unit.</span></span>

## <a name="default-bill-rate-and-sales-currency"></a><span data-ttu-id="242c4-113">Laskutushinnan ja myyntivaluutan oletusarvot</span><span class="sxs-lookup"><span data-stu-id="242c4-113">Default bill rate and sales currency</span></span>

<span data-ttu-id="242c4-114">Myyntihintoja käytetään kerran sopimusta kohden.</span><span class="sxs-lookup"><span data-stu-id="242c4-114">Sales prices are applied once per deal.</span></span> <span data-ttu-id="242c4-115">Myyntihinnaston hierarkian oletusarvo on seuraava:</span><span class="sxs-lookup"><span data-stu-id="242c4-115">The hierarchy for sale price list defaulting is as follows:</span></span>

1. <span data-ttu-id="242c4-116">Organisaatio</span><span class="sxs-lookup"><span data-stu-id="242c4-116">Organization</span></span>
2. <span data-ttu-id="242c4-117">Asiakas</span><span class="sxs-lookup"><span data-stu-id="242c4-117">Customer</span></span>
3. <span data-ttu-id="242c4-118">Tarjous/sopimus</span><span class="sxs-lookup"><span data-stu-id="242c4-118">Quote/contract</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]