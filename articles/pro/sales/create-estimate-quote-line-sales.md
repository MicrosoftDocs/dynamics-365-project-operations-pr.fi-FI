---
title: Projektipohjaisen tarjousrivin arviointi
description: Tässä aiheessa on tietoja siitä, miten projektipohjaiselle tarjousriville luodaan arvio.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 65aee7238781ac90f603e57c6d9b0b92cabd6644
ms.sourcegitcommit: f6509f7d50de4d4ebb92c1bf2cfcdf09f17458eb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/06/2020
ms.locfileid: "3966771"
---
# <a name="estimating-a-project-based-quote-line"></a>Projektipohjaisen tarjousrivin arviointi

_**Koskee:** Project Operationsin resurssiin / muuhun kuin resurssiin perustuvia skenaarioita, Lite-käyttöönotto-kaupasta proformalaskutukseen_

Projektipohjaisella tarjousrivillä on tietoja, joiden avulla voidaan arvioida tarjousrivin toimittamiseen liittyvän työn kustannuksia ja mahdollista tuottoa.

Jos haluat arvioida projektipohjaisen tarjousrivin, valitse projektipohjaisellatarjous rivillä **Tarjousrivin tiedot** -väl lehti. Arvio voidaan luoda projektipohjaisella tarjousrivillä kahdella tavalla:

- Luo arvio manuaalisesti suoraan tarjousriville tarjousrivin tietojen avulla 
- Luo projekti ja projektisuunnitelma ja liitä sitten projekti ja tehtävät projektiin tarjousriville. Prosessi, jossa projektisuunnitelman arviot tuodaan tarjousriville antamiesi tietojen perusteella, otetaan käyttöön.

## <a name="create-estimates-directly-on-a-project-based-quote-line"></a>Arvioiden luonti suoraan projektipohjaiselle tarjousriville

Jos haluat luoda arvion projektipohjaiselle tarjousriville, valitse **Tarjousrivin tiedot** -välilehti. Tässä välilehdessä luotavaan rivinimikkeeseen tulee yhteenveto tämän tarjousrivin tarjotusta arvosta. 

Jos haluat luoda tarjousrivin tiedot, valitse **Tarjousrivin tiedot** -aliruudukossa **+ Uusi tarjousrivin tieto**. Pikaluonti-liukuruutu avautuu. Seuraavat kentät **Tarjousrivi**-lomakkeessa:

| **Kenttä** | **Sijainti** | **Relevanssi, tarkoitus ja opastus** | **Loppupään vaikutus** |
| --- | --- | --- | --- |
| Kuvaus | Pikaluonti | Tietyn arvion kuvaus. | Tämän kentän oletusarvona on kustannukseen liittyvä tarjousrivin tieto, joka luodaan automaattisesti. |
| Tapahtumaluokka | Pikaluonti | Tämä avattava luettelo sisältää projektipohjaisen tarjous rivin **Yleiset**-välilehteen sisältyvät tapahtumaluokat.  | Tämän kentän oletusarvona on kustannukseen liittyvä tarjousrivin tieto, joka luodaan automaattisesti. |
| Rooli | Pikaluonti | Henkilö, joka suorittaa tämän työn tai aiheuttaa tämän kulun. | Tämän kentän oletusarvona on kustannukseen liittyvä tarjousrivin tieto, joka luodaan automaattisesti. |
| Luokka | Pikaluonti | Työn tai kulun luokka. | Tämän kentän oletusarvona on kustannukseen liittyvä tarjousrivin tieto, joka luodaan automaattisesti. |
| Aloituspäivämäärä | Pikaluonti | Työn alkamispäivämäärä. | Tämän kentän oletusarvona on kustannukseen liittyvä tarjousrivin tieto, joka luodaan automaattisesti. |
| Päättymispäivämäärä | Pikaluonti | Työn päättymispäivämäärä. | Tämän kentän oletusarvona on kustannukseen liittyvä tarjousrivin tieto, joka luodaan automaattisesti. |
| Resursointiyksikkö | Pikaluonti | Resursointiyksikkö, jolle tämä kustannus aiheutuu, ja joka tarjoaa resurssin työhön. | Tämän kentän oletusarvona on kustannukseen liittyvä tarjousrivin tieto, joka luodaan automaattisesti. Tätä kenttää käytetään myös kustannushinnan haussa. |
| Yksikön aikataulutus | Pikaluonti | Työn tai kulun yksikköryhmä. Yksiköt kuuluvat yksikköaikatauluun tai yksiköiden ryhmään. Esimerkiksi mailit ja kilometrit ovat yksiköitä, jotka kuuluvat etäisyyttä kuvaavien yksiköiden ryhmään. | Tämän kentän oletusarvona on kustannukseen liittyvä tarjousrivin tieto, joka luodaan automaattisesti. |
| Yksikkö | Pikaluonti | Työn tai kulun yksikkö. | Tämän kentän oletusarvona on kustannukseen liittyvä tarjousrivin tieto, joka luodaan automaattisesti. |
| Määrä | Pikaluonti | Työn tai kulun määrä | Tämän kentän oletusarvona on kustannukseen liittyvä tarjousrivin tieto, joka luodaan automaattisesti. |
| Yksikköhinta | Pikaluonti | Työn suorittavan roolin laskutushinta tai kululuokan myyntihinta. Tämän kentän oletusarvona on aikaperusteinen roolin ja resursointiyksikön yhdistelmä projektihinnastossa, joka on voimassa alkamispäivänä. Kulujen osalta tämä kenttä on oletusarvon mukaan projektihinnaston tapahtumaluokalle määritetty hinta, joka on voimassa alkamispäivänä. Jos tapahtumaluokan hinnoittelutapa ei ole hinta yksikköä kohden, oletusarvoa ei ole, ja tämä kenttä jätetään tyhjäksi. | Työn suorittavan roolin kustannushinta tai kululuokan yksikkökohtainen kustannus. Tämän kentän oletusarvona on aikaperusteinen roolin ja resursointiyksikön yhdistelmä sopimusyksikön hinta tarjouksen hinnastossa, joka on voimassa alkamispäivänä. Kulujen osalta tämä kenttä on oletusarvon mukaan sopimusyksikön kustannushinnastossa tapahtumaluokalle määritetty hinta, joka on voimassa alkamispäivänä. Jos tapahtumaluokan hinnoittelutapa ei ole hinta yksikköä kohden, oletusarvoa ei ole, ja tämä kenttä jätetään tyhjäksi. |
| Arvioitu vero | Pikaluonti | Voit syöttää tämän työn tai kulun arvioidun veron manuaalisesti. | Tämä kenttä ei vaikuta loppupään prosessiin. |
| Summa | Pikaluonti | Tähän kenttään voi syöttää tietoja manuaalisesti, jos **Määrä**- ja **Hinta**-kentät jätetään tyhjiksi. Jos nämä kentät eivät ole tyhjiä, tämä kenttä muuttuu vain luku -kentäksi, ja se lasketaan seuraavasti: (määrä\*yksikköhinta) + vero. | Tämä kenttä ei vaikuta loppupään prosessiin. |

