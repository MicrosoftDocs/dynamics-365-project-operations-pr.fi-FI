---
title: Arvioiden ja todellisten arvojen kustannushintojen selvittäminen – lite
description: Tässä aiheessa on tietoja siitä, miten arvioiden ja toteutuneiden kustannusten hinnat ratkaistaan.
author: rumant
manager: Annbe
ms.date: 10/13/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 3fedf7b577e2372fb10ea85ea1e3caa9bf2f5ad0
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/30/2020
ms.locfileid: "4176787"
---
# <a name="resolve-cost-prices-on-estimates-and-actuals---lite"></a>Arvioiden ja todellisten arvojen kustannushintojen selvittäminen – lite

_**Käytetään:** Lite-käyttöönotto – kauppa proformalaskutukseen_

Jos haluat selvittää kustannushinnat ja kustannushinnaston arvioita ja todellisia arvoja varten, järjestelmä käyttää liittyvän projektin **päivämäärä**-, **valuutta**- ja **hankintayksikkö**-kenttien tietoja. Kun kustannushinnasto on ratkaistu, sovellus ratkaisee kustannushinnan.

## <a name="resolving-cost-rates-on-actual-and-estimate-lines-for-time"></a>Todellisten ja arvioitujen aikarivien kustannushintojen selvittäminen

Ajan arvioidut rivit viittaavat projektin ajan ja resurssin varausten tarjous- ja sopimusrivin tietoihin.

Kun kustannushinnasto on ratkaistu, järjestelmä käyttää ajan arviorivillä olevia **roolin** ja **resurssiyksikön** kenttiä, jotta se vastaisi hinnaston roolien hintarivejä. Tämä vastine olettaa, että käytät valmiita hinnoitteludimensioita työvoimakustannukseen. Jos olet määrittänyt järjestelmän vastaamaan kenttiä **roolin** ja **resurssiyksikön** sijaan tai sen lisäksi, käytetään toista yhdistelmää, jolla haetaan vastaava roolihintarivi. Jos sovellus havaitsee roolien hintarivin, jolla on kustannushinta **roolin** ja **resurssiyksikön** yhdistelmälle, tämä on oletuskustannushinta. Jos sovellus ei pysty vastaamaan **roolin** ja **resursointiyksikön** arvojen vastaavuutta, se hakee roolikohtaiset hintarivit, joilla on vastaava osa, mutta **resurssiyksikön** tyhjäarvo. Kun sille on määritetty roolien hintatietue, kustannushinta on oletusarvon mukaan kyseisestä tietueesta. 

> [!NOTE]
> Jos määritetään erilainen **roolien** priorisointi ja **resursointiyksikkö** tai jos sinulla on muita suurempia dimensioita, tämä toiminta muuttuu vastaavasti. Järjestelmä hakee roolille hintatietueet, joiden arvot vastaavat kutakin hinnoitteludimension arvoa prioriteettijärjestyksessä ja rivit, joilla on tyhjäarvoja, kun kyseiset dimensiot tulevat viimeiseksi.

## <a name="resolving-cost-rates-on-actual-and-estimate-lines-for-expense"></a>Todellisten ja arvioitujen kulurivien kustannushintojen selvittäminen

Kulun arvioidut rivit viittaavat projektin kulun ja kuluarvioiden tarjous- ja sopimusrivin tietoihin.

Kun kustannushinnasto on ratkaistu, järjestelmä käyttää arviorivillä **Luokka**- ja **Yksikkö**-kenttien yhdistelmää kulujen kohdentamiseksi ratkaistun hinnaston **Luokkahinta**-riveihin. Jos järjestelmä löytää luokan hintarivin, jonka kustannushinta on **luokka**- ja **yksikkö**-kenttäyhdistelmässä, kustannushinta on oletusarvo. Jos järjestelmä ei pysty vastaamaan **luokka**- ja **yksikkö**-arvoja tai jos se löytää vastaavan luokkahintarivin, mutta hinnoittelutapa ei ole **yksikköhinta**, kustannushinta on oletusarvona nolla (0).
