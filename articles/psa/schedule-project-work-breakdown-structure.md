---
title: Ajoita projekti työrakenteen kanssa
description: Projektin aikatauluttaminen työrakenteen kanssa Project Servicessä
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
ms.openlocfilehash: d77d9f8427f06015d4f4cb9438d7f59ac840b061
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/16/2020
ms.locfileid: "4075530"
---
# <a name="schedule-a-project-with-a-work-breakdown-structure-project-service"></a><span data-ttu-id="7082a-103">Ajoita projekti työrakenteen (Project Service) kanssa</span><span class="sxs-lookup"><span data-stu-id="7082a-103">Schedule a project with a work breakdown structure (Project Service)</span></span>

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="7082a-104">Projektiaikataulu ilmaisee, mikä työ on suoritettava, mitkä resurssit suorittavat työn, ja aikajakson, jossa tämä työ on suoritettava.</span><span class="sxs-lookup"><span data-stu-id="7082a-104">A project schedule communicates what work needs to be performed, which resources will perform the work, and the timeframe in which that work needs to be completed.</span></span> <span data-ttu-id="7082a-105">Projektiaikataulu kuvastaa kaikkea työtä, joka liittyy projektin toimittaminen oikeaan aikaan.</span><span class="sxs-lookup"><span data-stu-id="7082a-105">The project schedule reflects all the work associated with delivering the project on time.</span></span> <span data-ttu-id="7082a-106">Yksi projektin ensimmäisistä vaiheista on projektiaikataulun laatiminen.</span><span class="sxs-lookup"><span data-stu-id="7082a-106">One of the first steps in the initiation phase of the project is to come up with a project schedule.</span></span> <span data-ttu-id="7082a-107">Projektin aikataulun määrittämiseksi on luotava työrakenne.</span><span class="sxs-lookup"><span data-stu-id="7082a-107">To establish a project schedule, you need to create a work breakdown structure.</span></span>  
  
 <span data-ttu-id="7082a-108">Luo projektirakenne ja työrakenne, jonka avulla voit:</span><span class="sxs-lookup"><span data-stu-id="7082a-108">Create a project structure with a work breakdown structure, which helps you:</span></span>  
  
- <span data-ttu-id="7082a-109">jakaa työn hallittaviksi tehtäviksi</span><span class="sxs-lookup"><span data-stu-id="7082a-109">Break down work into manageable tasks</span></span>  
  
- <span data-ttu-id="7082a-110">arvioida tehtävän suorittamiseen tarvittavan ajan</span><span class="sxs-lookup"><span data-stu-id="7082a-110">Estimate the time required to complete a task</span></span>  
  
- <span data-ttu-id="7082a-111">määrittää tehtävän riippuvuudet ja keston</span><span class="sxs-lookup"><span data-stu-id="7082a-111">Set task dependencies and task duration</span></span>  
  
- <span data-ttu-id="7082a-112">määrittää kunkin tehtävän suorittamiseen tarvittavat roolit</span><span class="sxs-lookup"><span data-stu-id="7082a-112">Determine the roles required to complete each task</span></span>  
  
  <span data-ttu-id="7082a-113">Työrakenteen projektiaikataulun ulkoasu on tuttu ja täydennetty vuorovaikutteisella Gantt-kaaviolla.</span><span class="sxs-lookup"><span data-stu-id="7082a-113">The project schedule in the work breakdown structure has a familiar look and feel, complete with an interactive Gantt chart.</span></span>  
  
## <a name="create-a-work-breakdown-structure-for-a-project"></a><span data-ttu-id="7082a-114">Luo projektin työrakenne</span><span class="sxs-lookup"><span data-stu-id="7082a-114">Create a work breakdown structure for a project</span></span>  
 <span data-ttu-id="7082a-115">Luo työrakenne kuvaamaan projektin tehtäväjärjestystä.</span><span class="sxs-lookup"><span data-stu-id="7082a-115">Create a work breakdown structure to represent the sequence of tasks in a project.</span></span> <span data-ttu-id="7082a-116">Työrakenne sisältää tehtävät, kunkin tehtävän vaatimukset ja tuotto- ja kustannustiedot.</span><span class="sxs-lookup"><span data-stu-id="7082a-116">The work breakdown structure includes tasks, requirements for each task, and revenue and cost information.</span></span> <span data-ttu-id="7082a-117">Voit lisätä työrakenteeseen:</span><span class="sxs-lookup"><span data-stu-id="7082a-117">In your work breakdown structure, you can add:</span></span>  
  
