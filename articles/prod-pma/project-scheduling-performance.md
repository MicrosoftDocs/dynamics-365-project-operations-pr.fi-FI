---
title: Projektin resurssien aikataulutuksen suorituskyky
description: Tässä aiheessa on tietoja siitä, miten voidaan parantaa resurssien aikatauluttamisen tehokkuutta useissa projekteissa.
author: Yowelle
manager: AnnBe
ms.date: 08/31/2020
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
ms.dyn365.ops.version: 10.0.14
ms.search.validFrom: 2020-09-01
ms.openlocfilehash: 34c31570778f9b64c23387112cf56fa1139cd0fd
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5289005"
---
# <a name="project-resource-scheduling-performance"></a><span data-ttu-id="2abe5-103">Projektin resurssien aikataulutuksen suorituskyky</span><span class="sxs-lookup"><span data-stu-id="2abe5-103">Project resource scheduling performance</span></span>

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]


<span data-ttu-id="2abe5-104">Resurssiaikataulutukseen liittyviä suorituskykyongelmia voi ilmetä, kun projektien määrä on tuhansia.</span><span class="sxs-lookup"><span data-stu-id="2abe5-104">Performance issues related to resource scheduling can occur when the number of projects reaches into the thousands.</span></span> <span data-ttu-id="2abe5-105">Resurssien aikataulutuksen tehokkuuden parantamiseksi käytettävissä on toiminto, jonka avulla käyttäjät voivat lyhentää resurssien saatavuuslomakkeen käynnistämiseen kuluvan ajan.</span><span class="sxs-lookup"><span data-stu-id="2abe5-105">To improve resource scheduling performance, a feature is available that allows users to reduce the time that it takes to launch the resource availability form.</span></span> <span data-ttu-id="2abe5-106">Tämä poistaa resurssikapasiteetin koontiprosessin ja nopeuttaa resurssihaun käyttöä **ResProjectResource**-taulukon avulla.</span><span class="sxs-lookup"><span data-stu-id="2abe5-106">Specifically, this removes the resource capacity roll-up synchronization process and uses the **ResProjectResource** table to speed up the resource lookup.</span></span> <span data-ttu-id="2abe5-107">Huomaa, että **ResRollup**-taulukkoa ei enää käytetä.</span><span class="sxs-lookup"><span data-stu-id="2abe5-107">Note that the **ResRollup** table will no longer be used.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="2abe5-108">Jos resurssikapasiteetin koontiprosessissa tai yhteenvetosynkronointiprosessissa on **ResProjectResource**-taulukko, älä käytä tätä ominaisuutta.</span><span class="sxs-lookup"><span data-stu-id="2abe5-108">If there is a dependency on either the resource capacity roll-up synchronization process or the **ResProjectResource** table, do not use this feature.</span></span>

## <a name="enable-resource-scheduling-performance-enhancement"></a><span data-ttu-id="2abe5-109">Resurssien aikataulutuksen tehokkuuden parantamisen käyttöönotto</span><span class="sxs-lookup"><span data-stu-id="2abe5-109">Enable resource scheduling performance enhancement</span></span>
<span data-ttu-id="2abe5-110">Jos haluat ottaa käyttöön resurssien aikataulutuksen tehokkuuden parantamisen, suorita seuraavat vaiheet.</span><span class="sxs-lookup"><span data-stu-id="2abe5-110">To enable resource scheduling performance enhancement, complete the following steps.</span></span>

1. <span data-ttu-id="2abe5-111">Siirry kohtaan **ominaisuuksien hallinta** > **Kaikki** ja etsi ominaisuusluettelosta **Ota käyttöön projektin resurssiajoitussuorituskyvyn parannus** -ominaisuus.</span><span class="sxs-lookup"><span data-stu-id="2abe5-111">Go to **Feature management** > **All**, and in the feature list, locate **Enable project resource scheduling performance enhancement feature**.</span></span>
2. <span data-ttu-id="2abe5-112">Valitse **Ota käyttöön nyt**.</span><span class="sxs-lookup"><span data-stu-id="2abe5-112">Select **Enable now**.</span></span>

> [!NOTE]
> <span data-ttu-id="2abe5-113">Jos et löydä ominaisuutta luettelosta, päivitä luettelo valitsemalla **Tarkista päivitykset**.</span><span class="sxs-lookup"><span data-stu-id="2abe5-113">If you can't find the feature in the list, select **Check for updates** to refresh the list.</span></span>

