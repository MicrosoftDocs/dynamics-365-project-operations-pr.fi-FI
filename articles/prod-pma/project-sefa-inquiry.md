---
title: Federal Awards -tutkimuksen kulujen aikataulu
description: Tässä aiheessa on tietoja Federal Awards -tutkimuksen kulujen aikataulusta.
author: velofog
manager: Ann Beebe
ms.date: 04/2/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PSNProjSEFAinquiry
audience: Application User
ms.devlang: ''
ms.reviewer: roschlom
ms.search.scope: Operations, Core
ms.tgt_pltfrm: ''
ms.custom: ''
ms.search.region: Global
ms.search.industry: public sector
ms.author: andchoi
ms.search.validFrom: 2020-4-01
ms.dyn365.ops.version: 10.0.11
ms.openlocfilehash: 70dff12c106723dda801668412cfd084c462db4b
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5288960"
---
# <a name="schedule-of-expenditures-of-federal-awards-inquiry"></a><span data-ttu-id="0a2d5-103">Federal Awards -tutkimuksen kulujen aikataulu</span><span class="sxs-lookup"><span data-stu-id="0a2d5-103">Schedule of Expenditures of Federal Awards inquiry</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0a2d5-104">Hallinto- ja budjettitoimiston (Circular A-133) mukaan viranomaiset, jotka vastaanottavat liittovaltion varoja, kuuluvat auditoinnin vaatimuksiin, joita kutsutaan myös yksittäiseksi tarkastuksiksi.</span><span class="sxs-lookup"><span data-stu-id="0a2d5-104">According to Office of Management and Budget Circular A-133, agencies that receive federal funds are subject to audit requirements, which are also known as single audits.</span></span> <span data-ttu-id="0a2d5-105">Auditointiprosessin avulla voidaan raportoida liittovaltion apurahojen tuotoista ja menoista toistuvasti.</span><span class="sxs-lookup"><span data-stu-id="0a2d5-105">The audit process is used to report on the revenues and expenditures of federal grants on a recurring basis.</span></span> <span data-ttu-id="0a2d5-106">Osa yhtenäisestä auditointiraportista sisältää Federal Awards -ohjelman (SEFA) kulujen aikataulun.</span><span class="sxs-lookup"><span data-stu-id="0a2d5-106">Part of the single audit report includes the Schedule of Expenditures of Federal Awards (SEFA).</span></span>

<span data-ttu-id="0a2d5-107">Federal Awards -tutkimuksen kulujen luettelo sisältää Federal Assistance (CFDA) -osaston ja -numeron, avustusnumeron, avustuksen vuoden, liittovaltion toimiston, joka tarjoaa varat, sekä sen nimen, jossa läpimenoentiteetti on.</span><span class="sxs-lookup"><span data-stu-id="0a2d5-107">The Schedule of Expenditures of Federal Awards inquiry includes the Catalog of Federal Domestic Assistance (CFDA) title and number, the grant number, the year of the grant, the name of the federal agency that provides the funds, and the name of the pass-through entity.</span></span> <span data-ttu-id="0a2d5-108">Kysely on tiettynä ajanjaksona.</span><span class="sxs-lookup"><span data-stu-id="0a2d5-108">The inquiry is for a specific period.</span></span> <span data-ttu-id="0a2d5-109">Yleensä kyseinen kausi on sama kuin tilinpäätöskausi, joka on tilikausi.</span><span class="sxs-lookup"><span data-stu-id="0a2d5-109">Typically, that period is the same as the financial statement period, which is a fiscal year.</span></span>

