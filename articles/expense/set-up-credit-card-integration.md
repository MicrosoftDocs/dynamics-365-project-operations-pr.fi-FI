---
title: Luottokortin integroinnin määrittäminen
description: Tässä aiheessa kerrotaan, miten kuluihin liittyviä luottokorttitapahtumia käsitellään.
author: suvaidya
manager: AnnBe
ms.date: 04/02/2021
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
ms.openlocfilehash: 72ff98f5985af4362cde3c9914e0d20247f1f09a
ms.sourcegitcommit: ca0fc078d1a12484eca193fe051b8442c0559db8
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/07/2021
ms.locfileid: "5866679"
---
# <a name="set-up-credit-card-integration"></a><span data-ttu-id="f3f73-103">Luottokortin integroinnin määrittäminen</span><span class="sxs-lookup"><span data-stu-id="f3f73-103">Set up credit card integration</span></span>

<span data-ttu-id="f3f73-104">_**Koskee:** Project Operationsin resurssiin / muuhun kuin resurssiin perustuvia skenaarioita, Lite-käyttöönotto-kaupasta proformalaskutukseen_</span><span class="sxs-lookup"><span data-stu-id="f3f73-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="f3f73-105">Kuluihin liittyvät luottokorttitapahtumat voidaan määrittää automaattisesti tuotaviksi toistuvalla aikataululla.</span><span class="sxs-lookup"><span data-stu-id="f3f73-105">Expense-related credit card transactions can be set up so that they are automatically imported on a recurring schedule.</span></span> <span data-ttu-id="f3f73-106">Vaihtoehtoisesti tapahtumat voidaan tuoda manuaalisesti tarvittaessa.</span><span class="sxs-lookup"><span data-stu-id="f3f73-106">Alternatively, the transactions can be manually imported as they are required.</span></span> <span data-ttu-id="f3f73-107">Luottokorttitapahtumat tuodaan luottokorttitapahtumien tietoentiteetin kautta.</span><span class="sxs-lookup"><span data-stu-id="f3f73-107">The credit card transactions are imported through the credit card transactions data entity.</span></span>

## <a name="import-credit-card-transactions"></a><span data-ttu-id="f3f73-108">Luottokorttitapahtumien tuominen</span><span class="sxs-lookup"><span data-stu-id="f3f73-108">Import credit card transactions</span></span>

<span data-ttu-id="f3f73-109">Voit tuoda luottokorttitapahtumia seuraavia vaiheita noudattamalla:</span><span class="sxs-lookup"><span data-stu-id="f3f73-109">To import credit card transactions, follow these steps:</span></span>

