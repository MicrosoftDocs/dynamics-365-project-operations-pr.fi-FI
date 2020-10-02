---
title: Luottokortin integroinnin määrittäminen
description: Tässä aihessa on tietoja kuluun liittyvien luottokorttitapahtumien tuomisesta ja ylläpitämisestä.
author: suvaidya
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: ''
ms.author: shylaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 483775e1334a281026dbfaf214d06d235255f13e
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/28/2020
ms.locfileid: "3896817"
---
# <a name="set-up-credit-card-integration"></a><span data-ttu-id="52ba9-103">Luottokortin integroinnin määrittäminen</span><span class="sxs-lookup"><span data-stu-id="52ba9-103">Set up credit card integration</span></span>

<span data-ttu-id="52ba9-104">_**Koskee:** Project Operationsin resurssiin / muuhun kuin resurssiin perustuvia skenaarioita, Lite-käyttöönotto-kaupasta proformalaskutukseen_</span><span class="sxs-lookup"><span data-stu-id="52ba9-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="52ba9-105">Kuluihin liittyvät luottokorttitapahtumat voidaan määrittää automaattisesti tuotaviksi toistuvalla aikataululla.</span><span class="sxs-lookup"><span data-stu-id="52ba9-105">Expense-related credit card transactions can be set up so that they are automatically imported on a recurring schedule.</span></span> <span data-ttu-id="52ba9-106">Vaihtoehtoisesti tapahtumat voidaan tuoda manuaalisesti tarvittaessa.</span><span class="sxs-lookup"><span data-stu-id="52ba9-106">Alternatively, the transactions can be manually imported as they are required.</span></span> <span data-ttu-id="52ba9-107">Luottokorttitapahtumat tuodaan luottokorttitapahtumien tietoentiteetin kautta.</span><span class="sxs-lookup"><span data-stu-id="52ba9-107">The credit card transactions are imported through the Credit card transactions data entity.</span></span>

## <a name="import-credit-card-transactions"></a><span data-ttu-id="52ba9-108">Luottokorttitapahtumien tuominen</span><span class="sxs-lookup"><span data-stu-id="52ba9-108">Import credit card transactions</span></span>

1. <span data-ttu-id="52ba9-109">Valitse **Luottokorttitapahtumat**-sivulla **Tuo tapahtumat**.</span><span class="sxs-lookup"><span data-stu-id="52ba9-109">On the **Credit card transactions** page, select **Import transactions**.</span></span> <span data-ttu-id="52ba9-110">Jos avaat tietojen hallinnan ensimmäisen kerran, järjestelmän on päivitettävä tieto-entiteettiluettelo ennen kuin jatkat.</span><span class="sxs-lookup"><span data-stu-id="52ba9-110">If you’re opening data management for the first time, the system must update the list of data entities before you can continue.</span></span>
2. <span data-ttu-id="52ba9-111">Anna **Nimi**-kenttään tuotavan työn yksilöivä kuvaus.</span><span class="sxs-lookup"><span data-stu-id="52ba9-111">In the **Name** field, enter a unique description of the import job.</span></span>
3. <span data-ttu-id="52ba9-112">Valitse **Lähdetietojen muoto** -kentässä sen tiedoston muoto, joka sisältää tuotavat luottokorttitapahtumat.</span><span class="sxs-lookup"><span data-stu-id="52ba9-112">In the **Source data format** field, select the format of the file that contains the credit card transactions to import.</span></span>
4. <span data-ttu-id="52ba9-113">Valitse **Lataa** ja etsi sitten tuotava tiedosto.</span><span class="sxs-lookup"><span data-stu-id="52ba9-113">Select **Upload**, and then find and select the file to import.</span></span>
5. <span data-ttu-id="52ba9-114">Kun tiedosto on ladattu, tarkista luottokorttitapahtumtiedoston ja luottokorttitapahtumien tietoentiteetin sarakkeiden yhdistämismääritys valitsemalla ruudun **Näytä yhdistämismääritys** -linkki.</span><span class="sxs-lookup"><span data-stu-id="52ba9-114">After the file has been uploaded, validate the mapping of the credit card transaction file and the columns of the Credit card transactions data entity by selecting the **View map** link on the tile.</span></span> <span data-ttu-id="52ba9-115">Jos löytyy yhdistämismääritysvirheitä tai jos yhdistämismääritys on muutettava, tee muutokset **Yhdistämismäärityksen visualisointi** -välilehdessä tai **Yhdistämismäärityksen tiedot** -välilehdessä.</span><span class="sxs-lookup"><span data-stu-id="52ba9-115">If there are mapping errors, or if you must change the mapping, make the mapping changes from either the **Mapping visualization** tab or the **Mapping details** tab.</span></span>
6. <span data-ttu-id="52ba9-116">Jos haluat automatisoida luottokorttitapahtumia, valitse **Luo toistuva tietotyö**.</span><span class="sxs-lookup"><span data-stu-id="52ba9-116">To automate the credit card transactions, select **Create recurring data job**.</span></span> <span data-ttu-id="52ba9-117">Tämän jälkeen voit määrittää toistuvuuden, joka määrittää, miten usein luottokorttitapahtumat tuodaan.</span><span class="sxs-lookup"><span data-stu-id="52ba9-117">You can then set the recurrence that defines how often credit card transactions should be imported.</span></span> <span data-ttu-id="52ba9-118">Kun olet valmis, valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="52ba9-118">When you’ve finished, select **OK**.</span></span>
7. <span data-ttu-id="52ba9-119">Jos haluat tuoda valitun tiedoston nyt, valitse **Tuo**.</span><span class="sxs-lookup"><span data-stu-id="52ba9-119">To import the selected file now, select **Import**.</span></span>
8. <span data-ttu-id="52ba9-120">Jos tuonnin aikana tapahtuu virheitä, voit tarkastella suorituslokia tai valmistelutietoja ja katsoa korjattavat virheet onnistuneen tuonnin varmistamiseksi.</span><span class="sxs-lookup"><span data-stu-id="52ba9-120">If errors occur during the import, you can view the execution log or staging data to see the errors that you must fix to help guarantee a successful import.</span></span>

