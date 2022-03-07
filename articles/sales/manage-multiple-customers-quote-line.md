---
title: Useiden asiakkaiden hallinta projektipohjaisilla tarjousriveillä
description: Tässä aiheessa on tietoja siitä, miten projektipohjaisilla tarjousriveillä hallitaan useita asiakkaita.
author: rumant
ms.date: 10/06/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: bf3d10cc4a742f7247586d09f5b209cbfdbbd790bdf97e09da06d9db583e61a5
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/06/2021
ms.locfileid: "6992022"
---
# <a name="manage-multiple-customers-on-project-based-quote-lines"></a>Useiden asiakkaiden hallinta projektipohjaisilla tarjousriveillä

_**Käytetään:** Project Operationsin resursseihin ja ei-varastoitaviin perustuvissa skenaarioissa_

Projektipohjaiset tarjousrivit tukevat skenaarioita, joissa kullakin tarjousrivillä on luettelo asiakkaista, jotka maksavat sen. Tämä projektipohjaisen tarjousrivin asiakasluettelo voi olla sama kuin tarjouksen asiakkaiden luettelo. Voit myös muuttaa asiakasluettelon toiseksi. Jos haluat luoda lopullisen projektisopimuksen, kun projektitarjous on voitettu, projektipohjaisen tarjousrivin asiakasluettelo kopioidaan vastaavaan projektipohjaiseen sopimusriviin. Projektipohjaisen tarjouksen asiakkaat kopioidaan projektisopimukseen.

Kun laskutat lopullista projektisopimusta, projektipohjaisen sopimusrivin asiakasluettelo on etusijalla projektisopimuksessa olevaan luetteloon nähden. Projektisopimuksen asiakasluetteloa käytetään vain uusien projektisopimusrivien oletusarvona.

Kaikki tarjouksen asiakkaat projektitarjouksen **Asiakkaat**-välilehdessä ovat projektitarjouksen rivin oletusarvona projektitarjousta varten luoduille uusille projektipohjaisille tarjousriveille. Aiemmin luodut projektipohjaiset tarjousrivit eivät peri uusia tarjouksen asiakastietueita, jotka on luotu niiden jälkeen.

## <a name="create-update-or-delete-a-quote-line-customer-record"></a>Tarjousrivin asiakastietueen luominen, päivittäminen tai poistaminen

Voit luoda, päivittää tai poistaa tarjousrivin asiakkaan **Tarjousrivin asiakkaat**-välilehdessä, joka on **Projektipohjainen tarjousrivi** -sivulla. Kun lisäät uuden asiakkaan projektipohjaiseen tarjousriviin, asiakas lisätään myös kokonaistarjoukseen tarjouksen asiakkaana siten, että sen ja laskutuksen jaon oletusprosenttiosuus kokonaistarjouksesta on 0 %. Kokonaistarjouksen laskutuksen jaon prosentti kopioidaan uusille tarjousriveille sekä lopulliseen projektisopimukseen. Laskutettaessa sopimuksesta käytetään kuitenkin laskutuksen jakoprosenttia tarjousrivitasolla, ei laskutuksen jakoprosenttia kokonaissopimustasolla. 

Seuraavassa taulukossa näkyy projektipohjaisen tarjousrivin Tarjousrivin asiakas -tietueen kentät.

| Field | Sijainti | Kuvaukset ja opastus | Loppupään vaikutus |
| --- | --- | --- | --- |
| **Asiakas** | **Tarjousrivin asiakkaat** -välilehden muokattava ruudukko sekä tarjousrivin asiakkaan päälomake ja pikaluontilomake. | Luettelee kaikki aktiiviset asiakkuudet. Tämä kenttä lukitaan sen jälkeen, kun tietue on luotu. Jos kenttää on päivitettävä, poista tietue ja luo se uudelleen. Jos olet tallentanut toteutuneita arvoja et voi poistaa tietuetta. | Kun valitset lisättävän asiakkuuden asiakkuuksien pääluettelosta, tarjousrivin asiakas lisätään myös tarjouksen asiakkaaksi. Tarjousrivin asiakkaat kopioidaan projektisopimusrivin asiakkaisiin, kun tarjous on voitettu. |
| **Laskutuksen jakoprosentti** | **Tarjousrivin asiakkaat** -välilehden muokattava ruudukko sekä tarjousrivin asiakkaan päälomake ja pikaluontilomake. | Ilmaisee kunkin laskuttamaton myyntitapahtuman prosenttiosuuden, joka kohdistetaan tähän tarjousrivin asiakkaaseen. | Kopioidaan projektisopimusrivin asiakkaisiin. |
| **Ei-ylitettävä rajoitus** | **Tarjousrivin asiakkaat** -välilehden muokattava ruudukko sekä tarjousrivin asiakkaan päälomake ja pikaluontilomake. | Osoittaa, onko neuvoteltu kyseiselle asiakkaalle laskutettavaan kokonaissummaan neuvoteltu rajoitus tai yläraja tälle tarjotulle riville. | Kopioidaan projektisopimusrivin asiakkaisiin, kun tarjous on voitettu. |
| **Omistava yritys** | **Tarjousrivin asiakkaat** -välilehden muokattava ruudukko sekä tarjousrivin asiakkaan päälomake ja pikaluontilomake. | Oikeushenkilö, joss tämä asiakas on määritetty **Projektinhallinta ja kirjanpito** -moduulissa. Tämä kenttä on vain luku -tilassa ja se määritetään itse tarjouksen omistavalle yritykselle. **Asiakkuus**-kenttään lisättävä asiakasluettelo on jo suodatettu omistavan yrityksen luetteloon Project Operationsin **Projektinhallinta ja kirjanpito** -moduulissa. | Omistava yritys vastaa oikeushenkilön käsitettä. Kaikki tästä projektista kertyvät kustannukset ja tuotot kirjataan omistavan yrityksen kirjanpitoon. |
| **Onko pyöristetty** | **Tarjousrivin asiakkaat** -välilehden muokattava ruudukko sekä tarjousrivin asiakkaan päälomake ja pikaluontilomake. | Ilmaisee, onko tämä asiakas tämän projektipohjaisen tarjousrivin oletuspyöristysasiakas. | Kopioidaan projektisopimuksen asiakkaisiin, kun tarjous on voitettu. |

## <a name="edit-billing-split-percentages"></a>Laskutuksen jakoprosenttien muokkaaminen

Voit muokata laskutuksen jakoprosentteja suoraan rivillä. Kun laskutuksen jakoprosentit eivät ole yhteensä 100 %, virhe tapahtuu. Kun olet muonkannut laskutuksen jakamisprosentit, voit poistaa virheen päivittämällä tarjousrivin sivun.

Käytä tasaisen jaon toimintoa tarjousrivin asiakkaiden aliruudukossa, jotta voit kohdistaa laskutuksen jaot kaikille tarjousrivin asiakkaille. Jos pyöristyskerroin on, se lisätään pyöristysasiakkaaseen. Yksi tarjousrivin asiakkaista merkitään aina pyöristysasiakkaaksi, jolloin tarjousrivin asiakastietueen pyöristysmerkinnän arvoksi on asetettu **Kyllä**. 


[!INCLUDE[footer-include](../includes/footer-banner.md)]