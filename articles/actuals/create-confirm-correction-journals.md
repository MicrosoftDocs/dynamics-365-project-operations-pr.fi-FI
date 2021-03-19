---
title: Oikaisukirjauskansioiden luominen ja vahvistaminen
description: Tässä aiheessa on tietoja oikaisukirjauskansion luomisesta ja vahvistamisesta.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 8ca35d1e66cbacaf65b7cd43493e3588f213788e
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5276929"
---
# <a name="create-and-confirm-correction-journals"></a><span data-ttu-id="010dc-103">Oikaisukirjauskansioiden luominen ja vahvistaminen</span><span class="sxs-lookup"><span data-stu-id="010dc-103">Create and confirm Correction journals</span></span>

<span data-ttu-id="010dc-104">_**Koskee:** Project Operationsin resurssiin / muuhun kuin resurssiin perustuvia skenaarioita, Lite-käyttöönotto-kaupasta proformalaskutukseen_</span><span class="sxs-lookup"><span data-stu-id="010dc-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="010dc-105">Silloin tällöin aika- tai kulumerkintä saatetaan syöttää virheellisesti.</span><span class="sxs-lookup"><span data-stu-id="010dc-105">Occasionally a time or expense entry may be entered incorrectly.</span></span> <span data-ttu-id="010dc-106">Esimerkiksi konsultti voi valita väärän päivämäärän luodessaan aikamerkintää tai sekoittaa numerot keskenään syöttäessään kulumerkintää.</span><span class="sxs-lookup"><span data-stu-id="010dc-106">For example, a consultant might select the wrong date when creating a time entry or they might transpose the numbers when entering an expense.</span></span> <span data-ttu-id="010dc-107">Jos konsultti ei voi tehdä muutoksia lähetettyihin merkintöihin, järjestelmänvalvoja voi korjata projektin merkinnän suoraan.</span><span class="sxs-lookup"><span data-stu-id="010dc-107">If a consultant can’t make the updates to the submitted entries, an administrator can directly correct the entry for a project.</span></span>

<span data-ttu-id="010dc-108">Tässä aiheessa kuvattujen toimien suorittaminen edellyttää järjestelmänvalvojan oikeuksia.</span><span class="sxs-lookup"><span data-stu-id="010dc-108">To complete the procedures in this topic, you will need Administrator permissions.</span></span>

## <a name="correct-approved-time-entries"></a><span data-ttu-id="010dc-109">Hyväksyttyjen aikamerkintöjen korjaaminen</span><span class="sxs-lookup"><span data-stu-id="010dc-109">Correct approved time entries</span></span>     

<span data-ttu-id="010dc-110">Noudata seuraavia ohjeita korjataksesi projektin yksittäisen aikamerkinnän tai useita aikamerkintöjä.</span><span class="sxs-lookup"><span data-stu-id="010dc-110">Complete the following steps to correct single or multiple time entries for a project.</span></span>

1. <span data-ttu-id="010dc-111">Valitse **Myynti**-alueelta **Tapahtumat** ja valitse sitten **Hyväksytty aika**.</span><span class="sxs-lookup"><span data-stu-id="010dc-111">In the **Sales** area, select **Transactions**, and then select **Approved Time**.</span></span> 

2. <span data-ttu-id="010dc-112">Etsi ja valitse **Hyväksytty aika** -luettelosta yksi tai useampi korjattava aikamerkintä.</span><span class="sxs-lookup"><span data-stu-id="010dc-112">In the **Approved Time** list, locate and select one or more approved time entries to correct.</span></span> <span data-ttu-id="010dc-113">Voit käyttää suodinta löytääksesi asiaankuuluvat merkinnät.</span><span class="sxs-lookup"><span data-stu-id="010dc-113">You can use the filter to locate related entries.</span></span> <span data-ttu-id="010dc-114">Voit suodattaa merkinnät esimerkiksi projektin tunnuksen mukaan ja valita sitten kaikki hyväksytyt aikamerkinnät, joilla on kyseinen projektitunnus.</span><span class="sxs-lookup"><span data-stu-id="010dc-114">For example, you might filter on a Project ID, and select all approved time entries with that Project ID.</span></span>