-   <span data-ttu-id="7082a-118">Hierarkian tehtävien järjestys</span><span class="sxs-lookup"><span data-stu-id="7082a-118">The sequence of tasks in a hierarchy</span></span>  
  
-   <span data-ttu-id="7082a-119">Muut tehtävät, jos sellaisia on, jotka on suoritettava, ennen kuin tehtävä voidaan aloittaa</span><span class="sxs-lookup"><span data-stu-id="7082a-119">Other tasks, if any, that must be completed before a task can be started</span></span>  
  
-   <span data-ttu-id="7082a-120">Alkamispäivämäärä, lopetuspäivämäärä ja tehtävän kesto</span><span class="sxs-lookup"><span data-stu-id="7082a-120">The starting date, ending date, and duration of a task</span></span>  
  
-   <span data-ttu-id="7082a-121">Tehtävän edellyttämä tuntimäärä</span><span class="sxs-lookup"><span data-stu-id="7082a-121">The number of hours required for a task</span></span>  
  
-   <span data-ttu-id="7082a-122">Mahdollisesti tarvittavat työntekijöiden taidot ja koulutus</span><span class="sxs-lookup"><span data-stu-id="7082a-122">Any required worker skills and education</span></span>  
  
-   <span data-ttu-id="7082a-123">Työntekijät, joille tehtävä on määritetty</span><span class="sxs-lookup"><span data-stu-id="7082a-123">The workers who are assigned to a task</span></span>  
  
-   <span data-ttu-id="7082a-124">Arvioitu tuotto ja kustannukset</span><span class="sxs-lookup"><span data-stu-id="7082a-124">Estimated revenue and costs</span></span>  
  
## <a name="task-types"></a><span data-ttu-id="7082a-125">Tehtävätyypit</span><span class="sxs-lookup"><span data-stu-id="7082a-125">Task types</span></span>  
<span data-ttu-id="7082a-126">Seuraavia tehtävätyyppejä käytetään luotaessa omaa työrakennetta:</span><span class="sxs-lookup"><span data-stu-id="7082a-126">You’ll use the following types of tasks when creating your work breakdown structure:</span></span>  

