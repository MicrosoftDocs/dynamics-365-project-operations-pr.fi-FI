---
title: Taloushallinnon dimension oletusarvot
description: Tässä aiheessa on tietoja taloushallinnon dimension oletusarvojen määrittämisestä.
author: sigitac
manager: Annbe
ms.date: 10/26/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 0a76447bb1a81a7157fccc0cd58eddd1eb5995de
ms.sourcegitcommit: 3d78338773929121d17ec3386f6cb67bfb2272cc
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/27/2021
ms.locfileid: "5950125"
---
# <a name="financial-dimension-defaults"></a><span data-ttu-id="2d7d4-103">Taloushallinnon dimension oletusarvot</span><span class="sxs-lookup"><span data-stu-id="2d7d4-103">Financial dimension defaults</span></span>

<span data-ttu-id="2d7d4-104">_**Käytetään:** Project Operationsin resursseihin ja ei-varastoitaviin perustuvissa skenaarioissa_</span><span class="sxs-lookup"><span data-stu-id="2d7d4-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="2d7d4-105">Dynamics 365 Project Operations käyttää [Taloushallinnon dimensiot](/dynamics365/finance/general-ledger/financial-dimensions) kehystä Dynamics 365 Financessa antamaan lisää merkityksellisiä tietoja projektin alitapahtumarekisterin ja yleisen tapahtumarekisterin tapahtumista.</span><span class="sxs-lookup"><span data-stu-id="2d7d4-105">Dynamics 365 Project Operations uses the [Financial dimensions](/dynamics365/finance/general-ledger/financial-dimensions) framework in Dynamics 365 Finance to provide additional insights on project subledger and general ledger transactions.</span></span>

<span data-ttu-id="2d7d4-106">Taloushallinnon oletusdimensiot voidaan määrittää asiakkaassa, projektin rajoituslähteessä, välitavoitteessa, projektin sopimusrivillä tai projektissa.</span><span class="sxs-lookup"><span data-stu-id="2d7d4-106">Default financial dimensions can be set on a customer, project funding source, milestone, project contract line, or project.</span></span>

## <a name="define-default-financial-dimensions-for-a-customer"></a><span data-ttu-id="2d7d4-107">Asiakkaan taloushallinnon oletusdimensioiden määrittäminen</span><span class="sxs-lookup"><span data-stu-id="2d7d4-107">Define default financial dimensions for a customer</span></span>

<span data-ttu-id="2d7d4-108">Asiakkaan dimensio-oletukset määritetään Financessa.</span><span class="sxs-lookup"><span data-stu-id="2d7d4-108">Customer dimension defaults are specified in Finance.</span></span> <span data-ttu-id="2d7d4-109">Määritä dimensio-oletukset suorittamalla seuraavat vaiheet.</span><span class="sxs-lookup"><span data-stu-id="2d7d4-109">Complete the following steps to set dimension defaults.</span></span>

1. <span data-ttu-id="2d7d4-110">Valitse **Myyntireskontra** > **Asiakkaat** > **Kaikki asiakkaat**.</span><span class="sxs-lookup"><span data-stu-id="2d7d4-110">Go to **Accounts receivable** > **Customers** > **All customers**.</span></span>
2. <span data-ttu-id="2d7d4-111">Määritä tietyn asiakkaan talousdimension arvot **Asiakkaat**-sivun **Taloushallinnon dimensiot** -välilehdessä.</span><span class="sxs-lookup"><span data-stu-id="2d7d4-111">On the **Customers** page, on the **Financial dimensions** tab, set the financial dimension values for specific customer.</span></span>

## <a name="define-default-financial-dimensions-for-project-contracts"></a><span data-ttu-id="2d7d4-112">Projektisopimuksen taloushallinnon oletusdimensioiden määrittäminen</span><span class="sxs-lookup"><span data-stu-id="2d7d4-112">Define default financial dimensions for project contracts</span></span>

