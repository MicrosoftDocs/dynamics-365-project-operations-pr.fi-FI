---
title: Mukautettujen kenttien ja entiteettien luominen
description: Tässä aiheessa selitetään, miten Power Apps-ympäristön omassa ratkaisussasi luodaan asetusjoukkoja ja entiteettejä.
author: Rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 11/26/2018
ms.topic: article
ms.prod: Project Service
ms.service: business-applications
ms.assetid: fb160bfd-e037-4a21-a968-3ff2e6e16481
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
ms.openlocfilehash: 7ee30e3bb6b8034ef226e2e9181195685355011f
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/24/2020
ms.locfileid: "3751240"
---
# <a name="create-custom-fields-and-entities"></a><span data-ttu-id="d682d-103">Mukautettujen kenttien ja entiteettien luominen</span><span class="sxs-lookup"><span data-stu-id="d682d-103">Create custom fields and entities</span></span> 

<span data-ttu-id="d682d-104">Toimi seuraavasti aina, kun haluat luoda mukautetun asetusjoukon tai entiteetin Power Apps-ympäristössä.</span><span class="sxs-lookup"><span data-stu-id="d682d-104">Complete the following steps any time that you want to create a custom option set or entity on the Power Apps platform.</span></span>  
<span data-ttu-id="d682d-105">Tämän aiheen toimintojoukot on tarkoitus suorittaa Project Service Automationin (PSA) verkkoliittymän avulla.</span><span class="sxs-lookup"><span data-stu-id="d682d-105">The procedures in this topic should be completed using the web interface of Project Service Automation (PSA).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="d682d-106">Suosittelemme kaikkien mukautettujen hinnoitteludimensioiden muutokset erillisessä ratkaisussa.</span><span class="sxs-lookup"><span data-stu-id="d682d-106">We recommend that you make all custom pricing dimension changes in a separate solution.</span></span> <span data-ttu-id="d682d-107">Tämä tärkeä paras käytäntö varmistaa, että muutoksia voidaan myöhemmin päivittää tai poistaa tarpeen mukaan, auttaa työn uudelleenkäytössä ja helpottaa näiden muutosten siirtämistä toiseen esiintymään.</span><span class="sxs-lookup"><span data-stu-id="d682d-107">This important best practice provides flexibility in the future to update or remove changes as needed, will help with re-use of your work, and makes it easier to port these changes to another instance.</span></span> <span data-ttu-id="d682d-108">Kun olet tehnyt kaikki tarvittavat muutokset, vie tämä ratkaisu muodossa **Hallittu ratkaisu** ja tuo se muihin esiintymiin, jotta voit käyttää hinnoittelumäärityksiäsi uudelleen.</span><span class="sxs-lookup"><span data-stu-id="d682d-108">After you have made all of the required changes, export this solution as a **Managed solution** and import it into other instances to reuse your pricing setup.</span></span>


## <a name="create-a-custom-solution-for-pricing-dimensions"></a><span data-ttu-id="d682d-109">Mukautetun ratkaisun luominen hinnoitteludimensioille</span><span class="sxs-lookup"><span data-stu-id="d682d-109">Create a custom solution for pricing dimensions</span></span>
1. <span data-ttu-id="d682d-110">Napsauta PSA:ssa **Asetukset** > **Ratkaisut** ja luo sitten uusi ratkaisu napsauttamalla **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="d682d-110">In PSA, click **Settings** > **Solutions**, and then click **New** to create a new solution.</span></span> 
2. <span data-ttu-id="d682d-111">Anna ratkaisulle nimeksi **\<organisaatiosi nimi > hinnoitteludimensiot**, anna muut tarvittavat tiedot ja napsauta **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="d682d-111">Name the solution, **\<your organization name> pricing dimensions**, enter the remaining required information, and then click **Save**.</span></span>

> ![Mukautetun ratkaisun luominen hinnoitteludimensioille](media/Creation-of-custom-pricing-dimension-solution.PNG)
  
## <a name="create-custom-fields-and-option-sets-in-the-pricing-dimension-solution"></a><span data-ttu-id="d682d-113">Mukautettujen kenttien ja asetusjoukkojen luominen hinnoitteludimensioratkaisussa</span><span class="sxs-lookup"><span data-stu-id="d682d-113">Create custom fields and option sets in the pricing dimension solution</span></span>

