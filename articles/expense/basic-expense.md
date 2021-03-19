---
title: Kulun merkintä (lite)
description: Tässä aiheessa on tietoja siitä, miten voit käsitellä kulumerkintöjä lite-ympäristössä.
author: stsporen
manager: AnnBe
ms.date: 11/19/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 539d0ba6be6f49a6f0509595a0776ef67135496d
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5276749"
---
# <a name="expense-entry-lite"></a><span data-ttu-id="589a3-103">Kulun merkintä (lite)</span><span class="sxs-lookup"><span data-stu-id="589a3-103">Expense entry (lite)</span></span>

<span data-ttu-id="589a3-104">_**Käytetään:** Lite-käyttöönotto – kauppa proformalaskutukseen_</span><span class="sxs-lookup"><span data-stu-id="589a3-104">_**Applies to:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="589a3-105">Basic- tai Lite-kulujen hallinta on mahdollisuus tallentaa yksinkertaisia kuluja.</span><span class="sxs-lookup"><span data-stu-id="589a3-105">Basic, or lite, expense management is the capability to record simple expenses.</span></span> <span data-ttu-id="589a3-106">Voit kirjata kuluja projektiin, minkä jälkeen projektin hyväksyjä tarkistaa ne ja hyväksyy ne.</span><span class="sxs-lookup"><span data-stu-id="589a3-106">You can record expenses against a project, and then the project approver will review and approve them.</span></span>

<span data-ttu-id="589a3-107">Lisätietoja kuluominaisuuksista Dynamics 365 Project Operationsissa on aiheessa [Kulujen yleiskatsaus](expense-overview.md).</span><span class="sxs-lookup"><span data-stu-id="589a3-107">For more information about expense capabilities in Dynamics 365 Project Operations, see [Expense overview](expense-overview.md).</span></span>

## <a name="capture-a-basic-expense"></a><span data-ttu-id="589a3-108">Peruskulun sieppaaminen</span><span class="sxs-lookup"><span data-stu-id="589a3-108">Capture a basic expense</span></span>

<span data-ttu-id="589a3-109">Voit tallentaa kulut, jotta voit lähettää ne hyväksyjälle.</span><span class="sxs-lookup"><span data-stu-id="589a3-109">You can capture your expenses so that you can submit them to the approver.</span></span>

1. <span data-ttu-id="589a3-110">Siirry kohtaan **Kulut** ja valitse **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="589a3-110">Go to **Expenses**, and select **New**.</span></span>
2. <span data-ttu-id="589a3-111">Kirjoita **Uusi kulu** -sivulla pakolliset kulutiedot ja valitse sitten **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="589a3-111">On the **New Expense** page, enter the required expense information, and then select **Save**.</span></span>

## <a name="submit-a-basic-expense"></a><span data-ttu-id="589a3-112">Peruskulun lähettäminen</span><span class="sxs-lookup"><span data-stu-id="589a3-112">Submit a basic expense</span></span>

<span data-ttu-id="589a3-113">Kun olet lopettanut kaikkien kulujen tallentamisen ja olet valmis siirtymään hyväksymisvaiheeseen, sinun täytyy lähettää ne.</span><span class="sxs-lookup"><span data-stu-id="589a3-113">After you've finished capturing all your expenses, and you're ready to have them approved, you must submit them.</span></span>

1. <span data-ttu-id="589a3-114">Siirry kohtaan **Kulut** ja valitse kulu.</span><span class="sxs-lookup"><span data-stu-id="589a3-114">Go to **Expenses**, and select an expense.</span></span> <span data-ttu-id="589a3-115">Voit myös valita kaikki kulut käyttämällä otsikon valintaruutua.</span><span class="sxs-lookup"><span data-stu-id="589a3-115">Or, select all the expenses by using the check box on the header.</span></span>
2. <span data-ttu-id="589a3-116">Valitse **Lähetä**.</span><span class="sxs-lookup"><span data-stu-id="589a3-116">Select **Submit**.</span></span> <span data-ttu-id="589a3-117">Järjestelmä käsittelee valitut tapahtumat ja luo sitten kulun hyväksyntäpyynnöt.</span><span class="sxs-lookup"><span data-stu-id="589a3-117">The system processes the selected entries and then creates expense approval requests.</span></span>

## <a name="add-an-attachment"></a><span data-ttu-id="589a3-118">Lisää liite</span><span class="sxs-lookup"><span data-stu-id="589a3-118">Add an attachment</span></span>

