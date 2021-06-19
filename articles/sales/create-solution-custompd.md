---
title: Ratkaisun luominen mukautetuille hinnoitteludimensioille
description: Tässä aiheessa on tietoja mukautettujen hinnoitteludimensioiden luomisesta.
author: Rumant
ms.date: 11/09/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 86f4cd2c26ebfca621d1b226b571d220d3b2441e
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/10/2021
ms.locfileid: "6010332"
---
# <a name="create-a-solution-for-custom-pricing-dimensions"></a><span data-ttu-id="3a8f4-103">Ratkaisun luominen mukautetuille hinnoitteludimensioille</span><span class="sxs-lookup"><span data-stu-id="3a8f4-103">Create a solution for custom pricing dimensions</span></span>

 <span data-ttu-id="3a8f4-104">_**Koskee:** Project Operationsin resurssiin / muuhun kuin resurssiin perustuvia skenaarioita, Lite-käyttöönotto-kaupasta proformalaskutukseen_</span><span class="sxs-lookup"><span data-stu-id="3a8f4-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span> 

>[!IMPORTANT]
><span data-ttu-id="3a8f4-105">Kaikkien mukautettujen hinnoitteludimension muutosten on oltava erillisessä ratkaisussa.</span><span class="sxs-lookup"><span data-stu-id="3a8f4-105">All custom pricing dimension changes should be in a separate solution.</span></span> <span data-ttu-id="3a8f4-106">Tämä tärkeä paras käytäntö tarjoaa joustavuutta, jonka avulla voidaan myöhemmin päivittää tai poistaa muutoksia tarpeen mukaan, auttaa työn uudelleenkäytössä ja helpottaa näiden muutosten siirtämistä toiseen esiintymään.</span><span class="sxs-lookup"><span data-stu-id="3a8f4-106">This important best practice allows the flexibility to update or remove changes as needed, helps with re-use of your work, and makes it easier to port changes to other instances.</span></span> <span data-ttu-id="3a8f4-107">Kun olet tehnyt kaikki tarvittavat muutokset, vie tämä ratkaisu muodossa **Hallittu** ratkaisu ja tuo se sitten muihin esiintymiin, jotta voit käyttää sitä uudelleen.</span><span class="sxs-lookup"><span data-stu-id="3a8f4-107">After you make the required changes, export this solution as a **Managed** solution, and then import into other instances for reuse.</span></span>

## <a name="create-a-solution-for-custom-pricing-dimensions"></a><span data-ttu-id="3a8f4-108">Ratkaisun luominen mukautetuille hinnoitteludimensioille</span><span class="sxs-lookup"><span data-stu-id="3a8f4-108">Create a solution for custom pricing dimensions</span></span>

1.  <span data-ttu-id="3a8f4-109">Valitse **Asetukset** > **Ratkaisut** ja valitse sitten **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="3a8f4-109">Select **Settings** > **Solutions**, and then select **New**.</span></span>
2.  <span data-ttu-id="3a8f4-110">Anna ratkaisulle nimeksi *<your organization name> hinnoitteludimensiot*.</span><span class="sxs-lookup"><span data-stu-id="3a8f4-110">Name the solution, *<your organization name> pricing dimensions*.</span></span>
3. <span data-ttu-id="3a8f4-111">Syötä muut tarvittavat tiedot ja valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="3a8f4-111">Enter the remaining required information, and then select **Save**.</span></span>

  ![Mukautetun hinnoitteludimensioratkaisun luominen](./media/Creation-of-custom-pricing-dimension-solution.png)
 
## <a name="add-all-required-entities-and-related-components-to-the-pricing-dimension-solution"></a><span data-ttu-id="3a8f4-113">Kaikkien tarvittavien entiteettien ja niihin liittyvien komponenttien lisääminen hinnoitteludimensioratkaisuun</span><span class="sxs-lookup"><span data-stu-id="3a8f4-113">Add all required entities and related components to the Pricing dimension solution</span></span>

<span data-ttu-id="3a8f4-114">Lisää hinnoitteluratkaisuun seuraavat Project Service -entiteetit, jotta voit tehdä hinnoitteluratkaisuun tärkeitä rakennemuutoksia.</span><span class="sxs-lookup"><span data-stu-id="3a8f4-114">Add the following Project Service entities to your pricing solution to make important schema changes in the pricing solution.</span></span> <span data-ttu-id="3a8f4-115">Kun olet suorittanut tämän toiminpiteen, entiteetit tunnistavat uudet hinnoitteludimensiot.</span><span class="sxs-lookup"><span data-stu-id="3a8f4-115">After you have completed this procedure, the entities will recognize the new pricing dimensions.</span></span>