3. <span data-ttu-id="010dc-115">Valitse **Viennin oikaisu**.</span><span class="sxs-lookup"><span data-stu-id="010dc-115">Select **Correct entries**.</span></span> <span data-ttu-id="010dc-116">Uusi oikaisukirjauskansio luodaan automaattisesti tyypillä **Ajan korjaus**.</span><span class="sxs-lookup"><span data-stu-id="010dc-116">A new correction journal is automatically created, with the assigned type **Time correction**.</span></span> <span data-ttu-id="010dc-117">Valitsemasi merkinnät lisätään kirjauskansioon.</span><span class="sxs-lookup"><span data-stu-id="010dc-117">The entries you selected are added to the journal.</span></span> 

4. <span data-ttu-id="010dc-118">Syötä oikaisukirjauskansiolle kuvaus **Uusi kirjauskansio** -sivun **Kuvaus**-kenttään ja valitse sitten **Aikamerkinnän korjaukset** -välilehti.</span><span class="sxs-lookup"><span data-stu-id="010dc-118">On the **New Journal** page, enter a **Description** for your correction journal, and then select the **Time Entry Corrections** tab.</span></span>  

5. <span data-ttu-id="010dc-119">Päivitä kentät oikeilla tiedoilla tarvittaessa **Aikamerkintöjen uudet arvot** -osiossa.</span><span class="sxs-lookup"><span data-stu-id="010dc-119">In the **New Values for Time Entries** section, update the fields with the correct information as necessary.</span></span> <span data-ttu-id="010dc-120">Voit esimerkiksi muuttaa delegoitua projektia tai varattavissa olevaa resurssia.</span><span class="sxs-lookup"><span data-stu-id="010dc-120">For example, you can change the assigned project or the bookable resource.</span></span>

6. <span data-ttu-id="010dc-121">Valitse **Esikatselu**.</span><span class="sxs-lookup"><span data-stu-id="010dc-121">Select **Preview**.</span></span> <span data-ttu-id="010dc-122">Valitse valintaikkunasta **OK**.</span><span class="sxs-lookup"><span data-stu-id="010dc-122">In the dialog box, select **OK**.</span></span> <span data-ttu-id="010dc-123">**Kirjauskansion rivit** -välilehdessä näet luettelon alkuperäisistä todellisista arvoista, jotka liittyvät valittuihin palautettuihin aikamerkintöihin, sekä vastaavat luodut korjatut rivit.</span><span class="sxs-lookup"><span data-stu-id="010dc-123">On the **Journal lines** tab, you can view a list of the original actuals that are related to the selected time entries that have been reversed and the corrected corresponding lines that have been created.</span></span> <span data-ttu-id="010dc-124">Jos sinun tarvitsee tehdä lisää korjauksia, toista vaiheet 5 ja 6.</span><span class="sxs-lookup"><span data-stu-id="010dc-124">If additional corrections need to be made, repeat steps 5 and 6.</span></span> 

> [!NOTE]
> <span data-ttu-id="010dc-125">Kaikilla korjatuilla todellisilla arvoilla on samat arvot kuin jotka valitsit **Aikamerkintöjen uudet arvot** -osiossa.</span><span class="sxs-lookup"><span data-stu-id="010dc-125">All the corrected actuals will have the same values that you selected in the **New values for Time Entries** section.</span></span>

7. <span data-ttu-id="010dc-126">Jos korjaukset näkyvät odotetulla tavalla, valitse **Vahvista**.</span><span class="sxs-lookup"><span data-stu-id="010dc-126">If the corrections appear as expected, select **Confirm**.</span></span> <span data-ttu-id="010dc-127">Valitse valintaikkunasta **OK**.</span><span class="sxs-lookup"><span data-stu-id="010dc-127">In the dialog box, select **OK**.</span></span>

8. <span data-ttu-id="010dc-128">Palaa **Myynti**-alueelle, valitse **Projektit** ja avaa projekti, jonka aikamerkinnät päivitit juuri.</span><span class="sxs-lookup"><span data-stu-id="010dc-128">Return to the **Sales** area, select **Projects**, and then open the project for which you just updated the time entries.</span></span> 

