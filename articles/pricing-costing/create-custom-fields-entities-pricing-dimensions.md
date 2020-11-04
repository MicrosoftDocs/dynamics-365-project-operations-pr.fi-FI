---
title: Mukautettujen kenttien ja entiteettien luominen hinnoitteludimensioina
description: Tässä aiheessa on tietoja mukautetun asetusjoukon tai mukautettujen entiteettien luomisesta.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 9dd43be79f8e906298578911b3bff03e66c2f1e5
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/16/2020
ms.locfileid: "4075386"
---
# <a name="create-custom-fields-and-entities-as-pricing-dimensions"></a><span data-ttu-id="063fb-103">Mukautettujen kenttien ja entiteettien luominen hinnoitteludimensioina</span><span class="sxs-lookup"><span data-stu-id="063fb-103">Create custom fields and entities as pricing dimensions</span></span>

<span data-ttu-id="063fb-104">_**Koskee:** Project Operationsin resurssiin / muuhun kuin resurssiin perustuvia skenaarioita, Lite-käyttöönotto-kaupasta proformalaskutukseen_</span><span class="sxs-lookup"><span data-stu-id="063fb-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="063fb-105">Toimi seuraavasti aina, kun haluat luoda mukautetun asetusjoukon tai entiteetin.</span><span class="sxs-lookup"><span data-stu-id="063fb-105">Complete the following steps any time that you want to create a custom option set or entity.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="063fb-106">Suosittelemme kaikkien mukautettujen hinnoitteludimensioiden muutokset erillisessä ratkaisussa.</span><span class="sxs-lookup"><span data-stu-id="063fb-106">We recommend that you make all custom pricing dimension changes in a separate solution.</span></span> <span data-ttu-id="063fb-107">Tämä tärkeä paras käytäntö varmistaa, että muutoksia voidaan myöhemmin päivittää tai poistaa tarpeen mukaan, auttaa työn uudelleenkäytössä ja helpottaa näiden muutosten siirtämistä toiseen esiintymään.</span><span class="sxs-lookup"><span data-stu-id="063fb-107">This important best practice provides flexibility in the future to update or remove changes as needed, will help with re-use of your work, and makes it easier to port these changes to another instance.</span></span> <span data-ttu-id="063fb-108">Kun olet tehnyt kaikki tarvittavat muutokset, vie tämä ratkaisu muodossa **Hallittu ratkaisu** ja tuo se muihin esiintymiin, jotta voit käyttää hinnoittelumäärityksiäsi uudelleen.</span><span class="sxs-lookup"><span data-stu-id="063fb-108">After you have made all of the required changes, export this solution as a **Managed solution** and import it into other instances to reuse your pricing setup.</span></span>


## <a name="create-a-custom-solution-for-pricing-dimensions"></a><span data-ttu-id="063fb-109">Mukautetun ratkaisun luominen hinnoitteludimensioille</span><span class="sxs-lookup"><span data-stu-id="063fb-109">Create a custom solution for pricing dimensions</span></span>
1. <span data-ttu-id="063fb-110">Siirry kohtaan **Asetukset** > **Ratkaisut** ja luo uusi ratkaisu valitsemalla **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="063fb-110">Go to **Settings** > **Solutions** , and then select **New** to create a new solution.</span></span> 
2. <span data-ttu-id="063fb-111">Anna ratkaisulle nimeksi **organisaation \<your organization name> hinnoitteludimensiot** , anna muut tarvittavat tiedot ja valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="063fb-111">Name the solution, **\<your organization name> pricing dimensions** , enter the remaining required information, and then select **Save**.</span></span>
  
## <a name="create-custom-fields-and-option-sets-in-the-pricing-dimension-solution"></a><span data-ttu-id="063fb-112">Mukautettujen kenttien ja asetusjoukkojen luominen hinnoitteludimensioratkaisussa</span><span class="sxs-lookup"><span data-stu-id="063fb-112">Create custom fields and option sets in the pricing dimension solution</span></span>

