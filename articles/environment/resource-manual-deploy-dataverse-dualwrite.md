---
title: Project Operations Dataverse -sovelluksen käyttöönotto manuaalisesti kaksoiskirjoituksen tuella
description: Tässä aiheessa kerrotaan, miten Project Operations Dataverse-sovellus voidaan ottaa käyttöön manuaalisesti siten, että se tukee kaksoiskirjoitusta.
author: stsporen
ms.date: 06/18/2021
ms.topic: article
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 2ad147da542fc9e7a2705da7a834d1a6512907e5
ms.sourcegitcommit: 205a94ab4168de25b102f31d00a691c8205ba63e
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/18/2021
ms.locfileid: "6274004"
---
# <a name="manually-deploy-the-project-operations-dataverse-app-with-dual-write-support"></a><span data-ttu-id="d10c6-103">Project Operations Dataverse -sovelluksen käyttöönotto manuaalisesti kaksoiskirjoituksen tuella</span><span class="sxs-lookup"><span data-stu-id="d10c6-103">Manually deploy the Project Operations Dataverse app with dual-write support</span></span>

<span data-ttu-id="d10c6-104">_**Käytetään:** Project Operationsin resursseihin ja ei-varastoitaviin perustuvissa skenaarioissa_</span><span class="sxs-lookup"><span data-stu-id="d10c6-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="d10c6-105">Tässä aiheessa kerrotaan, miten Microsoft Dynamics 365 Project Operations Microsoft Dataversessa voidaan ottaa käyttöön manuaalisesti siten, että se tukee kaksoiskirjoitusta.</span><span class="sxs-lookup"><span data-stu-id="d10c6-105">This topic explains how to manually deploy Microsoft Dynamics 365 Project Operations in Microsoft Dataverse so that it supports dual-write.</span></span> <span data-ttu-id="d10c6-106">Project Operations havaitsee ympäristön määritykset ja lisää lisätuen kaksoiskirjoitukselle, jos vaatimukset täyttyvät.</span><span class="sxs-lookup"><span data-stu-id="d10c6-106">Project Operations detects the environment's configuration and adds additional support for dual-write if the prerequisites are met.</span></span>

<span data-ttu-id="d10c6-107">Jos olet toiminut tämän aiheen ohjeiden mukaisesti käyttöönoton aikana Microsoft Dynamics Lifecycle Services (LCS) -palvelussa, voit ohittaa Microsoft Power Platform -integroinnin käyttöönoton (jota kutsuttiin aiemmin Common Data Service -ympäristöksi).</span><span class="sxs-lookup"><span data-stu-id="d10c6-107">During deployment through Microsoft Dynamics Lifecycle Services (LCS), if you've followed the instructions in this topic, you can skip the deployment of the Microsoft Power Platform integration (previously known as the Common Data Service environment).</span></span>

<span data-ttu-id="d10c6-108">Project Operationsin käyttöönotossa Dataversessa siten, että se tukee kaksoiskirjoitusta, on neljä päävaihetta:</span><span class="sxs-lookup"><span data-stu-id="d10c6-108">The process of deploying Project Operations in Dataverse so that it supports dual-write has four main steps:</span></span>

