---
title: Uuden ympäristön valmisteleminen
description: Tässä aiheessa on tietoja siitä, miten uuden Project Operations -ympäristön voi valmistella.
author: sigitac
manager: Annbe
ms.date: 12/11/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 09af2a7693c45d1d0b9c75420d018cc50d2cc0fa
ms.sourcegitcommit: 04c446746aad97fc3f4c3d441983c586b918a3a6
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/11/2020
ms.locfileid: "4727786"
---
# <a name="provision-a-new-environment"></a><span data-ttu-id="7cbbd-103">Uuden ympäristön valmisteleminen</span><span class="sxs-lookup"><span data-stu-id="7cbbd-103">Provision a new environment</span></span>

<span data-ttu-id="7cbbd-104">_**Käytetään:** Project Operationsin resursseihin ja ei-varastoitaviin perustuvissa skenaarioissa_</span><span class="sxs-lookup"><span data-stu-id="7cbbd-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="7cbbd-105">Tässä aiheessa on tietoja uuden Dynamics 365 Project Operations -ympäristön valmistelusta resurssi/ei-varastoitava -pohjaisille skenaarioille.</span><span class="sxs-lookup"><span data-stu-id="7cbbd-105">This topic provides information about how to provision a new Dynamics 365 Project Operations environment for resource/non-stocked based scenarios.</span></span>

## <a name="enable-project-operations-automated-provisioning-in-an-lcs-project"></a><span data-ttu-id="7cbbd-106">Project Operationsin automaattisen valmistelun käyttöönotto LCS-projektissa</span><span class="sxs-lookup"><span data-stu-id="7cbbd-106">Enable Project Operations automated provisioning in an LCS project</span></span>

<span data-ttu-id="7cbbd-107">Käytä seuraavia vaiheita, kun haluat ottaa käyttöön Project Operationsin automatisoidun valmistelutyönkulun LCS-projektillesi.</span><span class="sxs-lookup"><span data-stu-id="7cbbd-107">Use following steps to enable the Project Operations automated provisioning flow for your LCS project.</span></span>

