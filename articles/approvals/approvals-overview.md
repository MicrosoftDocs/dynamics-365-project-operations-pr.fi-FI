---
title: Hyväksyntöjen yleiskatsaus
description: Tämä aihe tarjoaa tietoja hyväksymisten käsittelemisestä Project Operationsissa.
author: stsporen
manager: Annbe
ms.date: 10/05/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 37994422e9146765076fdbb77f5c763b4f1d0802
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/16/2020
ms.locfileid: "4075208"
---
# <a name="approvals-overview"></a><span data-ttu-id="b2e2a-103">Hyväksyntöjen yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="b2e2a-103">Approvals overview</span></span>

<span data-ttu-id="b2e2a-104">_**Koskee:** Project Operationsin resurssiin / muuhun kuin resurssiin perustuvia skenaarioita, Lite-käyttöönotto-kaupasta proformalaskutukseen_</span><span class="sxs-lookup"><span data-stu-id="b2e2a-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="b2e2a-105">Ajan ja kulujen lähetykset siirtyvät hyväksymisen työnkulun läpi.</span><span class="sxs-lookup"><span data-stu-id="b2e2a-105">Time and Expense submissions move through an approval workflow.</span></span> <span data-ttu-id="b2e2a-106">Kun tapahtumat on hyväksytty, tapahtumat kirjataan toteutuneisiin tai aika varataan aikataulussa.</span><span class="sxs-lookup"><span data-stu-id="b2e2a-106">After the entries are approved, transactions are recorded in actuals or time is booked in the schedule.</span></span>

## <a name="approvals-workflow"></a><span data-ttu-id="b2e2a-107">Hyväksyntätyönkulku</span><span class="sxs-lookup"><span data-stu-id="b2e2a-107">Approvals workflow</span></span>
<span data-ttu-id="b2e2a-108">Kun luot ja lähetät aika- tai kulutapahtuman, järjestelmä luo hyväksymismerkinnän.</span><span class="sxs-lookup"><span data-stu-id="b2e2a-108">When you create and submit a time or expense entry, an approval entry is created.</span></span> <span data-ttu-id="b2e2a-109">Projektin hyväksyjä tai esimies tarkistaa ja hyväksyy merkinnän.</span><span class="sxs-lookup"><span data-stu-id="b2e2a-109">The Project approver or your manager reviews and approves your entry.</span></span> <span data-ttu-id="b2e2a-110">Jos merkintä liittyy projektiin, todelliset arvot luodaan, kun se on hyväksytty.</span><span class="sxs-lookup"><span data-stu-id="b2e2a-110">If the entry is related to a project, when it's approved, the actuals will be created.</span></span> <span data-ttu-id="b2e2a-111">Tämä sallii kustannusten ja laskutuksen seurannan.</span><span class="sxs-lookup"><span data-stu-id="b2e2a-111">This allows the cost and billing to be tracked.</span></span> 

## <a name="approve-an-entry"></a><span data-ttu-id="b2e2a-112">Merkinnän hyväksyminen</span><span class="sxs-lookup"><span data-stu-id="b2e2a-112">Approve an entry</span></span>
<span data-ttu-id="b2e2a-113">**Hyväksynnät** -lomakkeen avulla voit siirtyä eri näkymien välillä niin, että voit tarkastella eri hyväksyntöjen tyyppejä.</span><span class="sxs-lookup"><span data-stu-id="b2e2a-113">The **Approvals** form allows you to switch between different views so that you can view the different types of approvals.</span></span>
  
1. <span data-ttu-id="b2e2a-114">Siirry **Hyväksynnät** -lomakkeeseen ja valitse **Kulut** , **Aika** tai **Peruutukset**.</span><span class="sxs-lookup"><span data-stu-id="b2e2a-114">Go to the **Approvals** form and select **Expenses** , **Time** , or **Recalls**.</span></span>
2. <span data-ttu-id="b2e2a-115">Tarkista kukin hyväksyntä ja valitse ne, jotka haluat hyväksyä.</span><span class="sxs-lookup"><span data-stu-id="b2e2a-115">Review each approval, and select the ones you want to approve.</span></span>
3. <span data-ttu-id="b2e2a-116">Hyväksy valitut tapahtumat valitsemalla **Hyväksy**.</span><span class="sxs-lookup"><span data-stu-id="b2e2a-116">Select **Approve** to approve the selected entries.</span></span>
<span data-ttu-id="b2e2a-117">Järjestelmä käsittelee nämä merkinnät ja luo toteutuneet arvot tai varauksen.</span><span class="sxs-lookup"><span data-stu-id="b2e2a-117">The system will process these entries and create actuals or a booking.</span></span>

## <a name="reject-an-entry"></a><span data-ttu-id="b2e2a-118">Tietueen hylkääminen</span><span class="sxs-lookup"><span data-stu-id="b2e2a-118">Reject an entry</span></span>
<span data-ttu-id="b2e2a-119">Projektin hyväksyjänä sinun täytyy ehkä lähettää tapahtuma uudelleen käyttäjälle korjausta varten.</span><span class="sxs-lookup"><span data-stu-id="b2e2a-119">As the Project approver, you may have to send an entry back to a user for correction.</span></span>
  
