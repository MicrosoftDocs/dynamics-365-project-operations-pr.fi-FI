---
title: Korjatut laskut
description: Tässä aiheessa on tietoja korjatuista laskuista.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: e14da1c07d5b697de6caf1b9041c30581ecff102
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/28/2020
ms.locfileid: "3898077"
---
# <a name="corrected-invoices"></a>Korjatut laskut

_**Koskee:** Project Operationsin resurssiin / muuhun kuin resurssiin perustuvia skenaarioita, Lite-käyttöönotto-kaupasta proformalaskutukseen_

Vahvistettuja laskuja voidaan muokata. Kun muokkaat vahvistettua laskua, korjatusta laskusta luodaan luonnos. Koska oletuksena on, että haluat kumota kaikki alkuperäisen laskun tapahtumat ja määrät, tämä korjattu lasku sisältää kaikki alkuperäisen laskun tapahtumat ja kaikki siinä olevat määrät ovat nollia (0).

Jos jotkin tapahtumat eivät vaadi korjausta, voit poistaa ne korjaavasta laskuluonnoksesta. Jos haluat kumota tai palauttaa vain osamäärän, voit muokata rivin tietojen Määrä-kenttää. Voit tarkastella alkuperäisen laskun määrää avaamalla laskurivin tiedot. Tämän jälkeen voit muokata nykyisen laskun määrää siten, että se ylittää tai alittaa alkuperäisen laskun määrän.

Kun vahvistat korjaavan laskun, alkuperäinen laskutetun myynnin todellinen arvo kumotaan ja uusi laskutetun myynnin todellinen arvo luodaan. Jos määrää vähennettiin, ero aiheuttaa myös uuden laskuttamattoman myynnin todellisen arvon luomiseen. Jos alkuperäinen laskutettu myynti esimerkiksi oli kahdeksan tuntia ja korjattujen laskurivien tietojen määrä on vain kuusi tuntia, alkuperäisen laskutetun myynnin rivi peruutetaan ja seuraavat kaksi uutta todellista arvoa luodaan:

- Laskutetun myynnin todellisen arvon kuudelle tunnille.
- Laskuttamattoman myynnin todellisen arvon kahdelle jäljelle jääneelle tunnille. Tämä tapahtuma voidaan joko laskuttaa myöhemmin tai merkitä ei-veloitettavaksi riippuen siitä, mitä asiakkaan kanssa sovitaan.
