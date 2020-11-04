---
title: Projektibudjettien siirtäminen tilikauden lopussa
description: Tässä artikkelissa on tietoja siitä, miten jäljellä olevat budjetin summat siirretään tuleville vuosille ja budjettirekisteritiedot luodaan.
author: Yowelle
manager: AnnBe
ms.date: 03/23/2020
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
ms.openlocfilehash: 26e013ab99e9a0aeafe25916715ce0ee024df3f7
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/16/2020
ms.locfileid: "4075481"
---
# <a name="transfer-project-budgets-at-fiscal-year-end"></a><span data-ttu-id="a91f5-103">Projektibudjettien siirtäminen tilikauden lopussa</span><span class="sxs-lookup"><span data-stu-id="a91f5-103">Transfer project budgets at fiscal year end</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a91f5-104">Kun työskentelet usean vuoden projektissa, tilikausi lopussa voi olla jäljellä oleva budjetti.</span><span class="sxs-lookup"><span data-stu-id="a91f5-104">When working on a multi-year project, you might have remaining budget at the end of the fiscal year.</span></span> <span data-ttu-id="a91f5-105">Voit siirtää jäljellä olevat budjetin summat tulevalle vuodelle ja luoda budjettirekisteritiedot liittyvien kirjanpitotilien summille.</span><span class="sxs-lookup"><span data-stu-id="a91f5-105">You can transfer the remaining budget amounts to a future year, and create budget register details for the amounts in the associated general ledger accounts.</span></span> <span data-ttu-id="a91f5-106">Ennen jäljellä olevien summien siirtämistä voit tarkastella ja analysoida jäljellä olevia budjetin summia.</span><span class="sxs-lookup"><span data-stu-id="a91f5-106">Before you carry forward the remaining amounts, review and analyze the remaining budget amounts.</span></span>

## <a name="review-and-analyze-remaining-budget-amounts"></a><span data-ttu-id="a91f5-107">Jäljellä olevien budjettisummien tarkistaminen ja analysoiminen</span><span class="sxs-lookup"><span data-stu-id="a91f5-107">Review and analyze remaining budget amounts</span></span>

<span data-ttu-id="a91f5-108">Tarkista projektien vuoden lopun budjettisummat tekemällä seuraavat toimet, mutta älä siirrä summia eteenpäin.</span><span class="sxs-lookup"><span data-stu-id="a91f5-108">Complete the following steps to review the year-end budget amounts for projects, but not carry the amounts forward.</span></span>

1. <span data-ttu-id="a91f5-109">Siirry kohtaan **projektinhallinta ja kirjanpito** > **kausittaiset** > **budjetit** > **Siirrettävät budjetit**.</span><span class="sxs-lookup"><span data-stu-id="a91f5-109">Go to **Project management and accounting** > **Periodic** > **Budgets** > **Carry forward budgets**.</span></span> 
2. <span data-ttu-id="a91f5-110">Tarkista **Projektibudjetin siirtoprosessi** -sivun **vuoden lopun asetukset** -välilehdessä, että **Siirrä jäljellä olevat projektibudjetin summat** ei ole käytössä.</span><span class="sxs-lookup"><span data-stu-id="a91f5-110">On the **Project budget carry-forward process** page, on the **Year-end options** tab, verify that **Carry forward remaining project budget amounts** is not enabled.</span></span>
3. <span data-ttu-id="a91f5-111">Valitse **parametrit** -välilehden **Projektibudjettivuosi** -kentässä tilikausi, jonka jäljellä olevan budjetin summan haluat nähdä.</span><span class="sxs-lookup"><span data-stu-id="a91f5-111">On the **Parameters** tab, in the **Project budget year** field, select the fiscal year for which you want to view the remaining budget amount.</span></span> 
4. <span data-ttu-id="a91f5-112">Valitse **Avaava tilikausi** -kentästä tilivuosi, jolle haluat tarkastella jäljellä olevaa budjettisummaa.</span><span class="sxs-lookup"><span data-stu-id="a91f5-112">In the **Opening fiscal year** field, select the fiscal year for which you want to view the remaining budget amount.</span></span> 
5. <span data-ttu-id="a91f5-113">Valitse **mistä ennustemalli** -kentässä **jäljellä oleva budjetti**.</span><span class="sxs-lookup"><span data-stu-id="a91f5-113">In the **From forecast model** field, select **Remaining budget**.</span></span> 
6. <span data-ttu-id="a91f5-114">Jos haluat lisätä projekteja, jotka vastaavat valittuja ehtoja ja joilla ei ole jäljellä olevaa budjettia, valitse **Näytä nolla jäljellä**.</span><span class="sxs-lookup"><span data-stu-id="a91f5-114">To include projects that meet your selected criteria and have no remaining budget, select **Show zero remaining**.</span></span>  
7. <span data-ttu-id="a91f5-115">Valitse **Valitse budjetit** -välilehdessä **Nouda kaikki budjetit** , jos haluat ladata kaikki valittuja ehtoja vastaavat budjetit, ja valitse sitten **Käsittele**.</span><span class="sxs-lookup"><span data-stu-id="a91f5-115">On the **Select Budgets** tab, select **Retrieve all budgets** to load all budgets that match your selected criteria, and then select **Process**.</span></span> 
8. <span data-ttu-id="a91f5-116">Jos haluat suunnitella tietokantakyselyn, joka lataa tietyn budjettijoukon ruutuun, valitse **Nouda valitut budjetit**.</span><span class="sxs-lookup"><span data-stu-id="a91f5-116">To design a database query that loads a specific set of budgets into the pane, select **Retrieve selected budgets**.</span></span>

