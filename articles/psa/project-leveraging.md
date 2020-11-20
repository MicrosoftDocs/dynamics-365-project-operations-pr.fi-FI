---
title: Myyntiarviot ja projektit
description: Tässä aiheessa on tietoja siitä, miten aikataulua ja arvioita voidaan hyödyntää myyntiprosessissa.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
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
ms.openlocfilehash: d8bb380519759659dc1b4151b62228a626ee7a26
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/28/2020
ms.locfileid: "4120674"
---
# <a name="sales-estimates-and-projects"></a><span data-ttu-id="13897-103">Myyntiarviot ja projektit</span><span class="sxs-lookup"><span data-stu-id="13897-103">Sales estimates and projects</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="13897-104">Voit luoda myyntiarvioita myyntiprosessin aikana linkittämällä projektin myyntitarjoukseen.</span><span class="sxs-lookup"><span data-stu-id="13897-104">During the sales process, you can create sales estimates by linking a project to a sales quote.</span></span> <span data-ttu-id="13897-105">Tällä tavoin deterministinen arvio voi tapahtua myyntiprosessin aikana, jotta voidaan hyödyntää projektien aikatauluttamis- ja arviointimahdollisuuksia.</span><span class="sxs-lookup"><span data-stu-id="13897-105">In this way, deterministic estimation can occur during the sales process, to take advantage of project scheduling and estimation capabilities.</span></span> <span data-ttu-id="13897-106">Jos kauppa tehdään, myynnin arviointitarkoituksessa käytettyä aikataulua voidaan käyttää perustana projektisuunnitelman tarkentamista varten.</span><span class="sxs-lookup"><span data-stu-id="13897-106">If the sale goes through, the schedule that was used for sales estimation purposes can be used as the basis for further refinement of the project plan.</span></span>

## <a name="linking-a-project-to-a-quote-line"></a><span data-ttu-id="13897-107">Projektin linkittäminen tarjouspyynnön riviin</span><span class="sxs-lookup"><span data-stu-id="13897-107">Linking a project to a quote line</span></span>

<span data-ttu-id="13897-108">Kun luot projektipohjaisen tarjousrivin, voit luoda uuden projektin tai liittää aiemmin luodun projektin **tarjousrivi**-sivulle.</span><span class="sxs-lookup"><span data-stu-id="13897-108">When you create a project-based quote line, you can create a new project or associate an existing project pn the **Quote Line** page.</span></span> 

> ![Tarjousrivilomake](media/project-8.png)
 
<span data-ttu-id="13897-110">Kun luot uuden projektin tarjousrivin tiedoista, voit hyödyntää projektimalleja.</span><span class="sxs-lookup"><span data-stu-id="13897-110">When you create a new project from the quote line details, you can take advantage of project templates.</span></span> <span data-ttu-id="13897-111">Projektimallit ovat malliprojekteja, jotka edustavat organisaation kannalta tyypillisiä, tavallisia projektisuunnitelmia ja talousarvioita.</span><span class="sxs-lookup"><span data-stu-id="13897-111">Project templates are model projects that represent standard project plans and financial estimates that are typical in an organization.</span></span> <span data-ttu-id="13897-112">Ne voivat myös edustaa aiempien projektien projektisuunnitelmien ja arvioiden kopioita.</span><span class="sxs-lookup"><span data-stu-id="13897-112">They can also represent copies of project plans and estimates from past projects.</span></span>

> ![Tarjousrivin tiedot](media/project-9.png)
  
<span data-ttu-id="13897-114">Luomalla projektin tarjouksesta projekti liitetään automaattisesti tarjouksen riviin.</span><span class="sxs-lookup"><span data-stu-id="13897-114">When you create the project from the quote, the project is automatically associated with the quote line.</span></span>

## <a name="components-of-estimates-in-a-project"></a><span data-ttu-id="13897-115">Projektin arvioiden osat</span><span class="sxs-lookup"><span data-stu-id="13897-115">Components of estimates in a project</span></span>

<span data-ttu-id="13897-116">Aikataulun avulla voit jakaa työn tehtäviin, ylläpitää tehtävähierarkiaa, määrittää, mitkä resurssit tarvitaan tehtävän suorittamiseen, ja määrittää arvion tehtävän suorittamiseen tarvittavista toimista.</span><span class="sxs-lookup"><span data-stu-id="13897-116">A schedule lets you divide work into tasks, maintain a hierarchy of tasks, determine what resources are required to complete a task, and assign an estimate of the effort that is required to complete a task.</span></span>

<span data-ttu-id="13897-117">Voit määrittää työmäärän ja aikataulutuksen arviot käyttämällä **Aikataulu**-välilehden kenttiä **Projekti**-sivulla.</span><span class="sxs-lookup"><span data-stu-id="13897-117">You can define the work effort and schedule estimates by using the fields on the **Schedule** tab of the **Project** page.</span></span> <span data-ttu-id="13897-118">Koska projektiin liittyy hinnasto, talousarviot lasketaan käyttämällä hinnastossa määritettyjä kustannus- ja myyntihintoja.</span><span class="sxs-lookup"><span data-stu-id="13897-118">Because a price list is associated with the project, financial estimates are calculated by using cost and sales prices that are defined in the price list.</span></span>

## <a name="importing-estimates-from-a-project-into-a-quote"></a><span data-ttu-id="13897-119">Arvioiden tuominen projektista tarjoukseen</span><span class="sxs-lookup"><span data-stu-id="13897-119">Importing estimates from a project into a quote</span></span>

<span data-ttu-id="13897-120">Kun olet määrittänyt projektin arviot, voit tuoda ne tarjousriviin.</span><span class="sxs-lookup"><span data-stu-id="13897-120">After you define project estimates, you can import them into the quote line.</span></span> <span data-ttu-id="13897-121">Valitse **Tarjousrivin tiedot** -sivulla tehtäväpalkissa **Tuo arvioista** luodaksesi yhteenvedon projektin arvioista tapahtumatyypin, roolin tai tehtävän tason mukaan.</span><span class="sxs-lookup"><span data-stu-id="13897-121">On the **Quote Line Details** page, select **Import from estimates** on the ribbon to summarize project estimates by transaction type, role, or task level.</span></span>