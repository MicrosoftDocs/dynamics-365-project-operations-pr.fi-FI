---
title: Projektiaikataulun ohjelmointirajapintojen käyttö toimintojen suorittamiseen aikataulutusentiteeteillä
description: Tässä aiheessa on tietoja ja esimerkkejä projektiaikataulun ohjelmointirajapintojen käyttämisestä.
author: sigitac
ms.date: 06/22/2021
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 55bd9020275fbb72761b45ba09294f57266b418c0e5b506ba55a2a498aff24e5
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/06/2021
ms.locfileid: "7008762"
---
# <a name="use-project-schedule-apis-to-perform-operations-with-scheduling-entities"></a>Projektiaikataulun ohjelmointirajapintojen käyttö toimintojen suorittamiseen aikataulutusentiteeteillä

_**Koskee:** Project Operationsin resurssiin / muuhun kuin resurssiin perustuvia skenaarioita, Lite-käyttöönotto-kaupasta proformalaskutukseen_

> [!IMPORTANT] 
> Kaikki tai osa tässä aiheessa käsitellyistä toiminnoista ovat saatavilla esiversiojulkaisun osana. Sisältö ja toiminnot voivat muuttua. 

## <a name="scheduling-entities"></a>Aikataulutusentiteetit

Projektiaikataulun ohjelmointirajapintojen avulla voi luoda, päivittää ja poistaa toimintoja **aikataulutusentiteettien** avulla. Näitä entiteettejä hallitaan verkkopohjaisessa Projectissa aikataulutusytimen kautta. Luonti-, päivitys- ja poisto-operaatioita **Aikataulutusentiteettien avulla** rajoitettiin aiemmissa Dynamics 365 Project Operations -julkaisuissa.

Seuraavassa taulukossa on täydellinen luettelo Projektiaikataulu -entiteeteistä.

| Entiteetin nimi  | Entiteetin looginen nimi |
| --- | --- |
| Project | msdyn_project |
| Projektin tehtävä  | msdyn_projecttask  |
| Projektitehtävän riippuvuus  | msdyn_projecttaskdependency  |
| Resurssien delegointi | msdyn_resourceassignment |
| Projektin joukko  | msdyn_projectbucket |
| Projektiryhmän jäsen | msdyn_projectteam |

## <a name="operationset"></a>OperationSet

OperationSet on työyksikkörakenne, jota voidaan käyttää, kun useita aikatauluihin vaikuttavia pyyntöjä on käsiteltävä tapahtumassa.

## <a name="project-schedule-apis"></a>Projektiaikataulujen ohjelmointirajapinnat

Seuraavassa on luettelo nykyisistä Projektiaikataulun ohjelmointirajapinnoista.

- **msdyn_CreateProjectV1**: Tämän ohjelmointirajapinnan avulla voidaan luoda projekti. Projekti ja projektin oletussäilö luodaan heti.
- **msdyn_CreateTeamMemberV1**: Tämän ohjelmointirajapinnan avulla voidaan luoda projektiryhmän jäsen. Ryhmän jäsentietue luodaan heti.
- **msdyn_CreateOperationSetV1**: Tämän ohjelmointirajapinnan avulla voidaan aikatauluttaa useita pyyntöjä, jotka on suoritettava tapahtumassa.
- **msdyn_PSSCreateV1**: Tämän ohjelmointirajapinnan avulla voidaan luoda entiteetti. Entiteetti voi olla mikä tahansa luontitoimintoa tukeva projektin aikataulutusentiteetti.
- **msdyn_PSSUpdateV1**: Tämän ohjelmointirajapinnan avulla voidaan päivittää entiteetti. Entiteetti voi olla mikä tahansa päivitystoimintoa tukeva projektin aikataulutusentiteetti.
- **msdyn_PSSDeleteV1**: Tämän ohjelmointirajapinnan avulla voidaan poistaa entiteetti. Entiteetti voi olla mikä tahansa poistotoimintoa tukeva projektin aikataulutusentiteetti.
- **msdyn_ExecuteOperationSetV1**: Tämän ohjelmointirajapinnan avulla suoritetaan kaikki toiminnot tietyn toimintojoukon sisällä.

## <a name="using-project-schedule-apis-with-operationset"></a>Projektiaikataulun ohjelmointirajapintojen käyttäminen OperationSetin kanssa