1. <span data-ttu-id="f3f73-110">Valitse **Luottokorttitapahtumat**-sivulla **Tuo tapahtumat**.</span><span class="sxs-lookup"><span data-stu-id="f3f73-110">On the **Credit card transactions** page, select **Import transactions**.</span></span> <span data-ttu-id="f3f73-111">Jos avaat tietojen hallinnan ensimmäisen kerran, järjestelmän on päivitettävä tieto-entiteettiluettelo ennen kuin jatkat.</span><span class="sxs-lookup"><span data-stu-id="f3f73-111">If you’re opening data management for the first time, the system must update the list of data entities before you can continue.</span></span>
2. <span data-ttu-id="f3f73-112">Kirjoita **Nimi**-kenttään tuontityön yksilöivä kuvaus.</span><span class="sxs-lookup"><span data-stu-id="f3f73-112">In the **Name** field, enter a unique description for the import job.</span></span>
3. <span data-ttu-id="f3f73-113">Valitse **Lähdetietojen muoto** -kentässä sen tiedoston muoto, joka sisältää tuotavat luottokorttitapahtumat.</span><span class="sxs-lookup"><span data-stu-id="f3f73-113">In the **Source data format** field, select the format of the file that contains the credit card transactions to import.</span></span>
4. <span data-ttu-id="f3f73-114">Valitse **Lataa** ja etsi sitten tuotava tiedosto.</span><span class="sxs-lookup"><span data-stu-id="f3f73-114">Select **Upload**, and then find and select the file to import.</span></span>
5. <span data-ttu-id="f3f73-115">Kun tiedosto on ladattu, tarkista luottokorttitapahtumtiedoston ja luottokorttitapahtumien tietoentiteetin sarakkeiden yhdistämismääritys valitsemalla ruudun **Näytä yhdistämismääritys** -linkki.</span><span class="sxs-lookup"><span data-stu-id="f3f73-115">After the file has been uploaded, validate the mapping of the credit card transaction file and the columns of the credit card transactions data entity by selecting the **View map** link on the tile.</span></span> <span data-ttu-id="f3f73-116">Jos löytyy yhdistämismääritysvirheitä tai jos yhdistämismääritys on muutettava, tee muutokset **Yhdistämismäärityksen visualisointi** -välilehdessä tai **Yhdistämismäärityksen tiedot** -välilehdessä.</span><span class="sxs-lookup"><span data-stu-id="f3f73-116">If there are mapping errors, or if you must change the mapping, make the mapping changes from either the **Mapping visualization** tab or the **Mapping details** tab.</span></span>
6. <span data-ttu-id="f3f73-117">Jos haluat automatisoida luottokorttitapahtumia, valitse **Luo toistuva tietotyö**.</span><span class="sxs-lookup"><span data-stu-id="f3f73-117">To automate the credit card transactions, select **Create recurring data job**.</span></span> <span data-ttu-id="f3f73-118">Tämän jälkeen voit määrittää toistuvuuden, joka määrittää, miten usein luottokorttitapahtumat tuodaan.</span><span class="sxs-lookup"><span data-stu-id="f3f73-118">You can then set the recurrence that defines how often credit card transactions should be imported.</span></span> <span data-ttu-id="f3f73-119">Kun olet valmis, valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="f3f73-119">When you’ve finished, select **OK**.</span></span>
7. <span data-ttu-id="f3f73-120">Jos haluat tuoda valitun tiedoston nyt, valitse **Tuo**.</span><span class="sxs-lookup"><span data-stu-id="f3f73-120">To import the selected file now, select **Import**.</span></span>
8. <span data-ttu-id="f3f73-121">Jos tuonnin aikana ilmenee virheitä, voit tarkastella suorituslokia tai väliaikaistietoja nähdäksesi virheet, jotka on korjattava, jotta tuonti onnistuisi.</span><span class="sxs-lookup"><span data-stu-id="f3f73-121">If errors occur during the import, you can view the execution log or staging data to see the errors that you must fix to help ensure a successful import.</span></span>

> [!NOTE]
> <span data-ttu-id="f3f73-122">Jos haluat tuoda useita tiedostomuotoja, luo erilliset tuontityöt kullekin muototyypille.</span><span class="sxs-lookup"><span data-stu-id="f3f73-122">If you need to import more than one file format, you must create separate import jobs for each format type.</span></span>

## <a name="reassign-the-credit-card-transactions-for-terminated-employees"></a><span data-ttu-id="f3f73-123">Niiden työntekijöiden luottokorttitapahtumien määrittäminen uudelleen, joiden työsuhde on päättynyt</span><span class="sxs-lookup"><span data-stu-id="f3f73-123">Reassign the credit card transactions for terminated employees</span></span>

