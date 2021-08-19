---
title: Ennakkomaksujen aikataulun määrittäminen
description: Tässä aiheessa on tietoja ennakkomaksuaikataulun määrittämisestä Project Operationsissa.
author: rumant
ms.date: 10/22/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: a1cfd83837a91a8d1b3db6df688da6e216a90ada4735e5909a7e8cb26b87247d
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/06/2021
ms.locfileid: "6994362"
---
# <a name="set-up-a-retainer-schedule"></a>Ennakkomaksujen aikataulun määrittäminen

_**Koskee:** Project Operationsin resurssiin / muuhun kuin resurssiin perustuvia skenaarioita, Lite-käyttöönotto-kaupasta proformalaskutukseen_

Ennakkomaksuaikataulut määritetään **Projektisopimus**-sivulla Dynamics 365 Project Operationsissa.

1. Valitse **Projektisopimus**-sivun **Ennakot ja ennakkomaksut** -välilehdessä **Määritä ennakkomaksuaikataulu**.
2. Seuraavassa taulukossa olevat kentät näkyvät avautuvalla valintasivulla. Taulukko on esimerkki tavasta, jolla annetut arvot vaikuttavat luotavaan ennakkomaksuaikatauluun.

| Field | Kuvaus | Loppupään vaikutus |
| --- | --- | --- |
| Projektisopimuksen asiakas | Asiakas tai sopimus, josta tämä ennakkomaksu tai ennakko laskutetaan. | Jos sopimuksessa on useita asiakkaita ja niistä jokaiselta on laskutettava tietty ennakkomaksu- tai ennakkosumma, luo kullekin asiakkaalle manuaalisesti yksi lasku. |
| Ennakkomaksuaikataulun alku | Anna ennakkomaksuaikataulun alkamispäivä. | Tämä päivämäärä ei saa olla päivämäärä, jolloin ensimmäinen ennakkomaksu tai ennakko luodaan. Myös laskutustiheys vaikuttaa päivämäärään, jolloin ensimmäinen ennakkomaksu tai ennakko luodaan. |
| Ennakkomaksuaikataulun loppu | Anna ennakkomaksuaikataulun päättymispäivä. | Tämä päivämäärä ei saa olla päivämäärä, jolloin viimeinen ennakkomaksu tai ennakko luodaan. Myös laskutustiheys vaikuttaa päivämäärään, jolloin viimeinen ennakkomaksu tai ennakko luodaan. |
| Luotavien ennakkomaksujen määrä | Kun annat luotavien ennakkomaksujen määrän, järjestelmä luo luvun tähän kenttään käyttämällä aloituspäivää ja tiheyttä. | Kun tämä kenttä päivitetään manuaalisesti, järjestelmä ohittaa **Ennakkomaksuaikataulun loppu** -kentän arvo ja luo sen sijaan tietyn määrän ennakkomaksuja tai ennakoita. |
| Laskutustiheys | Sovelluksen ennakkomaksujen ja ennakoiden luontitiheys. | Tämä arvo vaikuttaa suoraan ennakkomaksujen ja ennakoiden määrään sekä luotuihin päivämääriin. |
| Loppusumma | Kokonaissumma on summa, joka jaetaan luotaviin yksittäisiin ennakkomaksuihin tai ennakoiden maksuihin. | Tämä kenttä ei vaikuta loppupään prosessiin. |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]