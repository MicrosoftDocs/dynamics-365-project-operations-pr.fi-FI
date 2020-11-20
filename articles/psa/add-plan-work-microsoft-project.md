---
title: Töiden suunnittelu Microsoft Projectissa Project Service -apuohjelmalla | MicrosoftDocs
description: Tässä aiheessa on tietoja Microsoft Project Servicen Microsoft Project -apuohjelman lisäämisestä, määrityksestä ja käytöstä.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 04/06/2019
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
ms.openlocfilehash: 6bc74442866caccc02e53afc913a55aab81f9629
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/28/2020
ms.locfileid: "4129674"
---
# <a name="use-the-project-service-automation-add-in-to-plan-your-work-in-microsoft-project"></a><span data-ttu-id="df65e-103">Töiden suunnittelu Microsoft Projectissa Project Service Automation -apuohjelmalla</span><span class="sxs-lookup"><span data-stu-id="df65e-103">Use the Project Service Automation Add-in to plan your work in Microsoft Project</span></span>

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

[!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] <span data-ttu-id="df65e-104">helpottaa projektinsuunnittelua, kuten arvioita.</span><span class="sxs-lookup"><span data-stu-id="df65e-104">makes it easier for you to do your project planning, including estimates.</span></span> <span data-ttu-id="df65e-105">Voit määrittää työn niin, että kustannukset, tavoite ja myynnin arvot ovat selvillä, kun lopullinen ehdotus lähetetään.</span><span class="sxs-lookup"><span data-stu-id="df65e-105">You can define the work so that costs, effort, and sales value are clear as the final proposal is submitted.</span></span>  

 <span data-ttu-id="df65e-106">Asentamalla [!INCLUDE[pn_ms_dyn_365_psa_for_ms_project](../includes/pn-ms-dyn-365-psa-for-ms-project.md)]in voit suunnitella työt tutussa [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] -ympäristössä.</span><span class="sxs-lookup"><span data-stu-id="df65e-106">Now you can install the [!INCLUDE[pn_ms_dyn_365_psa_for_ms_project](../includes/pn-ms-dyn-365-psa-for-ms-project.md)] and do your planning work in the familiar environment of [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].</span></span> <span data-ttu-id="df65e-107">Käytä [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]in tehokkaita suunnittelu- ja hallintatoimintoja ja päivitä projektisuunnitelma sitten Project Service Automationiin.</span><span class="sxs-lookup"><span data-stu-id="df65e-107">Use the robust planning and management capabilities of [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] and then update your project plan in Project Service Automation.</span></span>  

> [!IMPORTANT]
> - <span data-ttu-id="df65e-108">Jotta SharePointin tiedostojen hallintatoimintoa voi käyttää [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] -tiedostojesi tallentamiseksi [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] -projekteja varten, [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]in järjestelmänvalvojan on otettava tiedostojen hallinta käyttöön.</span><span class="sxs-lookup"><span data-stu-id="df65e-108">To use SharePoint document management to store your [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] files for [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] projects, your [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] admin will need to turn on document management.</span></span> 
> - <span data-ttu-id="df65e-109">[!INCLUDE[pn_ms_dyn_365_psa_for_ms_project](../includes/pn-ms-dyn-365-psa-for-ms-project.md)] on yhteensopiva vain [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] 2016 Professional Editionin kanssa.</span><span class="sxs-lookup"><span data-stu-id="df65e-109">The [!INCLUDE[pn_ms_dyn_365_psa_for_ms_project](../includes/pn-ms-dyn-365-psa-for-ms-project.md)] is only compatible with [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] 2016 Professional Edition.</span></span>  

