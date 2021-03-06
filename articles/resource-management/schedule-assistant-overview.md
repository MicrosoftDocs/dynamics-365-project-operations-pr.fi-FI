---
title: Ajoitusavustajan yleiskatsaus
description: Tässä aiheessa on tietoja resurssien varaamisesta ajoitusavustajan avulla.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: da551e805f395e466952df1dbb7d193bdddba358
ms.sourcegitcommit: 56c42d7f5995a674426a1c2a81bae897dceb391c
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/01/2020
ms.locfileid: "3908068"
---
# <a name="schedule-assistant-overview"></a>Ajoitusavustajan yleiskatsaus

_**Koskee:** Project Operationsin resurssiin / muuhun kuin resurssiin perustuvia skenaarioita, Lite-käyttöönotto-kaupasta proformalaskutukseen_

Ajoitusavustajan avulla voit varata resursseja projektipäällikön määrittämien vaatimusten perusteella. Ajoitusavustaja käyttää resurssitarpeen parametreja löytääkseen resurssin. Ajoitusavustaja suosittelee resursseja, jotka vastaavat asiaankuuluvia vaatimuksia, kuten aikaikkunoita tai tarvittavia taitoja.

Kun tarvittavat resurssit on tunnistettu, resurssi- tai projektipäällikkö voi varata resurssin työhön.

## <a name="prerequisites"></a>Edellytykset

Ajoitusavustaja on osa Universal Resource Scheduling -ratkaisua. Tämä ratkaisu sisältyy ja asennetaan Dynamics 365 Project Operationsin, Dynamics 365 Field Servicee ja Dynamics 365 Customer Servicen kanssa.

## <a name="matching-requirements-and-resources"></a>Vastaavat tarpeet ja resurssit

Luotu resurssitarve perustuu esimerkiksi seuraaviin tietoihin:

-   Ominaisuudet
-   Roolit
-   Liiketoimintayksiköt
-   Resurssin asetukset
-   Työmäärän aikaväli
-   Aikavyöhyke

Ajoitusavustaja käyttää näitä tietoja resurssien suodattamiseen.

## <a name="launch-the-schedule-assistant"></a>Ajoitusavustajan käynnistäminen

Ajoitusavustaja voidaan käynnistää kahdella tavalla. Jos käytät hybriditilaa, voit valita Ryhmän jäsen -ruudukossa minkä tahansa ryhmän jäsenen, jonka resurssitarve on täyttämättä, ja valita sitten **Varaa**. Jos käytät keskitettyä tilaa, resurssipäällikkö etsii ja valitsee resurssin.

## <a name="schedule-assistant-filters"></a>Ajoitusavustajan suodattimet

Kun ajoitusavustaja on suoritettu, resurssitarpeen tiedot näkyvät vasemmanpuoleisessa ruudussa suodatettuina arvoina. Resurssipäällikkö tai projektiäällikkö voi hienosäätää tuloksia säätämällä suodattimia vastaamaan aikataulutuksen tarpeita.

Suodatusruudussa näkyvät työhön liittyvät asetukset, kuten seuraavat:

-   Työn aloitus- ja päättymisajat
-   Ominaisuudet
-   Roolit
-   Organisaatioyksiköt
-   Resursoiva yritys
-   Resurssityypit
-   Ensisijaiset resurssit
