---
title: Projektilaskutuksen integrointi
description: Tässä artikkelissa on tietoja Project Operationsin asiakaslaskutuksen kaksoiskirjoituksen integroinnista.
author: sigitac
ms.date: 04/26/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 5ee2d78f1ca1d78f6909d9995a92ac301f06d6a6
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8912098"
---
# <a name="project-invoice-integration"></a>Projektilaskutuksen integrointi

Tässä artikkelissa on tietoja Project Operationsin asiakaslaskutuksen kaksoiskirjoituksen integroinnista.

Project Operationsissa projektipäällikkö hallitsee projektin laskutuksen taustalokia ja luo proformalaskun asiakkaalle Microsoft Dataversessä. Tämän proformalaskun perusteella myyntireskontran hoitaja tai projektin kirjanpitäjä luo asiakkaalle laskun. Kaksoiskirjoituksen integrointi varmistaa, että proformalaskun tiedot synkronoidaan talous- ja toimintosovelluksiin. Kun asiakkaalle suunnattu lasku on julkaistu, järjestelmä päivittää projektin toteutuneet tiedot Dataverseen kirjanpidon tiedoista. Seuraava kuva antaa korkean tason käsitteellisen yleiskatsauksen tästä integraatiosta.

   ![Projektilaskutuksen integrointi.](./media/DW5Invoicing.png)

Kun projektipäällikkö on vahvistanut proformalaskun Dataversessa, proformalaskun otsikkotiedot synkronoidaan talous- ja toimintosovelluksiin käyttämällä kaksoiskirjoitustaulukkokarttaa **Projektilaskuehdotus V2 (laskut)**. Tämä on yksisuuntainen integrointi Dataversesta talous- ja toimintosovelluksiin. Projektilaskuehdotusten luomista tai poistamista suoraan talous- ja toimintosovelluksissa ei tueta.

Laskun vahvistus Dataversessä käynnistää myös liiketoimintalogiikan, joka luo laskutukseen liittyviä tietueita **Toteutuneet**-kohteeseen. Nämä tietueet synkronoidaan talous- ja toimintosovelluksiin käyttämällä kaksoiskirjoitustaulukkokarttaa **Project Operations -integroinnin toteutuneet arvot (msdyn\_actuals)**. Lisätietoja on aiheissa [Projektin arviot ja todelliset kulut](resource-dual-write-estimates-actuals.md). 

Projektilaskun ehdotusrivit luodaan jaksottaisen prosessin avulla, **Tuo valmistelusta**. Tämä prosessi perustuu **Toteutuneet valmistelut** -taulukon laskutettuihin myyntitietoihin, Lisätietoja on ohjeaiheessa [Projektilaskuehdotusten hallinta](../invoicing/format-update-project-invoice-proposals.md#create-project-invoice-proposals). 
