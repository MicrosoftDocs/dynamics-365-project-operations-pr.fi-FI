---
title: Uutuudet ja muutokset Project Service Automation -päivitysjulkaisussa 33, V3
description: Tässä aiheessa on luettelo ominaisuuksista ja korjauksista, jotka ovat käytettävissä Project Service Automation -päivitysjulkaisussa 33, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 06/30/2021
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
ms.openlocfilehash: 2c96e4abd484bb66285421baaad82ead9589bbe9
ms.sourcegitcommit: be5beba71ee9770c0083b4fe5cc89e7ec6b741b8
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 07/02/2021
ms.locfileid: "6334530"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-33-v3"></a><span data-ttu-id="41302-103">Uutuudet ja muutokset Project Service Automation -päivitysjulkaisussa 33, V3</span><span class="sxs-lookup"><span data-stu-id="41302-103">What's new or changed in Project Service Automation Update Release 33, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="41302-104">Meillä on ilo esitellä Microsoft Dynamics 365 Project Service Automation -sovelluksen uusin päivitys.</span><span class="sxs-lookup"><span data-stu-id="41302-104">We're pleased to announce the latest update for the Microsoft Dynamics 365 Project Service Automation app.</span></span> <span data-ttu-id="41302-105">Tämä julkaisu sisältää joitakin tärkeitä parannuksia laatuun, tehokkuuteen ja käytettävyyteen.</span><span class="sxs-lookup"><span data-stu-id="41302-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="41302-106">Se on yhteensopiva Dynamics 365 9.x -version kanssa.</span><span class="sxs-lookup"><span data-stu-id="41302-106">It's compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="41302-107">Päivitä tähän versioon asentamalla päivitys Dynamics 365 -hallintakeskuksen online-ratkaisujen sivulta.</span><span class="sxs-lookup"><span data-stu-id="41302-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page, and install the update.</span></span> <span data-ttu-id="41302-108">Lisätietoja: [Ensisijaisen ratkaisun asentaminen, päivittäminen tai poistaminen](/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="41302-108">For more information, see [Install, update, or remove a preferred solution](/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="41302-109">Tässä aiheessa on luettelo ominaisuuksista ja korjauksista, jotka ovat uusia tai muuttuneita Project Service Automation V3 -päivitysjulkaisussa 33.</span><span class="sxs-lookup"><span data-stu-id="41302-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 33.</span></span> <span data-ttu-id="41302-110">Tämän version koontiversionumero on V3.10.54.98 ja se on yleisesti saatavilla itsepäivityksenä heinäkuussa 2021.</span><span class="sxs-lookup"><span data-stu-id="41302-110">This version has a build number of V3.10.54.98 and is generally available through a self-update in July 2021.</span></span>

## <a name="update-release-33"></a><span data-ttu-id="41302-111">Päivitysjulkaisu 33</span><span class="sxs-lookup"><span data-stu-id="41302-111">Update Release 33</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="41302-112">Ohjelmavirhekorjauksia</span><span class="sxs-lookup"><span data-stu-id="41302-112">Bug fixes</span></span>

<span data-ttu-id="41302-113">**Aika ja kulu**</span><span class="sxs-lookup"><span data-stu-id="41302-113">**Time and Expense**</span></span>

<span data-ttu-id="41302-114">Seuraavat ongelmat on korjattu:</span><span class="sxs-lookup"><span data-stu-id="41302-114">The following issues have been fixed:</span></span>

