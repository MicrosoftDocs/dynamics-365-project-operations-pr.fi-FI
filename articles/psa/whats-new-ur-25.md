---
title: Uutuudet ja muutokset Project Service Automation -päivitysjulkaisussa 25, V3
description: Tässä aiheessa on luettelo ominaisuuksista ja korjauksista, jotka ovat käytettävissä Project Service Automation -päivitysjulkaisussa 25, V3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 10/26/2020
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
ms.openlocfilehash: aabee3fe755e33d2c0f01a96b6f53a68957bc041
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/10/2021
ms.locfileid: "5143735"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-25-v3"></a>Uutuudet ja muutokset Project Service Automation -päivitysjulkaisussa 25, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Meillä on ilo julkistaa Dynamics 365:n Project Service Automation-sovelluksen uusin päivitys. Tämä julkaisu sisältää joitakin tärkeitä parannuksia laatuun, tehokkuuteen ja käytettävyyteen. Tämä versio on yhteensopiva Dynamics 365 -versioiden 9.x kanssa. Jos haluat päivittää tämän julkaisun, avaa Dynamics 365 online -hallintakeskuksen Ratkaisut-sivu ja asenna päivitys. Lisätietoja: [Ensisijaisen ratkaisun asentaminen, päivittäminen tai poistaminen](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).

Tässä ohjeaiheessa on luettelo Project Service Automation V3, päivitysversion 25 uusista tai muuttuneista ominaisuuksista ja korjauksista. Tämän version koontiversion numero on 3.10.43.76 ja se on yleisesti saatavana omana päivityksenä lokakuussa 2020.

## <a name="update-release-25"></a>Päivitysjulkaisu 25

### <a name="bug-fixes"></a>Ohjelmavirhekorjauksia

**Aika ja kulu**

Seuraava ongelma on korjattu:

- Aikamerkintäkaavio sisältää lisätietoja liian pitkästä noudon aikavälistä.

**Resurssienhallinta**

Seuraava ongelma on korjattu:

- Lisättiin Package Deployer -koodi ohittamaan Universal Resource Scheduling -korjaustiedoston tuonti, jos uudempi korjaustiedoston versio on jo olemassa.

**Projektinhallinta**

Seuraavat ongelmat on korjattu:

- Korjattiin pyöristys- ja vaihtokurssipoikkeamat, joiden seurauksena oli virheellisesti suunniteltu kustannus projektin seurantaruudukossa.
- Tukee mahdollisuutta näyttää vähintään kaksi reagointiruudukkoa **Projekti**-lomakkeessa.
- Annettu vahvistus, jolla voi delegoida tehtävän kalenteriin päättymispäivän jälkeen, jolloin seurauksena on epäonnistunut resurssin delegointi.
- Parannettiin virheen käsittelyä ottamaan huomioon seuraavasta luotu tyhjäarvon viitepoikkeus:

    - **PreValidateProjectTeamMemberCreate**-laajennus
    - **PreValidateProjectTaskCreate**, kun projektitehtävä luotiin ilman liitettyä projektia
    - **PreProjectTeamMemberCreate**-laajennus
    - **PostProjectTeamMemberDelete**-laajennus
    - **PreValidateProjectTaskDelete**-laajennus

**Sales**

Seuraavat ongelmat on korjattu:

- Parannettiin virheiden käsittelyä ottamaan huomioon tyhjäarvoinen viitepoikkeus, joka luotiin kohdasta **Kopioi projekti: arvioi HelperResource-hallinta**.
- **Keskeneräiset ajan ja materiaalin laskutukset** -kohdan **Ei ole valmis laskutettavaksi** ei tyhjennä laskutustilaa.
- Korjattiin virheellisesti merkityt **Hinnat**-painikkeet **Roolin hinta**- ja **Luettelon nimikkeet** -välilehdessä.


[!INCLUDE[footer-include](../includes/footer-banner.md)]