---
title: Projektiaikataulun ohjelmointirajapintojen käyttö toimintojen suorittamiseen aikataulutusentiteeteillä
description: Tässä artikkelissa on tietoja ja esimerkkejä projektiaikataulun ohjelmointirajapintojen käyttämisestä.
author: sigitac
ms.date: 01/13/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 159d395efff98f2af780e5ed1e5ab3d6483cba89
ms.sourcegitcommit: b1c26ea57be721c5b0b1a33f2de0380ad102648f
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/20/2022
ms.locfileid: "9541120"
---
# <a name="use-project-schedule-apis-to-perform-operations-with-scheduling-entities"></a>Projektiaikataulun ohjelmointirajapintojen käyttö toimintojen suorittamiseen aikataulutusentiteeteillä

_**Koskee:** Project Operationsin resurssiin / muuhun kuin resurssiin perustuvia skenaarioita, Lite-käyttöönotto-kaupasta proformalaskutukseen_


**Aikataulutusentiteetit**

Projektiaikataulun ohjelmointirajapintojen avulla voi luoda, päivittää ja poistaa toimintoja **aikataulutusentiteettien** avulla. Näitä entiteettejä hallitaan verkkopohjaisessa Projectissa aikataulutusytimen kautta. Luonti-, päivitys- ja poisto-operaatioita **Aikataulutusentiteettien avulla** rajoitettiin aiemmissa Dynamics 365 Project Operations -julkaisuissa.

Seuraavassa taulukossa on täydellinen luettelo Projektiaikataulu -entiteeteistä.

| **Entiteetin nimi**         | **Entiteetin looginen nimi**     |
|-------------------------|-----------------------------|
| Project                 | msdyn_project               |
| Projektin tehtävä            | msdyn_projecttask           |
| Projektitehtävän riippuvuus | msdyn_projecttaskdependency |
| Resurssien delegointi     | msdyn_resourceassignment    |
| Projektin joukko          | msdyn_projectbucket         |
| Projektiryhmän jäsen     | msdyn_projectteam           |
| Projektin tarkistusluettelot      | msdyn_projectchecklist      |
| Projektin selite           | msdyn_projectlabel          |
| Projektitehtävä, jolle annetaan selite   | msdyn_projecttasktolabel    |
| Projektisprintti          | msdyn_projectsprint         |

**OperationSet**

OperationSet on työyksikkörakenne, jota voidaan käyttää, kun useita aikatauluihin vaikuttavia pyyntöjä on käsiteltävä tapahtumassa.

**Projektiaikataulujen ohjelmointirajapinnat**

Seuraavassa on luettelo nykyisistä Projektiaikataulun ohjelmointirajapinnoista.

| **Ohjelmointirajapinta**                                 | Description                                                                                                                       |
|-----------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| **msdyn_CreateProjectV1**               | Tätä ohjelmointirajapintaa käytetään projektin luomiseen. Projekti ja oletusprojektisäilö luodaan heti.                         |
| **msdyn_CreateTeamMemberV1**            | Tätä ohjelmointirajapintaa käytetään projektin ryhmän jäsenen luomiseen. Ryhmän jäsentietue luodaan heti.                                  |
| **msdyn_CreateOperationSetV1**          | Tämän ohjelmointirajapinnan avulla voidaan aikatauluttaa useita pyyntöjä, jotka on suoritettava tapahtumassa.                                        |
| **msdyn_PssCreateV1**                   | Tätä ohjelmointirajapintaa käytetään entiteetin luomiseen. Entiteetti voi olla mikä tahansa luontitoimintoa tukeva projektin aikataulutusentiteetti. |
| **msdyn_PssUpdateV1**                   | Tätä ohjelmointirajapintaa käytetään entiteetin päivittämiseen. Entiteetti voi olla mikä tahansa päivitystoimintoa tukeva projektin aikataulutusentiteetti  |
| **msdyn_PssDeleteV1**                   | Tätä ohjelmointirajapintaa käytetään entiteetin poistamiseen. Entiteetti voi olla mikä tahansa poistotoimintoa tukeva projektin aikataulutusentiteetti. |
| **msdyn_ExecuteOperationSetV1**         | Tämän ohjelmointirajapinnan avulla suoritetaan kaikki toiminnot tietyn toimintojoukon sisällä.                                                 |
| **msdyn_PssUpdateResourceAssignmentV1** | Tätä ohjelmointirajapintaa käytetään päivittämään resurssin määrityksen suunnitellut työt.                                                        |



