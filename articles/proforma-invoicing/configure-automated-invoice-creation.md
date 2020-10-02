---
title: Automaattisen laskun luonnin määrittäminen
description: Tässä aiheessa on tietoja siitä, miten järjestelmä määritetään luomaan laskuja automaattisesti.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 764fd4568619e4f5676ee3cbf7fce14ffb069548
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/28/2020
ms.locfileid: "3898122"
---
# <a name="configure-automated-invoice-creation"></a><span data-ttu-id="c4ab7-103">Automaattisen laskun luonnin määrittäminen</span><span class="sxs-lookup"><span data-stu-id="c4ab7-103">Configure automated invoice creation</span></span>

<span data-ttu-id="c4ab7-104">_**Koskee:** Project Operationsin resurssiin / muuhun kuin resurssiin perustuvia skenaarioita, Lite-käyttöönotto-kaupasta proformalaskutukseen_</span><span class="sxs-lookup"><span data-stu-id="c4ab7-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="c4ab7-105">Suorita seuraavat vaiheet, jos haluat määrittää Project Operationsille automaattisen laskujen suorittamisen.</span><span class="sxs-lookup"><span data-stu-id="c4ab7-105">Complete the following steps to configure an automated invoice run in Project operations.</span></span>

1. <span data-ttu-id="c4ab7-106">Siirry kohtaan **Asetukset** \> **Erätyöt**.</span><span class="sxs-lookup"><span data-stu-id="c4ab7-106">Go to **Settings** \> **Batch jobs**.</span></span>
2. <span data-ttu-id="c4ab7-107">Luo erätyö ja anna sille nimeksi **Project Operationsin laskujen luominen**.</span><span class="sxs-lookup"><span data-stu-id="c4ab7-107">Create a batch job, and name it **Project operations create invoices**.</span></span> <span data-ttu-id="c4ab7-108">Erätyön nimessä on oltava termi "laskujen luominen".</span><span class="sxs-lookup"><span data-stu-id="c4ab7-108">The name of the batch job must include the term "create invoices."</span></span>
3. <span data-ttu-id="c4ab7-109">Valitse **Työtyyppi**-kentässä **Ei mitään**.</span><span class="sxs-lookup"><span data-stu-id="c4ab7-109">In the **Job type** field, select **None**.</span></span> <span data-ttu-id="c4ab7-110">Asetusten **Päivittäin** ja **On aktiivinen** oletusarvo on **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="c4ab7-110">By default, the **Frequency Daily** and **Is Active** options are set to **Yes**.</span></span>
4. <span data-ttu-id="c4ab7-111">Valitse **Suorita työnkulku**.</span><span class="sxs-lookup"><span data-stu-id="c4ab7-111">Select **Run Workflow**.</span></span> <span data-ttu-id="c4ab7-112">**Valitse tietue** -valintaikkunassa näkyy kolme työnkulkua:</span><span class="sxs-lookup"><span data-stu-id="c4ab7-112">In the **Look Up Record** dialog box, you will see three workflows:</span></span>

    - <span data-ttu-id="c4ab7-113">ProcessRunCaller</span><span class="sxs-lookup"><span data-stu-id="c4ab7-113">ProcessRunCaller</span></span>
    - <span data-ttu-id="c4ab7-114">ProcessRunner</span><span class="sxs-lookup"><span data-stu-id="c4ab7-114">ProcessRunner</span></span>
    - <span data-ttu-id="c4ab7-115">UpdateRoleUtilization</span><span class="sxs-lookup"><span data-stu-id="c4ab7-115">UpdateRoleUtilization</span></span>

5. <span data-ttu-id="c4ab7-116">Valitse **ProcessRunCaller** ja sitten **Lisää**.</span><span class="sxs-lookup"><span data-stu-id="c4ab7-116">Select **ProcessRunCaller**, and then select **Add**.</span></span>
6. <span data-ttu-id="c4ab7-117">Valitse seuraavassa valintaikkunassa **OK**.</span><span class="sxs-lookup"><span data-stu-id="c4ab7-117">In the next dialog box, select **OK**.</span></span> <span data-ttu-id="c4ab7-118">**Lepo**-työnkulkua seuraa **Käsittely**-työnkulku.</span><span class="sxs-lookup"><span data-stu-id="c4ab7-118">A **Sleep** workflow is followed by a **Process** workflow.</span></span>

    <span data-ttu-id="c4ab7-119">Vaiheessa 5 voit myös valita **ProcessRunner**.</span><span class="sxs-lookup"><span data-stu-id="c4ab7-119">You can also select **ProcessRunner** in step 5.</span></span> <span data-ttu-id="c4ab7-120">Kun tämän jälkeen valitset **OK**, **Käsittely**-työnkulkua seuraa **Lepo**-työnkulku.</span><span class="sxs-lookup"><span data-stu-id="c4ab7-120">Then, when you select **OK**, a **Process** workflow is followed by a **Sleep** workflow.</span></span>