3. <span data-ttu-id="2abe5-114">Päivitä selain ja siirry sitten kohtaan **projektinhallinta ja kirjanpito** > **kausittainen** > **Projektiresurssit** > **Synkronoi resurssikalenterit kaikkien yritysten kesken**.</span><span class="sxs-lookup"><span data-stu-id="2abe5-114">Refresh your browser, and then go to **Project management and accounting** > **Periodic** > **Project resources** > **Synchronize resource calendars capacity across all companies**.</span></span>
4. <span data-ttu-id="2abe5-115">Jos haluat poistaa aiemmat tiedot, aseta **Poista nykyiset kapasiteettitietueet** -valinnan arvoksi **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="2abe5-115">Set **Remove existing capacity records** to **Yes** to remove previous data.</span></span> <span data-ttu-id="2abe5-116">Jos haluat luoda arvon lisätietoja, aseta se arvoksi **Ei**.</span><span class="sxs-lookup"><span data-stu-id="2abe5-116">If you want generate incremental data, set it to **No**.</span></span>
5. <span data-ttu-id="2abe5-117">Valitse **kausikoodi**-kentässä ajanjakso, jolta tiedot on luotava.</span><span class="sxs-lookup"><span data-stu-id="2abe5-117">In the **Period code** field, select the period in which data should be generated.</span></span> <span data-ttu-id="2abe5-118">Jos valitset kausikoodin, aloitus- ja päättymispäivämäärää ei tarvitse määrittää.</span><span class="sxs-lookup"><span data-stu-id="2abe5-118">If you select a period code, a start and end date do not need to be defined.</span></span>
6. <span data-ttu-id="2abe5-119">Jos jätät **kausikoodi**-kentän tyhjäksi, luo tiedot valitsemalla tietyt alkamis- ja päättymispäivämäärät.</span><span class="sxs-lookup"><span data-stu-id="2abe5-119">If you leave the **Period code** field blank, select specific start and end dates to generate data.</span></span>
7. <span data-ttu-id="2abe5-120">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="2abe5-120">Select **OK**.</span></span>

 > [!NOTE]
 > <span data-ttu-id="2abe5-121">Tämä jakaa yleiset tiedot **ResCalendarCapacity**-taulukkoon kaikissa ympäristössäsi olevissa yrityksissä, joten eräajo on suoritettava vain yhdessä yrityksessä.</span><span class="sxs-lookup"><span data-stu-id="2abe5-121">This will distribute general data to the **ResCalendarCapacity** table across all companies in your environment, so the batch job only needs to be run in one legal entity.</span></span> <span data-ttu-id="2abe5-122">Tämän eräajon tietoja tarvitaan resurssikapasiteetin laskemiseen liitetyn kalenterin kautta.</span><span class="sxs-lookup"><span data-stu-id="2abe5-122">The data in this batch job is needed to calculate resource capacity through the associated calendar.</span></span>

8. <span data-ttu-id="2abe5-123">Siirry kohtaan **projektinhallinta ja kirjanpito** > **kausittainen** > **Projektiresurssit** > **Täyttävät projektiresurssit kaikissa yrityksissä**, ja valitse sitten **OK**.</span><span class="sxs-lookup"><span data-stu-id="2abe5-123">Go to **Project management and accounting** > **Periodic** > **Project resources** > **Populate project resources across all companies** and then select **OK**.</span></span> <span data-ttu-id="2abe5-124">Tämä on tietojen päivityskomentosarja yleisille tiedoille, jotka ovat **ResProjectResource**-, **ResCalendarDateTimeRange**- ja **ResEffectiveDateTimeRange**-taulukot.</span><span class="sxs-lookup"><span data-stu-id="2abe5-124">This is the data upgrade script for general data in the **ResProjectResource**, **ResCalendarDateTimeRange**, and **ResEffectiveDateTimeRange** tables.</span></span> <span data-ttu-id="2abe5-125">**PSAPRojSchedRole.RootActivity**-kentän arvot päivittyvät myös.</span><span class="sxs-lookup"><span data-stu-id="2abe5-125">Values for the **PSAPRojSchedRole.RootActivity** field are also updated.</span></span> <span data-ttu-id="2abe5-126">Jos tätä ei suoriteta, näyttöön tulee varoitus, kun yrität suorittaa resurssien aikataulutustoimintoja.</span><span class="sxs-lookup"><span data-stu-id="2abe5-126">If this is not run, you will receive a warning when you try to execute resource scheduling operations.</span></span>
 
