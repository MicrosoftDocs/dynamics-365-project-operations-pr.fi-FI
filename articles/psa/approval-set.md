---
title: Hyväksyntäjoukot
description: Tässä aiheessa on tietoja hyväksyntäjoukoista, pyynnöistä ja näiden toimintojen alijoukoista.
author: stsporen
manager: tfehr
ms.date: 05/28/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: ac73313420029ece740d0bdb9c21c7abaa9defc6
ms.sourcegitcommit: fc96c6eb9a2094f9fa3d1ae39646730ef9d558ba
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/28/2021
ms.locfileid: "6116867"
---
# <a name="approval-sets"></a><span data-ttu-id="44599-103">Hyväksyntäjoukot</span><span class="sxs-lookup"><span data-stu-id="44599-103">Approval sets</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="44599-104">Hyväksyntäjoukot ryhmittelevät hyväksyntäpyynnöt pienempiin toimintojen alijoukkoihin.</span><span class="sxs-lookup"><span data-stu-id="44599-104">Approval sets group approval requests together into smaller subsets of operations.</span></span> <span data-ttu-id="44599-105">Tämä ryhmittely sallii projektin käsitellä hyväksynnät järjestyksessä, ja se mahdollistaa uudelleen yrittämisen ja sekvensoinnin.</span><span class="sxs-lookup"><span data-stu-id="44599-105">This grouping allows approvals to be processed in order by Project and allows for retrying and sequencing.</span></span> <span data-ttu-id="44599-106">Ryhmittely parantaa luotettavuutta ja jäljittämistä, kun hyväksyntöjä käsitellään suuria määriä.</span><span class="sxs-lookup"><span data-stu-id="44599-106">Grouping improves the reliability and traceability of approval processing for large volumes of approvals.</span></span>

<span data-ttu-id="44599-107">Hyväksyntäjoukot osoittavat niihin liittyvien tietueiden käsittelyn kokonaistilan.</span><span class="sxs-lookup"><span data-stu-id="44599-107">Approval sets indicate the overall processing state of their related records.</span></span> <span data-ttu-id="44599-108">Kun hyväksyntätietue käsitellään käyttämällä hyväksyntäjoukkoa, se siirtyy **Lähetetty**-tilasta **Hyväksytty**-tilaan ja irrotetaan hyväksyntäjoukosta.</span><span class="sxs-lookup"><span data-stu-id="44599-108">When an approval record is processed using an approval set, the record moves from **Submitted** to **Approved**, and is unlinked from the approval set.</span></span> <span data-ttu-id="44599-109">Jos tietue epäonnistuu, kun se lähetetään hyväksyttäväksi, se säilyy **Lähetetty**-tilassa ja hyväksyntäjoukko merkitään epäonnistuneeksi.</span><span class="sxs-lookup"><span data-stu-id="44599-109">If a record fails when it is submitted for approval, the record remains in a status of **Submitted** and the approval set is marked as failed.</span></span> <span data-ttu-id="44599-110">Hyväksyntäjoukko kirjaa virhesanoman lokiin.</span><span class="sxs-lookup"><span data-stu-id="44599-110">The approval set logs the error message of the failure.</span></span>

## <a name="processing-approvals-and-approval-sets"></a><span data-ttu-id="44599-111">Hyväksyntöjen ja hyväksyntäjoukkojen käsittely</span><span class="sxs-lookup"><span data-stu-id="44599-111">Processing approvals and approval sets</span></span>
<span data-ttu-id="44599-112">Hyväksynnät, jotka on lisätty jonoon käsittelyä varten, näytetään **Käsittelyssä olevat hyväksynnät** -näkymässä.</span><span class="sxs-lookup"><span data-stu-id="44599-112">Approvals that are queued for processing are visible in the **Processing Approvals** view.</span></span> <span data-ttu-id="44599-113">Järjestelmä yrittää käsitellä kaikki merkinnät useita kertoja asynkronisesti ja yrittää hyväksyntää uudelleen, jos aiemmat yritykset epäonnistuvat.</span><span class="sxs-lookup"><span data-stu-id="44599-113">The system tries to process all the entries multiple times asynchronously, including retrying an approval if previous attempts failed.</span></span>

<span data-ttu-id="44599-114">**Hyväksyntäjoukon elinkaari** -kenttä sisältää jäljellä olevien käsittely-yritysten määrän ennen kuin joukko merkitään epäonnistuneeksi.</span><span class="sxs-lookup"><span data-stu-id="44599-114">The **Approval Set Lifetime** field records the number of attempts left to process the set before it's marked as failed.</span></span>