Koska tietueet, joissa on sekä **CreateProjectV1** että **CreateTeamMemberV1** luodaan välittömästi, näitä ohjelmointirajapintoja ei voida käyttää suoraan **OperationSet** issä. Ohjelmointirajapinnan avulla voit kuitenkin luoda tarvittavat tietueet, luoda **OperationSet** in, ja käyttää sitten näitä aiemmin luotuja tietueita **OperationSet** issä.

## <a name="supported-operations"></a>Tuetut toiminnot

| Aikataulutusentiteetti | Luo | Päivitys | Delete | Tärkeitä huomioon otettavia seikkoja |
| --- | --- | --- | --- | --- |
Projektitehtävä | Kyllä | Kyllä | Kyllä | Ei ole |
| Projektitehtävän riippuvuus | Kyllä | Kyllä | | Projektitehtävän riippuvuustietueita ei päivitetä. Sen sijaan voidaan poistaa vanha tietue ja luoda uusi tietue. |
| Resurssien delegointi | Kyllä | Kyllä | | Toimintoja, joilla on seuraavat kentät, ei tueta: **BookableResourceID**, **Effort**, **EffortCompleted**, **EffortRemaining** ja **PlannedWork**. Resurssien määritystietueita ei päivitetä. Sen sijaan voidaan poistaa vanha tietue ja luoda uusi tietue. |
| Projektin säilö | – | – | – | Oletussäilö luodaan **CreateProjectV1** -ohjelmointirajapinnan avulla. |
| Projektiryhmän jäsen | Kyllä | Kyllä | Kyllä | Käytä luontioperaatiolle **CreateTeamMemberV1** -ohjelmointirajapintaa. |
| Project | Kyllä | Kyllä | – | Toimintoja, joilla on seuraavat kentät, ei tueta **StateCode**, **BulkGenerationStatus**, **GlobalRevisionToken**, **CalendarID**, **Effort**, **EffortCompleted**, **EffortRemaining**, **Progress**, **Finish**, **TaskEarliestStart** ja **Duration**. |

Näitä ohjelmointirajapintoja voidaan kutsua entiteettiobjekteilla, jotka sisältävät mukautettuja kenttiä.

Tunnusominaisuus on valinnainen. Jos se on annettu, järjestelmä yrittää käyttää sitä ja antaa poikkeuksen, jos sitä ei voi käyttää. Jos sitä ei ole annettu, järjestelmä luo sen.

## <a name="restricted-fields"></a>Rajoitetut kentät

Seuraavissa taulukoissa määritetään kentät, joita ei voi **luoda** ja **muokata**.

### <a name="project-task"></a>Projektitehtävä

| **Looginen nimi**                       | **Voidaan luoda** | **Voidaan muokata**     |
|----------------------------------------|----------------|------------------|
| msdyn_actualcost                       | ei             | ei               |
| msdyn_actualcost_base                  | ei             | ei               |
| msdyn_actualend                        | ei             | ei               |
| msdyn_actualsales                      | ei             | ei               |
| msdyn_actualsales_base                 | ei             | ei               |
| msdyn_actualstart                      | ei             | ei               |
| msdyn_costatcompleteestimate           | ei             | ei               |
| msdyn_costatcompleteestimate_base      | ei             | ei               |
| msdyn_costconsumptionpercentage        | ei             | ei               |
| msdyn_effortcompleted                  | ei             | ei               |
| msdyn_effortestimateatcomplete         | ei             | ei               |
| msdyn_iscritical                       | ei             | ei               |
| msdyn_iscriticalname                   | ei             | ei               |
| msdyn_ismanual                         | ei             | ei               |
| msdyn_ismanualname                     | ei             | ei               |
| msdyn_ismilestone                      | ei             | ei               |
| msdyn_ismilestonename                  | ei             | ei               |
| msdyn_LinkStatus                       | ei             | ei               |
| msdyn_linkstatusname                   | ei             | ei               |
| msdyn_msprojectclientid                | ei             | ei               |
| msdyn_plannedcost                      | ei             | ei               |
| msdyn_plannedcost_base                 | ei             | ei               |
| msdyn_plannedsales                     | ei             | ei               |
| msdyn_plannedsales_base                | ei             | ei               |
| msdyn_pluginprocessingdata             | ei             | ei               |
| msdyn_progress                         | ei             | ei (kyllä P4W:lle) |
| msdyn_remainingcost                    | ei             | ei               |
| msdyn_remainingcost_base               | ei             | ei               |
| msdyn_remainingsales                   | ei             | ei               |
| msdyn_remainingsales_base              | ei             | ei               |
| msdyn_requestedhours                   | ei             | ei               |
| msdyn_resourcecategory                 | ei             | ei               |
| msdyn_resourcecategoryname             | ei             | ei               |
| msdyn_resourceorganizationalunitid     | ei             | ei               |
| msdyn_resourceorganizationalunitidname | ei             | ei               |
| msdyn_salesconsumptionpercentage       | ei             | ei               |
| msdyn_salesestimateatcomplete          | ei             | ei               |
| msdyn_salesestimateatcomplete_base     | ei             | ei               |
| msdyn_salesvariance                    | ei             | ei               |
| msdyn_salesvariance_base               | ei             | ei               |
| msdyn_scheduleddurationminutes         | ei             | ei               |
| msdyn_scheduledend                     | ei             | ei               |
| msdyn_scheduledstart                   | ei             | ei               |
| msdyn_schedulevariance                 | ei             | ei               |
| msdyn_skipupdateestimateline           | ei             | ei               |
| msdyn_skipupdateestimatelinename       | ei             | ei               |
| msdyn_summary                          | ei             | ei               |
| msdyn_varianceofcost                   | ei             | ei               |
| msdyn_varianceofcost_base              | ei             | ei               |

