---
title: Anna jonkun muun lisätä aikakirjaus tai kulu puolestasi
description: Toisen käyttäjän tekemän aika- tai kulumerkinnän salliminen Project Servicessä
author: revathiMuthiah
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 7/31/2018
ms.topic: article
ms.author: revathim
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: f56fae115b383d66a59cbcb08fffe95c83c83e17
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/16/2020
ms.locfileid: "4075321"
---
# <a name="allow-someone-else-to-enter-your-time-entry-or-expense-project-service"></a><span data-ttu-id="514a9-103">Toisen käyttäjän tekemän aika- tai kulumerkinnän salliminen (Project Service)</span><span class="sxs-lookup"><span data-stu-id="514a9-103">Allow someone else to enter your time entry or expense (Project Service)</span></span>

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="514a9-104">Määritä edustaja, jotta joku muu saa tehdä puolestasi aika- tai kulumerkintöjä [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]issa.</span><span class="sxs-lookup"><span data-stu-id="514a9-104">Set up a delegate to let someone else make time or expense entries on your behalf in [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span></span>  
  
## <a name="create-a-delegate"></a><span data-ttu-id="514a9-105">Edustajan luominen</span><span class="sxs-lookup"><span data-stu-id="514a9-105">Create a delegate</span></span>  
  
1.  <span data-ttu-id="514a9-106">Valitse päävalikosta **Project Service** > **Delegoinnit**.</span><span class="sxs-lookup"><span data-stu-id="514a9-106">From the main menu, click **Project Service** > **Delegations**.</span></span>  
  
2.  <span data-ttu-id="514a9-107">Napsauta komentopalkissa **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="514a9-107">On the command bar, click **New**.</span></span>  
  
3. <span data-ttu-id="514a9-108">**Nimi** : anna tietueen nimi.</span><span class="sxs-lookup"><span data-stu-id="514a9-108">**Name** : Enter a name for the record.</span></span>  
  
4. <span data-ttu-id="514a9-109">**Tyyppi** : valitse, saako edustaja tehdä aika- tai kulumerkintöjä puolestasi.</span><span class="sxs-lookup"><span data-stu-id="514a9-109">**Type** : Select whether the delegate can enter time or expense entries on your behalf.</span></span>  
  
5. <span data-ttu-id="514a9-110">**Edustaja** : valitse sen henkilön nimi, jonka haluat edustajaksi.</span><span class="sxs-lookup"><span data-stu-id="514a9-110">**Delegate** : Select the name of the person you want to be the delegate.</span></span>  
  
6. <span data-ttu-id="514a9-111">**Alkamis- ja päättymispäivät** : valitse päivämäärät, jolloin delegointi alkaa ja päättyy.</span><span class="sxs-lookup"><span data-stu-id="514a9-111">**Start and end dates** : Choose dates when delegation starts and ends.</span></span>  
  
7.  <span data-ttu-id="514a9-112">Kun olet valmis, valitse **Tallenna ja sulje**.</span><span class="sxs-lookup"><span data-stu-id="514a9-112">When you're done, click **Save & Close**.</span></span>  
  
## <a name="turn-off-delegation"></a><span data-ttu-id="514a9-113">Delegoinnin poistaminen käytöstä</span><span class="sxs-lookup"><span data-stu-id="514a9-113">Turn off delegation</span></span>  
  
1.  <span data-ttu-id="514a9-114">Valitse päävalikosta **Project Service** > **Delegoinnit**.</span><span class="sxs-lookup"><span data-stu-id="514a9-114">From the main menu, click **Project Service** > **Delegations**.</span></span>  
  
2.  <span data-ttu-id="514a9-115">Valitse delegointitietue, jonka haluat poistaa käytöstä.</span><span class="sxs-lookup"><span data-stu-id="514a9-115">Select the delegation record you want to turn off.</span></span>  
  
3.  <span data-ttu-id="514a9-116">Valitse komentopalkissa **Poista käytöstä**.</span><span class="sxs-lookup"><span data-stu-id="514a9-116">On the command bar, click **Deactivate**.</span></span>  
  
4.  <span data-ttu-id="514a9-117">Valitse **Vahvista aktivoinnin poisto** -valintaikkunassa **Poista aktivointi** :</span><span class="sxs-lookup"><span data-stu-id="514a9-117">On the **Confirm Deactivation** dialog box, click **Deactivate**.</span></span>  
  
## <a name="enter-time-for-someone-else"></a><span data-ttu-id="514a9-118">Ajan merkitsemin jollekin toiselle</span><span class="sxs-lookup"><span data-stu-id="514a9-118">Enter time for someone else</span></span>  
  
1.  <span data-ttu-id="514a9-119">Valitse päävalikossa **Project Service** > **Aikamerkinnät**.</span><span class="sxs-lookup"><span data-stu-id="514a9-119">From the main menu, click **Project Service** > **Time Entries**.</span></span>  
  
2.  <span data-ttu-id="514a9-120">Valitse komentopalkissa avattavasta **RESURSSINIMI** -valikosta sen henkilön nimi, jolle teet aikamerkinnän.</span><span class="sxs-lookup"><span data-stu-id="514a9-120">On the command bar, select the **RESOURCE NAME** drop-down menu, and select the name of the person who you’re entering time for.</span></span>  
  
3.  <span data-ttu-id="514a9-121">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="514a9-121">Click **OK**.</span></span>  
  
4.  <span data-ttu-id="514a9-122">Kalenteri tulee näyttöön.</span><span class="sxs-lookup"><span data-stu-id="514a9-122">This brings up the calendar.</span></span> <span data-ttu-id="514a9-123">Saat näkyviin kalenterin edellisen tai seuraavan viikon valitsemalla **Edellinen** tai **Seuraava**.</span><span class="sxs-lookup"><span data-stu-id="514a9-123">To see the calendar for the previous or next week, click **Previous** or **Next**.</span></span> <span data-ttu-id="514a9-124">Valitsemalla **tänään** palaat kuluvaan viikkoon.</span><span class="sxs-lookup"><span data-stu-id="514a9-124">Click **Today** to get back to the current week.</span></span>  
  
5.  <span data-ttu-id="514a9-125">Voit määrittää ajan joko valitsemalla **Uusi** tai kaksoisnapsauttamalla kalenteria kohdassa, johon haluat määrittää ajan.</span><span class="sxs-lookup"><span data-stu-id="514a9-125">To enter your time, either click **New** or double-click in the calendar under the day you want to enter time for.</span></span>  
  
6.  <span data-ttu-id="514a9-126">Täytä **Aikamerkintä** -lomakkeen kentät ja valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="514a9-126">Fill in the fields in the **Time Entry** form and click **Save**.</span></span>  
  
7.  <span data-ttu-id="514a9-127">Jatka kirjoittamalla koko viikon ajat.</span><span class="sxs-lookup"><span data-stu-id="514a9-127">Continue entering time for the week.</span></span> <span data-ttu-id="514a9-128">Kun se on valmis ja kaikki näyttää olevan kunnossa, valitse **Lähetä**.</span><span class="sxs-lookup"><span data-stu-id="514a9-128">When you’re done and everything looks correct, click **Submit**.</span></span>  
  
## <a name="enter-expenses-for-someone-else"></a><span data-ttu-id="514a9-129">Kulujen merkitseminen jollekin toiselle</span><span class="sxs-lookup"><span data-stu-id="514a9-129">Enter expenses for someone else</span></span>  
  
1.  <span data-ttu-id="514a9-130">Valitse päävalikossa **Project Service** > **Kulut**.</span><span class="sxs-lookup"><span data-stu-id="514a9-130">From the main menu, click **Project Service** > **Expenses**.</span></span>  
  
2.  <span data-ttu-id="514a9-131">Valitse komentopalkissa avattavasta **RESURSSINIMI** -valikosta sen henkilön nimi, jolle teet kulumerkinnän.</span><span class="sxs-lookup"><span data-stu-id="514a9-131">On the command bar, select the **RESOURCE NAME** drop-down menu, and select the name of the person who you’re entering expenses for.</span></span>  
  
3.  <span data-ttu-id="514a9-132">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="514a9-132">Click **OK**.</span></span>  
  
4.  <span data-ttu-id="514a9-133">Saat näkyviin kalenterin edellisen tai seuraavan viikon valitsemalla **Edellinen** tai **Seuraava**.</span><span class="sxs-lookup"><span data-stu-id="514a9-133">To see the calendar for the previous or next week, click **Previous** or **Next**.</span></span> <span data-ttu-id="514a9-134">Valitsemalla **tänään** palaat kuluvaan viikkoon.</span><span class="sxs-lookup"><span data-stu-id="514a9-134">Click **Today** to get back to the current week.</span></span>  
  
5.  <span data-ttu-id="514a9-135">Anna kulu valitsemalla **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="514a9-135">To enter an expense, either click **New**</span></span>  
  
6.  <span data-ttu-id="514a9-136">Täytä **Uusi kulu** -lomakkeen kentät.</span><span class="sxs-lookup"><span data-stu-id="514a9-136">Fill in the fields in the **New Expense** form.</span></span> <span data-ttu-id="514a9-137">Voit myös lisätä kuitteja.</span><span class="sxs-lookup"><span data-stu-id="514a9-137">You can also add receipts.</span></span>  
  
7.  <span data-ttu-id="514a9-138">Kun olet valmis, valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="514a9-138">When you’re done, click **Save**.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="514a9-139">Katso myös</span><span class="sxs-lookup"><span data-stu-id="514a9-139">See Also</span></span>  
 [<span data-ttu-id="514a9-140">Aika-, kulu- ja yhteistyöopas</span><span class="sxs-lookup"><span data-stu-id="514a9-140">Time, Expense, and Collaboration Guide</span></span>](../psa/time-expense-collaboration-guide.md)
