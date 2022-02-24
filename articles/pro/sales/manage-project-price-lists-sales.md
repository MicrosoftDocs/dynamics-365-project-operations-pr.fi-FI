---
title: Projektihinnastojen hallinta projektitarjouksissa
description: Tämä aihe tarjoaa tietoja tarjouksien projektihinnastojen käsittelystä.
author: rumant
manager: Annbe
ms.date: 03/30/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 912d2fad33ac02c3ba980da7eeb88eef5c331230
ms.sourcegitcommit: 5fd529f2308edfe9322082313e6d50146df56aca
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/06/2021
ms.locfileid: "5858604"
---
# <a name="manage-project-price-lists-on-project-quotes"></a>Projektihinnastojen hallinta projektitarjouksissa 

_**Käytetään:** Lite-käyttöönotto – kauppa proformalaskutukseen_

Projektitarjoukset on suunniteltu tukemaan useita päivämääräkohtaisia myyntihinnastoja. Dynamics 365 Project Operationsissa lisätään uusi liittyvä entiteetti nimeltä **Projektihinnastot**. Tällä entiteetillä on yksi-moneen-suhde projektitarjoukseen.

Projektin hinnastoilla hinnoitellaan aikaa, materiaalia ja kulutapahtumia projektissa. Kun tarjouksessa on yksi tai useampi projektihinnasto, näitä hinnastoja käytetään ajan, materiaalinen, kuluarvioiden ja toteutuneiden arvojen hinnoitteluun projekteissa, jotka liittyvät tarjoukseen tarjousrivin kautta.

Jos projektitarjouksessa ei ole projektihinnastoa, näyttöön tulee varoitussanoma. Sanomassa ilmoitetaan, että koska projektihinnastoja ei ole, arvioituja ja toteutuneita projektitöitä ja kuluja ei hinnoitella. Sen sijaan niillä on myyntiarvojen hintana nolla (0).

## <a name="associate-or-disassociate-a-project-price-list-on-a-project-quote"></a>Projektihinnaston liittäminen projektitarjoukseen tai liitoksen poistaminen

Jos haluat luoda tai valita tietyn hinnaston projektipohjaisen työn ja kulujen arviointia varten, tee seuraavat toimet.

1. Valitse tarjouksessa **Projektihinta**-välilehti ja valitse aliruudukossa **+ Lisää uusi projektihinnasto**.
2. Valitse hinnasto Pikaluonti-sivulla. Avattavassa luettelossa näkyvät kaikki hinnastot, joiden kontekstiksi on määritetty **Myynti** ja joiden valuutta vastaa tarjouksen valuuttaa.
4. Kirjoita projektihinnaston liitoksen kuvaus ja valitse **Tallenna ja sulje**.

Projektihinnaston liitos luodaan.

Voit toistaa tämän prosessin, jos haluat liittää projektitarjoukseen useamman kuin yhden projektihinnaston. Luo useita projektihinnastoja vain, jos kullakin liitetystä projektihinnastosta on eri voimassaolopäivämäärät.

> [!NOTE]
> Project Operations ei tue projektiinnastojen päällekkäisiä voimassaolopäivämääriä. Jos tapahtumalle on määritetty useita projektihinnastoja tiettynä päivämääränä, kyseisen tapahtuman hinnaksi tulee oletusarvona nolla (0).
Jos haluat poistaa projektihinnaston liitoksen, valitse projektihinnasto ja valitse sitten **Poista tarjouksen projektihinnasto**. Hinnasto poistetaan tarjouksen projektihinnastoista, mutta itse hinnastoa ei poisteta. Vain liitos tarjoukseen poistetaan.

## <a name="set-up-default-project-price-lists-on-a-quote"></a>Projektin oletushinnastojen määrittäminen tarjouksessa

Projektihinnastot voidaan määrittää oletusarvoksi projektitarjouksessa. Tämä asetus varmistaa, että kaikki organisaation tarjoukset alkavat aina vakiohinnastosta kyseiselle hintajaksolle.

### <a name="set-up-organizational-default-for-project-price-lists"></a>Organisaation oletusarvojen määrittäminen projektihinnastoille

1. Siirry kohtaan **Asetukset** > **Yleiset** > **Parametrit**.
2. Etsi **Aktiiviset parametrit** -luettelosivulla tietue ja avaa se kaksoisnapsauttamalla sitä. 
3. Valitse **Parametrit**-sivulla **Hinnasto**-välilehti. Näkyvissä on luettelo oletushinnastoista. Tämä on luettelo vakiokustannuksista ja myyntihinnastoista. Kun myyntihinnasto on liitetty tähän kaikille myyntivaluutoille, tämä varmistaa, että tämän myyntihinnasto on oletusarvo kaikissa asiakkaille luotavissa tarjouksissa, jotka käyttävät tätä valuuttaa.

### <a name="set-up-customer-specific-project-price-lists"></a>Asiakaskohtaisten projektihinnastojen määrittäminen

Asiakaskohtaiset projektihinnastot voidaan määrittää myös silloin, kun olet neuvotellut päähinnoittelusopimuksen asiakkaiden kanssa.

Jos haluat määrittää asiakaskohtaisen projektihinnaston, suorita seuraavat vaiheet.

1. Valitse **Myynti**-alueessa **Asiakkaat**.
2. Valitse ja avaa aktiivisten asiakkuuksien luettelosta asiakastietue, jolle sinulla on erikoishinnasto.
3. **Projektihinnastot**-välilehdessä voit luoda uuden hinnastoliitoksen, joka on juuri kyseiselle asiakkaalle määritetty projektihinnasto.

## <a name="create-custom-pricing-on-a-project-quote"></a>Mukautetun hinnoittelun luominen projektitarjoukseen

Kun sinulla on organisaation ja asiakaskohtaiset oletusprojektihinnastot, projektitarjoukset luodaan automaattisesti käyttäen näitä projektihinnastojen liitoksia. Joissakin tapauksissa tiettyä projektitarjousta varten on kuitenkin ehkä luotava mukautettu hinnoittelu. 

1. Tarkista **Projektihinnasto**-välilehden **Projektitarjous**-kohdan aliruudukossa, että mitään tiettyä hinnastotietuetta ei ole valittu.
2. Valitse **Luo mukautettu hinnoittelu**. Tämä kopioi kaikki tarjoukseen tällä hetkellä liittyvät vakiohinnastot ja liittää nämä kopiot tarjoukseen. Olemassa olevat liitokset vakiohinnastoihin poistetaan. Tämän jälkeen myyjä voi alkaa tehdä muokkauksia näihin kopioihin. Näitä muuttuneita hintoja sovelletaan vain tähän projektitarjoukseen.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
