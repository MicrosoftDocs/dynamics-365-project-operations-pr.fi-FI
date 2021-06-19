---
title: Uutuudet ja muutokset Project Service Automation -päivitysjulkaisussa 29, V3
description: Tässä aiheessa on luettelo ominaisuuksista ja korjauksista, jotka ovat käytettävissä Project Service Automation -päivitysjulkaisussa 29, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 02/22/2021
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
ms.openlocfilehash: 320f4f74cb5997e42e2dc9e1d8c8a5ab95ae6647
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/10/2021
ms.locfileid: "6010467"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-29-v3"></a><span data-ttu-id="cae65-103">Uutuudet ja muutokset Project Service Automation -päivitysjulkaisussa 29, V3</span><span class="sxs-lookup"><span data-stu-id="cae65-103">What's new or changed in Project Service Automation Update Release 29, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="cae65-104">Meillä on ilo julkistaa Dynamics 365:n Project Service Automation-sovelluksen uusin päivitys.</span><span class="sxs-lookup"><span data-stu-id="cae65-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="cae65-105">Tämä julkaisu sisältää joitakin tärkeitä parannuksia laatuun, tehokkuuteen ja käytettävyyteen.</span><span class="sxs-lookup"><span data-stu-id="cae65-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="cae65-106">Tämä versio on yhteensopiva Dynamics 365 -versioiden 9.x kanssa.</span><span class="sxs-lookup"><span data-stu-id="cae65-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="cae65-107">Jos haluat päivittää tämän julkaisun, avaa Dynamics 365 online -hallintakeskuksen Ratkaisut-sivu ja asenna päivitys.</span><span class="sxs-lookup"><span data-stu-id="cae65-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="cae65-108">Lisätietoja: [Ensisijaisen ratkaisun asentaminen, päivittäminen tai poistaminen](/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="cae65-108">For more information, see [Install, update, or remove a preferred solution](/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="cae65-109">Tässä aiheessa on luettelo ominaisuuksista ja korjauksista, jotka ovat uusia tai muuttuneita Project Service Automation V3 -päivitysjulkaisussa 29.</span><span class="sxs-lookup"><span data-stu-id="cae65-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 29.</span></span> <span data-ttu-id="cae65-110">Tämän version koontiversionumero on V3.10.47.7 ja se on yleisesti saatavilla omatoimipäivityksenä helmikuussa 2021.</span><span class="sxs-lookup"><span data-stu-id="cae65-110">This version has a build number of V3.10.47.7 and is generally available through a self-update in February 2021.</span></span>

## <a name="update-release-29"></a><span data-ttu-id="cae65-111">Päivitysjulkaisu 29</span><span class="sxs-lookup"><span data-stu-id="cae65-111">Update Release 29</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="cae65-112">Ohjelmavirhekorjauksia</span><span class="sxs-lookup"><span data-stu-id="cae65-112">Bug fixes</span></span>

<span data-ttu-id="cae65-113">**Aika ja kulu**</span><span class="sxs-lookup"><span data-stu-id="cae65-113">**Time and Expense**</span></span>

<span data-ttu-id="cae65-114">Seuraavat ongelmat on korjattu:</span><span class="sxs-lookup"><span data-stu-id="cae65-114">The following issues have been fixed:</span></span>

- <span data-ttu-id="cae65-115">Käyttäjät eivät näe työaikaruudukossa ei-työpäivinä kirjattuja työaikoja.</span><span class="sxs-lookup"><span data-stu-id="cae65-115">Users can't see working hours logged on non-working days in the time entry grid.</span></span>
- <span data-ttu-id="cae65-116">Hyväksyttyjä kulumerkintöjä voidaan muokata ruudukossa.</span><span class="sxs-lookup"><span data-stu-id="cae65-116">Approved expense entries can be edited on the grid.</span></span>

<span data-ttu-id="cae65-117">**Projektinhallinta**</span><span class="sxs-lookup"><span data-stu-id="cae65-117">**Project Management**</span></span>

<span data-ttu-id="cae65-118">Seuraavat ongelmat on korjattu:</span><span class="sxs-lookup"><span data-stu-id="cae65-118">The following issues have been fixed:</span></span>

- <span data-ttu-id="cae65-119">Puuttuva vahvistuslogiikka sen varmistamiseksi, että resurssien varaukseen käytetyt työtunnit eivät voi olla negatiivisia.</span><span class="sxs-lookup"><span data-stu-id="cae65-119">Missing validation logic to ensure resource assignment effort hours can't be negative.</span></span>
- <span data-ttu-id="cae65-120">Mukautettu **AssignResourcesForTask**-toiminto päivittää kaikki kentät vain muutettujen kenttien sijaan.</span><span class="sxs-lookup"><span data-stu-id="cae65-120">The custom action, **AssignResourcesForTask** updates all fields instead of only changed fields.</span></span>
- <span data-ttu-id="cae65-121">Kun kopioit projektin ympäristössä, jossa on **LuoProjekti**-tapahtumaan rekisteröityjä laajennuksia tai työnkulkuja, **msdyn_bulkgenerationstatus**-määritettä ei päivitä, jos **KopioiWBSprojektiin**-toiminto epäonnistuu.</span><span class="sxs-lookup"><span data-stu-id="cae65-121">When copying a project in an environment with plug-ins or workflows that are registered on the **CreateProject** event, the **msdyn_bulkgenerationstatus** attribute isn't updated if the **CopyWBSToProject** fails.</span></span>
- <span data-ttu-id="cae65-122">Kun laajennat projektikalenterin, työpäiviä ei lajitella nousevassa järjestyksessä, jolloin jotkin projektitehtäväpäivitykset epäonnistuvat.</span><span class="sxs-lookup"><span data-stu-id="cae65-122">When you expand the project calendar, the working days aren't sorted in ascending order causing some project task updates to fail.</span></span>
- <span data-ttu-id="cae65-123">Projektinhallinnan muuttaminen aiemmin luodussa projektissa käynnistää organisaatioyksikön oletuslogiikan.</span><span class="sxs-lookup"><span data-stu-id="cae65-123">Changing the Project Manager on an existing project triggers the organizational unit defaulting logic.</span></span>

<span data-ttu-id="cae65-124">**Myynti**</span><span class="sxs-lookup"><span data-stu-id="cae65-124">**Sales**</span></span>

<span data-ttu-id="cae65-125">Seuraavat ongelmat on korjattu:</span><span class="sxs-lookup"><span data-stu-id="cae65-125">The following issues have been fixed:</span></span>

- <span data-ttu-id="cae65-126">**Sopimus**-sivun **Sopimuksen suorituskyky** -välilehti epäonnistuu hiljaisesti alustuksen aikana, kun sopimusrivejä ei ole.</span><span class="sxs-lookup"><span data-stu-id="cae65-126">The **Contract Performance** tab on the **Contract** page fails silently during initialization when no contract lines are present.</span></span>