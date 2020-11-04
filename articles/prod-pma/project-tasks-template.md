---
title: Synkronoi projektitehtäviä suoraan Project Service Automationista Finance and Operationsiin
description: Tässä aiheessa kuvataan malli ja sen pohjana oleva tehtävä, jota käytetään projektitehtävien synkronoimiseen suoraan Microsoft Dynamics 365 Project Service Automationista Dynamics 365 Financeen.
author: Yowelle
manager: AnnBe
ms.date: 07/20/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.3.0
ms.openlocfilehash: 0383607a07def6c21562bf4b0893fe3ce3db6a04
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/16/2020
ms.locfileid: "4075330"
---
# <a name="synchronize-project-tasks-directly-from-project-service-automation-to-finance-and-operations"></a>Synkronoi projektitehtäviä suoraan Project Service Automationista Finance and Operationsiin

[!include[banner](../includes/banner.md)]

Tässä aiheessa kuvataan malli ja sen pohjana oleva tehtävä, jota käytetään projektitehtävien synkronoimiseen suoraan Dynamics 365 Project Service Automationista Dynamics 365 Financeen.

> [!NOTE]
> - Projektitehtävien integrointi, kulutapahtumien luokat, työaika-arviot, kuluarviot ja toimintojen lukitus ovat käytettävissä versiossa 8.0.
> - Jos käytössäsi on Enterprise Edition 7.3.0, kun olet asentanut tietokannan 4132657 ja tietokannan 4132660, voit integroida malleja projektitehtävien, kulutapahtumien luokkien, tuntiarvioiden, kuluarvioiden ja toteutuneiden arvojen sekä toimintojen lukitsemisen määrittämiseksi. Jos sinun on nollattava kirjanpidollinen jako, suosittelemme myös tietokannan 4131710 asentamista.
> - Toteutuneiden arvojen integrointi on käytettävissä alkaen versiosta 8.0.1 tai myöhempi.

## <a name="data-flow-for-project-service-automation-to-finance"></a>Tietovuo Project Service Automationista Financeen

Project Service Automationin integrointiratkaisua Financeen käyttää tietojen integrointitoimintoa tietojen synkronointiin Project Service Automationin ja Financen eri esiintymien välillä. Tietojen integrointitoiminnossa käytettävissä oleva integrointimalli mahdollistavaa projektitehtävien tietovuon Project Service Automationista Financeen.

Seuraavassa kuvassa on esitetty, miten tiedot synkronoidaan Project Service Automationin ja Financen välillä.

[![Tietovuo Project Service Automationin Financeen integroinnissa](./media/ProjectTasksFlow.png)](./media/ProjectTasksFlow.png)

## <a name="template-and-task"></a>Malli ja tehtävä

Jos haluat käyttää mallia, valitse Microsoft Power Appsin hallintakeskuksessa **Projektit** ja sitten oikeassa yläkulmassa **Uusi projekti** valitaksesi julkisia malleja.

Seuraavaa mallia ja pohjana olevaa tehtävää käytetään projektitehtävien synkronoimiseen Project Service Automationista Financeen:

- **Tietojen integroinnin mallin nimi:** Projektitehtävät (PSA:sta Fin:iin ja Ops:iin)
- **Projektin tehtävän nimi:** Projektitehtävä

Ennen kuin projektitehtäviä voi synkronoitava, on synkronoitava projektisopimukset ja projektit.

## <a name="entity-set"></a>Entiteettijoukko

| Project Service Automation | Rahoitus                             |
|----------------------------|-------------------------------------|
| Projektitehtävät              | Projektitehtävän integroinnin entiteetti |

## <a name="entity-flow"></a>Entiteettivuo

Projektitehtäviä hallitaan Project Service Automationissa, ja ne synkronoidaan Financeen projektiaktiviteetteina.

## <a name="prerequisites-and-mapping-setup"></a>Edellytykset ja yhdistämismääritykset

Ennen kuin projektitehtäviä voi synkronoitava, on synkronoitava projektisopimukset ja projektit.

## <a name="power-query"></a>Power Query

Sinun on käytettävä Microsoft Power Query for Excel -isäosaa suodattamaan tietoja, jos seuraava ehto täyttyy:

- Projektitehtävässä on resurssikohtaisia tietueita.

Jos sinun on käytettävä Power Queryä, noudata seuraavaa ohjetta:

- Projektitehtävien (PSA:sta Fin:iin ja Ops:iin) on oletussuodatin, joka jättää resurssikohtaiset tietueet pois projektitehtävästä määrittämällä **IsLineTask** -suodattimen arvoksi **Epätosi**. Jos luot oman mallin, tämä suodatin on lisättävä.

## <a name="template-mapping-in-data-integration"></a>Mallien yhdistämismääritys tietojen integroinnissa

Seuraavassa kuvissa on esimerkki mallitehtävien yhdistämismäärityksestä tietojen integroinnissa. Yhdistämismäärityksessä näytetään kenttätiedot, jotka synkronoidaan Project Service Automationista Financeen.

[![Yhdistelmämääritysmalli](./media/ProjectTasksMapping.png)](./media/ProjectTasksMapping.png)
