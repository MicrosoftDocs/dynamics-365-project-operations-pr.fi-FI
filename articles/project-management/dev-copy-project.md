---
title: Projektimallien kehittäminen kopiointiprojektin avulla
description: Tässä aiheessa on tietoja siitä, miten projektimalleja luodaan kopioi projekti -mukautetun toiminnon avulla.
author: stsporen
manager: Annbe
ms.date: 10/07/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 0100c29873be6346614e958ef6ea0c77da2c9590
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/28/2020
ms.locfileid: "4131609"
---
# <a name="develop-project-templates-with-copy-project"></a>Projektimallien kehittäminen kopiointiprojektin avulla

_**Koskee:** Project Operationsin resurssiin / muuhun kuin resurssiin perustuvia skenaarioita, Lite-käyttöönotto-kaupasta proformalaskutukseen_

Dynamics 365 Project Operations tukee mahdollisuutta kopioida projekti ja palauttaa tehtävät takaisin roolia edustaville yleisille resursseille. Tämän toiminnon avulla asiakkaat voivat luoda perusprojektimalleja.

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

Lisätietoja oletustoiminnoista on kohdassa [Verkko-ohjelmointirajapintojen toimintojen käyttö](https://docs.microsoft.com/powerapps/developer/common-data-service/webapi/use-web-api-actions)

## <a name="specify-fields-to-copy"></a>Kopioitavien kenttien määrittäminen 
Kun toimintoa kutsutaan, **Kopioi projekti** näyttää projektinäkymän **Kopioi projekti sarakkeet**, kun haluat määrittää, mitkä kentät kopioidaan projektin kopioinnin yhteydessä.
