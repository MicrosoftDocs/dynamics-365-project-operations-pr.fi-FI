---
title: Arvioiden ja todellisten arvojen kustannushintojen selvittäminen
description: Tässä aiheessa on tietoja siitä, miten arvioiden ja toteutuneiden kustannusten hinnat ratkaistaan.
author: rumant
manager: Annbe
ms.date: 10/13/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: c2fe2a15d38ab5a1f2a93c6db4ed6b7eb9bbd33d
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5275669"
---
# <a name="resolving-cost-prices-for-estimates-and-actuals"></a>Arvioiden ja todellisten arvojen kustannushintojen selvittäminen

_**Käytetään:** Project Operationsin resursseihin ja ei-varastoitaviin perustuvissa skenaarioissa_

Jos haluat selvittää kustannushinnat ja kustannushinnaston arvioita ja todellisia arvoja varten, järjestelmä käyttää liittyvän projektin **päivämäärä**-, **valuutta**- ja **hankintayksikkö**-kenttien tietoja. Kun kustannushinnasto on ratkaistu, sovellus ratkaisee kustannushinnan.

## <a name="resolving-cost-rates-on-actual-and-estimate-lines-for-time"></a>Todellisten ja arvioitujen aikarivien kustannushintojen selvittäminen

Ajan arvioidut rivit viittaavat projektin ajan ja resurssin varausten tarjous- ja sopimusrivin tietoihin.

Kun kustannushinnasto on ratkaistu, järjestelmä käyttää arviorivillä olevaa **roolin**, **resurssiyrityksen** ja **resursointiyksikön** kenttiä, jotta se vastaisi hinnaston roolien hintarivejä. Tämä vastine olettaa, että käytät valmiita hinnoitteludimensioita työvoimakustannukseen. Jos olet määrittänyt järjestelmän vastaamaan kenttiä **roolin**, **resurssiyrityksen** ja **resurssiyksikön** sijaan tai sen lisäksi, käytetään toista yhdistelmää, jolla haetaan vastaava roolihintarivi. Jos sovellus havaitsee roolien hintarivin, jolla on kustannushinta **roolille**, **resurssiyritykselle** ja **resurssiyksikön** yhdistelmälle, tämä on oletuskustannushinta. Jos sovellus ei pysty vastaamaan **roolien**, **resursointiyrityksen** ja **resursointiyksikön** arvojen vastaavuutta, se hakee roolikohtaiset hintarivit, joilla on vastaava osa, mutta **resurssiyksikön** tyhjäarvo. Kun sille on määritetty roolien hintatietue, kustannushinta on oletusarvon mukaan kyseisestä tietueesta. 

> [!NOTE]
> Jos määritetään erilainen **roolien** priorisointi, **resursointiyritys** ja **resursointiyksikkö** tai jos sinulla on muita suurempia dimensioita, tämä toiminta muuttuu vastaavasti. Järjestelmä hakee roolille hintatietueet, joiden arvot vastaavat kutakin hinnoitteludimension arvoa prioriteettijärjestyksessä ja rivit, joilla on tyhjäarvoja, kun kyseiset dimensiot tulevat viimeiseksi.

## <a name="resolving-cost-rates-on-actual-and-estimate-lines-for-expense"></a>Todellisten ja arvioitujen kulurivien kustannushintojen selvittäminen

Kulun arvioidut rivit viittaavat projektin kulun ja kuluarvioiden tarjous- ja sopimusrivin tietoihin.

Kun kustannushinnasto on ratkaistu, järjestelmä käyttää arviorivillä **Luokka**- ja **Yksikkö**-kenttien yhdistelmää kulujen kohdentamiseksi ratkaistun hinnaston **Luokkahinta**-riveihin. Jos järjestelmä löytää luokan hintarivin, jonka kustannushinta on **luokka**- ja **yksikkö**-kenttäyhdistelmässä, kustannushinta on oletusarvo. Jos järjestelmä ei pysty vastaamaan **luokka**- ja **yksikkö**-arvoja tai jos se löytää vastaavan luokkahintarivin, mutta hinnoittelutapa ei ole **yksikköhinta**, kustannushinta on oletusarvona nolla (0).


[!INCLUDE[footer-include](../includes/footer-banner.md)]