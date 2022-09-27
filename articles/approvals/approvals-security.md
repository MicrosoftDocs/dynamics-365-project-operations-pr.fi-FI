---
title: Suojaus ja hyväksynnät
description: Tässä artikkelissa on tietoja hyväksymisten käsittelemisen suojausasetuksista Microsoft Dynamics 365 Project Operationsissa.
author: stsporen
ms.date: 08/29/2022
ms.topic: security
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: bc33f63f66bdcf1470e5d9386cfc3661774436fd
ms.sourcegitcommit: b2d05f898daa552179d67fdf4c060c93a9c66bd1
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/16/2022
ms.locfileid: "9525358"
---
# <a name="security-and-approvals"></a>Suojaus ja hyväksynnät

_**Koskee:** Project Operationsin resurssiin / muuhun kuin resurssiin perustuvia skenaarioita, Lite-käyttöönotto-kaupasta proformalaskutukseen_

Microsoft Dynamics 365 Project Operations sallii ajan, kulujen ja materiaalimerkintöjen hyväksynnän kahdella käyttöoikeusroolilla:

- Projektin hyväksyjä
- Projektin hyväksyjä Järjestelmänvalvoja

## <a name="project-approver"></a>Projektin hyväksyjä

**Projektin hyväksyjä** -käyttöoikeusrooli tarvitaan projektin ajan, kulujen ja materiaalien syötteiden hyväksymiseen. Sinulla on oltava myös liittyvien entiteettien, kuten **Projekti**-entiteettien, käyttöoikeus. Käyttöoikeuden voi määrittää joku, jolla on **projektipäällikkö**-rooli. Lisäksi sinun täytyy olla projektin ryhmän jäsen ja merkitty hyväksyjäksi.

Jos haluat hyväksyä muita kuin projektimerkintöjä, sinun on oltava lähettäjän esihenkilö.

## <a name="project-approver-admin"></a>Projektin hyväksyjä Järjestelmänvalvoja

> [!NOTE]
> [Hyväksyntäjoukot](approval-sets.md)-ominaisuus on otettava käyttöön, ennen kuin voit käyttää projektin hyväksyjän hallintatoimintoa.

**Projektin hyväksyjän järjestelmänvalvojan** käyttöoikeusrooli käyttäjät voivat ohittaa käytäntöjä ja hyväksyä kaikkien projektien merkintöjä. Tämän roolin määrittäminen ohittaa tarkistuslogiikan, joka edellyttää ryhmän jäsenyyttä ja hyväksyjäksi merkitsemistä. Sinulla on oltava myös liittyvien entiteettien, kuten **Projekti**-entiteettien, käyttöoikeus. Käyttöoikeuden voi määrittää joku, jolla on **projektipäällikkö**-rooli.

JÄRJESTELMÄN käyttäjän konteksti ohittaa vahvistukset samalla tavalla kuin projektin hyväksyjän käyttöoikeusrooli.
