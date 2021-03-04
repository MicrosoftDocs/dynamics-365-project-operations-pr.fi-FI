---
title: Kulukuittien käsittely
description: Tässä aiheessa on tietoja kuittien optisesta merkintunnistuksesta (OCR). Tämä ominaisuus on suunniteltu parantamaan Microsoft Dynamics 365 Financessa luotujen kuluraporttien käyttökokemusta.
author: stsporen
manager: AnnBe
ms.date: 05/14/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Operations, Core
ms.search.region: Global
ms.author: stsporen
ms.search.validFrom: 2019-11-20
ms.dyn365.ops.version: 10.0.8
ms.openlocfilehash: 64901610144f9dfe274bd4c2294ab32659743a1a
ms.sourcegitcommit: 9f31b33ed6e7f1b49200a407913201a1337f3401
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/14/2021
ms.locfileid: "4960288"
---
# <a name="expense-receipt-processing"></a><span data-ttu-id="8dfb4-104">Kulukuittien käsittely</span><span class="sxs-lookup"><span data-stu-id="8dfb4-104">Expense receipt processing</span></span>

<span data-ttu-id="8dfb4-105">Kulun syöttöä on parannettu kuittien optisen merkintunnistuksen (OCR) käsittelyn avulla.</span><span class="sxs-lookup"><span data-stu-id="8dfb4-105">Expense entry has been enhanced through the introduction of optical character recognition (OCR) processing for receipts.</span></span> <span data-ttu-id="8dfb4-106">Tämä ominaisuus on suunniteltu parantamaan luotujen kuluraporttien käyttökokemusta.</span><span class="sxs-lookup"><span data-stu-id="8dfb4-106">This feature is designed to improve the user experience when expense reports are created.</span></span>

## <a name="key-features"></a><span data-ttu-id="8dfb4-107">Tärkeimmät ominaisuudet</span><span class="sxs-lookup"><span data-stu-id="8dfb4-107">Key features</span></span>

- <span data-ttu-id="8dfb4-108">Myyjän nimi, päivämäärä ja kokonaissumma poimitaan kuiteista.</span><span class="sxs-lookup"><span data-stu-id="8dfb4-108">The merchant name, date, and total amount are extracted from receipts.</span></span>
- <span data-ttu-id="8dfb4-109">Ominaisuus yrittää määrittää liittämättömät kuitit liittämättömiin kulutapahtumiin.</span><span class="sxs-lookup"><span data-stu-id="8dfb4-109">The feature tries to match unattached receipts to unattached expense transactions.</span></span>
- <span data-ttu-id="8dfb4-110">Käyttäjät voivat luoda manuaalisesti syötettyjä kulutapahtumia kuiteista.</span><span class="sxs-lookup"><span data-stu-id="8dfb4-110">Users can create manually entered expense transactions from receipts.</span></span>

## <a name="usage-examples"></a><span data-ttu-id="8dfb4-111">Käyttöesimerkkejä</span><span class="sxs-lookup"><span data-stu-id="8dfb4-111">Usage examples</span></span>

<span data-ttu-id="8dfb4-112">Jos haluat liittää kuluraportin luomisen yhteydessä automaattisesti luottokorttitapahtumia sisältävät kuitit, tee seuraavat vaiheet:</span><span class="sxs-lookup"><span data-stu-id="8dfb4-112">To automatically attach receipts that include credit card transactions when an expense report is created, do the following:</span></span>

  1. <span data-ttu-id="8dfb4-113">Avaa **Kulun hallinta** -työtila.</span><span class="sxs-lookup"><span data-stu-id="8dfb4-113">Open the **Expense management** workspace.</span></span>
  2. <span data-ttu-id="8dfb4-114">Tarkista **Kuitit**-välilehdessä, että liitetyt kuitit ovat olemassa.</span><span class="sxs-lookup"><span data-stu-id="8dfb4-114">On the **Receipts** tab, verify that unattached receipts exist.</span></span> <span data-ttu-id="8dfb4-115">Voit myös ladata kuitit **Kuitit**-välilehteen.</span><span class="sxs-lookup"><span data-stu-id="8dfb4-115">You can also upload receipts on the **Receipts** tab.</span></span>
  3. <span data-ttu-id="8dfb4-116">Tarkista **Kulut**-välilehdessä, että liitetyt kulut ovat olemassa.</span><span class="sxs-lookup"><span data-stu-id="8dfb4-116">On the **Expenses** tab, verify that unattached expenses exist.</span></span> <span data-ttu-id="8dfb4-117">Yleensä kulujen järjestelmänvalvoja tuo nämä kulut luottokortin myöntäjältä.</span><span class="sxs-lookup"><span data-stu-id="8dfb4-117">Typically, the expense administrator imports these expenses from the credit card provider.</span></span>
  4. <span data-ttu-id="8dfb4-118">Valitse **Uusi kuluraportti**.</span><span class="sxs-lookup"><span data-stu-id="8dfb4-118">Select **New expense report**.</span></span> <span data-ttu-id="8dfb4-119">Huomaa, että voit lisätä kuluja ja kuitteja myös nyt, kun luot kuluraportin.</span><span class="sxs-lookup"><span data-stu-id="8dfb4-119">Notice that you can include expenses, and receipts, now as well, when you create an expense report.</span></span> <span data-ttu-id="8dfb4-120">Jos lisäät sekä kuluja että kuitteja, järjestelmä käynnistää kuittausten automaattisen täsmäytyksen kuluihin.</span><span class="sxs-lookup"><span data-stu-id="8dfb4-120">If you add both expenses and receipts, automatic matching of the receipts against the expenses is triggered.</span></span>