<span data-ttu-id="2d7d4-113">Projektisopimukset luodaan ja niitä ylläpidetään Common Data Servicessa (CDS).</span><span class="sxs-lookup"><span data-stu-id="2d7d4-113">Project contracts are created and maintained in Common Data Service (CDS).</span></span> <span data-ttu-id="2d7d4-114">Projektisopimusten kirjanpitomääritteet määritetään Financen **Projektinhallinta ja kirjanpito** -moduulissa.</span><span class="sxs-lookup"><span data-stu-id="2d7d4-114">Accounting attributes for project contracts are set in the **Project management and accounting** module in Finance.</span></span>

### <a name="set-financial-dimensions-for-a-project-funding-source"></a><span data-ttu-id="2d7d4-115">Projektin rahoituslähteen taloushallinnon dimensioiden määrittäminen</span><span class="sxs-lookup"><span data-stu-id="2d7d4-115">Set financial dimensions for a project funding source</span></span>

1. <span data-ttu-id="2d7d4-116">Valitse **Projektinhallinta ja kirjanpito** > **Projektit** > **Projektiyhteyshenkilöt**.</span><span class="sxs-lookup"><span data-stu-id="2d7d4-116">Go to **Project management and accounting** > **Projects** > **Project contracts**.</span></span>
2. <span data-ttu-id="2d7d4-117">Valitse päivitettävä tietue ja valitse sitten **Projektisopimus**-välilehdessä **Näytä oletuskirjanpito**.</span><span class="sxs-lookup"><span data-stu-id="2d7d4-117">Select the record you want to update, and on the **Project contract** tab, select **Show default accounting**.</span></span>
3. <span data-ttu-id="2d7d4-118">Laajenna **Liittyvät tiedot** ja valitse **Rahoituslähteet**-välilehti.</span><span class="sxs-lookup"><span data-stu-id="2d7d4-118">Expand **Related information** and select the **Funding sources** tab.</span></span>
4. <span data-ttu-id="2d7d4-119">Määritä taloushallinnon dimension oletusarvot.</span><span class="sxs-lookup"><span data-stu-id="2d7d4-119">Set the financial dimension defaults.</span></span> <span data-ttu-id="2d7d4-120">Huomaa, että taloushallinnon dimensioiden oletusarvo saadaan asiakastililtä.</span><span class="sxs-lookup"><span data-stu-id="2d7d4-120">Notice that the financial dimensions default from the customer account.</span></span>

### <a name="set-financial-dimensions-for-a-project-contract-line"></a><span data-ttu-id="2d7d4-121">Projektin sopimusrivin taloushallinnon dimensioiden määrittäminen</span><span class="sxs-lookup"><span data-stu-id="2d7d4-121">Set financial dimensions for a project contract line</span></span>

1. <span data-ttu-id="2d7d4-122">Valitse **Projektinhallinta ja kirjanpito** > **Projektit** > **Projektiyhteyshenkilöt**.</span><span class="sxs-lookup"><span data-stu-id="2d7d4-122">Go to **Project management and accounting** > **Projects** > **Project contracts**.</span></span>
2. <span data-ttu-id="2d7d4-123">Valitse päivitettävä tietue ja valitse sitten **Projektisopimus**-välilehdessä **Näytä oletuskirjanpito**.</span><span class="sxs-lookup"><span data-stu-id="2d7d4-123">Select the record you want to update and on the **Project contract** tab, select **Show default accounting**.</span></span>
3. <span data-ttu-id="2d7d4-124">Laajenna **Liittyvät tiedot** ja valitse **Sopimusrivit**-välilehti.</span><span class="sxs-lookup"><span data-stu-id="2d7d4-124">Expand **Related information** and select the **Contract lines** tab.</span></span>
4. <span data-ttu-id="2d7d4-125">Määritä taloushallinnon dimension oletusarvot.</span><span class="sxs-lookup"><span data-stu-id="2d7d4-125">Set the financial dimension defaults.</span></span> <span data-ttu-id="2d7d4-126">Taloushallinnon dimension oletusarvot ovat käytettävissä, ja niitä voi käyttää vain kiinteähintaisilla (välitavoitteiden) sopimusrivillä.</span><span class="sxs-lookup"><span data-stu-id="2d7d4-126">The financial dimension defaults are applicable and can be used only with Fixed price (milestone) contract lines.</span></span>