### <a name="project-task-dependency"></a>Projektitehtävän riippuvuus

| **Looginen nimi**              | **Voidaan luoda** | **Voidaan muokata** |
|-------------------------------|----------------|--------------|
| msdyn_linktype                | ei             | ei           |
| msdyn_linktypename            | ei             | ei           |
| msdyn_predecessortask         | kyllä            | ei           |
| msdyn_predecessortaskname     | kyllä            | ei           |
| msdyn_project                 | kyllä            | ei           |
| msdyn_projectname             | kyllä            | ei           |
| msdyn_projecttaskdependencyid | kyllä            | ei           |
| msdyn_successortask           | kyllä            | ei           |
| msdyn_successortaskname       | kyllä            | ei           |

### <a name="resource-assignment"></a>Resurssien delegointi

| **Looginen nimi**             | **Voidaan luoda** | **Voidaan muokata** |
|------------------------------|----------------|--------------|
| msdyn_bookableresourceid     | kyllä            | ei           |
| msdyn_bookableresourceidname | kyllä            | ei           |
| msdyn_bookingstatusid        | ei             | ei           |
| msdyn_bookingstatusidname    | ei             | ei           |
| msdyn_committype             | ei             | ei           |
| msdyn_committypename         | ei             | ei           |
| msdyn_effort                 | ei             | ei           |
| msdyn_effortcompleted        | ei             | ei           |
| msdyn_effortremaining        | ei             | ei           |
| msdyn_finish                 | ei             | ei           |
| msdyn_plannedcost            | ei             | ei           |
| msdyn_plannedcost_base       | ei             | ei           |
| msdyn_plannedcostcontour     | ei             | ei           |
| msdyn_plannedsales           | ei             | ei           |
| msdyn_plannedsales_base      | ei             | ei           |
| msdyn_plannedsalescontour    | ei             | ei           |
| msdyn_plannedwork            | ei             | ei           |
| msdyn_projectid              | kyllä            | ei           |
| msdyn_projectidname          | ei             | ei           |
| msdyn_projectteamid          | ei             | ei           |
| msdyn_projectteamidname      | ei             | ei           |
| msdyn_start                  | ei             | ei           |
| msdyn_taskid                 | ei             | ei           |
| msdyn_taskidname             | ei             | ei           |
| msdyn_userresourceid         | ei             | ei           |

### <a name="project-team-member"></a>Projektiryhmän jäsen

