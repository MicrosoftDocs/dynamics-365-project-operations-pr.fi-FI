---
title: Useiden asiakkaiden hallinta projektisopimuksissa
description: Tässä aiheessa on tietoja useiden asiakkaiden hallinnasta projektisopimuksessa.
author: rumant
ms.date: 11/18/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 1adb786c36d43a148e8c5a8b25ded5a997557119f7e6e9e2248935ad4ed211d5
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/06/2021
ms.locfileid: "6992067"
---
# <a name="manage-multiple-customers-on-project-contracts"></a>Useiden asiakkaiden hallinta projektisopimuksissa

Tässä aiheessa on tietoja useiden asiakkaiden hallinnasta projektisopimuksessa. Voit käyttää projektisopimusta, kun useita asiakkaita sisältävä sopimus tarvitaan sopimuksen rahoittamiseen. **Projektisopimus**-sivun **Yhteenveto** -välilehdessä on tietoja sopimuksen ensisijaisesta asiakkaasta. Muut asiakkaat, jotka osallistuvat sopimukseen, voidaan lisätä **Asiakkaat** -välilehteen.

Kaikki projektisopimuksen **Asiakkaat**-välilehden asiakkaat ovat oletusarvoisesti sopimusrivin asiakkaita projektiin perustuvilla uusilla sopimusriveillä. Mahdollisesti aiemmin luodut projektipohjaiset sopimusrivit eivät peri uusia sopimusasiakastietueita, jotka luodaan myöhemmin.

Sopimuksen asiakkaita ja sopimusrivin asiakkaita voidaan lisätä, päivittää tai poistaa koska tahansa ennen sopimuksen voittamista. Projektisopimuksen asiakas täytyy määrittää asiakkaaksi omistavan yrityksen **Asiakkaat**-sivulla. Yrityksen määritetään **Projektinhallinta ja kirjanpito** -moduulissa Dynamics 365 Project Operationsissa, ja ne ovat käytössä yrityksinä **Projektimyynnit**- ja **Toimitus**-moduuleissa Project Operationsissa.

## <a name="primary-customers"></a>Ensisijaiset asiakkaat

Projektisopimuksen **Yhteenveto**-välilehdessä potentiaalisena asiakkaana mainittu asiakas on sopimuksen ensisijainen asiakas. Ensisijaista asiakasta ei voi päivittää sopimuksen asiakasluettelossa. Jos yrität poistaa ensisijaisen asiakkaan sopimuksen asiakasluettelosta, saat virhesanoman, jonka mukaan sopimuksen ensisijaisen asiakkaan tietuetta ei voi poistaa. Vaihda sen sijaan asiakas **Potentiaalinen asiakas** -kentässä projektisopimuksen **Yhteenveto**-välilehdessä. Kun tämä kenttä päivitetään, uusi valittu asiakas lisätään uudeksi sopimusasiakkaaksi, jonka **Ensisijainen** merkinnän arvo on **Kyllä**. Edellinen ensisijainen asiakas on edelleen sopimuksen asiakas, mutta se ei ole enää ensisijainen asiakas.

## <a name="create-update-or-delete-a-contract-customer-record"></a>Sopimuksen asiakastietueen luominen, päivittäminen tai poistaminen

Sopimusasiakas voidaan luoda, päivittää tai poistaa **Sopimusasiakkaat**-välilehdessä **Sopimus**-sivulla. Projektisopimuksen sopimusasiakastietueessa on seuraavat kentät.