<span data-ttu-id="8dfb4-121">Jos haluat luoda kulun tai määrittää kuitin kulun vastaavuuden, tee seuraavalla tavalla:</span><span class="sxs-lookup"><span data-stu-id="8dfb4-121">To create an expense, or match an expense from a receipt, do the following:</span></span>

  1. <span data-ttu-id="8dfb4-122">Liitä kuluraportin **Kuitit**-välilehteen kuitti valitsemalla **Lisää kuitteja**.</span><span class="sxs-lookup"><span data-stu-id="8dfb4-122">On an expense report, on the **Receipts** tab, attach a receipt by selecting **Add receipts**.</span></span>
  2. <span data-ttu-id="8dfb4-123">Huomaa kuitin ladatun kuvan alla olevat **Luo**- ja **Määritä vastaavuus** -vaihtoehdot.</span><span class="sxs-lookup"><span data-stu-id="8dfb4-123">Under the uploaded image of the receipt, notice the **Create** and **Match** options.</span></span>

      - <span data-ttu-id="8dfb4-124">Valitse **Luo**, jos haluat luoda manuaalisesti syötetyn kulutapahtuman ja täyttää arvot, jotka on poimittu kuitista.</span><span class="sxs-lookup"><span data-stu-id="8dfb4-124">Select **Create** to create a manually entered expense transaction and fill in the values that are extracted from the receipt.</span></span>
      - <span data-ttu-id="8dfb4-125">Jos valitset **Määritä vastaavuus**, järjestelmä yrittää määrittää olemassa olevan kulun ja kuitin vastaavuuden.</span><span class="sxs-lookup"><span data-stu-id="8dfb4-125">If you select **Match**, the system tries to match an existing expense to the receipt.</span></span>

## <a name="installation"></a><span data-ttu-id="8dfb4-126">Asennus</span><span class="sxs-lookup"><span data-stu-id="8dfb4-126">Installation</span></span>

<span data-ttu-id="8dfb4-127">Tämä ominaisuus toimii yhdessä **uudelleen suunniteltujen kuluraporttien** kanssa, mikä helpottaa kulukokemusta.</span><span class="sxs-lookup"><span data-stu-id="8dfb4-127">This feature works in combination with the **Expense reports re-imagined** feature to help simplify the expense experience.</span></span> <span data-ttu-id="8dfb4-128">Tämä ominaisuus on käytettävissä vain Tier 2+-ympäristöissä, jotka ovat eritys- ja tuotantoympäristö.</span><span class="sxs-lookup"><span data-stu-id="8dfb4-128">This feature is only available for Tier 2+ environments, which are Sandbox and Production.</span></span>

<span data-ttu-id="8dfb4-129">Jos haluat käyttää kulujen lisäominasuuksia, asenna Microsoft Dynamics 365 Financen kulujen hallintapalvelun apuohjelma ja ota toiminnot käyttöön esiintymässä.</span><span class="sxs-lookup"><span data-stu-id="8dfb4-129">To use these advanced expense capabilities, install the Expense Management Service add-in for Microsoft Dynamics 365 Finance, and turn on the features in your instance.</span></span> <span data-ttu-id="8dfb4-130">Voit käyttää Microsoft Dynamics Lifecycle Services (LCS) -sovelluksen projektin apuohjelmaa.</span><span class="sxs-lookup"><span data-stu-id="8dfb4-130">You can access the add-in from your project in Microsoft Dynamics Lifecycle Services (LCS).</span></span>

