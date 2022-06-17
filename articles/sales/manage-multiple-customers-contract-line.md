---
title: Useiden asiakkaiden hallinta projektipohjaisilla sopimusriveillä
description: Tässä artikkelissa on tietoja sopimusrivien ja useita asiakkaita sisältävien sopimusten käyttämisestä.
author: rumant
ms.date: 10/22/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 0e0652d4b9cdb0489d4f191ef0f3b251e39262f5
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8914858"
---
# <a name="manage-multiple-customers-on-project-based-contract-lines"></a>Useiden asiakkaiden hallinta projektipohjaisilla sopimusriveillä

_**Koskee:** Project Operationsin resurssiin / muuhun kuin resurssiin perustuvia skenaarioita, Lite-käyttöönotto-kaupasta proformalaskutukseen_

Projektipohjaisilla sopimusriveillä voi olla luettelo asiakkaista, jotka vastaavat maksusta. Projektipohjaisen sopimusrivin asiakasluettelo voi olla sama kuin palvelusopimuksessa oleva asiakasluettelo, mutta se ei ole välttämätöntä. Kun projektitarjous voitetaan ja projektisopimus luodaan, tarjousrivin asiakasluettelo kopioidaan vastaavalle sopimusriville. Tarjouksen asiakkaat kopioidaan palvelusopimukseen.

Kun projektisopimusta laskutetaan, projektipohjaisen asiakasrivin asiakasluettelo priorisoidaan sopimuksen asiakasluettelon ohitse. Projektisopimuksen asiakasluetteloa käytetään vain uusien sopimusrivien oletuksena.

Kaikki projektisopimuksen **Asiakkaat**-välilehden asiakkaat ovat oletusarvoisesti sopimusrivin asiakkaita projektisopimukselle luoduilla uusilla sopimusriveillä. Mahdolliset aiemmin luodut sopimusrivit eivät peri niiden mukaan luotuja uusien sopimusasiakkaiden tietueita.

## <a name="create-update-or-delete-a-contract-line-customer-record"></a>Sopimusrivin asiakastietueen luominen, päivittäminen tai poistaminen

Voit luoda, päivittää tai poistaa sopimusrivin asiakkaan **Projektipohjainen sopimusrivi** -sivun **Sopimusrivin asiakkaat** -välilehdessä. Kun uusi asiakas lisätään projektipohjaiselle sopimusriville, se lisätään myös itse sopimukseen sopimusasiakkaana, jonka laskutuksen oletusjakoprosentti on nolla. Koko sopimuksen laskutuksen jakoprosentti kopioidaan uusille sopimusriveille ja lopulta myös projektisopimukseen. Kun laskutus kuitenkin tehdään sopimuksesta, käytössä on sopimusrivitason laskutuksen jakoprosentti eikä koko sopimustasoon laskutuksen jakoprosentti. 

Seuraavat projektipohjaisen sopimusrivin sopimusrivin asiakastietueen kentät kannattaa muistaa käytön aikana:

| Field | Sijainti | Kuvaus | Loppupään vaikutus |
| --- | --- | --- | --- |
| Tili | **Sopimusriviin asiakkaat** -välilehden sekä sopimusrivin asiakkaan pää- ja pikaluontilomakkeiden muokattava ruudukko | Kaikki aktiiviset tilit. Tämä kenttä lukitaan sen jälkeen, kun tietue on luotu. Kentän voi päivittää poistamalla tietueen ja luomalla uuden tietueen. Jos todellisia arvoja on jo kirjattu, tietuetta ei voi poistaa. Kyseisen tilin laskutuksen jakoprosentin voi kuitenkin merkitä nollaksi. Kun tietueen arvoksi on merkitty nolla, sillä on vaikutusta mahdollisiin tuleviin kyseiselle asiakkaalle määritettyihin tai jaettuihin todellisiin kustannuksiin tai tuloihin. | Kun tili valitaan tilien pääluettelossa lisättäväksi tai tallennettavaksi, myös sopimusrivin asiakas lisätään sopimuksen asiakkaana. Sopimusrivin asiakkaita käytetään, kun laskuja luodaan. |
| Laskutuksen jakoprosentti | **Sopimusriviin asiakkaat** -välilehden sekä sopimusrivin asiakkaan pää- ja pikaluontilomakkeiden muokattava ruudukko | Tämä kenttä ilmaisee kunkin tälle sopimusrivin asiakkaalle määritetyn laskuttamattoman myyntitapahtuman prosentin. | Sopimusrivin asiakkaita ja laskutuksen jakoprosentteja käytetään, kun todelliset arvot luodaan hyväksynnän jälkeen ja kun lasku luodaan. |
| Ei-ylitettävä rajoitus | **Sopimusriviin asiakkaat** -välilehden sekä sopimusrivin asiakkaan pää- ja pikaluontilomakkeiden muokattava ruudukko | Ilmaisee, jos sopimusrivin asiakkaan laskutuksen kokonaissummassa on neuvoteltu raja tai yläraja. | Sopimusrivin asiakkaan ei-ylitettävää rajoitusta käytetään, kun todelliset arvot ja laskut luodaan. |
| Omistava yritys | **Tarjousrivin asiakkaat** -välilehden sekä tarjousrivin asiakkaan pää- ja pikaluontilomakkeiden muokattava ruudukko | Yritys, jossa tämä asiakas on määritetty. Tämä kenttä on vain luku -muotoinen ja sen määrityksenä on tarjouksen omistava yritys. Asiakasluettelo lisätään **Tili**-kenttään, joka on suodatettu kyseisen omistavan yrityksen luetteloksi. | Omistavan yhtiön käsite vastaa yrityksen käsitettä. Kaikki tästä projektista kertyvät kustannukset ja tuotot kirjataan omistavalle yrityksen kirjanpitoon. |
| Onko pyöristetty | **Sopimusriviin asiakkaat** -välilehden sekä sopimusrivin asiakkaan pää- ja pikaluontilomakkeiden muokattava ruudukko | Tämä kenttä ilmaisee, onko asiakas tämän projektipohjaisen sopimusrivin oletusarvoinen pyöristysasiakas. | Kun luot laskutuksen jakoprosentin mukaisen todellisen arvon, pyöristyseroja voi esiintyä. Siinä tapauksessa pyöristyserot määritetään asiakkaalle. |

## <a name="edit-billing-split-percentages"></a>Laskutuksen jakoprosenttien muokkaaminen

Laskutuksen jakoprosenttia voidaan muokata ruudukossa. Jos laskutuksen jakoprosenttien yhteissumma ei ole 100 prosentti, seurauksena on virhe. Kun laskutuksen jakoprosentteja on muokattu, poista virhe päivittämällä sivu.

Voit kokeilla myös **Jaa tasaisesti** -vaihtoehdon valintaa sopimusrivin asiakkaan aliruudukossa. Tämä toiminto jakaa laskutuksen jaot tasaisesti kaikille sopimusrivin asiakkaille. Mahdollinen pyöristyskerron lisätään pyöristysasiakkaaseen. Yksi sopimusrivin asiakas merkitään aina **Pyöristys**-asiakkaaksi määrittämällä **Pyöristys**-merkinnän arvoksi **Kyllä**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]