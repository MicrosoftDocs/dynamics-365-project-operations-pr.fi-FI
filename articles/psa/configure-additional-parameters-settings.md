---
title: Lisäparametrien asetusten määrittäminen
description: Lisäparametrien asetusten määrittäminen Project Servicessä
author: JohnPBurrows
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
ms.openlocfilehash: f4e883e71beacffb6e2b0b56967046c3f38f7d50
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/10/2021
ms.locfileid: "6001107"
---
# <a name="configure-additional-parameter-settings-project-service"></a><span data-ttu-id="00f4d-103">Lisäparametrien asetusten määrittäminen (Project Service)</span><span class="sxs-lookup"><span data-stu-id="00f4d-103">Configure additional parameter settings (Project Service)</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="00f4d-104">Kun olet määrittänyt kohteet edellisiin aiheisiin, sinun on tehtävä muiden projektiparametrien asetukset, joita käytetään projektissa.</span><span class="sxs-lookup"><span data-stu-id="00f4d-104">Once you’ve configured the items in previous topics, you need to set additional project parameters to use for your projects.</span></span> <span data-ttu-id="00f4d-105">Loit [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] -asennuksen yhteydessä parametriasetuksen kaikkien [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] -palvelussa tarvittavien tietueiden luomista varten.</span><span class="sxs-lookup"><span data-stu-id="00f4d-105">When you first installed [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], you created a parameters setting to first create all the records required for [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] to work.</span></span> <span data-ttu-id="00f4d-106">Tämän jälkeen palataan taaksepäin ja määritetään lisäkenttiä tätä asetusta varten.</span><span class="sxs-lookup"><span data-stu-id="00f4d-106">Now it’s time to go back and configure additional fields for these settings.</span></span>  
  
 <span data-ttu-id="00f4d-107">Seuraavat asetukset pitää määrittää:</span><span class="sxs-lookup"><span data-stu-id="00f4d-107">You’ll need to have configured the following settings:</span></span>  
  
-   <span data-ttu-id="00f4d-108">Organisaatioyksikkö</span><span class="sxs-lookup"><span data-stu-id="00f4d-108">Organizational unit</span></span>  
  
-   <span data-ttu-id="00f4d-109">Laskutustiheys</span><span class="sxs-lookup"><span data-stu-id="00f4d-109">Invoice frequency</span></span>  
  
-   <span data-ttu-id="00f4d-110">Työtuntimalli</span><span class="sxs-lookup"><span data-stu-id="00f4d-110">Work hours template</span></span>  
  
-   <span data-ttu-id="00f4d-111">Hinnasto</span><span class="sxs-lookup"><span data-stu-id="00f4d-111">Price list</span></span>  
 
<span data-ttu-id="00f4d-112">Tässä vaiheessa voit myös osoittaa, miten resurssit kohdistetaan:</span><span class="sxs-lookup"><span data-stu-id="00f4d-112">In this step, you’ll also indicate what type of resource allocation you want:</span></span>  
  
- <span data-ttu-id="00f4d-113">**Keskitetty**.</span><span class="sxs-lookup"><span data-stu-id="00f4d-113">**Central**.</span></span> <span data-ttu-id="00f4d-114">Vain resurssipäälliköt voivat kohdistaa resursseja projekteihin.</span><span class="sxs-lookup"><span data-stu-id="00f4d-114">Only resource managers can allocate resources to projects.</span></span>  
  
- <span data-ttu-id="00f4d-115">**Hybridi**.</span><span class="sxs-lookup"><span data-stu-id="00f4d-115">**Hybrid**.</span></span> <span data-ttu-id="00f4d-116">Projektien resursseja voivat kohdistaa resurssipäälliköt, projektipäälliköt ja asiakkuuspäälliköt.</span><span class="sxs-lookup"><span data-stu-id="00f4d-116">Resource managers, project managers, and account managers can allocate resources to projects.</span></span>  
  
 
<span data-ttu-id="00f4d-117">Projektin parametriasetusten tekeminen:</span><span class="sxs-lookup"><span data-stu-id="00f4d-117">To set project parameters:</span></span>  
  
1. <span data-ttu-id="00f4d-118">Siirry kohtaan **Project Service > Parametrit**.</span><span class="sxs-lookup"><span data-stu-id="00f4d-118">Go to **Project Service > Parameters**.</span></span>  
  
2. <span data-ttu-id="00f4d-119">Valitse parametrien asetus, jonka haluat määrittää (sama, jonka loit [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] -asennuksen yhteydessä), tai luo uusi valitsemalla **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="00f4d-119">Click the parameters setting you want to configure (the one you created when you first installed [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]), or click **New** to create a new one.</span></span>  
  
3. <span data-ttu-id="00f4d-120">**Yleinen**-alueessa määritä projektiparametrien asetukset.</span><span class="sxs-lookup"><span data-stu-id="00f4d-120">In the **General** area, set all the options for your project parameters.</span></span>  
  
4. <span data-ttu-id="00f4d-121">**Hinnasto**-alueessa valitse **+** ja lisää hinnasto, valitse hinnasto avattavasta **Projektin parametrin hinnasto** -luettelosta ja valitse sitten **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="00f4d-121">In the **Price List** area, click **+** to add a price list, select a price list in the **Project Parameter Price List** drop-down list, and then click **Save**.</span></span>  
  
5. <span data-ttu-id="00f4d-122">Napsauta näytön oikeassa alakulmassa **Tallenna**-painiketta.</span><span class="sxs-lookup"><span data-stu-id="00f4d-122">Click the **Save** button in the bottom right corner of the screen.</span></span>  

> [!NOTE]
> <span data-ttu-id="00f4d-123">Projektiparametritietue on säilytettävä, jotta Project Service toimisi oikein.</span><span class="sxs-lookup"><span data-stu-id="00f4d-123">The project parameter record must be maintained for Project Service to function correcly.</span></span> <span data-ttu-id="00f4d-124">Tätä tietuetta ei pitäisi poistaa.</span><span class="sxs-lookup"><span data-stu-id="00f4d-124">This record should not be deleted.</span></span>

### <a name="see-also"></a><span data-ttu-id="00f4d-125">Katso myös</span><span class="sxs-lookup"><span data-stu-id="00f4d-125">See Also</span></span>  
 [<span data-ttu-id="00f4d-126">Resurssien määrittäminen</span><span class="sxs-lookup"><span data-stu-id="00f4d-126">Set up resources</span></span>](../psa/set-up-resources.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]