---
title: Projektipohjaisen sopimusrivin arviointi
description: Tässä aiheessa on tietoja projektipohjaisten sopimusrivien arvioista.
author: rumant
manager: Annbe
ms.date: 10/27/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 24299d997074efcff3776168652809d490c81b17
ms.sourcegitcommit: f6f86e80dfef15a7b5f9174b55dddf410522f7c8
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/31/2020
ms.locfileid: "4180458"
---
# <a name="estimate-a-projectbased-contract-line"></a>Projektipohjaisen sopimusrivin arviointi

_**Käytetään:** Project Operationsin resursseihin ja ei-varastoitaviin perustuvissa skenaarioissa_ 

Dynamics 365 Project Operationsin projektipohjaisella sopimusrivillä on tietoja, joiden avulla voi arvioida sopimusrivin toimittamiseen liittyvän työn kustannuksia ja potentiaalista tuottoa.

Projektipohjaisen sopimusrivin voi arvioida siirtymällä projektipohjaisella **sopimusrivillä** **Sopimusrivin tiedot** -välilehteen.  Arvion voi luoda projektipohjaisella sopimusrivillä kahdella tavalla:

   - Luo arvio suoraan sopimusrivillä lisäämällä sopimusrivin tiedot manuaalisesti.
   - Luo projekti ja projektisuunnitelma ja liitä sitten projekti ja tehtävät projektin sopimusriville. Tällä tavoin otetaan käyttöön prosessi, jolla voit tuoda projektisuunnitelman arvion sopimusriville sopimusriviin sisältyvien komponenttien perusteella.

## <a name="create-an-estimate-directly-on-a-projectbased-contract-line"></a>Arvion luominen suoraan projektipohjaisella sopimusrivillä

1. Siirry sopimusriville ja valitse **Sopimusrivin tiedot** -välilehti. Tässä välilehdessä luotavat rivit lasketaan yhteen, ja ne näkyvät tämän **sopimusrivin** **sopimuksen arvona**. 
2. Valitse **Sopimusrivin tiedot** -alaruudussa **+ Uusi sopimusrivin tieto**. Pikaluonnin liukusäädin avautuu. **Sopimusrivin tiedot** -lomakkeessa on seuraavat kentät:

| Field | Sijainti | Kuvaus | Loppupään vaikutus |
| --- | --- | --- | --- |
| **Kuvaus** | **Pikaluonti** | Tietyn arvion kuvaus. | Tämän kentän oletusarvona on automaattisesti luotuihin kustannuksiin liittyvän sopimusrivin tiedot. |
| **Tapahtumaluokka** | **Pikaluonti** | Tässä avattavassa luettelossa on tapahtumaluokkia, jotka sisältyvät projektipohjaisen sopimusrivin **Yleiset**-välilehteen. | Tämän kentän oletusarvona on automaattisesti luotuihin kustannuksiin liittyvän sopimusrivin tiedot. |
| **Rooli** | **Pikaluonti** | Tämän työn suorittavan tai tämän kulun aiheuttavan henkilön rooli. | Tämän kentän oletusarvona on automaattisesti luotuihin kustannuksiin liittyvän sopimusrivin tiedot. |
| **Luokka** | **Pikaluonti** | Työn tai kulun luokka. | Tämän kentän oletusarvona on automaattisesti luotuihin kustannuksiin liittyvän sopimusrivin tiedot. |
| **Aloituspäivämäärä** | **Pikaluonti** | Työn alkamispäivämäärä. | Tämän kentän oletusarvona on automaattisesti luotuihin kustannuksiin liittyvän sopimusrivin tiedot. |
| **Päättymispäivä** | **Pikaluonti** | Työn päättymispäivämäärä. | Tämän kentän oletusarvona on automaattisesti luotuun kustannukseen liittyvän sopimusrivin tiedot. |
| **Resursoiva yritys** | **Pikaluonti** | Resursoiva yritys tai yritys, joka aiheuttaa tämän kustannuksen ja toimittaa resurssin siinä tehtävää työtä varten. | Tämän kentän oletusarvona on automaattisesti luotuihin kustannuksiin liittyvän sopimusrivin tiedot. Tätä kenttää käytetään myös kustannushinnan haussa. |
| **Resursointiyksikkö** | **Pikaluonti** | Tämän kustannuksen aiheuttava resursointiyksikkö, joka toimittaa siinä työtä tekevän resurssin. | Tämän kentän oletusarvona on automaattisesti luotuihin kustannuksiin liittyvän sopimusrivin tiedot. Tätä kenttää käytetään myös kustannushinnan haussa. |
| **Yksikön aikataulutus** | **Pikaluonti** | Työn tai kulun yksikköryhmä. Yksiköt kuuluvat yksikköaikatauluun tai yksiköiden ryhmään. Esimerkiksi *mailit* ja *kilometrit (km)* ovat etäisyyttä kuvaavaan yksikköryhmään kuuluvia yksiköitä. | Tämän kentän oletusarvona on automaattisesti luotuihin kustannuksiin liittyvän sopimusrivin tiedot. |
| **Yksikkö** | **Pikaluonti** | Työn tai kulun yksikkö. | Tämän kentän oletusarvona on automaattisesti luotuihin kustannuksiin liittyvän sopimusrivin tiedot. |
| **Määrä** | **Pikaluonti** | Työn tai kulun määrä. | Tämän kentän oletusarvona on automaattisesti luotuihin kustannuksiin liittyvän sopimusrivin tiedot. |
| **Yksikköhinta** | **Pikaluonti** | Työn suorittavan rooli laskutushinta tai kululuokan myyntihinta. Tämän kentän oletusarvona on **aikaan** perustuva roolin ja resursointiyksikön yhdistelmä projektihinnastossa, joka on voimassa alkamispäivänä. Kulujen osalta tämän kentän oletusarvo saadaan sen projektihinnaston tapahtumaluokan hintamäärityksistä, joka on voimassa alkamispäivänä. Jos tapahtumaluokan hinnoittelutapa ei ole **yksikköhinta**, oletusarvoa ei ole, ja tämä kenttä jätetään tyhjäksi. | Työn suorittavan rooli kustannushinta tai kululuokan yksikkökohtainen kustannus. Tämän kentän oletusarvo **ajalle perustuu roolin** ja resursointiyksikön yhdistelmään sillä sopimusyksikköön liitetyn kustannushintaluettelon roolin hintarivillä, joka on voimassa alkamispäivänä. Kulujen osalta tämän kentän oletusarvo perustuu siihen sopimusyksikköön liitettyyn kustannushintaluettelon luokan hintariviin, joka on voimassa alkamispäivänä. Jos tapahtumaluokan hinnoittelutapa ei ole hinta yksikköä kohden, oletusarvoa ei ole, ja tämä kenttä jätetään tyhjäksi. |
| **Arvioitu vero** | **Pikaluonti** | Tämän työn tai kulun käyttäjän antama arvioitu vero. | Tämän työn tai kulun käyttäjän antama arvioitu vero. |
| **Summa** | **Pikaluonti** | Käyttäjä voi lisätä tämän kentän arvon, jos **Määrä**- ja **Hinta**-kentät on jätetty tyhjiksi. Jos **Määrä**- ja **Hinta**-kentät on täytetty, **Summa**-kenttä on vain luku -muotoinen ja se lasketaan kaavalla **(Määrä \* Yksikköhinta) + Vero**. | &nbsp; |

