---
title: Projektin tilan seuraaminen
description: Projektin tilan seuraaminen Project Servicessä
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
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
ms.openlocfilehash: 70d07c98bd9432712e939445dbf867b96642f5ba
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/16/2020
ms.locfileid: "4075434"
---
# <a name="track-a-projects-status-project-service"></a><span data-ttu-id="0ff1f-103">Seuraa projektin tilaa (Project Service)</span><span class="sxs-lookup"><span data-stu-id="0ff1f-103">Track a project’s status (Project Service)</span></span>

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="0ff1f-104">[!INCLUDE[pn_dyn_365_project_service_auto](../includes/pn-dyn-365-project-service-auto.md)] -palvelussa voit seurata asiakkaan projektin edistymistä.</span><span class="sxs-lookup"><span data-stu-id="0ff1f-104">Use the [!INCLUDE[pn_dyn_365_project_service_auto](../includes/pn-dyn-365-project-service-auto.md)] to track the progress of a client’s project.</span></span>  

<span data-ttu-id="0ff1f-105">Valmistelun edetessä projektin vaiheet päivitetään automaattisesti vastaamaan valmistelun vaihetta:</span><span class="sxs-lookup"><span data-stu-id="0ff1f-105">As the engagement progresses, the project stages update to reflect the stage of the engagement:</span></span>  


|              |                                                                                                                                                                                                                                                                                                  |
|--------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|   <span data-ttu-id="0ff1f-106">**Uusi**</span><span class="sxs-lookup"><span data-stu-id="0ff1f-106">**New**</span></span>    | <span data-ttu-id="0ff1f-107">Kun luot projektin, vaiheeksi on määritetty **uusi**.</span><span class="sxs-lookup"><span data-stu-id="0ff1f-107">When you create a project, the stage is set to **New**.</span></span> <span data-ttu-id="0ff1f-108">Jos projekti on luotu mallista, tässä vaiheessa projektilla voi olla aikataulu, arviot ja ryhmän tiedot.</span><span class="sxs-lookup"><span data-stu-id="0ff1f-108">If you created the project from a template, at this stage the project may have a schedule, estimates, and team data.</span></span> <span data-ttu-id="0ff1f-109">Muussa tapauksessa se on projektin jäsennys, ja sinun on syötettävä manuaalisesti muut projektin osat.</span><span class="sxs-lookup"><span data-stu-id="0ff1f-109">Otherwise, it will be the outline of the project and you need to manually enter the rest of the project components.</span></span> |
|  <span data-ttu-id="0ff1f-110">**Tarjous**</span><span class="sxs-lookup"><span data-stu-id="0ff1f-110">**Quote**</span></span>   |      <span data-ttu-id="0ff1f-111">Kun liität projektin tarjoukseen tai luot sen tarjouksesta, projektivaiheeksi on määritetty **tarjous** , ja arvioitu aloitus- ja päättymispäivät päivitetään myös.</span><span class="sxs-lookup"><span data-stu-id="0ff1f-111">When you associate a project to a quote or create it from a quote, the project stage is set to **Quote** , and the estimated start and end datesare updated as well.</span></span> <span data-ttu-id="0ff1f-112">Kun projekti on on tarjousvaiheessa, tarjouksen yksityiskohdat näkyvät **Myynti** -välilehdellä **Projekti** -sivulla.</span><span class="sxs-lookup"><span data-stu-id="0ff1f-112">When the project is in the quote stage, details on the quote display on the **Sales** tab on the **Project** page.</span></span>      |
|   <span data-ttu-id="0ff1f-113">**Suunnitelma**</span><span class="sxs-lookup"><span data-stu-id="0ff1f-113">**Plan**</span></span>   |                                     <span data-ttu-id="0ff1f-114">Kun projektiin liittyvä tarjous voittaa ja valmistelu etenee sopimusvaiheeseen, projektivaihe päivittää **suunnitelman**.</span><span class="sxs-lookup"><span data-stu-id="0ff1f-114">When you win a quote associated with a project, and when the engagement progresses to the contract stage, the project stage updates to **Plan**.</span></span> <span data-ttu-id="0ff1f-115">Sopimuksen tiedot näkyvät **Myynti** -välilehdellä **Projektin** -sivulla.</span><span class="sxs-lookup"><span data-stu-id="0ff1f-115">Contract details display on the **Sales** tab on the **Project** page.</span></span>                                      |
| <span data-ttu-id="0ff1f-116">**Valmis**</span><span class="sxs-lookup"><span data-stu-id="0ff1f-116">**Complete**</span></span> |                    <span data-ttu-id="0ff1f-117">Kun projektin työ on valmis, voit vaihtaa vaiheeksi **Valmis**.</span><span class="sxs-lookup"><span data-stu-id="0ff1f-117">When the project work is complete, you can flip the stage to **Complete**.</span></span> <span data-ttu-id="0ff1f-118">Kun projektivaiheeksi on muutettu valmis, on selvää, että työ on suoritettu 100-prosenttisesti, mutta projekti pidetään avoinna, jotta odottavat aika- tai kulumerkinnät kirjataan.</span><span class="sxs-lookup"><span data-stu-id="0ff1f-118">When the project stage is set to complete, it’s understood that the work is 100% complete but the project is kept open for any pending time or expense entries to be recorded.</span></span>                     |
|  <span data-ttu-id="0ff1f-119">**Sulje**</span><span class="sxs-lookup"><span data-stu-id="0ff1f-119">**Close**</span></span>   |           <span data-ttu-id="0ff1f-120">Kun kaikki tapahtumat on tallennettu projektiin ja et odota uusia kirjattavaksi, voit manuaalisesti määrittää vaiheeksi **Sulje**.</span><span class="sxs-lookup"><span data-stu-id="0ff1f-120">When all transactions have been recorded on the project and you don't expect any more to be logged, you can manually set the stage to **Close**.</span></span> <span data-ttu-id="0ff1f-121">Kun projektin tilaksi on määritetty **Sulje** , et voi kirjautua enää projektin tapahtumiin ja projektin voi vain lukea.</span><span class="sxs-lookup"><span data-stu-id="0ff1f-121">When the project is set to **Close** , you can’t log any more transactions on the project and the project will be read only.</span></span>           |

