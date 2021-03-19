---
title: Etenemiseen perustuvien edistyksellisten hinnoittelusopimusten luominen
description: Tässä aiheessa kerrotaan, miten projektisopimuksia luodaan, jotta asiakkaille voidaan luoda laskuja valmiin työn prosenttimäärän perusteella.
author: RadhikaRS
manager: AnnBe
ms.date: 03/26/2020
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
ms.openlocfilehash: b1de330df8cf85ed30c0ee4e4f2f2fe74d05dbff
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5289500"
---
# <a name="create-advanced-contracts-for-billing-based-on-progress"></a><span data-ttu-id="d279a-103">Etenemiseen perustuvien edistyksellisten hinnoittelusopimusten luominen</span><span class="sxs-lookup"><span data-stu-id="d279a-103">Create advanced contracts for billing based on progress</span></span>
[!include [banner](../includes/banner.md)]

<span data-ttu-id="d279a-104">Tässä aiheessa kerrotaan, miten projektisopimuksia luodaan, jotta asiakkaille voidaan luoda laskuja valmiin työn prosenttimäärän perusteella.</span><span class="sxs-lookup"><span data-stu-id="d279a-104">This topic explains how to create project contracts so that you can create invoices for customers, based on a percentage of completed work.</span></span> <span data-ttu-id="d279a-105">Laskun summat lasketaan automaattisesti projektille määritettyjen budjettiluokkien mukaan.</span><span class="sxs-lookup"><span data-stu-id="d279a-105">Invoice amounts are automatically calculated for the budget categories of work that you set up for a project.</span></span> <span data-ttu-id="d279a-106">Laskun ajoitus määritetään, kun neuvotellaan projektisopimuksesta asiakkaan kanssa.</span><span class="sxs-lookup"><span data-stu-id="d279a-106">The invoice timing is set when you negotiate the project contract with the customer.</span></span>

<span data-ttu-id="d279a-107">Tämän aiheen ohjeiden avulla voit määrittää palvelusopimuksen, siihen liittyvän projektin ja laskutussäännöt, jotka laskevat projektin budjettiluokkien laskujen summat.</span><span class="sxs-lookup"><span data-stu-id="d279a-107">Use the procedures in this topic to set up a contract, an associated project, and the billing rules that calculate invoice amounts for the budget categories of work that you set up for the project.</span></span>

<span data-ttu-id="d279a-108">Kun olet luonut palvelusopimuksen ja projektin, voit määrittää projektin tiedot.</span><span class="sxs-lookup"><span data-stu-id="d279a-108">After you've created the contract and the project, you can set up the details of the project.</span></span> <span data-ttu-id="d279a-109">Voit esimerkiksi määrittää aktiviteetteja ja delegoida työntekijöitä projektiin.</span><span class="sxs-lookup"><span data-stu-id="d279a-109">For example, you can define activities and assign workers to the project.</span></span>

## <a name="example"></a><span data-ttu-id="d279a-110">Esimerkki:</span><span class="sxs-lookup"><span data-stu-id="d279a-110">Example</span></span>

<span data-ttu-id="d279a-111">Organisaatiosi on ohjelmistokehitysyritys.</span><span class="sxs-lookup"><span data-stu-id="d279a-111">Your organization is a software development firm.</span></span> <span data-ttu-id="d279a-112">Sitoudut kehittämään palkanlaskentapaketin asiakkaalle 20 000 Yhdysvaltain dollarin (USD) kokonaismaksua vastaan.</span><span class="sxs-lookup"><span data-stu-id="d279a-112">You agree to develop a payroll accounting package for a customer for a total fee of 20,000 US dollars (USD).</span></span> <span data-ttu-id="d279a-113">Organisaatiosi sitoutuu laskuttamaan asiakasta samalla, kun se täyttää tietyt projektin prosenttiosuudet.</span><span class="sxs-lookup"><span data-stu-id="d279a-113">Your organization agrees to invoice the customer as you complete specific percentages of the project.</span></span> <span data-ttu-id="d279a-114">Voit määrittää työlle seuraavat projektiluokat, jotta voit käyttää niitä laskutusprosessissa:</span><span class="sxs-lookup"><span data-stu-id="d279a-114">You set up the following project categories for the work, so that you can use them in the billing process:</span></span>

