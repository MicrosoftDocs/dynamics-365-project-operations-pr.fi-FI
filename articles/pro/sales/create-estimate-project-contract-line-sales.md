---
title: Projektipohjaisen sopimusrivin arviointi – lite
description: Tässä aiheessa on tietoja projektipohjaisen sopimusrivin arvioinnista.
author: rumant
ms.date: 03/30/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 179994a2515686bce2370964121cbdca08a9d085
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/14/2022
ms.locfileid: "8597334"
---
# <a name="estimate-a-projectbased-contract-line---lite"></a>Projektipohjaisen sopimusrivin arviointi – lite

_**Käytetään:** Lite-käyttöönotto – kauppa proformalaskutukseen_

Dynamics 365 Project Operationsin projektipohjaisella sopimusrivillä on tietoja, joiden avulla voi arvioida sopimusrivin toimittamiseen liittyvän työn kustannuksia ja potentiaalista tuottoa.

Projektipohjaisen sopimusrivin voi arvioida siirtymällä projektipohjaisella **sopimusrivillä** **Sopimusrivin tiedot** -välilehteen.  Arvion voi luoda projektipohjaisella sopimusrivillä kahdella tavalla:

   - Luo arvio suoraan sopimusrivillä lisäämällä sopimusrivin tiedot manuaalisesti.
   - Luo projekti ja projektisuunnitelma ja liitä sitten projekti ja tehtävät projektin sopimusriville. Tällä tavoin otetaan käyttöön prosessi, jolla voit tuoda projektisuunnitelman arvion sopimusriville sopimusriviin sisältyvien komponenttien perusteella.

## <a name="create-an-estimation-directly-on-a-projectbased-contract-line"></a>Arvioinnin luominen suoraan projektipohjaisella sopimusrivillä

Arvion luonti suoraan projektipohjaisella sopimusrivillä tapahtuu seuraavia vaiheita seuraamalla:

1. Siirry sopimusriville ja valitse **Sopimusrivin tiedot** -välilehti. Tässä välilehdessä luotavat rivit lasketaan yhteen, ja ne näkyvät tämän **sopimusrivin** **sopimuksen arvona**. 
2. Valitse **Sopimusrivin tiedot** -alaruudukossa **Uusi sopimusrivin tieto**. Pikaluonnin liukusäädin avautuu. Seuraavat kentät ovat käytettävissä **Sopimusrivin tiedot** -sivulla.

