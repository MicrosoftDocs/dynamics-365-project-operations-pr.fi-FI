---
title: Esittelyn asennus- ja määritystietojen käyttäminen – lite
description: Tässä aiheessa on tietoja esittelyn asennus- ja määritystietojen käyttöönotosta Project Operationsissa.
author: sigitac
manager: Annbe
ms.date: 11/04/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 5cfc270c07a568d692f6cd180b9c367ae185044c
ms.sourcegitcommit: 14aa380759214713d9bf560f5a7f619b7f4bd5b8
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/05/2020
ms.locfileid: "4401259"
---
# <a name="apply-demo-setup-and-configuration-data-for-project-operations---lite"></a><span data-ttu-id="82b70-103">Project Operationsin esittelyn asennus- ja määritystietojen käyttäminen – lite</span><span class="sxs-lookup"><span data-stu-id="82b70-103">Apply demo setup and configuration data for Project Operations - lite</span></span> 

<span data-ttu-id="82b70-104">_\*\*Lite-käyttöönotto – kauppa proformalaskutukseen_</span><span class="sxs-lookup"><span data-stu-id="82b70-104">_\*\*Lite deployment - deal to proforma invoicing_</span></span>

## <a name="prerequisites"></a><span data-ttu-id="82b70-105">Edellytykset</span><span class="sxs-lookup"><span data-stu-id="82b70-105">Prerequisites</span></span>

<span data-ttu-id="82b70-106">Ennen määrityksen aloittamista Dynamics 365 Project Operationsin Common Data Service (CDS) -ympäristön on oltava määritettynä.</span><span class="sxs-lookup"><span data-stu-id="82b70-106">Before you begin the configuration, you must have a Common Data Service (CDS) environment provisioned for Dynamics 365 Project Operations.</span></span>


## <a name="instructions"></a><span data-ttu-id="82b70-107">Ohjeet</span><span class="sxs-lookup"><span data-stu-id="82b70-107">Instructions</span></span>

