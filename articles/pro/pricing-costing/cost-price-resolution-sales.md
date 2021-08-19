---
title: Kustannushintojen selvittäminen projektin arvioissa ja toteutuneissa arvoissa
description: Tässä aiheessa on tietoja kustannushintojen ratkaisemisesta projektin arvioissa ja toteutuneissa arvoissa.
author: rumant
ms.date: 04/07/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: a2a2df7672118a4a4d7748795174e8e8238dd7618a48437185879e06a253a381
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/06/2021
ms.locfileid: "6997557"
---
# <a name="resolve-cost-prices-on-project-estimates-and-actuals"></a>Kustannushintojen selvittäminen projektin arvioissa ja toteutuneissa arvoissa 

_**Käytetään:** Lite-käyttöönotto – kauppa proformalaskutukseen_

Jos haluat selvittää kustannushinnat ja kustannushinnaston arvioita ja todellisia arvoja varten, järjestelmä käyttää liittyvän projektin **päivämäärä**-, **valuutta**- ja **hankintayksikkö**-kenttien tietoja. Kun kustannushinnasto on ratkaistu, sovellus ratkaisee kustannushinnan.

## <a name="resolving-cost-rates-on-actual-and-estimate-lines-for-time"></a>Todellisten ja arvioitujen aikarivien kustannushintojen selvittäminen

Ajan arvioidut rivit viittaavat projektin ajan ja resurssin varausten tarjous- ja sopimusrivin tietoihin.

Kun kustannushinnasto on ratkaistu, Ajan arviointirivin **Rooli**- ja **Resursointiyksikkö**-kentät täsmäytetään hinnastossa oleviin roolihintariveihin. Tässä vastaavuudessa oletetaan, että käytät työn kustannushintojen vakiohinnoitteludimensioita. Jos olet määrittänyt järjestelmän vastaamaan kenttiä **roolin** ja **resurssiyksikön** sijaan tai sen lisäksi, käytetään toista yhdistelmää, jolla haetaan vastaava roolihintarivi. Jos sovellus havaitsee roolien hintarivin, jolla on kustannushinta **roolin** ja **resurssiyksikön** yhdistelmälle, tämä on oletuskustannushinta. Jos sovellus ei pysty vastaamaan **roolin** ja **resursointiyksikön** arvojen vastaavuutta, se hakee roolikohtaiset hintarivit, joilla on vastaava osa, mutta **resurssiyksikön** tyhjäarvo. Kun sille on määritetty roolien hintatietue, kustannushinta on oletusarvon mukaan kyseisestä tietueesta. 

> [!NOTE]
> Jos määritetään erilainen **roolien** priorisointi ja **resursointiyksikkö** tai jos sinulla on muita suurempia dimensioita, tämä toiminta muuttuu vastaavasti. Järjestelmä hakee roolille hintatietueet, joiden arvot vastaavat kutakin hinnoitteludimension arvoa prioriteettijärjestyksessä ja rivit, joilla on tyhjäarvoja, kun kyseiset dimensiot tulevat viimeiseksi.

## <a name="resolving-cost-rates-on-actual-and-estimate-lines-for-expense"></a>Todellisten ja arvioitujen kulurivien kustannushintojen selvittäminen

Kulun arvioidut rivit viittaavat projektin kulun ja kuluarvioiden tarjous- ja sopimusrivin tietoihin.

Kun kustannushinnasto on ratkaistu, järjestelmä käyttää kustannusarviorivin **Luokka**- ja **Yksikkö**-kenttien yhdistelmää täsmäyttämiseen ratkaistun hinnaston **Luokkahinta**-rivien kanssa. Jos järjestelmä löytää luokan hintarivin, jonka kustannushinta on **luokka**- ja **yksikkö**-kenttäyhdistelmässä, kustannushinta on oletusarvo. Jos järjestelmä ei pysty täsmäyttämään **Luokka**- ja **Yksikkö**-arvoja tai jos se pystyy löytämään vastaavan luokan hintarivin, mutta hinnoittelumenetelmä ei ole **Yksikköhinta**, kustannushinnan oletusarvo on nolla (0).

## <a name="resolving-cost-rates-on-actual-and-estimate-lines-for-material"></a>Kustannusten arvojen selvittäminen materiaalin toteutuneiden arvojen ja arvioiden riveillä

Materiaalin arviorivit viittaavat tarjouksen ja sopimusrivin tietoihin materiaaleille ja materiaalin arvioiriveihin projektissa.

Kun kustannushinnasto on selvitetty, järjestelmä käyttää yhdistelmää kentistä **Tuote** ja **Yksikkö** materiaalin arvion arviorivillä verratakseen sitä **Hinnaston nimikkeiden**-riveihin selvitetyssä hinnastossa. Jos järjestelmä löytää tuotehintarivin, jolla on kustannushinta **Tuotteen** ja **Yksikön** kenttien yhdistelmälle, kustannushinta saa oletusarvon. Jos järjestelmä ei pysty yhdistämään **Tuote**- ja **Yksikkö**-arvoja, tai se kykenee löytämään vastaavan hinnastonimikkeen rivin, mutta hinnoittelumenetelmä perustuu peruskustannuksiin tai nykyisiin kustannuksiin eikä kumpaakaan määritellä tuotteessa, yksikkökustannus saa oletusarvon nolla.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
