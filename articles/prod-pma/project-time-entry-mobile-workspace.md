---
title: Project Time Entry -mobiilityötila
description: Tässä aiheessa on tietoja Project Time Entry -mobiilityötilasta. Tämän työtilan avulla käyttäjät voivat kirjata ja tallentaa aikaa projektiin mobiililaitteellaan.
author: Yowelle
manager: AnnBe
ms.date: 12/01/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 272101
ms.assetid: 4505f021-b9bb-4b87-be24-6bf0bd88ee60
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.openlocfilehash: 23a5a9f25cfdd6df74257b3500c7a035d711b5f6
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/16/2020
ms.locfileid: "4075329"
---
# <a name="project-time-entry-mobile-workspace"></a><span data-ttu-id="7a301-104">Project Time Entry -mobiilityötila</span><span class="sxs-lookup"><span data-stu-id="7a301-104">Project time entry mobile workspace</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7a301-105">Tässä aiheessa on tietoja **Project Time Entry** -mobiilityötilasta.</span><span class="sxs-lookup"><span data-stu-id="7a301-105">This topic provides information about the **Project time entry** mobile workspace.</span></span> <span data-ttu-id="7a301-106">Tämän työtilan avulla käyttäjät voivat kirjata ja tallentaa aikaa projektiin mobiililaitteellaan.</span><span class="sxs-lookup"><span data-stu-id="7a301-106">This workspace lets users enter and save time against a project by using their mobile device.</span></span>

<span data-ttu-id="7a301-107">Tämä mobiilityötila on tarkoitettu käytettäväksi Dynamics 365 Unified Ops -mobiilisovelluksen kanssa.</span><span class="sxs-lookup"><span data-stu-id="7a301-107">This mobile workspace is intended to be used with the Dynamics 365 Unified Ops mobile app.</span></span> 

## <a name="overview"></a><span data-ttu-id="7a301-108">Yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="7a301-108">Overview</span></span>
<span data-ttu-id="7a301-109">Osana päivittäistä työtään projektiresurssit ovat usein asiakkaan tiloissa tai matkustamassa.</span><span class="sxs-lookup"><span data-stu-id="7a301-109">As part of their daily work, project resources are often on-site or traveling.</span></span> <span data-ttu-id="7a301-110">**Project Time Entry** -mobiilityötilan avulla käyttäjät voivat määrittää laskutettavat ja ei-laskutettavat työtuntinsa projektissa valitsemallaan mobiililaitteella.</span><span class="sxs-lookup"><span data-stu-id="7a301-110">The **Project time entry** mobile workspace lets users enter their billable or non-billable time against a project on the mobile device of their choice.</span></span> <span data-ttu-id="7a301-111">Siksi projektiresurssit voivat kirjata työaikoja milloin ja missä tahansa.</span><span class="sxs-lookup"><span data-stu-id="7a301-111">Therefore, project resources can record time entries anytime and anywhere.</span></span> <span data-ttu-id="7a301-112">He voivat myös tarkastella jo kirjattuja aikamerkintöjä.</span><span class="sxs-lookup"><span data-stu-id="7a301-112">They can also view time entries that have already been recorded.</span></span> 

<span data-ttu-id="7a301-113">Tarkat tehtävät, joita käyttäjät voivat suorittaa **Project Time Entry** -mobiilityötilassa:</span><span class="sxs-lookup"><span data-stu-id="7a301-113">Specifically, in the **Project time entry** mobile workspace, users can perform these tasks:</span></span>