| **Looginen nimi**                                 | **Voidaan luoda** | **Voidaan muokata** |
|--------------------------------------------------|----------------|--------------|
| msdyn_calendarid                                 | ei             | ei           |
| msdyn_creategenericteammemberwithrequirementname | ei             | ei           |
| msdyn_deletestatus                               | ei             | ei           |
| msdyn_deletestatusname                           | ei             | ei           |
| msdyn_effort                                     | ei             | ei           |
| msdyn_effortcompleted                            | ei             | ei           |
| msdyn_effortremaining                            | ei             | ei           |
| msdyn_finish                                     | ei             | ei           |
| msdyn_hardbookedhours                            | ei             | ei           |
| msdyn_hours                                      | ei             | ei           |
| msdyn_markedfordeletiontimer                     | ei             | ei           |
| msdyn_markedfordeletiontimestamp                 | ei             | ei           |
| msdyn_msprojectclientid                          | ei             | ei           |
| msdyn_percentage                                 | ei             | ei           |
| msdyn_requiredhours                              | ei             | ei           |
| msdyn_softbookedhours                            | ei             | ei           |
| msdyn_start                                      | ei             | ei           |

### <a name="project"></a>Project

| **Looginen nimi**                       | **Voidaan luoda** | **Voidaan muokata** |
|----------------------------------------|----------------|--------------|
| msdyn_actualexpensecost                | ei             | ei           |
| msdyn_actualexpensecost_base           | ei             | ei           |
| msdyn_actuallaborcost                  | ei             | ei           |
| msdyn_actuallaborcost_base             | ei             | ei           |
| msdyn_actualsales                      | ei             | ei           |
| msdyn_actualsales_base                 | ei             | ei           |
| msdyn_contractlineproject              | kyllä            | ei           |
| msdyn_contractorganizationalunitid     | kyllä            | ei           |
| msdyn_contractorganizationalunitidname | kyllä            | ei           |
| msdyn_costconsumption                  | ei             | ei           |
| msdyn_costestimateatcomplete           | ei             | ei           |
| msdyn_costestimateatcomplete_base      | ei             | ei           |
| msdyn_costvariance                     | ei             | ei           |
| msdyn_costvariance_base                | ei             | ei           |
| msdyn_duration                         | ei             | ei           |
| msdyn_effort                           | ei             | ei           |
| msdyn_effortcompleted                  | ei             | ei           |
| msdyn_effortestimateatcompleteeac      | ei             | ei           |
| msdyn_effortremaining                  | ei             | ei           |
| msdyn_finish                           | kyllä            | kyllä          |
| msdyn_globalrevisiontoken              | ei             | ei           |
| msdyn_islinkedtomsprojectclient        | ei             | ei           |
| msdyn_islinkedtomsprojectclientname    | ei             | ei           |
| msdyn_linkeddocumenturl                | ei             | ei           |
| msdyn_msprojectdocument                | ei             | ei           |
| msdyn_msprojectdocumentname            | ei             | ei           |
| msdyn_plannedexpensecost               | ei             | ei           |
| msdyn_plannedexpensecost_base          | ei             | ei           |
| msdyn_plannedlaborcost                 | ei             | ei           |
| msdyn_plannedlaborcost_base            | ei             | ei           |
| msdyn_plannedsales                     | ei             | ei           |
| msdyn_plannedsales_base                | ei             | ei           |
| msdyn_progress                         | ei             | ei           |
| msdyn_remainingcost                    | ei             | ei           |
| msdyn_remainingcost_base               | ei             | ei           |
| msdyn_remainingsales                   | ei             | ei           |
| msdyn_remainingsales_base              | ei             | ei           |
| msdyn_replaylogheader                  | ei             | ei           |
| msdyn_salesconsumption                 | ei             | ei           |
| msdyn_salesestimateatcompleteeac       | ei             | ei           |
| msdyn_salesestimateatcompleteeac_base  | ei             | ei           |
| msdyn_salesvariance                    | ei             | ei           |
| msdyn_salesvariance_base               | ei             | ei           |
| msdyn_scheduleperformance              | ei             | ei           |
| msdyn_scheduleperformancename          | ei             | ei           |
| msdyn_schedulevariance                 | ei             | ei           |
| msdyn_taskearlieststart                | ei             | ei           |
| msdyn_teamsize                         | ei             | ei           |
| msdyn_teamsize_date                    | ei             | ei           |
| msdyn_teamsize_state                   | ei             | ei           |
| msdyn_totalactualcost                  | ei             | ei           |
| msdyn_totalactualcost_base             | ei             | ei           |
| msdyn_totalplannedcost                 | ei             | ei           |
| msdyn_totalplannedcost_base            | ei             | ei           |


## <a name="limitations-and-known-issues"></a>Rajoitukset ja tunnetut ongelmat
Seuraavassa on luettelo rajoituksista ja tunnetuista ongelmista:

- Projektiaikataulun ohjelmointirajapintoja voivat käyttää vain **käyttäjät, joilla on Microsoft Project -lisenssi**. Niitä eivät voi käyttää:
    - Sovelluksen käyttäjät
    - Järjestelmäkäyttäjät
    - Integrointikäyttäjät
    - Muut käyttäjät, joilla ei ole tarvittavaa lisenssiä
- Kussakin **OperationSet** issä voi olla enintään 100 toimintoa.
- Kullakin käyttäjällä voi olla enintään 10 avointa **OperationSet** iä.
- Project Operations tukee tällä hetkellä projektissa enintään 500 tehtävää.
- **OperationSet**-virheen tila- ja virhelokit eivät ole tällä hetkellä käytettävissä.
- [Projektien ja tehtävien rajoitukset ja rajat](/project-for-the-web/project-for-the-web-limits-and-boundaries)

## <a name="error-handling"></a>Virheen käsittely

   - Voit tarkastella toimintojoukoista luotuja virheitä kohdassa **Asetukset** \> **Aikatauluta integrointi** \> **Toimintojoukot**.
   - Voit tarkastella Projektin aikataulupalvelussa luotuja virheitä valitsemalla **Asetukset** \> **Aikataulun integrointi** \> **PSS-virhelokit**.

## <a name="sample-scenario"></a>Näyteskenaario

Tässä skenaariossa luodaan projekti, ryhmän jäsen, neljä tehtävää ja kaksi resurssivarausta. Seuraavaksi päivität yhden tehtävän, päivität projektin, poistat yhden tehtävän, poistat yhden resurssin määrityksen ja luot riippuvuuden.

```csharp
Entity project = CreateProject();
project.Id = CallCreateProjectAction(project);
var projectReference = project.ToEntityReference();

var teamMember = new Entity("msdyn_projectteam", Guid.NewGuid());
teamMember["msdyn_name"] = $"TM {DateTime.Now.ToShortTimeString()}";
teamMember["msdyn_project"] = projectReference;
var createTeamMemberResponse = CallCreateTeamMemberAction(teamMember);

var description = $"My demo {DateTime.Now.ToShortTimeString()}";
var operationSetId = CallCreateOperationSetAction(project.Id, description);

var task1 = GetTask("1WW", projectReference);
var task2 = GetTask("2XX", projectReference, task1.ToEntityReference());
var task3 = GetTask("3YY", projectReference);
var task4 = GetTask("4ZZ", projectReference);

var assignment1 = GetResourceAssignment("R1", teamMember, task2, project);
var assignment2 = GetResourceAssignment("R2", teamMember, task3, project);

var task1Response = CallPssCreateAction(task1, operationSetId);
var task2Response = CallPssCreateAction(task2, operationSetId);
var task3Response = CallPssCreateAction(task3, operationSetId);
var task4Response = CallPssCreateAction(task4, operationSetId);

var assignment1Response = CallPssCreateAction(assignment1, operationSetId);
var assignment2Response = CallPssCreateAction(assignment2, operationSetId);

task2["msdyn_subject"] = "Updated Task";
var task2UpdateResponse = CallPssUpdateAction(task2, operationSetId);

project["msdyn_subject"] = $"Proj update {DateTime.Now.ToShortTimeString()}";
var projectUpdateResponse = CallPssUpdateAction(project, operationSetId);

var task4DeleteResponse = CallPssDeleteAction(task4.Id.ToString(), task4.LogicalName, operationSetId);

var assignment2DeleteResponse = CallPssDeleteAction(assignment2.Id.ToString(), assignment2.LogicalName, operationSetId);

var dependency1 = GetTaskDependency(project, task2, task3);
var dependency1Response = CallPssCreateAction(dependency1, operationSetId);

CallExecuteOperationSetAction(operationSetId);
Console.WriteLine("Done....");
```

## <a name="additional-samples"></a>Muita näytteitä

