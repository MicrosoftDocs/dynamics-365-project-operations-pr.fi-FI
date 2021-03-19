---
title: Uutuudet ja muutokset Project Service Automation -päivitysjulkaisussa 15, V3
description: Tässä aiheessa on tietoja Project Service Automation -päivitysversion 15, V3:n uusista ominaisuuksista.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 01/27/2020
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
ms.openlocfilehash: 189b99c6a4bf18b6063c7b6020dbf1ac372b41e9
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5280934"
---
# <a name="project-service-automation-update-release-15-v3"></a><span data-ttu-id="87309-103">Project Service Automation -päivitysjulkaisu 15, V3</span><span class="sxs-lookup"><span data-stu-id="87309-103">Project Service Automation Update Release 15, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="87309-104">Olemme iloisia voidessamme julkistaa uusimman Dynamics 365 Project Service Automation (PSA) -sovelluksen päivityksen.</span><span class="sxs-lookup"><span data-stu-id="87309-104">We’re pleased to announce the latest update for the Dynamics 365 Project Service Automation (PSA) application.</span></span> <span data-ttu-id="87309-105">Tämä julkaisu sisältää joitakin tärkeitä parannuksia laatuun, tehokkuuteen ja käytettävyyteen.</span><span class="sxs-lookup"><span data-stu-id="87309-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="87309-106">Tämä versio on yhteensopiva Dynamics 365 -versioiden 9.x kanssa.</span><span class="sxs-lookup"><span data-stu-id="87309-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="87309-107">Jos haluat päivittää tämän julkaisun, käy Dynamics 365 online -hallintakeskuksessa ja asenna päivitys siirtymällä Ratkaisut-sivulle.</span><span class="sxs-lookup"><span data-stu-id="87309-107">To update to this release, visit the Admin Center for Dynamics 365 online, and go to the solutions page to install the update.</span></span> <span data-ttu-id="87309-108">Lisätietoja: [Ensisijaisen ratkaisun asentaminen, päivittäminen tai poistaminen](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="87309-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="87309-109">Tässä aiheessa on luettelo ominaisuuksista ja korjauksista, jotka ovat uusia tai muuttuneita PSA V3 -päivitysjulkaisussa 15.</span><span class="sxs-lookup"><span data-stu-id="87309-109">This topic lists the features and fixes that are new or changed for PSA V3, Update Release 15.</span></span> <span data-ttu-id="87309-110">Tällä versiolla on koontinumero V3.10.5.28 ja se on ollut yleisesti saatavilla itsepalvelupäivityksenä tammikuusta 2020 lähtien.</span><span class="sxs-lookup"><span data-stu-id="87309-110">This version has a build number of V3.10.5.28 and is generally available through a self-update in January 2020.</span></span>

## <a name="update-release-15"></a><span data-ttu-id="87309-111">Päivitysjulkaisu 15</span><span class="sxs-lookup"><span data-stu-id="87309-111">Update Release 15</span></span> 

### <a name="enhancements"></a><span data-ttu-id="87309-112">Parannukset</span><span class="sxs-lookup"><span data-stu-id="87309-112">Enhancements</span></span>

- <span data-ttu-id="87309-113">Projektinhallinta</span><span class="sxs-lookup"><span data-stu-id="87309-113">Project Management</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="87309-114">Ohjelmistovirheiden korjaukset</span><span class="sxs-lookup"><span data-stu-id="87309-114">Bug fixes</span></span>

- <span data-ttu-id="87309-115">Aika ja kulu</span><span class="sxs-lookup"><span data-stu-id="87309-115">Time and Expense</span></span>

  - <span data-ttu-id="87309-116">Korjattu: Lisää latausvirheen käsittely täsmäytysnäkymään.</span><span class="sxs-lookup"><span data-stu-id="87309-116">Fixed: Add on-load error handling in the reconciliation view.</span></span>
  - <span data-ttu-id="87309-117">Korjattu: Projektiresurssikeskus: Nimeä **Summa** uudelleen epäselvyyden vähentämiseksi.</span><span class="sxs-lookup"><span data-stu-id="87309-117">Fixed: Project Resource Hub: Rename **Amount** to reduce ambiguity.</span></span>
  - <span data-ttu-id="87309-118">Korjattu: Säädä **Kopioi aikamerkinnän sarakkeet** -näkymä sisältämään tyypin.</span><span class="sxs-lookup"><span data-stu-id="87309-118">Fixed: Adjust the view **Copy Time Entry Columns** to include the type.</span></span>
  - <span data-ttu-id="87309-119">Korjattu: aikamerkinnän keston muokkaaminen ruudukkonäkymässä desimaalinumeroita käyttäen aiheuttaa joillekin numeroille tuntemattoman virheen.</span><span class="sxs-lookup"><span data-stu-id="87309-119">Fixed: Editing time entry duration in the grid view using decimal numbers results in unknown error for some numbers.</span></span>