## <a name="turn-off-resource-scheduling-performance-enhancement"></a><span data-ttu-id="2abe5-127">Resurssien aikataulutuksen tehokkuuden parantamisen käytöstä poisto</span><span class="sxs-lookup"><span data-stu-id="2abe5-127">Turn off resource scheduling performance enhancement</span></span>

1. <span data-ttu-id="2abe5-128">Siirry kohtaan **ominaisuuksien hallinta** > **Kaikki** ja etsi **Ota käyttöön projektin resurssiajoitussuorituskyvyn parannus** -ominaisuus.</span><span class="sxs-lookup"><span data-stu-id="2abe5-128">Go to **Feature management** > **All**  and search for **Enable project resource scheduling performance enhancement feature**.</span></span>
2. <span data-ttu-id="2abe5-129">Valitse toiminto ja valitse sitten **Poista käytöstä** -painike.</span><span class="sxs-lookup"><span data-stu-id="2abe5-129">Select the feature, and then select the **Disable** button.</span></span>
3. <span data-ttu-id="2abe5-130">Päivitä selain.</span><span class="sxs-lookup"><span data-stu-id="2abe5-130">Refresh your browser.</span></span>
4. <span data-ttu-id="2abe5-131">Valitse **Projektinhallinta ja kirjanpito** > **Jaksoittainen** > **Kapasiteetin synkronointi** > **Synkronoi resurssikapasiteettien koonnit**.</span><span class="sxs-lookup"><span data-stu-id="2abe5-131">Go to **Project management and accounting** > **Periodic** > **Capacity synchronization** > **Synchronize resource capacity roll-ups**.</span></span>
5. <span data-ttu-id="2abe5-132">Voit poistaa aiemmat tiedot määrittämällä **kapasiteetin koonti-synkronointi** -sivulla **Poista nykyiset kapasiteetti tietueet** **Kyllä**-arvoksi.</span><span class="sxs-lookup"><span data-stu-id="2abe5-132">On the **Capacity roll-up synchronization** page, set **Remove existing capacity records** to **Yes** to remove previous data.</span></span> <span data-ttu-id="2abe5-133">Jos haluat luoda arvon lisätietoja, aseta se arvoksi **Ei**.</span><span class="sxs-lookup"><span data-stu-id="2abe5-133">If you want to generate incremental data, set it to **No**.</span></span>
6. <span data-ttu-id="2abe5-134">Valitse **kausikoodi**-kentässä ajanjakso, jolta tiedot on luotava.</span><span class="sxs-lookup"><span data-stu-id="2abe5-134">In the **Period code** field, select the period in which data should be generated.</span></span> <span data-ttu-id="2abe5-135">Jos valitset kausikoodin, aloitus- ja päättymispäivämäärää ei tarvitse määrittää.</span><span class="sxs-lookup"><span data-stu-id="2abe5-135">If you select a period code, a start and end date do not need to be defined.</span></span>
7. <span data-ttu-id="2abe5-136">Jos jätät **kausikoodi**-kentän tyhjäksi, luo tiedot valitsemalla tietyt alkamis- ja päättymispäivämäärät.</span><span class="sxs-lookup"><span data-stu-id="2abe5-136">If you leave the **Period code** field blank, select specific start and end dates to generate data.</span></span>
8. <span data-ttu-id="2abe5-137">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="2abe5-137">Select **OK**.</span></span>

> [!NOTE]
> <span data-ttu-id="2abe5-138">Tämä jakaa yleiset tiedot **ResRollup**-taulukkoon kaikissa ympäristössäsi olevissa yrityksissä, joten eräajo on suoritettava vain yhdessä yrityksessä.</span><span class="sxs-lookup"><span data-stu-id="2abe5-138">This will distribute general data to the **ResRollup** table across all companies in your environment, so the batch job only needs to be run in one legal entity.</span></span> <span data-ttu-id="2abe5-139">Tätä eräajoa tarvitaan kaikissa **resurssin käytettävyys** -näkymissä.</span><span class="sxs-lookup"><span data-stu-id="2abe5-139">This batch job is needed for all **Resource Availability** views.</span></span> <span data-ttu-id="2abe5-140">Jos tätä eräajoa ei suoriteta, **ResRollup**-tiedot luodaan lennossa, mikä voi viedä aikaa.</span><span class="sxs-lookup"><span data-stu-id="2abe5-140">If this batch job is not run, the **ResRollup** data will be generated on the fly, which can take time.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]