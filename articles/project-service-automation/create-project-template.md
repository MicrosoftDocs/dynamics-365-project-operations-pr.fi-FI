---
title: Luo projektimalli
description: Projektimallin luominen (Project Service)
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: ba15d6d5-a43b-456a-9488-db6e92023fa1
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 50e12d65d5ed957565485413490b8d9f0e2f47ab
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/24/2020
ms.locfileid: "3751134"
---
# <a name="create-a-project-template-project-service"></a><span data-ttu-id="af068-103">Luo projektimalli (Project Service)</span><span class="sxs-lookup"><span data-stu-id="af068-103">Create a project template (Project Service)</span></span>

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="af068-104">Projektimallit säästävät aikaa, jos yritys tekee säännöllisesti samankaltaisia hankkeita.</span><span class="sxs-lookup"><span data-stu-id="af068-104">Project templates save you time if your company regularly bids on similar types of projects.</span></span> <span data-ttu-id="af068-105">Ne tarjoavat standardit roolit ja arvioidut tunnit projektityypille.</span><span class="sxs-lookup"><span data-stu-id="af068-105">They provide a standard set of roles and estimated hours for a type of project.</span></span> <span data-ttu-id="af068-106">Asiakaspäälliköt ja projektipäälliköt voivat luoda projektimallin mukaisia projekteja tai he voivat kopioida mallin ja tehdä omia.</span><span class="sxs-lookup"><span data-stu-id="af068-106">Account managers and project managers can create projects based on a project template, or they can copy the template and make one of their own.</span></span>  
  
## <a name="components-of-project-template"></a><span data-ttu-id="af068-107">Projektimallin osat</span><span class="sxs-lookup"><span data-stu-id="af068-107">Components of project template</span></span>
 <span data-ttu-id="af068-108">Projektimalli koostuu kolmesta osasta:</span><span class="sxs-lookup"><span data-stu-id="af068-108">A project template consists of three components:</span></span>  
  
- <span data-ttu-id="af068-109">**Työrakenne**:Projektimallin työrakenteessa on samoja elementtejä kuin projektissa.</span><span class="sxs-lookup"><span data-stu-id="af068-109">**Work breakdown structure**: A work breakdown structure in a project template has the same set of elements as in the project.</span></span> <span data-ttu-id="af068-110">Voit luoda tehtävähierarkian, liittää roolit tehtäville, määrittää aikataulu-ominaisuuksia, luoda riippuvuuksia ja tarkastella kaikkia tietoja Gantt-kaaviossa.</span><span class="sxs-lookup"><span data-stu-id="af068-110">You can create a task hierarchy, associate roles to task, define schedule attributes, set dependencies and view all the data in the Gantt.</span></span> <span data-ttu-id="af068-111">Projektimallien työrakenteet tukevat myös tehtävätiloja kullekin tehtävälle.</span><span class="sxs-lookup"><span data-stu-id="af068-111">The work breakdown structure in project templates also support task modes for each task.</span></span> <span data-ttu-id="af068-112">Projektimallilla ja projektilla ei ole eroa luotaessa työaikataulua.</span><span class="sxs-lookup"><span data-stu-id="af068-112">There is no difference between a project template and a project when creating work schedule.</span></span>  
  
- <span data-ttu-id="af068-113">**Projektiarviot**: Projektiarviot toimivat projektimallissa samoin kuin projekteissa, paitsi että oletusarvoiset kustannus- ja myyntihinnat sisältävät hinnastot ovat aina [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] -parametreissa määritetyt oletuskustannus- ja myyntihinnastot.</span><span class="sxs-lookup"><span data-stu-id="af068-113">**Project estimates**: Project estimates in templates work the same way as they do in projects, except the price lists for defaulting the cost and sales prices are always the default cost and sales price lists defined in [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] parameters.</span></span> <span data-ttu-id="af068-114">Loput toiminnallisuudet ovat samoja, kuin projektissa.</span><span class="sxs-lookup"><span data-stu-id="af068-114">The rest of the functionality is the same as in a project.</span></span>  
  
- <span data-ttu-id="af068-115">**Projektiryhmän muodostuminen**: kun muodostat projektiryhmää projektimallille et voi varata nimettyä resurssia mallissa.</span><span class="sxs-lookup"><span data-stu-id="af068-115">**Project team formation**: When forming a project team for a project template, you can’t book a named resource in a template.</span></span> <span data-ttu-id="af068-116">Voit käyttää **Luo projektiryhmä** -valintaa työrakenteessa yleisten resurssijoukkojen luomiseksi.</span><span class="sxs-lookup"><span data-stu-id="af068-116">You can use **Generate Project Team** in the work breakdown structure to generate a set of generic resources.</span></span> <span data-ttu-id="af068-117">Voit myös määrittää tarvittavat taidot ja ammattitaidot yleisiä resursseja varten.</span><span class="sxs-lookup"><span data-stu-id="af068-117">You can also specify required skills and proficiencies for generic resources.</span></span> <span data-ttu-id="af068-118">Ei voi korvata yleistä resurssia varattavalla resurssilla projektimalleissa.</span><span class="sxs-lookup"><span data-stu-id="af068-118">You can’t substitute a generic resource with a bookable resource in project templates.</span></span>  
  
