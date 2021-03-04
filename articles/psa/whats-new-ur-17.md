---
title: Uutuudet ja muutokset Project Service Automation -päivitysjulkaisussa 17, V3
description: Tässä aiheessa on luettelo ominaisuuksista ja korjauksista, jotka ovat käytettävissä Project Service Automation -päivitysjulkaisussa 17, V3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 03/06/2020
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
ms.openlocfilehash: f9fb941a95b0610dc546b1c12a87aa7faef4d676
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/10/2021
ms.locfileid: "5143703"
---
# <a name="project-service-automation-update-release-17-v3"></a><span data-ttu-id="8a9fa-103">Project Service Automation -päivitysjulkaisu 17, V3</span><span class="sxs-lookup"><span data-stu-id="8a9fa-103">Project Service Automation Update Release 17, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="8a9fa-104">Meillä on ilo julkistaa Dynamics 365:n Project Service Automation-sovelluksen uusin päivitys.</span><span class="sxs-lookup"><span data-stu-id="8a9fa-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="8a9fa-105">Tämä julkaisu sisältää joitakin tärkeitä parannuksia laatuun, tehokkuuteen ja käytettävyyteen.</span><span class="sxs-lookup"><span data-stu-id="8a9fa-105">This release includes some important improvements to quality, performance, and usability.</span></span>  <span data-ttu-id="8a9fa-106">Tämä versio on yhteensopiva Dynamics 365 -versioiden 9.x kanssa.</span><span class="sxs-lookup"><span data-stu-id="8a9fa-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="8a9fa-107">Jos haluat päivittää tämän julkaisun, avaa Dynamics 365 online -hallintakeskuksen Ratkaisut-sivu ja asenna päivitys.</span><span class="sxs-lookup"><span data-stu-id="8a9fa-107">To update to this release, visit the Admin Center for Dynamics 365 online, solutions page to install the update.</span></span> <span data-ttu-id="8a9fa-108">Lisätietoja: [Ensisijaisen ratkaisun asentaminen, päivittäminen tai poistaminen](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="8a9fa-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="8a9fa-109">Tässä aiheessa on luettelo ominaisuuksista ja korjauksista, jotka ovat uusia tai muuttuneita PSA V3 -päivitysjulkaisussa 17.</span><span class="sxs-lookup"><span data-stu-id="8a9fa-109">This topic lists the features and fixes that are new or changed for PSA V3, Update Release 17.</span></span> <span data-ttu-id="8a9fa-110">Tällä versiolla on koontinumero V3.10.6.34 ja se on ollut yleisesti saatavilla itsepalvelupäivityksenä maaliskuusta 2020 lähtien.</span><span class="sxs-lookup"><span data-stu-id="8a9fa-110">This version has a build number of V3.10.6.34 and is generally available through a self-update in March 2020.</span></span>


## <a name="update-release-17"></a><span data-ttu-id="8a9fa-111">Päivitysjulkaisu 17</span><span class="sxs-lookup"><span data-stu-id="8a9fa-111">Update Release 17</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="8a9fa-112">Ohjelmistovirheiden korjaukset</span><span class="sxs-lookup"><span data-stu-id="8a9fa-112">Bug fixes</span></span>

<span data-ttu-id="8a9fa-113">**Yleiset**</span><span class="sxs-lookup"><span data-stu-id="8a9fa-113">**General**</span></span>

- <span data-ttu-id="8a9fa-114">Korjattu: Päivitä Project Service Automation vaatiaksesi Team Member -käyttöoikeuksien noudattamista (projektiresurssikeskus sisältää Team Member Service -suunnitelman metatiedot 3.x)</span><span class="sxs-lookup"><span data-stu-id="8a9fa-114">Fixed: Update Project Service Automation to enforce Team Member licenses (Project Resource Hub will include Team Member Service plan metadata 3.x)</span></span>
 
<span data-ttu-id="8a9fa-115">**Aika ja kulu**</span><span class="sxs-lookup"><span data-stu-id="8a9fa-115">**Time and Expense**</span></span>

- <span data-ttu-id="8a9fa-116">Korjattu: Kuluarviota ei voi muuttaa ei-nolla-hinnasta nollaan (0).</span><span class="sxs-lookup"><span data-stu-id="8a9fa-116">Fixed: It is not possible to change an expense estimate from a non-zero price to zero (0).</span></span> <span data-ttu-id="8a9fa-117">Muutos ohitetaan.</span><span class="sxs-lookup"><span data-stu-id="8a9fa-117">The change is ignored.</span></span>

<span data-ttu-id="8a9fa-118">**Projektinhallinta**</span><span class="sxs-lookup"><span data-stu-id="8a9fa-118">**Project Management**</span></span>

- <span data-ttu-id="8a9fa-119">Korjattu: Tiimin jäsenen työnimikkeen nimelle on lisätty null-arvojen tarkistus.</span><span class="sxs-lookup"><span data-stu-id="8a9fa-119">Fixed: A check for null values has been added on a team member's position name.</span></span>
- <span data-ttu-id="8a9fa-120">Korjattu: **msdyn_resourceassignment**-entiteetin **msdyn_userresourceid**-kenttä on merkitty vanhentuneeksi.</span><span class="sxs-lookup"><span data-stu-id="8a9fa-120">Fixed: **msdyn_userresourceid** field on the **msdyn_resourceassignment** entity has been deprecated.</span></span>
- <span data-ttu-id="8a9fa-121">Korjattu: Päivitys versiosta 2.x versioon 3.x käsittelee nyt tehtävien delegoinnin tyhjät töiden jaksottumiset.</span><span class="sxs-lookup"><span data-stu-id="8a9fa-121">Fixed: Upgrade from 2.x to 3.x now handles empty effort contours on task assignments.</span></span>

<span data-ttu-id="8a9fa-122">**Sales**</span><span class="sxs-lookup"><span data-stu-id="8a9fa-122">**Sales**</span></span>

- <span data-ttu-id="8a9fa-123">Korjattu: **Invoice.PreValidateInvoiceUpdate** käsittelee nyt tietueiden omistajien uudelleendelegoinnin oikein.</span><span class="sxs-lookup"><span data-stu-id="8a9fa-123">Fixed: **Invoice.PreValidateInvoiceUpdate** now handles the scenario of reassigning record owners properly.</span></span>
- <span data-ttu-id="8a9fa-124">Korjattu: Kun tapahtuman luokka on **Aika**, **UnitGroup**-arvoa ei voida muokata millekään entiteetille, mukaan lukien **QuoteLineDetails**, **JournalLine**, **InvoiceLineDetail** ja **ContractLineDetails**.</span><span class="sxs-lookup"><span data-stu-id="8a9fa-124">Fixed: When the transaction class is **Time**, **UnitGroup** is non-editable for all entities including, **QuoteLineDetails**, **JournalLine**, **InvoiceLineDetail**, and **ContractLineDetails**.</span></span> <span data-ttu-id="8a9fa-125">**Yksikkö**-arvoa voi kuitenkin muokata, paitsi **JournalLine**- ja **InvoiceLineDetails**-entiteeteille.</span><span class="sxs-lookup"><span data-stu-id="8a9fa-125">However, **Unit** is non-editable only for **JournalLine** and **InvoiceLineDetails**.</span></span>


