---
title: Tehtäväruudukossa työskentelyn vianmääritys
description: Tässä aihe sisältää vianmääritystietoja, joita tarvitaan tehtäväruudukossa.
author: ruhercul
manager: tfehr
ms.date: 01/19/2021
ms.topic: article
ms.product: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: dedd989cc7c959d9ea97a0abfb13f8f1b2150a56
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5286559"
---
# <a name="troubleshoot-working-in-the-task-grid"></a><span data-ttu-id="d290a-103">Tehtäväruudukossa työskentelyn vianmääritys</span><span class="sxs-lookup"><span data-stu-id="d290a-103">Troubleshoot working in the Task grid</span></span> 

<span data-ttu-id="d290a-104">_**Koskee:** Project Operationsin resurssiin / muuhun kuin resurssiin perustuvia skenaarioita, Lite-käyttöönotto-kaupasta proformalaskutukseen_</span><span class="sxs-lookup"><span data-stu-id="d290a-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="d290a-105">Tässä aiheessa kuvataan, miten Cost Managementin käytössä mahdollisesti kohtaamiasi ongelmia ratkaistaan.</span><span class="sxs-lookup"><span data-stu-id="d290a-105">This topic describes how to fix issues that you might encounter while working with cost management.</span></span>

## <a name="enable-cookies"></a><span data-ttu-id="d290a-106">Ota evästeet käyttöön</span><span class="sxs-lookup"><span data-stu-id="d290a-106">Enable cookies</span></span>

<span data-ttu-id="d290a-107">Project Operations edellyttää, että kolmannen osapuolen evästeet on otettu käyttöön, jotta työrakenne voidaan hahmontaa.</span><span class="sxs-lookup"><span data-stu-id="d290a-107">Project Operations requires that third-party cookies be enabled in order to render the work breakdown structure.</span></span> <span data-ttu-id="d290a-108">Kun kolmannen osapuolen evästeitä ei ole otettu käyttöön, tehtävien sijaan näet tyhjän sivun, kun valitset **Tehtävät**-välilehden **Projekti**-sivulla.</span><span class="sxs-lookup"><span data-stu-id="d290a-108">When third-party cookies aren't enabled, instead of seeing tasks, you will see a blank page when you select the **Tasks** tab on the **Project** page.</span></span>

![Tyhjä välilehti, kun kolmannen osapuolen evästeitä ei ole otettu käyttöön](media/blankschedule.png)


### <a name="workaround"></a><span data-ttu-id="d290a-110">Ratkaisutapa</span><span class="sxs-lookup"><span data-stu-id="d290a-110">Workaround</span></span>
<span data-ttu-id="d290a-111">Seuraavissa ohjeissa kerrotaan, miten selainasetus päivitetään kolmannen osapuolen evästeiden käyttöönottamiseksi Microsoft Edge- ja Google Chrome -selaimissa.</span><span class="sxs-lookup"><span data-stu-id="d290a-111">For Microsoft Edge or Google Chrome browsers, the following procedures outline how to update your browser setting to enable third-party cookies.</span></span>

#### <a name="microsoft-edge"></a><span data-ttu-id="d290a-112">Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="d290a-112">Microsoft Edge</span></span>

1. <span data-ttu-id="d290a-113">Avaa Edge-selain.</span><span class="sxs-lookup"><span data-stu-id="d290a-113">Open your Edge browser.</span></span>
2. <span data-ttu-id="d290a-114">Valitse oikeasta yläkulmasta **kolme pistettä** (...) ja valitse sitten **Asetukset**.</span><span class="sxs-lookup"><span data-stu-id="d290a-114">In the upper-right corner, select the **ellipsis** (...), and then select **Settings**.</span></span>
3. <span data-ttu-id="d290a-115">Valitse **Evästeet ja sivuston oikeudet** -kohdasta **Evästeet ja sivustotiedot**.</span><span class="sxs-lookup"><span data-stu-id="d290a-115">Under **Cookies and site permissions**, select **Cookies and site data**.</span></span>
4. <span data-ttu-id="d290a-116">Poista käytöstä **Estä kolmansien osapuolten evästeet**.</span><span class="sxs-lookup"><span data-stu-id="d290a-116">Turn off **Block third-party cookies**.</span></span>

#### <a name="google-chrome"></a><span data-ttu-id="d290a-117">Google Chrome</span><span class="sxs-lookup"><span data-stu-id="d290a-117">Google Chrome</span></span>

