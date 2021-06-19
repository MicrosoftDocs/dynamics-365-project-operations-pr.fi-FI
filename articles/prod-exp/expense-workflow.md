---
title: Kulujen hallinnan työnkulku
description: Tässä aiheessa kerrotaan, miten voit käyttää työnkulkujärjestelmää Microsoft Dynamics 365 Finance -järjestelmässä ja määrittää kuluraporttien tarkistusprosessin kulunhallinnassa.
author: ShylaThompson
ms.date: 09/13/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WorkflowtableListPageRnr
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 51ac2712f62d5c5d85b21c0ea929517ccb893bca
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/10/2021
ms.locfileid: "6005202"
---
# <a name="expense-management-workflow"></a><span data-ttu-id="e1b74-103">Kulujen hallinnan työnkulku</span><span class="sxs-lookup"><span data-stu-id="e1b74-103">Expense management workflow</span></span>

<span data-ttu-id="e1b74-104">Voit käyttää työnkulkujärjestelmää määrittääksesi kuluraporttien tarkistusprosessin kulunhallinnassa.</span><span class="sxs-lookup"><span data-stu-id="e1b74-104">You can use the workflow system to set up a review process for expense reports in Expense management.</span></span> <span data-ttu-id="e1b74-105">Voit määrittää työnkulun, joka määrittää seuraavia ehtoja käyttäen, kuka hyväksyy kuluraportit:</span><span class="sxs-lookup"><span data-stu-id="e1b74-105">You can set up a workflow that uses the following criteria to determine who approves expense reports:</span></span>

- <span data-ttu-id="e1b74-106">Työntekijöiden raportointihierarkia ja valmiit hyväksyntärajat</span><span class="sxs-lookup"><span data-stu-id="e1b74-106">The employee reporting hierarchy and predefined approval limits</span></span>
- <span data-ttu-id="e1b74-107">Monitasoinen hyväksyntä, joka tukee väliaikaisia hyväksyjiä ja lopullista hyväksyjää</span><span class="sxs-lookup"><span data-stu-id="e1b74-107">Multi-level approval that supports interim approvers and a final approver</span></span>
- <span data-ttu-id="e1b74-108">Taloushallinnon dimensiot ja projektivastuu</span><span class="sxs-lookup"><span data-stu-id="e1b74-108">Financial dimensions and project responsibility</span></span>
- <span data-ttu-id="e1b74-109">Delegointi tietyille käyttäjille tai käyttäjäryhmille</span><span class="sxs-lookup"><span data-stu-id="e1b74-109">Assignment to specific users or user groups</span></span>

<span data-ttu-id="e1b74-110">Työnkulun hyväksyntöjä voi luoda kuluraportteja, matkustusehdotuksia, käteisennakkoja ja arvonlisäveroa (ALV) varten.</span><span class="sxs-lookup"><span data-stu-id="e1b74-110">Workflow approvals can be created for expense reports, travel requisitions, cash advances, and value-added tax (VAT) recovery.</span></span>

<span data-ttu-id="e1b74-111">**Esimerkki**</span><span class="sxs-lookup"><span data-stu-id="e1b74-111">**Example**</span></span>

<span data-ttu-id="e1b74-112">Seuraava prosessi on esimerkki kuluraportin kulunhallinnan työnkulusta.</span><span class="sxs-lookup"><span data-stu-id="e1b74-112">The following process is an example of the expense management workflow for an expense report.</span></span>

