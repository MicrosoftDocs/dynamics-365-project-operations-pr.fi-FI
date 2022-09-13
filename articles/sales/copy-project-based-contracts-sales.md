---
title: Projektipohjaisten sopimusten kopioiminen
description: Tässä artikkelissa on tietoja projektisopimusten kopioinnista Microsoft Dynamics 365 Project Operationsissa.
author: rumant
ms.date: 09/01/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 21994ef6d8f6e6cdf321599d107cc80368c96ecc
ms.sourcegitcommit: 16c9eded66d60d4c654872ff5a0267cccae9ef0e
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/07/2022
ms.locfileid: "9410319"
---
# <a name="copy-project-based-contracts"></a>Projektipohjaisten sopimusten kopioiminen

_**Käytetään:** Project Operationsin resursseihin ja ei-varastoitaviin perustuvissa skenaarioissa_

Voit helposti luoda uusia projektisopimuksia tekemällä kopioita aiemmin luoduista palvelusopimuksista kahdella tavalla:

- Valitse projektisopimus **Projektisopimukset**-luettelosivulla ja valitse sitten **Kopioi**.
- Valitse **Projektisopimuksen** tiedot-sivulla **Kopioi**.

Molemmissa tapauksissa näyttöön avautuu ruutu, jossa voit määrittää kopioidun sopimuksen parametrit. Seuraavat kentät sisältyvät valintaikkunaan. Kopiointiprosessi voi muuttua valittujen arvojen mukaan.

| Field | Description | Loppupään vaikutus |
| --- | --- | --- |
| Aihe | Kirjoita kohdesopimuksen aihe. Kun valintaikkunaruutu avautuu, järjestelmä määrittää kentän arvoksi lähdesopimuksen nimen, johon lisätty teksti "kopio". | Tämä kenttä ei vaikuta loppupään prosessiin. |
| asiakas | Viittaus asiakkaan yritykseen tai asiakastietueeseen. Kun valintaikkunaruutu avautuu, järjestelmä määrittää kentän arvoksi lähdesopimuksen asiakastilin. | Tämä kenttä on sopimuksen ensisijainen asiakas. |
| Omistava yritys | Yritys, joka on vastuussa tähän sopimukseen liittyvien projektien toimituksesta. Kun valintaikkunaruutu avautuu, järjestelmä määrittää kentän arvoksi lähdesopimuksen omistavan yrityksen. | Omistava yritys on juridinen entiteetti, joka toteuttaa projektin sen jälkeen, kun sopimus on suljettu. Omistavan yrityksen valuutta on oltava sama kuin sopimusyksikön valuutta. |
| Sopimusyksikkö | Organisaatioyksikkö, joka on vastuussa tähän sopimukseen liittyvien projektien toimituksesta. Kun valintaikkunaruutu avautuu, järjestelmä määrittää kentän arvoksi lähdesopimuksen sopimusyksikön. | Sopimusyksikkö on sen yrityksen osasto, joka suorittaa projektit, kun sopimus on tehty. Jokaisella sopimusyksiköllä on valuutta. Tätä valuuttaa käytetään projektin aikana arvioitujen ja todellisten kustannusten raportoimiseen. |
| Valuutta | Valuutta, jota sovelletaan sopimuksen tapahtumiin. Kun valintaikkunaruutu avautuu, järjestelmä asettaa kentän lähdesopimuksen valuutaksi. Valuuttaa ei voi muuttaa. Jos näin on, **Kopioi hinnoittelu**-kentän arvo on aina **Ei**, koska lähdesopimuksen hinnastot eivät ole enää merkityksellisiä. | Valuuttaa käytetään oletushinnastojen määrittämiseen, tarjouksen kustannusarvioiden luomiseen ja lopuksi asiakkaan laskutukseen, kun kauppa on voitettu. |
| Pyydetty toimituspäivä | Syötä asiakkaan pyytämän toimituksen päivämäärä. | Tätä päivämäärää käytetään päättymispäivänä, kun luot laskutuspäivämääriä tietyllä tiheydellä. |
| Kopioi hinnoittelu | Arvo, joka osoittaa, kopioidaanko sopimuksen hinnoittelu lähdesopimuksesta. | Jos kentän arvoksi on asetettu **Kyllä**, projektihinnasto- ja tuotehinnastoviittaukset kopioidaan lähdesopimuksesta kohdesopimukseen. Jos on valittu **Ei**, oletushinnastoja käytetään tilin tai projektin parametrien viimeisimpiin hinnastoihin perustuen. |

Kun valitset dialogiruudulla **OK**, järjestelmä luo sopimuksesta kopion, joka perustuu määrittämiisi parametriarvoihin. SItten uusi palvelusopimus avautuu.

Seuraavia tietoja **ei** kopioida lähdesopimuksesta kohdesopimukseen, koska ne liittyvät kuhunkin palvelusopimukseen:

- Laskutusaikataulut
- Sopimus ja sopimusrivin asiakkaat
- Projektipohjaisten sopimusrivien projektiviittaus
- Asiakkaan budjettitiedot

Projektien ja tuotteiden sopimusrivit, sopimusrivien tietojen arviot ja sopimustason ei-ylitettävät arvot kopioidaan. Oletushintojen ja -kustannushintojen syöttäminen määräytyvät **Kopioi parametrit** -ruudussa valitun **Kopioi hinnoittelu** -kentän valinnan mukaan.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