## <a name="update-prices-on-contract-line-details"></a>Sopimusrivin tietojen hintojen päivittäminen

Jos muutat sopimukseen tai sopimusyksikön kustannushintaluetteloon liitettyjä projektihinnaston hintoja, yksittäisen sopimusrivin tietojen hinnat voidaan päivittää vastaamaan muutosta. Valitse **Palvelusopimus**-sivulla **Laske uudelleen**. Avautuva varoitus ilmoittaa, että kaikkien tämän sopimuksen sopimusrivien hinnat palautetaan alkutilaan. Valitsemalla **Kyllä** voit päivittää sekä myynnin että kustannuksen sopimusrivin tietojen hinnat päivitetään.

## <a name="access-contract-line-details-for-cost"></a>Kustannuksen sopimusrivin tietojen käyttäminen

Valitse **Sopimusrivin tiedot** -välilehdessä ruudussa rivi, jolloin toiminnot tulevat näkyviin aliruudukon työkalurivillä. Aliruudukon työkalurivin ensimmäinen toiminto **Avaa kustannuksen tiedot**. Saat tämän sopimusrivin tietojen liittyvän kustannushinnan ja summan näkyviin valitsemalla **Avaa kustannuksen tiedot**. 

> [!NOTE]
> Resursointiyrityksen, resursointiyksikön, määrän, päivämäärien, roolin tai luokan arvojen muuttaminen **kustannuksen** sopimusrivin tiedoissa muuttaa myös vastaavat arvot **myynnin** sopimusrivin tiedoissa.

## <a name="currency-on-contract-line-details-for-cost-and-sales"></a>Kustannusten ja myynnin sopimusrivin tietojen valuutta

**Myynnin** sopimusrivin tiedot määrittävät oletusvaluutan projektihinnastosta, joka on voimassa sopimusrivin tietojen alkamispäivänä.

**Kustannusten** sopimusrivin tiedot määrittävät oletusvaluutan sen sopimuksen sopimusyksikön hinnastosta, joka on voimassa **kustannusten** sopimusrivin tietojen alkamispäivänä.

Kannattavuuslaskelmat muuntavat **kustannusten** ja **myynnin** sopimusrivin tietojen summat ympäristön perusvaluutaksi, jolloin voidaan raportoida sopimuksen todelliset ja arvioidut kokonaiskatteet.

> [!NOTE]
> Valuutan pyöristysvirheitä ja muuttuneita katteita voi esiintyä, koska vaihtokurssien voimassaolopäivä puuttuu. Käytä näitä projektisopimusten laskelmia vain likimääräisinä arvoina eikä varsinaisena lakisääteisenä tai muuna raportointina, joka edellyttää tarkkuutta pyöristyksen osalta tai tietoisuutta vaihtokurssien voimassaolopäivästä.


[!INCLUDE[footer-include](../includes/footer-banner.md)]