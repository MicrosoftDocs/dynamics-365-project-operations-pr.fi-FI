---
title: Konsernin sisäiset kulut
description: Työntekijä, joka on yhden yrityksen palveluksessa organisaatiossa, voi suorittaa työn toiselle saman organisaation yritykselle. Tässä tilanteessa voit käyttää konserniyritysten välistä kuluominaisuutta, kun haluat delegoida työntekijän kulut sille yritykselle, jolle työ suoritettiin.
author: ShylaThompson
manager: AnnBe
ms.date: 05/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TrvParameters
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0967f23e4e1f8e0431c55d4d54554e7e90e2451c
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/16/2020
ms.locfileid: "4075499"
---
# <a name="intercompany-expenses"></a><span data-ttu-id="7c8a1-104">Konsernin sisäiset kulut</span><span class="sxs-lookup"><span data-stu-id="7c8a1-104">Intercompany expenses</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7c8a1-105">Työntekijä, joka on yhden yrityksen palveluksessa organisaatiossa, voi suorittaa työn toiselle saman organisaation yritykselle.</span><span class="sxs-lookup"><span data-stu-id="7c8a1-105">A worker who is employed by one legal entity in an organization might perform work for another legal entity in the same organization.</span></span> <span data-ttu-id="7c8a1-106">Tässä tilanteessa voit käyttää konserniyritysten välistä kuluominaisuutta, kun haluat delegoida työntekijän kulut sille yritykselle, jolle työ suoritettiin.</span><span class="sxs-lookup"><span data-stu-id="7c8a1-106">In this situation, you can use the intercompany expense feature to assign the worker’s expenses to the legal entity for which the work was performed.</span></span> <span data-ttu-id="7c8a1-107">Yritystä, jonka palveluksessa työntekijä on, kutsutaan lainaavaksi yritykseksi.</span><span class="sxs-lookup"><span data-stu-id="7c8a1-107">The legal entity that employs the worker is called the loaning legal entity.</span></span> <span data-ttu-id="7c8a1-108">Yritystä, jolle työntekijästä aiheutuu kuluja, kutsutaan lainaavaksi yritykseksi.</span><span class="sxs-lookup"><span data-stu-id="7c8a1-108">The legal entity for which the worker incurs expenses is called the borrowing legal entity.</span></span> 

<span data-ttu-id="7c8a1-109">Ennen kuin työntekijä voi luoda ja lähettää kuluja työstä, joka suoritetaan eri yritykselle, valitse lainaavalle yritykselle **kulun hallinnan parametrit** -sivulla **Salli konsernin kulurivit** -vaihtoehto.</span><span class="sxs-lookup"><span data-stu-id="7c8a1-109">Before a worker can create and submit expenses for work that is performed for a different legal entity, in the loaning legal entity, on the **Expense management parameters** page, select the **Allow intercompany expense lines** option.</span></span> 

## <a name="tax-posting-for-intercompany-expenses"></a><span data-ttu-id="7c8a1-110">Konsernin sisäisten kulujen verokirjaus</span><span class="sxs-lookup"><span data-stu-id="7c8a1-110">Tax posting for intercompany expenses</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7c8a1-111">Jos haluat käyttää veroryhmiä, jotka on liitetty (lähde) yritykseen kuluraportin lainaavan (kohde) yrityksen sijaan, sinun täytyy määrittää tämä kirjanpidon arvonlisäveromäärityksessä.</span><span class="sxs-lookup"><span data-stu-id="7c8a1-111">If you want to use tax groups that are associated with the loaning (source) legal entity instead of the borrowing (destination) legal entity in your expense report, you will need to configure this in the General ledger sales tax set up.</span></span> <span data-ttu-id="7c8a1-112">Kun kirjanpitoparametri, **konsernin sisäisen veron kirjausyritykselle** on asetettu **lähde** ja **Käytä arvonlisäveron verosääntöjä** -asetukseksi on määritetty **ei** , lainaavan yrityksen veroyhdistelmää käytetään.</span><span class="sxs-lookup"><span data-stu-id="7c8a1-112">When the General ledger parameter, **Legal entity for intercompany tax posting** is set to **Source** and **Apply sales tax taxation rules** is set to **No** , the tax combination for the loaning legal entity will be used.</span></span> <span data-ttu-id="7c8a1-113">Kun sama parametri on asetettu **kohteeseen** , käytetään lainaavan yrityksen veroyhdistelmää.</span><span class="sxs-lookup"><span data-stu-id="7c8a1-113">When the same parameter is set to **Destination** , the tax combination for borrowing legal entity will be used.</span></span> <span data-ttu-id="7c8a1-114">Jos kyseessä on Yhdysvaltalainen yritys, kun parametrin arvoksi on määritetty **lähde** , **arvonlisäverosaatavat** -kentän asetukset on määritettävä myös uuden **kirjanpidon kirjausryhmät** -sivulla.</span><span class="sxs-lookup"><span data-stu-id="7c8a1-114">For legal entities in the United States, when the parameter is set to **Source** , the **Sales tax receivable** field must also be configured on the new **Ledger posting groups** page.</span></span> <span data-ttu-id="7c8a1-115">Kirjanpitomoduuli käyttää tämän kentän tietoja veroihin liittyvään kirjanpitomerkintään.</span><span class="sxs-lookup"><span data-stu-id="7c8a1-115">The accounting engine will use the information from this field for tax related accounting entry.</span></span>   
<span data-ttu-id="7c8a1-116">Toiminta on yhdenmukainen projektin kanssa tai ei-kirjattujen kulurivien kanssa.</span><span class="sxs-lookup"><span data-stu-id="7c8a1-116">The behavior is consistent for expense lines posted with or without a project.</span></span>  
