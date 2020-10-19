---
title: Käytä esittelyn asennus- ja määritystietoja
description: Tässä aiheessa on tietoja esittelyn asennus- ja määritystietojen käyttöönotosta Project Operationsissa.
author: sigitac
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 42e02f393e89d20b2a462645f519a3792bee8f2f
ms.sourcegitcommit: b9d8bf00239815f31686e9b28998ac684fd2fca4
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/02/2020
ms.locfileid: "3948837"
---
# <a name="apply-demo-setup-and-configuration-data-for-project-operations-lite-deployment---deal-to-proforma-invoicing"></a><span data-ttu-id="c734f-103">Ota esittelyn asennus- ja määritystietoja käyttöön Project Operations lite – kauppa proformalaskutukseen -käyttöönotossa</span><span class="sxs-lookup"><span data-stu-id="c734f-103">Apply demo setup and configuration data for Project Operations lite deployment - deal to proforma invoicing</span></span>

<span data-ttu-id="c734f-104">_\*\*Lite-käyttöönotto – kauppa proformalaskutukseen_</span><span class="sxs-lookup"><span data-stu-id="c734f-104">_\*\*Lite deployment - deal to proforma invoicing_</span></span>

1. <span data-ttu-id="c734f-105">Lataa [päätietopaketti](https://download.microsoft.com/download/3/4/1/341bf279-a64f-4baa-af31-ce624859b518/ProjOpsSampleSetupData%20-%20CE%20only%20CMT.zip).</span><span class="sxs-lookup"><span data-stu-id="c734f-105">Download the [Master Data Package](https://download.microsoft.com/download/3/4/1/341bf279-a64f-4baa-af31-ce624859b518/ProjOpsSampleSetupData%20-%20CE%20only%20CMT.zip).</span></span> 
2. <span data-ttu-id="c734f-106">Siirry kansioon *ProjOpsDemoDataSetupAndMaster - Integrated CMT* ja suorita suoritettava tiedosto *DataMigrationUtility*.</span><span class="sxs-lookup"><span data-stu-id="c734f-106">Navigate to the folder *ProjOpsDemoDataSetupAndMaster - Integrated CMT* and run the executable file, *DataMigrationUtility*.</span></span>
3. <span data-ttu-id="c734f-107">Valitse ohjatussa Common Data Service Configuration Migration (CMT) -toiminnossa sivulla 1 **Tuo tiedot** ja sitten **Jatka**.</span><span class="sxs-lookup"><span data-stu-id="c734f-107">On page 1 of the Common Data Service Configuration Migration (CMT) Wizard, select **Import Data** and then select **Continue**.</span></span>

![Määrityksen siirto](./media/1ConfigurationMigration.png)

4. <span data-ttu-id="c734f-109">Valitse ohjatun CMT-toiminnon sivulla 2 **Office 365** **asennustyypiksi**.</span><span class="sxs-lookup"><span data-stu-id="c734f-109">On Page 2 of the CMT Wizard, select **Office 365** as the **Deployment Type**.</span></span>
5. <span data-ttu-id="c734f-110">Valitse **Näytä käytettävissä olevien organisaatioiden luettelo** ja **Näytä lisäasetukset** -valintaruutu.</span><span class="sxs-lookup"><span data-stu-id="c734f-110">Select the **Display a list of available organizations** and **Show Advanced** check boxes.</span></span>
6. <span data-ttu-id="c734f-111">Valitse vuokraajan alue, anna tunnistetietosi ja valitse **Kirjaudu**.</span><span class="sxs-lookup"><span data-stu-id="c734f-111">Select the region of your tenant, enter your credentials, and then select **Login**.</span></span>

![Kirjautuminen määritykseen](./media/2ConfigurationSignin.png)

7. <span data-ttu-id="c734f-113">Valitse sivulla 3 vuokraajan organisaatioiden luettelosta organisaatio, johon haluat tuoda esittelytiedot, ja valitse sitten **Kirjaudu**.</span><span class="sxs-lookup"><span data-stu-id="c734f-113">On page 3, from the list of Organizations on the Tenant, select which organization you want to import the demo data into and then select **Login**.</span></span>
8. <span data-ttu-id="c734f-114">Valitse sivulla 4 puretusta *ProjOpsDemoDataSetupAndMaster - Integrated CMT* -kansiosta zip-tiedosto *MasterAndSetupData*.</span><span class="sxs-lookup"><span data-stu-id="c734f-114">On page 4, select the zip file, *MasterAndSetupData* from the unpacked folder, *ProjOpsDemoDataSetupAndMaster - Integrated CMT*.</span></span>

![Zip-tiedosto](./media/3ZipFile.png)

![Valitse tiedosto](./media/4SelectAFile.png)

9. <span data-ttu-id="c734f-117">Kun zip-tiedosto on valittu, valitse **Tuo tiedot**.</span><span class="sxs-lookup"><span data-stu-id="c734f-117">After the zip file is selected, select **Import Data**.</span></span>

![Tuo tiedot](./media/5ImportData.png)

10. <span data-ttu-id="c734f-119">Tuonti kestää noin 2-10 minuuttia verkon nopeuden mukaan.</span><span class="sxs-lookup"><span data-stu-id="c734f-119">Import will run for approximately two-ten minutes depending on your network speed.</span></span> <span data-ttu-id="c734f-120">Kun tuonti on valmis, sulje ohjattu CMT-toiminto.</span><span class="sxs-lookup"><span data-stu-id="c734f-120">After it completes, exit the CMT Wizard.</span></span> 
11. <span data-ttu-id="c734f-121">Tarkista organisaatiosi tiedot seuraavissa 20 entiteetissä:</span><span class="sxs-lookup"><span data-stu-id="c734f-121">Check your organization for data in the following 20 entities:</span></span>

- <span data-ttu-id="c734f-122">Valuutta</span><span class="sxs-lookup"><span data-stu-id="c734f-122">Currency</span></span>
- <span data-ttu-id="c734f-123">Organisaatioyksikkö</span><span class="sxs-lookup"><span data-stu-id="c734f-123">Organizational Unit</span></span>
- <span data-ttu-id="c734f-124">Ota yhteyttä</span><span class="sxs-lookup"><span data-stu-id="c734f-124">Contact</span></span>
- <span data-ttu-id="c734f-125">Veroryhmä</span><span class="sxs-lookup"><span data-stu-id="c734f-125">Tax Group</span></span>
- <span data-ttu-id="c734f-126">Asiakasryhmä</span><span class="sxs-lookup"><span data-stu-id="c734f-126">Customer Group</span></span>
- <span data-ttu-id="c734f-127">Yksikkö</span><span class="sxs-lookup"><span data-stu-id="c734f-127">Unit</span></span>
- <span data-ttu-id="c734f-128">Yksikköryhmä</span><span class="sxs-lookup"><span data-stu-id="c734f-128">Unit Group</span></span>
- <span data-ttu-id="c734f-129">Hinnasto</span><span class="sxs-lookup"><span data-stu-id="c734f-129">Price List</span></span>
- <span data-ttu-id="c734f-130">Projektin parametrin hinnasto</span><span class="sxs-lookup"><span data-stu-id="c734f-130">Project Parameter Price List</span></span>
- <span data-ttu-id="c734f-131">Laskutustiheys</span><span class="sxs-lookup"><span data-stu-id="c734f-131">Invoice Frequency</span></span>
- <span data-ttu-id="c734f-132">Laskutustiheyden tiedot</span><span class="sxs-lookup"><span data-stu-id="c734f-132">Invoice Frequency Detail</span></span>
- <span data-ttu-id="c734f-133">Varattavissa olevan resurssin luokka</span><span class="sxs-lookup"><span data-stu-id="c734f-133">Bookable Resource Category</span></span>
- <span data-ttu-id="c734f-134">Tapahtumakategoria</span><span class="sxs-lookup"><span data-stu-id="c734f-134">Transaction Category</span></span>
- <span data-ttu-id="c734f-135">Kululuokka</span><span class="sxs-lookup"><span data-stu-id="c734f-135">Expense Category</span></span>
- <span data-ttu-id="c734f-136">Roolin hinta</span><span class="sxs-lookup"><span data-stu-id="c734f-136">Role Price</span></span>
- <span data-ttu-id="c734f-137">Tapahtumaluokan hinta</span><span class="sxs-lookup"><span data-stu-id="c734f-137">Transaction Category Price</span></span>
- <span data-ttu-id="c734f-138">Ominaisuus</span><span class="sxs-lookup"><span data-stu-id="c734f-138">Characteristic</span></span>
- <span data-ttu-id="c734f-139">Varattavissa oleva resurssi</span><span class="sxs-lookup"><span data-stu-id="c734f-139">Bookable Resource</span></span>
- <span data-ttu-id="c734f-140">Varattavissa olevan resurssin luokkaliitos</span><span class="sxs-lookup"><span data-stu-id="c734f-140">Bookable resource category Assn</span></span>
- <span data-ttu-id="c734f-141">Varattavissa olevan resurssin ominaisuus</span><span class="sxs-lookup"><span data-stu-id="c734f-141">Bookable Resource Characteristic</span></span>

![Suorita tuonti](./media/6CompleteImport.png)
