---
title: Peruuta hyväksytyt aika- tai kulukirjaukset
description: Tässä aiheessa on tietoja aiemmin hyväksytyn aika- tai kulutapahtuman peruuttamisesta.
author: rumant
manager: kfend
ms.service: project-operations
ms.custom: ''
ms.author: rumant
ms.date: 03/08/2019
ms.topic: article
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 1a199985099745b2e62b844ef748ea2031054458
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5283454"
---
# <a name="recall-approved-time-or-expense-entries"></a><span data-ttu-id="ef474-103">Peruuta hyväksytyt aika- tai kulukirjaukset</span><span class="sxs-lookup"><span data-stu-id="ef474-103">Recall approved time or expense entries</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="ef474-104">Projektiryhmän jäsen tai toinen henkilö, joka lähettää aika- tai kulumerkinnän, voi peruuttaa tämän aika- tai kulumerkinnän sen hyväksymisen jälkeen.</span><span class="sxs-lookup"><span data-stu-id="ef474-104">A project team member or an other person who submits a time or expense entry can recall that time or expense entry after it has been approved.</span></span> <span data-ttu-id="ef474-105">Hyväksytyn aika- tai kulumerkinnän peruuttamisprosessissa on kaksi vaihetta:</span><span class="sxs-lookup"><span data-stu-id="ef474-105">The process for recalling an approved time or expense entry has two steps:</span></span>

1. <span data-ttu-id="ef474-106">Lähettäjä pyytää peruuttamista.</span><span class="sxs-lookup"><span data-stu-id="ef474-106">A submitter requests a recall.</span></span>
2. <span data-ttu-id="ef474-107">Hyväksyjä hyväksyy peruutuksen.</span><span class="sxs-lookup"><span data-stu-id="ef474-107">An approver approves the recall.</span></span>

## <a name="request-a-recall"></a><span data-ttu-id="ef474-108">Pyydä peruutusta</span><span class="sxs-lookup"><span data-stu-id="ef474-108">Request a recall</span></span>

<span data-ttu-id="ef474-109">Seuraa näitä vaiheita pyytääksesi hyväksytyn aika- tai kulumerkinnän poistamista.</span><span class="sxs-lookup"><span data-stu-id="ef474-109">Follow these steps to request a recall of an approved time or expense entry.</span></span>

1. <span data-ttu-id="ef474-110">Jos kyseessä on aikamerkintä, siirry kohtaan **Projektit** \> **Oma työ** \> **Aikakirjaus**.</span><span class="sxs-lookup"><span data-stu-id="ef474-110">For time entries, go to **Projects** \> **My Work** \> **Time Entry**.</span></span>

    <span data-ttu-id="ef474-111">-tai-</span><span class="sxs-lookup"><span data-stu-id="ef474-111">–or–</span></span>

    <span data-ttu-id="ef474-112">Jos kyseessä on kulumerkintä, siirry kohtaan **Projektit** \> **Oma työ** \> **Kulut**.</span><span class="sxs-lookup"><span data-stu-id="ef474-112">For expense entries, go to **Projects** \> **My Work** \> **Expenses**.</span></span>

2. <span data-ttu-id="ef474-113">Jos kyseessä on aikakirjaus, valitse kaikki tietyn projektin ja tehtävän yhdistelmän aikamerkinnät.</span><span class="sxs-lookup"><span data-stu-id="ef474-113">For time entries, select all the time entries for a specific combination of a project and a task.</span></span> <span data-ttu-id="ef474-114">Vaihtoehtoisesti voit valita ruudukossa yksittäiset solut tiettynä päivämääränä tiettyä projektia varten.</span><span class="sxs-lookup"><span data-stu-id="ef474-114">Alternatively, in the grid, select the individual cells for time on a specific date for a specific project.</span></span>

    <span data-ttu-id="ef474-115">-tai-</span><span class="sxs-lookup"><span data-stu-id="ef474-115">–or–</span></span>

    <span data-ttu-id="ef474-116">Jos kyseessä on kulutapahtuma, valitse se kulutapahtumarivi, jonka haluat peruuttaa.</span><span class="sxs-lookup"><span data-stu-id="ef474-116">For expense entries, select the row for the expense entry to recall.</span></span>

