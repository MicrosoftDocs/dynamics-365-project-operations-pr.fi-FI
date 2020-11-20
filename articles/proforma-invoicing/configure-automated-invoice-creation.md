---
title: Automaattisen laskun luonnin määrittäminen
description: Tässä aiheessa on tietoja siitä, miten järjestelmä määritetään luomaan laskuja automaattisesti.
author: rumant
manager: Annbe
ms.date: 10/13/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 295c3b099c9670c930fb2ba2fd208be63a77217f
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/28/2020
ms.locfileid: "4122429"
---
# <a name="configure-automatic-invoice-creation"></a><span data-ttu-id="7ec73-103">Automaattisen laskun luonnin määrittäminen</span><span class="sxs-lookup"><span data-stu-id="7ec73-103">Configure automatic invoice creation</span></span>

<span data-ttu-id="7ec73-104">_**Käytetään:** Project Operationsin resursseihin ja ei-varastoitaviin perustuvissa skenaarioissa_</span><span class="sxs-lookup"><span data-stu-id="7ec73-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>


<span data-ttu-id="7ec73-105">Suorita seuraavat vaiheet, jos haluat määrittää Dynamics 365 Project Operationsille automaattisen laskujen suorittamisen.</span><span class="sxs-lookup"><span data-stu-id="7ec73-105">Complete the following steps to configure an automated invoice run in Dynamics 365 Project operations.</span></span>

1. <span data-ttu-id="7ec73-106">Siirry kohtaan **Asetukset** > **Erätyöt**.</span><span class="sxs-lookup"><span data-stu-id="7ec73-106">Go to **Settings** > **Batch jobs**.</span></span>
2. <span data-ttu-id="7ec73-107">Luo erätyö ja anna sille nimeksi **Project Operationsin laskujen luominen**.</span><span class="sxs-lookup"><span data-stu-id="7ec73-107">Create a batch job, and name it **Project operations create invoices**.</span></span> <span data-ttu-id="7ec73-108">Erätyön nimessä on oltava sanat "laskujen luominen".</span><span class="sxs-lookup"><span data-stu-id="7ec73-108">The name of the batch job must include the words "create invoices."</span></span>
3. <span data-ttu-id="7ec73-109">Valitse **Työtyyppi**-kentässä **Ei mitään**.</span><span class="sxs-lookup"><span data-stu-id="7ec73-109">In the **Job Type** field, select **None**.</span></span> <span data-ttu-id="7ec73-110">Asetusten **Päivittäin** ja **On aktiivinen** oletusarvo on **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="7ec73-110">By default, the **Frequency Daily** and **Is Active** options are set to **Yes**.</span></span>
4. <span data-ttu-id="7ec73-111">Valitse **Suorita työnkulku**.</span><span class="sxs-lookup"><span data-stu-id="7ec73-111">Select **Run Workflow**.</span></span> <span data-ttu-id="7ec73-112">**Valitse tietue** -valintaikkunassa näkyy kolme työnkulkua:</span><span class="sxs-lookup"><span data-stu-id="7ec73-112">In the **Look Up Record** dialog box, you will see three workflows:</span></span>

    - <span data-ttu-id="7ec73-113">ProcessRunCaller</span><span class="sxs-lookup"><span data-stu-id="7ec73-113">ProcessRunCaller</span></span>
    - <span data-ttu-id="7ec73-114">ProcessRunner</span><span class="sxs-lookup"><span data-stu-id="7ec73-114">ProcessRunner</span></span>
    - <span data-ttu-id="7ec73-115">UpdateRoleUtilization</span><span class="sxs-lookup"><span data-stu-id="7ec73-115">UpdateRoleUtilization</span></span>

5. <span data-ttu-id="7ec73-116">Valitse **ProcessRunCaller** ja sitten **Lisää**.</span><span class="sxs-lookup"><span data-stu-id="7ec73-116">Select **ProcessRunCaller**, and then select **Add**.</span></span>
6. <span data-ttu-id="7ec73-117">Valitse seuraavassa valintaikkunassa **OK**.</span><span class="sxs-lookup"><span data-stu-id="7ec73-117">In the next dialog box, select **OK**.</span></span> <span data-ttu-id="7ec73-118">**Lepo**-työnkulkua seuraa **Käsittely**-työnkulku.</span><span class="sxs-lookup"><span data-stu-id="7ec73-118">A **Sleep** workflow is followed by a **Process** workflow.</span></span>

  > [!NOTE]
  > <span data-ttu-id="7ec73-119">Vaiheessa 5 voit myös valita **ProcessRunner**.</span><span class="sxs-lookup"><span data-stu-id="7ec73-119">You can also select **ProcessRunner** in step 5.</span></span> <span data-ttu-id="7ec73-120">Kun tämän jälkeen valitset **OK**, **Käsittely**-työnkulkua seuraa **Lepo**-työnkulku.</span><span class="sxs-lookup"><span data-stu-id="7ec73-120">Then, when you select **OK**, a **Process** workflow is followed by a **Sleep** workflow.</span></span>

