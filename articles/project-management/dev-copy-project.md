---
title: Projektimallien kehittäminen kopiointiprojektin avulla
description: Tässä aiheessa on tietoja siitä, miten projektimalleja luodaan kopioi projekti -mukautetun toiminnon avulla.
author: stsporen
manager: Annbe
ms.date: 01/21/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 27847575e2d6ec9af77d24f756b13d3aeb0efea7
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5286919"
---
# <a name="develop-project-templates-with-copy-project"></a><span data-ttu-id="17fd1-103">Projektimallien kehittäminen kopiointiprojektin avulla</span><span class="sxs-lookup"><span data-stu-id="17fd1-103">Develop project templates with Copy Project</span></span>

<span data-ttu-id="17fd1-104">_**Koskee:** Project Operationsin resurssiin / muuhun kuin resurssiin perustuvia skenaarioita, Lite-käyttöönotto-kaupasta proformalaskutukseen_</span><span class="sxs-lookup"><span data-stu-id="17fd1-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="17fd1-105">Dynamics 365 Project Operations tukee mahdollisuutta kopioida projekti ja palauttaa kaikki varaukset yleisiksi resursseiksi, jotka edustavat roolia.</span><span class="sxs-lookup"><span data-stu-id="17fd1-105">Dynamics 365 Project Operations supports the ability to copy a project and revert any assignments back to the generic resources that represent the role.</span></span> <span data-ttu-id="17fd1-106">Tämän toiminnon avulla asiakkaat voivat luoda perusprojektimalleja.</span><span class="sxs-lookup"><span data-stu-id="17fd1-106">Customers can use this functionality to build basic project templates.</span></span>

<span data-ttu-id="17fd1-107">Kun valitset **Kopioi projekti**, kohdeprojektin tila päivittyy.</span><span class="sxs-lookup"><span data-stu-id="17fd1-107">When you select **Copy Project**, the status of the target project is updated.</span></span> <span data-ttu-id="17fd1-108">**Tilan syyn** avulla voit määrittää, milloin kopiointitoiminto on valmis.</span><span class="sxs-lookup"><span data-stu-id="17fd1-108">Use **Status Reason** to determine when the copy action is complete.</span></span> <span data-ttu-id="17fd1-109">Jos valitset **Kopioi projekti**, myös projektin alkamispäiväksi tulee nykyinen alkamispäivä, jos kohdeprojektientiteetissä ei havaita tavoitepäivämäärää.</span><span class="sxs-lookup"><span data-stu-id="17fd1-109">Selecting **Copy Project** also updates the start date of the project to the current start date if no target date is detected in the target project entity.</span></span>

## <a name="copy-project-custom-action"></a><span data-ttu-id="17fd1-110">Kopioi projektin mukautettu toiminto</span><span class="sxs-lookup"><span data-stu-id="17fd1-110">Copy Project custom action</span></span> 

### <a name="name"></a><span data-ttu-id="17fd1-111">Nimi</span><span class="sxs-lookup"><span data-stu-id="17fd1-111">Name</span></span> 

<span data-ttu-id="17fd1-112">**msdyn_CopyProjectV2**</span><span class="sxs-lookup"><span data-stu-id="17fd1-112">**msdyn_CopyProjectV2**</span></span>

### <a name="input-parameters"></a><span data-ttu-id="17fd1-113">Syöteparametrit</span><span class="sxs-lookup"><span data-stu-id="17fd1-113">Input parameters</span></span>
<span data-ttu-id="17fd1-114">Syöttöparametreja on kolme:</span><span class="sxs-lookup"><span data-stu-id="17fd1-114">There are three input parameters:</span></span>

| <span data-ttu-id="17fd1-115">Parametri</span><span class="sxs-lookup"><span data-stu-id="17fd1-115">Parameter</span></span>          | <span data-ttu-id="17fd1-116">Laji</span><span class="sxs-lookup"><span data-stu-id="17fd1-116">Type</span></span>   | <span data-ttu-id="17fd1-117">Arvot</span><span class="sxs-lookup"><span data-stu-id="17fd1-117">Values</span></span>                                                   | 
|--------------------|--------|----------------------------------------------------------|
| <span data-ttu-id="17fd1-118">ProjectCopyOption</span><span class="sxs-lookup"><span data-stu-id="17fd1-118">ProjectCopyOption</span></span>  | <span data-ttu-id="17fd1-119">String</span><span class="sxs-lookup"><span data-stu-id="17fd1-119">String</span></span> | <span data-ttu-id="17fd1-120">**{"removeNamedResources":true}** tai **{"clearTeamsAndAssignments":true}**</span><span class="sxs-lookup"><span data-stu-id="17fd1-120">**{"removeNamedResources":true}** or **{"clearTeamsAndAssignments":true}**</span></span> |
| <span data-ttu-id="17fd1-121">SourceProject</span><span class="sxs-lookup"><span data-stu-id="17fd1-121">SourceProject</span></span>      | <span data-ttu-id="17fd1-122">Entiteettiviittaus</span><span class="sxs-lookup"><span data-stu-id="17fd1-122">Entity Reference</span></span> | <span data-ttu-id="17fd1-123">Lähdeprojekti</span><span class="sxs-lookup"><span data-stu-id="17fd1-123">Source Project</span></span> |
| <span data-ttu-id="17fd1-124">Kohde</span><span class="sxs-lookup"><span data-stu-id="17fd1-124">Target</span></span>             | <span data-ttu-id="17fd1-125">Entiteettiviittaus</span><span class="sxs-lookup"><span data-stu-id="17fd1-125">Entity Reference</span></span> | <span data-ttu-id="17fd1-126">Kohdeprojekti</span><span class="sxs-lookup"><span data-stu-id="17fd1-126">Target Project</span></span> |


