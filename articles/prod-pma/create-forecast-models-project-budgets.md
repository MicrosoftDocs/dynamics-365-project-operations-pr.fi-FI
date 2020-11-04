---
title: Ennustemallien luominen projektibudjeteille
description: Tässä aiheessa kuvataan, miten jäljellä oleville budjeteille luodaan ennustemalli.
author: Yowelle
manager: AnnBe
ms.date: 04/24/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: 32a436d240f5535ff15f8bc3b8ba9be2d1d4da17
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/16/2020
ms.locfileid: "4075484"
---
# <a name="create-forecast-models-for-project-budgets"></a><span data-ttu-id="29327-103">Ennustemallien luominen projektibudjeteille</span><span class="sxs-lookup"><span data-stu-id="29327-103">Create forecast models for project budgets</span></span> 

[!include [banner](../includes/banner.md)]

<span data-ttu-id="29327-104">Tässä aiheessa kuvataan, miten jäljellä oleville budjeteille luodaan ennustemalli.</span><span class="sxs-lookup"><span data-stu-id="29327-104">This topic describes how to create a forecast model for remaining budgets.</span></span> <span data-ttu-id="29327-105">Budjetinhallinnan kohteena oleva projekti käyttää kahdentyyppisiä budjetteja: alkuperäistä ja jäljellä olevaa projektia.</span><span class="sxs-lookup"><span data-stu-id="29327-105">A project that is subject to budget control uses two types of budgets: original and remaining.</span></span> <span data-ttu-id="29327-106">Kun luot projektibudjetin, sinun täytyy määrittää alkuperäiset ja jäljellä olevat budjettiennustemallit, jotka on luotu **ennustemallit** -sivulla.</span><span class="sxs-lookup"><span data-stu-id="29327-106">When you create a project budget, you must specify the original and remaining budget forecast models that were created in the **Forecast models** page.</span></span> <span data-ttu-id="29327-107">Määritettyihin malleihin perustuvat projektibudjetit luodaan projektibudjetin toteutuksen yhteydessä.</span><span class="sxs-lookup"><span data-stu-id="29327-107">Project budgets based on the specified models are created when you commit the project budget.</span></span>

> [!NOTE]
> <span data-ttu-id="29327-108">Budjetinhallinnan ennustemallilla ei voi olla osamallia eikä sitä voi käyttää osamallina.</span><span class="sxs-lookup"><span data-stu-id="29327-108">A forecast model that is used for budget control can’t have a submodel or be used as a submodel.</span></span>