<span data-ttu-id="0a2d5-110">Kysely sisältää apurahoja, joiden ennustepäivämäärät ovat valitulla päivämäärävälillä.</span><span class="sxs-lookup"><span data-stu-id="0a2d5-110">The inquiry includes grants that have projection dates in the selected date range.</span></span> <span data-ttu-id="0a2d5-111">**Kyselyn myöntäjä** -sarakkeessa näkyy apuraha-asiakas tai apurahan myöntäjä.</span><span class="sxs-lookup"><span data-stu-id="0a2d5-111">The **Grantor agency** column of the inquiry shows the grant customer or, for a pass-through grant, the grantor agency.</span></span> <span data-ttu-id="0a2d5-112">Myönnettyä apurahaa varten **Myöntävä toimisto**-sarake näyttää apurahan asiakkaan.</span><span class="sxs-lookup"><span data-stu-id="0a2d5-112">For a pass-through grant, the **Pass-through agency** column shows the grant customer.</span></span> <span data-ttu-id="0a2d5-113">Jos apuraha ei ole myönnetty apuraha, **Myöntävä toimisto**-sarake on tyhjä.</span><span class="sxs-lookup"><span data-stu-id="0a2d5-113">If the grant isn't a pass-through grant, the **Pass-through agency** column is blank.</span></span>

## <a name="set-up-the-cfda-clusters"></a><span data-ttu-id="0a2d5-114">Määritä CFDA-klusterit</span><span class="sxs-lookup"><span data-stu-id="0a2d5-114">Set up the CFDA clusters</span></span>

<span data-ttu-id="0a2d5-115">Sinun täytyy määrittää CFDA-klusterit, jotka voidaan liittää CFDA-numeroihin Federal Awards -kyselyn kulujen aikataulussa.</span><span class="sxs-lookup"><span data-stu-id="0a2d5-115">You must set up the CFDA clusters that can be associated with CFDA numbers in the Schedule of Expenditures of Federal Awards inquiry.</span></span>

1. <span data-ttu-id="0a2d5-116">Siirry kohtaan **projektinhallinta ja kirjanpito \> asetukset \> apurahat \> luettelo liittovaltion kotimaisista avustusklustereista**.</span><span class="sxs-lookup"><span data-stu-id="0a2d5-116">Go to **Project management and accounting \> Setup \> Grants \> Catalog of Federal Domestic Assistance clusters**.</span></span>
2. <span data-ttu-id="0a2d5-117">Jos haluat luoda uuden CFDA-klusterin, valitse **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="0a2d5-117">Select **New** to create a CFDA cluster.</span></span>
3. <span data-ttu-id="0a2d5-118">Anna klusterin nimi.</span><span class="sxs-lookup"><span data-stu-id="0a2d5-118">Enter the cluster name.</span></span>
4. <span data-ttu-id="0a2d5-119">Tallenna muutokset valitsemalla **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="0a2d5-119">Select **Save** to save your changes.</span></span>

## <a name="set-up-cfda-numbers"></a><span data-ttu-id="0a2d5-120">CFDA-numeroiden määrittäminen</span><span class="sxs-lookup"><span data-stu-id="0a2d5-120">Set up CFDA numbers</span></span>

<span data-ttu-id="0a2d5-121">Sinun on määritettävä CFDA-numerot, jotka voidaan lisätä apurahoihin ja sisällyttää liittovaltion palkintojen kyselyaikatauluun.</span><span class="sxs-lookup"><span data-stu-id="0a2d5-121">You must set up CFDA numbers that can be added to grants and included in the Schedule of Expenditures of Federal Awards inquiry.</span></span>

