---
title: Projektin resurssien määrittäminen
description: Tämä aihe sisältää tietoja projektiresurssien määrittämisestä tai pyytämisestä.
author: Yowelle
manager: AnnBe
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0bf146c3bfb2fd558c471d8a9e980834cb1b87df
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5288735"
---
# <a name="set-up-project-resources"></a><span data-ttu-id="98d00-103">Projektin resurssien määrittäminen</span><span class="sxs-lookup"><span data-stu-id="98d00-103">Set up project resources</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="98d00-104">Sinun on määritettävä kalenteri ja osoitettava se työntekijälle.</span><span class="sxs-lookup"><span data-stu-id="98d00-104">You must set up a calendar and associate it with an employee or a worker.</span></span> <span data-ttu-id="98d00-105">Kalenteria käytetään projektin ja projektiin varattujen resurssien työaikojen aikatauluttamiseen.</span><span class="sxs-lookup"><span data-stu-id="98d00-105">The calendar is used to schedule the project and the working time of the resources that are reserved for the project.</span></span> <span data-ttu-id="98d00-106">Kalenterin määrittämisen aikana projektipäälliköt voivat tasata resursseja osana resurssien optimointia.</span><span class="sxs-lookup"><span data-stu-id="98d00-106">During calendar setup, project managers can do resource leveling as part of resource optimization.</span></span> <span data-ttu-id="98d00-107">Resursseille voi määrittää rajoituksia kalenteriaikataulun perusteella.</span><span class="sxs-lookup"><span data-stu-id="98d00-107">Based on the calendar schedule, restrictions can be put on resources.</span></span> <span data-ttu-id="98d00-108">Voit määrittää kalenterin **Kalenterit**-sivulla.</span><span class="sxs-lookup"><span data-stu-id="98d00-108">You can set up a calendar on the **Calendars** page.</span></span>

<span data-ttu-id="98d00-109">Kun määrität työntekijän projektin resurssiksi, voit valita niistä työntekijöistä, jotka ovat töissä siinä yrityksessä, jolle määrität resursseja.</span><span class="sxs-lookup"><span data-stu-id="98d00-109">When you set up a worker as a project resource, you can select from workers who work in the company that you're setting up resources for.</span></span> <span data-ttu-id="98d00-110">Vaihtoehtoisesti voit valita työntekijöitä muista yrityksistä organisaatiossasi.</span><span class="sxs-lookup"><span data-stu-id="98d00-110">Alternatively, you can select workers from other companies in your organization.</span></span> <span data-ttu-id="98d00-111">Näitä työntekijöitä kutsutaan yritystenvälisiksi resursseiksi.</span><span class="sxs-lookup"><span data-stu-id="98d00-111">These workers are known as intercompany resources.</span></span>

<span data-ttu-id="98d00-112">Seuraavissa menettelyissä kerrotaan, miten työntekijä määritetään projektiresurssiksi yrityksessäsi ja miten yritystenvälinen projektiresurssi määritetään.</span><span class="sxs-lookup"><span data-stu-id="98d00-112">The following procedures explain how to set up a worker as a project resource in your company and how to set up an intercompany project resource.</span></span>

## <a name="set-up-a-worker-as-a-project-resource"></a><span data-ttu-id="98d00-113">Työntekijän määrittäminen projektiresurssiksi</span><span class="sxs-lookup"><span data-stu-id="98d00-113">Set up a worker as a project resource</span></span>

1. <span data-ttu-id="98d00-114">Valitse **Työntekijät**-sivun **Työntekijät**-luettelosta se työntekijä, jonka olet lisäämässä projektiresurssiksi ja avaa työntekijän tietue.</span><span class="sxs-lookup"><span data-stu-id="98d00-114">On the **Workers** page, in the **Workers** list, select the worker that you're adding as a project resource, and open the worker record.</span></span>
2. <span data-ttu-id="98d00-115">Valitse toimintoruudussa **Projekti** &gt; **Määritys** &gt; **Projektin määritys**.</span><span class="sxs-lookup"><span data-stu-id="98d00-115">On the Action Pane, select **Project** &gt; **Setup** &gt; **Project setup**.</span></span>
3. <span data-ttu-id="98d00-116">Valitse kalenteri ja sulje sitten sivu.</span><span class="sxs-lookup"><span data-stu-id="98d00-116">Select a calendar, and then close the page.</span></span>