## <a name="download-and-install-the-add-in"></a><span data-ttu-id="df65e-110">Apuohjelman lataaminen ja asentaminen</span><span class="sxs-lookup"><span data-stu-id="df65e-110">Download and install the add-in</span></span>  
 <span data-ttu-id="df65e-111">Varmista, että [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] -kirjautumistiedot ovat valmiina.</span><span class="sxs-lookup"><span data-stu-id="df65e-111">Have your [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] sign-in information ready.</span></span> <span data-ttu-id="df65e-112">Tarvitset näitä tietoja [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]in ja [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]in välisen yhteyden muodostamiseen.</span><span class="sxs-lookup"><span data-stu-id="df65e-112">You will need this information to connect from [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] to [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span></span>  

1.  <span data-ttu-id="df65e-113">Voit ladata tuetun Project Service -versiosi lisäosan [joko V2.X](https://go.microsoft.com/fwlink/?linkid=828268) tai [V3.4+](https://www.microsoft.com/download/details.aspx?id=57956) latauskeskuksesta.</span><span class="sxs-lookup"><span data-stu-id="df65e-113">From the Download Center, download the add-in for your supported version of Project Service, either [V2.X](https://go.microsoft.com/fwlink/?linkid=828268) or [V3.4+](https://www.microsoft.com/download/details.aspx?id=57956).</span></span>  

2.  <span data-ttu-id="df65e-114">Napsauta lataamislinkkiä.</span><span class="sxs-lookup"><span data-stu-id="df65e-114">Click the download link.</span></span>  

3.  <span data-ttu-id="df65e-115">Kun lataus on valmis, asenna apuohjelma valitsemalla **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="df65e-115">When the download is complete, click **Yes** to install the add-in.</span></span>  

## <a name="configure-the-add-in"></a><span data-ttu-id="df65e-116">Apuohjelman määrittäminen</span><span class="sxs-lookup"><span data-stu-id="df65e-116">Configure the add-in</span></span>  

1. <span data-ttu-id="df65e-117">Avaa [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] ja valitse **Project Service** -välilehti.</span><span class="sxs-lookup"><span data-stu-id="df65e-117">Open [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] and click the **Project Service** tab.</span></span>  

2. <span data-ttu-id="df65e-118">Valitse **Yhdistä**.</span><span class="sxs-lookup"><span data-stu-id="df65e-118">Click **Connect**.</span></span>  

3. <span data-ttu-id="df65e-119">Anna kirjautumistiedot ja valitse **Kirjaudu**.</span><span class="sxs-lookup"><span data-stu-id="df65e-119">Enter your sign-in information and then click **Sign in**.</span></span>  

   <span data-ttu-id="df65e-120">Voit nyt aloittaa apuohjelman käytön.</span><span class="sxs-lookup"><span data-stu-id="df65e-120">Now you can start using the add-in.</span></span>  

## <a name="read-from-a-template"></a><span data-ttu-id="df65e-121">Mallin lukeminen</span><span class="sxs-lookup"><span data-stu-id="df65e-121">Read from a template</span></span>  
 <span data-ttu-id="df65e-122">Lue [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]issa luodusta ja [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]in kopioidusta mallista ja aloita projektin suunnittelu.</span><span class="sxs-lookup"><span data-stu-id="df65e-122">Read from a template that you created in [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] and copied into [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] to start your project planning.</span></span> [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] <span data-ttu-id="df65e-123">[Projektimallin luominen (Project Service Automation)](../psa/create-project-template.md)</span><span class="sxs-lookup"><span data-stu-id="df65e-123">[Create a project template (Project Service Automation)](../psa/create-project-template.md)</span></span>  

1.  <span data-ttu-id="df65e-124">Valitse **Project Service** -välilehdessä **Lue** > **Project Service Automation -projektimalli**.</span><span class="sxs-lookup"><span data-stu-id="df65e-124">From the **Project Service** tab, click **Read** > **Project Service Automation Project Template**.</span></span>  

2.  <span data-ttu-id="df65e-125">Valitse ensin projektimalli luettelosta ja sitten **Avaa**.</span><span class="sxs-lookup"><span data-stu-id="df65e-125">Choose a project template from the list and then click **Open**.</span></span>  

    > [!NOTE]
    >  <span data-ttu-id="df65e-126">Mallista Projectiin kopioidut tehtävät määritetään oletusarvoisesti manuaalisesti aikataulutetuksi.</span><span class="sxs-lookup"><span data-stu-id="df65e-126">By default, the tasks that are copied from the template into Project are set as manually scheduled.</span></span>  

## <a name="assign-pn_project_service_auto-roles-to-project-resources"></a><span data-ttu-id="df65e-127">[!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]in roolien delegointi projektin resursseille</span><span class="sxs-lookup"><span data-stu-id="df65e-127">Assign [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] roles to project resources</span></span>  

1.  <span data-ttu-id="df65e-128">Avaa projekti ja napsauta **Tehtävä**-valintanauhaa.</span><span class="sxs-lookup"><span data-stu-id="df65e-128">Open a project and click the **Task** ribbon.</span></span>  

2.  <span data-ttu-id="df65e-129">Valitse ensin **Gantt-kaavio**-valikko ja valitse sitten **Resurssitaulukko**.</span><span class="sxs-lookup"><span data-stu-id="df65e-129">Click the **Gantt Chart** menu and then choose **Resource Sheet**.</span></span>  

3.  <span data-ttu-id="df65e-130">Napsauta Resurssitaulukko-kohdassa avattavaa **Project Service -resurssirooli** -valikkoa ja valitse Project Service Automation -rooli.</span><span class="sxs-lookup"><span data-stu-id="df65e-130">On the Resource Sheet, click the **Project Service Resource Role** drop-down menu and choose a Project Service Automation role.</span></span>  

## <a name="staff-your-project-with-resources"></a><span data-ttu-id="df65e-131">Resurssien valinta projektiin</span><span class="sxs-lookup"><span data-stu-id="df65e-131">Staff your project with resources</span></span>  

1.  <span data-ttu-id="df65e-132">Valitse Project Service -välilehdessä ensin rivi ja sitten **Etsi resursseja**.</span><span class="sxs-lookup"><span data-stu-id="df65e-132">From the Project Service tab, select a row and click **Find Resources**.</span></span>  

2.  <span data-ttu-id="df65e-133">Valitse **Varaa resurssi** -näytössä projektissa käytettävä resurssi.</span><span class="sxs-lookup"><span data-stu-id="df65e-133">On the **Book Resource** screen, select the resource that you want to use for the project.</span></span>  

3.  <span data-ttu-id="df65e-134">Valitse ensin **Varaa** ja sitten **OK**.</span><span class="sxs-lookup"><span data-stu-id="df65e-134">Click **Book** and then click **OK**.</span></span>  

## <a name="publish-your-project"></a><span data-ttu-id="df65e-135">Projektin julkaiseminen</span><span class="sxs-lookup"><span data-stu-id="df65e-135">Publish your project</span></span>  
<span data-ttu-id="df65e-136">Kun projektisuunnittelu on valmis, seuraavana vaiheena on projekti tuonti ja julkaisu [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]issa.</span><span class="sxs-lookup"><span data-stu-id="df65e-136">When your project planning is complete, the next step is to import and publish the project in to [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span></span>  

<span data-ttu-id="df65e-137">Projekti tuodaan [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]iin.</span><span class="sxs-lookup"><span data-stu-id="df65e-137">The project will import into [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span></span> <span data-ttu-id="df65e-138">Hinnoittelu- ja ryhmänmuodostusprosessia käytetään.</span><span class="sxs-lookup"><span data-stu-id="df65e-138">The pricing and team generation process are applied.</span></span> <span data-ttu-id="df65e-139">Avaa projekti [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]issa ja tarkista, että ryhmä, projektiarviot ja työrakenne on luotu.</span><span class="sxs-lookup"><span data-stu-id="df65e-139">Open the project in [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] to see that the team, project estimates, and work breakdown structure has been generated.</span></span> <span data-ttu-id="df65e-140">Seuraavassa taulukossa näkyy, mistä löydät tulokset:</span><span class="sxs-lookup"><span data-stu-id="df65e-140">The following table shows where to find the results:</span></span>


|                                                                                          |                                                                                                                                   |
|------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
|  [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] <span data-ttu-id="df65e-141">**Gantt-kaaviot**</span><span class="sxs-lookup"><span data-stu-id="df65e-141">**Gantt Chart**</span></span>   | <span data-ttu-id="df65e-142">Tuo tiedot [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]:n **Työrakenne**-näytölle.</span><span class="sxs-lookup"><span data-stu-id="df65e-142">Imports into the [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] **Work Breakdown Structure** screen.</span></span> |
| [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] <span data-ttu-id="df65e-143">**Resurssisivu**</span><span class="sxs-lookup"><span data-stu-id="df65e-143">**Resource Sheet**</span></span> |   <span data-ttu-id="df65e-144">Tuo tiedot [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]:n **Projektiryhmän jäsenet** -näytölle.</span><span class="sxs-lookup"><span data-stu-id="df65e-144">Imports into the [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] **Project Team Members** screen.</span></span>   |
|   [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] <span data-ttu-id="df65e-145">**Käytön käyttö**</span><span class="sxs-lookup"><span data-stu-id="df65e-145">**Use Usage**</span></span>    |    <span data-ttu-id="df65e-146">Tuo tiedot [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]:n **Projektin arviot** -näyttöön.</span><span class="sxs-lookup"><span data-stu-id="df65e-146">Omports into the [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] **Project Estimates** screen.</span></span>     |

<span data-ttu-id="df65e-147">**Projektin tuominen ja julkaisu**</span><span class="sxs-lookup"><span data-stu-id="df65e-147">**To import and publish your project**</span></span>  
1. <span data-ttu-id="df65e-148">Valitse **Project Service** -välilehdessä **Julkaise** > **Uusi Project Service Automation -projekti**.</span><span class="sxs-lookup"><span data-stu-id="df65e-148">From the **Project Service** tab, click **Publish** > **New Project Service Automation Project**.</span></span>  

2. <span data-ttu-id="df65e-149">Anna **Julkaise uuteen Project Service -projektiin** -valintaikkunassa **Projektin nimi** ja valitse **Asiakas**.</span><span class="sxs-lookup"><span data-stu-id="df65e-149">On **Publish to a new project in Project Service** dialog box, enter the **Project Name** and select the **Customer**.</span></span>  

3. <span data-ttu-id="df65e-150">Voit vaihtoehtoisesti valita **Linkitä projektisuunnitelma Project Service Automationiin** -vaihtoehdon, jolloin suunnitelman Project-tiedosto linkitetään Project Service Automationiin.</span><span class="sxs-lookup"><span data-stu-id="df65e-150">Optionally check the **Link project plan to Project Service Automation** to link the plan Project file to Project Service Automation.</span></span>  

4. <span data-ttu-id="df65e-151">Valitse **Julkaise**.</span><span class="sxs-lookup"><span data-stu-id="df65e-151">Click **Publish**.</span></span>  

   <span data-ttu-id="df65e-152">Kun Project-tiedosto linkitetään [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]iin, Project-tiedostosta tulee päätiedosto ja [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]in työrakenne on vain luku -muotoinen.</span><span class="sxs-lookup"><span data-stu-id="df65e-152">Linking the Project file to [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] makes the Project file the master and sets the work breakdown structure in [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] to read-only.</span></span>  <span data-ttu-id="df65e-153">Jos haluat tehdä muutoksia projektisuunnitelmaan, ne on tehtävä [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]issa ja julkaistava päivityksinä [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]issa.</span><span class="sxs-lookup"><span data-stu-id="df65e-153">In order to make changes to the project plan, you need to make them in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] and publish them as updates to [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span></span>  

## <a name="edit-a-project-thats-been-imported"></a><span data-ttu-id="df65e-154">Tuodun projektin muokkaaminen</span><span class="sxs-lookup"><span data-stu-id="df65e-154">Edit a project that’s been imported</span></span>  
 <span data-ttu-id="df65e-155">Voit tehdä [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]iin tuotuun projektisuunnitelmaan muutoksia kahdella tavalla:</span><span class="sxs-lookup"><span data-stu-id="df65e-155">To make changes to a project plan that's been imported into [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], you have two options:</span></span>  

- <span data-ttu-id="df65e-156">Voit avata päätiedoston ja muokata sitä [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]issa.</span><span class="sxs-lookup"><span data-stu-id="df65e-156">Open the master file and edit it in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].</span></span>  

- <span data-ttu-id="df65e-157">Voit poistaa tiedoston linkin ja muokata sitä suoraan Project Servicessä.</span><span class="sxs-lookup"><span data-stu-id="df65e-157">Unlink the file and edit it directly in Project Service.</span></span> <span data-ttu-id="df65e-158">[!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]ista ladattu tiedosto lukitaan oletusarvoisesti, ja sitä voi muokata vain Projectissa.</span><span class="sxs-lookup"><span data-stu-id="df65e-158">By default, a project that’s been uploaded from [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] is locked and can only be edited in Project.</span></span> <span data-ttu-id="df65e-159">Jos haluat muokata tiedostoa [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]issa, tiedoston linkitys on poistettava.</span><span class="sxs-lookup"><span data-stu-id="df65e-159">To edit the file in [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], the file has to be unlinked.</span></span>  

### <a name="edit-in-pn_microsoft_project"></a><span data-ttu-id="df65e-160">Muokkaa [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]issa</span><span class="sxs-lookup"><span data-stu-id="df65e-160">Edit in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]</span></span>  

1. <span data-ttu-id="df65e-161">Valitse päävalikosta **Project Service** > **Projektit**.</span><span class="sxs-lookup"><span data-stu-id="df65e-161">From the main menu, click **Project Service** > **Projects**.</span></span>  

2. <span data-ttu-id="df65e-162">Avaa projektiluettelosta [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]issa luotu projekti.</span><span class="sxs-lookup"><span data-stu-id="df65e-162">From the list of projects, open the one you created in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].</span></span>  

3. <span data-ttu-id="df65e-163">Valitse valintanauhassa **Avaa MS Projectissa**.</span><span class="sxs-lookup"><span data-stu-id="df65e-163">Click **Open in MS Project** from the ribbon.</span></span> <span data-ttu-id="df65e-164">Linkitetty päätiedosto avataan [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]issa.</span><span class="sxs-lookup"><span data-stu-id="df65e-164">This will open the linked master file in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].</span></span>  

### <a name="unlink-a-file-and-edit-in-pn_microsoft_project-service"></a><span data-ttu-id="df65e-165">Tiedoston linkin poistaminen ja sen muokkaaminen [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] Servicessä</span><span class="sxs-lookup"><span data-stu-id="df65e-165">Unlink a file and edit in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] Service</span></span>  

1. <span data-ttu-id="df65e-166">Valitse päävalikosta **Project Service** > **Projektit**.</span><span class="sxs-lookup"><span data-stu-id="df65e-166">From the main menu, click **Project Service** > **Projects**.</span></span>  

2. <span data-ttu-id="df65e-167">Avaa projektiluettelosta [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]issa luotu projekti.</span><span class="sxs-lookup"><span data-stu-id="df65e-167">From the list of projects, open the one you created in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].</span></span>  

