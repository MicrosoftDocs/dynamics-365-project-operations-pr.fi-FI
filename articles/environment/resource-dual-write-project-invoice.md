---
title: Projektilaskutuksen integrointi
description: Tässä aiheessa on tietoja Project Operationsin asiakaslaskutuksen kaksoiskirjoituksen integroinnista.
author: sigitac
ms.date: 04/26/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 37549080d76e3bffd7cb002aee8e3c46b9eeb18e3cec915cd971881b69747534
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/06/2021
ms.locfileid: "6993237"
---
# <a name="project-invoice-integration"></a>Projektilaskutuksen integrointi

Tässä aiheessa on tietoja Project Operationsin asiakaslaskutuksen kaksoiskirjoituksen integroinnista.

Project Operationsissa projektipäällikkö hallitsee projektin laskutuksen taustalokia ja luo proformalaskun asiakkaalle Microsoft Dataversessä. Tämän proformalaskun perusteella myyntireskontran hoitaja tai projektin kirjanpitäjä luo asiakkaalle laskun. Kaksoiskirjoituksen integrointi varmistaa, että proformalaskun tiedot synkronoidaan Finance and Operations -sovelluksiin. Kun asiakkaalle suunnattu lasku on julkaistu, järjestelmä päivittää projektin toteutuneet tiedot Dataverseen kirjanpidon tiedoista. Seuraava kuva antaa korkean tason käsitteellisen yleiskatsauksen tästä integraatiosta.

   ![Projektilaskutuksen integrointi.](./media/DW5Invoicing.png)

Kun projektipäällikkö on vahvistanut proformalaskun Dataversessä, proformalaskun otsikkotiedot synkronoivat Finance and Operations -sovellukset käyttämällä kaksoiskirjoitustaulukkokarttaa **Projektilaskuehdotus V2 (laskut)**. Tämä on yksi tapa integroida Dataversestä Finance and Operations -sovelluksiin. Projektilaskuehdotusten luomista tai poistamista suoraan Finance and Operations -sovelluksista ei tueta.

Laskun vahvistus Dataversessä käynnistää myös liiketoimintalogiikan, joka luo laskutukseen liittyviä tietueita **Toteutuneet**-kohteeseen. Nämä tiedot synkronoidaan Finance and Operationsiin käyttämällä kaksoiskirjoitustaulukkokarttaa, **Project Operationsin integrointien toteutuneet (msdyn\_actuals)**. Lisätietoja on aiheissa [Projektin arviot ja todelliset kulut](resource-dual-write-estimates-actuals.md). 

Projektilaskun ehdotusrivit luodaan jaksottaisen prosessin avulla, **Tuo valmistelusta**. Tämä prosessi perustuu **Toteutuneet valmistelut** -taulukon laskutettuihin myyntitietoihin, Lisätietoja on ohjeaiheessa [Projektilaskuehdotusten hallinta](../invoicing/format-update-project-invoice-proposals.md#create-project-invoice-proposals). 