1. <span data-ttu-id="7cbbd-108">Siirry [LCS:sään](https://lcs.dynamics.com/v2) ja valitse **Esiversio-ominaisuuksien hallinta** -ruutu.</span><span class="sxs-lookup"><span data-stu-id="7cbbd-108">Go to [LCS](https://lcs.dynamics.com/v2) and select the **Preview Feature management** tile.</span></span>
2. <span data-ttu-id="7cbbd-109">Valitse **Esiversio-ominaisuus** -luettelosta **Project Operations -ominaisuus** ja ota sitten Project Operations käyttöön valitsemalla **Esiversio-ominaisuus käytössä**.</span><span class="sxs-lookup"><span data-stu-id="7cbbd-109">In the **Preview feature** list, select **Project Operations Feature**, and then select **Preview feature enabled** to enable Project Operations.</span></span>

> [!NOTE]
> <span data-ttu-id="7cbbd-110">Tämä vaihe suoritetaan vain kerran LCS-projektia kohden.</span><span class="sxs-lookup"><span data-stu-id="7cbbd-110">This step is performed only one time per LCS project.</span></span>

## <a name="provision-a-project-operations-environment"></a><span data-ttu-id="7cbbd-111">Project Operations -ympäristön tarjoaminen</span><span class="sxs-lookup"><span data-stu-id="7cbbd-111">Provision a Project Operations environment</span></span>

1. <span data-ttu-id="7cbbd-112">Avaa uusi Dynamics 365 Finance [-esittely-ympäristön](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) tai [eristys-/tuotantoympäristön](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deployenvironment-newinfrastructure) käyttöönotto.</span><span class="sxs-lookup"><span data-stu-id="7cbbd-112">Open a new Dynamics 365 Finance [demo environment](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) or [sandbox/ production environment](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deployenvironment-newinfrastructure) deployment.</span></span> 
2. <span data-ttu-id="7cbbd-113">Suorita ohjatun **Ympäristön valmistelu** -toiminnon vaiheet.</span><span class="sxs-lookup"><span data-stu-id="7cbbd-113">Walk through the **Environment provisioning** wizard.</span></span> 

> [!IMPORTANT]
> <span data-ttu-id="7cbbd-114">Varmista, että valittu sovellusversio on 10.0.13 tai uudempi.</span><span class="sxs-lookup"><span data-stu-id="7cbbd-114">Make sure selected application version is 10.0.13 or higher.</span></span>

3. <span data-ttu-id="7cbbd-115">Jos haluat valmistella Project Operationsi, valitse **Lisäasetukset**-kohdassa **Common Data Service**.</span><span class="sxs-lookup"><span data-stu-id="7cbbd-115">To provision Project Operations, under **Advance settings**, select **Common Data Service**.</span></span> 
4. <span data-ttu-id="7cbbd-116">Ota **Common Data Service -asetukset** käyttöön valitsemalla **Kyllä** ja kirjoitramalla tiedot pakollisiin kenttiin:</span><span class="sxs-lookup"><span data-stu-id="7cbbd-116">Enable the **Common Data Service Setting** by selecting **Yes** and then enter information in the required fields:</span></span>

  - <span data-ttu-id="7cbbd-117">Nimi</span><span class="sxs-lookup"><span data-stu-id="7cbbd-117">Name</span></span>
  - <span data-ttu-id="7cbbd-118">Alue</span><span class="sxs-lookup"><span data-stu-id="7cbbd-118">Region</span></span>
  - <span data-ttu-id="7cbbd-119">Language</span><span class="sxs-lookup"><span data-stu-id="7cbbd-119">Language</span></span>
  - <span data-ttu-id="7cbbd-120">Valuutta</span><span class="sxs-lookup"><span data-stu-id="7cbbd-120">Currency</span></span>
 
5. <span data-ttu-id="7cbbd-121">Valitse **Common Data Service -malli** -kentässä **Project Operations**</span><span class="sxs-lookup"><span data-stu-id="7cbbd-121">In the **Common Data Service Template** field, select **Project Operations**</span></span> 

6. <span data-ttu-id="7cbbd-122">Valitse käyttöönoton ympäristötyyppi.</span><span class="sxs-lookup"><span data-stu-id="7cbbd-122">Select the environment type for your deployment.</span></span> <span data-ttu-id="7cbbd-123">Tilauspohjaisen kokeiluversion avulla voit käyttää CDS-ympäristöä 30 päivän ajan.</span><span class="sxs-lookup"><span data-stu-id="7cbbd-123">A subscription-based trial will let you deploy a CDS environment for 30 days.</span></span> 

![Käyttööntoton asetukset](./media/1DeploymentSettings.png)

> [!IMPORTANT]
> <span data-ttu-id="7cbbd-125">Valitse **Hyväksy**, kun hyväksyt palveluehdot, ja palaa sitten käyttöönottoasetuksiin valitsemalla **Valmis**.</span><span class="sxs-lookup"><span data-stu-id="7cbbd-125">Select **Agree** to acknowledge the terms of service and then select **Done** to return to the deployment settings.</span></span>

![Käyttöönoton suostumus](./media/2DeploymentConsent.png)

7. <span data-ttu-id="7cbbd-127">Valinnainen - Käytä esittelytietoja ympäristössä.</span><span class="sxs-lookup"><span data-stu-id="7cbbd-127">Optional - Apply demo data to the environment.</span></span> <span data-ttu-id="7cbbd-128">Valitse **Lisäasetukset**, valitse **Mukauta SQL-tietokannan määrityksiä** ja aseta **Määritä sovellustietokannan tietojoukko** -asetukseksi **Esittely**.</span><span class="sxs-lookup"><span data-stu-id="7cbbd-128">Go to **Advanced settings**, select **Customize SQL Database Configuration**, and set **Specify a dataset for Application database** to **Demo**.</span></span>

8. <span data-ttu-id="7cbbd-129">Täytä loput pakolliset kentät ohjatussa toiminnossa ja vahvista asennus.</span><span class="sxs-lookup"><span data-stu-id="7cbbd-129">Complete the remaining required fields in the wizard and confirm the deployment.</span></span> <span data-ttu-id="7cbbd-130">Ympäristön valmisteluaika vaihtelee ympäristötyypin mukaan.</span><span class="sxs-lookup"><span data-stu-id="7cbbd-130">The time to provision the environment varies based on the environment type.</span></span> <span data-ttu-id="7cbbd-131">Valmistelu voi kestää jopa kuusi tuntia.</span><span class="sxs-lookup"><span data-stu-id="7cbbd-131">Provisioning might take up to six hours.</span></span>

  <span data-ttu-id="7cbbd-132">Kun käyttöönotto on valmis, ympäristö näkyy tilassa **Otettu käyttöön**.</span><span class="sxs-lookup"><span data-stu-id="7cbbd-132">After the deployment completes successfully, the environment will show as **Deployed**.</span></span>

9. <span data-ttu-id="7cbbd-133">Voit varmistaa, että ympäristön käyttöönotto onnistui, valitsemalla **Kirjaudu sisään** ja kirjautumalla ympäristöön.</span><span class="sxs-lookup"><span data-stu-id="7cbbd-133">To confirm that the environment has deployed successfully, select **Login** and log on to the environment to confirm.</span></span>

![-ympäristön tiedot](./media/3EnvironmentDetails.png)

## <a name="apply-updates-to-the-finance-environment"></a><span data-ttu-id="7cbbd-135">Ota päivitykset käyttöön Finance-ympäristössä</span><span class="sxs-lookup"><span data-stu-id="7cbbd-135">Apply updates to the Finance environment</span></span>

<span data-ttu-id="7cbbd-136">Project Operations edellyttää Finance-ympäristöä, jossa on sovellusversio **10.0.13 (10.0.569.20009)** tai uudempi.</span><span class="sxs-lookup"><span data-stu-id="7cbbd-136">Project Operations requires a Finance environment with application version **10.0.13 (10.0.569.20009)** or higher.</span></span>

<span data-ttu-id="7cbbd-137">Sinun täytyy ehkä ottaa käyttöön laatupäivityksiä Finance-ympäristössäsi, jotta saat tämän version.</span><span class="sxs-lookup"><span data-stu-id="7cbbd-137">You might need to apply quality updates to your Finance environment to receive this version.</span></span>

1. <span data-ttu-id="7cbbd-138">Valitse LCS:n **Ympäristön tiedot** -sivun **Saatavilla olevat päivitykset** -kohdassa **Näytä päivitys**.</span><span class="sxs-lookup"><span data-stu-id="7cbbd-138">In LCS, on the **Environment details** page, in the **Available Updates** section, select **View Update**.</span></span>

![Näytä päivitykset](./media/5ViewUpdates.png)

2. <span data-ttu-id="7cbbd-140">Valitse **Binaaripäivitykset**-sivulla **Tallenna paketti.**</span><span class="sxs-lookup"><span data-stu-id="7cbbd-140">On the **Binary updates** page, select **Save package.**</span></span>

![Tallenna paketti](./media/6SavePackage.png)

3. <span data-ttu-id="7cbbd-142">Valitse **Valitse kaikki** ja sitten **Tallenna paketti**.</span><span class="sxs-lookup"><span data-stu-id="7cbbd-142">Click **Select all** and then select **Save package**.</span></span>

![Päivitysten tarkistaminen ja tallentaminen](./media/7ReviewAndSaveUpdates.png)

4. <span data-ttu-id="7cbbd-144">Kirjoita paketin nimi ja kuvaus ja valitse sitten **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="7cbbd-144">Enter a name and a description of the package, and then select **Save**.</span></span> <span data-ttu-id="7cbbd-145">Internet-yhteydestä riippuen tämä prosessi voi kestää jonkin aikaa.</span><span class="sxs-lookup"><span data-stu-id="7cbbd-145">Depending on the internet connection, this process might take some time.</span></span>

![Lataa paketti Resurssit-kirjastoon](./media/8UploadPackageToAssetsLibrary.png)

5. <span data-ttu-id="7cbbd-147">Kun paketti on tallennettu, valitse **Valmis** ja tallenna paketti LCS-projektin Resurssit-kirjastoon.</span><span class="sxs-lookup"><span data-stu-id="7cbbd-147">After the package is saved, select **Done** and save this package to the Assets library in your LCS project.</span></span>

<span data-ttu-id="7cbbd-148">Paketin tallentaminen ja tarkistaminen voi kestää noin 15 minuuttia.</span><span class="sxs-lookup"><span data-stu-id="7cbbd-148">Saving and validating the package might take ~15 minutes.</span></span>

6. <span data-ttu-id="7cbbd-149">Voit ottaa päivityksen käyttöön siirtymällä LCS:n **Ympäristön tiedot** -sivulle ja valitsemalla **Ylläpidä** > **Ota päivitykset käyttöön**.</span><span class="sxs-lookup"><span data-stu-id="7cbbd-149">To apply the update, navigate to the **Environment details** page in LCS and select **Maintain** > **Apply updates**.</span></span>

![Ympäristöjen ylläpito](./media/9MaintainEnvironment.png)

7. <span data-ttu-id="7cbbd-151">Valitse päivitysluettelosta luomasi paketti ja valitse sitten **Käytä**.</span><span class="sxs-lookup"><span data-stu-id="7cbbd-151">In the updates list select the package you created, and select **Apply**.</span></span>

![Päivitysten ottaminen käyttöön](./media/10ApplyUpdates.png)

<span data-ttu-id="7cbbd-153">Ympäristön huolto kestää jonkin aikaa.</span><span class="sxs-lookup"><span data-stu-id="7cbbd-153">Environment servicing will take some time.</span></span> <span data-ttu-id="7cbbd-154">Kun ympäristö on valmis, se palaa käyttöön otettuun tilaan.</span><span class="sxs-lookup"><span data-stu-id="7cbbd-154">After it is complete, the environment will return to a deployed state.</span></span>

![Ympäristö otettu käyttöön](./media/11EnvironmentDeployed.png)

## <a name="establish-a-dual-write-connection"></a><span data-ttu-id="7cbbd-156">Kaksinkertaisen kirjoituksen yhteyden muodostaminen</span><span class="sxs-lookup"><span data-stu-id="7cbbd-156">Establish a Dual Write connection</span></span> 

1. <span data-ttu-id="7cbbd-157">Siirry LCS-projektissa **Ympäristön tiedot** -sivulle.</span><span class="sxs-lookup"><span data-stu-id="7cbbd-157">In your LCS project, go to the **Environment details** page.</span></span>
2. <span data-ttu-id="7cbbd-158">**Common Data Service -ympäristön tiedot** -kohdassa **Linkitä CDS for Appsiin**.</span><span class="sxs-lookup"><span data-stu-id="7cbbd-158">Under **Common Data Service Environment Information**, select **Link to CDS for Apps**.</span></span>
3. <span data-ttu-id="7cbbd-159">Kun linkki on valmis, valitse uudelleen **Linkitä CDS for Appsiin**.</span><span class="sxs-lookup"><span data-stu-id="7cbbd-159">After the link is complete, select **Link to CDS for Apps** again.</span></span> <span data-ttu-id="7cbbd-160">Sinut ohjataan Financen kaksoiskirjoitukseen.</span><span class="sxs-lookup"><span data-stu-id="7cbbd-160">You will be redirected to Dual Write in Finance.</span></span>

![Linkitä CDS:ään](./media/12LinktoCDS.png)

4. <span data-ttu-id="7cbbd-162">Valitse **Käytä ratkaisua**, kun haluat käyttää entiteettejä, jotkan yhdistetään integrointiin.</span><span class="sxs-lookup"><span data-stu-id="7cbbd-162">Select **Apply Solution** to access the entities that will be mapped in the integration.</span></span>

![Ota ratkaisut käyttöön](./media/13ApplySolutions.png)

5. <span data-ttu-id="7cbbd-164">Valitse molemmat ratkaisut, **Dynamics 365 Finance and Operations Kaksoiskirjoitusentiteetin yhdistämismääritys** ja **Dynamics 365 Project Operations Kaksoiskirjoitusentiteettien yhdistämismääritykset** ja valitse sitten **Käytä**.</span><span class="sxs-lookup"><span data-stu-id="7cbbd-164">Select both solutions, **Dynamics 365 Finance and Operations Dual Write Entity Map** and **Dynamics 365 Project Operations Dual Write Entity Maps**, and then select **Apply**.</span></span>

![Ratkaisujen vahvistaminen](./media/14ConfirmSolutions.png)

<span data-ttu-id="7cbbd-166">Kun ratkaisut on otettu käyttöön, kaksoiskirjoituskohteet otetaan käyttöön ympäristössä.</span><span class="sxs-lookup"><span data-stu-id="7cbbd-166">After the solutions are applied, the Dual Write entities are applied to the environment.</span></span>

![Ratkaisujen käyttöönotto](./media/15ApplyingSolutions.png)

<span data-ttu-id="7cbbd-168">Kun entiteetit otetaan käyttöön, kaikki käytettävissä olevat yhdistämismääritykset näkyvät ympäristössä.</span><span class="sxs-lookup"><span data-stu-id="7cbbd-168">After the entities are applied, all available mappings are listed in the environment.</span></span>

![Kaksoiskirjoituksen yhdistämismääritykset](./media/15DWMappings.png)

## <a name="refresh-the-data-entities-after-the-update"></a><span data-ttu-id="7cbbd-170">Päivitä tietoentiteetit päivityksen jälkeen</span><span class="sxs-lookup"><span data-stu-id="7cbbd-170">Refresh the data entities after the update</span></span>

1. <span data-ttu-id="7cbbd-171">Siirry Financessa **Tietojen hallinta** -työtilaan.</span><span class="sxs-lookup"><span data-stu-id="7cbbd-171">In Finance, go to the **Data management** workspace.</span></span>

![Tietojen hallinnan työtila](./media/16DataManagement.png)

2. <span data-ttu-id="7cbbd-173">Valitse **Kehyksen parametrit** -ruutu.</span><span class="sxs-lookup"><span data-stu-id="7cbbd-173">Select the **Framework parameters** tile.</span></span>

![Kehyksen parametrit](./media/17FrameworkParameters.png)

3. <span data-ttu-id="7cbbd-175">Valitse **Entiteetin asetukset** -sivulla **Päivitä entiteettiluettelo**.</span><span class="sxs-lookup"><span data-stu-id="7cbbd-175">On the **Entity settings** page, select **Refresh Entity list**.</span></span>

![Päivitä entiteettiluettelo](./media/18RefreshEntityList.png)

<span data-ttu-id="7cbbd-177">Päivitys kestää noin 20 minuuttia.</span><span class="sxs-lookup"><span data-stu-id="7cbbd-177">The refresh is going to take approximately 20 minutes.</span></span> <span data-ttu-id="7cbbd-178">Saat ilmoituksen, kun se on valmis.</span><span class="sxs-lookup"><span data-stu-id="7cbbd-178">You will receive an alert when it is complete.</span></span>

![Päivityksen vahvistus](./media/19RefreshConfirmation.png)

## <a name="update-security-settings-on-project-operations-on-dataverse"></a><span data-ttu-id="7cbbd-180">Suojausasetusten päivittäminen Dataversen Project Operationsissa</span><span class="sxs-lookup"><span data-stu-id="7cbbd-180">Update security settings on Project Operations on Dataverse</span></span>

1. <span data-ttu-id="7cbbd-181">Siirry Project Operationsiin Dataverse-ympäristössä.</span><span class="sxs-lookup"><span data-stu-id="7cbbd-181">Go to Project Operations on your Dataverse environment.</span></span> 
2. <span data-ttu-id="7cbbd-182">Valitse **Asetukset** > **Suojaus** > **Käyttöoikeusroolit**.</span><span class="sxs-lookup"><span data-stu-id="7cbbd-182">Go to **Settings** > **Security** > **Security roles**.</span></span> 
3. <span data-ttu-id="7cbbd-183">Valitse **Käyttöoikeusroolit**-sivun rooliluettelosta **kaksoiskirjoitussovelluksen käyttäjä** ja valitse **Mukautetut entiteetit** -välilehti.</span><span class="sxs-lookup"><span data-stu-id="7cbbd-183">On the **Security roles** page, in the list of roles, select **dual-write app user** and select the **Custom Entities** tab.</span></span>  
4. <span data-ttu-id="7cbbd-184">Varmista, että roolilla on **Luku**- ja **Lisää kohteeseen** -oikeudet seuraaville:</span><span class="sxs-lookup"><span data-stu-id="7cbbd-184">Verify that the role has **Read** and **Append To** permissions for the:</span></span>
      
      - <span data-ttu-id="7cbbd-185">**Valuuttakurssin tyyppi**</span><span class="sxs-lookup"><span data-stu-id="7cbbd-185">**Currency Exchange Rate Type**</span></span>
      - <span data-ttu-id="7cbbd-186">**Tilikartta**</span><span class="sxs-lookup"><span data-stu-id="7cbbd-186">**Chart Of Accounts**</span></span>
      - <span data-ttu-id="7cbbd-187">**Kirjanpitokalenteri**</span><span class="sxs-lookup"><span data-stu-id="7cbbd-187">**Fiscal Calendar**</span></span>
      - <span data-ttu-id="7cbbd-188">**Tapahtumarekisteri**</span><span class="sxs-lookup"><span data-stu-id="7cbbd-188">**Ledger**</span></span>

5. <span data-ttu-id="7cbbd-189">Kun käyttöoikeusrooli on päivitetty, siirry kohtaan **Asetukset** > **Suojaus** > **Ryhmät** ja valitse oletusryhmä **Oman yksikön omistaja** -ryhmänäkymässä.</span><span class="sxs-lookup"><span data-stu-id="7cbbd-189">After the security role is updated, go to **Settings** > **Security** > **Teams**, and select the default team in the **Local Business Owner** team view.</span></span>
6. <span data-ttu-id="7cbbd-190">Valitse **Hallitse rooleja** ja varmista, että **kaksoiskirjoitussovelluksen käyttäjä** -käyttöoikeus on käytössä tässä ryhmässä.</span><span class="sxs-lookup"><span data-stu-id="7cbbd-190">Select **Manage Roles** and verify that the **dual-write app user** security privilege is applied to this team.</span></span>

## <a name="run-project-operations-dual-write-maps"></a><span data-ttu-id="7cbbd-191">Suorita Project Operationsin kaksoiskirjoituksen yhdistämismääritykset</span><span class="sxs-lookup"><span data-stu-id="7cbbd-191">Run Project Operations Dual Write maps</span></span>

1. <span data-ttu-id="7cbbd-192">Siirry LCS-projektissa **Ympäristön tiedot** -sivulle.</span><span class="sxs-lookup"><span data-stu-id="7cbbd-192">In your LCS project, go to the **Environment details** page.</span></span>
2. <span data-ttu-id="7cbbd-193">Valitse **Common Data Service -ympäristön tiedot** -kohdassa **Linkitä CDS for Appsiin.**</span><span class="sxs-lookup"><span data-stu-id="7cbbd-193">Under **Common Data Service Environment Information**, select **Link to CDS for Apps.**</span></span> <span data-ttu-id="7cbbd-194">Kun olet valinnut linkin, sinut ohjataan yhdistämismääritysten entiteettiluetteloon.</span><span class="sxs-lookup"><span data-stu-id="7cbbd-194">After you select the link, you will be redirected to the list of entities in the mappings.</span></span>
3. <span data-ttu-id="7cbbd-195">Käynnistä yhdistäm,ismääritykset seuraavassa taulukossa kuvatulla tavalla.</span><span class="sxs-lookup"><span data-stu-id="7cbbd-195">Start the maps as described in the following table.</span></span> <span data-ttu-id="7cbbd-196">Varmista, että seuraat järjestystä luettelossa.</span><span class="sxs-lookup"><span data-stu-id="7cbbd-196">Make sure to follow the sequence as listed.</span></span>

| <span data-ttu-id="7cbbd-197">**Entiteetin yhdistämismääritys**</span><span class="sxs-lookup"><span data-stu-id="7cbbd-197">**Entity Map**</span></span> | <span data-ttu-id="7cbbd-198">**Päivitä entiteetti**</span><span class="sxs-lookup"><span data-stu-id="7cbbd-198">**Refresh entity**</span></span> | <span data-ttu-id="7cbbd-199">**Ensimmäinen synkronointi**</span><span class="sxs-lookup"><span data-stu-id="7cbbd-199">**Initial sync**</span></span> | <span data-ttu-id="7cbbd-200">**Ensimmäisen synkronoinnin pääkohde**</span><span class="sxs-lookup"><span data-stu-id="7cbbd-200">**Master for initial sync**</span></span> | <span data-ttu-id="7cbbd-201">**Suorita edellytykset**</span><span class="sxs-lookup"><span data-stu-id="7cbbd-201">**Run prerequisites**</span></span> | <span data-ttu-id="7cbbd-202">**Edellytysten ensimmäinen synkronointi**</span><span class="sxs-lookup"><span data-stu-id="7cbbd-202">**Prerequisites initial sync**</span></span> |
| --- | --- | --- | --- | --- | --- |
| <span data-ttu-id="7cbbd-203">**Kaikkien yritysten projektiresurssiroolit (bookableresourcecategories)**</span><span class="sxs-lookup"><span data-stu-id="7cbbd-203">**Project Resource Roles for All Companies (bookableresourcecategories)**</span></span> | <span data-ttu-id="7cbbd-204">No</span><span class="sxs-lookup"><span data-stu-id="7cbbd-204">No</span></span> | <span data-ttu-id="7cbbd-205">Kyllä</span><span class="sxs-lookup"><span data-stu-id="7cbbd-205">Yes</span></span> | <span data-ttu-id="7cbbd-206">Common Data Service</span><span class="sxs-lookup"><span data-stu-id="7cbbd-206">Common Data Service</span></span> | <span data-ttu-id="7cbbd-207">No</span><span class="sxs-lookup"><span data-stu-id="7cbbd-207">No</span></span> | <span data-ttu-id="7cbbd-208">–</span><span class="sxs-lookup"><span data-stu-id="7cbbd-208">N\A</span></span> |
| <span data-ttu-id="7cbbd-209">**Yritykset (cdm\_companies)**</span><span class="sxs-lookup"><span data-stu-id="7cbbd-209">**Legal entities (cdm\_companies)**</span></span> | <span data-ttu-id="7cbbd-210">No</span><span class="sxs-lookup"><span data-stu-id="7cbbd-210">No</span></span> | <span data-ttu-id="7cbbd-211">Kyllä</span><span class="sxs-lookup"><span data-stu-id="7cbbd-211">Yes</span></span> | <span data-ttu-id="7cbbd-212">Finance and Operations -sovellukset</span><span class="sxs-lookup"><span data-stu-id="7cbbd-212">Finance and Operations apps</span></span> | <span data-ttu-id="7cbbd-213">No</span><span class="sxs-lookup"><span data-stu-id="7cbbd-213">No</span></span> | <span data-ttu-id="7cbbd-214">–</span><span class="sxs-lookup"><span data-stu-id="7cbbd-214">N\A</span></span> |
| <span data-ttu-id="7cbbd-215">**Tapahtumarekisteri (msdyn_ledgers)**</span><span class="sxs-lookup"><span data-stu-id="7cbbd-215">**Ledger (msdyn_ledgers)**</span></span> | <span data-ttu-id="7cbbd-216">No</span><span class="sxs-lookup"><span data-stu-id="7cbbd-216">No</span></span> | <span data-ttu-id="7cbbd-217">Kyllä</span><span class="sxs-lookup"><span data-stu-id="7cbbd-217">Yes</span></span> | <span data-ttu-id="7cbbd-218">Finance and Operations -sovellukset</span><span class="sxs-lookup"><span data-stu-id="7cbbd-218">Finance and Operations apps</span></span> | <span data-ttu-id="7cbbd-219">Kyllä</span><span class="sxs-lookup"><span data-stu-id="7cbbd-219">Yes</span></span> | <span data-ttu-id="7cbbd-220">Kyllä, Finance and Operations -sovellukset</span><span class="sxs-lookup"><span data-stu-id="7cbbd-220">Yes, Finance and Operations apps</span></span> |
| <span data-ttu-id="7cbbd-221">**Project Operations -integroinnin todelliset arvot (msdyn\_actuals)**</span><span class="sxs-lookup"><span data-stu-id="7cbbd-221">**Project Operations integration actuals (msdyn\_actuals)**</span></span> | <span data-ttu-id="7cbbd-222">No</span><span class="sxs-lookup"><span data-stu-id="7cbbd-222">No</span></span> | <span data-ttu-id="7cbbd-223">No</span><span class="sxs-lookup"><span data-stu-id="7cbbd-223">No</span></span> | <span data-ttu-id="7cbbd-224">–</span><span class="sxs-lookup"><span data-stu-id="7cbbd-224">N\A</span></span> | <span data-ttu-id="7cbbd-225">Kyllä</span><span class="sxs-lookup"><span data-stu-id="7cbbd-225">Yes</span></span> | <span data-ttu-id="7cbbd-226">No</span><span class="sxs-lookup"><span data-stu-id="7cbbd-226">No</span></span> |
| <span data-ttu-id="7cbbd-227">**Projektin sopimusrivit (salesorderdetails)**</span><span class="sxs-lookup"><span data-stu-id="7cbbd-227">**Project contract lines (salesorderdetails)**</span></span> | <span data-ttu-id="7cbbd-228">No</span><span class="sxs-lookup"><span data-stu-id="7cbbd-228">No</span></span> | <span data-ttu-id="7cbbd-229">No</span><span class="sxs-lookup"><span data-stu-id="7cbbd-229">No</span></span> | <span data-ttu-id="7cbbd-230">–</span><span class="sxs-lookup"><span data-stu-id="7cbbd-230">N\A</span></span> | <span data-ttu-id="7cbbd-231">No</span><span class="sxs-lookup"><span data-stu-id="7cbbd-231">No</span></span> | <span data-ttu-id="7cbbd-232">No</span><span class="sxs-lookup"><span data-stu-id="7cbbd-232">No</span></span> |
| <span data-ttu-id="7cbbd-233">**Projektitapahtuman integrointikohdesuhteet (msdyn\_transactionconnections)**</span><span class="sxs-lookup"><span data-stu-id="7cbbd-233">**Integration entity for project transaction relationships (msdyn\_transactionconnections)**</span></span> | <span data-ttu-id="7cbbd-234">No</span><span class="sxs-lookup"><span data-stu-id="7cbbd-234">No</span></span> | <span data-ttu-id="7cbbd-235">No</span><span class="sxs-lookup"><span data-stu-id="7cbbd-235">No</span></span> | <span data-ttu-id="7cbbd-236">–</span><span class="sxs-lookup"><span data-stu-id="7cbbd-236">N\A</span></span> | <span data-ttu-id="7cbbd-237">No</span><span class="sxs-lookup"><span data-stu-id="7cbbd-237">No</span></span> | <span data-ttu-id="7cbbd-238">–</span><span class="sxs-lookup"><span data-stu-id="7cbbd-238">N\A</span></span> |
| <span data-ttu-id="7cbbd-239">**Project Operations -integroinnin sopimusrivin välitavoitteet (msdyn\_contractlinesscheduleofvalues)**</span><span class="sxs-lookup"><span data-stu-id="7cbbd-239">**Project Operations integration contract line milestones (msdyn\_contractlinesscheduleofvalues)**</span></span> | <span data-ttu-id="7cbbd-240">No</span><span class="sxs-lookup"><span data-stu-id="7cbbd-240">No</span></span> | <span data-ttu-id="7cbbd-241">No</span><span class="sxs-lookup"><span data-stu-id="7cbbd-241">No</span></span> | <span data-ttu-id="7cbbd-242">–</span><span class="sxs-lookup"><span data-stu-id="7cbbd-242">N\A</span></span> | <span data-ttu-id="7cbbd-243">No</span><span class="sxs-lookup"><span data-stu-id="7cbbd-243">No</span></span> | <span data-ttu-id="7cbbd-244">–</span><span class="sxs-lookup"><span data-stu-id="7cbbd-244">N\A</span></span> |
| <span data-ttu-id="7cbbd-245">**Project Operations -integrointikohde kuluarvioita varten (msdyn\_estimateslines)**</span><span class="sxs-lookup"><span data-stu-id="7cbbd-245">**Project Operations integration entity for expense estimates (msdyn\_estimateslines)**</span></span> | <span data-ttu-id="7cbbd-246">No</span><span class="sxs-lookup"><span data-stu-id="7cbbd-246">No</span></span> | <span data-ttu-id="7cbbd-247">No</span><span class="sxs-lookup"><span data-stu-id="7cbbd-247">No</span></span> | <span data-ttu-id="7cbbd-248">–</span><span class="sxs-lookup"><span data-stu-id="7cbbd-248">N\A</span></span> | <span data-ttu-id="7cbbd-249">No</span><span class="sxs-lookup"><span data-stu-id="7cbbd-249">No</span></span> | <span data-ttu-id="7cbbd-250">–</span><span class="sxs-lookup"><span data-stu-id="7cbbd-250">N\A</span></span> |
| <span data-ttu-id="7cbbd-251">**Project Operations -integroinnin projektikululuokkien vientientiteetti (msdyn\_expensecategories)**</span><span class="sxs-lookup"><span data-stu-id="7cbbd-251">**Project Operations integration project expense categories export entity (msdyn\_expensecategories)**</span></span> | <span data-ttu-id="7cbbd-252">No</span><span class="sxs-lookup"><span data-stu-id="7cbbd-252">No</span></span> | <span data-ttu-id="7cbbd-253">No</span><span class="sxs-lookup"><span data-stu-id="7cbbd-253">No</span></span> | <span data-ttu-id="7cbbd-254">–</span><span class="sxs-lookup"><span data-stu-id="7cbbd-254">N\A</span></span> | <span data-ttu-id="7cbbd-255">No</span><span class="sxs-lookup"><span data-stu-id="7cbbd-255">No</span></span> | <span data-ttu-id="7cbbd-256">–</span><span class="sxs-lookup"><span data-stu-id="7cbbd-256">N\A</span></span> |
| <span data-ttu-id="7cbbd-257">**Project Operations -integroinnin projektikulujen vientientiteetti (msdyn\_expenses)**</span><span class="sxs-lookup"><span data-stu-id="7cbbd-257">**Project Operations integration project expenses export entity (msdyn\_expenses)**</span></span> | <span data-ttu-id="7cbbd-258">Kyllä</span><span class="sxs-lookup"><span data-stu-id="7cbbd-258">Yes</span></span> | <span data-ttu-id="7cbbd-259">No</span><span class="sxs-lookup"><span data-stu-id="7cbbd-259">No</span></span> | <span data-ttu-id="7cbbd-260">–</span><span class="sxs-lookup"><span data-stu-id="7cbbd-260">N\A</span></span> | <span data-ttu-id="7cbbd-261">No</span><span class="sxs-lookup"><span data-stu-id="7cbbd-261">No</span></span> | <span data-ttu-id="7cbbd-262">–</span><span class="sxs-lookup"><span data-stu-id="7cbbd-262">N\A</span></span> |
| <span data-ttu-id="7cbbd-263">**Project Operations -integrointikohde tuntiarvioita varten (msdyn\_resourceassignments)**</span><span class="sxs-lookup"><span data-stu-id="7cbbd-263">**Project Operations integration entity for hour estimates (msdyn\_resourceassignments)**</span></span> | <span data-ttu-id="7cbbd-264">Kyllä</span><span class="sxs-lookup"><span data-stu-id="7cbbd-264">Yes</span></span> | <span data-ttu-id="7cbbd-265">No</span><span class="sxs-lookup"><span data-stu-id="7cbbd-265">No</span></span> | <span data-ttu-id="7cbbd-266">–</span><span class="sxs-lookup"><span data-stu-id="7cbbd-266">N\A</span></span> | <span data-ttu-id="7cbbd-267">No</span><span class="sxs-lookup"><span data-stu-id="7cbbd-267">No</span></span> | <span data-ttu-id="7cbbd-268">–</span><span class="sxs-lookup"><span data-stu-id="7cbbd-268">N\A</span></span> |


4. <span data-ttu-id="7cbbd-269">Jos haluat päivittää entiteetin, valitse yhdistämismäärityksen nimi ja valitse sitten **Päivitä entiteetit**.</span><span class="sxs-lookup"><span data-stu-id="7cbbd-269">To refresh the entity, select the map name, and then select **Refresh entities**.</span></span> 


![Päivitä yhdistämismääritys](./media/20RefreshMapping.png)

5. <span data-ttu-id="7cbbd-271">Suorita yhdistämismääritys, kun päivitys on valmis.</span><span class="sxs-lookup"><span data-stu-id="7cbbd-271">After the refresh is complete, run the map.</span></span> <span data-ttu-id="7cbbd-272">Ennen kuin otat seuraavan yhdistämismäärityksen käyttöön, tarkista, että taulukon yhdistämismääritys on tilassa **Käynnissä**.</span><span class="sxs-lookup"><span data-stu-id="7cbbd-272">Before you enable the next map, verify that the map in the table is in a state of **Running**.</span></span> <span data-ttu-id="7cbbd-273">Sellaisten yhdistämismääritysten suorittaminen, joissa on paljon edellytyksiä, voi kestää jonkin aikaa.</span><span class="sxs-lookup"><span data-stu-id="7cbbd-273">Running maps with a larger number of prerequisites might take some time.</span></span>

<span data-ttu-id="7cbbd-274">Jos haluat suorittaa yhdistämismääritys ja edellytykset, ota käyttöön **Näytä liittyvät entiteetin yhdistämismääritykset** -valintapainike.</span><span class="sxs-lookup"><span data-stu-id="7cbbd-274">To run a map with prerequisites, enable the **Show related entity maps** toggle.</span></span> <span data-ttu-id="7cbbd-275">Jos taulukko osoittaa **Edellytyksen ensimmäinen synkronointi** -kohdaas arvo **Ei**, tarkista, että **Ensimmäinen synkronointi** -merkintä on **Ei käytössä** kaikissa edellytysyhdistämismäärityksissä, ennen kuin suoritat sen.</span><span class="sxs-lookup"><span data-stu-id="7cbbd-275">If the table indicates **Prerequisite initial sync** is **No**, verify that the **Initial sync** flag is **Off** in all the prerequisite maps before you run it.</span></span>

![Suorita yhdistämismääritys](./media/21RunMap.png)

6. <span data-ttu-id="7cbbd-277">Tarkista, että kaikki projektiin liittyvät yhdistämismääritykset ovat Käynnissä-tilassa.</span><span class="sxs-lookup"><span data-stu-id="7cbbd-277">Validate all project related maps are in the running state.</span></span>

![Kaikki yhdistämismääritykset käynnissä](./media/22AllMapsRunning.png)


## <a name="apply-configuration-data-in-cds-for-project-operations-optional"></a><span data-ttu-id="7cbbd-279">Määritystietojen ottaminen käyttöön Project Operationsin CDS:ssä (valinnainen)</span><span class="sxs-lookup"><span data-stu-id="7cbbd-279">Apply configuration data in CDS for Project Operations (optional)</span></span>

<span data-ttu-id="7cbbd-280">Jos olet käyttänyt esittelytietoja Finance-ympäristössä, lisätietoja esittelytietojen käyttämisestä CDS-ympäristössä on kohdassa [Määritystietojen määrittäminen ja käyttäminen Project Operationsin Common Data Servicessa](resource-apply-pro-setup-config-data.md).</span><span class="sxs-lookup"><span data-stu-id="7cbbd-280">If you have applied demo data to the Finance environment, see [Set up and apply configuration data in the Common Data Service for Project Operations](resource-apply-pro-setup-config-data.md) to apply demo data to CDS environment.</span></span>


<span data-ttu-id="7cbbd-281">Project Operations -ympäristö on nyt valmisteltu ja määritetty.</span><span class="sxs-lookup"><span data-stu-id="7cbbd-281">Your Project Operations environment is now provisioned and configured.</span></span> 
