---
title: Hinnastojen aktivoinnin poistaminen
description: Tässä aiheessa kerrotaan, miten voit poistaa käyttämättömien, vanhojen hinnastojen aktivoinnin tai poistaa ne käytöstä.
author: rumant
ms.date: 03/19/2021
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Professional Service industries
ms.author: rumant
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: d5d6cf6b4b097c08edca5a3235ed1b438a0eae2d
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/10/2021
ms.locfileid: "6001332"
---
# <a name="deactivate-price-lists"></a><span data-ttu-id="f4925-103">Hinnastojen aktivoinnin poistaminen</span><span class="sxs-lookup"><span data-stu-id="f4925-103">Deactivate price lists</span></span> 

<span data-ttu-id="f4925-104">_**Koskee:** Project Operationsin resurssiin / muuhun kuin resurssiin perustuvia skenaarioita, Lite-käyttöönotto-kaupasta proformalaskutukseen_</span><span class="sxs-lookup"><span data-stu-id="f4925-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="f4925-105">Jos haluat poistaa vanhoja tai käyttämättömiä hinnastoja Dynamics 365 Project Operationsista, suorita seuraavat kaksi vaihetta.</span><span class="sxs-lookup"><span data-stu-id="f4925-105">To remove old or unused price lists from Dynamics 365 Project Operations, there are two steps you must complete.</span></span> 

1. <span data-ttu-id="f4925-106">Hinnaston poistaminen tai sen poistaminen tietyiltä sivuilta.</span><span class="sxs-lookup"><span data-stu-id="f4925-106">Remove or delete the price list from specific pages.</span></span>
2. <span data-ttu-id="f4925-107">Poista hinnaston aktivointi tai poista se aktiivisista hinnastoista **Hinnastot**-sivulla.</span><span class="sxs-lookup"><span data-stu-id="f4925-107">Deactivate or delete the price list from the Active price lists on the **Price Lists** page.</span></span>

>[!IMPORTANT]
> <span data-ttu-id="f4925-108">Molemmat vaiheet on suoritettava hinnaston poistamiseksi täysin.</span><span class="sxs-lookup"><span data-stu-id="f4925-108">You must complete both steps to fully remove a price list.</span></span> <span data-ttu-id="f4925-109">Ei riitä, että vain vaihe 2, jossa hinnasto poistetaan tai sen aktivointi poistetaan aktiivisten hinnastojen näkymästä, suoritetaan.</span><span class="sxs-lookup"><span data-stu-id="f4925-109">Only performing step 2, which is to directly delete or deactivate the price list from the Active Price Lists view, is not sufficient.</span></span> <span data-ttu-id="f4925-110">On myös poistettava tämän hinnaston suhde kaikista paikoista, jotka on mainittu vaiheessa 1.</span><span class="sxs-lookup"><span data-stu-id="f4925-110">You must also delete the association of this price list from all the places mentioned in step 1.</span></span>

## <a name="delete-the-price-list-from-specific-pages"></a><span data-ttu-id="f4925-111">Hinnaston poistaminen tietyiltä sivuilta</span><span class="sxs-lookup"><span data-stu-id="f4925-111">Delete the price list from specific pages</span></span>
1. <span data-ttu-id="f4925-112">Jos haluat poistaa hinnaston Project Operationsista, siirry seuraaville sivuille:</span><span class="sxs-lookup"><span data-stu-id="f4925-112">To delete a price list from Project Operations, go to the following pages:</span></span>  

      - <span data-ttu-id="f4925-113">**Projektiparametrit**-sivu > **Hinnastot**-välilehti</span><span class="sxs-lookup"><span data-stu-id="f4925-113">**Project parameters** page > **Price Lists** tab</span></span>
      - <span data-ttu-id="f4925-114">**Organisaatioyksikkö**-sivu > **Hinnastot**-ruudukko</span><span class="sxs-lookup"><span data-stu-id="f4925-114">**Organizational Unit** page > **Price Lists** grid</span></span>
      - <span data-ttu-id="f4925-115">**Tilit**-sivu > **Projektihinnastot**-ruudukko</span><span class="sxs-lookup"><span data-stu-id="f4925-115">**Account** page > **Project Price Lists** grid</span></span>
      - <span data-ttu-id="f4925-116">**Projektitarjoukset**-sivu > **Projektihinnastot** -ruudukko: Tämä koskee kaikkia aktiivisia projektitarjouksia.</span><span class="sxs-lookup"><span data-stu-id="f4925-116">**Project Quotes** page > **Project Price Lists** grid: This applies to all active project quotes.</span></span>
      - <span data-ttu-id="f4925-117">**Projektisopimukset**-sivu > **Projektihinnastot** -ruudukko: Tämä koskee kaikkia aktiivisia projektisopimuksia.</span><span class="sxs-lookup"><span data-stu-id="f4925-117">**Project Contracts** page > **Project Price Lists** grid: This applies to all active project contracts.</span></span>

 2. <span data-ttu-id="f4925-118">Valitse kullakin sivulla poistettava hinnasto ja valitse sitten **Poista**.</span><span class="sxs-lookup"><span data-stu-id="f4925-118">For each page, you need to select the price list that you want to delete, and then select **Delete**.</span></span> 
 
## <a name="delete-or-deactivate-the-price-list-from-the-price-lists-page"></a><span data-ttu-id="f4925-119">Poista hinnasto tai poista sen aktivointi Hinnastot-sivulla</span><span class="sxs-lookup"><span data-stu-id="f4925-119">Delete or deactivate the price list from the Price Lists page</span></span>
 
1. <span data-ttu-id="f4925-120">Jos haluat poistaa hinnaston aktiivisista hinnastoista, siirry kohtaan **Myynti** > **Asiakkaat** > **Hinnastot**.</span><span class="sxs-lookup"><span data-stu-id="f4925-120">To delete a price list from the active price lists, go to **Sales** > **Customers** > **Price Lists**.</span></span> 
2. <span data-ttu-id="f4925-121">Valitse poistettava hinnasto ja valitse sitten **Poista**.</span><span class="sxs-lookup"><span data-stu-id="f4925-121">Select the price list that you want to delete and then select **Delete**.</span></span> <span data-ttu-id="f4925-122">Jos hinnastoon viitataan aiemmin luoduissa tapahtumissa, et voi poistaa sitä.</span><span class="sxs-lookup"><span data-stu-id="f4925-122">If the price list is referenced on any existing transactions, you won't be able to delete it.</span></span> <span data-ttu-id="f4925-123">Jos tämä tapahtuu, voit poistaa hinnaston aktivoinnin niin, että se ei näy missään näkymissä.</span><span class="sxs-lookup"><span data-stu-id="f4925-123">If this happens, you can deactivate the price list so that it doesn't appear in any views.</span></span> 
3. <span data-ttu-id="f4925-124">Jos haluat poistaa hinnastosta aktivoinnin, valitse hinnasto uudelleen ja valitse sitten **Poista aktivointi**.</span><span class="sxs-lookup"><span data-stu-id="f4925-124">To deactivate the price list, select the price list again, and then select **Deactivate**.</span></span>   
