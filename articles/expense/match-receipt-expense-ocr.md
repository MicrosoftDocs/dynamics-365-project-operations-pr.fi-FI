---
title: Kuitin ja kulun täsmäyttäminen OCR-tunnistuksella
description: Tässä aiheessa on tietoja kuittien optisesta merkintunnistuksesta (OCR).
author: suvaidya
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: ''
ms.author: shylaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 55f63c8c092942b73a55c9d86d867bca600f42e5
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/28/2020
ms.locfileid: "4124319"
---
# <a name="match-a-receipt-to-an-expense-using-ocr"></a><span data-ttu-id="c138c-103">Kuitin ja kulun täsmäyttäminen OCR-tunnistuksella</span><span class="sxs-lookup"><span data-stu-id="c138c-103">Match a receipt to an expense using OCR</span></span>

<span data-ttu-id="c138c-104">_**Koskee:** Project Operationsin resurssiin / muuhun kuin resurssiin perustuvia skenaarioita, Lite-käyttöönotto-kaupasta proformalaskutukseen_</span><span class="sxs-lookup"><span data-stu-id="c138c-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="c138c-105">Kulun syöttöä on parannettu kuittien optisen merkintunnistuksen (OCR) käsittelyn avulla.</span><span class="sxs-lookup"><span data-stu-id="c138c-105">Expense entry has been enhanced through the introduction of optical character recognition (OCR) processing for receipts.</span></span> <span data-ttu-id="c138c-106">Tämä toiminto on suunniteltu parantamaan kuluraporttien luomisen käyttökokemusta.</span><span class="sxs-lookup"><span data-stu-id="c138c-106">This functionality is designed to improve the user experience when creating expense reports.</span></span>

## <a name="key-features"></a><span data-ttu-id="c138c-107">Tärkeimmät ominaisuudet</span><span class="sxs-lookup"><span data-stu-id="c138c-107">Key features</span></span>

- <span data-ttu-id="c138c-108">Järjestelmä poimii myyjän nimen, päivämäärän ja kokonaissumman kuiteista.</span><span class="sxs-lookup"><span data-stu-id="c138c-108">The system extracts the merchant name, date, and total amount from receipts.</span></span>
- <span data-ttu-id="c138c-109">Järjestelmä yrittää määrittää liittämättömät kuitit liittämättömiin kulutapahtumiin.</span><span class="sxs-lookup"><span data-stu-id="c138c-109">The system will try to match unattached receipts to unattached expense transactions.</span></span>
- <span data-ttu-id="c138c-110">Voit luoda manuaalisesti syötettyjä kulutapahtumia kuiteista.</span><span class="sxs-lookup"><span data-stu-id="c138c-110">You can create manually entered expense transactions from receipts.</span></span>

## <a name="attach-receipts-to-an-expense-report"></a><span data-ttu-id="c138c-111">Kuittien liittäminen kuluraportteihin</span><span class="sxs-lookup"><span data-stu-id="c138c-111">Attach receipts to an expense report</span></span>

