---
title: Uutuudet ja muutokset Project Service Automation -päivitysjulkaisussa 35, V3
description: Tässä aiheessa on lueteltu ominaisuudet ja korjaukset, jotka ovat saatavissa Microsoft Dynamics 365 Project Service Automation -päivityksessä 35, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 09/03/2021
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
ms.openlocfilehash: 53670e2c7f54f8fccf636b2855e190f5f85c6068
ms.sourcegitcommit: 5bb8ca5055deda57e2b1173a2e45c53b15f61d62
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/03/2021
ms.locfileid: "7473261"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-35-v3"></a>Uutuudet ja muutokset Project Service Automation -päivitysjulkaisussa 35, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Meillä on ilo esitellä Microsoft Dynamics 365 Project Service Automation -sovelluksen uusin päivitys. Tämä julkaisu sisältää joitakin tärkeitä parannuksia laatuun, tehokkuuteen ja käytettävyyteen. Se on yhteensopiva Dynamics 365 9.x -version kanssa. Päivitä tähän versioon asentamalla päivitys Dynamics 365 -hallintakeskuksen online-ratkaisujen sivulta. Lisätietoja: [Ensisijaisen ratkaisun asentaminen, päivittäminen tai poistaminen](/power-platform/admin/install-remove-preferred-solution).

Tässä aiheessa on luettelo ominaisuuksista ja korjauksista, jotka ovat uusia tai muuttuneita Project Service Automationin Päivitysjulkaisussa 35, V3. Tämän version koontiversionumero on V3.10.56.110 ja se on yleisesti saatavilla itsepäivityksenä syyskuussa 2021.

## <a name="update-release-35"></a>Päivitysjulkaisu 35

### <a name="bug-fixes"></a>Ohjelmavirhekorjauksia

Seuraavat ongelmat on korjattu.

**Aika ja kulu**

- Projektin hyväksyjä saa lukuoikeusvirheen hyväksyessään kulumerkintöjä **Projektin hyväksyjä** -roolilla.
- Projektin hyväksyjä saa kirjoitusoikeusvirheen **msdyn_projectapproval**, kun hän peruuttaa hyväksytyn aikamerkinnän **Projektin hyväksyjä** -roolilla.
- Kun valitset aikamerkinnässä **Kopioi viikko** Dynamics 365 for phone - Project Resource Hub -sovellusmoduulissa, tulee seuraava virhe: "...\OfficeProductivity_RibbonRules.js.map: HTTP error: status code 404, net::ERR_HTTP_RESPONSE_CODE_FAILURE."
- **Yritä uudelleen** -käytäntö hyväksyy automaattisesti merkinnät, jotka aiemmin hylättiin.
- **Hyväksyntäjoukot**-aliruudukko näyttää nauhan toiminnot, joita ei voi käyttää.
- Kuvakkeet puuttuvat **Projektitehtävä**- ja **Resurssirooli**-kohdista **Aikamerkintä**-entiteetissä.
- Kun tuot resurssitehtäviä, tuotujen aikamerkintöjen kesto ei ole oikea tehtäville, jotka luotiin manuaalisten tilatehtävien avulla.
- **Poista** puuttuu **Aikamerkintätietueiden erikoishaku** -sivulta.
- **Tallenna** puuttuu **Aikamerkinnän tiedot** -sivulta. Tämä ongelma estää muutosten tallentamisen, kun sivu suljetaan.

**Projektin suunnittelu**

- Ruudukot **Resurssivaraukset** ja **Resurssin täsmäytys** eivät lajittele ryhmiteltyjä määritteitä aakkosten mukaan.
- Tehtäviä ei voi luoda, jos päivämäärän toiminnaksi on mukautettu **vain päivämäärä**.

**Resurssien hallinta**

- Jos sekä Dynamics 365 Field Service että Project Service Automation ovat asennettuina, lisäämisongelmia tulee, kun **Resurssitarpeiden liitetty näkymä** liitetään pääsivuun.
- Kun kaksoisnapsautetaan **Tallenna** **Ryhmän jäsenen pikaluonti** -dialogiruudussa, resurssivaatimusta ei voi luoda.

**Myynti**

- Poikkeus ilmenee, jos poistat tehtävän, joka on liitetty tarjoukseen, jonka tila on **Voitettu**.