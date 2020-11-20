---
title: Ennakkomaksuaikataulun määrittäminen – lite
description: Tässä aiheessa on tietoja ennakkomaksuaikataulun määrittämisestä Project Operationsissa.
author: rumant
manager: Annbe
ms.date: 10/22/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 5e0312b89d9969f140146b6aaaa9bdcfde702c0b
ms.sourcegitcommit: f6f86e80dfef15a7b5f9174b55dddf410522f7c8
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/31/2020
ms.locfileid: "4181268"
---
# <a name="set-up-a-retainer-schedule---lite"></a>Ennakkomaksuaikataulun määrittäminen – lite

_**Käytetään:** Lite-käyttöönotto – kauppa proformalaskutukseen_

Ennakkomaksuaikataulut määritetään Dynamics 365 Project Operationsin **Projektisopimus**-sivulla.

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