<span data-ttu-id="c138c-112">Jos haluat liittää kuluraportin luomisen yhteydessä automaattisesti luottokorttitapahtumia sisältävät kuitit, suorita seuraavat vaiheet.</span><span class="sxs-lookup"><span data-stu-id="c138c-112">To automatically attach receipts that include credit card transactions when an expense report is created, complete the following steps.</span></span>

  1. <span data-ttu-id="c138c-113">Avaa **Kulun hallinta** -työtila.</span><span class="sxs-lookup"><span data-stu-id="c138c-113">Open the **Expense management** workspace.</span></span>
  2. <span data-ttu-id="c138c-114">Tarkista **Kuitit**-välilehdessä, että liitetyt kuitit ovat olemassa.</span><span class="sxs-lookup"><span data-stu-id="c138c-114">On the **Receipts** tab, verify that unattached receipts exist.</span></span> <span data-ttu-id="c138c-115">Voit myös ladata kuitit **Kuitit**-välilehteen.</span><span class="sxs-lookup"><span data-stu-id="c138c-115">You can also upload receipts on the **Receipts** tab.</span></span>
  3. <span data-ttu-id="c138c-116">Tarkista **Kulut**-välilehdessä, että liitetyt kulut ovat olemassa.</span><span class="sxs-lookup"><span data-stu-id="c138c-116">On the **Expenses** tab, verify that unattached expenses exist.</span></span> <span data-ttu-id="c138c-117">Yleensä kulujen järjestelmänvalvoja tuo nämä kulut luottokortin myöntäjältä.</span><span class="sxs-lookup"><span data-stu-id="c138c-117">Typically, the expense administrator imports these expenses from the credit card provider.</span></span>
  4. <span data-ttu-id="c138c-118">Valitse **Uusi kuluraportti**.</span><span class="sxs-lookup"><span data-stu-id="c138c-118">Select **New expense report**.</span></span> <span data-ttu-id="c138c-119">Huomaa, että voit lisätä kuluja ja kuitteja myös nyt, kun luot kuluraportin.</span><span class="sxs-lookup"><span data-stu-id="c138c-119">Notice that you can include expenses, and receipts, now as well, when you create an expense report.</span></span> <span data-ttu-id="c138c-120">Jos lisäät sekä kuluja että kuitteja, järjestelmä käynnistää kuittausten automaattisen täsmäytyksen kuluihin.</span><span class="sxs-lookup"><span data-stu-id="c138c-120">If you add both expenses and receipts, automatic matching of the receipts against the expenses is triggered.</span></span>

## <a name="create-or-match-receipts-to-an-expense-report"></a><span data-ttu-id="c138c-121">Kuittien luominen tai liittäminen kuluraportteihin</span><span class="sxs-lookup"><span data-stu-id="c138c-121">Create or match receipts to an expense report</span></span>
<span data-ttu-id="c138c-122">Jos haluat luoda kulun tai määrittää kuitin kulun vastaavuuden, tee seuraavat vaiheet.</span><span class="sxs-lookup"><span data-stu-id="c138c-122">To create an expense, or match an expense from a receipt, complete the following steps.</span></span>

  1. <span data-ttu-id="c138c-123">Liitä kuluraportin **Kuitit**-välilehteen kuitti valitsemalla **Lisää kuitteja**.</span><span class="sxs-lookup"><span data-stu-id="c138c-123">On an expense report, on the **Receipts** tab, attach a receipt by selecting **Add receipts**.</span></span>
  2. <span data-ttu-id="c138c-124">Huomaa kuitin ladatun kuvan alla olevat **Luo**- ja **Määritä vastaavuus** -vaihtoehdot.</span><span class="sxs-lookup"><span data-stu-id="c138c-124">Under the uploaded image of the receipt, notice the **Create** and **Match** options.</span></span>

      - <span data-ttu-id="c138c-125">Valitse **Luo**, jos haluat luoda manuaalisesti syötetyn kulutapahtuman ja täyttää arvot, jotka on poimittu kuitista.</span><span class="sxs-lookup"><span data-stu-id="c138c-125">Select **Create** to create a manually entered expense transaction and fill in the values that are extracted from the receipt.</span></span>
      - <span data-ttu-id="c138c-126">Jos valitset **Määritä vastaavuus**, järjestelmä yrittää määrittää olemassa olevan kulun ja kuitin vastaavuuden.</span><span class="sxs-lookup"><span data-stu-id="c138c-126">If you select **Match**, the system tries to match an existing expense to the receipt.</span></span>

## <a name="installation"></a><span data-ttu-id="c138c-127">Asennus</span><span class="sxs-lookup"><span data-stu-id="c138c-127">Installation</span></span>

<span data-ttu-id="c138c-128">Jos haluat käyttää kulujen lisäominasuuksia, asenna Microsoft Dynamics 365 Financen kulujen hallintapalvelun apuohjelma ja ota toiminnot käyttöön esiintymässä.</span><span class="sxs-lookup"><span data-stu-id="c138c-128">To use these advanced expense capabilities, install the Expense Management Service add-in for Microsoft Dynamics 365 Finance, and turn on the features in your instance.</span></span> <span data-ttu-id="c138c-129">Voit käyttää Microsoft Dynamics Lifecycle Services (LCS) -sovelluksen projektin apuohjelmaa.</span><span class="sxs-lookup"><span data-stu-id="c138c-129">You can access the add-in from your project in Microsoft Dynamics Lifecycle Services (LCS).</span></span>