| | | 
|---------------------------------------|-----------------------------------------------------------------| 
| <span data-ttu-id="7082a-127">**Projektin pääsolmu**</span><span class="sxs-lookup"><span data-stu-id="7082a-127">**Project root node**</span></span> | <span data-ttu-id="7082a-128">Projektin ylätason yhteenvetotehtävä.</span><span class="sxs-lookup"><span data-stu-id="7082a-128">The top-level summary task for the project.</span></span> <span data-ttu-id="7082a-129">Kaikki muut projektitehtävät luodaan sen alaisuuteen.</span><span class="sxs-lookup"><span data-stu-id="7082a-129">All other project tasks are created under it.</span></span> <span data-ttu-id="7082a-130">Projektinimi on juuressa olevan tehtävän nimi.</span><span class="sxs-lookup"><span data-stu-id="7082a-130">The name of the root task is the project name.</span></span> <span data-ttu-id="7082a-131">Pääsolmun työmäärä, päivämäärä ja kesto perustuvat sen alapuolella hierarkiassa oleviin arvoihin.</span><span class="sxs-lookup"><span data-stu-id="7082a-131">The effort, dates, and duration of the root node are based on the values on the hierarchy below it.</span></span> <span data-ttu-id="7082a-132">Et voi muokata pääsolmun ominaisuuksia etkä poistaa pääsolmua.</span><span class="sxs-lookup"><span data-stu-id="7082a-132">You can’t edit root node properties or delete the root node.</span></span> | 
| <span data-ttu-id="7082a-133">**Yhteenvetotehtävät tai säilössä olevat tehtävät**</span><span class="sxs-lookup"><span data-stu-id="7082a-133">**Summary or container tasks**</span></span> | <span data-ttu-id="7082a-134">Yhteenvetotehtävä on tehtävä, jolla on alitehtäviä.</span><span class="sxs-lookup"><span data-stu-id="7082a-134">A summary task is a task that has sub-tasks under it.</span></span> <span data-ttu-id="7082a-135">Yhteenvetotehtävällä ei ole omaa työmäärää eikä kustannuksia.</span><span class="sxs-lookup"><span data-stu-id="7082a-135">A summary task doesn’t have any work effort or cost of its own.</span></span> <span data-ttu-id="7082a-136">Sen työmäärä ja kustannukset ovat kooste alitehtävistä.</span><span class="sxs-lookup"><span data-stu-id="7082a-136">Its work effort and cost are a rollup of its sub-tasks.</span></span> <span data-ttu-id="7082a-137">Voit muuttaa yhteenvetotehtävän nimeä, mutta et voi muuttaa työmäärää, päivämääriä tai kestoa, koska ne lasketaan automaattisesti.</span><span class="sxs-lookup"><span data-stu-id="7082a-137">You can change the name of a summary task, but you can’t change the effort, dates, or duration, because those are automatically calculated.</span></span> <span data-ttu-id="7082a-138">Yhteenvetotehtävän poistaminen poistaa tehtävän ja kaikki sen alitehtävät.</span><span class="sxs-lookup"><span data-stu-id="7082a-138">Deleting a summary task deletes the task and all of its sub-tasks.</span></span>|  
| <span data-ttu-id="7082a-139">**Lehtisolmutehtävät**</span><span class="sxs-lookup"><span data-stu-id="7082a-139">**Leaf node tasks**</span></span> | <span data-ttu-id="7082a-140">Lehtisolmutehtävä edustaa projektin tarkimmin eriteltyä työtä.</span><span class="sxs-lookup"><span data-stu-id="7082a-140">A leaf node task represents the most detailed work on the project.</span></span> <span data-ttu-id="7082a-141">Sillä on arvioitu työmäärä, suunniteltu määrä resursseja, suunnitellut alkamis- ja päättymispäivämäärät ja kesto.</span><span class="sxs-lookup"><span data-stu-id="7082a-141">It has an estimated effort, a planned number of resources, planned start and end dates, and a duration.</span></span>|

  
## <a name="task-hierarchy"></a><span data-ttu-id="7082a-142">Tehtävähierarkia</span><span class="sxs-lookup"><span data-stu-id="7082a-142">Task hierarchy</span></span>  
 <span data-ttu-id="7082a-143">Tehtävähierarkian luomisen vaihtoehdot:</span><span class="sxs-lookup"><span data-stu-id="7082a-143">You have the following options when creating a task hierarchy:</span></span>  
  
- <span data-ttu-id="7082a-144">**Lisää tehtävä**</span><span class="sxs-lookup"><span data-stu-id="7082a-144">**Add task**.</span></span>   <span data-ttu-id="7082a-145">Voit lisätä tehtävän haluamaasi paikkaan tehtävähierarkiassa.</span><span class="sxs-lookup"><span data-stu-id="7082a-145">You can add a task at a position you choose in the task hierarchy.</span></span> <span data-ttu-id="7082a-146">Jos et valitse paikkaa, uusi tehtävä näkyy lopussa.</span><span class="sxs-lookup"><span data-stu-id="7082a-146">If you don’t select a position, your new task appears at the end.</span></span>  
  
- <span data-ttu-id="7082a-147">**Sisennä tehtävä**.</span><span class="sxs-lookup"><span data-stu-id="7082a-147">**Indent task**.</span></span>   <span data-ttu-id="7082a-148">Sisennä tehtävä, josta tulee sen yläpuolella olevan tehtävän alitehtävä.</span><span class="sxs-lookup"><span data-stu-id="7082a-148">Indent a task to make it a child of the task directly above it.</span></span>  
  
- <span data-ttu-id="7082a-149">**Ulonna tehtävä**</span><span class="sxs-lookup"><span data-stu-id="7082a-149">**Outdent task**.</span></span>   <span data-ttu-id="7082a-150">Ulonna tehtävä, jotta se ei enää ole alkuperäisen ylätason tehtävän alitehtävä.</span><span class="sxs-lookup"><span data-stu-id="7082a-150">Outdent a task to make it so it’s no longer a sub-task of its original parent task.</span></span>  
  
