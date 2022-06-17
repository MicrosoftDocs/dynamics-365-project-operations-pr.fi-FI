---
title: Projektikalenterien määrittäminen
description: Tässä artikkelissa on tietoja siitä, miten kalenterimallia käytetään projektissa projektin aikataulun seuraamiseen.
author: ruhercul
ms.date: 02/05/2021
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: ruhercul
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: e195cdb0dc5acc2ea816fadce40811675a855de2
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8933534"
---
# <a name="define-project-calendars"></a>Projektikalenterien määrittäminen

_**Koskee:** Project Operationsin resurssiin / muuhun kuin resurssiin perustuvia skenaarioita, Lite-käyttöönotto-kaupasta proformalaskutukseen_

Projektia voi luoda ja hallita käyttämällä projektissa kalenterimallia. Kalenterimalli määrittää seuraavat projektimääritteet:

- Työaika, mukaan lukien alkamis- ja päättymisaika
- Työpäivät
- Kalenteripoikkeukset, kuten muut kuin työpäivät

Projektiin käytettävä kalenterimalli on kopio organisaation asetuksissa määritetystä kalenterimallista.

> [!NOTE]
> Jos muutat kalenterimallia, muutokset eivät leviä projektin työaikaan. Jotta projektin työaikaa voidaan muuttaa, on otettava käyttöön uusi malli.

Organisaation kalenterimallin luomiselle on kaksi tärkeää avainvaatimusta:

- Määritä mallin haluttu työaika käyttämällä uutta tai aiemmin luotua varattavissa olevaa resurssia.
- Luo uusi kalenterimalli ja liitä malli varattavaan resurssiin.

**Määritä mallin työaika**

1. Siirry kohtaan **Resurssit** \> **Resurssit**.
2. Luo uusi resurssi, jota haluat käyttää kalenterimallissa, tai valitse aiemmin luotu resurssi.
3. Valitse **resurssin työaika** -välilehti ja noudata ohjeita kohdasta [Resurssin työaikojen määrittäminen](/dynamics365/field-service/set-work-hours-resource) kalenterisääntöjen määrittämiseksi.

**Luo uusi kalenterimalli**

1. Valitse **Asetukset** \> **Kalenterimalli**.
2. Valitse **Uusi** ja kirjoita nimi, kuvaus ja malliresurssi.

> [!NOTE]
> Kun resurssiin viitataan kalenterimallissa, kalenterimalliin liitetään resurssin kalenterin kopio. Jos kopioidun mallin työajat muuttuvat, nämä muutokset eivät levitä kalenterimalliin.

Voit nyt liittää työmallin projektin kalenterimalliin.


[!INCLUDE[footer-include](../includes/footer-banner.md)]

