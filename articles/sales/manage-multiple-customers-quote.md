---
title: Useiden asiakkaiden hallinta projektitarjouksissa
description: Tässä aiheessa on tietoja siitä, miten käsitellään tarjouksia, joissa käsitellään useita asiakkaita, jotka rahoittavat projektia.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 8b1d9284c063e34e34ec6525072a1f8f860116b6
ms.sourcegitcommit: 56c42d7f5995a674426a1c2a81bae897dceb391c
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/01/2020
ms.locfileid: "3908082"
---
# <a name="manage-multiple-customers-on-project-quotes"></a>Useiden asiakkaiden hallinta projektitarjouksissa

_**Koskee:** Project Operationsin resurssiin / muuhun kuin resurssiin perustuvia skenaarioita, Lite-käyttöönotto-kaupasta proformalaskutukseen_

Projektitarjoukset tukevat skenaariota, joissa ehdotukseen liittyy useita asiakkaita, jotka rahoittavat sopimuksen. Tarjouksen **Yhteenveto**-välilehdessä on **Mahdollinen asiakas** -kenttä, joka määrittää kaupan ensisijaisen asiakkaan. Sopimuksen muut asiakkaat voidaan määrittää projektitarjouksen **Asiakkaat**-välilehdessä.

Kaikki tarjouksen asiakkaat projektitarjouksen **Asiakkaat**-välilehdessä ovat projektitarjouksen rivin oletusarvona tarjousta varten luoduille **uusille** projektipohjaisille tarjousriveille. Aiemmin luodut projektipohjaiset tarjousrivit eivät peri uusia tarjouksen asiakastietueita, jotka on luotu niiden jälkeen.

Tarjouksen asiakkaat ja tarjousrivin asiakkaat voidaan lisätä, päivittää tai poistaa milloin tahansa, ennen kuin tarjous on voitettu. Tarjouksen kelvollinen asiakas täytyy määrittää asiakkaaksi omistavan yrityksen tai oikeushenkilön **Asiakkaat**-sivulla. Yritykset määritetään Dynamics 365 Project Operationsin **Projektinhallinta ja kirjanpito** -moduulissa, ja ne ovat käytettävissä yrityksinä Project Operationsin **Projektimyynti ja toimitus** -moduuleissa.

## <a name="concept-of-a-primary-customer"></a>Ensisijaisen asiakkaan käsite

Asiakas, joka on listattu projektitarjouksen **Yhteenveto**-välilehdessä mahdollisena asiakkaana, on tarjouksen ensisijainen asiakas. Jos yrität poistaa ensisijaisen asiakkaan tarjouksen asiakasluettelosta, näkyviin tulee virhe, jonka mukaan tarjouksen ensisijaista asiakastietuetta ei voi poistaa.

Ensisijaista asiakasta ei saa päivittää tarjouksen asiakasluettelosta. Voit kuitenkin vaikuttaa ensisijaiseen asiakkaaseen muuttamalla mahdollisen asiakkaan tarjouksen **Yhteenveto**-välilehdessä. Kun tämä kenttä päivitetään **tarjouksen yhteenvedossa**, juuri valittu potentiaalinen asiakas lisätään uudeksi tarjouksen asiakkaaksi, jolla on **Ensisijainen**-merkintä. Vanha potentiaalinen asiakas on edelleen tarjouksen asiakas.

## <a name="create-update-or-delete-a-quote-customer-record"></a>Tarjouksen asiakastietueen luominen, päivittäminen tai poistaminen

Tarjouksen asiakas voidaan luoda, päivittää tai poistaa **Tarjous**-sivun **Tarjouksen asiakkaat** -välilehdestä. Seuraavassa taulukossa luetellut kentät ovat projektitarjouksen Tarjouksen asiakas -tietueessa.

