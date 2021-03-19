---
title: Mukautettujen ratkaisujen luominen hinnoitteludimensioille
description: Tässä aiheessa kerrotaan, miten luodaan mukautettu ratkaisu, kun luodaan mukautettuja hinnoitteludimensioita.
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
ms.openlocfilehash: 1d8117d6f6bcedc97264401fc941470f34efb1ae
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5284984"
---
# <a name="create-custom-solutions-for-pricing-dimensions"></a><span data-ttu-id="e5f8b-103">Mukautettujen ratkaisujen luominen hinnoitteludimensioille</span><span class="sxs-lookup"><span data-stu-id="e5f8b-103">Create custom solutions for pricing dimensions</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

> [!IMPORTANT]
> <span data-ttu-id="e5f8b-104">Kaikkien mukautettujen hinnoitteludimension muutosten on oltava erillisessä ratkaisussa.</span><span class="sxs-lookup"><span data-stu-id="e5f8b-104">All custom pricing dimension changes should be in a separate solution.</span></span> <span data-ttu-id="e5f8b-105">Tämä tärkeä paras käytäntö varmistaa, että muutoksia voidaan myöhemmin päivittää tai poistaa tarpeen mukaan, auttaa työn uudelleenkäytössä ja helpottaa näiden muutosten siirtämistä toiseen esiintymään.</span><span class="sxs-lookup"><span data-stu-id="e5f8b-105">This important best practice provides flexibility in the future to update or remove changes as needed, will help with re-use of your work, and makes it easier to port these changes to another instance.</span></span> <span data-ttu-id="e5f8b-106">Kun olet tehnyt kaikki tarvittavat muutokset, vie tämä ratkaisu muodossa **Hallittu ratkaisu** ja tuo se muihin esiintymiin, jotta voit käyttää hinnoittelumäärityksiäsi uudelleen.</span><span class="sxs-lookup"><span data-stu-id="e5f8b-106">After you make the required changes, export this solution as a **Managed solution**, and import it into other instances to reuse your pricing setup.</span></span>

1. <span data-ttu-id="e5f8b-107">Valitse **Asetukset** > **Ratkaisut** ja valitse sitten **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="e5f8b-107">Select **Settings** > **Solutions**, and then select **New**.</span></span> 
2. <span data-ttu-id="e5f8b-108">Anna ratkaisulle nimeksi **organisaation \<your organization name> hinnoitteludimensiot**, anna muut tarvittavat tiedot ja valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="e5f8b-108">Name the solution, **\<your organization name> pricing dimensions**, enter the remaining required information, and then select **Save**.</span></span>

> ![Mukautetun ratkaisun luominen hinnoitteludimensioille](media/Creation-of-custom-pricing-dimension-solution.PNG)
  
## <a name="add-all-required-entities-and-related-components-to-the-pricing-dimension-solution"></a><span data-ttu-id="e5f8b-110">Kaikkien tarvittavien entiteettien ja niihin liittyvien komponenttien lisääminen hinnoitteludimensioratkaisuun</span><span class="sxs-lookup"><span data-stu-id="e5f8b-110">Add all required entities and related components to the Pricing dimension solution</span></span>
<span data-ttu-id="e5f8b-111">Sinun on lisättävä seuraavat Project Service -entiteetit hinnoitteluratkaisuusi.</span><span class="sxs-lookup"><span data-stu-id="e5f8b-111">You will need to add the following Project Service entities to your pricing solution.</span></span> <span data-ttu-id="e5f8b-112">Tämän toimintosarjan vaiheet suorittamalla voit tehdä tärkeitä rakennemuutoksia hinnoitteluratkaisuun, jotta entiteetit ottavat uudet hinnoitteludimensiot huomioon.</span><span class="sxs-lookup"><span data-stu-id="e5f8b-112">Complete the steps in this procedure to make some important schema changes in the pricing solution so that the entities become aware of the new pricing dimensions.</span></span>