<span data-ttu-id="d682d-114">Hinnoitteludimensio voi olla asetusjoukko tai entiteetti.</span><span class="sxs-lookup"><span data-stu-id="d682d-114">A pricing dimension can be an option set or an entity.</span></span> <span data-ttu-id="d682d-115">Molemmat on luotava hinnoitteluratkaisussa.</span><span class="sxs-lookup"><span data-stu-id="d682d-115">Both must be created in your pricing solution.</span></span> <span data-ttu-id="d682d-116">Tämän toimintosarjojen vaiheissa selitetään, miten luodaan entiteettiperusteisia dimensioita ja asetusjoukkoperusteisia dimensioita.</span><span class="sxs-lookup"><span data-stu-id="d682d-116">The steps in this procedure explain how to create entity-based dimensions and option set-based dimensions.</span></span>

### <a name="entity-based-dimensions"></a><span data-ttu-id="d682d-117">Entiteettiperusteiset dimensiot</span><span class="sxs-lookup"><span data-stu-id="d682d-117">Entity-based dimensions</span></span>

1. <span data-ttu-id="d682d-118">Napsauta PSA:ssa **Asetukset** > **Ratkaisut** kaksoisnapsauta sitten **\<organisaatiosi nimi>: hinnoitteludimensiot**.</span><span class="sxs-lookup"><span data-stu-id="d682d-118">In PSA, click **Settings** > **Solutions**, and then double-click **\<your organization name> pricing dimensions**.</span></span>
2. <span data-ttu-id="d682d-119">Valitse vasemman siirtymisruudun Ratkaisunhallinnassa **Entiteetit**.</span><span class="sxs-lookup"><span data-stu-id="d682d-119">In Solution Explorer, on the left navigation pane, select **Entities**.</span></span>
3. <span data-ttu-id="d682d-120">Napsauta **Uusi**, jos haluat luoda uuden entiteetin nimellä **Vakio-otsikko**.</span><span class="sxs-lookup"><span data-stu-id="d682d-120">Click **New** to create a new entity called **Standard Title**.</span></span> <span data-ttu-id="d682d-121">Syötä muut tarvittavat tiedot ja napsauta **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="d682d-121">Enter the remaining required information, and then click **Save**.</span></span>

> ![Vakio-otsikko-entiteetin määritys](media/Standard-Title-entity-definition.png)


### <a name="option-set-based-dimensions"></a><span data-ttu-id="d682d-123">Asetusjoukkoperusteiset dimensiot</span><span class="sxs-lookup"><span data-stu-id="d682d-123">Option set-based dimensions</span></span> 
<span data-ttu-id="d682d-124">Voit luoda kaksi asetusjoukkoperusteista dimensiota.</span><span class="sxs-lookup"><span data-stu-id="d682d-124">You can create two option set-based dimensions.</span></span> <span data-ttu-id="d682d-125">Käytä asetusjoukkoa **Resurssin työn sijainti** seurataksesi töiden **Koti** ja **Asiakkaan tiloissa** ja käytä kentän **Resurssin työtunnit** arvoja **Tavallinen työ** ja **Ylityö** hinnankorotuksen perusteena, kun työ on valmis.</span><span class="sxs-lookup"><span data-stu-id="d682d-125">Use **Resource Work Location** to track the price of **Home** location work and **Onsite** work and use **Resource Work hours** with values **Regular** and **Overtime** to apply a markup when work is completed.</span></span>


1. <span data-ttu-id="d682d-126">Napsauta PSA:ssa **Asetukset** > **Ratkaisut** ja kaksoisnapsauta sitten **\<organisaatiosi nimi>: hinnoitteludimensiot**.</span><span class="sxs-lookup"><span data-stu-id="d682d-126">In PSA, click **Settings** > **Solutions**, and then double-click  **\<your organization name> pricing dimensions**.</span></span> 
2. <span data-ttu-id="d682d-127">Valitse vasemman siirtymisruudun Ratkaisunhallinnassa **Asetusjoukot**.</span><span class="sxs-lookup"><span data-stu-id="d682d-127">In Solution Explorer, on the left navigation pane, select  **Option Sets**.</span></span> 
3. <span data-ttu-id="d682d-128">Napsauta **Uusi** luodaksesi uuden asetusjoukon, syötä muut tarvittavat tiedot ja napsauta **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="d682d-128">Click **New** to create a new option set, enter the remaining required information, and then click **Save**.</span></span>