| **Kenttä** | **Sijainti** | **Kuvaus** | 
| --- | --- | --- | 
| Tili | Muokattava ruudukko **Sopimusasiakas**-välilehdellä sekä pää- ja pikaluontisivut sopimusasiakkaalle. | Näyttää kaikki aktiiviset asiakkuudet. Tämä kenttä lukitaan sen jälkeen, kun tietue on luotu. Tietueen voi päivittää poistamalla sen ja luomalla sen uudelleen. Jos olet kirjannut todellisia arvoja ja jos sopimuksen asiakastietue on ensisijainen asiakas, tietuetta ei voi poistaa. Sopimuksen asiakkaat kopioidaan sopimusrivin asiakkaina sopimusriviä luotaessa. |
| Laskutuksen jakoprosentti | Muokattava ruudukko **Sopimusasiakas**-välilehdellä sekä pää- ja pikaluontisivut sopimusasiakkaalle. | Ilmaisee kunkin tälle sopimuksen asiakkaalle määritetyn laskuttamattoman myyntitapahtuman prosentin. Kun uusia projektisopimusrivejä luodaan, laskutuksen jakamisprosentti kopioidaan uusille luoduille sopimusriveille ja projektisopimusrivin asiakkaille. |
| Laskutusyhteyshenkilön nimi | Muokattava ruudukko **Sopimusasiakas**-välilehdellä sekä pää- ja pikaluontisivut sopimusasiakkaalle. | Tämän tekstikentän avulla määritetään asiakkaan laskun yhteyshenkilö. Oletusarvo saadaan liittyvästä tilitietueesta. Yhteyshenkilön nimi kopioidaan **Laskutusyhteyshenkilön nimi** -kohtaan asiakkaalle luotavassa laskussa. |
| Laskutusosoitteen nimi | Muokattava ruudukko **Sopimusasiakas**-välilehdellä sekä pää- ja pikaluontisivut sopimusasiakkaalle. | Tämän tekstikentän avulla määritetään asiakkaan laskun yhteyshenkilö. Oletusarvo saadaan liittyvästä tilitietueesta. Nimi kopioidaan asiakkaalle luodun laskun **Laskutusyhteyshenkilön nimi** -kenttään. |
| Maksuehdot | Muokattava ruudukko **Sopimusasiakas**-välilehdellä sekä pää- ja pikaluontisivut sopimusasiakkaalle. | Oletusarvo saadaan liittyvästä tilitietueesta. Ehdot kopioidaan **Laskutusyhteyshenkilön nimi** -kohtaan asiakkaalle luotavassa laskussa. |
| Omistava yritys | Muokattava ruudukko **Projektisopimuksen asiakkaat**-välilehdellä sekä pää- ja pikaluontisivut projektisopimuksen asiakkaille. | Yritys,, johon asiakas on määritetty **Projektinhallinta ja kirjanpito** -moduulissa. Tämä kenttä on vain luku -muotoinen ja sen määrityksenä on projektisopimuksen omistava yritys.</br>**Asiakkuus**-kenttään lisättävä asiakasluettelo on jo suodatettu omistavan yrityksen luetteloon Project Operationsin **Projektinhallinta ja kirjanpito** -moduulissa. Omistava yritys on sama kuin yritys Project Operationsin **Projektinhallinta ja kirjanpito** -moduulissa. Kaikki tästä projektista kertyvät kustannukset ja tuotot kirjataan omistavan yrityksen päätapahtumarekisteriin. |
| Onko pyöristetty | Muokattava ruudukko **Sopimusasiakas**-välilehdellä sekä pää- ja pikaluontisivut sopimusasiakkaalle. | Ilmaisee, onko asiakas kaupan oletuspyöristysasiakas. Projektisopimuksessa voi olla vain yksi pyöristysasiakas. Kun kustannusten ja laskuttamattoman myynnin määrän jako johtaa pyöristyseroon, kyseinen ero sijoitetaan todelliseen arvoon, joka yhdistyy tähän asiakkaaseen. |
| Ei-ylitettävä rajoitus | Muokattava ruudukko **Sopimusasiakas**-välilehdellä sekä pää- ja pikaluontisivut sopimusasiakkaalle. | Ilmaisee, onko tämän sitoumuksen asiakkaan laskutuksen kokonaissummalle neuvoteltu raja tai yläraja. Sopimuksen asiakastasolla määritetty ei-ylitettävä rajoitus arvioidaan tähän sopimusasiakkaaseen viittaavien laskuttamattomien todellisten myyntien perusteella. |

## <a name="edit-billing-split-percentages"></a>Laskutuksen jakoprosenttien muokkaaminen

Laskutuksen jakoprosenttia voidaan muokata ruudukossa. Jos laskutuksen jakoprosenttien yhteissumma ei ole 100 prosentti, seurauksena on virhe. Kun laskutuksen jakoprosenttia on muokattu, päivitä **Projektisopimus**-sivu virheen poistamiseksi.

Voit kokeilla myös **Jaa tasaisesti** -vaihtoehdon valintaa projektisopimusasiakkaiden aliruudukossa. Laskutuksen jakoprosentit kohdistetaan tasaisesti kaikille projektisopimuksen asiakkaille. Mahdollinen pyöristyskerron lisätään pyöristysasiakkaaseen. Jonkin sopimusasiakkaan **Pyöristys** lipun arvon on aina oltava **Kyllä**. Tämä asiakas on pyöristysasiakas. Yleensä pyöristysasiakas on myös palvelusopimuksen ensisijainen asiakas, mutta se ei ole pakollista.


[!INCLUDE[footer-include](../includes/footer-banner.md)]