1. <span data-ttu-id="e5f8b-113">Valitse **Asetukset** > **Ratkaisut** ja kaksoisnapsauta **\<your organization name> hinnoitteludimensioita**.</span><span class="sxs-lookup"><span data-stu-id="e5f8b-113">Select **Settings** > **Solutions**, and then double-click **\<your organization name> pricing dimensions**.</span></span> 
2. <span data-ttu-id="e5f8b-114">Valitse vasemman siirtymisruudun Ratkaisunhallinnassa **Lisää aiemmin luoto** > **Entiteetit**.</span><span class="sxs-lookup"><span data-stu-id="e5f8b-114">In Solution Explorer, on the left navigation pane, select **Add Existing** > **Entities**.</span></span>
3. <span data-ttu-id="e5f8b-115">Valitse **Ratkaisun osat** -valintaikkunassa seuraavat entiteetit:</span><span class="sxs-lookup"><span data-stu-id="e5f8b-115">In the **Solution Components** dialog box, select the following entities:</span></span>

- <span data-ttu-id="e5f8b-116">Todellinen</span><span class="sxs-lookup"><span data-stu-id="e5f8b-116">Actual</span></span>
- <span data-ttu-id="e5f8b-117">Varattavissa oleva resurssi</span><span class="sxs-lookup"><span data-stu-id="e5f8b-117">Bookable Resource</span></span>
- <span data-ttu-id="e5f8b-118">Arviorivi</span><span class="sxs-lookup"><span data-stu-id="e5f8b-118">Estimate Line</span></span>
- <span data-ttu-id="e5f8b-119">Projektin tehtävä</span><span class="sxs-lookup"><span data-stu-id="e5f8b-119">Project Task</span></span>
- <span data-ttu-id="e5f8b-120">Laskurivin tiedot</span><span class="sxs-lookup"><span data-stu-id="e5f8b-120">Invoice Line Detail</span></span>
- <span data-ttu-id="e5f8b-121">Kirjauskansion rivi</span><span class="sxs-lookup"><span data-stu-id="e5f8b-121">Journal Line</span></span>
- <span data-ttu-id="e5f8b-122">Projektin sopimusrivin tiedot</span><span class="sxs-lookup"><span data-stu-id="e5f8b-122">Project Contract Line Detail</span></span>
- <span data-ttu-id="e5f8b-123">Projektiryhmän jäsen</span><span class="sxs-lookup"><span data-stu-id="e5f8b-123">Project Team Member</span></span>
- <span data-ttu-id="e5f8b-124">Tarjousrivin tiedot</span><span class="sxs-lookup"><span data-stu-id="e5f8b-124">Quote Line Detail</span></span>
- <span data-ttu-id="e5f8b-125">Roolin hinnankorotus</span><span class="sxs-lookup"><span data-stu-id="e5f8b-125">Role Price Markup</span></span>
- <span data-ttu-id="e5f8b-126">Roolin hinta</span><span class="sxs-lookup"><span data-stu-id="e5f8b-126">Role Price</span></span> 
- <span data-ttu-id="e5f8b-127">Aikamerkintä</span><span class="sxs-lookup"><span data-stu-id="e5f8b-127">Time Entry</span></span> 

> ![Aiemmin luotujen entiteettien lisääminen hinnoitteludimensioratkaisuun](media/Existing-entities-to-PD-solution.png)

> ![Valitse ratkaisun osat](media/Dimension-Components.png)

> [!NOTE]
> <span data-ttu-id="e5f8b-130">Varmista, että lisäät kaikkien valittujen entiteettien kaikki lomakkeet ja näkymät.</span><span class="sxs-lookup"><span data-stu-id="e5f8b-130">Make sure to include all forms and views for each of the entities selected.</span></span>

4. <span data-ttu-id="e5f8b-131">Kun sinua pyydetään lisäämään yllä valituista entiteeteistä riippuvaisia entiteettejä, valitse **Ei**.</span><span class="sxs-lookup"><span data-stu-id="e5f8b-131">When prompted to include any dependent entities for the selected entities, select **No**.</span></span>

> ![Älä lisää kaikkia liittyviä komponentteja.](media/Do-not-include-required.png)




[!INCLUDE[footer-include](../includes/footer-banner.md)]