<span data-ttu-id="2d7d4-127">Näitä oletusarvoja käytetään liittyvien projektien tilitapahtumissa ja laskuriveillä.</span><span class="sxs-lookup"><span data-stu-id="2d7d4-127">These defaults are used on related project on-account transactions and invoice lines.</span></span>

## <a name="define-default-financial-dimensions-for-projects"></a><span data-ttu-id="2d7d4-128">Projektien taloushallinnon oletusdimensioiden määrittäminen</span><span class="sxs-lookup"><span data-stu-id="2d7d4-128">Define default financial dimensions for projects</span></span>

<span data-ttu-id="2d7d4-129">Projektit luodaan ja niitä ylläpidetään ssa (CDS).</span><span class="sxs-lookup"><span data-stu-id="2d7d4-129">Projects are created and maintained in CDS.</span></span> <span data-ttu-id="2d7d4-130">Projektien kirjanpitomääritteet määritetään Financen **Projektinhallinta ja kirjanpito** -moduulissa.</span><span class="sxs-lookup"><span data-stu-id="2d7d4-130">Accounting attributes for projects are set in the **Project management and accounting** module in Finance.</span></span>

1. <span data-ttu-id="2d7d4-131">Valitse **Projektinhallinta ja kirjanpito** > **Projektit** > **Kaikki projektit**.</span><span class="sxs-lookup"><span data-stu-id="2d7d4-131">Go to **Project management and accounting** > **Projects** > **All projects**.</span></span>
2. <span data-ttu-id="2d7d4-132">Valitse päivitettävä tietue ja valitse sitten **Projekti**-välilehdessä **Näytä oletuskirjanpito**.</span><span class="sxs-lookup"><span data-stu-id="2d7d4-132">Select the record that you want to update and on the **Project** tab, select **Show default accounting**.</span></span>
3. <span data-ttu-id="2d7d4-133">Laajenna **Liittyvät tiedot** ja valitse **Määritys**-välilehti.</span><span class="sxs-lookup"><span data-stu-id="2d7d4-133">Expand **Related information** and select the **Setup** tab.</span></span>
4. <span data-ttu-id="2d7d4-134">Määritä taloushallinnon dimension oletusarvot.</span><span class="sxs-lookup"><span data-stu-id="2d7d4-134">Set the financial dimension defaults.</span></span> <span data-ttu-id="2d7d4-135">Huomaa, että taloushallinnon dimensioiden oletusarvo saadaan asiakastililtä.</span><span class="sxs-lookup"><span data-stu-id="2d7d4-135">Notice that financial dimensions default from the customer account.</span></span> <span data-ttu-id="2d7d4-136">Jos projekti on liitetty sopimusriviin, jossa on useita projektisopimuksen asiakkaita, ensisijaista asiakasta käytetään taloushallinnon dimensioiden oletusarvona.</span><span class="sxs-lookup"><span data-stu-id="2d7d4-136">If the project is associated with a contract line with multiple project contract customers, the primary customer is used to default financial dimensions.</span></span>

<span data-ttu-id="2d7d4-137">Projektin taloushallinnon oletusdimensioita käytetään määrittämään aika-, kulu- ja maksutapahtumien kirjauskansioiden rivin oletusarvot **Project Operationsin integroinnin kirjauskansiossa** ja liittyvillä projektilaskuriveillä.</span><span class="sxs-lookup"><span data-stu-id="2d7d4-137">Project default financial dimensions are used to set journal line defaults for time, expense, and fee transactions in the **Project Operations Integration Journal** and on related project invoice lines.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]