-   <span data-ttu-id="7a301-114">Tiettyyn tehtävään käytettyjen työtuntien kirjaaminen mille tahansa päivämäärälle.</span><span class="sxs-lookup"><span data-stu-id="7a301-114">For any selected date, enter the number of hours that you spent on a specific task.</span></span>
-   <span data-ttu-id="7a301-115">Projektien haku työaikojen kirjausta varten projektin nimen tai asiakkaan perusteella.</span><span class="sxs-lookup"><span data-stu-id="7a301-115">Search by project name or customer to find the project to enter time for.</span></span>
-   <span data-ttu-id="7a301-116">Käytetäyn ajan luokan ja aktiviteetin määrittäminen.</span><span class="sxs-lookup"><span data-stu-id="7a301-116">Specify the category and activity for the time that you spent.</span></span>
-   <span data-ttu-id="7a301-117">Ajan kirjaaminen projektiin laskutettavaksi tai ei-laskutettavaksi.</span><span class="sxs-lookup"><span data-stu-id="7a301-117">Record the time as billable or non-billable for the project.</span></span>
-   <span data-ttu-id="7a301-118">Vaihtoehtoiesesti ulkoisten tai sisäisten kommenttien lisääminen.</span><span class="sxs-lookup"><span data-stu-id="7a301-118">Optionally enter any external or internal comments.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="7a301-119">Edellytykset</span><span class="sxs-lookup"><span data-stu-id="7a301-119">Prerequisites</span></span>
<span data-ttu-id="7a301-120">Edellytykset vaihtelevat organisaatiossa käyttöön otetun Microsoft Dynamics 365 -version mukaan.</span><span class="sxs-lookup"><span data-stu-id="7a301-120">The prerequisites differ, based on the version of Microsoft Dynamics 365 that has been deployed for your organization.</span></span>

### <a name="prerequisites-if-you-use-dynamics-365-finance"></a><span data-ttu-id="7a301-121">Edellytykset käytettäessä Dynamics 365 Financea</span><span class="sxs-lookup"><span data-stu-id="7a301-121">Prerequisites if you use Dynamics 365 Finance</span></span>
<span data-ttu-id="7a301-122">Jos organisaatiossasi on otettu käyttöön Finance, järjestelmänvalvojan on julkaistava **Project Time Entry** -mobiilityötila.</span><span class="sxs-lookup"><span data-stu-id="7a301-122">If Finance has been deployed for your organization, the system administrator must publish the **Project time entry** mobile workspace.</span></span> <span data-ttu-id="7a301-123">Ohjeet [Mobiilityötilan julkaiseminen ](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/mobile-apps/publish-mobile-workspace).</span><span class="sxs-lookup"><span data-stu-id="7a301-123">For instructions, see [Publish a mobile workspace](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/mobile-apps/publish-mobile-workspace).</span></span>

### <a name="prerequisites-if-you-use-version-1611-with-platform-update-3-or-later"></a><span data-ttu-id="7a301-124">Edellytykset, jos käytössä on versio 1611 ja Platform Update 3 tai uudempi</span><span class="sxs-lookup"><span data-stu-id="7a301-124">Prerequisites if you use version 1611 with Platform update 3 or later</span></span>
<span data-ttu-id="7a301-125">Jos organisaatiossasi on otettu käyttöön versio 1611, jossa on Platform Update 3 tai uudempi, järjestelmänvalvoja on täytettävä seuraavat edellytykset.</span><span class="sxs-lookup"><span data-stu-id="7a301-125">If version 1611 with Platform update 3 or later has been deployed for your organization, the system administrator must complete the following prerequisites.</span></span> 

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="7a301-126">Edellytykset</span><span class="sxs-lookup"><span data-stu-id="7a301-126">Prerequisite</span></span></th>
<th><span data-ttu-id="7a301-127">Rooli</span><span class="sxs-lookup"><span data-stu-id="7a301-127">Role</span></span></th>
<th><span data-ttu-id="7a301-128">Kuvaus</span><span class="sxs-lookup"><span data-stu-id="7a301-128">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">

