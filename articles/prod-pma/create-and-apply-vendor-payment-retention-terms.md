---
title: Toimittajan maksun pidätysehtojen luominen ja käyttäminen
description: Tässä aiheessa on tietoja toimittajamaksujen säilytysehtojen määrittämisestä ja ylläpidosta.
author: Yowelle
manager: AnnBe
ms.date: 05/26/2020
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
ms.openlocfilehash: 1970a24a5073de6af43db1f1c068332c9ba9c8fe
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/16/2020
ms.locfileid: "4075485"
---
# <a name="create-and-apply-vendor-payment-retention-terms"></a><span data-ttu-id="e1de5-103">Toimittajan maksun pidätysehtojen luominen ja käyttäminen</span><span class="sxs-lookup"><span data-stu-id="e1de5-103">Create and apply vendor payment retention terms</span></span>

[!include [banner](../includes/banner.md)] 

<span data-ttu-id="e1de5-104">Toimittajamaksun pidätysehtojen määrittäminen projektille on hyödyllistä silloin, kun organisaatio haluaa säilyttää osan toimittajalle tehdyistä maksuista.</span><span class="sxs-lookup"><span data-stu-id="e1de5-104">Setting up vendor payment retention terms for a project is useful when your organization wants to retain part of the payments made to a vendor.</span></span> <span data-ttu-id="e1de5-105">Jos esimerkiksi haluat pidättää maksun toimittajalle, kunnes toimitetut tuotteet vastaavat odotuksiasi.</span><span class="sxs-lookup"><span data-stu-id="e1de5-105">For example, when you want to hold payment to a vendor until the products delivered meet your expectations.</span></span> <span data-ttu-id="e1de5-106">Toimittajan maksun säilytysehdot voidaan määrittää, kun neuvotellaan toimittajasopimuksesta.</span><span class="sxs-lookup"><span data-stu-id="e1de5-106">Vendor payment retention terms can be specified when you negotiate a vendor contract.</span></span>

## <a name="create-vendor-payment-retention-terms"></a><span data-ttu-id="e1de5-107">Toimittajan maksun pidätysehtojen luominen</span><span class="sxs-lookup"><span data-stu-id="e1de5-107">Create vendor payment retention terms</span></span>

<span data-ttu-id="e1de5-108">Voit syöttää toimittajan maksun prosenttiosuuden pidätyksestä ja prosenttiosuuden aiemmin pidätetyistä vapautettavista summista.</span><span class="sxs-lookup"><span data-stu-id="e1de5-108">You can enter the percentage of vendor payment for retention and the percentage of the previously retained amounts to be released.</span></span> <span data-ttu-id="e1de5-109">Summat säilytetään automaattisesti toimittajan laskuissa, kunnes palvelusopimus saavuttaa määritetyn valmistumisasteen.</span><span class="sxs-lookup"><span data-stu-id="e1de5-109">Amounts are automatically retained on vendor invoices until the contract reaches the specified state of completion.</span></span> <span data-ttu-id="e1de5-110">Kun olet määrittänyt säilytysehdot, voit kohdistaa ne mihin tahansa kyseisen toimittajan projektiin.</span><span class="sxs-lookup"><span data-stu-id="e1de5-110">After you set up the retention terms, you can apply them to any project for that vendor.</span></span>

<span data-ttu-id="e1de5-111">Seuraavien vaiheiden avulla voit määrittää ja ylläpitää toimittajan maksujen säilytysehtoja.</span><span class="sxs-lookup"><span data-stu-id="e1de5-111">Use the following steps to set up and maintain retention terms for vendor payments.</span></span> 

