---
title: Matkalaskut ja monta hyväksyjää
description: Tässä aiheessa on tietoja kuluraporteista, jotka vaativat usean henkilön hyväksynnän.
author: suvaidya
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: ''
ms.author: shylaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 548673541cee5ce598721f94415c0444995c8325
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/16/2020
ms.locfileid: "4075351"
---
# <a name="expense-reports-and-multiple-approvers"></a><span data-ttu-id="b0442-103">Matkalaskut ja monta hyväksyjää</span><span class="sxs-lookup"><span data-stu-id="b0442-103">Expense reports and multiple approvers</span></span>

<span data-ttu-id="b0442-104">_**Koskee:** Project Operationsin resurssiin / muuhun kuin resurssiin perustuvia skenaarioita, Lite-käyttöönotto-kaupasta proformalaskutukseen_</span><span class="sxs-lookup"><span data-stu-id="b0442-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="b0442-105">Organisaation kulujen hyväksyntäkäytännöt voivat edellyttää, että lähetetty kuluraportti vaatii usean henkilön hyväksynnän.</span><span class="sxs-lookup"><span data-stu-id="b0442-105">Depending on your organization's expense approval policies, more than one person might have to approve a submitted expense report.</span></span> <span data-ttu-id="b0442-106">Kun määrität työnkulkuprosessin kuluraportin hyväksynnälle, voit lisätä tehtäviä tai vaiheita sisältäviä työnkulkuelementtejä yhdelle tai usealle kuluraportin hyväksyjälle.</span><span class="sxs-lookup"><span data-stu-id="b0442-106">When you set up the workflow process for expense report approval, you can add workflow elements that include tasks or steps for one or more expense report approvers.</span></span> <span data-ttu-id="b0442-107">Voit esimerkiksi edellyttää, että kahden henkilön on hyväksyttävä kaikki kuluraportit. Henkilöt voivat olla raportin lähettäneen työntekijän esimies ja ostoreskontran koordinaattori.</span><span class="sxs-lookup"><span data-stu-id="b0442-107">For example, you might require that all expense reports be approved by two separate people, the manager of the employee who submitted the report and the Accounts payable coordinator.</span></span>

<span data-ttu-id="b0442-108">Jos päätät vaatia kuluraportille useita hyväksyjiä, voit lisätä työnkulkuelementit jollakin seuraavista tavoista:</span><span class="sxs-lookup"><span data-stu-id="b0442-108">If you decide to require multiple expense report approvers, you can add the workflow elements in any of the following ways:</span></span>

- <span data-ttu-id="b0442-109">Lisää yksi hyväksyntäelementti, jossa on yksi vaihe.</span><span class="sxs-lookup"><span data-stu-id="b0442-109">Add one approval element that has one step.</span></span> <span data-ttu-id="b0442-110">Vaihe voi edellyttää esimerkiksi, että kuluraportti on määritettävä käyttäjäryhmälle ja että käyttäjäryhmän jäsenistä 50 prosentin on hyväksyttävä se.</span><span class="sxs-lookup"><span data-stu-id="b0442-110">For example, the step might require that an expense report be assigned to a user group, and that it be approved by 50 percent of the user group's members.</span></span>
- <span data-ttu-id="b0442-111">Lisää yksi hyväksyntäelementti, jossa on useita vaiheita.</span><span class="sxs-lookup"><span data-stu-id="b0442-111">Add one approval element that has multiple steps.</span></span> <span data-ttu-id="b0442-112">Hyväksyntäelementillä voi olla esimerkiksi seuraavat vaiheet:</span><span class="sxs-lookup"><span data-stu-id="b0442-112">For example, the approval element might have the following steps:</span></span>

    1. <span data-ttu-id="b0442-113">Kuluraportin lähettäneen työntekijän esimies hyväksyy raportin.</span><span class="sxs-lookup"><span data-stu-id="b0442-113">The manager of the employee who submitted the expense report approves it.</span></span>
    2. <span data-ttu-id="b0442-114">Ostoreskontran virkailija tarkistaa kuitit ja kuluraportin nimikkeet.</span><span class="sxs-lookup"><span data-stu-id="b0442-114">The Accounts payable clerk verifies the receipts and the expense report items.</span></span>
    3. <span data-ttu-id="b0442-115">Budjetin omistaja hyväksyy kuluraportin.</span><span class="sxs-lookup"><span data-stu-id="b0442-115">The budget owner approves the expense report.</span></span>

- <span data-ttu-id="b0442-116">Lisää useita hyväksyntäelementtejä, joista jokaisessa on yksi vaihe.</span><span class="sxs-lookup"><span data-stu-id="b0442-116">Add multiple approval elements, each of which has one step.</span></span> <span data-ttu-id="b0442-117">Voit esimerkiksi lisätä erillisen hyväksyntäelementin kullekin seuraavista vaiheista:</span><span class="sxs-lookup"><span data-stu-id="b0442-117">For example, you might add a separate approval element for each of the following steps:</span></span>

    1. <span data-ttu-id="b0442-118">Työntekijän esimies hyväksyy kuluraportin.</span><span class="sxs-lookup"><span data-stu-id="b0442-118">The employee's manager approves the expense report.</span></span>
    2. <span data-ttu-id="b0442-119">Budjetin omistaja hyväksyy kuluraportin.</span><span class="sxs-lookup"><span data-stu-id="b0442-119">The budget owner approves the expense report.</span></span>
