---
title: Oletushinnastot
description: Tässä artikkelissa on tietoja oletusmyynti- ja tuotehinnastoista Project Operationsissa.
author: rumant
ms.date: 10/13/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 7a8f99cd03e5c2c15941c17469cc5632765b0fdc
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8917710"
---
# <a name="default-price-lists"></a>Oletushinnastot

_**Koskee:** Project Operationsin resurssiin / muuhun kuin resurssiin perustuvia skenaarioita, Lite-käyttöönotto-kaupasta proformalaskutukseen_

## <a name="sales-price-lists"></a>Myyntihinnastot

Jokainen Dynamics 365 Project Operationsissa oleva projektitarjous ja sopimus sisältää oletusmyyntihinnaston. 

### <a name="price-list-default-on-project-quotes"></a>Oletushinnasto projektitarjouksille
Järjestelmä viimeistelee seuraavan prosessin määrittäen projektitarjouksen oletushinnaston:

1. Järjestelmä tarkastelee hinnastoja, jotka on liitetty asiakkaan projektihinnastoihin. 
2. Jos asiakastietueeseen on liitetty projektihinnastoja, järjestelmä tarkastelee projektiparametreihin liitettyjä myyntihinnastoja, jotka vastaavat projektin tarjouksen valuuttaa.
3. Järjestelmä tarkistaa seuraavaksi niiden hinnastojen päivämäärän, jotka vastaavat projektitarjouksen päivämääräaluetta. Erityisesti päivämäärän, jolloin tarjous luotiin.
4. Jos projektitarjouksen päivämäärälle on käytettävissä useita hinnastoja, kaikki hinnastot ovat oletusarvoisesti projektitarjouksessa.
5. Jos projektitarjouksen päivämäärälle ei ole käytössä hinnastoja, projektitarjouksessa ei ole oletusprojektihinnastoa. Projektitarjouksessa näkyy varoitussanoma. Sanomassa ilmoitetaan, että projektin todellisia kuluja ja arvioita ei hinnoitella, koska liitteenä ei ole projektin hinnastoja.

### <a name="price-list-default-on-project-contracts"></a>Oletushinnasto projektisopimuksille 
Järjestelmä viimeistelee seuraavan prosessin määrittäen projektisopimuksen oletushinnaston:

1. Jos palvelusopimus luodaan tarjouksesta, tarjouksen projektihinnastot kopioidaan erikseen ja liitetään projektisopimukseen.
2. Jos palvelusopimus luodaan alusta alkaen, järjestelmä tarkastelee asiakkaan projektin hinnastoihin liitettyjä hinnastoja. Jos asiakastietueeseen ei ole liitetty projektihinnastoja, järjestelmä tarkastelee projektiparametreihin liitettyjä myyntihinnastoja, jotka vastaavat projektisopimuksen valuuttaa.
4. Järjestelmä tarkistaa seuraavaksi niiden hinnastojen päivämäärän, jotka vastaavat projektisopimuksen päivämääräaluetta. Erityisesti päivämäärän, jolloin sopimus luotiin.
5. Jos sopimuksen päivämäärälle on käytettävissä useita hinnastoja, kaikki hinnastot ovat oletusarvoisesti sopimuksessa.
6. Jos sopimuksen päivämäärälle ei ole käytössä hinnastoja, sopimuksessa ei ole oletusprojektihinnastoa. Projektisopimuksessa näkyy varoitussanoma. Sanomassa ilmoitetaan, että projektin todellisia kuluja ja arvioita ei hinnoitella, koska liitteenä ei ole projektin hinnastoja.

## <a name="cost-price-lists"></a>Kustannushinnastot

Kustannushinnastot eivät ole oletusarvoisesti missään Project Operationsin entiteetissä. Projektikustannuksissa käytettävän kustannushinnaston määrittäminen tehdään aina tällä hetkellä. Järjestelmä viimeistelee seuraavan prosessin määrittäen projektikulujen hinnaston:

1. Järjestelmä tutkii ensin hinnastot, jotka on liitetty projektin sopimusorganisaatioyksikköön.
2. Järjestelmä tarkastelee sen jälkeen niiden hinnastojen päivämäärää, jotka vastaavat saapuvan arvion tai todellisen rivin päivämäärää. Tässä tilanteessa *arviorivi* viittaa kolmeen Project Operationsin arviokontekstiin:

    - Projektin arviorivi
    - Tarjousrivin tiedot
    - Sopimusrivin tieto
  
3. Jos tulevan arvion tai todellisen päivämäärän kohdalla on useita tehokkaita hinnastoja, viimeksi luotu hinnasto on valittuna.
4. Jos projektin sopimusorganisaatioyksikköön ei ole liitetty projektihinnastoja, järjestelmä tarkastelee projektiparametreihin liitettyjä kuluhinnastoja, jotka vastaavat projektin tarjouksen valuuttaa.
5. Seuraavaksi järjestelmä tarkastelee niiden hinnastojen päivämäärää, jotka vastaavat saapuvan arvion tai todellisen rivin päivämäärää. 
6. Jos tulevan arvion tai todellisen päivämäärän kohdalla on useita tehokkaita hinnastoja, viimeksi luotu hinnasto on valittuna.
7. Jos projektiparametreihin, jotka vastaavat valuuttaa ja voimaantulopäivää, ei ole liitetty kustannushinnastoja, järjestelmäoletusarvona on, että kustannushinta on nolla (0) saapuvassa arviossa tai todellisella rivillä.


[!INCLUDE[footer-include](../includes/footer-banner.md)]