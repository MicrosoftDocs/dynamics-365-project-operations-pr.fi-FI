---
title: Yleisten varattavissa olevien resurssien kohdentaminen tehtävälle ja projektiryhmälle
description: Tässä aiheessa on tietoja yleisten resurssien varaamisesta tehtäville ja projektiryhmille.
author: JohnPBurrows
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 12/11/2018
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
ms.openlocfilehash: 5b4c47513b96310745fd2cdb296988a57df0e966
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5291390"
---
# <a name="assign-generic-bookable-resources-to-a-task-and-generate-resource-requirements"></a><span data-ttu-id="44e20-103">Yleisten varattavissa olevien resurssien kohdennus tehtävälle ja resurssitarpeiden luominen</span><span class="sxs-lookup"><span data-stu-id="44e20-103">Assign generic bookable resources to a task and generate resource requirements</span></span> 

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="44e20-104">Nimettyjen tai todellisten resurssien projektillesi varaamisen ja kohdentamisen lisäksi voit kohdentaa yleisiä resursseja projektitehtäville.</span><span class="sxs-lookup"><span data-stu-id="44e20-104">In addition to booking and assigning named or real resources to your project, you can assign generic resources to project tasks.</span></span> <span data-ttu-id="44e20-105">Tämä resurssit voivat toimia nimettyjen resurssien paikkamerkkeinä, kunnes olet valmis täyttämään projektisi nimetyillä resursseilla.</span><span class="sxs-lookup"><span data-stu-id="44e20-105">These resources can serve as placeholders for named resources until you are ready to staff your project with named resources.</span></span> 

1. <span data-ttu-id="44e20-106">Avaa Project Service Automationissa (PSA:ssa) **Projekti**-sivu ja kirjoita yleisen resurssin toimen nimi **Aikataulut**-välilehden **Resurssi**-soluun.</span><span class="sxs-lookup"><span data-stu-id="44e20-106">In Project Service Automation (PSA), open the **Project** page and on the **Schedule** tab, enter the position name of the generic resource in the **Resource** cell of the schedule.</span></span> <span data-ttu-id="44e20-107">Voit myös valita solun **Resurssi**-solun avataksesi resurssinvalitsimen ja kirjoittaa nimen yleiselle resurssille, jonka haluat luoda.</span><span class="sxs-lookup"><span data-stu-id="44e20-107">Or, click the **Resource** icon in the cell to open the resource picker and then enter the name of the generic resource that you want to create.</span></span>

![Yleisen ryhmän jäsenen luominen ja kohdennus](media/RM-how-to-9.png)

<span data-ttu-id="44e20-109">Näkyviin tulee **Pikaluonti: projektiryhmän jäsen** -paneeli.</span><span class="sxs-lookup"><span data-stu-id="44e20-109">This will open the **Quick Create: Project Team Member** panel.</span></span> 

2. <span data-ttu-id="44e20-110">Kirjoita yleisen ryhmän jäsenen rooli ja napsauta **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="44e20-110">Enter the role and organization unit of the generic resource team member and then click **Save**.</span></span>

![Yleisen ryhmän jäsenen pikaluonti](media/RM-how-to-10.png)

3. <span data-ttu-id="44e20-112">Kun olet luonut uuden yleisen ryhmän jäsenen, se kohdennetaan tehtävälle.</span><span class="sxs-lookup"><span data-stu-id="44e20-112">After you have created the new generic resource team member, it is assigned to the task.</span></span> <span data-ttu-id="44e20-113">Voit jatkaa kyseisen yleisen resurssin kohdentamista muille tehtäväaikataulun tehtäville.</span><span class="sxs-lookup"><span data-stu-id="44e20-113">You can continue to assign that generic resource to other tasks in the task schedule.</span></span>

![Yleisten ryhmän jäsenten kohdentaminen tehtäville](media/RM-how-to-11.png)

4. <span data-ttu-id="44e20-115">Kun olet kohdentanut yleisen resurssin, voit luoda resurssitarpeen ja täyttää sen suoralla varaamisella tai lähettämällä resurssipyynnön resurssipäällikölle.</span><span class="sxs-lookup"><span data-stu-id="44e20-115">After you have assigned the generic resource, you can generate a resource requirement and fulfill it by directly booking or submitting a resource request to a resource manager.</span></span>

![Yleisen ryhmän jäsenen tarpeen luominen](media/RM-how-to-12.png)

<span data-ttu-id="44e20-117">Ryhmän jäsenten ruudukossa voit resurssinvalitsimen yllä mainitulla tavalla käyttämisen lisäksi lisätä suoraan yleisiä resursseja.</span><span class="sxs-lookup"><span data-stu-id="44e20-117">On the team member grid, in addition to being able to use the resource picker as mentioned above, you can add generic resources directly.</span></span> <span data-ttu-id="44e20-118">Lisättävillä resurssilla on resurssitarve, joka perustuu **Pikaluonti: projektiryhmän jäsen** -paneelissa määritettyihin alkamis- ja päättymispäiviin ja kohdennustapaan.</span><span class="sxs-lookup"><span data-stu-id="44e20-118">The resources are added with a resource requirement that is based on the start/end dates and allocation method specified in the **Quick Create: Project Team Member** panel.</span></span>

<span data-ttu-id="44e20-119">Voit nähdä eron, jos lisäät yleisen ryhmän jäsenen suoraan ja kohdennat yleiselle resurssille tehtävämäärän, joka ylittää niiden tarvittujen tuntien määrän, jotka sen on katettava.</span><span class="sxs-lookup"><span data-stu-id="44e20-119">You can see a difference if you add the generic team member directly and then assign more tasks to the generic resource than they have required hours to cover.</span></span> <span data-ttu-id="44e20-120">Valitse **Luo tarve**, jos haluat luoda tarpeen uudelleen tasapainottaaksesi tarvittavat tunnit ja kohdennukset.</span><span class="sxs-lookup"><span data-stu-id="44e20-120">Click **Generate Requirement** to regenerate the requirement to balance the required hours against assignments.</span></span>

<span data-ttu-id="44e20-121">Voit myös napsauttaa ryhmäruudukon **Resurssitarve**-linkkiä avataksesi tarpeen ja lisätäksesi osaamisalueita, ensisijaisia resursseja jne.</span><span class="sxs-lookup"><span data-stu-id="44e20-121">You can also click the **Resource requirement** link in the team grid to open the requirement and add skills, preferred resources, etc.</span></span>

![Resurssitarve](media/RM-how-to-13.png)



[!INCLUDE[footer-include](../includes/footer-banner.md)]