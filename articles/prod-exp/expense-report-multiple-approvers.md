---
title: Matkalaskun monta hyväksyjää
description: Tässä aiheessa on tietoja kuluraporteista, jotka vaativat usean henkilön hyväksynnän.
author: saraschi2
manager: AnnBe
ms.date: 02/23/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TrvExpensesReportList
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ce24b156a268f9f5aada35f9314d2d9c6607200b
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/16/2020
ms.locfileid: "4075504"
---
# <a name="multiple-approvers-on-an-expense-report"></a><span data-ttu-id="31ce8-103">Matkalaskun monta hyväksyjää</span><span class="sxs-lookup"><span data-stu-id="31ce8-103">Multiple approvers on an expense report</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="31ce8-104">Organisaation kulujen hyväksyntäkäytännöt voivat edellyttää, että työntekijän lähettämä kuluraportti vaatii usean henkilön hyväksynnän.</span><span class="sxs-lookup"><span data-stu-id="31ce8-104">Depending on your organization's expense approval policies, more than one person might have to approve an expense report that is submitted by an employee.</span></span> <span data-ttu-id="31ce8-105">Kun määrität työnkulkuprosessin kuluraportin hyväksynnälle, voit lisätä tehtäviä tai vaiheita sisältäviä työnkulkuelementtejä yhdelle tai usealle kuluraportin hyväksyjälle.</span><span class="sxs-lookup"><span data-stu-id="31ce8-105">When you set up the workflow process for expense report approval, you can add workflow elements that include tasks or steps for one or more expense report approvers.</span></span> <span data-ttu-id="31ce8-106">Voit esimerkiksi edellyttää, että ensin työntekijän esimiehen ja sitten ostoreskontran koordinaattorin on hyväksyttävä kaikki kuluraportit.</span><span class="sxs-lookup"><span data-stu-id="31ce8-106">For example, you might require that all expense reports be approved first by the manager of the employee who submitted the report and then by the Accounts payable coordinator.</span></span>

<span data-ttu-id="31ce8-107">Jos päätät vaatia kuluraportille useita hyväksyjiä, voit lisätä työnkulkuelementit jollakin seuraavista tavoista:</span><span class="sxs-lookup"><span data-stu-id="31ce8-107">If you decide to require multiple expense report approvers, you can add the workflow elements in any of the following ways:</span></span>

- <span data-ttu-id="31ce8-108">Lisää yksi hyväksyntäelementti, jossa on yksi vaihe.</span><span class="sxs-lookup"><span data-stu-id="31ce8-108">Add one approval element that has one step.</span></span> <span data-ttu-id="31ce8-109">Vaihe voi edellyttää esimerkiksi, että kuluraportti on määritettävä käyttäjäryhmälle ja että käyttäjäryhmän jäsenistä 50 prosentin on hyväksyttävä se.</span><span class="sxs-lookup"><span data-stu-id="31ce8-109">For example, the step might require that an expense report be assigned to a user group, and that it be approved by 50 percent of the user group's members.</span></span>
- <span data-ttu-id="31ce8-110">Lisää yksi hyväksyntäelementti, jossa on useita vaiheita.</span><span class="sxs-lookup"><span data-stu-id="31ce8-110">Add one approval element that has multiple steps.</span></span> <span data-ttu-id="31ce8-111">Hyväksyntäelementillä voi olla esimerkiksi seuraavat vaiheet:</span><span class="sxs-lookup"><span data-stu-id="31ce8-111">For example, the approval element might have the following steps:</span></span>

    1. <span data-ttu-id="31ce8-112">Kuluraportin lähettäneen työntekijän esimies hyväksyy raportin.</span><span class="sxs-lookup"><span data-stu-id="31ce8-112">The manager of the employee who submitted the expense report approves it.</span></span>
    2. <span data-ttu-id="31ce8-113">Ostoreskontran virkailija tarkistaa kuitit ja kuluraportin nimikkeet.</span><span class="sxs-lookup"><span data-stu-id="31ce8-113">The Accounts payable clerk verifies the receipts and the expense report items.</span></span>
    3. <span data-ttu-id="31ce8-114">Budjetin omistaja hyväksyy kuluraportin.</span><span class="sxs-lookup"><span data-stu-id="31ce8-114">The budget owner approves the expense report.</span></span>

- <span data-ttu-id="31ce8-115">Lisää useita hyväksyntäelementtejä, joista jokaisessa on yksi vaihe.</span><span class="sxs-lookup"><span data-stu-id="31ce8-115">Add multiple approval elements, each of which has one step.</span></span> <span data-ttu-id="31ce8-116">Voit esimerkiksi lisätä erillisen hyväksyntäelementin kullekin seuraavista vaiheista:</span><span class="sxs-lookup"><span data-stu-id="31ce8-116">For example, you might add a separate approval element for each of the following steps:</span></span>

    1. <span data-ttu-id="31ce8-117">Työntekijän esimies hyväksyy kuluraportin.</span><span class="sxs-lookup"><span data-stu-id="31ce8-117">The employee's manager approves the expense report.</span></span>
    2. <span data-ttu-id="31ce8-118">Budjetin omistaja hyväksyy kuluraportin.</span><span class="sxs-lookup"><span data-stu-id="31ce8-118">The budget owner approves the expense report.</span></span>