1. <span data-ttu-id="b2e2a-120">Siirry **Hyväksynnät** -lomakkeeseen ja valitse hylättävä tapahtuma.</span><span class="sxs-lookup"><span data-stu-id="b2e2a-120">Go to the **Approvals** form and select the entry to reject.</span></span> 
2. <span data-ttu-id="b2e2a-121">Valitse **Hylkää**.</span><span class="sxs-lookup"><span data-stu-id="b2e2a-121">Select **Reject**.</span></span>
3. <span data-ttu-id="b2e2a-122">Valinnainen – Voit lisätä kommentin **Hylkäyksen kommentit** -valintaikkunaan ja ilmoittaa käyttäjälle, miksi merkintä hylätään.</span><span class="sxs-lookup"><span data-stu-id="b2e2a-122">Optional - Add a comment in the **Rejection Comments** dialog to inform the user why the entry is being rejected.</span></span>
4. <span data-ttu-id="b2e2a-123">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="b2e2a-123">Select **OK**.</span></span> <span data-ttu-id="b2e2a-124">Tapahtuma palautetaan käyttäjälle.</span><span class="sxs-lookup"><span data-stu-id="b2e2a-124">The entry will be returned to the user.</span></span>
  
## <a name="recall-entries"></a><span data-ttu-id="b2e2a-125">Merkintöjen peruuttaminen</span><span class="sxs-lookup"><span data-stu-id="b2e2a-125">Recall entries</span></span>
<span data-ttu-id="b2e2a-126">Jossakin vaiheessa on ehkä peruutettava lähetetty tapahtuma.</span><span class="sxs-lookup"><span data-stu-id="b2e2a-126">At some point, you might need to recall a submitted entry.</span></span> <span data-ttu-id="b2e2a-127">Jos tapahtumaa ei ole hyväksytty, se palautetaan heti.</span><span class="sxs-lookup"><span data-stu-id="b2e2a-127">If the entry has not been approved, it will be returned immediately.</span></span> <span data-ttu-id="b2e2a-128">Hyväksytyllä tapahtumalla voi kuitenkin olla merkittävä vaikutus.</span><span class="sxs-lookup"><span data-stu-id="b2e2a-128">An approved entry however, may have a material impact.</span></span> <span data-ttu-id="b2e2a-129">Projektin hyväksyjän on hyväksyttävä peruutus, jotta tapahtuma voidaan palauttaa toteutuneissa arvoissa.</span><span class="sxs-lookup"><span data-stu-id="b2e2a-129">The Project approver is required to approve the recall in order to reverse the transaction in Actuals.</span></span>

## <a name="specify-project-approvers"></a><span data-ttu-id="b2e2a-130">Määritä projektin hyväksyjät</span><span class="sxs-lookup"><span data-stu-id="b2e2a-130">Specify Project approvers</span></span>
<span data-ttu-id="b2e2a-131">Kullakin projektilla on useita projektiryhmän jäseniä.</span><span class="sxs-lookup"><span data-stu-id="b2e2a-131">Each project has a number of project team members.</span></span> <span data-ttu-id="b2e2a-132">Voit määrittää, mitkä ryhmän jäsenet ovat myös projektin hyväksyjiä.</span><span class="sxs-lookup"><span data-stu-id="b2e2a-132">You can specify which team members are also Project approvers.</span></span>

1. <span data-ttu-id="b2e2a-133">Siirry **Projektit** -lomakkeeseen ja avaa projekti luettelosta.</span><span class="sxs-lookup"><span data-stu-id="b2e2a-133">Go to the **Projects** form and open the project from the list.</span></span>
2. <span data-ttu-id="b2e2a-134">Valitse **Ryhmä** -välilehdestä ryhmän jäsen, josta tulee projektin hyväksyjä, ja valitse sitten **Muokkaa**.</span><span class="sxs-lookup"><span data-stu-id="b2e2a-134">On the **Team** tab, select the team member who will be a Project approver and then select **Edit**.</span></span>
3. <span data-ttu-id="b2e2a-135">Valitse **Projektin hyväksyjä** -kentässä **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="b2e2a-135">Set the **Project Approver** field to **Yes**.</span></span>
4. <span data-ttu-id="b2e2a-136">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="b2e2a-136">Select **Save**.</span></span>
5. <span data-ttu-id="b2e2a-137">Lisää projektin hyväksyjiä toistamalla vaiheet 2–4.</span><span class="sxs-lookup"><span data-stu-id="b2e2a-137">Repeat steps 2-4 to add additional Project approvers.</span></span>

## <a name="configure-the-users-manager"></a><span data-ttu-id="b2e2a-138">Käyttäjän esimiehen määrittäminen</span><span class="sxs-lookup"><span data-stu-id="b2e2a-138">Configure the user's manager</span></span>

1. <span data-ttu-id="b2e2a-139">Valitse **Asetukset** > **Suojaus** > **Käyttäjät**.</span><span class="sxs-lookup"><span data-stu-id="b2e2a-139">Go to **Settings** > **Security** > **Users**.</span></span>
2. <span data-ttu-id="b2e2a-140">Valitse käyttäjä, jolle delegoit esimiehen, ja valitse **Organisaation tiedot** -alueessa esimies luettelosta.</span><span class="sxs-lookup"><span data-stu-id="b2e2a-140">Select the user to whom you are assigning a manager and in the **Organization Information** area, select the manager from the list.</span></span> 
3. <span data-ttu-id="b2e2a-141">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="b2e2a-141">Select **Save**.</span></span>


