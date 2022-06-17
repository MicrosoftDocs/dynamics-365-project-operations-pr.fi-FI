---
title: Projektipohjaisten sopimusrivien yleiskatsaus – lite
description: Tässä artikkelissa on tietoja tuotepohjaisista sopimusriveistä.
author: rumant
ms.date: 10/07/2020
ms.topic: overview
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 4ad1fe6d5d56468d887535ddf107eefed3cbd28d
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8919872"
---
# <a name="product-based-contract-lines-overview---lite"></a>Projektipohjaisten sopimusrivien yleiskatsaus – lite

_**Käytetään:** Lite-käyttöönotto – kauppa proformalaskutukseen_

Dynamics 365 Project Operationsissa voidaan luoda tuotepohjaisia sopimusrivejä. Tuotepohjaiset sopimusrivit voivat olla käsin lisättyjä rivejä tai ne voivat olla tuoteluettelon nimikkeitä.

## <a name="product-catalog"></a>Tuoteluettelo

Tuoteluettelossa olevilla tuotteilla on oletusarvoinen yksikkö ja yksikköryhmä. Jos useilla tuotteilla on sama määritejoukko, voit luoda tuoteperheen, jolla on myös kyseiset määritteet. Kaikki tuoteperheen tuotteet perivät saman määritejoukon.

Tässä esimerkissä yritys myy tilauskäyttöoikeuksia erilaisille ohjelmistoille. Kaikilla tilausohjelmistoilla on seuraavat kaksi määritettä:

- Käyttäjien määrä
- Tilausten kesto (kuukausina)

Jos haluat ylläpitää tämäntyyppistä luetteloa, luo tuoteperhe, jonka nimi on **tilausohjelmisto**. Lisää tuoteperheeseen määritteet **käyttäjien määrä** ja **tilausten kesto**. Lisää sitten yksittäiset tuotteet **tilausohjelmisto**-tuoteperheeseen.

## <a name="add-product-catalog-items-to-a-project-contract"></a>Lisää tuoteluettelon nimikkeet projektisopimukseen

Projektisopimuksissa on osioita kahdenlaisille riveille, projektiperusteisille ja tuoteperusteisille riveille. Tuotepohjaisia rivejä ovat kaikki tuotteet ja yksiköt palvelusopimuksen tuotehinnastossa. Tuotteita, jotka eivät sisälly sopimuksen tuotehinnastoon, voi lisätä.

Voit valita tuotteita muista hinnastoista tai suoraan tuoteluettelosta. Kun valitset tuotteita suoraan tuoteluettelosta, kyseisen tuotteen oletushinnastoa käytetään tuotteen myyntihinnan määrittämiseen. Jos oletushinnastoa ei ole määritetty, hinnaksi määritetään 0 (nolla).

Jos sopimusrivi perustuu tuoteluetteloon, voit korvata myyntihinnan suoraan sopimusrivillä. Sopimusrivillä on **hinnoittelu**-kenttä, jolla on kaksi arvoa:

- **Korvaa hinnoittelu**
- **Käytä oletusta**

Jos määrität **Hinnoittelu**-kentän arvoksi **Korvaa hinnoittelu**, oletushintaa ei määritetä. Anna projektin sopimusrivin tuotteen hinta. Jos määrität kentän arvoksi **Käytä oletusarvoa**, käytetään oletusmyyntihintaa eikä kenttää voi muokata.

Kun olet asentanut Project Operationsin, oletusmyyntihinnat syötetään sopimuksen tuoteperusteisille riveille. **Hinnoittelu**-kentän arvoksi määritetään **Korvaa hinnoittelu**, jotta voit muokata sopimusrivien oletushintaa. Tämä on Project Operations -kohtainen toiminto, joita käytetään Dynamics 365 Salesin tuotepohjaisiin riveihin.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]