---
title: Toimittajan laskutus – käsite ja luonti
description: Tässä artikkelissa käsitellään toimittajan laskukäsitettä, käyttöskenaarioita ja toimittajan laskujen luontia Microsoft Dynamics 365 Project Operationsissa.
author: rumant
ms.date: 03/25/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: b57ec8cdb6097e6f2207056667aadfb43ee8acfc
ms.sourcegitcommit: b2224d1f3c0bd4925d647e6ca3960db81a209521
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/11/2022
ms.locfileid: "9261930"
---
# <a name="vendor-invoicing---concept-and-creation"></a>Toimittajan laskutus – käsite ja luonti

_**Käytetään:** Lite-käyttöönotto – kauppa proformalaskutukseen_

Microsoft Dynamics 365 Project Operationsin toimittajalaskutuksen avulla voidaan kirjata projektiin toimittajien palvelujen ja/tai materiaalien toimitusten kustannukset.

Kun palvelut ja/tai materiaalit alihankitaan toimittajalta, alihankintasopimus edustaa tämän toimittajan kanssa tehtyä sopimusta. Kun toimittaja toimittaa palvelut tai materiaalit vastaanotetaan ja käytetään projektitehtävissä, kustannukset kirjataan projektiin. Toimittaja lähettää säännöllisesti laskut, jotka tarkistetaan ja täsmäytetään projektiin tallennettuihin kustannuksiin. Kun tarkistusprosessi on valmis, toimittajan lasku vahvistetaan ja se vapautetaan maksua varten.

## <a name="scenarios-for-use"></a>Käyttöskenaarioita

Project Operationsin toimittajien laskujen avulla voidaan tukea kahta erillistä skenaariota.

### <a name="customers-use-the-full-subcontracting-experiences"></a>Asiakkaat käyttävät täysiä alihankkimiskokemuksia

Toimittajan laskujen käyttökokemusten avulla voidaan tarkistaa ja täsmäyttää aikakirjaukset, materiaalin käyttö ja kulumerkinnät, jotka liittyvät alihankintakomponentteihin toimittajan laskuriveillä. Tämän prosessin avulla voidaan tarkistaa toimittajan laskurivien tarkkuus. Kun tarkistusprosessi on valmis ja toimittajan lasku vahvistetaan, sovellus kumoaa toteutuneet tiedot, jotka on tallennettu hyväksytyissä aika-, kulu- ja materiaalikäyttölokeissa, ja luo uudet kustannusten toteutuneet arvot käyttämällä toimittajan laskurivejä.

### <a name="customers-dont-use-the-full-subcontracting-experiences-but-want-to-have-a-unified-view-of-costs-on-projects-in-project-operations"></a>Asiakkaat eivät käytä täysiä alihankkimiskokemuksia, mutta he haluavat yhtenäisen näkymän projektien kustannuksista Project Operationsissa

Jos seuraat alihankkijaprosessia kolmannen osapuolen järjestelmässä, voit kirjata kustannukset ulkopuolisesta järjestelmästä Project Operationsiin luomalla toimittajan laskuja, jotka eivät viittaa alihankintasopimuksiin. Näin projektipäälliköilläsi voi olla yksi yhtenäinen näkymä projektin kaikista kustannuksista.

## <a name="creation-of-vendor-invoices-in-project-operations"></a>Toimittajan laskujen luominen Project Operationsissa

Toimittajan laskut voidaan luoda kahdella tavalla:

- Toimittajan laskuluettelosivulta tai yksittäisen toimittajan laskun tietosivulta
- Alihankintasopimusluettelosivulta tai yksittäisen alihankintasopimuksen tietosivulta

### <a name="creation-from-the-vendor-invoice-list-page-or-details-page"></a>Luonti toimittajan laskuluettelosivulta tai tietosivulta

1. Siirry kohtaan **Ostaminen** \> **Toimittajan laskut**.
2. Valitse toimittajan laskuluettelosivulla tai yksittäisen toimittajan laskun tietosivulla **Uusi**, jos haluat luoda uuden toimittajan laskun.

Tällä tavalla luodut toimittajan laskut voivat viitata myös alihankintasopimukseen.

### <a name="creation-from-the-subcontract-list-page-or-details-page"></a>Luonti toimittajan alihankintasopimusten luettelosivulta tai tietosivulta

1. Siirry kohtaan **Ostaminen** \> **Alihankintasopimukset**.
2. Valitse ainakin yksi alihankintasopimus.
3. Valitse alihankintasopimusluettelosivulla tai yksittäisen alihankintasopimuksen tietosivulla **Luo toimittajan lasku**, jos haluat luoda uuden toimittajan laskun.

Jokaiselle valitsemallesi alihankintasopimukselle luodaan uusi **Luonnos**-tilassa oleva toimittajan lasku.

Tällä tavalla luotavat toimittajan laskut viittaavat aina toimittajan laskun otsikon alihankintasopimukseen. Jokainen alihankintasopimuksen rivi, jolla on aika- ja materiaalilaskutustapa, luo rivin toimittajan laskuun. Jokainen alihankintasopimuksen rivi, jolla on kiinteähintainen laskutustapa, luo toimittajan laskuun rivin jokaiselle alihankintasopimusrivin välitavoitteelle, jonka tila on **Valmis laskutettavaksi**.

Seuraavat kentät ja liittyvät tietueet kopioidaan alihankintasopimuksesta toimittajan laskun otsikkoon:

- Toimittaja.
- Liittyvät hinnastot kopioidaan toimittajan laskuun hinnastoina.
- Valuutta.
- Sopimusyksikkö.
- Maksuehdot.

Aika- ja materiaali -alihankintasopimusriveille kopioidaan seuraavat kentät ja liittyvät tietueet alihankintasopimusriviltä toimittajan laskuriville:

- Alihankintasopimuksen ja alihankintasopimusrivin viittaukset
- Tapahtumaluokka
- Rooli
- Tapahtumaluokka
- Tuotekentät
- Project
- Tehtävä
- Varattavissa oleva resurssi

Kiinteä hinta -alihankintasopimusriveille kopioidaan seuraavat kentät alihankintasopimusriviltä ja alihankintasopimusrivin välitavoitteesta toimittajan laskuriville:

- Alihankintasopimuksen ja alihankintasopimusrivin viittaukset.
- Tapahtumaluokka. Oletusarvon mukaan arvo on **Välitavoite**.
- Välitavoitteen nimi ja summa kopioidaan liittyvästä alihankintasopimusrivin välitavoitteesta.
- Käyttäjä voi valita projektin ja tehtävän toimittajan laskurivillä.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
