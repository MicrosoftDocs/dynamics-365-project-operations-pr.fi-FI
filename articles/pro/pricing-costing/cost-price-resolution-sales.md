---
title: Arvioiden ja todellisten arvojen kustannushintojen selvittäminen – lite
description: Tässä aiheessa on tietoja siitä, miten arvioiden ja toteutuneiden kustannusten hinnat ratkaistaan.
author: rumant
manager: Annbe
ms.date: 10/13/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: bbb79fdc5c68d67530b5aa34fe6105211eff1768
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5274545"
---
# <a name="resolve-cost-prices-on-estimates-and-actuals---lite"></a>Arvioiden ja todellisten arvojen kustannushintojen selvittäminen – lite

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


[!INCLUDE[footer-include](../../includes/footer-banner.md)]