<td><span data-ttu-id="7a301-129">Tietokannan 4018050 käyttöönotto.</span><span class="sxs-lookup"><span data-stu-id="7a301-129">Implement KB 4018050.</span></span></td>
<td><span data-ttu-id="7a301-130">Järjestelmänvalvoja</span><span class="sxs-lookup"><span data-stu-id="7a301-130">System administrator</span></span></td>
<td><span data-ttu-id="7a301-131">Tietokanta 4018050 on X++-päivitys tai metatietojen hotfix-korjaus, joka sisältää <strong>Project Time Entry</strong> -mobiilityötilan.</span><span class="sxs-lookup"><span data-stu-id="7a301-131">KB 4018050 is an X++ update or metadata hotfix that contains the <strong>Project time entry</strong> mobile workspace.</span></span> <span data-ttu-id="7a301-132">Tietokannan 4018050 käyttöönottoa varten järjestelmänvalvojasi on suoritettava seuraavat vaiheet.</span><span class="sxs-lookup"><span data-stu-id="7a301-132">To implement KB 4018050, your system administrator must follow these steps.</span></span>
<ol>
<li><span data-ttu-id="7a301-133"><a href="https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/download-hotfix-lcs">Metatietojen hotfix-korjauksen lataaminen Microsoft Dynamics Lifecycle Services (LCS) palveluista</a>.</span><span class="sxs-lookup"><span data-stu-id="7a301-133"><a href="https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/download-hotfix-lcs">Download the metadata hotfix from Microsoft Dynamics Lifecycle Services (LCS)</a>.</span></span></li>
<li><span data-ttu-id="7a301-134"><a href="https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/install-metadata-hotfix-package">Metatietojen hotfix-korjauksen asentaminen</a>.</span><span class="sxs-lookup"><span data-stu-id="7a301-134"><a href="https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/install-metadata-hotfix-package">Install the metadata hotfix</a>.</span></span></li>
<li><span data-ttu-id="7a301-135"><a href="https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/create-apply-deployable-package">Sellaisen käyttöönotettavan paketin luominen</a>, joka sisältää mallit <strong>ApplicationSuite</strong> ja <strong>ProjectMobile</strong>, ja sitten käyttöönotettavan paketin lataaminen LCS-palveluun.</span><span class="sxs-lookup"><span data-stu-id="7a301-135"><a href="https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/create-apply-deployable-package">Create a deployable package</a> that contains the <strong>ApplicationSuite</strong> and <strong>ProjectMobile</strong> models, and then upload the deployable package to LCS.</span></span></li>
<li><span data-ttu-id="7a301-136"><a href="https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/apply-deployable-package-system">Käyttöönotettavan paketin käyttöönotto</a>.</span><span class="sxs-lookup"><span data-stu-id="7a301-136"><a href="https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/apply-deployable-package-system">Apply the deployable package</a>.</span></span></li>

</ol></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7a301-137"><strong>Project Time Entry</strong> -mobiilityötilan julkaiseminen.</span><span class="sxs-lookup"><span data-stu-id="7a301-137">Publish the <strong>Project time entry</strong> mobile workspace.</span></span></td>
<td><span data-ttu-id="7a301-138">Järjestelmänvalvoja</span><span class="sxs-lookup"><span data-stu-id="7a301-138">System administrator</span></span></td>
<td><span data-ttu-id="7a301-139">Katso <a href="https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/mobile-apps/publish-mobile-workspace">Mobiilityötilan julkaiseminen </a>.</span><span class="sxs-lookup"><span data-stu-id="7a301-139">See <a href="https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/mobile-apps/publish-mobile-workspace">Publish a mobile workspace</a>.</span></span></td>
</tr>
</tbody>
</table>

## <a name="download-and-install-the-mobile-app"></a><span data-ttu-id="7a301-140">Mobiilisovelluksen lataaminen ja asennus</span><span class="sxs-lookup"><span data-stu-id="7a301-140">Download and install the mobile app</span></span>

<span data-ttu-id="7a301-141">Lataa ja asenna Finance and Operations -mobiilisovellus:</span><span class="sxs-lookup"><span data-stu-id="7a301-141">Download and install the Finance and Operations mobile app:</span></span>