3. <span data-ttu-id="df65e-168">Valitse valintanauhassa **Poista projektin linkitys MS Projectista**.</span><span class="sxs-lookup"><span data-stu-id="df65e-168">Click **Unlink from MS Project** from the ribbon.</span></span>  

## <a name="upload-a-project-file-to-sharepoint-or-office-groups"></a><span data-ttu-id="df65e-169">Project-tiedoston lataaminen SharePointiin tai Office-ryhmiin</span><span class="sxs-lookup"><span data-stu-id="df65e-169">Upload a Project file to SharePoint or Office Groups</span></span>  
 <span data-ttu-id="df65e-170">Voit ladata Project-tiedoston SharePointiin, jossa se sijaitsee [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]-projektin liitetyissä tiedostoissa.</span><span class="sxs-lookup"><span data-stu-id="df65e-170">You can upload your Project file to SharePoint and find it under the Associated Documents for your [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] project.</span></span>  <span data-ttu-id="df65e-171">SharePoint-tiedostojen hallinnan määrittäjän on oltava järjestelmänvalvoja, joka voi myös ottaa toiminnon käyttöön Project-entiteetissä.</span><span class="sxs-lookup"><span data-stu-id="df65e-171">You need to have your administrator configure SharePoint document management and turn it on for the Project entity.</span></span> 

 <span data-ttu-id="df65e-172">Voit myös ladata Project-tiedoston [!INCLUDE[pn_onedrive_for_business](../includes/pn-onedrive-for-business.md)]iin, jos Office-ryhmät on määritetty.</span><span class="sxs-lookup"><span data-stu-id="df65e-172">You can also upload your Project file to [!INCLUDE[pn_onedrive_for_business](../includes/pn-onedrive-for-business.md)] if you have Office Groups set up.</span></span>

