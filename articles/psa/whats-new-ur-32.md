---
title: Uutuudet ja muutokset Project Service Automation -päivitysjulkaisussa 32, V3
description: Tässä aiheessa on luettelo ominaisuuksista ja korjauksista, jotka ovat käytettävissä Project Service Automation -päivitysjulkaisussa 32, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 06/01/2021
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 11bf451ef4f24e2301ffde4f86a556a8a4fe30b0
ms.sourcegitcommit: 886102894244887d72e5a6213071e8d8a52c9d48
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/01/2021
ms.locfileid: "6129662"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-32-v3"></a><span data-ttu-id="76cf8-103">Uutuudet ja muutokset Project Service Automation -päivitysjulkaisussa 32, V3</span><span class="sxs-lookup"><span data-stu-id="76cf8-103">What's new or changed in Project Service Automation Update Release 32, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="76cf8-104">Meillä on ilo esitellä Microsoft Dynamics 365 Project Service Automation -sovelluksen uusin päivitys.</span><span class="sxs-lookup"><span data-stu-id="76cf8-104">We're pleased to announce the latest update for the Microsoft Dynamics 365 Project Service Automation app.</span></span> <span data-ttu-id="76cf8-105">Tämä julkaisu sisältää joitakin tärkeitä parannuksia laatuun, tehokkuuteen ja käytettävyyteen.</span><span class="sxs-lookup"><span data-stu-id="76cf8-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="76cf8-106">Se on yhteensopiva Dynamics 365 9.x -version kanssa.</span><span class="sxs-lookup"><span data-stu-id="76cf8-106">It's compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="76cf8-107">Päivitä tähän versioon asentamalla päivitys Dynamics 365 -hallintakeskuksen online-ratkaisujen sivulta.</span><span class="sxs-lookup"><span data-stu-id="76cf8-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page, and install the update.</span></span> <span data-ttu-id="76cf8-108">Lisätietoja: [Ensisijaisen ratkaisun asentaminen, päivittäminen tai poistaminen](/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="76cf8-108">For more information, see [Install, update, or remove a preferred solution](/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="76cf8-109">Tässä aiheessa on luettelo ominaisuuksista ja korjauksista, jotka ovat uusia tai muuttuneita Project Service Automation V3 -päivitysjulkaisussa 32.</span><span class="sxs-lookup"><span data-stu-id="76cf8-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 32.</span></span> <span data-ttu-id="76cf8-110">Tämän version koontiversion numero on V3.10.53.108, ja se on yleisesti saatavana itsepäivittyvänä kesäkuussa 2021.</span><span class="sxs-lookup"><span data-stu-id="76cf8-110">This version has a build number of V3.10.53.108 and is generally available through a self-update in June 2021.</span></span>

## <a name="update-release-32"></a><span data-ttu-id="76cf8-111">Päivitysjulkaisu 32</span><span class="sxs-lookup"><span data-stu-id="76cf8-111">Update Release 32</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="76cf8-112">Ohjelmavirhekorjauksia</span><span class="sxs-lookup"><span data-stu-id="76cf8-112">Bug fixes</span></span>

#### <a name="general"></a><span data-ttu-id="76cf8-113">Yhteiset</span><span class="sxs-lookup"><span data-stu-id="76cf8-113">General</span></span>

- <span data-ttu-id="76cf8-114">Kun pääversiopäivitys epäonnistuu, vain pääsovelluksen aloituskohdat tulisi estää, jotta jaetut entiteetit ovat yhä käytettävissä.</span><span class="sxs-lookup"><span data-stu-id="76cf8-114">When a major upgrade fails, only the main application entry points should be blocked, to ensure that shared entities are still accessible.</span></span>

#### <a name="time-and-expense"></a><span data-ttu-id="76cf8-115">Aika ja kulu</span><span class="sxs-lookup"><span data-stu-id="76cf8-115">Time and Expense</span></span>

