---
title: Arvioiden ja todellisten arvojen kustannushintojen selvittäminen
description: Tässä aiheessa on tietoja siitä, miten arvioiden ja toteutuneiden kustannusten hinnat ratkaistaan.
author: rumant
manager: Annbe
ms.date: 04/09/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 13903acc22e765ddc5bc1b87428ef3565f2b0a44
ms.sourcegitcommit: ac90be6106592f883a0de39a75836fb40255d65a
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/09/2021
ms.locfileid: "5877308"
---
# <a name="resolving-cost-prices-for-estimates-and-actuals"></a>Arvioiden ja todellisten arvojen kustannushintojen selvittäminen

_**Käytetään:** Project Operationsin resursseihin ja ei-varastoitaviin perustuvissa skenaarioissa_

Jos haluat selvittää kustannushinnat ja kustannushinnaston arvioita ja todellisia arvoja varten, järjestelmä käyttää liittyvän projektin **päivämäärä**-, **valuutta**- ja **hankintayksikkö**-kenttien tietoja. Kun kustannushinnasto on ratkaistu, sovellus ratkaisee kustannushinnan.

## <a name="resolving-cost-rates-on-actual-and-estimate-lines-for-time"></a>Todellisten ja arvioitujen aikarivien kustannushintojen selvittäminen

Ajan arvioidut rivit viittaavat projektin ajan ja resurssin varausten tarjous- ja sopimusrivin tietoihin.

Kun kustannushinnasto on ratkaistu, järjestelmä käyttää arviorivillä olevaa **roolin**, **resurssiyrityksen** ja **resursointiyksikön** kenttiä, jotta se vastaisi hinnaston roolien hintarivejä. Tämä vastine olettaa, että käytät valmiita hinnoitteludimensioita työvoimakustannukseen. Jos olet määrittänyt järjestelmän vastaamaan kenttiä **roolin**, **resurssiyrityksen** ja **resurssiyksikön** sijaan tai sen lisäksi, käytetään toista yhdistelmää, jolla haetaan vastaava roolihintarivi. Jos sovellus havaitsee roolien hintarivin, jolla on kustannushinta **roolille**, **resurssiyritykselle** ja **resurssiyksikön** yhdistelmälle, tämä on oletuskustannushinta. Jos sovellus ei pysty täysin yhdistämään **Roolin**, **Resursoivan yrityksen** ja **Resursoivan yksikön** arvoja, se hakee roolihinnan rivit vastaavasta roolin arvosta, mutta sillä on tyhjäarvoiset arvot **Resursoivalle yksikölle** ja **Resursoivalle yritykselle**. Kun vastaava roolihintatietue ja vastaava roolihinnan arvo on löytynyt, kustannushinta saa oletusarvon kyseisestä tietueesta. 

> [!NOTE]
> Jos määritetään erilainen **roolien** priorisointi, **resursointiyritys** ja **resursointiyksikkö** tai jos sinulla on muita suurempia dimensioita, tämä toiminta muuttuu vastaavasti. Järjestelmä noutaa roolin hintatietueet, joiden arvot vastaavat jokaista hinnoitteludimension arvoa prioriteetin mukaisessa järjestyksessä ja rivit, joilla on tyhjäarvot kyseisissä dimensioissa, ovat prioriteettijärjestyksessä viimeisiä.

## <a name="resolving-cost-rates-on-actual-and-estimate-lines-for-expense"></a>Todellisten ja arvioitujen kulurivien kustannushintojen selvittäminen

Kulun arvioidut rivit viittaavat projektin kulun ja kuluarvioiden tarjous- ja sopimusrivin tietoihin.

Kun kustannushinnasto on ratkaistu, järjestelmä käyttää arviorivillä **Luokka**- ja **Yksikkö**-kenttien yhdistelmää kulujen kohdentamiseksi ratkaistun hinnaston **Luokkahinta**-riveihin. Jos järjestelmä löytää luokan hintarivin, jonka kustannushinta on **luokka**- ja **yksikkö**-kenttäyhdistelmässä, kustannushinta on oletusarvo. Jos järjestelmä ei pysty vastaamaan **luokka**- ja **yksikkö**-arvoja tai jos se löytää vastaavan luokkahintarivin, mutta hinnoittelutapa ei ole **yksikköhinta**, kustannushinta on oletusarvona nolla (0).

## <a name="resolving-cost-rates-on-actual-and-estimate-lines-for-material"></a>Kustannusten arvojen selvittäminen materiaalin toteutuneiden arvojen ja arvioiden riveillä

Materiaalin arviorivit viittaavat tarjouksen ja sopimusrivin tietoihin materiaaleille ja materiaalin arvioiriveihin projektissa.

Kun kustannushinnasto on selvitetty, järjestelmä käyttää yhdistelmää kentistä **Tuote** ja **Yksikkö** materiaalin arvion arviorivillä verratakseen sitä **Hinnaston nimikkeiden**-riveihin selvitetyssä hinnastossa. Jos järjestelmä löytää tuotehintarivin, jolla on kustannushinta **Tuotteen** ja **Yksikön** kenttien yhdistelmälle, kustannushinta saa oletusarvon. Jos järjestelmä ei pysty yhdistämään **Tuote**- ja **Yksikkö**-arvoja, yksikkökustannus saa oletusarvon nolla. Tämä oletusarvoistuminen tapahtuu myös silloin, jos hinnastossa on vastaava nimikerivi, mutta hinnoittelutapa perustuu vakiokustannuksiin tai nykyisiin kustannuksiin, joita ei ole määritetty tuotteessa.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