1. <span data-ttu-id="d290a-118">Avaa Chrome-selain.</span><span class="sxs-lookup"><span data-stu-id="d290a-118">Open your Chrome browser.</span></span>
2. <span data-ttu-id="d290a-119">Valitse oikeasta yläkulmasta kolme pystysuuntaista pistettä ja valitse sitten **Asetukset**.</span><span class="sxs-lookup"><span data-stu-id="d290a-119">In the upper-right corner, select the three vertical dots, and then select **Settings**.</span></span>
3. <span data-ttu-id="d290a-120">Valitse **Tietosuoja ja turvallisuus** -kohdasta **Evästeet ja muut sivuston tiedot**.</span><span class="sxs-lookup"><span data-stu-id="d290a-120">Under **Privacy and security**, select **Cookies and other site data**.</span></span>
4. <span data-ttu-id="d290a-121">Valitse **Salli kaikki evästeet**.</span><span class="sxs-lookup"><span data-stu-id="d290a-121">Select **Allow all cookies**.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="d290a-122">Jos estät kolmansien osapuolten evästeet, kaikki muiden sivustojen evästeet ja sivustotiedot estetään, vaikka sivusto olisi sallittu poikkeusluettelossasi.</span><span class="sxs-lookup"><span data-stu-id="d290a-122">If you block third-party cookies, all cookies and site data from other sites will be blocked, even if the site is allowed on your exceptions list.</span></span>

## <a name="pex-endpoint"></a><span data-ttu-id="d290a-123">PEX-päätepiste</span><span class="sxs-lookup"><span data-stu-id="d290a-123">PEX Endpoint</span></span>

<span data-ttu-id="d290a-124">Project Operations edellyttää, että projektiparametri viittaa PEX-päätepisteeseen.</span><span class="sxs-lookup"><span data-stu-id="d290a-124">Project Operations requires that a project parameter reference the PEX Endpoint.</span></span> <span data-ttu-id="d290a-125">Tämän päätepisteen on oltava yhteydessä palveluun, jota käytetään työrakenteen hahmontamiseen.</span><span class="sxs-lookup"><span data-stu-id="d290a-125">This endpoint is required to communicate with the service used to render the work breakdown structure.</span></span> <span data-ttu-id="d290a-126">Jos parametria ei ole otettu käyttöön, näyttöön tulee seuraava virhe: "Projektiparametri on virheellinen".</span><span class="sxs-lookup"><span data-stu-id="d290a-126">If the parameter isn't enabled, you will receive the error, "The project parameter is not valid".</span></span> 

### <a name="workaround"></a><span data-ttu-id="d290a-127">Ratkaisutapa</span><span class="sxs-lookup"><span data-stu-id="d290a-127">Workaround</span></span>
 ![PEX-päätepiste-kenttä projektiparametrissa](media/projectparameter.png)

1. <span data-ttu-id="d290a-129">Lisää **PEX-päätepiste**-kenttä **Projektiparametrit**-sivulle.</span><span class="sxs-lookup"><span data-stu-id="d290a-129">Add the **PEX Endpoint** field to the **Project Parameters** page.</span></span>
2. <span data-ttu-id="d290a-130">Päivitä kenttään seuraava arvo: `https://project.microsoft.com/<lang>/?org=<cdsServer>#/taskgrid?projectId=\<id>&type=2`</span><span class="sxs-lookup"><span data-stu-id="d290a-130">Update the field with the following value: `https://project.microsoft.com/<lang>/?org=<cdsServer>#/taskgrid?projectId=\<id>&type=2`</span></span>
3. <span data-ttu-id="d290a-131">Poista kenttä **Projektiparametrit**-sivulta.</span><span class="sxs-lookup"><span data-stu-id="d290a-131">Remove the field from the **Project Parameters** page.</span></span>

## <a name="privileges-for-project-for-the-web"></a><span data-ttu-id="d290a-132">Projektin verkko-oikeudet</span><span class="sxs-lookup"><span data-stu-id="d290a-132">Privileges for Project for the Web</span></span>

