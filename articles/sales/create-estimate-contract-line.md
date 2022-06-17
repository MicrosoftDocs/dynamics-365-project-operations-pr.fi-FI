---
title: Projektin sopimusrivin arvioiminen
description: Tässä artikkelissa on tietoja projektisopimusrivin arvioista.
author: rumant
ms.date: 10/27/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 553f7e4a9e9f57732267a48da2b299c1751b0c0e
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8932016"
---
# <a name="estimate-a-project-contract-line"></a>Projektin sopimusrivin arvioiminen

_**Käytetään:** Project Operationsin resursseihin ja ei-varastoitaviin perustuvissa skenaarioissa_ 

Dynamics 365 Project Operationsin projektipohjaisella sopimusrivillä on tietoja, joiden avulla voi arvioida sopimusrivin toimittamiseen liittyvän työn kustannuksia ja potentiaalista tuottoa.

Projektipohjaisen sopimusrivin voi arvioida siirtymällä projektipohjaisella **sopimusrivillä** **Sopimusrivin tiedot** -välilehteen.  Arvion voi luoda projektipohjaisella sopimusrivillä kahdella tavalla:

   - Luo arvio suoraan sopimusrivillä lisäämällä sopimusrivin tiedot manuaalisesti.
   - Luo projekti ja projektisuunnitelma ja liitä sitten projekti ja tehtävät projektin sopimusriville. Tällä tavoin otetaan käyttöön prosessi, jolla voit tuoda projektisuunnitelman arvion sopimusriville sopimusriviin sisältyvien komponenttien perusteella.

## <a name="create-an-estimate-directly-on-a-project-contract-line"></a>Arvion luonti suoraan projektin sopimusrivillä

Arvion luonti suoraan projektin sopimusrivillä tapahtuu seuraavia vaiheita seuraamalla:

1. Siirry sopimusriville ja valitse **Sopimusrivin tiedot** -välilehti. Tässä välilehdessä luotavat rivit lasketaan yhteen, ja ne näkyvät tämän **sopimusrivin** **sopimuksen arvona**. 
2. Valitse **Sopimusrivin tiedot** -alaruudukossa **Uusi sopimusrivin tieto**. Pikaluonnin liukusäädin avautuu. Seuraavat kentät ovat käytettävissä **Sopimusrivin tiedot** -sivulla.

