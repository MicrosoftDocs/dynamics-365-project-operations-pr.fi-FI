---
title: Resurssien hallinnan muutokset (Project Service Automation 3.x)
description: Tässä aiheessa on tietoja resurssien hallinnan muutoksista.
author: makk
ms.custom:
- dyn365-projectservice
ms.date: 03/18/2019
ms.topic: article
ms.author: makk
audience: admin
search.audienceType:
- admin
- customizer
search.app:
- D365PS
- ProjectOperations
ms.reviewer: johnmichalak
ms.openlocfilehash: d19b8b453c544bb4c6fd11a8b9f750cb08e0c168
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/14/2022
ms.locfileid: "8595494"
---
# <a name="resource-management-changes-project-service-automation-3x"></a>Resurssien hallinnan muutokset (Project Service Automation 3.x)

[!include [banner](../../includes/psa-now-project-operations.md)]

Tämän aiheen osissa on tietoja muutoksista, joita on tehty resurssien hallinnan alueelle Dynamics 365 Project Service Automation versiossa 3. x.

## <a name="project-estimates"></a>Projektin arviot

Sen sijaan, että perustuisivat **msdyn\_projecttask** -entiteettiin (**Projektitehtävä**), projektin arviot perustuvat **msdyn\_resourceassignment** -entiteettiin (**Resurssin kohdentaminent**). Resurssien kohdennuksista on tullut "totuuden lähde" tehtävien aikatauluttamista ja hinnoittelua varten.

## <a name="line-tasks"></a>Rivitehtävät

PSA 3. x:ssä rivitehtävät ovat vanhentuneet (vanhentunut). Määritykset osoittavat nyt koko tehtävään rivitehtävien sijaan.

Seuraavasta esimerkistä näkyy, miten tehtävä, jonka nimi on "Testitehtävä", on määritetty ryhmän jäsenille A ja B PSA:N aiemmissa versioissa ja PSA 3. x:ssä.

- **Ennen PSA 3. x:ää:**

    - Testitehtävä

        - Testitehtävä – Rivitehtävä 1

            - Kohdennus A:lle

        - Testitehtävä – Rivitehtävä 2

            - Kohdennus B:lle

- **PSA 3.x:**

    - Testitehtävä

        - Kohdennus A:lle
        - Kohdennus B:lle

## <a name="unassigned-assignment"></a>Kohdentamaton kohdennus

PSA 3.x:ssä kohdentamaton kohdennus on sellainen kohdennus, joka on kohdennettu ryhmän jäsenelle **NULL** ja resurssille **NULL**. Kohdentamattomia kohdennuksia voi tapahtua muutamissa tapauksissa:

- Jos tehtävä on luotu, mutta sitä ei ole vielä kohdennettu millekään ryhmän jäsenelle, kohdentamaton kohdennus luodaan aina. 
- Jos kaikki tehtävään kohdennetut henkilöt poistetaan, kohdentamaton kohdennus luodaan uudelleen kyseiselle tehtävälle.

## <a name="scheduling-fields-on-the-project-task-entity"></a>Projekti tehtävä -entiteetin aikataulutuskentät

Kentät **msdyn\_projecttask**-entiteetissä ovat vanhentuneet tai siirretty **msdyn\_resourceassignment**-entiteettiin, tai niihin viitataan nyt **msdyn\_projectteam**-entiteetissä (**Projektiryhmän jäsen**).

| Vanhentunut kenttä kohteessa msdyn\_projecttask (Projektitehtävä) | Uusi kenttä kohteessa msdyn\_resourceassignment (Resurssin kohdennus) | Kommentti |
|---|---|---|
| msdyn\_assignedresources | Ei ole | |
| msdyn\_assignedteammembers | Ei ole | |
| msdyn\_numberofresources | Ei ole | |
| msdyn\_scheduledhours | Ei ole | |
| msdyn\_effortcontour | msdyn\_plannedwork | JavaScript Object Notation (JSON) -tietorakenteen, joka on tallennettu kenttään, muoto on muuttunut. |

## <a name="schedule-contour"></a>Aikataulun muoto

Aikataulun muoto on tallennettu **Suunniteltu työ** -kenttään (**msdyn\_plannedwork**) jokaisessa **Resurssin kohdennus** -entiteetissä (**msdyn\_resourceassignment**).

### <a name="structure"></a>Rakenne