1. <span data-ttu-id="8dfb4-131">Kirjaudu sisään LCS-sovellukseen ja avaa haluamasi ympäristö.</span><span class="sxs-lookup"><span data-stu-id="8dfb4-131">Sign in to LCS, and open the desired environment.</span></span>
2. <span data-ttu-id="8dfb4-132">Siirry kohtaan **Täydelliset tiedot**.</span><span class="sxs-lookup"><span data-stu-id="8dfb4-132">Go to **Full details**.</span></span>
3. <span data-ttu-id="8dfb4-133">Valitse **Ylläpidä** tai siirry **Ympäristön apuohjelmat** -pikavälilehteen virittämällä.</span><span class="sxs-lookup"><span data-stu-id="8dfb4-133">Select **Maintain**, or scroll down to the **Environment add-ins** FastTab.</span></span>
4. <span data-ttu-id="8dfb4-134">Valitse **Asenna uusi apuohjelma**.</span><span class="sxs-lookup"><span data-stu-id="8dfb4-134">Select **Install a new add-in**.</span></span>
5. <span data-ttu-id="8dfb4-135">Valitse **Kulujen hallintapalvelu**.</span><span class="sxs-lookup"><span data-stu-id="8dfb4-135">Select **Expense Management Service**.</span></span>
6. <span data-ttu-id="8dfb4-136">Seuraa asennusopasta ja hyväksy ehdot.</span><span class="sxs-lookup"><span data-stu-id="8dfb4-136">Follow the installation guide, and agree to the terms and conditions.</span></span>
7. <span data-ttu-id="8dfb4-137">Valitse **Asennus**.</span><span class="sxs-lookup"><span data-stu-id="8dfb4-137">Select **Install**.</span></span>

<span data-ttu-id="8dfb4-138">Ota **Ominaisuuksien hallinta** -työtilassa käyttöön seuraavat ominaisuudet:</span><span class="sxs-lookup"><span data-stu-id="8dfb4-138">In the **Feature management** workspace, turn on the following features:</span></span>

- <span data-ttu-id="8dfb4-139">Uudistetut kuluraportit</span><span class="sxs-lookup"><span data-stu-id="8dfb4-139">Expense reports re-imagined</span></span>
- <span data-ttu-id="8dfb4-140">Automaattinen vastaavuus ja kulun luominen kuitista</span><span class="sxs-lookup"><span data-stu-id="8dfb4-140">Auto-match and create expense from receipt</span></span>

<span data-ttu-id="8dfb4-141">Kun otat nämä ominaisuudet käyttöön, suoritetaan seuraavat toiminnot:</span><span class="sxs-lookup"><span data-stu-id="8dfb4-141">When you turn on these features the following actions occur:</span></span>

- <span data-ttu-id="8dfb4-142">Aiemmin luotu **Kulun hallinta** -työtila korvataan uudella työtilalla.</span><span class="sxs-lookup"><span data-stu-id="8dfb4-142">The existing **Expense management** workspace is replaced with the new workspace.</span></span>
- <span data-ttu-id="8dfb4-143">Kulukentän näkyvyydelle lisätään uusi valikon vaihtoehto.</span><span class="sxs-lookup"><span data-stu-id="8dfb4-143">A new menu item for expense field visibility is added.</span></span>
- <span data-ttu-id="8dfb4-144">Voit yhä avata aiemman **Kuluraportit**-sivun siirtymällä kohtaan **Kulujen hallinta > Omat kulut > Kuluraportit**.</span><span class="sxs-lookup"><span data-stu-id="8dfb4-144">You can still open the former **Expense reports** page by going to **Expense management > My expenses > Expense reports**.</span></span>
- <span data-ttu-id="8dfb4-145">Työnkulkujen ja hyväksyntöjen avulla käyttäjä siirretään yhä olemassa olevien kuluraporttien sivulle.</span><span class="sxs-lookup"><span data-stu-id="8dfb4-145">Workflows and any approvals still take you to the existing expense reports page.</span></span>
- <span data-ttu-id="8dfb4-146">Microsoft Azure Cognitive Services -sovellus käsittelee kuitit ja metatiedot puretaan ja lisätään.</span><span class="sxs-lookup"><span data-stu-id="8dfb4-146">Receipts will be processed through Microsoft Azure Cognitive Services, and metadata will be extracted and added.</span></span>
- <span data-ttu-id="8dfb4-147">Järjestelmä lisää vaihtoehdon sellaisen kuluraportin luomista varten, joka sisältää liittämättömiä kuitteja, joiden vastaavuutta ei ole määritetty.</span><span class="sxs-lookup"><span data-stu-id="8dfb4-147">An option is added that lets you create an expense report that includes matched unattached receipts.</span></span>
- <span data-ttu-id="8dfb4-148">Kuluraportteihin lisättävän vaihtoehdon avulla voit luoda kulurivin kuitista tai yrittää määrittää olemassa olevan kuitin ja olemassa olevan kulurivin vastaavuuden.</span><span class="sxs-lookup"><span data-stu-id="8dfb4-148">An option that is added to expense reports lets you create an expense line from a receipt, or attempts to match an existing receipt to an existing expense line.</span></span>

