---
title: Uutuudet ja muutokset Project Service Automation -päivitysjulkaisussa 28, V3
description: Tässä aiheessa on luettelo ominaisuuksista ja korjauksista, jotka ovat käytettävissä Project Service Automation -päivitysjulkaisussa 28, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 01/26/2021
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
ms.openlocfilehash: b06a5ee6d0e2da76801a36701f38f1885d6c7562
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/10/2021
ms.locfileid: "6010512"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-28-v3"></a><span data-ttu-id="cede6-103">Uutuudet ja muutokset Project Service Automation -päivitysjulkaisussa 28, V3</span><span class="sxs-lookup"><span data-stu-id="cede6-103">What's new or changed in Project Service Automation Update Release 28, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="cede6-104">Meillä on ilo julkistaa Dynamics 365:n Project Service Automation-sovelluksen uusin päivitys.</span><span class="sxs-lookup"><span data-stu-id="cede6-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="cede6-105">Tämä julkaisu sisältää joitakin tärkeitä parannuksia laatuun, tehokkuuteen ja käytettävyyteen.</span><span class="sxs-lookup"><span data-stu-id="cede6-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="cede6-106">Tämä versio on yhteensopiva Dynamics 365 -versioiden 9.x kanssa.</span><span class="sxs-lookup"><span data-stu-id="cede6-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="cede6-107">Jos haluat päivittää tämän julkaisun, avaa Dynamics 365 online -hallintakeskuksen Ratkaisut-sivu ja asenna päivitys.</span><span class="sxs-lookup"><span data-stu-id="cede6-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="cede6-108">Lisätietoja: [Ensisijaisen ratkaisun asentaminen, päivittäminen tai poistaminen](/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="cede6-108">For more information, see [Install, update, or remove a preferred solution](/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="cede6-109">Tässä ohjeaiheessa on luettelo Project Service Automation V3, päivitysversion 28 uusista tai muuttuneista ominaisuuksista ja korjauksista. Tämän version koontiversion numero on 3.10.46.32 ja se on yleisesti saatavana omana päivityksenä tammikuussa 2021.</span><span class="sxs-lookup"><span data-stu-id="cede6-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 28 This version has a build number of V3.10.46.32 and is generally available through a self-update in January 2021.</span></span>

## <a name="update-release-28"></a><span data-ttu-id="cede6-110">Päivitysjulkaisu 28</span><span class="sxs-lookup"><span data-stu-id="cede6-110">Update Release 28</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="cede6-111">Ohjelmavirhekorjauksia</span><span class="sxs-lookup"><span data-stu-id="cede6-111">Bug fixes</span></span>

<span data-ttu-id="cede6-112">**Aika ja kulu**</span><span class="sxs-lookup"><span data-stu-id="cede6-112">**Time and Expense**</span></span>

<span data-ttu-id="cede6-113">Seuraavat ongelmat on korjattu:</span><span class="sxs-lookup"><span data-stu-id="cede6-113">The following issues have been fixed:</span></span>

- <span data-ttu-id="cede6-114">Käyttäjät voivat **joukkomuokkauksen** avulla päivittää hyväksyttyjä ja lähetettyjä aikamerkintöjä.</span><span class="sxs-lookup"><span data-stu-id="cede6-114">Users can use **Bulk Edit** to update time entries that have been approved and submitted.</span></span>

<span data-ttu-id="cede6-115">**Projektinhallinta**</span><span class="sxs-lookup"><span data-stu-id="cede6-115">**Project Management**</span></span>

<span data-ttu-id="cede6-116">Seuraavat ongelmat on korjattu:</span><span class="sxs-lookup"><span data-stu-id="cede6-116">The following issues have been fixed:</span></span>

- <span data-ttu-id="cede6-117">Jos tehtävän GUID-tunnus tulkitaan numeroksi, tehtäviä ei voi avata muokattavaksi käyttämällä **Muokkaa tehtävää** -vaihtoehtoa **Työrakenne**-sivun valintanauhassa.</span><span class="sxs-lookup"><span data-stu-id="cede6-117">In cases where the task GUID is interpreted as a number, tasks can't be opened for edit using **Edit Task** in the ribbon on the **Work Breakdown Structure** page.</span></span>

<span data-ttu-id="cede6-118">**Sales**</span><span class="sxs-lookup"><span data-stu-id="cede6-118">**Sales**</span></span>

<span data-ttu-id="cede6-119">Seuraavat ongelmat on korjattu:</span><span class="sxs-lookup"><span data-stu-id="cede6-119">The following issues have been fixed:</span></span>

- <span data-ttu-id="cede6-120">Tyhjäarvon viittauspoikkeus luodaan, kun **GetEstimatesForProject**-laajennus käynnistetään.</span><span class="sxs-lookup"><span data-stu-id="cede6-120">A null reference exception is generated when the **GetEstimatesForProject** plug-in is invoked.</span></span>
- <span data-ttu-id="cede6-121">**Merkitse valmiiksi laskuttamista varten** välitavoiteruudukossa päivittää määritteet vain osittain, lukuun ottamatta **InvoiceStatus**-määritettä, joka päivitetään.</span><span class="sxs-lookup"><span data-stu-id="cede6-121">**Mark ready to invoice** on the milestone grid only partially updates attributes, except for the **InvoiceStatus** attribute, which is updated.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]