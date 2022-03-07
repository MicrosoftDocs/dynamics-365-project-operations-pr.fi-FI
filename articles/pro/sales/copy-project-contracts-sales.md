---
title: Projektin palvelusopimusten kopiointi – lite
description: Tässä aiheessa on tietoja projektien kopioinnista projektisopimuksista Project Operationsissa.
author: rumant
ms.date: 10/07/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: d5c45c6f1631d9e20bd0416410c7fe24a11623da425c8e2a633b085fbfabdd79
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/06/2021
ms.locfileid: "7006017"
---
# <a name="copy-project-contracts---lite"></a>Projektin palvelusopimusten kopiointi – lite

_**Käytetään:** Lite-käyttöönotto – kauppa proformalaskutukseen_

Voit helposti luoda uusia projektisopimuksia tekemällä kopioita aiemmin luoduista palvelusopimuksista kahdella tavalla: 

  - Valitse projektisopimus **Projektisopimukset**-luettelosivulla ja valitse sitten **Kopioi**.
  - Valitse **Projektisopimuksen** tiedot-sivulla **Kopioi**.

Näyttöön avautuu valintaikkuna, josta voit valita kopioidun sopimuksen parametrit. Seuraavat kentät sisältyvät valintaikkunaan. Kopiointiprosessi voi muuttua tässä dialogissa valitsemiesi arvojen mukaan.

| **Kenttä** | **Kuvaus** | **Loppupään vaikutus** |
| --- | --- | --- |
| Aihe | Kirjoita kohdesopimuksen aihe. Kun valintaikkunasivu avautuu, järjestelmä määrittää tämän kentän arvoksi sen lähdesopimuksen nimen, johon lisätty teksti **kopio**. | Tämä kenttä ei vaikuta loppupään prosessiin. |
| Asiakas | Viittaus asiakkaan yritykseen tai asiakastietueeseen. Kun valintaikkuna avautuu, järjestelmä määrittää tämän kentän arvoksi lähdesopimuksen tilin. | Tämä kenttä on sopimuksen ensisijainen asiakas. |
| Sopimusyksikkö | Organisaatioyksikkö, joka on vastuussa tähän sopimukseen liittyvien projektien toimituksesta. Kun valintaikkunasivu avautuu, järjestelmä määrittää arvoksi lähdesopimuksen sopimusyksikön. | Sopimusyksikkö on sen yrityksen osasto, joka suorittaa projektit, kun sopimus on tehty. Jokaisella sopimusyksiköllä on valuutta. Tätä valuuttaa käytetään projektin aikana arvioitujen ja todellisten kustannusten raportoimiseen. |
| Valuutta | Valuutta, jota sovelletaan sopimuksen tapahtumiin. Kun valintaikkuna avautuu, järjestelmä asettaa kentän lähdesopimuksen valuutaksi. Valuuttaa ei voi muuttaa. Jos näin on, **kopiohinnoittelu**-kentän arvo on aina **Ei**, koska lähdesopimuksen hinnastot eivät ole enää merkityksellisiä. | Valuuttaa käytetään oletushinnastojen määrittämiseen, tarjouksen kustannusarvioiden rakentamiseen ja lopuksi asiakkaan laskutukseen, kun kauppa on voitettu. |
| Pyydetty toimituspäivä | Syötä asiakkaan pyytämän toimituksen päivämäärä. | Tätä päivämäärää käytetään päättymispäivänä, kun luot laskutuspäivämääriä tietyllä tiheydellä. |
| Kopioi hinnoittelu | Osoittaa, kopioidaanko sopimuksen hinnoittelu lähdesopimuksesta. | Jos kentän arvoksi on asetettu **Kyllä**, projektihinnasto- ja tuotehinnastoviittaukset kopioidaan lähdesopimuksesta kohdesopimukseen. Jos on valittu **Ei**, hinnastot perustuvat oletuksena tilin tai projektin parametrien viimeisimpiin hinnastoihin. |

Kun valitset dialogisivulla **OK**, järjestelmä luo sopimuksesta kopion, joka perustuu valittuihin parametreihin. Uusi palvelusopimus avautuu.

Seuraavia tietoja ei kopioida **lähdetarjouksesta** **kohdetarjoukseen**:

  - Laskutusaikataulut
  - Sopimus ja sopimusrivin asiakkaat
  - Projektipohjaisten sopimusrivien projektiviittaus
  - Asiakkaan budjettitiedot

Koska nämä tiedot ovat sopimuskohtaisia, näitä kenttiä ja tietueita ei kopioida. Projektien ja tuotteiden sopimusrivit, sopimusrivien tietojen arviot ja sopimustason ei-ylitettävät arvot kopioidaan. Hinta- ja kustannushintaoletukset määräytyvät valinnoista **Kopioi parametrit** -kentässä valitun **Kopioi parametrit** -asetuksen mukaan.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]