<span data-ttu-id="f3f73-124">Kun työntekijätietue päätetään, työntekijän Active Directory -toimialueen palveluiden (AD DS) tili poistetaan käytöstä.</span><span class="sxs-lookup"><span data-stu-id="f3f73-124">After an employee record is terminated, the employee’s Active Directory Domain Services (AD DS) account is disabled.</span></span> <span data-ttu-id="f3f73-125">Aktiivisia luottokorttitapahtumia, jotka on veloitettava ja korvattava, voi kuitenkin yhä olla.</span><span class="sxs-lookup"><span data-stu-id="f3f73-125">However, there might be active credit card transactions that must still be expensed and reimbursed.</span></span> <span data-ttu-id="f3f73-126">**Luottokorttitapahtumat**-sivulla voit määrittää työntekijän uudelleen luottokortin tapahtumalle, jonka mukaan liitetty työntekijä on lopetettu.</span><span class="sxs-lookup"><span data-stu-id="f3f73-126">On the **Credit card transactions** page, you can reassign the employee for any credit card transaction where the associated employee has been terminated.</span></span>

<span data-ttu-id="f3f73-127">Valitse vähintään yksi luottokorttitapahtuma ja valitse sitten **Määritä tapahtumat uudelleen**.</span><span class="sxs-lookup"><span data-stu-id="f3f73-127">Select one or more credit card transactions, and then select **Reassign transactions**.</span></span> <span data-ttu-id="f3f73-128">Tämän jälkeen voit valita toisen työntekijän, jolle luottokorttitapahtumat määritetään.</span><span class="sxs-lookup"><span data-stu-id="f3f73-128">You can then select another employee to assign the credit card transactions to.</span></span> <span data-ttu-id="f3f73-129">Kun luottokorttitapahtumat on määritetty uudelleen, ne voidaan valita kuluraporttia varten ja maksaa kuluraportin korvauksen normaalin prosessin avulla.</span><span class="sxs-lookup"><span data-stu-id="f3f73-129">After the credit card transactions have been reassigned, they can be selected for an expense report and paid through the usual process for expense report reimbursement.</span></span>

## <a name="delete-credit-card-transactions"></a><span data-ttu-id="f3f73-130">Luottokorttitapahtumien poistaminen</span><span class="sxs-lookup"><span data-stu-id="f3f73-130">Delete credit card transactions</span></span> 

<span data-ttu-id="f3f73-131">Joskus luottokorttitapahtumien tuonnin jälkeen jotkin tapahtumat on ehkä poistettava.</span><span class="sxs-lookup"><span data-stu-id="f3f73-131">Sometimes, after credit card transactions are imported, certain transactions may need to be deleted.</span></span> <span data-ttu-id="f3f73-132">Tämä voi johtuu siitä, että tapahtumat ovat kaksoiskappaleita tai siitä, että tiedot eivät ehkä ole oikeita.</span><span class="sxs-lookup"><span data-stu-id="f3f73-132">This could be because the transactions are duplicates or because the data might isn't accurate.</span></span> <span data-ttu-id="f3f73-133">Järjestelmänvalvojat voivat käyttää **Luottokorttitapahtumien poistaminen** -toimintoa valitakseen ja poistaakseen luottokorttitapahtumia, joita **ei ole liitetty** kuluraporttiin.</span><span class="sxs-lookup"><span data-stu-id="f3f73-133">Admins can use the **"Delete credit card transactions"** feature to select and delete credit card transactions that are **not attached** to an expense report.</span></span> 

1. <span data-ttu-id="f3f73-134">Siirry kohtaan **Jaksoittaiset tehtävät** > **Poista luottokorttitapahtumia**.</span><span class="sxs-lookup"><span data-stu-id="f3f73-134">Go to **Periodic tasks** > **Delete credit card transactions**.</span></span>
2. <span data-ttu-id="f3f73-135">Valitse **Suodata** ja anna sisällytettävät tietueet tunnistavat tiedot.</span><span class="sxs-lookup"><span data-stu-id="f3f73-135">Select **Filter** and provide information to identify the records to include.</span></span>
3. <span data-ttu-id="f3f73-136">Voit poistaa tietueet valitsemalla **OK**.</span><span class="sxs-lookup"><span data-stu-id="f3f73-136">Select **OK** to delete the records.</span></span> 

[!INCLUDE[footer-include](../includes/footer-banner.md)]
