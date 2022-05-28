---
title: Uutuudet ja muutokset Project Service Automation -päivitysjulkaisussa 29, V3
description: Tässä aiheessa on luettelo ominaisuuksista ja korjauksista, jotka ovat käytettävissä Project Service Automation -päivitysjulkaisussa 29, V3.
author: ruhercul
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
ms.reviewer: johnmichalak
ms.openlocfilehash: 56cf47d207c7ee518d5d4b53866c3d6ddf1d1fb3
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/14/2022
ms.locfileid: "8587214"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-29-v3"></a>Uutuudet ja muutokset Project Service Automation -päivitysjulkaisussa 29, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Meillä on ilo julkistaa Dynamics 365:n Project Service Automation-sovelluksen uusin päivitys. Tämä julkaisu sisältää joitakin tärkeitä parannuksia laatuun, tehokkuuteen ja käytettävyyteen. Tämä versio on yhteensopiva Dynamics 365 -versioiden 9.x kanssa. Jos haluat päivittää tämän julkaisun, avaa Dynamics 365 online -hallintakeskuksen Ratkaisut-sivu ja asenna päivitys. Lisätietoja: [Ensisijaisen ratkaisun asentaminen, päivittäminen tai poistaminen](/power-platform/admin/install-remove-preferred-solution).

Tässä aiheessa on luettelo ominaisuuksista ja korjauksista, jotka ovat uusia tai muuttuneita Project Service Automation V3 -päivitysjulkaisussa 29. Tämän version koontiversionumero on V3.10.47.7 ja se on yleisesti saatavilla omatoimipäivityksenä helmikuussa 2021.

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
