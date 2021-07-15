---
title: Tuotepohjaisten tarjousrivien yleiskatsaus – lite
description: Tässä aiheessa on tietoja tuotepohjaisten tarjousrivien käyttämisestä.
author: rumant
ms.date: 10/30/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.custom: intro-internal
ms.openlocfilehash: 8b904f9abd3d2505c5397906f63a5ae8ff4be41b
ms.sourcegitcommit: 0fafe022731f0e1e8693382ff906e3f8541d34ca
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 07/07/2021
ms.locfileid: "6369822"
---
# <a name="product-based-quote-lines-overview---lite"></a>Tuotepohjaisten tarjousrivien yleiskatsaus – lite

_**Käytetään:** Lite-käyttöönotto – kauppa proformalaskutukseen_

Dynamics 365 Project Operationsissa voidaan luoda tuotepohjaisia tarjousrivejä. Tuotepohjaiset tarjousrivit voidaan lisätä manuaalisesti, tai ne voivat olla tuoteluettelon nimikkeitä.

## <a name="product-catalog"></a>Tuoteluettelo

Kullakin tuoteluettelon tuotteella on oletusarvoinen yksikkö ja yksikköryhmä. Jos useilla tuotteilla on sama määritejoukko, voit luoda tuoteperheen, jotka jakavat nämä määritteet. 

Tässä esimerkissä yritys myy tilauskäyttöoikeuksia erilaisille ohjelmistoille. Kaikilla tilausohjelmistoilla on seuraavat kaksi määritettä:

- Käyttäjien määrä
- Tilausten kesto mitataan kuukausina

Tällaista luetteloa ylläpidetään luomalla **Tilausohjelmisto**-niminen tuoteperhe ja lisäämällä käyttäjien määrä ja tilauksen kesto määritteinä. Seuraavaksi voit lisätä yksittäisiä tuotteita **Tilausohjelmisto**-tuoteperheeseen.

## <a name="add-product-catalog-items-to-a-project-quote"></a>Tuoteluettelon nimikkeiden lisääminen projektitarjoukseen

**Projektitarjous**- ja **Projektisopimus**-sivuilla on oma osa projektipohjaisille riveille ja tuotepohjaisille riveille. Tuotepohjaisten rivien tarjous- tai projektisopimusrivin avattava luettelo sisältää kaikki tuotehinnaston tuotteet ja yksiköt. Voit lisätä myös tuotteita, jotka eivät sisälly tuotehinnastoon.

Lisäksi voit valita tuotteita muista hinnastoista tai suoraan tuoteluettelosta. Kun valitset tuotteita suoraan tuoteluettelosta, kyseisen tuotteen oletushinnastoa käytetään tuotteen myyntihinnan määrittämiseen. Jos oletushinnastoa ei ole määritetty, hinnaksi määritetään nolla (0).

Jos tarjousrivi perustuu tuoteluetteloon, voit korvata myyntihinnan suoraan tarjousrivillä. **Hinnoittelu**-kentän tarjousrivillä on kaksi mahdollista arvoa:

- **Ohita hinnoittelu**
- **Käytä oletusta**

Jos valitset **Ohita hinnoittelu**, oletushintaa ei määritetä. Tuotteelle on sen sijaan annettava hinta tarjousrivillä. Jos valitset **Käytä oletusta**, oletusmyyntihintaa käytetään ja kenttä lukitaan, joten sitä ei voi muokata.

Oletusmyyntihinnat annetaan tarjouksen tuotepohjaisilla riveillä. **Hinnoittelu** -kentän arvoksi määritetään sitten **Ohita hinnoittelu**, jotta voit muokata tarjousrivien oletushintaa. Tämä on Project Operations -kohtainen Dynamics 365 Salesin tuotepohjaisen rivitoiminnan ohitus.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]