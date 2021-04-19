---
title: Uutuudet ja muutokset Project Service Automation -päivitysjulkaisussa 30, V3
description: Tässä aiheessa on luettelo ominaisuuksista ja korjauksista, jotka ovat käytettävissä Project Service Automation -päivitysjulkaisussa 30, V3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 04/01/2021
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
ms.openlocfilehash: 1169ee13c42e982cb30a40d92df660f8933786a9
ms.sourcegitcommit: b4a05c7d5512d60abdb0d05bedd390e288e8adc9
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/02/2021
ms.locfileid: "5852847"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-30-v3"></a><span data-ttu-id="6bebd-103">Uutuudet ja muutokset Project Service Automation -päivitysjulkaisussa 30, V3</span><span class="sxs-lookup"><span data-stu-id="6bebd-103">What's new or changed in Project Service Automation Update Release 30, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="6bebd-104">Meillä on ilo julkistaa Dynamics 365:n Project Service Automation-sovelluksen uusin päivitys.</span><span class="sxs-lookup"><span data-stu-id="6bebd-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="6bebd-105">Tämä julkaisu sisältää joitakin tärkeitä parannuksia laatuun, tehokkuuteen ja käytettävyyteen.</span><span class="sxs-lookup"><span data-stu-id="6bebd-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="6bebd-106">Tämä versio on yhteensopiva Dynamics 365 -versioiden 9.x kanssa.</span><span class="sxs-lookup"><span data-stu-id="6bebd-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="6bebd-107">Jos haluat päivittää tämän julkaisun, avaa Dynamics 365 online -hallintakeskuksen Ratkaisut-sivu ja asenna päivitys.</span><span class="sxs-lookup"><span data-stu-id="6bebd-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="6bebd-108">Lisätietoja: [Ensisijaisen ratkaisun asentaminen, päivittäminen tai poistaminen](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="6bebd-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="6bebd-109">Tässä aiheessa on luettelo ominaisuuksista ja korjauksista, jotka ovat uusia tai muuttuneita Project Service Automation V3 -päivitysjulkaisussa 30.</span><span class="sxs-lookup"><span data-stu-id="6bebd-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 30.</span></span> <span data-ttu-id="6bebd-110">Tämän version koontiversion numero on V3.10.51.61, ja se on yleisesti saatavana itsepäivittyvänä huhtikuussa 2021.</span><span class="sxs-lookup"><span data-stu-id="6bebd-110">This version has a build number of V3.10.51.61 and is generally available through a self-update in April 2021.</span></span>

## <a name="update-release-30"></a><span data-ttu-id="6bebd-111">Päivitysjulkaisu 30</span><span class="sxs-lookup"><span data-stu-id="6bebd-111">Update Release 30</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="6bebd-112">Ohjelmavirhekorjauksia</span><span class="sxs-lookup"><span data-stu-id="6bebd-112">Bug fixes</span></span>

<span data-ttu-id="6bebd-113">**Aika ja kulu**</span><span class="sxs-lookup"><span data-stu-id="6bebd-113">**Time and Expense**</span></span>

<span data-ttu-id="6bebd-114">Seuraavat ongelmat on korjattu:</span><span class="sxs-lookup"><span data-stu-id="6bebd-114">The following issues have been fixed:</span></span>

- <span data-ttu-id="6bebd-115">Virhe luotaessa ja tallennettaessa aikasyötettä **Pikaluonti**-sivulla, jos **Rooli**-kenttä poistetaan.</span><span class="sxs-lookup"><span data-stu-id="6bebd-115">An error occurs when you create and save a time entry on the **Quick Create** page if the **Role** field is removed.</span></span>
- <span data-ttu-id="6bebd-116">Ajan syöttösuodatin käyttää väärää suodatusoperaattoria.</span><span class="sxs-lookup"><span data-stu-id="6bebd-116">The Time Entry filter applies the wrong filter operator.</span></span>
- <span data-ttu-id="6bebd-117">Kopioidut työaikaraportit eivät tule näkyviin automaattisesti, kun valitset ajan syötteenohjausobjektista **Kopioi viikko**.</span><span class="sxs-lookup"><span data-stu-id="6bebd-117">Copied timesheets aren't automatically displayed when you select **Copy Week** on the time entry control.</span></span>