**Projektiaikataulun ohjelmointirajapintojen käyttäminen OperationSetin kanssa**

Koska tietueet, joissa on sekä **CreateProjectV1** että **CreateTeamMemberV1** luodaan välittömästi, näitä ohjelmointirajapintoja ei voida käyttää suoraan **OperationSet** issä. Ohjelmointirajapinnan avulla voit kuitenkin luoda tarvittavat tietueet, luoda **OperationSet** in, ja käyttää sitten näitä aiemmin luotuja tietueita **OperationSet** issä.

**Tuetut toiminnot**

| **Aikataulutusentiteetti**   | **Luo** | **Update** | **Delete** | **Tärkeitä huomioon otettavia seikkoja**                                                                                                                                                                                                                                                                                                                            |
|-------------------------|------------|------------|------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Projektitehtävä            | Kyllä        | Kyllä        | Kyllä        | **Progress**-, **EffortCompleted**- ja **EffortRemaining**-kenttiä voi muokata Project for the Webissä, mutta niitä ei voi muokata Project Operationsissa.                                                                                                                                                                                             |
| Projektitehtävän riippuvuus | Kyllä        | No         | Kyllä        | Projektitehtävän riippuvuustietueita ei päivitetä. Sen sijaan voidaan poistaa vanha tietue ja luoda uusi tietue.                                                                                                                                                                                                                                 |
| Resurssien delegointi     | Kyllä        | Kyllä\*      | Kyllä        | Toimintoja, joilla on seuraavat kentät, ei tueta: **BookableResourceID**, **Effort**, **EffortCompleted**, **EffortRemaining** ja **PlannedWork**. Resurssien määritystietueita ei päivitetä. Sen sijaan voidaan poistaa vanha tietue ja luoda uusi tietue. Erillinen ohjelmointirajapinta on annettu resurssin määritysten päivittämiseen. |
| Projektin säilö          | Kyllä        | Kyllä        | Kyllä        | Oletussäilö luodaan **CreateProjectV1**-ohjelmointirajapinnan avulla. Update Release 16 -versiossa lisättiin projektisäilöjen luonti- ja poistotuki.                                                                                                                                                                                                   |
| Projektiryhmän jäsen     | Kyllä        | Kyllä        | Kyllä        | Käytä luontioperaatiolle **CreateTeamMemberV1** -ohjelmointirajapintaa.                                                                                                                                                                                                                                                                                           |
| Project                 | Kyllä        | Kyllä        |            | Toimintoja, joilla on seuraavat kentät, ei tueta **StateCode**, **BulkGenerationStatus**, **GlobalRevisionToken**, **CalendarID**, **Effort**, **EffortCompleted**, **EffortRemaining**, **Progress**, **Finish**, **TaskEarliestStart** ja **Duration**.                                                                                       |
| Projektin tarkistusluettelot      | Kyllä        | Kyllä        | Kyllä        |                                                                                                                                                                                                                                                                                                                                                         |
| Projektin selite           | No         | Kyllä        | No         | Selitteiden nimiä voi muuttaa. Tämä toiminto on käytettävissä vain Project for the Webissä                                                                                                                                                                                                                                                                      |
| Projektitehtävä, jolle annetaan selite   | Kyllä        | No         | Kyllä        | Tämä toiminto on käytettävissä vain Project for the Webissä                                                                                                                                                                                                                                                                                                  |
| Projektisprintti          | Kyllä        | Kyllä        | Kyllä        | **Aloitus**-kentässä on oltava **Päättymispäivä**-kenttää vanhempi päivämäärä. Saman projektin sprintit eivät voi olla päällekkäisiä toistensa kanssa. Tämä toiminto on käytettävissä vain Project for the Webissä                                                                                                                                                                    |




Tunnusominaisuus on valinnainen. Jos se on annettu, järjestelmä yrittää käyttää sitä ja antaa poikkeuksen, jos sitä ei voi käyttää. Jos sitä ei ole annettu, järjestelmä luo sen.

