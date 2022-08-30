---
title: Uutuudet ja muutokset Project Service Automation -päivitysjulkaisussa 37, V3
description: Tässä artikkelissa on lueteltu ominaisuudet ja korjaukset, jotka ovat saatavissa Microsoft Dynamics 365 Project Service Automation -päivitysjulkaisussa 37, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 11/01/2021
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
ms.openlocfilehash: bdbb125b4f41bb9970f5bd8a01cf0bb863c34738
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8922494"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-37-v3"></a>Uutuudet ja muutokset Project Service Automation -päivitysjulkaisussa 37, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Meillä on ilo esitellä Microsoft Dynamics 365 Project Service Automation -sovelluksen uusin päivitys. Tämä julkaisu sisältää joitakin tärkeitä parannuksia laatuun, tehokkuuteen ja käytettävyyteen. Se on yhteensopiva Dynamics 365 9.x -version kanssa. Päivitä tähän versioon asentamalla päivitys Dynamics 365 -hallintakeskuksen online-ratkaisujen sivulta. Lisätietoja: [Ensisijaisen ratkaisun asentaminen, päivittäminen tai poistaminen](/power-platform/admin/install-remove-preferred-solution).

Tässä artikkelissa on luettelo ominaisuuksista ja korjauksista, jotka ovat uusia tai muuttuneita Project Service Automationin päivitysjulkaisussa 37, V3. Tämä versio sisältää koontiversion numero V3.10.58.120 ja on yleisesti saatavilla itsepäivityksessä marraskuussa 2021.

## <a name="update-release-37"></a>Päivitysjulkaisu 37

### <a name="bug-fixes"></a>Ohjelmavirhekorjauksia

Seuraavat ongelmat on korjattu.

**Aika ja kulu**
- Käyttäjät eivät voi poistaa aikamerkintää tyhjentämällä solua.
- **Omat epäonnistuneet hyväksynnät** -näkymä sisältää vain projektin hyväksynnät, joiden tila on **Lähetetty**.

**Projektinhallinta**
- Käyttäjät saavat tyhjäviittauksen poikkeusvirheen avattaessa projektia Microsoftin pöytätietokoneen apuohjelmassa, jos projektiryhmän jäsenen sijainnin nimi on tyhjä.
- **Projektitehtävät**-sivulla ei ole **Tallenna**-painiketta, joten käyttäjät eivät voi tallentaa tehtävätietueisiin tehtyjä muutoksia.
- Käyttäjät eivät voi poistaa projektia, jonka tila on **Voitettu**.

**Myynti**
- **Projekti**-sivun **Valuutta**-kenttä päivittyy vastaamaan käytössä ollutta mallin valuuttaa.
- Kustannus lasketaan virheellisesti tehtäville, joissa on useita valuuttoja.