---
title: Matkalaskujen kirjaaminen
description: Tässä aiheessa kerrotaan, miten kuluraportit kirjataan.
author: suvaidya
manager: AnnBe
ms.date: 09/09/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: ''
ms.author: shylaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: ec897373cd74f7d7f63cd9ca4c46f4245336eb7f
ms.sourcegitcommit: 56c42d7f5995a674426a1c2a81bae897dceb391c
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/01/2020
ms.locfileid: "3907404"
---
# <a name="post-expense-reports"></a><span data-ttu-id="e5e9b-103">Matkalaskujen kirjaaminen</span><span class="sxs-lookup"><span data-stu-id="e5e9b-103">Post expense reports</span></span>

<span data-ttu-id="e5e9b-104">Kun kuluraportti on hyväksytty ja siirretty yleiseen päiväkirjaan, se voidaan kirjata.</span><span class="sxs-lookup"><span data-stu-id="e5e9b-104">After an expense report has been approved and transferred to the general journal, it can be posted.</span></span> <span data-ttu-id="e5e9b-105">Kun kirjaat kuluraportin, kulut, joista voidaan palauttaa arvonlisävero (ALV), tunnistetaan.</span><span class="sxs-lookup"><span data-stu-id="e5e9b-105">When you post an expense report, expenses that are eligible for recovery of value-added tax (VAT) are identified.</span></span> <span data-ttu-id="e5e9b-106">ALV-maksujen tarkistamisen ja palauttamisen tehtävä määritetään työntekijälle, joka on vastuussa kuluraportin tarkistamisesta.</span><span class="sxs-lookup"><span data-stu-id="e5e9b-106">The task of verifying and recovering VAT payments is assigned to the employee who is responsible for verifying the expense report.</span></span>

<span data-ttu-id="e5e9b-107">Jos kuluraportin kulut veloitetaan muulle yritykselle kuin yritykselle, joka työllistää työntekijän, sinun täytyy tarkistaa sekä yritys jolle kyseiset kulut ollaan velkaa että yritys, joka on velkaa.</span><span class="sxs-lookup"><span data-stu-id="e5e9b-107">If expenses on an expense report are charged to a company other than the company that employs the employee, you must verify both the company that those expenses are owed to and the company that they are owed from.</span></span> <span data-ttu-id="e5e9b-108">Esimerkiksi kuluraportin lähettänyt työntekijä toimii DAT-yrityksessä, mutta veloitti kulun DIR-yritykseltä.</span><span class="sxs-lookup"><span data-stu-id="e5e9b-108">For example, the employee who submitted an expense report works for the DAT company but charged an expense to the DIR company.</span></span> <span data-ttu-id="e5e9b-109">Tällöin DAT on yritys, jolle kulu ollaan velkaa, ja DIR on yritys joka on velkaa kulun.</span><span class="sxs-lookup"><span data-stu-id="e5e9b-109">In this case, DAT is the company that the expense is owed to, and DIR is the company that the expense is owed from.</span></span> <span data-ttu-id="e5e9b-110">Kun olet tarkistanut nämä kirjauskansionrivit, voit kirjata kulurivit pääkirjanpitoon.</span><span class="sxs-lookup"><span data-stu-id="e5e9b-110">After you verify these journal lines, you can post the expense lines to the general ledger.</span></span>

<span data-ttu-id="e5e9b-111">Voit kirjata kuluraportin valitsemalla **Hyväksytyt kuluraportit** -sivulla kuluraportin ja valitsemalla sitten toimintoruudussa **Kirjaa**.</span><span class="sxs-lookup"><span data-stu-id="e5e9b-111">To post an expense report, on the **Approved expense reports** page, select the expense report, and then, on the Action Pane, select **Post**.</span></span>

<span data-ttu-id="e5e9b-112">Voit myös kirjata kaikki luettelon kuluraportit samalla kertaa.</span><span class="sxs-lookup"><span data-stu-id="e5e9b-112">You can also post all the expense reports in the list at the same time.</span></span> <span data-ttu-id="e5e9b-113">Valitse kaikki kuluraportit ja valitse sitten **Kirjaa**.</span><span class="sxs-lookup"><span data-stu-id="e5e9b-113">Select all the expense reports, and then select **Post**.</span></span>
