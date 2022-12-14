---
title: Tuotepohjaisten tarjousrivien yleiskatsaus
description: Tässä artikkelissa on tietoja tuotepohjaisten tarjousrivien käyttämisestä.
author: rumant
ms.date: 10/30/2020
ms.topic: overview
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: a260c0f51cc2d958281dbc6f0f711347cab85a9a
ms.sourcegitcommit: e0cbbe7c6f03d4978134405cf04bd8bc1d019f65
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/05/2022
ms.locfileid: "9826218"
---
# <a name="product-based-quote-lines-overview"></a>Tuotepohjaisten tarjousrivien yleiskatsaus

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