### <a name="upload-a-file-for-sharepoint"></a><span data-ttu-id="df65e-173">Lataa tiedosto SharePointia varten</span><span class="sxs-lookup"><span data-stu-id="df65e-173">Upload a file for SharePoint</span></span>  

1. <span data-ttu-id="df65e-174">Valitse päävalikosta **Project Service** > **Siirrä**.</span><span class="sxs-lookup"><span data-stu-id="df65e-174">From the main menu, click **Project Service** > **Upload**.</span></span>  

2. <span data-ttu-id="df65e-175">Valitse **Project Service Automation -projektin asiakirjat**.</span><span class="sxs-lookup"><span data-stu-id="df65e-175">Select **To Project Service Automation Project Documents**.</span></span>  

3. <span data-ttu-id="df65e-176">Valitse **Ota Avaa [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]issa käyttöön** -valintaikkunassa **Kyllä** tai **Ei**.</span><span class="sxs-lookup"><span data-stu-id="df65e-176">On the **Enable Open in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** dialog, select **Yes** or **No**.</span></span>  

   - <span data-ttu-id="df65e-177">Jos valitset **Kyllä**, voit valita **Avaa [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]issa** -painiketta Project Service Automationissa sekä käynnistää [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]in ja ladata Project-tiedoston SharePoint-tiedostokirjastosta.</span><span class="sxs-lookup"><span data-stu-id="df65e-177">If you click **Yes**, you'll be able select the **Open in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** button in Project Service Automation, launch [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)], and load the Project file from the SharePoint document library.</span></span>  

   - <span data-ttu-id="df65e-178">Jos valitset **Ei**, **Avaa [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]issa** -painikkeen linkki ei toimi.</span><span class="sxs-lookup"><span data-stu-id="df65e-178">If you click **No**, the link for the **Open in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** button won't work.</span></span>  

