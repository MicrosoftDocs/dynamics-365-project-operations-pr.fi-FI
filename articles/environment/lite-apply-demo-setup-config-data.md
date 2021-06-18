---
title: Esittelyn asennus- ja määritystietojen käyttäminen – lite
description: Tässä aiheessa on tietoja esittelyn asennus- ja määritystietojen käyttöönotosta Project Operationsissa.
author: sigitac
ms.date: 01/27/2021
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 7729b4a9ef5f498b78af298f7233d7dd45434bb3
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/10/2021
ms.locfileid: "5997147"
---
# <a name="apply-demo-setup-and-configuration-data-for-project-operations---lite"></a><span data-ttu-id="d8ebd-103">Project Operationsin esittelyn asennus- ja määritystietojen käyttäminen – lite</span><span class="sxs-lookup"><span data-stu-id="d8ebd-103">Apply demo setup and configuration data for Project Operations - lite</span></span> 

<span data-ttu-id="d8ebd-104">_\*\*Lite-käyttöönotto – kauppa proformalaskutukseen_</span><span class="sxs-lookup"><span data-stu-id="d8ebd-104">_\*\*Lite deployment - deal to proforma invoicing_</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

## <a name="prerequisites"></a><span data-ttu-id="d8ebd-105">Edellytykset</span><span class="sxs-lookup"><span data-stu-id="d8ebd-105">Prerequisites</span></span>

<span data-ttu-id="d8ebd-106">Ennen määrityksen aloittamista, Common Data Service (CDS) -ympäristön on oltava valmisteltuna Dynamics 365 Project Operationsia varten.</span><span class="sxs-lookup"><span data-stu-id="d8ebd-106">Before you begin the configuration, you must have a Common Data Service (CDS) environment provisioned for Dynamics 365 Project Operations.</span></span>


## <a name="instructions"></a><span data-ttu-id="d8ebd-107">Ohjeet</span><span class="sxs-lookup"><span data-stu-id="d8ebd-107">Instructions</span></span>