```csharp
#region Call actions --- Sample code ----

/// <summary>
/// Calls the action to create an operationSet
/// </summary>
/// <param name="projectId">project id for the operations to be included in this operationSet</param>
/// <param name="description">description of this operationSet</param>
/// <returns>operationSet id</returns>
private string CallCreateOperationSetAction(Guid projectId, string description)
{
    OrganizationRequest operationSetRequest = new OrganizationRequest("msdyn_CreateOperationSetV1");
    operationSetRequest["ProjectId"] = projectId.ToString();
    operationSetRequest["Description"] = description;
    OrganizationResponse response = organizationService.Execute(operationSetRequest);
    return response["OperationSetId"].ToString();
}

/// <summary>
/// Calls the action to create an entity, only Task and Resource Assignment for now
/// </summary>
/// <param name="entity">Task or Resource Assignment</param>
/// <param name="operationSetId">operationSet id</param>
/// <returns>OperationSetResponse</returns>

private OperationSetResponse CallPssCreateAction(Entity entity, string operationSetId)
{
    OrganizationRequest operationSetRequest = new OrganizationRequest("msdyn_PssCreateV1");
    operationSetRequest["Entity"] = entity;
    operationSetRequest["OperationSetId"] = operationSetId;
    return GetOperationSetResponseFromOrgResponse(organizationService.Execute(operationSetRequest));
}

/// <summary>
/// Calls the action to update an entity, only Task for now
/// </summary>
/// <param name="entity">Task or Resource Assignment</param>
/// <param name="operationSetId">operationSet Id</param>
/// <returns>OperationSetResponse</returns>
private OperationSetResponse CallPssUpdateAction(Entity entity, string operationSetId)
{
    OrganizationRequest operationSetRequest = new OrganizationRequest("msdyn_PssUpdateV1");
    operationSetRequest["Entity"] = entity;
    operationSetRequest["OperationSetId"] = operationSetId;
    return GetOperationSetResponseFromOrgResponse(organizationService.Execute(operationSetRequest));
}

/// <summary>
/// Calls the action to update an entity, only Task and Resource Assignment for now
/// </summary>
/// <param name="recordId">Id of the record to be deleted</param>
/// <param name="entityLogicalName">Entity logical name of the record</param>
/// <param name="operationSetId">OperationSet Id</param>
/// <returns>OperationSetResponse</returns>
private OperationSetResponse CallPssDeleteAction(string recordId, string entityLogicalName, string operationSetId)
{
    OrganizationRequest operationSetRequest = new OrganizationRequest("msdyn_PssDeleteV1");
    operationSetRequest["RecordId"] = recordId;
    operationSetRequest["EntityLogicalName"] = entityLogicalName;
    operationSetRequest["OperationSetId"] = operationSetId;
    return GetOperationSetResponseFromOrgResponse(organizationService.Execute(operationSetRequest));
}

/// <summary>
/// Calls the action to execute requests in an operationSet
/// </summary>
/// <param name="operationSetId">operationSet id</param>
/// <returns>OperationSetResponse</returns>
private OperationSetResponse CallExecuteOperationSetAction(string operationSetId)
{
    OrganizationRequest operationSetRequest = new OrganizationRequest("msdyn_ExecuteOperationSetV1");
    operationSetRequest["OperationSetId"] = operationSetId;
    return GetOperationSetResponseFromOrgResponse(organizationService.Execute(operationSetRequest));
}

/// <summary>
/// This can be used to abandon an operationSet that is no longer needed
/// </summary>
/// <param name="operationSetId">operationSet id</param>
/// <returns>OperationSetResponse</returns>
protected OperationSetResponse CallAbandonOperationSetAction(Guid operationSetId)
{
    OrganizationRequest operationSetRequest = new OrganizationRequest("msdyn_AbandonOperationSetV1");
    operationSetRequest["OperationSetId"] = operationSetId.ToString();
    return GetOperationSetResponseFromOrgResponse(organizationService.Execute(operationSetRequest));
}


/// <summary>
/// Calls the action to create a new project
/// </summary>
/// <param name="project">Project</param>
/// <returns>project Id</returns>
private Guid CallCreateProjectAction(Entity project)
{
    OrganizationRequest createProjectRequest = new OrganizationRequest("msdyn_CreateProjectV1");
    createProjectRequest["Project"] = project;
    OrganizationResponse response = organizationService.Execute(createProjectRequest);
    var projectId = Guid.Parse((string)response["ProjectId"]);
    return projectId;
}

/// <summary>
/// Calls the action to create a new project team member
/// </summary>
/// <param name="teamMember">Project team member</param>
/// <returns>project team member Id</returns>
private string CallCreateTeamMemberAction(Entity teamMember)
{
    OrganizationRequest request = new OrganizationRequest("msdyn_CreateTeamMemberV1");
    request["TeamMember"] = teamMember;
    OrganizationResponse response = organizationService.Execute(request);
    return (string)response["TeamMemberId"];
}

private OperationSetResponse GetOperationSetResponseFromOrgResponse(OrganizationResponse orgResponse)
{
    return JsonConvert.DeserializeObject<OperationSetResponse>((string)orgResponse.Results["OperationSetResponse"]);
}

private EntityCollection GetDefaultBucket(EntityReference projectReference)
{
    var columnsToFetch = new ColumnSet("msdyn_project", "msdyn_name");
    var getDefaultBucket = new QueryExpression("msdyn_projectbucket")
    {
        ColumnSet = columnsToFetch,
        Criteria =
        {
            Conditions =
            {
                new ConditionExpression("msdyn_project", ConditionOperator.Equal, projectReference.Id),
                new ConditionExpression("msdyn_name", ConditionOperator.Equal, "Bucket 1")
            }
        }
    };

    return organizationService.RetrieveMultiple(getDefaultBucket);
}

private Entity GetBucket(EntityReference projectReference)
{
    var bucketCollection = GetDefaultBucket(projectReference);
    if (bucketCollection.Entities.Count > 0)
    {
        return bucketCollection[0].ToEntity<Entity>();
    }

    throw new Exception($"Please open project with id {projectReference.Id} in the Dynamics UI and navigate to the Tasks tab");
}

private Entity CreateProject()
{
    var project = new Entity("msdyn_project", Guid.NewGuid());
    project["msdyn_subject"] = $"Proj {DateTime.Now.ToShortTimeString()}";

    return project;
}



private Entity GetTask(string name, EntityReference projectReference, EntityReference parentReference = null)
{
    var task = new Entity("msdyn_projecttask", Guid.NewGuid());
    task["msdyn_project"] = projectReference;
    task["msdyn_subject"] = name;
    task["msdyn_effort"] = 4d;
    task["msdyn_scheduledstart"] = DateTime.Today;
    task["msdyn_scheduledend"] = DateTime.Today.AddDays(5);
    task["msdyn_progress"] = 0.34m;
    task["msdyn_start"] = DateTime.Now.AddDays(1);
    task["msdyn_projectbucket"] = GetBucket(projectReference).ToEntityReference();
    task["msdyn_LinkStatus"] = new OptionSetValue(192350000);

    //Custom field handling
    /*
    task["new_custom1"] = "Just my test";
    task["new_age"] = 98;
    task["new_amount"] = 591.34m;
    task["new_isready"] = new OptionSetValue(100000000);
    */

    if (parentReference == null)
    {
        task["msdyn_outlinelevel"] = 1;
    }
    else
    {
        task["msdyn_parenttask"] = parentReference;
    }

    return task;
}

private Entity GetResourceAssignment(string name, Entity teamMember, Entity task, Entity project)
{
    var assignment = new Entity("msdyn_resourceassignment", Guid.NewGuid());
    assignment["msdyn_projectteamid"] = teamMember.ToEntityReference();
    assignment["msdyn_taskid"] = task.ToEntityReference();
    assignment["msdyn_projectid"] = project.ToEntityReference();
    assignment["msdyn_name"] = name;
    assignment["msdyn_start"] = DateTime.Now;
    assignment["msdyn_finish"] = DateTime.Now;

    return assignment;
}

protected Entity GetTaskDependency(Entity project, Entity predecessor, Entity successor)
{
    var taskDependency = new Entity("msdyn_projecttaskdependency", Guid.NewGuid());
    taskDependency["msdyn_project"] = project.ToEntityReference();
    taskDependency["msdyn_predecessortask"] = predecessor.ToEntityReference();
    taskDependency["msdyn_successortask"] = successor.ToEntityReference();
    taskDependency["msdyn_linktype"] = new OptionSetValue(192350000);

    return taskDependency;
}

#endregion


#region OperationSetResponse DataContract --- Sample code ----

[DataContract]
public class OperationSetResponse
{
[DataMember(Name = "operationSetId")]
public Guid OperationSetId { get; set; }

[DataMember(Name = "operationSetDetailId")]
public Guid OperationSetDetailId { get; set; }

[DataMember(Name = "operationType")]
public string OperationType { get; set; }

[DataMember(Name = "recordId")]
public string RecordId { get; set; }

[DataMember(Name = "correlationId")]
public string CorrelationId { get; set; }
}

#endregion
```
