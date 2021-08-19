---
title: Uutuudet ja muutokset Project Service Automation -päivitysjulkaisussa 32, V3
description: Tässä aiheessa on luettelo ominaisuuksista ja korjauksista, jotka ovat käytettävissä Project Service Automation -päivitysjulkaisussa 32, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 06/01/2021
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
ms.openlocfilehash: 11bf451ef4f24e2301ffde4f86a556a8a4fe30b0
ms.sourcegitcommit: 886102894244887d72e5a6213071e8d8a52c9d48
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/01/2021
ms.locfileid: "6129662"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-32-v3"></a>Uutuudet ja muutokset Project Service Automation -päivitysjulkaisussa 32, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Meillä on ilo esitellä Microsoft Dynamics 365 Project Service Automation -sovelluksen uusin päivitys. Tämä julkaisu sisältää joitakin tärkeitä parannuksia laatuun, tehokkuuteen ja käytettävyyteen. Se on yhteensopiva Dynamics 365 9.x -version kanssa. Päivitä tähän versioon asentamalla päivitys Dynamics 365 -hallintakeskuksen online-ratkaisujen sivulta. Lisätietoja: [Ensisijaisen ratkaisun asentaminen, päivittäminen tai poistaminen](/power-platform/admin/install-remove-preferred-solution).

Tässä aiheessa on luettelo ominaisuuksista ja korjauksista, jotka ovat uusia tai muuttuneita Project Service Automation V3 -päivitysjulkaisussa 32. Tämän version koontiversion numero on V3.10.53.108, ja se on yleisesti saatavana itsepäivittyvänä kesäkuussa 2021.

## <a name="update-release-32"></a>Päivitysjulkaisu 32

### <a name="bug-fixes"></a>Ohjelmavirhekorjauksia

#### <a name="general"></a>Yhteiset

- Kun pääversiopäivitys epäonnistuu, vain pääsovelluksen aloituskohdat tulisi estää, jotta jaetut entiteetit ovat yhä käytettävissä.

#### <a name="time-and-expense"></a>Aika ja kulu

Seuraavat ongelmat on korjattu:

- **TimeEntriesImportFromResourceAssignment** ei säilytä resurssin delegoinnin jaksotussektorin aloitus- ja päättymisaikoja.
- Kun valitset **Aikamerkintä**-ruudukosta **Avaa merkintä**, sinua saatetaan estää valitsemasta muita lomakkeita.
- Kun tuot tehtäviä aikamerkintöihin, asiakaskoodin kysely saattaa luoda pitkän URL-osoitteen, jonka vuoksi kysely epäonnistuu.
- Kun **Aikamerkintä**-ruudukon solusta poistetaan arvo, kohdistus ei jää ruudukkoon.
- **Hylkää**-painike on poistettu **Käsittelyssä olevat hyväksynnät** -näkymästä moderneilta hyväksynnöiltä.
- Lukkiutumat ja **Aikamerkintä**-entiteettiin liittyvien mukautusten asianmukaiseen käsittelyyn liittyvät virheet vaikuttavat aikamerkintöjen joukkohyväksynnän vakauteen ja suorituskykyyn.

#### <a name="project-planning"></a>Projektin suunnittelu

- Kun päivität projektin, jonka **Sopimusyksikkö**-kentässä on null-arvo, tapahtuu null-viittauksen poikkeus.
- **Päivitä projektin summat** laskee projektin jäljellä olevat kustannukset ja jäljellä olevan myynnin virheellisesti.
- Tarpeettomat hinnastojen laskutoimet vaikuttavat resurssin delegoinnin jaksotuksen päivitysten suorituskykyyn.

#### <a name="resource-management"></a>Resurssienhallinta

Seuraava ongelma on korjattu:

- Kun varattavissa olevan resurssin kalenterikapasiteetti on yli 1, Project Service Automation tunnistaa kapasiteetin virheellisesti nollaksi (0). Tästä syystä aikataulunäkymässä ilmenee loputon silmukka.

#### <a name="sales"></a>Myynti

Seuraavat ongelmat on korjattu:

- Mukautettua tapahtumatyyppiä käyttävän kirjauskansion rivin luominen aiheuttaa seuraavan null-viitteen poikkeuksen: *Microsoft.Dynamics.ProjectService.Plugins.JournalLinePlugins.ValidateUnitScheduleAndUnitWithTransactionType(TransactionTypetransactionType, TransactionTypeCode transTypeCodeFromPlugin)*.
- Roolia ja luokkia, joiden aktivointi on kumottu ennen tarjouksen kopioimista, ei tulisi lisätä uuden kopioidun tarjouksen laskutettaviin rooleihin ja luokkiin.
- Asiakirjan päivämäärä ja kirjanpitopäivämäärä eivät vastaa aloituspäivää, jotka on annettu suoraan luonnoslaskuun luodun laskurivin tiedoissa.
- Null-viitteiden poikkeuksia aiheutuu tilanteissa, jotka liittyvät roolien ja luokkien aktivoinnin kumoamiseen ennen tarjouksen kopioimista.
- **Projektit**-sivun **Päivitä hinnat** -toiminto ei päivitä kuluarvioita tai materiaaliarvioita.