- <span data-ttu-id="17fd1-127">**{"clearTeamsAndAssignments":true}**: Kolme oletuskäyttäytyminen web-projektille ja poistaa kaikki varaukset ja ryhmän jäsenet.</span><span class="sxs-lookup"><span data-stu-id="17fd1-127">**{"clearTeamsAndAssignments":true}**: Thee default behavior for Project for the Web, and will remove all assignments and team members.</span></span>
- <span data-ttu-id="17fd1-128">**{"removeNamedResources":true}** Oletustoiminta Project Operationsille ja palauttaa varaukset yleisiin resursseihin.</span><span class="sxs-lookup"><span data-stu-id="17fd1-128">**{"removeNamedResources":true}** The default behavior for Project Operations, and will revert assignments to generic resources.</span></span>

<span data-ttu-id="17fd1-129">Lisätietoja oletustoiminnoista on kohdassa [Verkko-ohjelmointirajapintojen toimintojen käyttö](https://docs.microsoft.com/powerapps/developer/common-data-service/webapi/use-web-api-actions)</span><span class="sxs-lookup"><span data-stu-id="17fd1-129">For more defaults on actions, see [Use Web API actions](https://docs.microsoft.com/powerapps/developer/common-data-service/webapi/use-web-api-actions)</span></span>

## <a name="specify-fields-to-copy"></a><span data-ttu-id="17fd1-130">Kopioitavien kenttien määrittäminen</span><span class="sxs-lookup"><span data-stu-id="17fd1-130">Specify fields to copy</span></span> 
<span data-ttu-id="17fd1-131">Kun toimintoa kutsutaan, **Kopioi projekti** näyttää projektinäkymän **Kopioi projekti sarakkeet**, kun haluat määrittää, mitkä kentät kopioidaan projektin kopioinnin yhteydessä.</span><span class="sxs-lookup"><span data-stu-id="17fd1-131">When the action is called, **Copy Project** will look at the project view **Copy Project Columns** to determine which fields to copy when the project is copied.</span></span>


### <a name="example"></a><span data-ttu-id="17fd1-132">Esimerkiksi</span><span class="sxs-lookup"><span data-stu-id="17fd1-132">Example</span></span>
<span data-ttu-id="17fd1-133">Seuraavassa esimerkissä näytetään, miten mukautettu toimintoa **CopyProject** kutsutaan **removeNamedResources**-parametrijoukolla.</span><span class="sxs-lookup"><span data-stu-id="17fd1-133">The following example shows how to call the **CopyProject** custom action with the **removeNamedResources** parameter set.</span></span>
```C#
{
    using System;
    using System.Runtime.Serialization;
    using Microsoft.Xrm.Sdk;
    using Newtonsoft.Json;

    [DataContract]
    public class ProjectCopyOption
    {
        /// <summary>
        /// Clear teams and assignments.
        /// </summary>
        [DataMember(Name = "clearTeamsAndAssignments")]
        public bool ClearTeamsAndAssignments { get; set; }

        /// <summary>
        /// Replace named resource with generic resource.
        /// </summary>
        [DataMember(Name = "removeNamedResources")]
        public bool ReplaceNamedResources { get; set; }
    }

    public class CopyProjectSample
    {
        private IOrganizationService organizationService;

        public CopyProjectSample(IOrganizationService organizationService)
        {
            this.organizationService = organizationService;
        }

        public void SampleRun()
        {
            // Example source project GUID
            Guid sourceProjectId = new Guid("11111111-1111-1111-1111-111111111111");
            var sourceProject = new Entity("msdyn_project", sourceProjectId);

            Entity targetProject = new Entity("msdyn_project");
            targetProject["msdyn_subject"] = "Example Project";
            targetProject.Id = organizationService.Create(targetProject);

            ProjectCopyOption copyOption = new ProjectCopyOption();
            copyOption.ReplaceNamedResources = true;

            CallCopyProjectAPI(sourceProject.ToEntityReference(), targetProject.ToEntityReference(), copyOption);
            Console.WriteLine("Done ...");
        }

        private void CallCopyProjectAPI(EntityReference sourceProject, EntityReference TargetProject, ProjectCopyOption projectCopyOption)
        {
            OrganizationRequest req = new OrganizationRequest("msdyn_CopyProjectV2");
            req["SourceProject"] = sourceProject;
            req["Target"] = TargetProject;
            req["ProjectCopyOption"] = JsonConvert.SerializeObject(projectCopyOption);
            OrganizationResponse response = organizationService.Execute(req);
        }
    }
}
```


[!INCLUDE[footer-include](../includes/footer-banner.md)]