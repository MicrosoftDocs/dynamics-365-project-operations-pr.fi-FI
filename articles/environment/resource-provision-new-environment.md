---
title: Uuden ympäristön valmisteleminen
description: Tässä aiheessa on tietoja siitä, miten uuden Project Operations -ympäristön voi valmistella.
author: sigitac
manager: Annbe
ms.date: 10/02/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 45700371c50e3b5a840df45fc24fa8a5b4584b61
ms.sourcegitcommit: 87b7a8d793c19c50f3765b8d788cde24a6a0ca24
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/02/2020
ms.locfileid: "3949358"
---
# <a name="provision-a-new-environment"></a><span data-ttu-id="8607d-103">Uuden ympäristön valmisteleminen</span><span class="sxs-lookup"><span data-stu-id="8607d-103">Provision a new environment</span></span>

<span data-ttu-id="8607d-104">_**Käytetään:** Project Operationsin resursseihin ja ei-varastoitaviin perustuvissa skenaarioissa_</span><span class="sxs-lookup"><span data-stu-id="8607d-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="8607d-105">Tässä aiheessa on tietoja siitä, miten luodaan uusi Dynamics 365 Project Operations -ympäristö resurssien ja ei-varastoitavien skenaarioiden perusteella.</span><span class="sxs-lookup"><span data-stu-id="8607d-105">This topic provides information about how to provision a new Dynamics 365 Project Operations environment for resource/non-stocked based scenarios.</span></span>

## <a name="enable-project-operations-automated-provisioning-in-an-lcs-project"></a><span data-ttu-id="8607d-106">Project Operationsin automaattisen valmistelun käyttöönotto LCS-projektissa</span><span class="sxs-lookup"><span data-stu-id="8607d-106">Enable Project Operations automated provisioning in an LCS project</span></span>

<span data-ttu-id="8607d-107">Käytä seuraavia vaiheita, kun haluat ottaa käyttöön Project Operationsin automatisoidun valmistelutyönkulun LCS-projektillesi.</span><span class="sxs-lookup"><span data-stu-id="8607d-107">Use following steps to enable the Project Operations automated provisioning flow for your LCS project.</span></span>

