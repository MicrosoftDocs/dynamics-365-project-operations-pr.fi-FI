---
title: Uutuudet ja muutokset Project Service Automation -päivitysjulkaisussa 22, V3
description: Tässä aiheessa on luettelo ominaisuuksista ja korjauksista, jotka ovat käytettävissä Project Service Automation -päivitysjulkaisussa 22, V3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 07/28/2020
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
ms.openlocfilehash: 8863d321ad88d761d0fcbd82ca26562a69468f2f
ms.sourcegitcommit: 3d78338773929121d17ec3386f6cb67bfb2272cc
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/27/2021
ms.locfileid: "5949000"
---
# <a name="project-service-automation-update-release-22-v3"></a><span data-ttu-id="13b41-103">Project Service Automation -päivitysjulkaisu 22, V3</span><span class="sxs-lookup"><span data-stu-id="13b41-103">Project Service Automation Update Release 22, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="13b41-104">Meillä on ilo julkistaa Dynamics 365:n Project Service Automation-sovelluksen uusin päivitys.</span><span class="sxs-lookup"><span data-stu-id="13b41-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="13b41-105">Tämä julkaisu sisältää joitakin tärkeitä parannuksia laatuun, tehokkuuteen ja käytettävyyteen.</span><span class="sxs-lookup"><span data-stu-id="13b41-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="13b41-106">Tämä versio on yhteensopiva Dynamics 365 -versioiden 9.x kanssa.</span><span class="sxs-lookup"><span data-stu-id="13b41-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="13b41-107">Jos haluat päivittää tämän julkaisun, avaa Dynamics 365 online -hallintakeskuksen Ratkaisut-sivu ja asenna päivitys.</span><span class="sxs-lookup"><span data-stu-id="13b41-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="13b41-108">Lisätietoja: [Ensisijaisen ratkaisun asentaminen, päivittäminen tai poistaminen](/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="13b41-108">For more information, see [Install, update, or remove a preferred solution](/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="13b41-109">Tässä aiheessa on luettelo ominaisuuksista ja korjauksista, jotka ovat uusia tai muuttuneita Project Service Automation V3 -päivitysjulkaisussa 22.</span><span class="sxs-lookup"><span data-stu-id="13b41-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 22.</span></span> <span data-ttu-id="13b41-110">Tämän version koontiversion numero on V 3.10.33.48, ja se on yleisesti saatavana itsepäivittyvänä kesäkuussa 2020.</span><span class="sxs-lookup"><span data-stu-id="13b41-110">This version has a build number of V 3.10.33.48 and is generally available through a self-update in June 2020.</span></span>

## <a name="update-release-22"></a><span data-ttu-id="13b41-111">Päivitysjulkaisu 22</span><span class="sxs-lookup"><span data-stu-id="13b41-111">Update Release 22</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="13b41-112">Ohjelmavirhekorjauksia</span><span class="sxs-lookup"><span data-stu-id="13b41-112">Bug fixes</span></span>



<span data-ttu-id="13b41-113">**Aika ja kulu**</span><span class="sxs-lookup"><span data-stu-id="13b41-113">**Time and Expense**</span></span>

<span data-ttu-id="13b41-114">Seuraavat ongelmat on korjattu:</span><span class="sxs-lookup"><span data-stu-id="13b41-114">The following issues have been fixed:</span></span>

- <span data-ttu-id="13b41-115">**Aikamerkintöjä** ei lisätä automaattisesti aikamerkintöjen aikatauluun tuonnin jälkeen.</span><span class="sxs-lookup"><span data-stu-id="13b41-115">**Time entries** are not automatically added in the Time entries schedule after import.</span></span>
- <span data-ttu-id="13b41-116">**Aikamerkinnän** ruudukon päivämäärävalitsin ei tunnista käyttäjän aluekohtaisia asetuksia.</span><span class="sxs-lookup"><span data-stu-id="13b41-116">The **Time Entry** grid date picker does not recognize a user's regional settings.</span></span>

<span data-ttu-id="13b41-117">**Resurssienhallinta**</span><span class="sxs-lookup"><span data-stu-id="13b41-117">**Resource Management**</span></span>

<span data-ttu-id="13b41-118">Seuraavat ongelmat on korjattu:</span><span class="sxs-lookup"><span data-stu-id="13b41-118">The following issues have been fixed:</span></span>

- <span data-ttu-id="13b41-119">**Resurssien delegointi** -jaksotusten muutoksia ei tunnisteta manuaalisessa tilassa, kun **resurssitarpeita** luodaan.</span><span class="sxs-lookup"><span data-stu-id="13b41-119">In manual mode, changes to **Resource Assignment** contours are not recognized when generating **Resource Requirements**.</span></span>
- <span data-ttu-id="13b41-120">**Resurssipyynnöt** eivät tue mukautetun pyynnön tiloja.</span><span class="sxs-lookup"><span data-stu-id="13b41-120">**Resource Requests** do not support custom request statuses.</span></span>

