---
title: Oletushinnastot
description: Tämä aihe tarjoaa tietoja oletusmyynti- ja tuotehinnastoista Project Operationsissa.
author: rumant
manager: Annbe
ms.date: 10/13/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: fd29a3fc9c873d46dd66a05ad100c7515177d6cd
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/28/2020
ms.locfileid: "4130934"
---
# <a name="default-price-lists"></a>Oletushinnastot

_**Koskee:** Project Operationsin resurssiin / muuhun kuin resurssiin perustuvia skenaarioita, Lite-käyttöönotto-kaupasta proformalaskutukseen_

## <a name="sales-price-lists"></a>Myyntihinnastot

Jokainen Dynamics 365 Project Operationsin projektitarjous ja palvelusopimus sisältää oletusmyyntihinnaston. 

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