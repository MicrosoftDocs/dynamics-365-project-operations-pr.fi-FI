---
title: Projektien materiaalien taloudelliset arviot
description: Tässä aiheessa on tietoja projektipohjaisten materiaalien määrittämisestä ja arvioista.
author: rumant
ms.date: 03/30/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 089158666dc8fd09cd5d2b615715ed8aaff5575a
ms.sourcegitcommit: e6090e1fef5f475a3cd56b78b6abca29f90da8f5
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/10/2022
ms.locfileid: "8737298"
---
# <a name="financial-estimates-for-materials-on-projects"></a>Projektien materiaalien taloudelliset arviot

_**Koskee:** Project Operationsin resurssiin / muuhun kuin resurssiin perustuvia skenaarioita, Lite-käyttöönotto-kaupasta proformalaskutukseen_

Dynamics 365 Project Operationsissa projektipäälliköt voivat määrittää projektiin perustuvia materiaalikustannuksia kullekin projektille tai tehtävälle. Kukin materiaaliarvio voidaan liittää tiettyyn projektitehtävään. Projekteihin käytettävät materiaalit voivat olla tuoteluettelon tuotteita tai käsin lisättyjä tuotteita. Kullekin tuotteen ja yksikön yhdistelmälle voidaan määrittää hinta projektien myynnin ja projektihinnastoissa kustannuksen projektihinnastoissa.  

Tarkastele, lisää tai poista projektimateriaaliarvio seuraavien vaiheiden mukaisesti.

1. Siirry **Projektit**-kohtaan ja valitse projekti, jota haluat päivittää.
2. Tarkastele **Materiaaliarviot**-välilehdessä projektimateriaaliarvioiden luetteloa.
3. Luo uusi materiaaliarvio valitsemalla **Uusi materiaaliarvio**. Voit myös valita poistettavan materiaaliarvion ja valita sitten **Poista materiaaliarvio**.

Seuraavassa taulukossa on tietoja projektin **Materiaaliarviorivin** kentistä. 

| **Kenttä** | **Kuvaus** | **Loppupään vaikutus** |
| --- | --- | --- |
| Tehtävä | Projektin tehtävien luettelo. Tähän sisältyvät yhteenveto ja lehtisolmun tehtävät. | Kun valitset tehtävän materiaaliarvioriville,se vaikuttaa tehtävän arvioituihin materiaalikustannuksiin ja arvioituun materiaalimyyntiin. Jos tämä kenttä on tyhjä, materiaaliarviota seurataan ja yhteenveto tehdään vain projektitasolla. |
| Valitse tuote |  Voit valinnaisesti määrittää, onko arviorivi aiemmin luodulle (luettelon) tuotteelle vai käsin lisättävälle tuotteelle. | Tämä kenttä määrittää, valitaanko tuote luettelosta vai lisätäänkö tuote käsin. |
| Tuote | Tuoteluettelon tuotteen tunnus. Kun valitset tuotetunnuksen, **Valitse tuote** -kentän arvoksi päivittyy automaattisesti **Aiemmin luotu** tuote. Tunnuksen avulla haetaan kustannus- ja myyntihinta hinnastosta. | Tämä kenttä ei vaikuta loppupään prosessiin. |
| Käsin lisätyn tuotteen kuvaus | Tekstikenttä, johon kirjoitetaan tuotteen nimi. Tätä kenttää käytetään vain, kun valitaan **Käsin lisättävä** **Valitse tuote** -kentässä.| Tämä kenttä ei vaikuta loppupään prosessiin. |
| Alkamispäivä | Ennustettu päivämäärä, jona materiaalia on tarkoitus käyttää. | Tämä kenttä ei vaikuta loppupään prosessiin. |
| Yksikköryhmä | Tämän kentän oletusarvo on tuoteluettelon tuotteen oletusyksikköryhmä. Voit päivittää kentän ja valita toisen yksikköryhmän. | Tämä kenttä ei vaikuta loppupään prosessiin. |
| Yksikkö | Tämän kentän arvo saadaan valitun tuotteen oletusyksiköstä. Voit päivittää kentän ja valita toisen yksikön. | Jos yksikköä muutetaan, oletusyksikköhinta ja kustannus ovat erilaiset. |
| Määrä | Projektissa käytettävä tuotteen arvioitu määrä. | Tämä kenttä ei vaikuta loppupään prosessiin. |
| Yksikkökustannus | Valitun tuotteen ja yksikköyhdistelmän yksikkökustannukset, jotka on määritetty soveltuvassa kustannusluettelossa. | Yksikkökustannus näkyy aina projektin kustannusvaluuttana. Jos tuote- ja yksikköasetusten yhdistelmälle ei ole määritetty yksikkökustannusta hinnastossa, yksikkökustannuksen oletusarvo on 0,00. |
| Yksikköhinta | Valitun tuotteen ja yksikköyhdistelmän hinta, joka on määritetty soveltuvassa myyntihinnastossa. | Yksikköhinta näkyy aina projektin kustannusvaluuttana. Jos tuote- ja yksikköasetusten yhdistelmälle ei ole määritetty yksikköhintaa hinnastossa, yksikköhinnan oletusarvo on 0,00.|
| Kokonaiskustannukset | Kustannussumma, joka lasketaan määrän \* yksikkökustannuksena.| Yksikkökustannuksen summa näkyy aina projektin kustannusvaluuttana. |
| Kokonaismyynti | Myyntisumma, joka lasketaan määrän \* yksikköhintana. | Myyntisumma näkyy aina projektin kustannusvaluuttana. |


[!INCLUDE[footer-include](../includes/footer-banner.md)]
