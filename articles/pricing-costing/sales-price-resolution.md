---
title: Arvioiden ja todellisten arvojen myyntihintojen selvittäminen
description: Tämä aihe tarjoaa tietoja myyntihintojen ratkaisemisesta arvioiden ja todellisuuden mukaan.
author: rumant
manager: Annbe
ms.date: 10/19/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 8c18dd734312b2dd147381169f5c3dc38a68a601
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/28/2020
ms.locfileid: "4119549"
---
# <a name="resolve-sales-prices-for-estimates-and-actuals"></a>Arvioiden ja todellisten arvojen myyntihintojen selvittäminen

_**Käytetään:** Project Operationsin resursseihin ja ei-varastoitaviin perustuvissa skenaarioissa_

Kun arviot ja toteutuneet myyntihinnat on ratkaistu Dynamics 365 Project Operationsissa, järjestelmä käyttää ensin liittyvän projektitarjouksen tai palvelusopimuksen päivämäärää ja valuuttaa myyntihinnaston selvittämiseen. Kun myyntihinnasto on ratkaistu, järjestelmä ratkaisee myynnin tai laskun hinnan.

## <a name="resolve-sales-rates-on-actual-and-estimate-lines-for-time"></a>Todellisten ja arvioitujen aikarivien kustannushintojen selvittäminen

Project Operationsissa arviorivien avulla voidaan osoittaa tarjousrivin ja sopimusrivin tiedot sekä projektin resurssivaraukset.

Kun myyntihinnasto on ratkaistu, järjestelmä suorittaa laskun hinnan oletusarvon seuraavasti:

1. Järjestelmä käyttää arviorivillä olevaa **roolin**, **resurssiyrityksen** ja **resursointiyksikön** kenttiä, jotta se vastaisi hinnaston roolien hintarivejä ratkaistuissa hinnastoissa. Tämä vastaavuus olettaa, että laskuhintojen hinnoittelun ulottuvuuksia käytetään. Jos olet määrittänyt hinnoittelun mihin tahansa muuhun kenttään **roolin**, **resurssiyrityksen** ja **resurssiyksikön** sijaan tai sen lisäksi, sitä yhdistelmää käytetään vastaavan roolihintarivin noutamiseen.
2. Jos järjestelmä havaitsee roolien hintarivin, jolla on laskutushinta **rooli**-, **resurssiyritys**- ja **resurssiyksikkö** -kentän yhdistelmälle, tämä laskutushinta on oletuskustannushinta.
3. Jos järjestelmä ei pysty vastaamaan **roolien**, **resursointiyrityksen** ja **resursointiyksikön** kenttäarvojen vastaavuutta, se hakee roolikohtaiset hintarivit, joilla on vastaava osa, mutta **resurssiyksikön** tyhjäarvo. Kun järjestelmä on löytänyt vastaavan roolien hintatietueen, se määrittää kyseisen tietueen laskun hinnan oletusarvoksi. Tämä hakutoiminto olettaa, että myyntihinnoittelu dimensiona on **roolin** vs. **resurssiyksikön** suhteellinen prioriteetti.

> [!NOTE]
> Jos olet määrittänyt erilaisen priorisoinnin **roolille**, **resursointiyritykselle** ja **resursointiyksikölle** tai jos sinulla on muita suurempia dimensioita, tämä toiminta muuttuu vastaavasti. Järjestelmä hakee roolille hintatietueet, joiden arvot vastaavat kutakin hinnoitteludimension arvoa prioriteettijärjestyksessä ja rivit, joilla on tyhjäarvoja, kun kyseiset dimensiot tulevat viimeiseksi.

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


[!INCLUDE[footer-include](../includes/footer-banner.md)]