## <a name="create-a-project-from-a-template"></a><span data-ttu-id="af068-119">Luo projekti mallista</span><span class="sxs-lookup"><span data-stu-id="af068-119">Create a project from a template</span></span>  
 <span data-ttu-id="af068-120">Voit luoda projektin mallista seuraavilla tavoilla:</span><span class="sxs-lookup"><span data-stu-id="af068-120">You can create a project from a template in these following ways:</span></span>  
  
-   <span data-ttu-id="af068-121">Kun luot projektia tarjouksesta voit valita projektimallin projektin pikaluontilomakkeesta.</span><span class="sxs-lookup"><span data-stu-id="af068-121">When creating a project from the quote, you can choose a project template in the project quick create form.</span></span>  
  
-   <span data-ttu-id="af068-122">projektilomake näytetään, ennen kuin tallennat tietueen, kun luot projektin napsauttamalla **uusi projekti**</span><span class="sxs-lookup"><span data-stu-id="af068-122">When creating a project by clicking **New Project**, the project form displays before you save the record.</span></span> <span data-ttu-id="af068-123">Täältä voit valita **valitse malli** -kentän, jos haluat valita ennalta määritettyjä projektimalleja organisaation luettelosta.</span><span class="sxs-lookup"><span data-stu-id="af068-123">From here, you can click **Pick a template** field to choose from the list of pre-defined project templates in your organization.</span></span>  
  
-   <span data-ttu-id="af068-124">Valitse **Luo projekti mallista** **Projektimalli** -sivulla, kun haluat luoda projektin mallista.</span><span class="sxs-lookup"><span data-stu-id="af068-124">Click **Create project from a template** on the **Project Template** page to create a project from the template.</span></span>  
  
## <a name="copying-components-of-a-template-to-a-project"></a><span data-ttu-id="af068-125">Projektimallin osien kopiointi projektiin</span><span class="sxs-lookup"><span data-stu-id="af068-125">Copying components of a template to a project</span></span>  
 <span data-ttu-id="af068-126">On muutamia asioita joita sinun tulisi tietää, kun kopioit projektimallin osia.</span><span class="sxs-lookup"><span data-stu-id="af068-126">When you copy components of a template into a project, there are a few things you should know about.</span></span>  
  
 <span data-ttu-id="af068-127">**Työrakenteen kopiointi**: kun kopioit työrakenteen projektimallista, jos projektissa on eri projektikalenteri kuin mallissa, tehtävien ajoitus kohdistetaan projektin kalenterin työaikaan.</span><span class="sxs-lookup"><span data-stu-id="af068-127">**Copying a work breakdown structure**: When you copy the work breakdown structure from a project template, if the project has a different project calendar than the template, the work hours from the project’s calendar will be applied to the schedule of tasks.</span></span> <span data-ttu-id="af068-128">Tämä muuttaa aikataulun varmistavaan projektikalenteriin.</span><span class="sxs-lookup"><span data-stu-id="af068-128">This adjusts the schedule to the backing project calendar.</span></span> <span data-ttu-id="af068-129">Vastaavasti ensimmäinen työrakenteen tehtävä saa projektin alkamispäivän, joten loput tehtävän hierarkia-aikataulusta päivitetään määritetyn mallin työrakenteen keston ja riippuvuuksien perusteella.</span><span class="sxs-lookup"><span data-stu-id="af068-129">Similarly, the first task on the work breakdown structure takes the project’s start date, so the rest of the task hierarchy schedule is updated based on the duration and dependencies specified in the template’s work breakdown structure.</span></span>  
  
 <span data-ttu-id="af068-130">**Projektien arvioiden kopiointi**: Kun kopioit koko projektin arvioiden rivit, hinnastot on päivitetty hankkeen omistavan yksikön kustannushinnaston ja asiakkaan myyntihinnaston perusteella.</span><span class="sxs-lookup"><span data-stu-id="af068-130">**Copying project estimates**: When you copy across project estimate lines, price lists are updated based on the owning unit of the project for the cost price list and customer for the sales price list.</span></span> <span data-ttu-id="af068-131">Yksikön kustannus- ja myyntihinnat määritetään projekteille, jotka liittyvät myyntientiteetin näin hinnastoihin.</span><span class="sxs-lookup"><span data-stu-id="af068-131">The unit cost and sales prices are determined from these price lists on projects that are associated to a sales entity.</span></span>  
  
 <span data-ttu-id="af068-132">**Projektiryhmän kopiointi**: Kun kopioit projektiryhmän projektimallista, yleisiä resursseja kopioidaan yli yhdessä mallissa määritettyjen taitojen ja ammattitaitojen kanssa.</span><span class="sxs-lookup"><span data-stu-id="af068-132">**Copying a project team**: When you copy the project team from the template to a project, the generic resources are copied across, along with the skills and proficiencies defined in the template.</span></span> <span data-ttu-id="af068-133">Projektimallissa säilytetään myös yleisiä resurssivarauksia.</span><span class="sxs-lookup"><span data-stu-id="af068-133">Generic resource assignments are also maintained as in the project template.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="af068-134">Katso myös</span><span class="sxs-lookup"><span data-stu-id="af068-134">See Also</span></span>  
 [<span data-ttu-id="af068-135">Projektipäällikön opas</span><span class="sxs-lookup"><span data-stu-id="af068-135">Project Manager Guide</span></span>](../project-service/project-manager-guide.md)
