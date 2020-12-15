---
title: Ratkaisun luominen mukautetuille hinnoitteludimensioille
description: Tässä aiheessa on tietoja mukautettujen hinnoitteludimensioiden luomisesta.
author: Rumant
manager: tfehr
ms.date: 11/09/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 441501dff23d16960381b3f9fb4b2cceba2b3ba5
ms.sourcegitcommit: 869bde007805ef255f61b03937e4a44aeef61df9
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/12/2020
ms.locfileid: "4513977"
---
# <a name="create-a-solution-for-custom-pricing-dimensions"></a><span data-ttu-id="f590b-103">Ratkaisun luominen mukautetuille hinnoitteludimensioille</span><span class="sxs-lookup"><span data-stu-id="f590b-103">Create a solution for custom pricing dimensions</span></span>

 <span data-ttu-id="f590b-104">_**Koskee:** Project Operationsin resurssiin / muuhun kuin resurssiin perustuvia skenaarioita, Lite-käyttöönotto-kaupasta proformalaskutukseen_</span><span class="sxs-lookup"><span data-stu-id="f590b-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span> 

>[!IMPORTANT]
><span data-ttu-id="f590b-105">Kaikkien mukautettujen hinnoitteludimension muutosten on oltava erillisessä ratkaisussa.</span><span class="sxs-lookup"><span data-stu-id="f590b-105">All custom pricing dimension changes should be in a separate solution.</span></span> <span data-ttu-id="f590b-106">Tämä tärkeä paras käytäntö tarjoaa joustavuutta, jonka avulla voidaan myöhemmin päivittää tai poistaa muutoksia tarpeen mukaan, auttaa työn uudelleenkäytössä ja helpottaa näiden muutosten siirtämistä toiseen esiintymään.</span><span class="sxs-lookup"><span data-stu-id="f590b-106">This important best practice allows the flexibility to update or remove changes as needed, helps with re-use of your work, and makes it easier to port changes to other instances.</span></span> <span data-ttu-id="f590b-107">Kun olet tehnyt kaikki tarvittavat muutokset, vie tämä ratkaisu muodossa **Hallittu** ratkaisu ja tuo se sitten muihin esiintymiin, jotta voit käyttää sitä uudelleen.</span><span class="sxs-lookup"><span data-stu-id="f590b-107">After you make the required changes, export this solution as a **Managed** solution, and then import into other instances for reuse.</span></span>

## <a name="create-a-solution-for-custom-pricing-dimensions"></a><span data-ttu-id="f590b-108">Ratkaisun luominen mukautetuille hinnoitteludimensioille</span><span class="sxs-lookup"><span data-stu-id="f590b-108">Create a solution for custom pricing dimensions</span></span>

1.  <span data-ttu-id="f590b-109">Valitse **Asetukset** > **Ratkaisut** ja valitse sitten **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="f590b-109">Select **Settings** > **Solutions**, and then select **New**.</span></span>
2.  <span data-ttu-id="f590b-110">Anna ratkaisulle nimeksi *<your organization name> hinnoitteludimensiot*.</span><span class="sxs-lookup"><span data-stu-id="f590b-110">Name the solution, *<your organization name> pricing dimensions*.</span></span>
3. <span data-ttu-id="f590b-111">Syötä muut tarvittavat tiedot ja valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="f590b-111">Enter the remaining required information, and then select **Save**.</span></span>

  ![Mukautetun hinnoitteludimensioratkaisun luominen](./media/Creation-of-custom-pricing-dimension-solution.png)
 
## <a name="add-all-required-entities-and-related-components-to-the-pricing-dimension-solution"></a><span data-ttu-id="f590b-113">Kaikkien tarvittavien entiteettien ja niihin liittyvien komponenttien lisääminen hinnoitteludimensioratkaisuun</span><span class="sxs-lookup"><span data-stu-id="f590b-113">Add all required entities and related components to the Pricing dimension solution</span></span>

<span data-ttu-id="f590b-114">Lisää hinnoitteluratkaisuun seuraavat Project Service -entiteetit, jotta voit tehdä hinnoitteluratkaisuun tärkeitä rakennemuutoksia.</span><span class="sxs-lookup"><span data-stu-id="f590b-114">Add the following Project Service entities to your pricing solution to make important schema changes in the pricing solution.</span></span> <span data-ttu-id="f590b-115">Kun olet suorittanut tämän toiminpiteen, entiteetit tunnistavat uudet hinnoitteludimensiot.</span><span class="sxs-lookup"><span data-stu-id="f590b-115">After you have completed this procedure, the entities will recognize the new pricing dimensions.</span></span>