1. <span data-ttu-id="c138c-130">Kirjaudu sisään LCS-sovellukseen ja avaa haluamasi ympäristö.</span><span class="sxs-lookup"><span data-stu-id="c138c-130">Sign in to LCS, and open the desired environment.</span></span>
2. <span data-ttu-id="c138c-131">Siirry kohtaan **Täydelliset tiedot**.</span><span class="sxs-lookup"><span data-stu-id="c138c-131">Go to **Full details**.</span></span>
3. <span data-ttu-id="c138c-132">Valitse **Ylläpidä** tai siirry **Ympäristön apuohjelmat** -pikavälilehteen virittämällä.</span><span class="sxs-lookup"><span data-stu-id="c138c-132">Select **Maintain**, or scroll down to the **Environment add-ins** FastTab.</span></span>
4. <span data-ttu-id="c138c-133">Valitse **Asenna uusi apuohjelma**.</span><span class="sxs-lookup"><span data-stu-id="c138c-133">Select **Install a new add-in**.</span></span>
5. <span data-ttu-id="c138c-134">Valitse **Kulujen hallintapalvelu**.</span><span class="sxs-lookup"><span data-stu-id="c138c-134">Select **Expense Management Service**.</span></span>
6. <span data-ttu-id="c138c-135">Seuraa asennusopasta ja hyväksy ehdot.</span><span class="sxs-lookup"><span data-stu-id="c138c-135">Follow the installation guide, and agree to the terms and conditions.</span></span>
7. <span data-ttu-id="c138c-136">Valitse **Asennus**.</span><span class="sxs-lookup"><span data-stu-id="c138c-136">Select **Install**.</span></span>

<span data-ttu-id="c138c-137">Ota **Ominaisuuksien hallinta** -työtilassa käyttöön seuraavat ominaisuudet:</span><span class="sxs-lookup"><span data-stu-id="c138c-137">In the **Feature management** workspace, turn on the following features:</span></span>

- <span data-ttu-id="c138c-138">Uudistetut kuluraportit</span><span class="sxs-lookup"><span data-stu-id="c138c-138">Expense reports re-imagined</span></span>
- <span data-ttu-id="c138c-139">Automaattinen vastaavuus ja kulun luominen kuitista</span><span class="sxs-lookup"><span data-stu-id="c138c-139">Auto-match and create expense from receipt</span></span>

<span data-ttu-id="c138c-140">Kun otat nämä ominaisuudet käyttöön, suoritetaan seuraavat toiminnot:</span><span class="sxs-lookup"><span data-stu-id="c138c-140">When you turn on these features the following actions occur:</span></span>

- <span data-ttu-id="c138c-141">Aiemmin luotu **Kulun hallinta** -työtila korvataan uudella työtilalla.</span><span class="sxs-lookup"><span data-stu-id="c138c-141">The existing **Expense management** workspace is replaced with the new workspace.</span></span>
- <span data-ttu-id="c138c-142">Kulukentän näkyvyydelle lisätään uusi valikon vaihtoehto.</span><span class="sxs-lookup"><span data-stu-id="c138c-142">A new menu item for expense field visibility is added.</span></span>
- <span data-ttu-id="c138c-143">Voit yhä avata aiemman **Kuluraportit**-sivun siirtymällä kohtaan **Kulujen hallinta > Omat kulut > Kuluraportit**.</span><span class="sxs-lookup"><span data-stu-id="c138c-143">You can still open the former **Expense reports** page by going to **Expense management > My expenses > Expense reports**.</span></span>
- <span data-ttu-id="c138c-144">Työnkulkujen ja hyväksyntöjen avulla käyttäjä siirretään yhä olemassa olevien kuluraporttien sivulle.</span><span class="sxs-lookup"><span data-stu-id="c138c-144">Workflows and any approvals still take you to the existing expense reports page.</span></span>
- <span data-ttu-id="c138c-145">Microsoft Azure Cognitive Services -sovellus käsittelee kuitit ja metatiedot puretaan ja lisätään.</span><span class="sxs-lookup"><span data-stu-id="c138c-145">Receipts will be processed through Microsoft Azure Cognitive Services, and metadata will be extracted and added.</span></span>
- <span data-ttu-id="c138c-146">Järjestelmä lisää vaihtoehdon sellaisen kuluraportin luomista varten, joka sisältää liittämättömiä kuitteja, joiden vastaavuutta ei ole määritetty.</span><span class="sxs-lookup"><span data-stu-id="c138c-146">An option is added that lets you create an expense report that includes matched unattached receipts.</span></span>
- <span data-ttu-id="c138c-147">Kuluraportteihin lisättävän vaihtoehdon avulla voit luoda kulurivin kuitista tai yrittää määrittää olemassa olevan kuitin ja olemassa olevan kulurivin vastaavuuden.</span><span class="sxs-lookup"><span data-stu-id="c138c-147">An option that is added to expense reports lets you create an expense line from a receipt, or attempts to match an existing receipt to an existing expense line.</span></span>