> ![<span data-ttu-id="d682d-129">Asetusjoukkoperusteinen hinnoitteludimensio nimeltään Resurssin työn sijainti</span><span class="sxs-lookup"><span data-stu-id="d682d-129">Option set based pricing dimension called Resource Work Location</span></span> ](media/Option-set-PD-called-Resource-Work-Location.png)

> ![<span data-ttu-id="d682d-130">Asetusjoukkoperusteinen hinnoitteludimensio nimeltään Resurssin työntunnit</span><span class="sxs-lookup"><span data-stu-id="d682d-130">Option set based pricing dimension called Resource Work Hours</span></span> ](media/Option-set-PD-called-Resource-Work-Hours.PNG)


## <a name="create-data-for-entity-based-dimensions"></a><span data-ttu-id="d682d-131">Tietojen luominen entiteettiperusteisia dimensioita varten</span><span class="sxs-lookup"><span data-stu-id="d682d-131">Create data for entity-based dimensions</span></span>

<span data-ttu-id="d682d-132">Voit luoda tietoja entiteettiperusteisille dimensioille manuaalisesti tai käyttämällä Microsoft Excelin tuontia tai palvelukutsuja.</span><span class="sxs-lookup"><span data-stu-id="d682d-132">You can create data for entity-based dimensions manually, or by using Microsoft Excel import or service calls.</span></span> <span data-ttu-id="d682d-133">Luo tämän toimintosarjan vaiheiden avulla kaksi vakionimekettä eli **Järjestelmäinsinööri** ja **Vanhempi järjestelmäinsinööri** entiteettiperusteisen dimension **Vakionimike** perusteella.</span><span class="sxs-lookup"><span data-stu-id="d682d-133">Use the steps in this procedure to create two standard titles, **Systems Engineer** and **Senior Systems Engineer** from the entity-based dimension, **Standard Title**.</span></span> <span data-ttu-id="d682d-134">Jos haluamasi tietomäärä on vähäinen, kuten seuraavassa esimerkissä, voit käyttää vakiolomaketta.</span><span class="sxs-lookup"><span data-stu-id="d682d-134">If the data that you want to create is small, as in the following example, you can use a standard form.</span></span>

1. <span data-ttu-id="d682d-135">Napsauta PSA:ssa **Erikoishaku**.</span><span class="sxs-lookup"><span data-stu-id="d682d-135">In PSA, click **Advanced Find**.</span></span> <span data-ttu-id="d682d-136">Valitse entiteetti **Vakionimike** ja napsauta sitten **Tulokset**.</span><span class="sxs-lookup"><span data-stu-id="d682d-136">Select the entity **Standard Title** and then click **Results**.</span></span> <span data-ttu-id="d682d-137">Näkyviin tulevat kaikki **Vakionimike**-entiteetin rivit.</span><span class="sxs-lookup"><span data-stu-id="d682d-137">All of the rows in the **Standard Title** entity will be shown.</span></span>
2. <span data-ttu-id="d682d-138">Valitse **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="d682d-138">Click **New**.</span></span> <span data-ttu-id="d682d-139">Syötä **Nimi**-kenttään "Järjestelmäinsinööri" ja napsauta **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="d682d-139">In the **Name** field, enter "Systems Engineer" and then click **Save**.</span></span>
3. <span data-ttu-id="d682d-140">Sulje lomake.</span><span class="sxs-lookup"><span data-stu-id="d682d-140">Close the form.</span></span> 
4. <span data-ttu-id="d682d-141">Luo toinen vakionimike Vanhemmalle järjestelmäinsinöörille toistamalla vaiheet 1–3.</span><span class="sxs-lookup"><span data-stu-id="d682d-141">Repeat steps 1 - 3 to create another standard title for "Senior Systems Engineer".</span></span>

> ![<span data-ttu-id="d682d-142">Esimerkkitietoja Vakionimike-entiteetille</span><span class="sxs-lookup"><span data-stu-id="d682d-142">Sample Data for Standard Title entity</span></span> ](media/ST-data.png)

## <a name="add-all-required-psa-entities-and-related-components-to-the-pricing-dimension-solution"></a><span data-ttu-id="d682d-143">Kaikkien tarvittavien PSA-entiteettien ja niihin liittyvien komponenttien lisääminen hinnoitteludimensioratkaisuun</span><span class="sxs-lookup"><span data-stu-id="d682d-143">Add all required PSA entities and related components to the Pricing Dimension Solution</span></span>
<span data-ttu-id="d682d-144">Sinun on lisättävä seuraavat Project Service -entiteetit hinnoitteluratkaisuusi.</span><span class="sxs-lookup"><span data-stu-id="d682d-144">You will need to add the following Project Service entities to your pricing solution.</span></span> <span data-ttu-id="d682d-145">Tee tämän toimintosarjan vaiheiden avulla tärkeitä rakennemuutoksia hinnoitteluratkaisuun, jotta entiteetit ottavat uudet hinnoitteludimensiot huomioon.</span><span class="sxs-lookup"><span data-stu-id="d682d-145">Use the steps in this procedure to make some important schema changes in the pricing solution so that the entities become aware of the new pricing dimensions.</span></span>

