---
title: Projektiarvion poistaminen
description: Tässä aiheessa on tietoja siitä, miten projektiarvion voi poistaa, kun se on valmis.
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
ms.openlocfilehash: 8bda8a7357e883b948449b2a19bea476996dde3c
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/16/2020
ms.locfileid: "4075401"
---
# <a name="eliminate-a-project-estimate"></a><span data-ttu-id="2490c-103">Projektiarvion poistaminen</span><span class="sxs-lookup"><span data-stu-id="2490c-103">Eliminate a project estimate</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2490c-104">Projektin arviot tarjoavat taloudellisen näkymän työhön, joka on arvioitu ja aikataulutettu projektille.</span><span class="sxs-lookup"><span data-stu-id="2490c-104">Project estimates provide the financial view for work that is estimated and scheduled for a project.</span></span> <span data-ttu-id="2490c-105">Projektiin liittyvien arvioiden käsitteleminen edellyttää, että projekti liitetään arviointiprojektiin.</span><span class="sxs-lookup"><span data-stu-id="2490c-105">To work with estimates for a project, you must attach the project to an estimate project.</span></span> <span data-ttu-id="2490c-106">Arviointiprojekti perustuu aina aiemmin luotuun projektiin, mutta useat projektit voivat viitata yksittäiseen arviointiprojektiin.</span><span class="sxs-lookup"><span data-stu-id="2490c-106">An estimate project is always based on an existing project, however multiple projects can refer to a single estimate project.</span></span> <span data-ttu-id="2490c-107">Vain kiinteähintaiset ja investointiprojektit voidaan liittää arviointiprojekteihin, ja näiden projektien on kuuluttava samaan projektiryhmään kuin arviointiprojekti.</span><span class="sxs-lookup"><span data-stu-id="2490c-107">Only fixed-price and investment projects can be attached to estimate projects, and those projects must belong to the same project group as the estimate project.</span></span>

<span data-ttu-id="2490c-108">Jotta arviointiprojekti voidaan poistaa, sen on oltava valmis.</span><span class="sxs-lookup"><span data-stu-id="2490c-108">To eliminate an estimate project, it must be complete.</span></span> <span data-ttu-id="2490c-109">Seuraavassa kerrotaan, miten arvio voidaan poistaa.</span><span class="sxs-lookup"><span data-stu-id="2490c-109">The following steps explain how to eliminate an estimate.</span></span>

