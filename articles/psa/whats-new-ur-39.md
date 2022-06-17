---
title: Uutuudet ja muutokset Project Service Automation -päivitysjulkaisussa 39, V3
description: Tässä artikkelissa on lueteltu ominaisuudet ja korjaukset, jotka ovat saatavissa Microsoft Dynamics 365 Project Service Automation -päivitysjulkaisussa 39, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 01/20/2022
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
ms.openlocfilehash: d5b5938762d98acaead9e26c47bce07e0059faf6
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8922448"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-39-v3"></a>Uutuudet ja muutokset Project Service Automation -päivitysjulkaisussa 39, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Meillä on ilo esitellä Microsoft Dynamics 365 Project Service Automation -sovelluksen uusin päivitys. Tämä julkaisu sisältää joitakin tärkeitä parannuksia laatuun, tehokkuuteen ja käytettävyyteen. Se on yhteensopiva Dynamics 365 9.x -version kanssa. Päivitä tähän versioon asentamalla päivitys Dynamics 365 -hallintakeskuksen online-ratkaisujen sivulta. Lisätietoja: [Ensisijaisen ratkaisun asentaminen, päivittäminen tai poistaminen](/power-platform/admin/install-remove-preferred-solution).

Tässä artikkelissa on luettelo ominaisuuksista ja korjauksista, jotka ovat uusia tai muuttuneita Project Service Automationin päivitysjulkaisussa 39, V3. Tällä versiolla on koontinumero V3.10.60.170 ja se on ollut yleisesti saatavilla itsepalvelupäivityksenä tammikuusta 2022 lähtien.

## <a name="update-release-39"></a>Päivitysjulkaisu 39

### <a name="bug-fixes"></a>Ohjelmavirhekorjauksia

Seuraavat ongelmat on korjattu.

**Yhteiset**

- Arabian kielen käännöstä varten sivustokarttaan on tehty useita parannuksia.

**Projektinhallinta**

- Virhe, kun vaihdat projektin projektipäälliköksi käyttäjän, joka on jo projektiryhmän jäsen.

**Myynti**

- **Projektisopimuksen hinnasto** on virheellinen, kun hinnasto luodaan automaattisesti. 
- Hinnaston voimassaolon päivämääriä ei noudateta, kun hinnastoa käytetään projektiparametrissa.
- Sopimusyksiköllä ei ehkä ole oikeaa oletusarvoa muokattaessa kahta erillistä tarjousta.