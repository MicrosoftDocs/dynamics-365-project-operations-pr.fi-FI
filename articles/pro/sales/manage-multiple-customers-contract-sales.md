---
title: Useiden asiakkaiden hallinta projektisopimuksissa – lite
description: Tässä aiheessa on tietoja useiden asiakkaiden hallinnasta projektisopimuksissa.
author: rumant
manager: Annbe
ms.date: 10/27/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: b248dabdbd5239b140da7c99d3f38609facfe75e
ms.sourcegitcommit: f6f86e80dfef15a7b5f9174b55dddf410522f7c8
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/31/2020
ms.locfileid: "4181313"
---
# <a name="manage-multiple-customers-on-project-contracts---lite"></a>Useiden asiakkaiden hallinta projektisopimuksissa – lite

_**Käytetään:** Lite-käyttöönotto – kauppa proformalaskutukseen_

Dynamics 365 Project Operationsin projektisopimukset tukevat skenaariota, jossa sopimuksessa on useita kauppaa rahoittavia asiakkaita. **Projektisopimus**-sivun **Yhteenveto**-kentässä on **Asiakas**-kenttä. Tämä kenttä ilmaisee kaupan ensisijaisen asiakkaan. Muut kaupan asiakkaat voidaan määrittää **Projektisopimus**-sivun **Asiakkaat**-välilehdessä.

Kaikki projektisopimuksen luettelossa olevat asiakkaat ovat oletusarvoisesti projektipohjaisen sopimusrivin asiakkaita projektisopimukselle luotavilla uusilla sopimusriveillä. Aiemmin luodut projektipohjaiset sopimusrivit eivät peri uusia sopimuksen asiakkaita uusia tietueita luotaessa.

Tuotepohjaiset sopimusrivit liitetään automaattisesti ensisijaiseen asiakkaaseen.

Sopimuksen asiakkaita ja sopimusrivin asiakkaita voidaan lisätä, päivittää tai poistaa koska tahansa ennen sopimuksen voittamista.

## <a name="primary-customer"></a>Ensisijainen asiakas

Projektisopimuksen **Yhteenveto**-välilehdessä potentiaalisena asiakkaana mainittu asiakas on sopimuksen ensisijainen asiakas. Jos yrität poistaa ensisijaisen asiakkaan sopimuksen asiakasluettelosta, saat virhesanoman, jonka mukaan sopimuksen ensisijaisen asiakkaan tietuetta ei voi poistaa.

Ensisijaista asiakasta ei voi päivittää sopimuksen asiakasluettelossa. Sen sijaan on muutettava potentiaalista asiakasta sopimuksen **Yhteenveto**-välilehdessä. Kun tämä kenttä päivitetään **Sopimuksen yhteenveto** -sivulla, uusia asiakas lisätään uutena sopimuksen asiakkaana siten, että siinä on määritetty **Ensisijainen**-merkintä. Edellinen ensisijainen asiakas on silti edelleen sopimuksen asiakas.

## <a name="create-update-or-delete-a-contract-customer-record"></a>Sopimuksen asiakastietueen luominen, päivittäminen tai poistaminen

Sopimuksen asiakas voidaan luoda, päivittää tai poistaa **Projektisopimus**-sivun **Asiakkaat**-välilehdessä. Seuraavan taulukon kentät ovat projektisopimuksen sopimuksen asiakastietueessa, ja ne kannattaa muistaa sopimusta käytettäessä.

