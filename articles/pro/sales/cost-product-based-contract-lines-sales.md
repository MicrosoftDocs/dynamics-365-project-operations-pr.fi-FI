---
title: Kustannusten tuotepohjaiset sopimusrivit – lite
description: Tässä aiheessa on tietoja siitä, kuinka luodaan
author: rumant
manager: Annbe
ms.date: 10/19/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 0e961bcf32a5dd662b7cd27a23eb5f664c45c292
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/30/2020
ms.locfileid: "4177237"
---
# <a name="cost-product-based-contract-lines---lite"></a><span data-ttu-id="f49c9-103">Kustannusten tuotepohjaiset sopimusrivit – lite</span><span class="sxs-lookup"><span data-stu-id="f49c9-103">Cost product-based contract lines - lite</span></span>

<span data-ttu-id="f49c9-104">_**Käytetään:** Lite-käyttöönotto – kauppa proformalaskutukseen_</span><span class="sxs-lookup"><span data-stu-id="f49c9-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="f49c9-105">Dynamics 365 Project Operationsin tuotepohjaiset sopimusrivit sisältävät **kustannushinta**-kentän, joka tallentaa tuotteen kustannushinnan loppupään kannattavuuden laskentaan.</span><span class="sxs-lookup"><span data-stu-id="f49c9-105">Product-based contract lines in Dynamics 365 Project Operations include the **Cost Price** field, which stores the cost price of the product for downstream profitability calculations.</span></span>

<span data-ttu-id="f49c9-106">Kun tuotepohjainen sopimusrivi luodaan luettelotuotteelle, tuotepohjaisen sopimusrivin kustannuksen oletusarvona on tuoteluettelon **Vakiokustannus**-kenttä.</span><span class="sxs-lookup"><span data-stu-id="f49c9-106">When a product-based contract line is created for a catalog product, the cost of the product-based contract line defaults from the **Standard Cost** field in the product catalog.</span></span> <span data-ttu-id="f49c9-107">Tuoteluettelon **Vakiokustannus**-kenttä määritetään organisaation perusvaluuttana.</span><span class="sxs-lookup"><span data-stu-id="f49c9-107">The **Standard Cost** field in the product catalog is set up in the Organization's base currency.</span></span> <span data-ttu-id="f49c9-108">Kun yksikkökustannuksen oletusarvo on sopimusrivillä, se muunnetaan palvelusopimuksen myyntivaluutaksi.</span><span class="sxs-lookup"><span data-stu-id="f49c9-108">When the unit cost defaults on the contract line, it's converted into the sales currency on the contract.</span></span>

## <a name="unit-cost-on-a-product-based-contract-line"></a><span data-ttu-id="f49c9-109">Yksikkökustannus tuotepohjaisella sopimusrivillä</span><span class="sxs-lookup"><span data-stu-id="f49c9-109">Unit cost on a product-based contract line</span></span>

<span data-ttu-id="f49c9-110">Yksikkökustannusten ottaminen tuotepohjaiseen sopimusriviin sallii eri tuotekustannukset jokaiselle yksikön myynnille.</span><span class="sxs-lookup"><span data-stu-id="f49c9-110">Having a unit cost on a product-based contract line allows for different product costs for each sale of a unit.</span></span> <span data-ttu-id="f49c9-111">Vaikka ei olekaan aina tarpeen, on tiettyjä tilanteita, joissa toimittaja voi diskontata tuotteen hintaa.</span><span class="sxs-lookup"><span data-stu-id="f49c9-111">While not always necessary, there are certain scenarios where the cost of the product may be discounted for the customer by the supplier.</span></span> <span data-ttu-id="f49c9-112">Esimerkkitilanne:</span><span class="sxs-lookup"><span data-stu-id="f49c9-112">Consider the following scenario:</span></span>

<span data-ttu-id="f49c9-113">Fabrikam Robotics asentaa robottikäsiä Adatum Corporationin kokoonpanolinjoilla.</span><span class="sxs-lookup"><span data-stu-id="f49c9-113">Fabrikam Robotics is installing robotic arms at Adatum Corporation's assembly lines.</span></span> <span data-ttu-id="f49c9-114">Fabrikam tarjoaa asennuspalveluita, mutta robottikädet hankitaan Trey Research -yrityksestä.</span><span class="sxs-lookup"><span data-stu-id="f49c9-114">Fabrikam provides installation services but the robotic arms are procured from Trey Research.</span></span> <span data-ttu-id="f49c9-115">Jos robottikäsien asennus Adatum Corporationissa avaa uuden toimialayksikön, Treyn Researchille, he voivat tarjota Fabrikamille erikoisalennuksen tästä sopimuksesta.</span><span class="sxs-lookup"><span data-stu-id="f49c9-115">If the installation of robotic arms at Adatum Corporation opens a new industry vertical for Trey Research, they could offer a special discount for this deal to Fabrikam.</span></span> <span data-ttu-id="f49c9-116">Tässä tapauksessa Fabrikam luo tuotepohjaisen sopimusrivin robottikäsille ja syöttää tämän sopimuksen yksikkökustannukset, jotka poikkeavat Trey Researchin vakiokustannuksista.</span><span class="sxs-lookup"><span data-stu-id="f49c9-116">In this case, Fabrikam creates a product-based contract line for Robotic Arms and inputs a per unit cost for this contract that is different from the standard cost of robotic arms from Trey Research.</span></span>
