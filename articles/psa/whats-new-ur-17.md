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
ms.openlocfilehash: c2b27582a401e41da0a9e60c8f2f32dcdd1944c2
ms.sourcegitcommit: 3d78338773929121d17ec3386f6cb67bfb2272cc
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/27/2021
ms.locfileid: "5949225"
---
# <a name="project-service-automation-update-release-17-v3"></a><span data-ttu-id="44f7d-103">Project Service Automation -päivitysjulkaisu 17, V3</span><span class="sxs-lookup"><span data-stu-id="44f7d-103">Project Service Automation Update Release 17, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="44f7d-104">Meillä on ilo julkistaa Dynamics 365:n Project Service Automation-sovelluksen uusin päivitys.</span><span class="sxs-lookup"><span data-stu-id="44f7d-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="44f7d-105">Tämä julkaisu sisältää joitakin tärkeitä parannuksia laatuun, tehokkuuteen ja käytettävyyteen.</span><span class="sxs-lookup"><span data-stu-id="44f7d-105">This release includes some important improvements to quality, performance, and usability.</span></span>  <span data-ttu-id="44f7d-106">Tämä versio on yhteensopiva Dynamics 365 -versioiden 9.x kanssa.</span><span class="sxs-lookup"><span data-stu-id="44f7d-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="44f7d-107">Jos haluat päivittää tämän julkaisun, avaa Dynamics 365 online -hallintakeskuksen Ratkaisut-sivu ja asenna päivitys.</span><span class="sxs-lookup"><span data-stu-id="44f7d-107">To update to this release, visit the Admin Center for Dynamics 365 online, solutions page to install the update.</span></span> <span data-ttu-id="44f7d-108">Lisätietoja: [Ensisijaisen ratkaisun asentaminen, päivittäminen tai poistaminen](/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="44f7d-108">For more information, see [Install, update, or remove a preferred solution](/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="44f7d-109">Tässä aiheessa on luettelo ominaisuuksista ja korjauksista, jotka ovat uusia tai muuttuneita PSA V3 -päivitysjulkaisussa 17.</span><span class="sxs-lookup"><span data-stu-id="44f7d-109">This topic lists the features and fixes that are new or changed for PSA V3, Update Release 17.</span></span> <span data-ttu-id="44f7d-110">Tällä versiolla on koontinumero V3.10.6.34 ja se on ollut yleisesti saatavilla itsepalvelupäivityksenä maaliskuusta 2020 lähtien.</span><span class="sxs-lookup"><span data-stu-id="44f7d-110">This version has a build number of V3.10.6.34 and is generally available through a self-update in March 2020.</span></span>


## <a name="update-release-17"></a><span data-ttu-id="44f7d-111">Päivitysjulkaisu 17</span><span class="sxs-lookup"><span data-stu-id="44f7d-111">Update Release 17</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="44f7d-112">Ohjelmistovirheiden korjaukset</span><span class="sxs-lookup"><span data-stu-id="44f7d-112">Bug fixes</span></span>

<span data-ttu-id="44f7d-113">**Yleiset**</span><span class="sxs-lookup"><span data-stu-id="44f7d-113">**General**</span></span>

- <span data-ttu-id="44f7d-114">Korjattu: Päivitä Project Service Automation vaatiaksesi Team Member -käyttöoikeuksien noudattamista (projektiresurssikeskus sisältää Team Member Service -suunnitelman metatiedot 3.x)</span><span class="sxs-lookup"><span data-stu-id="44f7d-114">Fixed: Update Project Service Automation to enforce Team Member licenses (Project Resource Hub will include Team Member Service plan metadata 3.x)</span></span>
 
<span data-ttu-id="44f7d-115">**Aika ja kulu**</span><span class="sxs-lookup"><span data-stu-id="44f7d-115">**Time and Expense**</span></span>

- <span data-ttu-id="44f7d-116">Korjattu: Kuluarviota ei voi muuttaa ei-nolla-hinnasta nollaan (0).</span><span class="sxs-lookup"><span data-stu-id="44f7d-116">Fixed: It is not possible to change an expense estimate from a non-zero price to zero (0).</span></span> <span data-ttu-id="44f7d-117">Muutos ohitetaan.</span><span class="sxs-lookup"><span data-stu-id="44f7d-117">The change is ignored.</span></span>

<span data-ttu-id="44f7d-118">**Projektinhallinta**</span><span class="sxs-lookup"><span data-stu-id="44f7d-118">**Project Management**</span></span>

- <span data-ttu-id="44f7d-119">Korjattu: Tiimin jäsenen työnimikkeen nimelle on lisätty null-arvojen tarkistus.</span><span class="sxs-lookup"><span data-stu-id="44f7d-119">Fixed: A check for null values has been added on a team member's position name.</span></span>
- <span data-ttu-id="44f7d-120">Korjattu: **msdyn_resourceassignment**-entiteetin **msdyn_userresourceid**-kenttä on merkitty vanhentuneeksi.</span><span class="sxs-lookup"><span data-stu-id="44f7d-120">Fixed: **msdyn_userresourceid** field on the **msdyn_resourceassignment** entity has been deprecated.</span></span>
- <span data-ttu-id="44f7d-121">Korjattu: Päivitys versiosta 2.x versioon 3.x käsittelee nyt tehtävien delegoinnin tyhjät töiden jaksottumiset.</span><span class="sxs-lookup"><span data-stu-id="44f7d-121">Fixed: Upgrade from 2.x to 3.x now handles empty effort contours on task assignments.</span></span>

<span data-ttu-id="44f7d-122">**Sales**</span><span class="sxs-lookup"><span data-stu-id="44f7d-122">**Sales**</span></span>

- <span data-ttu-id="44f7d-123">Korjattu: **Invoice.PreValidateInvoiceUpdate** käsittelee nyt tietueiden omistajien uudelleendelegoinnin oikein.</span><span class="sxs-lookup"><span data-stu-id="44f7d-123">Fixed: **Invoice.PreValidateInvoiceUpdate** now handles the scenario of reassigning record owners properly.</span></span>
- <span data-ttu-id="44f7d-124">Korjattu: Kun tapahtuman luokka on **Aika**, **UnitGroup**-arvoa ei voida muokata millekään entiteetille, mukaan lukien **QuoteLineDetails**, **JournalLine**, **InvoiceLineDetail** ja **ContractLineDetails**.</span><span class="sxs-lookup"><span data-stu-id="44f7d-124">Fixed: When the transaction class is **Time**, **UnitGroup** is non-editable for all entities including, **QuoteLineDetails**, **JournalLine**, **InvoiceLineDetail**, and **ContractLineDetails**.</span></span> <span data-ttu-id="44f7d-125">**Yksikkö**-arvoa voi kuitenkin muokata, paitsi **JournalLine**- ja **InvoiceLineDetails**-entiteeteille.</span><span class="sxs-lookup"><span data-stu-id="44f7d-125">However, **Unit** is non-editable only for **JournalLine** and **InvoiceLineDetails**.</span></span>




[!INCLUDE[footer-include](../includes/footer-banner.md)]