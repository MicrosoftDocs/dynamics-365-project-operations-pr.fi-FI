---
title: Uutuudet ja muutokset Project Service Automation -päivitysjulkaisussa 31, V3
description: Tässä aiheessa on luettelo ominaisuuksista ja korjauksista, jotka ovat käytettävissä Project Service Automation -päivitysjulkaisussa 31, V3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 04/26/2021
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
ms.openlocfilehash: a595c0a129ac35d3416984e57908e73e1eaef2fd
ms.sourcegitcommit: 6e1498502461e86cff722ccaf8795ff11c7c47ad
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/27/2021
ms.locfileid: "5945531"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-31-v3"></a><span data-ttu-id="86921-103">Uutuudet ja muutokset Project Service Automation -päivitysjulkaisussa 31, V3</span><span class="sxs-lookup"><span data-stu-id="86921-103">What's new or changed in Project Service Automation Update Release 31, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="86921-104">Meillä on ilo julkistaa Dynamics 365:n Project Service Automation-sovelluksen uusin päivitys.</span><span class="sxs-lookup"><span data-stu-id="86921-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="86921-105">Tämä julkaisu sisältää joitakin tärkeitä parannuksia laatuun, tehokkuuteen ja käytettävyyteen.</span><span class="sxs-lookup"><span data-stu-id="86921-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="86921-106">Tämä versio on yhteensopiva Dynamics 365 -versioiden 9.x kanssa.</span><span class="sxs-lookup"><span data-stu-id="86921-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="86921-107">Jos haluat päivittää tämän julkaisun, avaa Dynamics 365 online -hallintakeskuksen Ratkaisut-sivu ja asenna päivitys.</span><span class="sxs-lookup"><span data-stu-id="86921-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="86921-108">Lisätietoja: [Ensisijaisen ratkaisun asentaminen, päivittäminen tai poistaminen](/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="86921-108">For more information, see [Install, update, or remove a preferred solution](/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="86921-109">Tässä aiheessa on luettelo ominaisuuksista ja korjauksista, jotka ovat uusia tai muuttuneita Project Service Automation V3 -päivitysjulkaisussa 31.</span><span class="sxs-lookup"><span data-stu-id="86921-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 31.</span></span> <span data-ttu-id="86921-110">Tämän version koontiversion numero on V3.10.52.77, ja se on yleisesti saatavana itsepäivittyvänä toukokuussa 2021.</span><span class="sxs-lookup"><span data-stu-id="86921-110">This version has a build number of V3.10.52.77 and is generally available through a self-update in May 2021.</span></span>

## <a name="update-release-31"></a><span data-ttu-id="86921-111">Päivitysjulkaisu 31</span><span class="sxs-lookup"><span data-stu-id="86921-111">Update Release 31</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="86921-112">Ohjelmavirhekorjauksia</span><span class="sxs-lookup"><span data-stu-id="86921-112">Bug fixes</span></span>

<span data-ttu-id="86921-113">**Aika ja kulu**</span><span class="sxs-lookup"><span data-stu-id="86921-113">**Time and Expense**</span></span>

<span data-ttu-id="86921-114">Seuraavat ongelmat on korjattu:</span><span class="sxs-lookup"><span data-stu-id="86921-114">The following issues have been fixed:</span></span>

- <span data-ttu-id="86921-115">**Varattavissa oleva resurssi** -sivun aikaohjausobjektien komentopainikkeet hämmentävät.</span><span class="sxs-lookup"><span data-stu-id="86921-115">Time entry control command buttons on the **Bookable Resource** page were confusing.</span></span>
- <span data-ttu-id="86921-116">Kohdassa **Project.SetTrackingFields** luotiin tyhjä viittauspoikkeus, kun aikamerkintä hyväksyttiin.</span><span class="sxs-lookup"><span data-stu-id="86921-116">A null reference exception was generated in **Project.SetTrackingFields** when approving a time entry.</span></span>

<span data-ttu-id="86921-117">**Resurssienhallinta**</span><span class="sxs-lookup"><span data-stu-id="86921-117">**Resource Management**</span></span>

<span data-ttu-id="86921-118">Seuraavat ongelmat on korjattu:</span><span class="sxs-lookup"><span data-stu-id="86921-118">The following issues have been fixed:</span></span>

- <span data-ttu-id="86921-119">**Luo ryhmän jäsen** luominen ei näytä oikein varauksen määritysten metatietoasetusta **varauksen sidotulle oletustilalle**.</span><span class="sxs-lookup"><span data-stu-id="86921-119">**Create Team Member** doesn't correctly display the booking setup metadata setting for **Default Booking Committed Status**.</span></span>
- <span data-ttu-id="86921-120">Kun päivität PSA 1.X:stä 3.X:ksi, päivitysprosessi epäonnistuu **UpgradeResourceRequirements**-kohdassa.</span><span class="sxs-lookup"><span data-stu-id="86921-120">When upgrading from PSA 1.X to 3.X, the upgrade process fails at **UpgradeResourceRequirements**.</span></span>


<span data-ttu-id="86921-121">**Myynti**</span><span class="sxs-lookup"><span data-stu-id="86921-121">**Sales**</span></span>

<span data-ttu-id="86921-122">Seuraavat ongelmat on korjattu:</span><span class="sxs-lookup"><span data-stu-id="86921-122">The following issues have been fixed:</span></span>

- <span data-ttu-id="86921-123">Todellinen myyntituotto muuntaa summat seurantaruudukon projektivaluuttaan.</span><span class="sxs-lookup"><span data-stu-id="86921-123">Actual revenue converts the amounts to the project currency in the tracking grid.</span></span>
- <span data-ttu-id="86921-124">Valuuttaoletusarvo on hyvä, kun luodaan kirjausrivejä, tarjousrivejä ja sopimusrivejä skenaarioissa, joissa organisaation perusvaluutta eroaa projektivaluutasta.</span><span class="sxs-lookup"><span data-stu-id="86921-124">The currency default is unclear when creating journal lines, quote lines, and contract lines in scenarios where an organization's base currency differs from the project currency.</span></span>
- <span data-ttu-id="86921-125">**Odottava korjauskirjaustarkistus** -kysely ei suodata projektin mukaan.</span><span class="sxs-lookup"><span data-stu-id="86921-125">**Pending correction journal validation** query doesn't filter by project.</span></span>
- <span data-ttu-id="86921-126">Loput myynnit lasketaan projektin mukaan virheellisesti.</span><span class="sxs-lookup"><span data-stu-id="86921-126">Remaining sales are calculated incorrectly on a project.</span></span>
- <span data-ttu-id="86921-127">Yhteyshenkilön perusteella luodut tarjoukset epäonnistuvat, kun niitä luodaan ilman hinnastoa.</span><span class="sxs-lookup"><span data-stu-id="86921-127">Quotes based on a contact fail when they are created without a price list.</span></span>
- <span data-ttu-id="86921-128">Kun valitset **Vahvista lasku**, näkyviin ei näy käsittelykierrosta.</span><span class="sxs-lookup"><span data-stu-id="86921-128">No processing spinner is shown when you select **Confirm Invoice**.</span></span>
- <span data-ttu-id="86921-129">Kun valitset **Luo lasku**, näkyviin ei näy käsittelykierrosta.</span><span class="sxs-lookup"><span data-stu-id="86921-129">No processing spinner is shown when you select **Create Invoice**.</span></span>
- <span data-ttu-id="86921-130">Tarjouksen sulkeminen hävittynä ei peruuta varauksia.</span><span class="sxs-lookup"><span data-stu-id="86921-130">Closing a quote as lost doesn't cancel the bookings.</span></span>







