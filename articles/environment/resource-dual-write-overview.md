---
title: Project Operationsin kaksoiskirjoituksen integrointi
description: Tässä aiheessa on yleiskatsaus Project Operationsin kaksoiskirjoituksen integroinnista.
author: sigitac
ms.date: 04/28/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.custom: intro-internal
ms.openlocfilehash: b65c40e8aaa9524c1c634738dadd23f21e86e2ec095c47bc849467c8806addbc
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/06/2021
ms.locfileid: "7007907"
---
# <a name="project-operations-dual-write-integration-overview"></a>Project Operationsin kaksoiskirjoituksen integroinnin yleiskatsaus

_**Käytetään:** Project Operationsin resursseihin ja ei-varastoitaviin perustuvissa skenaarioissa_

Project Operations käyttää [kaksoiskirjoitustoimintoja](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-home-page) sykronoidakseen tietoa Microsoft Dataversen ja Dynamics 365 Financen välillä.

Seuraavassa kuvassa on esitetty, miten tiedot synkronoidaan osana tätä Dataversen ja Financen välistä integrointia.

![Project Operationsin tietovuon yleiskatsaus.](./media/ProjectOperationsFlows.jpg)

Project Operations Dataversessä tarjoaa uudenaikaisen käyttöliittymän ja helpon koodittoman ja vähäkoodisen laajennettavuuden käyttämällä Power Platformin ominaisuuksia. Projektipäälliköt, henkilöstöpäälliköt, projektiryhmän jäsenet ja muut toimiston jäsenet suorittavat tehtävänsä Project Operationsissa Dataversessä.

Financen Project Operations tukee projektien kirjanpitoa ja tuottojen kirjaamista. Project Operations liittää Financen rahoituskehykseen arvonlisäveron laskemista, valuuttakursseja, taloudellisen dimension raportointia ja muuta varten. Projektin kirjanpitäjän kokemukset perustuvat enimmäkseen Financeen.

Project Operationsin integrointi koostuu seuraavasta komponenttien integroinnista:


- [Project Operationsin määritysten ja määritystietojen integrointi](resource-dual-write-setup-integration.md) 
- [Projektin arviot ja toteutuneet kulut](resource-dual-write-estimates-actuals.md)
- [Projektin laskut](resource-dual-write-project-invoice.md)
- [Kulujen hallinta](resource-dual-write-expense.md)
- [Toimittajan lasku](resource-dual-write-vendor-invoice.md)