1. <span data-ttu-id="0a2d5-122">Siirry kohtaan **projektinhallinta ja kirjanpito \> asetukset \> apurahat \> luettelo liittovaltion kotimaisista avustusnumeroista**.</span><span class="sxs-lookup"><span data-stu-id="0a2d5-122">Go to **Project management and accounting \> Setup \> Grants \> Catalog of Federal Domestic Assistance numbers**.</span></span>
2. <span data-ttu-id="0a2d5-123">Jos haluat luoda CFDA-numeron, valitse **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="0a2d5-123">Select **New** to create a CFDA number.</span></span>
3. <span data-ttu-id="0a2d5-124">Kirjoita CFDA-numero **Numero**-sarakkeeseen.</span><span class="sxs-lookup"><span data-stu-id="0a2d5-124">In the **Number** column, enter the CFDA number.</span></span>
4. <span data-ttu-id="0a2d5-125">Paina **sarkain**-näppäintä.</span><span class="sxs-lookup"><span data-stu-id="0a2d5-125">Press the **Tab** key.</span></span>
5. <span data-ttu-id="0a2d5-126">Kirjoita CFDA-ruutuun **Kuvaus**-sarakkeessa.</span><span class="sxs-lookup"><span data-stu-id="0a2d5-126">In the **Description** column, enter the CFDA title.</span></span>
6. <span data-ttu-id="0a2d5-127">Paina **sarkain**-näppäintä.</span><span class="sxs-lookup"><span data-stu-id="0a2d5-127">Press the **Tab** key.</span></span>
7. <span data-ttu-id="0a2d5-128">Valinnainen: Lisää **Ohjelman klusteri** -kenttään sopiva CFDA-klusteri.</span><span class="sxs-lookup"><span data-stu-id="0a2d5-128">Optional: In the **Program cluster** field, add the appropriate CFDA cluster.</span></span>
8. <span data-ttu-id="0a2d5-129">Tallenna muutokset valitsemalla **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="0a2d5-129">Select **Save** to save your changes.</span></span>

## <a name="set-up-grants-to-report-for-the-schedule-of-expenditures-of-federal-awards-inquiry"></a><span data-ttu-id="0a2d5-130">Määritä apurahat, jotka raportoivat Federal Awards -tutkimuksen kulujen aikataulusta</span><span class="sxs-lookup"><span data-stu-id="0a2d5-130">Set up grants to report for the Schedule of Expenditures of Federal Awards inquiry</span></span>

1. <span data-ttu-id="0a2d5-131">Siirry kohtaan **projektin hallinta ja kirjan pito \> avustukset \> avustukset** ja valitse olemassa oleva avustus.</span><span class="sxs-lookup"><span data-stu-id="0a2d5-131">Go to **Project management and accounting \> Grants \> Grants**, and select an existing grant.</span></span>
2. <span data-ttu-id="0a2d5-132">Määritä **Asetukset**-pikavälilehden **Federal Domestic Assistance- luettelo** -kentän luettelossa CFDA-numero.</span><span class="sxs-lookup"><span data-stu-id="0a2d5-132">On the **Setup** FastTab, in the **Catalog of Federal Domestic Assistance** field, assign the CFDA number.</span></span> <span data-ttu-id="0a2d5-133">Apurahan CFDA-numero määrittää CFDA-klusterin raportointia varten.</span><span class="sxs-lookup"><span data-stu-id="0a2d5-133">The CFDA number on the grant determines the CFDA cluster for reporting.</span></span>
3. <span data-ttu-id="0a2d5-134">Kirjoita **yhteyshenkilön tiedot** -pikavälilehden myöntäjä-tiedot seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="0a2d5-134">On **Contact information** FastTab, enter the grantor information by following these steps:</span></span>

    1. <span data-ttu-id="0a2d5-135">Kirjoita **Avustusasiakas**-kenttään avustuksesta vastaava asiakas.</span><span class="sxs-lookup"><span data-stu-id="0a2d5-135">In the **Grant customer** field, enter the customer who is responsible for the grant.</span></span> <span data-ttu-id="0a2d5-136">Jos kyseessä on olemassa oleva apuraha, nämä tiedot on ehkä jo syötetty.</span><span class="sxs-lookup"><span data-stu-id="0a2d5-136">For an existing grant, this information might already be entered.</span></span>
    2. <span data-ttu-id="0a2d5-137">Ilmaise, onko avustusasiakas rahoittaja.</span><span class="sxs-lookup"><span data-stu-id="0a2d5-137">Indicate whether the grant customer is the funder.</span></span> <span data-ttu-id="0a2d5-138">Jos avustusasiakas on rahoittaja, jätä **läpivalinta**-ruutu tyhjäksi.</span><span class="sxs-lookup"><span data-stu-id="0a2d5-138">If the grant customer is the funder, leave the **Pass-through** check box cleared.</span></span> <span data-ttu-id="0a2d5-139">Jos toinen asiakas on rahoittaja ja avustusasiakas on vastuussa rahavarojen käytöstä ja seurannasta, valitse **Läpimeno**-valintaruutu.</span><span class="sxs-lookup"><span data-stu-id="0a2d5-139">If another customer is the funder, and the grant customer is responsible for spending and tracking the money, select the **Pass-through** check box.</span></span>