1. <span data-ttu-id="2490c-110">Siirry kohtaan **Projektinhallinta ja kirjanpito** > **Kaikki projektit** ja avaa projekti.</span><span class="sxs-lookup"><span data-stu-id="2490c-110">Go to **Project management and accounting** > **All Projects** and open the project.</span></span> 
2. <span data-ttu-id="2490c-111">Valitse **hallinta** -välilehdessä **arviot** ja valitse sitten **arvio** -sivulla **Poista**.</span><span class="sxs-lookup"><span data-stu-id="2490c-111">On the **Manage** tab, select **Estimates** , and on the **Estimate** page select **Eliminate**.</span></span>
3. <span data-ttu-id="2490c-112">Määritä **yleiset** -välilehden **Poista arvio** -sivulla seuraavat asetukset:</span><span class="sxs-lookup"><span data-stu-id="2490c-112">On the **Eliminate estimate** page on the **General** tab, set the following options:</span></span>

   - <span data-ttu-id="2490c-113">**Kausikoodi** : Valitse kausikoodi, jos haluat valita sopivat arviointiprojektit.</span><span class="sxs-lookup"><span data-stu-id="2490c-113">**Period code** : Select the period code to choose the appropriate estimate projects.</span></span> 
   - <span data-ttu-id="2490c-114">**Arviopäivämäärä** : Valitse eliminoinnin arviopäivä.</span><span class="sxs-lookup"><span data-stu-id="2490c-114">**Estimate date** : Select the appropriate estimate date for elimination.</span></span>
   - <span data-ttu-id="2490c-115">**Eliminoiminen KET-varoituksilla** : Ota tämä asetus käyttöön, jos haluat ilmoittaa, kun keskeneräiseen työhön (KET) liittyvä arvio poistetaan.</span><span class="sxs-lookup"><span data-stu-id="2490c-115">**Eliminate with WIP warnings** : Enable this option to provide notification when an estimate that is associated with a work in progress (WIP) will be eliminated.</span></span> <span data-ttu-id="2490c-116">Kun tämä vaihtoehto ei ole käytössä, eliminointi ei voi jatkua, jos yhtään ei-arvioitua tapahtumaa on olemassa.</span><span class="sxs-lookup"><span data-stu-id="2490c-116">When this option is not enabled, elimination can’t continue if any non-estimated transactions exist.</span></span> 
   > [!NOTE]
   > <span data-ttu-id="2490c-117">Tämä vaihtoehto on käytettävissä vain, kun eliminointi kohdistetaan arviointiprojektiin.</span><span class="sxs-lookup"><span data-stu-id="2490c-117">This option is available only when elimination is applied to an estimate project.</span></span> <span data-ttu-id="2490c-118">Se ei ole käytettävissä, jos käytät kausittaisia kirjauksia.</span><span class="sxs-lookup"><span data-stu-id="2490c-118">It is not available if you are using periodic postings.</span></span> <span data-ttu-id="2490c-119">Tämä asetus toimii **Projektiparametrit** -sivun **arvio** -välilehden asetusten **Salli eliminointi, kun ei-arvioituja tapahtumia on** -kenttäryhmässä.</span><span class="sxs-lookup"><span data-stu-id="2490c-119">This setting works with the settings on the **Estimate** tab on the **Project parameters** page, in the **Allow elimination when non-estimated transactions exist** field group.</span></span>
   - <span data-ttu-id="2490c-120">**Aseta vaihe valmiiksi** : Ota tämä asetus käyttöön, kun haluat määrittää arviointiprojektin vaiheen **päättyneeksi** , kun olet suorittanut eliminoinnin.</span><span class="sxs-lookup"><span data-stu-id="2490c-120">**Set stage to Finished** : Enable this option to set the estimate project’s stage to **Finished** after you run the elimination.</span></span>
   - <span data-ttu-id="2490c-121">**Tulosta arvioluettelo** : Valitse tiedot, jotka sisällytetään, kun arvioluettelo tulostetaan.</span><span class="sxs-lookup"><span data-stu-id="2490c-121">**Print estimate list** : Select the information to be included when the estimate list is printed.</span></span>
   - <span data-ttu-id="2490c-122">**Näytä infoloki** : Ota tämä asetus käyttöön, kun haluat näyttää infolokin.</span><span class="sxs-lookup"><span data-stu-id="2490c-122">**Show Infolog** : Enable this option to display the Infolog.</span></span>
   - <span data-ttu-id="2490c-123">**Kirjauspvm** : Valitse arvion kirjanpidon kirjauspäivä.</span><span class="sxs-lookup"><span data-stu-id="2490c-123">**Posting date** : Choose the ledger posting date of the estimate.</span></span>

4.  <span data-ttu-id="2490c-124">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="2490c-124">Select **OK**.</span></span>
5. <span data-ttu-id="2490c-125">Kun eliminointiprosessi on valmis, eliminoitu arviointiprojekti näytetään negatiivisena.</span><span class="sxs-lookup"><span data-stu-id="2490c-125">After the elimination process is complete, the eliminated estimate project is displayed with a negative value.</span></span> 

<span data-ttu-id="2490c-126">Jos et aio poistaa arviota, voit valita eliminoidun arvion ja valita **Peruuta eliminointi**.</span><span class="sxs-lookup"><span data-stu-id="2490c-126">If you did not intend to eliminate an estimate, you can select the eliminated estimate and select **Reverse elimination**.</span></span>   
