---
title: Kulun merkintä (lite)
description: Tässä aiheessa on tietoja siitä, miten voit käsitellä kulumerkintöjä lite-ympäristössä.
author: stsporen
manager: AnnBe
ms.date: 10/06/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 746d5d9ff56222e7d6b9b6e264db75d5814365c7
ms.sourcegitcommit: fd8ea1779db2bb39a428f459ae3293c4fd785572
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/06/2020
ms.locfileid: "3965773"
---
# <a name="expense-entry-lite"></a><span data-ttu-id="5f2a2-103">Kulun merkintä (lite)</span><span class="sxs-lookup"><span data-stu-id="5f2a2-103">Expense entry (lite)</span></span>

<span data-ttu-id="5f2a2-104">_**Käytetään:** Lite-käyttöönotto – kauppa proformalaskutukseen_</span><span class="sxs-lookup"><span data-stu-id="5f2a2-104">_**Applies to:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="5f2a2-105">Basic- tai Lite-kulujen hallinta on mahdollisuus tallentaa yksinkertaisia kuluja.</span><span class="sxs-lookup"><span data-stu-id="5f2a2-105">Basic, or lite, expense management is the capability to record simple expenses.</span></span> <span data-ttu-id="5f2a2-106">Voit kirjata kuluja projektiin, minkä jälkeen projektin hyväksyjä tarkistaa ne ja hyväksyy ne.</span><span class="sxs-lookup"><span data-stu-id="5f2a2-106">You can record expenses against a project, and then the project approver will review and approve them.</span></span>

<span data-ttu-id="5f2a2-107">Lisätietoja Dynamics 365 Project Operationsin kuluominaisuuksista on ohjeaiheessa [kulujen yleiskuvaus](expense-overview.md).</span><span class="sxs-lookup"><span data-stu-id="5f2a2-107">For more information about expense capabilities in Dynamics 365 Project Operations, see [Expense overview](expense-overview.md).</span></span>

## <a name="capture-a-basic-expense"></a><span data-ttu-id="5f2a2-108">Peruskulun sieppaaminen</span><span class="sxs-lookup"><span data-stu-id="5f2a2-108">Capture a basic expense</span></span>

<span data-ttu-id="5f2a2-109">Voit tallentaa kulut, jotta voit lähettää ne hyväksyjälle.</span><span class="sxs-lookup"><span data-stu-id="5f2a2-109">You can capture your expenses so that you can submit them to the approver.</span></span>

1. <span data-ttu-id="5f2a2-110">Siirry kohtaan **Kulut** ja valitse **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="5f2a2-110">Go to **Expenses**, and select **New**.</span></span>
2. <span data-ttu-id="5f2a2-111">Kirjoita **Uusi kulu** -sivulla pakolliset kulutiedot ja valitse sitten **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="5f2a2-111">On the **New Expense** page, enter the required expense information, and then select **Save**.</span></span>

## <a name="submit-a-basic-expense"></a><span data-ttu-id="5f2a2-112">Peruskulun lähettäminen</span><span class="sxs-lookup"><span data-stu-id="5f2a2-112">Submit a basic expense</span></span>

<span data-ttu-id="5f2a2-113">Kun olet lopettanut kaikkien kulujen tallentamisen ja olet valmis siirtymään hyväksymisvaiheeseen, sinun täytyy lähettää ne.</span><span class="sxs-lookup"><span data-stu-id="5f2a2-113">After you've finished capturing all your expenses, and you're ready to have them approved, you must submit them.</span></span>

1. <span data-ttu-id="5f2a2-114">Siirry kohtaan **Kulut** ja valitse kulu.</span><span class="sxs-lookup"><span data-stu-id="5f2a2-114">Go to **Expenses**, and select an expense.</span></span> <span data-ttu-id="5f2a2-115">Voit myös valita kaikki kulut käyttämällä otsikon valintaruutua.</span><span class="sxs-lookup"><span data-stu-id="5f2a2-115">Or, select all the expenses by using the check box on the header.</span></span>
2. <span data-ttu-id="5f2a2-116">Valitse **Lähetä**.</span><span class="sxs-lookup"><span data-stu-id="5f2a2-116">Select **Submit**.</span></span> <span data-ttu-id="5f2a2-117">Järjestelmä käsittelee valitut tapahtumat ja luo sitten kulun hyväksyntäpyynnöt.</span><span class="sxs-lookup"><span data-stu-id="5f2a2-117">The system processes the selected entries and then creates expense approval requests.</span></span>