3. <span data-ttu-id="ef474-117">Valitse **Peruuta**.</span><span class="sxs-lookup"><span data-stu-id="ef474-117">Select **Recall**.</span></span> <span data-ttu-id="ef474-118">Vahvistusvalintaikkuna avautuu.</span><span class="sxs-lookup"><span data-stu-id="ef474-118">A confirmation dialog box appears.</span></span> <span data-ttu-id="ef474-119">Jos valitut aika- ja kulutapahtumat on jo hyväksytty, sinua pyydetään syöttämään peruutuksen syy.</span><span class="sxs-lookup"><span data-stu-id="ef474-119">If the selected time and expense entries were already approved, you're prompted to enter a reason for the recall.</span></span>
4. <span data-ttu-id="ef474-120">Syötä peruutuksen syy ja vahvista sen jälkeen toiminto valitsemalla **OK**.</span><span class="sxs-lookup"><span data-stu-id="ef474-120">Enter a reason for the recall, and then select **OK** to confirm the operation.</span></span> <span data-ttu-id="ef474-121">Järjestelmä lähettää tietueet hyväksyneelle henkilölle pyynnön hyväksyä peruutus.</span><span class="sxs-lookup"><span data-stu-id="ef474-121">The system sends the person who approved the entries a request to approve the recall.</span></span>

> [!NOTE]
> <span data-ttu-id="ef474-122">Vaikka hyväksyttyjä aika- ja kulukirjauksia voidaan peruuttaa, jos hyväksytty aika tai kulu on jo laskutettu asiakkaalta, peruutuspyyntöä ei voi tehdä.</span><span class="sxs-lookup"><span data-stu-id="ef474-122">Although approved time and expense entries can be recalled, if an approved time or expense has already been invoiced to the customer, a recall request can't be created.</span></span> <span data-ttu-id="ef474-123">Käyttäjä, joka yrittää luoda peruutuspyynnön, saa sanoman, jonka mukaan aikaa tai kulua ei voi peruuttaa, koska se on jo laskutettu.</span><span class="sxs-lookup"><span data-stu-id="ef474-123">A user who tries to create a recall request will receive a message that states that the time or expense can't be recalled because it was already invoiced.</span></span>

## <a name="approve-or-reject-a-recall-request"></a><span data-ttu-id="ef474-124">Peruutuspyynnön hyväksyminen tai hylkääminen</span><span class="sxs-lookup"><span data-stu-id="ef474-124">Approve or reject a recall request</span></span>

<span data-ttu-id="ef474-125">Voit hyväksyä tai hylätä peruutuspyynnön seuraavien vaiheiden mukaisesti.</span><span class="sxs-lookup"><span data-stu-id="ef474-125">Follow these steps to approve or reject a recall request.</span></span>

1. <span data-ttu-id="ef474-126">Siirry kohtaan **Projektit** \> **Omat työt** \> **Hyväksynnät**.</span><span class="sxs-lookup"><span data-stu-id="ef474-126">Go to **Projects** \> **My Work** \> **Approvals**.</span></span>
2. <span data-ttu-id="ef474-127">Vaihda **Hyväksynnät** -luettelosivulla näkymäksi **Hyväksyttävät peruutuspyynnöt**.</span><span class="sxs-lookup"><span data-stu-id="ef474-127">On the **Approvals** list page, change the view to **Recall requests for approval**.</span></span> <span data-ttu-id="ef474-128">Näkyviin tulee luettelo lähetetyistä peruutuspyynnöistä.</span><span class="sxs-lookup"><span data-stu-id="ef474-128">A list of submitted recall requests is shown.</span></span>
3. <span data-ttu-id="ef474-129">Valitse vähintään yksi merkintä ja valitse sitten **Hyväksy** tai **Hylkää**.</span><span class="sxs-lookup"><span data-stu-id="ef474-129">Select one or more entries, and then select either **Approve** or **Reject**.</span></span>
4. <span data-ttu-id="ef474-130">Jos valitsit **Hyväksy**, näkyviin tulee varoitussanoma, jossa on selostettu hyväksynnän vaikutus.</span><span class="sxs-lookup"><span data-stu-id="ef474-130">If you selected **Approve**, you receive a warning message that explains the impact of the approval.</span></span> <span data-ttu-id="ef474-131">Vahvista toiminto valitsemalla **OK**.</span><span class="sxs-lookup"><span data-stu-id="ef474-131">Select **OK** to confirm the operation.</span></span> <span data-ttu-id="ef474-132">Peruutuspyyntö on hyväksytty.</span><span class="sxs-lookup"><span data-stu-id="ef474-132">The recall request is approved.</span></span>

    <span data-ttu-id="ef474-133">-tai-</span><span class="sxs-lookup"><span data-stu-id="ef474-133">–or–</span></span>

    <span data-ttu-id="ef474-134">Jos valitsit **Hylkää**, peruutuspyyntö hylätään.</span><span class="sxs-lookup"><span data-stu-id="ef474-134">If you selected **Reject**, the recall request is rejected.</span></span>

