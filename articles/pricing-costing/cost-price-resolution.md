---
title: Projektipohjaisten arvioiden ja toteutuneiden arvojen kustannusten määrittäminen
description: Tässä artikkelissa on tietoja kustannushintojen määrittämisestä projektipohjaisissa arvioissa ja toteutuneissa arvoissa.
author: rumant
ms.date: 9/12/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 822a7bd8ae87d4fd4044d8b46347bfe1b4ca13ca
ms.sourcegitcommit: 60a34a00e2237b377c6f777612cebcd6380b05e1
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/13/2022
ms.locfileid: "9475269"
---
# <a name="determine-cost-rates-for-project-based-estimates-and-actuals"></a>Projektipohjaisten arvioiden ja toteutuneiden arvojen kustannusten määrittäminen

_**Käytetään:** Project Operationsin resursseihin ja ei-varastoitaviin perustuvissa skenaarioissa_

Kun arvioiden ja todellisten arvojen kustannushinnat määritetään Microsoft Dynamics 365 Project Operationsissa, järjestelmä käyttää ensin saapuvan arvioiden ja todellisten arvojen kontekstin valuuttaa myyntihinnaston määrittämiseksi. Erityisesti todellisten arvojen kontekstissa järjestelmä määrittää **Tapahtumapäivä**-kentän avulla, mitä hinnastoa käytetään. Saapuvan arvion tai toteutuneiden arvojen **Tapahtumapäivämäärä**-arvoa verrataan hinnastossa **Voimassaolon alkamispäivä (aikavyöhykkeestä riippumaton)**- ja **Voimassaolon päättymispäivä (aikavyöhykkeestä riippumaton)** -arvoihin. Kun kustannushinnasto on määritetty, järjestelmä määrittää kustannushinnan.

## <a name="determining-cost-rates-in-estimate-and-actual-contexts-for-time"></a>Arvioitujen ja todellisten arvojen kustannushintojen selvittäminen ajalle

**Aika**-arviokonteksti viittaa seuraavaan:

- Tarjousrivin tiedot kohteelle **Aika**.
- Sopimusrivin tiedot kohteelle **Aika**.
- Resurssimääritykset projektissa.

Todellisten arvojen **Aika**-konteksti viittaa seuraavaan:

- Merkintä- ja korjauskirjauskansiorivit kohteelle **Aika**.
- Kirjauskansiorivit, jotka luodaan, kun aikamerkintä lähetetään.

Kun kustannushinnasto on määritetty, järjestelmä suorittaa oletuskustannushinnan syöttämisen seuraavasti.

1. Järjestelmä täsmäyttää **roolin**, **resursointiyrityksen** ja **resursointiyksikön** kenttien yhdistelmän arvioitujen tai todellisten arvojen kontekstissa kohteelle **Aika**, jotta se vastaisi hinnaston roolien hintarivejä hinnastoissa. Tässä täsmäytyksessä oletetaan, että käytät työn kustannushintojen vakiohinnoitteludimensioita. Jos olet määrittänyt järjestelmän vastaamaan muita kenttiä **roolin**, **resurssiyrityksen** ja **resurssiyksikön** sijaan tai niiden lisäksi, käytetään toista yhdistelmää, jolla haetaan vastaava roolihintarivi.
1. Jos järjestelmä havaitsee roolien hintarivin, jolla on kustannushinta **roolille**, **resurssiyritykselle** ja **resurssiyksikön** yhdistelmälle, tämä on oletuskustannushinta.
1. Jos järjestelmä ei voi täsmäyttää **rooli**-, **resursoiva yritys** ja **resurssiyksikkö**-arvoja, se pudottaa pois alimman prioriteetin dimension, etsii roolin hintarivejä, jotka vastaavat kahta muuta dimensioarvoa, ja pudottaa edelleen asteittain dimensioita, kunnes vastaava roolihintarivi löytyy. Tietueen kustannushintaa käytetään oletuskustannushintana. Jos järjestelmä ei löydä vastaavaa roolin hintariviä, hinnaksi määritetään oletusarvoisesti **0** (nolla).

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

[!INCLUDE[footer-include](../includes/footer-banner.md)]