9. <span data-ttu-id="010dc-129">Tarkasta tekemäsi muutokset **Projektit**-sivun **Todelliset arvot** -välilehdestä.</span><span class="sxs-lookup"><span data-stu-id="010dc-129">On the **Projects** page, on the **Actuals** tab, view the changes that you made.</span></span> 

> [!NOTE]
> <span data-ttu-id="010dc-130">Jos **Todelliset arvot** -välilehti ei ole näkyvissä, valitse **Liittyvät** > **Todelliset arvot**.</span><span class="sxs-lookup"><span data-stu-id="010dc-130">If the **Actuals** tab is not visible, select **Related** > **Actuals**.</span></span>  

10. <span data-ttu-id="010dc-131">**Todellisten arvojen liitetty näkymä** -luettelossa näet, että alkuperäiset palautetut aikamerkinnät ovat edelleen luettelossa vastaavien korjattujen aikamerkintöjen kanssa.</span><span class="sxs-lookup"><span data-stu-id="010dc-131">In the **Actual Associated View** list, you can see that the original time entries that have been reversed are still listed, as are the corresponding corrected time entries.</span></span> 

<span data-ttu-id="010dc-132">Esimerkiksi seuraavassa kuva on kaksi nimikettä, joiden määrä on 8,00 ja joilla on veloituksia Summa-sarakkeessa.</span><span class="sxs-lookup"><span data-stu-id="010dc-132">For example, in the following graphic, there are two line items with a quantity of 8.00 that have debits listed in the Amount column.</span></span> <span data-ttu-id="010dc-133">Lisäksi näet kaksi nimikettä, joiden summa on -8,00 ja joilla on hyvitettyjä summia Summa-sarakkeessa.</span><span class="sxs-lookup"><span data-stu-id="010dc-133">Additionally, there are two line items with a quantity of -8.00 that show credited amounts in the Amount column.</span></span> <span data-ttu-id="010dc-134">Nämä korjaukset tuovat määrän nollaan.</span><span class="sxs-lookup"><span data-stu-id="010dc-134">These corrections bring the quantity to zero.</span></span>

 
## <a name="correct-approved-expense-entries"></a><span data-ttu-id="010dc-135">Hyväksyttyjen kulumerkintöjen korjaaminen</span><span class="sxs-lookup"><span data-stu-id="010dc-135">Correct approved expense entries</span></span>

<span data-ttu-id="010dc-136">Noudata seuraavia ohjeita korjataksesi yhden tai useamman kulumerkinnän.</span><span class="sxs-lookup"><span data-stu-id="010dc-136">Complete the following steps to correct one or more expense entries.</span></span> 

1. <span data-ttu-id="010dc-137">Valitse **Myynti**-alueen vasemmanpuoleisen siirtymisruudun **Tapahtumat**-osiosta **Hyväksytyt kulut**.</span><span class="sxs-lookup"><span data-stu-id="010dc-137">In the **Sales** area, in the left navigation pane, under **Transactions**, select **Approved Expenses**.</span></span>

2. <span data-ttu-id="010dc-138">Valitse **Hyväksytyt kulut** -luettelosta projekti, jonka haluat korjata, ja valitse sitten **Viennin oikaisu**.</span><span class="sxs-lookup"><span data-stu-id="010dc-138">In the **Approved Expenses** list, select the project that you want to correct, and then select **Correct entries**.</span></span> <span data-ttu-id="010dc-139">Uusi oikaisukirjauskansio luodaan automaattisesti tyypillä **Kulun korjaus**.</span><span class="sxs-lookup"><span data-stu-id="010dc-139">A new correction journal will be created automatically with the assigned type of **Expense correction**.</span></span> 

