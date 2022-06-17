---
title: Uutuudet ja muutokset Project Service Automation -päivitysjulkaisussa 30, V3
description: Tässä artikkelissa on luettelo ominaisuuksista ja korjauksista Project Service Automationin päivitysjulkaisussa 30, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 04/01/2021
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
ms.openlocfilehash: ad00b126a13e18a5de47df335aea06b9690efa13
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8925070"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-30-v3"></a>Uutuudet ja muutokset Project Service Automation -päivitysjulkaisussa 30, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Meillä on ilo julkistaa Dynamics 365:n Project Service Automation-sovelluksen uusin päivitys. Tämä julkaisu sisältää joitakin tärkeitä parannuksia laatuun, tehokkuuteen ja käytettävyyteen. Tämä versio on yhteensopiva Dynamics 365 -versioiden 9.x kanssa. Jos haluat päivittää tämän julkaisun, avaa Dynamics 365 online -hallintakeskuksen Ratkaisut-sivu ja asenna päivitys. Lisätietoja: [Ensisijaisen ratkaisun asentaminen, päivittäminen tai poistaminen](/power-platform/admin/install-remove-preferred-solution).

Tässä artikkelissa on luettelo ominaisuuksista ja korjauksista, jotka ovat uusia tai muuttuneita Project Service Automation V3:n päivitysjulkaisussa 30. Tämän version koontiversion numero on V3.10.51.61, ja se on yleisesti saatavana itsepäivittyvänä huhtikuussa 2021.

## <a name="update-release-30"></a>Päivitysjulkaisu 30

### <a name="bug-fixes"></a>Ohjelmavirhekorjauksia

**Aika ja kulu**

Seuraavat ongelmat on korjattu:

- Virhe luotaessa ja tallennettaessa aikasyötettä **Pikaluonti**-sivulla, jos **Rooli**-kenttä poistetaan.
- Ajan syöttösuodatin käyttää väärää suodatusoperaattoria.
- Kopioidut työaikaraportit eivät tule näkyviin automaattisesti, kun valitset ajan syötteenohjausobjektista **Kopioi viikko**.

**Resurssienhallinta**

Seuraavat ongelmat on korjattu:

- Kun laajennat varauksen, kovalle varaukselle määritetty varaustila on virheellinen. Varauksen laajentaminen noudattaa varausmäärityksen metatiedoissa **Sidottu**-tilaksi määritettyä varaustilaa.
- Kun kelvollista varaustilaa ei määritetä, virhesanomaa ei lokalisoida oikein.

**Projektinhallinta**

Seuraavat ongelmat on korjattu:

- Projekteja ei voi luoda yhtenä valuuttana ja sisällyttää niihin liittyviä tehtäviä toiseen valuuttaan.

**Myynti**

Seuraavat ongelmat on korjattu:

- Kun hinnasto kopioidaan, hintoja ei päivitetä.
- Kun tarjous suljetaan voitettuna, kustannuserittelyllä on alkuperän arvo.
- **Projektitehtävä**-entiteetissä **Arvioitu kustannus** on nimetty uudelleen **Suunnitelluksi kustannukseksi (perusvaluutta)** .
- Tyhjäarvoinen poikkeus luodaan, kun laskuja luodaan tai poistetaan.
