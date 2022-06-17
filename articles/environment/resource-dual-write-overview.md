---
title: Project Operationsin kaksoiskirjoituksen integrointi
description: Tässä artikkelissa on yleiskatsaus Project Operationsin kaksoiskirjoituksen integroinnista.
author: sigitac
ms.date: 04/28/2021
ms.topic: overview
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: d365a036f96ff4f7b14107b43e8c6b70df0b5362
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8927968"
---
# <a name="project-operations-dual-write-integration-overview"></a>Project Operationsin kaksoiskirjoituksen integroinnin yleiskatsaus

_**Käytetään:** Project Operationsin resursseihin ja ei-varastoitaviin perustuvissa skenaarioissa_

Project Operations käyttää [kaksoiskirjoitustoimintoja](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-home-page) Microsoft Dataverse- ja Dynamics 365 Finance -tietojen synkronointiin.

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