## <a name="failed-approvals-and-approval-sets"></a><span data-ttu-id="44599-115">Epäonnistuneet hyväksynnät ja hyväksyntäjoukot</span><span class="sxs-lookup"><span data-stu-id="44599-115">Failed approvals and approval sets</span></span>
<span data-ttu-id="44599-116">**Epäonnistuneet hyväksynnät** -näkymässä näytetään kaikki hyväksynnät, jotka edellyttävät käyttäjän toimia.</span><span class="sxs-lookup"><span data-stu-id="44599-116">The **Failed Approvals** view lists all approvals that require user intervention.</span></span> <span data-ttu-id="44599-117">Avaa asiaan liittyvät hyväksyntäjoukon lokit selvittääksesi virheen syyn.</span><span class="sxs-lookup"><span data-stu-id="44599-117">Open the associated approval set logs to identify the cause of the failure.</span></span>
<span data-ttu-id="44599-118">Jos valitset **Yritä uudelleen**, hyväksyntäjoukon elinkaaren arvo kasvaa, hyväksyntäjoukko siirtyy takaisin **Käsittely**-tilaan ja jäljellä olevat tietueet yritetään käsitellä uudelleen.</span><span class="sxs-lookup"><span data-stu-id="44599-118">Selecting **Retry** adds to the approval set lifetime count, moves the approval set back to a status of **Processing**, and attempts to process the remaining records.</span></span>

## <a name="configure-approval-sets"></a><span data-ttu-id="44599-119">Hyväksyntäjoukkojen määrittäminen</span><span class="sxs-lookup"><span data-stu-id="44599-119">Configure approval sets</span></span>

###  <a name="enable-the-approval-sets-feature"></a><span data-ttu-id="44599-120">Hyväksyntäjoukot-ominaisuuden ottaminen käyttöön</span><span class="sxs-lookup"><span data-stu-id="44599-120">Enable the Approval sets feature</span></span>
<span data-ttu-id="44599-121">Varmista ennen Hyväksyntäjoukot-ominaisuuden ottamista käyttöön, ettei hyväksyntöjä käsitellä tällä hetkellä.</span><span class="sxs-lookup"><span data-stu-id="44599-121">Before you enable the Approval sets feature, verify that there are no approvals currently being processed.</span></span>

- <span data-ttu-id="44599-122">Siirry **Projektin parametrit** -sivulle ja valitse **Ominaisuuden ohjausobjekti** > **Ota modernit hyväksynnät käyttöön**.</span><span class="sxs-lookup"><span data-stu-id="44599-122">Go to the **Project parameters** page and select **Feature Control** > **Enable Modern Approvals**.</span></span>

### <a name="turn-off-the-approval-sets-feature"></a><span data-ttu-id="44599-123">Hyväksyntäjoukot-ominaisuuden poistaminen käytöstä</span><span class="sxs-lookup"><span data-stu-id="44599-123">Turn off the Approval sets feature</span></span>
<span data-ttu-id="44599-124">Varmista ennen Hyväksyntäjoukot-ominaisuuden käytöstä poistamista, ettei hyväksyntöjä käsitellä tällä hetkellä.</span><span class="sxs-lookup"><span data-stu-id="44599-124">Before you turn off the Approval sets feature, verify that there are no approvals currently being processed.</span></span>

- <span data-ttu-id="44599-125">Siirry **Projektin parametrit** -sivulle ja valitse **Ominaisuuden ohjausobjekti** > **Poista modernit hyväksynnät käytöstä**.</span><span class="sxs-lookup"><span data-stu-id="44599-125">Go to the **Project Parameters** page and select **Feature Control** > **Disable Modern Approvals**.</span></span>

### <a name="configuring-the-asynchronous-threshold"></a><span data-ttu-id="44599-126">Asynkronisen kynnysarvon määrittäminen</span><span class="sxs-lookup"><span data-stu-id="44599-126">Configuring the asynchronous threshold</span></span> 
<span data-ttu-id="44599-127">Kun hyväksyntäjoukkoja luodaan, käsittely siirtyy taustalle, kun hyväksyttäväksi valittujen tietueiden määrä ylittää määritetyn kynnysarvon.</span><span class="sxs-lookup"><span data-stu-id="44599-127">When approval sets are created, processing moves to the background when the selected number of records for approval exceeds the indicated threshold.</span></span> <span data-ttu-id="44599-128">Käytä **Asynkroninen kynnysarvo** -kenttää määrittääksesi, milloin hyväksyntöjen käsittely tulisi suorittaa synkronisesti tai asynkronisesti.</span><span class="sxs-lookup"><span data-stu-id="44599-128">Use the **Asynchronous Threshold** field to configure when approval processing should be run synchronously or asynchronously.</span></span>
<span data-ttu-id="44599-129">Kelvolliset arvot ovat:</span><span class="sxs-lookup"><span data-stu-id="44599-129">Valid values are:</span></span>

  - <span data-ttu-id="44599-130">Nolla: Kaikki pyynnöt tulisi käsitellä asynkronisesti.</span><span class="sxs-lookup"><span data-stu-id="44599-130">Zero: All requests should be processed asynchronously.</span></span> 
  - <span data-ttu-id="44599-131">Nollaa suuremmat arvot: Hyväksynnät käsitellään asynkronisesti vain, kun lähetettyjen hyväksyntöjen määrä ylittää tämän arvon.</span><span class="sxs-lookup"><span data-stu-id="44599-131">Numbers greater than zero: Approvals are processed asynchronously only when the submitted number of approvals exceeds this value.</span></span>

[!INCLUDE[footer-include](../includes/footer-banner.md)]
