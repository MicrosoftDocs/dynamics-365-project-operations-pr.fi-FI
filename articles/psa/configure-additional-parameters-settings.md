---
title: Lisäparametrien asetusten määrittäminen
description: Lisäparametrien asetusten määrittäminen Project Servicessä
author: JohnPBurrows
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
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
ms.openlocfilehash: 5ce7ffd635b10689c8295d9349966450f11282d1
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/28/2020
ms.locfileid: "4129359"
---
# <a name="configure-additional-parameter-settings-project-service"></a><span data-ttu-id="0e839-103">Lisäparametrien asetusten määrittäminen (Project Service)</span><span class="sxs-lookup"><span data-stu-id="0e839-103">Configure additional parameter settings (Project Service)</span></span>

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="0e839-104">Kun olet määrittänyt kohteet edellisiin aiheisiin, sinun on tehtävä muiden projektiparametrien asetukset, joita käytetään projektissa.</span><span class="sxs-lookup"><span data-stu-id="0e839-104">Once you’ve configured the items in previous topics, you need to set additional project parameters to use for your projects.</span></span> <span data-ttu-id="0e839-105">Loit [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] -asennuksen yhteydessä parametriasetuksen kaikkien [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] -palvelussa tarvittavien tietueiden luomista varten.</span><span class="sxs-lookup"><span data-stu-id="0e839-105">When you first installed [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], you created a parameters setting to first create all the records required for [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] to work.</span></span> <span data-ttu-id="0e839-106">Tämän jälkeen palataan taaksepäin ja määritetään lisäkenttiä tätä asetusta varten.</span><span class="sxs-lookup"><span data-stu-id="0e839-106">Now it’s time to go back and configure additional fields for these settings.</span></span>  
  
 <span data-ttu-id="0e839-107">Seuraavat asetukset pitää määrittää:</span><span class="sxs-lookup"><span data-stu-id="0e839-107">You’ll need to have configured the following settings:</span></span>  
  
-   <span data-ttu-id="0e839-108">Organisaatioyksikkö</span><span class="sxs-lookup"><span data-stu-id="0e839-108">Organizational unit</span></span>  
  
-   <span data-ttu-id="0e839-109">Laskutustiheys</span><span class="sxs-lookup"><span data-stu-id="0e839-109">Invoice frequency</span></span>  
  
-   <span data-ttu-id="0e839-110">Työtuntimalli</span><span class="sxs-lookup"><span data-stu-id="0e839-110">Work hours template</span></span>  
  
-   <span data-ttu-id="0e839-111">Hinnasto</span><span class="sxs-lookup"><span data-stu-id="0e839-111">Price list</span></span>  
 
<span data-ttu-id="0e839-112">Tässä vaiheessa voit myös osoittaa, miten resurssit kohdistetaan:</span><span class="sxs-lookup"><span data-stu-id="0e839-112">In this step, you’ll also indicate what type of resource allocation you want:</span></span>  
  
- <span data-ttu-id="0e839-113">**Keskitetty**.</span><span class="sxs-lookup"><span data-stu-id="0e839-113">**Central**.</span></span> <span data-ttu-id="0e839-114">Vain resurssipäälliköt voivat kohdistaa resursseja projekteihin.</span><span class="sxs-lookup"><span data-stu-id="0e839-114">Only resource managers can allocate resources to projects.</span></span>  
  
- <span data-ttu-id="0e839-115">**Hybridi**.</span><span class="sxs-lookup"><span data-stu-id="0e839-115">**Hybrid**.</span></span> <span data-ttu-id="0e839-116">Projektien resursseja voivat kohdistaa resurssipäälliköt, projektipäälliköt ja asiakkuuspäälliköt.</span><span class="sxs-lookup"><span data-stu-id="0e839-116">Resource managers, project managers, and account managers can allocate resources to projects.</span></span>  
  
 
<span data-ttu-id="0e839-117">Projektin parametriasetusten tekeminen:</span><span class="sxs-lookup"><span data-stu-id="0e839-117">To set project parameters:</span></span>  
  
1. <span data-ttu-id="0e839-118">Siirry kohtaan **Project Service > Parametrit**.</span><span class="sxs-lookup"><span data-stu-id="0e839-118">Go to **Project Service > Parameters**.</span></span>  
  
2. <span data-ttu-id="0e839-119">Valitse parametrien asetus, jonka haluat määrittää (sama, jonka loit [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] -asennuksen yhteydessä), tai luo uusi valitsemalla **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="0e839-119">Click the parameters setting you want to configure (the one you created when you first installed [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]), or click **New** to create a new one.</span></span>  
  
3. <span data-ttu-id="0e839-120">**Yleinen**-alueessa määritä projektiparametrien asetukset.</span><span class="sxs-lookup"><span data-stu-id="0e839-120">In the **General** area, set all the options for your project parameters.</span></span>  
  
4. <span data-ttu-id="0e839-121">**Hinnasto**-alueessa valitse **+** ja lisää hinnasto, valitse hinnasto avattavasta **Projektin parametrin hinnasto** -luettelosta ja valitse sitten **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="0e839-121">In the **Price List** area, click **+** to add a price list, select a price list in the **Project Parameter Price List** drop-down list, and then click **Save**.</span></span>  
  
5. <span data-ttu-id="0e839-122">Napsauta näytön oikeassa alakulmassa **Tallenna**-painiketta.</span><span class="sxs-lookup"><span data-stu-id="0e839-122">Click the **Save** button in the bottom right corner of the screen.</span></span>  

> [!NOTE]
> <span data-ttu-id="0e839-123">Projektiparametritietue on säilytettävä, jotta Project Service toimisi oikein.</span><span class="sxs-lookup"><span data-stu-id="0e839-123">The project parameter record must be maintained for Project Service to function correcly.</span></span> <span data-ttu-id="0e839-124">Tätä tietuetta ei pitäisi poistaa.</span><span class="sxs-lookup"><span data-stu-id="0e839-124">This record should not be deleted.</span></span>

### <a name="see-also"></a><span data-ttu-id="0e839-125">Katso myös</span><span class="sxs-lookup"><span data-stu-id="0e839-125">See Also</span></span>  
 [<span data-ttu-id="0e839-126">Resurssien määrittäminen</span><span class="sxs-lookup"><span data-stu-id="0e839-126">Set up resources</span></span>](../psa/set-up-resources.md)