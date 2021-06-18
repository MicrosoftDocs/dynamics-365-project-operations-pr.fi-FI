---
title: Kulujen hallinnan työnkulkujen määrittäminen
description: Voit määrittää työnkulkuprosessin, jota käytetään matka- ja kuluasiakirjojen tarkistukseen ja hyväksyntään.
author: suvaidya
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: ''
ms.author: shylaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: aab6e18d1ddcffa57cf7cd4cb09eec5a4b89c0fd
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/10/2021
ms.locfileid: "6001017"
---
# <a name="set-up-workflows-for-expense-management"></a><span data-ttu-id="49d52-103">Kulujen hallinnan työnkulkujen määrittäminen</span><span class="sxs-lookup"><span data-stu-id="49d52-103">Set up workflows for Expense management</span></span>

<span data-ttu-id="49d52-104">_**Koskee:** Project Operationsin resurssiin / muuhun kuin resurssiin perustuvia skenaarioita, Lite-käyttöönotto-kaupasta proformalaskutukseen_</span><span class="sxs-lookup"><span data-stu-id="49d52-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="49d52-105">Voit määrittää matka- ja kuluasiakirjojen tarkistuksen ja hyväksynnän työnkulkuprosessin.</span><span class="sxs-lookup"><span data-stu-id="49d52-105">You can set up a workflow process to review and approve travel and expense documents.</span></span> <span data-ttu-id="49d52-106">Voit määrittää kuluraporttien, matkustusehdotusten ja käteisennakkopyyntöjen työnkulut.</span><span class="sxs-lookup"><span data-stu-id="49d52-106">You can define workflows for expense reports, travel requisitions, and cash advance requests.</span></span>

<span data-ttu-id="49d52-107">Työn kulku edustaa liiketoimintaprosessia ja määrittää, miten asiakirja siirtyy järjestelmässä.</span><span class="sxs-lookup"><span data-stu-id="49d52-107">A workflow represents a business process and defines how a document flows through the system.</span></span> <span data-ttu-id="49d52-108">Työnkulku tarkoittaa myös sitä, kenen on suoritettava tehtävä tai hyväksyttävä asiakirja.</span><span class="sxs-lookup"><span data-stu-id="49d52-108">The workflow also indicates who must complete a task or approve a document.</span></span> <span data-ttu-id="49d52-109">Työnkulkujärjestelmän käyttäminen tuo seuraavat hyödyt organisaatiolle:</span><span class="sxs-lookup"><span data-stu-id="49d52-109">There are several benefits of using the workflow system in your organization:</span></span>

- <span data-ttu-id="49d52-110">**Yhtenäiset prosessit**: Voit määrittää kuluraportin tietyille asiakirjoille, kuten ostoehdotuksille ja kuluraporteille.</span><span class="sxs-lookup"><span data-stu-id="49d52-110">**Consistent processes**: You can define the approval process for specific documents, such as purchase requisitions and expense reports.</span></span> <span data-ttu-id="49d52-111">Työnkulkujärjestelmän avulla varmistat, että asiakirjat käsitellään ja hyväksytään yhdenmukaisesti ja tehokkaasti.</span><span class="sxs-lookup"><span data-stu-id="49d52-111">Using the workflow system helps ensure that documents are processed and approved in a consistent and efficient manner.</span></span>
- <span data-ttu-id="49d52-112">**Prosessin näkyvyys**: Voit seurata tietyn työnkulun esiintymän tila-, historia- ja suorituskykymittareita.</span><span class="sxs-lookup"><span data-stu-id="49d52-112">**Process visibility**: You can track the status, history, and performance metrics of a specific workflow instance.</span></span> <span data-ttu-id="49d52-113">Tämän avulla voit määrittää, onko työnkulkuun tehtävä muutoksia tehokkuuden parantamiseksi.</span><span class="sxs-lookup"><span data-stu-id="49d52-113">This helps you determine whether changes should be made to the workflow to improve efficiency.</span></span>
- <span data-ttu-id="49d52-114">**Keskitetty työluettelo**: Käyttäjät voivat tarkastella keskitettyä työluetteloa ja tarkastella heille määritettyjä työnkulun tehtäviä ja hyväksyntöjä.</span><span class="sxs-lookup"><span data-stu-id="49d52-114">**Centralized work list**: Users can view a centralized work list to view the workflow tasks and approvals assigned to them.</span></span> 

