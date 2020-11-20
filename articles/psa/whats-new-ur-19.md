---
title: Uutuudet ja muutokset Project Service Automation -päivitysjulkaisussa 19, V3
description: Tässä aiheessa on luettelo ominaisuuksista ja korjauksista, jotka ovat käytettävissä Project Service Automation -päivitysjulkaisussa 19, V3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 05/05/2020
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
ms.openlocfilehash: e116bcbb8e9d184b7b894709c893aaf1dadefc2f
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/28/2020
ms.locfileid: "4126834"
---
# <a name="project-service-automation-update-release-19-v3"></a><span data-ttu-id="e4698-103">Project Service Automation -päivitysjulkaisu 19, V3</span><span class="sxs-lookup"><span data-stu-id="e4698-103">Project Service Automation Update Release 19, V3</span></span>

<span data-ttu-id="e4698-104">Meillä on ilo julkistaa Dynamics 365:n Project Service Automation-sovelluksen uusin päivitys.</span><span class="sxs-lookup"><span data-stu-id="e4698-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="e4698-105">Tämä julkaisu sisältää joitakin tärkeitä parannuksia laatuun, tehokkuuteen ja käytettävyyteen.</span><span class="sxs-lookup"><span data-stu-id="e4698-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="e4698-106">Tämä versio on yhteensopiva Dynamics 365 -versioiden 9.x kanssa.</span><span class="sxs-lookup"><span data-stu-id="e4698-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="e4698-107">Jos haluat päivittää tämän julkaisun, avaa Dynamics 365 online -hallintakeskuksen Ratkaisut-sivu ja asenna päivitys.</span><span class="sxs-lookup"><span data-stu-id="e4698-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="e4698-108">Lisätietoja: [Ensisijaisen ratkaisun asentaminen, päivittäminen tai poistaminen](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="e4698-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="e4698-109">Tässä aiheessa on luettelo ominaisuuksista ja korjauksista, jotka ovat uusia tai muuttuneita PSA V3 -päivitysjulkaisussa 19.</span><span class="sxs-lookup"><span data-stu-id="e4698-109">This topic lists the features and fixes that are new or changed for PSA V3, Update Release 19.</span></span> <span data-ttu-id="e4698-110">Tämän version koontiversion numero on V3.10.30.41, ja se on yleisesti saatavana itsepäivittyvänä toukokuussa 2020.</span><span class="sxs-lookup"><span data-stu-id="e4698-110">This version has a build number of V3.10.30.41 and is generally available through a self-update in May 2020.</span></span>

## <a name="update-release-19"></a><span data-ttu-id="e4698-111">Päivitysjulkaisu 19</span><span class="sxs-lookup"><span data-stu-id="e4698-111">Update Release 19</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="e4698-112">Ohjelmavirhekorjauksia</span><span class="sxs-lookup"><span data-stu-id="e4698-112">Bug fixes</span></span>

<span data-ttu-id="e4698-113">**Aika ja kulu**</span><span class="sxs-lookup"><span data-stu-id="e4698-113">**Time and Expense**</span></span>

<span data-ttu-id="e4698-114">Seuraavat ongelmat on korjattu:</span><span class="sxs-lookup"><span data-stu-id="e4698-114">The following issues have been fixed:</span></span> 

- <span data-ttu-id="e4698-115">Aikamerkintöjen tuonneisrta johdetut virheet eivät näy oikein.</span><span class="sxs-lookup"><span data-stu-id="e4698-115">Errors derived from time entry imports are not surfaced correctly.</span></span>
- <span data-ttu-id="e4698-116">Ajansyöttöruudukko ei tue **Vain päivämäärä** -kentän toimintaa.</span><span class="sxs-lookup"><span data-stu-id="e4698-116">Time Entry Grid does not support **Date Only** field behavior.</span></span>
- <span data-ttu-id="e4698-117">Projektiresurssit eivät voi luoda kuluja projektiin.</span><span class="sxs-lookup"><span data-stu-id="e4698-117">Project Resources are unable to create an expense with a project.</span></span>

<span data-ttu-id="e4698-118">**Projektinhallinta**</span><span class="sxs-lookup"><span data-stu-id="e4698-118">**Project Management**</span></span>

<span data-ttu-id="e4698-119">Seuraavat ongelmat on korjattu:</span><span class="sxs-lookup"><span data-stu-id="e4698-119">The following issues have been fixed:</span></span> 

-  <span data-ttu-id="e4698-120">Alitason alitason tehtävä aiheuttaa virheellisen työmääräarvion valmistumisen laskennan (EAC) aikana.</span><span class="sxs-lookup"><span data-stu-id="e4698-120">Grandchild task causes an incorrect effort estimate during the Completion (EAC) Calculation.</span></span>

<span data-ttu-id="e4698-121">**Sales**</span><span class="sxs-lookup"><span data-stu-id="e4698-121">**Sales**</span></span>

<span data-ttu-id="e4698-122">Seuraavat ongelmat on korjattu:</span><span class="sxs-lookup"><span data-stu-id="e4698-122">The following issues have been fixed:</span></span> 

- <span data-ttu-id="e4698-123">**Laske uudelleen** -toiminto ei toimi kulusopimusrivin tai tarjousrivin tietojen kanssa.</span><span class="sxs-lookup"><span data-stu-id="e4698-123">The **Recalculate** action does not work with expense contract line details or quote line details.</span></span>
- <span data-ttu-id="e4698-124">Kuluarvioista puuttuu **Päivitä hinnat**.</span><span class="sxs-lookup"><span data-stu-id="e4698-124">**Update Prices** is missing for expense estimates.</span></span>
-  <span data-ttu-id="e4698-125">Asiakkaat eivät voi valita mukautettuja palvelusopimuksen tilan syitä **Projektisopimus**-sivulla.</span><span class="sxs-lookup"><span data-stu-id="e4698-125">Customers are unable to select custom contract status reasons from the **Project Contract** page.</span></span>
- <span data-ttu-id="e4698-126">Asiakkaat kokevat heikentyneen suorituskyvyn luotaessa mukautettua hinnastoa tarjouksesta.</span><span class="sxs-lookup"><span data-stu-id="e4698-126">Customers experience degraded performance when creating a custom price list from a quote.</span></span>
- <span data-ttu-id="e4698-127">Asiakkaat kokevat epäjohdonmukaisuutta **Tarjousrivin tiedot**- ja **Sopimusrivin tiedot** -sivujen **yksiköiden** oletusarvojen kanssa.</span><span class="sxs-lookup"><span data-stu-id="e4698-127">Customers experience inconsistency with **unit** defaults on **Quote Line Details** and **Contract Line Details** pages.</span></span>
- <span data-ttu-id="e4698-128">Jos lisäät ei-laskutettavan tapahtumaluokan nimikkeitä laskutettavaan sopimusriviin, toiminta ei noudata tapahtumaluokan **Ei-laskutettava**-laskutustyyppiä.</span><span class="sxs-lookup"><span data-stu-id="e4698-128">Adding non-chargeable transaction category items to a chargeable contract line will not respect the **Non-chargeable** billing type of the transaction category.</span></span>
- <span data-ttu-id="e4698-129">Asiakkaat eivät voi käyttää aiemmin luotujen palvelusopimusten juuri lisättyjä rooleja ja luokkia.</span><span class="sxs-lookup"><span data-stu-id="e4698-129">Customers can't use the newly added roles and category on previously created contracts.</span></span>
- <span data-ttu-id="e4698-130">Asiakkaat kokevat heikentyneen suorituskyvyn tarpeettomasssa kohteen PreValidateProjectTeamMemberUpdate.cs noudossa</span><span class="sxs-lookup"><span data-stu-id="e4698-130">Customers experience degraded performance Unnecessary retrieve in PreValidateProjectTeamMemberUpdate.cs</span></span>
- <span data-ttu-id="e4698-131">Jos roolit on määritetty ei-laskutettaviksi **Resurssiluokat**-luettelossa, ne on lisättävä **Laskutettavat roolit** -välilehteen projektisopimusriville arvolla **Ei-laskutettava**.</span><span class="sxs-lookup"><span data-stu-id="e4698-131">Roles set up as non-chargeable in the **Resource Categories** list should be added to the **Chargeable Roles** tab as **Non0chargeable** on the contract line for a project.</span></span>
- <span data-ttu-id="e4698-132">Asiakkaat saattavat kokea heikentyneen suorituskyvyn luodessaan projektia, koska **GetBookableResourceIdFromUser** hakee varattavissa olevien resurssien kaikki sarakkeet pelkän ensisijaisen tunnuksen sijaan.</span><span class="sxs-lookup"><span data-stu-id="e4698-132">Customers may experience degraded performance when creating a project because **GetBookableResourceIdFromUser** retrieves all columns of bookable resources instead of just the primary ID.</span></span>
- <span data-ttu-id="e4698-133">**TransactionType**-entiteetistä puuttuu esivahtistuken päivityslaajennus, joka estää käyttäjiä syöttämästä **yksiköitä** ja **yksikköryhmiä**, jotka eivät ole kelvollisia tapahtumatyypeille.</span><span class="sxs-lookup"><span data-stu-id="e4698-133">**TransactionType** entity missing the pre-validation update plug-in to prevent users from entering **Units** and **UnitGroups** that are not valid for transaction types.</span></span>
- <span data-ttu-id="e4698-134">**Poista**-vaihe ei toimi aikamerkintöjen tuonnissa.</span><span class="sxs-lookup"><span data-stu-id="e4698-134">The **Remove** step does not work for time entry import.</span></span>