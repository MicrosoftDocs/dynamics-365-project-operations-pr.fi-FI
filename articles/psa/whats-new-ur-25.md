---
title: Uutuudet ja muutokset Project Service Automation -päivitysjulkaisussa 25, V3
description: Tässä aiheessa on luettelo ominaisuuksista ja korjauksista, jotka ovat käytettävissä Project Service Automation -päivitysjulkaisussa 25, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 10/26/2020
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
ms.openlocfilehash: 92dd74378457cf877e8ec26eb85a7883dda97d51
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/10/2021
ms.locfileid: "6000207"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-25-v3"></a><span data-ttu-id="7172b-103">Uutuudet ja muutokset Project Service Automation -päivitysjulkaisussa 25, V3</span><span class="sxs-lookup"><span data-stu-id="7172b-103">What's new or changed in Project Service Automation Update Release 25, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="7172b-104">Meillä on ilo julkistaa Dynamics 365:n Project Service Automation-sovelluksen uusin päivitys.</span><span class="sxs-lookup"><span data-stu-id="7172b-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="7172b-105">Tämä julkaisu sisältää joitakin tärkeitä parannuksia laatuun, tehokkuuteen ja käytettävyyteen.</span><span class="sxs-lookup"><span data-stu-id="7172b-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="7172b-106">Tämä versio on yhteensopiva Dynamics 365 -versioiden 9.x kanssa.</span><span class="sxs-lookup"><span data-stu-id="7172b-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="7172b-107">Jos haluat päivittää tämän julkaisun, avaa Dynamics 365 online -hallintakeskuksen Ratkaisut-sivu ja asenna päivitys.</span><span class="sxs-lookup"><span data-stu-id="7172b-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="7172b-108">Lisätietoja: [Ensisijaisen ratkaisun asentaminen, päivittäminen tai poistaminen](/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="7172b-108">For more information, see [Install, update, or remove a preferred solution](/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="7172b-109">Tässä ohjeaiheessa on luettelo Project Service Automation V3, päivitysversion 25 uusista tai muuttuneista ominaisuuksista ja korjauksista. Tämän version koontiversion numero on 3.10.43.76 ja se on yleisesti saatavana omana päivityksenä lokakuussa 2020.</span><span class="sxs-lookup"><span data-stu-id="7172b-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 25 This version has a build number of V 3.10.43.76 and is generally available through a self-update in October 2020.</span></span>

## <a name="update-release-25"></a><span data-ttu-id="7172b-110">Päivitysjulkaisu 25</span><span class="sxs-lookup"><span data-stu-id="7172b-110">Update Release 25</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="7172b-111">Ohjelmavirhekorjauksia</span><span class="sxs-lookup"><span data-stu-id="7172b-111">Bug fixes</span></span>

<span data-ttu-id="7172b-112">**Aika ja kulu**</span><span class="sxs-lookup"><span data-stu-id="7172b-112">**Time and Expense**</span></span>

<span data-ttu-id="7172b-113">Seuraava ongelma on korjattu:</span><span class="sxs-lookup"><span data-stu-id="7172b-113">The following issue has been fixed:</span></span>

- <span data-ttu-id="7172b-114">Aikamerkintäkaavio sisältää lisätietoja liian pitkästä noudon aikavälistä.</span><span class="sxs-lookup"><span data-stu-id="7172b-114">Time entry chart showing additional data based on too large of an interval being retrieved.</span></span>

<span data-ttu-id="7172b-115">**Resurssienhallinta**</span><span class="sxs-lookup"><span data-stu-id="7172b-115">**Resource Management**</span></span>

<span data-ttu-id="7172b-116">Seuraava ongelma on korjattu:</span><span class="sxs-lookup"><span data-stu-id="7172b-116">The following issue has been fixed:</span></span>

- <span data-ttu-id="7172b-117">Lisättiin Package Deployer -koodi ohittamaan Universal Resource Scheduling -korjaustiedoston tuonti, jos uudempi korjaustiedoston versio on jo olemassa.</span><span class="sxs-lookup"><span data-stu-id="7172b-117">Added package deployer code to skip the Universal Resource Scheduling patch import if a higher version patch already exists.</span></span>

<span data-ttu-id="7172b-118">**Projektinhallinta**</span><span class="sxs-lookup"><span data-stu-id="7172b-118">**Project Management**</span></span>