Aikataulu muodon uusi rakenne koostuu joustavista aikaviipaleista, jotka on määritetty kullekin aikataulun päivälle. Kullakin aikaviipaleella on seuraavat ominaisuudet:

- **Aloitus** – päivän työajan alkamisaika projektikalenterin mukaan.
- **Lopetus** – päivän työajan päättymisaika projektikalenterin mukaan.
- **Tunnit** – päivälle määritettyjen tuntien määrä.

**Esimerkki**

Tässä esimerkissä käytetään projektikalenteria, jossa työpäivä on UTC-8 aikavyöhykkeellä klo 9.00-17.00.

```json
[{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":8},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":8},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":2}]
```

### <a name="auto-scheduling-and-manual-scheduling"></a>Automaattinen aikataulutus ja manuaalinen aikataulutus

Jos tehtävä on aikataulutettu automaattisesti, tunnit on ladattu etualalle ja tehtävän kesto voi pienentyä.

**Esimerkki**

Seuraava tehtävä on ajoitettu automaattisesti 18 tunniksi kolmen päivän ajaksi (3. joulukuuta 2018 - 5. joulukuuta 2018).

```json
[{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":8},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":8},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":2}]
```

Jos tehtävä on aikataulutettu manuaalisesti, tunnit jaetaan tasaisesti kaikille päivämäärille.

**Esimerkki**

Seuraava tehtävä on ajoitettu manuaalisesti 18 tunniksi kolmen päivän ajaksi (3. joulukuuta 2018 - 5. joulukuuta 2018).

```json
[{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":6},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":6},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":6}]
```

### <a name="assignment-unit"></a>Kohdennusyksikkö

Kohdennusyksikkö on vanhentunut PSA 3.x:ssä. Tehtävien työtunnit jaetaan nyt yhtä päivää kohden kaikkien määritettyjen resurssien kesken.

**Esimerkki**

Tässä esimerkissä tehtävälle on määritetty kaksi resurssia, ja se ajoitetaan automaattisesti 36 tunniksi kolmen päivän ajaksi (3. joulukuuta 2018 - 5. joulukuuta 2018).

- Kohdennus 1:

    ```json
    [{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":8},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":8},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":2}]
    ```

- Kohdennus 2:

    ```json
    [{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":8},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":8},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":2}]
    ```

## <a name="pricing-dimensions"></a>Hinnoitteludimensiot

PSA 3.x:ssa resurssikohtaiset hinnoitteludimensiokentät (kuten **Rooli** ja **Organisaatioyksikkö**) on poistettu **msdyn\_projecttask**-entiteetistä. Nämä kentät ovat nyt saatavilla vastaavassa projektiryhmän jäsenessä (**msdyn\_projectteam**) resurssikohdennuksessa (**msdyn\_resourceassignment**), kun projektin arviot on luotu. Uusi kenttä, **msdyn\_organizationalunit**, on lisätty **msdyn\_projectteam**-entiteettiin.

| Vanhentunut kenttä kohteessa msdyn\_projecttask (Projektitehtävä) | Kenttä kohteesta msdyn\_projectteam (Projektiryhmän jäsen), jota käytetään sen tilalla |
|---|---|
| msdyn\_resourcecategory | msdyn\_resourcecategory |
| msdyn\_organizationalunit | msdyn\_organizationalunit |

## <a name="contours"></a>Muodot

Hinnoittelun ja arvioiden muotokentät ovat vanhentuneet **msdyn\_projecttask**-entiteetissä. Ne on siirretty **msdyn\_resourceassignment**-entiteettiin.

| Vanhentunut kenttä kohteessa msdyn\_projecttask (Projektitehtävä) | Uusi kenttä kohteessa msdyn\_resourceassignment (Resurssin kohdennus) |
|---|---|
| msdyn\_costestimatecontour | msdyn\_plannedcostcontour |
| msdyn\_salesestimatecontour | msdyn\_plannedsalescontour |

Seuraavat kentät on lisätty **msdyn\_resourceassignment**-entiteettiin:

* msdyn\_plannedcost
* msdyn\_plannedsales

Seuraavat suunniteltujen, toteutuneiden ja jäljellä olevien kustannusten ja myynnin kentät ovat muuttumattomina **msdyn\_projecttask**-entiteetissä:

* msdyn\_plannedcost
* msdyn\_plannedsales
* msdyn\_actualcost
* msdyn\_actualsales
* msdyn\_remainingcost
* msdyn\_remainingsales


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