<span data-ttu-id="76cf8-116">Seuraavat ongelmat on korjattu:</span><span class="sxs-lookup"><span data-stu-id="76cf8-116">The following issues have been fixed:</span></span>

- <span data-ttu-id="76cf8-117">**TimeEntriesImportFromResourceAssignment** ei säilytä resurssin delegoinnin jaksotussektorin aloitus- ja päättymisaikoja.</span><span class="sxs-lookup"><span data-stu-id="76cf8-117">**TimeEntriesImportFromResourceAssignment** doesn't maintain the start and end times of the resource assignment contour slice.</span></span>
- <span data-ttu-id="76cf8-118">Kun valitset **Aikamerkintä**-ruudukosta **Avaa merkintä**, sinua saatetaan estää valitsemasta muita lomakkeita.</span><span class="sxs-lookup"><span data-stu-id="76cf8-118">When you select **Open Entry** on the **Time Entry** grid, you might be prevented from selecting other forms.</span></span>
- <span data-ttu-id="76cf8-119">Kun tuot tehtäviä aikamerkintöihin, asiakaskoodin kysely saattaa luoda pitkän URL-osoitteen, jonka vuoksi kysely epäonnistuu.</span><span class="sxs-lookup"><span data-stu-id="76cf8-119">While you import assignments to time entries, the client code query could generate a long URL that fails the query.</span></span>
- <span data-ttu-id="76cf8-120">Kun **Aikamerkintä**-ruudukon solusta poistetaan arvo, kohdistus ei jää ruudukkoon.</span><span class="sxs-lookup"><span data-stu-id="76cf8-120">In the **Time Entry** grid, after a value is deleted from a cell, the focus doesn't remain in the grid.</span></span>
- <span data-ttu-id="76cf8-121">**Hylkää**-painike on poistettu **Käsittelyssä olevat hyväksynnät** -näkymästä moderneilta hyväksynnöiltä.</span><span class="sxs-lookup"><span data-stu-id="76cf8-121">The **Reject** button has been removed from the **Processing approvals** view for modern approvals.</span></span>
- <span data-ttu-id="76cf8-122">Lukkiutumat ja **Aikamerkintä**-entiteettiin liittyvien mukautusten asianmukaiseen käsittelyyn liittyvät virheet vaikuttavat aikamerkintöjen joukkohyväksynnän vakauteen ja suorituskykyyn.</span><span class="sxs-lookup"><span data-stu-id="76cf8-122">The stability and performance of time entry bulk approval are affected by deadlocks and a failure to appropriately handle customizations that are related to the **Time Entry** entity.</span></span>

#### <a name="project-planning"></a><span data-ttu-id="76cf8-123">Projektin suunnittelu</span><span class="sxs-lookup"><span data-stu-id="76cf8-123">Project Planning</span></span>

- <span data-ttu-id="76cf8-124">Kun päivität projektin, jonka **Sopimusyksikkö**-kentässä on null-arvo, tapahtuu null-viittauksen poikkeus.</span><span class="sxs-lookup"><span data-stu-id="76cf8-124">A null reference exception is generated when you update a project that has a null value in the **Contracting Unit** field.</span></span>
- <span data-ttu-id="76cf8-125">**Päivitä projektin summat** laskee projektin jäljellä olevat kustannukset ja jäljellä olevan myynnin virheellisesti.</span><span class="sxs-lookup"><span data-stu-id="76cf8-125">**Refresh Project Totals** incorrectly calculates the remaining cost and remaining sales on a project.</span></span>
- <span data-ttu-id="76cf8-126">Tarpeettomat hinnastojen laskutoimet vaikuttavat resurssin delegoinnin jaksotuksen päivitysten suorituskykyyn.</span><span class="sxs-lookup"><span data-stu-id="76cf8-126">Redundant pricing calculations affect performance that is related to updates on resource assignment contours.</span></span>

