---
title: Uutuudet ja muutokset Project Service Automation -päivitysjulkaisussa 23, V3
description: Tässä aiheessa on luettelo ominaisuuksista ja korjauksista, jotka ovat käytettävissä Project Service Automation -päivitysjulkaisussa 23, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 08/25/2020
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
ms.openlocfilehash: adf893a0627ae59f2132bb46686110dafda01d3d
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/10/2021
ms.locfileid: "6006462"
---
# <a name="project-service-automation-update-release-23-v3"></a><span data-ttu-id="63063-103">Project Service Automation -päivitysjulkaisu 23, V3</span><span class="sxs-lookup"><span data-stu-id="63063-103">Project Service Automation Update Release 23, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="63063-104">Meillä on ilo julkistaa Dynamics 365:n Project Service Automation-sovelluksen uusin päivitys.</span><span class="sxs-lookup"><span data-stu-id="63063-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="63063-105">Tämä julkaisu sisältää joitakin tärkeitä parannuksia laatuun, tehokkuuteen ja käytettävyyteen.</span><span class="sxs-lookup"><span data-stu-id="63063-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="63063-106">Tämä versio on yhteensopiva Dynamics 365 -versioiden 9.x kanssa.</span><span class="sxs-lookup"><span data-stu-id="63063-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="63063-107">Jos haluat päivittää tämän julkaisun, avaa Dynamics 365 online -hallintakeskuksen Ratkaisut-sivu ja asenna päivitys.</span><span class="sxs-lookup"><span data-stu-id="63063-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="63063-108">Lisätietoja: [Ensisijaisen ratkaisun asentaminen, päivittäminen tai poistaminen](/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="63063-108">For more information, see [Install, update, or remove a preferred solution](/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="63063-109">Tässä aiheessa on luettelo ominaisuuksista ja korjauksista, jotka ovat uusia tai muuttuneita Project Service Automation V3 -päivitysjulkaisussa 23.</span><span class="sxs-lookup"><span data-stu-id="63063-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 23.</span></span> <span data-ttu-id="63063-110">Tällä versiolla on koontinumero V3.10.34.30 ja se on ollut yleisesti saatavilla itsepalvelupäivityksenä elokuusta 2020 lähtien.</span><span class="sxs-lookup"><span data-stu-id="63063-110">This version has a build number of V 3.10.34.30 and is generally available through a self-update in August 2020.</span></span>

## <a name="update-release-23"></a><span data-ttu-id="63063-111">Päivitysjulkaisu 23</span><span class="sxs-lookup"><span data-stu-id="63063-111">Update Release 23</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="63063-112">Ohjelmavirhekorjauksia</span><span class="sxs-lookup"><span data-stu-id="63063-112">Bug fixes</span></span>

<span data-ttu-id="63063-113">**Aika ja kulu**</span><span class="sxs-lookup"><span data-stu-id="63063-113">**Time and Expense**</span></span>

<span data-ttu-id="63063-114">Seuraavat ongelmat on korjattu:</span><span class="sxs-lookup"><span data-stu-id="63063-114">The following issues have been fixed:</span></span>
- <span data-ttu-id="63063-115">Käsittele reunan palvelupyyntö kohdassa **Projektiryhmän jäsenen poisto**, jotta saat mielekkään poikkeuksen.</span><span class="sxs-lookup"><span data-stu-id="63063-115">Handle edge case in **Project Team Member Delete** to provide a meaningful exception.</span></span>
- <span data-ttu-id="63063-116">Delegoinnin tuonnin tuloksena on tyhjä poistoruutu.</span><span class="sxs-lookup"><span data-stu-id="63063-116">Assignment import results in a blank remove screen.</span></span>

<span data-ttu-id="63063-117">**Resurssienhallinta**</span><span class="sxs-lookup"><span data-stu-id="63063-117">**Resource Management**</span></span>

<span data-ttu-id="63063-118">Seuraavat ongelmat on korjattu:</span><span class="sxs-lookup"><span data-stu-id="63063-118">The following issues have been fixed:</span></span>