<span data-ttu-id="d290a-133">Project Operations luottaa ulkoiseen aikataulutuspalveluun.</span><span class="sxs-lookup"><span data-stu-id="d290a-133">Project Operations relies on an external scheduling service.</span></span> <span data-ttu-id="d290a-134">Palvelu edellyttää, että käyttäjälle on delegoitu useita rooleja työrakenteeseen liittyvien entiteettien lukemista ja kirjoittamista varten.</span><span class="sxs-lookup"><span data-stu-id="d290a-134">The service requires that a user have several roles assigned to read and write to entities related to the work breakdown structure.</span></span> <span data-ttu-id="d290a-135">Näitä entiteettejä ovat projektitehtävät, resurssimääritykset ja tehtävien riippuvuudet.</span><span class="sxs-lookup"><span data-stu-id="d290a-135">These entities include project tasks, resource assignments, and task dependencies.</span></span> <span data-ttu-id="d290a-136">Jos käyttäjä ei voi hahmontaa työrakennetta, kun hän siirtyy **Tehtävät**-välilehteen, se johtuu luultavasti siitä, että Project Operationsin projektia ei ole otettu käyttöön.</span><span class="sxs-lookup"><span data-stu-id="d290a-136">If a user can't render the work breakdown structure when they go to the **Tasks** tab, it's probably because Project for Project Operations hasn't been enabled.</span></span> <span data-ttu-id="d290a-137">Käyttäjä voi saada joko käyttöoikeusroolivirheen tai käytönestoon liittyvän virheen.</span><span class="sxs-lookup"><span data-stu-id="d290a-137">A user might receive either a security role error, or an error related to a denial of access.</span></span>


## <a name="workaround"></a><span data-ttu-id="d290a-138">Ratkaisutapa</span><span class="sxs-lookup"><span data-stu-id="d290a-138">Workaround</span></span>

1. <span data-ttu-id="d290a-139">Valitse **Asetus > Suojaus > Käyttäjät > Sovelluksen käyttäjät**.</span><span class="sxs-lookup"><span data-stu-id="d290a-139">Go to **Setting > Security > Users > Application Users**.</span></span>  

   ![Sovelluslukija](media/applicationuser.jpg)
   
2. <span data-ttu-id="d290a-141">Tarkista seuraavat seikat kaksoisnapsauttamalla sovelluksen käyttäjätietuetta:</span><span class="sxs-lookup"><span data-stu-id="d290a-141">Double-click the application user record to verify the following:</span></span>

 - <span data-ttu-id="d290a-142">Käyttäjällä on projektin käyttöoikeus.</span><span class="sxs-lookup"><span data-stu-id="d290a-142">The user has access to the project.</span></span> <span data-ttu-id="d290a-143">Tarkistus tehdään yleensä varmistamalla, että käyttäjällä on **projektipäällikön** käyttöoikeusrooli.</span><span class="sxs-lookup"><span data-stu-id="d290a-143">This verification is typically done by ensuring that the user has **Project Manager** security role.</span></span>
 - <span data-ttu-id="d290a-144">Microsoft Project -sovelluksen käyttäjä on olemassa ja määritetty oikein.</span><span class="sxs-lookup"><span data-stu-id="d290a-144">The Microsoft Project application user exists and is configured correctly.</span></span>
 
3. <span data-ttu-id="d290a-145">Jos käyttäjää ei ole, voit luoda uuden käyttäjätietueen.</span><span class="sxs-lookup"><span data-stu-id="d290a-145">If this user doesn't exist, you can create a new user record.</span></span> <span data-ttu-id="d290a-146">Valitse **Uudet käyttäjät**.</span><span class="sxs-lookup"><span data-stu-id="d290a-146">Select **New Users**.</span></span> <span data-ttu-id="d290a-147">Vaihda syöttölomakkeeksi **Sovelluksen käyttäjä** ja lisää sitten **sovellustunnus**.</span><span class="sxs-lookup"><span data-stu-id="d290a-147">Change the entry form to **Application User**, and then add the **Application ID**.</span></span>

   ![Sovelluksen käyttäjän tiedot](media/applicationuserdetails.jpg)

4. <span data-ttu-id="d290a-149">Tarkista, että käyttäjälle on määritetty oikea käyttöoikeus ja että palvelu on otettu käyttöön käyttöoikeuden palvelusuunnitelmissa.</span><span class="sxs-lookup"><span data-stu-id="d290a-149">Verify that the user has been assigned the correct license and that the service is enabled in the service plans details of the license.</span></span>
5. <span data-ttu-id="d290a-150">Tarkista, että käyttäjä voi avata osoitteen project.microsoft.com.</span><span class="sxs-lookup"><span data-stu-id="d290a-150">Verify that the user can open project.microsoft.com.</span></span>
6. <span data-ttu-id="d290a-151">Tarkista projektiparametrien kautta, että järjestelmä osoittaa oikeaan projektin päätepisteeseen.</span><span class="sxs-lookup"><span data-stu-id="d290a-151">Verify through the project parameters that the system is pointing to the correct project endpoint.</span></span>
7. <span data-ttu-id="d290a-152">Tarkista, että projektisovelluksen käyttäjä on luotu.</span><span class="sxs-lookup"><span data-stu-id="d290a-152">Verify that the project application user is created.</span></span>
8. <span data-ttu-id="d290a-153">Ota käyttäjälle käyttöön seuraavat käyttöoikeusroolit:</span><span class="sxs-lookup"><span data-stu-id="d290a-153">Apply the following security roles to the user:</span></span>

  - <span data-ttu-id="d290a-154">Dataverse -palvelun käyttäjä</span><span class="sxs-lookup"><span data-stu-id="d290a-154">Dataverse User</span></span>
  - <span data-ttu-id="d290a-155">Project Operations -järjestelmä</span><span class="sxs-lookup"><span data-stu-id="d290a-155">Project Operations System</span></span>
  - <span data-ttu-id="d290a-156">Projektijärjestelmä</span><span class="sxs-lookup"><span data-stu-id="d290a-156">Project System</span></span>

