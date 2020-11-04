---
title: Luo uusi projekti
description: Tässä aiheessa on tietoja uuden projektin luomisesta.
author: Yowelle
manager: AnnBe
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 727d287c571b2a64bf10b2393a87567093a420d2
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/16/2020
ms.locfileid: "4075483"
---
# <a name="create-a-new-project"></a><span data-ttu-id="20ee7-103">Luo uusi projekti</span><span class="sxs-lookup"><span data-stu-id="20ee7-103">Create a new project</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="20ee7-104">Luodaksesi uuden projektin, toimi seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="20ee7-104">Complete the following steps to create a new project.</span></span>

1. <span data-ttu-id="20ee7-105">Valitse **Projektinhallinta** -sivulla **Uusi projekti** ja syötä seuraavat arvot:</span><span class="sxs-lookup"><span data-stu-id="20ee7-105">On the **Project management** page, select **New project** , and enter the following values:</span></span>

    - <span data-ttu-id="20ee7-106">**Projektityyppi:** Aika ja materiaali</span><span class="sxs-lookup"><span data-stu-id="20ee7-106">**Project type:** Time and material</span></span>
    - <span data-ttu-id="20ee7-107">**Projektin nimi:** XYZ-päivityksen vaihe 2</span><span class="sxs-lookup"><span data-stu-id="20ee7-107">**Project name:** XYZ Upgrade Phase 2</span></span>
    - <span data-ttu-id="20ee7-108">**Projektiryhmä:** TM\_WIP</span><span class="sxs-lookup"><span data-stu-id="20ee7-108">**Project group:** TM\_WIP</span></span>
    - <span data-ttu-id="20ee7-109">**Projektisopimuksen tunnus:** 00000002</span><span class="sxs-lookup"><span data-stu-id="20ee7-109">**Project contract ID:** 00000002</span></span>

2. <span data-ttu-id="20ee7-110">Valitse **Luo projekti**.</span><span class="sxs-lookup"><span data-stu-id="20ee7-110">Select **Create project**.</span></span>

## <a name="assign-a-resource-to-a-project"></a><span data-ttu-id="20ee7-111">Resurssin osoittaminen projektille</span><span class="sxs-lookup"><span data-stu-id="20ee7-111">Assign a resource to a project</span></span>

1. <span data-ttu-id="20ee7-112">Valitse **Työntekijät** -sivun **Työntekijät** -luettelosta sen työntekijän tietue, jolle olet aiemmin määrittänyt pätevyyksiä, ja avaa työntekijän tietue.</span><span class="sxs-lookup"><span data-stu-id="20ee7-112">On the **Workers** page, in the **Workers** list, select the record for the worker that you previously set up competencies for, and open the worker record.</span></span>
2. <span data-ttu-id="20ee7-113">Valitse toimintoruudun **Projekti** -välilehden **Määritys** -ryhmässä **Osoita projekteja**.</span><span class="sxs-lookup"><span data-stu-id="20ee7-113">On the Action Pane, on the **Project** tab, in the **Setup** group, select **Assign projects**.</span></span>
3. <span data-ttu-id="20ee7-114">Käytä suodattimena **XYZ-päivityksen vaihe 2** -projektia suodattimena **Resurssivahvistuksen projektiosoitukset** -sivun **Projektit** -välilehden **Lisää projekti valittuihin projekteihin** -kentässä.</span><span class="sxs-lookup"><span data-stu-id="20ee7-114">On the **Resource validation project assignments** page, on the **Projects** tab, in the **Add the project to selected projects** field, filter on the **XYZ Upgrade Phase 2** project.</span></span>
4. <span data-ttu-id="20ee7-115">Valitse **Jäljellä olevat projektit** -ruudussa projekti ja lisää se sitten **Valitut projektit** -ruutuun valitsemalla nuolipainike.</span><span class="sxs-lookup"><span data-stu-id="20ee7-115">In the **Remaining projects** pane, select a project, and then select the arrow button to add it to the **Selected projects** pane.</span></span>

