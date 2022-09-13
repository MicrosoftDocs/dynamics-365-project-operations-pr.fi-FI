---
title: Oletushinnastot
description: Tässä artikkelissa on tietoja oletusmyynti- ja tuotehinnastoista Project Operationsissa.
author: rumant
ms.date: 09/01/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 50dbf74e31b9eb8d63c378e5fd718dc17c9691f4
ms.sourcegitcommit: 16c9eded66d60d4c654872ff5a0267cccae9ef0e
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/07/2022
ms.locfileid: "9410258"
---
# <a name="default-price-lists"></a>Oletushinnastot

_**Koskee:** Project Operationsin resurssiin / muuhun kuin resurssiin perustuvia skenaarioita, Lite-käyttöönotto-kaupasta proformalaskutukseen_

## <a name="sales-price-lists"></a>Myyntihinnastot

Jokainen Dynamics 365 Project Operationsissa oleva projektitarjous ja sopimus sisältää oletusmyyntihinnaston. 

### <a name="price-list-default-on-project-quotes"></a>Oletushinnasto projektitarjouksille
Järjestelmä viimeistelee seuraavan prosessin määrittäen projektitarjouksen oletushinnaston:

1. Järjestelmä tarkastelee hinnastoja, jotka on liitetty asiakkaan projektihinnastoihin. 
1. Jos asiakastietueeseen ei ole liitetty projektihinnastoja, järjestelmä tarkastelee projektiparametreihin liitettyjä myyntihinnastoja, jotka vastaavat projektin tarjouksen valuuttaa.
1. Järjestelmä tarkistaa seuraavaksi niiden hinnastojen päivämäärän, jotka vastaavat projektitarjouksen päivämääräaluetta. Erityisesti päivämäärän, jolloin tarjous luotiin.
1. Jos projektitarjouksen päivämäärälle on käytettävissä useita hinnastoja, kaikki hinnastot ovat oletusarvoisesti projektitarjouksessa.
1. Jos projektitarjouksen päivämäärälle ei ole käytössä hinnastoja, projektitarjouksessa ei ole oletusprojektihinnastoa. Projektitarjouksessa näkyy varoitussanoma. Sanomassa ilmoitetaan, että projektin todellisia kuluja ja arvioita ei hinnoitella, koska liitteenä ei ole projektin hinnastoja.

### <a name="price-list-default-on-project-contracts"></a>Oletushinnasto projektisopimuksille 
Järjestelmä viimeistelee seuraavan prosessin määrittäen projektisopimuksen oletushinnaston:

1. Jos palvelusopimus luodaan tarjouksesta, tarjouksen projektihinnastot kopioidaan erikseen ja liitetään projektisopimukseen.
1. Jos palvelusopimus luodaan alusta alkaen, järjestelmä tarkastelee asiakkaan projektin hinnastoihin liitettyjä hinnastoja. Jos asiakastietueeseen ei ole liitetty projektihinnastoja, järjestelmä tarkastelee projektiparametreihin liitettyjä myyntihinnastoja, jotka vastaavat projektisopimuksen valuuttaa.
1. Järjestelmä tarkistaa seuraavaksi niiden hinnastojen päivämäärän, jotka vastaavat projektisopimuksen päivämääräaluetta. Erityisesti päivämäärän, jolloin sopimus luotiin.
1. Jos sopimuksen päivämäärälle on käytettävissä useita hinnastoja, kaikki hinnastot ovat oletusarvoisesti sopimuksessa.
1. Jos sopimuksen päivämäärälle ei ole käytössä hinnastoja, sopimuksessa ei ole oletusprojektihinnastoa. Projektisopimuksessa näkyy varoitussanoma. Sanomassa ilmoitetaan, että projektin todellisia kuluja ja arvioita ei hinnoitella, koska liitteenä ei ole projektin hinnastoja.

## <a name="cost-price-lists"></a>Kustannushinnastot

Kustannushinnastot eivät ole oletusarvoisesti missään Project Operationsin entiteetissä. Projektikustannuksissa käytettävän kustannushinnaston määrittäminen tehdään aina tapahtumakohtaisesti. Järjestelmä viimeistelee seuraavan prosessin määrittäen projektikulujen hinnaston:

1. Järjestelmä tutkii hinnastot, jotka on liitetty projektin sopimusorganisaatioyksikköön.
1. Seuraavaksi järjestelmä tarkastelee niiden hinnastojen päivämäärää, jotka vastaavat saapuvan arvion tai todellisen kontekstin päivämäärää.

    - *Arvion konteksti* viittaa johonkin kolmesta Project Operationsin arviokontekstista:

        - Projektin arviorivi
        - Tarjousrivin tiedot
        - Sopimusrivin tieto

    - *Todellisten arvojen konteksti* viittaa johonkin kolmesta Project Operationsin todellisten arvojen lähteestä:

       - Manuaalisesti luodut kirjausrivit tai korjauskirjauskansiossa luotujen korjauskirjauskansiorivien kirjaaminen
       - Ajan, kulun tai materiaalin käyttölokien lähettämisen yhteydessä luodut kirjauskansiorivit
       - Laskurivin tiedot

    Kun Project Operations täsmäyttää saapuvan kirjauskansiorivin tai laskurivin yksityiskohtien päivämäärän voimassaoloa *todellisten arvojen kontekstissa*, se käyttää **Tapahtumapäivämäärä**-kenttää.

    - Jos saapuvan arvion tai todellisen kontekstin päivämäärän kohdalla on useita voimassa olevia hinnastoja, viimeksi luotu hinnasto valitaan.
    - Jos projektin sopimusorganisaatioyksikköön ei ole liitetty projektihinnastoja, järjestelmä tarkastelee projektiparametreihin liitettyjä kuluhinnastoja, jotka vastaavat projektin tarjouksen valuuttaa.

## <a name="enable-multi-currency-cost-price-list"></a>Ota käyttöön useiden valuuttojen kustannushinnasto

Tämä asetus löytyy kohdassa **Asetukset** \> **Parametrit**. Oletusarvo on **Ei**.

Kun tämä asetus on käytössä (eli arvoksi on määritetty **Kyllä**), järjestelmä toimii seuraavasti:

- Se sallii kustannushinnastojen (missä tahansa valuutassa) liittämisen organisaatioyksikköön. Esimerkiksi kustannushinnasto EUR-valuuttana voidaan liittää organisaatioyksikköön USD-valuuttana. Järjestelmä jatkaa niiden kustannushinnastojen tarkistamista, että organisaatioyksikköön liitettyjen kustannushintaluetteloiden voimassaolopäivä ei ole päällekkäinen.
- Se tarkistaa, että projektiparametreihin liitetyissä kustannushintaluetteloissa ei ole päällekkäisiä voimassaolopäivämääriä, vaikka niillä olisi eri valuutat. Tämä toiminta eroaa oletustoiminnasta (joka on siis toimintatapa, kun arvoksi on määritetty **Ei**). Oletuskäyttäytymisen mukaan vain ne kustannushintaluettelot, joissa on **sama** valuutta, tarkistetaan, että päivämäärä ei ole päällekkäinen.
- Saapuvan tapahtuman kontekstissa se määrittää kustannushinnaston vain päivämäärän voimassaolon perusteella. Tämä toimintatapa eroaa oletuskäyttäytymisestä, jossa järjestelmä valitsee kustannushinnaston, joka vastaa sekä projektin valuuttaa että päivämäärän voimassaoloa.

Näiden käyttäytymisen muutosten vuoksi Project Operationsin asiakkaat voivat ylläpitää yleistä kustannushinnastoa, joka koskee koko yritystä. Kussakin toimintojen valuutassa ei tarvitse olla omia hinnastoja. Yleisessä hinnastossa on päivämäärän voimassaolo, ja sen avulla kustannushinnat voidaan määrittää missä tahansa valuutassa tietylle hinnoitteludimension arvojen yhdistelmälle. Kustannushinnaston valuutan avulla voi määrittää oletusarvoja vain, kun **Roolihinnat**-, **Luokkahinnat**- ja **Hinnasto**-nimiketietueita luodaan. Sitä ei käytetä hinnaston määrittämiseen.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