- <span data-ttu-id="7082a-151">**Siirrä ylöspäin ja Siirrä alaspäin**.</span><span class="sxs-lookup"><span data-stu-id="7082a-151">**Move up and Move down**.</span></span>   <span data-ttu-id="7082a-152">Siirtää tehtäviä ylös-ja alaspäin päätehtävän hierarkiassa.</span><span class="sxs-lookup"><span data-stu-id="7082a-152">Move tasks up and down in the hierarchy of its parent task.</span></span> <span data-ttu-id="7082a-153">Tehtävän siirtäminen ylös- tai alaspäin ole vaikuta sen työmäärään, kustannuksiin, päivämääriin eikä kestoon.</span><span class="sxs-lookup"><span data-stu-id="7082a-153">Moving a task up or down has no effect on its effort, cost, dates, or duration.</span></span>  
  
## <a name="task-attributes"></a><span data-ttu-id="7082a-154">Tehtävän määritteet</span><span class="sxs-lookup"><span data-stu-id="7082a-154">Task attributes</span></span>  
 <span data-ttu-id="7082a-155">Tehtävän nimi kuvaa keskeneräistä työtä.</span><span class="sxs-lookup"><span data-stu-id="7082a-155">A task’s name describes the work that needs to be completed.</span></span> <span data-ttu-id="7082a-156">Tehtävän määritteiden avulla kuvataan tehtävän aikataulua ja henkilöstötarpeita.</span><span class="sxs-lookup"><span data-stu-id="7082a-156">You use various task attributes to describe the schedule and staffing requirements for the task.</span></span>  
  
### <a name="schedule-attributes"></a><span data-ttu-id="7082a-157">Aikataulun määritteet</span><span class="sxs-lookup"><span data-stu-id="7082a-157">Schedule attributes</span></span>

 - <span data-ttu-id="7082a-158">Määritä tehtävän aikataulu antamalla arvot kohtiin **Työtunnit** , **Resurssien määrä** , **Alkamispäivämäärä** , **Lopetuspäivämäärä** ja **Kesto**.</span><span class="sxs-lookup"><span data-stu-id="7082a-158">Assign values to **Effort hours** , **Number of resources** , **Start date** , **End date** , and **Duration** to determine the schedule for the task.</span></span> 
 - <span data-ttu-id="7082a-159">**Työmäärä** on arvioitu tuntimäärä, jonka tehtävän suorittaminen kestää.</span><span class="sxs-lookup"><span data-stu-id="7082a-159">**Effort** is an estimate of the hours it takes to complete the task.</span></span>
 - <span data-ttu-id="7082a-160">**Resurssien määrä** on arvio, jonka projektipäällikkö asettaa tehtävälle parhaan mahdollisen aikataulun aikaansaamiseksi.</span><span class="sxs-lookup"><span data-stu-id="7082a-160">**Number of resources** is an estimate that the project manager puts in the task to help come up with the best possible schedule.</span></span> 
 - <span data-ttu-id="7082a-161">**Kesto** (päivinä) ilmaisee työpäivien määrän, jonka tehtävän suorittaminen kestää.</span><span class="sxs-lookup"><span data-stu-id="7082a-161">**Duration** (in days) indicates the number of work days it will take to complete the task.</span></span>  
  
### <a name="staffing-attributes"></a><span data-ttu-id="7082a-162">Henkilöstömääritteet</span><span class="sxs-lookup"><span data-stu-id="7082a-162">Staffing attributes</span></span>

 - <span data-ttu-id="7082a-163">**Rooli** , **Resurssin organisaatioyksikkö** , **Resurssien määrä** ja **Resurssit** kuvaavat tehtävän henkilöstötarpeita.</span><span class="sxs-lookup"><span data-stu-id="7082a-163">**Role** , **Resource organizational unit** , **Number of resources** , and **Resources** describe the staffing requirements for the task.</span></span> 
 - <span data-ttu-id="7082a-164">**Rooli** kuvaa tehtävän suorittamiseen tarvittavaa resurssityyppiä.</span><span class="sxs-lookup"><span data-stu-id="7082a-164">**Role** describes the type of resource needed to perform the task.</span></span> 
 - <span data-ttu-id="7082a-165">**Resurssin organisaatioyksikkö** osoittaa organisaatioyksikön, josta henkilöstöresurssit tulee valita kyseiseen tehtävään. Tämä myös vaikuttaa tehtävän kustannus- ja myyntiarvioon, koska tämä kirjataan määritettäessä resurssin yksikkömyyntihintaa.</span><span class="sxs-lookup"><span data-stu-id="7082a-165">**Resource organizational unit** indicates the organizational unit from which resources should be staffed for that task; this also impacts the cost and sales estimate of the task, since this is accounted for when determining the unit sales price for the resource.</span></span> 
 - <span data-ttu-id="7082a-166">**Resurssit** sisältää yleisen resurssin tai nimetyn resurssin, kun sellainen löytyy.</span><span class="sxs-lookup"><span data-stu-id="7082a-166">**Resources** holds a generic resource or a named resource when one is found.</span></span>  
  
