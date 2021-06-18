---
title: Määritystietojen määrittäminen ja käyttäminen Common Data Servicessa
description: Tässä aiheessa on tietoja määritystietojen määrittämisestä ja käyttöönotosta Project Operationsissa.
author: sigitac
ms.date: 05/10/2021
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 2ea00df6112fb69b61f1889463424fdfee79aec9
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/10/2021
ms.locfileid: "6001287"
---
# <a name="set-up-and-apply-configuration-data-in-the-common-data-service"></a><span data-ttu-id="ace5c-103">Määritystietojen määrittäminen ja käyttäminen Common Data Servicessa</span><span class="sxs-lookup"><span data-stu-id="ace5c-103">Set up and apply configuration data in the Common Data Service</span></span> 

<span data-ttu-id="ace5c-104">_**Käytetään:** Project Operationsin resursseihin ja ei-varastoitaviin perustuvissa skenaarioissa_</span><span class="sxs-lookup"><span data-stu-id="ace5c-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

## <a name="prerequisites"></a><span data-ttu-id="ace5c-105">Edellytykset</span><span class="sxs-lookup"><span data-stu-id="ace5c-105">Prerequisites</span></span>

<span data-ttu-id="ace5c-106">Seuraavien edellytysten on täytyttävä ennen kuin aloitat tietojen määrittämisen Common Data Servicessa (CDS):</span><span class="sxs-lookup"><span data-stu-id="ace5c-106">Before you begin to configure data in the Common Data Service (CDS), the following prerequisites must be met:</span></span>

1.  <span data-ttu-id="ace5c-107">Project Operationsia varten valmistellut CDS- ja Dynamics 365 Finance -ympäristöt.</span><span class="sxs-lookup"><span data-stu-id="ace5c-107">Provision a CDS environment and a Dynamics 365 Finance environment for Project Operations.</span></span>
2.  <span data-ttu-id="ace5c-108">CDS-ympäristöön jaetut Dynamics 365 Financen yritystiedot.</span><span class="sxs-lookup"><span data-stu-id="ace5c-108">Legal entity information from Dynamics 365 Finance is shared to the CDS environment.</span></span> <span data-ttu-id="ace5c-109">Tämän vuoksi CDS:n **Yhtiö**-entiteetillä on seuraavat yhtiötietueet:</span><span class="sxs-lookup"><span data-stu-id="ace5c-109">This means that the **Company** entity in CDS has the following company records:</span></span>
  - <span data-ttu-id="ace5c-110">THPM</span><span class="sxs-lookup"><span data-stu-id="ace5c-110">THPM</span></span>
  - <span data-ttu-id="ace5c-111">USPM</span><span class="sxs-lookup"><span data-stu-id="ace5c-111">USPM</span></span>
  - <span data-ttu-id="ace5c-112">GBPM</span><span class="sxs-lookup"><span data-stu-id="ace5c-112">GBPM</span></span>

## <a name="install-setup-and-configuration-data"></a><span data-ttu-id="ace5c-113">Asenna määritys- ja konfiguraatiotiedot</span><span class="sxs-lookup"><span data-stu-id="ace5c-113">Install setup and configuration data</span></span>

