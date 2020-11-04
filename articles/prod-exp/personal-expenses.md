---
title: Matkalaskun henkilökohtaiset kulut
description: Tässä aiheessa kerrotaan kahdesta tavasta käsitellä työntekijän henkilökohtaisia kuluja Microsoft Dynamics 365 Financessa.
author: saraschi2
manager: AnnBe
ms.date: 02/23/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TrvParameters
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 825b6c131c8a65b99d5b7ebdadcd6389886f2d11
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/16/2020
ms.locfileid: "4075497"
---
# <a name="personal-expenses-on-an-expense-report"></a><span data-ttu-id="2a06b-103">Matkalaskun henkilökohtaiset kulut</span><span class="sxs-lookup"><span data-stu-id="2a06b-103">Personal expenses on an expense report</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2a06b-104">Liikematkustuksen aikana työntekijät saattavat joskus veloittaa henkilökohtaisia kuluja yrityksen luottokortilta.</span><span class="sxs-lookup"><span data-stu-id="2a06b-104">During business travel, workers might sometimes charge personal expenses to their corporate credit cards.</span></span> <span data-ttu-id="2a06b-105">Jos henkilökohtaisten kulujen käsittelyprosessia ei määritetä, kuluraporttien hyväksyntäprosessi voi häiriintyä, kun työntekijät lähettävät eriteltyjä kuluraporttejaan.</span><span class="sxs-lookup"><span data-stu-id="2a06b-105">If you don't define a process for handling personal expenses, the approval process for expense reports might be disrupted when workers submit their itemized expense reports.</span></span> 

<span data-ttu-id="2a06b-106">Työntekijän henkilökohtaisten kulujen käsittelyyn on kaksi tapaa:</span><span class="sxs-lookup"><span data-stu-id="2a06b-106">There are two methods for handling a worker's personal expenses:</span></span>

- <span data-ttu-id="2a06b-107">**Työntekijän maksama** – organisaatiosi ei maksa henkilökohtaisia kuluja, jotka näkyvät yrityksen luottokorttilaskussa.</span><span class="sxs-lookup"><span data-stu-id="2a06b-107">**Paid by employee** – Your organization doesn't pay personal expenses that appear on the bill for the corporate credit card.</span></span> <span data-ttu-id="2a06b-108">Sen sijaan se luo raportin, jossa näkyvät henkilökohtaiset kulut sekä yrityksen luottokortilta veloitetut yrityksen kulut.</span><span class="sxs-lookup"><span data-stu-id="2a06b-108">Instead, it creates a report that shows personal expenses together with the corporate expenses that were charged to the corporate credit card.</span></span>
- <span data-ttu-id="2a06b-109">**Yrityksen maksama** – Organisaatiosi maksaa koko laskun yrityksen luottokortilta ja veloittaa sitten työntekijän henkilökohtaiset kulut.</span><span class="sxs-lookup"><span data-stu-id="2a06b-109">**Paid by company** – Your organization pays the whole bill for the corporate credit card and then debits the worker's account for the personal expenses.</span></span>

<span data-ttu-id="2a06b-110">Voit valita menetelmän, jota organisaatiosi käyttää **kulun hallinnan parametrit** -sivulla.</span><span class="sxs-lookup"><span data-stu-id="2a06b-110">You can select the method that your organization uses on the **Expense management parameters** page.</span></span>