1. <span data-ttu-id="d8ebd-108">Lataa [päätietopaketti](https://download.microsoft.com/download/3/4/1/341bf279-a64f-4baa-af31-ce624859b518/ProjOpsSampleSetupData-%20CE%20only.zip).</span><span class="sxs-lookup"><span data-stu-id="d8ebd-108">Download the [Master Data Package](https://download.microsoft.com/download/3/4/1/341bf279-a64f-4baa-af31-ce624859b518/ProjOpsSampleSetupData-%20CE%20only.zip).</span></span> 
2. <span data-ttu-id="d8ebd-109">Siirry kansioon *ProjOpsSampleSetupData - CE only CMT* ja suorita suoritettava tiedosto *DataMigrationUtility*.</span><span class="sxs-lookup"><span data-stu-id="d8ebd-109">Navigate to the folder *ProjOpsSampleSetupData - CE only CMT* and run the executable file, *DataMigrationUtility*.</span></span>
3. <span data-ttu-id="d8ebd-110">Valitse ohjatussa Common Data Service Configuration Migration (CMT) -toiminnossa sivulla 1 **Tuo tiedot** ja sitten **Jatka**.</span><span class="sxs-lookup"><span data-stu-id="d8ebd-110">On page 1 of the Common Data Service Configuration Migration (CMT) Wizard, select **Import Data** and then select **Continue**.</span></span>

    ![Määrityksen siirto](./media/1ConfigurationMigration.png)

4. <span data-ttu-id="d8ebd-112">Valitse ohjatun CMT-toiminnon sivulla 2 **Microsoft 365** **Käyttöönottotyypiksi**.</span><span class="sxs-lookup"><span data-stu-id="d8ebd-112">On Page 2 of the CMT Wizard, select **Microsoft 365** as the **Deployment Type**.</span></span>
5. <span data-ttu-id="d8ebd-113">Valitse **Näytä käytettävissä olevien organisaatioiden luettelo** ja **Näytä lisäasetukset** -valintaruutu.</span><span class="sxs-lookup"><span data-stu-id="d8ebd-113">Select the **Display a list of available organizations** and **Show Advanced** check boxes.</span></span>
6. <span data-ttu-id="d8ebd-114">Valitse vuokraajan alue, anna tunnistetietosi ja valitse **Kirjaudu**.</span><span class="sxs-lookup"><span data-stu-id="d8ebd-114">Select the region of your tenant, enter your credentials, and then select **Login**.</span></span>

   ![Kirjautuminen määritykseen](./media/2ConfigurationSignin.png)

7. <span data-ttu-id="d8ebd-116">Valitse sivulla 3 vuokraajan organisaatioiden luettelosta organisaatio, johon haluat tuoda esittelytiedot, ja valitse sitten **Kirjaudu**.</span><span class="sxs-lookup"><span data-stu-id="d8ebd-116">On page 3, from the list of Organizations on the Tenant, select which organization you want to import the demo data into and then select **Login**.</span></span>
8. <span data-ttu-id="d8ebd-117">Valitse sivulla 4 zip-tiedosto *SampleSetupAndConfigData* pakkaamattomasta kansiosta *ProjOpsSampleSetupData - CE only CMT*.</span><span class="sxs-lookup"><span data-stu-id="d8ebd-117">On page 4, select the zip file, *SampleSetupAndConfigData* from the unpacked folder, *ProjOpsSampleSetupData - CE only CMT*.</span></span>

   ![Zip-tiedosto](./media/3ZipFile.png)

   ![Valitse tiedosto](./media/4SelectAFile.png)

9. <span data-ttu-id="d8ebd-120">Kun zip-tiedosto on valittu, valitse **Tuo tiedot**.</span><span class="sxs-lookup"><span data-stu-id="d8ebd-120">After the zip file is selected, select **Import Data**.</span></span>

   ![Tuo tiedot](./media/5ImportData.png)

10. <span data-ttu-id="d8ebd-122">Tuonti kestää noin 2-10 minuuttia verkon nopeuden mukaan.</span><span class="sxs-lookup"><span data-stu-id="d8ebd-122">Import will run for approximately two-ten minutes depending on your network speed.</span></span> <span data-ttu-id="d8ebd-123">Kun tuonti on valmis, sulje ohjattu CMT-toiminto.</span><span class="sxs-lookup"><span data-stu-id="d8ebd-123">After it completes, exit the CMT Wizard.</span></span> 
11. <span data-ttu-id="d8ebd-124">Tarkista organisaatiosi tiedot seuraavissa 18 entiteetissä:</span><span class="sxs-lookup"><span data-stu-id="d8ebd-124">Check your organization for data in the following 18 entities:</span></span>

    -   <span data-ttu-id="d8ebd-125">Valuutta</span><span class="sxs-lookup"><span data-stu-id="d8ebd-125">Currency</span></span>
    -   <span data-ttu-id="d8ebd-126">Tili</span><span class="sxs-lookup"><span data-stu-id="d8ebd-126">Account</span></span>
    -   <span data-ttu-id="d8ebd-127">Organisaatioyksikkö</span><span class="sxs-lookup"><span data-stu-id="d8ebd-127">Organizational Unit</span></span>
    -   <span data-ttu-id="d8ebd-128">Ota yhteyttä</span><span class="sxs-lookup"><span data-stu-id="d8ebd-128">Contact</span></span>
    -   <span data-ttu-id="d8ebd-129">Yksikkö</span><span class="sxs-lookup"><span data-stu-id="d8ebd-129">Unit</span></span>
    -   <span data-ttu-id="d8ebd-130">Yksikköryhmä</span><span class="sxs-lookup"><span data-stu-id="d8ebd-130">Unit Group</span></span>
    -   <span data-ttu-id="d8ebd-131">Hinnasto</span><span class="sxs-lookup"><span data-stu-id="d8ebd-131">Price List</span></span>
    -   <span data-ttu-id="d8ebd-132">Projektin parametrin hinnasto</span><span class="sxs-lookup"><span data-stu-id="d8ebd-132">Project Parameter Price List</span></span> 
    -   <span data-ttu-id="d8ebd-133">Laskutustiheys</span><span class="sxs-lookup"><span data-stu-id="d8ebd-133">Invoice Frequency</span></span>
    -   <span data-ttu-id="d8ebd-134">Varattavissa olevan resurssin luokka</span><span class="sxs-lookup"><span data-stu-id="d8ebd-134">Bookable Resource Category</span></span>
    -   <span data-ttu-id="d8ebd-135">Tapahtumakategoria</span><span class="sxs-lookup"><span data-stu-id="d8ebd-135">Transaction Category</span></span>
    -   <span data-ttu-id="d8ebd-136">Kululuokka</span><span class="sxs-lookup"><span data-stu-id="d8ebd-136">Expense Category</span></span>
    -   <span data-ttu-id="d8ebd-137">Roolin hinta</span><span class="sxs-lookup"><span data-stu-id="d8ebd-137">Role Price</span></span>
    -   <span data-ttu-id="d8ebd-138">Tapahtumaluokan hinta</span><span class="sxs-lookup"><span data-stu-id="d8ebd-138">Transaction Category Price</span></span>
    -   <span data-ttu-id="d8ebd-139">Ominaisuus</span><span class="sxs-lookup"><span data-stu-id="d8ebd-139">Characteristic</span></span>
    -   <span data-ttu-id="d8ebd-140">Varattavissa oleva resurssi</span><span class="sxs-lookup"><span data-stu-id="d8ebd-140">Bookable Resource</span></span>
    -   <span data-ttu-id="d8ebd-141">Varattavissa olevan resurssin luokkaliitos</span><span class="sxs-lookup"><span data-stu-id="d8ebd-141">Bookable resource category Assn</span></span>
    -   <span data-ttu-id="d8ebd-142">Varattavissa olevan resurssin ominaisuus</span><span class="sxs-lookup"><span data-stu-id="d8ebd-142">Bookable Resource Characteristic</span></span>

    ![Suorita tuonti](./media/6CompleteImport.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
