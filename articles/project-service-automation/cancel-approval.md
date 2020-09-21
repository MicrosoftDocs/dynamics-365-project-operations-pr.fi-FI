---
title: Aiemmin hyväksyttyjen aika- ja kulumerkintöjen peruminen
description: Tässä aiheessa on tietoja aiemmin hyväksytyn projektin aika- ja kulutapahtuman perumisesta.
author: rumant
manager: kfend
ms.service: business-applications
ms.custom:
- dyn365-projectservice
ms.date: 03/07/2019
ms.topic: article
ms.prod: ''
ms.technology: Microsoft Dynamics 365 Project Service Automation
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 2fc74aba2a837b7cdff55385ffa20d78c2678bb7
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/24/2020
ms.locfileid: "3751089"
---
# <a name="cancel-previously-approved-time-or-expense-entries"></a><span data-ttu-id="9dc49-103">Aiemmin hyväksyttyjen aika- tai kulumerkintöjen peruminen</span><span class="sxs-lookup"><span data-stu-id="9dc49-103">Cancel previously approved time or expense entries</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="9dc49-104">Dynamics 365 Project Service Automationin viimeisimmässä versiossa hyväksyjät voivat perua aika- tai kulumerkintöjä, jotka he ovat aiemmin hyväksyneet.</span><span class="sxs-lookup"><span data-stu-id="9dc49-104">In the latest version of Dynamics 365 Project Service Automation, approvers can cancel time or expense entries that they previously approved.</span></span>

## <a name="cancel-a-previously-approved-time-or-expense-entry"></a><span data-ttu-id="9dc49-105">Aiemmin hyväksytyn aika- tai kulumerkinnän peruminen</span><span class="sxs-lookup"><span data-stu-id="9dc49-105">Cancel a previously approved time or expense entry</span></span>

<span data-ttu-id="9dc49-106">Seuraa näitä vaiheita peruaksesi aiemmin hyväksymäsi aika- tai kulumerkinnän.</span><span class="sxs-lookup"><span data-stu-id="9dc49-106">Follow these steps to cancel a time or expense entry that you previously approved.</span></span>

1. <span data-ttu-id="9dc49-107">Siirry kohtaan **Projektit** \> **Omat työt** \> **Hyväksynnät**.</span><span class="sxs-lookup"><span data-stu-id="9dc49-107">Go to **Projects** \> **My Work** \> **Approvals**.</span></span>
2. <span data-ttu-id="9dc49-108">Vaihda **Hyväksynnät** -luettelosivulla näkymäksi **Omat aikaisemmat hyväksynnät**.</span><span class="sxs-lookup"><span data-stu-id="9dc49-108">On the **Approvals** list page, change the view to **My past approvals**.</span></span> <span data-ttu-id="9dc49-109">Näkyviin tulee luettelo aiemmin hyväksymistäsi aika- ja kulumerkinnöistä.</span><span class="sxs-lookup"><span data-stu-id="9dc49-109">A list of the time and expense entries that you previously approved is shown.</span></span>
3. <span data-ttu-id="9dc49-110">Valitse vähintään yksi merkintä ja valitse sitten **Peru hyväksyntä**.</span><span class="sxs-lookup"><span data-stu-id="9dc49-110">Select one or more entries, and then select **Cancel approval**.</span></span> <span data-ttu-id="9dc49-111">Näyttöön tulee varoitus.</span><span class="sxs-lookup"><span data-stu-id="9dc49-111">You receive a warning message.</span></span>
4. <span data-ttu-id="9dc49-112">Peru hyväksyntä valitsemalla **OK**.</span><span class="sxs-lookup"><span data-stu-id="9dc49-112">Select **OK** to cancel the approval.</span></span>

## <a name="understand-the-impact-of-canceling-a-time-or-expense-entry-approval"></a><span data-ttu-id="9dc49-113">Aika- tai kulumerkinnän perumisen vaikutukset</span><span class="sxs-lookup"><span data-stu-id="9dc49-113">Understand the impact of canceling a time or expense entry approval</span></span>

