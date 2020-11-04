---
title: Projektiin perustuvien mahdollisuuksien kopioiminen
description: Tämä aihe tarjoaa tietoja Project Operationsin projektipohjaisten mahdollisuuksien kopioimisesta.
author: rumant
manager: Annbe
ms.date: 10/09/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 89f5a63581f36b30634bdd302a6d360d6b5e75bd
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/16/2020
ms.locfileid: "4075287"
---
# <a name="copy-project-based-opportunities"></a>Projektiin perustuvien mahdollisuuksien kopioiminen

_**Käytetään:** Project Operationsin resursseihin ja ei-varastoitaviin perustuvissa skenaarioissa_


Projektimahdollisuudet voidaan helposti kopioida uusien projektimahdollisuuksien luomiseksi. 

1. Siirry **Projektimahdollisuudet** -luettelosivulle ja valitse mahdollisuus luettelosta. Voit myös avata tietyn mahdollisuuden tiedot-sivun. 
2. Valitse jommallakummalla sivulla **Kopioi**. Näkyviin tulee dialogisivu, joka sisältää seuraavat kenttätiedot. Kopiointiprosessi voi muuttua tässä dialogissa valittujen arvojen mukaan.

    | **Kenttä** | **Relevanssi, tarkoitus ja opastus** | **Loppupään vaikutus** |
    | --- | --- | --- |
    | Aihe | Kirjoita kohdemahdollisuuden asiaankuuluva aihe. Kun valintaikkuna avautuu, järjestelmä määrittää arvoksi sen lähdemahdollisuuden aiheen, johon lisätty teksti **kopio**. | Tämä kenttä ei vaikuta loppupään prosessiin. |
    | Tili | Viittaa asiakkaan yritykseen tai asiakastietueeseen. Kun valintaikkuna avautuu, järjestelmä määrittää arvoksi lähdemahdollisuuden tilin. | Tämä kenttä on mahdollisuuden ensisijainen asiakas. |
    | Sopimusyksikkö | Tähän sopimukseen liittyvien projektien toimituksesta vastuussa oleva organisaatioyksikkö. Kun valintaikkuna avautuu, järjestelmä määrittää arvoksi lähdemahdollisuuden sopimusyksikön. | Sopimusyksikkö on sen yrityksen osasto, joka suorittaa projektit, kun sopimus on tehty. Jokaisella sopimusyksiköllä on valuutta, ja tätä valuuttaa käytetään projektin aikana arvioitujen ja todellisten kustannusten raportoimiseen. |
    | Valuutta | Valuutta, jota sovelletaan sopimuksen tapahtumiin. Kun valintasivu avautuu, järjestelmä määrittää arvoksi lähdemahdollisuuden valuutan. | Valuuttaa käytetään hinnastojen oletusarvon ja talousarvioiden muodostamiseen tarjouksessa. Valuuttaa käytetään lopulta laskutettaessa asiakasta, kun kauppa on voitettu. |
    | Kopioi hinnoittelu | Kyllä/ei-arvo, joka osoittaa, kopioidaanko mahdollisuuden hinnoittelu lähdemahdollisuudesta. | Jos **Kyllä** on valittuna, hinnastot kopioidaan lähteestä kohdemahdollisuuteen. Jos **Ei** on valittu, oletushinnastot määritetään perustuen uusimpiin hinnastoihin. |

3. Valitse **OK**. Järjestelmä luo projektimahdollisuudesta kopion valittujen parametrien perusteella, ja uusi projektimahdollisuus avataan.
