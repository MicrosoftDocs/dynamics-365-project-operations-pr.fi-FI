---
title: Mukautettujen kenttien ja entiteettien luominen hinnoitteludimensioina
description: Tässä aiheessa on tietoja mukautetun asetusjoukon tai mukautettujen entiteettien luomisesta.
author: rumant
manager: AnnBe
ms.date: 11/18/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
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
ms.openlocfilehash: 089481cd3e7c0f8f1d1aa880d64cb79e8d677c2d
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5275624"
---
# <a name="create-custom-fields-and-entities-as-pricing-dimensions"></a><span data-ttu-id="8b3a8-103">Mukautettujen kenttien ja entiteettien luominen hinnoitteludimensioina</span><span class="sxs-lookup"><span data-stu-id="8b3a8-103">Create custom fields and entities as pricing dimensions</span></span>

<span data-ttu-id="8b3a8-104">_**Koskee:** Project Operationsin resurssiin / muuhun kuin resurssiin perustuvia skenaarioita, Lite-käyttöönotto-kaupasta proformalaskutukseen_</span><span class="sxs-lookup"><span data-stu-id="8b3a8-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="8b3a8-105">Suorita seuraavat vaiheet, kun haluat luoda mukautetun asetusjoukon tai entiteetin sen käyttämiseksi hinnoitteludimensiona.</span><span class="sxs-lookup"><span data-stu-id="8b3a8-105">Complete the following steps when you want to create a custom option set or entity for using it as a pricing dimension.</span></span> <span data-ttu-id="8b3a8-106">Katso lisätietoja kohdasta [Hinnoitteludimensioiden yleiskatsaus](pricing-dimensions-overview.md).</span><span class="sxs-lookup"><span data-stu-id="8b3a8-106">For more information, see [Pricing dimensions overview](pricing-dimensions-overview.md).</span></span>  

> [!IMPORTANT]
> <span data-ttu-id="8b3a8-107">Suosittelemme kaikkien mukautettujen hinnoitteludimensioiden muutokset erillisessä ratkaisussa.</span><span class="sxs-lookup"><span data-stu-id="8b3a8-107">We recommend that you make all custom pricing dimension changes in a separate solution.</span></span> <span data-ttu-id="8b3a8-108">Tämä tärkeä parhaaksi todettu käytäntö tarjoaa joustavulla tulevaisuudessa tarvittavia päivityksiä ja poistoja varten.</span><span class="sxs-lookup"><span data-stu-id="8b3a8-108">This important best practice provides flexibility in the future to update or remove changes as needed.</span></span> <span data-ttu-id="8b3a8-109">Tämä auttaa myös tehdyn työn uudelleenkäyttämisessä, ja helpottaa näiden muutosten siirrossa toiseen esiintymään. Kun kaikki tarvittavat muutokset on tehty, vie tämä ratkaisu muodossa **Hallittu ratkaisu** ja tuo se toisiin esiintymiin hinnoittelumääritysten uudelleenkäyttöä varten.</span><span class="sxs-lookup"><span data-stu-id="8b3a8-109">This will also help with re-use of your work and make it easier to port these changes to another instance After you have made all of the required changes, export this solution as a **Managed solution** and import it into other instances to reuse your pricing setup.</span></span>

  
## <a name="create-custom-fields-and-option-sets-in-the-pricing-dimension-solution"></a><span data-ttu-id="8b3a8-110">Mukautettujen kenttien ja asetusjoukkojen luominen hinnoitteludimensioratkaisussa</span><span class="sxs-lookup"><span data-stu-id="8b3a8-110">Create custom fields and option sets in the pricing dimension solution</span></span>

<span data-ttu-id="8b3a8-111">Hinnoitteludimensio voi olla asetusjoukko tai entiteetti.</span><span class="sxs-lookup"><span data-stu-id="8b3a8-111">A pricing dimension can be an option set or an entity.</span></span> <span data-ttu-id="8b3a8-112">Molemmat on luotava hinnoitteluratkaisussa.</span><span class="sxs-lookup"><span data-stu-id="8b3a8-112">Both must be created in your pricing solution.</span></span> <span data-ttu-id="8b3a8-113">Tämän toimintosarjojen vaiheissa selitetään, miten luodaan entiteettiperusteisia dimensioita ja asetusjoukkoperusteisia dimensioita.</span><span class="sxs-lookup"><span data-stu-id="8b3a8-113">The steps in this procedure explain how to create entity-based dimensions and option set-based dimensions.</span></span>

