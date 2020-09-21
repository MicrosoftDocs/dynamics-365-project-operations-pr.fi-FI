---
title: Luo uusi työtuntimalli
description: Työtuntimallin luominen Project Servicessä
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: 1a519487-25f1-4e9d-b739-1c1becf1d649
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 5e7ef4af5f22419cccd8f29ea2a0a0a21a75875a
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/24/2020
ms.locfileid: "3751202"
---
# <a name="create-a-work-hours-template-project-service"></a><span data-ttu-id="f2099-103">Luo työtuntimalli (Project Service)</span><span class="sxs-lookup"><span data-stu-id="f2099-103">Create a work hours template (Project Service)</span></span>

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="f2099-104">Ennen kuin voit luoda projektiaikataulun, sinun pitää määrittää projektikalenteri, joka määrittää päivittäisen työajan aikatauluun ja mahdolliset palvelukatkot.</span><span class="sxs-lookup"><span data-stu-id="f2099-104">Before you can create project schedules, you need to set up a project calendar that defines the number of working hours to accommodate per day in the schedule and any business closures.</span></span> <span data-ttu-id="f2099-105">Tähän käytetään työtuntimallia, joka sisältää tietoja päivittäisistä työtunneista, vapaapäivistä ja muista palvelukatkoista.</span><span class="sxs-lookup"><span data-stu-id="f2099-105">You do this with a work hours template, which contains details about work hours per day, days off, and any other business closures.</span></span>  
  
 <span data-ttu-id="f2099-106">Kun luot projektin, voit liittää työmallin projektin kalenteriin jota sovelletaan projektin aikatauluun.</span><span class="sxs-lookup"><span data-stu-id="f2099-106">When you’re creating a project, you associate a work template to the project calendar to apply the schedule for the project.</span></span>  
  
 <span data-ttu-id="f2099-107">Voit luoda työtuntimallin kahdella tavalla:</span><span class="sxs-lookup"><span data-stu-id="f2099-107">There are two ways you can create a work hours template:</span></span>  
  
-   <span data-ttu-id="f2099-108">Luo työtuntimalli resurssikalenterin perusteella.</span><span class="sxs-lookup"><span data-stu-id="f2099-108">Create a work hours template based on a resource’s calendar.</span></span>  
  
-   <span data-ttu-id="f2099-109">Luo uusi työtuntimalli.</span><span class="sxs-lookup"><span data-stu-id="f2099-109">Create a new work hours template.</span></span>  
  
#### <a name="to-create-a-work-hours-template-based-on-a-resources-calendar"></a><span data-ttu-id="f2099-110">Työtuntimallin luominen resurssikalenterin perusteella.</span><span class="sxs-lookup"><span data-stu-id="f2099-110">To create a work hours template based on a resource’s calendar</span></span>  
  
1.  <span data-ttu-id="f2099-111">Siirry kohtaan **Project Service > Resurssit**.</span><span class="sxs-lookup"><span data-stu-id="f2099-111">Go to **Project Service > Resources**.</span></span>  
  
2.  <span data-ttu-id="f2099-112">Valitse haluamasi resurssi, jota käytetään työaikasi pohjana.</span><span class="sxs-lookup"><span data-stu-id="f2099-112">Select the resource you want to base your work hours on.</span></span>  
  
3.  <span data-ttu-id="f2099-113">Valitse **Tallenna kalenteri nimellä**, anna työtuntimallille nimi ja valitse sitten **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="f2099-113">Click **Save Calendar As**, enter a name for the work hours template, and then click **Save**.</span></span>  
  
4.  <span data-ttu-id="f2099-114">Kun asetusten muutos on valmis, valitse **Tallenna ja sulje**.</span><span class="sxs-lookup"><span data-stu-id="f2099-114">When you’re done changing options, click **Save and Close**.</span></span>  
  
5.  <span data-ttu-id="f2099-115">Napsauta näytön oikeassa alakulmassa olevaa **Tallenna**-painiketta.</span><span class="sxs-lookup"><span data-stu-id="f2099-115">Click the **Save** button at the bottom right corner of the screen.</span></span>  
  
#### <a name="to-create-a-new-work-hours-template"></a><span data-ttu-id="f2099-116">Uuden työtuntimallin luominen</span><span class="sxs-lookup"><span data-stu-id="f2099-116">To create a new work hours template</span></span>  
  
1.  <span data-ttu-id="f2099-117">Siirry kohtaan **Project Service > Työtuntimallit**.</span><span class="sxs-lookup"><span data-stu-id="f2099-117">Go to **Project Service > Work Hours Templates**.</span></span>  
  
2.  <span data-ttu-id="f2099-118">Valitse **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="f2099-118">Click **New**.</span></span>  
  
3.  <span data-ttu-id="f2099-119">Anna työtuntimallille nimi.</span><span class="sxs-lookup"><span data-stu-id="f2099-119">Enter a name for the work hours template.</span></span>  
  
4.  <span data-ttu-id="f2099-120">Valitse resurssi työajan pohjaksi ja valitse sitten **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="f2099-120">Select a resource to base the work hours on, and then click **Save**.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="f2099-121">Katso myös</span><span class="sxs-lookup"><span data-stu-id="f2099-121">See Also</span></span>  
 [<span data-ttu-id="f2099-122">Resurssien määrittäminen</span><span class="sxs-lookup"><span data-stu-id="f2099-122">Set up resources</span></span>](../project-service/set-up-resources.md)