> [!NOTE]
> <span data-ttu-id="ef474-135">Kuten peruutusta pyydettäessä, ku peruutus hyväksytään, järjestelmä tarkistaa, onko aika- tai kulumerkinnöissä laskutusaktiviteetteja.</span><span class="sxs-lookup"><span data-stu-id="ef474-135">As when a recall is requested, when a recall is approved, the system checks for any invoicing activity on the time or expense entries.</span></span> <span data-ttu-id="ef474-136">Jos tapahtuma on jo laskutettu tai jos se on luonnoslaskulla, hyväksyjä saa virhesanoman, jonka mukaan ajan tai kulun peruutusta ei voi hyväksyä, koska se on jo laskutettu.</span><span class="sxs-lookup"><span data-stu-id="ef474-136">If an entry was already invoiced, or if it's on a draft invoice, the approver will receive an error message that states that the time or expense can't be approved for recall, because it was already invoiced.</span></span>

## <a name="impact-of-a-recall-request"></a><span data-ttu-id="ef474-137">Peruutuspyynnön vaikutus</span><span class="sxs-lookup"><span data-stu-id="ef474-137">Impact of a recall request</span></span>

<span data-ttu-id="ef474-138">Kun hyväksyntä peruutetaan, siihen liittyy sekä toiminnallisia vaikutuksia että taloudellisia vaikutuksia.</span><span class="sxs-lookup"><span data-stu-id="ef474-138">When an approval is recalled, there is both operational impact and financial impact.</span></span>

### <a name="operational-impact"></a><span data-ttu-id="ef474-139">Toiminnallinen vaikutus</span><span class="sxs-lookup"><span data-stu-id="ef474-139">Operational impact</span></span>

<span data-ttu-id="ef474-140">Jos peruutuspyyntö hyväksytään, hyväksyntätietue merkitään **Hylätyksi**.</span><span class="sxs-lookup"><span data-stu-id="ef474-140">If a recall request is approved, the approval record is marked as **Rejected**.</span></span> <span data-ttu-id="ef474-141">Tapahtuman tilaksi tulee joko **Palautunut** tai **Hylätty** sen mukaan, onko kyseessä aika- vai kulutapahtuma.</span><span class="sxs-lookup"><span data-stu-id="ef474-141">The status of the entry is changed to either **Returned** or **Rejected**, depending on whether it's a time entry or an expense entry.</span></span>

<span data-ttu-id="ef474-142">Projektiryhmän jäsen voi tarkastella tapahtumia, muokata ja lähettää merkintöjä uudelleen tai poistaa tietueita kokonaan.</span><span class="sxs-lookup"><span data-stu-id="ef474-142">The project team member can view entries, edit and then resubmit entries, or delete entries entirely.</span></span>

<span data-ttu-id="ef474-143">Jos peruutuspyyntö hylätään, merkinnän tila säilyy ennallaan **Hyväksyttynä**, eikä projektiryhmän jäsen tai projektin hyväksyjä voi muokata merkintää.</span><span class="sxs-lookup"><span data-stu-id="ef474-143">If a recall request is rejected, the status of the entry remains **Approved**, and the entry can't be edited by the project team member or the approver for the project.</span></span>

### <a name="financial-impact"></a><span data-ttu-id="ef474-144">Taloudellinen vaikutus</span><span class="sxs-lookup"><span data-stu-id="ef474-144">Financial impact</span></span>

<span data-ttu-id="ef474-145">Jos peruutuspyyntö hyväksytään, vastaavat toteutuneet kustannukset ja myynnit päivitetään seuraavalla tavalla:</span><span class="sxs-lookup"><span data-stu-id="ef474-145">If a recall request is approved, the corresponding actuals for cost and sales are updated in the following manner:</span></span>

