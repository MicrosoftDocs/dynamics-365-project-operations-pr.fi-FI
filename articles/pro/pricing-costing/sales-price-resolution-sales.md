---
title: Myyntihintojen määrittäminen projektin arvioille ja toteutuneille arvoille
description: Tässä artikkelissa on tietoja myyntihintojen määrittämisestä projektin arvioissa ja toteutuneissa arvoissa.
author: rumant
ms.date: 09/01/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 1288a571d50604ee400db9c16822719d0649628b
ms.sourcegitcommit: 60a34a00e2237b377c6f777612cebcd6380b05e1
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/13/2022
ms.locfileid: "9475180"
---
# <a name="determine-sales-prices-for-project-estimates-and-actuals"></a>Myyntihintojen määrittäminen projektin arvioille ja toteutuneille arvoille

_**Käytetään:** Lite-käyttöönotto – kauppa proformalaskutukseen_

Kun arvioiden ja todellisten arvojen myyntihinnat määritetään Microsoft Dynamics 365 Project Operationsissa, järjestelmä käyttää ensin saapuvan arvioiden ja todellisten arvojen kontekstin valuuttaa myyntihinnan määrittämiseksi. Erityisesti todellisten arvojen kontekstissa järjestelmä määrittää **Tapahtumapäivä**-kentän avulla, mitä hinnastoa käytetään. Saapuvan arvion tai toteutuneiden arvojen **Tapahtumapäivämäärä**-arvoa verrataan hinnastossa **Voimassaolon alkamispäivä (aikavyöhykkeestä riippumaton)**- ja **Voimassaolon päättymispäivä (aikavyöhykkeestä riippumaton)** -arvoihin. Kun myyntihinnasto on määritetty, järjestelmä määrittää myynnin tai laskun hinnan.

## <a name="determining-sales-rates-on-actual-and-estimate-lines-for-time"></a>Todellisten ja arvioitujen aikarivien kustannushintojen määrittäminen

**Aika**-arviokonteksti viittaa seuraavaan:

- Tarjousrivin tiedot kohteelle **Aika**.
- Sopimusrivin tiedot kohteelle **Aika**.
- Resurssimääritykset projektissa.

Todellisten arvojen **Aika**-konteksti viittaa seuraavaan:

- Merkintä- ja korjauskirjauskansiorivit kohteelle **Aika**.
- Kirjauskansiorivit, jotka luodaan, kun aikamerkintä lähetetään.
- Laskurivin tiedot kohteelle **Aika**. 

Kun myyntihinnasto on määritetty, järjestelmä syöttää laskun oletushinnan seuraavasti.

1. Järjestelmä täsmäyttää **roolin** ja **resursointiyksikön** kenttien yhdistelmän arvioitujen tai todellisten arvojen kontekstissa kohteelle **Aika**, jotta se vastaisi hinnaston roolien hintarivejä hinnastoissa. Tämä vastaavuus olettaa, että laskuhintojen käyttövalmiita hinnoitteludimensioita käytetään. Jos olet määrittänyt hinnoittelun mihin tahansa muuhun kenttään **roolin** ja **resurssiyksikön** sijaan tai sen lisäksi, sitä kenttien yhdistelmää käytetään vastaavan roolihintarivin noutamiseen.
1. Jos järjestelmä havaitsee roolien hintarivin, jolla on laskutushinta **rooli**- ja **resurssiyksikkö**-kentän yhdistelmälle, tätä laskutushintaa käytetään laskun oletushintana.
1. Jos järjestelmä ei pysty täsmäyttämään **roolien** ja **resursointiyksikön** arvojen vastaavuutta, se hakee roolikohtaiset hintarivit, joilla on vastaavat arvot **Rooli**-kentälle, mutta **Resurssiyksikkö**-kentässä tyhjäarvo. Kun järjestelmä on löytänyt vastaavan roolien hintatietueen, se määrittää kyseisen tietueen laskuhinnan oletuslaskuhinnaksi. Tämä hakutoiminto olettaa, että myyntihinnoittelu dimensiona on **roolin** vs. **resurssiyksikön** suhteellisen prioriteetin käyttövalmis määritys.

> [!NOTE]
> Jos määritetään erilainen **rooli**- ja **resursointiyksikkö**-kenttien priorisointi tai jos sinulla on muita suuremman prioriteetin dimensioita, edeltävä toiminta muuttuu vastaavasti. Järjestelmä noutaa roolin hintatietueet, joissa on arvoja, jotka vastaavat jokaista hinnoitteludimension arvoa prioriteettijärjestyksessä. Rivit, joilla on tyhjäarvot kyseisille dimensioille, tulevat viimeisenä.