1. <span data-ttu-id="d682d-146">Napsauta PSA:ssa **Asetukset** > **Ratkaisut** kaksoisnapsauta sitten **\<organisaatiosi nimi>: hinnoitteludimensiot**.</span><span class="sxs-lookup"><span data-stu-id="d682d-146">In PSA, click **Settings** > **Solutions**, and then double-click **\<your organization name> pricing dimensions**.</span></span> 
2. <span data-ttu-id="d682d-147">Valitse vasemman siirtymisruudun Ratkaisunhallinnassa **Lisää aiemmin luoto** > **Entiteetit**.</span><span class="sxs-lookup"><span data-stu-id="d682d-147">In Solution Explorer, on the left navigation pane, select **Add Existing** > **Entities**.</span></span>
3. <span data-ttu-id="d682d-148">Valitse **Ratkaisun osat** -valintaikkunassa seuraavat entiteetit:</span><span class="sxs-lookup"><span data-stu-id="d682d-148">In the **Solution Components** dialog box, select the following entities:</span></span>

- <span data-ttu-id="d682d-149">Todellinen</span><span class="sxs-lookup"><span data-stu-id="d682d-149">Actual</span></span>
- <span data-ttu-id="d682d-150">Varattava resurssi</span><span class="sxs-lookup"><span data-stu-id="d682d-150">Bookable Resource</span></span>
- <span data-ttu-id="d682d-151">Arviorivi</span><span class="sxs-lookup"><span data-stu-id="d682d-151">Estimate Line</span></span>
- <span data-ttu-id="d682d-152">Laskurivin tiedot</span><span class="sxs-lookup"><span data-stu-id="d682d-152">Invoice Line Detail</span></span>
- <span data-ttu-id="d682d-153">Kirjauskansion rivi</span><span class="sxs-lookup"><span data-stu-id="d682d-153">Journal Line</span></span>
- <span data-ttu-id="d682d-154">Projektin sopimusrivin tiedot</span><span class="sxs-lookup"><span data-stu-id="d682d-154">Project Contract Line Detail</span></span>
- <span data-ttu-id="d682d-155">Projektiryhmän jäsen</span><span class="sxs-lookup"><span data-stu-id="d682d-155">Project Team Member</span></span>
- <span data-ttu-id="d682d-156">Tarjousrivin tiedot</span><span class="sxs-lookup"><span data-stu-id="d682d-156">Quote Line Detail</span></span>
- <span data-ttu-id="d682d-157">Roolin hinnankorotus</span><span class="sxs-lookup"><span data-stu-id="d682d-157">Role Price Markup</span></span>
- <span data-ttu-id="d682d-158">Roolin hinta</span><span class="sxs-lookup"><span data-stu-id="d682d-158">Role Price</span></span> 
- <span data-ttu-id="d682d-159">Aikamerkintä</span><span class="sxs-lookup"><span data-stu-id="d682d-159">Time Entry</span></span> 

> ![Aiemmin luotujen entiteettien lisääminen hinnoitteludimensioratkaisuun](media/Existing-entities-to-PD-solution.png)

> ![Valitse ratkaisun osat](media/Dimension-Components.png)

> [!NOTE]
> <span data-ttu-id="d682d-162">Varmista, että lisäät kaikkien valittujen entiteettien kaikki lomakkeet ja näkymät.</span><span class="sxs-lookup"><span data-stu-id="d682d-162">Make sure to include all forms and views for each of the entities selected.</span></span>

4. <span data-ttu-id="d682d-163">Kun sinua pyydetään lisäämään yllä valituista entiteeteistä riippuvaisia entiteettejä, valitse **Ei**.</span><span class="sxs-lookup"><span data-stu-id="d682d-163">When prompted to include any dependent entities for the entities selected above, click **No**.</span></span>

> ![Älä lisää kaikkia liittyviä komponentteja.](media/Do-not-include-required.png)