## <a name="error-when-updating-the-work-breakdown-structure"></a><span data-ttu-id="d290a-157">Virhe päivitettäessä työrakennetta</span><span class="sxs-lookup"><span data-stu-id="d290a-157">Error when updating the work breakdown structure</span></span>

<span data-ttu-id="d290a-158">Kun vähintään yksi päivitys tehdään työrakenteeseen, muutokset epäonnistuvat lopulta eikä niitä tallenneta.</span><span class="sxs-lookup"><span data-stu-id="d290a-158">When one or more updates are made to the work breakdown structure, the changes eventually fail and aren't saved.</span></span> <span data-ttu-id="d290a-159">Aikatauluruudukossa tapahtuu virhe, jonka mukaan "Äskettäin tehtyä muutosta ei voi tallentaa".</span><span class="sxs-lookup"><span data-stu-id="d290a-159">An error occurs in the schedule grid noting that “Recent change you’ve made couldn’t be saved.”</span></span>

### <a name="workaround"></a><span data-ttu-id="d290a-160">Ratkaisutapa</span><span class="sxs-lookup"><span data-stu-id="d290a-160">Workaround</span></span>

1. <span data-ttu-id="d290a-161">Tarkista, että käyttäjälle on määritetty oikea käyttöoikeus ja että palvelu on otettu käyttöön käyttöoikeuden palvelusuunnitelmissa.</span><span class="sxs-lookup"><span data-stu-id="d290a-161">Verify that the user has been assigned the correct license and that the service is enabled in the service plans details of the license.</span></span>
2. <span data-ttu-id="d290a-162">Tarkista, että käyttäjä voi avata osoitteen project.microsoft.com.</span><span class="sxs-lookup"><span data-stu-id="d290a-162">Verify that the user can open project.microsoft.com.</span></span>
3. <span data-ttu-id="d290a-163">Tarkista, että järjestelmä osoittaa oikeaan projektin päätepisteeseen.</span><span class="sxs-lookup"><span data-stu-id="d290a-163">Verify that the system is pointing to the correct project endpoint,.</span></span>
4. <span data-ttu-id="d290a-164">Tarkista, että projektisovelluksen käyttäjä on luotu.</span><span class="sxs-lookup"><span data-stu-id="d290a-164">Verify that the Project Application user has been created.</span></span>
5. <span data-ttu-id="d290a-165">Ota käyttäjälle käyttöön seuraavat käyttöoikeusroolit:</span><span class="sxs-lookup"><span data-stu-id="d290a-165">Apply the following security roles to the user:</span></span>
  
  - <span data-ttu-id="d290a-166">Dataverse-käyttäjä tai peruskäyttäjä</span><span class="sxs-lookup"><span data-stu-id="d290a-166">Dataverse user or Base user</span></span>
  - <span data-ttu-id="d290a-167">Project Operations -järjestelmä</span><span class="sxs-lookup"><span data-stu-id="d290a-167">Project Operations System</span></span>
  - <span data-ttu-id="d290a-168">Projektijärjestelmä</span><span class="sxs-lookup"><span data-stu-id="d290a-168">Project System</span></span>
  - <span data-ttu-id="d290a-169">Project Operationsin kaksoiskirjoitusjärjestelmä (tämä rooli on pakollinen, jos otat käyttöön Project Operationsin resursseihin ja ei-varastoitaviin perustuvissa skenaarioissa).</span><span class="sxs-lookup"><span data-stu-id="d290a-169">Project Operations Dual Write System (This role is required if you are deploying the resource/non-stocked based scenario of Project Operations.)</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]