1.  <span data-ttu-id="f590b-116">Valitse **Asetukset** > **Ratkaisut** ja kaksoisnapauta sen jälkeen **<*organisaatiosi nimen*> hinnoitteludimensioita**.</span><span class="sxs-lookup"><span data-stu-id="f590b-116">Select **Settings** > **Solutions**, and then double-click **<*your organization name*> pricing dimensions**.</span></span>
2.  <span data-ttu-id="f590b-117">Valitse vasemman siirtymisruudun Ratkaisunhallinnassa **Lisää aiemmin luoto** > **Entiteetit**.</span><span class="sxs-lookup"><span data-stu-id="f590b-117">In Solution Explorer, on the left navigation pane, select **Add Existing** > **Entities**.</span></span>
3.  <span data-ttu-id="f590b-118">Valitse **Ratkaisun osat** -valintaikkunassa seuraavat entiteetit:</span><span class="sxs-lookup"><span data-stu-id="f590b-118">In the **Solution Components** dialog box, select the following entities:</span></span>
 
   - <span data-ttu-id="f590b-119">**Todellinen**</span><span class="sxs-lookup"><span data-stu-id="f590b-119">**Actual**</span></span>
   - <span data-ttu-id="f590b-120">**Varattavissa oleva resurssi**</span><span class="sxs-lookup"><span data-stu-id="f590b-120">**Bookable Resource**</span></span>
   - <span data-ttu-id="f590b-121">**Arviorivi**</span><span class="sxs-lookup"><span data-stu-id="f590b-121">**Estimate Line**</span></span>
   - <span data-ttu-id="f590b-122">**Projektin tehtävä**</span><span class="sxs-lookup"><span data-stu-id="f590b-122">**Project Task**</span></span>
   - <span data-ttu-id="f590b-123">**Laskurivin tiedot**</span><span class="sxs-lookup"><span data-stu-id="f590b-123">**Invoice Line Detail**</span></span>
   - <span data-ttu-id="f590b-124">**Kirjauskansion rivi**</span><span class="sxs-lookup"><span data-stu-id="f590b-124">**Journal Line**</span></span>
   - <span data-ttu-id="f590b-125">**Projektin sopimusrivin tiedot**</span><span class="sxs-lookup"><span data-stu-id="f590b-125">**Project Contract Line Detail**</span></span>
   - <span data-ttu-id="f590b-126">**Projektiryhmän jäsen**</span><span class="sxs-lookup"><span data-stu-id="f590b-126">**Project Team Member**</span></span>
   - <span data-ttu-id="f590b-127">**Tarjousrivin tiedot**</span><span class="sxs-lookup"><span data-stu-id="f590b-127">**Quote Line Detail**</span></span>
   - <span data-ttu-id="f590b-128">**Roolin hinnankorotus**</span><span class="sxs-lookup"><span data-stu-id="f590b-128">**Role Price Markup**</span></span>
   - <span data-ttu-id="f590b-129">**Roolin hinta**</span><span class="sxs-lookup"><span data-stu-id="f590b-129">**Role Price**</span></span>
   - <span data-ttu-id="f590b-130">**Aikamerkintä**</span><span class="sxs-lookup"><span data-stu-id="f590b-130">**Time Entry**</span></span>
 
   ![Aiemmin luotujen entiteettien lisääminen mukautettuun hinnoitteludimensioratkaisuun](./media/Existing-entities-to-PD-solution.png)
 
 4. <span data-ttu-id="f590b-132">Tarkista kunkin entiteetin osalta lisättävät komponentit ja kunkin yhteisön lopullinen resurssiluettelo.</span><span class="sxs-lookup"><span data-stu-id="f590b-132">For each entity, review the components being added and the final list of entity assets for each entity.</span></span> 

   >[!NOTE]
   > <span data-ttu-id="f590b-133">Lisää kaikkien valittujen entiteettien kaikki lomakkeet ja näkymät.</span><span class="sxs-lookup"><span data-stu-id="f590b-133">Include all forms and views for each of the selected entities.</span></span>

  ![Lisätyt entiteetit](./media/solution-component-selection.png)


5.  <span data-ttu-id="f590b-135">Kun sinua pyydetään sisällytämään valituista entiteeteistä riippuvaisia entiteettejä, valitse **Ei, älä sisällytä pakollisia komponentteja.**</span><span class="sxs-lookup"><span data-stu-id="f590b-135">When prompted to include any dependent entities for the selected entities, select **No, do not include required components.**</span></span>

    ![Sisältäen riippuvaiset entiteetit](./media/Do-not-include-required.png)
