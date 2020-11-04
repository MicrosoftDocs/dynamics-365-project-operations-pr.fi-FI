---
title: Luottokorttitapahtumien tuonti ja ylläpitäminen
description: Tässä aihessa on tietoja kuluun liittyvien luottokorttitapahtumien tuomisesta ja ylläpitämisestä. Nämä tapahtumat voidaan määrittää siten, että ne tuodaan automaattisesti toistuvaan aikatauluun, tai ne voidaan tuoda manuaalisesti tarpeen mukaan.
author: KimANelson
manager: AnnBe
ms.date: 01/12/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TrvPbsMainDataLines
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 274023
ms.assetid: 3605eda1-a7ed-4675-8031-5279c5a8f5e4
ms.search.region: Global
ms.author: suvaidya
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.openlocfilehash: 6cec15e436bc699e361577c970dd5845c6c68908
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/16/2020
ms.locfileid: "4075501"
---
# <a name="import-and-maintain-credit-card-transactions"></a><span data-ttu-id="b2233-104">Luottokorttitapahtumien tuonti ja ylläpitäminen</span><span class="sxs-lookup"><span data-stu-id="b2233-104">Import and maintain credit card transactions</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b2233-105">Kuluihin liittyvät luottokorttitapahtumat voidaan määrittää automaattisesti tuotaviksi toistuvalla aikataululla.</span><span class="sxs-lookup"><span data-stu-id="b2233-105">Expense-related credit card transactions can be set up so that they are automatically imported on a recurring schedule.</span></span> <span data-ttu-id="b2233-106">Vaihtoehtoisesti tapahtumat voidaan tuoda manuaalisesti tarvittaessa.</span><span class="sxs-lookup"><span data-stu-id="b2233-106">Alternatively, the transactions can be manually imported as they are required.</span></span> <span data-ttu-id="b2233-107">Luottokorttitapahtumat tuodaan luottokorttitapahtumien tietoentiteetin kautta.</span><span class="sxs-lookup"><span data-stu-id="b2233-107">The credit card transactions are imported through the Credit card transactions data entity.</span></span>

<span data-ttu-id="b2233-108">Lisätietoja tietoyksiköistä on kohdassa [Tietoyksiköt](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/data-entities/data-entities).</span><span class="sxs-lookup"><span data-stu-id="b2233-108">For more information about data entities, see [Data entities](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/data-entities/data-entities).</span></span>

## <a name="import-credit-card-transactions"></a><span data-ttu-id="b2233-109">Luottokorttitapahtumien tuominen</span><span class="sxs-lookup"><span data-stu-id="b2233-109">Import credit card transactions</span></span>

1. <span data-ttu-id="b2233-110">Valitse **Luottokorttitapahtumat** -sivulla **Tuo tapahtumat**.</span><span class="sxs-lookup"><span data-stu-id="b2233-110">On the **Credit card transactions** page, select **Import transactions**.</span></span> <span data-ttu-id="b2233-111">Jos avaat tietojen hallinnan ensimmäisen kerran, järjestelmän on päivitettävä tieto-entiteettiluettelo ennen kuin jatkat.</span><span class="sxs-lookup"><span data-stu-id="b2233-111">If you’re opening data management for the first time, the system must update the list of data entities before you can continue.</span></span>
2. <span data-ttu-id="b2233-112">Anna **Nimi** -kenttään tuotavan työn yksilöivä kuvaus.</span><span class="sxs-lookup"><span data-stu-id="b2233-112">In the **Name** field, enter a unique description of the import job.</span></span>
3. <span data-ttu-id="b2233-113">Valitse **Lähdetietojen muoto** -kentässä sen tiedoston muoto, joka sisältää tuotavat luottokorttitapahtumat.</span><span class="sxs-lookup"><span data-stu-id="b2233-113">In the **Source data format** field, select the format of the file that contains the credit card transactions to import.</span></span>
4. <span data-ttu-id="b2233-114">Valitse **Lataa** ja etsi sitten tuotava tiedosto.</span><span class="sxs-lookup"><span data-stu-id="b2233-114">Select **Upload** , and then find and select the file to import.</span></span>
5. <span data-ttu-id="b2233-115">Kun tiedosto on ladattu, tarkista luottokorttitapahtumtiedoston ja luottokorttitapahtumien tietoentiteetin sarakkeiden yhdistämismääritys valitsemalla ruudun **Näytä yhdistämismääritys** -linkki.</span><span class="sxs-lookup"><span data-stu-id="b2233-115">After the file has been uploaded, validate the mapping of the credit card transaction file and the columns of the Credit card transactions data entity by selecting the **View map** link on the tile.</span></span> <span data-ttu-id="b2233-116">Jos löytyy yhdistämismääritysvirheitä tai jos yhdistämismääritys on muutettava, tee muutokset **Yhdistämismäärityksen visualisointi** -välilehdessä tai **Yhdistämismäärityksen tiedot** -välilehdessä.</span><span class="sxs-lookup"><span data-stu-id="b2233-116">If there are mapping errors, or if you must change the mapping, make the mapping changes from either the **Mapping visualization** tab or the **Mapping details** tab.</span></span>
6. <span data-ttu-id="b2233-117">Jos haluat automatisoida luottokorttitapahtumia, valitse **Luo toistuva tietotyö**.</span><span class="sxs-lookup"><span data-stu-id="b2233-117">To automate the credit card transactions, select **Create recurring data job**.</span></span> <span data-ttu-id="b2233-118">Tämän jälkeen voit määrittää toistuvuuden, joka määrittää, miten usein luottokorttitapahtumat tuodaan.</span><span class="sxs-lookup"><span data-stu-id="b2233-118">You can then set the recurrence that defines how often credit card transactions should be imported.</span></span> <span data-ttu-id="b2233-119">Kun olet valmis, valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="b2233-119">When you’ve finished, select **OK**.</span></span>
7. <span data-ttu-id="b2233-120">Jos haluat tuoda valitun tiedoston nyt, valitse **Tuo**.</span><span class="sxs-lookup"><span data-stu-id="b2233-120">To import the selected file now, select **Import**.</span></span>
8. <span data-ttu-id="b2233-121">Jos tuonnin aikana tapahtuu virheitä, voit tarkastella suorituslokia tai valmistelutietoja ja katsoa korjattavat virheet onnistuneen tuonnin varmistamiseksi.</span><span class="sxs-lookup"><span data-stu-id="b2233-121">If errors occur during the import, you can view the execution log or staging data to see the errors that you must fix to help guarantee a successful import.</span></span>