- <span data-ttu-id="d279a-115">Konsultointipalvelut</span><span class="sxs-lookup"><span data-stu-id="d279a-115">Consulting</span></span>
- <span data-ttu-id="d279a-116">Suunnittele</span><span class="sxs-lookup"><span data-stu-id="d279a-116">Design</span></span>
- <span data-ttu-id="d279a-117">Asennus</span><span class="sxs-lookup"><span data-stu-id="d279a-117">Installation</span></span>

<span data-ttu-id="d279a-118">Voit myös määrittää laskutussäännöt, jotka laskevat automaattisesti kullekin luokalle valmiin projektityön prosenttimäärän laskusummat.</span><span class="sxs-lookup"><span data-stu-id="d279a-118">You also set up billing rules that automatically calculate the invoice amounts for the percentage of project work that is completed in each category.</span></span>

<span data-ttu-id="d279a-119">Budjettipäällikkö luo budjetin projektiluokille.</span><span class="sxs-lookup"><span data-stu-id="d279a-119">The budget manager creates a budget for the project categories.</span></span> <span data-ttu-id="d279a-120">Valmiin työn määrä lasketaan automaattisesti prosentteina todellisesta työstä budjetoitujen summien perusteella.</span><span class="sxs-lookup"><span data-stu-id="d279a-120">The amount of completed work is automatically calculated as a percentage of actual work in comparison to the budgeted amounts.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="d279a-121">Edellytykset</span><span class="sxs-lookup"><span data-stu-id="d279a-121">Prerequisites</span></span>

<span data-ttu-id="d279a-122">Ennen kuin luot laskutussääntöjä käyttävän projektin, sinun täytyy määrittää numerosarjat laskutussäännöille ja maksukirjauskansiolle, jota käytetään edistymiseen perustuvan laskutuksen kirjauksessa.</span><span class="sxs-lookup"><span data-stu-id="d279a-122">Before you create a project that uses billing rules, you must set up the number sequences for billing rules and a fee journal that is used to post progress billings.</span></span>

1. <span data-ttu-id="d279a-123">Siirry kohtaan **Projektinhallinta ja kirjanpito** \> **Määritys** \> **Projektinhallinnan ja kirjanpidon parametrit**.</span><span class="sxs-lookup"><span data-stu-id="d279a-123">Go to **Project management and accounting** \> **Setup** \> **Project management and accounting parameters**.</span></span>
2. <span data-ttu-id="d279a-124">Määritä **projektinhallinta ja kirjanpidon parametrit** -sivun **numerosarjat**-välilehdessä numerosarja, jota haluat käyttää, kun laskutussääntöjä luodaan.</span><span class="sxs-lookup"><span data-stu-id="d279a-124">On the **Project management and accounting parameters** page, on the **Number sequences** tab, set up the number sequence that you want to use when billing rules are created.</span></span>
3. <span data-ttu-id="d279a-125">Siirry kohtaan **Projektinhallinta ja kirjanpito** \> **Kirjauskansiot** \> **Maksu**.</span><span class="sxs-lookup"><span data-stu-id="d279a-125">Go to **Project management and accounting** \> **Journals** \> **Fee**.</span></span>
4. <span data-ttu-id="d279a-126">Valitse **maksukirjauskansio**-sivulla **Uusi** ja kirjoita kirjauskansion nimi.</span><span class="sxs-lookup"><span data-stu-id="d279a-126">On the **Fee journal** page, select **New**, and enter the journal name.</span></span>

