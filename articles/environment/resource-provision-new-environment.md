---
title: Uuden ympäristön valmisteleminen
description: Tässä aiheessa on tietoja siitä, miten uuden Project Operations -ympäristön voi valmistella.
author: sigitac
manager: Annbe
ms.date: 10/26/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 9ed502a1312b702e029d8910d62f72b8e0e4df06
ms.sourcegitcommit: 573be7e36604ace82b35e439cfa748aa7c587415
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/25/2020
ms.locfileid: "4642963"
---
# <a name="provision-a-new-environment"></a><span data-ttu-id="0842c-103">Uuden ympäristön valmisteleminen</span><span class="sxs-lookup"><span data-stu-id="0842c-103">Provision a new environment</span></span>

<span data-ttu-id="0842c-104">_**Käytetään:** Project Operationsin resursseihin ja ei-varastoitaviin perustuvissa skenaarioissa_</span><span class="sxs-lookup"><span data-stu-id="0842c-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="0842c-105">Tässä aiheessa on tietoja uuden Dynamics 365 Project Operations -ympäristön valmistelusta resurssi/ei-varastoitava -pohjaisille skenaarioille.</span><span class="sxs-lookup"><span data-stu-id="0842c-105">This topic provides information about how to provision a new Dynamics 365 Project Operations environment for resource/non-stocked based scenarios.</span></span>

## <a name="enable-project-operations-automated-provisioning-in-an-lcs-project"></a><span data-ttu-id="0842c-106">Project Operationsin automaattisen valmistelun käyttöönotto LCS-projektissa</span><span class="sxs-lookup"><span data-stu-id="0842c-106">Enable Project Operations automated provisioning in an LCS project</span></span>

<span data-ttu-id="0842c-107">Käytä seuraavia vaiheita, kun haluat ottaa käyttöön Project Operationsin automatisoidun valmistelutyönkulun LCS-projektillesi.</span><span class="sxs-lookup"><span data-stu-id="0842c-107">Use following steps to enable the Project Operations automated provisioning flow for your LCS project.</span></span>

