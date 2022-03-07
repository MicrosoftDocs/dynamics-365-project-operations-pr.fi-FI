---
title: Project Operationsin kaksoiskirjoituksen integrointi
description: Tässä aiheessa on yleiskatsaus Project Operationsin kaksoiskirjoituksen integroinnista.
author: sigitac
ms.date: 04/28/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: ce4f7bf8185e6f3f942df14d30d7b8d0a3e4444a
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/10/2021
ms.locfileid: "5998677"
---
# <a name="project-operations-dual-write-integration-overview"></a>Project Operationsin kaksoiskirjoituksen integroinnin yleiskatsaus

_**Käytetään:** Project Operationsin resursseihin ja ei-varastoitaviin perustuvissa skenaarioissa_

Project Operations käyttää [kaksoiskirjoitustoimintoja](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-home-page) sykronoidakseen tietoa Microsoft Dataversen ja Dynamics 365 Financen välillä.

Seuraavassa kuvassa on esitetty, miten tiedot synkronoidaan osana tätä Dataversen ja Financen välistä integrointia.

![Project Operationsin tietovuon yleiskatsaus](./media/ProjectOperationsFlows.jpg)

Project Operations Dataversessä tarjoaa uudenaikaisen käyttöliittymän ja helpon koodittoman ja vähäkoodisen laajennettavuuden käyttämällä Power Platformin ominaisuuksia. Projektipäälliköt, henkilöstöpäälliköt, projektiryhmän jäsenet ja muut toimiston jäsenet suorittavat tehtävänsä Project Operationsissa Dataversessä.

Financen Project Operations tukee projektien kirjanpitoa ja tuottojen kirjaamista. Project Operations liittää Financen rahoituskehykseen arvonlisäveron laskemista, valuuttakursseja, taloudellisen dimension raportointia ja muuta varten. Projektin kirjanpitäjän kokemukset perustuvat enimmäkseen Financeen.

Project Operationsin integrointi koostuu seuraavasta komponenttien integroinnista:


- [Project Operationsin määritysten ja määritystietojen integrointi](resource-dual-write-setup-integration.md) 
- [Projektin arviot ja toteutuneet kulut](resource-dual-write-estimates-actuals.md)
- [Projektin laskut](resource-dual-write-project-invoice.md)
- [Kulujen hallinta](resource-dual-write-expense.md)
- [Toimittajan lasku](resource-dual-write-vendor-invoice.md)
