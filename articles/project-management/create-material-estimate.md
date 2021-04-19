---
title: Projektien materiaalien taloudelliset arviot
description: Tässä aiheessa on tietoja projektipohjaisten materiaalien määrittämisestä ja arvioista.
author: rumant
manager: Annbe
ms.date: 03/30/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 98e3611b2b3948aab09a3eadeac7b95b893812e9
ms.sourcegitcommit: 504c09365bf404c1f1aa9b5034c1e1e5bc9d0d54
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2021
ms.locfileid: "5788849"
---
# <a name="financial-estimates-for-materials-on-projects"></a>Projektien materiaalien taloudelliset arviot

_**Koskee:** Project Operationsin resurssiin / muuhun kuin resurssiin perustuvia skenaarioita, Lite-käyttöönotto-kaupasta proformalaskutukseen_

Dynamics 365 Project Operationsissa projektipäälliköt voivat määrittää projektiin perustuvia materiaalikustannuksia kullekin projektille tai tehtävälle. Kukin materiaaliarvio voidaan liittää tiettyyn projektitehtävään. Kulut luokitellaan eri kululuokkiin, jotka on määritetty organisaatiotasolla. Kunkin kululuokan hinnoittelu ja kustannuslaskenta määritetään hinnastossa. 

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
