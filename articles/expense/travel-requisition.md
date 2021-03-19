---
title: Matkustusehdotukset
description: Tässä aiheessa on tietoja matkustusehdotuksista.
author: suvaidya
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: suvaidya
ms.openlocfilehash: fa612696944082e179ab2484e2fdd76d1696b889
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5275984"
---
# <a name="travel-requisitions"></a><span data-ttu-id="95d4b-103">Matkustusehdotukset</span><span class="sxs-lookup"><span data-stu-id="95d4b-103">Travel requisitions</span></span>

<span data-ttu-id="95d4b-104">_**Käytetään:** Project Operationsin resursseihin ja ei-varastoitaviin perustuvissa skenaarioissa_</span><span class="sxs-lookup"><span data-stu-id="95d4b-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="95d4b-105">Matkustusehdotuksessa on luettelo kuluista, jotka aiheutuvat matkustamisen tarkoituksesta.</span><span class="sxs-lookup"><span data-stu-id="95d4b-105">A travel requisition lists the expenses that will be incurred for the purpose of travel.</span></span> <span data-ttu-id="95d4b-106">Matkustusehdotus lähetetään tarkistettavaksi, ja sitä voidaan käyttää kulujen valtuuttamiseen.</span><span class="sxs-lookup"><span data-stu-id="95d4b-106">A travel requisition is submitted for review and can be used to authorize expenses.</span></span>

<span data-ttu-id="95d4b-107">Sinun täytyy ehkä lähettää matkaehdotus, ennen kuin sinulle aiheutuu kuluja, jotka veloitetaan organisaatiolta.</span><span class="sxs-lookup"><span data-stu-id="95d4b-107">You may be required to submit a travel requisition before you incur any expense that is charged to the organization.</span></span> <span data-ttu-id="95d4b-108">Tämä vaatimus pätee riippumatta siitä, veloitatko kuluja yrityksen luottokortilta, käytätkö käteisennakon käteistä vai kerrytätkö organisaation korvaamia kuluja omalla käteiselläsi.</span><span class="sxs-lookup"><span data-stu-id="95d4b-108">This requirement applies, regardless of whether you charge expenses to a corporate credit card, spend cash that you received from a cash advance, or incur out-of-pocket expenses that will be reimbursed by the organization.</span></span>

<span data-ttu-id="95d4b-109">Matkaehdotusten ja käytäntöjen avulla voit hallita organisaation kuluja.</span><span class="sxs-lookup"><span data-stu-id="95d4b-109">Travel requisitions and policies can be used to help manage organization expenditures.</span></span> <span data-ttu-id="95d4b-110">Jos organisaatiosi esimerkiksi työstää kiinteähintaista projektia, jotka edellyttää matkustamista, projektiryhmän jäsenten matkakulujen on sovittava yhteen projektibudjetin kanssa.</span><span class="sxs-lookup"><span data-stu-id="95d4b-110">For example, if your organization is working on a fixed-price project that requires travel, the travel expenses of the project's team members must fit within the project budget.</span></span> <span data-ttu-id="95d4b-111">Vaatimalla, että matkakulut hyväksytään ennen niiden syntymistä, organisaatio voi auttaa varmistamaan, että projekti säilyy budjetissa.</span><span class="sxs-lookup"><span data-stu-id="95d4b-111">By requiring that travel expenses be approved before they are incurred, the organization can help make sure that the project remains within budget.</span></span>

## <a name="configuration"></a><span data-ttu-id="95d4b-112">Määritys</span><span class="sxs-lookup"><span data-stu-id="95d4b-112">Configuration</span></span> 

<span data-ttu-id="95d4b-113">Matkaehdotukset voidaan määrittää "pakollisiksi" ottamalla käyttöön Matkan valtuutus etukäteen on pakollista -parametrin kulujen hallinnan parametreissa.</span><span class="sxs-lookup"><span data-stu-id="95d4b-113">Travel Requisitions can be configured as "mandatory" by enabling the "Pre-authorization of travel is mandatory" parameter in Expense Management Parameters.</span></span> 

## <a name="create-and-submit-a-travel-requisition"></a><span data-ttu-id="95d4b-114">Matkustusehdotuksen luominen ja lähettäminen</span><span class="sxs-lookup"><span data-stu-id="95d4b-114">Create and submit a travel requisition</span></span>

