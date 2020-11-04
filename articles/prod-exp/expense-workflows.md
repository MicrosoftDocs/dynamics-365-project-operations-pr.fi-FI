---
title: Kulujen hallinnan työnkulkujen määrittäminen
description: Voit määrittää matka- ja kuluasiakirjojen tarkistuksen ja hyväksynnän työnkulkuprosessin.
author: ShylaThompson
manager: AnnBe
ms.date: 09/13/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WorkflowtableListPageRnr
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0af23ed2cf172e4c90de72f5db389c349303c039
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/16/2020
ms.locfileid: "4075502"
---
# <a name="set-up-expense-management-workflows"></a><span data-ttu-id="5ba66-103">Kulujen hallinnan työnkulkujen määrittäminen</span><span class="sxs-lookup"><span data-stu-id="5ba66-103">Set up Expense management workflows</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5ba66-104">Voit määrittää työnkulkuprosessin, jota käytetään matka- ja kuluasiakirjojen tarkistukseen ja hyväksyntään.</span><span class="sxs-lookup"><span data-stu-id="5ba66-104">You can set up a workflow process that is used to review and approve travel and expense documents.</span></span> <span data-ttu-id="5ba66-105">Asiakirjat, joille työnkulut voidaan määritellä, sisältävät kuluraportit, matkapyynnöt ja käteisennakkopyynnöt.</span><span class="sxs-lookup"><span data-stu-id="5ba66-105">The documents for which workflows can be defined include expense reports, travel requisitions, and cash advance requests.</span></span>

<span data-ttu-id="5ba66-106">Työnkulku edustaa liiketoimintaprosessia.</span><span class="sxs-lookup"><span data-stu-id="5ba66-106">A workflow represents a business process.</span></span> <span data-ttu-id="5ba66-107">Se määrittää, miten asiakirja kuljetetaan järjestelmässä, ja osoittaa, kenen on suoritettava tehtävä tai hyväksyttävä asiakirja.</span><span class="sxs-lookup"><span data-stu-id="5ba66-107">It defines how a document flows through the system and indicates who must complete a task or approve a document.</span></span> <span data-ttu-id="5ba66-108">Työnkulkujärjestelmän käyttäminen tuo seuraavat hyödyt organisaatiolle:</span><span class="sxs-lookup"><span data-stu-id="5ba66-108">There are several benefits of using the workflow system in your organization:</span></span>

-   <span data-ttu-id="5ba66-109">**Yhtenäiset prosessit** — Voit määrittää kuluraportin tietyille asiakirjoille, kuten ostoehdotuksille ja kuluraporteille.</span><span class="sxs-lookup"><span data-stu-id="5ba66-109">**Consistent processes** — You can define the approval process for specific documents, such as purchase requisitions and expense reports.</span></span> <span data-ttu-id="5ba66-110">Työnkulkujärjestelmä auttaa varmistamaan, että asiakirjat käsitellään ja hyväksytään yhdenmukaisesti ja tehokkaasti.</span><span class="sxs-lookup"><span data-stu-id="5ba66-110">Using the workflow system helps to ensure that documents are processed and approved in a consistent and efficient manner.</span></span>

-   <span data-ttu-id="5ba66-111">Prosessin näkyvyys — Voit seurata tietyn työnkulun esiintymän tila-, historia- ja suorituskykymittareita.</span><span class="sxs-lookup"><span data-stu-id="5ba66-111">Process visibility — You can track the status, history, and performance metrics of a specific workflow instance.</span></span> <span data-ttu-id="5ba66-112">Tämän avulla voit määrittää, onko työnkulkuun tehtävä muutoksia tehokkuuden parantamiseksi.</span><span class="sxs-lookup"><span data-stu-id="5ba66-112">This helps you determine whether changes should be made to the workflow to improve efficiency.</span></span>

-   <span data-ttu-id="5ba66-113">Keskitetty työluettelo — Käyttäjät voivat tarkastella keskitettyä työluetteloa ja tarkastella heille määritettyjä työnkulun tehtäviä ja hyväksyntöjä.</span><span class="sxs-lookup"><span data-stu-id="5ba66-113">Centralized work list — Users can view a centralized work list to view the workflow tasks and approvals assigned to them.</span></span> 