<span data-ttu-id="20ee7-116">Voit myös määrittää resurssille luokkia tarpeen mukaan.</span><span class="sxs-lookup"><span data-stu-id="20ee7-116">You can also assign categories for a resource as you require.</span></span> <span data-ttu-id="20ee7-117">Luokan tyyppi on joko **Kustannus** tai **Tuotto**.</span><span class="sxs-lookup"><span data-stu-id="20ee7-117">The category type is either **Cost** or **Revenue**.</span></span> <span data-ttu-id="20ee7-118">Organisaatiosi määrittää luokkatyypin.</span><span class="sxs-lookup"><span data-stu-id="20ee7-118">The category type is determined by your organization.</span></span> <span data-ttu-id="20ee7-119">Jos resurssille ei ole määritetty luokkia, Finance hakee tuntihintojen oletusluokan kustannuksille ja tuotoille.</span><span class="sxs-lookup"><span data-stu-id="20ee7-119">If no categories are assigned for a resource, Finance looks up the default category on hour prices for cost and revenue.</span></span>

## <a name="set-up-project-resource-and-role-characteristics"></a><span data-ttu-id="20ee7-120">Projektiresurssin ja rooliominaisuuksien määrittäminen</span><span class="sxs-lookup"><span data-stu-id="20ee7-120">Set up project resource and role characteristics</span></span>

<span data-ttu-id="20ee7-121">Projektipäällikkö voi luoda projektin edellyttämiä rooleja projektin resusointitoiminnon avulla.</span><span class="sxs-lookup"><span data-stu-id="20ee7-121">A project manager can use the project resourcing functionality to create the roles that are required for the project.</span></span> <span data-ttu-id="20ee7-122">Rooleja voidaan käyttää, jos vahvistetut resurssit ovat vielä tuntemattomia, kun resursseja varataan.</span><span class="sxs-lookup"><span data-stu-id="20ee7-122">Roles can be used if confirmed resources are still unknown when resources are being reserved.</span></span> <span data-ttu-id="20ee7-123">Roolit voidaan varata väliaikaisesti suunnitelluiksi resursseiksi, jotta voit jatkaa projektin suunnitteluvaiheita.</span><span class="sxs-lookup"><span data-stu-id="20ee7-123">Roles can be temporarily reserved as planned resources, so that you can continue the project planning stages.</span></span>

<span data-ttu-id="20ee7-124">[![Esimerkki roolista](./media/projectresourcing05.jpg)](./media/projectresourcing05.jpg)</span><span class="sxs-lookup"><span data-stu-id="20ee7-124">[![Example of a role](./media/projectresourcing05.jpg)](./media/projectresourcing05.jpg)</span></span> 

<span data-ttu-id="20ee7-125">**Skenaario:** Contoso palkattiin suorittamaan Aika ja materiaali -projekti, jolla on hyväksytty projektin peruskirja.</span><span class="sxs-lookup"><span data-stu-id="20ee7-125">**Scenario:** Contoso was hired to complete a Time and material project that has an approved project charter.</span></span> <span data-ttu-id="20ee7-126">Aliprojektipäällikkö määrittää edelleen projektin vaikutusaluetta.</span><span class="sxs-lookup"><span data-stu-id="20ee7-126">The junior project manager is still completing the scope of the project.</span></span> <span data-ttu-id="20ee7-127">Resurssipäällikkö on tällä hetkellä määrittämässä erityisiä resursseja, jotka varataan työskentelemään uudessa projektissa.</span><span class="sxs-lookup"><span data-stu-id="20ee7-127">The resource manager is currently identifying specific resources that will be reserved to work on the new project.</span></span> <span data-ttu-id="20ee7-128">Projektin kriittisen luonteen vuoksi projektin rahoittaja pyysi projektipäällikköä yhdeksi rooleista.</span><span class="sxs-lookup"><span data-stu-id="20ee7-128">Because of the critical nature of the project, the project sponsor requested Senior project manager as one of the roles.</span></span> <span data-ttu-id="20ee7-129">Resurssipäällikön täytyy hankkia uusi resurssi ja määrittää se järjestelmässä, jos aliprojektipäällikkö tarvitsee resurssin tiedot projektisuunnittelun aikana.</span><span class="sxs-lookup"><span data-stu-id="20ee7-129">The resource manager must acquire the new resource and define the role in the system in case the junior project manager requires the resource information during project planning.</span></span>

