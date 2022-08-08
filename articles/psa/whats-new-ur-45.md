---
title: Uutuudet ja muutokset Project Service Automation -päivitysjulkaisussa 45, V3
description: Tässä artikkelissa on lueteltu ominaisuudet ja korjaukset, jotka ovat saatavissa Microsoft Dynamics 365 Project Service Automation -päivitysjulkaisussa 45, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 07/14/2022
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
ms.openlocfilehash: 98f7c973917d7d6334e6e0aeb15214c538b33143
ms.sourcegitcommit: 36fda4f45ddeb0f81d30bd1e22852727df644754
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 07/16/2022
ms.locfileid: "9169153"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-45-v3"></a>Uutuudet ja muutokset Project Service Automation -päivitysjulkaisussa 45, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Meillä on ilo esitellä Microsoft Dynamics 365 Project Service Automation -sovelluksen uusin päivitys. Tämä julkaisu sisältää joitakin tärkeitä parannuksia laatuun, tehokkuuteen ja käytettävyyteen. Se on yhteensopiva Dynamics 365 9.x -version kanssa. Päivitä tähän versioon asentamalla päivitys Dynamics 365 -hallintakeskuksen online-ratkaisujen sivulta. Lisätietoja: [Ensisijaisen ratkaisun asentaminen, päivittäminen tai poistaminen](/power-platform/admin/install-remove-preferred-solution).

Tässä artikkelissa on luettelo ominaisuuksista ja korjauksista, jotka ovat uusia tai muuttuneita Project Service Automationin päivitysjulkaisussa 45, V3. Tämän version koontiversionumero on V3.10.76.168 ja se on yleisesti saatavilla itsepäivityksenä heinäkuussa 2022.

## <a name="update-release-45"></a>Päivitysjulkaisu 45

### <a name="bug-fixes"></a>Ohjelmavirhekorjauksia

Seuraavat ongelmat on korjattu.

**Myynti**

- Käyttäjät eivät saa laskuja luotua sen jälkeen, kun he luovat laskun ilman laskuttamatonta myyntiä, jos he ovat tarkastelemassa sivun samaa esiintymää, eivätkä päivitä sitä.

**Aika ja kulu**

- Kun modernit hyväksynnät on otettu käyttöön ja peruutettu projektin hyväksyntä on hyväksytty, tietueen tilaksi päivitetään virheellisesti **Peruutuspyyntö hyväksytty**.
- Kun modernit hyväksynnät on otettu käyttöön ja pilvityönkulku on passiivinen, hyväksyntäprosessi ei onnistu, eikä lähettävälle tai hyväksyvälle käyttäjälle lähetetä ilmoitusta.