1. <span data-ttu-id="82b70-108">Lataa [päätietopaketti](https://download.microsoft.com/download/3/4/1/341bf279-a64f-4baa-af31-ce624859b518/ProjOpsSampleSetupData%20-%20CE%20only%20CMT.zip).</span><span class="sxs-lookup"><span data-stu-id="82b70-108">Download the [Master Data Package](https://download.microsoft.com/download/3/4/1/341bf279-a64f-4baa-af31-ce624859b518/ProjOpsSampleSetupData%20-%20CE%20only%20CMT.zip).</span></span> 
2. <span data-ttu-id="82b70-109">Siirry kansioon *ProjOpsDemoDataSetupAndMaster - Integrated CMT* ja suorita suoritettava tiedosto *DataMigrationUtility*.</span><span class="sxs-lookup"><span data-stu-id="82b70-109">Navigate to the folder *ProjOpsDemoDataSetupAndMaster - Integrated CMT* and run the executable file, *DataMigrationUtility*.</span></span>
3. <span data-ttu-id="82b70-110">Valitse ohjatussa Common Data Service Configuration Migration (CMT) -toiminnossa sivulla 1 **Tuo tiedot** ja sitten **Jatka**.</span><span class="sxs-lookup"><span data-stu-id="82b70-110">On page 1 of the Common Data Service Configuration Migration (CMT) Wizard, select **Import Data** and then select **Continue**.</span></span>

![Määrityksen siirto](./media/1ConfigurationMigration.png)

4. <span data-ttu-id="82b70-112">Valitse ohjatun CMT-toiminnon sivulla 2 **Microsoft 365** **Käyttöönottotyypiksi**.</span><span class="sxs-lookup"><span data-stu-id="82b70-112">On Page 2 of the CMT Wizard, select **Microsoft 365** as the **Deployment Type**.</span></span>
5. <span data-ttu-id="82b70-113">Valitse **Näytä käytettävissä olevien organisaatioiden luettelo** ja **Näytä lisäasetukset** -valintaruutu.</span><span class="sxs-lookup"><span data-stu-id="82b70-113">Select the **Display a list of available organizations** and **Show Advanced** check boxes.</span></span>
6. <span data-ttu-id="82b70-114">Valitse vuokraajan alue, anna tunnistetietosi ja valitse **Kirjaudu**.</span><span class="sxs-lookup"><span data-stu-id="82b70-114">Select the region of your tenant, enter your credentials, and then select **Login**.</span></span>

![Kirjautuminen määritykseen](./media/2ConfigurationSignin.png)

7. <span data-ttu-id="82b70-116">Valitse sivulla 3 vuokraajan organisaatioiden luettelosta organisaatio, johon haluat tuoda esittelytiedot, ja valitse sitten **Kirjaudu**.</span><span class="sxs-lookup"><span data-stu-id="82b70-116">On page 3, from the list of Organizations on the Tenant, select which organization you want to import the demo data into and then select **Login**.</span></span>
8. <span data-ttu-id="82b70-117">Valitse sivulla 4 puretusta *ProjOpsDemoDataSetupAndMaster - Integrated CMT* -kansiosta zip-tiedosto *MasterAndSetupData*.</span><span class="sxs-lookup"><span data-stu-id="82b70-117">On page 4, select the zip file, *MasterAndSetupData* from the unpacked folder, *ProjOpsDemoDataSetupAndMaster - Integrated CMT*.</span></span>

![Zip-tiedosto](./media/3ZipFile.png)

![Valitse tiedosto](./media/4SelectAFile.png)

9. <span data-ttu-id="82b70-120">Kun zip-tiedosto on valittu, valitse **Tuo tiedot**.</span><span class="sxs-lookup"><span data-stu-id="82b70-120">After the zip file is selected, select **Import Data**.</span></span>

![Tuo tiedot](./media/5ImportData.png)

10. <span data-ttu-id="82b70-122">Tuonti kestää noin 2-10 minuuttia verkon nopeuden mukaan.</span><span class="sxs-lookup"><span data-stu-id="82b70-122">Import will run for approximately two-ten minutes depending on your network speed.</span></span> <span data-ttu-id="82b70-123">Kun tuonti on valmis, sulje ohjattu CMT-toiminto.</span><span class="sxs-lookup"><span data-stu-id="82b70-123">After it completes, exit the CMT Wizard.</span></span> 
11. <span data-ttu-id="82b70-124">Tarkista organisaatiosi tiedot seuraavissa 20 entiteetissä:</span><span class="sxs-lookup"><span data-stu-id="82b70-124">Check your organization for data in the following 20 entities:</span></span>

-   <span data-ttu-id="82b70-125">Valuutta</span><span class="sxs-lookup"><span data-stu-id="82b70-125">Currency</span></span>
-   <span data-ttu-id="82b70-126">Tili</span><span class="sxs-lookup"><span data-stu-id="82b70-126">Account</span></span>
-   <span data-ttu-id="82b70-127">Organisaatioyksikkö</span><span class="sxs-lookup"><span data-stu-id="82b70-127">Organizational Unit</span></span>
-   <span data-ttu-id="82b70-128">Ota yhteyttä</span><span class="sxs-lookup"><span data-stu-id="82b70-128">Contact</span></span>
-   <span data-ttu-id="82b70-129">Veroryhmä</span><span class="sxs-lookup"><span data-stu-id="82b70-129">Tax Group</span></span>
-   <span data-ttu-id="82b70-130">Asiakasryhmä</span><span class="sxs-lookup"><span data-stu-id="82b70-130">Customer Group</span></span>
-   <span data-ttu-id="82b70-131">Yksikkö</span><span class="sxs-lookup"><span data-stu-id="82b70-131">Unit</span></span>
-   <span data-ttu-id="82b70-132">Yksikköryhmä</span><span class="sxs-lookup"><span data-stu-id="82b70-132">Unit Group</span></span>
-   <span data-ttu-id="82b70-133">Hinnasto</span><span class="sxs-lookup"><span data-stu-id="82b70-133">Price List</span></span>
-   <span data-ttu-id="82b70-134">Projektin parametrin hinnasto</span><span class="sxs-lookup"><span data-stu-id="82b70-134">Project Parameter Price List</span></span> 
-   <span data-ttu-id="82b70-135">Laskutustiheys</span><span class="sxs-lookup"><span data-stu-id="82b70-135">Invoice Frequency</span></span>
-   <span data-ttu-id="82b70-136">Varattavissa olevan resurssin luokka</span><span class="sxs-lookup"><span data-stu-id="82b70-136">Bookable Resource Category</span></span>
-   <span data-ttu-id="82b70-137">Tapahtumakategoria</span><span class="sxs-lookup"><span data-stu-id="82b70-137">Transaction Category</span></span>
-   <span data-ttu-id="82b70-138">Kululuokka</span><span class="sxs-lookup"><span data-stu-id="82b70-138">Expense Category</span></span>
-   <span data-ttu-id="82b70-139">Roolin hinta</span><span class="sxs-lookup"><span data-stu-id="82b70-139">Role Price</span></span>
-   <span data-ttu-id="82b70-140">Tapahtumaluokan hinta</span><span class="sxs-lookup"><span data-stu-id="82b70-140">Transaction Category Price</span></span>
-   <span data-ttu-id="82b70-141">Ominaisuus</span><span class="sxs-lookup"><span data-stu-id="82b70-141">Characteristic</span></span>
-   <span data-ttu-id="82b70-142">Varattavissa oleva resurssi</span><span class="sxs-lookup"><span data-stu-id="82b70-142">Bookable Resource</span></span>
-   <span data-ttu-id="82b70-143">Varattavissa olevan resurssin luokkaliitos</span><span class="sxs-lookup"><span data-stu-id="82b70-143">Bookable resource category Assn</span></span>
-   <span data-ttu-id="82b70-144">Varattavissa olevan resurssin ominaisuus</span><span class="sxs-lookup"><span data-stu-id="82b70-144">Bookable Resource Characteristic</span></span>

![Suorita tuonti](./media/6CompleteImport.png)