| Kenttä | Sijainti | Kuvaus | Loppupään vaikutus |
| --- | --- | --- | --- |
| **Kuvaus** | **Pikaluonti** | Tietyn arvion kuvaus. | Tämä arvo saa oletusarvon, joka on automaattisesti luotu liittyvä sopimusrivin kustannustieto. |
| **Tapahtumaluokka** | **Pikaluonti** | Tämä tapahtumaluokkien luettelo sisältyy projektipohjaisen sopimusrivin **Yleiset**-välilehteen. | Tämä arvo saa oletusarvon, joka on automaattisesti luotu liittyvä sopimusrivin kustannustieto. |
| **Valitse tuote** | **Pikaluonti** | Koskee, kun tapahtumaluokka on **Materiaali**. Voit valinnaisesti määrittää, että tämä arviorivi on **Aiemmin luodulle** (luettelon) tuotteelle tai **Käsin lisättävälle** tuotteelle. | Tämä arvo saa oletusarvon, joka on automaattisesti luotu liittyvä sopimusrivin kustannustieto. |
| **Tuote** | **Pikaluonti** | Tuoteluettelon tuotteen tunnus. Tämä kenttä on käytössä vain, kun valitset **Aiemmin luodun tuotteen** **Valitse tuote** -kentässä. Tunnuksen avulla haetaan myyntihinta sopimuksen projektihinnastosta. | Tämä arvo saa oletusarvon, joka on automaattisesti luotu liittyvä sopimusrivin kustannustieto. |
| **Käsin lisätty tuote** | **Pikaluonti** | Tekstikenttä, johon syötetään tuotteen nimi. Tämä kenttä on käytössä vain, kun valitset **Käsin lisättävä** **Valitse tuote** -kentässä.| Tämä arvo saa oletusarvon, joka on automaattisesti luotu liittyvä sopimusrivin kustannustieto. |
| **Rooli** | **Pikaluonti** | Tämän työn suorittavan tai tämän kulun aiheuttavan henkilön rooli. | Tämä arvo saa oletusarvon, joka on automaattisesti luotu liittyvä sopimusrivin kustannustieto.|
| **Luokka** | **Pikaluonti** | Työn tai kulun luokka. | Tämä arvo saa oletusarvon, joka on automaattisesti luotu liittyvä sopimusrivin kustannustieto.|
| **Aloituspäivämäärä** | **Pikaluonti** | Työn alkamispäivämäärä. | Tämä arvo saa oletusarvon, joka on automaattisesti luotu liittyvä sopimusrivin kustannustieto. |
| **Päättymispäivä** | **Pikaluonti** | Työn päättymispäivämäärä. | Tämä arvo saa oletusarvon, joka on automaattisesti luotu liittyvä sopimusrivin kustannustieto. |
| **Resursoiva yritys** | **Pikaluonti** | Resursoiva yritys tai kustannuksen aiheuttava yritys ja tarjoaa resurssit sen suhteen tehtävään työhön. | Tämä arvo saa oletusarvon, joka on automaattisesti luotu liittyvä sopimusrivin kustannuksen tieto ja jota käytetään kustannushinnan hakemiseen. |
| **Resursointiyksikkö** | **Pikaluonti** | Resursoiva yksikkö, joka aiheittaa tämän kustannuksen ja tarjoaa resurssit sen suhteen tehtävään työhön. | Tämä arvo saa oletusarvon, joka on automaattisesti luotu liittyvä sopimusrivin kustannuksen tieto ja jota käytetään kustannushinnan hakemiseen. |
| **Yksikön aikataulutus** | **Pikaluonti** | Työn, tuotteen tai kulun yksikköryhmä. Yksiköt kuuluvat yksikköaikatauluun tai yksiköiden ryhmään. Esimerkiksi *mailit* ja *kilometrit (km)* ovat etäisyyttä kuvaavaan yksikköryhmään kuuluvia yksiköitä. | Tämä arvo saa oletusarvon, joka on automaattisesti luotu liittyvä sopimusrivin kustannustieto. |
| **Yksikkö** | **Pikaluonti** | Työn, tuotteen tai kulun yksikkö. | Tämä arvo saa oletusarvon, joka on automaattisesti luotu liittyvä sopimusrivin kustannustieto. |
| **Määrä** | **Pikaluonti** | Työn, tuotteen tai kulun määrä. | Tämä arvo saa oletusarvon, joka on automaattisesti luotu liittyvä sopimusrivin kustannustieto. |
| **Yksikköhinta** | **Pikaluonti** | Työn suorittavan roolin laskutushinta, tuotteen yksikkökustannus tai tuote- tai kululuokan myyntihinta. **Ajan** oletusarvo perustuu alkamispäivänä voimassa olevassa projektihinnastossa olevien roolihintarivien hinnoitteludimensioiden arvojen yhdistelmiin. **Kulut**-kentän oletusarvo saadaan alkamispäivänä voimassa olevassa projektihinnastossa olevan tapahtumaluokan hinnoittelumäärityksistä. Jos tapahtumaluokan hinnoittelutapa ei ole **yksikköhinta**, oletusarvoa ei ole, ja tämä kenttä jätetään tyhjäksi. Tämän kentän oletusarvo tuotteille perustuu **Hinnaston nimike** -riviin projektihinnastossa, joka on voimassa alkamispäivänä.| Työn suorittavan roolin kustannushinta, kululuokan yksikkökustannus tai tuotteen yksikkökustannus. **Ajan** oletusarvo perustuu alkamispäivänä voimassa olevaan sopimusyksikköön liitetyssä projektihinnastossa olevien roolihintarivien hinnoitteludimensioiden arvojen yhdistelmiin. **Kulut**-kentän oletusarvo perustuun alkamispäivänä voimassa olevaan sopimusyksikköön yhdistetyssä projektihinnastossa olevan kustannushinnaston luokan hintarivin hinnoittelumäärityksiin. Jos tapahtumaluokan hinnoittelutapa ei ole hinta yksikköä kohden, oletusarvoa ei ole, ja tämä kenttä jätetään tyhjäksi. Tämän kentän oletusarvo tuotteille perustuu **Hinnaston nimike** -riviin kustannushinnastossa, joka liittyy sopimusyksikköön, joka on voimassa alkamispäivänä.|
| **Arvioitu vero** | **Pikaluonti** | Tämän työn tai kulun käyttäjän antama arvioitu vero. | &nbsp; |
| **Summa** | **Pikaluonti** | Tämän kentän arvo voidaan lisätä, jos **Määrä**- ja  **Hinta**-kentät jätetään tyhjiksi. Jos **Määrä**- ja **Hinta**-kentät on täytetty, **Summa**-kenttä on vain luku -muotoa, ja se lasketaan kaavasta **(Määrä \*Yksikköhinta) + Vero**. | &nbsp; |

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


[!INCLUDE[footer-include](../includes/footer-banner.md)]