## <a name="create-a-contract-for-progress-billings"></a><span data-ttu-id="d279a-127">Luo sopimus edistymälaskutusta varten</span><span class="sxs-lookup"><span data-stu-id="d279a-127">Create a contract for progress billings</span></span>

<span data-ttu-id="d279a-128">Tämän menettelyn avulla voit luoda projektisopimuksen kiinteähintaiselle projektille.</span><span class="sxs-lookup"><span data-stu-id="d279a-128">Use this procedure to create a project contract for a fixed-price project.</span></span> <span data-ttu-id="d279a-129">Projektilasku luodaan, kun projektissa valmis työ saavuttaa määritetyn prosenttiosuuden.</span><span class="sxs-lookup"><span data-stu-id="d279a-129">You create a project invoice when the work that is completed on the project reaches a specified percentage.</span></span>

1. <span data-ttu-id="d279a-130">Siirry kohtaan **Projektinhallinta ja kirjanpito** \> **projektit** \> **Projektiyhteyshenkilöt**.</span><span class="sxs-lookup"><span data-stu-id="d279a-130">Go to **Project management and accounting** \> **Projects** \> **Project contracts**.</span></span>
2. <span data-ttu-id="d279a-131">Valitse **Projektisopimukset**-sivulla **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="d279a-131">On the **Project contracts** page, select **New**.</span></span>
3. <span data-ttu-id="d279a-132">Määritä **Uusi projekti sopimus** -valintaikkunassa seuraavat kentät:</span><span class="sxs-lookup"><span data-stu-id="d279a-132">In the **New project contract** dialog box, set the following fields:</span></span>

    - <span data-ttu-id="d279a-133">**Nimi**</span><span class="sxs-lookup"><span data-stu-id="d279a-133">**Name**</span></span>
    - <span data-ttu-id="d279a-134">**Rahoitustyyppi**</span><span class="sxs-lookup"><span data-stu-id="d279a-134">**Funding type**</span></span>
    - <span data-ttu-id="d279a-135">**Rahoituslähde**</span><span class="sxs-lookup"><span data-stu-id="d279a-135">**Funding source**</span></span>
    - <span data-ttu-id="d279a-136">**Myyntivaluutta** – tätä valuuttaa käytetään oletusarvon mukaan projektisopimukseen liitetyistä asiakaslaskuista.</span><span class="sxs-lookup"><span data-stu-id="d279a-136">**Sales currency** – By default, this currency is used for customer invoices that are associated with the project contract.</span></span> <span data-ttu-id="d279a-137">Voit kuitenkin muuttaa tietyn asiakaslaskun myyntivaluuttaa.</span><span class="sxs-lookup"><span data-stu-id="d279a-137">However, you can change the sales currency on a specific customer invoice.</span></span>

4. <span data-ttu-id="d279a-138">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="d279a-138">Select **OK**.</span></span> <span data-ttu-id="d279a-139">Tiedot kopioidaan **Projektisopimukset**-sivun otsikkoon.</span><span class="sxs-lookup"><span data-stu-id="d279a-139">The information is copied to the header of the **Project contracts** page.</span></span>
5. <span data-ttu-id="d279a-140">Täytä **Projektisopimukset**-sivulla loput projektin pakolliset tiedot.</span><span class="sxs-lookup"><span data-stu-id="d279a-140">On the **Project contracts** page, fill in the rest of the required information for the project.</span></span>

## <a name="create-a-project-for-progress-billings"></a><span data-ttu-id="d279a-141">Luo projekti edistymälaskutusta varten</span><span class="sxs-lookup"><span data-stu-id="d279a-141">Create a project for progress billings</span></span>

<span data-ttu-id="d279a-142">Seuraavien vaiheiden mukaisesti voit luoda projektin ja kaikki projektisopimukseen liittyvät aliprojektit.</span><span class="sxs-lookup"><span data-stu-id="d279a-142">Follow these steps to create a project and any subprojects that are associated with a project contract.</span></span>