| Kenttä | Sijainti | Kuvaus | Loppupään vaikutus |
| --- | --- | --- | --- |
| **Kuvaus** | **Pikaluonti** | Tietyn arvion kuvaus. | Tämä arvo saa oletusarvon, joka on automaattisesti luotu liittyvä sopimusrivin kustannustieto. |
| **Tapahtumaluokka** | **Pikaluonti** | Tämä on tapahtumaluokkien luettelo, joka sisältyy projektipohjaisen sopimusrivin **Yleiset**-välilehteen. | Tämä arvo saa oletusarvon, joka on automaattisesti luotu liittyvä sopimusrivin kustannustieto. |
| **Valitse tuote** | **Pikaluonti** | Koskee, kun tapahtumaluokka on **Materiaali**. Voit valinnaisesti määrittää, onko tämä arviorivi **Aiemmin luodulle** (luettelon) tuotteelle vai **Käsin lisättävälle** tuotteelle. | Tämä arvo saa oletusarvon, joka on automaattisesti luotu liittyvä sopimusrivin kustannustieto. |
| **Tuote** | **Pikaluonti** | Tuoteluettelon tuotteen tunnus. Tämä kenttä on käytössä vain, kun valitset **Aiemmin luodun tuotteen** **Valitse tuote** -kentässä. Tunnuksen avulla haetaan myyntihinta sopimuksen projektihinnastosta. | Tämä arvo saa oletusarvon, joka on automaattisesti luotu liittyvä sopimusrivin kustannustieto. |
| **Käsin lisätty tuote** | **Pikaluonti** | Tekstikenttä, johon syötetään tuotteen nimi. Tämä kenttä on käytössä vain, kun valitset **Käsin lisättävä** **Valitse tuote** -kentässä.| Tämä arvo saa oletusarvon, joka on automaattisesti luotu liittyvä sopimusrivin kustannustieto. |
| **Rooli** | **Pikaluonti** | Tämän työn suorittavan tai tämän kulun aiheuttavan henkilön rooli. | Tämä arvo saa oletusarvon, joka on automaattisesti luotu liittyvä sopimusrivin kustannustieto.|
| **Luokka** | **Pikaluonti** | Työn tai kulun luokka. |Tämä arvo saa oletusarvon, joka on automaattisesti luotu liittyvä sopimusrivin kustannustieto.|
| **Aloituspäivämäärä** | **Pikaluonti** | Työn alkamispäivämäärä. | Tämä arvo saa oletusarvon, joka on automaattisesti luotu liittyvä sopimusrivin kustannustieto. |
| **Päättymispäivä** | **Pikaluonti** | Työn päättymispäivämäärä. | Tämä arvo saa oletusarvon, joka on automaattisesti luotu liittyvä sopimusrivin kustannustieto. |
| **Resursointiyksikkö** | **Pikaluonti** | Resursoiva yksikkö, joka aiheittaa tämän kustannuksen ja tarjoaa resurssit sen suhteen tehtävään työhön. |Tämä arvo saa oletusarvon, joka on automaattisesti luotu liittyvä sopimusrivin kustannuksen tieto ja jota käytetään kustannushinnan hakemiseen. |
| **Yksikön aikataulutus** | **Pikaluonti** | Työn, tuotteen tai kulun yksikköryhmä. Yksiköt kuuluvat yksikköaikatauluun tai yksiköiden ryhmään. Esimerkiksi *mailit* ja *kilometrit (km)* ovat etäisyyttä kuvaavaan yksikköryhmään kuuluvia yksiköitä. | Tämä arvo saa oletusarvon, joka on automaattisesti luotu liittyvä sopimusrivin kustannustieto. |
| **Yksikkö** | **Pikaluonti** | Työn, tuotteen tai kulun yksikkö. | Tämä arvo saa oletusarvon, joka on automaattisesti luotu liittyvä sopimusrivin kustannustieto. |
| **Määrä** | **Pikaluonti** | Työn, tuotteen tai kulun määrä. | Tämä arvo saa oletusarvon, joka on automaattisesti luotu liittyvä sopimusrivin kustannustieto. |
| **Yksikköhinta** | **Pikaluonti** | Työn suorittavan roolin laskutushinta, tuotteen yksikkökustannus tai tuote- tai kululuokan myyntihinta. Tämä kenttä saa oletusarvoksi **Ajan** perustuen alkamispäivänä voimassa olevassa projektihinnastossa olevien roolihintarivien hinnoitteludimensioiden arvojen yhdistelmiin. **Kulujen** osalta tämän kentän oletusarvo saadaan sen projektihinnaston tapahtumaluokan hintamäärityksistä, joka on voimassa alkamispäivänä. Jos tapahtumaluokan hinnoittelutapa ei ole **yksikköhinta**, oletusarvoa ei ole, ja tämä kenttä jätetään tyhjäksi. Tämän kentän oletusarvo tuotteille perustuu **Hinnaston nimike** -riviin projektihinnastossa, joka on voimassa alkamispäivänä.| Työn suorittavan roolin kustannushinta, kululuokan yksikkökustannus tai tuotteen yksikkökustannus. Tämä kenttä saa oletusarvoksi **Ajan** perustuen alkamispäivänä voimassa olevaan sopimusyksikköön liitetyssä projektihinnastossa olevien roolihintarivien hinnoitteludimensioiden arvojen yhdistelmiin. Kulujen osalta tämän kentän oletusarvo perustuu siihen sopimusyksikköön liitettyyn kustannushintaluettelon luokan hintariviin, joka on voimassa alkamispäivänä. Jos tapahtumaluokan hinnoittelutapa ei ole hinta yksikköä kohden, oletusarvoa ei ole, ja tämä kenttä jätetään tyhjäksi. Tämän kentän oletusarvo tuotteille perustuu **Hinnaston nimike** -riviin kustannushinnastossa, joka liittyy sopimusyksikköön, joka on voimassa alkamispäivänä.|
| **Arvioitu vero** | **Pikaluonti** | Tämän työn tai kulun arvioitu vero. | Tämän työn tai kulun arvioitu vero. |
| **Summa** | **Pikaluonti** | Tämän kentän arvo voidaan lisätä, jos **Määrä**- ja  **Hinta**-kentät jätetään tyhjiksi. Jos **Määrä**- ja **Hinta**-kentät on täytetty, **Summa**-kenttä on vain luku -muotoinen ja se lasketaan kaavalla **(Määrä \* Yksikköhinta) + Vero**. | &nbsp; |

