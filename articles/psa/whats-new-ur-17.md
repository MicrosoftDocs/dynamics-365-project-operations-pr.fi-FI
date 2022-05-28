---
title: Uutuudet ja muutokset Project Service Automation -päivitysjulkaisussa 17, V3
description: Tässä aiheessa on luettelo ominaisuuksista ja korjauksista, jotka ovat käytettävissä Project Service Automation -päivitysjulkaisussa 17, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 03/06/2020
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
ms.openlocfilehash: 70749646f5b67db3cf868a6d9a83c14dc490793a
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/14/2022
ms.locfileid: "8585087"
---
# <a name="project-service-automation-update-release-17-v3"></a>Project Service Automation -päivitysjulkaisu 17, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Meillä on ilo julkistaa Dynamics 365:n Project Service Automation-sovelluksen uusin päivitys. Tämä julkaisu sisältää joitakin tärkeitä parannuksia laatuun, tehokkuuteen ja käytettävyyteen.  Tämä versio on yhteensopiva Dynamics 365 -versioiden 9.x kanssa. Jos haluat päivittää tämän julkaisun, avaa Dynamics 365 online -hallintakeskuksen Ratkaisut-sivu ja asenna päivitys. Lisätietoja: [Ensisijaisen ratkaisun asentaminen, päivittäminen tai poistaminen](/power-platform/admin/install-remove-preferred-solution).

Tässä aiheessa on luettelo ominaisuuksista ja korjauksista, jotka ovat uusia tai muuttuneita PSA V3 -päivitysjulkaisussa 17. Tällä versiolla on koontinumero V3.10.6.34 ja se on ollut yleisesti saatavilla itsepalvelupäivityksenä maaliskuusta 2020 lähtien.


## <a name="update-release-17"></a>Päivitysjulkaisu 17

### <a name="bug-fixes"></a>Ohjelmistovirheiden korjaukset

**Yleiset**

- Korjattu: Päivitä Project Service Automation vaatiaksesi Team Member -käyttöoikeuksien noudattamista (projektiresurssikeskus sisältää Team Member Service -suunnitelman metatiedot 3.x)
 
**Aika ja kulu**

- Korjattu: Kuluarviota ei voi muuttaa ei-nolla-hinnasta nollaan (0). Muutos ohitetaan.

**Projektinhallinta**

- Korjattu: Tiimin jäsenen työnimikkeen nimelle on lisätty null-arvojen tarkistus.
- Korjattu: **msdyn_resourceassignment**-entiteetin **msdyn_userresourceid**-kenttä on merkitty vanhentuneeksi.
- Korjattu: Päivitys versiosta 2.x versioon 3.x käsittelee nyt tehtävien delegoinnin tyhjät töiden jaksottumiset.

**Sales**

- Korjattu: **Invoice.PreValidateInvoiceUpdate** käsittelee nyt tietueiden omistajien uudelleendelegoinnin oikein.
- Korjattu: Kun tapahtuman luokka on **Aika**, **UnitGroup**-arvoa ei voida muokata millekään entiteetille, mukaan lukien **QuoteLineDetails**, **JournalLine**, **InvoiceLineDetail** ja **ContractLineDetails**. **Yksikkö**-arvoa voi kuitenkin muokata, paitsi **JournalLine**- ja **InvoiceLineDetails**-entiteeteille.




[!INCLUDE[footer-include](../includes/footer-banner.md)]
