---
title: Uutuudet ja muutokset Project Service Automation -päivitysjulkaisussa 33, V3
description: Tässä aiheessa on luettelo ominaisuuksista ja korjauksista, jotka ovat käytettävissä Project Service Automation -päivitysjulkaisussa 33, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 06/30/2021
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
ms.openlocfilehash: a72202905fc0464577bb126aa5890a8f952dc3a8aff505416e535b42b53df7db
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/06/2021
ms.locfileid: "7006512"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-33-v3"></a>Uutuudet ja muutokset Project Service Automation -päivitysjulkaisussa 33, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Meillä on ilo esitellä Microsoft Dynamics 365 Project Service Automation -sovelluksen uusin päivitys. Tämä julkaisu sisältää joitakin tärkeitä parannuksia laatuun, tehokkuuteen ja käytettävyyteen. Se on yhteensopiva Dynamics 365 9.x -version kanssa. Päivitä tähän versioon asentamalla päivitys Dynamics 365 -hallintakeskuksen online-ratkaisujen sivulta. Lisätietoja: [Ensisijaisen ratkaisun asentaminen, päivittäminen tai poistaminen](/power-platform/admin/install-remove-preferred-solution).

Tässä aiheessa on luettelo ominaisuuksista ja korjauksista, jotka ovat uusia tai muuttuneita Project Service Automation V3 -päivitysjulkaisussa 33. Tämän version koontiversionumero on V3.10.54.98 ja se on yleisesti saatavilla itsepäivityksenä heinäkuussa 2021.

## <a name="update-release-33"></a>Päivitysjulkaisu 33

### <a name="bug-fixes"></a>Ohjelmavirhekorjauksia

**Aika ja kulu**

Seuraavat ongelmat on korjattu:

- Kaksi lukittua kenttää, **msdyn_description** ja **msdyn_externaldescription** ovat muokattavissa lähettämisen jälkeen.
- Virhesanoma tulee näyttöön, jos luodaan kulu, joka ei liity projektiin.
- Kun aikamerkintä luodaan, resurssirooliksi tulee oletusarvo passiivinen rooli.
- Takaisinvetoon ja poistettuun kuluun liittyviä kirjauskansion rivejä ei poisteta.
- Päivitä **Aikamerkinnän pikaluontilomakkeessa** **Projektitehtäväluettelo**-näkymä muuttaaksesi oletusarvoisesti tehtävän alkamispäiväksi näytettävä päivämäärä.
- Kun luot aikamerkinnän varattavissa olevan resurssin **Liittyvä**-välilehdessä, ajankirjaaminen luodaan virheellisesti kirjautuneena olevalle käyttäjälle päätason varattavissa olevan resurssin asemesta.
- **Joukkohyväksyntä MDD**-valintaikkunaan lisätään uusia kenttiä.

**Projektin suunnittelu**

Seuraavat ongelmat on korjattu:
- Projektin luonnin hidas suorituskyky, kun projektityötuntimalleja käytetään monitasoisten kalenterien kanssa.
- Jos alkamispäivä on päättymispäivää suurempi, projektimallissa näkyy virhe, koska kussakin kentässä on eroja aikakomponentissa.

**Resurssien hallinta**

Seuraavat ongelmat on korjattu:
- Resurssin käyttökyselyssä käytetään virheellistä parametria, ja XML-liidit johtavat virheellisiin suodatustuloksiin **Resurssin käyttö** -ruudukossa.
- **Varausten jatkaminen** -vahvistus näyttää virheellisen päättymispäivän varauksia varten.

**Myynti**

Seuraavat ongelmat on korjattu:
- Virheilmoitus tapahtuu luotaessa luokkahintaa, jonka arvot puuttuvat.
- Virheilmoitus tapahtuu luotaessa sopimusrivin välitavoitetta ilman tilausriviä.
