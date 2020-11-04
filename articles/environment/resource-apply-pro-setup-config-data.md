---
title: Aseta määritystiedot ja ota ne käyttöön Common Data Service for Project Operationsissa
description: Tässä aiheessa on tietoja määritystietojen määrittämisestä ja käyttöönotosta Project Operationsissa.
author: sigitac
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 5e72b88a4dae1eb89859fdfd55f6d5e6ee5befcd
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/16/2020
ms.locfileid: "4075221"
---
# <a name="set-up-and-apply-configuration-data-in-the-common-data-service-for-project-operations"></a><span data-ttu-id="31dfb-103">Aseta määritystiedot ja ota ne käyttöön Common Data Service for Project Operationsissa</span><span class="sxs-lookup"><span data-stu-id="31dfb-103">Set up and apply configuration data in the Common Data Service for Project Operations</span></span>

<span data-ttu-id="31dfb-104">_**Käytetään:** Project Operationsin resursseihin ja ei-varastoitaviin perustuvissa skenaarioissa_</span><span class="sxs-lookup"><span data-stu-id="31dfb-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

## <a name="install-setup-and-configuration-data"></a><span data-ttu-id="31dfb-105">Asenna määritys- ja konfiguraatiotiedot</span><span class="sxs-lookup"><span data-stu-id="31dfb-105">Install setup and configuration data</span></span>