1. <span data-ttu-id="e1b74-113">Työntekijä luo ja tallentaa kuluraportin.</span><span class="sxs-lookup"><span data-stu-id="e1b74-113">An employee creates and saves an expense report.</span></span>
2. <span data-ttu-id="e1b74-114">Työntekijä lähettää kuluraportin hyväksyttäväksi.</span><span class="sxs-lookup"><span data-stu-id="e1b74-114">The employee submits the expense report for approval.</span></span> <span data-ttu-id="e1b74-115">Hyväksyjä tunnistetaan työnkulun määrittämisen yhteydessä määritettyjen sääntöjen perusteella.</span><span class="sxs-lookup"><span data-stu-id="e1b74-115">The approver is identified based on the rules that were defined when the workflow was set up.</span></span>
3. <span data-ttu-id="e1b74-116">Hyväksyjä saa ilmoituksen siitä, että kuluraportti on valmis hyväksyttäväksi.</span><span class="sxs-lookup"><span data-stu-id="e1b74-116">The approver receives a notification that an expense report is ready for approval.</span></span> <span data-ttu-id="e1b74-117">Hyväksyjä tarkistaa kuluraportin ja varmistaa, että seuraavat ehdot täyttyvät:</span><span class="sxs-lookup"><span data-stu-id="e1b74-117">The approver reviews the expense report and verifies that the following conditions are met:</span></span>

    - <span data-ttu-id="e1b74-118">Kulut eivät riko mitään kulukäytäntöjä.</span><span class="sxs-lookup"><span data-stu-id="e1b74-118">The expenses don't violate any expense policies.</span></span> <span data-ttu-id="e1b74-119">Jos kulu rikkoo käytäntöä, hyväksyjä tarkistaa, että kuluraportti sisältää kelvollisen liiketoimintaperusteen.</span><span class="sxs-lookup"><span data-stu-id="e1b74-119">If an expense violates a policy, the approver verifies that the expense report includes a valid business justification.</span></span>
    - <span data-ttu-id="e1b74-120">Sähköiset kuitit on liitetty kuluraporttiin.</span><span class="sxs-lookup"><span data-stu-id="e1b74-120">Electronic receipts are attached to the expense report.</span></span>

4. <span data-ttu-id="e1b74-121">Hyväksyjä hyväksyy kuluraportin.</span><span class="sxs-lookup"><span data-stu-id="e1b74-121">The approver approves the expense report.</span></span>
5. <span data-ttu-id="e1b74-122">Kuluraportti delegoidaan ostoreskontran koordinaattorille kirjausta varten.</span><span class="sxs-lookup"><span data-stu-id="e1b74-122">The expense report is assigned to the Accounts payable coordinator for posting.</span></span>
6. <span data-ttu-id="e1b74-123">Jokin seuraavista vaiheista tapahtuu sen mukaan, onko automaattinen kirjaaminen määritetty:</span><span class="sxs-lookup"><span data-stu-id="e1b74-123">One of the following steps occurs, depending on whether automatic posting is configured:</span></span>

    - <span data-ttu-id="e1b74-124">Jos automaattinen kirjaus on määritetty, kuluraportti käsitellään maksua varten ja kuluraportin tila päivittyy.</span><span class="sxs-lookup"><span data-stu-id="e1b74-124">If automatic posting is configured, the expense report is processed for payment, and the status of the expense report is updated.</span></span>
    - <span data-ttu-id="e1b74-125">Jos automaattista kirjausta ei määritetä, ostoreskontrakoordinaattori tarkistaa, että kaikki alkuperäiset kuitit on lähetetty ja että vastaanotot on kohdistettu kuluraportin kulujen kanssa.</span><span class="sxs-lookup"><span data-stu-id="e1b74-125">If automatic posting isn't configured, the Accounts payable coordinator verifies that all original receipts have been submitted, and that the receipts are aligned with the expenses on the expense report.</span></span> <span data-ttu-id="e1b74-126">Kaikki kuluraporttiin kirjoitetut verokoodit on myös tarkistettava oikeiksi.</span><span class="sxs-lookup"><span data-stu-id="e1b74-126">All tax codes that are entered on the expense report must also be verified as correct.</span></span>

<span data-ttu-id="e1b74-127">Kun nämä vaatimukset on tarkistettu, kuluraportti kirjataan.</span><span class="sxs-lookup"><span data-stu-id="e1b74-127">After these requirements are verified, the expense report is posted.</span></span>

<span data-ttu-id="e1b74-128">Kun kuluraportti on kirjattu, maksu on sallittu kuluraportille ja työntekijälle hyvitetään.</span><span class="sxs-lookup"><span data-stu-id="e1b74-128">After the expense report is posted, payment is authorized for the expense report, and the employee is reimbursed.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]