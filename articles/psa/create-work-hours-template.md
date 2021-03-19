---
title: Luo uusi työtuntimalli
description: Työtuntimallin luominen Project Servicessä
author: ruhercul
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
ms.openlocfilehash: 5e859a58f86d8cd98fa429beeeb99cf397a207cf
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5285029"
---
# <a name="create-a-work-hours-template-project-service"></a><span data-ttu-id="f24eb-103">Luo työtuntimalli (Project Service)</span><span class="sxs-lookup"><span data-stu-id="f24eb-103">Create a work hours template (Project Service)</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="f24eb-104">Ennen kuin voit luoda projektiaikataulun, sinun pitää määrittää projektikalenteri, joka määrittää päivittäisen työajan aikatauluun ja mahdolliset palvelukatkot.</span><span class="sxs-lookup"><span data-stu-id="f24eb-104">Before you can create project schedules, you need to set up a project calendar that defines the number of working hours to accommodate per day in the schedule and any business closures.</span></span> <span data-ttu-id="f24eb-105">Tähän käytetään työtuntimallia, joka sisältää tietoja päivittäisistä työtunneista, vapaapäivistä ja muista palvelukatkoista.</span><span class="sxs-lookup"><span data-stu-id="f24eb-105">You do this with a work hours template, which contains details about work hours per day, days off, and any other business closures.</span></span>  
  
 <span data-ttu-id="f24eb-106">Kun luot projektin, voit liittää työmallin projektin kalenteriin jota sovelletaan projektin aikatauluun.</span><span class="sxs-lookup"><span data-stu-id="f24eb-106">When you’re creating a project, you associate a work template to the project calendar to apply the schedule for the project.</span></span>  
  
 <span data-ttu-id="f24eb-107">Voit luoda työtuntimallin kahdella tavalla:</span><span class="sxs-lookup"><span data-stu-id="f24eb-107">There are two ways you can create a work hours template:</span></span>  
  
-   <span data-ttu-id="f24eb-108">Luo työtuntimalli resurssikalenterin perusteella.</span><span class="sxs-lookup"><span data-stu-id="f24eb-108">Create a work hours template based on a resource’s calendar.</span></span>  
  
-   <span data-ttu-id="f24eb-109">Luo uusi työtuntimalli.</span><span class="sxs-lookup"><span data-stu-id="f24eb-109">Create a new work hours template.</span></span>  
  
#### <a name="to-create-a-work-hours-template-based-on-a-resources-calendar"></a><span data-ttu-id="f24eb-110">Työtuntimallin luominen resurssikalenterin perusteella.</span><span class="sxs-lookup"><span data-stu-id="f24eb-110">To create a work hours template based on a resource’s calendar</span></span>  
  
1.  <span data-ttu-id="f24eb-111">Siirry kohtaan **Project Service > Resurssit**.</span><span class="sxs-lookup"><span data-stu-id="f24eb-111">Go to **Project Service > Resources**.</span></span>  
  
2.  <span data-ttu-id="f24eb-112">Valitse haluamasi resurssi, jota käytetään työaikasi pohjana.</span><span class="sxs-lookup"><span data-stu-id="f24eb-112">Select the resource you want to base your work hours on.</span></span>  
  
3.  <span data-ttu-id="f24eb-113">Valitse **Tallenna kalenteri nimellä**, anna työtuntimallille nimi ja valitse sitten **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="f24eb-113">Click **Save Calendar As**, enter a name for the work hours template, and then click **Save**.</span></span>  
  
4.  <span data-ttu-id="f24eb-114">Kun asetusten muutos on valmis, valitse **Tallenna ja sulje**.</span><span class="sxs-lookup"><span data-stu-id="f24eb-114">When you’re done changing options, click **Save and Close**.</span></span>  
  
5.  <span data-ttu-id="f24eb-115">Napsauta näytön oikeassa alakulmassa olevaa **Tallenna**-painiketta.</span><span class="sxs-lookup"><span data-stu-id="f24eb-115">Click the **Save** button at the bottom right corner of the screen.</span></span>  
  
#### <a name="to-create-a-new-work-hours-template"></a><span data-ttu-id="f24eb-116">Uuden työtuntimallin luominen</span><span class="sxs-lookup"><span data-stu-id="f24eb-116">To create a new work hours template</span></span>  
  
1.  <span data-ttu-id="f24eb-117">Siirry kohtaan **Project Service > Työtuntimallit**.</span><span class="sxs-lookup"><span data-stu-id="f24eb-117">Go to **Project Service > Work Hours Templates**.</span></span>  
  
2.  <span data-ttu-id="f24eb-118">Valitse **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="f24eb-118">Click **New**.</span></span>  
  
3.  <span data-ttu-id="f24eb-119">Anna työtuntimallille nimi.</span><span class="sxs-lookup"><span data-stu-id="f24eb-119">Enter a name for the work hours template.</span></span>  
  
4.  <span data-ttu-id="f24eb-120">Valitse resurssi työajan pohjaksi ja valitse sitten **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="f24eb-120">Select a resource to base the work hours on, and then click **Save**.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="f24eb-121">Katso myös</span><span class="sxs-lookup"><span data-stu-id="f24eb-121">See Also</span></span>  
 [<span data-ttu-id="f24eb-122">Resurssien määrittäminen</span><span class="sxs-lookup"><span data-stu-id="f24eb-122">Set up resources</span></span>](../psa/set-up-resources.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]