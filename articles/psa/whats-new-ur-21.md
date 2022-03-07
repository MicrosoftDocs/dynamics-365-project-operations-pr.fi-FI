---
title: Uutuudet ja muutokset Project Service Automation -päivitysjulkaisussa 21, V3
description: Tässä aiheessa on luettelo ominaisuuksista ja korjauksista, jotka ovat käytettävissä Project Service Automation -päivitysjulkaisussa 21, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 06/19/2020
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
ms.openlocfilehash: e7bf9d5c85d2fab0d17c435bdd96057c0c80be8f41b16f94afe6b1f554e7a9fe
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/06/2021
ms.locfileid: "6984733"
---
# <a name="project-service-automation-update-release-21-v3"></a>Project Service Automation -päivitysjulkaisu 21, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Meillä on ilo julkistaa Dynamics 365:n Project Service Automation-sovelluksen uusin päivitys. Tämä julkaisu sisältää joitakin tärkeitä parannuksia laatuun, tehokkuuteen ja käytettävyyteen. Tämä versio on yhteensopiva Dynamics 365 -versioiden 9.x kanssa. Jos haluat päivittää tämän julkaisun, avaa Dynamics 365 online -hallintakeskuksen Ratkaisut-sivu ja asenna päivitys. Lisätietoja: [Ensisijaisen ratkaisun asentaminen, päivittäminen tai poistaminen](/power-platform/admin/install-remove-preferred-solution).

Tässä aiheessa on luettelo ominaisuuksista ja korjauksista, jotka ovat uusia tai muuttuneita Project Service Automation V3 -päivitysjulkaisussa 21. Tämän version koontiversion numero on V 3.10.32.50, ja se on yleisesti saatavana itsepäivittyvänä kesäkuussa 2020.

## <a name="update-release-21"></a>Päivitysjulkaisu 21

### <a name="bug-fixes"></a>Ohjelmavirhekorjauksia

**Aika ja kulu**

Seuraavat ongelmat on korjattu:

- Kun **Aikamerkinnän ruudukko -ohjausobjekti** on käytössä koontinäytössä, ruudukko ei käytä koontinäytön ruudukkosäilön koko leveyttä.
- **Aikamerkinnän ruudukko** -ohjausobjekti ei näytä tietueita tietyillä aikavyöhykkeillä.
- Kello 21.00 jälkeiset aikamerkit näkyvät vääränä päivänä.
- Käyttäjät eivät voi lähettää kuluja, jos kululuokassa **Kulun kuitti pakollinen** ei ole arvoa.

**Resurssienhallinta**

Seuraavat ongelmat on korjattu:

- Passiiviset varaukset näkyvät **Täsmäytys**-näkymässä.
- Yleisestä resurssin toteutuksesta puuttui vahvistus, jolla varmistettiin, että varauksella on kelvollinen tila.

**Projektinhallinta**

Seuraavat ongelmat on korjattu:

- **Projekti**-lomakeruudukoita (**Resurssien delegointi**, **Tehtävä**, **Täsmäytys**-näkymä, **Kuluarviot**) ovat muokattavissa, vaikka projekti ei ole aktiivinen.
- Asiakkaiden kaksoiskappaleita ei voi yhdistää asiakkaisiin, jotka on linkitetty vahvistettuihin projektisopimuksiin.
- Jos resurssiin ei ole lisätty kelvollista kalenteria, järjestelmä ei palauta käyttäjäystävällistä virhesanomaa.
- Tehtäväruudukon **Lisää tehtävä** -painike on otettu käyttöön, kun projekti on linkitetty **Microsoft Project -apuohjelmaan**.
- Työmäärä kasvaa hallitsemattomasti, kun luokan sisältävä tehtävä delegoidaan resurssille, jonka rooliin on määritetty kustannushinta.

**Sales**

Seuraavat parannukset on tehty:

- **Laskutustiheys**- ja **Laskutuksen aloitus** on siirretty **Laskutusaikataulu**-välilehteen.

Seuraavat ongelmat on korjattu:

- **Luokan** **Myyntihinta yhteensä** on nolla (0), vaikka **roolin** myyntihinta yhteensä ei ole nolla.
- Asiakkaat eivät voi muuttaa **Laskun tila** -kentän arvoksi **Valmis laskutukseen**, kun toinen mukautettu prosessi päivittää lisäkenttää.
- **Päivitä laskurivit** -painike voi luoda useita rivien kaksoiskappaleita, jos se valitaan toistuvasti.
- **Päivitä hinnat** -painike ei toimi **Pikanäkymä**-lomakkeen **Roolin hinnat** -aliruudukossa.
- **Myyntihinnaston ratkaisun** logiikka käsittelee aikavyöhykkeitä virheellisesti, jolloin tuloksena on hinnastojen virheellinen valinta.
- Projektin **Todelliset kulut yhteensä** voi olla murto-osan väärässä yhden aikamerkinnän hyväksynnän jälkeen.
- **Hinnan ratkaisun** logiikka ei anna käyttäjäystävällistä virhesanomaa, jos **Noudettu roolihinta** -arvoja ei ole **Ensisijainen yksikkö**- ja **Hinta ensisijaisessa yksikössä** -kentissä.


[!INCLUDE[footer-include](../includes/footer-banner.md)]