1. <span data-ttu-id="e1de5-112">Siirry kohtaan **projektinhallinta ja kirjanpito** > **säilyttäminen** > **Toimittajamaksujen säilytysehdot**.</span><span class="sxs-lookup"><span data-stu-id="e1de5-112">Go to **Project management and accounting** > **Retention** > **Vendor payment retention terms**.</span></span>
2. <span data-ttu-id="e1de5-113">Valitse **Uusi** , jos haluat lisätä uuden toimittajan säilytysehdon.</span><span class="sxs-lookup"><span data-stu-id="e1de5-113">Select **New** to add a new vendor retention term.</span></span> <span data-ttu-id="e1de5-114">Uuden termin **sääntötunnus** -arvo syötetään automaattisesti.</span><span class="sxs-lookup"><span data-stu-id="e1de5-114">The **Rule ID** value for the new term is automatically entered.</span></span> 
3. <span data-ttu-id="e1de5-115">Kirjoita lyhyt kuvaus **kuvaus** -kenttään ja valitse **ehdot** -pikavälilehdessä **Lisää rivi** , jos haluat määrittää termin arvot seuraaville:</span><span class="sxs-lookup"><span data-stu-id="e1de5-115">Enter a brief description in the **Description** field, and on the **Terms** FastTab, select **Add line** to enter term values for the following:</span></span>

   - <span data-ttu-id="e1de5-116">**Toimitettujen yksiköiden prosenttimäärä** : Kirjoita termin valmistumisprosentti.</span><span class="sxs-lookup"><span data-stu-id="e1de5-116">**Percentage of units delivered** : Enter a percentage of completion for the term.</span></span> <span data-ttu-id="e1de5-117">Summat säilytetään automaattisesti toimittajan laskuissa, kunnes projektin valmistumisvaihe on sama kuin määritetty prosenttiosuus.</span><span class="sxs-lookup"><span data-stu-id="e1de5-117">Amounts are automatically retained on vendor invoices until the project stage of completion is equal to the specified percentage.</span></span> <span data-ttu-id="e1de5-118">Jos esimerkiksi kirjoitat 50,00, summat pidätetään, kunnes projektista on 50 prosenttia valmiina.</span><span class="sxs-lookup"><span data-stu-id="e1de5-118">For example, if you enter 50.00, amounts are retained until the project is 50 percent completed.</span></span>
   - <span data-ttu-id="e1de5-119">**Pidätettävä prosentti** : Anna toimittajan laskun määrän pidätettävä prosenttiosuus.</span><span class="sxs-lookup"><span data-stu-id="e1de5-119">**Percentage to retain** : Enter a percentage of the vendor invoice amount to be retained.</span></span> <span data-ttu-id="e1de5-120">Jos esimerkiksi kirjoitat 10,00, 10 prosenttia toimittajan laskusta pidätetään, kunnes projektin valmistumisprosentti on sama kuin määritetty **toimitetut yksiköt prosentteina -kentässä**.</span><span class="sxs-lookup"><span data-stu-id="e1de5-120">For example, if you enter 10.00, then 10 percent of the amount on a vendor invoice is retained until the project reaches the percentage of completion as set in the **Percentage of units delivered field**.</span></span>
   - <span data-ttu-id="e1de5-121">**Vapautettava prosentti** : Valitse **Lisää rivi** , jos haluat määrittää, kuinka monta prosenttia aiemmin kertyneistä summista vapautetaan valitun projektin valmistumisasteen mukaan.</span><span class="sxs-lookup"><span data-stu-id="e1de5-121">**Percentage to release** : Select **Add line** to enter a percentage of any previously retained amounts to be released for the selected level of project completion.</span></span>

> [!NOTE]
> <span data-ttu-id="e1de5-122">Jos projektin valmistumisen eri tasoilla on useampi kuin yksi välitavoite, kirjoita kullekin säilytyssäännölle erillinen toimittajan säilytysajan rivi.</span><span class="sxs-lookup"><span data-stu-id="e1de5-122">If you have more than one milestone for different levels of project completion, enter a separate vendor retention term line for each retention rule.</span></span> <span data-ttu-id="e1de5-123">Kullakin rivillä voidaan määrittää eri säilytysprosentti ja eri vapautusprosentti kullekin projektin valmistumistasolle.</span><span class="sxs-lookup"><span data-stu-id="e1de5-123">Each line can specify a different retention percentage and a different release percentage for each designated level of project completion.</span></span>