## <a name="workflow-types"></a><span data-ttu-id="49d52-115">Työnkulkutyypit</span><span class="sxs-lookup"><span data-stu-id="49d52-115">Workflow types</span></span>

<span data-ttu-id="49d52-116">Seuraavassa taulukossa on esitetty työnkulkutyypit, jotka **kulun hallinnan** avulla voi luoda.</span><span class="sxs-lookup"><span data-stu-id="49d52-116">The following table lists the types of workflows that you can create in **Expense Management**.</span></span>


|              <span data-ttu-id="49d52-117"><strong>Tyyppi</strong></span><span class="sxs-lookup"><span data-stu-id="49d52-117"><strong>Type</strong></span></span>              |                   <span data-ttu-id="49d52-118"><strong>Tämän tyypin avulla voit</strong></span><span class="sxs-lookup"><span data-stu-id="49d52-118"><strong>Use this type to</strong></span></span>                   |
|-------------------------------------------------|-----------------------------------------------------------------------|
|   <span data-ttu-id="49d52-119"><strong>Kuluraportin automaattinen hyväksyntä</strong></span><span class="sxs-lookup"><span data-stu-id="49d52-119"><strong>Expense report auto approval</strong></span></span> |            <span data-ttu-id="49d52-120">Luo kuluraporttien hyväksyntätyönkulkuja.</span><span class="sxs-lookup"><span data-stu-id="49d52-120">Create approval workflows for expense reports.</span></span>             |
|  <span data-ttu-id="49d52-121"><strong>Kuluraportin automaattinen kirjaaminen</strong></span><span class="sxs-lookup"><span data-stu-id="49d52-121"><strong>Expense report auto posting</strong></span></span>   |        <span data-ttu-id="49d52-122">Luo työnkulkujen automaattinen kirjaaminen kuluraportteihin.</span><span class="sxs-lookup"><span data-stu-id="49d52-122">Create automatic posting workflows for expense reports.</span></span>        |
|       <span data-ttu-id="49d52-123"><strong>Kulurivin nimike</strong></span><span class="sxs-lookup"><span data-stu-id="49d52-123"><strong>Expense line item</strong></span></span>        |     <span data-ttu-id="49d52-124">Luo kuluraporttien rivinimikkeiden hyväksyntätyönkulkuja.</span><span class="sxs-lookup"><span data-stu-id="49d52-124">Create approval workflows for line items on expense reports.</span></span>      |
| <span data-ttu-id="49d52-125"><strong>Kulun rivinimikkeen automaattinen kirjaaminen</strong></span><span class="sxs-lookup"><span data-stu-id="49d52-125"><strong>Expense line item auto posting</strong></span></span> | <span data-ttu-id="49d52-126">Luo kuluraporttien rivinimikkeiden työnkulkujen automaattinen kirjaaminen.</span><span class="sxs-lookup"><span data-stu-id="49d52-126">Create automatic posting workflows for line items on expense reports.</span></span> |
|       <span data-ttu-id="49d52-127"><strong>Matkustusehdotus</strong></span><span class="sxs-lookup"><span data-stu-id="49d52-127"><strong>Travel requisition</strong></span></span>       |          <span data-ttu-id="49d52-128">Luo matkaehdotusten hyväksyntätyönkulkuja.</span><span class="sxs-lookup"><span data-stu-id="49d52-128">Create approval workflows for travel requisitions.</span></span>           |
|      <span data-ttu-id="49d52-129"><strong>Käteisennakkopyyntö</strong></span><span class="sxs-lookup"><span data-stu-id="49d52-129"><strong>Cash advance request</strong></span></span>      |         <span data-ttu-id="49d52-130">Luo hyväksyntätyönkulut käteisennakkopyynnöille.</span><span class="sxs-lookup"><span data-stu-id="49d52-130">Create approval workflows for cash advance requests.</span></span>          |
|        <span data-ttu-id="49d52-131"><strong>ALV:n palautus</strong></span><span class="sxs-lookup"><span data-stu-id="49d52-131"><strong>VAT tax recovery</strong></span></span>        | <span data-ttu-id="49d52-132">Voit luoda hyväksyntätyönkulkuja arvonlisäveron palautusta varten.</span><span class="sxs-lookup"><span data-stu-id="49d52-132">Create approval workflows for the recovery of value-added tax (VAT).</span></span>  |


[!INCLUDE[footer-include](../includes/footer-banner.md)]