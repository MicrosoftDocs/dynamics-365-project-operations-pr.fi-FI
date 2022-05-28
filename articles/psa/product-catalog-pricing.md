---
title: Tuoteluettelon hinnoittelu
description: Tämä aihe sisältää tietoja siitä, miten tuoteluettelun hinnoittelu toimii Dynamics 365 Project Service Automationissa (PSA:ssa).
author: rumant
ms.custom:
- dyn365-projectservice
ms.date: 03/07/2019
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
ms.reviewer: johnmichalak
ms.openlocfilehash: 6cf50a09226bd6fdb803fd1fd379fec80838be75
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/14/2022
ms.locfileid: "8600646"
---
# <a name="product-catalog-pricing"></a>Tuoteluettelon hinnoittelu 

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]


Hinnastot ja hinnaston nimike-entiteetit tukevat tuoteluettelon hinnoittelua. Yleensä tätä toimintoa käytetään projektitarjousten ja projektisopimusten luetteloperusteisissa riveissä.

Projektiperusteisilla riveillä sopimus edustaa kauppaa sen voittamisen jälkeen. Koska neuvotteluprosessi yleensä edeltää voittoa, tarjoukseen liitetty hinnoittelu kopioidaan aina sellaisenaan uuteen hinnastoon ja liitetään sopimukseen. uutta hinnastoa ei voi muuttaa sopimuksen laajuuden ulkopuolella. Tämä rajoitus auttaa suojaamaan ilmoitushinnastoa, joka neuvoteltiin päähinnastossa tapahtuvista hinnanmuutoksista.

Tuotteet olisi määritettävä siten, että niillä on tuoteluettelossa oletusarvoiset kustannusluettelot ja hinnastot. Oletusarvoisten kustannus- ja luettelohintojen määrittämisessä on käytettävä luettelohintaa, vakiokustannusta ja päivän hintaa. Oletusarvoisia luettelohintoja käytetään tarjousrivillä tai projektisopimusrivillä vain, kun järjestelmä ei löydä tarjouksen tai projektisopimuksen tuotehinnastosta hinnastoriviä tuotteelle.

Tuoteluettelon rivien kustannushintaa voi muuttaa tarjousten välillä. Tämä ominaisuus on tärkeä, koska jos kustannuksia ei seurata tarkasti, projektisitoumusten toiminnallista voittoa ei voi määrittää. Oletusarvoisesti kustannushintana käytetään tuotteen vakiokustannusta. Tarjousrivin oletusarvoista kustannushintaa voidaan kuitenkin päivittää, jos asianomaiselle tarjoukselle on olemassa eri kustannushinta.

## <a name="price-list-items"></a>Hinnaston nimikkeet

Voit lisätä tuotteita tuoteluettelosta eri hinnastoihin. Tuotteiden hinnastorivit viittaavat aina tiettyyn yksikköön. Hinnaston nimikkeisiin kuuluvan tuotteen hinnoittelu voidaan määrittää valuuttamääräisesti. Vaihtoehtoisesti se voidaan määrittää luettelohinnan, päivän hinnan tai vakiokustannuksen funktioksi.

PSA tukee erilaisia pyöristysvaihtoehtoja, kun hinnat määritetään luettelohinnan, vakiokustannuksen tai päivän hinnan funktioksi. Useiden hinnoittelutapojen ja pyöristysvaihtoehtojen hyödyntämisen lisäksi voit yhdistää hinnaston nimikkeisiin alennusluetteloja. 

> ![Tuotteiden lisääminen luettelosta eri hinnastoihin.](media/basic-guide-16.png)

Kun luot tarjoukselle uuden mukautetun hinnaston valitsemalla **Luo mukautettu hinnoittelu** **Projektitarjous**-sivulla, PSA luo kopion hinnastosta, ja **Entiteetti**-kenttä uuden hinnaston otsikossa määritetään muotoon **Myyntientiteetti**. Uuden hinnaston nimeen lisätään tarjouksen nimi ja aikaleima. Voit myös käyttää uuden hinnaston nimeä ja tarjouksen nimeä mukautetuissa työnkuluissa, kun haluat käynnistää lisäarviointeja ja -hyväksyntöjä tarjouksille, joissa käytetään mukautettua hinnoittelua.

 
## <a name="default-product-price-list"></a>Oletusarvoinen tuotehinnasto
Kussakin asiakastietueessa on **Oletushinnasto**-kenttä, jossa voit määrittää hinnaston, jossa käytetään asiakkaan valuuttaa. PSA:ssa tähän kenttään ei lisätä automaattisesti oletusarvoa. Kun tietyn asiakkaan kanssa on tehty mukautettu hinnoittelusopimus, voit käyttää tätä kenttää lisätäksesi hinnaston kyseiselle asiakkaalle.

Entiteetit Mahdollisuus, Tarjous ja Projektisopimukset lisäävät oletusarvoisia tuotehinnastoja seuraavassa järjestyksessä. Samaa järjestystä käytetään projektihinnastoissa.

1.  Tarjous
2.  Mahdollisuus
3.  Asiakas
4.  PSA:n yleiset asetukset

Oletusarvoisesti tarjousrivin **Tuote**-rivillä luetellaan kaikki tarjouksen tuotehinnaston aktiiviset tuotteet. Jos tuote ei ole aktiivinen tai jos se on tuoteluonnos, se ei näy luettelossa, vaikka se olisi hinnastossa. 

Tuoteluettelon rivit lisätään laskuriveinä ensimmäiselle projektisopimusat varten luodulle laskulle. Nämä laskurivit voidaan poistaa laskuluonnoksessa. Tällöin rivit tulevat näkyviin myöhemmässä laskussa, kunnes ne on laskutettu tai kunnes lasku on lähetetty asiakkaalle. PSA:ssa ei voi laskuttaa tuotteen laskurivin osittaista määrää. Kun projektisopimuksen tuoterivit laskutetaan, luodaan todellisia arvoja. Näitä todellisia arvoja ei kuitenkaan linkitetä niihin liittyvään projektientiteettiin. Toisin sanoen tuoteperusteiset projektisopimusrivit ovat riippumattomia projektiperusteisesta käytöstä. PSA ei seuraa materiaalien kulutusta projekteissa.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