- <span data-ttu-id="41302-115">Kaksi lukittua kenttää, **msdyn_description** ja **msdyn_externaldescription** ovat muokattavissa lähettämisen jälkeen.</span><span class="sxs-lookup"><span data-stu-id="41302-115">Two locked fields, **msdyn_description** and **msdyn_externaldescription** are editable after submission.</span></span>
- <span data-ttu-id="41302-116">Virhesanoma tulee näyttöön, jos luodaan kulu, joka ei liity projektiin.</span><span class="sxs-lookup"><span data-stu-id="41302-116">An error message occurs if an expense is created that isn't related to a project.</span></span>
- <span data-ttu-id="41302-117">Kun aikamerkintä luodaan, resurssirooliksi tulee oletusarvo passiivinen rooli.</span><span class="sxs-lookup"><span data-stu-id="41302-117">When a time entry is created, the resource role defaults to an inactive role.</span></span>
- <span data-ttu-id="41302-118">Takaisinvetoon ja poistettuun kuluun liittyviä kirjauskansion rivejä ei poisteta.</span><span class="sxs-lookup"><span data-stu-id="41302-118">Journal lines associated with a recalled and deleted expense aren't deleted.</span></span>
- <span data-ttu-id="41302-119">Päivitä **Aikamerkinnän pikaluontilomakkeessa** **Projektitehtäväluettelo**-näkymä muuttaaksesi oletusarvoisesti tehtävän alkamispäiväksi näytettävä päivämäärä.</span><span class="sxs-lookup"><span data-stu-id="41302-119">On the **Time entry Quick Create Form**, update the **Project Task List** view to change the date displayed by default to the start date of the task.</span></span>
- <span data-ttu-id="41302-120">Kun luot aikamerkinnän varattavissa olevan resurssin **Liittyvä**-välilehdessä, ajankirjaaminen luodaan virheellisesti kirjautuneena olevalle käyttäjälle päätason varattavissa olevan resurssin asemesta.</span><span class="sxs-lookup"><span data-stu-id="41302-120">When you create a time entry from the **Related** tab of the bookable resource, the time entry is incorrectly created for the signed-in user instead of the parent bookable resource.</span></span>
- <span data-ttu-id="41302-121">**Joukkohyväksyntä MDD**-valintaikkunaan lisätään uusia kenttiä.</span><span class="sxs-lookup"><span data-stu-id="41302-121">New fields are added to the **Bulk approval MDD** dialog box.</span></span>

<span data-ttu-id="41302-122">**Projektin suunnittelu**</span><span class="sxs-lookup"><span data-stu-id="41302-122">**Project planning**</span></span>

<span data-ttu-id="41302-123">Seuraavat ongelmat on korjattu:</span><span class="sxs-lookup"><span data-stu-id="41302-123">The following issues have been fixed:</span></span>
- <span data-ttu-id="41302-124">Projektin luonnin hidas suorituskyky, kun projektityötuntimalleja käytetään monitasoisten kalenterien kanssa.</span><span class="sxs-lookup"><span data-stu-id="41302-124">Slow project creation performance when project work hour templates are applied with complex calendars.</span></span>
- <span data-ttu-id="41302-125">Jos alkamispäivä on päättymispäivää suurempi, projektimallissa näkyy virhe, koska kussakin kentässä on eroja aikakomponentissa.</span><span class="sxs-lookup"><span data-stu-id="41302-125">When the start date is greater than the end date, an error displays on the copy project template because of differences in the time component of each field.</span></span>

<span data-ttu-id="41302-126">**Resurssien hallinta**</span><span class="sxs-lookup"><span data-stu-id="41302-126">**Resource management**</span></span>

<span data-ttu-id="41302-127">Seuraavat ongelmat on korjattu:</span><span class="sxs-lookup"><span data-stu-id="41302-127">The following issues have been fixed:</span></span>
- <span data-ttu-id="41302-128">Resurssin käyttökyselyssä käytetään virheellistä parametria, ja XML-liidit johtavat virheellisiin suodatustuloksiin **Resurssin käyttö** -ruudukossa.</span><span class="sxs-lookup"><span data-stu-id="41302-128">An incorrect parameter is used in the resource utilization query and the XML leads to incorrect filter results on the **Resource Utilization** grid.</span></span>
- <span data-ttu-id="41302-129">**Varausten jatkaminen** -vahvistus näyttää virheellisen päättymispäivän varauksia varten.</span><span class="sxs-lookup"><span data-stu-id="41302-129">The **Extend Bookings** confirmation displays incorrect end date for bookings.</span></span>

<span data-ttu-id="41302-130">**Myynti**</span><span class="sxs-lookup"><span data-stu-id="41302-130">**Sales**</span></span>

<span data-ttu-id="41302-131">Seuraavat ongelmat on korjattu:</span><span class="sxs-lookup"><span data-stu-id="41302-131">The following issues have been fixed:</span></span>
- <span data-ttu-id="41302-132">Virheilmoitus tapahtuu luotaessa luokkahintaa, jonka arvot puuttuvat.</span><span class="sxs-lookup"><span data-stu-id="41302-132">An error message occurs if a category price is created with missing values.</span></span>
- <span data-ttu-id="41302-133">Virheilmoitus tapahtuu luotaessa sopimusrivin välitavoitetta ilman tilausriviä.</span><span class="sxs-lookup"><span data-stu-id="41302-133">An error message occurs if a contract line milestone is created without an order line.</span></span>