1. <span data-ttu-id="d279a-143">Siirry kohtaan **Projektinhallinta ja kirjanpito** \> **Projektit** \> **Kaikki projektit**.</span><span class="sxs-lookup"><span data-stu-id="d279a-143">Go to **Project management and accounting** \> **Projects** \> **All projects**.</span></span>
2. <span data-ttu-id="d279a-144">Valitse **Kaikki projektit**-sivulla **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="d279a-144">On the **All projects** page, select **New**.</span></span>
3. <span data-ttu-id="d279a-145">Valitse **Uusi projekti** -valintaikkunan **Projektityyppi**-kentässä **Aika ja materiaali**.</span><span class="sxs-lookup"><span data-stu-id="d279a-145">In the **New project** dialog box, in the **Project type** field, select **Time and material**.</span></span>
4. <span data-ttu-id="d279a-146">Valitse projektiryhmä.</span><span class="sxs-lookup"><span data-stu-id="d279a-146">Select a project group.</span></span> <span data-ttu-id="d279a-147">Projektiryhmä määrittää ryhmälle delegoitujen projektien kirjaustiedot.</span><span class="sxs-lookup"><span data-stu-id="d279a-147">A project group defines the posting information for the projects that are assigned to the group.</span></span>
5. <span data-ttu-id="d279a-148">Valitse **Luo projekti**.</span><span class="sxs-lookup"><span data-stu-id="d279a-148">Select **Create project**.</span></span>
6. <span data-ttu-id="d279a-149">Kun projekti on luotu, määritä projektin vaiheeksi **tekeillä**.</span><span class="sxs-lookup"><span data-stu-id="d279a-149">After the project is created, set the project stage to **In process**.</span></span>

## <a name="create-a-budget-for-a-project"></a><span data-ttu-id="d279a-150">Budjetin luominen projektiin</span><span class="sxs-lookup"><span data-stu-id="d279a-150">Create a budget for a project</span></span>

<span data-ttu-id="d279a-151">Budjettiluokkia käytetään laskettaessa laskusummat kullekin luokalle valmistuneesta työstä.</span><span class="sxs-lookup"><span data-stu-id="d279a-151">Budget categories are used to automatically calculate the invoice amounts for the percentage of work that is completed for each category.</span></span> <span data-ttu-id="d279a-152">Seuraavien vaiheiden mukaisesti voit luoda arvioidut kustannusluokat.</span><span class="sxs-lookup"><span data-stu-id="d279a-152">Follow these steps to create budget categories for the estimated costs.</span></span>

1. <span data-ttu-id="d279a-153">Siirry kohtaan **Projektinhallinta ja kirjanpito** \> **Projektit** \> **Kaikki projektit**.</span><span class="sxs-lookup"><span data-stu-id="d279a-153">Go to **Project management and accounting** \> **Projects** \> **All projects**.</span></span>
2. <span data-ttu-id="d279a-154">Valitse ja avaa haluamasi projekti **kaikki projektit** -sivulla.</span><span class="sxs-lookup"><span data-stu-id="d279a-154">On the **All projects** page, select and open the project that you want.</span></span>
3. <span data-ttu-id="d279a-155">Valitse **projektit**-sivun toimintoruudun **suunnitelma**-välilehden **budjetti**-ryhmässä **Projektibudjetti**.</span><span class="sxs-lookup"><span data-stu-id="d279a-155">On the **Projects** page, on the Action Pane, on the **Plan** tab, in the **Budget** group, select **Project budget**.</span></span>
4. <span data-ttu-id="d279a-156">Kirjoita **projektibudjetti**-sivulle arvioidut kustannukset kullekin projektiluokalle.</span><span class="sxs-lookup"><span data-stu-id="d279a-156">On the **Project budget** page, enter an estimated cost for each category in the project.</span></span>

## <a name="create-billing-rules-for-progress-billings"></a><span data-ttu-id="d279a-157">Laskutussääntöjen luominen keskeneräisiä laskuja varten</span><span class="sxs-lookup"><span data-stu-id="d279a-157">Create billing rules for progress billings</span></span>

