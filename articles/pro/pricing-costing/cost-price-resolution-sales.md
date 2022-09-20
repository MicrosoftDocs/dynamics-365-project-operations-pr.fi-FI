---
title: Projektiarvioiden ja toteutuneiden arvojen kustannusten määrittäminen
description: Tässä artikkelissa on tietoja kustannushintojen määrittämisestä projektin arvioissa ja toteutuneissa arvoissa.
author: rumant
ms.date: 09/01/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: c2295174df1ce766c6d1304f4e9c55d32d5c4775
ms.sourcegitcommit: 60a34a00e2237b377c6f777612cebcd6380b05e1
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/13/2022
ms.locfileid: "9475227"
---
# <a name="determine-cost-rates-for-project-estimates-and-actuals"></a>Projektiarvioiden ja toteutuneiden arvojen kustannusten määrittäminen

_**Käytetään:** Lite-käyttöönotto – kauppa proformalaskutukseen_

Kun arvioiden ja todellisten arvojen kustannushinnat määritetään Microsoft Dynamics 365 Project Operationsissa, järjestelmä käyttää ensin saapuvan arvioiden ja todellisten arvojen kontekstin valuuttaa kustannushinnaston määrittämiseksi. Erityisesti todellisten arvojen kontekstissa järjestelmä määrittää **Tapahtumapäivä**-kentän avulla, mitä hinnastoa käytetään. Saapuvan arvion tai toteutuneiden arvojen **Tapahtumapäivämäärä**-arvoa verrataan hinnastossa **Voimassaolon alkamispäivä (aikavyöhykkeestä riippumaton)**- ja **Voimassaolon päättymispäivä (aikavyöhykkeestä riippumaton)** -arvoihin. Kun kustannushinnasto on määritetty, järjestelmä määrittää kustannushinnan. 

## <a name="determining-cost-rates-in-estimate-and-actual-contexts-for-time"></a>Arvioitujen ja todellisten arvojen kustannushintojen selvittäminen ajalle

**Aika**-arviokonteksti viittaa seuraavaan:

- Tarjousrivin tiedot kohteelle **Aika**.
- Sopimusrivin tiedot kohteelle **Aika**.
- Resurssimääritykset projektissa.

Todellisten arvojen **Aika**-konteksti viittaa seuraavaan:

- Merkintä- ja korjauskirjauskansiorivit kohteelle **Aika**.
- Kirjauskansiorivit, jotka luodaan, kun aikamerkintä lähetetään.

Kun kustannushinnasto on määritetty, järjestelmä suorittaa oletuskustannushinnan syöttämisen seuraavasti.

1. Järjestelmä täsmäyttää **roolin** ja **resursointiyksikön** kenttien yhdistelmän arvioitujen tai todellisten arvojen kontekstissa kohteelle **Aika**, jotta se vastaisi hinnaston roolien hintarivejä hinnastoissa. Tässä täsmäytyksessä oletetaan, että käytät työn kustannushintojen vakiohinnoitteludimensioita. Jos olet määrittänyt järjestelmän vastaamaan kenttiä **roolin** ja **resurssiyksikön** sijaan tai sen lisäksi, käytetään toista yhdistelmää, jolla haetaan vastaava roolihintarivi.
1. Jos järjestelmä havaitsee roolien hintarivin, jolla on kustannushinta **roolin** ja **resurssiyksikön** yhdistelmälle, tätä kustannushintaa käytetään oletuskustannushintana.
1. Jos järjestelmä ei pysty täsmäyttämään **roolien** ja **resursointiyksikön** arvojen vastaavuutta, se hakee roolikohtaiset hintarivit, joilla on vastaavat arvot **Rooli**-kentälle, mutta **Resursointiyksikkö**-kentässä tyhjäarvo. Kun järjestelmä on löytänyt vastaavan roolien hintatietueen, se määrittää kyseisen tietueen kustannushinnan oletuskustannushinnaksi.