<span data-ttu-id="5ba66-114">**Luotavissa olevat työnkulutyypit**</span><span class="sxs-lookup"><span data-stu-id="5ba66-114">**The types of workflows you can create**</span></span>

<span data-ttu-id="5ba66-115">Seuraavassa taulukossa on esitetty työnkulkutyypit, jotka **Kulun** avulla voi luoda.</span><span class="sxs-lookup"><span data-stu-id="5ba66-115">The following table lists the types of workflows that you can create in **Expense**.</span></span>


|              <span data-ttu-id="5ba66-116"><strong>Tyyppi</strong></span><span class="sxs-lookup"><span data-stu-id="5ba66-116"><strong>Type</strong></span></span>              |                   <span data-ttu-id="5ba66-117"><strong>Tämän tyypin avulla voit</strong></span><span class="sxs-lookup"><span data-stu-id="5ba66-117"><strong>Use this type to</strong></span></span>                   |
|-------------------------------------------------|-----------------------------------------------------------------------|
|         <span data-ttu-id="5ba66-118"><strong>Kuluraportti</strong></span><span class="sxs-lookup"><span data-stu-id="5ba66-118"><strong>Expense report</strong></span></span>         |            <span data-ttu-id="5ba66-119">Luo kuluraporttien hyväksyntätyönkulkuja.</span><span class="sxs-lookup"><span data-stu-id="5ba66-119">Create approval workflows for expense reports.</span></span>             |
|  <span data-ttu-id="5ba66-120"><strong>Kuluraportin automaattinen kirjaaminen</strong></span><span class="sxs-lookup"><span data-stu-id="5ba66-120"><strong>Expense report auto posting</strong></span></span>   |        <span data-ttu-id="5ba66-121">Luo työnkulkujen automaattinen kirjaaminen kuluraportteihin.</span><span class="sxs-lookup"><span data-stu-id="5ba66-121">Create automatic posting workflows for expense reports.</span></span>        |
|       <span data-ttu-id="5ba66-122"><strong>Kulurivin nimike</strong></span><span class="sxs-lookup"><span data-stu-id="5ba66-122"><strong>Expense line item</strong></span></span>        |     <span data-ttu-id="5ba66-123">Luo kuluraporttien rivinimikkeiden hyväksyntätyönkulkuja.</span><span class="sxs-lookup"><span data-stu-id="5ba66-123">Create approval workflows for line items on expense reports.</span></span>      |
| <span data-ttu-id="5ba66-124"><strong>Kulun rivinimikkeen automaattinen kirjaaminen</strong></span><span class="sxs-lookup"><span data-stu-id="5ba66-124"><strong>Expense line item auto posting</strong></span></span> | <span data-ttu-id="5ba66-125">Luo kuluraporttien rivinimikkeiden työnkulkujen automaattinen kirjaaminen.</span><span class="sxs-lookup"><span data-stu-id="5ba66-125">Create automatic posting workflows for line items on expense reports.</span></span> |
|       <span data-ttu-id="5ba66-126"><strong>Matkustusehdotus</strong></span><span class="sxs-lookup"><span data-stu-id="5ba66-126"><strong>Travel requisition</strong></span></span>       |          <span data-ttu-id="5ba66-127">Luo matkaehdotusten hyväksyntätyönkulkuja.</span><span class="sxs-lookup"><span data-stu-id="5ba66-127">Create approval workflows for travel requisitions.</span></span>           |
|      <span data-ttu-id="5ba66-128"><strong>Käteisennakkopyyntö</strong></span><span class="sxs-lookup"><span data-stu-id="5ba66-128"><strong>Cash advance request</strong></span></span>      |         <span data-ttu-id="5ba66-129">Luo hyväksyntätyönkulut käteisennakkopyynnöille.</span><span class="sxs-lookup"><span data-stu-id="5ba66-129">Create approval workflows for cash advance requests.</span></span>          |
|        <span data-ttu-id="5ba66-130"><strong>ALV:n palautus</strong></span><span class="sxs-lookup"><span data-stu-id="5ba66-130"><strong>VAT tax recovery</strong></span></span>        | <span data-ttu-id="5ba66-131">Voit luoda hyväksyntätyönkulkuja arvonlisäveron palautusta varten.</span><span class="sxs-lookup"><span data-stu-id="5ba66-131">Create approval workflows for the recovery of value-added tax (VAT).</span></span>  |

