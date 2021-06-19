---
title: Project Service Automationin yleiskatsaus
description: Tässä aiheessa on tietoja Dynamics 365 Project Service Automationin Dynamics 365 Financeen integroinnin ratkaisusta.
author: ruhercul
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: ruhercul
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: ruhercul
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5ca459b99881b612e4656be112c8a2e420b4196e
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/10/2021
ms.locfileid: "6005877"
---
# <a name="project-service-automation-overview"></a>Project Service Automationin yleiskatsaus

[!include[banner](../includes/banner.md)]
[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Project Service Automationin integrointiratkaisua Financeen käyttää tietojen integrointitoimintoa tietojen synkronointiin Dynamics 365 Financen ja Dynamics 365 Project Service Automationin eri esiintymien välillä Common Data Servicen kautta. Tietojen integrointitoiminnossa käytettävissä olevat integrointimallit mahdollistaa projektien, projektisopimusten, projektisopimusten rivien, projektisopimusten rivien välitavoitteiden, projektitehtävien, kulutapahtumaluokkien, työaika-arvioiden ja kuluarvioiden vuon Project Service Automationista Financeen.

> [!NOTE]
> - Jos käytössäsi on versio 7.3.0, sinun täytyy asentaa tietokanta 4074835. Sen jälkeen voit integroida kiinteähintaisia projekteja.
> - Jos käytössäsi on versio 7.3.0 ja tuot maksutapahtumia Project Service Automationin kautta, sinun täytyy asentaa tietokanta 4345320, jotta voit lisätä kyseiset maksut projektilaskuun.
> - Jos käytät versiota 8.0 voit käyttää projektitehtävien integrointia, kulutapahtumien luokkia, työaika-arvioita, kuluarvioita ja toimintojen lukitusta.
> - Jos käytössäsi on versio 8.0.1 tai uudempi, voit synkronoida toteutuneet.

Ennen kuin voit integroida Project Service Automation Financeen, sinun täytyy määrittää Project Service Automation -integroinnin parametrit. Lisätietoja [Project Service Automation -integroinnin parametrit](PSA-parameters.md).

Tämä integrointiratkaisu mahdollistaa suoran synkronoinnin seuraavissa tilanteissa:

- Projektisopimusten ylläpitäminen Project Service Automationissa ja suora synkronointi Project Service Autiomationista Financeen.
- Projektien luominen Project Service Automationissa ja suora synkronointi Project Service Autiomationista Financeen.
- Projektisopimusten rivien ylläpitäminen Project Service Automationissa ja suora synkronointi Project Service Autiomationista Financeen.
- Projektisopimusten rivien välitavoitteiden ylläpitäminen Project Service Automationissa ja suora synkronointi Project Service Autiomationista Financeen.
- Projektitehtävien ylläpitäminen Project Service Automationissa ja suora synkronointi Project Service Autiomationista Financeen.
- Kulutapahtumaluokkien ylläpitäminen Financesta ja suora synkronointi Financesta Project Service Autiomationiin.
- Projektien työaikaennusteiden luominen Project Service Automationissa ja suora synkronointi Project Service Autiomationista Financeen.
- Projektien kuluennusteiden luominen Project Service Automationissa ja suora synkronointi Project Service Autiomationista Financeen.
- Projektin toteutuneiden työaikojen, kulujen ja maksujen luominen Project Service Automationissa ja projektitapahtumien luominen Project Service Automationin integroinnin kirjauskansioon, jotta ne voidaan kirjata Financeen.

## <a name="data-synchronization"></a>Tietojen synkronointi

Seuraavassa kuvassa on esitetty, miten tiedot synkronoidaan osana integrointia Project Service Automationin ja Financen välillä.

> [!NOTE]
> Kaikki mallit eivät ole tällä hetkellä käytettävissä. Mallit julkaistaan, kun ne ovat valmiit.

[![Project Service Automationin integrointi Financeen](./media/PSA-integration.png)](./media/PSA-integration.png)

## <a name="system-requirements-for-finance"></a>Financen järjestelmävaatimukset

Jotta voit käyttää Project Service Automationin Financeen integroinnin ratkaisua, sinun on asennettava Enterprise Edition 7.3 ja Platform Update 12 tai uudempi.

## <a name="system-requirements-for-project-service-automation"></a>Project Service Automationin järjestelmävaatimukset

Jotta voit käyttää Project Service Automationin Financeen integroinnin ratkaisua, sinun on asennettava seuraavat osat:

- Dynamics 365 Project Service Automation -versio 9.0.0.0 tai uudempi
- Dynamics 365 Salesin Prospect to Cash -ratkaisun versio 1.14.0.0 (v14) tai uudempi
- Dynamics 365 Project Service Automationin Project Service Automationista Financeen versio 1.0.0.0 tai uudempi

## <a name="install-the-project-service-automation-to-finance-integration-solution-in-your-project-service-automation-instance"></a>Project Service Automationista Financeen integroinnin ratkaisun asentaminen Project Service Automationin esiintymään

Lataa Project Service Automationista Financeen integroinnin ratkaisu [Microsoft Download Centeristä](https://www.microsoft.com/download/details.aspx?id=57016) ja noudata ratkaisuun sisältyviä ohjeita.


[!INCLUDE[footer-include](../includes/footer-banner.md)]