**Rajoitukset ja tunnetut ongelmat**

Seuraavassa on luettelo rajoituksista ja tunnetuista ongelmista:

-   Projektiaikataulun ohjelmointirajapintoja voivat käyttää vain **käyttäjät, joilla on Microsoft Project -lisenssi**. Niitä eivät voi käyttää:
    -   Sovelluksen käyttäjät
    -   Järjestelmäkäyttäjät
    -   Integrointikäyttäjät
    -   Muut käyttäjät, joilla ei ole tarvittavaa lisenssiä
-   Kussakin **OperationSet** issä voi olla enintään 100 toimintoa.
-   Kullakin käyttäjällä voi olla enintään 10 avointa **OperationSet** iä.
-   Project Operations tukee tällä hetkellä projektissa enintään 500 tehtävää.
-   Kukin päivitysresurssien määritystoiminto lasketaan yhdeksi toiminnoksi.
-   Kussakin päivitetyssä luettelossa voi olla enintään 100 aikaviipaletta.
-   **OperationSet**-virheen tila- ja virhelokit eivät ole tällä hetkellä käytettävissä.
-   Projektissa voi olla enintään 400 sprinttiä.
-   [Projektien ja tehtävien rajoitukset ja rajat](/project-for-the-web/project-for-the-web-limits-and-boundaries).
-   Selitteet ovat käytettävissä vain Project for the Webissä.

**Virheen käsittely**

-   Voit tarkastella toimintojoukoista luotuja virheitä kohdassa **Asetukset** \> **Aikatauluta integrointi** \> **Toimintojoukot**.
-   Voit tarkastella Projektin aikataulupalvelussa luotuja virheitä valitsemalla **Asetukset** \> **Aikataulun integrointi** \> **PSS-virhelokit**.

**Resurssien määrityksen jaksotuksen muokkaaminen**

Toisin kuin kaikki muut entiteettiä päivittävät projektin aikataulutuksen ohjelmointirajapinnat, resurssin määrityksen ohjelmointirajapinta vastaa yksin yhteen kenttään tehtävistä päivityksistä, msdyn_plannedwork, yksittäisessä entiteetissä, msydn_resourceassignment.

Annettu aikataulutila on:

-   **kiinteät yksiköt**
-   Projektikalenteri on 9–5p on 9–5pst, ma, ti, to, perjantai (EI TÖITÄ KESKIVIIKKOISIN)
-   ja resurssikalenteri on 9–1p PST ma–pe

Tämä tehtävä on yhdelle viikolle, neljä tuntia päivässä. Tämä johtuu siitä, että resurssikalenteri on 9–1 PST tai neljä tuntia päivässä.

| &nbsp;     | Tehtävä | Aloituspäivämäärä | Päättymispäivämäärä  | Määrä | 6/13/2022 | 6/14/2022 | 6/15/2022 | 6/16/2022 | 6/17/2022 |
|------------|------|------------|-----------|----------|-----------|-----------|-----------|-----------|-----------|
| 9-1-työntekijä |  T1  | 6/13/2022  | 6/17/2022 | 20       | 4         | 4         | 4         | 4         | 4         |

Jos esimerkiksi haluat, että työntekijä työskentelee vain kolme tuntia joka päivä tällä viikolla ja sallitaan tunti muita tehtäviä varten.

#### <a name="updatedcontours-sample-payload"></a>UpdatedContours-näytehyötykuorma:

```json
[{

"minutes":900.0,

"start":"2022-06-13T00:00:00-07:00",

"end":"2022-06-18T00:00:00-07:00"

}]
```

Tämä on tehtävä Päivitä aikataulu -ohjelmointirajapinnan suorituksen jälkeen.

| &nbsp;     | Tehtävä | Aloituspäivämäärä | Päättymispäivämäärä  | Määrä | 6/13/2022 | 6/14/2022 | 6/15/2022 | 6/16/2022 | 6/17/2022 |
|------------|------|------------|-----------|----------|-----------|-----------|-----------|-----------|-----------|
| 9-1-työntekijä | T1   | 6/13/2022  | 6/17/2022 | 15       | 3         | 3         | 3         | 3         | 3         |


**Näyteskenaario**

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

** Muita näytteitä

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