> [!NOTE]
> Jos määritetään erilainen **rooli**- ja **resursointiyksikkö**-kenttien priorisointi tai jos sinulla on muita suuremman prioriteetin dimensioita, edeltävä toiminta muuttuu vastaavasti. Järjestelmä noutaa roolin hintatietueet, joissa on arvoja, jotka vastaavat jokaista hinnoitteludimension arvoa prioriteettijärjestyksessä. Rivit, joilla on tyhjäarvot kyseisille dimensioille, tulevat viimeisenä.

## <a name="determining-cost-rates-on-actual-and-estimate-lines-for-expense"></a>Todellisten ja arvioitujen kulurivien kustannushintojen määrittäminen

**Kulu**-arviokonteksti viittaa seuraavaan:

- Tarjousrivin tiedot kohteelle **Kulu**.
- Sopimusrivin tiedot kohteelle **Kulu**.
- Projektin kuluarviot.

Todellisten arvojen **Kulu**-konteksti viittaa seuraavaan:

- Merkintä- ja korjauskirjauskansiorivit kohteelle **Kulu**.
- Kirjauskansiorivit, jotka luodaan, kun kulumerkintä lähetetään.

Kun kustannushinnasto on määritetty, järjestelmä suorittaa oletuskustannushinnan syöttämisen seuraavasti.

1. Järjestelmä täsmäyttää **Luokka**- ja **Yksikkö**-kenttien yhdistelmän arvioitujen tai todellisten arvojen kontekstissa kohteelle **Kulu**, jotta se vastaisi hinnaston luokkien hintarivejä hinnastoissa.
1. Jos järjestelmä löytää luokan hintarivin, jonka kustannushinta on **luokka**- ja **yksikkö**-kenttäyhdistelmässä, tätä kustannushintaa käytetään oletuskustannushintana.
1. Jos järjestelmä ei pysty yhdistämään **Luokka**- ja **Yksikkö**-arvoja, hinta saa oletusarvon **0** (nolla).
1. Jos järjestelmä ei pysty arviokontekstissa täsmäyttämään luokan hintariviä, mutta hinnoittelumenetelmä ei ole **Yksikköhinta**, kustannushinnan oletusarvo on **0** (nolla).

## <a name="determining-cost-rates-on-actual-and-estimate-lines-for-material"></a>Kustannusten arvojen määrittäminen materiaalin toteutuneiden arvojen ja arvioiden riveillä

**Materiaali**-arviokonteksti viittaa seuraavaan:

- Tarjousrivin tiedot kohteelle **Materiaali**.
- Sopimusrivin tiedot kohteelle **Materiaali**.
- Projektin materiaaliarviot.

Todellisten arvojen **Materiaali**-konteksti viittaa seuraavaan:

- Merkintä- ja korjauskirjauskansiorivit kohteelle **Materiaali**.
- Kirjauskansiorivit, jotka luodaan, kun Materiaalin käyttö -loki lähetetään.

Kun kustannushinnasto on määritetty, järjestelmä suorittaa oletuskustannushinnan syöttämisen seuraavasti.

1. Järjestelmä käyttää **Tuote**- ja **Yksikkö**-kenttien yhdistelmän arvioitujen tai todellisten arvojen kontekstissa kohteelle **Materiaali**, jotta se vastaisi hinnaston nimikerivejä hinnastoissa.
1. Jos järjestelmä löytää hinnaston nimikerivin, jonka kustannushinta on **Tuote**- ja **yksikkö**-kenttäyhdistelmässä, tätä kustannushintaa käytetään oletuskustannushintana.
1. Jos järjestelmä ei pysty yhdistämään **Tuote**- ja **Yksikkö**-arvoja, yksikkökustannus saa oletusarvon **0** (nolla).
1. Jos arvioitujen tai todellisten arvojen kontekstissa järjestelmä ei pysty arviokontekstissa täsmäyttämään hinnaston nimikeriviä, mutta hinnoittelumenetelmä ei ole **Valuuttasumma**, yksikkökustannuksen oletusarvo on **0** (nolla). Näin käy, koska Project Operations tukee vain projektissa käytettyä materiaalien **Valuuttasumma**-hinnoittelutapaa.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