## <a name="task-dependencies"></a><span data-ttu-id="7082a-167">Tehtävän riippuvuudet</span><span class="sxs-lookup"><span data-stu-id="7082a-167">Task dependencies</span></span>  
 <span data-ttu-id="7082a-168">Voit luoda edeltäjäsuhteita yhden tai useamman tehtävän välille työrakenteeseen.</span><span class="sxs-lookup"><span data-stu-id="7082a-168">You can create predecessor relationships between one or more tasks in the work breakdown structure.</span></span> <span data-ttu-id="7082a-169">Voit määrittää edeltäjä-kenttään useita arvoja tehtäville ilmaisemaan tehtäviä, joista se on riippuvainen.</span><span class="sxs-lookup"><span data-stu-id="7082a-169">You can set one or more values for the predecessor field on tasks to indicate the tasks that it will be dependent on.</span></span> <span data-ttu-id="7082a-170">Kun määrität tehtävälle edeltäjäarvon, tehtävän voi aloittaa vasta kun edeltäjätehtävät on suoritettu.</span><span class="sxs-lookup"><span data-stu-id="7082a-170">When you assign a predecessor value to a task, the task can only start when all the predecessor tasks have completed.</span></span> <span data-ttu-id="7082a-171">Tämän riippuvuuden määrittäminen tehtävälle johtaa tehtävän suunnitellun alkamispäivän sekä kaikkien sen edeltäjien myöhäisimmän päättymispäivämäärän uudelleenlaskentaan.</span><span class="sxs-lookup"><span data-stu-id="7082a-171">Setting this dependency on a task will result in the recalculation of the planned start date of the task as the latest end of all of its predecessors.</span></span> <span data-ttu-id="7082a-172">Tehtävälle määritetty tehtävätila ei rajoita edeltäjiin liittyviä vaikutuksia aikatauluun.</span><span class="sxs-lookup"><span data-stu-id="7082a-172">Predecessor-related impacts on a schedule are not limited by the task mode defined on the task.</span></span>  
  
## <a name="task-mode"></a><span data-ttu-id="7082a-173">Tehtävätila</span><span class="sxs-lookup"><span data-stu-id="7082a-173">Task mode</span></span>  
 <span data-ttu-id="7082a-174">Tehtävätila on yksi tärkeitä tekijöitä, jotka määrittävät lehtisolmun tehtävien ajoituksen.</span><span class="sxs-lookup"><span data-stu-id="7082a-174">Task mode is one of the important factors that determine scheduling leaf node tasks.</span></span> <span data-ttu-id="7082a-175">Jokaiseen tehtävälle on kaksi tehtävätilaa: automaattinen aikataulutustila ja manuaalisen aikataulutustila.</span><span class="sxs-lookup"><span data-stu-id="7082a-175">There are two task modes for every task: auto scheduling mode and manual scheduling mode.</span></span>  
  
-   <span data-ttu-id="7082a-176">**Automaattinen aikatauluttaminen**</span><span class="sxs-lookup"><span data-stu-id="7082a-176">**Auto scheduling**.</span></span>   <span data-ttu-id="7082a-177">Kun määrität tehtävätilan arvoksi Automaattisesti aikataulutettu, ajoitusmoduuli käyttää ajoitussääntöjä seuraaviin tehtävän määritteisiin määrittäessään tehtävän ajoitusta:</span><span class="sxs-lookup"><span data-stu-id="7082a-177">When you set the task mode to Automatically Scheduled, the task scheduling engine uses the scheduling rules on the following task attributes to determine the schedule for the task:</span></span>  
  
    -   <span data-ttu-id="7082a-178">Edeltäjät</span><span class="sxs-lookup"><span data-stu-id="7082a-178">Predecessors</span></span>  
  
    -   <span data-ttu-id="7082a-179">Työmäärä</span><span class="sxs-lookup"><span data-stu-id="7082a-179">Effort</span></span>  
  
    -   <span data-ttu-id="7082a-180">Resurssien määrä</span><span class="sxs-lookup"><span data-stu-id="7082a-180">Number of resources</span></span>  
  
    -   <span data-ttu-id="7082a-181">aloitus- ja päättymispäivät</span><span class="sxs-lookup"><span data-stu-id="7082a-181">Start and end dates</span></span>  
  