<span data-ttu-id="20ee7-130">Seuraavissa vaiheissa näytetään, miten resurssipäällikkö voi määrittää projektipäällikön roolin ja osoittaa sille resurssiominaisuuksia.</span><span class="sxs-lookup"><span data-stu-id="20ee7-130">The following steps show how the resource manager can set up the Senior project manager role and associate resource characteristics with it.</span></span> <span data-ttu-id="20ee7-131">Roolia voi myöhemmin käyttää sellaisten käytettävissä olevien resurssien hakemiseen, jotka täyttävät resurssin pätevyysvaatimukset.</span><span class="sxs-lookup"><span data-stu-id="20ee7-131">Later, the role can be used to search for available resources that match the required resource competencies.</span></span>

1. <span data-ttu-id="20ee7-132">Valitse **Määritä roolit** -sivulla **Uusi** ja syötä seuraavat arvot:</span><span class="sxs-lookup"><span data-stu-id="20ee7-132">On the **Setup roles** page, select **New** , and enter the following values:</span></span>

    - <span data-ttu-id="20ee7-133">**Roolin tunnus:** Projektipäällikkö</span><span class="sxs-lookup"><span data-stu-id="20ee7-133">**Role ID:** Senior Project Manager</span></span>
    - <span data-ttu-id="20ee7-134">**Kuvaus:** Projektipäällikkö</span><span class="sxs-lookup"><span data-stu-id="20ee7-134">**Description:** Senior Project Manager</span></span>

2. <span data-ttu-id="20ee7-135">Valitse **Luo**.</span><span class="sxs-lookup"><span data-stu-id="20ee7-135">Select **Create**.</span></span>
3. <span data-ttu-id="20ee7-136">Valitse **Projektipäällikkö** -rooli ja valitse sitten **Määritä ominaisuudet**.</span><span class="sxs-lookup"><span data-stu-id="20ee7-136">Select the **Senior Project Manager** role, and then select **Configure characteristics**.</span></span>
4. <span data-ttu-id="20ee7-137">Valitse **Ominaisuustyyppi** -kentässä **Taito**.</span><span class="sxs-lookup"><span data-stu-id="20ee7-137">In the **Characteristics type** field, select **Skill**.</span></span>
5. <span data-ttu-id="20ee7-138">Syötä haettava taito **Käytettävissä olevat ominaisuudet** -kenttään.</span><span class="sxs-lookup"><span data-stu-id="20ee7-138">In the **Available characteristics** field, enter the skill to search for.</span></span>
6. <span data-ttu-id="20ee7-139">Valitse **Ominaisuustyyppi** -kentässä **Sertifikaatti**.</span><span class="sxs-lookup"><span data-stu-id="20ee7-139">In the **Characteristic type** field, select **Certificate**.</span></span>
7. <span data-ttu-id="20ee7-140">Syötä haettava sertifikaattityyppi **Käytettävissä olevat ominaisuudet** -kenttään.</span><span class="sxs-lookup"><span data-stu-id="20ee7-140">In the **Available characteristics** field, enter the certificate type to search for.</span></span>

## <a name="assign-a-project-resource-to-a-project"></a><span data-ttu-id="20ee7-141">Projektiresurssin osoittaminen projektille</span><span class="sxs-lookup"><span data-stu-id="20ee7-141">Assign a project resource to a project</span></span>

