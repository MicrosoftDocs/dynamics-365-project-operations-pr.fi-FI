---
title: Kustannuslaskennan tuotepohjaiset tarjousrivit
description: Tässä aiheessa on tietoja kustannushinnan käyttämisestä tuotepohjaisella tarjousrivillä.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 17b377eab5bcbc1a2327cb3ff87cc75d8de40953
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/16/2020
ms.locfileid: "4075251"
---
# <a name="costing-product-based-quote-lines"></a><span data-ttu-id="31855-103">Kustannuslaskennan tuotepohjaiset tarjousrivit</span><span class="sxs-lookup"><span data-stu-id="31855-103">Costing product-based quote lines</span></span>

<span data-ttu-id="31855-104">_**Koskee:** Project Operationsin resurssiin / muuhun kuin resurssiin perustuvia skenaarioita, Lite-käyttöönotto-kaupasta proformalaskutukseen_</span><span class="sxs-lookup"><span data-stu-id="31855-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="31855-105">Dynamics 365 Project Operationsissa tuotepohjaisilla tarjousriveillä voi olla myös **Kustannushinta** -kenttä.</span><span class="sxs-lookup"><span data-stu-id="31855-105">Product-based quote lines in Dynamics 365 Project Operations also have a **Cost Price** field.</span></span> <span data-ttu-id="31855-106">Tämän kentän avulla seurataan tuotteen kustannushintaa tarjousrivillä ja tehdään prosessin loppupään kannattavuuslaskelmia.</span><span class="sxs-lookup"><span data-stu-id="31855-106">This field is used to track the cost price for the product on the quote line and for downstream profitability calculations.</span></span>

<span data-ttu-id="31855-107">Kun tuotepohjainen tarjousrivi luodaan luettelotuotteelle, tuotepohjaisen tarjousrivin kustannuksen oletusarvona on tuoteluettelon **Vakiokustannus** -kenttä.</span><span class="sxs-lookup"><span data-stu-id="31855-107">When a product-based quote line is created for a catalog product, the cost of the product-based quote line is defaulted from the **Standard Cost** field in the product catalog.</span></span> <span data-ttu-id="31855-108">Tuoteluettelon Vakiokustannus -kenttä määritetään organisaation perusvaluuttana.</span><span class="sxs-lookup"><span data-stu-id="31855-108">The standard cost field in the product catalog is set up in the Organization's base currency.</span></span> <span data-ttu-id="31855-109">Tuotepohjaisen tarjousrivin oletusyksikkökustannus muunnetaan tarjouksen myyntivaluutaksi.</span><span class="sxs-lookup"><span data-stu-id="31855-109">The default unit cost on the product-based quote line is converted to the sales currency on the quote.</span></span>

## <a name="unit-cost-on-a-product-based-quote-line"></a><span data-ttu-id="31855-110">Yksikkökustannus tuotepohjaisella tarjousrivillä</span><span class="sxs-lookup"><span data-stu-id="31855-110">Unit cost on a product-based quote line</span></span>

<span data-ttu-id="31855-111">Yksikkökustannuksen tarkoitus tuotepohjaisella tarjousrivillä on sallia tuotteelle eri kustannukset eri myyntitilanteisiin.</span><span class="sxs-lookup"><span data-stu-id="31855-111">The purpose of having a unit cost on a product-based quote line is to allow for different costs for a product for each sale.</span></span> <span data-ttu-id="31855-112">Tämä ei ole tyypillinen skenaario, mutta joskus toimittaja voi alentaa tuotteen kustannusta myynnin loppuasiakkaan mukaan.</span><span class="sxs-lookup"><span data-stu-id="31855-112">This is not a typical scenario, but sometimes the cost of the product may be discounted by the supplier depending on the customer of the final sale.</span></span>

<span data-ttu-id="31855-113">Esimerkkejä:</span><span class="sxs-lookup"><span data-stu-id="31855-113">For example:</span></span>

<span data-ttu-id="31855-114">Fabrikam Robotics asentaa robottikäsiä Datum Corporationin kokoonpanolinjoilla.</span><span class="sxs-lookup"><span data-stu-id="31855-114">Fabrikam Robotics is installing robotic arms at A Datum Corporation's assembly lines.</span></span> <span data-ttu-id="31855-115">Fabrikam tarjoaa asennuspalveluita, mutta robottikädet hankitaan Trey Robotics -yrityksestä.</span><span class="sxs-lookup"><span data-stu-id="31855-115">Fabrikam provides installation services but the robotic arms are procured from Trey robotics.</span></span> <span data-ttu-id="31855-116">Jos robottikäsien asennus Datum Corporationissa avaa uuden toimialayksikön, Treyn robottikäsille, Trey voi antaa Fabrikamille erikoisalennuksen tästä sopimuksesta.</span><span class="sxs-lookup"><span data-stu-id="31855-116">If the installation of robotic arms at A Datum Corporation opens a new industry vertical for Trey's robotic arms, Trey could give a special discount for this deal to Fabrikam.</span></span>

<span data-ttu-id="31855-117">Tässä tapauksessa Fabrikam luo tuotepohjaisen tarjousrivin Robotic Armsille ja syöttää tälle tarjoukselle erityisen yksikkökustannuksen.</span><span class="sxs-lookup"><span data-stu-id="31855-117">In this case, Fabrikam will create product-based quote line for Robotic Arms and input a special per unit cost for this quote.</span></span> <span data-ttu-id="31855-118">Tämä kustannus poikkeaa Trey Robotic Armsin vakiokustannuksista.</span><span class="sxs-lookup"><span data-stu-id="31855-118">This cost is different from the standard cost of Trey Robotic Arms.</span></span>
