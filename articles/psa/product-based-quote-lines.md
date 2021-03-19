---
title: Tuotepohjaiset tarjousrivit
description: Tässä aiheessa on tietoja tuotepohjaisista tarjousriveistä.
author: rumant
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 03/06/2019
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 8bde88f5f2d00c09129c6a9363c09f6f6ad1dd90
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5284084"
---
# <a name="product-based-quote-lines"></a>Tuotepohjaiset tarjousrivit

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]


Dynamics 365 Project Service Automationissa voidaan luoda tuotepohjaisia tarjousrivejä. Tuotepohjaiset tarjousrivit voivat olla käsin lisättyjä rivejä tai ne voivat olla tuoteluettelon nimikkeitä.

## <a name="product-catalog"></a>Tuoteluettelo

Dynamics 365 -tuoteluettelossa olevilla tuotteilla on oletusarvoinen yksikkö ja yksikköryhmä. Jos useilla tuotteilla on sama määritejoukko, voit luoda tuoteperheen, jolla on myös kyseiset määritteet. Kaikki tuoteperheen tuotteet perivät saman määritejoukon.

Tässä esimerkissä yritys myy tilauskäyttöoikeuksia erilaisille ohjelmistoille. Kaikilla tilausohjelmistoilla on seuraavat kaksi määritettä:

- käyttäjämäärä 
- Tilausten kesto (kuukausina)

Hyvä tapa ylläpitää tällaista luetteloa on luoda tuoteperhe nimellä **Tilausohjelmisto**, jolla on määritteinä **Käyttäjämäärä** ja **Tilausten kesto**. Tämän jälkeen **Tilausohjelmisto**-tuoteperheeseen voidaan lisätä yksittäisiä tuotteita, kuten **Dynamics 365 Sales** tai **Dynamics 365 Field Service**.

## <a name="adding-product-catalog-items-to-a-project-quote"></a>Tuoteluettelon nimikkeiden lisääminen projektitarjoukseen

Projektitarjouksen ja projektisopimuksen sivuilla on osioita kahdenlaisille riveille: projektiperusteisille ja tuoteperusteisille riveille. Tuoteperusteisten rivien osalta Dynamics 365:ttä käytetään nimikkeiden lisäämiseen tuoteluettelosta tarjoukseen. Tarjous- tai projektisopimusrivin avattava luettelo sisältää kaikki tarjoukseen tai projektisopimukseen liitetyn tuotehinnaston tuotteet ja yksiköt. Voit myös lisätä tuotteita, jotka eivät sisälly tarjouksen tuotehinnastoon.

Lisäksi voit valita tuotteita muista hinnastoista tai voit valita tuotteita suoraan tuoteluettelosta. Kun valitset tuotteita suoraan tuoteluettelosta, kyseisen tuotteen oletushinnastoa käytetään tuotteen myyntihinnan määrittämiseen. Jos oletushinnastoa ei ole määritetty, hinnaksi määritetään 0 (nolla).

Jos tarjousrivi perustuu tuoteluetteloon, voit korvata myyntihinnan suoraan tarjousrivillä. Huomaa, että Dynamics 365:n tarjousrivillä on **Hinnoittelu**-kenttä. Käytettävissä on kaksi arvoa:

- Korvaa hinnoittelu  
- Käytä oletusta

Jos määrität tämän kentän arvoksi **Korvaa hinnoittelu**, Dynamics 365 ei määritä oletushintaa. Tuotteelle on määritettävä hinta tarjousrivillä. Jos kentän arvoksi määritetään **Käytä oletusta**, Dynamics 365 käyttää oletusmyyntihintaa ja lukitsee kentän muokkaamisen estämiseksi.

Kun olet asentanut PSA:n, oletusmyyntihinnat syötetään tarjouksen tuoteperusteisille riveille. **Hinnoittelu** -kentän arvoksi määritetään sitten **Korvaa hinnoittelu**, jotta voit muokata tarjousrivien oletushintaa.

> ![Hinnoittelun korvaamisen määritys](media/basic-guide-10.png)
 
## <a name="quantity-factors-for-products"></a>Tuotteiden määräkertoimet

PSA:ssa käytetään määräkertoimia tukemaan tilausperusteisten tuotteiden myyntiä. Tilausperusteisten tuotteiden osalta tarjouksen tai projektisopimuksen rivin määrä ilmaistaan käyttäjäkuukausien lukumääränä.

Yleensä tilausohjelmiston hinta tallennetaan luetteloon käyttäjäkohtaisena kuukausihintana. Voit kuitenkin käyttää muitakin aikakuvauksia. Myyntiprosessin aikana tarjousrivillä oleva hinta on yleensä se käyttäjäkohtainen kuukausihinta, jonka IT-myyjä on neuvotellut ja josta hän on antanut alennusta. Kullakin kaupalla on eri määrä käyttäjiä ja eri määrä tilauskuukausia. Tarjousrivin summan laskemiseen käytettävä määrä perustuu käyttäjämäärään ja tilauskuukausien määrään.

Tällaisen myynnin tukemista varten PSA:ssa on otettu käyttöön määräkertoimien konsepti. Määräkertoimet perustuvat Dynamics 365:n tuotemääritteisiin. Kun määrität tuotteelle tiettyjä ominaisuuksia, voit valita osan näistä määritteistä tai ne kaikki määräkertoimiksi.

PSA varmistaa, että määräkertoimiksi valitaan vain numeerisia ominaisuuksia tai tuoteominaisuuksia joilla on numeerinen tietotyyppi. Kun tarjousriville lisätään tuote, jolle on määritetty määräkertoimia, tarjousrivin **Määrä** -kentästä tulee vain luku -kenttä. Kun olet määrittänyt arvot tuoteominaisuuksille, jotka ovat määräkertoimia, PSA laskee tarjousrivin määrän.

Esimerkiksi Dynamics 365:llä voi olla seuraavat ominaisuudet: 

- **Käyttäjät** – Käyttäjien määrä 
- **Kuukaudet** – Tilauskuukausien määrä
- **Tuote-SKU** 

Ominaisuudet **Käyttäjät** ja **Kuukaudet** voidaan valita määräkertoimiksi muokkaamalla tuoterivin ominaisuuksia. 

> ![Ominaisuuksien Käyttäjät ja Kuukaudet valinta määräkertoimiksi](media/basic-guide-11.png)
 


[!INCLUDE[footer-include](../includes/footer-banner.md)]