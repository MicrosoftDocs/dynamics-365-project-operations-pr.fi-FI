---
title: Uutuudet ja muutokset Project Service Automation -päivitysjulkaisussa 38, V3
description: Tässä artikkelissa on lueteltu ominaisuudet ja korjaukset, jotka ovat saatavissa Microsoft Dynamics 365 Project Service Automation -päivitysjulkaisussa 38, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 12/06/2021
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
ms.openlocfilehash: ccc08cd0bc365bd4761424a4c0ceac91985e7c89
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8915181"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-38-v3"></a>Uutuudet ja muutokset Project Service Automation -päivitysjulkaisussa 38, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Meillä on ilo esitellä Microsoft Dynamics 365 Project Service Automation -sovelluksen uusin päivitys. Tämä julkaisu sisältää joitakin tärkeitä parannuksia laatuun, tehokkuuteen ja käytettävyyteen. Se on yhteensopiva Dynamics 365 9.x -version kanssa. Päivitä tähän versioon asentamalla päivitys Dynamics 365 -hallintakeskuksen online-ratkaisujen sivulta. Lisätietoja: [Ensisijaisen ratkaisun asentaminen, päivittäminen tai poistaminen](/power-platform/admin/install-remove-preferred-solution).

Tässä artikkelissa on luettelo ominaisuuksista ja korjauksista, jotka ovat uusia tai muuttuneita Project Service Automationin päivitysjulkaisussa 38, V3. Tämän version koontiversionumero on V3.10.59.117 ja se on yleisesti saatavilla omatoimipäivityksenä joulukuussa 2021.

## <a name="update-release-38"></a>Päivitysjulkaisu 38

### <a name="bug-fixes"></a>Ohjelmavirhekorjauksia

Seuraavat ongelmat on korjattu.

**Aika ja kulu**

- Poikkeus syntyy, kun hyväksyntäjoukon lokien pituus ylittää 100 000 tietuetta.
- Käyttäjät eivät voi käyttää **Aikamerkintä**-ruudukkoa **Aikamerkintä**-pääsivulta.
- **Aikamerkinnän tuonti** -dialogi, ei näytä tekstiä, jos kohteita ei voi tuoda.
- Käyttäjät voivat luoda hyväksyntäjoukkoja, jos **Kohteen tila** -kenttä on määritetty arvoon **Tuntematon**.

**Projektinhallinta**

- Käyrät eivät näy oikein resurssimäärityksissä ajoille UTC(+09.30) ja UTC(+10.00), kun kesäaika alkaa.
- Työrakenteen **Lisäsarake**-kenttä on piilotettu joillakin alueilla.
- Kalenteriohjausobjektin päivämäärävalitsinta **Projektitehtävä**-ruudukossa ei ole lokalisoitu oikein kiinaksi.

**Myynti**

- Arvot **Sopimuksen tehokkuus** ja **Projektin toteutunut kustannus** eivät vastaa toisiaan, kun varattavat resurssit, joilla on eri sopimusyksiköt ja valuutat, lähettävät aikamerkintöjä.
- Mukautettu työnkulku, joka vahvistaa laskut automaattisesti, epäonnistuu, kun laskut tuodaan hallittuna ratkaisuna. Seuraava sanoma näkyy: "Microsoft.Xrm.Sdk.InvalidPluginExecutionException Message: Virheellinen laskun tila."
- Kun **Juuri** valitaan yhteenvedon laatimisen vaihtoehdoksi ja projektilla on arvioita eri tapahtumaluokista (esimerkiksi ajan, kulun ja materiaaliarvion yhdistelmä), järjestelmä laatii yhteenvedon tapahtumaluokista yhtenä maksurivinä.
- Skenaarioissa, joissa kulurivi lisätään ennen kuin sopimusrivi yhdistetään projektiin, oikeaa hinnoittelua ei syötetä oletusarvona **Päivitä hinta** -kenttään.
- **Projekti**- ja **Tehtävä**-entiteeteissä ei sallita negatiivisia myyntisummia.
