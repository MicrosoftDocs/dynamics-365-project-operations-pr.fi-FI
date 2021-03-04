---
title: Tuotepohjaisten tarjousrivien yleiskatsaus – lite
description: Tässä aiheessa on tietoja tuotepohjaisten tarjousrivien käyttämisestä.
author: rumant
manager: Annbe
ms.date: 10/30/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: f6aa428c486f149308ad078f9d7a80a0be0f0f04
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/30/2020
ms.locfileid: "4178184"
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