1. <span data-ttu-id="ace5c-114">Lataa, poista esto ja pura [Asennus- ja määritystietopaketti](https://download.microsoft.com/download/e/2/d/e2da6c98-d5dd-450c-aabe-fd6bf2ba374b/ProjOpsSampleSetupData-%20Integrated%20Latest.zip).</span><span class="sxs-lookup"><span data-stu-id="ace5c-114">Download, unblock, and unzip the [Setup and Configuration Data Package](https://download.microsoft.com/download/e/2/d/e2da6c98-d5dd-450c-aabe-fd6bf2ba374b/ProjOpsSampleSetupData-%20Integrated%20Latest.zip).</span></span>
2. <span data-ttu-id="ace5c-115">Siirry purettuun kansioon ja suorita suoritettava tiedosto *DataMigrationUtility*.</span><span class="sxs-lookup"><span data-stu-id="ace5c-115">Navigate to the unzipped folder and run the executable file, *DataMigrationUtility*.</span></span>
3. <span data-ttu-id="ace5c-116">Valitse ohjatussa Common Data Service Configuration Migration (CMT) -toiminnossa sivulla 1 **Tuo tiedot** ja sitten **Jatka**.</span><span class="sxs-lookup"><span data-stu-id="ace5c-116">On page 1 of the Common Data Service Configuration Migration (CMT) Wizard, select **Import Data** and then select **Continue**.</span></span>

![Määrityksen siirto](./media/1ConfigurationMigration.png)

4. <span data-ttu-id="ace5c-118">Valitse ohjatun CMT-toiminnon sivulla 2 **Microsoft 365** **Käyttöönottotyypiksi**.</span><span class="sxs-lookup"><span data-stu-id="ace5c-118">On Page 2 of the CMT Wizard, select **Microsoft 365** as the **Deployment Type**.</span></span>
5. <span data-ttu-id="ace5c-119">Valitse **Näytä käytettävissä olevien organisaatioiden luettelo** ja **Näytä lisäasetukset** -valintaruutu.</span><span class="sxs-lookup"><span data-stu-id="ace5c-119">Select the **Display a list of available organizations** and **Show Advanced** check boxes.</span></span>
6. <span data-ttu-id="ace5c-120">Valitse vuokraajan alue, anna tunnistetietosi ja valitse **Kirjaudu**.</span><span class="sxs-lookup"><span data-stu-id="ace5c-120">Select the region of your tenant, enter your credentials, and select **Login**.</span></span>

![Kirjautuminen määritykseen](./media/2ConfigurationSignin.png)

7. <span data-ttu-id="ace5c-122">Valitse sivulla 3 vuokraajan organisaatioiden luettelosta organisaatio, johon haluat tuoda esittelytiedot, ja valitse sitten **Kirjaudu**.</span><span class="sxs-lookup"><span data-stu-id="ace5c-122">On page 3, from the list of organizations on the tenant, select the organization you want to import the demo data into and select **Login**.</span></span>
8. <span data-ttu-id="ace5c-123">Valitse sivulla 4 puretusta kansiosta zip-tiedosto *SampleSetupAndConfigData*.</span><span class="sxs-lookup"><span data-stu-id="ace5c-123">On page 4, select the zip file, *SampleSetupAndConfigData* from the unpacked folder.</span></span>

![Zip-tiedoston valinta](./media/3ZipFile.png)

![Valitse tiedosto](./media/4SelectAFile.png)

9. <span data-ttu-id="ace5c-126">Kun zip-tiedosto on valittu, valitse **Tuo tiedot**.</span><span class="sxs-lookup"><span data-stu-id="ace5c-126">After the zip file is selected, select **Import Data**.</span></span>

![Tuo tiedot](./media/5ImportData.png)

10. <span data-ttu-id="ace5c-128">Tuonti kestää noin 2-10 minuuttia verkon nopeuden mukaan.</span><span class="sxs-lookup"><span data-stu-id="ace5c-128">Import will run for approximately two-ten minutes depending on your network speed.</span></span> <span data-ttu-id="ace5c-129">Kun tuonti on valmis, sulje ohjattu CMT-toiminto.</span><span class="sxs-lookup"><span data-stu-id="ace5c-129">After import completes, exit the CMT Wizard.</span></span> 
11. <span data-ttu-id="ace5c-130">Tarkista organisaatiosi tiedot seuraavissa 26 entiteetissä:</span><span class="sxs-lookup"><span data-stu-id="ace5c-130">Check your organization for data in the following 26 entities:</span></span>

  - <span data-ttu-id="ace5c-131">Valuutta</span><span class="sxs-lookup"><span data-stu-id="ace5c-131">Currency</span></span>
  - <span data-ttu-id="ace5c-132">Tilikartta</span><span class="sxs-lookup"><span data-stu-id="ace5c-132">Chart of Accounts</span></span>
  - <span data-ttu-id="ace5c-133">Kirjanpitokalenteri</span><span class="sxs-lookup"><span data-stu-id="ace5c-133">Fiscal Calendar</span></span>
  - <span data-ttu-id="ace5c-134">Vaihtokurssien tyypit</span><span class="sxs-lookup"><span data-stu-id="ace5c-134">Currency Exchange Rate Types</span></span>
  - <span data-ttu-id="ace5c-135">Maksupäivä</span><span class="sxs-lookup"><span data-stu-id="ace5c-135">Payment Day</span></span>
  - <span data-ttu-id="ace5c-136">Maksuaikataulu</span><span class="sxs-lookup"><span data-stu-id="ace5c-136">Payment Schedule</span></span>
  - <span data-ttu-id="ace5c-137">Maksuehto</span><span class="sxs-lookup"><span data-stu-id="ace5c-137">Payment Term</span></span>
  - <span data-ttu-id="ace5c-138">Organisaatioyksikkö</span><span class="sxs-lookup"><span data-stu-id="ace5c-138">Organizational Unit</span></span>
  - <span data-ttu-id="ace5c-139">Ota yhteyttä</span><span class="sxs-lookup"><span data-stu-id="ace5c-139">Contact</span></span>
  - <span data-ttu-id="ace5c-140">Veroryhmä</span><span class="sxs-lookup"><span data-stu-id="ace5c-140">Tax Group</span></span>
  - <span data-ttu-id="ace5c-141">Asiakasryhmä</span><span class="sxs-lookup"><span data-stu-id="ace5c-141">Customer Group</span></span>
  - <span data-ttu-id="ace5c-142">Toimittajaryhmä</span><span class="sxs-lookup"><span data-stu-id="ace5c-142">Vendor Group</span></span>
  - <span data-ttu-id="ace5c-143">Yksikkö</span><span class="sxs-lookup"><span data-stu-id="ace5c-143">Unit</span></span>
  - <span data-ttu-id="ace5c-144">Yksikköryhmä</span><span class="sxs-lookup"><span data-stu-id="ace5c-144">Unit Group</span></span>
  - <span data-ttu-id="ace5c-145">Hinnasto</span><span class="sxs-lookup"><span data-stu-id="ace5c-145">Price List</span></span>
  - <span data-ttu-id="ace5c-146">Projektin parametrin hinnasto</span><span class="sxs-lookup"><span data-stu-id="ace5c-146">Project Parameter Price List</span></span>
  - <span data-ttu-id="ace5c-147">Laskutustiheys</span><span class="sxs-lookup"><span data-stu-id="ace5c-147">Invoice Frequency</span></span>
  - <span data-ttu-id="ace5c-148">Varattavissa olevan resurssin luokka</span><span class="sxs-lookup"><span data-stu-id="ace5c-148">Bookable Resource Category</span></span>
  - <span data-ttu-id="ace5c-149">Tapahtumakategoria</span><span class="sxs-lookup"><span data-stu-id="ace5c-149">Transaction Category</span></span>
  - <span data-ttu-id="ace5c-150">Kululuokka</span><span class="sxs-lookup"><span data-stu-id="ace5c-150">Expense Category</span></span>
  - <span data-ttu-id="ace5c-151">Roolin hinta</span><span class="sxs-lookup"><span data-stu-id="ace5c-151">Role Price</span></span>
  - <span data-ttu-id="ace5c-152">Tapahtumaluokan hinta</span><span class="sxs-lookup"><span data-stu-id="ace5c-152">Transaction Category Price</span></span>
  - <span data-ttu-id="ace5c-153">Ominaisuus</span><span class="sxs-lookup"><span data-stu-id="ace5c-153">Characteristic</span></span>
  - <span data-ttu-id="ace5c-154">Varattavissa oleva resurssi</span><span class="sxs-lookup"><span data-stu-id="ace5c-154">Bookable Resource</span></span>
  - <span data-ttu-id="ace5c-155">Varattavissa olevan resurssin luokkaliitos</span><span class="sxs-lookup"><span data-stu-id="ace5c-155">Bookable resource category Assn</span></span>
  - <span data-ttu-id="ace5c-156">Varattavissa olevan resurssin ominaisuus</span><span class="sxs-lookup"><span data-stu-id="ace5c-156">Bookable Resource Characteristic</span></span>

![Suorita tuonti](./media/6CompleteImport.png)

## <a name="update-project-operations-configurations"></a><span data-ttu-id="ace5c-158">Project Operations -määritysten päivittäminen</span><span class="sxs-lookup"><span data-stu-id="ace5c-158">Update Project Operations configurations</span></span>

1. <span data-ttu-id="ace5c-159">Siirry CE-ympäristöön.</span><span class="sxs-lookup"><span data-stu-id="ace5c-159">Navigate to the CE environment.</span></span> <span data-ttu-id="ace5c-160">Löydät sen avaamalla [Power Platform -hallintakeskuksen](https://admin.powerplatform.microsoft.com/environments), valitsemalla ympäristön ja valitsemalla sitten **Avaa ympäristö**.</span><span class="sxs-lookup"><span data-stu-id="ace5c-160">You can find it by opening the [Power Platform Admin Center](https://admin.powerplatform.microsoft.com/environments), selecting the environment, and then selecting **Open Environment**.</span></span> 

![Avaa ympäristö](./media/7OpenEnvironment.png)

2. <span data-ttu-id="ace5c-162">Siirry kohtaan **Projektit** > **Resurssit** ja valitse sitten **Uusi**, jos haluat luoda käyttäjälle varattavissa olevan resurssin.</span><span class="sxs-lookup"><span data-stu-id="ace5c-162">Go to **Projects** > **Resources** and then select **New** to create a bookable resource for your user.</span></span>

![Varattavissa olevat resurssit](./media/8BookableResources.png)

3. <span data-ttu-id="ace5c-164">Valitse **Yleiset**-välilehdessä järjestelmänvalvojakäyttäjä.</span><span class="sxs-lookup"><span data-stu-id="ace5c-164">On the **General** tab, select your admin user.</span></span> <span data-ttu-id="ace5c-165">Tarkista, että aikavyöhyke vastaa sitä, missä olet.</span><span class="sxs-lookup"><span data-stu-id="ace5c-165">Verify that the time zone matches the one you are in.</span></span> 

![Uusi varattava resurssi](./media/9NewBookableResource.png)

4. <span data-ttu-id="ace5c-167">Valitse **Aikataulutus**-välilehden **Yritys**-kentässä **USPM**-yritys ja valitse sitten **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="ace5c-167">On the **Scheduling** tab, in the **Company** field, pick the **USPM** company, and then select **Save**.</span></span> 

![Aikataulutus-välilehti](./media/10SchedulingTab.png)

5. <span data-ttu-id="ace5c-169">Valitse **Työtunnit**-välilehti.</span><span class="sxs-lookup"><span data-stu-id="ace5c-169">Select the **Work hours** tab.</span></span>  

![Työaika](./media/11WorkHours.png)

6. <span data-ttu-id="ace5c-171">Kaksoisnapsauta mitä tahansa kalenterin arvoa ja valitse sitten **Muokkaa** > **Kaikki sarjan tapahtumat**.</span><span class="sxs-lookup"><span data-stu-id="ace5c-171">Double-click on any value in the calendar and select **Edit** > **All events in the series**.</span></span> 

![Työkalenteri](./media/12WorkCalendar.png)

7. <span data-ttu-id="ace5c-173">Vaihda työaika kahdeksan (8) tunnin työpäivään, merkitse viikonloput ei-työpäiviksi ja varmista, että aikavyöhyke omaasi.</span><span class="sxs-lookup"><span data-stu-id="ace5c-173">Change work hours to an eight (8) hour work day, mark weekends as non-work days, and make sure time zone matches yours.</span></span> 
8. <span data-ttu-id="ace5c-174">Valitse **Tallenna ja sulje**.</span><span class="sxs-lookup"><span data-stu-id="ace5c-174">Select **Save and close**.</span></span>

![Päivitä kalenteri](./media/13UpdateCalendar.png)

9. <span data-ttu-id="ace5c-176">Siirry kohtaan **Asetukset** > **Kalenterimallit** ja valitse **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="ace5c-176">Go to **Settings** > **Calendar templates** and select **New**.</span></span>
 
 ![Kalenterimallit](./media/14CalendarTemplates.png)
 
 10. <span data-ttu-id="ace5c-178">Kirjoita nimi, valitse luomasi malliresurssi ja valitse sitten **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="ace5c-178">Enter a name, select the template resource you created, and then select **Save**.</span></span> 
 
 ![Tallenna kalenterimalli](./media/15SaveCalendarTemplate.png)
 
 11. <span data-ttu-id="ace5c-180">Siirry kohtaan **Parametrit** ja kaksoisnapsauta tietuetta.</span><span class="sxs-lookup"><span data-stu-id="ace5c-180">Go to **Parameters** and double-click the record.</span></span> 
 
 ![Projektin parametrit](./media/16ProjectParameters.png)
 
12. <span data-ttu-id="ace5c-182">Päivitä seuraavat kentät:</span><span class="sxs-lookup"><span data-stu-id="ace5c-182">Update the following fields:</span></span>

 - <span data-ttu-id="ace5c-183">**Oletusyritys**: USPM</span><span class="sxs-lookup"><span data-stu-id="ace5c-183">**Default company**: USPM</span></span>
 - <span data-ttu-id="ace5c-184">**Oletusorganisaatioyksikkö**: Contoso Robotics Global</span><span class="sxs-lookup"><span data-stu-id="ace5c-184">**Default Organizational Unit**: Contoso Robotics Global</span></span>
 - <span data-ttu-id="ace5c-185">**Laskutustiheys**: seitsemäs ja viimeinen päivä</span><span class="sxs-lookup"><span data-stu-id="ace5c-185">**Invoice Frequency**: Seventh and Last day</span></span>
 - <span data-ttu-id="ace5c-186">**Työtuntimalli**: Vaihda luomaasi malliin.</span><span class="sxs-lookup"><span data-stu-id="ace5c-186">**Work hour template**: Change to the template you created.</span></span>

13. <span data-ttu-id="ace5c-187">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="ace5c-187">Select **Save**.</span></span> 

![Päivitetyt projektin parametrit](./media/17UpdatedProjectParameters.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