## <a name="determining-sales-rates-on-actual-and-estimate-lines-for-expense"></a>Todellisten ja arvioitujen kulurivien kuluhintojen määrittäminen

**Kulu**-arviokonteksti viittaa seuraavaan:

- Tarjousrivin tiedot kohteelle **Kulu**.
- Sopimusrivin tiedot kohteelle **Kulu**.
- Projektin kuluarviorivit.

Todellisten arvojen **Kulu**-konteksti viittaa seuraavaan:

- Merkintä- ja korjauskirjauskansiorivit kohteelle **Kulu**.
- Kirjauskansiorivit, jotka luodaan, kun kulumerkintä lähetetään.
- Laskurivin tiedot kohteelle **Kulu**. 

Kun myyntihinnasto on määritetty, järjestelmä syöttää oletusyksikkömyyntihinnan seuraavasti.

1. Järjestelmä käyttää arviorivillä **Luokka**- ja **Yksikkö**-kenttäyhdistelmää **Kulu**-arviorivin täsmäyttämiseksi hinnaston luokan hintariveihin.
1. Jos järjestelmä löytää luokan hintarivin, jonka myyntihinta on **luokka**- ja **yksikkö**-kenttäyhdistelmässä, tätä myyntihintaa käytetään oletusarvona.
1. Jos järjestelmä löytää vastaavan luokan hintarivin, oletusmyyntihinnan syöttämiseen voidaan käyttää hinnoittelutapaa. Seuraavassa taulukossa on esitetty kuluhintojen oletuskäyttäytyminen Project Operationsissa.

    | Konteksti | Hinnoittelutapa | Oletushinta |
    | --- | --- | --- |
    | Arvio | Yksikköhinta | Luokan hintarivin perusteella. |
    |        | Kustannusten mukaan | 0.00 |
    |        | Hinnankorotus | 0.00 |
    | Todellinen | Yksikköhinta | Luokan hintarivin perusteella. |
    |        | Kustannusten mukaan | Perustuu liittyviin todellisiin kustannuksiin. |
    |        | Hinnankorotus | Käytetään luokan hintarivillä määritettyä merkintää, joka liittyy liittyvän kustannuksen todellisen arvon yksikkökustannushintaan. |

1. Jos järjestelmä ei pysty yhdistämään **Luokka**- ja **Yksikkö**-arvoja, myyntihinta saa oletusarvon **0** (nolla).

## <a name="determining-sales-rates-on-actual-and-estimate-lines-for-material"></a>Myynnin arvojen määrittäminen materiaalin toteutuneiden arvojen ja arvioiden riveillä

**Materiaali**-arviokonteksti viittaa seuraavaan:

- Tarjousrivin tiedot kohteelle **Materiaali**.
- Sopimusrivin tiedot kohteelle **Materiaali**.
- Projektin materiaaliarviorivit.

Todellisten arvojen **Materiaali**-konteksti viittaa seuraavaan:

- Merkintä- ja korjauskirjauskansiorivit kohteelle **Materiaali**.
- Kirjauskansiorivit, jotka luodaan, kun Materiaalin käyttö -loki lähetetään.
- Laskurivin tiedot kohteelle **Materiaali**. 

Kun myyntihinnasto on määritetty, järjestelmä syöttää oletusyksikkömyyntihinnan seuraavasti.

1. Järjestelmä käyttää **Materiaali**-arviointirivin **Tuote**- ja **Yksikkö**-kenttäyhdistelmiä täsmäytykseen hinnaston nimikerivien kanssa.
1. Jos järjestelmä löytää hinnaston nimikerivin, jolla on myyntihinta **Tuote**- ja **Yksikkö**-kentän yhdistelmälle ja jos hinnoittelutapa on **Valuuttasumma**, käytetään hinnastorivillä määritettyä myyntihintaa. 
1. Jos **Tuote**- ja **Yksikkö**-kentän arvot eivät vastaa toisiaan tai hinnoittelutapa on jokin muu kuin **Valuuttasumma**, myyntihinnaksi määritetään oletusarvon mukaan **0** (nolla). Näin käy, koska Project Operations tukee vain projektissa käytettyä materiaalien **Valuuttasumma**-hinnoittelutapaa.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