<span data-ttu-id="063fb-113">Hinnoitteludimensio voi olla asetusjoukko tai entiteetti.</span><span class="sxs-lookup"><span data-stu-id="063fb-113">A pricing dimension can be an option set or an entity.</span></span> <span data-ttu-id="063fb-114">Molemmat on luotava hinnoitteluratkaisussa.</span><span class="sxs-lookup"><span data-stu-id="063fb-114">Both must be created in your pricing solution.</span></span> <span data-ttu-id="063fb-115">Tämän toimintosarjojen vaiheissa selitetään, miten luodaan entiteettiperusteisia dimensioita ja asetusjoukkoperusteisia dimensioita.</span><span class="sxs-lookup"><span data-stu-id="063fb-115">The steps in this procedure explain how to create entity-based dimensions and option set-based dimensions.</span></span>

### <a name="entity-based-dimensions"></a><span data-ttu-id="063fb-116">Entiteettiperusteiset dimensiot</span><span class="sxs-lookup"><span data-stu-id="063fb-116">Entity-based dimensions</span></span>

1. <span data-ttu-id="063fb-117">Siirry kohtaan **Asetukset** > **Ratkaisut** ja kaksoisnapsauta **organisaation \<your organization name> hinnoitteludimensio** -kohtaa.</span><span class="sxs-lookup"><span data-stu-id="063fb-117">Go to **Settings** > **Solutions** , and then double-click **\<your organization name> pricing dimensions**.</span></span>
2. <span data-ttu-id="063fb-118">Valitse vasemman siirtymisruudun Ratkaisunhallinnassa **Entiteetit**.</span><span class="sxs-lookup"><span data-stu-id="063fb-118">In Solution Explorer, on the left navigation pane, select **Entities**.</span></span>
3. <span data-ttu-id="063fb-119">Valitse **Uusi** , jos haluat luoda uuden entiteetin nimellä **Vakio-otsikko**.</span><span class="sxs-lookup"><span data-stu-id="063fb-119">Select **New** to create a new entity called **Standard Title**.</span></span> 
4. <span data-ttu-id="063fb-120">Syötä muut tarvittavat tiedot ja valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="063fb-120">Enter the remaining required information, and then select **Save**.</span></span>


### <a name="option-set-based-dimensions"></a><span data-ttu-id="063fb-121">Asetusjoukkoperusteiset dimensiot</span><span class="sxs-lookup"><span data-stu-id="063fb-121">Option set-based dimensions</span></span> 
<span data-ttu-id="063fb-122">Voit luoda kaksi asetusjoukkoperusteista dimensiota.</span><span class="sxs-lookup"><span data-stu-id="063fb-122">You can create two option set-based dimensions.</span></span> <span data-ttu-id="063fb-123">Käytä asetusjoukkoa **Resurssin työn sijainti** seurataksesi töiden **Koti** ja **Asiakkaan tiloissa** ja käytä kentän **Resurssin työtunnit** arvoja **Tavallinen työ** ja **Ylityö** hinnankorotuksen perusteena, kun työ on valmis.</span><span class="sxs-lookup"><span data-stu-id="063fb-123">Use **Resource Work Location** to track the price of **Home** location work and **Onsite** work and use **Resource Work hours** with values **Regular** and **Overtime** to apply a markup when work is completed.</span></span>


1. <span data-ttu-id="063fb-124">Siirry kohtaan **Asetukset** > **Ratkaisut** ja kaksoisnapsauta **organisaation \<your organization name> hinnoitteludimensio** -kohtaa.</span><span class="sxs-lookup"><span data-stu-id="063fb-124">Go to **Settings** > **Solutions** , and double-click  **\<your organization name> pricing dimensions**.</span></span> 
2. <span data-ttu-id="063fb-125">Valitse vasemman siirtymisruudun Ratkaisunhallinnassa **Asetusjoukot**.</span><span class="sxs-lookup"><span data-stu-id="063fb-125">In Solution Explorer, on the left navigation pane, select  **Option Sets**.</span></span> 
3. <span data-ttu-id="063fb-126">Valitse **Uusi** luodaksesi uuden asetusjoukon. Syötä muut tarvittavat tiedot ja valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="063fb-126">Select **New** to create a new option set, enter the remaining required information, and then select **Save**.</span></span>

