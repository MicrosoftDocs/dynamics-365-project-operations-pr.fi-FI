---
title: Uutuudet ja muutokset Project Service Automation -päivitysjulkaisussa 17.5, Hotfix, V3
description: Tässä aiheessa on luettelo ominaisuuksista ja korjauksista, jotka ovat käytettävissä Project Service Automation -päivitysjulkaisussa 17.5, V3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 03/13/2020
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
ms.openlocfilehash: b3d58cb4a2f8fea1495d143dd985ad17a5cc4130
ms.sourcegitcommit: 3d78338773929121d17ec3386f6cb67bfb2272cc
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/27/2021
ms.locfileid: "5949270"
---
# <a name="project-service-automation-update-release-175-v3"></a><span data-ttu-id="fc9e1-103">Project Service Automation -päivitysjulkaisu 17.5, V3</span><span class="sxs-lookup"><span data-stu-id="fc9e1-103">Project Service Automation Update Release 17.5, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="fc9e1-104">Meillä on ilo julkistaa Dynamics 365:n Project Service Automation-sovelluksen uusin päivitys.</span><span class="sxs-lookup"><span data-stu-id="fc9e1-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="fc9e1-105">Tämä julkaisu sisältää joitakin tärkeitä parannuksia laatuun, tehokkuuteen ja käytettävyyteen.</span><span class="sxs-lookup"><span data-stu-id="fc9e1-105">This release includes some important improvements to quality, performance, and usability.</span></span>  <span data-ttu-id="fc9e1-106">Tämä versio on yhteensopiva Dynamics 365 -versioiden 9.x kanssa.</span><span class="sxs-lookup"><span data-stu-id="fc9e1-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="fc9e1-107">Jos haluat päivittää tämän julkaisun, avaa Dynamics 365 online -hallintakeskuksen Ratkaisut-sivu ja asenna päivitys.</span><span class="sxs-lookup"><span data-stu-id="fc9e1-107">To update to this release, visit the Admin Center for Dynamics 365 online, solutions page to install the update.</span></span> <span data-ttu-id="fc9e1-108">Lisätietoja: [Ensisijaisen ratkaisun asentaminen, päivittäminen tai poistaminen](/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="fc9e1-108">For more information, see [Install, update, or remove a preferred solution](/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="fc9e1-109">Tässä aiheessa on luettelo ominaisuuksista ja korjauksista, jotka ovat uusia tai muuttuneita V3:n päivitysjulkaisussa 17.5.</span><span class="sxs-lookup"><span data-stu-id="fc9e1-109">This topic lists the features and fixes that are new or changed for V3, Update Release 17.5.</span></span> <span data-ttu-id="fc9e1-110">Tällä versiolla on koontinumero V3.10.7.32 ja se on ollut yleisesti saatavilla itsepalvelupäivityksenä maaliskuusta 2020 lähtien.</span><span class="sxs-lookup"><span data-stu-id="fc9e1-110">This version has a build number of V3.10.7.32 and is generally available through a self-update in March 2020.</span></span>


## <a name="update-release-175"></a><span data-ttu-id="fc9e1-111">Päivitysjulkaisu 17.5</span><span class="sxs-lookup"><span data-stu-id="fc9e1-111">Update Release 17.5</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="fc9e1-112">Ohjelmistovirheiden korjaukset</span><span class="sxs-lookup"><span data-stu-id="fc9e1-112">Bug fixes</span></span>


<span data-ttu-id="fc9e1-113">**Projektinhallinta**</span><span class="sxs-lookup"><span data-stu-id="fc9e1-113">**Project Management**</span></span>

- <span data-ttu-id="fc9e1-114">Korjattu: Korjattiin palvelinpuolen synkronointiongelmat, joita ilmenee pitkäkestoisten tehtävien kanssa.</span><span class="sxs-lookup"><span data-stu-id="fc9e1-114">Fixed: Addressed server-side synchronization issues that occur with long duration tasks.</span></span>
- <span data-ttu-id="fc9e1-115">Korjattu: Korjattiin 24 tunnin työtuntimallit, jotka lisäsivät virheellisesti tehtäviin ylimääräisen päivän.</span><span class="sxs-lookup"><span data-stu-id="fc9e1-115">Fixed: Addressed 24-hour work hour templates inaccurately adding an additional day to tasks.</span></span>
- <span data-ttu-id="fc9e1-116">Korjattu: Korjattiin +13 GMT -työtuntimallit, jotka siirsivät tehtäviä virheellisesti yhden päivän eteenpäin.</span><span class="sxs-lookup"><span data-stu-id="fc9e1-116">Fixed: Addressed +13 GMT work hour templates inaccurately shifting tasks one day ahead.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]