## <a name="update-prices-on-quote-line-details"></a>Hintojen päivittäminen tarjousrivin tiedoissa

Jos olet muuttanut tarjoukseen liitetyn projektihinnaston hintoja tai sopimusyksikön kustannushinnastoa, voit valita **Tarjous**-sivulla **Laske uudelleen**, jos haluat päivittää yksittäisten tarjousrivin tietojen hinnat tämän muutoksen mukaisiksi. Kun valitset **Laske uudelleen**, näkyviin tulee varoitus, joka ilmoittaa, että tarjouksen kaikkien tarjousrivien tiedot palautetaan. Valitse **Kyllä**, jos haluat päivittää sekä myynti- että kustannustarjousrivin tietojen hinnat.

## <a name="access-quote-line-details-for-cost"></a>Kustannuksen tarjousrivin tietojen käyttäminen

Valitse **Tarjousrivin tiedot** -väli lehdessä ruudukon rivi, jotta aliruudukon työkalurivillä voidaan ottaa käyttöön joitakin toimintoja. Aliruudukon työkalurivin ensimmäinen toiminto, kun tarjousrivin tieto valitaan, on **Avaa kustannuksen tiedot**. Valitsemalla **Avaa kustannuksen tiedot** saat näkyviin kyseisen tarjousrivin liittyvän kustannushinnan ja määrän.

> [!NOTE]
> Resursointiyksikön, määrän, päivämäärien, roolien tai luokkien arvojen muuttaminen tarjousrivin kustannustiedoissa muuttaa myynnin tarjousrivin tietojen vastaavat arvot.
## <a name="currency-on-quote-line-details-for-cost-and-sales"></a>Tarjousrivin tietojen valuutta kustannuksille ja myynnille

Tarjousrivin tietojen valuutta myynnille tulee oletuksena projektihinnastosta, joka on voimassa tarjousrivin tietojen alkamispäivänä.

Tarjousrivin tietojen valuutta kustannukselle tulee oletuksena tarjouksen sopimusyksikön hinnastosta, joka on voimassa ksutannuksen tarjousrivin tietojen alkamispäivänä.

Kannattavuuslaskelmat muuntavat tarjousrivin tiedot kustannukselle ja myynnille ympäristön perusvaluuttaan ja ilmoittavat tarjouksen yleisen arvioidun katteen.

Tämä voi johtaa valuutan pyöristysvirheisiin ja katteen muuttumiseen, koska valuuttakursseista puuttuu voimassaolopäivät. Käytä näitä laskelmia projektitarjouksissa vain arvioina eikä toteutuneena lakisääteisenä tai muuna raportina, joka edellyttää suurempaa pyöristyksen tarkkuutta ja tietoisuutta valuuttakurssien voimassolon päivämääristä.
