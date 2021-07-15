---
title: Hyväksyntöjen yleiskatsaus
description: Tämä aihe tarjoaa tietoja hyväksymisten käsittelemisestä Project Operationsissa.
author: stsporen
ms.date: 03/31/2021
ms.topic: article
ms.reviewer: kfend
ms.author: stsporen
ms.custom: intro-internal
ms.openlocfilehash: 9148c9f55e8664850c38aebbc9c4bbaa243475ad
ms.sourcegitcommit: 0fafe022731f0e1e8693382ff906e3f8541d34ca
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 07/07/2021
ms.locfileid: "6368652"
---
# <a name="approvals-overview"></a><span data-ttu-id="a617a-103">Hyväksyntöjen yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="a617a-103">Approvals overview</span></span>

<span data-ttu-id="a617a-104">_**Koskee:** Project Operationsin resurssiin / muuhun kuin resurssiin perustuvia skenaarioita, Lite-käyttöönotto-kaupasta proformalaskutukseen_</span><span class="sxs-lookup"><span data-stu-id="a617a-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="a617a-105">Ajan, kulun ja materiaalin käytön lähetykset liikkuvat hyväksynnän työnkulun läpi.</span><span class="sxs-lookup"><span data-stu-id="a617a-105">Time, expense, and material usage submissions move through an approval workflow.</span></span> <span data-ttu-id="a617a-106">Kun tapahtumat on hyväksytty, tapahtumat kirjataan toteutuneisiin tai aika varataan aikataulussa.</span><span class="sxs-lookup"><span data-stu-id="a617a-106">After the entries are approved, transactions are recorded in actuals or time is booked in the schedule.</span></span>

## <a name="approvals-workflow"></a><span data-ttu-id="a617a-107">Hyväksyntätyönkulku</span><span class="sxs-lookup"><span data-stu-id="a617a-107">Approvals workflow</span></span>
<span data-ttu-id="a617a-108">Kun luot ja lähetät ajan, kulun tai materiaalin käytön merkinnän, luodaan hyväksyntätietue.</span><span class="sxs-lookup"><span data-stu-id="a617a-108">When you create and submit a time, expense, or material usage entry, an approval record is created.</span></span> <span data-ttu-id="a617a-109">Projektin hyväksyjä tai esimies arvioi ja hyväksyy merkinnän.</span><span class="sxs-lookup"><span data-stu-id="a617a-109">The project approver or manager reviews and approves the entry.</span></span> <span data-ttu-id="a617a-110">Jos merkintä liittyy projektiin, toteutuneet arvot luodaan, kun se hyväksytään.</span><span class="sxs-lookup"><span data-stu-id="a617a-110">If the entry is related to a project, the actuals will be created when it's approved.</span></span> <span data-ttu-id="a617a-111">Tämä sallii kustannusten ja laskutuksen seurannan.</span><span class="sxs-lookup"><span data-stu-id="a617a-111">This allows the cost and billing to be tracked.</span></span>

## <a name="approve-an-entry"></a><span data-ttu-id="a617a-112">Merkinnän hyväksyminen</span><span class="sxs-lookup"><span data-stu-id="a617a-112">Approve an entry</span></span>
<span data-ttu-id="a617a-113">**Hyväksynnät**-sivulla voit siirtyä eri näkymien välillä niin, että voit tarkastella erityyppisiä hyväksyntöjä.</span><span class="sxs-lookup"><span data-stu-id="a617a-113">The **Approvals** page allows you to switch between different views so that you can view the different types of approvals.</span></span>
  
1. <span data-ttu-id="a617a-114">Siirry **Hyväksynnät**-sivulle ja valitse **Kulut**, **Aika**, **Materiaalin käyttö** tai **Peruutukset**.</span><span class="sxs-lookup"><span data-stu-id="a617a-114">Go to the **Approvals** page and select **Expenses**, **Time**, **Material Usage**, or **Recalls**.</span></span>
2. <span data-ttu-id="a617a-115">Tarkista kukin hyväksyntä ja valitse ne, jotka haluat hyväksyä.</span><span class="sxs-lookup"><span data-stu-id="a617a-115">Review each approval, and select the ones you want to approve.</span></span>
3. <span data-ttu-id="a617a-116">Hyväksy valitut tapahtumat valitsemalla **Hyväksy**.</span><span class="sxs-lookup"><span data-stu-id="a617a-116">Select **Approve** to approve the selected entries.</span></span>
<span data-ttu-id="a617a-117">Järjestelmä käsittelee nämä merkinnät ja luo toteutuneet arvot.</span><span class="sxs-lookup"><span data-stu-id="a617a-117">The system processes these entries and create actuals.</span></span>

## <a name="reject-an-entry"></a><span data-ttu-id="a617a-118">Tietueen hylkääminen</span><span class="sxs-lookup"><span data-stu-id="a617a-118">Reject an entry</span></span>
<span data-ttu-id="a617a-119">Projektin hyväksyjänä sinun täytyy ehkä lähettää tapahtuma uudelleen käyttäjälle korjausta varten.</span><span class="sxs-lookup"><span data-stu-id="a617a-119">As the Project approver, you may have to send an entry back to a user for correction.</span></span>
  
