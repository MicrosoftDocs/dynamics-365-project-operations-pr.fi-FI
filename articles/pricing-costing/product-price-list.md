---
title: Tuotehinnastot
description: Tässä aiheessa on tietoja luettelon hinnoittelun hinnastoista, joita käytetään projektitarjouksissa ja sopimuksissa.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 702402854c0787dae0bde854c9c274f5c23c131f
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/28/2020
ms.locfileid: "4119594"
---
# <a name="product-price-lists"></a>Tuotehinnastot

_**Koskee:** Project Operationsin resurssiin / muuhun kuin resurssiin perustuvia skenaarioita, Lite-käyttöönotto-kaupasta proformalaskutukseen_

Hinnastot ja hinnaston nimike-entiteetit tukevat tuoteluettelon hinnoittelua. Yleensä tätä toimintoa käytetään projektitarjousten ja projektisopimusten luetteloperusteisissa riveissä.

Projektiperusteisilla riveillä sopimus edustaa kauppaa sen voittamisen jälkeen. Koska neuvotteluprosessi yleensä edeltää voittoa, tarjoukseen liitetty hinnoittelu kopioidaan aina sellaisenaan uuteen hinnastoon ja liitetään sopimukseen. uutta hinnastoa ei voi muuttaa sopimuksen laajuuden ulkopuolella. Tämä rajoitus auttaa suojaamaan ilmoitushinnastoa, joka neuvoteltiin päähinnastossa tapahtuvista hinnanmuutoksista.

Tuotteet olisi määritettävä siten, että niillä on tuoteluettelossa oletusarvoiset kustannusluettelot ja hinnastot. Oletusarvoisten kustannus- ja luettelohintojen määrittämisessä on käytettävä luettelohintaa, vakiokustannusta ja päivän hintaa. Oletusarvoisia luettelohintoja käytetään tarjousrivillä tai projektisopimusrivillä vain, kun järjestelmä ei löydä tarjouksen tai projektisopimuksen tuotehinnastosta hinnastoriviä tuotteelle.

Tuoteluettelon rivien kustannushintaa voi muuttaa tarjousten välillä. Tämä ominaisuus on tärkeä, koska jos kustannuksia ei seurata tarkasti, projektisitoumusten toiminnallista voittoa ei voi määrittää. Oletusarvoisesti kustannushintana käytetään tuotteen vakiokustannusta. Tarjousrivin oletusarvoista kustannushintaa voidaan kuitenkin päivittää, jos asianomaiselle tarjoukselle on olemassa eri kustannushinta.

## <a name="price-list-items"></a>Hinnaston nimikkeet

Voit lisätä tuotteita tuoteluettelosta eri hinnastoihin. Tuotteiden hinnastorivit viittaavat aina tiettyyn yksikköön. Hinnaston nimikkeisiin kuuluvan tuotteen hinnoittelu voidaan määrittää valuuttamääräisesti. Vaihtoehtoisesti se voidaan määrittää luettelohinnan, päivän hinnan tai vakiokustannuksen funktioksi.

PSA tukee erilaisia pyöristysvaihtoehtoja, kun hinnat määritetään luettelohinnan, vakiokustannuksen tai päivän hinnan funktioksi. Useiden hinnoittelutapojen ja pyöristysvaihtoehtojen hyödyntämisen lisäksi voit yhdistää hinnaston nimikkeisiin alennusluetteloja. 

Kun luot tarjoukselle uuden mukautetun hinnaston valitsemalla **Luo mukautettu hinnoittelu** **Projektitarjous**-sivulla, luodaan kopio hinnastosta, ja **Entiteetti**-kenttä uuden hinnaston otsikossa määritetään muotoon **Myyntientiteetti**. Uuden hinnaston nimeen lisätään tarjouksen nimi ja aikaleima. Voit myös käyttää uuden hinnaston nimeä ja tarjouksen nimeä mukautetuissa työnkuluissa, kun haluat käynnistää lisäarviointeja ja -hyväksyntöjä tarjouksille, joissa käytetään mukautettua hinnoittelua.

 
## <a name="default-product-price-list"></a>Oletusarvoinen tuotehinnasto
Kussakin asiakastietueessa on **Oletushinnasto**-kenttä, jossa voit määrittää hinnaston, jossa käytetään asiakkaan valuuttaa. Tähän kenttään ei lisätä automaattisesti oletusarvoa. Kun tietyn asiakkaan kanssa on tehty mukautettu hinnoittelusopimus, voit käyttää tätä kenttää lisätäksesi hinnaston kyseiselle asiakkaalle.

Entiteetit Mahdollisuus, Tarjous ja Projektisopimukset lisäävät oletusarvoisia tuotehinnastoja seuraavassa järjestyksessä. Samaa järjestystä käytetään projektihinnastoissa.

1.  Tarjous
2.  Mahdollisuus
3.  Asiakas
4.  Yleiset asetukset 

Oletusarvoisesti tarjousrivin **Tuote**-rivillä luetellaan kaikki tarjouksen tuotehinnaston aktiiviset tuotteet. Jos tuote ei ole aktiivinen tai jos se on tuoteluonnos, se ei näy luettelossa, vaikka se olisi hinnastossa. 

Tuoteluettelon rivit lisätään laskuriveinä ensimmäiselle projektisopimusat varten luodulle laskulle. Nämä laskurivit voidaan poistaa laskuluonnoksessa. Tällöin rivit tulevat näkyviin myöhemmässä laskussa, kunnes ne on laskutettu tai kunnes lasku on lähetetty asiakkaalle. Tuotteen laskurivin osittaista määrää ei voi laskuttaa. Kun projektisopimuksen tuoterivit laskutetaan, luodaan todellisia arvoja. Näitä todellisia arvoja ei kuitenkaan linkitetä niihin liittyvään projektientiteettiin. Toisin sanoen tuoteperusteiset projektisopimusrivit ovat riippumattomia projektiperusteisesta käytöstä. Materiaalien kulutusta projekteissa ei seurata.


[!INCLUDE[footer-include](../includes/footer-banner.md)]