| Field | Sijainti | Kuvaus | Loppupään vaikutus |
| --- | --- | --- | --- |
| **Asiakas** | Ruudukkoa voi muokata **Sopimuksen asiakkaat** -välilehdessä sekä sopimusrivin asiakkaan **Pää**- ja **Pikaluonti**-lomakkeissa. | Näyttää kaikki aktiiviset asiakkuudet. Tämä kenttä lukitaan sen jälkeen, kun tietue on luotu. Tilin voi päivittää poistamalla tietueen ja luomalla sen uudelleen. Jos olet kirjannut todellisia arvoja ja jos sopimuksen asiakastietue on ensisijainen asiakas, tietuetta ei voi poistaa. | Sopimuksen asiakkaat kopioidaan sopimusrivin asiakkaina sopimusriviä luotaessa. |
| **Laskutuksen jakoprosentti** | Ruudukkoa voi muokata **Sopimuksen asiakkaat** -välilehdessä sekä sopimusrivin asiakkaan **Pää**- ja **Pikaluonti**-lomakkeissa. | Ilmaisee kunkin tälle sopimuksen asiakkaalle määritetyn laskuttamattoman myyntitapahtuman prosentin. | Kopioidaan uusille sopimusriveille ja uusien sopimusrivien projektinsopimusrivin asiakkaille. |
| **Laskutusyhteyshenkilön nimi** | Ruudukkoa voi muokata **Sopimuksen asiakkaat** -välilehdessä sekä sopimusrivin asiakkaan **Pää**- ja **Pikaluonti**-lomakkeissa. | Tätä tekstikenttää tulisi käyttää tämän asiakkaan laskun yhteyshenkilön määrittämiseen. Tämän kentän oletusarvo saadaan liittyvästä tilitietueesta. | Kopioidaan tälle asiakkaalle luodun laskun **Laskutusyhteyshenkilön nimi** -kenttään. |
| **Laskutusosoitteen nimi** | Ruudukkoa voi muokata **Sopimuksen asiakkaat** -välilehdessä sekä sopimusrivin asiakkaan **Pää**- ja **Pikaluonti**-lomakkeissa | Tätä tekstikenttää tulisi käyttää tämän asiakkaan laskun yhteyshenkilön määrittämiseen. Tämän kentän oletusarvo saadaan liittyvästä tilitietueesta. | Kopioidaan tälle asiakkaalle luodun laskun **Laskutusyhteyshenkilön nimi** -kenttään. |
| **Maksuehdot** | Ruudukkoa voi muokata **Sopimuksen asiakkaat** -välilehdessä sekä sopimusrivin asiakkaan **Pää**- ja **Pikaluonti**-lomakkeissa. | Oletusarvot saadaan liittyvästä tilitietueesta. | Kopioidaan tälle asiakkaalle luodun laskun **Laskutusyhteyshenkilön nimi** -kenttään. |
| **Onko pyöristetty** | Ruudukkoa voi muokata **Sopimuksen asiakkaat** -välilehdessä sekä sopimusrivin asiakkaan **Pää**- ja **Pikaluonti**-lomakkeissa. | Osoittaa, onko tämä asiakas tämän kaupan oletuspyöristyksen asiakas. Projektisopimuksessa voi olla vain yksi pyöristysasiakas. | Kun kustannusten ja laskuttamattoman myynnin määrän jako johtaa pyöristyseroon, kyseistä eroa käytetään tähän asiakkaaseen yhdistävässä todellisessa arvossa. |
| **Ei-ylitettävä rajoitus** | Ruudukkoa voi muokata **Sopimuksen asiakkaat** -välilehdessä sekä sopimusrivin asiakkaan **Pää**- ja **Pikaluonti**-lomakkeissa | Ilmaisee, jos tämän sitoumuksen asiakkaan laskutuksen kokonaissummassa on neuvoteltu raja tai yläraja. | Sopimuksen asiakastasolla määritetty **Ei-ylitettävä rajoitus** arvioidaan tähän sopimuksen asiakkaaseen viittaavassa **Laskuttamattoman myynnin todelliset arvot** -kohdassa. |

## <a name="edit-billing-split-percentages"></a>Laskutuksen jakoprosenttien muokkaaminen

Laskutuksen jakoprosenttia voidaan muokata ruudukon muokkaustoiminnolla. Jos laskutuksen jakoprosenttien yhteissumma ei ole 100 prosenttia, seurauksena on virhe. Kun laskutuksen jakoprosentteja on muokattu, hylkää virhe päivittämällä sivu.

Voit myös valita **Jaa tasaisesti** **Sopimuksen asiakkaat** -aliruudukossa, jolloin laskutus jaetaan tasaisesti kaikille sopimuksen asiakkaille. Mahdollinen pyöristyskerron lisätään pyöristysasiakkaaseen. Yksi sopimuksen asiakkaista merkitään aina **pyöristysasiakkaaksi**, minkä vuoksi sopimuksen asiakastietueen pyöristysmerkintänä on **Kyllä**. Yleensä kyse on sopimuksen ensisijaisesta asiakkaasta, mutta se voidaan vaihtaa.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]