1. <span data-ttu-id="8607d-108">Siirry [LCS:sään](https://lcs.dynamics.com/v2) ja valitse **Esiversio-ominaisuuksien hallinta** -ruutu.</span><span class="sxs-lookup"><span data-stu-id="8607d-108">Go to [LCS](https://lcs.dynamics.com/v2) and select the **Preview Feature management** tile.</span></span>
2. <span data-ttu-id="8607d-109">Valitse **Esiversio-ominaisuus** -luettelosta **Project Operations** ja ota Project Operations käyttöön valitsemalla **Esiversio-ominaisuus käytössä**.</span><span class="sxs-lookup"><span data-stu-id="8607d-109">In the **Preview feature** list, select **Project Operations** and the select **Preview feature enabled** to enable Project Operations.</span></span>

> [!NOTE]
> <span data-ttu-id="8607d-110">Tämä vaihe suoritetaan vain kerran LCS-projektia kohden.</span><span class="sxs-lookup"><span data-stu-id="8607d-110">This step is performed only one time per LCS project.</span></span>

## <a name="provision-a-project-operations-environment"></a><span data-ttu-id="8607d-111">Project Operations -ympäristön tarjoaminen</span><span class="sxs-lookup"><span data-stu-id="8607d-111">Provision a Project Operations environment</span></span>

1. <span data-ttu-id="8607d-112">Avaa uusi Dynamics 365 Finance [-esittely-ympäristön](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) tai [eristys-/tuotantoympäristön](https://docs.microsoft.com/edynamics365/fin-ops-core/dev-itpro/deployment/deployenvironment-newinfrastructure) käyttöönotto.</span><span class="sxs-lookup"><span data-stu-id="8607d-112">Open a new Dynamics 365 Finance [demo environment](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) or [sandbox/ production environment](https://docs.microsoft.com/edynamics365/fin-ops-core/dev-itpro/deployment/deployenvironment-newinfrastructure) deployment.</span></span> 
2. <span data-ttu-id="8607d-113">Suorita ohjatun **Ympäristön valmistelu** -toiminnon vaiheet.</span><span class="sxs-lookup"><span data-stu-id="8607d-113">Walk through the **Environment provisioning** wizard.</span></span> 

> [!IMPORTANT]
> <span data-ttu-id="8607d-114">Varmista, että valittu sovellusversio on 10.0.13 tai uudempi.</span><span class="sxs-lookup"><span data-stu-id="8607d-114">Make sure selected application version is 10.0.13 or higher.</span></span>

3. <span data-ttu-id="8607d-115">Jos haluat valmistella Project Operationsi, valitse **Lisäasetukset**-kohdassa **Common Data Service**.</span><span class="sxs-lookup"><span data-stu-id="8607d-115">To provision Project Operations, under **Advance settings**, select **Common Data Service**.</span></span> 
4. <span data-ttu-id="8607d-116">Ota **Common Data Service -asetukset** käyttöön valitsemalla **Kyllä** ja kirjoitramalla tiedot pakollisiin kenttiin:</span><span class="sxs-lookup"><span data-stu-id="8607d-116">Enable the **Common Data Service Setting** by selecting **Yes** and then enter information in the required fields:</span></span>

  - <span data-ttu-id="8607d-117">Nimi</span><span class="sxs-lookup"><span data-stu-id="8607d-117">Name</span></span>
  - <span data-ttu-id="8607d-118">Alue</span><span class="sxs-lookup"><span data-stu-id="8607d-118">Region</span></span>
  - <span data-ttu-id="8607d-119">Language</span><span class="sxs-lookup"><span data-stu-id="8607d-119">Language</span></span>
  - <span data-ttu-id="8607d-120">Valuutta</span><span class="sxs-lookup"><span data-stu-id="8607d-120">Currency</span></span>
 
5. <span data-ttu-id="8607d-121">Valitse **Common Data Service -malli** -kentässä **Project Operations**</span><span class="sxs-lookup"><span data-stu-id="8607d-121">In the **Common Data Service Template** field, select **Project Operations**</span></span> 

6. <span data-ttu-id="8607d-122">Valitse käyttöönoton ympäristötyyppi.</span><span class="sxs-lookup"><span data-stu-id="8607d-122">Select the environment type for your deployment.</span></span> <span data-ttu-id="8607d-123">Tilauspohjaisen kokeiluversion avulla voit käyttää CDS-ympäristöä 30 päivän ajan.</span><span class="sxs-lookup"><span data-stu-id="8607d-123">A subscription-based trial will let you deploy a CDS environment for 30 days.</span></span> 

![Käyttööntoton asetukset](./media/1DeploymentSettings.png)

> [!IMPORTANT]
> <span data-ttu-id="8607d-125">Valitse **Hyväksy**, kun hyväksyt palveluehdot, ja palaa sitten käyttöönottoasetuksiin valitsemalla **Valmis**.</span><span class="sxs-lookup"><span data-stu-id="8607d-125">Select **Agree** to acknowledge the terms of service and then select **Done** to return to the deployment settings.</span></span>

![Käyttöönoton suostumus](./media/2DeploymentConsent.png)

7. <span data-ttu-id="8607d-127">Täytä loput pakolliset kentät ohjatussa toiminnossa ja vahvista asennus.</span><span class="sxs-lookup"><span data-stu-id="8607d-127">Complete the remaining required fields in the wizard and confirm the deployment.</span></span> <span data-ttu-id="8607d-128">Ympäristön valmisteluaika vaihtelee ympäristötyypin mukaan.</span><span class="sxs-lookup"><span data-stu-id="8607d-128">Environment provisioning time varies based on the environment type.</span></span> <span data-ttu-id="8607d-129">Valmistelu voi kestää jopa kuusi tuntia.</span><span class="sxs-lookup"><span data-stu-id="8607d-129">Provisioning might take up to six hours.</span></span>

  <span data-ttu-id="8607d-130">Kun käyttöönotto on valmis, ympäristö näkyy tilassa **Otettu käyttöön**.</span><span class="sxs-lookup"><span data-stu-id="8607d-130">After the deployment completes successfully, the environment will show as **Deployed**.</span></span>

8. <span data-ttu-id="8607d-131">Varmista, että ympäristö on otettu käyttöön, valitsemalla **Kirjaudu** ja kirjautumalla ympäristöön sekä tarkistamalla käyttöönoton tilan.</span><span class="sxs-lookup"><span data-stu-id="8607d-131">To confirm the environment has deployed successfully, select **Login** and log on to the environment to confirm.</span></span>

![-ympäristön tiedot](./media/3EnvironmentDetails.png)

## <a name="apply-project-operations-finance-demo-data-optional-step"></a><span data-ttu-id="8607d-133">Project Operationsin Finance -esittelytietojen käyttöönotto (valinnainen vaihe)</span><span class="sxs-lookup"><span data-stu-id="8607d-133">Apply Project Operations Finance demo data (optional step)</span></span>

<span data-ttu-id="8607d-134">Käytä Project Operationsin Finance-esittelytietoja 10.0.13-palvelujulkaisun pilvessä isännöityyn ympäristöön, kuten kuvattu [tässä artikkelissa](resource-apply-finance-demo-data.md).</span><span class="sxs-lookup"><span data-stu-id="8607d-134">Apply Project Operations Finance demo data to 10.0.13 service release Cloud Hosted Environment as described in [this article](resource-apply-finance-demo-data.md).</span></span>

## <a name="apply-updates-to-the-finance-environment"></a><span data-ttu-id="8607d-135">Ota päivitykset käyttöön Finance-ympäristössä</span><span class="sxs-lookup"><span data-stu-id="8607d-135">Apply updates to the Finance environment</span></span>

<span data-ttu-id="8607d-136">Project Operations edellyttää Finance-ympäristöä, jossa on sovellusversio **10.0.13 (10.0.569.20009)** tai uudempi.</span><span class="sxs-lookup"><span data-stu-id="8607d-136">Project Operations requires a Finance environment with application version **10.0.13 (10.0.569.20009)** or higher.</span></span>

<span data-ttu-id="8607d-137">Sinun täytyy ehkä ottaa käyttöön laatupäivityksiä Finance-ympäristössäsi, jotta saat tämän version.</span><span class="sxs-lookup"><span data-stu-id="8607d-137">You might need to apply quality updates to your Finance environment to receive this version.</span></span>

1. <span data-ttu-id="8607d-138">Valitse LCS:n **Ympäristön tiedot** -sivun **Saatavilla olevat päivitykset** -kohdassa **Näytä päivitys**.</span><span class="sxs-lookup"><span data-stu-id="8607d-138">In LCS, on the **Environment details** page, in the **Available Updates** section, select **View Update**.</span></span>

![Näytä päivitykset](./media/5ViewUpdates.png)

2. <span data-ttu-id="8607d-140">Valitse **Binaaripäivitykset**-sivulla **Tallenna paketti.**</span><span class="sxs-lookup"><span data-stu-id="8607d-140">On the **Binary updates** page, select **Save package.**</span></span>

![Tallenna paketti](./media/6SavePackage.png)

3. <span data-ttu-id="8607d-142">Valitse **Valitse kaikki** ja sitten **Tallenna paketti**.</span><span class="sxs-lookup"><span data-stu-id="8607d-142">Click **Select all** and then select **Save package**.</span></span>

![Päivitysten tarkistaminen ja tallentaminen](./media/7ReviewAndSaveUpdates.png)

4. <span data-ttu-id="8607d-144">Kirjoita paketin nimi ja kuvaus ja valitse sitten **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="8607d-144">Enter a name and a description of the package, and then select **Save**.</span></span> <span data-ttu-id="8607d-145">Internet-yhteydestä riippuen tämä prosessi voi kestää jonkin aikaa.</span><span class="sxs-lookup"><span data-stu-id="8607d-145">Depending on the internet connection, this process might take some time.</span></span>

![Lataa paketti Resurssit-kirjastoon](./media/8UploadPackageToAssetsLibrary.png)

5. <span data-ttu-id="8607d-147">Kun paketti on tallennettu, valitse **Valmis** ja tallenna paketti LCS-projektin Resurssit-kirjastoon.</span><span class="sxs-lookup"><span data-stu-id="8607d-147">After the package is saved, select **Done** and save this package to the Assets library in your LCS project.</span></span>

<span data-ttu-id="8607d-148">Paketin tallentaminen ja tarkistaminen voi kestää noin 15 minuuttia.</span><span class="sxs-lookup"><span data-stu-id="8607d-148">Saving and validating the package might take ~15 minutes.</span></span>

6. <span data-ttu-id="8607d-149">Voit ottaa päivityksen käyttöön siirtymällä LCS:n **Ympäristön tiedot** -sivulle ja valitsemalla **Ylläpidä** > **Ota päivitykset käyttöön**.</span><span class="sxs-lookup"><span data-stu-id="8607d-149">To apply the update, navigate to the **Environment details** page in LCS and select **Maintain** > **Apply updates**.</span></span>

![Ympäristöjen ylläpito](./media/9MaintainEnvironment.png)

7. <span data-ttu-id="8607d-151">Valitse päivitysluettelosta luomasi paketti ja valitse sitten **Käytä**.</span><span class="sxs-lookup"><span data-stu-id="8607d-151">In the updates list select the package you created, and select **Apply**.</span></span>

![Päivitysten ottaminen käyttöön](./media/10ApplyUpdates.png)

<span data-ttu-id="8607d-153">Ympäristön huolto kestää jonkin aikaa.</span><span class="sxs-lookup"><span data-stu-id="8607d-153">Environment servicing will take some time.</span></span> <span data-ttu-id="8607d-154">Kun ympäristö on valmis, se palaa käyttöön otettuun tilaan.</span><span class="sxs-lookup"><span data-stu-id="8607d-154">After it is complete, the environment will return to a deployed state.</span></span>

![Ympäristö otettu käyttöön](./media/11EnvironmentDeployed.png)

## <a name="establish-a-dual-write-connection"></a><span data-ttu-id="8607d-156">Kaksinkertaisen kirjoituksen yhteyden muodostaminen</span><span class="sxs-lookup"><span data-stu-id="8607d-156">Establish a Dual Write connection</span></span> 

1. <span data-ttu-id="8607d-157">Siirry LCS-projektissa **Ympäristön tiedot** -sivulle.</span><span class="sxs-lookup"><span data-stu-id="8607d-157">In your LCS project, go to the **Environment details** page.</span></span>
2. <span data-ttu-id="8607d-158">**Common Data Service -ympäristön tiedot** -kohdassa **Linkitä CDS for Appsiin**.</span><span class="sxs-lookup"><span data-stu-id="8607d-158">Under **Common Data Service Environment Information**, select **Link to CDS for Apps**.</span></span>
3. <span data-ttu-id="8607d-159">Kun linkki on valmis, valitse uudelleen **Linkitä CDS for Appsiin**.</span><span class="sxs-lookup"><span data-stu-id="8607d-159">After the link is complete, select **Link to CDS for Apps** again.</span></span> <span data-ttu-id="8607d-160">Sinut ohjataan Financen kaksoiskirjoitukseen.</span><span class="sxs-lookup"><span data-stu-id="8607d-160">You will be redirected to Dual Write in Finance.</span></span>

![Linkitä CDS:ään](./media/12LinktoCDS.png)

4. <span data-ttu-id="8607d-162">Valitse **Käytä ratkaisua**, kun haluat käyttää entiteettejä, jotkan yhdistetään integrointiin.</span><span class="sxs-lookup"><span data-stu-id="8607d-162">Select **Apply Solution** to access the entities that will be mapped in the integration.</span></span>

![Ota ratkaisut käyttöön](./media/13ApplySolutions.png)

5. <span data-ttu-id="8607d-164">Valitse molemmat ratkaisut,, **Dynamics 365 Finance and Operations – kaksoiskirjoituksen entiteettikartta** and **Dynamics 365 Project Operations – Kaksoiskirjoituksen entiteettikartat**, ja valitse sitten **Käytä**.</span><span class="sxs-lookup"><span data-stu-id="8607d-164">Select both solutions, **Dynamics 365 Finance and Operations Dual Write Entity Map** and **Dynamics 365 Project Operations Dual Write Entity Maps**, and then select **Apply**.</span></span>

![Ratkaisujen vahvistaminen](./media/14ConfirmSolutions.png)

<span data-ttu-id="8607d-166">Kun ratkaisut on otettu käyttöön, kaksoiskirjoituskohteet otetaan käyttöön ympäristössä.</span><span class="sxs-lookup"><span data-stu-id="8607d-166">After the solutions are applied, the Dual Write entities are applied to the environment.</span></span>

![Ratkaisujen käyttöönotto](./media/15ApplyingSolutions.png)

<span data-ttu-id="8607d-168">Kun entiteetit otetaan käyttöön, kaikki käytettävissä olevat yhdistämismääritykset näkyvät ympäristössä.</span><span class="sxs-lookup"><span data-stu-id="8607d-168">After the entities are applied, all available mappings are listed in the environment.</span></span>

![Kaksoiskirjoituksen yhdistämismääritykset](./media/15DWMappings.png)

## <a name="refresh-the-data-entities-after-the-update"></a><span data-ttu-id="8607d-170">Päivitä tietoentiteetit päivityksen jälkeen</span><span class="sxs-lookup"><span data-stu-id="8607d-170">Refresh the data entities after the update</span></span>

1. <span data-ttu-id="8607d-171">Siirry Financessa **Tietojen hallinta** -työtilaan.</span><span class="sxs-lookup"><span data-stu-id="8607d-171">In Finance, go to the **Data management** workspace.</span></span>

![Tietojen hallinnan työtila](./media/16DataManagement.png)

2. <span data-ttu-id="8607d-173">Valitse **Kehyksen parametrit** -ruutu.</span><span class="sxs-lookup"><span data-stu-id="8607d-173">Select the **Framework parameters** tile.</span></span>

![Kehyksen parametrit](./media/17FrameworkParameters.png)

3. <span data-ttu-id="8607d-175">Valitse **Entiteetin asetukset** -sivulla **Päivitä entiteettiluettelo**.</span><span class="sxs-lookup"><span data-stu-id="8607d-175">On the **Entity settings** page, select **Refresh Entity list**.</span></span>

![Päivitä entiteettiluettelo](./media/18RefreshEntityList.png)

<span data-ttu-id="8607d-177">Päivitys kestää noin 20 minuuttia.</span><span class="sxs-lookup"><span data-stu-id="8607d-177">The refresh is going to take approximately 20 minutes.</span></span> <span data-ttu-id="8607d-178">Saat ilmoituksen, kun se on valmis.</span><span class="sxs-lookup"><span data-stu-id="8607d-178">You will receive an alert when it is complete.</span></span>

![Päivityksen vahvistus](./media/19RefreshConfirmation.png)

## <a name="run-project-operations-dual-write-maps"></a><span data-ttu-id="8607d-180">Suorita Project Operationsin kaksoiskirjoituksen yhdistämismääritykset</span><span class="sxs-lookup"><span data-stu-id="8607d-180">Run Project Operations Dual Write maps</span></span>

1. <span data-ttu-id="8607d-181">Siirry LCS-projektissa **Ympäristön tiedot** -sivulle.</span><span class="sxs-lookup"><span data-stu-id="8607d-181">In your LCS project, go to the **Environment details** page.</span></span>
2. <span data-ttu-id="8607d-182">Valitse **Common Data Service -ympäristön tiedot** -kohdassa **Linkitä CDS for Appsiin.**</span><span class="sxs-lookup"><span data-stu-id="8607d-182">Under **Common Data Service Environment Information**, select **Link to CDS for Apps.**</span></span> <span data-ttu-id="8607d-183">Kun olet valinnut linkin, sinut ohjataan yhdistämismääritysten entiteettiluetteloon.</span><span class="sxs-lookup"><span data-stu-id="8607d-183">After you select the link, you will be redirected to the list of entities in the mappings.</span></span>
3. <span data-ttu-id="8607d-184">Käynnistä yhdistäm,ismääritykset seuraavassa taulukossa kuvatulla tavalla.</span><span class="sxs-lookup"><span data-stu-id="8607d-184">Start the maps as described in the following table.</span></span> <span data-ttu-id="8607d-185">Varmista, että seuraat järjestystä luettelossa.</span><span class="sxs-lookup"><span data-stu-id="8607d-185">Make sure to follow the sequence as listed.</span></span>

| <span data-ttu-id="8607d-186">**Entiteetin yhdistämismääritys**</span><span class="sxs-lookup"><span data-stu-id="8607d-186">**Entity Map**</span></span> | <span data-ttu-id="8607d-187">**Päivitä entiteetti**</span><span class="sxs-lookup"><span data-stu-id="8607d-187">**Refresh entity**</span></span> | <span data-ttu-id="8607d-188">**Ensimmäinen synkronointi**</span><span class="sxs-lookup"><span data-stu-id="8607d-188">**Initial sync**</span></span> | <span data-ttu-id="8607d-189">**Ensimmäisen synkronoinnin pääkohde**</span><span class="sxs-lookup"><span data-stu-id="8607d-189">**Master for initial sync**</span></span> | <span data-ttu-id="8607d-190">**Suorita edellytykset**</span><span class="sxs-lookup"><span data-stu-id="8607d-190">**Run prerequisites**</span></span> | <span data-ttu-id="8607d-191">**Edellytysten ensimmäinen synkronointi**</span><span class="sxs-lookup"><span data-stu-id="8607d-191">**Prerequisites initial sync**</span></span> |
| --- | --- | --- | --- | --- | --- |
| <span data-ttu-id="8607d-192">**Kaikkien yritysten projektiresurssiroolit (bookableresourcecategories)**</span><span class="sxs-lookup"><span data-stu-id="8607d-192">**Project Resource Roles for All Companies (bookableresourcecategories)**</span></span> | <span data-ttu-id="8607d-193">No</span><span class="sxs-lookup"><span data-stu-id="8607d-193">No</span></span> | <span data-ttu-id="8607d-194">Kyllä</span><span class="sxs-lookup"><span data-stu-id="8607d-194">Yes</span></span> | <span data-ttu-id="8607d-195">Common Data Service</span><span class="sxs-lookup"><span data-stu-id="8607d-195">Common Data Service</span></span> | <span data-ttu-id="8607d-196">No</span><span class="sxs-lookup"><span data-stu-id="8607d-196">No</span></span> | <span data-ttu-id="8607d-197">–</span><span class="sxs-lookup"><span data-stu-id="8607d-197">N\A</span></span> |
| <span data-ttu-id="8607d-198">**Yritykset (cdm\_companies)**</span><span class="sxs-lookup"><span data-stu-id="8607d-198">**Legal entities (cdm\_companies)**</span></span> | <span data-ttu-id="8607d-199">No</span><span class="sxs-lookup"><span data-stu-id="8607d-199">No</span></span> | <span data-ttu-id="8607d-200">Kyllä</span><span class="sxs-lookup"><span data-stu-id="8607d-200">Yes</span></span> | <span data-ttu-id="8607d-201">Finance and Operations -sovellukset</span><span class="sxs-lookup"><span data-stu-id="8607d-201">Finance and Operations apps</span></span> | <span data-ttu-id="8607d-202">No</span><span class="sxs-lookup"><span data-stu-id="8607d-202">No</span></span> | <span data-ttu-id="8607d-203">–</span><span class="sxs-lookup"><span data-stu-id="8607d-203">N\A</span></span> |
| <span data-ttu-id="8607d-204">**Project Operations -integroinnin todelliset arvot (msdyn\_actuals)**</span><span class="sxs-lookup"><span data-stu-id="8607d-204">**Project Operations integration actuals (msdyn\_actuals)**</span></span> | <span data-ttu-id="8607d-205">No</span><span class="sxs-lookup"><span data-stu-id="8607d-205">No</span></span> | <span data-ttu-id="8607d-206">No</span><span class="sxs-lookup"><span data-stu-id="8607d-206">No</span></span> | <span data-ttu-id="8607d-207">–</span><span class="sxs-lookup"><span data-stu-id="8607d-207">N\A</span></span> | <span data-ttu-id="8607d-208">Kyllä</span><span class="sxs-lookup"><span data-stu-id="8607d-208">Yes</span></span> | <span data-ttu-id="8607d-209">No</span><span class="sxs-lookup"><span data-stu-id="8607d-209">No</span></span> |
| <span data-ttu-id="8607d-210">**Projektin sopimusrivit (salesorderdetails)**</span><span class="sxs-lookup"><span data-stu-id="8607d-210">**Project contract lines (salesorderdetails)**</span></span> | <span data-ttu-id="8607d-211">No</span><span class="sxs-lookup"><span data-stu-id="8607d-211">No</span></span> | <span data-ttu-id="8607d-212">No</span><span class="sxs-lookup"><span data-stu-id="8607d-212">No</span></span> | <span data-ttu-id="8607d-213">–</span><span class="sxs-lookup"><span data-stu-id="8607d-213">N\A</span></span> | <span data-ttu-id="8607d-214">No</span><span class="sxs-lookup"><span data-stu-id="8607d-214">No</span></span> | <span data-ttu-id="8607d-215">No</span><span class="sxs-lookup"><span data-stu-id="8607d-215">No</span></span> |
| <span data-ttu-id="8607d-216">**Projektitapahtuman integrointikohdesuhteet (msdyn\_transactionconnections)**</span><span class="sxs-lookup"><span data-stu-id="8607d-216">**Integration entity for project transaction relationships (msdyn\_transactionconnections)**</span></span> | <span data-ttu-id="8607d-217">No</span><span class="sxs-lookup"><span data-stu-id="8607d-217">No</span></span> | <span data-ttu-id="8607d-218">No</span><span class="sxs-lookup"><span data-stu-id="8607d-218">No</span></span> | <span data-ttu-id="8607d-219">–</span><span class="sxs-lookup"><span data-stu-id="8607d-219">N\A</span></span> | <span data-ttu-id="8607d-220">No</span><span class="sxs-lookup"><span data-stu-id="8607d-220">No</span></span> | <span data-ttu-id="8607d-221">–</span><span class="sxs-lookup"><span data-stu-id="8607d-221">N\A</span></span> |
| <span data-ttu-id="8607d-222">**Project Operations -integroinnin sopimusrivin välitavoitteet (msdyn\_contractlinesscheduleofvalues)**</span><span class="sxs-lookup"><span data-stu-id="8607d-222">**Project Operations integration contract line milestones (msdyn\_contractlinesscheduleofvalues)**</span></span> | <span data-ttu-id="8607d-223">No</span><span class="sxs-lookup"><span data-stu-id="8607d-223">No</span></span> | <span data-ttu-id="8607d-224">No</span><span class="sxs-lookup"><span data-stu-id="8607d-224">No</span></span> | <span data-ttu-id="8607d-225">–</span><span class="sxs-lookup"><span data-stu-id="8607d-225">N\A</span></span> | <span data-ttu-id="8607d-226">No</span><span class="sxs-lookup"><span data-stu-id="8607d-226">No</span></span> | <span data-ttu-id="8607d-227">–</span><span class="sxs-lookup"><span data-stu-id="8607d-227">N\A</span></span> |
| <span data-ttu-id="8607d-228">**Project Operations -integrointikohde kuluarvioita varten (msdyn\_estimateslines)**</span><span class="sxs-lookup"><span data-stu-id="8607d-228">**Project Operations integration entity for expense estimates (msdyn\_estimateslines)**</span></span> | <span data-ttu-id="8607d-229">No</span><span class="sxs-lookup"><span data-stu-id="8607d-229">No</span></span> | <span data-ttu-id="8607d-230">No</span><span class="sxs-lookup"><span data-stu-id="8607d-230">No</span></span> | <span data-ttu-id="8607d-231">–</span><span class="sxs-lookup"><span data-stu-id="8607d-231">N\A</span></span> | <span data-ttu-id="8607d-232">No</span><span class="sxs-lookup"><span data-stu-id="8607d-232">No</span></span> | <span data-ttu-id="8607d-233">–</span><span class="sxs-lookup"><span data-stu-id="8607d-233">N\A</span></span> |
| <span data-ttu-id="8607d-234">**Project Operations -integrointikohde tuntiarvioita varten (msdyn\_resourceassignments)**</span><span class="sxs-lookup"><span data-stu-id="8607d-234">**Project Operations integration entity for hour estimates (msdyn\_resourceassignments)**</span></span> | <span data-ttu-id="8607d-235">No</span><span class="sxs-lookup"><span data-stu-id="8607d-235">No</span></span> | <span data-ttu-id="8607d-236">No</span><span class="sxs-lookup"><span data-stu-id="8607d-236">No</span></span> | <span data-ttu-id="8607d-237">–</span><span class="sxs-lookup"><span data-stu-id="8607d-237">N\A</span></span> | <span data-ttu-id="8607d-238">No</span><span class="sxs-lookup"><span data-stu-id="8607d-238">No</span></span> | <span data-ttu-id="8607d-239">–</span><span class="sxs-lookup"><span data-stu-id="8607d-239">N\A</span></span> |
| <span data-ttu-id="8607d-240">**Project Operations -integroinnin projektikulujen vientientiteetti (msdyn\_expenses)**</span><span class="sxs-lookup"><span data-stu-id="8607d-240">**Project Operations integration project expenses export entity (msdyn\_expenses)**</span></span> | <span data-ttu-id="8607d-241">Kyllä</span><span class="sxs-lookup"><span data-stu-id="8607d-241">Yes</span></span> | <span data-ttu-id="8607d-242">No</span><span class="sxs-lookup"><span data-stu-id="8607d-242">No</span></span> | <span data-ttu-id="8607d-243">–</span><span class="sxs-lookup"><span data-stu-id="8607d-243">N\A</span></span> | <span data-ttu-id="8607d-244">No</span><span class="sxs-lookup"><span data-stu-id="8607d-244">No</span></span> | <span data-ttu-id="8607d-245">–</span><span class="sxs-lookup"><span data-stu-id="8607d-245">N\A</span></span> |
| <span data-ttu-id="8607d-246">**Project Operations -integrointikohde tuntiarvioita varten (msdyn\_resourceassignments)**</span><span class="sxs-lookup"><span data-stu-id="8607d-246">**Project Operations integration entity for hour estimates (msdyn\_resourceassignments)**</span></span> | <span data-ttu-id="8607d-247">Kyllä</span><span class="sxs-lookup"><span data-stu-id="8607d-247">Yes</span></span> | <span data-ttu-id="8607d-248">No</span><span class="sxs-lookup"><span data-stu-id="8607d-248">No</span></span> | <span data-ttu-id="8607d-249">–</span><span class="sxs-lookup"><span data-stu-id="8607d-249">N\A</span></span> | <span data-ttu-id="8607d-250">No</span><span class="sxs-lookup"><span data-stu-id="8607d-250">No</span></span> | <span data-ttu-id="8607d-251">–</span><span class="sxs-lookup"><span data-stu-id="8607d-251">N\A</span></span> |

4. <span data-ttu-id="8607d-252">Jos haluat päivittää entiteetin, valitse yhdistämismäärityksen nimi ja valitse sitten **Päivitä entiteetit**.</span><span class="sxs-lookup"><span data-stu-id="8607d-252">To refresh the entity, select the map name, and then select **Refresh entities**.</span></span> 
5. <span data-ttu-id="8607d-253">Jatka suorittamalla yhdistämismääritys, kun päivitys on valmis.</span><span class="sxs-lookup"><span data-stu-id="8607d-253">Proceed with running the map after the refresh is complete.</span></span>

![Päivitä yhdistämismääritys](./media/20RefreshMapping.png)

<span data-ttu-id="8607d-255">Ennen kuin otat seuraavan yhdistämismäärityksen käyttöön, tarkista, että taulukon yhdistämismääritys on tilassa **Käynnissä**.</span><span class="sxs-lookup"><span data-stu-id="8607d-255">Before you enable the next map, verify that the map in the table is in a state of **Running**.</span></span> <span data-ttu-id="8607d-256">Sellaisten yhdistämismääritysten suorittaminen, joissa on paljon edellytyksiä, voi kestää jonkin aikaa.</span><span class="sxs-lookup"><span data-stu-id="8607d-256">Running maps with a larger number of prerequisites might take some time.</span></span>

<span data-ttu-id="8607d-257">Jos haluat suorittaa yhdistämismääritys ja edellytykset, ota käyttöön **Näytä liittyvät entiteetin yhdistämismääritykset** -valintapainike.</span><span class="sxs-lookup"><span data-stu-id="8607d-257">To run a map with prerequisites, enable the **Show related entity maps** toggle.</span></span> <span data-ttu-id="8607d-258">Jos taulukko osoittaa **Edellytyksen ensimmäinen synkronointi** -kohdaas arvo **Ei**, tarkista, että **Ensimmäinen synkronointi** -merkintä on **Ei käytössä** kaikissa edellytysyhdistämismäärityksissä, ennen kuin suoritat sen.</span><span class="sxs-lookup"><span data-stu-id="8607d-258">If the table indicates **Prerequisite initial sync** is **No**, verify that the **Initial sync** flag is **Off** in all the prerequisite maps before you run it.</span></span>

![Suorita yhdistämismääritys](./media/21RunMap.png)

6. <span data-ttu-id="8607d-260">Tarkista, että kaikki projektiin liittyvät yhdistämismääritykset ovat Käynnissä-tilassa.</span><span class="sxs-lookup"><span data-stu-id="8607d-260">Validate all project related maps are in the running state.</span></span>

![Kaikki yhdistämismääritykset käynnissä](./media/22AllMapsRunning.png)

<span data-ttu-id="8607d-262">Project Operations -ympäristö on nyt valmisteltu ja määritetty.</span><span class="sxs-lookup"><span data-stu-id="8607d-262">Your Project Operations environment is now provisioned and configured.</span></span>