1. <span data-ttu-id="20ee7-142">Valitse **Kaikki projektit** -sivulla **XYZ-päivityksen vaihe 2** -projekti.</span><span class="sxs-lookup"><span data-stu-id="20ee7-142">On the **All projects** page, select the **XYZ Upgrade Phase 2** project.</span></span>
2. <span data-ttu-id="20ee7-143">Valitse **Projektitiimi ja aikataulutus** -välilehdellä **Lisää**.</span><span class="sxs-lookup"><span data-stu-id="20ee7-143">On the **Project team and scheduling** tab, select **Add**.</span></span>
3. <span data-ttu-id="20ee7-144">Valitse **Rooli** -kentässä **Tiimin jäsen**.</span><span class="sxs-lookup"><span data-stu-id="20ee7-144">In the **Role** field, select **Team member**.</span></span>
4. <span data-ttu-id="20ee7-145">Valitse **Varaa kalenterissa**.</span><span class="sxs-lookup"><span data-stu-id="20ee7-145">Select **Book from calendar**.</span></span>
5. <span data-ttu-id="20ee7-146">Valitse **Resurssin käytettävyys** -sivulla **Näytä asetukset**.</span><span class="sxs-lookup"><span data-stu-id="20ee7-146">On the **Resource availability** page, select **View settings**.</span></span>
6. <span data-ttu-id="20ee7-147">Syötä **Säädä näkymäasetuksia** -sivulle seuraavat arvot:</span><span class="sxs-lookup"><span data-stu-id="20ee7-147">On the **Adjust view settings** page, enter the following values:</span></span>

    - <span data-ttu-id="20ee7-148">**Päivämäärävälinäkymän muoto:** Päivä</span><span class="sxs-lookup"><span data-stu-id="20ee7-148">**Format for date range view:** Day</span></span>
    - <span data-ttu-id="20ee7-149">**Näytä käytettävyyskuvaukset:** Kyllä</span><span class="sxs-lookup"><span data-stu-id="20ee7-149">**Display availability descriptions:** Yes</span></span>
    - <span data-ttu-id="20ee7-150">**Näytä jäljellä oleva kapasiteetti:** Kyllä</span><span class="sxs-lookup"><span data-stu-id="20ee7-150">**Display remaining capacity:** Yes</span></span>

7. <span data-ttu-id="20ee7-151">Valitse resurssi resurssiluettelosta.</span><span class="sxs-lookup"><span data-stu-id="20ee7-151">In the list of resources, select a resource.</span></span>
8. <span data-ttu-id="20ee7-152">Valitse **Tee sitova varaus** ja **Täysi kapasiteetti**.</span><span class="sxs-lookup"><span data-stu-id="20ee7-152">Select **Hard book** and **Full capacity**.</span></span>

## <a name="assign-a-resource-to-a-default-role"></a><span data-ttu-id="20ee7-153">Osoita resurssi oletusroolille</span><span class="sxs-lookup"><span data-stu-id="20ee7-153">Assign a resource to a default role</span></span>

<span data-ttu-id="20ee7-154">Jotta projekti- tai resurssipäälliköt voisivat porautua helpommin syvemmälle projektille varattavissa oleviin resursseihin.</span><span class="sxs-lookup"><span data-stu-id="20ee7-154">To help project or resource managers can drill down further on the resources that can be reserved for a project.</span></span> <span data-ttu-id="20ee7-155">Voit liittää oletusroolin aiemmin luotuun resurssiin tai juuri hankittuun resurssiin.</span><span class="sxs-lookup"><span data-stu-id="20ee7-155">You can associate a default role with an existing resource or a newly acquired resource.</span></span> <span data-ttu-id="20ee7-156">Kun esimerkiksi Taneli palkattiin, hänellä oli kokemus ja taidot liiketoiminta-analyytikon roolin täyttämiseen.</span><span class="sxs-lookup"><span data-stu-id="20ee7-156">For example, when Daniel was hired, he had the experience and skills to fill the Business analyst role.</span></span> <span data-ttu-id="20ee7-157">Resurssipäällikkö osoitti kyseisen roolin Tanelin oletusrooliksi.</span><span class="sxs-lookup"><span data-stu-id="20ee7-157">The resource manager assigned this role as Daniel's default role.</span></span> <span data-ttu-id="20ee7-158">Siksi resurssipäällikkö lisäsi Tanelin niiden liiketoiminta-analyytikkojen varantoon, jotka ovat käytettävissä projekteissa työskentelemiseen.</span><span class="sxs-lookup"><span data-stu-id="20ee7-158">Therefore, the resource manager added Daniel to a pool of business analysts who are available to work on projects.</span></span>