## <a name="frequently-asked-questions"></a><span data-ttu-id="c138c-148">Usein kysyttyjä kysymyksiä</span><span class="sxs-lookup"><span data-stu-id="c138c-148">Frequently asked questions</span></span>

<span data-ttu-id="c138c-149">**Käyttääkö Microsoft tietojani malleissa?**</span><span class="sxs-lookup"><span data-stu-id="c138c-149">**Does Microsoft use my data for its models?**</span></span>

<span data-ttu-id="c138c-150">Ei. Microsoft on rakentanut yleisen koneoppiminen mallin kuittien käsittelypalvelua varten.</span><span class="sxs-lookup"><span data-stu-id="c138c-150">No, Microsoft has built a general machine learning model for its receipt processing service.</span></span> <span data-ttu-id="c138c-151">Tämä malli ei perustu kuitteihin, joita käyttäjä lataa.</span><span class="sxs-lookup"><span data-stu-id="c138c-151">This model isn't based on the receipts that you upload.</span></span>

<span data-ttu-id="c138c-152">**Missä tämä toiminto on käytettävissä ja missä sitä käsitellään?**</span><span class="sxs-lookup"><span data-stu-id="c138c-152">**Where is this feature available and processed?**</span></span>

<span data-ttu-id="c138c-153">Tällä hetkellä tuetaan käyttöä Yhdysvalloissa.</span><span class="sxs-lookup"><span data-stu-id="c138c-153">Currently, the United States is supported.</span></span>

<span data-ttu-id="c138c-154">**Minne kuitit siirretään?**</span><span class="sxs-lookup"><span data-stu-id="c138c-154">**Where do my receipts go?**</span></span>

<span data-ttu-id="c138c-155">Finance ottaa yhteyttä Cognitive Services -sovellukseen ja purkaa kentän tiedot.</span><span class="sxs-lookup"><span data-stu-id="c138c-155">Finance will contact Cognitive Services to extract the field data.</span></span> <span data-ttu-id="c138c-156">Cognitive Services -sovellus säilyttää kuittikopion käsittelyn ajan, mutta enintään 24 tuntia.</span><span class="sxs-lookup"><span data-stu-id="c138c-156">Cognitive Services will retain a copy of your receipt for up to 24 hours while processing occurs.</span></span> <span data-ttu-id="c138c-157">Kun käsittely on valmis, Cognitive Services poistaa kuitin.</span><span class="sxs-lookup"><span data-stu-id="c138c-157">After processing is completed, Cognitive Services will remove the receipt.</span></span> <span data-ttu-id="c138c-158">Kuitit tallennetaan edelleen Finance-sovellukseen.</span><span class="sxs-lookup"><span data-stu-id="c138c-158">Receipts are still stored in Finance.</span></span>

<span data-ttu-id="c138c-159">Lisätietoja on kohdassa [Lisätietoja kuiteista lomakkeen tunnistustoiminnon uuden ominaisuuden avulla](https://azure.microsoft.com/blog/enable-receipt-understanding-with-form-recognizer-s-new-capability/).</span><span class="sxs-lookup"><span data-stu-id="c138c-159">For more information, see [Enable receipt understanding with Form Recognizer's new capability](https://azure.microsoft.com/blog/enable-receipt-understanding-with-form-recognizer-s-new-capability/).</span></span>