### <a name="entity-based-dimensions"></a><span data-ttu-id="8b3a8-114">Entiteettiperusteiset dimensiot</span><span class="sxs-lookup"><span data-stu-id="8b3a8-114">Entity-based dimensions</span></span>
<span data-ttu-id="8b3a8-115">Voit luoda entiteettipohjaisia dimensioita seuraamalla näitä vaiheita:</span><span class="sxs-lookup"><span data-stu-id="8b3a8-115">To create entity-based dimensions, follow these steps:</span></span>

1. <span data-ttu-id="8b3a8-116">Siirry kohtaan **Asetukset** > **Ratkaisut** ja kaksoisnapsauta **organisaation \<your organization name> hinnoitteludimensio** -kohtaa.</span><span class="sxs-lookup"><span data-stu-id="8b3a8-116">Go to **Settings** > **Solutions**, and then double-click **\<your organization name> pricing dimensions**.</span></span>
2. <span data-ttu-id="8b3a8-117">Valitse vasemman siirtymisruudun Ratkaisunhallinnassa **Entiteetit**.</span><span class="sxs-lookup"><span data-stu-id="8b3a8-117">In Solution Explorer, in the left navigation pane, select **Entities**.</span></span>
3. <span data-ttu-id="8b3a8-118">Valitse **Uusi**, jos haluat luoda uuden entiteetin nimellä **Vakio-otsikko**.</span><span class="sxs-lookup"><span data-stu-id="8b3a8-118">Select **New** to create a new entity called **Standard Title**.</span></span> 
4. <span data-ttu-id="8b3a8-119">Syötä muut tarvittavat tiedot ja valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="8b3a8-119">Enter the remaining required information, and then select **Save**.</span></span>

> ![Vakio-otsikko-entiteetin määritys](media/Standard-Title-entity-definition.png)

### <a name="option-set-based-dimensions"></a><span data-ttu-id="8b3a8-121">Asetusjoukkoperusteiset dimensiot</span><span class="sxs-lookup"><span data-stu-id="8b3a8-121">Option set-based dimensions</span></span> 
<span data-ttu-id="8b3a8-122">Voit luoda kaksi asetusjoukkoperusteista dimensiota.</span><span class="sxs-lookup"><span data-stu-id="8b3a8-122">You can create two option set-based dimensions.</span></span> 

- <span data-ttu-id="8b3a8-123">**Resurssien työsijainnin** avulla voit seurata **Koti**-sijainnin työn ja **Asiakkaan tiloissa** tapahtuvan työn hintaa.</span><span class="sxs-lookup"><span data-stu-id="8b3a8-123">Use **Resource Work Location** to track the price of **Home** location work and **Onsite** work.</span></span> 
- <span data-ttu-id="8b3a8-124">Käytä **Resurssin työaikaa** arvoilla **Normaali** ja **Ylityö**, jos haluat korottaa hintaa, kun työ on valmis.</span><span class="sxs-lookup"><span data-stu-id="8b3a8-124">Use **Resource Work hours** with values **Regular** and **Overtime** to apply a markup when the work is complete.</span></span>

<span data-ttu-id="8b3a8-125">Seuraavassa kuvassa on **Resurssin työsijainti** -dimension näkymä.</span><span class="sxs-lookup"><span data-stu-id="8b3a8-125">The following graphic provides a view of the **Resource Work Location** dimension.</span></span> 

> ![Asetusjoukkoperusteinen hinnoitteludimensio nimeltään Resurssin työn sijainti](media/Option-set-PD-called-Resource-Work-Location.png)

<span data-ttu-id="8b3a8-127">Seuraavassa kuvassa on **Resurssin työtunnit** -dimension näkymä.</span><span class="sxs-lookup"><span data-stu-id="8b3a8-127">The following graphic provides a view of the **Resource Work Hours** dimension.</span></span> 