<span data-ttu-id="20ee7-159">Resurssivarauksen aikana projektipäälliköt voivat suodattaa niitä rooliresursseja, jotka ovat käytettävissä projekteissa työskentelemiseen.</span><span class="sxs-lookup"><span data-stu-id="20ee7-159">During resource reservation, project managers can filter the role resources that are available to work on projects.</span></span> <span data-ttu-id="20ee7-160">He voivat käyttää näitä tietoja yhtenä perusteena, kun he suorittavat useiden perusteiden päätösanalyysiä resurssin täyttämisen aikana.</span><span class="sxs-lookup"><span data-stu-id="20ee7-160">They can use this information as one criterion when they perform multi-criteria decision analysis during resource fulfillment.</span></span> <span data-ttu-id="20ee7-161">He voivat myös lisätä suodattimeen muita resurssiominaisuuksia hakeakseen resursseja, joilla on tietyt taidot, koulutus ja kokemus tiettyä projektia varten.</span><span class="sxs-lookup"><span data-stu-id="20ee7-161">They can also add other resource characteristics to the filter to search for resources that have specific skills, education, and experience for a given project.</span></span>

<span data-ttu-id="20ee7-162">**Skenaario:** Hyväksytty projekti on alkanut ja projektipäällikön rooli varattiin suunnitelluksi resurssiksi projektin suunnitteluvaiheessa.</span><span class="sxs-lookup"><span data-stu-id="20ee7-162">**Scenario:** An approved project has started, and the Senior project manager role was reserved as a planned resource during the project planning stage.</span></span> <span data-ttu-id="20ee7-163">Resurssipäällikkö on nyt hankkinut resurssin täyttämään projektipäällikön roolin.</span><span class="sxs-lookup"><span data-stu-id="20ee7-163">The resource manager has now acquired a resource to fulfill the Senior project manager role.</span></span>

1. <span data-ttu-id="20ee7-164">Valitse **Resurssiluettelo** -sivulla **Taneli Kultaranta**.</span><span class="sxs-lookup"><span data-stu-id="20ee7-164">On the **Resources list** page, select **Daniel Goldschmidt**.</span></span>
2. <span data-ttu-id="20ee7-165">Valitse **Resurssin rooli** -sivulla **Uusi** ja syötä seuraavat arvot:</span><span class="sxs-lookup"><span data-stu-id="20ee7-165">On the **Resource role** page, select **New** , and enter the following values:</span></span>

    - <span data-ttu-id="20ee7-166">**Voimaantulo:** Anna nykyinen päivämäärä.</span><span class="sxs-lookup"><span data-stu-id="20ee7-166">**Effective:** Enter the current date.</span></span>
    - <span data-ttu-id="20ee7-167">**Vanheneminen:** Syötä **Ei koskaan**.</span><span class="sxs-lookup"><span data-stu-id="20ee7-167">**Expiration:** Enter **Never**.</span></span>
    - <span data-ttu-id="20ee7-168">**Rooli:** Syötä **Projektipäällikkö**.</span><span class="sxs-lookup"><span data-stu-id="20ee7-168">**Role:** Enter **Senior Project Manager**.</span></span>

3. <span data-ttu-id="20ee7-169">Valitse **Tallenna** ja sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="20ee7-169">Select **Save** , and then close the page.</span></span>
4. <span data-ttu-id="20ee7-170">Lisää **Pätevyydet** -välilehdessä taito **ProjectMgmt** ja sertifikaatti **PMP**.</span><span class="sxs-lookup"><span data-stu-id="20ee7-170">On the **Competencies** tab, add the **ProjectMgmt** skill and the **PMP** certificate.</span></span>
