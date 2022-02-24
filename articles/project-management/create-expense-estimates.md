---
title: Projektien kulujen taloudelliset arviot
description: Tässä aiheessa on tietoja projektipohjaisten kulujen määrittämisestä tai arvioinnista.
author: rumant
manager: Annbe
ms.date: 03/19/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: ad4901b1264289f1da881154bc147fc3f8da698f
ms.sourcegitcommit: 386921f44f1e9a8a828b140206d52945de07aee7
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/22/2021
ms.locfileid: "5701778"
---
# <a name="financial-estimates-for-expenses-on-projects"></a>Projektien kulujen taloudelliset arviot
_**Koskee:** Project Operationsin resurssiin / muuhun kuin resurssiin perustuvia skenaarioita, Lite-käyttöönotto-kaupasta proformalaskutukseen_

Dynamics 365 Project Operationsissa projektipäälliköt voivat määrittää projektiin perustuvia kuluja kullekin projektille tai tehtävälle. Kukin kulunimike voidaan liittää tiettyyn projektitehtävään. Kulut luokitellaan eri kululuokkiin, jotka on määritetty organisaatiotasolla. Kunkin kululuokan hinnoittelu ja kustannuslaskenta määritetään hinnastossa. 

Voit tarkastella, lisätä tai poistaa projektikuluja tekemällä seuraavat toimet.

1. Siirry kohtaan **Projektit** ja valitse projekti, jota haluat käsitellä.
2. Valitse **Projektiarviot**-välilehti ja tarkastele projektikulujen luetteloa.
3. Lisää kulu valitsemalla **Uusi kulu**. Voit myös valita poistettavan kulun ja valita sitten **Poista kulu**.

Seuraavassa taulukossa on tietoja projektin **kuluarviorivin** kentistä. 

| **Kenttä** | **Kuvaus** | **Loppupään vaikutus** |
| --- | --- | --- |
| Tehtävä | Projektin tehtävien luettelo. Tähän sisältyvät yhteenveto ja lehtisolmun tehtävät. | Kun kuluarvioriville valitaan tehtävä, se vaikuttaa tehtävän arvioituihin kulukustannuksiin ja arvioituun kulumyyntiin. Jos tämä kenttä jätetään tyhjäksi, kuluarviota seurataan ja yhteenveto tehdään vain projektitasolla. |
| Luokka | Niiden tapahtumaluokkien luettelo, joissa on linkitettyjä kululuokkia sovelluksessa. | Luokan valitseminen määrittää hinnoittelua ja kustannuslaskentaa kuluarviorivillä. |
| Alkamispäivä | Kulun ennustettu päivämäärä. | Tämä kenttä ei vaikuta loppupään prosessiin. |
| Yksikköryhmä | Tämän kentän oletusarvo tulee yksikköryhmästä, joka on määritetty valitulle luokalle oletusarvoksi. Voit päivittää kentän ja valita toisen yksikköryhmän. | Tämä kenttä ei vaikuta loppupään prosessiin. |
| Yksikkö | Tämän kentän arvoksi on oletusarvona valitun luokan oletusyksikkö. Voit päivittää kentän ja valita toisen yksikön. | Jos yksikköä muutetaan, oletusyksikköhinta ja kustannus ovat erilaiset. |
| Määrä | Sen arvioidun kulun määrä, jonka sinulle aiheutuu. | Tämä kenttä ei vaikuta loppupään prosessiin. |
| Yksikkökustannus | Valitun luokan ja yksikköyhdistelmän kustannukset, jotka on määritetty soveltuvassa kustannusluettelossa | Yksikkökustannus näkyy aina projektin kustannusvaluuttana. |
| Yksikköhinta | Valitun luokan ja yksikköyhdistelmän hinta, joka on määritetty soveltuvassa hinnastossa. | Yksikköhinta näkyy aina projektin kustannusvaluuttana. |
| Kokonaiskustannukset | Kustannussumma, joka lasketaan määrän \* yksikkökustannuksena.| Yksikkökustannuksen summa näkyy aina projektin kustannusvaluuttana. |
| Kokonaismyynti | Myyntisumma, joka lasketaan määrän \* yksikköhintana. | Myyntisumma näkyy aina projektin kustannusvaluuttana. |


[!INCLUDE[footer-include](../includes/footer-banner.md)]