> [!NOTE]
> <span data-ttu-id="b2233-122">Jos sinun täytyy tuoda useita tiedostomuotoja, luo erilliset tuontityöt kullekin muototyypille.</span><span class="sxs-lookup"><span data-stu-id="b2233-122">If you must import more than one file format, you must create separate import jobs for each format type.</span></span>

## <a name="reassign-the-credit-card-transactions-for-terminated-employees"></a><span data-ttu-id="b2233-123">Niiden työntekijöiden luottokorttitapahtumien määrittäminen uudelleen, joiden työsuhde on päättynyt</span><span class="sxs-lookup"><span data-stu-id="b2233-123">Reassign the credit card transactions for terminated employees</span></span>

<span data-ttu-id="b2233-124">Kun työntekijätietue päätetään, työntekijän Active Directory -toimialueen palveluiden (AD DS) tili poistetaan käytöstä.</span><span class="sxs-lookup"><span data-stu-id="b2233-124">After an employee record is terminated, the employee’s Active Directory Domain Services (AD DS) account is disabled.</span></span> <span data-ttu-id="b2233-125">Aktiivisia luottokorttitapahtumia, jotka on veloitettava ja korvattava, voi kuitenkin yhä olla.</span><span class="sxs-lookup"><span data-stu-id="b2233-125">However, there might be active credit card transactions that must still be expensed and reimbursed.</span></span> <span data-ttu-id="b2233-126">**Luottokorttitapahtumat** -sivulla voit määrittää työntekijän uudelleen mihin tahansa luottokorttitapahtumaan, jonka työntekijän työsuhde on päättynyt.</span><span class="sxs-lookup"><span data-stu-id="b2233-126">From the **Credit card transactions** page, you can reassign the employee for any credit card transaction where the associated employee has been terminated.</span></span>

<span data-ttu-id="b2233-127">Valitse vähintään yksi luottokorttitapahtuma ja valitse sitten **Määritä tapahtumat uudelleen**.</span><span class="sxs-lookup"><span data-stu-id="b2233-127">Select one or more credit card transactions, and then select **Reassign transactions**.</span></span> <span data-ttu-id="b2233-128">Tämän jälkeen voit valita toisen työntekijän, jolle luottokorttitapahtumat määritetään.</span><span class="sxs-lookup"><span data-stu-id="b2233-128">You can then select another employee to assign the credit card transactions to.</span></span> <span data-ttu-id="b2233-129">Kun luottokorttitapahtumat on määritetty uudelleen, ne voidaan valita kuluraporttia varten ja maksaa kuluraportin korvauksen normaalin prosessin avulla.</span><span class="sxs-lookup"><span data-stu-id="b2233-129">After the credit card transactions have been reassigned, they can be selected for an expense report and paid through the usual process for expense report reimbursement.</span></span>