<span data-ttu-id="c4ab7-121">Työnkulut **ProcessRunCaller** ja **ProcessRunner** luovat laskuja.</span><span class="sxs-lookup"><span data-stu-id="c4ab7-121">The **ProcessRunCaller** and **ProcessRunner** workflows create invoices.</span></span> <span data-ttu-id="c4ab7-122">Työnkulku **ProcessRunCaller** kutsuu työnkulun **ProcessRunner**.</span><span class="sxs-lookup"><span data-stu-id="c4ab7-122">**ProcessRunCaller** calls **ProcessRunner**.</span></span> <span data-ttu-id="c4ab7-123">**ProcessRunner** on se työnkulku, joka tosiasiassa luo laskut.</span><span class="sxs-lookup"><span data-stu-id="c4ab7-123">**ProcessRunner** is the workflow that actually creates the invoices.</span></span> <span data-ttu-id="c4ab7-124">Se käy läpi kaikki sopimusrivit, joille on luotava lasku, ja luo kyseiset laskut.</span><span class="sxs-lookup"><span data-stu-id="c4ab7-124">It goes through all the contract lines that invoices must be created for, and it creates invoices for those lines.</span></span> <span data-ttu-id="c4ab7-125">Työnkulku tarkistaa sopimusrivien laskujen suorituspäiviä määrittääkseen ne sopimusrivit, joille on luotava laskuja.</span><span class="sxs-lookup"><span data-stu-id="c4ab7-125">To determine the contract lines that invoices must be created for, the job looks at invoice run dates for the contract lines.</span></span> <span data-ttu-id="c4ab7-126">Jos yhteen sopimukseen kuuluvilla sopimusriveillä on sama laskujen suorituspäivä, tapahtumat yhdistetään yhteen laskuun, jolla on kaksi laskutusriviä.</span><span class="sxs-lookup"><span data-stu-id="c4ab7-126">If contract lines that belong to one contract have the same invoice run date, the transactions are combined into one invoice that has two invoice lines.</span></span> <span data-ttu-id="c4ab7-127">Jos laskujen luomista edellyttäviä tapahtumia ei ole, työnkulku ohittaa laskujen luonnin.</span><span class="sxs-lookup"><span data-stu-id="c4ab7-127">If there are no transactions to create invoices for, the job skips invoice creation.</span></span>

<span data-ttu-id="c4ab7-128">Kun **ProcessRunner** on valmis, se kutsuu työnkulun **ProcessRunCaller**, antaa päättymisajan ja sulkeutuu.</span><span class="sxs-lookup"><span data-stu-id="c4ab7-128">After **ProcessRunner** has finished running, it calls **ProcessRunCaller**, provides the end time, and is closed.</span></span> <span data-ttu-id="c4ab7-129">**ProcessRunCaller**käynnistää sitten ajastimen, joka kestää 24 tuntia määritetystä päättymisajasta eteenpäin.</span><span class="sxs-lookup"><span data-stu-id="c4ab7-129">**ProcessRunCaller** then starts a timer that runs for 24 hours from the specified end time.</span></span> <span data-ttu-id="c4ab7-130">Ajastimen loputtua, **ProcessRunCaller** sulkeutuu.</span><span class="sxs-lookup"><span data-stu-id="c4ab7-130">At the end of the timer, **ProcessRunCaller** is closed.</span></span>

<span data-ttu-id="c4ab7-131">Laskujen luomisen erätyö on toistuva työ.</span><span class="sxs-lookup"><span data-stu-id="c4ab7-131">The batch process job for creating invoices is a recurrent job.</span></span> <span data-ttu-id="c4ab7-132">Jos tämä erätyö suoritetaan useita kertoja, siitä luodaan useita esiintymiä, mikä voi aiheuttaa virheitä.</span><span class="sxs-lookup"><span data-stu-id="c4ab7-132">If this batch process is run many times, multiple instances of the job are created and cause errors.</span></span> <span data-ttu-id="c4ab7-133">Siksi erätyö kannatta käynnistää vain kerran ja käynnistää uudelleen vain, jos se pysähtyy.</span><span class="sxs-lookup"><span data-stu-id="c4ab7-133">Therefore, you should start the batch process only one time, and you should restart it only if it stops running.</span></span>

> [!NOTE]
> <span data-ttu-id="c4ab7-134">Erälaskutus suoritetaan vain sellaisille projektisopimusriveille, jotka on määritetty laskun aikataulun mukaan.</span><span class="sxs-lookup"><span data-stu-id="c4ab7-134">Batch invoicing only runs for project contract lines that are configured by invoice schedules.</span></span> <span data-ttu-id="c4ab7-135">Jos sopimusrivillä on kiinteähintainen laskutusmenetelmä, sillä on oltava määritettyinä välitavoitteet.</span><span class="sxs-lookup"><span data-stu-id="c4ab7-135">A contract line with a fixed price billing method must have milestones configured.</span></span> <span data-ttu-id="c4ab7-136">Jos projektisopimusrivillä on aika- ja materiaalipohjainen laskutusmenetelmä, sille on määritettävä päivämäärään perustuva laskutusaikataulu.</span><span class="sxs-lookup"><span data-stu-id="c4ab7-136">A project contract line with a time and material billing method will need a date-based invoice schedule set up.</span></span> <span data-ttu-id="c4ab7-137">Sama koskee myös projektipohjaista sopimusriviä.</span><span class="sxs-lookup"><span data-stu-id="c4ab7-137">The same applies to a project-based contract line.</span></span>     