## <a name="recall-a-basic-expense"></a><span data-ttu-id="5f2a2-118">Peruskulun peruttaaminen</span><span class="sxs-lookup"><span data-stu-id="5f2a2-118">Recall a basic expense</span></span>

<span data-ttu-id="5f2a2-119">Kun lähetät kulun vahingossa, voit peruuttaa sen.</span><span class="sxs-lookup"><span data-stu-id="5f2a2-119">When you submit an expense by mistake, you can recall it.</span></span> <span data-ttu-id="5f2a2-120">Kulumerkinnän peruutuksen edellyttämä aika määräytyy sen hyväksyntävaiheen mukaan.</span><span class="sxs-lookup"><span data-stu-id="5f2a2-120">The time that is required to recall an expense entry depends on its approval stage.</span></span>  <span data-ttu-id="5f2a2-121">Jos hyväksyjä ei ole vielä hyväksynyt merkintää, peruuttaminen voi tapahtua heti.</span><span class="sxs-lookup"><span data-stu-id="5f2a2-121">If the approver hasn't yet approved the entry, the recall can occur immediately.</span></span> <span data-ttu-id="5f2a2-122">Jos tapahtuma on kuitenkin jo hyväksytty, hyväksyjää pyydetään hyväksymään peruutus ja peruuttamaan tapahtumat.</span><span class="sxs-lookup"><span data-stu-id="5f2a2-122">However, if the entry has already been approved, the approver is asked to approve the recall and reverse the transactions.</span></span>

1. <span data-ttu-id="5f2a2-123">Siirry kohtaan **Kulut** ja valitse sitten kulujen luettelosta peruutettava kulu.</span><span class="sxs-lookup"><span data-stu-id="5f2a2-123">Go to **Expenses**, and then, in the list of expenses, select the expense to recall.</span></span>
2. <span data-ttu-id="5f2a2-124">Valitse **Peruuta**.</span><span class="sxs-lookup"><span data-stu-id="5f2a2-124">Select **Recall**.</span></span> <span data-ttu-id="5f2a2-125">Jos kulumerkintää ei ole vielä hyväksytty, järjestelmä palauttaa sen heti.</span><span class="sxs-lookup"><span data-stu-id="5f2a2-125">If the expense entry hasn't yet been approved, the system immediately recalls it.</span></span> <span data-ttu-id="5f2a2-126">Jos kulumerkintä on jo hyväksytty, järjestelmä luo palautus pyynnön, joka ilmoittaa hyväksyjälle, että haluat peruuttaa kulun.</span><span class="sxs-lookup"><span data-stu-id="5f2a2-126">If the expense entry has already been approved, a recall request is created to notify the approver that you want to reverse the expense.</span></span> <span data-ttu-id="5f2a2-127">Hyväksyjä vahvistaa, että palautus voidaan tehdä, ja merkintä palautetaan.</span><span class="sxs-lookup"><span data-stu-id="5f2a2-127">The approver will then confirm that the reversal can be done, and the entry will be returned.</span></span>

## <a name="delete-a-basic-expense"></a><span data-ttu-id="5f2a2-128">Peruskulun poistaminen</span><span class="sxs-lookup"><span data-stu-id="5f2a2-128">Delete a basic expense</span></span>

<span data-ttu-id="5f2a2-129">Kulut, joita ei ole vielä lähetetty, voidaan poistaa.</span><span class="sxs-lookup"><span data-stu-id="5f2a2-129">Expenses that haven't yet been submitted can be deleted.</span></span> <span data-ttu-id="5f2a2-130">Jos haluat poistaa jo lähetetyn kulun, sinun täytyy ensin peruuttaa se.</span><span class="sxs-lookup"><span data-stu-id="5f2a2-130">To delete an expense that has already been submitted, you must first recall it.</span></span>

## <a name="see-also"></a><span data-ttu-id="5f2a2-131">Katso myös</span><span class="sxs-lookup"><span data-stu-id="5f2a2-131">See also</span></span>

- [<span data-ttu-id="5f2a2-132">Hyväksyntöjen yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="5f2a2-132">Approvals overview</span></span>](../approvals/approvals-overview.md)