1. <span data-ttu-id="d279a-158">Siirry kohtaan **Projektinhallinta ja kirjanpito** \> **projektit** \> **Projektiyhteyshenkilöt**.</span><span class="sxs-lookup"><span data-stu-id="d279a-158">Go to **Project management and accounting** \> **Projects** \> **Project contracts**.</span></span>
2. <span data-ttu-id="d279a-159">Avaa projektisopimus **Projektisopimukset**-luettelosivulla.</span><span class="sxs-lookup"><span data-stu-id="d279a-159">On the **Project contracts** page, select and open a project contract.</span></span>
3. <span data-ttu-id="d279a-160">Valitse projektisopimus-sivun **laskutussäännöt**-pikavälilehdessä **Lisää**.</span><span class="sxs-lookup"><span data-stu-id="d279a-160">On the project contract page, on the **Billing rules** FastTab, select **Add**.</span></span>
4. <span data-ttu-id="d279a-161">Valitse **Laskutussääntö**-sivun **rivityyppi**-kentässä **edistyminen**.</span><span class="sxs-lookup"><span data-stu-id="d279a-161">On the **Billing rule** page, in the **Line type** field, select **Progress**.</span></span>
5. <span data-ttu-id="d279a-162">Kirjoita **laskutussääntörivin tiedot** -pikavälilehden **sopimuksen arvo** -kenttään palvelusopimuksen kokonaisarvo.</span><span class="sxs-lookup"><span data-stu-id="d279a-162">On the **Billing rule line details** FastTab, in the **Contract value** field, enter the total value of the contract.</span></span>
6. <span data-ttu-id="d279a-163">Valitse **luokka**-kentässä luokka, johon maksutapahtuma kirjataan.</span><span class="sxs-lookup"><span data-stu-id="d279a-163">In the **Category** field, select the category to post the fee transaction to.</span></span>
7. <span data-ttu-id="d279a-164">Valitse **projekti**-kentästä projekti, joka käyttää tätä laskutussääntöä.</span><span class="sxs-lookup"><span data-stu-id="d279a-164">In the **Project** field, select the project that uses this billing rule.</span></span>
8. <span data-ttu-id="d279a-165">Valinnainen: voit delegoida laskutussäännön lisäprojekteille.</span><span class="sxs-lookup"><span data-stu-id="d279a-165">Optional: Assign the billing rule to additional projects.</span></span> <span data-ttu-id="d279a-166">Valitse **projekti**-pikavälilehden **käytettävissä olevat projektit** -osasta ja valitse sitten oikea nuolipainike, kun haluat lisätä projektin **Valitut projektit** -osaan.</span><span class="sxs-lookup"><span data-stu-id="d279a-166">On the **Project** FastTab, in the **Available projects** section, select a project, and then select the right arrow button to add the project to the **Selected projects** section.</span></span>
9. <span data-ttu-id="d279a-167">Valinnainen: Laske sen prosenttimäärän summa, jonka asiakas pidättää maksuista laskulla.</span><span class="sxs-lookup"><span data-stu-id="d279a-167">Optional: Calculate the percentage amount that the customer withholds from payments on an invoice.</span></span> <span data-ttu-id="d279a-168">Valitse **maksun pidätysehdot** -pikavälilehdessä rahoituslähde ja kirjoita sitten **pidätysprosentti** -kenttään pidätysprosentti.</span><span class="sxs-lookup"><span data-stu-id="d279a-168">On the **Payment retention terms** FastTab, select the funding source, and then, in the **Retention percentage** field, enter the retention percentage.</span></span>
10. <span data-ttu-id="d279a-169">Toista nämä vaiheet, kun haluat luoda projektisopimukselle lisää laskutussääntöjä.</span><span class="sxs-lookup"><span data-stu-id="d279a-169">Repeat these steps to create additional billing rules for the project contract.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]