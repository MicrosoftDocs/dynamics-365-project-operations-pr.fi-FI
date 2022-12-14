---
title: Useiden asiakkaiden hallinta projektin tarjousriveillä
description: Tässä artikkelissa on tietoja useiden asiakkaiden hallinnasta projektipohjaisilla sopimusriveillä.
author: rumant
ms.date: 10/27/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: ec8457fd32a5c215bbc2056b02b2ab3527c4ab1f
ms.sourcegitcommit: e0cbbe7c6f03d4978134405cf04bd8bc1d019f65
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/05/2022
ms.locfileid: "9825936"
---
# <a name="manage-multiple-customers-on-project-contract-lines"></a>Useiden asiakkaiden hallinta projektin tarjousriveillä

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
