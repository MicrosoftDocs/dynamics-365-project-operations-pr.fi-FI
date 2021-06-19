---
title: Mukautettujen ratkaisujen luominen hinnoitteludimensioille
description: Tässä aiheessa kerrotaan, miten luodaan mukautettu ratkaisu, kun luodaan mukautettuja hinnoitteludimensioita.
author: Rumant
ms.custom:
- dyn365-projectservice
ms.date: 10/01/2020
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: ae7f22b9cb092e956d0f1eaf1f1997c8e97392f4
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/10/2021
ms.locfileid: "6012312"
---
# <a name="create-custom-solutions-for-pricing-dimensions"></a><span data-ttu-id="c9373-103">Mukautettujen ratkaisujen luominen hinnoitteludimensioille</span><span class="sxs-lookup"><span data-stu-id="c9373-103">Create custom solutions for pricing dimensions</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

> [!IMPORTANT]
> <span data-ttu-id="c9373-104">Kaikkien mukautettujen hinnoitteludimension muutosten on oltava erillisessä ratkaisussa.</span><span class="sxs-lookup"><span data-stu-id="c9373-104">All custom pricing dimension changes should be in a separate solution.</span></span> <span data-ttu-id="c9373-105">Tämä tärkeä paras käytäntö varmistaa, että muutoksia voidaan myöhemmin päivittää tai poistaa tarpeen mukaan, auttaa työn uudelleenkäytössä ja helpottaa näiden muutosten siirtämistä toiseen esiintymään.</span><span class="sxs-lookup"><span data-stu-id="c9373-105">This important best practice provides flexibility in the future to update or remove changes as needed, will help with re-use of your work, and makes it easier to port these changes to another instance.</span></span> <span data-ttu-id="c9373-106">Kun olet tehnyt kaikki tarvittavat muutokset, vie tämä ratkaisu muodossa **Hallittu ratkaisu** ja tuo se muihin esiintymiin, jotta voit käyttää hinnoittelumäärityksiäsi uudelleen.</span><span class="sxs-lookup"><span data-stu-id="c9373-106">After you make the required changes, export this solution as a **Managed solution**, and import it into other instances to reuse your pricing setup.</span></span>

1. <span data-ttu-id="c9373-107">Valitse **Asetukset** > **Ratkaisut** ja valitse sitten **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="c9373-107">Select **Settings** > **Solutions**, and then select **New**.</span></span> 
2. <span data-ttu-id="c9373-108">Anna ratkaisulle nimeksi **organisaation \<your organization name> hinnoitteludimensiot**, anna muut tarvittavat tiedot ja valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="c9373-108">Name the solution, **\<your organization name> pricing dimensions**, enter the remaining required information, and then select **Save**.</span></span>

> ![Mukautetun ratkaisun luominen hinnoitteludimensioille](media/Creation-of-custom-pricing-dimension-solution.PNG)
  
## <a name="add-all-required-entities-and-related-components-to-the-pricing-dimension-solution"></a><span data-ttu-id="c9373-110">Kaikkien tarvittavien entiteettien ja niihin liittyvien komponenttien lisääminen hinnoitteludimensioratkaisuun</span><span class="sxs-lookup"><span data-stu-id="c9373-110">Add all required entities and related components to the Pricing dimension solution</span></span>
<span data-ttu-id="c9373-111">Sinun on lisättävä seuraavat Project Service -entiteetit hinnoitteluratkaisuusi.</span><span class="sxs-lookup"><span data-stu-id="c9373-111">You will need to add the following Project Service entities to your pricing solution.</span></span> <span data-ttu-id="c9373-112">Tämän toimintosarjan vaiheet suorittamalla voit tehdä tärkeitä rakennemuutoksia hinnoitteluratkaisuun, jotta entiteetit ottavat uudet hinnoitteludimensiot huomioon.</span><span class="sxs-lookup"><span data-stu-id="c9373-112">Complete the steps in this procedure to make some important schema changes in the pricing solution so that the entities become aware of the new pricing dimensions.</span></span>