#### <a name="resource-management"></a><span data-ttu-id="76cf8-127">Resurssienhallinta</span><span class="sxs-lookup"><span data-stu-id="76cf8-127">Resource Management</span></span>

<span data-ttu-id="76cf8-128">Seuraava ongelma on korjattu:</span><span class="sxs-lookup"><span data-stu-id="76cf8-128">The following issue has been fixed:</span></span>

- <span data-ttu-id="76cf8-129">Kun varattavissa olevan resurssin kalenterikapasiteetti on yli 1, Project Service Automation tunnistaa kapasiteetin virheellisesti nollaksi (0).</span><span class="sxs-lookup"><span data-stu-id="76cf8-129">When a bookable resource's calendar capacity is more than 1, Project Service Automation incorrectly recognizes the capacity as 0 (zero).</span></span> <span data-ttu-id="76cf8-130">Tästä syystä aikataulunäkymässä ilmenee loputon silmukka.</span><span class="sxs-lookup"><span data-stu-id="76cf8-130">Therefore, an infinite loop occurs in the schedule view.</span></span>

#### <a name="sales"></a><span data-ttu-id="76cf8-131">Myynti</span><span class="sxs-lookup"><span data-stu-id="76cf8-131">Sales</span></span>

<span data-ttu-id="76cf8-132">Seuraavat ongelmat on korjattu:</span><span class="sxs-lookup"><span data-stu-id="76cf8-132">The following issues have been fixed:</span></span>

- <span data-ttu-id="76cf8-133">Mukautettua tapahtumatyyppiä käyttävän kirjauskansion rivin luominen aiheuttaa seuraavan null-viitteen poikkeuksen: *Microsoft.Dynamics.ProjectService.Plugins.JournalLinePlugins.ValidateUnitScheduleAndUnitWithTransactionType(TransactionTypetransactionType, TransactionTypeCode transTypeCodeFromPlugin)*.</span><span class="sxs-lookup"><span data-stu-id="76cf8-133">When a journal line is created that has a custom transaction type, the following null reference exception occurs: *Microsoft.Dynamics.ProjectService.Plugins.JournalLinePlugins.ValidateUnitScheduleAndUnitWithTransactionType(TransactionTypetransactionType, TransactionTypeCode transTypeCodeFromPlugin)*.</span></span>
- <span data-ttu-id="76cf8-134">Roolia ja luokkia, joiden aktivointi on kumottu ennen tarjouksen kopioimista, ei tulisi lisätä uuden kopioidun tarjouksen laskutettaviin rooleihin ja luokkiin.</span><span class="sxs-lookup"><span data-stu-id="76cf8-134">Roles and categories that are inactivated before a quotation is copied should not be added to chargeable roles and categories of the newly copied quotation.</span></span>
- <span data-ttu-id="76cf8-135">Asiakirjan päivämäärä ja kirjanpitopäivämäärä eivät vastaa aloituspäivää, jotka on annettu suoraan luonnoslaskuun luodun laskurivin tiedoissa.</span><span class="sxs-lookup"><span data-stu-id="76cf8-135">The document date and accounting date aren't aligned with the start date that is provided on an invoice line detail that is created directly on a draft invoice.</span></span>
- <span data-ttu-id="76cf8-136">Null-viitteiden poikkeuksia aiheutuu tilanteissa, jotka liittyvät roolien ja luokkien aktivoinnin kumoamiseen ennen tarjouksen kopioimista.</span><span class="sxs-lookup"><span data-stu-id="76cf8-136">Null reference exceptions are generated in scenarios that are related to inactivation of roles and categories before a quotation is copied.</span></span>
- <span data-ttu-id="76cf8-137">**Projektit**-sivun **Päivitä hinnat** -toiminto ei päivitä kuluarvioita tai materiaaliarvioita.</span><span class="sxs-lookup"><span data-stu-id="76cf8-137">The **Update Prices** action on the **Projects** page doesn't update expense estimates and material estimates.</span></span>