-   <span data-ttu-id="7082a-182">**Omat ajoitussäännöt**.</span><span class="sxs-lookup"><span data-stu-id="7082a-182">**Scheduling rules**.</span></span>   <span data-ttu-id="7082a-183">Lehtisolmutehtävän, jolla ei ole edeltäjiä, aloituspäivämäärän oletusarvo on projektin ajoituksen aloituspäivämäärä.</span><span class="sxs-lookup"><span data-stu-id="7082a-183">The start date of a leaf node task that does not have predecessors defaults to the project’s scheduling start date.</span></span> <span data-ttu-id="7082a-184">Lehtisolmutehtävän kesto vastaa aina alkamis- ja päättymispäivämäärien välisten työpäivien lukumäärää.</span><span class="sxs-lookup"><span data-stu-id="7082a-184">The duration of a leaf node task is always calculated as the number of working days between its start and end dates.</span></span> <span data-ttu-id="7082a-185">Kun tehtävä ajoitetaan automaattisesti, aikataulutusmoduuli noudattaa seuraavia sääntöjä:</span><span class="sxs-lookup"><span data-stu-id="7082a-185">When a task is automatically scheduled, the scheduling engine follows the rules below:</span></span>  
  
    -   <span data-ttu-id="7082a-186">Tehtävän alkamis- ja päättymispäivien on aina oltava projektin ajoituskalenterin mukaisia työpäiviä</span><span class="sxs-lookup"><span data-stu-id="7082a-186">Start and end dates of a task must always be working days according to the project’s scheduling calendar</span></span>  
  
    -   <span data-ttu-id="7082a-187">Tehtävän, jolla on edeltäjiä, aloituspäivämäärän oletusarvo on sen edeltäjien myöhäisin lopetuspäivämäärä.</span><span class="sxs-lookup"><span data-stu-id="7082a-187">The start date of a task that has predecessors defaults to the latest end date of its predecessors</span></span>  
  
    -   <span data-ttu-id="7082a-188">Työmäärä = Henkilömäärä \* kesto \* projektikalenterin normaalin työpäivän tuntimäärä</span><span class="sxs-lookup"><span data-stu-id="7082a-188">Effort = Number of people \* Duration \* hours in a standard work day of the project calendar</span></span>  
  
-   <span data-ttu-id="7082a-189">**Manuaalinen aikataulutus**.</span><span class="sxs-lookup"><span data-stu-id="7082a-189">**Manual scheduling**.</span></span>   <span data-ttu-id="7082a-190">Joissakin tapauksissa haluat ehkä poiketa näistä säännöistä.</span><span class="sxs-lookup"><span data-stu-id="7082a-190">In some cases, you might want to deviate from these rules.</span></span> <span data-ttu-id="7082a-191">Näissä tapauksissa voit määrittää tehtävän tehtävätilan manuaalisesti ajoitettavaksi.</span><span class="sxs-lookup"><span data-stu-id="7082a-191">In these cases, you can set the task mode for the task to be manually scheduled.</span></span> <span data-ttu-id="7082a-192">Tämä estää aikataulutusmoduulia laskemasta muiden ajoitusmääritteiden arvoja.</span><span class="sxs-lookup"><span data-stu-id="7082a-192">This stops the scheduling engine from calculating the values for other scheduling attributes.</span></span> <span data-ttu-id="7082a-193">Tehtävien edeltäjien määrittäminen vaikuttaa aina riippuvaisen tehtävän alkamispäivämäärän.</span><span class="sxs-lookup"><span data-stu-id="7082a-193">Setting predecessors on tasks always impacts the dependent task’s start date.</span></span>  
  
## <a name="create-a-work-breakdown-structure"></a><span data-ttu-id="7082a-194">Luo työrakenne</span><span class="sxs-lookup"><span data-stu-id="7082a-194">Create a work breakdown structure</span></span>  
  
