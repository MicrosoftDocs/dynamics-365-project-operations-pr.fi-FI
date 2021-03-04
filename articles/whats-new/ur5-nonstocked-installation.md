---
title: Project Operationsin päivittäminen Finance-ympäristössä
description: Tässä aiheessa on tietoja Project Operationsin päivittämisestä Dynamics 365 Finance -ympäristössä.
author: ruhercul
manager: tfehr
ms.date: 12/11/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 249b8dba17165da04596ec46a625131b9b4daeb5
ms.sourcegitcommit: f4fc6e3a81e8551da050e92f8fde85f8d7b52fbd
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/29/2020
ms.locfileid: "4816621"
---
# <a name="update-project-operations-in-your-finance-environment"></a><span data-ttu-id="ae65d-103">Project Operationsin päivittäminen Finance-ympäristössä</span><span class="sxs-lookup"><span data-stu-id="ae65d-103">Update Project Operations in your Finance environment</span></span>

<span data-ttu-id="ae65d-104">_**Käytetään:** Project Operationsin resursseihin ja ei-varastoitaviin perustuvissa skenaarioissa_</span><span class="sxs-lookup"><span data-stu-id="ae65d-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>


<span data-ttu-id="ae65d-105">Tässä aiheessa on tietoja Dynamics 365 Project Operationsin päivittämisestä Dynamics 365 Finance -ympäristössä.</span><span class="sxs-lookup"><span data-stu-id="ae65d-105">This topic provides information about how to update Dynamics 365 Project Operations in your Dynamics 365 Finance environment.</span></span> <span data-ttu-id="ae65d-106">Project Operationsin päivittäminen päivitysversioon 5 (UR5) edellyttää kolmea toimenpidettä:</span><span class="sxs-lookup"><span data-stu-id="ae65d-106">There are three procedures that are required to update Project Operations to Update 5 (UR5):</span></span>

