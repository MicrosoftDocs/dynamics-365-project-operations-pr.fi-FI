---
title: Toimittajan säilytyksen yleiskatsaus
description: Tässä aiheessa on yleiskatsaus toimittajan säilytyksen ominaisuuksista.
author: sigitac
ms.date: 10/01/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 5f89904af5fb00eac46de834a438f412b371e74e
ms.sourcegitcommit: 098ea345ecfaf4445520094c32f5511b67e7953c
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/02/2021
ms.locfileid: "7594581"
---
# <a name="vendor-retention-overview"></a>Toimittajan säilytyksen yleiskatsaus

_**Käytetään:** Project Operationsin resursseihin ja ei-varastoitaviin perustuvissa skenaarioissa_

Organisaatiosi saattaa haluta säilyttää osan organisaatiosi projekteissa työskenteleville toimittajille tehtävistä maksuista. Esimerkiksi, ennen kuin organisaatio maksaa toimittajalle, organisaatio ehkä haluaa varmistaa, että toimittajien tuotteet ja palvelut vastaavat odotuksia.

Kun neuvottelet projektien ostoista toimittajien kanssa, voit määrittää toimittajan säilytysehdot, jotka sisältävät säilytyksen prosenttiluvun tai summan. Kun toimittaja toimittaa tuotteita ja palveluita, voit vähentää määritetyn säilytysprosentin tai summan maksusta toimittajalle. Kun projekti on valmis tai saavuttaa toimittajasopimuksessa määritetyn välivaiheen, voit vapauttaa säilytetyn summan ja luoda maksun toimittajalle.

## <a name="vendor-retention-example"></a>Toimittajan säilytyksen esimerkki

Seuraavassa esimerkissä esitetään, miten toimittajan laskun summan prosenttiosuus säilytetään projektin valmistumisprosentin perusteella.

Contoso Robotics USA on tehnyt sopimuksen Fabrikam-toimittajan kanssa 100 tunnin koulutuksesta välineiden uusimisprojektia varten. Palvelusopimuksen kokonaisarvo on USD 30 000 ja ostohinta USD 300 tuntia kohti.

Koulutus toimitetaan kolmessa vaiheessa seuraavan aikataulun mukaisesti:

- Vaihe 1: 50 tuntia tai 50 prosenttia projektista
- Vaihe 2: 30 tuntia tai 80 prosenttia koko projektista
- Vaihe 3: 20 tuntia tai 100 prosenttia projektista

Säilytysehdot näkyvät seuraavassa taulukossa.

| **Toimitettujen yksiköiden prosenttiosuus** | **Säilytyksen prosenttiosuus** | **Vapautuksen prosenttiosuus** |
| --- | --- | --- |
| 50 % | 20 % | 0 % |
| 80 % | 10 % | 10 % |
| 100% | 0 % | 100% |

Tapahtumien tuloksena saadaan seuraavat summat:

- Vaihe 1:
  - Maksettava summa on 50 x 300 eli 15 000.
  - 20 prosenttia määrästä eli 3 000 on säilytetty, ja se vapautetaan myöhemmin.
  - Toimittajalle maksettu summa on 12 000.
- Vaihe 2:
  - Maksettava summa on 30 x 300 eli 9 000.
  - 10 prosenttia määrästä eli 900 on säilytetty.
  - 10 prosenttia 3 000:sta, joka säilytettiin vaiheessa 1, eli 300, vapautetaan.
  - Toimittajalle maksettu summa on 8 400. Summa on 9 000, josta vähennetään 900:n säilytys ja johon lisätään 300, joka vapautettiin vaiheen 1 vapautuksessa.
- Vaihe 3:
  - Maksettava summa on 20 x 300 eli 6 000.
  - Mitään summaa ei säilytetä.
  - Vapautettu summa on 3 600. Summa on vaiheessa 1 säilytetty 3 000, josta vähennetään ensimmäisen vaiheen 300, joka vapautettiin vaiheessa 2 ja johon lisätään 900, joka säilytettiin vaiheessa 2.
  - Toimittajalle maksettu summa on 9 600. Summa on säilytetty summa 3 600, johon lisätään 6 000 vaiheen 3 valmistumisesta.

Toimittajalle kolmen vaiheen valmistumisen jälkeen maksettu kokonaissumma on 30 000, joka on ostotilauksen kokonaissumma (15 000 + 9 000 + 6 000).