1.  <span data-ttu-id="7082a-195">Siirry kohtaan **Project Service > Projektit**.</span><span class="sxs-lookup"><span data-stu-id="7082a-195">Go to **Project Service > Projects**.</span></span>  
  
2.  <span data-ttu-id="7082a-196">Napsauta käsiteltävää projektia.</span><span class="sxs-lookup"><span data-stu-id="7082a-196">Click the project you want to work on.</span></span>  
  
3.  <span data-ttu-id="7082a-197">Valitse näytön yläosassa olevassa palkissa, projektin nimen vieressä oleva alanuoli ja valitse sitten työrakenne.</span><span class="sxs-lookup"><span data-stu-id="7082a-197">In the bar across the top of the screen, select the down arrow next to the project name, and then click Work breakdown structure.</span></span>  
  
4.  <span data-ttu-id="7082a-198">Lisää tehtävä valitsemalla **Lisää tehtävä**.</span><span class="sxs-lookup"><span data-stu-id="7082a-198">To add a task, click **Add Task**.</span></span> <span data-ttu-id="7082a-199">Täytä tehtävän kenttien tiedot ja valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="7082a-199">Fill in the fields for the task, and then click **Save**.</span></span>  
  
5.  <span data-ttu-id="7082a-200">Jatkaa tehtävien lisäämistä kunnes työrakenne on valmis.</span><span class="sxs-lookup"><span data-stu-id="7082a-200">Continue adding tasks until your work breakdown structure is complete.</span></span> <span data-ttu-id="7082a-201">Luodessasi työrakennetta voit järjestää tehtäviä seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="7082a-201">While creating your work breakdown structure, you can do the following to organize your tasks:</span></span>  
  
    -   <span data-ttu-id="7082a-202">Valitse tehtävä ja siirrä se toisen tehtävän alapuolelle valitsemalla **Sisennä** tai siirrä se yhden tason verran taaksepäin valitsemalla Poista sisennys.</span><span class="sxs-lookup"><span data-stu-id="7082a-202">Select a task and click **Indent** to move it under another task or click Outdent to move it out a level.</span></span>  
  
    -   <span data-ttu-id="7082a-203">Valitse tehtävä ja siirrä sitä ylös- tai alaspäin luettelossa valitsemalla **Siirrä ylöspäin** tai **Siirrä alaspäin**.</span><span class="sxs-lookup"><span data-stu-id="7082a-203">Select a task and click **Move Up** or **Move Down** to move it up or down in the list.</span></span>  
  
    -   <span data-ttu-id="7082a-204">Piilota Gantt-kaavio valitsemalla **Piilota Gantt-kaavio** ja valitse **Näytä Gantt-kaavio** kun haluat näyttää sen uudelleen.</span><span class="sxs-lookup"><span data-stu-id="7082a-204">Click **Hide Gantt** to hide the Gantt chart, and click **Show Gantt** to display it again.</span></span>  
  
    -   <span data-ttu-id="7082a-205">Valitse eri aikaväli Gantt-kaaviolle kohdassa **Aika-asteikko**.</span><span class="sxs-lookup"><span data-stu-id="7082a-205">Select a different period of time for the Gantt chart in **Time Scale**.</span></span>  
  
6.  <span data-ttu-id="7082a-206">Lisää rooleja, jotka määritit projektin ryhmän jäsenille työrakenteessa, valitsemalla **Luo projektiryhmä**.</span><span class="sxs-lookup"><span data-stu-id="7082a-206">To add the roles you specified in your work breakdown structure to your project’s team members, click **Generate Project Team**.</span></span>  
  
7.  <span data-ttu-id="7082a-207">Valitse **Tallenna** näytön oikeassa alakulmassa, kun olet tehnyt kaikki muutokset.</span><span class="sxs-lookup"><span data-stu-id="7082a-207">Click **Save** at the bottom right corner of the screen when you’re done making changes.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="7082a-208">Katso myös</span><span class="sxs-lookup"><span data-stu-id="7082a-208">See Also</span></span>  
 [<span data-ttu-id="7082a-209">Projektipäällikön opas</span><span class="sxs-lookup"><span data-stu-id="7082a-209">Project manager guide</span></span>](../psa/project-manager-guide.md)