1. <span data-ttu-id="95d4b-115">Siirry kohtaan **Omat kulut: matkustusehdotus** ja valitse **Uusi matkustusehdotus**.</span><span class="sxs-lookup"><span data-stu-id="95d4b-115">Go to **My expenses: Travel Requisition**, and select **New travel Requisition**.</span></span>
2. <span data-ttu-id="95d4b-116">Määritä ehdotuksen tarkoitus ja kohde.</span><span class="sxs-lookup"><span data-stu-id="95d4b-116">Enter a purpose and destination for the requisition.</span></span>
3. <span data-ttu-id="95d4b-117">Kirjoita **Matkan kuvaus** -kenttään mahdolliset lisätiedot.</span><span class="sxs-lookup"><span data-stu-id="95d4b-117">In the  **Travel description** field, enter any additional information.</span></span> 
4. <span data-ttu-id="95d4b-118">Luo kulurivinimike kullekin oletetulle kustannukselle, kuten lennoille, aterioille tai auton vuokralle.</span><span class="sxs-lookup"><span data-stu-id="95d4b-118">For each of the expected expenses, such as Flight, meals, or car rental, create an expense line item.</span></span> <span data-ttu-id="95d4b-119">Sisällytä kullekin kululle arvioitu päivämäärä, arvioitu summa ja valuutta.</span><span class="sxs-lookup"><span data-stu-id="95d4b-119">Include the estimated date, estimated amount, and the currency for each expense.</span></span> 
5. <span data-ttu-id="95d4b-120">Kun olet lisännyt oletetut kulut, valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="95d4b-120">When you have finished adding the expected expenses, select **Save**.</span></span>
6. <span data-ttu-id="95d4b-121">Kun olet valmis lähettämään matkustusehdotuksen, valitse **Työnkulku** > **Lähetä**.</span><span class="sxs-lookup"><span data-stu-id="95d4b-121">When you are ready to submit the travel requisition, select **Workflow** > **Submit**.</span></span>

<span data-ttu-id="95d4b-122">Voit tarkastella hyväksyttyjä matkustusehdotuksia **Omat kulut: matkustusehdotus** -kohdassa.</span><span class="sxs-lookup"><span data-stu-id="95d4b-122">You can view your approved travel requisitions under **My Expenses: Travel Requisition**.</span></span> 

## <a name="view-available-travel-requisitions"></a><span data-ttu-id="95d4b-123">Käytettävissä olevien matkaehdotusten tarkasteleminen</span><span class="sxs-lookup"><span data-stu-id="95d4b-123">View available travel requisitions</span></span>

<span data-ttu-id="95d4b-124">Voit tarkastella kaikkia matkustusehdotuksiasi **Omat kulut: matkustusehdotukset** -kohdassa.</span><span class="sxs-lookup"><span data-stu-id="95d4b-124">You can view all of your travel requisitions under **My Expenses: Travel Requisitions**.</span></span>

## <a name="approve-travel-requisitions"></a><span data-ttu-id="95d4b-125">Matkustusehdotusten hyväksyminen</span><span class="sxs-lookup"><span data-stu-id="95d4b-125">Approve travel requisitions</span></span>

<span data-ttu-id="95d4b-126">Valitse hyväksyttävä matkustusehdotus ja valitse sitten **Työnkulku** > **Hyväksy**.</span><span class="sxs-lookup"><span data-stu-id="95d4b-126">Select the travel requisition that you want to approve, and then select **Workflow** > **Approve**.</span></span>  

## <a name="submit-an-expense-report-using-your-approved-travel-requisition"></a><span data-ttu-id="95d4b-127">Kuluraportin lähettäminen käyttäen hyväksyttyä matkaehdotusta</span><span class="sxs-lookup"><span data-stu-id="95d4b-127">Submit an expense report using your approved travel requisition</span></span>

1. <span data-ttu-id="95d4b-128">Luo uusi kuluraportti ja valitse kuluraportin otsikossa hyväksyttyjen matkaehdotusten luettelosta **Yhdistä matkustusehdotukseen**.</span><span class="sxs-lookup"><span data-stu-id="95d4b-128">Create a new expense report and in the expense report header, and from the list of approved travel requisitions, select **Map to Travel requisition**.</span></span>
2. <span data-ttu-id="95d4b-129">**Matkustusehdotuksen summa** -kenttä päivittyy automaattisesti kuluraportin otsikossa.</span><span class="sxs-lookup"><span data-stu-id="95d4b-129">The **Travel requisition amount** field is automatically updated in the expense report header.</span></span>
3. <span data-ttu-id="95d4b-130">Lisää kaikki matkasta aiheutuneet kulut.</span><span class="sxs-lookup"><span data-stu-id="95d4b-130">Add each expense incurred for the trip.</span></span> <span data-ttu-id="95d4b-131">Jos **Valtuutettu etukäteen** -kenttä on käytössä, tietyn kululuokan täsmäytetty summa ja valtuutettu summa päivitetään.</span><span class="sxs-lookup"><span data-stu-id="95d4b-131">If the **Pre-authorized** field is enabled, the reconciled amount and authorized amount for the specific expense category will be updated.</span></span>

> [!NOTE]
> <span data-ttu-id="95d4b-132">Kun yhdistät kuluraportin hyväksyttyyn matkaehdotukseen, tapahtuman summa ei voi olla suurempi kuin valtuutettu summa.</span><span class="sxs-lookup"><span data-stu-id="95d4b-132">When you map an expense report to an approved travel requisition, the transaction amount can't be greater than the authorized amount.</span></span> 


[!INCLUDE[footer-include](../includes/footer-banner.md)]