<span data-ttu-id="13b41-121">**Projektinhallinta**</span><span class="sxs-lookup"><span data-stu-id="13b41-121">**Project Management**</span></span>

<span data-ttu-id="13b41-122">Seuraavat ongelmat on korjattu:</span><span class="sxs-lookup"><span data-stu-id="13b41-122">The following issues have been fixed:</span></span>

- <span data-ttu-id="13b41-123">EstimateGridControl-ohjausobjektin kaksoisnapsautus ei jäsennä oikein hollantilaisen muotoilun numeroita.</span><span class="sxs-lookup"><span data-stu-id="13b41-123">Using double-click on EstimateGridControl will not correctly parse Dutch format numbers.</span></span>
- <span data-ttu-id="13b41-124">Delegoidut tunnit eivät päivity oikein, kun delegointeja muutetaan Microsoft Projectin työpöytäasiakasohjelman apuohjelmalla.</span><span class="sxs-lookup"><span data-stu-id="13b41-124">Assigned hours do not update correctly when assignments are changed using the Microsoft Project desktop client add-in.</span></span>
- <span data-ttu-id="13b41-125">Projektin seuranta- ja Arviot-ruudukoissa näkyy virheellinen myyntivaluutan koodi, kun sopimusvaluutta ei ole sama kuin asiakasvaluutta ja kun organisaation on määritetty näyttämään valuuttakoodit eikä rahayksikön tunnuksia.</span><span class="sxs-lookup"><span data-stu-id="13b41-125">Project Tracking and Estimates grids display incorrect sales currency code when contract currency is different than customer currency and organization is configured to display currency codes instead of currency symbols.</span></span>
- <span data-ttu-id="13b41-126">Ryhmän jäsenen päättymispäivä lisää yhden päivän, jos työaika-aikataulu käyttää 24 tunnin aikataulua.</span><span class="sxs-lookup"><span data-stu-id="13b41-126">A Team member's finish date will add one day if the work hour schedule is 24-hours per day.</span></span>
- <span data-ttu-id="13b41-127">Tapahtumaluokan lisääminen projektiaikataulussa tehtävään ei käynnistä automaattista tallennusta.</span><span class="sxs-lookup"><span data-stu-id="13b41-127">On the Project Schedule, adding a Transaction Category to a task does not trigger auto save.</span></span>
- <span data-ttu-id="13b41-128">Seuraava virhe näytetään, kun ryhmän jäsen lisätään projektimalliin: Resurssitarpeita ei voi liittää projektimalleihin.</span><span class="sxs-lookup"><span data-stu-id="13b41-128">The following error is displayed when adding a team member to the Project Template: "Resource requirements cannot be associated with project templates".</span></span> 
- <span data-ttu-id="13b41-129">Valintanauhasäännön skripti msdyn.Approval.CanApproveOrReject näyttää aikakatkaisuvirheen.</span><span class="sxs-lookup"><span data-stu-id="13b41-129">Ribbon rule script "msdyn.Approval.CanApproveOrReject" displays a timeout error.</span></span>

<span data-ttu-id="13b41-130">**Sales**</span><span class="sxs-lookup"><span data-stu-id="13b41-130">**Sales**</span></span>

<span data-ttu-id="13b41-131">Seuraavat ongelmat on korjattu:</span><span class="sxs-lookup"><span data-stu-id="13b41-131">The following issues have been fixed:</span></span>

- <span data-ttu-id="13b41-132">Vahvistuksen virhesanomaa ei näytetä, kun kustannushinnasto valitaan hinnastovalinnassa Uusi tarjouksen projektihinnasto -lomakkeessa tai -entiteetissä.</span><span class="sxs-lookup"><span data-stu-id="13b41-132">Validation error message not displayed when a Cost Price List is selected in Price List lookup on 'New Quote Project Price List' form/entity.</span></span>
- <span data-ttu-id="13b41-133">Tarjouksen sulkeminen voitettuna ei siirrä luotuun sopimukseen, jos tarjoukseen liitetty liiketoimintaprosessi on viimeisessä vaiheessa.</span><span class="sxs-lookup"><span data-stu-id="13b41-133">Closing the quote as won does not navigate to the created contract if a BPF attached to the quote is in the final stage.</span></span>
- <span data-ttu-id="13b41-134">**Laskuttamattoman myynnin** vastakirjaus linkitetään alkuperäiseen kustannukseen, kun aikamerkintä palautettiin.</span><span class="sxs-lookup"><span data-stu-id="13b41-134">Reversing **Unbilled Sales** is linked to original cost when a time entry is recalled.</span></span>
- <span data-ttu-id="13b41-135">Laskun tilaksi ei tule **Vahvistettu** **Vahvista**-painikkeen valinnan jälkeen, jos laskua ei päivitetä.</span><span class="sxs-lookup"><span data-stu-id="13b41-135">After selecting the **Confirm** button, the invoice status doesn't change to **Confirmed** unless the invoice is refreshed.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]