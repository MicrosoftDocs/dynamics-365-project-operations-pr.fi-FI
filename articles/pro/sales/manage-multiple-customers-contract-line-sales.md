---
title: Useiden asiakkaiden hallinta projektipohjaisilla sopimusriveillä – lite
description: Tässä aiheessa on tietoja useiden asiakkaiden hallinnasta projektipohjaisilla sopimusriveillä.
author: rumant
ms.date: 10/27/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: a7e29b1a92a5fefcf4812931383d03e5f81a27001f0e6525bb4eeb8dc93b18b9
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/06/2021
ms.locfileid: "7001787"
---
# <a name="manage-multiple-customers-on-project-based-contract-lines---lite"></a>Useiden asiakkaiden hallinta projektipohjaisilla sopimusriveillä – lite

_**Käytetään:** Lite-käyttöönotto – kauppa proformalaskutukseen_

Projektipohjaisilla sopimusriveillä voi olla luettelo asiakkaista, jotka vastaavat maksusta. Projektipohjaisen sopimusrivin asiakasluettelo voi olla sama kuin palvelusopimuksessa oleva asiakasluettelo, mutta se ei ole välttämätöntä. Kun projektitarjous voitetaan ja projektisopimus luodaan, tarjousrivin asiakasluettelo kopioidaan vastaavalle sopimusriville. Tarjouksen asiakkaat kopioidaan palvelusopimukseen.

Kun projektisopimusta laskutetaan, projektipohjaisen asiakasrivin asiakasluettelo priorisoidaan sopimuksen asiakasluettelon ohitse. Projektisopimuksen asiakasluetteloa käytetään vain uusien sopimusrivien oletuksena.

Kaikki projektisopimuksen **Asiakkaat**-välilehden asiakkaat ovat oletusarvoisesti sopimusrivin asiakkaita projektisopimukselle luoduilla uusilla sopimusriveillä. Mahdolliset aiemmin luodut sopimusrivit eivät peri niiden mukaan luotuja uusien sopimusasiakkaiden tietueita.

## <a name="create-update-or-delete-a-contract-line-customer-record"></a>Sopimusrivin asiakastietueen luominen, päivittäminen tai poistaminen

Voit luoda, päivittää tai poistaa sopimusrivin asiakkaan Projektipohjainen sopimusrivi -sivun Sopimusrivin asiakkaat -välilehdessä. Kun uusi asiakas lisätään projektipohjaiselle sopimusriville, se lisätään myös itse sopimukseen sopimusasiakkaana, jonka laskutuksen oletusjakoprosentti on nolla. Koko sopimuksen laskutuksen jakoprosentti kopioidaan uusille sopimusriveille ja lopulta myös projektisopimukseen. Kun laskutus kuitenkin tehdään sopimuksesta, käytössä on sopimusrivitason laskutuksen jakoprosentti eikä koko sopimustasoon laskutuksen jakoprosentti.

Seuraavat projektipohjaisen sopimusrivin **Sopimus**-rivin asiakastietueen kentät kannattaa muistaa käytön aikana:

| Field | Sijainti | Kuvaus | Loppupään vaikutus |
| --- | --- | --- | --- |
| **Asiakas** | **Sopimuksen asiakkaat** -välilehden sekä sopimuksen asiakkaan **Pää**- ja **Pikaluonti**-lomakkeiden muokattava ruudukko. | Kaikki aktiiviset tilit. Tämä kenttä lukitaan sen jälkeen, kun tietue on luotu. Kentän voi päivittää poistamalla tietueen ja luomalla uuden tietueen. Jos todellisia arvoja on jo kirjattu, tietuetta ei voi poistaa. Kyseisen tilin laskutuksen jakoprosentin voi kuitenkin merkitä nollaksi. Kun tietueen arvoksi on merkitty nolla, sillä on vaikutusta mahdollisiin tuleviin kyseiselle asiakkaalle määritettyihin tai jaettuihin todellisiin kustannuksiin tai tuloihin. | Kun tili valitaan tilien pääluettelossa lisättäväksi tai tallennettavaksi, myös sopimusrivin asiakas lisätään sopimuksen asiakkaana. Sopimusrivin asiakkaita käytetään, kun laskuja luodaan. |
| **Laskutuksen jakoprosentti** | **Sopimuksen asiakkaat** -välilehden sekä sopimuksen asiakkaan **Pää**- ja **Pikaluonti**-lomakkeiden muokattava ruudukko. | Tämä kenttä ilmaisee kunkin tälle sopimusrivin asiakkaalle määritetyn laskuttamattoman myyntitapahtuman prosentin. | Sopimusrivin asiakkaita ja laskutuksen jakoprosentteja käytetään, kun todelliset arvot luodaan hyväksynnän jälkeen ja kun lasku luodaan. |
| **Ei-ylitettävä rajoitus** | **Sopimuksen asiakkaat** -välilehden sekä sopimuksen asiakkaan **Pää**- ja **Pikaluonti**-lomakkeiden muokattava ruudukko. | Ilmaisee, jos sopimusrivin asiakkaan laskutuksen kokonaissummassa on neuvoteltu raja tai yläraja. | Sopimusrivin asiakkaan ei-ylitettävää rajoitusta käytetään, kun todelliset arvot ja laskut luodaan. |
| **Onko pyöristetty** | **Sopimuksen asiakkaat** -välilehden sekä sopimusrivin asiakkaan **Pää**- ja **Pikaluonti**-lomakkeiden muokattava ruudukko. | Tämä kenttä ilmaisee, onko asiakas tämän projektipohjaisen sopimusrivin oletusarvoinen pyöristysasiakas. | Kun luot laskutuksen jakoprosentin mukaisen todellisen arvon, pyöristyseroja voi esiintyä. Siinä tapauksessa pyöristyserot määritetään asiakkaalle. |

## <a name="edit-billing-split-percentages"></a>Laskutuksen jakoprosenttien muokkaaminen

Laskutuksen jakoprosenttia voidaan muokata ruudukossa. Jos laskutuksen jakoprosenttien yhteissumma ei ole 100 prosentti, seurauksena on virhe. Kun laskutuksen jakoprosentteja on muokattu, poista virhe päivittämällä sivu.

Voit kokeilla myös **Jaa tasaisesti** -vaihtoehdon valintaa sopimusrivin asiakkaan aliruudukossa. Tämä toiminto jakaa laskutuksen jaot tasaisesti kaikille sopimusrivin asiakkaille. Mahdollinen pyöristyskerron lisätään pyöristysasiakkaaseen. Yksi sopimusrivin asiakas merkitään aina **Pyöristys**-asiakkaaksi määrittämällä **Pyöristys**-merkinnän arvoksi **Kyllä**.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]