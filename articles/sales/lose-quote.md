---
title: Projektipohjaisten tarjousten kopiointi
description: Tämä aihe tarjoaa tietoja Project Operationsin projektitpohjaisten tarjousten kopioimisesta.
author: rumant
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 4e9009391d33c5dd5988ae65e13ca1ca1ec398bc
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/10/2021
ms.locfileid: "5999082"
---
# <a name="copy-project-based-quotes"></a>Projektipohjaisten tarjousten kopiointi

_**Koskee:** Project Operationsin resurssiin / muuhun kuin resurssiin perustuvia skenaarioita, Lite-käyttöönotto-kaupasta proformalaskutukseen_

Voit helposti luoda uuden projektitarjouksen kopioimalla aiemmin luodun tarjouksen. 

- Jos haluat kopioida projektitarjouksen valitsemalla **Projektitarjoukset**-luettelosivulla tai **Projektitarjous**-tietosivulla kopioitava projektitarjous ja valitse sitten **Kopioi**.

Tämä avaa valintaikkunasivun, johon voit kirjoittaa kopion parametrit. Seuraavassa taulukossa on luettelo valintaikkunasivun kentistä. Kopiointiprosessi voi muuttua valittujen arvojen mukaan.

| **Kenttä** | **Kuvaus** | **Loppupään vaikutus** |
| --- | --- | --- |
| Aihe | Kirjoita kohdetarjouksen asiaankuuluva aihe tai nimi. Kun valintaikkuna avautuu, järjestelmä määrittää arvoksi sen lähdetarjouksen aiheen, johon lisätty teksti **kopio**. | |
| Mahdollinen asiakas | Viittaus asiakkaan yritykseen tai asiakastietueeseen. Kun valintaikkuna avautuu, järjestelmä määrittää arvoksi lähdetarjouksen tilin. | Tämä kenttä on tarjouksen ensisijainen asiakas. |
| Sopimusyksikkö | Organisaatioyksikkö, joka on vastuussa tähän sopimukseen liittyvien projektien toimituksesta.
Kun valintaikkuna avautuu, järjestelmä määrittää arvoksi lähdetarjouksen sopimusyksikön. | Sopimusyksikkö on sen yrityksen osasto, joka suorittaa projektit, kun sopimus on tehty. Jokaisella sopimusyksiköllä on valuutta. Tätä valuuttaa käytetään projektin toteutuksen aikana arvioitujen ja todellisten kustannusten raportoimiseen. |
| Valuutta | Tämä on se valuutta, jota sovelletaan sopimuksen tapahtumiin. Kun valintaikkuna avautuu, järjestelmä määrittää arvoksi lähdetarjouksen valuutan. Tätä voidaan muokata, ja jos se on muuttunut, **Kopioi hinnoittelu**-kentän arvo on aina **Ei**. Syynä tähän on se, että lähdetarjouksen hinnastot eivät ole enää voimassa. | Valuuttaa käytetään oletushinnaston määrittämiseen, tarjouksen kustannusarvion rakentamiseen ja lopuksi asiakkaan laskutukseen, kun kauppa on voitettu. |
| Pyydetty toimituspäivä | Tämä on asiakkaan pyytämä toimituspäivä. | Tätä käytetään päättymispäivänä luotaessa laskutuspäivämääriä tietyllä tiheydellä. |
| Kopioi hinnoittelu | Kyllä/Ei-arvo osoittaa, kopioidaanko tarjouksen hinnoittelu lähdetarjouksesta. | Jos **Kyllä** on valittuna, projektihinnasto- ja tuotehinnnastoviittaukset kopioidaan lähdetarjouksesta kohdetarjoukseen. Jos on valittu **Ei**, oletushinnastoiksi määritetään perustuen uusimpiin hinnastoihin, jotka on määritetty asiakas- tai projektiparametreissa. |

Kun valitset dialogisivulla **OK**, järjestelmä luo projektitarjouksesta kopion, joka perustuu dialogissa valittuihin parametreihin. Uusi projektitarjous avautuu. 

> [!NOTE]
> Seuraavia tietoja ei kopioida lähdetarjouksesta kohdetarjoukseen:
>
> - Laskutusaikataulut
> - Tarjouksen ja tarjousrivin asiakkaat
> - Projektiviittaus projektipohjaisilla tarjousriveillä – asiakasbudjetin tiedot
>
>Koska nämä tiedot ovat hyvin tarjouskohtaisia, näitä kenttiä ja tietueita ei kopioida. Projektien ja tuotteiden tarjousrivit, tarjousrivien tietojen arviot ja tarjoustason ei-ylitettävät arvot kopioidaan. Hinta- ja kustannushintaoletukset määräytyvät **Kopioi parametrit** -valintaikkunassa valitun **Kopioi hinnoittelu** -asetuksen mukaan.


[!INCLUDE[footer-include](../includes/footer-banner.md)]