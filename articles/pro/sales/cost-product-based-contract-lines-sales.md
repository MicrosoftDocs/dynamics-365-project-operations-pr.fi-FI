---
title: Kustannusten tuotepohjaiset sopimusrivit – lite
description: Tässä aiheessa on tietoja siitä, kuinka luodaan
author: rumant
manager: Annbe
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 001b0b54abcdd5fcd1eca7f3271cc78392f68860
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5273689"
---
# <a name="cost-product-based-contract-lines---lite"></a><span data-ttu-id="dcbba-103">Kustannusten tuotepohjaiset sopimusrivit – lite</span><span class="sxs-lookup"><span data-stu-id="dcbba-103">Cost product-based contract lines - lite</span></span>

<span data-ttu-id="dcbba-104">_**Käytetään:** Lite-käyttöönotto – kauppa proformalaskutukseen_</span><span class="sxs-lookup"><span data-stu-id="dcbba-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="dcbba-105">Tuotepohjaiset sopimusrivit Dynamics 365 Project Operationsissa sisältävät **Kustannushinta**-kentän, jossa on tuotteen kustannushinta kannattavuuslaskelmia varten.</span><span class="sxs-lookup"><span data-stu-id="dcbba-105">Product-based contract lines in Dynamics 365 Project Operations include the **Cost Price** field, which stores the cost price of the product for downstream profitability calculations.</span></span>

<span data-ttu-id="dcbba-106">Kun tuotepohjainen sopimusrivi luodaan luettelotuotteelle, rivin hinta on oletusarvon mukaan tuoteluettelon **Vakiokustannus**-kentän mukainen.</span><span class="sxs-lookup"><span data-stu-id="dcbba-106">When a product-based contract line is created for a catalog product, the cost of the line defaults from the **Standard Cost** field in the product catalog.</span></span> <span data-ttu-id="dcbba-107">Tuoteluettelon **Vakiokustannus**-kenttä määritetään organisaation perusvaluuttana.</span><span class="sxs-lookup"><span data-stu-id="dcbba-107">The **Standard Cost** field in the product catalog is set up in the Organization's base currency.</span></span> <span data-ttu-id="dcbba-108">Kun yksikkökustannuksen oletusarvo on sopimusrivillä, se muunnetaan palvelusopimuksen myyntivaluutaksi.</span><span class="sxs-lookup"><span data-stu-id="dcbba-108">When the unit cost defaults on the contract line, it's converted into the sales currency on the contract.</span></span>

## <a name="unit-cost-on-a-product-based-contract-line"></a><span data-ttu-id="dcbba-109">Yksikkökustannus tuotepohjaisella sopimusrivillä</span><span class="sxs-lookup"><span data-stu-id="dcbba-109">Unit cost on a product-based contract line</span></span>

<span data-ttu-id="dcbba-110">Yksikkökustannusten ottaminen tuotepohjaiseen sopimusriviin sallii eri tuotekustannukset jokaiselle yksikön myynnille.</span><span class="sxs-lookup"><span data-stu-id="dcbba-110">Having a unit cost on a product-based contract line allows for different product costs for each sale of a unit.</span></span> <span data-ttu-id="dcbba-111">Vaikka ei olekaan aina tarpeen, on tiettyjä tilanteita, joissa toimittaja voi diskontata tuotteen hintaa.</span><span class="sxs-lookup"><span data-stu-id="dcbba-111">While not always necessary, there are certain scenarios where the cost of the product may be discounted for the customer by the supplier.</span></span> <span data-ttu-id="dcbba-112">Esimerkkitilanne:</span><span class="sxs-lookup"><span data-stu-id="dcbba-112">Consider the following scenario:</span></span>

<span data-ttu-id="dcbba-113">Fabrikam Robotics asentaa robottikäsiä Adatum Corporationin kokoonpanolinjoilla.</span><span class="sxs-lookup"><span data-stu-id="dcbba-113">Fabrikam Robotics is installing robotic arms at Adatum Corporation's assembly lines.</span></span> <span data-ttu-id="dcbba-114">Fabrikam tarjoaa asennuspalvelut, mutta robottikädet ovat peräisin Trey Researchilta.</span><span class="sxs-lookup"><span data-stu-id="dcbba-114">Fabrikam provides installation services but the robotic arms are from Trey Research.</span></span> <span data-ttu-id="dcbba-115">Jos robottikäsien asennus Adatum Corporationissa avaa uuden toimialayksikön, Treyn Researchille, he voivat tarjota Fabrikamille erikoisalennuksen tästä sopimuksesta.</span><span class="sxs-lookup"><span data-stu-id="dcbba-115">If the installation of robotic arms at Adatum Corporation opens a new industry vertical for Trey Research, they could offer a special discount for this deal to Fabrikam.</span></span> <span data-ttu-id="dcbba-116">Tässä tapauksessa Fabrikam luo tuotepohjaisen sopimusrivin robottikäsille.</span><span class="sxs-lookup"><span data-stu-id="dcbba-116">In this case, Fabrikam creates a product-based contract line for Robotic Arms.</span></span> <span data-ttu-id="dcbba-117">Tähän palvelusopimukseen syötetään yksikkökustannus.</span><span class="sxs-lookup"><span data-stu-id="dcbba-117">A per unit cost is entered for this contract.</span></span> <span data-ttu-id="dcbba-118">Kustannus eroaa Trey Researchin robottikäsien kustannuksesta.</span><span class="sxs-lookup"><span data-stu-id="dcbba-118">The cost is different from the cost of robotic arms from Trey Research.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]