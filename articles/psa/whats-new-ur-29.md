---
title: Uutuudet ja muutokset Project Service Automation -päivitysjulkaisussa 29, V3
description: Tässä aiheessa on luettelo ominaisuuksista ja korjauksista, jotka ovat käytettävissä Project Service Automation -päivitysjulkaisussa 29, V3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 02/22/2021
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
ms.openlocfilehash: 711255ab66f84fe46d0f16fa72e5a10fe0360394
ms.sourcegitcommit: f78087174a8512199a1bcbd7e8610bbc80e64801
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/04/2021
ms.locfileid: "5499667"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-29-v3"></a>Uutuudet ja muutokset Project Service Automation -päivitysjulkaisussa 29, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Meillä on ilo julkistaa Dynamics 365:n Project Service Automation-sovelluksen uusin päivitys. Tämä julkaisu sisältää joitakin tärkeitä parannuksia laatuun, tehokkuuteen ja käytettävyyteen. Tämä versio on yhteensopiva Dynamics 365 -versioiden 9.x kanssa. Jos haluat päivittää tämän julkaisun, avaa Dynamics 365 online -hallintakeskuksen Ratkaisut-sivu ja asenna päivitys. Lisätietoja: [Ensisijaisen ratkaisun asentaminen, päivittäminen tai poistaminen](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).

Tässä aiheessa on luettelo ominaisuuksista ja korjauksista, jotka ovat uusia tai muuttuneita Project Service Automation V3 -päivitysjulkaisussa 29. Tämän version koontiversionumero on V3.10.45.98 ja se on yleisesti saatavilla omatoimipäivityksenä helmikuussa 2021.

## <a name="update-release-29"></a>Päivitysjulkaisu 29

### <a name="bug-fixes"></a>Ohjelmavirhekorjauksia

**Aika ja kulu**

Seuraavat ongelmat on korjattu:

- Käyttäjät eivät näe työaikaruudukossa ei-työpäivinä kirjattuja työaikoja.
- Hyväksyttyjä kulumerkintöjä voidaan muokata ruudukossa.

**Projektinhallinta**

Seuraavat ongelmat on korjattu:

- Puuttuva vahvistuslogiikka sen varmistamiseksi, että resurssien varaukseen käytetyt työtunnit eivät voi olla negatiivisia.
- Mukautettu **AssignResourcesForTask**-toiminto päivittää kaikki kentät vain muutettujen kenttien sijaan.
- Kun kopioit projektin ympäristössä, jossa on **LuoProjekti**-tapahtumaan rekisteröityjä laajennuksia tai työnkulkuja, **msdyn_bulkgenerationstatus**-määritettä ei päivitä, jos **KopioiWBSprojektiin**-toiminto epäonnistuu.
- Kun laajennat projektikalenterin, työpäiviä ei lajitella nousevassa järjestyksessä, jolloin jotkin projektitehtäväpäivitykset epäonnistuvat.
- Projektinhallinnan muuttaminen aiemmin luodussa projektissa käynnistää organisaatioyksikön oletuslogiikan.

**Myynti**

Seuraavat ongelmat on korjattu:

- **Sopimus**-sivun **Sopimuksen suorituskyky** -välilehti epäonnistuu hiljaisesti alustuksen aikana, kun sopimusrivejä ei ole.