1. <span data-ttu-id="29327-109">Valitse **projektinhallinta ja kirjanpito** > **asetukset** > **ennusteet**  > **ennustemallit**.</span><span class="sxs-lookup"><span data-stu-id="29327-109">Select **Project management and accounting** > **Setup** > **Forecasts**  > **Forecast models**.</span></span>
2. <span data-ttu-id="29327-110">Valitse **Uusi** , jos haluat luoda uuden ennustemallin, ja kirjoita sitten mallin tunnusnumero ja nimi uudelle mallille.</span><span class="sxs-lookup"><span data-stu-id="29327-110">Select **New** to create a new forecast model, and then enter a model ID number and name for the new model.</span></span> 
3. <span data-ttu-id="29327-111">Jos haluat estää ennustemallin ennusterivien muuttamisen, aseta **pysäytetty** -asetuksen arvoksi **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="29327-111">Set the **Stopped** option to **Yes** to prevent any changes to the forecast lines for the forecast model.</span></span> 
4. <span data-ttu-id="29327-112">Jos ennusteriveille, joihin malli liittyy, tulisi luoda kassavirtaennusteita pääkirjaan, aseta **Sisällytä kassavirtaennusteisiin** asetukseksi **Kyllä.**</span><span class="sxs-lookup"><span data-stu-id="29327-112">If the forecast lines that the model is associated with should generate cash flow forecasts in the general ledger, set **Include in Cash flow forecasts** to **Yes.**</span></span> 
5. <span data-ttu-id="29327-113">Jos haluat käyttää projektin päivämäärää laskunpäivämääränä, aseta **ennustettu laskun päivämäärä** -kentän arvoksi **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="29327-113">To use the project date as the invoice date, set **Forecast Invoice date** to **Yes**.</span></span> 
6. <span data-ttu-id="29327-114">Valitse **budjetin tyyppi** -kentässä jokin seuraavista mallityypeistä:</span><span class="sxs-lookup"><span data-stu-id="29327-114">In the **Budget type** field, select one of the following model types:</span></span>

   - <span data-ttu-id="29327-115">**Alkuperäinen budjetti** : Käytä alkuperäistä budjettisummaa, joka on sidottu, kun alkuperäinen budjetti luodaan ja hyväksytään.</span><span class="sxs-lookup"><span data-stu-id="29327-115">**Original budget** : Use the original budget amounts that are committed when the initial budget is created and approved.</span></span>
   - <span data-ttu-id="29327-116">**Jäljellä oleva budjetti** : Käytä jäljellä olevia budjetin summia projektin käyttöiän aikana.</span><span class="sxs-lookup"><span data-stu-id="29327-116">**Remaining budget** : Use the remaining budget amounts during the life of the project.</span></span> <span data-ttu-id="29327-117">Tämän ennustemallin saldosta vähennetään toteutuneita tapahtumia ja niitä korotetaan tai vähennetään budjetin versioissa.</span><span class="sxs-lookup"><span data-stu-id="29327-117">The balances in this forecast model are reduced by actual transactions and increased or decreased by budget revisions.</span></span>
   - <span data-ttu-id="29327-118">**Siirto eteenpäin** : Käytä projektin siirtobudjetin summia.</span><span class="sxs-lookup"><span data-stu-id="29327-118">**Carry-forward** : Use the carry-forward budget amounts for the project.</span></span> <span data-ttu-id="29327-119">Siirtäminen eteenpäin on valinnainen prosessi, jonka avulla voidaan siirtää käyttämättömät budjettisummat yhdestä tilikaudesta toiseen.</span><span class="sxs-lookup"><span data-stu-id="29327-119">Carry-forward is an optional process that can be run to transfer unused budget amounts from one fiscal year to another.</span></span>

7. <span data-ttu-id="29327-120">Määritä seuraavat asetukset tarpeen mukaan:</span><span class="sxs-lookup"><span data-stu-id="29327-120">Set the following options as required:</span></span>

   - <span data-ttu-id="29327-121">Jos haluat käyttää projektin päivämäärää laskunpäivämääränä, ota **ennustettu laskun päivämäärä** käyttöön.</span><span class="sxs-lookup"><span data-stu-id="29327-121">Enable **Forecast invoice date** to use the project date as the invoice date.</span></span>
   - <span data-ttu-id="29327-122">Ota käyttöön **ennuste, jossa KET** ennustaaksesi keskeneräisen työn (KET) perusteella, ja valitse sitten KET-tyyppi.</span><span class="sxs-lookup"><span data-stu-id="29327-122">Enable **Forecast with WIP** to forecast based on work in progress (WIP), and then select the type of WIP.</span></span> 
   - <span data-ttu-id="29327-123">Voit säilyttää oletus- **budjettityypiksi** **ei mitään** tai määrittää uuden tyypin.</span><span class="sxs-lookup"><span data-stu-id="29327-123">You can keep the default **Budget type** as **None** or enter a new type.</span></span> <span data-ttu-id="29327-124">Budjetin tyyppiä ei voi muuttaa, kun muutat tietuetta.</span><span class="sxs-lookup"><span data-stu-id="29327-124">The budget type can't be changed after you change a record.</span></span>     
    > [!NOTE]
    > <span data-ttu-id="29327-125">Jos muutat oletusbudjettityyppiä, kaikki muut asetukset eivät ole käytettävissä päivityksille, etkä voi käyttää tätä ennustemallia uudelleen.</span><span class="sxs-lookup"><span data-stu-id="29327-125">If you change the default budget type, all other options will become unavailable for updates, and you can't reuse this forecast model.</span></span> 
   


 