<span data-ttu-id="9dc49-114">Kun hyväksyntä perutaan, siihen liittyy sekä toiminnallisia vaikutuksia että taloudellisia vaikutuksia.</span><span class="sxs-lookup"><span data-stu-id="9dc49-114">When an approval is canceled, there is both operational impact and financial impact.</span></span>

### <a name="operational-impact"></a><span data-ttu-id="9dc49-115">Toiminnallinen vaikutus</span><span class="sxs-lookup"><span data-stu-id="9dc49-115">Operational impact</span></span>

<span data-ttu-id="9dc49-116">Kun hyväksyntä perutaan, tietueen tilaksi palautuu toiminnallisella puolella **Luonnos** eikä hyväksyntä enää näy **Omat aikaisemmat hyväksynnät** -näkymässä.</span><span class="sxs-lookup"><span data-stu-id="9dc49-116">On the operations side, when an approval is canceled, the status of the record is reset to **Draft**, and the approval no longer appears in the **My past approvals** view.</span></span> <span data-ttu-id="9dc49-117">Sen sijaan peruttu hyväksyntä tulee näkyviin joko näkymässä **Aikamerkinnät hyväksyttäväksi** tai näkymässä **Kulumerkinnät hyväksyttäväksi** riippuen siitä, oliko kyseessä aika- vai kulumerkintä.</span><span class="sxs-lookup"><span data-stu-id="9dc49-117">Instead, the canceled approval appears in either the **Time entries for approval** view or the **Expense entries for approval** view, depending on whether it was a time entry or an expense entry.</span></span> <span data-ttu-id="9dc49-118">Lisäksi siihen liittyvän aika- tai kulumerkinnän tilaksi vaihtuu **Lähetetty**, jotta liittyvä merkintä on yhdenmukainen niiden hyväksyntöjen kanssa, joiden tila on **Luonnos**.</span><span class="sxs-lookup"><span data-stu-id="9dc49-118">Additionally, the status of the related time or expense entry is changed to **Submitted**, so that the related entry is consistent with approvals that have a status of **Draft**.</span></span>

<span data-ttu-id="9dc49-119">Hyväksyjänä voit muokata joitakin hyväksynnän kenttiä, joiden tilana on **Luonnos**.</span><span class="sxs-lookup"><span data-stu-id="9dc49-119">As an approver, you can edit some of the fields of an approval that has a status of **Draft**.</span></span> <span data-ttu-id="9dc49-120">Näitä kenttiä ovat esimerkiksi **Laskutustyyppi** ja **Aikamerkintöjen laskutettavat tunnit**.</span><span class="sxs-lookup"><span data-stu-id="9dc49-120">These fields include **Billing Type** and **Billable Hours for Time Entries**.</span></span> <span data-ttu-id="9dc49-121">Kun olet tehnyt muutoksia, voit hyväksyä tietueen uudelleen.</span><span class="sxs-lookup"><span data-stu-id="9dc49-121">After you make changes, you can approve the record again.</span></span> <span data-ttu-id="9dc49-122">Voit myös hylätä merkinnän.</span><span class="sxs-lookup"><span data-stu-id="9dc49-122">Alternatively, you can reject the entry.</span></span> <span data-ttu-id="9dc49-123">Jos hylkäät aikamerkinnän, sen tilaksi vaihtuu **Palautettu**.</span><span class="sxs-lookup"><span data-stu-id="9dc49-123">If you reject the approval of a time entry, the status of the entry is changed to **Returned**.</span></span> <span data-ttu-id="9dc49-124">Jos hylkäät kulumerkinnän, sen tilaksi vaihtuu **Hylätty**.</span><span class="sxs-lookup"><span data-stu-id="9dc49-124">If you reject the approval of an expense entry, the status is changed to **Rejected**.</span></span> <span data-ttu-id="9dc49-125">Toiminnalliselta kannalta palautetut ja hylätyt merkinnät toimivat samalla tavalla kuin merkintä, jonka tilana on **Luonnos**.</span><span class="sxs-lookup"><span data-stu-id="9dc49-125">Functionally, both returned and rejected entries behave the same as an entry that has a status of **Draft**.</span></span> <span data-ttu-id="9dc49-126">Projektiryhmän jäsen voi joko tehdä tarvittavat muutokset merkintään ja lähettää sen uudelleen hyväksyttäväksi tai poistaa merkinnän kokonaan.</span><span class="sxs-lookup"><span data-stu-id="9dc49-126">A project team member can either make any required changes to the entry and then resubmit it for approval, or delete the entry entirely.</span></span>

