---
title: Uutuudet ja muutokset Project Service Automation -päivitysjulkaisussa 31, V3
description: Tässä artikkelissa on luettelo ominaisuuksista ja korjauksista Project Service Automationin päivitysjulkaisussa 31, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 04/26/2021
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
ms.openlocfilehash: 8d62b12a5363637e46b29c2e9edf4e1f17da729f
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8925024"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-31-v3"></a>Uutuudet ja muutokset Project Service Automation -päivitysjulkaisussa 31, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Meillä on ilo julkistaa Dynamics 365:n Project Service Automation-sovelluksen uusin päivitys. Tämä julkaisu sisältää joitakin tärkeitä parannuksia laatuun, tehokkuuteen ja käytettävyyteen. Tämä versio on yhteensopiva Dynamics 365 -versioiden 9.x kanssa. Jos haluat päivittää tämän julkaisun, avaa Dynamics 365 online -hallintakeskuksen Ratkaisut-sivu ja asenna päivitys. Lisätietoja: [Ensisijaisen ratkaisun asentaminen, päivittäminen tai poistaminen](/power-platform/admin/install-remove-preferred-solution).

Tässä artikkelissa on luettelo ominaisuuksista ja korjauksista, jotka ovat uusia tai muuttuneita Project Service Automation V3:n päivitysjulkaisussa 31. Tämän version koontiversion numero on V3.10.52.77, ja se on yleisesti saatavana itsepäivittyvänä toukokuussa 2021.

## <a name="update-release-31"></a>Päivitysjulkaisu 31

### <a name="bug-fixes"></a>Ohjelmavirhekorjauksia

**Aika ja kulu**

Seuraavat ongelmat on korjattu:

- **Varattavissa oleva resurssi** -sivun aikaohjausobjektien komentopainikkeet hämmentävät.
- Kohdassa **Project.SetTrackingFields** luotiin tyhjä viittauspoikkeus, kun aikamerkintä hyväksyttiin.

**Resurssienhallinta**

Seuraavat ongelmat on korjattu:

- **Luo ryhmän jäsen** luominen ei näytä oikein varauksen määritysten metatietoasetusta **varauksen sidotulle oletustilalle**.
- Kun päivität PSA 1.X:stä 3.X:ksi, päivitysprosessi epäonnistuu **UpgradeResourceRequirements**-kohdassa.


**Myynti**

Seuraavat ongelmat on korjattu:

- Todellinen myyntituotto muuntaa summat seurantaruudukon projektivaluuttaan.
- Valuuttaoletusarvo on hyvä, kun luodaan kirjausrivejä, tarjousrivejä ja sopimusrivejä skenaarioissa, joissa organisaation perusvaluutta eroaa projektivaluutasta.
- **Odottava korjauskirjaustarkistus** -kysely ei suodata projektin mukaan.
- Loput myynnit lasketaan projektin mukaan virheellisesti.
- Yhteyshenkilön perusteella luodut tarjoukset epäonnistuvat, kun niitä luodaan ilman hinnastoa.
- Kun valitset **Vahvista lasku**, näkyviin ei näy käsittelykierrosta.
- Kun valitset **Luo lasku**, näkyviin ei näy käsittelykierrosta.
- Tarjouksen sulkeminen hävittynä ei peruuta varauksia.







