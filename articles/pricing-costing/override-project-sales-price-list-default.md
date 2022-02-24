---
title: Projektin myyntihinnastojen ohittaminen
description: Tässä aiheessa on tietoja mukautettujen myyntihinnastojen luomisesta.
author: rumant
manager: Annbe
ms.date: 10/22/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: af9baca540d89f4e5e616bdfdd6111bef29abe28
ms.sourcegitcommit: 656a9d03f260c29e988e2ff05b6e07ae0365d6d0
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/04/2020
ms.locfileid: "4672227"
---
# <a name="override-project-sales-price-lists"></a>Projektin myyntihinnastojen ohittaminen

_**Koskee:** Project Operationsin resurssiin / muuhun kuin resurssiin perustuvia skenaarioita, Lite-käyttöönotto-kaupasta proformalaskutukseen_

## <a name="customer-specific-project-price-lists"></a>Asiakaskohtaiset projektihinnastot

Asiakaskohtaiset hintasopimukset voidaan määrittää projektihinnastoiksi Dynamics 365 Project Operationsin tilitietueessa.

Määritä asiakaskohtainen projektihinnasto siirtymällä **Myynti**-alueella tilitietueeseen.

1. Avaa **Tilit**-luettelosivu.
2. Avaa **Tilit**-tietosivu etsimällä asiakastietue ja kaksoisnapsauttamalla sitä.
3. Valitse **Projektin hinnastot** -välilehdellä **+ Uusi projektihinnasto**.
4. Valitse **Uusi projektihinnasto** -sivulla hinnasto avattavasta luettelosta. Vain hinnastot, joiden kontekstiksi on määritetty **Myynti** ja joiden valuutta vastaa tilivaluuttaa, ovat tässä luettelossa.
5. Anna liitoksen nimi valitse sitten **Tallenna**. Asiakaskohtainen projektihinnasto luodaan. Tätä hinnastoa käytetään projektihintojen oletuksena tälle asiakkaalle projektitarjouksissa tai -sopimuksissa, joissa tarjouksen tai projektin sopimuksen luontipäivä on hinnaston voimassaolopäivänä.

## <a name="custom-pricing-on-project-quotes"></a>Projektitarjousten mukautettu hinnoittelu

Projektitarjouksissa projektin hinnoittelu voi alkaa oletusarvoisesti vakiohinnastosta, joka saadaan oletuksena asiakkaalta tai projektiparametreista.

Jos tarvitset projektiin liittyvään työhön mukautetun hinnoittelun jossakin tarjouksessa, saat sen projektihinnastoon liitetystä entiteetistä.

Määritä tarjouskohtainen projektin hinnoittelu seuraavien ohjeiden mukaisesti.

1. Avaa projektitarjous ja valitse **Projektihinnastot**-välilehti.
2. Valitse aliruudukossa **Luo mukautettu hinnoittelu**.

Kaikki tarjoukseen liitetyt projektihinnastot kopioidaan uusiin hinnastoihin. Uusien hinnastojen nimet vastaavat tarjouksen nimeä, ja niissä on päivämäärä- ja aikaleima, joka ilmaisee hinnastojen luontiajankohdan.

Voit käyttää näitä hinnastoja ja päivittää työn (roolin hinta) ja kulujen (luokkahinta) hinnat. Näitä hintoja käytetään vain kyseisessä projektitarjouksessa.

## <a name="price-lists-on-a-project-contract"></a>Projektisopimuksen hinnastot

Projektisopimuksen projektihinnoittelun oletusarvona on aina mukautettu hinnasto, jossa on sopimuksen nimi ja jonka nimeen on lisätty luontipäivä- ja aikaleima. Tämä pitää paikkansa riippumatta siitä. luontiinko sopimus silloin, kun tarjous voitettiin, vai luotiinko sopimus alusta alkaen. Voit tarvittaessa poistaa tämän liitoksen mukautettuun hinnastoon ja liittää sen sijaan vakiohinnaston projektisopimukseen.

Jos liität vakiohinnaston tarjouksen tai sopimuksen projektihinnastoihin, hinnaston hintoihin tehdyt muutokset vaikuttavat kaikkiin hinnastoa käyttäviin tarjouksiin ja sopimuksiin.
