---
title: Hinnastojen aktivoinnin poistaminen
description: Tässä aiheessa kerrotaan, miten voit poistaa käyttämättömien, vanhojen hinnastojen aktivoinnin tai poistaa ne käytöstä.
author: rumant
manager: AnnBe
ms.date: 03/19/2021
ms.topic: article
ms.prod: ''
ms.service: project-operations
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
ms.openlocfilehash: 3fa902e93815002be7d6915880cd7759dbbde5ef
ms.sourcegitcommit: 386921f44f1e9a8a828b140206d52945de07aee7
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/22/2021
ms.locfileid: "5701926"
---
# <a name="deactivate-price-lists"></a><span data-ttu-id="3f745-103">Hinnastojen aktivoinnin poistaminen</span><span class="sxs-lookup"><span data-stu-id="3f745-103">Deactivate price lists</span></span> 

<span data-ttu-id="3f745-104">_**Koskee:** Project Operationsin resurssiin / muuhun kuin resurssiin perustuvia skenaarioita, Lite-käyttöönotto-kaupasta proformalaskutukseen_</span><span class="sxs-lookup"><span data-stu-id="3f745-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="3f745-105">Jos haluat poistaa vanhoja tai käyttämättömiä hinnastoja Dynamics 365 Project Operationsista, suorita seuraavat kaksi vaihetta.</span><span class="sxs-lookup"><span data-stu-id="3f745-105">To remove old or unused price lists from Dynamics 365 Project Operations, there are two steps you must complete.</span></span> 

1. <span data-ttu-id="3f745-106">Hinnaston poistaminen tai sen poistaminen tietyiltä sivuilta.</span><span class="sxs-lookup"><span data-stu-id="3f745-106">Remove or delete the price list from specific pages.</span></span>
2. <span data-ttu-id="3f745-107">Poista hinnaston aktivointi tai poista se aktiivisista hinnastoista **Hinnastot**-sivulla.</span><span class="sxs-lookup"><span data-stu-id="3f745-107">Deactivate or delete the price list from the Active price lists on the **Price Lists** page.</span></span>

>[!IMPORTANT]
> <span data-ttu-id="3f745-108">Molemmat vaiheet on suoritettava hinnaston poistamiseksi täysin.</span><span class="sxs-lookup"><span data-stu-id="3f745-108">You must complete both steps to fully remove a price list.</span></span> <span data-ttu-id="3f745-109">Ei riitä, että vain vaihe 2, jossa hinnasto poistetaan tai sen aktivointi poistetaan aktiivisten hinnastojen näkymästä, suoritetaan.</span><span class="sxs-lookup"><span data-stu-id="3f745-109">Only performing step 2, which is to directly delete or deactivate the price list from the Active Price Lists view, is not sufficient.</span></span> <span data-ttu-id="3f745-110">On myös poistettava tämän hinnaston suhde kaikista paikoista, jotka on mainittu vaiheessa 1.</span><span class="sxs-lookup"><span data-stu-id="3f745-110">You must also delete the association of this price list from all the places mentioned in step 1.</span></span>

## <a name="delete-the-price-list-from-specific-pages"></a><span data-ttu-id="3f745-111">Hinnaston poistaminen tietyiltä sivuilta</span><span class="sxs-lookup"><span data-stu-id="3f745-111">Delete the price list from specific pages</span></span>
1. <span data-ttu-id="3f745-112">Jos haluat poistaa hinnaston Project Operationsista, siirry seuraaville sivuille:</span><span class="sxs-lookup"><span data-stu-id="3f745-112">To delete a price list from Project Operations, go to the following pages:</span></span>  

      - <span data-ttu-id="3f745-113">**Projektiparametrit**-sivu > **Hinnastot**-välilehti</span><span class="sxs-lookup"><span data-stu-id="3f745-113">**Project parameters** page > **Price Lists** tab</span></span>
      - <span data-ttu-id="3f745-114">**Organisaatioyksikkö**-sivu > **Hinnastot**-ruudukko</span><span class="sxs-lookup"><span data-stu-id="3f745-114">**Organizational Unit** page > **Price Lists** grid</span></span>
      - <span data-ttu-id="3f745-115">**Tilit**-sivu > **Projektihinnastot**-ruudukko</span><span class="sxs-lookup"><span data-stu-id="3f745-115">**Account** page > **Project Price Lists** grid</span></span>
      - <span data-ttu-id="3f745-116">**Projektitarjoukset**-sivu > **Projektihinnastot** -ruudukko: Tämä koskee kaikkia aktiivisia projektitarjouksia.</span><span class="sxs-lookup"><span data-stu-id="3f745-116">**Project Quotes** page > **Project Price Lists** grid: This applies to all active project quotes.</span></span>
      - <span data-ttu-id="3f745-117">**Projektisopimukset**-sivu > **Projektihinnastot** -ruudukko: Tämä koskee kaikkia aktiivisia projektisopimuksia.</span><span class="sxs-lookup"><span data-stu-id="3f745-117">**Project Contracts** page > **Project Price Lists** grid: This applies to all active project contracts.</span></span>

 2. <span data-ttu-id="3f745-118">Valitse kullakin sivulla poistettava hinnasto ja valitse sitten **Poista**.</span><span class="sxs-lookup"><span data-stu-id="3f745-118">For each page, you need to select the price list that you want to delete, and then select **Delete**.</span></span> 
 
## <a name="delete-or-deactivate-the-price-list-from-the-price-lists-page"></a><span data-ttu-id="3f745-119">Poista hinnasto tai poista sen aktivointi Hinnastot-sivulla</span><span class="sxs-lookup"><span data-stu-id="3f745-119">Delete or deactivate the price list from the Price Lists page</span></span>
 
1. <span data-ttu-id="3f745-120">Jos haluat poistaa hinnaston aktiivisista hinnastoista, siirry kohtaan **Myynti** > **Asiakkaat** > **Hinnastot**.</span><span class="sxs-lookup"><span data-stu-id="3f745-120">To delete a price list from the active price lists, go to **Sales** > **Customers** > **Price Lists**.</span></span> 
2. <span data-ttu-id="3f745-121">Valitse poistettava hinnasto ja valitse sitten **Poista**.</span><span class="sxs-lookup"><span data-stu-id="3f745-121">Select the price list that you want to delete and then select **Delete**.</span></span> <span data-ttu-id="3f745-122">Jos hinnastoon viitataan aiemmin luoduissa tapahtumissa, et voi poistaa sitä.</span><span class="sxs-lookup"><span data-stu-id="3f745-122">If the price list is referenced on any existing transactions, you won't be able to delete it.</span></span> <span data-ttu-id="3f745-123">Jos tämä tapahtuu, voit poistaa hinnaston aktivoinnin niin, että se ei näy missään näkymissä.</span><span class="sxs-lookup"><span data-stu-id="3f745-123">If this happens, you can deactivate the price list so that it doesn't appear in any views.</span></span> 
3. <span data-ttu-id="3f745-124">Jos haluat poistaa hinnastosta aktivoinnin, valitse hinnasto uudelleen ja valitse sitten **Poista aktivointi**.</span><span class="sxs-lookup"><span data-stu-id="3f745-124">To deactivate the price list, select the price list again, and then select **Deactivate**.</span></span>   