<span data-ttu-id="98d00-117">Voit myös määrittää resurssille oletusprojekteja ennakkovarauksina.</span><span class="sxs-lookup"><span data-stu-id="98d00-117">You can also specify default projects for a resource as a type of pre-assignment.</span></span> <span data-ttu-id="98d00-118">Ennakkovarauksia voi käyttää, kun resurssi- tai projektipäällikkö tietää etukäteen, missä projekteissa resurssi tulee työskentelemään.</span><span class="sxs-lookup"><span data-stu-id="98d00-118">Pre-assignments can be used when the resource manager or project manager knows which projects the resource will be working on in advance.</span></span> <span data-ttu-id="98d00-119">Ennakkovaraukset voivat perustua myös projektin rajoittajan tai asiakkaan pyyntöön.</span><span class="sxs-lookup"><span data-stu-id="98d00-119">Pre-assignments can also be based on the request of a project sponsor or customer.</span></span> <span data-ttu-id="98d00-120">Jos haluat tehdä projektille ennakkovarauksen, valitse **Määritä projekteja** -sivulla **Projektit**-välilehden **Jäljellä olevat projektit** -luettelosta asianmukainen projekti.</span><span class="sxs-lookup"><span data-stu-id="98d00-120">To pre-assign a project, on the **Assign projects** page, on the **Projects** tab, in the **Remaining projects** list, select the appropriate project.</span></span>

## <a name="set-up-an-intercompany-resource"></a><span data-ttu-id="98d00-121">Yritystenvälisen resurssin määrittäminen</span><span class="sxs-lookup"><span data-stu-id="98d00-121">Set up an intercompany resource</span></span>

<span data-ttu-id="98d00-122">Kun määrität työntekijän yritystenväliseksi resurssiksi, sinun täytyy suorittaa määritys sekä työntekijän lähtö- että kohdeyrityksessä.</span><span class="sxs-lookup"><span data-stu-id="98d00-122">When you set up a worker as an intercompany resource, you must complete the setup in both the lending company and the borrowing company.</span></span>

### <a name="in-the-lending-company"></a><span data-ttu-id="98d00-123">Lähtöyrityksessä</span><span class="sxs-lookup"><span data-stu-id="98d00-123">In the lending company</span></span>

1. <span data-ttu-id="98d00-124">Varmista Financessa, että lähdeyritys on valittuna ja suorita sitten edellisen kohdan menettely Määritä työntekijä projektiresurssiksi.</span><span class="sxs-lookup"><span data-stu-id="98d00-124">In Finance, verify that the lending company is selected, and then complete the procedure in the previous section, "Set up a worker as a project resource."</span></span>
2. <span data-ttu-id="98d00-125">Valitse **Yritystenvälinen kirjanpito**-sivulla **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="98d00-125">On the **Intercompany accounting** page, select **New**.</span></span>
3. <span data-ttu-id="98d00-126">entiteettiValitse **Oikeushenkilön tunnus** kentässä lähtöyritys.</span><span class="sxs-lookup"><span data-stu-id="98d00-126">In the **Legal entity ID** field, select the lending company.</span></span> <span data-ttu-id="98d00-127">Täytä jäljellä olevat kentät asianmukaisesti ja valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="98d00-127">Fill in the remaining fields as appropriate, and then select **Save**.</span></span>
4. <span data-ttu-id="98d00-128">Valitse **Siirtohinta**-sivulla **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="98d00-128">On the **Transfer price** page, select **New**.</span></span>
5. <span data-ttu-id="98d00-129">Valitse **Kohdeoikeushenkilö** -kentässä asianmukainen yritys.</span><span class="sxs-lookup"><span data-stu-id="98d00-129">In the **Borrowing legal entity** field, select the appropriate company.</span></span>
6. <span data-ttu-id="98d00-130">Jos haluat lainata kohdeyritykselle vain tämän osan alussa luomasi resurssin, valitse **Resurssi**-kentässä luomasi resurssin nimi.</span><span class="sxs-lookup"><span data-stu-id="98d00-130">To lend the borrowing company only the resource that you created at the beginning of this section, in the **Resource** field, select the name of the resource that you created.</span></span> <span data-ttu-id="98d00-131">Jos haluat antaa kaikki lähtöyrityksen resurssit kohdeyrityksen käyttöön, jätä **Resurssi**-kenttä tyhjäksi.</span><span class="sxs-lookup"><span data-stu-id="98d00-131">To make all resources in the lending company available to the borrowing company, leave the **Resource** field blank.</span></span>
7. <span data-ttu-id="98d00-132">Märitä **Projektinhallinnan ja kirjanpidon parametrit**-sivun **Yritystenvälinen**-välilehdessä **Ota yritystenvälisten resurssien aikataulutus ja tuntilomakkeet käyttöön** -asetukseksi **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="98d00-132">On the **Project management and accounting parameters** page, on the **Intercompany** tab, set the **Enable intercompany resource scheduling and timesheets** option to **Yes**.</span></span>

