---
title: Tuotehinnastot
description: Tässä aiheessa on tietoja luettelon hinnoittelun hinnastoista, joita käytetään projektitarjouksissa ja sopimuksissa.
author: rumant
ms.date: 04/05/2021
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: rumant
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 4feb7638dd7b6826e575d83457ae7f74ef6793bf
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/14/2022
ms.locfileid: "8593240"
---
# <a name="product-price-lists"></a>Tuotehinnastot

_**Käytetään:** Lite-käyttöönotto – kauppa proformalaskutukseen_

 Project Operationsissa **Tuotehinnastot** ja niihin liittyvät hinnastonimikkeen entiteetit tukevat tuotteiden hinnoittelutoimintoja tuotepohjaisilla tarjous- ja sopimusriveillä. Projektihinnastojen hinnastonimiketietueita käytetään projekteissa käytetyille tuotteille. 

Tuotteet olisi määritettävä siten, että niillä on tuoteluettelossa oletusarvoiset kustannusluettelot ja hinnastot. Oletusarvoisten kustannus- ja luettelohintojen määrittämisessä on käytettävä luettelohintaa, vakiokustannusta ja päivän hintaa. Oletusarvoisia luettelohintoja käytetään tarjousrivillä tai projektisopimusrivillä vain, kun järjestelmä ei löydä tarjouksen tai projektisopimuksen tuotehinnastosta hinnastoriviä tuotteelle.

Tuoteluettelon rivien kustannushintaa voi muuttaa tarjousten välillä. Tämä ominaisuus on tärkeä, koska jos kustannuksia ei seurata tarkasti, projektisitoumusten toiminnallista voittoa ei voi määrittää. Oletusarvoisesti kustannushintana käytetään tuotteen vakiokustannusta. Tarjousrivin oletusarvoista kustannushintaa voidaan kuitenkin päivittää, jos asianomaiselle tarjoukselle on olemassa eri kustannushinta.

## <a name="price-list-items"></a>Hinnaston nimikkeet

Voit lisätä tuotteita tuoteluettelosta eri hinnastoihin. Tuotteiden hinnastorivit viittaavat aina tiettyyn yksikköön. Hinnaston nimikkeisiin kuuluvan tuotteen hinnoittelu voidaan määrittää valuuttamääräisesti. Vaihtoehtoisesti se voidaan määrittää luettelohinnan, päivän hinnan tai vakiokustannuksen funktioksi.

Hinnoittelutoiminto tukee erilaisia pyöristysvaihtoehtoja, kun tuotteiden hinnat määritetään luettelohinnan, vakiokustannuksen tai päivän hinnan funktioiksi. Useiden hinnoittelutapojen ja pyöristysvaihtoehtojen hyödyntämisen lisäksi voit yhdistää hinnaston nimikkeisiin alennusluetteloja. 

 
## <a name="default-product-price-list"></a>Oletusarvoinen tuotehinnasto
Kussakin asiakastietueessa on **Oletushinnasto**-kenttä, jossa voit määrittää hinnaston, jossa käytetään asiakkaan valuuttaa. Tähän kenttään ei lisätä automaattisesti oletusarvoa. Kun tietyn asiakkaan kanssa on tehty mukautettu hinnoittelusopimus, voit käyttää tätä kenttää lisätäksesi hinnaston kyseiselle asiakkaalle.

Entiteetit Mahdollisuus, Tarjous ja Projektisopimukset lisäävät oletusarvoisia tuotehinnastoja seuraavassa järjestyksessä. Samaa järjestystä käytetään projektihinnastoissa.

1.  Tarjous
2.  Mahdollisuus
3.  Asiakas
4.  Yleiset asetukset 

Oletusarvoisesti tarjousrivin **Tuote**-rivillä luetellaan kaikki tarjouksen tuotehinnaston aktiiviset tuotteet. Jos tuote ei ole aktiivinen tai jos se on tuoteluonnos, se ei näy luettelossa, vaikka se olisi hinnastossa. 

Tuoteluettelon rivit lisätään laskuriveinä ensimmäiselle projektisopimusat varten luodulle laskulle. Nämä laskurivit voidaan poistaa laskuluonnoksessa. Tällöin rivit tulevat näkyviin myöhemmässä laskussa, kunnes ne on laskutettu tai kunnes lasku on lähetetty asiakkaalle. Tuotteen laskurivin osittaista määrää ei voi laskuttaa. Kun projektisopimuksen tuoterivit laskutetaan, luodaan todellisia arvoja. Näitä todellisia arvoja ei kuitenkaan linkitetä niihin liittyvään projektientiteettiin. Toisin sanoen tuoteperusteiset projektisopimusrivit ovat riippumattomia projektiperusteisesta käytöstä. 


[!INCLUDE[footer-include](../includes/footer-banner.md)]
