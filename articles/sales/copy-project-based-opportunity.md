---
title: Projektimahdollisuuksien kopiointi
description: Tässä artikkelissa on tietoja Project Operationsin projektipohjaisten mahdollisuuksien kopioimisesta.
author: rumant
ms.date: 10/09/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 0fe29918e14a944de7277639f752ad53513a7589
ms.sourcegitcommit: e0cbbe7c6f03d4978134405cf04bd8bc1d019f65
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/05/2022
ms.locfileid: "9826124"
---
# <a name="copy-project-opportunities"></a>Projektimahdollisuuksien kopiointi

_**Koskee:** Project Operationsin resurssiin / muuhun kuin resurssiin perustuvia skenaarioita, Lite-käyttöönotto-kaupasta proformalaskutukseen_


Projektimahdollisuudet voidaan helposti kopioida uusien projektimahdollisuuksien luomiseksi. 

1. Siirry **Projektimahdollisuudet**-luettelosivulle ja valitse mahdollisuus luettelosta. Voit myös avata tietyn mahdollisuuden tiedot-sivun. 
2. Valitse jommallakummalla sivulla **Kopioi**. Näkyviin tulee dialogisivu, joka sisältää seuraavat kenttätiedot. Kopiointiprosessi voi muuttua tässä dialogissa valittujen arvojen mukaan.

    | **Kenttä** | **Kuvaus** | **Loppupään vaikutus** |
    | --- | --- | --- |
    | Aihe | Kirjoita kohdemahdollisuuden asiaankuuluva aihe. Kun valintaikkuna avautuu, järjestelmä määrittää arvoksi sen lähdemahdollisuuden aiheen, johon lisätty teksti **kopio**. | Tämä kenttä ei vaikuta loppupään prosessiin. |
    | Tili | Viittaa asiakkaan yritykseen tai asiakastietueeseen. Kun valintaikkuna avautuu, järjestelmä määrittää arvoksi lähdemahdollisuuden tilin. | Tämä kenttä on mahdollisuuden ensisijainen asiakas. |
    | Sopimusyksikkö | Tähän sopimukseen liittyvien projektien toimituksesta vastuussa oleva organisaatioyksikkö. Kun valintaikkuna avautuu, järjestelmä määrittää arvoksi lähdemahdollisuuden sopimusyksikön. | Sopimusyksikkö on sen yrityksen osasto, joka suorittaa projektit, kun sopimus on tehty. Jokaisella sopimusyksiköllä on valuutta, ja tätä valuuttaa käytetään projektin aikana arvioitujen ja todellisten kustannusten raportoimiseen. |
    | Valuutta | Valuutta, jota sovelletaan sopimuksen tapahtumiin. Kun valintasivu avautuu, järjestelmä määrittää arvoksi lähdemahdollisuuden valuutan. | Valuuttaa käytetään hinnastojen oletusarvon ja talousarvioiden muodostamiseen tarjouksessa. Valuuttaa käytetään lopulta laskutettaessa asiakasta, kun kauppa on voitettu. |
    | Kopioi hinnoittelu | Kyllä/ei-arvo, joka osoittaa, kopioidaanko mahdollisuuden hinnoittelu lähdemahdollisuudesta. | Jos **Kyllä** on valittuna, hinnastot kopioidaan lähteestä kohdemahdollisuuteen. Jos **Ei** on valittu, oletushinnastot määritetään perustuen uusimpiin hinnastoihin. |

3. Valitse **OK**. Järjestelmä luo projektimahdollisuudesta kopion valittujen parametrien perusteella, ja uusi projektimahdollisuus avataan.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