4. <span data-ttu-id="df65e-179">[!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] -tiedosto sijaitsee [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]issa tietyn [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] -projektin **Tiedostot**-kohdassa.</span><span class="sxs-lookup"><span data-stu-id="df65e-179">The [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] file can be found in [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] under **Documents** for the specific [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] project.</span></span>  

### <a name="upload-a-file-for-office-groups"></a><span data-ttu-id="df65e-180">Tiedoston siirtäminen Office-ryhmiin</span><span class="sxs-lookup"><span data-stu-id="df65e-180">Upload a file for Office Groups</span></span>  

1. <span data-ttu-id="df65e-181">Valitse päävalikosta **Project Service** > **Siirrä**.</span><span class="sxs-lookup"><span data-stu-id="df65e-181">From the main menu, click **Project Service** > **Upload**.</span></span>  

2. <span data-ttu-id="df65e-182">Valitse **Project Service Automation -projektin asiakirjat**.</span><span class="sxs-lookup"><span data-stu-id="df65e-182">Select **To Project Service Automation Project Documents**.</span></span>  

3. <span data-ttu-id="df65e-183">Valitse **Ota Avaa [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]issa käyttöön** -valintaikkunassa **Kyllä** tai **Ei**.</span><span class="sxs-lookup"><span data-stu-id="df65e-183">On the **Enable Open in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** dialog, select **Yes** or **No**.</span></span>  

   - <span data-ttu-id="df65e-184">Jos valitset **Kyllä**, voit valita **Avaa [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]issa** -painiketta Project Service Automationissa sekä käynnistää [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]in ja ladata Project-tiedoston SharePoint-tiedostokirjastosta.</span><span class="sxs-lookup"><span data-stu-id="df65e-184">If you click **Yes**, you'll be able to select the **Open in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** button in Project Service Automation, launch [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)], and load the Project file from the SharePoint document library.</span></span>  

   - <span data-ttu-id="df65e-185">Jos valitset **Ei**, **Avaa [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]issa** -painikkeen linkki ei toimi.</span><span class="sxs-lookup"><span data-stu-id="df65e-185">If you click **No**, the link for the **Open in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** button won't work.</span></span>  