## <a name="to-track-a-projects-status"></a><span data-ttu-id="0ff1f-122">Projektin tilan seuraaminen</span><span class="sxs-lookup"><span data-stu-id="0ff1f-122">To track a project’s status</span></span>  

1.  <span data-ttu-id="0ff1f-123">Siirry kohtaan **Project Service > Projektit**.</span><span class="sxs-lookup"><span data-stu-id="0ff1f-123">Go to **Project Service > Projects**.</span></span>  

2.  <span data-ttu-id="0ff1f-124">Napsauta käsiteltävää projektia.</span><span class="sxs-lookup"><span data-stu-id="0ff1f-124">Click the project you want to work on.</span></span>  

3.  <span data-ttu-id="0ff1f-125">Valitse näytön yläosassa olevassa palkissa, projektin nimen vieressä oleva alanuoli ja valitse sitten **Projektin seuranta**.</span><span class="sxs-lookup"><span data-stu-id="0ff1f-125">In the bar across the top of the screen, select the down arrow next to the project name, and then click **Project Tracking**.</span></span>  

4.  <span data-ttu-id="0ff1f-126">Valitse **Työmäärän seuranta** tai **Kustannusten seuranta** tehtäväluettelon yläpuolella olevasta avattavasta luettelosta.</span><span class="sxs-lookup"><span data-stu-id="0ff1f-126">Select **Effort Tracking** or **Cost Tracking** in the drop-down list above the task list.</span></span>  

5.  <span data-ttu-id="0ff1f-127">Voit muokata tehtävää kaksoisnapsauttamalla sitä.</span><span class="sxs-lookup"><span data-stu-id="0ff1f-127">Double-click any task to edit it.</span></span> <span data-ttu-id="0ff1f-128">Voit muuttaa aikaa ja tehtävän edistymistä myös siirtämällä palkkeja tai muuttamalla niiden kokoa Gantt-kaaviossa.</span><span class="sxs-lookup"><span data-stu-id="0ff1f-128">You can also move or resize the bars in the Gantt chart to change the time and progress for a task.</span></span>  

### <a name="see-also"></a><span data-ttu-id="0ff1f-129">Katso myös</span><span class="sxs-lookup"><span data-stu-id="0ff1f-129">See Also</span></span>  
 [<span data-ttu-id="0ff1f-130">Projektipäällikön opas</span><span class="sxs-lookup"><span data-stu-id="0ff1f-130">Project Manager Guide</span></span>](../psa/project-manager-guide.md)