- <span data-ttu-id="87309-120">Projektinhallinta</span><span class="sxs-lookup"><span data-stu-id="87309-120">Project Management</span></span>

  - <span data-ttu-id="87309-121">Korjattu: **Käytä seurantanäkymässä** -kohteen avattavaa valikkoa laajennetaan nyt vaihtoehtojen leveyden mukaan.</span><span class="sxs-lookup"><span data-stu-id="87309-121">Fixed: The drop-down menu for **Use in Tracking View** now expands based on the width of the options.</span></span>
  - <span data-ttu-id="87309-122">Korjattu: kun projekteja hallitaan yli 13 aikavyöhykkeellä, tehtävien laskennassa voi näkyä virheellisiä tuloksia.</span><span class="sxs-lookup"><span data-stu-id="87309-122">Fixed: When managing projects in the +13 time zone, tasks calculations can display inaccurate results.</span></span>
  - <span data-ttu-id="87309-123">Korjattu: **Ryhmän jäsenen päättymisaika** on korjattu käytettäessä 24 tunnin kalenteria.</span><span class="sxs-lookup"><span data-stu-id="87309-123">Fixed: **Team Member End Time** has been corrected when using a 24-hour calendar.</span></span>
  - <span data-ttu-id="87309-124">Korjattu: **BPF** on aktivoitu uudelleen **msdyn_project**-päälomakkeessa.</span><span class="sxs-lookup"><span data-stu-id="87309-124">Fixed: Re-activated the **BPF** in **msdyn_project** main form.</span></span>
  - <span data-ttu-id="87309-125">Korjattu: varausten laskennassa ei enää ohiteta yhtä päivää.</span><span class="sxs-lookup"><span data-stu-id="87309-125">Fixed: Assignments calculation no longer ignores one day.</span></span>
  - <span data-ttu-id="87309-126">Korjattu: projektilomakkeeseen on lisätty uusi ilmoituspalkki, kun aikavyöhyke eroaa käyttäjän ja projektin välillä.</span><span class="sxs-lookup"><span data-stu-id="87309-126">Fixed: A new notification banner has been added to the project form when the time zone differs between user and project.</span></span>

- <span data-ttu-id="87309-127">Sales</span><span class="sxs-lookup"><span data-stu-id="87309-127">Sales</span></span>

  - <span data-ttu-id="87309-128">Korjattu: kuluarvioluokan valintaa voidaan käyttää kaksoiskappaleiden suodattamiseen.</span><span class="sxs-lookup"><span data-stu-id="87309-128">Fixed: Expense estimate category lookup can be used to filter duplicates.</span></span>
  - <span data-ttu-id="87309-129">Korjattu: Koodi kohdassa **PluginDomain.ExecuteInTryCatchBlock(..)** ei enää piilota poikkeuksen alkuperää.</span><span class="sxs-lookup"><span data-stu-id="87309-129">Fixed: Code in **PluginDomain.ExecuteInTryCatchBlock(..)** no longer hides the origin of the exception.</span></span>
  - <span data-ttu-id="87309-130">Korjattu: Ei enää virheviestiä **Projektin valinta** -kohdassa **Tarjousrivi**-lomakkeessa, kun projekteja on yli 1 000.</span><span class="sxs-lookup"><span data-stu-id="87309-130">Fixed: No longer get an error message in **Project lookup** in the **Quote Line** form when there are more than 1000 projects.</span></span>
  - <span data-ttu-id="87309-131">Korjattu: **Arviot**-ruudukko työmääräarvioille ja kuluarvioille näyttää nyt oikean valuuttasymbolin.</span><span class="sxs-lookup"><span data-stu-id="87309-131">Fixed: **Estimates** grid for labor estimates and expense estimates now displays the correct currency symbol.</span></span>
  - <span data-ttu-id="87309-132">Korjattu: kun organisaatio on päivittänyt PSA:n päivitysversiosta 14 päivitysversioon 15, **Aikataulu** -välilehti ei enää näy tyhjänä **Projekti**-lomakkeessa.</span><span class="sxs-lookup"><span data-stu-id="87309-132">Fixed: After an organization updates PSA from Update Release 14 to Update Release 15, the **Schedule** tab no longer appears as blank on the **Project** form.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]