<span data-ttu-id="8dfb4-149">Lisätietoja kuluraporttien uudelleenkuvioitavista ominaisuuksista on kohdassa [Uudelleen suunnitellut kuluraportit](ExpenseWorkspaceNew.md).</span><span class="sxs-lookup"><span data-stu-id="8dfb4-149">For more information about the Expense reports re-imagined feature, see [Expense reports reimagined](ExpenseWorkspaceNew.md).</span></span>

## <a name="frequently-asked-questions"></a><span data-ttu-id="8dfb4-150">Usein kysyttyjä kysymyksiä</span><span class="sxs-lookup"><span data-stu-id="8dfb4-150">Frequently asked questions</span></span>

<span data-ttu-id="8dfb4-151">**Käyttääkö Microsoft tietojani malleissa?**</span><span class="sxs-lookup"><span data-stu-id="8dfb4-151">**Does Microsoft use my data for its models?**</span></span>

<span data-ttu-id="8dfb4-152">Ei. Microsoft on rakentanut yleisen koneoppiminen mallin kuittien käsittelypalvelua varten.</span><span class="sxs-lookup"><span data-stu-id="8dfb4-152">No, Microsoft has built a general machine learning model for its receipt processing service.</span></span> <span data-ttu-id="8dfb4-153">Tämä malli ei perustu kuitteihin, joita käyttäjä lataa.</span><span class="sxs-lookup"><span data-stu-id="8dfb4-153">This model isn't based on the receipts that you upload.</span></span>

<span data-ttu-id="8dfb4-154">**Missä tämä toiminto on käytettävissä ja missä sitä käsitellään?**</span><span class="sxs-lookup"><span data-stu-id="8dfb4-154">**Where is this feature available and processed?**</span></span>

<span data-ttu-id="8dfb4-155">Tällä hetkellä tuetaan käyttöä Yhdysvalloissa.</span><span class="sxs-lookup"><span data-stu-id="8dfb4-155">Currently, the United States is supported.</span></span>

<span data-ttu-id="8dfb4-156">**Minne kuitit siirretään?**</span><span class="sxs-lookup"><span data-stu-id="8dfb4-156">**Where do my receipts go?**</span></span>

<span data-ttu-id="8dfb4-157">Finance ottaa yhteyttä Cognitive Services -sovellukseen ja purkaa kentän tiedot.</span><span class="sxs-lookup"><span data-stu-id="8dfb4-157">Finance will contact Cognitive Services to extract the field data.</span></span> <span data-ttu-id="8dfb4-158">Cognitive Services -sovellus säilyttää kuittikopion käsittelyn ajan, mutta enintään 24 tuntia.</span><span class="sxs-lookup"><span data-stu-id="8dfb4-158">Cognitive Services will retain a copy of your receipt for up to 24 hours while processing occurs.</span></span> <span data-ttu-id="8dfb4-159">Kun käsittely on valmis, Cognitive Services poistaa kuitin.</span><span class="sxs-lookup"><span data-stu-id="8dfb4-159">After processing is completed, Cognitive Services will remove the receipt.</span></span> <span data-ttu-id="8dfb4-160">Kuitit tallennetaan edelleen Finance-sovellukseen.</span><span class="sxs-lookup"><span data-stu-id="8dfb4-160">Receipts are still stored in Finance.</span></span>

<span data-ttu-id="8dfb4-161">Lisätietoja on kohdassa [Lisätietoja kuiteista lomakkeen tunnistustoiminnon uuden ominaisuuden avulla](https://azure.microsoft.com/blog/enable-receipt-understanding-with-form-recognizer-s-new-capability/).</span><span class="sxs-lookup"><span data-stu-id="8dfb4-161">For more information, see [Enable receipt understanding with Form Recognizer's new capability](https://azure.microsoft.com/blog/enable-receipt-understanding-with-form-recognizer-s-new-capability/).</span></span>