-   [<span data-ttu-id="7a301-142">Android-puhelimille</span><span class="sxs-lookup"><span data-stu-id="7a301-142">For Android phones</span></span>](https://go.microsoft.com/fwlink/?linkid=850662)
-   [<span data-ttu-id="7a301-143">iPhone-puhelimille</span><span class="sxs-lookup"><span data-stu-id="7a301-143">For iPhones</span></span>](https://go.microsoft.com/fwlink/?linkid=850663)

## <a name="sign-in-to-the-mobile-app"></a><span data-ttu-id="7a301-144">Mobiilisovellukseen kirjautuminen</span><span class="sxs-lookup"><span data-stu-id="7a301-144">Sign in to the mobile app</span></span>
1.  <span data-ttu-id="7a301-145">Käynnistä sovellus mobiililaitteessa.</span><span class="sxs-lookup"><span data-stu-id="7a301-145">Start the app on your mobile device.</span></span>
2.  <span data-ttu-id="7a301-146">Syötä Dynamics 365:n URL-osoite.</span><span class="sxs-lookup"><span data-stu-id="7a301-146">Enter your Dynamics 365 URL.</span></span>
3.  <span data-ttu-id="7a301-147">Kun kirjaudut sisään ensimmäisen kerran, sinulta kysytään käyttäjätunnusta ja salasanaa.</span><span class="sxs-lookup"><span data-stu-id="7a301-147">The first time that you sign in, you're prompted for your user name and password.</span></span> <span data-ttu-id="7a301-148">Anna tunnistetiedot.</span><span class="sxs-lookup"><span data-stu-id="7a301-148">Enter your credentials.</span></span>
4.  <span data-ttu-id="7a301-149">Kun olet kirjautunut sisään, näkyviin tulevat yrityksessä käytettävissä olevat työtilat.</span><span class="sxs-lookup"><span data-stu-id="7a301-149">After you sign in, the available workspaces for your company are shown.</span></span> <span data-ttu-id="7a301-150">Huomaa, että jos järjestelmänvalvoja julkaisee uuden työtilan myöhemmin, sinun on päivitettävä mobiilityötilojen luettelo.</span><span class="sxs-lookup"><span data-stu-id="7a301-150">Note that if your system administrator publishes a new workspace later, you will have to refresh the list of mobile workspaces.</span></span>

<span data-ttu-id="7a301-151">[![Päivittäminen vetämällä](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)</span><span class="sxs-lookup"><span data-stu-id="7a301-151">[![Pull to refresh](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)</span></span>

## <a name="enter-time-by-using-the-project-time-entry-mobile-workspace"></a><span data-ttu-id="7a301-152">Ajan kirjaaminen käyttämällä Project Time Entry -mobiilityötilaa</span><span class="sxs-lookup"><span data-stu-id="7a301-152">Enter time by using the Project time entry mobile workspace</span></span>
1.  <span data-ttu-id="7a301-153">Valitse mobiililaitteessa **Project Time Entry** -työtila.</span><span class="sxs-lookup"><span data-stu-id="7a301-153">On your mobile device, select the **Project time entry** workspace.</span></span>
2.  <span data-ttu-id="7a301-154">Valitse **Aikamerkintä**.</span><span class="sxs-lookup"><span data-stu-id="7a301-154">Select **Time entry**.</span></span> <span data-ttu-id="7a301-155">Näkyviin tulevat kuluvan viikon kalenteripäivät.</span><span class="sxs-lookup"><span data-stu-id="7a301-155">The calendar dates for the current week are shown.</span></span>
3.  <span data-ttu-id="7a301-156">Valitse valitulle päivämäärälle **toiminnot** &gt; **Uusi merkintä**.</span><span class="sxs-lookup"><span data-stu-id="7a301-156">For a selected date, select **Actions** &gt; **New entry**.</span></span>
4.  <span data-ttu-id="7a301-157">Syötä tallennettavien tuntien määrä.</span><span class="sxs-lookup"><span data-stu-id="7a301-157">Enter the number of hours to record.</span></span>
5.  <span data-ttu-id="7a301-158">Valitse aikamerkinnän projekti.</span><span class="sxs-lookup"><span data-stu-id="7a301-158">Select the project for the time entry.</span></span> <span data-ttu-id="7a301-159">Luettelossa näkyvät projektit, jotka ladataan sovellukseesi offline-käyttöä varten.</span><span class="sxs-lookup"><span data-stu-id="7a301-159">A list shows the projects that are loaded into your app for offline use.</span></span> <span data-ttu-id="7a301-160">Oletusarvoisesti ladataan 50 nimikettä, mutta kehittäjä voi muuttaa tätä määrää.</span><span class="sxs-lookup"><span data-stu-id="7a301-160">By default, 50 items are loaded, but a developer can change this number.</span></span> <span data-ttu-id="7a301-161">Lisätietoja: [Mobiiliympäristö](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/mobile-apps/mobile-app-home-page).</span><span class="sxs-lookup"><span data-stu-id="7a301-161">For more information, see [Mobile platform](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/mobile-apps/mobile-app-home-page).</span></span>
6.  <span data-ttu-id="7a301-162">Jos projektia ei ole luettelossa, valitse **Hae**.</span><span class="sxs-lookup"><span data-stu-id="7a301-162">If your project isn't in the list, select **Search**.</span></span> <span data-ttu-id="7a301-163">Hae nimen mukaan tai vaihda hakuun projektin nimen tai asiakkaan perusteella.</span><span class="sxs-lookup"><span data-stu-id="7a301-163">Search by name, or switch to search by project name or customer.</span></span>
7.  <span data-ttu-id="7a301-164">Valitse luokka .</span><span class="sxs-lookup"><span data-stu-id="7a301-164">Select a category.</span></span> <span data-ttu-id="7a301-165">Luettelossa näkyvät luokat, jotka ladataan sovellukseesi offline-käyttöä varten.</span><span class="sxs-lookup"><span data-stu-id="7a301-165">A list shows the categories that are loaded into your app for offline use.</span></span> <span data-ttu-id="7a301-166">Oletusarvoisesti ladataan 50 nimikettä, mutta kehittäjä voi muuttaa tätä määrää.</span><span class="sxs-lookup"><span data-stu-id="7a301-166">By default, 50 items are loaded, but a developer can change this number.</span></span> <span data-ttu-id="7a301-167">Lisätietoja: [Mobiiliympäristö](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/mobile-apps/mobile-app-home-page).</span><span class="sxs-lookup"><span data-stu-id="7a301-167">For more information, see [Mobile platform](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/mobile-apps/mobile-app-home-page).</span></span>
8.  <span data-ttu-id="7a301-168">Jos luokkaa ei ole luettelossa, valitse **Hae**.</span><span class="sxs-lookup"><span data-stu-id="7a301-168">If your category isn't in the list, select **Search**.</span></span> <span data-ttu-id="7a301-169">Hae luokan mukaan tai vaihda hakuun luokan nimen perusteella.</span><span class="sxs-lookup"><span data-stu-id="7a301-169">Search by category, or switch to search by category name.</span></span>
9.  <span data-ttu-id="7a301-170">Valitse aktiviteetti.</span><span class="sxs-lookup"><span data-stu-id="7a301-170">Select an activity.</span></span> <span data-ttu-id="7a301-171">Luettelossa näkyvät aktiviteetit, jotka ladataan sovellukseesi offline-käyttöä varten.</span><span class="sxs-lookup"><span data-stu-id="7a301-171">A list shows the activities that are loaded into your app for offline use.</span></span> <span data-ttu-id="7a301-172">Oletusarvoisesti ladataan 50 nimikettä, mutta kehittäjä voi muuttaa tätä määrää.</span><span class="sxs-lookup"><span data-stu-id="7a301-172">By default, 50 items are loaded, but a developer can change this number.</span></span> <span data-ttu-id="7a301-173">Lisätietoja: [Mobiiliympäristö](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/mobile-apps/mobile-app-home-page).</span><span class="sxs-lookup"><span data-stu-id="7a301-173">For more information, see [Mobile platform](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/mobile-apps/mobile-app-home-page).</span></span>
10. <span data-ttu-id="7a301-174">Jos aktiviteettia ei ole luettelossa, valitse **Hae**.</span><span class="sxs-lookup"><span data-stu-id="7a301-174">If your activity isn't in the list, select **Search**.</span></span> <span data-ttu-id="7a301-175">Hae aktiviteetin numeron mukaan tai vaihda hakuun tarkoituksen mukaan.</span><span class="sxs-lookup"><span data-stu-id="7a301-175">Search by activity number, or switch to search by purpose.</span></span>

11. <span data-ttu-id="7a301-176">Valitse riviominaisuus.</span><span class="sxs-lookup"><span data-stu-id="7a301-176">Select the line property.</span></span>
12. <span data-ttu-id="7a301-177">Valinnaista: Lisää ulkoisia ja sisäisiä kommentteja.</span><span class="sxs-lookup"><span data-stu-id="7a301-177">Optional: Enter any external and internal comments.</span></span>
13. <span data-ttu-id="7a301-178">Valitse **Valmis**.</span><span class="sxs-lookup"><span data-stu-id="7a301-178">Select **Done**.</span></span>
