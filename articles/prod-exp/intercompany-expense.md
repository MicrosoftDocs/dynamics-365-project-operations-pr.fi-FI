---
title: Konsernin sisäiset kulut
description: Tämä aihe sisältää tietoja siitä, miten konsernin sisäisiä kuluja käytetään työntekijän kulujen kohdistamiseksi sille yritykselle, jolle työ on tehty.
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
ms.openlocfilehash: d908a1c062f5b7f01cf340dcd6f7f24714a992bf
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5271529"
---
# <a name="intercompany-expenses"></a><span data-ttu-id="d71a7-103">Konsernin sisäiset kulut</span><span class="sxs-lookup"><span data-stu-id="d71a7-103">Intercompany expenses</span></span>

<span data-ttu-id="d71a7-104">Työntekijä, joka on yhden yrityksen palveluksessa organisaatiossa, voi suorittaa työn toiselle saman organisaation yritykselle.</span><span class="sxs-lookup"><span data-stu-id="d71a7-104">A worker who is employed by one legal entity in an organization might perform work for another legal entity in the same organization.</span></span> <span data-ttu-id="d71a7-105">Voit käyttää konsernin sisäisiä kuluja työntekijän kulujen kohdistamiseksi sille yritykselle, jolle työ on tehty.</span><span class="sxs-lookup"><span data-stu-id="d71a7-105">You can use intercompany expenses to assign the worker’s expenses to the legal entity for which the  work was performed.</span></span> <span data-ttu-id="d71a7-106">Yritystä, jonka palveluksessa työntekijä on, kutsutaan lainaavaksi yritykseksi.</span><span class="sxs-lookup"><span data-stu-id="d71a7-106">The legal entity that employs the worker is called the loaning legal entity.</span></span> <span data-ttu-id="d71a7-107">Yritystä, jolle työntekijästä aiheutuu kuluja, kutsutaan lainaavaksi yritykseksi.</span><span class="sxs-lookup"><span data-stu-id="d71a7-107">The legal entity for which the worker incurs expenses is called the borrowing legal entity.</span></span> 

<span data-ttu-id="d71a7-108">Ennen kuin työntekijä voi luoda ja lähettää konsernin sisäisiä kuluja, sinun on otettava käyttöön konsernin sisäisten kulujen rivit.</span><span class="sxs-lookup"><span data-stu-id="d71a7-108">Before a worker can create and submit intercompany expenses, you must enable intercompany expense lines.</span></span> <span data-ttu-id="d71a7-109">Valitse lainan myöntävän yrityksen **Kulujen hallintaparametrit** -sivulta **Salli konsernin sisäisten kulujen rivit**.</span><span class="sxs-lookup"><span data-stu-id="d71a7-109">In the loaning legal entity, on the **Expense management parameters** page, select **Allow intercompany expense lines**.</span></span> 

## <a name="tax-posting-for-intercompany-expenses"></a><span data-ttu-id="d71a7-110">Konsernin sisäisten kulujen verokirjaus</span><span class="sxs-lookup"><span data-stu-id="d71a7-110">Tax posting for intercompany expenses</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d71a7-111">Ennen kuin voit käyttää lainan myöntävään (lähde) yritykseen liittyviä veroryhmiä lainan ottavan (kohde) yrityksen sijaan kuluraportissa, sinun on otettava käyttöön toiminto pääkirjan arvonlisäveroasetuksissa.</span><span class="sxs-lookup"><span data-stu-id="d71a7-111">Before you can use tax groups that are associated with the loaning (source) legal entity instead of the borrowing (destination) legal entity in your expense report, you must enable the functionality in the General ledger sales tax setup.</span></span> <span data-ttu-id="d71a7-112">Kun **Yritys konsernin sisäistä verokirjausta varten** -parametriksi on asetettu **Lähde** ja **Käytä arvonlisäveron verotussääntöjä** -asetukseksi on valittu **Ei**, lainan myöntävän yrityksen veroyhdistelmää käytetään.</span><span class="sxs-lookup"><span data-stu-id="d71a7-112">When the **Legal entity for intercompany tax posting** parameter is set to **Source** and **Apply sales tax taxation rules** is set to **No**, the tax combination for the loaning legal entity is used.</span></span> <span data-ttu-id="d71a7-113">Kun sama parametri on asetettu **kohteeseen**, käytetään lainaavan yrityksen veroyhdistelmää.</span><span class="sxs-lookup"><span data-stu-id="d71a7-113">When the same parameter is set to **Destination**, the tax combination for borrowing legal entity will be used.</span></span> <span data-ttu-id="d71a7-114">Jos kyseessä on Yhdysvaltalainen yritys, kun parametrin arvoksi on määritetty **lähde**, **arvonlisäverosaatavat**-kentän asetukset on määritettävä myös uuden **kirjanpidon kirjausryhmät** -sivulla.</span><span class="sxs-lookup"><span data-stu-id="d71a7-114">For legal entities in the United States, when the parameter is set to **Source**, the **Sales tax receivable** field must also be configured on the new **Ledger posting groups** page.</span></span> <span data-ttu-id="d71a7-115">Kirjanpitomoduuli käyttää tämän kentän tietoja veroihin liittyvään kirjanpitomerkintään.</span><span class="sxs-lookup"><span data-stu-id="d71a7-115">The accounting engine will use the information from this field for tax-related accounting entry.</span></span>   
<span data-ttu-id="d71a7-116">Toiminta on yhdenmukainen projektin kanssa tai ei-kirjattujen kulurivien kanssa.</span><span class="sxs-lookup"><span data-stu-id="d71a7-116">The behavior is consistent for expense lines posted with or without a project.</span></span>  


[!INCLUDE[footer-include](../includes/footer-banner.md)]