<span data-ttu-id="7172b-119">Seuraavat ongelmat on korjattu:</span><span class="sxs-lookup"><span data-stu-id="7172b-119">The following issues have been fixed:</span></span>

- <span data-ttu-id="7172b-120">Korjattiin pyöristys- ja vaihtokurssipoikkeamat, joiden seurauksena oli virheellisesti suunniteltu kustannus projektin seurantaruudukossa.</span><span class="sxs-lookup"><span data-stu-id="7172b-120">Corrected rounding and exchange rate discrepancies resulting in incorrect planned cost in the project tracking grid.</span></span>
- <span data-ttu-id="7172b-121">Tukee mahdollisuutta näyttää vähintään kaksi reagointiruudukkoa **Projekti**-lomakkeessa.</span><span class="sxs-lookup"><span data-stu-id="7172b-121">Support the ability to display two or more react grids on the **Project** form.</span></span>
- <span data-ttu-id="7172b-122">Annettu vahvistus, jolla voi delegoida tehtävän kalenteriin päättymispäivän jälkeen, jolloin seurauksena on epäonnistunut resurssin delegointi.</span><span class="sxs-lookup"><span data-stu-id="7172b-122">Provided validation to address the ability to assign a task past the calendar end date, which results in a failed resource assignment.</span></span>
- <span data-ttu-id="7172b-123">Parannettiin virheen käsittelyä ottamaan huomioon seuraavasta luotu tyhjäarvon viitepoikkeus:</span><span class="sxs-lookup"><span data-stu-id="7172b-123">Improved error handling to address Null Reference Exception generated from the following:</span></span>

    - <span data-ttu-id="7172b-124">**PreValidateProjectTeamMemberCreate**-laajennus</span><span class="sxs-lookup"><span data-stu-id="7172b-124">**PreValidateProjectTeamMemberCreate** plug-in</span></span>
    - <span data-ttu-id="7172b-125">**PreValidateProjectTaskCreate**, kun projektitehtävä luotiin ilman liitettyä projektia</span><span class="sxs-lookup"><span data-stu-id="7172b-125">**PreValidateProjectTaskCreate** when a project task is created without an associated project</span></span>
    - <span data-ttu-id="7172b-126">**PreProjectTeamMemberCreate**-laajennus</span><span class="sxs-lookup"><span data-stu-id="7172b-126">**PreProjectTeamMemberCreate** plug-in</span></span>
    - <span data-ttu-id="7172b-127">**PostProjectTeamMemberDelete**-laajennus</span><span class="sxs-lookup"><span data-stu-id="7172b-127">**PostProjectTeamMemberDelete** plug-in</span></span>
    - <span data-ttu-id="7172b-128">**PreValidateProjectTaskDelete**-laajennus</span><span class="sxs-lookup"><span data-stu-id="7172b-128">**PreValidateProjectTaskDelete** plug-in</span></span>

<span data-ttu-id="7172b-129">**Sales**</span><span class="sxs-lookup"><span data-stu-id="7172b-129">**Sales**</span></span>

<span data-ttu-id="7172b-130">Seuraavat ongelmat on korjattu:</span><span class="sxs-lookup"><span data-stu-id="7172b-130">The following issues have been fixed:</span></span>

- <span data-ttu-id="7172b-131">Parannettiin virheiden käsittelyä ottamaan huomioon tyhjäarvoinen viitepoikkeus, joka luotiin kohdasta **Kopioi projekti: arvioi HelperResource-hallinta**.</span><span class="sxs-lookup"><span data-stu-id="7172b-131">Improved error handling to address Null Reference Exceptions generated from **Copy Project: Estimates HelperResource Management**.</span></span>
- <span data-ttu-id="7172b-132">**Keskeneräiset ajan ja materiaalin laskutukset** -kohdan **Ei ole valmis laskutettavaksi** ei tyhjennä laskutustilaa.</span><span class="sxs-lookup"><span data-stu-id="7172b-132">**Not ready to Invoice** on a **Time and Material Billing Backlog** doesn't clear the billing status.</span></span>
- <span data-ttu-id="7172b-133">Korjattiin virheellisesti merkityt **Hinnat**-painikkeet **Roolin hinta**- ja **Luettelon nimikkeet** -välilehdessä.</span><span class="sxs-lookup"><span data-stu-id="7172b-133">Corrected mislabeled **Prices** buttons on the **Role Price** and **Catalog Items** tab.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]