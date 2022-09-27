---
title: Uutuudet ja muutokset Project Service Automation -päivitysjulkaisussa 47, V3
description: Tässä artikkelissa on lueteltu ominaisuudet ja korjaukset, jotka ovat saatavissa Microsoft Dynamics 365 Project Service Automation -päivitysjulkaisussa 47, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 09/14/2022
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
ms.openlocfilehash: 08e8fa9c41bdd77d93e4d5207266115022fba1b2
ms.sourcegitcommit: 498a5d5a33c47cab788fac4215fc47662042155a
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/14/2022
ms.locfileid: "9477230"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-47-v3"></a>Uutuudet ja muutokset Project Service Automation -päivitysjulkaisussa 47, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Meillä on ilo esitellä Microsoft Dynamics 365 Project Service Automation -sovelluksen uusin päivitys. Tämä julkaisu sisältää joitakin tärkeitä parannuksia laatuun, tehokkuuteen ja käytettävyyteen. Se on yhteensopiva Dynamics 365 9.x -version kanssa. Päivitä tähän versioon asentamalla päivitys Dynamics 365 -hallintakeskuksen online-ratkaisujen sivulta. Lisätietoja: [Ensisijaisen ratkaisun asentaminen, päivittäminen tai poistaminen](/power-platform/admin/install-remove-preferred-solution).

Tässä artikkelissa on luettelo ominaisuuksista ja korjauksista, jotka ovat uusia tai muuttuneita Project Service Automationin päivitysjulkaisussa 45, V3. Tämän version koontiversionumero on V3.10.78.8 ja se on yleisesti saatavilla itsepäivityksenä heinäkuussa 2022.

## <a name="update-release-47"></a>Päivitysjulkaisu 47

### <a name="bug-fixes"></a>Ohjelmavirhekorjauksia

Seuraavat ongelmat on korjattu.

**Resurssienhallinta**
- Tarkistus on päivitetty sen varmistamiseksi, että käyttäjät eivät voi käynnistää tyhjäarvon viittauspoikkeusta, kun he yrittävät luoda projektiryhmän jäsenen ilman **varattavaa resurssia**.