1. <span data-ttu-id="c9373-113">Valitse **Asetukset** > **Ratkaisut** ja kaksoisnapsauta **\<your organization name> hinnoitteludimensioita**.</span><span class="sxs-lookup"><span data-stu-id="c9373-113">Select **Settings** > **Solutions**, and then double-click **\<your organization name> pricing dimensions**.</span></span> 
2. <span data-ttu-id="c9373-114">Valitse vasemman siirtymisruudun Ratkaisunhallinnassa **Lisää aiemmin luoto** > **Entiteetit**.</span><span class="sxs-lookup"><span data-stu-id="c9373-114">In Solution Explorer, on the left navigation pane, select **Add Existing** > **Entities**.</span></span>
3. <span data-ttu-id="c9373-115">Valitse **Ratkaisun osat** -valintaikkunassa seuraavat entiteetit:</span><span class="sxs-lookup"><span data-stu-id="c9373-115">In the **Solution Components** dialog box, select the following entities:</span></span>

- <span data-ttu-id="c9373-116">Todellinen</span><span class="sxs-lookup"><span data-stu-id="c9373-116">Actual</span></span>
- <span data-ttu-id="c9373-117">Varattavissa oleva resurssi</span><span class="sxs-lookup"><span data-stu-id="c9373-117">Bookable Resource</span></span>
- <span data-ttu-id="c9373-118">Arviorivi</span><span class="sxs-lookup"><span data-stu-id="c9373-118">Estimate Line</span></span>
- <span data-ttu-id="c9373-119">Projektin tehtävä</span><span class="sxs-lookup"><span data-stu-id="c9373-119">Project Task</span></span>
- <span data-ttu-id="c9373-120">Laskurivin tiedot</span><span class="sxs-lookup"><span data-stu-id="c9373-120">Invoice Line Detail</span></span>
- <span data-ttu-id="c9373-121">Kirjauskansion rivi</span><span class="sxs-lookup"><span data-stu-id="c9373-121">Journal Line</span></span>
- <span data-ttu-id="c9373-122">Projektin sopimusrivin tiedot</span><span class="sxs-lookup"><span data-stu-id="c9373-122">Project Contract Line Detail</span></span>
- <span data-ttu-id="c9373-123">Projektiryhmän jäsen</span><span class="sxs-lookup"><span data-stu-id="c9373-123">Project Team Member</span></span>
- <span data-ttu-id="c9373-124">Tarjousrivin tiedot</span><span class="sxs-lookup"><span data-stu-id="c9373-124">Quote Line Detail</span></span>
- <span data-ttu-id="c9373-125">Roolin hinnankorotus</span><span class="sxs-lookup"><span data-stu-id="c9373-125">Role Price Markup</span></span>
- <span data-ttu-id="c9373-126">Roolin hinta</span><span class="sxs-lookup"><span data-stu-id="c9373-126">Role Price</span></span> 
- <span data-ttu-id="c9373-127">Aikamerkintä</span><span class="sxs-lookup"><span data-stu-id="c9373-127">Time Entry</span></span> 

> ![Aiemmin luotujen entiteettien lisääminen hinnoitteludimensioratkaisuun](media/Existing-entities-to-PD-solution.png)

> ![Valitse ratkaisun osat](media/Dimension-Components.png)

> [!NOTE]
> <span data-ttu-id="c9373-130">Varmista, että lisäät kaikkien valittujen entiteettien kaikki lomakkeet ja näkymät.</span><span class="sxs-lookup"><span data-stu-id="c9373-130">Make sure to include all forms and views for each of the entities selected.</span></span>

4. <span data-ttu-id="c9373-131">Kun sinua pyydetään lisäämään yllä valituista entiteeteistä riippuvaisia entiteettejä, valitse **Ei**.</span><span class="sxs-lookup"><span data-stu-id="c9373-131">When prompted to include any dependent entities for the selected entities, select **No**.</span></span>

> ![Älä lisää kaikkia liittyviä komponentteja.](media/Do-not-include-required.png)




[!INCLUDE[footer-include](../includes/footer-banner.md)]