4. <span data-ttu-id="df65e-186">[!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] -tiedosto sijaitsee [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]issa tietyn [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] -projektin **Tiedostot**-kohdassa.</span><span class="sxs-lookup"><span data-stu-id="df65e-186">The [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] file can be found in [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] under **Documents** for the specific [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] project.</span></span>  

## <a name="publish--your-project-as-a-template"></a><span data-ttu-id="df65e-187">Projektin julkaiseminen mallina</span><span class="sxs-lookup"><span data-stu-id="df65e-187">Publish  your project as a template</span></span>  
 <span data-ttu-id="df65e-188">Voit tallentaa projektin ja käyttää sitä uudelleen tallentamalla sen projektimallina [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]issa.</span><span class="sxs-lookup"><span data-stu-id="df65e-188">You can save your project and reuse it by saving it as a project template in [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span></span>  <span data-ttu-id="df65e-189">Projektimalleja ovat [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]issa uudelleenkäytettäviä projektisuunnitelmia.</span><span class="sxs-lookup"><span data-stu-id="df65e-189">Project templates are reusable project plans in [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span></span> [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] <span data-ttu-id="df65e-190">[Projektimallin luominen (Project Service Automation)](../psa/create-project-template.md)</span><span class="sxs-lookup"><span data-stu-id="df65e-190">[Create a project template (Project Service Automation)](../psa/create-project-template.md)</span></span>  

1. <span data-ttu-id="df65e-191">Valitse **Project Service** -välilehdessä **Julkaise** > **Uusi Project Service Automation -projektimalli**.</span><span class="sxs-lookup"><span data-stu-id="df65e-191">From the **Project Service** tab, click **Publish** > **New Project Service Automation Project Template**.</span></span>  

2. <span data-ttu-id="df65e-192">Anna **Julkaise uuteen Project Service -malliin** -valintaikkunassa **Projektimallin nimi**.</span><span class="sxs-lookup"><span data-stu-id="df65e-192">On the **Publish to a new project in Project Service template** dialog box, enter the **Project template name**.</span></span>  

3. <span data-ttu-id="df65e-193">Voit vaihtoehtoisesti valita **Linkitä projektisuunnitelma Project Service Automationiin** -vaihtoehdon, jolloin Project-tiedosto linkitetään [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]iin.</span><span class="sxs-lookup"><span data-stu-id="df65e-193">Optionally, check the **Link project plan to Project Service Automation** to link the Project file to [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span></span>  

4. <span data-ttu-id="df65e-194">Valitse **Julkaise**.</span><span class="sxs-lookup"><span data-stu-id="df65e-194">Click **Publish**.</span></span>  

<span data-ttu-id="df65e-195">Kun Project-tiedosto linkitetään [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]iin, Project-tiedostosta tulee päätiedosto ja [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] -mallin työrakenne on vain luku -muotoinen.</span><span class="sxs-lookup"><span data-stu-id="df65e-195">Linking the Project file to [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] makes the Project file the master and sets the work breakdown structure in the [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] template to read-only.</span></span>  <span data-ttu-id="df65e-196">Jos haluat tehdä muutoksia projektisuunnitelmaan, ne on tehtävä [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]issa ja julkaistava päivityksinä [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]issa.</span><span class="sxs-lookup"><span data-stu-id="df65e-196">In order to make changes to the project plan, you need to make them in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] and publish them as updates to [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span></span>

### <a name="see-also"></a><span data-ttu-id="df65e-197">Katso myös</span><span class="sxs-lookup"><span data-stu-id="df65e-197">See Also</span></span>  
 [<span data-ttu-id="df65e-198">Projektipäällikön opas</span><span class="sxs-lookup"><span data-stu-id="df65e-198">Project Manager Guide</span></span>](../psa/project-manager-guide.md)
