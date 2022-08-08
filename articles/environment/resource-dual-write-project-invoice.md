---
title: Projektilaskutuksen integrointi
description: Tässä artikkelissa on tietoja Project Operationsin asiakaslaskutuksen kaksoiskirjoituksen integroinnista.
author: sigitac
ms.date: 04/26/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 61f16ebdbabd6545c09d8d7bd82d99b85dc09975
ms.sourcegitcommit: a798fed5c59e3fefa62cdfa42c852d529b33fd35
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/18/2022
ms.locfileid: "9029020"
---
# <a name="project-invoice-integration"></a>Projektilaskutuksen integrointi

Tässä artikkelissa on tietoja Project Operationsin asiakaslaskutuksen kaksoiskirjoituksen integroinnista.

Project Operationsissa projektipäällikkö hallitsee projektin laskutuksen taustalokia ja luo proformalaskun asiakkaalle Microsoft Dataversessä. Tämän proformalaskun perusteella myyntireskontran hoitaja tai projektin kirjanpitäjä luo asiakkaalle laskun. Kaksoiskirjoituksen integrointi varmistaa, että proformalaskun tiedot synkronoidaan talous- ja toimintosovelluksiin. Kun asiakkaalle suunnattu lasku on julkaistu, järjestelmä päivittää projektin toteutuneet tiedot Dataverseen kirjanpidon tiedoista. Seuraava kuva antaa korkean tason käsitteellisen yleiskatsauksen tästä integraatiosta.

   ![Projektilaskutuksen integrointi.](./media/DW5Invoicing.png)

Kun projektipäällikkö on vahvistanut proformalaskun Dataversessa, proformalaskun otsikkotiedot synkronoidaan talous- ja toimintosovelluksiin käyttämällä kaksoiskirjoitustaulukkokarttaa **Projektilaskuehdotus V2 (laskut)**. Tämä on yksisuuntainen integrointi Dataversesta talous- ja toimintosovelluksiin. Projektilaskuehdotusten luomista tai poistamista suoraan talous- ja toimintosovelluksissa ei tueta.

Laskun vahvistus Dataversessä käynnistää myös liiketoimintalogiikan, joka luo laskutukseen liittyviä tietueita **Toteutuneet**-kohteeseen. Nämä tietueet synkronoidaan talous- ja toimintosovelluksiin käyttämällä kaksoiskirjoitustaulukkokarttaa **Project Operations -integroinnin toteutuneet arvot (msdyn\_actuals)**. Lisätietoja on aiheissa [Projektin arviot ja todelliset kulut](resource-dual-write-estimates-actuals.md). 

Projektilaskun ehdotusrivit luodaan jaksottaisen prosessin avulla, **Tuo valmistelusta**. Tämä prosessi perustuu **Toteutuneet valmistelut** -taulukon laskutettuihin myyntitietoihin, Lisätietoja on ohjeaiheessa [Projektilaskuehdotusten hallinta](../invoicing/format-update-project-invoice-proposals.md#create-project-invoice-proposals). 