<span data-ttu-id="589a3-119">Sinun on ehkä annettava hyväksyjälle lisäasiakirjoja kuluistasi.</span><span class="sxs-lookup"><span data-stu-id="589a3-119">You may have to provide the approver with additional documentation about your expense.</span></span> <span data-ttu-id="589a3-120">Voit liittää kuitin kulutapahtuman aikajanaan.</span><span class="sxs-lookup"><span data-stu-id="589a3-120">You can attach a receipt in the timeline of the expense entry.</span></span> <span data-ttu-id="589a3-121">Valitse **Muokkaa** ja sitten **Aikajana**-osassa paperiliitinkuvake kuittisi liittämiseksi.</span><span class="sxs-lookup"><span data-stu-id="589a3-121">Select **Edit** and in the **Timeline** section, and then select the paperclip icon to attach your receipt.</span></span>

## <a name="recall-a-basic-expense"></a><span data-ttu-id="589a3-122">Peruskulun peruttaaminen</span><span class="sxs-lookup"><span data-stu-id="589a3-122">Recall a basic expense</span></span>

<span data-ttu-id="589a3-123">Kun lähetät kulun vahingossa, voit peruuttaa sen.</span><span class="sxs-lookup"><span data-stu-id="589a3-123">When you submit an expense by mistake, you can recall it.</span></span> <span data-ttu-id="589a3-124">Kulumerkinnän peruutuksen edellyttämä aika määräytyy sen hyväksyntävaiheen mukaan.</span><span class="sxs-lookup"><span data-stu-id="589a3-124">The time that is required to recall an expense entry depends on its approval stage.</span></span>  <span data-ttu-id="589a3-125">Jos hyväksyjä ei ole vielä hyväksynyt merkintää, peruuttaminen voi tapahtua heti.</span><span class="sxs-lookup"><span data-stu-id="589a3-125">If the approver hasn't yet approved the entry, the recall can occur immediately.</span></span> <span data-ttu-id="589a3-126">Jos tapahtuma on kuitenkin jo hyväksytty, hyväksyjää pyydetään hyväksymään peruutus ja peruuttamaan tapahtumat.</span><span class="sxs-lookup"><span data-stu-id="589a3-126">However, if the entry has already been approved, the approver is asked to approve the recall and reverse the transactions.</span></span>

1. <span data-ttu-id="589a3-127">Siirry kohtaan **Kulut** ja valitse sitten kulujen luettelosta peruutettava kulu.</span><span class="sxs-lookup"><span data-stu-id="589a3-127">Go to **Expenses**, and then, in the list of expenses, select the expense to recall.</span></span>
2. <span data-ttu-id="589a3-128">Valitse **Peruuta**.</span><span class="sxs-lookup"><span data-stu-id="589a3-128">Select **Recall**.</span></span> <span data-ttu-id="589a3-129">Jos kulumerkintää ei ole vielä hyväksytty, järjestelmä palauttaa sen heti.</span><span class="sxs-lookup"><span data-stu-id="589a3-129">If the expense entry hasn't yet been approved, the system immediately recalls it.</span></span> <span data-ttu-id="589a3-130">Jos kulumerkintä on jo hyväksytty, järjestelmä luo palautus pyynnön, joka ilmoittaa hyväksyjälle, että haluat peruuttaa kulun.</span><span class="sxs-lookup"><span data-stu-id="589a3-130">If the expense entry has already been approved, a recall request is created to notify the approver that you want to reverse the expense.</span></span> <span data-ttu-id="589a3-131">Hyväksyjä vahvistaa, että palautus voidaan tehdä, ja merkintä palautetaan.</span><span class="sxs-lookup"><span data-stu-id="589a3-131">The approver will then confirm that the reversal can be done, and the entry will be returned.</span></span>

## <a name="delete-a-basic-expense"></a><span data-ttu-id="589a3-132">Peruskulun poistaminen</span><span class="sxs-lookup"><span data-stu-id="589a3-132">Delete a basic expense</span></span>

<span data-ttu-id="589a3-133">Kulut, joita ei ole vielä lähetetty, voidaan poistaa.</span><span class="sxs-lookup"><span data-stu-id="589a3-133">Expenses that haven't yet been submitted can be deleted.</span></span> <span data-ttu-id="589a3-134">Jos haluat poistaa jo lähetetyn kulun, sinun täytyy ensin peruuttaa se.</span><span class="sxs-lookup"><span data-stu-id="589a3-134">To delete an expense that has already been submitted, you must first recall it.</span></span>

## <a name="see-also"></a><span data-ttu-id="589a3-135">Katso myös</span><span class="sxs-lookup"><span data-stu-id="589a3-135">See also</span></span>

- [<span data-ttu-id="589a3-136">Hyväksyntöjen yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="589a3-136">Approvals overview</span></span>](../approvals/approvals-overview.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]