<span data-ttu-id="6bebd-118">**Resurssienhallinta**</span><span class="sxs-lookup"><span data-stu-id="6bebd-118">**Resource Management**</span></span>

<span data-ttu-id="6bebd-119">Seuraavat ongelmat on korjattu:</span><span class="sxs-lookup"><span data-stu-id="6bebd-119">The following issues have been fixed:</span></span>

- <span data-ttu-id="6bebd-120">Kun laajennat varauksen, kovalle varaukselle määritetty varaustila on virheellinen.</span><span class="sxs-lookup"><span data-stu-id="6bebd-120">When you extend a booking, the booking status assigned to the hard booking is incorrect.</span></span> <span data-ttu-id="6bebd-121">Varauksen laajentaminen noudattaa varausmäärityksen metatiedoissa **Sidottu**-tilaksi määritettyä varaustilaa.</span><span class="sxs-lookup"><span data-stu-id="6bebd-121">Extending a booking respects the booking status defined as **Committed** in the booking setup metadata.</span></span>
- <span data-ttu-id="6bebd-122">Kun kelvollista varaustilaa ei määritetä, virhesanomaa ei lokalisoida oikein.</span><span class="sxs-lookup"><span data-stu-id="6bebd-122">When a valid booking status isn't specified, the error message is not correctly localized.</span></span>

<span data-ttu-id="6bebd-123">**Projektinhallinta**</span><span class="sxs-lookup"><span data-stu-id="6bebd-123">**Project Management**</span></span>

<span data-ttu-id="6bebd-124">Seuraavat ongelmat on korjattu:</span><span class="sxs-lookup"><span data-stu-id="6bebd-124">The following issues have been fixed:</span></span>

- <span data-ttu-id="6bebd-125">Projekteja ei voi luoda yhtenä valuuttana ja sisällyttää niihin liittyviä tehtäviä toiseen valuuttaan.</span><span class="sxs-lookup"><span data-stu-id="6bebd-125">Projects can't be created in one currency and include related tasks in another currency.</span></span>

<span data-ttu-id="6bebd-126">**Myynti**</span><span class="sxs-lookup"><span data-stu-id="6bebd-126">**Sales**</span></span>

<span data-ttu-id="6bebd-127">Seuraavat ongelmat on korjattu:</span><span class="sxs-lookup"><span data-stu-id="6bebd-127">The following issues have been fixed:</span></span>

- <span data-ttu-id="6bebd-128">Kun hinnasto kopioidaan, hintoja ei päivitetä.</span><span class="sxs-lookup"><span data-stu-id="6bebd-128">When a price list is copied, prices aren't updated.</span></span>
- <span data-ttu-id="6bebd-129">Kun tarjous suljetaan voitettuna, kustannuserittelyllä on alkuperän arvo.</span><span class="sxs-lookup"><span data-stu-id="6bebd-129">Closing a quote as won fails when the cost detail has a value for origin.</span></span>
- <span data-ttu-id="6bebd-130">**Projektitehtävä**-entiteetissä **Arvioitu kustannus** on nimetty uudelleen **Suunnitelluksi kustannukseksi (perusvaluutta)** .</span><span class="sxs-lookup"><span data-stu-id="6bebd-130">On the **Project Task** entity, **Estimated Cost** has been renamed to **Planned Cost (Base)**.</span></span>
- <span data-ttu-id="6bebd-131">Tyhjäarvoinen poikkeus luodaan, kun laskuja luodaan tai poistetaan.</span><span class="sxs-lookup"><span data-stu-id="6bebd-131">A null reference exception is generated when invoices are created or deleted.</span></span>
