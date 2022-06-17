---
title: Työtuntimallien luominen
description: Tässä artikkelissa käsitellään työtuntimallin luontia Project Servicessä.
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.reviewer: johnmichalak
ms.openlocfilehash: 8f3ac17a29e79f86f7c3ce127edb4b02ca63ea04
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8916054"
---
# <a name="create-a-work-hours-template-project-service"></a>Luo työtuntimalli (Project Service)

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-3x.md)]

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


### <a name="see-also"></a>Katso myös  
 [Resurssien määrittäminen](../psa/set-up-resources.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
