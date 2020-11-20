---
title: Mukautettujen kenttien ja entiteettien luominen
description: Tässä aiheessa selitetään, miten Power Apps-ympäristön omassa ratkaisussasi luodaan asetusjoukkoja ja entiteettejä.
author: Rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 10/01/2020
ms.topic: article
ms.service: business-applications
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 442ff9cf2206bec307cea7ff30b9266502d8f77b
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/16/2020
ms.locfileid: "4075417"
---
# <a name="create-custom-fields-and-entities"></a><span data-ttu-id="e0710-103">Mukautettujen kenttien ja entiteettien luominen</span><span class="sxs-lookup"><span data-stu-id="e0710-103">Create custom fields and entities</span></span> 

<span data-ttu-id="e0710-104">Toimi seuraavasti aina, kun haluat luoda mukautetun asetusjoukon tai entiteetin Power Apps-ympäristössä.</span><span class="sxs-lookup"><span data-stu-id="e0710-104">Complete the following steps any time that you want to create a custom option set or entity on the Power Apps platform.</span></span>  
<span data-ttu-id="e0710-105">Tämän aiheen toimintojoukot on tarkoitus suorittaa Project Service Automationin (PSA) verkkoliittymän avulla.</span><span class="sxs-lookup"><span data-stu-id="e0710-105">The procedures in this topic should be completed using the web interface of Project Service Automation (PSA).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="e0710-106">Suosittelemme kaikkien mukautettujen hinnoitteludimensioiden muutokset erillisessä ratkaisussa.</span><span class="sxs-lookup"><span data-stu-id="e0710-106">We recommend that you make all custom pricing dimension changes in a separate solution.</span></span> <span data-ttu-id="e0710-107">Tämä tärkeä paras käytäntö varmistaa, että muutoksia voidaan myöhemmin päivittää tai poistaa tarpeen mukaan, auttaa työn uudelleenkäytössä ja helpottaa näiden muutosten siirtämistä toiseen esiintymään.</span><span class="sxs-lookup"><span data-stu-id="e0710-107">This important best practice provides flexibility in the future to update or remove changes as needed, will help with re-use of your work, and makes it easier to port these changes to another instance.</span></span> <span data-ttu-id="e0710-108">Kun olet tehnyt kaikki tarvittavat muutokset, vie tämä ratkaisu muodossa **Hallittu ratkaisu** ja tuo se muihin esiintymiin, jotta voit käyttää hinnoittelumäärityksiäsi uudelleen.</span><span class="sxs-lookup"><span data-stu-id="e0710-108">After you have made all of the required changes, export this solution as a **Managed solution** and import it into other instances to reuse your pricing setup.</span></span>

  
## <a name="create-custom-fields-and-option-sets-in-the-pricing-dimension-solution"></a><span data-ttu-id="e0710-109">Mukautettujen kenttien ja asetusjoukkojen luominen hinnoitteludimensioratkaisussa</span><span class="sxs-lookup"><span data-stu-id="e0710-109">Create custom fields and option sets in the pricing dimension solution</span></span>

<span data-ttu-id="e0710-110">Hinnoitteludimensio voi olla asetusjoukko tai entiteetti.</span><span class="sxs-lookup"><span data-stu-id="e0710-110">A pricing dimension can be an option set or an entity.</span></span> <span data-ttu-id="e0710-111">Molemmat on luotava hinnoitteluratkaisussa.</span><span class="sxs-lookup"><span data-stu-id="e0710-111">Both must be created in your pricing solution.</span></span> <span data-ttu-id="e0710-112">Tämän toimintosarjojen vaiheissa selitetään, miten luodaan entiteettiperusteisia dimensioita ja asetusjoukkoperusteisia dimensioita.</span><span class="sxs-lookup"><span data-stu-id="e0710-112">The steps in this procedure explain how to create entity-based dimensions and option set-based dimensions.</span></span>

### <a name="entity-based-dimensions"></a><span data-ttu-id="e0710-113">Entiteettiperusteiset dimensiot</span><span class="sxs-lookup"><span data-stu-id="e0710-113">Entity-based dimensions</span></span>

1. <span data-ttu-id="e0710-114">Valitse PSA:ssa **Asetukset** > **Ratkaisut** ja kaksoisnapsauta **\<your organization name> hinnoitteludimensiot**.</span><span class="sxs-lookup"><span data-stu-id="e0710-114">In PSA, click **Settings** > **Solutions** , and then double-click **\<your organization name> pricing dimensions**.</span></span>
2. <span data-ttu-id="e0710-115">Valitse vasemman siirtymisruudun Ratkaisunhallinnassa **Entiteetit**.</span><span class="sxs-lookup"><span data-stu-id="e0710-115">In Solution Explorer, on the left navigation pane, select **Entities**.</span></span>
3. <span data-ttu-id="e0710-116">Napsauta **Uusi** , jos haluat luoda uuden entiteetin nimellä **Vakio-otsikko**.</span><span class="sxs-lookup"><span data-stu-id="e0710-116">Click **New** to create a new entity called **Standard Title**.</span></span> <span data-ttu-id="e0710-117">Syötä muut tarvittavat tiedot ja napsauta **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="e0710-117">Enter the remaining required information, and then click **Save**.</span></span>

> ![Vakio-otsikko-entiteetin määritys](media/Standard-Title-entity-definition.png)