- <span data-ttu-id="ef474-146">**Oikaisun tila** -kenttä päivittyy **Oikaistuksi**.</span><span class="sxs-lookup"><span data-stu-id="ef474-146">The **Adjustment Status** field is updated to **Adjusted**.</span></span>
- <span data-ttu-id="ef474-147">**Laskutuksen tila** -kenttä päivittyy **Peruutetuksi**.</span><span class="sxs-lookup"><span data-stu-id="ef474-147">The **Billing Status** field is updated to **Canceled**.</span></span>

<span data-ttu-id="ef474-148">Seuraavaksi todellisten arvojen taulukossa luodaan palautusmerkintöjä.</span><span class="sxs-lookup"><span data-stu-id="ef474-148">Next, reversal entries are created in the Actuals table.</span></span> <span data-ttu-id="ef474-149">Peruutusmerkintöjen luomista varten järjestelmä kopioi kenttien arvot alkuperäisistä todellisista arvoista.</span><span class="sxs-lookup"><span data-stu-id="ef474-149">To create reversal entries, the system copies over the field values from the original actuals.</span></span> <span data-ttu-id="ef474-150">Ainoat arvot, joita ei kopioida, ovat määräarvot.</span><span class="sxs-lookup"><span data-stu-id="ef474-150">The only values that aren't copied over are the quantity values.</span></span> <span data-ttu-id="ef474-151">Sen sijaan kyseiset arvot kumotaan.</span><span class="sxs-lookup"><span data-stu-id="ef474-151">These values are reversed instead.</span></span> <span data-ttu-id="ef474-152">Kumottuja todellisia arvoja luodaan sekä **Kustannus**- että **Laskuttamaton myynti** -muotoisille todellisille arvoille.</span><span class="sxs-lookup"><span data-stu-id="ef474-152">Reversed actuals are created for both **Cost** and **Unbilled Sales** actuals.</span></span> <span data-ttu-id="ef474-153">**Oikaisun tila** -kentän arvoksi käänteisissä nykyarvoissa asetetaan **Oikaisukelvoton** ja **Laskutuksen tila** -kentän arvoksi **Peruutettu**.</span><span class="sxs-lookup"><span data-stu-id="ef474-153">The **Adjustment Status** field on the reversed actuals is set to **Unadjustable**, and the **Billing status** field is set to **Canceled**.</span></span> <span data-ttu-id="ef474-154">Näiden muutosten vuoksi projektin kirjatut menot ja tulot eivät enää vastaa summia, joita nämä nykyarvot edustavat.</span><span class="sxs-lookup"><span data-stu-id="ef474-154">Because of these changes, the recorded spending and the revenue backlog on the project will no longer account for the amounts that these actuals represent.</span></span>

<span data-ttu-id="ef474-155">Jos peruutuspyyntö hylätään, projektiin ei liity taloudellista vaikutusta.</span><span class="sxs-lookup"><span data-stu-id="ef474-155">If a recall request is rejected, there is no financial impact on the project.</span></span>

## <a name="changes-to-time-entry-records"></a><span data-ttu-id="ef474-156">Aikamerkintätietueiden muutokset</span><span class="sxs-lookup"><span data-stu-id="ef474-156">Changes to time entry records</span></span>

<span data-ttu-id="ef474-157">Seuraavassa kuvassa näkyvät muutokset, jotka tapahtuvat hyväksytyille aikakirjauksille kun ne peruutetaan.</span><span class="sxs-lookup"><span data-stu-id="ef474-157">The following illustration shows the changes that occur for approved time entries when they are recalled.</span></span>

![Ajan syötön tilasiirtymät](media/TimeEntryStateTransitions.png)

## <a name="changes-to-expense-entry-records"></a><span data-ttu-id="ef474-159">Kulumerkintätietueiden muutokset</span><span class="sxs-lookup"><span data-stu-id="ef474-159">Changes to expense entry records</span></span>

<span data-ttu-id="ef474-160">Seuraavassa kuvassa näkyvät muutokset, jotka tapahtuvat hyväksytyille kulukirjauksille kun ne peruutetaan.</span><span class="sxs-lookup"><span data-stu-id="ef474-160">The following illustration shows the changes that occur for approved expense entries when they are recalled.</span></span>

![Kulujen syötön tilasiirtymät](media/ExpenseEntryStateTransitions.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]