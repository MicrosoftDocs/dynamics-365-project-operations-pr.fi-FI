---
title: Hinnaston luominen
description: Hinnaston luominen Project Servicessä
author: rumant
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: bdd05aea-27a3-431d-9a80-2e220fb25e53
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 756af2fe3bc73d478b0355493aae6f0e49ac5835
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/24/2020
ms.locfileid: "3751264"
---
# <a name="create-a-price-list-project-service"></a><span data-ttu-id="ea4c8-103">Hinnaston luominen (Project Service)</span><span class="sxs-lookup"><span data-stu-id="ea4c8-103">Create a price list (Project Service)</span></span>

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="ea4c8-104">Hinnastot sisältävät mallin jota asiakkuuspäälliköt voivat käyttää luotaessa tarjouksia ja projekteja ja projektin kustannusten määrittämisessä.</span><span class="sxs-lookup"><span data-stu-id="ea4c8-104">Price lists provide a template your account managers can use for creating quotes and projects, and for establishing the costs of a project.</span></span> <span data-ttu-id="ea4c8-105">Ne sisältävät roolien ja kulujen rivinimikeluettelon ja niistä veloitettava hinnan.</span><span class="sxs-lookup"><span data-stu-id="ea4c8-105">They provide a line item list of roles and expenses, and the price you will charge for each.</span></span> <span data-ttu-id="ea4c8-106">Luomalla useita hinnastoja voit ylläpitää erilaisia hinnoittelurakenteita eri alueilla myytäviä tuotteita tai kanavia varten.</span><span class="sxs-lookup"><span data-stu-id="ea4c8-106">You can create multiple price lists so that you can maintain separate price structures for different regions you sell your products in or for different sales channels.</span></span> <span data-ttu-id="ea4c8-107">On hyvä luoda vähintään yksi hinnasto jokaiselle valuutalle jossa asiakkaita on tarkoitus laskuttaa.</span><span class="sxs-lookup"><span data-stu-id="ea4c8-107">It’s a good idea to create at least one price list for every currency you plan to bill your customers in.</span></span>  
  
<span data-ttu-id="ea4c8-108">Toimitettavan työn rahoitusta koskevien arvioiden luomiseksi varmista, että jokaisella projektilla on kustannus- ja myyntihinnaston varmuuskopio.</span><span class="sxs-lookup"><span data-stu-id="ea4c8-108">To create financial estimates for the work to be delivered, make sure every project has a backing cost and sales price list.</span></span> <span data-ttu-id="ea4c8-109">Määritä oletusarvoinen kustannus- ja myyntihinnasto, jota käytetään yrityksesi kaikissa projekteissa.</span><span class="sxs-lookup"><span data-stu-id="ea4c8-109">Set up a default cost and sales pricelist that applies to all projects created in your organization.</span></span>  
  
<span data-ttu-id="ea4c8-110">Hinnastot perustuvat rooleihin ja kululuokkiin. Ennen kuin luot hinnaston, varmista, että olet aiemmin määrittänyt roolit ja kululuokat, joita haluat käyttää hinnaston luomisen yhteydessä.</span><span class="sxs-lookup"><span data-stu-id="ea4c8-110">Price lists rely on roles and expense categories, so before you create a price list, make sure you’ve already configured the roles and expense categories you want to use while creating the price list.</span></span>  
  
1.  <span data-ttu-id="ea4c8-111">Siirry kohtaan **Project Service > Hinnastot**.</span><span class="sxs-lookup"><span data-stu-id="ea4c8-111">Go to **Project Service > Price Lists**.</span></span>  
  
2.  <span data-ttu-id="ea4c8-112">Valitse **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="ea4c8-112">Click **New**.</span></span>  
  
3.  <span data-ttu-id="ea4c8-113">Kohdassa **Konteksti** valitse, onko tämä **Kustannus**, **Osto** tai **Myynti** -hinnasto.</span><span class="sxs-lookup"><span data-stu-id="ea4c8-113">In **Context**, select whether this price list is for **Cost**, **Purchase**, or **Sales**.</span></span>  
  
4.  <span data-ttu-id="ea4c8-114">Kohtaan **Nimi** kirjoita hinnaston nimi.</span><span class="sxs-lookup"><span data-stu-id="ea4c8-114">In **Name**, enter a name for the price list.</span></span>  
  
5.  <span data-ttu-id="ea4c8-115">Kohdassa **Valuutta** valitse laskutuksessa tai kustannuslaskelmassa käytettävä valuutta.</span><span class="sxs-lookup"><span data-stu-id="ea4c8-115">In **Currency**, select the currency you’re going to use for billing or costing.</span></span>  
  
6.  <span data-ttu-id="ea4c8-116">Kohdassa **Aikayksikkö** määritä aikaväli, jota hinta koskee, esimerkiksi päivä tai tunti.</span><span class="sxs-lookup"><span data-stu-id="ea4c8-116">In **Time Unit**, specify the period of time the price applies to, such as day or hour.</span></span>  
  
7.  <span data-ttu-id="ea4c8-117">Täytä **Alkamispäivä**, **Päättymispäivä** ja **Kuvaus** tarpeen mukaan.</span><span class="sxs-lookup"><span data-stu-id="ea4c8-117">Fill in the **Start Date**, **End Date**, and **Description** as needed.</span></span>  
  
