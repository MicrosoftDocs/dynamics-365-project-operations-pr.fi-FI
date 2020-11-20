---
title: Luo projekti
description: Luo projekti Project Servicessä
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 8/13/2020
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
ms.openlocfilehash: a1a229641d0694311ecb7019e3915d0e8e6783c3
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/16/2020
ms.locfileid: "4075360"
---
# <a name="create-a-project-project-service"></a><span data-ttu-id="bed08-103">Luo projekti (Project Service)</span><span class="sxs-lookup"><span data-stu-id="bed08-103">Create a project (Project Service)</span></span>

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="bed08-104">Luo projekti käyttämällä [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] -ratkaisun [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] -toimintoja, kun haluat luoda mahdollisuuden, tarjouksen tai sopimuksen projektipohjaisille palveluille.</span><span class="sxs-lookup"><span data-stu-id="bed08-104">Create a project using the [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] capabilities in [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] when you want to create an opportunity, quote, or contract for project-based services.</span></span> <span data-ttu-id="bed08-105">[!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] -toimintojen avulla voit hallita projektia mahdollisuudesta valmistumiseen.</span><span class="sxs-lookup"><span data-stu-id="bed08-105">The [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] capabilities help you manage your project from opportunity through completion.</span></span> <span data-ttu-id="bed08-106">Kun luot projektin, luot myös työrakenteen, joka vaikuttaa tarjouksiin, kustannusarvioihin ja resurssien hallintaan.</span><span class="sxs-lookup"><span data-stu-id="bed08-106">When you create a project, you’ll also create a work breakdown structure, which affects your quotes, cost estimates, and resource management.</span></span>  
  
1.  <span data-ttu-id="bed08-107">Siirry kohtaan **Project Service > Projektit**.</span><span class="sxs-lookup"><span data-stu-id="bed08-107">Go to **Project Service > Projects**.</span></span>  
  
2.  <span data-ttu-id="bed08-108">Valitse **Uusi projekti**.</span><span class="sxs-lookup"><span data-stu-id="bed08-108">Click **New Project**.</span></span>  
  
3.  <span data-ttu-id="bed08-109">**Yhteenveto** alueella kirjoita projektin nimi ja täytä niin monta tietoa kuin voit.</span><span class="sxs-lookup"><span data-stu-id="bed08-109">In the **Summary** area, enter a name for your project, and then fill in as many of the details as you can.</span></span> <span data-ttu-id="bed08-110">Pakolliset kohteet on merkitty punaisella tähdellä (\*).</span><span class="sxs-lookup"><span data-stu-id="bed08-110">Items marked with a red asterisk (\*) are required.</span></span>  
  
4.  <span data-ttu-id="bed08-111">Valitse **Tallenna** ja luo projekti, jotta voit jatkaa muokkaamista.</span><span class="sxs-lookup"><span data-stu-id="bed08-111">Click **Save** to create your project so you can continue editing it.</span></span>  
  
<span data-ttu-id="bed08-112">Seuraavaksi luodaan työrakenne projektin tehtävien, ajoituksen ja tarvittavien projektin resurssien roolien määrittämiseen.</span><span class="sxs-lookup"><span data-stu-id="bed08-112">Next, you’ll create a work breakdown structure for your project to define the tasks, timing, and resource roles needed for the project.</span></span>  

> [!NOTE]
> <span data-ttu-id="bed08-113">Aikataulutettaessa Project Service Automation noudattaa käytettävän **Työaika** -mallin aikavyöhykettä.</span><span class="sxs-lookup"><span data-stu-id="bed08-113">When scheduling, Project Service Automation respects the time zone of the applied **Work Hour** template.</span></span> <span data-ttu-id="bed08-114">Kun tarkastelet aikataulun tehtäviä, tehtävän alkamis- ja päättymispäivät näkyvät kuitenkin käyttäjän aikavyöhykkeellä.</span><span class="sxs-lookup"><span data-stu-id="bed08-114">However, when viewing the schedule tasks, the start and end dates of a task will be displayed in the user's time zone.</span></span> <span data-ttu-id="bed08-115">Tämä koskee muita aikavaiheistettuja näkymiä **Projekti** -lomakkeessa.</span><span class="sxs-lookup"><span data-stu-id="bed08-115">This applies to other time-phased views in the **Project** form.</span></span> <span data-ttu-id="bed08-116">Jos käyttäjän aikavyöhyke ei vastaa projektiin sovellettavan työaikamallin aikavyöhykettä, näkyviin tulee varoitus, jossa ero on selitetty.</span><span class="sxs-lookup"><span data-stu-id="bed08-116">If the user's time zone does not match the time zone of the work hour template applied to the project, a warning which explains the difference will occur.</span></span> 
  
### <a name="see-also"></a><span data-ttu-id="bed08-117">Katso myös</span><span class="sxs-lookup"><span data-stu-id="bed08-117">See Also</span></span>  
 [<span data-ttu-id="bed08-118">Projektipäällikön opas</span><span class="sxs-lookup"><span data-stu-id="bed08-118">Project Manager Guide</span></span>](../psa/project-manager-guide.md)