<span data-ttu-id="7ec73-121">Työnkulut **ProcessRunCaller** ja **ProcessRunner** luovat laskuja.</span><span class="sxs-lookup"><span data-stu-id="7ec73-121">The **ProcessRunCaller** and **ProcessRunner** workflows create invoices.</span></span> <span data-ttu-id="7ec73-122">Työnkulku **ProcessRunCaller** kutsuu työnkulun **ProcessRunner**.</span><span class="sxs-lookup"><span data-stu-id="7ec73-122">**ProcessRunCaller** calls **ProcessRunner**.</span></span> <span data-ttu-id="7ec73-123">**ProcessRunner** on se työnkulku, joka tosiasiassa luo laskut.</span><span class="sxs-lookup"><span data-stu-id="7ec73-123">**ProcessRunner** is the workflow that actually creates the invoices.</span></span> <span data-ttu-id="7ec73-124">Se käy läpi kaikki sopimusrivit, joille on luotava lasku, ja luo kyseiset laskut.</span><span class="sxs-lookup"><span data-stu-id="7ec73-124">It goes through all the contract lines that invoices must be created for, and it creates invoices for those lines.</span></span> <span data-ttu-id="7ec73-125">Työnkulku tarkistaa sopimusrivien laskujen suorituspäiviä määrittääkseen ne sopimusrivit, joille on luotava laskuja.</span><span class="sxs-lookup"><span data-stu-id="7ec73-125">To determine the contract lines that invoices must be created for, the job looks at invoice run dates for the contract lines.</span></span> <span data-ttu-id="7ec73-126">Jos yhteen sopimukseen kuuluvilla sopimusriveillä on sama laskujen suorituspäivä, tapahtumat yhdistetään yhteen laskuun, jolla on kaksi laskutusriviä.</span><span class="sxs-lookup"><span data-stu-id="7ec73-126">If contract lines that belong to one contract have the same invoice run date, the transactions are combined into one invoice that has two invoice lines.</span></span> <span data-ttu-id="7ec73-127">Jos laskujen luomista edellyttäviä tapahtumia ei ole, työnkulku ohittaa laskujen luonnin.</span><span class="sxs-lookup"><span data-stu-id="7ec73-127">If there are no transactions to create invoices for, the job skips invoice creation.</span></span>

<span data-ttu-id="7ec73-128">Kun **ProcessRunner** on valmis, se kutsuu työnkulun **ProcessRunCaller**, antaa päättymisajan ja sulkeutuu.</span><span class="sxs-lookup"><span data-stu-id="7ec73-128">After **ProcessRunner** has finished running, it calls **ProcessRunCaller**, provides the end time, and is closed.</span></span> <span data-ttu-id="7ec73-129">**ProcessRunCaller** käynnistää sitten ajastimen, joka kestää 24 tuntia määritetystä päättymisajasta eteenpäin.</span><span class="sxs-lookup"><span data-stu-id="7ec73-129">**ProcessRunCaller** then starts a timer that runs for 24 hours from the specified end time.</span></span> <span data-ttu-id="7ec73-130">Ajastimen loputtua, **ProcessRunCaller** sulkeutuu.</span><span class="sxs-lookup"><span data-stu-id="7ec73-130">At the end of the timer, **ProcessRunCaller** is closed.</span></span>

<span data-ttu-id="7ec73-131">Laskujen luomisen erätyö on toistuva työ.</span><span class="sxs-lookup"><span data-stu-id="7ec73-131">The batch process job for creating invoices is a recurrent job.</span></span> <span data-ttu-id="7ec73-132">Jos tämä erätyö suoritetaan useita kertoja, siitä luodaan useita esiintymiä, mikä voi aiheuttaa virheitä.</span><span class="sxs-lookup"><span data-stu-id="7ec73-132">If this batch process is run many times, multiple instances of the job are created and cause errors.</span></span> <span data-ttu-id="7ec73-133">Siksi erätyö kannatta käynnistää vain kerran ja käynnistää uudelleen vain, jos se pysähtyy.</span><span class="sxs-lookup"><span data-stu-id="7ec73-133">Therefore, you should start the batch process only one time, and you should restart it only if it stops running.</span></span>

> [!NOTE]
> <span data-ttu-id="7ec73-134">Erälaskutus suoritetaan vain sellaisille projektisopimusriveille, jotka on määritetty laskun aikataulun mukaan.</span><span class="sxs-lookup"><span data-stu-id="7ec73-134">Batch invoicing only runs for project contract lines that are configured by invoice schedules.</span></span> <span data-ttu-id="7ec73-135">Jos sopimusrivillä on kiinteähintainen laskutusmenetelmä, sillä on oltava määritettyinä välitavoitteet.</span><span class="sxs-lookup"><span data-stu-id="7ec73-135">A contract line with a fixed price billing method must have milestones configured.</span></span> <span data-ttu-id="7ec73-136">Jos projektisopimusrivillä on aika- ja materiaalipohjainen laskutusmenetelmä, sille on määritettävä päivämäärään perustuva laskutusaikataulu.</span><span class="sxs-lookup"><span data-stu-id="7ec73-136">A project contract line with a time and material billing method will need a date-based invoice schedule set up.</span></span> <span data-ttu-id="7ec73-137">Sama koskee myös projektipohjaista sopimusriviä.</span><span class="sxs-lookup"><span data-stu-id="7ec73-137">The same applies to a project-based contract line.</span></span>     