### <a name="in-the-borrowing-company"></a><span data-ttu-id="98d00-133">Kohdeyrityksessä</span><span class="sxs-lookup"><span data-stu-id="98d00-133">In the borrowing company</span></span>

- <span data-ttu-id="98d00-134">Syötä **Resurssiluettelo**-sivun hakusuodattimeen lähtöyritykselle luomasi resurssin nimi sen varmistamiseksi, että nimi sisällytetään kohdeyrityksen resurssiluetteloon.</span><span class="sxs-lookup"><span data-stu-id="98d00-134">On the **Resources list** page, in the search filter, enter the name of the resource that you created for the lending company, to verify that the name is included in the resource list for the borrowing company.</span></span>

## <a name="request-project-resources"></a><span data-ttu-id="98d00-135">Projektiresurssien pyytäminen</span><span class="sxs-lookup"><span data-stu-id="98d00-135">Request project resources</span></span>
<span data-ttu-id="98d00-136">Projektiresurssien aikataulutustoiminto salli resurssipäälliköiden jakaa henkilöresursseja vain kiinnityksiin tai projekteihin.</span><span class="sxs-lookup"><span data-stu-id="98d00-136">The functionality for project resource scheduling only lets resource managers distribute staffed resources on engagements or projects.</span></span> <span data-ttu-id="98d00-137">Voit ottaa tämän toiminnon käyttöön täyttämällä suorittamalla seuraavat tehtävät tai varmistamalla, että ne on suoritettu:</span><span class="sxs-lookup"><span data-stu-id="98d00-137">To enable this functionality, complete the following tasks, or verify that they have been completed:</span></span>

- <span data-ttu-id="98d00-138">Numerosarjojen määrittäminen.</span><span class="sxs-lookup"><span data-stu-id="98d00-138">Set up number sequences.</span></span>
- <span data-ttu-id="98d00-139">Projektinhallinnan ja kirjanpidon työnkulkujen määritys.</span><span class="sxs-lookup"><span data-stu-id="98d00-139">Set up project management and accounting workflows.</span></span>
- <span data-ttu-id="98d00-140">Resurssipyyntöjen työnkulkujen käyttööotto.</span><span class="sxs-lookup"><span data-stu-id="98d00-140">Enable resource request workflows.</span></span>

<span data-ttu-id="98d00-141">Kun edeltävät tehtävät on suoritettu, voit suorittaa seuraavat tehtävät tarpeen mukaan:</span><span class="sxs-lookup"><span data-stu-id="98d00-141">After the preceding tasks have been completed, you can complete the following tasks as you require:</span></span>

- <span data-ttu-id="98d00-142">Resurssipyynnön luominen alustavasti varatusta henkilöresurssista.</span><span class="sxs-lookup"><span data-stu-id="98d00-142">Create a resource request from a soft-booked staffed resource.</span></span>
- <span data-ttu-id="98d00-143">Resurssipyyntöjen seuranta.</span><span class="sxs-lookup"><span data-stu-id="98d00-143">Monitor resource requests.</span></span>
- <span data-ttu-id="98d00-144">Resurssipyyntöjen täyttäminen.</span><span class="sxs-lookup"><span data-stu-id="98d00-144">Fulfill resource requests.</span></span>
- <span data-ttu-id="98d00-145">Pyydä henkilöresurssia työrakenteesta.</span><span class="sxs-lookup"><span data-stu-id="98d00-145">Request a staffed resource from a WBS.</span></span>
- <span data-ttu-id="98d00-146">Varaa resursseja projektiin ilman henkilöresurssia koskevaa pyyntöä.</span><span class="sxs-lookup"><span data-stu-id="98d00-146">Book resources to a project without having a request for a staffed resource.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]