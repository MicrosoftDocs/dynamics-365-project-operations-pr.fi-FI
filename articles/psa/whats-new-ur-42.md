---
title: Uutuudet ja muutokset Project Service Automation -päivitysjulkaisussa 42, V3
description: Tässä artikkelissa on lueteltu ominaisuudet ja korjaukset, jotka ovat saatavissa Microsoft Dynamics 365 Project Service Automation -päivitysjulkaisussa 42, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 04/05/2022
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
ms.openlocfilehash: e9911531e4acbd78db416f554c8d85c4f1fee1cf
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8912711"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-42-v3"></a>Uutuudet ja muutokset Project Service Automation -päivitysjulkaisussa 42, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Meillä on ilo esitellä Microsoft Dynamics 365 Project Service Automation -sovelluksen uusin päivitys. Tämä julkaisu sisältää joitakin tärkeitä parannuksia laatuun, tehokkuuteen ja käytettävyyteen. Se on yhteensopiva Dynamics 365 9.x -version kanssa. Päivitä tähän versioon asentamalla päivitys Dynamics 365 -hallintakeskuksen online-ratkaisujen sivulta. Lisätietoja: [Ensisijaisen ratkaisun asentaminen, päivittäminen tai poistaminen](/power-platform/admin/install-remove-preferred-solution).

Tässä artikkelissa on luettelo ominaisuuksista ja korjauksista, jotka ovat uusia tai muuttuneita Project Service Automationin päivitysjulkaisussa 42, V3. Tämän version koontiversion numero on V3.10.73.61, ja se on yleisesti saatavana itsepäivittyvänä huhtikuussa 2022.

## <a name="update-release-42"></a>Päivitysjulkaisu 42

### <a name="bug-fixes"></a>Ohjelmavirhekorjauksia

Seuraavat ongelmat on korjattu.

**Aika ja kulu**

- Kun aikataulukko hylätään, hylännyt käyttäjä tunnistetaan virheellisesti **järjestelmäksi**.
- Kun aikakirjauksia tuodaan, **Resurssiluokka**-arvo puuttuu.
- Projektin hyväksyjät voivat hyväksyä lähetetyt projektit, kun heidän käyttöoikeuksiaan ei ole määritetty erityisesti **Voi hyväksyä** -asetuksena.

**Myynti**

- Kun toteutuneet arvot kirjataan ei-päätason tehtäviin, todelliset kustannukset kootaan virheellisesti.