1. <span data-ttu-id="a617a-120">Siirry **Hyväksynnät**-sivulle ja valitse hylättävä merkintä.</span><span class="sxs-lookup"><span data-stu-id="a617a-120">Go to the **Approvals** page and select the entry to reject.</span></span> 
2. <span data-ttu-id="a617a-121">Valitse **Hylkää**.</span><span class="sxs-lookup"><span data-stu-id="a617a-121">Select **Reject**.</span></span>
3. <span data-ttu-id="a617a-122">Valinnaisesti voit lisätä kommentin **Hylkäyskommemmentit**-valintaikkunaan ja ilmoittaa käyttäjälle, miksi merkintä hylätään.</span><span class="sxs-lookup"><span data-stu-id="a617a-122">Optional, add a comment in the **Rejection Comments** dialog box to inform the user why the entry is being rejected.</span></span>
4. <span data-ttu-id="a617a-123">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="a617a-123">Select **OK**.</span></span> <span data-ttu-id="a617a-124">Tapahtuma palautetaan käyttäjälle.</span><span class="sxs-lookup"><span data-stu-id="a617a-124">The entry will be returned to the user.</span></span>
  
## <a name="cancel-approval"></a><span data-ttu-id="a617a-125">Peruuta hyväksyntä</span><span class="sxs-lookup"><span data-stu-id="a617a-125">Cancel approval</span></span>
<span data-ttu-id="a617a-126">Joissakin tapauksissa aiemmin hyväksytty merkintä on ehkä peruutettava.</span><span class="sxs-lookup"><span data-stu-id="a617a-126">In some cases, you might need to cancel a previously approved entry.</span></span> <span data-ttu-id="a617a-127">Aiemmin hyväksytyn merkinnän peruuttaminen vaikuttaa taloustietoihin.</span><span class="sxs-lookup"><span data-stu-id="a617a-127">Canceling a previously approved entry will have a financial impact.</span></span> 

## <a name="approving-recall-requests"></a><span data-ttu-id="a617a-128">Peruutuspyyntöjen hyväksyminen</span><span class="sxs-lookup"><span data-stu-id="a617a-128">Approving recall requests</span></span>
<span data-ttu-id="a617a-129">Joissakin tapauksissa konsultin on ehkä syytä peruuttaa aiemmin hyväksytty merkintä.</span><span class="sxs-lookup"><span data-stu-id="a617a-129">In some cases, a consultant may need to recall a previously approved entry.</span></span> <span data-ttu-id="a617a-130">Aiemmin hyväksytyn merkinnän peruuttaminen vaikuttaa taloustietoihin.</span><span class="sxs-lookup"><span data-stu-id="a617a-130">Canceling a previously approved entry will have a financial impact.</span></span> <span data-ttu-id="a617a-131">Projektin hyväksyjän on hyväksyttävä peruutus, jotta tapahtuma voidaan kumota toteutuneissa arvoissa.</span><span class="sxs-lookup"><span data-stu-id="a617a-131">The project approver is required to approve the recall to reverse the transaction in Actuals.</span></span>

## <a name="specify-project-approvers"></a><span data-ttu-id="a617a-132">Määritä projektin hyväksyjät</span><span class="sxs-lookup"><span data-stu-id="a617a-132">Specify Project approvers</span></span>
<span data-ttu-id="a617a-133">Kullakin projektilla on useita projektiryhmän jäseniä.</span><span class="sxs-lookup"><span data-stu-id="a617a-133">Each project has a number of project team members.</span></span> <span data-ttu-id="a617a-134">Voit määrittää, mitkä ryhmän jäsenet ovat myös projektin hyväksyjiä.</span><span class="sxs-lookup"><span data-stu-id="a617a-134">You can specify which team members are also Project approvers.</span></span>

1. <span data-ttu-id="a617a-135">Siirry **Projektit**-sivulle ja avaa projekti luettelosta.</span><span class="sxs-lookup"><span data-stu-id="a617a-135">Go to the **Projects** page and open the project from the list.</span></span>
2. <span data-ttu-id="a617a-136">Valitse **Ryhmä**-välilehdestä ryhmän jäsen, josta tulee projektin hyväksyjä, ja valitse sitten **Muokkaa**.</span><span class="sxs-lookup"><span data-stu-id="a617a-136">On the **Team** tab, select the team member who will be a Project approver and then select **Edit**.</span></span>
3. <span data-ttu-id="a617a-137">Valitse **Projektin hyväksyjä** -kentässä **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="a617a-137">Set the **Project Approver** field to **Yes**.</span></span>
4. <span data-ttu-id="a617a-138">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="a617a-138">Select **Save**.</span></span>
5. <span data-ttu-id="a617a-139">Lisää projektin hyväksyjiä toistamalla vaiheet 2–4.</span><span class="sxs-lookup"><span data-stu-id="a617a-139">Repeat steps 2-4 to add additional Project approvers.</span></span>

## <a name="configure-the-users-manager"></a><span data-ttu-id="a617a-140">Käyttäjän esimiehen määrittäminen</span><span class="sxs-lookup"><span data-stu-id="a617a-140">Configure the user's manager</span></span>

1. <span data-ttu-id="a617a-141">Valitse **Asetukset** > **Suojaus** > **Käyttäjät**.</span><span class="sxs-lookup"><span data-stu-id="a617a-141">Go to **Settings** > **Security** > **Users**.</span></span>
2. <span data-ttu-id="a617a-142">Valitse käyttäjä, jolle delegoit esimiehen, ja valitse **Organisaation tiedot** -alueessa esimies luettelosta.</span><span class="sxs-lookup"><span data-stu-id="a617a-142">Select the user to whom you are assigning a manager and in the **Organization Information** area, select the manager from the list.</span></span> 
3. <span data-ttu-id="a617a-143">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="a617a-143">Select **Save**.</span></span>




[!INCLUDE[footer-include](../includes/footer-banner.md)]