<span data-ttu-id="a91f5-117">Jos haluat lisätietoja tietystä ruudun rivistä, valitse rivi ja valitse sitten **Näytä budjetin tiedot** tai **Näytä tilit**.</span><span class="sxs-lookup"><span data-stu-id="a91f5-117">For more information about a specific line in the pane, select the line, and then select **View budget details** or **View accounts**.</span></span>

## <a name="carry-forward-remaining-budget-amounts"></a><span data-ttu-id="a91f5-118">Siirrä jäljellä olevat budjettisummat</span><span class="sxs-lookup"><span data-stu-id="a91f5-118">Carry forward remaining budget amounts</span></span> 

<span data-ttu-id="a91f5-119">Kun käsitellään jäljellä olevia budjettisummia, voit luoda pääkirjanpitoon tapahtumia, joita olet tekemässä.</span><span class="sxs-lookup"><span data-stu-id="a91f5-119">When you process remaining budget amounts, you can create transactions in the general ledger for the amounts that you are carrying forward.</span></span> <span data-ttu-id="a91f5-120">Jos haluat luoda kirjanpitotapahtumia, täytä osan vaiheet, [Siirrä budjettisummat ja luo kirjanpitotapahtumat](#carry-forward).</span><span class="sxs-lookup"><span data-stu-id="a91f5-120">To create general ledger transactions, complete the steps in the section, [Carry forward budget amounts and create general ledger transactions](#carry-forward).</span></span> 

> [!NOTE]
> <span data-ttu-id="a91f5-121">Siirretyt budjettisummat siirretään **ennustemallit** -sivussa valittuun ennustemalliin siirrettäväksi ennuste malliksi.</span><span class="sxs-lookup"><span data-stu-id="a91f5-121">Budget amounts that are carried forward are transferred to the forecast model that is selected in the **Forecast models** page as the carry-forward forecast model.</span></span>  

## <a name="carry-forward-budget-amounts-and-create-general-ledger-transactions"></a><a name="carry-forward"></a><span data-ttu-id="a91f5-122">Siirrä budjettisummat ja luo kirjanpitotapahtumat</span><span class="sxs-lookup"><span data-stu-id="a91f5-122">Carry forward budget amounts and create general ledger transactions</span></span>

1.  <span data-ttu-id="a91f5-123">Valitse **projektinhallinta ja kirjanpito** > **kausittaiset** > **budjetit** > **Siirrettävät budjetit**.</span><span class="sxs-lookup"><span data-stu-id="a91f5-123">Select **Project management and accounting** > **Periodic** > **Budgets** > **Carry forward budgets**.</span></span> 
2. <span data-ttu-id="a91f5-124">Valitse **projektibudjetin siirtoprosessi** -sivulla **vuoden loppu** ja ota sitten **Siirrä jäljellä olevat projektibudjetin summat** käyttöön ja **Luo budjettirekisterimerkinnät kirjanpitoon**.</span><span class="sxs-lookup"><span data-stu-id="a91f5-124">On the **Project budget carry-forward process** page, select **Year-end** , and then enable **Carry forward remaining project budget amounts** and **Create budget register entries in general ledger**.</span></span> 
3. <span data-ttu-id="a91f5-125">Valitse **Parametrit** -välilehdestä **Projektiparametrit** -kenttäryhmä ja valitse seuraava:</span><span class="sxs-lookup"><span data-stu-id="a91f5-125">On the **Parameters** tab, in the **Project parameters** field group, select the following:</span></span>

   - <span data-ttu-id="a91f5-126">**Projektibudjettivuosi** : Valitse sen tilivuoden alku, jolle haluat tarkastella jäljellä olevia budjettisummia.</span><span class="sxs-lookup"><span data-stu-id="a91f5-126">**Project budget year** : Select the beginning of the fiscal year for which you want to view the remaining budget amounts.</span></span> 
   - <span data-ttu-id="a91f5-127">**Voitto ja tappio** : Luo tulostapahtumia pääkirjanpitoon.</span><span class="sxs-lookup"><span data-stu-id="a91f5-127">**Profit and loss** : Create profit and loss transactions in the general ledger.</span></span> 
   -  <span data-ttu-id="a91f5-128">**KET** : Luo keskeneräisten töiden (KET) tapahtumia pääkirjaan.</span><span class="sxs-lookup"><span data-stu-id="a91f5-128">**WIP** : Create Work in Progress (WIP) transactions in the general ledger.</span></span>
   -  <span data-ttu-id="a91f5-129">**Palkanlaskenta** : Palkanlaskennan kohdistustapahtumien luominen pääkirjaan.</span><span class="sxs-lookup"><span data-stu-id="a91f5-129">**Payroll** : Create payroll allocation transactions in the general ledger.</span></span> 

5. <span data-ttu-id="a91f5-130">Anna **Pääkirjanpito** -kenttäryhmässä seuraavat tiedot:</span><span class="sxs-lookup"><span data-stu-id="a91f5-130">In the **General ledger** field group, provide the following information:</span></span> 

   - <span data-ttu-id="a91f5-131">Valitse **Avaava tilikausi** -kentästä tilikausi, jolle haluat siirtää jäljellä olevat budjettisummat projekteille.</span><span class="sxs-lookup"><span data-stu-id="a91f5-131">In the **Opening fiscal year** field, select the fiscal year that you want to transfer remaining budget amounts to for the projects.</span></span> <span data-ttu-id="a91f5-132">Oletusarvo on yksi vuosi **projektin budjettivuosi** -kentän arvon jälkeen.</span><span class="sxs-lookup"><span data-stu-id="a91f5-132">The default value is one year after the value in the **Project budget year** field.</span></span>
   -  <span data-ttu-id="a91f5-133">**Valitse siirrettävä kausi** -kentässä kausi, jolle haluat luoda budjettirekisterin tiedot pääkirjaan.</span><span class="sxs-lookup"><span data-stu-id="a91f5-133">In the **Carry-forward period** field, select the period that you want to create the budget register details for in the general ledger.</span></span> <span data-ttu-id="a91f5-134">Tämä on yleensä ensimmäinen kausi uudella tilikaudella.</span><span class="sxs-lookup"><span data-stu-id="a91f5-134">This is typically the first period in the opening fiscal year.</span></span>

6. <span data-ttu-id="a91f5-135">Anna **Kopioi kohteesta/kohteeseen** -kenttäryhmässä seuraavat tiedot:</span><span class="sxs-lookup"><span data-stu-id="a91f5-135">In the **Copy from/to** field group, provide the following information:</span></span>

   - <span data-ttu-id="a91f5-136">Valitse **mistä ennustemalli** -kentässä projektibudjetin ennustemalli, joka liittyy jäljellä oleviin budjettisummiin, jotka haluat siirtää projekteille.</span><span class="sxs-lookup"><span data-stu-id="a91f5-136">In the **From forecast model** field, select the project budget forecast model associated with the remaining budget amounts you want to transfer for the projects.</span></span> 
   - <span data-ttu-id="a91f5-137">Valitse **Kirjanpidon budjettimalliin** -kentässä kirjanpidonbudjettimalli, joka liittyy jäljellä oleviin budjettisummiin, jotka haluat siirtää kirjanpitoon.</span><span class="sxs-lookup"><span data-stu-id="a91f5-137">In the **To ledger budget model** field, select the ledger budget model associated with the budget amounts you want to transfer to the general ledger.</span></span> 
   -  <span data-ttu-id="a91f5-138">Valitse **Siirrä myyntivaluutta** , jos haluat käyttää projektin myyntivaluuttaa kirjanpitotapahtumissa, jotka luodaan, kun siirrät projektien budjettisummat.</span><span class="sxs-lookup"><span data-stu-id="a91f5-138">Select **Transfer sales currency** to use the project's sales currency for the general ledger transactions that are created when you transfer the budget amounts for the projects.</span></span> <span data-ttu-id="a91f5-139">Jos vaihtoehtoa ei ole valittu, tapahtumat käyttävät kirjanpitovaluuttaa.</span><span class="sxs-lookup"><span data-stu-id="a91f5-139">When the option is not selected, the transactions use the accounting currency.</span></span> 
   -  <span data-ttu-id="a91f5-140">Valitse **Näytä nolla jäljellä** , jos haluat lisätä projektit, joilla ei ole jäljellä olevia budjettisummia, mutta jotka täyttävät muut ehdot, jotka valitset alaruudussa näytettävistä projekteista.</span><span class="sxs-lookup"><span data-stu-id="a91f5-140">Select **Show zero remaining** to include projects that have no remaining budget amounts, but meet the other criteria that you select in the projects displayed in the bottom pane.</span></span>

7. <span data-ttu-id="a91f5-141">Valitse **Valitse budjetit** -välilehdessä **Nouda kaikki budjetit** , jos haluat ladata kaikki valittuja ehtoja vastaavat budjetit.</span><span class="sxs-lookup"><span data-stu-id="a91f5-141">On the **Select Budgets** tab, select **Retrieve all budgets** to load all budgets that match the criteria you selected.</span></span> <span data-ttu-id="a91f5-142">Jos haluat mieluummin suunnitella tietokantakyselyn, joka lataa tietyn projektibudjetin ruutuun, valitse **Nouda valitut budjetit**.</span><span class="sxs-lookup"><span data-stu-id="a91f5-142">If you prefer to design a database query that loads a specific set of project budgets into the pane, select **Retrieve selected budgets**.</span></span>
8. <span data-ttu-id="a91f5-143">Jos haluat käsitellä kutakin käsiteltävää projektia, valitse vaihtoehto projektirivin alussa.</span><span class="sxs-lookup"><span data-stu-id="a91f5-143">For each project that you want to process, select the option at the beginning of the line for the project.</span></span>

    > [!TIP]
    > <span data-ttu-id="a91f5-144">Jos haluat valita kaikki projektit tai useimmat niistä, valitse vasemmassa yläkulmassa oleva valintaruutu.</span><span class="sxs-lookup"><span data-stu-id="a91f5-144">To select all or most of the projects, select the check mark in the top upper-left corner.</span></span> <span data-ttu-id="a91f5-145">Jos et halua käsitellä yhtään projektia, poista kyseisen projektin valintamerkki.</span><span class="sxs-lookup"><span data-stu-id="a91f5-145">To exclude processing any project, clear the check mark for that project.</span></span>

9. <span data-ttu-id="a91f5-146">Jos haluat siirtää valittujen projektien jäljellä olevat budjettisummat valittuun tilikauteen ja luoda budjettirekisterin tiedot pääkirjaan, valitse **prosessi**.</span><span class="sxs-lookup"><span data-stu-id="a91f5-146">To transfer the remaining budget amounts for the selected projects to the selected fiscal year and create budget register details in the general ledger, select **Process**.</span></span>

## <a name="carry-forward-budget-amounts-without-creating-general-ledger-transactions"></a><span data-ttu-id="a91f5-147">Siirrä budjettisummat luomatta kirjanpitotapahtumia</span><span class="sxs-lookup"><span data-stu-id="a91f5-147">Carry forward budget amounts without creating general ledger transactions</span></span>

1. <span data-ttu-id="a91f5-148">Siirry kohtaan **projektinhallinta ja kirjanpito** > **kausittaiset** > **budjetit** > **Siirrettävät budjetit**.</span><span class="sxs-lookup"><span data-stu-id="a91f5-148">Go to **Project management and accounting** > **Periodic** > **Budgets** > **Carry forward budgets**.</span></span>
2. <span data-ttu-id="a91f5-149">Valitse **Projektibudjetin siirtoprosessi** -sivun **vuoden lopun asetukset** -kentässä **Siirrä jäljellä olevat projektibudjetin summat**.</span><span class="sxs-lookup"><span data-stu-id="a91f5-149">On the **Project budget carry-forward process** page, in the **Year-end options** field, select **Carry forward remaining project budget amounts**.</span></span>
3. <span data-ttu-id="a91f5-150">Valitse **parametrit** -ryhmän **Projektibudjettivuosi** -kentässä tilikausi, jonka jäljellä olevat budjettisummat haluat nähdä.</span><span class="sxs-lookup"><span data-stu-id="a91f5-150">In the **Parameters** group, in the **Project budget year** field, select the fiscal year for which you want to view the remaining budget amounts.</span></span>
4. <span data-ttu-id="a91f5-151">Anna **Kopioi kohteesta/kohteeseen** -ryhmässä seuraavat tiedot:</span><span class="sxs-lookup"><span data-stu-id="a91f5-151">In the **Copy from/to** group, provide the following information:</span></span>

   - <span data-ttu-id="a91f5-152">Valitse **mistä ennustemalli** -kentässä projektibudjetin ennustemalli, joka liittyy jäljellä oleviin budjettisummiin, jotka haluat siirtää projekteille.</span><span class="sxs-lookup"><span data-stu-id="a91f5-152">In the **From forecast model** field, select the project budget forecast model that is associated with the remaining budget amounts that you want to transfer for the projects.</span></span> 
   - <span data-ttu-id="a91f5-153">Valitse **Näytä nolla jäljellä** , jos haluat sisällyttää hankkeita, joissa ei ole jäljellä olevia budjettisummia, mutta jotka täyttävät muut valitsemasi ehdot.</span><span class="sxs-lookup"><span data-stu-id="a91f5-153">Select **Show zero remaining** to include projects that have no remaining budget amounts, but that meet the other criteria you selected.</span></span>
   - <span data-ttu-id="a91f5-154">Valitse **Valitse budjetit** -ryhmässä **Nouda kaikki budjetit** , jos haluat ladata kaikki valittuja ehtoja vastaavat budjetit.</span><span class="sxs-lookup"><span data-stu-id="a91f5-154">In the **Select Budgets** group, select **Retrieve all budgets** to load all budgets that match the criteria that you selected.</span></span> <span data-ttu-id="a91f5-155">Jos haluat suunnitella tietokantakyselyn, joka lataa tietyn projektibudjettijoukon ruutuun, valitse **Nouda valitut budjetit**.</span><span class="sxs-lookup"><span data-stu-id="a91f5-155">To design a database query that loads a specific set of project budgets into the pane, select **Retrieve selected budgets**.</span></span>

5. <span data-ttu-id="a91f5-156">Jos haluat käsitellä kutakin käsiteltävää projektia, valitse vaihtoehto projektirivin alussa.</span><span class="sxs-lookup"><span data-stu-id="a91f5-156">For each project that you want to process, select the option at the beginning of the line for the project.</span></span> 
6. <span data-ttu-id="a91f5-157">Valitse **prosessi** , jos haluat siirtää valittujen projektien jäljellä olevat budjettisummat valittuun tilikauteen.</span><span class="sxs-lookup"><span data-stu-id="a91f5-157">Select **Process** to transfer the remaining budget amounts for the selected projects to the selected fiscal year.</span></span>