### <a name="option-set-based-dimensions"></a><span data-ttu-id="e0710-119">Asetusjoukkoperusteiset dimensiot</span><span class="sxs-lookup"><span data-stu-id="e0710-119">Option set-based dimensions</span></span> 
<span data-ttu-id="e0710-120">Voit luoda kaksi asetusjoukkoperusteista dimensiota.</span><span class="sxs-lookup"><span data-stu-id="e0710-120">You can create two option set-based dimensions.</span></span> <span data-ttu-id="e0710-121">Käytä asetusjoukkoa **Resurssin työn sijainti** seurataksesi töiden **Koti** ja **Asiakkaan tiloissa** ja käytä kentän **Resurssin työtunnit** arvoja **Tavallinen työ** ja **Ylityö** hinnankorotuksen perusteena, kun työ on valmis.</span><span class="sxs-lookup"><span data-stu-id="e0710-121">Use **Resource Work Location** to track the price of **Home** location work and **Onsite** work and use **Resource Work hours** with values **Regular** and **Overtime** to apply a markup when work is completed.</span></span>


1. <span data-ttu-id="e0710-122">Valitse PSA:ssa **Asetukset** > **Ratkaisut** ja kaksoisnapsauta **\<your organization name> hinnoitteludimensioita**.</span><span class="sxs-lookup"><span data-stu-id="e0710-122">In PSA, click **Settings** > **Solutions** , and then double-click  **\<your organization name> pricing dimensions**.</span></span> 
2. <span data-ttu-id="e0710-123">Valitse vasemman siirtymisruudun Ratkaisunhallinnassa **Asetusjoukot**.</span><span class="sxs-lookup"><span data-stu-id="e0710-123">In Solution Explorer, on the left navigation pane, select  **Option Sets**.</span></span> 
3. <span data-ttu-id="e0710-124">Napsauta **Uusi** luodaksesi uuden asetusjoukon, syötä muut tarvittavat tiedot ja napsauta **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="e0710-124">Click **New** to create a new option set, enter the remaining required information, and then click **Save**.</span></span>

> ![<span data-ttu-id="e0710-125">Asetusjoukkoperusteinen hinnoitteludimensio nimeltään Resurssin työn sijainti</span><span class="sxs-lookup"><span data-stu-id="e0710-125">Option set based pricing dimension called Resource Work Location</span></span> ](media/Option-set-PD-called-Resource-Work-Location.png)

> ![<span data-ttu-id="e0710-126">Asetusjoukkoperusteinen hinnoitteludimensio nimeltään Resurssin työntunnit</span><span class="sxs-lookup"><span data-stu-id="e0710-126">Option set based pricing dimension called Resource Work Hours</span></span> ](media/Option-set-PD-called-Resource-Work-Hours.PNG)


## <a name="create-data-for-entity-based-dimensions"></a><span data-ttu-id="e0710-127">Tietojen luominen entiteettiperusteisia dimensioita varten</span><span class="sxs-lookup"><span data-stu-id="e0710-127">Create data for entity-based dimensions</span></span>

<span data-ttu-id="e0710-128">Voit luoda tietoja entiteettiperusteisille dimensioille manuaalisesti tai käyttämällä Microsoft Excelin tuontia tai palvelukutsuja.</span><span class="sxs-lookup"><span data-stu-id="e0710-128">You can create data for entity-based dimensions manually, or by using Microsoft Excel import or service calls.</span></span> <span data-ttu-id="e0710-129">Luo tämän toimintosarjan vaiheiden avulla kaksi vakionimekettä eli **Järjestelmäinsinööri** ja **Vanhempi järjestelmäinsinööri** entiteettiperusteisen dimension **Vakionimike** perusteella.</span><span class="sxs-lookup"><span data-stu-id="e0710-129">Use the steps in this procedure to create two standard titles, **Systems Engineer** and **Senior Systems Engineer** from the entity-based dimension, **Standard Title**.</span></span> <span data-ttu-id="e0710-130">Jos haluamasi tietomäärä on vähäinen, kuten seuraavassa esimerkissä, voit käyttää vakiolomaketta.</span><span class="sxs-lookup"><span data-stu-id="e0710-130">If the data that you want to create is small, as in the following example, you can use a standard form.</span></span>

1. <span data-ttu-id="e0710-131">Napsauta PSA:ssa **Erikoishaku**.</span><span class="sxs-lookup"><span data-stu-id="e0710-131">In PSA, click **Advanced Find**.</span></span> <span data-ttu-id="e0710-132">Valitse entiteetti **Vakionimike** ja napsauta sitten **Tulokset**.</span><span class="sxs-lookup"><span data-stu-id="e0710-132">Select the entity **Standard Title** and then click **Results**.</span></span> <span data-ttu-id="e0710-133">Näkyviin tulevat kaikki **Vakionimike** -entiteetin rivit.</span><span class="sxs-lookup"><span data-stu-id="e0710-133">All of the rows in the **Standard Title** entity will be shown.</span></span>
2. <span data-ttu-id="e0710-134">Valitse **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="e0710-134">Click **New**.</span></span> <span data-ttu-id="e0710-135">Syötä **Nimi** -kenttään "Järjestelmäinsinööri" ja napsauta **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="e0710-135">In the **Name** field, enter "Systems Engineer" and then click **Save**.</span></span>
3. <span data-ttu-id="e0710-136">Sulje lomake.</span><span class="sxs-lookup"><span data-stu-id="e0710-136">Close the form.</span></span> 
4. <span data-ttu-id="e0710-137">Luo toinen vakionimike Vanhemmalle järjestelmäinsinöörille toistamalla vaiheet 1–3.</span><span class="sxs-lookup"><span data-stu-id="e0710-137">Repeat steps 1 - 3 to create another standard title for "Senior Systems Engineer".</span></span>

> ![<span data-ttu-id="e0710-138">Esimerkkitietoja Vakionimike-entiteetille</span><span class="sxs-lookup"><span data-stu-id="e0710-138">Sample Data for Standard Title entity</span></span> ](media/ST-data.png)

