---
title: Myyntihintojen selvittäminen projektin arvioille ja toteutuneille arvoille
description: Tässä aiheessa on tietoja myyntihintojen selvittämisestä projektin arvioissa ja toteutuneissa arvoissa.
author: rumant
manager: Annbe
ms.date: 04/07/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 3bf4686b414300370e6b364834b33edad98b7f39
ms.sourcegitcommit: ac90be6106592f883a0de39a75836fb40255d65a
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/09/2021
ms.locfileid: "5877352"
---
# <a name="resolve-sales-prices-for-project-estimates-and-actuals"></a>Myyntihintojen selvittäminen projektin arvioille ja toteutuneille arvoille

_**Käytetään:** Lite-käyttöönotto – kauppa proformalaskutukseen_

Kun arvioiden ja todellisten arvojen myyntihinnat ratkaistaan Dynamics 365 Project Operationsissa, järjestelmä käyttää ensin liittyvän projektitarjouksen tai -sopimuksen päivämäärää ja valuuttaa myyntihinnan ratkaisemiseksi. Kun myyntihinnasto on ratkaistu, järjestelmä ratkaisee myynnin tai laskun hinnan.

## <a name="resolve-sales-rates-on-actual-and-estimate-lines-for-time"></a>Todellisten ja arvioitujen aikarivien kustannushintojen selvittäminen

Project Operationsissa arviorivien avulla voidaan osoittaa tarjousrivin ja sopimusrivin tiedot sekä projektin resurssivaraukset.

Kun myyntihinnasto on ratkaistu, järjestelmä suorittaa laskun hinnan oletusarvon seuraavasti:

1. Järjestelmä käyttää arviorivillä olevaa **roolin** ja **resursointiyksikön** kenttiä, jotta se vastaisi hinnaston roolien hintarivejä ratkaistuissa hinnastoissa. Tämä vastaavuus olettaa, että laskuhintojen hinnoittelun ulottuvuuksia käytetään. Jos olet määrittänyt hinnoittelun mihin tahansa muuhun kenttään **roolin** ja **resurssiyksikön** sijaan tai sen lisäksi, sitä yhdistelmää käytetään vastaavan roolihintarivin noutamiseen.
2. Jos järjestelmä havaitsee roolien hintarivin, jolla on laskutushinta **rooli**- ja **resurssiyksikkö**-kentän yhdistelmälle, tämä laskutushinta on oletuskustannushinta.
3. Jos järjestelmä ei pysty vastaamaan **roolien** ja **resursointiyksikön** kenttäarvojen vastaavuutta, se hakee roolikohtaiset hintarivit, joilla on vastaava osa, mutta **resurssiyksikön** tyhjäarvo. Kun järjestelmä on löytänyt vastaavan roolien hintatietueen, se määrittää kyseisen tietueen laskun hinnan oletusarvoksi. Tämä hakutoiminto olettaa, että myyntihinnoittelu dimensiona on **roolin** vs. **resurssiyksikön** suhteellinen prioriteetti.

> [!NOTE]
> Jos määritetään erilainen **roolien** priorisointi ja **resursointiyksikkö** tai jos sinulla on muita suurempia dimensioita, tämä toiminta muuttuu vastaavasti. Järjestelmä hakee roolille hintatietueet, joiden arvot vastaavat kutakin hinnoitteludimension arvoa prioriteettijärjestyksessä ja rivit, joilla on tyhjäarvoja, kun kyseiset dimensiot tulevat viimeiseksi.

## <a name="resolve-sales-rates-on-actual-and-estimate-lines-for-expense"></a>Todellisten ja arvioitujen kulurivien kustannushintojen selvittäminen

Project Operationsissa kustannusarvioita käytetään osoittamaan tarjous- ja sopimusrivin yksityiskohdat sekä projektin kustannusarviorivit.

Kun myyntihinnasto on ratkaistu, järjestelmä suorittaa yksikkömyyntihinnan oletusarvon seuraavasti:

1. Järjestelmä käyttää arviorivillä **Luokka**- ja **Yksikkö**-kenttäyhdistelmää kustannusten sovittamiseksi ratkaistun hinnaston luokan hintariveihin.
2. Jos järjestelmä löytää luokan hintarivin, jonka myyntihinta on **luokka**- ja **yksikkö**-kenttäyhdistelmässä, tämä myyntihinta on oletusarvo.
3. Jos järjestelmä löytää vastaavan luokan hintarivin, myyntihinnan oletusarvona voidaan käyttää hinnoittelutapaa. Seuraavassa taulukossa on esitetty kuluhinnan oletuskäyttäytyminen Project Operationsissa.

    | Konteksti | Hinnoittelutapa | Oletushinta |
    | --- | --- | --- |
    | Arvio | Yksikköhinta | Luokan hintarivin perusteella |
    | &nbsp; | Kustannusten mukaan | 0.00 |
    | &nbsp; | Hinnankorotus | 0.00 |
    | Todellinen | Yksikköhinta | Luokan hintarivin perusteella |
    | &nbsp; | Kustannusten mukaan | Perustuu liittyviin todellisiin kustannuksiin |
    | &nbsp; | Hinnankorotus | Käyttämällä luokan hintarivillä määritettyä merkintää, joka liittyy liittyvän kustannuksen todelliseen yksikkökustannushintaan |

4. Jos järjestelmä ei pysty vastaamaan **luokan** ja **yksikön** kenttien arvoja, myyntihinnan oletusarvona on nolla (0).

## <a name="resolving-sales-rates-on-actual-and-estimate-lines-for-material"></a>Myynnin arvojen selvittäminen materiaalin toteutuneiden arvojen ja arvioiden riveillä

Project Operationsin materiaalin arviorivejä käytetään tarjousrivin ja sopimusrivin tietojen kirjaamiseen materiaaleille ja materiaalin arvioiriveille projektissa.

Kun myyntihinnasto on ratkaistu, järjestelmä suorittaa yksikkömyyntihinnan oletusarvon seuraavasti:

1. Järjestelmä käyttää arviointirivin **Tuote**- ja **Yksikkö**-kenttäyhdistelmiä yhdistämään materiaali hinnaston nimikkeiden riveihin ratkaistussa hinnastossa.
2. Jos järjestelmä löytää hinnaston nimikerivin, jolla on myyntihinta **Tuote**- ja **Yksikkö**-kentän yhdistelmälle ja hinnoittelutapa on **Valuuttasumma**, käytetään hinnastorivillä määritettyä myyntihintaa.
3. Jos **Tuote**- ja **Yksikkö**-arvot eivät täsmää, myyntihinta saa oletusarvon nolla.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