## <a name="update-prices-on-contract-line-details"></a>Sopimusrivin tietojen hintojen päivittäminen

Jos muutat sopimukseen tai sopimusyksikön kustannushintaluetteloon liitettyjä projektihinnaston hintoja, yksittäisen sopimusrivin tietojen hinnat voidaan päivittää vastaamaan muutosta. Valitse **Palvelusopimus**-sivulla **Laske uudelleen**. Näkyviin tulee varoitus, joka ilmoittaa, että kaikkien tämän sopimuksen sopimusrivien hinnat nollataan. Valitsemalla **Kyllä** voit päivittää sekä myynnin että kustannuksen sopimusrivin tietojen hinnat päivitetään.

## <a name="access-contract-line-details-for-cost"></a>Kustannuksen sopimusrivin tietojen käyttäminen

Valitse **Sopimusrivin tiedot** -välilehdessä ruudussa rivi, jolloin toiminnot tulevat näkyviin aliruudukon työkalurivillä. Aliruudukon työkalurivin ensimmäinen toiminto **Avaa kustannuksen tiedot**. Saat tämän sopimusrivin tietojen liittyvän kustannushinnan ja summan näkyviin valitsemalla **Avaa kustannuksen tiedot**. 

> [!NOTE]
> Resursointiyrityksen, resursointiyksikön, määrän, päivämäärien, roolin tai luokan arvojen muuttaminen **kustannuksen** sopimusrivin tiedoissa muuttaa myös vastaavat arvot **myynnin** sopimusrivin tiedoissa.

## <a name="currency-on-contract-line-details-for-cost-and-sales"></a>Kustannusten ja myynnin sopimusrivin tietojen valuutta

**Myynnin** sopimusrivin tiedot määrittävät oletusvaluutan projektihinnastosta, joka on voimassa sopimusrivin tietojen alkamispäivänä.

**Kustannusten** sopimusrivin tiedot määrittävät oletusvaluutan sen sopimuksen sopimusyksikön hinnastosta, joka on voimassa **kustannusten** sopimusrivin tietojen alkamispäivänä.

Kannattavuuslaskelmat muuntavat **kustannusten** ja **myynnin** sopimusrivin tietojen summat ympäristön perusvaluutaksi, jolloin voidaan raportoida sopimuksen todelliset ja arvioidut kokonaiskatteet.

> [!NOTE]
> Valuutan pyöristysvirheitä ja muuttuneita katteita voi esiintyä, koska vaihtokurssien voimassaolopäivä puuttuu. Näitä laskelmia voi käyttää vain projektisopimuksissa, koska ne ovat pyöristyksiä, ja ne eivät ole varsinaisia lakimääräistä tai muuta raportointia, joka edellyttää valuuttakurssien pyöristystarkkuutta ja päivämäärävaikuttavuuden tuntemusta.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