8.  <span data-ttu-id="ea4c8-118">Valitse **Tallenna** ja luo tietue, jotta voit jatkaa muokkaamista.</span><span class="sxs-lookup"><span data-stu-id="ea4c8-118">Click **Save** to create the record so you can continue editing it.</span></span>  
  
9. <span data-ttu-id="ea4c8-119">Lisää roolin hinta hinnastoon, valitse **+** kohdassa **Roolin hinnat**.</span><span class="sxs-lookup"><span data-stu-id="ea4c8-119">To add a role price to the price list, click **+** under **Role prices**.</span></span>  
  
10. <span data-ttu-id="ea4c8-120">**Roolin hinta** -ruudussa täytä tiedot ja valitse sitten **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="ea4c8-120">In the **Role Price** pane, fill in the details, and then click **Save**.</span></span> <span data-ttu-id="ea4c8-121">Jatka roolihintojen lisäämistä tarpeen mukaan.</span><span class="sxs-lookup"><span data-stu-id="ea4c8-121">Continue adding role prices as necessary.</span></span> <span data-ttu-id="ea4c8-122">Valitse **Tallenna** näytön oikeassa alakulmassa, kun olet valmis.</span><span class="sxs-lookup"><span data-stu-id="ea4c8-122">When you’re done, click **Save** at the bottom right corner of the screen.</span></span>  
  
11. <span data-ttu-id="ea4c8-123">Lisää kululuokan hinta hinnastoon valitsemalla **+** kohdassa **Luokan hinnat**.</span><span class="sxs-lookup"><span data-stu-id="ea4c8-123">To add an expense category price to the price list, click **+** under **Category prices**.</span></span>  
  
12. <span data-ttu-id="ea4c8-124">**Tapahtumaluokan hinta** -ruudussa täytä tiedot ja valitse sitten **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="ea4c8-124">In the **Transaction Category Price** pane, fill in the details, and then click **Save**.</span></span> <span data-ttu-id="ea4c8-125">Jatka luokan hintojen lisäämistä tarpeen mukaan.</span><span class="sxs-lookup"><span data-stu-id="ea4c8-125">Continue adding category prices as necessary.</span></span> <span data-ttu-id="ea4c8-126">Valitse **Tallenna** näytön oikeassa alakulmassa, kun olet valmis.</span><span class="sxs-lookup"><span data-stu-id="ea4c8-126">When you’re done, click **Save** at the bottom right corner of the screen.</span></span>  
  
13. <span data-ttu-id="ea4c8-127">Jos haluat lisätä hinnastoon hinnaston nimikkeet, valitse **+** kohdassa **Hinnaston nimikkeet**.</span><span class="sxs-lookup"><span data-stu-id="ea4c8-127">To add price list items to the price list, click **+** under **Price List Items**.</span></span>  
  
14. <span data-ttu-id="ea4c8-128">**Hinnaston nimike** -ruudussa täytä tiedot ja valitse sitten **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="ea4c8-128">In the **Price List Item** pane, fill in the details, and then click **Save**.</span></span> <span data-ttu-id="ea4c8-129">Jatka hinnaston nimikkeiden lisäämistä tarpeen mukaan.</span><span class="sxs-lookup"><span data-stu-id="ea4c8-129">Continue adding price list items as necessary.</span></span> <span data-ttu-id="ea4c8-130">Valitse **Tallenna** näytön oikeassa alakulmassa, kun olet valmis.</span><span class="sxs-lookup"><span data-stu-id="ea4c8-130">When you’re done, click **Save** at the bottom right corner of the screen.</span></span>  
  
15. <span data-ttu-id="ea4c8-131">Lisää aluesuhteita hinnastoon valitsemalla **+** kohdassa **Aluesuhteet**.</span><span class="sxs-lookup"><span data-stu-id="ea4c8-131">To add territory relationships to the price list, click **+** under **Territory Relationships**.</span></span>  
  
16. <span data-ttu-id="ea4c8-132">**Uusi yhteys** -valintaikkunassa täytä tiedot ja valitse sitten **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="ea4c8-132">In the **New Connection** window, fill in the details, and then click **Save**.</span></span> <span data-ttu-id="ea4c8-133">Jatkaa aluesuhteiden lisäämistä tarpeen mukaan.</span><span class="sxs-lookup"><span data-stu-id="ea4c8-133">Continue adding territory relationships as necessary.</span></span> <span data-ttu-id="ea4c8-134">Valitse **Tallenna** näytön oikeassa alakulmassa, kun olet valmis.</span><span class="sxs-lookup"><span data-stu-id="ea4c8-134">When you’re done, click **Save** at the bottom right corner of the screen.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="ea4c8-135">Katso myös</span><span class="sxs-lookup"><span data-stu-id="ea4c8-135">See Also</span></span>  
 [<span data-ttu-id="ea4c8-136">Project Service Automationin määrittäminen</span><span class="sxs-lookup"><span data-stu-id="ea4c8-136">Configure Project Service Automation</span></span>](../project-service/configure.md)
