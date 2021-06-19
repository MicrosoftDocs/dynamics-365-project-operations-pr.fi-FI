---
title: Projektimallien kehittäminen kopiointiprojektin avulla
description: Tässä aiheessa on tietoja siitä, miten projektimalleja luodaan kopioi projekti -mukautetun toiminnon avulla.
author: stsporen
ms.date: 01/21/2021
ms.topic: article
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 7a1f602e789e07014fd6c742940f52341ce6c672
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/10/2021
ms.locfileid: "6005652"
---
# <a name="develop-project-templates-with-copy-project"></a>Projektimallien kehittäminen kopiointiprojektin avulla

_**Koskee:** Project Operationsin resurssiin / muuhun kuin resurssiin perustuvia skenaarioita, Lite-käyttöönotto-kaupasta proformalaskutukseen_

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Dynamics 365 Project Operations tukee mahdollisuutta kopioida projekti ja palauttaa kaikki varaukset yleisiksi resursseiksi, jotka edustavat roolia. Tämän toiminnon avulla asiakkaat voivat luoda perusprojektimalleja.

Kun valitset **Kopioi projekti**, kohdeprojektin tila päivittyy. **Tilan syyn** avulla voit määrittää, milloin kopiointitoiminto on valmis. Jos valitset **Kopioi projekti**, myös projektin alkamispäiväksi tulee nykyinen alkamispäivä, jos kohdeprojektientiteetissä ei havaita tavoitepäivämäärää.

## <a name="copy-project-custom-action"></a>Kopioi projektin mukautettu toiminto 

### <a name="name"></a>Nimi 

**msdyn_CopyProjectV2**

### <a name="input-parameters"></a>Syöteparametrit
Syöttöparametreja on kolme:

| Parametri          | Laji   | Arvot                                                   | 
|--------------------|--------|----------------------------------------------------------|
| ProjectCopyOption  | String | **{"removeNamedResources":true}** tai **{"clearTeamsAndAssignments":true}** |
| SourceProject      | Entiteettiviittaus | Lähdeprojekti |
| Kohde             | Entiteettiviittaus | Kohdeprojekti |


- **{"clearTeamsAndAssignments":true}**: Kolme oletuskäyttäytyminen web-projektille ja poistaa kaikki varaukset ja ryhmän jäsenet.
- **{"removeNamedResources":true}** Oletustoiminta Project Operationsille ja palauttaa varaukset yleisiin resursseihin.

Lisätietoja oletustoiminnoista on kohdassa [Verkko-ohjelmointirajapintojen toimintojen käyttö](/powerapps/developer/common-data-service/webapi/use-web-api-actions)

## <a name="specify-fields-to-copy"></a>Kopioitavien kenttien määrittäminen 
Kun toimintoa kutsutaan, **Kopioi projekti** näyttää projektinäkymän **Kopioi projekti sarakkeet**, kun haluat määrittää, mitkä kentät kopioidaan projektin kopioinnin yhteydessä.


### <a name="example"></a>Esimerkiksi
Seuraavassa esimerkissä näytetään, miten mukautettu toimintoa **CopyProject** kutsutaan **removeNamedResources**-parametrijoukolla.
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