> [!NOTE]
> <span data-ttu-id="52ba9-121">Jos sinun täytyy tuoda useita tiedostomuotoja, luo erilliset tuontityöt kullekin muototyypille.</span><span class="sxs-lookup"><span data-stu-id="52ba9-121">If you must import more than one file format, you must create separate import jobs for each format type.</span></span>

## <a name="reassign-the-credit-card-transactions-for-terminated-employees"></a><span data-ttu-id="52ba9-122">Niiden työntekijöiden luottokorttitapahtumien määrittäminen uudelleen, joiden työsuhde on päättynyt</span><span class="sxs-lookup"><span data-stu-id="52ba9-122">Reassign the credit card transactions for terminated employees</span></span>

<span data-ttu-id="52ba9-123">Kun työntekijätietue päätetään, työntekijän Active Directory -toimialueen palveluiden (AD DS) tili poistetaan käytöstä.</span><span class="sxs-lookup"><span data-stu-id="52ba9-123">After an employee record is terminated, the employee’s Active Directory Domain Services (AD DS) account is disabled.</span></span> <span data-ttu-id="52ba9-124">Aktiivisia luottokorttitapahtumia, jotka on veloitettava ja korvattava, voi kuitenkin yhä olla.</span><span class="sxs-lookup"><span data-stu-id="52ba9-124">However, there might be active credit card transactions that must still be expensed and reimbursed.</span></span> <span data-ttu-id="52ba9-125">**Luottokorttitapahtumat**-sivulla voit määrittää työntekijän uudelleen mihin tahansa luottokorttitapahtumaan, jonka työntekijän työsuhde on päättynyt.</span><span class="sxs-lookup"><span data-stu-id="52ba9-125">From the **Credit card transactions** page, you can reassign the employee for any credit card transaction where the associated employee has been terminated.</span></span>

<span data-ttu-id="52ba9-126">Valitse vähintään yksi luottokorttitapahtuma ja valitse sitten **Määritä tapahtumat uudelleen**.</span><span class="sxs-lookup"><span data-stu-id="52ba9-126">Select one or more credit card transactions, and then select **Reassign transactions**.</span></span> <span data-ttu-id="52ba9-127">Tämän jälkeen voit valita toisen työntekijän, jolle luottokorttitapahtumat määritetään.</span><span class="sxs-lookup"><span data-stu-id="52ba9-127">You can then select another employee to assign the credit card transactions to.</span></span> <span data-ttu-id="52ba9-128">Kun luottokorttitapahtumat on määritetty uudelleen, ne voidaan valita kuluraporttia varten ja maksaa kuluraportin korvauksen normaalin prosessin avulla.</span><span class="sxs-lookup"><span data-stu-id="52ba9-128">After the credit card transactions have been reassigned, they can be selected for an expense report and paid through the usual process for expense report reimbursement.</span></span>