### <a name="financial-impact"></a><span data-ttu-id="9dc49-127">Taloudellinen vaikutus</span><span class="sxs-lookup"><span data-stu-id="9dc49-127">Financial impact</span></span>

<span data-ttu-id="9dc49-128">Hyväksynnän perumisella on myös taloudellisia vaikutuksia projektiin.</span><span class="sxs-lookup"><span data-stu-id="9dc49-128">A project is also affected financially when an approval is canceled.</span></span> <span data-ttu-id="9dc49-129">Aluksi vastaavat toteutuneet kustannukset ja myynnit päivitetään seuraavalla tavalla:</span><span class="sxs-lookup"><span data-stu-id="9dc49-129">First, the corresponding actuals for cost and sales are updated in the following manner:</span></span>

- <span data-ttu-id="9dc49-130">Oikaisun tilaksi määritetään **Oikaistu**.</span><span class="sxs-lookup"><span data-stu-id="9dc49-130">The adjustment status is set to **Adjusted**.</span></span>
- <span data-ttu-id="9dc49-131">Laskutustilaksi määritetään **Peruttu**.</span><span class="sxs-lookup"><span data-stu-id="9dc49-131">The billing status is set to **Canceled**.</span></span>

<span data-ttu-id="9dc49-132">Seuraavaksi todellisten arvojen taulukossa luodaan palautusmerkintöjä.</span><span class="sxs-lookup"><span data-stu-id="9dc49-132">Next, reversal entries are created in the Actuals table.</span></span> <span data-ttu-id="9dc49-133">Peruutusmerkintöjen luomista varten järjestelmä kopioi kenttien arvot alkuperäisistä todellisista arvoista.</span><span class="sxs-lookup"><span data-stu-id="9dc49-133">To create reversal entries, the system copies over the field values from the original actuals.</span></span> <span data-ttu-id="9dc49-134">Ainoat arvot, joita ei kopioida, ovat määräarvot.</span><span class="sxs-lookup"><span data-stu-id="9dc49-134">The only values that aren't copied over are the quantity values.</span></span> <span data-ttu-id="9dc49-135">Sen sijaan kyseiset arvot kumotaan.</span><span class="sxs-lookup"><span data-stu-id="9dc49-135">These values are reversed instead.</span></span> <span data-ttu-id="9dc49-136">Kumottuja todellisia arvoja luodaan sekä **Kustannus**- että **Laskuttamaton myynti** -muotoisille todellisille arvoille.</span><span class="sxs-lookup"><span data-stu-id="9dc49-136">Reversed actuals are created for both **Cost** and **Unbilled Sales** actuals.</span></span> <span data-ttu-id="9dc49-137">**Oikaisun tila** -kentän arvoksi kumotuissa todellisissa arvoissa asetetaan **Oikaisukelvoton** ja laskutuksen tilaksi määritetään **Peruttu**.</span><span class="sxs-lookup"><span data-stu-id="9dc49-137">The **Adjustment Status** field on the reversed actuals is set to **Unadjustable**, and the billing status is set to **Canceled**.</span></span>

<span data-ttu-id="9dc49-138">Kun nämä muutokset on tehty, projektissa kulutetuksi kirjattu summa ja tulot eivät enää vastaa summia, joita nämä todelliset arvot edustavat.</span><span class="sxs-lookup"><span data-stu-id="9dc49-138">After these changes are made, the amount that is recorded as spent on the project and the revenue backlog on the project will longer account for the amounts that these actuals represent.</span></span>
