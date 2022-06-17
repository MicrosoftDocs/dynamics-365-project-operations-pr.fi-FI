---
title: Uutuudet ja muutokset Project Service Automation -päivitysjulkaisussa 41, V3
description: Tässä artikkelissa on lueteltu ominaisuudet ja korjaukset, jotka ovat saatavissa Microsoft Dynamics 365 Project Service Automation -päivitysjulkaisussa 41, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 03/07/2022
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
ms.openlocfilehash: 8625ae16e45da30614b3a3eec44193bee0c0b36f
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8930544"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-41-v3"></a>Uutuudet ja muutokset Project Service Automation -päivitysjulkaisussa 41, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Meillä on ilo esitellä Microsoft Dynamics 365 Project Service Automation -sovelluksen uusin päivitys. Tämä julkaisu sisältää joitakin tärkeitä parannuksia laatuun, tehokkuuteen ja käytettävyyteen. Se on yhteensopiva Dynamics 365 9.x -version kanssa. Päivitä tähän versioon asentamalla päivitys Dynamics 365 -hallintakeskuksen online-ratkaisujen sivulta. Lisätietoja: [Ensisijaisen ratkaisun asentaminen, päivittäminen tai poistaminen](/power-platform/admin/install-remove-preferred-solution).

Tässä artikkelissa on luettelo ominaisuuksista ja korjauksista, jotka ovat uusia tai muuttuneita Project Service Automationin päivitysjulkaisussa 41, V3. Tällä versiolla on koontinumero V3.10.62.162 ja se on ollut yleisesti saatavilla itsepalvelupäivityksenä maaliskuusta 2022 lähtien.

## <a name="update-release-41"></a>Päivitysjulkaisu 41

### <a name="bug-fixes"></a>Ohjelmavirhekorjauksia

Seuraavat ongelmat on korjattu.

**Projektinhallinta**
- Kun yrität luoda projektia työpöytäapuohjelmassa luotuun projektiin perustuvasta mallista, näyttöön tulee seuraava virhe: "Resurssin tehtävän suunnitellut työtehtävät -kentän tarkistus: jokaisen resurssin määritysajan osan päättymispäivä ei saa olla aikaisempi kuin sen alkamispäivä".

**Aika ja kulu**
- Kun yrität poistaa aikamerkinnän, näyttöön tulee seuraava virhesanoma: "ISV-koodista tapahtuu odottamaton virhe".

**Myynti**
- Kun luot laskun kiinteän hinnan välitavoitteesta, **Kuvaus**- ja **Ulkoinen kuvaus** -kenttiä ei täytetä. 
