---
title: Uutuudet ja muutokset Project Service Automation -päivitysjulkaisussa 28, V3
description: Tässä aiheessa on luettelo ominaisuuksista ja korjauksista, jotka ovat käytettävissä Project Service Automation -päivitysjulkaisussa 28, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 01/26/2021
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
ms.openlocfilehash: b06a5ee6d0e2da76801a36701f38f1885d6c7562
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/10/2021
ms.locfileid: "6010512"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-28-v3"></a>Uutuudet ja muutokset Project Service Automation -päivitysjulkaisussa 28, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Meillä on ilo julkistaa Dynamics 365:n Project Service Automation-sovelluksen uusin päivitys. Tämä julkaisu sisältää joitakin tärkeitä parannuksia laatuun, tehokkuuteen ja käytettävyyteen. Tämä versio on yhteensopiva Dynamics 365 -versioiden 9.x kanssa. Jos haluat päivittää tämän julkaisun, avaa Dynamics 365 online -hallintakeskuksen Ratkaisut-sivu ja asenna päivitys. Lisätietoja: [Ensisijaisen ratkaisun asentaminen, päivittäminen tai poistaminen](/power-platform/admin/install-remove-preferred-solution).

Tässä ohjeaiheessa on luettelo Project Service Automation V3, päivitysversion 28 uusista tai muuttuneista ominaisuuksista ja korjauksista. Tämän version koontiversion numero on 3.10.46.32 ja se on yleisesti saatavana omana päivityksenä tammikuussa 2021.

## <a name="update-release-28"></a>Päivitysjulkaisu 28

### <a name="bug-fixes"></a>Ohjelmavirhekorjauksia

**Aika ja kulu**

Seuraavat ongelmat on korjattu:

- Käyttäjät voivat **joukkomuokkauksen** avulla päivittää hyväksyttyjä ja lähetettyjä aikamerkintöjä.

**Projektinhallinta**

Seuraavat ongelmat on korjattu:

- Jos tehtävän GUID-tunnus tulkitaan numeroksi, tehtäviä ei voi avata muokattavaksi käyttämällä **Muokkaa tehtävää** -vaihtoehtoa **Työrakenne**-sivun valintanauhassa.

**Sales**

Seuraavat ongelmat on korjattu:

- Tyhjäarvon viittauspoikkeus luodaan, kun **GetEstimatesForProject**-laajennus käynnistetään.
- **Merkitse valmiiksi laskuttamista varten** välitavoiteruudukossa päivittää määritteet vain osittain, lukuun ottamatta **InvoiceStatus**-määritettä, joka päivitetään.



[!INCLUDE[footer-include](../includes/footer-banner.md)]