## <a name="create-data-for-entity-based-dimensions"></a><span data-ttu-id="063fb-127">Tietojen luominen entiteettiperusteisia dimensioita varten</span><span class="sxs-lookup"><span data-stu-id="063fb-127">Create data for entity-based dimensions</span></span>

<span data-ttu-id="063fb-128">Voit luoda tietoja entiteettiperusteisille dimensioille manuaalisesti tai käyttämällä Microsoft Excelin tuontia tai palvelukutsuja.</span><span class="sxs-lookup"><span data-stu-id="063fb-128">You can create data for entity-based dimensions manually, or by using Microsoft Excel import or service calls.</span></span> <span data-ttu-id="063fb-129">Luo tämän toimintosarjan vaiheiden avulla kaksi vakionimekettä eli **Järjestelmäinsinööri** ja **Vanhempi järjestelmäinsinööri** entiteettiperusteisen dimension **Vakionimike** perusteella.</span><span class="sxs-lookup"><span data-stu-id="063fb-129">Use the steps in this procedure to create two standard titles, **Systems Engineer** and **Senior Systems Engineer** from the entity-based dimension, **Standard Title**.</span></span> <span data-ttu-id="063fb-130">Jos haluamasi tietomäärä on vähäinen, kuten seuraavassa esimerkissä, voit käyttää vakiolomaketta.</span><span class="sxs-lookup"><span data-stu-id="063fb-130">If the data that you want to create is small, as in the following example, you can use a standard form.</span></span>

1. <span data-ttu-id="063fb-131">Valitse **Erikoishaku** , valitse entiteetin **Vakio-otsikko** ja valitse sitten **Tulokset**.</span><span class="sxs-lookup"><span data-stu-id="063fb-131">Select **Advanced Find** , select the entity **Standard Title** , and then select **Results**.</span></span> <span data-ttu-id="063fb-132">Näkyviin tulevat kaikki **Vakionimike** -entiteetin rivit.</span><span class="sxs-lookup"><span data-stu-id="063fb-132">All of the rows in the **Standard Title** entity will be shown.</span></span>
2. <span data-ttu-id="063fb-133">Valitse **Uusi** ja syötä **Nimi** -kenttään Järjestelmäinsinööri. Valitse sitten **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="063fb-133">Select **New** , and in the **Name** field, enter "Systems Engineer" and then select **Save**.</span></span>
3. <span data-ttu-id="063fb-134">Sulje lomake.</span><span class="sxs-lookup"><span data-stu-id="063fb-134">Close the form.</span></span> 
4. <span data-ttu-id="063fb-135">Luo toinen vakionimike Vanhemmalle järjestelmäinsinöörille toistamalla vaiheet 1–3.</span><span class="sxs-lookup"><span data-stu-id="063fb-135">Repeat steps 1 - 3 to create another standard title for "Senior Systems Engineer".</span></span>

## <a name="add-all-required-entities-and-related-components-to-the-pricing-dimension-solution"></a><span data-ttu-id="063fb-136">Kaikkien tarvittavien entiteettien ja niihin liittyvien komponenttien lisääminen hinnoitteludimensioratkaisuun</span><span class="sxs-lookup"><span data-stu-id="063fb-136">Add all required entities and related components to the Pricing Dimension Solution</span></span>
<span data-ttu-id="063fb-137">Sinun on lisättävä seuraavat entiteetit hinnoitteluratkaisuusi.</span><span class="sxs-lookup"><span data-stu-id="063fb-137">You will need to add the following entities to your pricing solution.</span></span> <span data-ttu-id="063fb-138">Tee tämän toimintosarjan vaiheiden avulla tärkeitä rakennemuutoksia hinnoitteluratkaisuun, jotta entiteetit ottavat uudet hinnoitteludimensiot huomioon.</span><span class="sxs-lookup"><span data-stu-id="063fb-138">Use the steps in this procedure to make some important schema changes in the pricing solution so that the entities become aware of the new pricing dimensions.</span></span>