> ![Asetusjoukkoperusteinen hinnoitteludimensio nimeltään Resurssin työntunnit](media/Option-set-PD-called-Resource-Work-Hours.png)

1. <span data-ttu-id="8b3a8-129">Siirry kohtaan **Asetukset** > **Ratkaisut** ja kaksoisnapsauta **organisaation \<your organization name> hinnoitteludimensio** -kohtaa.</span><span class="sxs-lookup"><span data-stu-id="8b3a8-129">Go to **Settings** > **Solutions**, and double-click  **\<your organization name> pricing dimensions**.</span></span> 
2. <span data-ttu-id="8b3a8-130">Valitse vasemman siirtymisruudun Ratkaisunhallinnassa **Asetusjoukot**.</span><span class="sxs-lookup"><span data-stu-id="8b3a8-130">In Solution Explorer, in the left navigation pane, select  **Option Sets**.</span></span> 
3. <span data-ttu-id="8b3a8-131">Valitse **Uusi** luodaksesi uuden asetusjoukon. Syötä muut tarvittavat tiedot ja valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="8b3a8-131">Select **New** to create a new option set, enter the remaining required information, and then select **Save**.</span></span>

## <a name="create-data-for-entity-based-dimensions"></a><span data-ttu-id="8b3a8-132">Tietojen luominen entiteettiperusteisia dimensioita varten</span><span class="sxs-lookup"><span data-stu-id="8b3a8-132">Create data for entity-based dimensions</span></span>

<span data-ttu-id="8b3a8-133">Voit luoda tietoja entiteettiperusteisille dimensioille manuaalisesti tai käyttämällä Microsoft Excelin tuontia tai palvelukutsuja.</span><span class="sxs-lookup"><span data-stu-id="8b3a8-133">You can create data for entity-based dimensions manually, or by using Microsoft Excel import or service calls.</span></span> <span data-ttu-id="8b3a8-134">Luo tämän toimintosarjan vaiheiden avulla kaksi vakionimekettä eli **Järjestelmäinsinööri** ja **Vanhempi järjestelmäinsinööri** entiteettiperusteisen dimension **Vakionimike** perusteella.</span><span class="sxs-lookup"><span data-stu-id="8b3a8-134">Use the steps in this procedure to create two standard titles, **Systems Engineer** and **Senior Systems Engineer** from the entity-based dimension, **Standard Title**.</span></span> <span data-ttu-id="8b3a8-135">Jos haluamasi tietomäärä on vähäinen, kuten seuraavassa esimerkissä, voit käyttää vakiolomaketta.</span><span class="sxs-lookup"><span data-stu-id="8b3a8-135">If the data that you want to create is small, as in the following example, you can use a standard form.</span></span>

1. <span data-ttu-id="8b3a8-136">Valitse **Erikoishaku**.</span><span class="sxs-lookup"><span data-stu-id="8b3a8-136">Select **Advanced Find**.</span></span>
2. <span data-ttu-id="8b3a8-137">Valitse entiteetti **Vakionimike** ja valitse sitten **Tulokset**.</span><span class="sxs-lookup"><span data-stu-id="8b3a8-137">Select the entity **Standard Title**, and then select **Results**.</span></span> <span data-ttu-id="8b3a8-138">Näkyviin tulevat kaikki **Vakionimike**-entiteetin rivit.</span><span class="sxs-lookup"><span data-stu-id="8b3a8-138">All of the rows in the **Standard Title** entity will be shown.</span></span>
3. <span data-ttu-id="8b3a8-139">Valitse **Uusi** ja syötä **Nimi**-kenttään Järjestelmäinsinööri. Valitse sitten **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="8b3a8-139">Select **New**, and in the **Name** field, enter "Systems Engineer" and then select **Save**.</span></span>
4. <span data-ttu-id="8b3a8-140">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="8b3a8-140">Close the page.</span></span> 
5. <span data-ttu-id="8b3a8-141">Luo toinen vakionimike Vanhemmalle järjestelmäinsinöörille toistamalla vaiheet 1–3.</span><span class="sxs-lookup"><span data-stu-id="8b3a8-141">Repeat steps 1-3 to create another standard title for "Senior Systems Engineer".</span></span>

> ![Esimerkkitietoja Vakionimike-entiteetille](media/ST-data.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]