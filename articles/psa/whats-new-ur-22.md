---
title: Uutuudet ja muutokset Project Service Automation -päivitysjulkaisussa 22, V3
description: Tässä aiheessa on luettelo ominaisuuksista ja korjauksista, jotka ovat käytettävissä Project Service Automation -päivitysjulkaisussa 22, V3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 07/28/2020
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
ms.openlocfilehash: db4cbb9f9daadcb1911325f8bee987d5e480e1cf
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/10/2021
ms.locfileid: "5150979"
---
# <a name="project-service-automation-update-release-22-v3"></a>Project Service Automation -päivitysjulkaisu 22, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Meillä on ilo julkistaa Dynamics 365:n Project Service Automation-sovelluksen uusin päivitys. Tämä julkaisu sisältää joitakin tärkeitä parannuksia laatuun, tehokkuuteen ja käytettävyyteen. Tämä versio on yhteensopiva Dynamics 365 -versioiden 9.x kanssa. Jos haluat päivittää tämän julkaisun, avaa Dynamics 365 online -hallintakeskuksen Ratkaisut-sivu ja asenna päivitys. Lisätietoja: [Ensisijaisen ratkaisun asentaminen, päivittäminen tai poistaminen](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).

Tässä aiheessa on luettelo ominaisuuksista ja korjauksista, jotka ovat uusia tai muuttuneita Project Service Automation V3 -päivitysjulkaisussa 22. Tämän version koontiversion numero on V 3.10.33.48, ja se on yleisesti saatavana itsepäivittyvänä kesäkuussa 2020.

## <a name="update-release-22"></a>Päivitysjulkaisu 22

### <a name="bug-fixes"></a>Ohjelmavirhekorjauksia



**Aika ja kulu**

Seuraavat ongelmat on korjattu:

- **Aikamerkintöjä** ei lisätä automaattisesti aikamerkintöjen aikatauluun tuonnin jälkeen.
- **Aikamerkinnän** ruudukon päivämäärävalitsin ei tunnista käyttäjän aluekohtaisia asetuksia.

**Resurssienhallinta**

Seuraavat ongelmat on korjattu:

- **Resurssien delegointi** -jaksotusten muutoksia ei tunnisteta manuaalisessa tilassa, kun **resurssitarpeita** luodaan.
- **Resurssipyynnöt** eivät tue mukautetun pyynnön tiloja.

**Projektinhallinta**

Seuraavat ongelmat on korjattu:

- EstimateGridControl-ohjausobjektin kaksoisnapsautus ei jäsennä oikein hollantilaisen muotoilun numeroita.
- Delegoidut tunnit eivät päivity oikein, kun delegointeja muutetaan Microsoft Projectin työpöytäasiakasohjelman apuohjelmalla.
- Projektin seuranta- ja Arviot-ruudukoissa näkyy virheellinen myyntivaluutan koodi, kun sopimusvaluutta ei ole sama kuin asiakasvaluutta ja kun organisaation on määritetty näyttämään valuuttakoodit eikä rahayksikön tunnuksia.
- Ryhmän jäsenen päättymispäivä lisää yhden päivän, jos työaika-aikataulu käyttää 24 tunnin aikataulua.
- Tapahtumaluokan lisääminen projektiaikataulussa tehtävään ei käynnistä automaattista tallennusta.
- Seuraava virhe näytetään, kun ryhmän jäsen lisätään projektimalliin: Resurssitarpeita ei voi liittää projektimalleihin. 
- Valintanauhasäännön skripti msdyn.Approval.CanApproveOrReject näyttää aikakatkaisuvirheen.

**Sales**

Seuraavat ongelmat on korjattu:

- Vahvistuksen virhesanomaa ei näytetä, kun kustannushinnasto valitaan hinnastovalinnassa Uusi tarjouksen projektihinnasto -lomakkeessa tai -entiteetissä.
- Tarjouksen sulkeminen voitettuna ei siirrä luotuun sopimukseen, jos tarjoukseen liitetty liiketoimintaprosessi on viimeisessä vaiheessa.
- **Laskuttamattoman myynnin** vastakirjaus linkitetään alkuperäiseen kustannukseen, kun aikamerkintä palautettiin.
- Laskun tilaksi ei tule **Vahvistettu** **Vahvista**-painikkeen valinnan jälkeen, jos laskua ei päivitetä.
