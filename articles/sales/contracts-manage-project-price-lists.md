---
title: Projektihinnastojen hallinta projektisopimuksissa
description: Tässä aiheessa on tietoja projektisopimusten projektihinnastojen hallinnasta.
author: rumant
ms.date: 03/30/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 824026d0620de809c0366c86c2d4d13fe83d4d1ddd4c0dc1cc2645ff712705d5
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/06/2021
ms.locfileid: "6996477"
---
# <a name="manage-project-price-lists-on-project-contracts"></a>Projektihinnastojen hallinta projektisopimuksissa

_**Koskee:** Project Operationsin resurssiin / muuhun kuin resurssiin perustuvia skenaarioita, Lite-käyttöönotto-kaupasta proformalaskutukseen_

Dynamics 365 Project Operationsin projektisopimukset on suunniteltu tukemaan sopimuksessa useita voimassaolopäiviä käyttäviä myyntihinnastoja. Project Operationsissa on uusi **Projektihinnastot**-niminen liitetty entiteetti. Tällä entiteetillä on yksi moneen -suhde projektisopimukseen.

Projektin hinnastoilla hinnoitellaan aikaa, materiaalia ja kulutapahtumia projektissa. Kun sopimuksessa on yksi tai useampi projektihinnasto, näitä hinnastoja käytetään ajan, materiaalinen, kuluarvioiden ja toteutuneiden arvojen hinnoitteluun projekteissa, jotka liittyvät sopimukseen sopimusrivin kautta.

Kun projektisopimuksessa ei ole projektihinnastoja, näkyviin tulee varoitus siitä, että projektihinnastoja ei ole, ja arvioitasi, projektin todellista työtä, materiaalia ja kirjattuja kuluja ei hinnoitella. Myyntiarvoilla ei ole hintaa.

## <a name="associate-or-unassociate-a-project-price-list-on-a-project-contract"></a>Projektihinnaston liittäminen projektisopimukseen tai tämän liitoksen poistaminen

### <a name="create-or-associate-a-specific-price-list-for-estimating-project-based-work-material-and-expenses"></a>Tietyn hinnaston luominen tai liittäminen projektipohjaisen työn, materiaalin ja kulujen arvioimista varten

1. Valitse projektisopimuksessa **Projektihinnastot**-välilehti.
2. Valitse aliruudukossa **+ Lisää uusi projektihinnasto**.
3. Valitse hinnasto **Pikaluonti**-liukusäätimessä. 

  Avattavassa luettelossa on kaikki hinnastot, joiden kontekstiksi on määritetty **Myynti** ja joiden valutta vastaa sopimuksen valuuttaa.
  
4. Annan projektihinnaston liitoksen kuvaus, valitse **Tallenna** ja sulje sitten **Pikaluonti**-liukusäädin.

   Projektihinnaston liitos luodaan.
   
5. Jos haluat lisätä useita projektihinnastoja projektisopimukseen toista vaiheet 1–4. Luo useita projektihinnastoja vain, jos kullakin liitetyllä projektihinnastolla on eri voimassaolopäivä.

> [!NOTE]
> Project Operations ei tue projektihinnastoja, joissa on päällekkäiset voimassaolopäivät. Jos tietyn päivämäärän tapahtumalla on useita projektihinnastoja, kyseisen tapahtuman hinta palautetaan oletusarvoon nolla.

### <a name="remove-a-project-price-list-association"></a>Projektihinnaston liitoksen poistaminen

- Valitse projektihinnasto ja valitse sitten aliruudukossa **Poista sopimuksen hinnasto**. 

  Hinnasto poistetaan sopimuksen projektihinnastoista. Itse hinnastoa ei poisteta. Sen sijaan vain liitos sopimukseen poistetaan.

## <a name="set-up-automatic-defaulting-of-project-price-lists-on-a-contract"></a>Sopimuksen projektihinnaston automaattisten oletusarvojen määrittäminen

Projektihinnasto voidaan määrittää projektin oletushinnastoksi. Tämä määritys varmistaa, että kaikki organisaation sopimukset alkavat aina vakiomuotoisella projektihinnastolla kyseiselle ajanjaksolle.

### <a name="set-up-the-organizational-default-for-project-price-lists"></a>Organisaation oletusprojektihinnaston määrittäminen

1. Valitse ensin **Asetukset** > **Yleiset** ja sitten **Parametrit**.
2. Valitse **Aktiiviset parametrit** -luettelosivulla tietue ja avaa se kaksoisnapsauttamalla. Kun kaksoisnapsautat tietuetta, varmista, ettet napsauta sellaista kentän arvo, joka on hyperlinkki. 
3. Valitse **Aktiiviset parametrit** -sivulla **Hinnasto**-luettelo. Oletushinnastojen luettelo näkyy aliruudukossa. Kyseinen luettelo on vakiokustannusten ja myyntihinnastojen luettelo. **Myynti**-hinnaston liittäminen tässä kohdassa jokaiseen valuuttaan, jolla myyntiä tehdään, varmistaa, että myyntihinnasto on oletushinnasto jokaisessa sopimuksessa, joka luodaan kyseistä valuuttaa käyttävälle asiakkaalle.

### <a name="set-up-a-customer-specific-project-price-list"></a>Asiakaskohtaisen projektihinnaston määrittäminen

Asiakaskohtainen projektihinnasto voidaan määrittää, kun asiakkaiden kanssa on neuvoteltu hinnoittelun pääsopimus.

1. Valitse **Myynti** > **Asiakkaat**.
2. Valitse aktiivisten asiakkaiden luettelosta asiakas, jolla on erikoishinnasto.
3. Avaa asiakastietue valitsemalla se ja valitse sitten **Projektihinnastot**-välilehti. Aliruudukossa on näkyvissä kyseisen asiakkaan hinnastot. 
4. Luo kyseisestä asiakasta koskeva projektihinnasto luomalla tässä kohdassa uusi hinnastoliitos.

## <a name="custom-pricing-on-a-project-contract"></a>Projektisopimuksen mukautettu hinnoittelu

Kun organisaation oletusprojektihinnastot ja asiakaskohtaiset projektihinnastot ovat käytettävissä, luotavissa projektisopimuksissa käytetään automaattisesti näitä projektihinnastoliitoksia. Projektisopimuksen projektihinnastot kuitenkin kopioidaan aina siten, että niihin on liitetty päivämäärä ja sopimuksen nimi. Tili- ja projektipäälliköt voivat sitten muokata hintoja näissä kopioiduissa versioissa. Tällä tavoin muutettuja hintoja käytetään vain kyseisessä projektisopimuksessa.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