<span data-ttu-id="e1de5-124">Kun olet luonut toimittajan pidätysehdot, voit kohdistaa ehdot projektiin.</span><span class="sxs-lookup"><span data-stu-id="e1de5-124">After you create vendor retention terms for a vendor, you can apply the terms to a project.</span></span>

## <a name="apply-vendor-retention-terms-to-a-project"></a><span data-ttu-id="e1de5-125">Toimittajan säilytysehtojen soveltaminen projektiin</span><span class="sxs-lookup"><span data-stu-id="e1de5-125">Apply vendor retention terms to a project</span></span>

1. <span data-ttu-id="e1de5-126">Siirry kohtaan **projektinhallinta- ja kirjanpito** > **projektit** > **kaikki projektit** ja avaa projekti projektiluettelo-sivulla.</span><span class="sxs-lookup"><span data-stu-id="e1de5-126">Go to **Project management and accounting** > **Projects** > **All projects** and open a project from the project list page.</span></span>
2. <span data-ttu-id="e1de5-127">Valitse **toimittajasopimukset** -pikavälilehdessä **Lisää rivi**.</span><span class="sxs-lookup"><span data-stu-id="e1de5-127">On the **Vendor agreements** FastTab, select **Add line**.</span></span>
3. <span data-ttu-id="e1de5-128">Valitse **tilikoodikentässä** jokin seuraavista vaihtoehdoista:</span><span class="sxs-lookup"><span data-stu-id="e1de5-128">In the **Account code field** , select one of the following options:</span></span> 

   - <span data-ttu-id="e1de5-129">**Taulukko** : toimittajan säilytysehdot koskevat yhtä toimittajaa.</span><span class="sxs-lookup"><span data-stu-id="e1de5-129">**Table** : The vendor retention terms apply to a single vendor.</span></span>
   - <span data-ttu-id="e1de5-130">**Ryhmä** : toimittajan säilytysehdot koskevat kaikkia toimittajaryhmän toimittajia.</span><span class="sxs-lookup"><span data-stu-id="e1de5-130">**Group** : The vendor retention terms apply to all vendors in a vendor group.</span></span>
   - <span data-ttu-id="e1de5-131">**Kaikki** : Toimittajan säilytysehdot koskevat kaikkia toimittajia.</span><span class="sxs-lookup"><span data-stu-id="e1de5-131">**All** : The vendor retention terms apply to all vendors.</span></span>

4. <span data-ttu-id="e1de5-132">Valitse **toimittaja/toimittajaryhmä -kentässä** toimittaja tai toimittajaryhmä, johon toimittajan säilytysehtoja sovelletaan.</span><span class="sxs-lookup"><span data-stu-id="e1de5-132">In the **Vendor/Vendor group field** , select the vendor or vendor group to which the vendor retention terms apply.</span></span> <span data-ttu-id="e1de5-133">Jos valitsit edellisessä vaiheessa **Kaikki** , tämä kenttä ei ole käytettävissä.</span><span class="sxs-lookup"><span data-stu-id="e1de5-133">If you selected **All** in the previous step, this field is unavailable.</span></span>
5. <span data-ttu-id="e1de5-134">**Valitse toimittajan säilytysehdot** -kentässä edellisessä toimintosarjassa luomasi säilytysehdot.</span><span class="sxs-lookup"><span data-stu-id="e1de5-134">In the **Vendor retention terms** field, select the retention terms that you created in the previous procedure.</span></span>
6. <span data-ttu-id="e1de5-135">Jos projektilla on myös toimittajalle määritetty maksu, kun maksettu (PWP) -ehdot, kirjoita projektin kynnysprosentti **PWP-kynnysprosentti** -kenttään.</span><span class="sxs-lookup"><span data-stu-id="e1de5-135">If the project also has pay-when-paid (PWP) terms set up for the vendor, enter the threshold percentage for the project in the **PWP threshold percentage** field.</span></span>

<span data-ttu-id="e1de5-136">Toimittajan säilytysehdot näkyvät myös toimittajalle luotavien ostotilausten yhteydessä.</span><span class="sxs-lookup"><span data-stu-id="e1de5-136">The vendor retention terms are also displayed on purchase orders that you create for the vendor.</span></span>
