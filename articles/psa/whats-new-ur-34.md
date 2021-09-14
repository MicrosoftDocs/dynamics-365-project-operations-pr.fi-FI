---
title: Uutuudet ja muutokset Project Service Automation -päivitysjulkaisussa 34, V3
description: Tässä aiheessa on luettelo ominaisuuksista ja korjauksista, jotka ovat käytettävissä Project Service Automation -päivitysjulkaisussa 34, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 08/05/2021
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
ms.openlocfilehash: 528d4f8d108720cb9c912cea1c0d5f37e3716eec
ms.sourcegitcommit: 80aa1e8070f0cb4992ac408fc05bdffe47cee931
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/13/2021
ms.locfileid: "7323277"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-34-v3"></a>Uutuudet ja muutokset Project Service Automation -päivitysjulkaisussa 34, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Meillä on ilo esitellä Microsoft Dynamics 365 Project Service Automation -sovelluksen uusin päivitys. Tämä julkaisu sisältää joitakin tärkeitä parannuksia laatuun, tehokkuuteen ja käytettävyyteen. Se on yhteensopiva Dynamics 365 9.x -version kanssa. Päivitä tähän versioon asentamalla päivitys Dynamics 365 -hallintakeskuksen online-ratkaisujen sivulta. Lisätietoja: [Ensisijaisen ratkaisun asentaminen, päivittäminen tai poistaminen](/power-platform/admin/install-remove-preferred-solution).

Tässä aiheessa on luettelo ominaisuuksista ja korjauksista, jotka ovat uusia tai muuttuneita Project Service Automation V3 -päivitysjulkaisussa 34. Tämän version koontiversionumero on V3.10.55.38 ja se on yleisesti saatavilla itsepäivityksenä heinäkuussa 2021.

## <a name="update-release-34"></a>Päivitysjulkaisu 34

### <a name="bug-fixes"></a>Ohjelmavirhekorjauksia
Seuraavat ongelmat on korjattu.

**Yhteiset**

- Julkaisijapohjaiset päivitykset eivät aktivoi uutta uudenaikaista hyväksynnän työnkulkua.
- **Hyväksyntäjoukon** pääsivusta puuttuvat **Kohdetila**- ja **Toimintotyyppi**-määritteet.

**Aika ja kulu**

- Palautuspyyntöä ei voi hyväksyä uudenaikaista hyväksyntäkulkua käyttämällä.
- Viikkomerkintöjen kopioiminen ei toimi, kun kopioit merkintöjä, jotka eivät liity kirjautuneeseen käyttäjään.

**Projektin suunnittelu**

- Resurssien määritykset ovat vioittuneet, kun niitä tuodaan Microsoft Project -työpöytäsovelluksesta.

**Resurssien hallinta**

- Kun julkaiset projektin Microsoft Project Desktop -työasemaohjelman apuohjelmasta, aiemmin luotujen vaatimusten päättymispäivää muutetaan.
- Desimaalien määrä ylittää kaksi desimaalia varausten vahvistusikkunassa.

**Myynti**

- Kun lisäät projektisopimukseen tuotepohjaisen rivin olemassa olevan tuotteen kanssa, **avainta ei löydy sanakirjasta** -poikkeus tulee näkyviin.
- Liidejä ei voi määrittää, kun tilaustyyppi on yhdistetty liidistä mahdollisuuteen.