1.  <span data-ttu-id="3a8f4-116">Valitse **Asetukset** > **Ratkaisut** ja kaksoisnapauta sen jälkeen **<*organisaatiosi nimen*> hinnoitteludimensioita**.</span><span class="sxs-lookup"><span data-stu-id="3a8f4-116">Select **Settings** > **Solutions**, and then double-click **<*your organization name*> pricing dimensions**.</span></span>
2.  <span data-ttu-id="3a8f4-117">Valitse vasemman siirtymisruudun Ratkaisunhallinnassa **Lisää aiemmin luoto** > **Entiteetit**.</span><span class="sxs-lookup"><span data-stu-id="3a8f4-117">In Solution Explorer, on the left navigation pane, select **Add Existing** > **Entities**.</span></span>
3.  <span data-ttu-id="3a8f4-118">Valitse **Ratkaisun osat** -valintaikkunassa seuraavat entiteetit:</span><span class="sxs-lookup"><span data-stu-id="3a8f4-118">In the **Solution Components** dialog box, select the following entities:</span></span>
 
   - <span data-ttu-id="3a8f4-119">**Todellinen**</span><span class="sxs-lookup"><span data-stu-id="3a8f4-119">**Actual**</span></span>
   - <span data-ttu-id="3a8f4-120">**Varattavissa oleva resurssi**</span><span class="sxs-lookup"><span data-stu-id="3a8f4-120">**Bookable Resource**</span></span>
   - <span data-ttu-id="3a8f4-121">**Arviorivi**</span><span class="sxs-lookup"><span data-stu-id="3a8f4-121">**Estimate Line**</span></span>
   - <span data-ttu-id="3a8f4-122">**Projektin tehtävä**</span><span class="sxs-lookup"><span data-stu-id="3a8f4-122">**Project Task**</span></span>
   - <span data-ttu-id="3a8f4-123">**Laskurivin tiedot**</span><span class="sxs-lookup"><span data-stu-id="3a8f4-123">**Invoice Line Detail**</span></span>
   - <span data-ttu-id="3a8f4-124">**Kirjauskansion rivi**</span><span class="sxs-lookup"><span data-stu-id="3a8f4-124">**Journal Line**</span></span>
   - <span data-ttu-id="3a8f4-125">**Projektin sopimusrivin tiedot**</span><span class="sxs-lookup"><span data-stu-id="3a8f4-125">**Project Contract Line Detail**</span></span>
   - <span data-ttu-id="3a8f4-126">**Projektiryhmän jäsen**</span><span class="sxs-lookup"><span data-stu-id="3a8f4-126">**Project Team Member**</span></span>
   - <span data-ttu-id="3a8f4-127">**Tarjousrivin tiedot**</span><span class="sxs-lookup"><span data-stu-id="3a8f4-127">**Quote Line Detail**</span></span>
   - <span data-ttu-id="3a8f4-128">**Roolin hinnankorotus**</span><span class="sxs-lookup"><span data-stu-id="3a8f4-128">**Role Price Markup**</span></span>
   - <span data-ttu-id="3a8f4-129">**Roolin hinta**</span><span class="sxs-lookup"><span data-stu-id="3a8f4-129">**Role Price**</span></span>
   - <span data-ttu-id="3a8f4-130">**Aikamerkintä**</span><span class="sxs-lookup"><span data-stu-id="3a8f4-130">**Time Entry**</span></span>
 
   ![Aiemmin luotujen entiteettien lisääminen mukautettuun hinnoitteludimensioratkaisuun](./media/Existing-entities-to-PD-solution.png)
 
 4. <span data-ttu-id="3a8f4-132">Tarkista kunkin entiteetin osalta lisättävät komponentit ja kunkin yhteisön lopullinen resurssiluettelo.</span><span class="sxs-lookup"><span data-stu-id="3a8f4-132">For each entity, review the components being added and the final list of entity assets for each entity.</span></span> 

   >[!NOTE]
   > <span data-ttu-id="3a8f4-133">Lisää kaikkien valittujen entiteettien kaikki lomakkeet ja näkymät.</span><span class="sxs-lookup"><span data-stu-id="3a8f4-133">Include all forms and views for each of the selected entities.</span></span>

  ![Lisätyt entiteetit](./media/solution-component-selection.png)


5.  <span data-ttu-id="3a8f4-135">Kun sinua pyydetään sisällytämään valituista entiteeteistä riippuvaisia entiteettejä, valitse **Ei, älä sisällytä pakollisia komponentteja.**</span><span class="sxs-lookup"><span data-stu-id="3a8f4-135">When prompted to include any dependent entities for the selected entities, select **No, do not include required components.**</span></span>

    ![Sisältäen riippuvaiset entiteetit](./media/Do-not-include-required.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]