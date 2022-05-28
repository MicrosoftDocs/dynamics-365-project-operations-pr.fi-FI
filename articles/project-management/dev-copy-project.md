---
title: Projektimallien kehittäminen kopiointiprojektin avulla
description: Tässä aiheessa on tietoja siitä, miten projektimalleja luodaan kopioi projekti -mukautetun toiminnon avulla.
author: stsporen
ms.date: 03/10/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: 72aa2db7c717eeab85ada448c673bf702087baeb
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/14/2022
ms.locfileid: "8590894"
---
# <a name="develop-project-templates-with-copy-project"></a>Projektimallien kehittäminen kopiointiprojektin avulla

_**Koskee:** Project Operationsin resurssiin / muuhun kuin resurssiin perustuvia skenaarioita, Lite-käyttöönotto-kaupasta proformalaskutukseen_

Dynamics 365 Project Operations tukee mahdollisuutta kopioida projekti ja palauttaa kaikki varaukset yleisiksi resursseiksi, jotka edustavat roolia. Tämän toiminnon avulla asiakkaat voivat luoda perusprojektimalleja.

Kun valitset **Kopioi projekti**, kohdeprojektin tila päivittyy. **Tilan syyn** avulla voit määrittää, milloin kopiointitoiminto on valmis. Jos valitset **Kopioi projekti**, myös projektin alkamispäiväksi tulee nykyinen alkamispäivä, jos kohdeprojektientiteetissä ei havaita tavoitepäivämäärää.

## <a name="copy-project-custom-action"></a>Kopioi projektin mukautettu toiminto

### <a name="name"></a>Name 

msdyn\_CopyProjectV3

### <a name="input-parameters"></a>Syöteparametrit

Syöttöparametreja on kolme:

- **ReplaceNamedResources** tai **ClearTeamsAndAssignments** – Määritä vain yksi vaihtoehto. Älä määritä molempia.

    - **\{"ReplaceNamedResources":true\}** – Project Operationsin oletustoimintatapa. Nimetyt resurssit korvataan yleisillä resursseilla.
    - **\{"ClearTeamsAndAssignments":true\}** – Project for the Webin oletustoimintatapa. Kaikki määritykset ja ryhmän jäsenet poistetaan.

- **SourceProject** – entiteettiviittaus lähdeprojektin, josta kopioidaan. Tämä parametri ei voi olla tyhjäarvoinen.
- **Target** – entiteettiviittaus kohdeprojektin, johon kopioidaan. Tämä parametri ei voi olla tyhjäarvoinen.

Seuraavassa taulukossa on yhteenveto näistä kolmesta parametrista.

| Parametri                | Type             | Arvo                 |
|--------------------------|------------------|-----------------------|
| ReplaceNamedResources    | Totuusarvo          | **Tosi** tai **Epätosi**. |
| ClearTeamsAndAssignments | Totuusarvo          | **Tosi** tai **Epätosi**. |
| SourceProject            | Entiteettiviittaus | Lähdeprojekti    |
| Target                   | Entiteettiviittaus | Kohdeprojekti    |

Lisätietoja oletustoiminnoista on kohdassa [Verkko-ohjelmointirajapintojen toimintojen käyttö](/powerapps/developer/common-data-service/webapi/use-web-api-actions).

### <a name="validations"></a>Vahvistukset

Seuraavat tarkistukset tehdään.

1. Tyhjäarvo tarkistaa ja noutaa lähde- ja kohdeprojektit, jotta varmistetaan, että molemmat projektit ovat olemassa organisaatiossa.
2. Järjestelmä tarkistaa, että kohdeprojekti on kelvollinen kopiointia varten, tarkistamalla seuraavat ehdot:

    - Projektissa ei ole aiempaa aktiviteettia (mukaan lukien **Tehtävät**-välilehden valinta) ja projekti on juuri luotu.
    - Ei ole aiempaa kopiota, tuontia ei ole pyydetty tälle projektille eikä projektin tilana ole **Epäonnistunut**.

3. Toimintoa ei kutsuta HTTP:n avulla.

## <a name="specify-fields-to-copy"></a>Kopioitavien kenttien määrittäminen

Kun toimintoa kutsutaan, **Kopioi projekti** näyttää projektinäkymän **Kopioi projekti sarakkeet**, kun haluat määrittää, mitkä kentät kopioidaan projektin kopioinnin yhteydessä.

### <a name="example"></a>Esimerkki:

Seuraavassa esimerkissä näytetään, miten mukautettua **CopyProjectV3** -toimintoa kutsutaan **removeNamedResources** -parametrijoukon avulla.

```C#
{
    using System;
    using System.Runtime.Serialization;
    using Microsoft.Xrm.Sdk;
    using Newtonsoft.Json;

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
            targetProject["msdyn_subject"] = "Example Project - Copy";
            targetProject.Id = organizationService.Create(targetProject);

            CallCopyProjectAPI(sourceProject.ToEntityReference(), targetProject.ToEntityReference(), copyOption, true, false);
            Console.WriteLine("Done ...");
        }

        private void CallCopyProjectAPI(EntityReference sourceProject, EntityReference TargetProject, bool replaceNamedResources = true, bool clearTeamsAndAssignments = false)
        {
            OrganizationRequest req = new OrganizationRequest("msdyn_CopyProjectV3");
            req["SourceProject"] = sourceProject;
            req["Target"] = TargetProject;

            if (replaceNamedResources)
            {
                req["ReplaceNamedResources"] = true;
            }
            else
            {
                req["ClearTeamsAndAssignments"] = true;
            }

            OrganizationResponse response = organizationService.Execute(req);
        }
    }
}
```

[!INCLUDE[footer-include](../includes/footer-banner.md)]