1. <span data-ttu-id="d10c6-109">[Luo Dataversessa uusi ympäristö, joka tukee kaksoiskirjoitusta](#create).</span><span class="sxs-lookup"><span data-stu-id="d10c6-109">[Create a new environment in Dataverse that supports dual-write](#create).</span></span>
2. <span data-ttu-id="d10c6-110">[Lisää kaksoiskirjoituksen vaatimukset ympäristöön](#prerequisites).</span><span class="sxs-lookup"><span data-stu-id="d10c6-110">[Add dual-write prerequisites to the environment](#prerequisites).</span></span>
3. <span data-ttu-id="d10c6-111">[Lisää Project Operations Dataverse -sovellus](#dataverse).</span><span class="sxs-lookup"><span data-stu-id="d10c6-111">[Add the Project Operations Dataverse app](#dataverse).</span></span>
4. <span data-ttu-id="d10c6-112">[Linkitä ympäristösi](#link).</span><span class="sxs-lookup"><span data-stu-id="d10c6-112">[Link your environments](#link).</span></span>

## <a name="create-a-new-environment-in-dataverse-that-supports-dual-write"></a><a name="create"></a><span data-ttu-id="d10c6-113">Luo Dataversessa uusi ympäristö, joka tukee kaksoiskirjoitusta</span><span class="sxs-lookup"><span data-stu-id="d10c6-113">Create a new environment in Dataverse that supports dual-write</span></span>

<span data-ttu-id="d10c6-114">Voit suorittaa tämän menettelyn kirjautumalla sisään järjestelmänvalvojana.</span><span class="sxs-lookup"><span data-stu-id="d10c6-114">To complete this procedure, you must sign in as an administrator.</span></span>

1. <span data-ttu-id="d10c6-115">Avaa [Power Platform -hallintakeskus](https://admin.powerplatform.com) ja kirjaudu sisään järjestelmänvalvojana.</span><span class="sxs-lookup"><span data-stu-id="d10c6-115">Open the [Power Platform admin center](https://admin.powerplatform.com), and sign in as an administrator.</span></span>
2. <span data-ttu-id="d10c6-116">Luo uusi ympäristö ja nimeä se.</span><span class="sxs-lookup"><span data-stu-id="d10c6-116">Create a new environment, and name it.</span></span>
3. <span data-ttu-id="d10c6-117">Valitse ympäristötyyppi.</span><span class="sxs-lookup"><span data-stu-id="d10c6-117">Select the environment type.</span></span> <span data-ttu-id="d10c6-118">Jos rekisteröidyit kokeilutarjousta varten, valitse **Kokeilu (tilauspohjainen)**.</span><span class="sxs-lookup"><span data-stu-id="d10c6-118">If you signed up for the trial offer, select **Trial (subscription-based)**.</span></span>
4. <span data-ttu-id="d10c6-119">Vahvista käyttöönottoalue.</span><span class="sxs-lookup"><span data-stu-id="d10c6-119">Confirm the deployment region.</span></span>
5. <span data-ttu-id="d10c6-120">Ota käyttöön **Luo tietokanta tätä ympäristöä varten** -vaihtoehto.</span><span class="sxs-lookup"><span data-stu-id="d10c6-120">Enable the **Create a database for this environment** option.</span></span> 
6. <span data-ttu-id="d10c6-121">Vahvista kieli ja vahvista sitten, että valuutta vastaa Finance and Operations -sovellusten valuuttaa.</span><span class="sxs-lookup"><span data-stu-id="d10c6-121">Confirm the language, and then confirm that the currency matches the currency for your Finance and Operations apps.</span></span>
7. <span data-ttu-id="d10c6-122">Ota **Dynamics 365 -sovellukset** -vaihtoehto käyttöön ja vahvista, että **Ota nämä sovellukset käyttöön automaattisesti** -kentän asetus on **Ei mitään**.</span><span class="sxs-lookup"><span data-stu-id="d10c6-122">Enable the **Dynamics 365 apps** option, and confirm that the **Automatically deploy these apps** field is set to **None**.</span></span>
8. <span data-ttu-id="d10c6-123">Lisää käyttöoikeusryhmä, jos käyttöoikeusryhmä on pakollinen.</span><span class="sxs-lookup"><span data-stu-id="d10c6-123">Add a security group, if a security group is required.</span></span>
9. <span data-ttu-id="d10c6-124">Valitse **Tallenna** luodaksesi ympäristön.</span><span class="sxs-lookup"><span data-stu-id="d10c6-124">Select **Save** to create the environment.</span></span>
10. <span data-ttu-id="d10c6-125">Odota käyttöönoton valmistumista ja että ympäristön tila on **Valmis**.</span><span class="sxs-lookup"><span data-stu-id="d10c6-125">Wait until the deployment is completed and the environment reaches the **Ready** state.</span></span>

## <a name="add-dual-write-prerequisites-to-the-environment"></a><a name="prerequisites"></a><span data-ttu-id="d10c6-126">Lisää kaksoiskirjoituksen vaatimukset ympäristöön</span><span class="sxs-lookup"><span data-stu-id="d10c6-126">Add dual-write prerequisites to the environment</span></span>

<span data-ttu-id="d10c6-127">Kaksoiskirjoituksen tuki sisältää lisäkenttiä, jotka lisätään avainentiteetteihin, kuten **Yritys**-entiteettiin.</span><span class="sxs-lookup"><span data-stu-id="d10c6-127">Dual-write support includes additional fields that are added to key entities, such as the **Company** entity.</span></span> <span data-ttu-id="d10c6-128">Jos lisäät kaksoiskirjoituksen tukea olemassa olevaan ympäristöön, tiedot on ehkä päivitettävä, jotta tuki voidaan ottaa käyttöön.</span><span class="sxs-lookup"><span data-stu-id="d10c6-128">If you're adding dual-write support to an existing environment, you might have to update the data to enable the support.</span></span> <span data-ttu-id="d10c6-129">Tietoja olemassa olevien tietojen käytössä on aiheessa[Käytä olemassa olevia yritystietoja](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/bootstrap-company-data).</span><span class="sxs-lookup"><span data-stu-id="d10c6-129">For information about how to bootstrap the data, see [Bootstrap company data](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/bootstrap-company-data).</span></span> <span data-ttu-id="d10c6-130">Lisätietoja kaksoiskirjoituksesta on aiheessa [Kaksoiskirjoituksen järjestelmävaatimukset](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-system-req).</span><span class="sxs-lookup"><span data-stu-id="d10c6-130">For more information about dual-write, see [Dual-write system requirements](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-system-req).</span></span>

<span data-ttu-id="d10c6-131">Suorita tämä menettely lisätäksesi kaksoiskirjoituksen vaatimukset ympäristöösi.</span><span class="sxs-lookup"><span data-stu-id="d10c6-131">Complete this procedure to add the dual-write prerequisites to your environment.</span></span>

1. <span data-ttu-id="d10c6-132">Avaa juuri luomasi ympäristö ja siirry sitten kohtaan **Resurssi** \> **Dynamics 365 -sovellukset**.</span><span class="sxs-lookup"><span data-stu-id="d10c6-132">Open the environment that you just created, and then go to **Resource** \> **Dynamics 365 apps**.</span></span>
2. <span data-ttu-id="d10c6-133">Valitse sovellusluettelosta **Kaksoiskirjoituksen ydinratkaisu** ja asenna se.</span><span class="sxs-lookup"><span data-stu-id="d10c6-133">Select **Dual-write core solution** in the app list, and install it.</span></span>
3. <span data-ttu-id="d10c6-134">Odota asennuksen valmistumista.</span><span class="sxs-lookup"><span data-stu-id="d10c6-134">Wait until the installation is completed.</span></span> <span data-ttu-id="d10c6-135">Valitse sitten sovellusluettelosta **Kaksoiskirjoituksen järjestämisratkaisu** ja asenna se.</span><span class="sxs-lookup"><span data-stu-id="d10c6-135">Then select **Dual-write application orchestration solution** in the app list, and install it.</span></span>

## <a name="add-the-project-operations-dataverse-app"></a><a name="dataverse"></a><span data-ttu-id="d10c6-136">Lisää Project Operations Dataverse -sovellus</span><span class="sxs-lookup"><span data-stu-id="d10c6-136">Add the Project Operations Dataverse app</span></span>

<span data-ttu-id="d10c6-137">Voit suorittaa tämän menettelyn vain, jos olet suorittanut aiemmat menettelyt ennen Project Operationsin asentamista.</span><span class="sxs-lookup"><span data-stu-id="d10c6-137">You can complete this procedure only if you completed the previous procedures before you installed Project Operations.</span></span> <span data-ttu-id="d10c6-138">Asennuksen aikana järjestelmä analysoi ympäristön määritykset ja lisää tarvittaessa kaksoiskirjoituksen tuen.</span><span class="sxs-lookup"><span data-stu-id="d10c6-138">During installation, the system analyzes the environment configuration and adds support for dual-write if it's required.</span></span>

1. <span data-ttu-id="d10c6-139">Avaa aiemmin luomasi ympäristö ja siirry sitten kohtaan **Resurssi** \> **Dynamics 365 -sovellukset**.</span><span class="sxs-lookup"><span data-stu-id="d10c6-139">Open the environment that you created earlier, and then go to **Resource** \> **Dynamics 365 apps**.</span></span>
2. <span data-ttu-id="d10c6-140">Valitse sovellusluettelosta **Microsoft Dynamics 365 Project Operations** ja asenna se.</span><span class="sxs-lookup"><span data-stu-id="d10c6-140">Select **Microsoft Dynamics 365 Project Operations** in the app list, and install it.</span></span>

## <a name="link-your-environments"></a><a name="link"></a><span data-ttu-id="d10c6-141">Linkitä ympäristösi</span><span class="sxs-lookup"><span data-stu-id="d10c6-141">Link your environments</span></span>

<span data-ttu-id="d10c6-142">Kun Dataverse-ympäristö on otettu käyttöön, voit määrittää linkin Finance and Operations -sovelluksissasi.</span><span class="sxs-lookup"><span data-stu-id="d10c6-142">After the Dataverse environment is deployed, you can set up the link in your Finance and Operations apps.</span></span> <span data-ttu-id="d10c6-143">Seuraa ohjeita kohdassa [Käytä kaksoiskirjoituksen opastettua toimintoja ympäristöihisi linkittämistä varten](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/link-your-environment).</span><span class="sxs-lookup"><span data-stu-id="d10c6-143">Follow the steps in [Use the dual-write wizard to link your environments](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/link-your-environment).</span></span>