3. <span data-ttu-id="010dc-140">Kirjoita korjaukselle kuvaus **Uusi kirjauskansio** -sivun **Kuvaus**-kenttään ja valitse **Kulun korjaus** -välilehden **Kulujen uudet arvot** -osiosta tietokentät, jotka haluat korjata valituille kulujen riveille.</span><span class="sxs-lookup"><span data-stu-id="010dc-140">On the **New Journal** page, enter a **Description** for the correction, and on the **Expense Correction** tab, in the **New Values for Expenses** section, select the data fields that you want to correct for the selected expense lines.</span></span> <span data-ttu-id="010dc-141">Voit esimerkiksi delegoida kulun toiseen **projektiin** tai korjata **Kululuokka**-, **Kulun päivämäärä**- tai **Varattavissa oleva resurssi** -arvot.</span><span class="sxs-lookup"><span data-stu-id="010dc-141">For example, you can assign the expense to another **Project**, or correct the **Expense Category**, **Expense Date**, or **Bookable Resource**.</span></span>

4. <span data-ttu-id="010dc-142">Valitse **Esikatselu**.</span><span class="sxs-lookup"><span data-stu-id="010dc-142">Select **Preview**.</span></span> <span data-ttu-id="010dc-143">Valitse valintaikkunasta **OK**.</span><span class="sxs-lookup"><span data-stu-id="010dc-143">In the dialog box, select **OK**.</span></span> 

5. <span data-ttu-id="010dc-144">Tarkasta korjaukset **Kirjauskansion rivit** -välilehdes. Näet luettelon alkuperäisistä todellisista arvoista, jotka liittyvät valittuihin palautettuihin kulumerkintöihin, sekä vastaavat luodut korjatut rivit.</span><span class="sxs-lookup"><span data-stu-id="010dc-144">Verify the corrections on the **Journal lines** tab. You can view a list of the original actuals that are related to the selected expense entries that have been reversed and the corrected corresponding lines that have been created.</span></span>

6. <span data-ttu-id="010dc-145">Jos korjatut arvot ovat oikein, valitse **Vahvista**.</span><span class="sxs-lookup"><span data-stu-id="010dc-145">If the corrected values are as expected, select **Confirm**.</span></span> <span data-ttu-id="010dc-146">Valitse valintaikkunasta **OK**.</span><span class="sxs-lookup"><span data-stu-id="010dc-146">In the dialog box, select **OK.**</span></span> <span data-ttu-id="010dc-147">Jos arvot eivät näy odotetulla tavalla, valitse **Peruuta** palataksesi **Hyväksytyt kulut** -luetteloon.</span><span class="sxs-lookup"><span data-stu-id="010dc-147">If the values are not showing as expected, select **Cancel** to return to the **Approved Expenses** list.</span></span> <span data-ttu-id="010dc-148">Toista vaiheet 2–5.</span><span class="sxs-lookup"><span data-stu-id="010dc-148">Repeat steps 2 through 5.</span></span> 

> [!NOTE]
> <span data-ttu-id="010dc-149">Korjatuilla todellisilla arvoilla on samat arvot kuin jotka valitsit **Kulujen uudet arvot** -osiossa.</span><span class="sxs-lookup"><span data-stu-id="010dc-149">The corrected actuals will have the same values that you selected in the **New values for Expenses** section.</span></span>

7. <span data-ttu-id="010dc-150">Kun olet tarkastanut oikaisukirjauskansion, siirry takaisin päivittämääsi projektiin tai projekteihin nähdäksesi muutoksesi.</span><span class="sxs-lookup"><span data-stu-id="010dc-150">After you confirm the correction journal, navigate back to the project or projects that you updated, to view your changes.</span></span>  

8. <span data-ttu-id="010dc-151">Tarkista **Todelliset arvot** -välilehdestä **Todellisten arvojen liitetty näkymä** .</span><span class="sxs-lookup"><span data-stu-id="010dc-151">In the project page, on the **Actuals** tab, review the **Actual Associated View**.</span></span> <span data-ttu-id="010dc-152">Luettelossa näytetään alkuperäiset ja korjatut merkinnät.</span><span class="sxs-lookup"><span data-stu-id="010dc-152">The original entries and the corrected entries are listed.</span></span> <span data-ttu-id="010dc-153">Seuraavassa kuvassa näytetään alkuperäisten kulumerkintöjen summat ja niitä vastaavien korjattujen kulumerkintöjen summat.</span><span class="sxs-lookup"><span data-stu-id="010dc-153">The following graphic shows original expense entry amounts and the corresponding corrected expense entry amounts.</span></span> 




[!INCLUDE[footer-include](../includes/footer-banner.md)]