- <span data-ttu-id="63063-119">**Resurssin käyttöasteruudukon resurssikortissa** näkyy virheellisiä tietoja, kun aika-asteikko on yli viisi päivää.</span><span class="sxs-lookup"><span data-stu-id="63063-119">The **Resource utilization grid resource card** shows incorrect data when the time scale is more than five days.</span></span>
- <span data-ttu-id="63063-120">Kun asiakkaat luovat varattavissa olevan resurssin, laajennus ei välillä lisää resurssia automaattisesti Microsoft Office 365 -ryhmään.</span><span class="sxs-lookup"><span data-stu-id="63063-120">When customers create a bookable resource, the plug-in intermittently fails to automatically add the resource to a Microsoft Office 365 group.</span></span>
- <span data-ttu-id="63063-121">**Täsmäytys**-näkymä näyttää manuaaliset muodot virheellisesti **Viikko**- tai **Kuukausi**-näkymässä.</span><span class="sxs-lookup"><span data-stu-id="63063-121">**Reconciliation** view displays manual contours incorrectly in the **Week** or **Month** view.</span></span>

<span data-ttu-id="63063-122">**Projektinhallinta**</span><span class="sxs-lookup"><span data-stu-id="63063-122">**Project Management**</span></span>

<span data-ttu-id="63063-123">Seuraavat ongelmat on korjattu:</span><span class="sxs-lookup"><span data-stu-id="63063-123">The following issues have been fixed:</span></span>

- <span data-ttu-id="63063-124">Jos **usersettings-asetuksen RetrieveMultiple** -entiteettejä on liian suuri määrä, se heikentää projektien hyväksyntöjen ja muiden toimintojen suorituskykyä.</span><span class="sxs-lookup"><span data-stu-id="63063-124">An excessive number of **RetrieveMultiple for usersettings** entities are causing degraded performance for project approvals and other operations.</span></span>
- <span data-ttu-id="63063-125">**Tehtävien suunnittelu** -ruudukon resurssivalinta on rajoitettu näyttämään enintään viisi projektiryhmän jäsentä.</span><span class="sxs-lookup"><span data-stu-id="63063-125">The **Task Planning** grid resource lookup is limited to only show up to five team members from the project team.</span></span> 
- <span data-ttu-id="63063-126">**Tehtävien suunnittelu** -ruudukon resurssihaku ei suodata passiivisia resursseja.</span><span class="sxs-lookup"><span data-stu-id="63063-126">The **Task Planning** grid resource lookup does not filter inactive resources.</span></span>
- <span data-ttu-id="63063-127">Manuaalinen tila ei toimi odotetulla tavalla projektisuunnittelun työrakenteessa.</span><span class="sxs-lookup"><span data-stu-id="63063-127">Manual mode is not working as expected in the project planning work breakdown structure.</span></span>
- <span data-ttu-id="63063-128">**Tehtävien suunnittelu** -ruudukko näyttää **Passiiviset tapahtumaluokat**.</span><span class="sxs-lookup"><span data-stu-id="63063-128">The **Task Planning** grid shows **Inactive Transaction Categories**.</span></span>
- <span data-ttu-id="63063-129">**Resurssien delegointi** -ruudukko pyöristää virheellisesti, kun tehtävällä on useita varauksia.</span><span class="sxs-lookup"><span data-stu-id="63063-129">The **Resource Assignment** grid rounds incorrectly when a task has multiple assignments.</span></span>
- <span data-ttu-id="63063-130">Pyöristysarvot eroavat suunniteltujen kustannusten ja todellisten kustannusten välillä yksittäisessä tehtävässä.</span><span class="sxs-lookup"><span data-stu-id="63063-130">Rounding values are different between planned cost and actual cost for a single task.</span></span>

<span data-ttu-id="63063-131">**Sales**</span><span class="sxs-lookup"><span data-stu-id="63063-131">**Sales**</span></span>

<span data-ttu-id="63063-132">Seuraavat ongelmat on korjattu:</span><span class="sxs-lookup"><span data-stu-id="63063-132">The following issues have been fixed:</span></span>

- <span data-ttu-id="63063-133">**Nouda kaikki tapahtumaluokat** -kaksoisnapsautus luo useita rivejä.</span><span class="sxs-lookup"><span data-stu-id="63063-133">**Fetch All Transaction Categories** double-click creates multiple lines.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]