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
ms.openlocfilehash: d6b9d4fa0f69b4b0fe4bd1786958d22e5580a321
ms.sourcegitcommit: 9f31b33ed6e7f1b49200a407913201a1337f3401
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/14/2021
ms.locfileid: "4960873"
---
# <a name="personal-expenses-on-an-expense-report"></a><span data-ttu-id="dfce8-103">Matkalaskun henkilökohtaiset kulut</span><span class="sxs-lookup"><span data-stu-id="dfce8-103">Personal expenses on an expense report</span></span>

<span data-ttu-id="dfce8-104">Liikematkustuksen aikana työntekijät saattavat joskus veloittaa henkilökohtaisia kuluja yrityksen luottokortilta.</span><span class="sxs-lookup"><span data-stu-id="dfce8-104">During business travel, workers might sometimes charge personal expenses to their corporate credit cards.</span></span> <span data-ttu-id="dfce8-105">Jos henkilökohtaisten kulujen käsittelyprosessia ei määritetä, kuluraporttien hyväksyntäprosessi voi häiriintyä, kun työntekijät lähettävät eriteltyjä kuluraporttejaan.</span><span class="sxs-lookup"><span data-stu-id="dfce8-105">If you don't define a process for handling personal expenses, the approval process for expense reports might be disrupted when workers submit their itemized expense reports.</span></span> 

<span data-ttu-id="dfce8-106">Työntekijän henkilökohtaisten kulujen käsittelyyn on kaksi tapaa:</span><span class="sxs-lookup"><span data-stu-id="dfce8-106">There are two methods for handling a worker's personal expenses:</span></span>

- <span data-ttu-id="dfce8-107">**Työntekijän maksama** – organisaatiosi ei maksa henkilökohtaisia kuluja, jotka näkyvät yrityksen luottokorttilaskussa.</span><span class="sxs-lookup"><span data-stu-id="dfce8-107">**Paid by employee** – Your organization doesn't pay personal expenses that appear on the bill for the corporate credit card.</span></span> <span data-ttu-id="dfce8-108">Sen sijaan se luo raportin, jossa näkyvät henkilökohtaiset kulut sekä yrityksen luottokortilta veloitetut yrityksen kulut.</span><span class="sxs-lookup"><span data-stu-id="dfce8-108">Instead, it creates a report that shows personal expenses together with the corporate expenses that were charged to the corporate credit card.</span></span>
- <span data-ttu-id="dfce8-109">**Yrityksen maksama** – Organisaatiosi maksaa koko laskun yrityksen luottokortilta ja veloittaa sitten työntekijän henkilökohtaiset kulut.</span><span class="sxs-lookup"><span data-stu-id="dfce8-109">**Paid by company** – Your organization pays the whole bill for the corporate credit card and then debits the worker's account for the personal expenses.</span></span>

<span data-ttu-id="dfce8-110">Voit valita menetelmän, jota organisaatiosi käyttää **kulun hallinnan parametrit** -sivulla.</span><span class="sxs-lookup"><span data-stu-id="dfce8-110">You can select the method that your organization uses on the **Expense management parameters** page.</span></span>
