---
title: Uutuudet ja muutokset Project Service Automation -päivitysjulkaisussa 29.5, Hotfix, V3
description: Tässä aiheessa on luettelo ominaisuuksista ja korjauksista Project Service Automationin Päivitysjulkaisussa 29.5 Hotfix, V3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 03/26/2021
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
ms.openlocfilehash: 99ba353236ad88b8bdff2c1b25e1247fa4bf3455
ms.sourcegitcommit: 9ebf7dd501898053bfa824f732adabf3f273613b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/26/2021
ms.locfileid: "5715661"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-295-v3"></a><span data-ttu-id="03826-103">Uutuudet ja muutokset Project Service Automation -päivitysjulkaisussa 29.5, V3</span><span class="sxs-lookup"><span data-stu-id="03826-103">What's new or changed in Project Service Automation Update Release 29.5, V3</span></span>

<span data-ttu-id="03826-104">Meillä on ilo julkistaa Dynamics 365:n Project Service Automation-sovelluksen uusin päivitys.</span><span class="sxs-lookup"><span data-stu-id="03826-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="03826-105">Tämä julkaisu sisältää joitakin tärkeitä parannuksia laatuun, tehokkuuteen ja käytettävyyteen.</span><span class="sxs-lookup"><span data-stu-id="03826-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="03826-106">Tämä versio on yhteensopiva Dynamics 365 -versioiden 9.x kanssa.</span><span class="sxs-lookup"><span data-stu-id="03826-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="03826-107">Jos haluat päivittää tämän julkaisun, avaa Dynamics 365 online -hallintakeskuksen Ratkaisut-sivu ja asenna päivitys.</span><span class="sxs-lookup"><span data-stu-id="03826-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="03826-108">Lisätietoja: [Ensisijaisen ratkaisun asentaminen, päivittäminen tai poistaminen](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="03826-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="03826-109">Tässä aiheessa on luettelo ominaisuuksista ja korjauksista, jotka ovat uusia tai muuttuneita Project Service Automation V3 -päivitysjulkaisussa 29.5.</span><span class="sxs-lookup"><span data-stu-id="03826-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 29.5.</span></span> <span data-ttu-id="03826-110">Tällä versiolla on koontinumero V3.10.47.150 ja se on ollut yleisesti saatavilla itsepalvelupäivityksenä tammikuusta 2021 lähtien.</span><span class="sxs-lookup"><span data-stu-id="03826-110">This version has a build number of V3.10.47.150 and is generally available through a self-update in January 2021.</span></span>

## <a name="update-release-295"></a><span data-ttu-id="03826-111">Päivitysjulkaisu 29.5</span><span class="sxs-lookup"><span data-stu-id="03826-111">Update Release 29.5</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="03826-112">Ohjelmavirhekorjauksia</span><span class="sxs-lookup"><span data-stu-id="03826-112">Bug fixes</span></span>


<span data-ttu-id="03826-113">**Myynti**</span><span class="sxs-lookup"><span data-stu-id="03826-113">**Sales**</span></span>

<span data-ttu-id="03826-114">Seuraavat ongelmat on korjattu:</span><span class="sxs-lookup"><span data-stu-id="03826-114">The following issues have been fixed:</span></span>

- <span data-ttu-id="03826-115">Mahdollinen tyhjäarvoisen viitteen sisältävä poikkeus tapahtuu kohteessa **ContractLineMapHelper.UpdateContractLineDetailPriceListReference**, kun tarjous suljetaan voitettuna eikä tarjouksella ole hinnastoa.</span><span class="sxs-lookup"><span data-stu-id="03826-115">A possible null reference exception occurs in **ContractLineMapHelper.UpdateContractLineDetailPriceListReference** when you close a quote as won and the quote has no price list.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