4. <span data-ttu-id="0a2d5-140">Jos valitsit edellisessä vaiheessa **läpimeno**-valintaruudun, anna **myöntäjätoimisto**-kenttään avustuksen toimittanut asiakas.</span><span class="sxs-lookup"><span data-stu-id="0a2d5-140">If you selected the **Pass-through** check box in the previous step, in the **Grantor agency** field, enter the customer who provided the grant.</span></span> <span data-ttu-id="0a2d5-141">Myöntäjä ja avustusasiakas eivät voi olla sama asiakas.</span><span class="sxs-lookup"><span data-stu-id="0a2d5-141">The grantor agency and the grant customer can't be the same customer.</span></span>

<span data-ttu-id="0a2d5-142">Seuraavassa on esimerkki läpilaskuavustuksesta:</span><span class="sxs-lookup"><span data-stu-id="0a2d5-142">Here is an example of a pass-through grant:</span></span>

<span data-ttu-id="0a2d5-143">Liittohallitus rahoitti valtion infrastruktuurihanketta.</span><span class="sxs-lookup"><span data-stu-id="0a2d5-143">The federal government funded an infrastructure project for a state.</span></span> <span data-ttu-id="0a2d5-144">Liittohallitus antoi rahat valtiolle.</span><span class="sxs-lookup"><span data-stu-id="0a2d5-144">The federal government gave the money to the state to spend.</span></span> <span data-ttu-id="0a2d5-145">Tässä tapauksessa liittohallitus on myöntäjä, ja osavaltio on avustusasiakas.</span><span class="sxs-lookup"><span data-stu-id="0a2d5-145">In this case, the federal government is the grantor agency, and the state is the grant customer.</span></span>

> [!NOTE] 
> <span data-ttu-id="0a2d5-146">Kun otat ominaisuuden käyttöön ensimmäisen kerran, ensimmäiset CFDA-numerot syötetään avustuksina olevien lukujen perusteella.</span><span class="sxs-lookup"><span data-stu-id="0a2d5-146">When you first turn on the feature, initial CFDA numbers will be entered by using the existing numbers on grants.</span></span>

## <a name="exclude-grants-from-sefa-reporting-based-on-the-grant-type"></a><span data-ttu-id="0a2d5-147">Älä sisällytä avustuksia SEFA-raportointiin avustustyypin perusteella</span><span class="sxs-lookup"><span data-stu-id="0a2d5-147">Exclude grants from SEFA reporting based on the grant type</span></span>

1. <span data-ttu-id="0a2d5-148">Siirry kohtaan **Projektinhallinta ja kirjanpito \> Määritys \> Avustukset \> Avustustyypit**.</span><span class="sxs-lookup"><span data-stu-id="0a2d5-148">Go to **Project management and accounting \> Setup \> Grants \> Grant types**.</span></span>
2. <span data-ttu-id="0a2d5-149">Valitse **Oletustiedot**-pikavälilehdessä **Ohita Federal Awards -ohjelman kulut** -valintaruutu.</span><span class="sxs-lookup"><span data-stu-id="0a2d5-149">On the **Default information** FastTab, select the **Exclude from Schedule of Expenditures of Federal Awards** check box.</span></span>
3. <span data-ttu-id="0a2d5-150">Tallenna muutokset valitsemalla **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="0a2d5-150">Select **Save** to save your changes.</span></span>