1. <span data-ttu-id="31dfb-106">Lataa, poista esto ja pura [Asennus- ja määritystietopaketti](https://download.microsoft.com/download/1/3/4/1349369c-6209-42b7-b3b4-5be0e67cacd8/ProjOpsSampleSetupData-%20Integrated%20UR1.zip).</span><span class="sxs-lookup"><span data-stu-id="31dfb-106">Download, unblock, and unzip the [Setup and Configuration Data Package](https://download.microsoft.com/download/1/3/4/1349369c-6209-42b7-b3b4-5be0e67cacd8/ProjOpsSampleSetupData-%20Integrated%20UR1.zip).</span></span>
2. <span data-ttu-id="31dfb-107">Siirry purettuun kansioon ja suorita suoritettava tiedosto *DataMigrationUtility*.</span><span class="sxs-lookup"><span data-stu-id="31dfb-107">Navigate to the unzipped folder and run the executable file, *DataMigrationUtility*.</span></span>
3. <span data-ttu-id="31dfb-108">Valitse ohjatussa Common Data Service Configuration Migration (CMT) -toiminnossa sivulla 1 **Tuo tiedot** ja sitten **Jatka**.</span><span class="sxs-lookup"><span data-stu-id="31dfb-108">On page 1 of the Common Data Service Configuration Migration (CMT) Wizard, select **Import Data** and then select **Continue**.</span></span>

![Määrityksen siirto](./media/1ConfigurationMigration.png)

4. <span data-ttu-id="31dfb-110">Valitse ohjatun CMT-toiminnon sivulla 2 **Microsoft 365** **Käyttöönottotyypiksi**.</span><span class="sxs-lookup"><span data-stu-id="31dfb-110">On Page 2 of the CMT Wizard, select **Microsoft 365** as the **Deployment Type**.</span></span>
5. <span data-ttu-id="31dfb-111">Valitse **Näytä käytettävissä olevien organisaatioiden luettelo** ja **Näytä lisäasetukset** -valintaruutu.</span><span class="sxs-lookup"><span data-stu-id="31dfb-111">Select the **Display a list of available organizations** and **Show Advanced** check boxes.</span></span>
6. <span data-ttu-id="31dfb-112">Valitse vuokraajan alue, anna tunnistetietosi ja valitse **Kirjaudu**.</span><span class="sxs-lookup"><span data-stu-id="31dfb-112">Select the region of your tenant, enter your credentials, and select **Login**.</span></span>

![Kirjautuminen määritykseen](./media/2ConfigurationSignin.png)

7. <span data-ttu-id="31dfb-114">Valitse sivulla 3 vuokraajan organisaatioiden luettelosta organisaatio, johon haluat tuoda esittelytiedot, ja valitse sitten **Kirjaudu**.</span><span class="sxs-lookup"><span data-stu-id="31dfb-114">On page 3, from the list of organizations on the tenant, select the organization you want to import the demo data into and select **Login**.</span></span>
8. <span data-ttu-id="31dfb-115">Valitse sivulla 4 puretusta kansiosta zip-tiedosto *SampleSetupAndConfigData*.</span><span class="sxs-lookup"><span data-stu-id="31dfb-115">On page 4, select the zip file, *SampleSetupAndConfigData* from the unpacked folder.</span></span>

![Zip-tiedoston valinta](./media/3ZipFile.png)

![Valitse tiedosto](./media/4SelectAFile.png)

9. <span data-ttu-id="31dfb-118">Kun zip-tiedosto on valittu, valitse **Tuo tiedot**.</span><span class="sxs-lookup"><span data-stu-id="31dfb-118">After the zip file is selected, select **Import Data**.</span></span>

![Tuo tiedot](./media/5ImportData.png)

10. <span data-ttu-id="31dfb-120">Tuonti kestää noin 2-10 minuuttia verkon nopeuden mukaan.</span><span class="sxs-lookup"><span data-stu-id="31dfb-120">Import will run for approximately two-ten minutes depending on your network speed.</span></span> <span data-ttu-id="31dfb-121">Kun tuonti on valmis, sulje ohjattu CMT-toiminto.</span><span class="sxs-lookup"><span data-stu-id="31dfb-121">After import completes, exit the CMT Wizard.</span></span> 
11. <span data-ttu-id="31dfb-122">Tarkista organisaatiosi tiedot seuraavissa 19 entiteetissä:</span><span class="sxs-lookup"><span data-stu-id="31dfb-122">Check your organization for data in the following 19 entities:</span></span>

  - <span data-ttu-id="31dfb-123">Valuutta</span><span class="sxs-lookup"><span data-stu-id="31dfb-123">Currency</span></span>
  - <span data-ttu-id="31dfb-124">Organisaatioyksikkö</span><span class="sxs-lookup"><span data-stu-id="31dfb-124">Organizational Unit</span></span>
  - <span data-ttu-id="31dfb-125">Ota yhteyttä</span><span class="sxs-lookup"><span data-stu-id="31dfb-125">Contact</span></span>
  - <span data-ttu-id="31dfb-126">Veroryhmä</span><span class="sxs-lookup"><span data-stu-id="31dfb-126">Tax Group</span></span>
  - <span data-ttu-id="31dfb-127">Asiakasryhmä</span><span class="sxs-lookup"><span data-stu-id="31dfb-127">Customer Group</span></span>
  - <span data-ttu-id="31dfb-128">Yksikkö</span><span class="sxs-lookup"><span data-stu-id="31dfb-128">Unit</span></span>
  - <span data-ttu-id="31dfb-129">Yksikköryhmä</span><span class="sxs-lookup"><span data-stu-id="31dfb-129">Unit Group</span></span>
  - <span data-ttu-id="31dfb-130">Hinnasto</span><span class="sxs-lookup"><span data-stu-id="31dfb-130">Price List</span></span>
  - <span data-ttu-id="31dfb-131">Projektin parametrin hinnasto</span><span class="sxs-lookup"><span data-stu-id="31dfb-131">Project Parameter Price List</span></span>
  - <span data-ttu-id="31dfb-132">Laskutustiheys</span><span class="sxs-lookup"><span data-stu-id="31dfb-132">Invoice Frequency</span></span>
  - <span data-ttu-id="31dfb-133">Varattavissa olevan resurssin luokka</span><span class="sxs-lookup"><span data-stu-id="31dfb-133">Bookable Resource Category</span></span>
  - <span data-ttu-id="31dfb-134">Tapahtumakategoria</span><span class="sxs-lookup"><span data-stu-id="31dfb-134">Transaction Category</span></span>
  - <span data-ttu-id="31dfb-135">Kululuokka</span><span class="sxs-lookup"><span data-stu-id="31dfb-135">Expense Category</span></span>
  - <span data-ttu-id="31dfb-136">Roolin hinta</span><span class="sxs-lookup"><span data-stu-id="31dfb-136">Role Price</span></span>
  - <span data-ttu-id="31dfb-137">Tapahtumaluokan hinta</span><span class="sxs-lookup"><span data-stu-id="31dfb-137">Transaction Category Price</span></span>
  - <span data-ttu-id="31dfb-138">Ominaisuus</span><span class="sxs-lookup"><span data-stu-id="31dfb-138">Characteristic</span></span>
  - <span data-ttu-id="31dfb-139">Varattavissa oleva resurssi</span><span class="sxs-lookup"><span data-stu-id="31dfb-139">Bookable Resource</span></span>
  - <span data-ttu-id="31dfb-140">Varattavissa olevan resurssin luokkaliitos</span><span class="sxs-lookup"><span data-stu-id="31dfb-140">Bookable resource category Assn</span></span>
  - <span data-ttu-id="31dfb-141">Varattavissa olevan resurssin ominaisuus</span><span class="sxs-lookup"><span data-stu-id="31dfb-141">Bookable Resource Characteristic</span></span>

![Suorita tuonti](./media/6CompleteImport.png)

## <a name="update-project-operations-configurations"></a><span data-ttu-id="31dfb-143">Project Operations -määritysten päivittäminen</span><span class="sxs-lookup"><span data-stu-id="31dfb-143">Update Project Operations configurations</span></span>

1. <span data-ttu-id="31dfb-144">Siirry CE-ympäristöön.</span><span class="sxs-lookup"><span data-stu-id="31dfb-144">Navigate to the CE environment.</span></span> <span data-ttu-id="31dfb-145">Löydät sen avaamalla [Power Platform -hallintakeskuksen](https://admin.powerplatform.microsoft.com/environments), valitsemalla ympäristön ja valitsemalla sitten **Avaa ympäristö**.</span><span class="sxs-lookup"><span data-stu-id="31dfb-145">You can find it by opening the [Power Platform Admin Center](https://admin.powerplatform.microsoft.com/environments), selecting the environment, and then selecting **Open Environment**.</span></span> 

![Avaa ympäristö](./media/7OpenEnvironment.png)

2. <span data-ttu-id="31dfb-147">Siirry kohtaan **Projektit** > **Resurssit** ja valitse sitten **Uusi** , jos haluat luoda käyttäjälle varattavissa olevan resurssin.</span><span class="sxs-lookup"><span data-stu-id="31dfb-147">Go to **Projects** > **Resources** and then select **New** to create a bookable resource for your user.</span></span>

![Varattavissa olevat resurssit](./media/8BookableResources.png)

3. <span data-ttu-id="31dfb-149">Valitse **Yleiset** -välilehdessä järjestelmänvalvojakäyttäjä.</span><span class="sxs-lookup"><span data-stu-id="31dfb-149">On the **General** tab, select your admin user.</span></span> <span data-ttu-id="31dfb-150">Tarkista, että aikavyöhyke vastaa sitä, missä olet.</span><span class="sxs-lookup"><span data-stu-id="31dfb-150">Verify that the time zone matches the one you are in.</span></span> 

![Uusi varattava resurssi](./media/9NewBookableResource.png)

4. <span data-ttu-id="31dfb-152">Valitse **Aikataulutus** -välilehden **Yritys** -kentässä **USPM** -yritys ja valitse sitten **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="31dfb-152">On the **Scheduling** tab, in the **Company** field, pick the **USPM** company, and then select **Save**.</span></span> 

![Aikataulutus-välilehti](./media/10SchedulingTab.png)

5. <span data-ttu-id="31dfb-154">Valitse **Työtunnit** -välilehti.</span><span class="sxs-lookup"><span data-stu-id="31dfb-154">Select the **Work hours** tab.</span></span>  

![Työaika](./media/11WorkHours.png)

6. <span data-ttu-id="31dfb-156">Kaksoisnapsauta mitä tahansa kalenterin arvoa ja valitse sitten **Muokkaa** > **Kaikki sarjan tapahtumat**.</span><span class="sxs-lookup"><span data-stu-id="31dfb-156">Double-click on any value in the calendar and select **Edit** > **All events in the series**.</span></span> 

![Työkalenteri](./media/12WorkCalendar.png)

7. <span data-ttu-id="31dfb-158">Vaihda työaika kahdeksan (8) tunnin työpäivään, merkitse viikonloput ei-työpäiviksi ja varmista, että aikavyöhyke omaasi.</span><span class="sxs-lookup"><span data-stu-id="31dfb-158">Change work hours to an eight (8) hour work day, mark weekends as non-work days, and make sure time zone matches yours.</span></span> 
8. <span data-ttu-id="31dfb-159">Valitse **Tallenna ja sulje**.</span><span class="sxs-lookup"><span data-stu-id="31dfb-159">Select **Save and close**.</span></span>

![Päivitä kalenteri](./media/13UpdateCalendar.png)

9. <span data-ttu-id="31dfb-161">Siirry kohtaan **Asetukset** > **Kalenterimallit** ja valitse **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="31dfb-161">Go to **Settings** > **Calendar templates** and select **New**.</span></span>
 
 ![Kalenterimallit](./media/14CalendarTemplates.png)
 
 10. <span data-ttu-id="31dfb-163">Kirjoita nimi, valitse luomasi malliresurssi ja valitse sitten **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="31dfb-163">Enter a name, select the template resource you created, and then select **Save**.</span></span> 
 
 ![Tallenna kalenterimalli](./media/15SaveCalendarTemplate.png)
 
 11. <span data-ttu-id="31dfb-165">Siirry kohtaan **Parametrit** ja kaksoisnapsauta tietuetta.</span><span class="sxs-lookup"><span data-stu-id="31dfb-165">Go to **Parameters** and double-click the record.</span></span> 
 
 ![Projektin parametrit](./media/16ProjectParameters.png)
 
12. <span data-ttu-id="31dfb-167">Päivitä seuraavat kentät:</span><span class="sxs-lookup"><span data-stu-id="31dfb-167">Update the following fields:</span></span>

 - <span data-ttu-id="31dfb-168">**Oletusyritys** : USPM</span><span class="sxs-lookup"><span data-stu-id="31dfb-168">**Default company** : USPM</span></span>
 - <span data-ttu-id="31dfb-169">**Oletusorganisaatioyksikkö** : Contoso Robotics Global</span><span class="sxs-lookup"><span data-stu-id="31dfb-169">**Default Organizational Unit** : Contoso Robotics Global</span></span>
 - <span data-ttu-id="31dfb-170">**Laskutustiheys** : seitsemäs ja viimeinen päivä</span><span class="sxs-lookup"><span data-stu-id="31dfb-170">**Invoice Frequency** : Seventh and Last day</span></span>
 - <span data-ttu-id="31dfb-171">**Työtuntimalli** : Vaihda luomaasi malliin.</span><span class="sxs-lookup"><span data-stu-id="31dfb-171">**Work hour template** : Change to the template you created.</span></span>

13. <span data-ttu-id="31dfb-172">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="31dfb-172">Select **Save**.</span></span> 

![Päivitetyt projektin parametrit](./media/17UpdatedProjectParameters.png)
