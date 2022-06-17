---
title: Uutuudet ja muutokset Project Service Automation -päivitysjulkaisussa 40, V3
description: Tässä artikkelissa on lueteltu ominaisuudet ja korjaukset, jotka ovat saatavissa Microsoft Dynamics 365 Project Service Automation -päivitysjulkaisussa 40, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 01/31/2022
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
ms.openlocfilehash: dca7f340b8d544b183aa0390ac3c11a38f536ed0
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8912788"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-40-v3"></a>Uutuudet ja muutokset Project Service Automation -päivitysjulkaisussa 40, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Meillä on ilo esitellä Microsoft Dynamics 365 Project Service Automation -sovelluksen uusin päivitys. Tämä julkaisu sisältää joitakin tärkeitä parannuksia laatuun, tehokkuuteen ja käytettävyyteen. Se on yhteensopiva Dynamics 365 9.x -version kanssa. Päivitä tähän versioon asentamalla päivitys Dynamics 365 -hallintakeskuksen online-ratkaisujen sivulta. Lisätietoja: [Ensisijaisen ratkaisun asentaminen, päivittäminen tai poistaminen](/power-platform/admin/install-remove-preferred-solution).

Tässä artikkelissa on luettelo ominaisuuksista ja korjauksista, jotka ovat uusia tai muuttuneita Project Service Automationin päivitysjulkaisussa 40, V3. Tämän version koontiversionumero on V3.10.61.61 ja se on yleisesti saatavilla omatoimipäivityksenä helmikuussa 2022.

## <a name="update-release-40"></a>Päivitysjulkaisu 40

### <a name="features"></a>Ominaisuudet
Päivityksen vaihe 1 Project Service Automationista Project Operations - Liteen julkaistaan helmikuussa 2022 kaikille asiakkaille. Tarkista kelpoisuus: [Päivittäminen Project Service Automationista Project Operationsiin](upgrade-project-operations-non-stocked.md). Jos sovellus ei näy Power Platform -hallintakeskuksessa ilmentymässäsi, ota yhteyttä tukeen ja pyydä, että väliversio otetaan käyttöön ympäristöissäsi. Pyynnössä on oltava luettelo ympäristötunnuksista, joissa väliversio on otettava käyttöön.

### <a name="bug-fixes"></a>Ohjelmavirhekorjauksia

Seuraavat ongelmat on korjattu.

**Aika ja kulu**
- Muistiinpanomerkintä puuttuu, kun aikamerkintä hylätään tai peruutetaan. 

**Myynti**

- Kun päivität kustannus- tai myyntiarvioita käyttämällä käyttövalmiita laajennuksia, sinulla on virheellisesti oikeus lähettää JSON-tietoja, jotka eivät ole kelvollisia käyttöliittymän ulkopuolella.
- Kun päivität tarjousrivejä käyttämällä pikanäkymää, voit aktivoida tarjouksia.