## <a name="run-the-schedule-of-expenditures-of-federal-awards-inquiry"></a><span data-ttu-id="0a2d5-151">Aja Federal Awards -tutkimuksen kulujen aikataulukysely</span><span class="sxs-lookup"><span data-stu-id="0a2d5-151">Run the Schedule of Expenditures of Federal Awards inquiry</span></span>

1. <span data-ttu-id="0a2d5-152">Siirry **projektinhallinta ja kirjanpito \> kyselyt ja raportit \> apurahakyselyt \> Federal Awards -tutkimuksen aikatauluun**.</span><span class="sxs-lookup"><span data-stu-id="0a2d5-152">Go to **Project management and accounting \> Inquiries and reports \> Grant inquiry \> Schedule of Expenditures of Federal Awards**.</span></span>
2. <span data-ttu-id="0a2d5-153">Toimi **Parameterit**-osassa seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="0a2d5-153">In the **Parameters** section, follow these steps:</span></span>

    1. <span data-ttu-id="0a2d5-154">Valitse **päivämääräväli**-kentässä päivämäärävälin koodi.</span><span class="sxs-lookup"><span data-stu-id="0a2d5-154">In the **Date interval** field, select the code for the date interval.</span></span> <span data-ttu-id="0a2d5-155">Voit vaihtoehtoisesti määrittää päivämäärävälin **alkamispäivä**- ja **pvm:stä**- kenttiin.</span><span class="sxs-lookup"><span data-stu-id="0a2d5-155">Alternatively, in the **From date** and **To date** fields, define the date interval.</span></span>
    2. <span data-ttu-id="0a2d5-156">Valinnainen: Jos haluat, että kyselyyn sisällytetään vain laskutetut tapahtumat, määritä **Sisällytä vain laskutetut tulot** -asetuksen arvoksi **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="0a2d5-156">Optional: To include only billed transactions as revenue in the inquiry, set the **Include only billed revenues** option to **Yes**.</span></span>

## <a name="columns"></a><span data-ttu-id="0a2d5-157">Sarakkeet</span><span class="sxs-lookup"><span data-stu-id="0a2d5-157">Columns</span></span>

<span data-ttu-id="0a2d5-158">Federal Awards -tutkimuksen kulujen aikataulu sisältää seuraavat sarakkeet:</span><span class="sxs-lookup"><span data-stu-id="0a2d5-158">The Schedule of Expenditures of Federal Awards inquiry includes the following columns:</span></span>

- <span data-ttu-id="0a2d5-159">Federal Domestic Assistance -klusterin nimi</span><span class="sxs-lookup"><span data-stu-id="0a2d5-159">Catalog of Federal Domestic Assistance cluster name</span></span>
- <span data-ttu-id="0a2d5-160">Myöntäjä</span><span class="sxs-lookup"><span data-stu-id="0a2d5-160">Grantor agency</span></span>
- <span data-ttu-id="0a2d5-161">Läpivientiyritys</span><span class="sxs-lookup"><span data-stu-id="0a2d5-161">Pass-through agency</span></span>
- <span data-ttu-id="0a2d5-162">Avustuksen nimi</span><span class="sxs-lookup"><span data-stu-id="0a2d5-162">Grant name</span></span>
- <span data-ttu-id="0a2d5-163">Avustuksen tunnus</span><span class="sxs-lookup"><span data-stu-id="0a2d5-163">Grant ID</span></span>
- <span data-ttu-id="0a2d5-164">Avustushakemuksen tunnus</span><span class="sxs-lookup"><span data-stu-id="0a2d5-164">Grant application ID</span></span>
- <span data-ttu-id="0a2d5-165">Federal Domestic Assistance -luettelo</span><span class="sxs-lookup"><span data-stu-id="0a2d5-165">Catalog of Federal Domestic Assistance</span></span>
- <span data-ttu-id="0a2d5-166">Kuitit</span><span class="sxs-lookup"><span data-stu-id="0a2d5-166">Receipts</span></span>
- <span data-ttu-id="0a2d5-167">Menot</span><span class="sxs-lookup"><span data-stu-id="0a2d5-167">Expenditures</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]