| **Kenttä** | **Sijainti** | **Relevanssi, tarkoitus ja opastus** | **Loppupään vaikutus** |
| --- | --- | --- | --- |
| Tili | **Tarjouksen asiakkaat** -välilehden muokattava ruudukko sekä tarjousasiakkaan **Päälomake** ja **Pikaluontilomake**. | Näyttää kaikki aktiiviset asiakkuudet. Tämä kenttä lukitaan sen jälkeen, kun tietue on luotu. Jos haluat päivittää sen, poista tietue ja luo se uudelleen. Jos olet kirjannut toteutuneita arvoja tai jos tarjouksen asiakastietue on ensisijainen asiakas, voit poistaa tietueen. | Tarjousasiakkaat kopioidaan tarjousrivin asiakkaina, kun tarjousrivi luodaan. Tarjousasiakkaat kopioidaan myös projektisopimusasiakkaisiin, kun tarjous on voitettu. |
| Laskutuksen jakoprosentti | **Tarjouksen asiakkaat** -välilehden muokattava ruudukko sekä tarjousasiakkaan **Päälomake** ja **Pikaluontilomake**. | Ilmaisee kunkin laskuttamaton myyntitapahtuman prosenttiosuuden, joka kohdistetaan tähän tarjousasiakkaaseen. | Kopioidaan luotaviin uusiin tarjousriveihin ja projektisopimusasiakkaisiin. |
| Laskutusyhteyshenkilön nimi | **Tarjouksen asiakkaat** -välilehden muokattava ruudukko sekä tarjousasiakkaan **Päälomake** ja **Pikaluontilomake**. | Tämä on tekstikenttä, ja sitä tulisi käyttää tämän asiakkaan laskun yhteyshenkilön määrittämiseen. Nämä tulevat oletusarvona liittyvästä asiakastietueesta | Kopioidaan projektisopimusasiakkaisiin, kun tarjous on voitettu, ja puolestaan asiakkaalle luodun laskun Laskutusyhteyshenkilön nimi -kenttään. |
| Laskutusosoitteen nimi | **Tarjouksen asiakkaat** -välilehden muokattava ruudukko sekä tarjousasiakkaan **Päälomake** ja **Pikaluontilomake**. | Tätä tekstikenttää tulisi käyttää tämän asiakkaan laskun yhteyshenkilön määrittämiseen. | Kopioidaan projektisopimusasiakkaisiin, kun tarjous on voitettu, ja puolestaan asiakkaalle luodun laskun **Laskutusyhteyshenkilön** nimi -kenttään. |
| Maksuehdot | **Tarjouksen asiakkaat** -välilehden muokattava ruudukko sekä tarjousasiakkaan **Päälomake** ja **Pikaluontilomake**. | Tämä on asetusjoukko, jonka arvot ovat oletusarvon mukaan liitetystä asiakkuustietueesta. | Kopioidaan projektisopimusasiakkaisiin, kun tarjous on voitettu, ja puolestaan asiakkaalle luodun laskun **Laskutusyhteyshenkilön** nimi -kenttään. |
| Onko pyöristetty | **Tarjouksen asiakkaat** -välilehden muokattava ruudukko sekä tarjousasiakkaan **Päälomake** ja **Pikaluontilomake**. | Osoittaa, onko tämä asiakas tämän kaupan oletuspyöristyksen asiakas. | Kopioidaan projektisopimusasiakkaisiin, kun tarjous on voitettu. |
| Omistava yritys | **Tarjouksen asiakkaat** -välilehden muokattava ruudukko sekä tarjousasiakkaan **Päälomake** ja **Pikaluontilomake**. | Oikeushenkilö, jonka avulla tämä asiakas on määritetty **Projektinhallinta ja kirjanpito** -moduulissa. Tämä kenttä on vain luku -tilassa ja se määritetään itse tarjouksen omistavalle yritykselle. **Asiakkuus**-kenttään lisättävä asiakasluettelo on jo suodatettu tämän omistavan yrityksen luetteloon Project Operationsin **Projektinhallinta ja kirjanpito** -moduulissa. | Omistava yritys vastaa oikeushenkilön käsitettä Project Operationsin **Projektinhallintaja kirjanpito** -moduulissa. Kaikki tästä projektista kertyvät kustannukset ja tuotot kirjataan omistavan yrityksen kirjanpitoon. |
| Ei-ylitettävä rajoitus | **Tarjouksen asiakkaat** -välilehden muokattava ruudukko sekä tarjousasiakkaan **Päälomake** ja **Pikaluontilomake**. | Osoittaa, onko neuvoteltu kyseiselle asiakkaalle laskutettavaan kokonaissummaan neuvoteltu rajoitus tai yläraja. | Kopioidaan projektisopimusasiakkaisiin, kun tarjous on voitettu. |

## <a name="editing-billing-split-percentages"></a>Laskutuksen jakoprosenttien muokkaaminen

Voit muokata laskutuksen jakoprosentteja käyttämällä rivin sisäistä ruudukonmuokkauskokemusta. Kun laskutuksen jakoprosentit eivät ole yhteensä 100 %, virhe tapahtuu. Kun olet päivittänyt laskutuksen jakamisprosentit, voit poistaa virheen päivittämällä sivun.

Voit myös kokeilla valita **Jaa tasaisesti** tarjouksen asiakkaiden aliruudukossa. Tämä toiminto kohdistaa laskutuksen jaot kaikkiin tarjousasiakkaisiin. Jos pyöristyskerroin on, se lisätään pyöristysasiakkaaseen. Yksi tarjouksen asiakkaista merkitään aina pyöristysasiakkaaksi. Tämä tarkoittaa sitä, että tarjousasiakastietueessa on **Pyöristys**-merkinnän arvoksi määritetty **Kyllä**. Tämä on yleensä tarjouksen ensisijainen asiakas, mutta sitä voi muuttaa.