- [<span data-ttu-id="ae65d-107">Paketin tuominen esiversioprojektiin</span><span class="sxs-lookup"><span data-stu-id="ae65d-107">Import the package into your preview project</span></span>](#import)
- [<span data-ttu-id="ae65d-108">Asenna päivitys</span><span class="sxs-lookup"><span data-stu-id="ae65d-108">Apply the update</span></span>](#apply)
- [<span data-ttu-id="ae65d-109">Dataverse-ympäristön päivittäminen</span><span class="sxs-lookup"><span data-stu-id="ae65d-109">Update your Dataverse environment</span></span>](#update)

## <a name="import-the-package-into-your-lcs-project"></a><a name="import"></a><span data-ttu-id="ae65d-110">Paketin tuominen LCS-projektiin</span><span class="sxs-lookup"><span data-stu-id="ae65d-110">Import the package into your LCS project</span></span>

1. <span data-ttu-id="ae65d-111">Kirjaudu [Lifecycle Servicesiin (LCS)](https://lcs.dynamics.com/) projektin omistajana tai ympäristön ylläpitäjänä.</span><span class="sxs-lookup"><span data-stu-id="ae65d-111">Sign in to [Lifecycle Services (LCS)](https://lcs.dynamics.com/) as a Project Owner or Environment manager.</span></span>
2. <span data-ttu-id="ae65d-112">Valitse LCS-projektisi projektiluettelosta.</span><span class="sxs-lookup"><span data-stu-id="ae65d-112">From the list of projects, select your LCS project.</span></span>
3. <span data-ttu-id="ae65d-113">Avaa **Projekti**-sivun **Ympäristöt**-ryhmästä se ympäristö, jonka haluat päivittää.</span><span class="sxs-lookup"><span data-stu-id="ae65d-113">On the **Project** page, in the **Environments** group, open the environment that you want to update.</span></span>
4. <span data-ttu-id="ae65d-114">Tarkista, että ympäristö on käytössä.</span><span class="sxs-lookup"><span data-stu-id="ae65d-114">Verify that the environment is running.</span></span> <span data-ttu-id="ae65d-115">Jos sitä ei ole käynnistetty, käynnistä ympäristö.</span><span class="sxs-lookup"><span data-stu-id="ae65d-115">If it isn't started, start the environment.</span></span>
5. <span data-ttu-id="ae65d-116">Valitse **Saatavilla olevat päivitukset** -kohdan alla olevasta **Uusi versio** -kohdasta **Näytä päivitys** versiolle 10.0.15.</span><span class="sxs-lookup"><span data-stu-id="ae65d-116">In the **New release** section under **Available updates**, select **View update** for 10.0.15.</span></span>

![Näytä päivitys -painike](media/view-update.png)

6. <span data-ttu-id="ae65d-118">Valitse **Binaaripäivitykset**-sivulla **Tallenna paketti**.</span><span class="sxs-lookup"><span data-stu-id="ae65d-118">On the **Binary updates** page, select **Save package**.</span></span>
7. <span data-ttu-id="ae65d-119">Valitse **Tarkista ja tallenna päivitykset**-sivulla **Tallenna paketti**.</span><span class="sxs-lookup"><span data-stu-id="ae65d-119">On the **Review and save updates** page, select **Save package**.</span></span>
8. <span data-ttu-id="ae65d-120">Kirjoita paketin nimi **Tallenna paketti resurssikirjastoon** -ruutuun ja valitse sitten **Tallenna paketti**.</span><span class="sxs-lookup"><span data-stu-id="ae65d-120">On the **Save package to asset library** pane that opens, enter the package name and then select **Save package**.</span></span>
9. <span data-ttu-id="ae65d-121">Kun LCS on tallentanut paketin, **Valmis**-painike on käytössä.</span><span class="sxs-lookup"><span data-stu-id="ae65d-121">When LCS has finished saving the package, the **Done** button is enabled.</span></span> <span data-ttu-id="ae65d-122">Valitse **Valmis**.</span><span class="sxs-lookup"><span data-stu-id="ae65d-122">Select **Done**.</span></span> <span data-ttu-id="ae65d-123">LCS tarkistaa paketin.</span><span class="sxs-lookup"><span data-stu-id="ae65d-123">LCS will verify the package.</span></span> <span data-ttu-id="ae65d-124">Tarkistaminen voi kestää muutaman minuutin tai jopa tunnin.</span><span class="sxs-lookup"><span data-stu-id="ae65d-124">Verification can take a few minutes or up to one hour.</span></span>


## <a name="apply-the-package-update"></a><a name="apply"></a><span data-ttu-id="ae65d-125">Asenna päivityspaketti</span><span class="sxs-lookup"><span data-stu-id="ae65d-125">Apply the package update</span></span>

1. <span data-ttu-id="ae65d-126">Valitse LCS:ssä **Ympäristön tiedot** -sivulla **Ylläpidä** > **Ota päivitykset käyttöön**.</span><span class="sxs-lookup"><span data-stu-id="ae65d-126">In LCS, on the **Environment details** page, select **Maintain** > **Apply Updates**.</span></span>
2. <span data-ttu-id="ae65d-127">Valitse luettelosta aiemmin tallennettu paketti ja valitse sitten **Käytä**.</span><span class="sxs-lookup"><span data-stu-id="ae65d-127">From the list, select the package that you saved earlier, and then select **Apply**.</span></span>
3. <span data-ttu-id="ae65d-128">Vahvista paketin käyttöönotto valitsemalla **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="ae65d-128">Select **Yes** to confirm that you want to deploy the package.</span></span>

![Vahvista paketin käyttöönotto -valintaikkuna](media/confirm-package-deployment.png)

4. <span data-ttu-id="ae65d-130">Vahvista sovelluksen päivitys valitsemalla **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="ae65d-130">Select **Yes** to confirm that you want to update the application.</span></span>

![Vahvista sovelluksen päivitys -valintaikkuna](media/confirm-application-update.png)

<span data-ttu-id="ae65d-132">Käyttöönotto ja sovelluspäivitys käynnistyy.</span><span class="sxs-lookup"><span data-stu-id="ae65d-132">The deployment and application update will start.</span></span> 

<span data-ttu-id="ae65d-133">**Ympäristön tiedot** -sivun oikeassa yläkulmassa ympäristön tilaksi päivittyy **Ylläpito**.</span><span class="sxs-lookup"><span data-stu-id="ae65d-133">On the **Environment details** page, in the top-right corner, the environment status will update to **Servicing**.</span></span> <span data-ttu-id="ae65d-134">Päivitys on valmis noin kahden tunnin kuluttua.</span><span class="sxs-lookup"><span data-stu-id="ae65d-134">In approximately two hours, the update will be complete.</span></span> <span data-ttu-id="ae65d-135">Sovelluksen julkaisutiedoiksi päivittyy **Microsoft Dynamics 365 for Finance and Operations 10.0.15)** ja ympäristön tilaksi päivittyy **Otettu käyttöön**.</span><span class="sxs-lookup"><span data-stu-id="ae65d-135">The application release information will update to **Microsoft Dynamics 365 for Finance and Operations 10.0.15)** and the environment status will update to **Deployed**.</span></span>


## <a name="update-your-dataverse-environment"></a><a name="update"></a><span data-ttu-id="ae65d-136">Dataverse-ympäristön päivittäminen</span><span class="sxs-lookup"><span data-stu-id="ae65d-136">Update your Dataverse environment</span></span>

1. <span data-ttu-id="ae65d-137">Kirjaudu [Power Platform -hallintakeskukseen](https://admin.powerplatform.com/).</span><span class="sxs-lookup"><span data-stu-id="ae65d-137">Sign in to the [Power Platform admin center](https://admin.powerplatform.com/).</span></span>
2. <span data-ttu-id="ae65d-138">Etsi ja avaa luettelosta ympäristö, jota käytit Project Operationsin asentamiseen.</span><span class="sxs-lookup"><span data-stu-id="ae65d-138">In the list, find and open the environment that you used to install Project Operations.</span></span>
3. <span data-ttu-id="ae65d-139">Valitse **Ympäristöt**-sivulla **Resurssi** > **Dynamics 365 -sovellukset**.</span><span class="sxs-lookup"><span data-stu-id="ae65d-139">On the **Environments** page, select **Resource** > **Dynamics 365 apps**.</span></span>
4. <span data-ttu-id="ae65d-140">Etsi luettelosta **Microsoft Dynamics 365 Project Operations** ja valitse **Tila**-sarakkeesta **Päivitys saatavilla**.</span><span class="sxs-lookup"><span data-stu-id="ae65d-140">In the list, locate **Microsoft Dynamics 365 Project Operations**, and in the **Status** column, select **Update Available**.</span></span>
5. <span data-ttu-id="ae65d-141">Valitse **Hyväksyn palveluehdot** -valintaruutu ja valitse sitten **Päivitä**.</span><span class="sxs-lookup"><span data-stu-id="ae65d-141">Select the **I agree to the terms of service** check box, and then select **Update**.</span></span> <span data-ttu-id="ae65d-142">Ratkaisun uusin versio asennetaan.</span><span class="sxs-lookup"><span data-stu-id="ae65d-142">The latest version of the solution will be installed.</span></span>

<span data-ttu-id="ae65d-143">Kun asennus on valmis, asennettuna on versio 4.5.0.134.</span><span class="sxs-lookup"><span data-stu-id="ae65d-143">After the installation is complete, you'll have version 4.5.0.134 installed.</span></span>

## <a name="configure-new-features"></a><span data-ttu-id="ae65d-144">Uusien ominaisuuksien määrittäminen</span><span class="sxs-lookup"><span data-stu-id="ae65d-144">Configure new features</span></span>

### <a name="enable-dual-write-mapping"></a><span data-ttu-id="ae65d-145">Ota käyttöön kaksoiskirjoituksen yhdistäminen</span><span class="sxs-lookup"><span data-stu-id="ae65d-145">Enable dual-write mapping</span></span>

<span data-ttu-id="ae65d-146">Kun olet päivittänyt Finance- ja Dataverse-ympäristöt, voit ottaa käyttöön tarvittavat kaksoiskirjoituksen yhdistämiset.</span><span class="sxs-lookup"><span data-stu-id="ae65d-146">After you complete the update on the Finance and Dataverse environments, you can enable the required dual-write mappings.</span></span> <span data-ttu-id="ae65d-147">Tee seuraavat toimet kaksoiskirjoituksen yhdistämisen käyttöönottamiseksi.</span><span class="sxs-lookup"><span data-stu-id="ae65d-147">Complete the following procedures to enable dual-write mappings.</span></span>

- [<span data-ttu-id="ae65d-148">Customer Engagement -ympäristön suojausasetusten päivittäminen</span><span class="sxs-lookup"><span data-stu-id="ae65d-148">Update security settings on Customer Engagement environment</span></span>](#security)
- [<span data-ttu-id="ae65d-149">Päivitä tietoentiteetit</span><span class="sxs-lookup"><span data-stu-id="ae65d-149">Refresh data entities</span></span>](#refresh)
- [<span data-ttu-id="ae65d-150">Kaksoiskirjoituksen yhdistämismääritysten päivittäminen ja suorittaminen</span><span class="sxs-lookup"><span data-stu-id="ae65d-150">Update and run the dual-write mappings</span></span>](#run)

### <a name="update-security-settings-on-the-dataverse-environment"></a><a name="security"></a><span data-ttu-id="ae65d-151">Dataverse-ympäristön suojausasetusten päivittäminen</span><span class="sxs-lookup"><span data-stu-id="ae65d-151">Update security settings on the Dataverse environment</span></span>

<span data-ttu-id="ae65d-152">UR5-päivityksessä tarvitaan seuraavat entiteettien suojausoikeuksien päivitykset.</span><span class="sxs-lookup"><span data-stu-id="ae65d-152">The following updates to the security privileges for entities are required as part of the update to UR5.</span></span>

1. <span data-ttu-id="ae65d-153">Valitse Dataverse-ympäristössä **Asetukset** ja valitse sitten **Järjestelmä**-ryhmästä **Suojaus**.</span><span class="sxs-lookup"><span data-stu-id="ae65d-153">In your Dataverse environment, go to **Settings**, and in the **System** group, select **Security**.</span></span>

![Dataverse -ympäristön asetukset](media/Picture21.png)

2. <span data-ttu-id="ae65d-155">**Käyttöoikeusroolien** valitseminen</span><span class="sxs-lookup"><span data-stu-id="ae65d-155">Select **Security Roles**.</span></span>
3. <span data-ttu-id="ae65d-156">Valitse rooliluettelosta **kaksoiskirjoitussovelluksen käyttäjä** ja valitse **Mukautetut entiteetit** -välilehti.</span><span class="sxs-lookup"><span data-stu-id="ae65d-156">From the list of roles, select **dual-write app user** and select the **Custom Entities** tab.</span></span> 
4. <span data-ttu-id="ae65d-157">Varmista, että roolilla on **Luku**- ja **Lisää kohteeseen** -oikeudet seuraaville:</span><span class="sxs-lookup"><span data-stu-id="ae65d-157">Verify that the role has **Read** and **Append To** permissions for:</span></span>

      - <span data-ttu-id="ae65d-158">**Valuuttakurssin tyyppi**</span><span class="sxs-lookup"><span data-stu-id="ae65d-158">**Currency Exchange Rate Type**</span></span>
      - <span data-ttu-id="ae65d-159">**Tilikartta**</span><span class="sxs-lookup"><span data-stu-id="ae65d-159">**Chart Of Accounts**</span></span> 
      - <span data-ttu-id="ae65d-160">**Kirjanpitokalenteri**</span><span class="sxs-lookup"><span data-stu-id="ae65d-160">**Fiscal Calendar**</span></span> 
      - <span data-ttu-id="ae65d-161">**Tapahtumarekisteri**</span><span class="sxs-lookup"><span data-stu-id="ae65d-161">**Ledger**</span></span>

5. <span data-ttu-id="ae65d-162">Kun käyttöoikeusrooli on päivitetty, valitse **Asetukset** > **Suojaus** > **Ryhmät**.</span><span class="sxs-lookup"><span data-stu-id="ae65d-162">After the security role is updated, go to **Settings** > **Security** > **Teams**.</span></span> <span data-ttu-id="ae65d-163">Tarkista, että **kaksoiskirjoitussovelluksen käyttäjä** -rooli on otettu käyttöön ryhmässä.</span><span class="sxs-lookup"><span data-stu-id="ae65d-163">Verify that the **dual-write app user** role has been applied to the team.</span></span> 

### <a name="refresh-data-entities-from-the-update"></a><a name="refresh"></a><span data-ttu-id="ae65d-164">Päivitä tietoentiteetit päivityspaketista</span><span class="sxs-lookup"><span data-stu-id="ae65d-164">Refresh data entities from the update</span></span>

1. <span data-ttu-id="ae65d-165">Avaa Finance-ympäristössä **Tiedonhallinta**-työtila ja avaa sitten **Framework-parametrit**-sivu.</span><span class="sxs-lookup"><span data-stu-id="ae65d-165">In your Finance environment, open the **Data management** workspace, and then open the **Framework parameters** page.</span></span>
2. <span data-ttu-id="ae65d-166">Valitse **Entiteettiasetukset**-välilehdessä **Päivitä entiteettiluettelo**.</span><span class="sxs-lookup"><span data-stu-id="ae65d-166">On the **Entity settings** tab, select **Refresh entity list**.</span></span>
3. <span data-ttu-id="ae65d-167">Vahvista entiteetin päivitys valitsemalla **Sulje**.</span><span class="sxs-lookup"><span data-stu-id="ae65d-167">Select **Close** to confirm the entity refresh.</span></span>

 > [!NOTE]
 > <span data-ttu-id="ae65d-168">Tämän prosessin suorittaminen kestää noin 20 minuuttia.</span><span class="sxs-lookup"><span data-stu-id="ae65d-168">This process will take approximately 20 minutes to complete.</span></span> <span data-ttu-id="ae65d-169">Saat ilmoituksen, kun päivitys on valmis.</span><span class="sxs-lookup"><span data-stu-id="ae65d-169">You will be notified when the refresh is complete.</span></span>

### <a name="update-dual-write-mappings"></a><a name="run"></a><span data-ttu-id="ae65d-170">Päivitä kaksoiskirjoituksen yhdistämismääritykset</span><span class="sxs-lookup"><span data-stu-id="ae65d-170">Update dual-write mappings</span></span>

1. <span data-ttu-id="ae65d-171">Valitse **Tiedonhallinta**-työtilassa **Kaksoiskirjoitus**.</span><span class="sxs-lookup"><span data-stu-id="ae65d-171">In the **Data management** workspace, select **Dual-write**.</span></span>
2. <span data-ttu-id="ae65d-172">Valitse **Ota ratkaisut käyttöön**, valitse molemmat ratkaisut luettelosta ja valitse sitten **Käytä**.</span><span class="sxs-lookup"><span data-stu-id="ae65d-172">Select **Apply solutions**, select both solutions in the list, and then select **Apply**.</span></span>
3. <span data-ttu-id="ae65d-173">Valitse **Kaksoiskirjoitus**-sivulla seuraavat taulukkokartat ja valitse sitten **Lopeta**.</span><span class="sxs-lookup"><span data-stu-id="ae65d-173">On the **Dual-write** page, select the following table maps, and then select **Stop**.</span></span>

    - <span data-ttu-id="ae65d-174">**Project Operations -integroinnin todelliset arvot (msdyn_actuals)**</span><span class="sxs-lookup"><span data-stu-id="ae65d-174">**Project Operations integration actuals (msdyn_actuals)**</span></span>
    - <span data-ttu-id="ae65d-175">**Project Operations -integroinnin projektikululuokat (msdyn_expensecategories)**</span><span class="sxs-lookup"><span data-stu-id="ae65d-175">**Project Operations integration project expense categories (msdyn_expensecategories)**</span></span>
    - <span data-ttu-id="ae65d-176">**Project Operations -integroinnin toteutuneiden projektikulujen vientientiteetti (msdyn_expenses)**</span><span class="sxs-lookup"><span data-stu-id="ae65d-176">**Project Operations integration actuals project expenses export entity (msdyn_expenses)**</span></span>

4. <span data-ttu-id="ae65d-177">Ota **Taulukon yhdistämismäärityksen versio** -sivulla käyttöön määrityksen uusi versio kussakin kolmessa entiteetissä.</span><span class="sxs-lookup"><span data-stu-id="ae65d-177">On the **Table map version** page, apply a new version of the map to each of the three entities.</span></span>
5. <span data-ttu-id="ae65d-178">Käynnistä määritykset uudelleen valitsemalla Suorita **Kaksoiskirjoitus**-sivulla.</span><span class="sxs-lookup"><span data-stu-id="ae65d-178">On the **Dual-write** page, select run to restart the maps.</span></span>
6. <span data-ttu-id="ae65d-179">Valitse määritysluettelosta **Tapahtumarekisteri (msdyn_ledgers)** -määritys ja kaikki edellytykset ja valitse sitten **Ensimmäinen synkronointi** -valintaruutu.</span><span class="sxs-lookup"><span data-stu-id="ae65d-179">From the list of maps, select the **Ledger (msdyn_ledgers)** map with all prerequisites and select the **Initial sync** check box.</span></span> 
7. <span data-ttu-id="ae65d-180">Valitse **Ensimmäisen synkronoinnin pääkohde** -kentässä **Finance and Operations -sovellukset** ja valitse sitten **Suorita**.</span><span class="sxs-lookup"><span data-stu-id="ae65d-180">In the **Master for initial sync** field, select **Finance and Operations apps** and then select **Run**.</span></span>
 
 ![Kirjanpitomäärityksen synkronointi](media/DW6.png)
 