1. <span data-ttu-id="0842c-108">Siirry [LCS:sään](https://lcs.dynamics.com/v2) ja valitse **Esiversio-ominaisuuksien hallinta** -ruutu.</span><span class="sxs-lookup"><span data-stu-id="0842c-108">Go to [LCS](https://lcs.dynamics.com/v2) and select the **Preview Feature management** tile.</span></span>
2. <span data-ttu-id="0842c-109">Valitse **Esiversio-ominaisuus** -luettelosta **Project Operations -ominaisuus** ja ota sitten Project Operations käyttöön valitsemalla **Esiversio-ominaisuus käytössä**.</span><span class="sxs-lookup"><span data-stu-id="0842c-109">In the **Preview feature** list, select **Project Operations Feature**, and then select **Preview feature enabled** to enable Project Operations.</span></span>

> [!NOTE]
> <span data-ttu-id="0842c-110">Tämä vaihe suoritetaan vain kerran LCS-projektia kohden.</span><span class="sxs-lookup"><span data-stu-id="0842c-110">This step is performed only one time per LCS project.</span></span>

## <a name="provision-a-project-operations-environment"></a><span data-ttu-id="0842c-111">Project Operations -ympäristön tarjoaminen</span><span class="sxs-lookup"><span data-stu-id="0842c-111">Provision a Project Operations environment</span></span>

1. <span data-ttu-id="0842c-112">Avaa uusi Dynamics 365 Finance [-esittely-ympäristön](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) tai [eristys-/tuotantoympäristön](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deployenvironment-newinfrastructure) käyttöönotto.</span><span class="sxs-lookup"><span data-stu-id="0842c-112">Open a new Dynamics 365 Finance [demo environment](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) or [sandbox/ production environment](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deployenvironment-newinfrastructure) deployment.</span></span> 
2. <span data-ttu-id="0842c-113">Suorita ohjatun **Ympäristön valmistelu** -toiminnon vaiheet.</span><span class="sxs-lookup"><span data-stu-id="0842c-113">Walk through the **Environment provisioning** wizard.</span></span> 

> [!IMPORTANT]
> <span data-ttu-id="0842c-114">Varmista, että valittu sovellusversio on 10.0.13 tai uudempi.</span><span class="sxs-lookup"><span data-stu-id="0842c-114">Make sure selected application version is 10.0.13 or higher.</span></span>

3. <span data-ttu-id="0842c-115">Jos haluat valmistella Project Operationsi, valitse **Lisäasetukset**-kohdassa **Common Data Service**.</span><span class="sxs-lookup"><span data-stu-id="0842c-115">To provision Project Operations, under **Advance settings**, select **Common Data Service**.</span></span> 
4. <span data-ttu-id="0842c-116">Ota **Common Data Service -asetukset** käyttöön valitsemalla **Kyllä** ja kirjoitramalla tiedot pakollisiin kenttiin:</span><span class="sxs-lookup"><span data-stu-id="0842c-116">Enable the **Common Data Service Setting** by selecting **Yes** and then enter information in the required fields:</span></span>

  - <span data-ttu-id="0842c-117">Nimi</span><span class="sxs-lookup"><span data-stu-id="0842c-117">Name</span></span>
  - <span data-ttu-id="0842c-118">Alue</span><span class="sxs-lookup"><span data-stu-id="0842c-118">Region</span></span>
  - <span data-ttu-id="0842c-119">Language</span><span class="sxs-lookup"><span data-stu-id="0842c-119">Language</span></span>
  - <span data-ttu-id="0842c-120">Valuutta</span><span class="sxs-lookup"><span data-stu-id="0842c-120">Currency</span></span>
 
5. <span data-ttu-id="0842c-121">Valitse **Common Data Service -malli** -kentässä **Project Operations**</span><span class="sxs-lookup"><span data-stu-id="0842c-121">In the **Common Data Service Template** field, select **Project Operations**</span></span> 

6. <span data-ttu-id="0842c-122">Valitse käyttöönoton ympäristötyyppi.</span><span class="sxs-lookup"><span data-stu-id="0842c-122">Select the environment type for your deployment.</span></span> <span data-ttu-id="0842c-123">Tilauspohjaisen kokeiluversion avulla voit käyttää CDS-ympäristöä 30 päivän ajan.</span><span class="sxs-lookup"><span data-stu-id="0842c-123">A subscription-based trial will let you deploy a CDS environment for 30 days.</span></span> 

![Käyttööntoton asetukset](./media/1DeploymentSettings.png)

> [!IMPORTANT]
> <span data-ttu-id="0842c-125">Valitse **Hyväksy**, kun hyväksyt palveluehdot, ja palaa sitten käyttöönottoasetuksiin valitsemalla **Valmis**.</span><span class="sxs-lookup"><span data-stu-id="0842c-125">Select **Agree** to acknowledge the terms of service and then select **Done** to return to the deployment settings.</span></span>

![Käyttöönoton suostumus](./media/2DeploymentConsent.png)

7. <span data-ttu-id="0842c-127">Täytä loput pakolliset kentät ohjatussa toiminnossa ja vahvista asennus.</span><span class="sxs-lookup"><span data-stu-id="0842c-127">Complete the remaining required fields in the wizard and confirm the deployment.</span></span> <span data-ttu-id="0842c-128">Ympäristön valmisteluaika vaihtelee ympäristötyypin mukaan.</span><span class="sxs-lookup"><span data-stu-id="0842c-128">Environment provisioning time varies based on the environment type.</span></span> <span data-ttu-id="0842c-129">Valmistelu voi kestää jopa kuusi tuntia.</span><span class="sxs-lookup"><span data-stu-id="0842c-129">Provisioning might take up to six hours.</span></span>

  <span data-ttu-id="0842c-130">Kun käyttöönotto on valmis, ympäristö näkyy tilassa **Otettu käyttöön**.</span><span class="sxs-lookup"><span data-stu-id="0842c-130">After the deployment completes successfully, the environment will show as **Deployed**.</span></span>

8. <span data-ttu-id="0842c-131">Varmista, että ympäristö on otettu käyttöön, valitsemalla **Kirjaudu** ja kirjautumalla ympäristöön sekä tarkistamalla käyttöönoton tilan.</span><span class="sxs-lookup"><span data-stu-id="0842c-131">To confirm the environment has deployed successfully, select **Login** and log on to the environment to confirm.</span></span>

![-ympäristön tiedot](./media/3EnvironmentDetails.png)

## <a name="apply-project-operations-finance-demo-data-optional-step"></a><span data-ttu-id="0842c-133">Project Operationsin Finance -esittelytietojen käyttöönotto (valinnainen vaihe)</span><span class="sxs-lookup"><span data-stu-id="0842c-133">Apply Project Operations Finance demo data (optional step)</span></span>

<span data-ttu-id="0842c-134">Käytä Project Operationsin Finance-esittelytietoja 10.0.13-palvelujulkaisun pilvessä isännöityyn ympäristöön, kuten kuvattu [tässä artikkelissa](resource-apply-finance-demo-data.md).</span><span class="sxs-lookup"><span data-stu-id="0842c-134">Apply Project Operations Finance demo data to 10.0.13 service release Cloud Hosted Environment as described in [this article](resource-apply-finance-demo-data.md).</span></span>

## <a name="apply-updates-to-the-finance-environment"></a><span data-ttu-id="0842c-135">Ota päivitykset käyttöön Finance-ympäristössä</span><span class="sxs-lookup"><span data-stu-id="0842c-135">Apply updates to the Finance environment</span></span>

<span data-ttu-id="0842c-136">Project Operations edellyttää Finance-ympäristöä, jossa on sovellusversio **10.0.13 (10.0.569.20009)** tai uudempi.</span><span class="sxs-lookup"><span data-stu-id="0842c-136">Project Operations requires a Finance environment with application version **10.0.13 (10.0.569.20009)** or higher.</span></span>

<span data-ttu-id="0842c-137">Sinun täytyy ehkä ottaa käyttöön laatupäivityksiä Finance-ympäristössäsi, jotta saat tämän version.</span><span class="sxs-lookup"><span data-stu-id="0842c-137">You might need to apply quality updates to your Finance environment to receive this version.</span></span>

1. <span data-ttu-id="0842c-138">Valitse LCS:n **Ympäristön tiedot** -sivun **Saatavilla olevat päivitykset** -kohdassa **Näytä päivitys**.</span><span class="sxs-lookup"><span data-stu-id="0842c-138">In LCS, on the **Environment details** page, in the **Available Updates** section, select **View Update**.</span></span>

![Näytä päivitykset](./media/5ViewUpdates.png)

2. <span data-ttu-id="0842c-140">Valitse **Binaaripäivitykset**-sivulla **Tallenna paketti.**</span><span class="sxs-lookup"><span data-stu-id="0842c-140">On the **Binary updates** page, select **Save package.**</span></span>

![Tallenna paketti](./media/6SavePackage.png)

3. <span data-ttu-id="0842c-142">Valitse **Valitse kaikki** ja sitten **Tallenna paketti**.</span><span class="sxs-lookup"><span data-stu-id="0842c-142">Click **Select all** and then select **Save package**.</span></span>

![Päivitysten tarkistaminen ja tallentaminen](./media/7ReviewAndSaveUpdates.png)

4. <span data-ttu-id="0842c-144">Kirjoita paketin nimi ja kuvaus ja valitse sitten **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="0842c-144">Enter a name and a description of the package, and then select **Save**.</span></span> <span data-ttu-id="0842c-145">Internet-yhteydestä riippuen tämä prosessi voi kestää jonkin aikaa.</span><span class="sxs-lookup"><span data-stu-id="0842c-145">Depending on the internet connection, this process might take some time.</span></span>

![Lataa paketti Resurssit-kirjastoon](./media/8UploadPackageToAssetsLibrary.png)

5. <span data-ttu-id="0842c-147">Kun paketti on tallennettu, valitse **Valmis** ja tallenna paketti LCS-projektin Resurssit-kirjastoon.</span><span class="sxs-lookup"><span data-stu-id="0842c-147">After the package is saved, select **Done** and save this package to the Assets library in your LCS project.</span></span>

<span data-ttu-id="0842c-148">Paketin tallentaminen ja tarkistaminen voi kestää noin 15 minuuttia.</span><span class="sxs-lookup"><span data-stu-id="0842c-148">Saving and validating the package might take ~15 minutes.</span></span>

6. <span data-ttu-id="0842c-149">Voit ottaa päivityksen käyttöön siirtymällä LCS:n **Ympäristön tiedot** -sivulle ja valitsemalla **Ylläpidä** > **Ota päivitykset käyttöön**.</span><span class="sxs-lookup"><span data-stu-id="0842c-149">To apply the update, navigate to the **Environment details** page in LCS and select **Maintain** > **Apply updates**.</span></span>

![Ympäristöjen ylläpito](./media/9MaintainEnvironment.png)

7. <span data-ttu-id="0842c-151">Valitse päivitysluettelosta luomasi paketti ja valitse sitten **Käytä**.</span><span class="sxs-lookup"><span data-stu-id="0842c-151">In the updates list select the package you created, and select **Apply**.</span></span>

![Päivitysten ottaminen käyttöön](./media/10ApplyUpdates.png)

<span data-ttu-id="0842c-153">Ympäristön huolto kestää jonkin aikaa.</span><span class="sxs-lookup"><span data-stu-id="0842c-153">Environment servicing will take some time.</span></span> <span data-ttu-id="0842c-154">Kun ympäristö on valmis, se palaa käyttöön otettuun tilaan.</span><span class="sxs-lookup"><span data-stu-id="0842c-154">After it is complete, the environment will return to a deployed state.</span></span>

![Ympäristö otettu käyttöön](./media/11EnvironmentDeployed.png)

## <a name="establish-a-dual-write-connection"></a><span data-ttu-id="0842c-156">Kaksinkertaisen kirjoituksen yhteyden muodostaminen</span><span class="sxs-lookup"><span data-stu-id="0842c-156">Establish a Dual Write connection</span></span> 

1. <span data-ttu-id="0842c-157">Siirry LCS-projektissa **Ympäristön tiedot** -sivulle.</span><span class="sxs-lookup"><span data-stu-id="0842c-157">In your LCS project, go to the **Environment details** page.</span></span>
2. <span data-ttu-id="0842c-158">**Common Data Service -ympäristön tiedot** -kohdassa **Linkitä CDS for Appsiin**.</span><span class="sxs-lookup"><span data-stu-id="0842c-158">Under **Common Data Service Environment Information**, select **Link to CDS for Apps**.</span></span>
3. <span data-ttu-id="0842c-159">Kun linkki on valmis, valitse uudelleen **Linkitä CDS for Appsiin**.</span><span class="sxs-lookup"><span data-stu-id="0842c-159">After the link is complete, select **Link to CDS for Apps** again.</span></span> <span data-ttu-id="0842c-160">Sinut ohjataan Financen kaksoiskirjoitukseen.</span><span class="sxs-lookup"><span data-stu-id="0842c-160">You will be redirected to Dual Write in Finance.</span></span>

![Linkitä CDS:ään](./media/12LinktoCDS.png)

4. <span data-ttu-id="0842c-162">Valitse **Käytä ratkaisua**, kun haluat käyttää entiteettejä, jotkan yhdistetään integrointiin.</span><span class="sxs-lookup"><span data-stu-id="0842c-162">Select **Apply Solution** to access the entities that will be mapped in the integration.</span></span>

![Ota ratkaisut käyttöön](./media/13ApplySolutions.png)

5. <span data-ttu-id="0842c-164">Valitse molemmat ratkaisut, **Dynamics 365 Finance and Operations Kaksoiskirjoitusentiteetin yhdistämismääritys** ja **Dynamics 365 Project Operations Kaksoiskirjoitusentiteettien yhdistämismääritykset** ja valitse sitten **Käytä**.</span><span class="sxs-lookup"><span data-stu-id="0842c-164">Select both solutions, **Dynamics 365 Finance and Operations Dual Write Entity Map** and **Dynamics 365 Project Operations Dual Write Entity Maps**, and then select **Apply**.</span></span>

![Ratkaisujen vahvistaminen](./media/14ConfirmSolutions.png)

<span data-ttu-id="0842c-166">Kun ratkaisut on otettu käyttöön, kaksoiskirjoituskohteet otetaan käyttöön ympäristössä.</span><span class="sxs-lookup"><span data-stu-id="0842c-166">After the solutions are applied, the Dual Write entities are applied to the environment.</span></span>

![Ratkaisujen käyttöönotto](./media/15ApplyingSolutions.png)

<span data-ttu-id="0842c-168">Kun entiteetit otetaan käyttöön, kaikki käytettävissä olevat yhdistämismääritykset näkyvät ympäristössä.</span><span class="sxs-lookup"><span data-stu-id="0842c-168">After the entities are applied, all available mappings are listed in the environment.</span></span>

![Kaksoiskirjoituksen yhdistämismääritykset](./media/15DWMappings.png)

## <a name="refresh-the-data-entities-after-the-update"></a><span data-ttu-id="0842c-170">Päivitä tietoentiteetit päivityksen jälkeen</span><span class="sxs-lookup"><span data-stu-id="0842c-170">Refresh the data entities after the update</span></span>

1. <span data-ttu-id="0842c-171">Siirry Financessa **Tietojen hallinta** -työtilaan.</span><span class="sxs-lookup"><span data-stu-id="0842c-171">In Finance, go to the **Data management** workspace.</span></span>

![Tietojen hallinnan työtila](./media/16DataManagement.png)

2. <span data-ttu-id="0842c-173">Valitse **Kehyksen parametrit** -ruutu.</span><span class="sxs-lookup"><span data-stu-id="0842c-173">Select the **Framework parameters** tile.</span></span>

![Kehyksen parametrit](./media/17FrameworkParameters.png)

3. <span data-ttu-id="0842c-175">Valitse **Entiteetin asetukset** -sivulla **Päivitä entiteettiluettelo**.</span><span class="sxs-lookup"><span data-stu-id="0842c-175">On the **Entity settings** page, select **Refresh Entity list**.</span></span>

![Päivitä entiteettiluettelo](./media/18RefreshEntityList.png)

<span data-ttu-id="0842c-177">Päivitys kestää noin 20 minuuttia.</span><span class="sxs-lookup"><span data-stu-id="0842c-177">The refresh is going to take approximately 20 minutes.</span></span> <span data-ttu-id="0842c-178">Saat ilmoituksen, kun se on valmis.</span><span class="sxs-lookup"><span data-stu-id="0842c-178">You will receive an alert when it is complete.</span></span>

![Päivityksen vahvistus](./media/19RefreshConfirmation.png)

## <a name="run-project-operations-dual-write-maps"></a><span data-ttu-id="0842c-180">Suorita Project Operationsin kaksoiskirjoituksen yhdistämismääritykset</span><span class="sxs-lookup"><span data-stu-id="0842c-180">Run Project Operations Dual Write maps</span></span>

1. <span data-ttu-id="0842c-181">Siirry LCS-projektissa **Ympäristön tiedot** -sivulle.</span><span class="sxs-lookup"><span data-stu-id="0842c-181">In your LCS project, go to the **Environment details** page.</span></span>
2. <span data-ttu-id="0842c-182">Valitse **Common Data Service -ympäristön tiedot** -kohdassa **Linkitä CDS for Appsiin.**</span><span class="sxs-lookup"><span data-stu-id="0842c-182">Under **Common Data Service Environment Information**, select **Link to CDS for Apps.**</span></span> <span data-ttu-id="0842c-183">Kun olet valinnut linkin, sinut ohjataan yhdistämismääritysten entiteettiluetteloon.</span><span class="sxs-lookup"><span data-stu-id="0842c-183">After you select the link, you will be redirected to the list of entities in the mappings.</span></span>
3. <span data-ttu-id="0842c-184">Käynnistä yhdistäm,ismääritykset seuraavassa taulukossa kuvatulla tavalla.</span><span class="sxs-lookup"><span data-stu-id="0842c-184">Start the maps as described in the following table.</span></span> <span data-ttu-id="0842c-185">Varmista, että seuraat järjestystä luettelossa.</span><span class="sxs-lookup"><span data-stu-id="0842c-185">Make sure to follow the sequence as listed.</span></span>

| <span data-ttu-id="0842c-186">**Entiteetin yhdistämismääritys**</span><span class="sxs-lookup"><span data-stu-id="0842c-186">**Entity Map**</span></span> | <span data-ttu-id="0842c-187">**Päivitä entiteetti**</span><span class="sxs-lookup"><span data-stu-id="0842c-187">**Refresh entity**</span></span> | <span data-ttu-id="0842c-188">**Ensimmäinen synkronointi**</span><span class="sxs-lookup"><span data-stu-id="0842c-188">**Initial sync**</span></span> | <span data-ttu-id="0842c-189">**Ensimmäisen synkronoinnin pääkohde**</span><span class="sxs-lookup"><span data-stu-id="0842c-189">**Master for initial sync**</span></span> | <span data-ttu-id="0842c-190">**Suorita edellytykset**</span><span class="sxs-lookup"><span data-stu-id="0842c-190">**Run prerequisites**</span></span> | <span data-ttu-id="0842c-191">**Edellytysten ensimmäinen synkronointi**</span><span class="sxs-lookup"><span data-stu-id="0842c-191">**Prerequisites initial sync**</span></span> |
| --- | --- | --- | --- | --- | --- |
| <span data-ttu-id="0842c-192">**Kaikkien yritysten projektiresurssiroolit (bookableresourcecategories)**</span><span class="sxs-lookup"><span data-stu-id="0842c-192">**Project Resource Roles for All Companies (bookableresourcecategories)**</span></span> | <span data-ttu-id="0842c-193">No</span><span class="sxs-lookup"><span data-stu-id="0842c-193">No</span></span> | <span data-ttu-id="0842c-194">Kyllä</span><span class="sxs-lookup"><span data-stu-id="0842c-194">Yes</span></span> | <span data-ttu-id="0842c-195">Common Data Service</span><span class="sxs-lookup"><span data-stu-id="0842c-195">Common Data Service</span></span> | <span data-ttu-id="0842c-196">No</span><span class="sxs-lookup"><span data-stu-id="0842c-196">No</span></span> | <span data-ttu-id="0842c-197">–</span><span class="sxs-lookup"><span data-stu-id="0842c-197">N\A</span></span> |
| <span data-ttu-id="0842c-198">**Yritykset (cdm\_companies)**</span><span class="sxs-lookup"><span data-stu-id="0842c-198">**Legal entities (cdm\_companies)**</span></span> | <span data-ttu-id="0842c-199">No</span><span class="sxs-lookup"><span data-stu-id="0842c-199">No</span></span> | <span data-ttu-id="0842c-200">Kyllä</span><span class="sxs-lookup"><span data-stu-id="0842c-200">Yes</span></span> | <span data-ttu-id="0842c-201">Finance and Operations -sovellukset</span><span class="sxs-lookup"><span data-stu-id="0842c-201">Finance and Operations apps</span></span> | <span data-ttu-id="0842c-202">No</span><span class="sxs-lookup"><span data-stu-id="0842c-202">No</span></span> | <span data-ttu-id="0842c-203">–</span><span class="sxs-lookup"><span data-stu-id="0842c-203">N\A</span></span> |
| <span data-ttu-id="0842c-204">**Tapahtumarekisteri (msdyn_ledgers)**</span><span class="sxs-lookup"><span data-stu-id="0842c-204">**Ledger (msdyn_ledgers)**</span></span> | <span data-ttu-id="0842c-205">No</span><span class="sxs-lookup"><span data-stu-id="0842c-205">No</span></span> | <span data-ttu-id="0842c-206">Kyllä</span><span class="sxs-lookup"><span data-stu-id="0842c-206">Yes</span></span> | <span data-ttu-id="0842c-207">Finance and Operations -sovellukset</span><span class="sxs-lookup"><span data-stu-id="0842c-207">Finance and Operations apps</span></span> | <span data-ttu-id="0842c-208">Kyllä</span><span class="sxs-lookup"><span data-stu-id="0842c-208">Yes</span></span> | <span data-ttu-id="0842c-209">Kyllä, Finance and Operations -sovellukset</span><span class="sxs-lookup"><span data-stu-id="0842c-209">Yes, Finance and Operations apps</span></span> |
| <span data-ttu-id="0842c-210">**Project Operations -integroinnin todelliset arvot (msdyn\_actuals)**</span><span class="sxs-lookup"><span data-stu-id="0842c-210">**Project Operations integration actuals (msdyn\_actuals)**</span></span> | <span data-ttu-id="0842c-211">No</span><span class="sxs-lookup"><span data-stu-id="0842c-211">No</span></span> | <span data-ttu-id="0842c-212">No</span><span class="sxs-lookup"><span data-stu-id="0842c-212">No</span></span> | <span data-ttu-id="0842c-213">–</span><span class="sxs-lookup"><span data-stu-id="0842c-213">N\A</span></span> | <span data-ttu-id="0842c-214">Kyllä</span><span class="sxs-lookup"><span data-stu-id="0842c-214">Yes</span></span> | <span data-ttu-id="0842c-215">No</span><span class="sxs-lookup"><span data-stu-id="0842c-215">No</span></span> |
| <span data-ttu-id="0842c-216">**Projektin sopimusrivit (salesorderdetails)**</span><span class="sxs-lookup"><span data-stu-id="0842c-216">**Project contract lines (salesorderdetails)**</span></span> | <span data-ttu-id="0842c-217">No</span><span class="sxs-lookup"><span data-stu-id="0842c-217">No</span></span> | <span data-ttu-id="0842c-218">No</span><span class="sxs-lookup"><span data-stu-id="0842c-218">No</span></span> | <span data-ttu-id="0842c-219">–</span><span class="sxs-lookup"><span data-stu-id="0842c-219">N\A</span></span> | <span data-ttu-id="0842c-220">No</span><span class="sxs-lookup"><span data-stu-id="0842c-220">No</span></span> | <span data-ttu-id="0842c-221">No</span><span class="sxs-lookup"><span data-stu-id="0842c-221">No</span></span> |
| <span data-ttu-id="0842c-222">**Projektitapahtuman integrointikohdesuhteet (msdyn\_transactionconnections)**</span><span class="sxs-lookup"><span data-stu-id="0842c-222">**Integration entity for project transaction relationships (msdyn\_transactionconnections)**</span></span> | <span data-ttu-id="0842c-223">No</span><span class="sxs-lookup"><span data-stu-id="0842c-223">No</span></span> | <span data-ttu-id="0842c-224">No</span><span class="sxs-lookup"><span data-stu-id="0842c-224">No</span></span> | <span data-ttu-id="0842c-225">–</span><span class="sxs-lookup"><span data-stu-id="0842c-225">N\A</span></span> | <span data-ttu-id="0842c-226">No</span><span class="sxs-lookup"><span data-stu-id="0842c-226">No</span></span> | <span data-ttu-id="0842c-227">–</span><span class="sxs-lookup"><span data-stu-id="0842c-227">N\A</span></span> |
| <span data-ttu-id="0842c-228">**Project Operations -integroinnin sopimusrivin välitavoitteet (msdyn\_contractlinesscheduleofvalues)**</span><span class="sxs-lookup"><span data-stu-id="0842c-228">**Project Operations integration contract line milestones (msdyn\_contractlinesscheduleofvalues)**</span></span> | <span data-ttu-id="0842c-229">No</span><span class="sxs-lookup"><span data-stu-id="0842c-229">No</span></span> | <span data-ttu-id="0842c-230">No</span><span class="sxs-lookup"><span data-stu-id="0842c-230">No</span></span> | <span data-ttu-id="0842c-231">–</span><span class="sxs-lookup"><span data-stu-id="0842c-231">N\A</span></span> | <span data-ttu-id="0842c-232">No</span><span class="sxs-lookup"><span data-stu-id="0842c-232">No</span></span> | <span data-ttu-id="0842c-233">–</span><span class="sxs-lookup"><span data-stu-id="0842c-233">N\A</span></span> |
| <span data-ttu-id="0842c-234">**Project Operations -integrointikohde kuluarvioita varten (msdyn\_estimateslines)**</span><span class="sxs-lookup"><span data-stu-id="0842c-234">**Project Operations integration entity for expense estimates (msdyn\_estimateslines)**</span></span> | <span data-ttu-id="0842c-235">No</span><span class="sxs-lookup"><span data-stu-id="0842c-235">No</span></span> | <span data-ttu-id="0842c-236">No</span><span class="sxs-lookup"><span data-stu-id="0842c-236">No</span></span> | <span data-ttu-id="0842c-237">–</span><span class="sxs-lookup"><span data-stu-id="0842c-237">N\A</span></span> | <span data-ttu-id="0842c-238">No</span><span class="sxs-lookup"><span data-stu-id="0842c-238">No</span></span> | <span data-ttu-id="0842c-239">–</span><span class="sxs-lookup"><span data-stu-id="0842c-239">N\A</span></span> |
| <span data-ttu-id="0842c-240">**Project Operations -integroinnin projektikululuokkien vientientiteetti (msdyn\_expensecategories)**</span><span class="sxs-lookup"><span data-stu-id="0842c-240">**Project Operations integration project expense categories export entity (msdyn\_expensecategories)**</span></span> | <span data-ttu-id="0842c-241">No</span><span class="sxs-lookup"><span data-stu-id="0842c-241">No</span></span> | <span data-ttu-id="0842c-242">No</span><span class="sxs-lookup"><span data-stu-id="0842c-242">No</span></span> | <span data-ttu-id="0842c-243">–</span><span class="sxs-lookup"><span data-stu-id="0842c-243">N\A</span></span> | <span data-ttu-id="0842c-244">No</span><span class="sxs-lookup"><span data-stu-id="0842c-244">No</span></span> | <span data-ttu-id="0842c-245">–</span><span class="sxs-lookup"><span data-stu-id="0842c-245">N\A</span></span> |
| <span data-ttu-id="0842c-246">**Project Operations -integroinnin projektikulujen vientientiteetti (msdyn\_expenses)**</span><span class="sxs-lookup"><span data-stu-id="0842c-246">**Project Operations integration project expenses export entity (msdyn\_expenses)**</span></span> | <span data-ttu-id="0842c-247">Kyllä</span><span class="sxs-lookup"><span data-stu-id="0842c-247">Yes</span></span> | <span data-ttu-id="0842c-248">No</span><span class="sxs-lookup"><span data-stu-id="0842c-248">No</span></span> | <span data-ttu-id="0842c-249">–</span><span class="sxs-lookup"><span data-stu-id="0842c-249">N\A</span></span> | <span data-ttu-id="0842c-250">No</span><span class="sxs-lookup"><span data-stu-id="0842c-250">No</span></span> | <span data-ttu-id="0842c-251">–</span><span class="sxs-lookup"><span data-stu-id="0842c-251">N\A</span></span> |
| <span data-ttu-id="0842c-252">**Project Operations -integrointikohde tuntiarvioita varten (msdyn\_resourceassignments)**</span><span class="sxs-lookup"><span data-stu-id="0842c-252">**Project Operations integration entity for hour estimates (msdyn\_resourceassignments)**</span></span> | <span data-ttu-id="0842c-253">Kyllä</span><span class="sxs-lookup"><span data-stu-id="0842c-253">Yes</span></span> | <span data-ttu-id="0842c-254">No</span><span class="sxs-lookup"><span data-stu-id="0842c-254">No</span></span> | <span data-ttu-id="0842c-255">–</span><span class="sxs-lookup"><span data-stu-id="0842c-255">N\A</span></span> | <span data-ttu-id="0842c-256">No</span><span class="sxs-lookup"><span data-stu-id="0842c-256">No</span></span> | <span data-ttu-id="0842c-257">–</span><span class="sxs-lookup"><span data-stu-id="0842c-257">N\A</span></span> |


4. <span data-ttu-id="0842c-258">Jos haluat päivittää entiteetin, valitse yhdistämismäärityksen nimi ja valitse sitten **Päivitä entiteetit**.</span><span class="sxs-lookup"><span data-stu-id="0842c-258">To refresh the entity, select the map name, and then select **Refresh entities**.</span></span> 


![Päivitä yhdistämismääritys](./media/20RefreshMapping.png)

5. <span data-ttu-id="0842c-260">Suorita yhdistämismääritys, kun päivitys on valmis.</span><span class="sxs-lookup"><span data-stu-id="0842c-260">After the refresh is complete, run the map.</span></span> <span data-ttu-id="0842c-261">Ennen kuin otat seuraavan yhdistämismäärityksen käyttöön, tarkista, että taulukon yhdistämismääritys on tilassa **Käynnissä**.</span><span class="sxs-lookup"><span data-stu-id="0842c-261">Before you enable the next map, verify that the map in the table is in a state of **Running**.</span></span> <span data-ttu-id="0842c-262">Sellaisten yhdistämismääritysten suorittaminen, joissa on paljon edellytyksiä, voi kestää jonkin aikaa.</span><span class="sxs-lookup"><span data-stu-id="0842c-262">Running maps with a larger number of prerequisites might take some time.</span></span>

<span data-ttu-id="0842c-263">Jos haluat suorittaa yhdistämismääritys ja edellytykset, ota käyttöön **Näytä liittyvät entiteetin yhdistämismääritykset** -valintapainike.</span><span class="sxs-lookup"><span data-stu-id="0842c-263">To run a map with prerequisites, enable the **Show related entity maps** toggle.</span></span> <span data-ttu-id="0842c-264">Jos taulukko osoittaa **Edellytyksen ensimmäinen synkronointi** -kohdaas arvo **Ei**, tarkista, että **Ensimmäinen synkronointi** -merkintä on **Ei käytössä** kaikissa edellytysyhdistämismäärityksissä, ennen kuin suoritat sen.</span><span class="sxs-lookup"><span data-stu-id="0842c-264">If the table indicates **Prerequisite initial sync** is **No**, verify that the **Initial sync** flag is **Off** in all the prerequisite maps before you run it.</span></span>

![Suorita yhdistämismääritys](./media/21RunMap.png)

6. <span data-ttu-id="0842c-266">Tarkista, että kaikki projektiin liittyvät yhdistämismääritykset ovat Käynnissä-tilassa.</span><span class="sxs-lookup"><span data-stu-id="0842c-266">Validate all project related maps are in the running state.</span></span>

![Kaikki yhdistämismääritykset käynnissä](./media/22AllMapsRunning.png)


## <a name="apply-configuration-data-in-cds-for-project-operations-optional"></a><span data-ttu-id="0842c-268">Määritystietojen ottaminen käyttöön Project Operationsin CDS:ssä (valinnainen)</span><span class="sxs-lookup"><span data-stu-id="0842c-268">Apply configuration data in CDS for Project Operations (optional)</span></span>

<span data-ttu-id="0842c-269">Jos olet käyttänyt esittelytietoja Finance-ympäristössä, lisätietoja esittelytietojen käyttämisestä CDS-ympäristössä on kohdassa [Määritystietojen määrittäminen ja käyttäminen Project Operationsin Common Data Servicessa](resource-apply-pro-setup-config-data.md).</span><span class="sxs-lookup"><span data-stu-id="0842c-269">If you have applied demo data to the Finance environment, see [Set up and apply configuration data in the Common Data Service for Project Operations](resource-apply-pro-setup-config-data.md) to apply demo data to CDS environment.</span></span>


<span data-ttu-id="0842c-270">Project Operations -ympäristö on nyt valmisteltu ja määritetty.</span><span class="sxs-lookup"><span data-stu-id="0842c-270">Your Project Operations environment is now provisioned and configured.</span></span> 