1. <span data-ttu-id="063fb-139">Valitse **Asetukset** > **Ratkaisut** ja kaksoisnapsauta **organisaation \<your organization name> hinnoitteludimensio** -kohtaa.</span><span class="sxs-lookup"><span data-stu-id="063fb-139">Select **Settings** > **Solutions** , and double-click **\<your organization name> pricing dimensions**.</span></span> 
2. <span data-ttu-id="063fb-140">Valitse vasemman siirtymisruudun Ratkaisunhallinnassa **Lisää aiemmin luoto** > **Entiteetit**.</span><span class="sxs-lookup"><span data-stu-id="063fb-140">In Solution Explorer, on the left navigation pane, select **Add Existing** > **Entities**.</span></span>
3. <span data-ttu-id="063fb-141">Valitse **Ratkaisun osat** -valintaikkunassa seuraavat entiteetit:</span><span class="sxs-lookup"><span data-stu-id="063fb-141">In the **Solution Components** dialog box, select the following entities:</span></span>

  - <span data-ttu-id="063fb-142">Todellinen</span><span class="sxs-lookup"><span data-stu-id="063fb-142">Actual</span></span>
  - <span data-ttu-id="063fb-143">Varattava resurssi</span><span class="sxs-lookup"><span data-stu-id="063fb-143">Bookable Resource</span></span>
  - <span data-ttu-id="063fb-144">Arviorivi</span><span class="sxs-lookup"><span data-stu-id="063fb-144">Estimate Line</span></span>
  - <span data-ttu-id="063fb-145">Laskurivin tiedot</span><span class="sxs-lookup"><span data-stu-id="063fb-145">Invoice Line Detail</span></span>
  - <span data-ttu-id="063fb-146">Kirjauskansion rivi</span><span class="sxs-lookup"><span data-stu-id="063fb-146">Journal Line</span></span>
  - <span data-ttu-id="063fb-147">Projektin sopimusrivin tiedot</span><span class="sxs-lookup"><span data-stu-id="063fb-147">Project Contract Line Detail</span></span>
  - <span data-ttu-id="063fb-148">Projektiryhmän jäsen</span><span class="sxs-lookup"><span data-stu-id="063fb-148">Project Team Member</span></span>
  - <span data-ttu-id="063fb-149">Tarjousrivin tiedot</span><span class="sxs-lookup"><span data-stu-id="063fb-149">Quote Line Detail</span></span>
  - <span data-ttu-id="063fb-150">Roolin hinnankorotus</span><span class="sxs-lookup"><span data-stu-id="063fb-150">Role Price Markup</span></span>
  - <span data-ttu-id="063fb-151">Roolin hinta</span><span class="sxs-lookup"><span data-stu-id="063fb-151">Role Price</span></span> 
  - <span data-ttu-id="063fb-152">Aikamerkintä</span><span class="sxs-lookup"><span data-stu-id="063fb-152">Time Entry</span></span> 


> [!NOTE]
> <span data-ttu-id="063fb-153">Varmista, että lisäät kaikkien valittujen entiteettien kaikki lomakkeet ja näkymät.</span><span class="sxs-lookup"><span data-stu-id="063fb-153">Make sure to include all forms and views for each of the entities selected.</span></span>

4. <span data-ttu-id="063fb-154">Kun sinua pyydetään lisäämään yllä valituista entiteeteistä riippuvaisia entiteettejä, valitse **Ei**.</span><span class="sxs-lookup"><span data-stu-id="063fb-154">When prompted to include any dependent entities for the entities selected above, select **No**.</span></span>

