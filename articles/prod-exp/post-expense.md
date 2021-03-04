---
title: Kirjaa matkalasku
description: Tässä aiheessa kerrotaan, miten kuluraportti kirjataan pääkirjanpitoon.
author: saraschi2
manager: AnnBe
ms.date: 02/26/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TrvPerDiems
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 982b7621c35547448b5d756f77f3873b9fbbcb9d
ms.sourcegitcommit: 9f31b33ed6e7f1b49200a407913201a1337f3401
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/14/2021
ms.locfileid: "4960107"
---
# <a name="post-an-expense-report"></a><span data-ttu-id="ee03a-103">Kirjaa matkalasku</span><span class="sxs-lookup"><span data-stu-id="ee03a-103">Post an expense report</span></span>

<span data-ttu-id="ee03a-104">Kun kuluraportti on hyväksytty ja siirretty yleiseen päiväkirjaan, se voidaan kirjata pääkirjanpitoon.</span><span class="sxs-lookup"><span data-stu-id="ee03a-104">After an expense report has been approved and transferred to the general journal, it can be posted to the general ledger.</span></span> <span data-ttu-id="ee03a-105">Kun kirjaat kuluraportin, kulut, joista voidaan palauttaa arvonlisävero (ALV), tunnistetaan.</span><span class="sxs-lookup"><span data-stu-id="ee03a-105">When you post an expense report, expenses that are eligible for recovery of value-added tax (VAT) are identified.</span></span> <span data-ttu-id="ee03a-106">ALV-maksujen tarkistamisen ja palauttamisen tehtävä määritetään työntekijälle, joka on vastuussa kuluraportin tarkistamisesta.</span><span class="sxs-lookup"><span data-stu-id="ee03a-106">The task of verifying and recovering VAT payments is assigned to the employee who is responsible for verifying the expense report.</span></span>

<span data-ttu-id="ee03a-107">Jos kuluraportin kulut veloitetaan muulle yritykselle kuin yritykselle, joka työllistää työntekijän, sinun täytyy tarkistaa yritys jolle kyseiset kulut ollaan velkaa että yritys, joka on velkaa kyseiset kulut.</span><span class="sxs-lookup"><span data-stu-id="ee03a-107">If expenses on an expense report are charged to a company other than the company that employs the employee, you must verify the company that those expenses are owed to and the company that the expenses are owed from.</span></span> <span data-ttu-id="ee03a-108">Esimerkiksi kuluraportin lähettänyt työntekijä toimii DAT-yrityksessä, mutta veloitti kulun DIR-yritykseltä.</span><span class="sxs-lookup"><span data-stu-id="ee03a-108">For example, the employee who submitted an expense report works for the DAT company but charged an expense to the DIR company.</span></span> <span data-ttu-id="ee03a-109">Tällöin DAT on yritys, jolle kulu ollaan velkaa, ja DIR on yritys joka on velkaa kulun.</span><span class="sxs-lookup"><span data-stu-id="ee03a-109">In this case, DAT is the company that the expense is owed to, and DIR is the company that the expense is owed from.</span></span> <span data-ttu-id="ee03a-110">Kun olet tarkistanut nämä kirjauskansionrivit, voit kirjata kulurivit pääkirjanpitoon.</span><span class="sxs-lookup"><span data-stu-id="ee03a-110">After you verify these journal lines, you can post the expense lines to the general ledger.</span></span>

<span data-ttu-id="ee03a-111">Voit kirjata kuluraportin valitsemalla **Hyväksytyt kuluraportit** -sivulla kuluraportin ja valitsemalla sitten toimintoruudussa **Kirjaa**.</span><span class="sxs-lookup"><span data-stu-id="ee03a-111">To post an expense report, on the **Approved expense reports** page, select the expense report, and then, on the Action Pane, select **Post**.</span></span>

<span data-ttu-id="ee03a-112">Voit myös kirjata kaikki luettelon kuluraportit samalla kertaa.</span><span class="sxs-lookup"><span data-stu-id="ee03a-112">You can also post all the expense reports in the list at the same time.</span></span> <span data-ttu-id="ee03a-113">Valitse kaikki kuluraportit ja valitse sitten **Kirjaa**.</span><span class="sxs-lookup"><span data-stu-id="ee03a-113">Select all the expense reports, and then select **Post**.</span></span>
