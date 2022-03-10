---
title: Projektin tarjousrivin arviointi
description: Tässä aiheessa on tietoja arvion luomisesta projektin tarjousrivillä.
author: rumant
ms.date: 04/01/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 84283ac055aea802fadbd6814ea65a6d3dc01d29e1e3c6290ef11f72f6a75692
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/06/2021
ms.locfileid: "7003947"
---
# <a name="estimate-a-project-quote-line"></a>Projektin tarjousrivin arviointi

_**Käytetään:** Project Operationsin resursseihin ja ei-varastoitaviin perustuvissa skenaarioissa_

Projektipohjaisella tarjousrivillä on tietoja, joiden avulla voidaan arvioida tarjousrivin toimittamiseen liittyvän työn kustannuksia ja mahdollista tuottoa.

Jos haluat arvioida projektipohjaisen tarjousrivin, valitse **Tarjousrivin tiedot** -välilehti tarjousriviltä. Arvion voi luoda projektipohjaiselle tarjousriville kahdella tavalla:

   - Luo arvio manuaalisesti suoraan tarjousriville tarjousrivin tietojen avulla. 
   - Luo projekti ja projektisuunnitelma ja liitä sitten projekti ja tehtävät projektiin tarjousriville. Prosessi, jossa projektisuunnitelman arviot tuodaan tarjousriville antamiesi tietojen perusteella, otetaan käyttöön.

## <a name="create-estimates-directly-on-a-project-based-quote-line"></a>Arvioiden luonti suoraan projektipohjaiselle tarjousriville

Arvioiden luonti suoraan projektipohjaisella tarjousrivillä tapahtuu seuraavia vaiheita seuraamalla:

1. Jos haluat luoda arvion projektipohjaiselle tarjousriville, valitse **Tarjousrivin tiedot** -välilehti. Tässä välilehdessä luotavaan rivinimikkeeseen tulee yhteenveto tämän tarjousrivin tarjotusta arvosta. 
2. Luo tarjousrivin tiedot valitsemalla **Uusi tarjousrivin tieto** **Tarjousrivin tiedot** -aliruudukossa. Pikaluonti-liukuruutu avautuu. Seuraavat **Tarjousrivi**-sivun kentät.

| **Kenttä** | **Sijainti** | **Kuvaus** | **Loppupään vaikutus** |
| --- | --- | --- | --- |
| Kuvaus | Pikaluonti | Tietyn arvion kuvaus. | Tämä arvo saa oletusarvon, joka on automaattisesti luotu liittyvä tarjousrivin kustannustieto. |
| Tapahtumaluokka | Pikaluonti | Tämä avattava luettelo sisältää projektipohjaisen tarjous rivin **Yleiset**-välilehteen sisältyvät tapahtumaluokat.  | Tämä arvo saa oletusarvon, joka on automaattisesti luotu liittyvä tarjousrivin kustannustieto. |
| Valitse tuote | Pikaluonti | Koskee, kun tapahtumaluokka on **Materiaali**. Voit valinnaisesti määrittää, että tämä arviorivi on **Aiemmin luodulle** (luettelon) tuotteelle tai **Käsin lisättävälle** tuotteelle. | Tämä arvo saa oletusarvon, joka on automaattisesti luotu liittyvä tarjousrivin kustannustieto. |
| Tuote | Pikaluonti | Tuoteluettelon tuotteen tunnus. Tämä kenttä on käytössä vain, kun valitset **Aiemmin luotu** **Valitse tuote** -kentässä. Tunnuksen avulla haetaan myyntihinta tarjouksen projektihinnastosta. | Tämä arvo saa oletusarvon, joka on automaattisesti luotu liittyvä tarjousrivin kustannustieto. |
| Käsin lisätty tuote | Pikaluonti | Tekstiruutu, johon kirjoitetaan tuotteen nimessä. Tämä kenttä on käytössä vain, kun valitset **Käsin lisättävä** **Valitse tuote** -kentässä.| Tämä arvo saa oletusarvon, joka on automaattisesti luotu liittyvä tarjousrivin kustannustieto. |
| Rooli | Pikaluonti | Sen henkilön rooli, joka suorittaa nämä työt tai aiheuttaa tämän kulun. | Tämä arvo saa oletusarvon, joka on automaattisesti luotu liittyvä tarjousrivin kustannustieto. |
| Luokka | Pikaluonti | Työn tai kulun luokka. | Tämä arvo saa oletusarvon, joka on automaattisesti luotu liittyvä tarjousrivin kustannustieto. |
| Aloituspäivämäärä | Pikaluonti | Työn alkamispäivämäärä. | Tämä kenttä saa oletusarvon, joka on automaattisesti luotu tarjousrivin kustannustieto. |
| Päättymispäivämäärä | Pikaluonti | Työn päättymispäivämäärä. | Tämä kenttä saa oletusarvon, joka on automaattisesti luotu tarjousrivin kustannustieto. |
| Resursoiva yritys | Pikaluonti | Resursoiva yritys tai kustannuksen aiheuttava yritys ja tarjoaa resurssit sen suhteen tehtävään työhön. | Arvo saa oletusarvon, joka on automaattisesti luotu liittyvä tarjousrivin kustannuksen tieto ja jota käytetään kustannushinnan hakemiseen. |
| Resursointiyksikkö | Pikaluonti | Resursoiva yksikkö, joka aiheittaa tämän kustannuksen ja tarjoaa resurssit sen suhteen tehtävään työhön. | Tämä arvo saa oletusarvon, joka on automaattisesti luotu liittyvä tarjousrivin kustannuksen tieto ja jota käytetään kustannushinnan hakemiseen. |
| Yksikön aikataulutus | Pikaluonti | Työn, tuotteen tai kulun yksikköryhmä. Yksiköt kuuluvat yksikköaikatauluun tai yksiköiden ryhmään. Esimerkiksi mailit ja kilometrit ovat etäisyyttä kuvaavaan yksikköryhmään kuuluvia yksiköitä. | Tämä arvo saa oletusarvon, joka on automaattisesti luotu liittyvä tarjousrivin kustannustieto. |
| Yksikkö | Pikaluonti | Työn, tuotteen tai kulun yksikkö. | Tämä arvo saa oletusarvon, joka on automaattisesti luotu liittyvä tarjousrivin kustannustieto. |
| Määrä | Pikaluonti | Työn, tuotteen tai kulun määrä. | Tämä arvo saa oletusarvon, joka on automaattisesti luotu liittyvä tarjousrivin kustannustieto. |
| Yksikköhinta | Pikaluonti |Työn suorittavan roolin laskutushinta, tuotteen yksikkökustannus tai tuote- tai kululuokan myyntihinta. **Ajan** oletusarvo perustuu alkamispäivänä voimassa olevassa projektihinnastossa olevien roolihintarivien hinnoitteludimensioiden arvojen yhdistelmiin. **Kulujen** oletusarvo on sen projektihinnaston tapahtumaluokan hintamääritys, joka on voimassa alkamispäivänä. Jos tapahtumaluokan hinnoittelutapa ei ole hinta yksikköä kohden, oletusarvoa ei ole, ja tämä kenttä jätetään tyhjäksi. Tämän kentän oletusarvo tuotteille perustuu **Hinnaston nimike** -riviin projektihinnastossa, joka on voimassa alkamispäivänä.| Työn suorittavan roolin kustannushinta, kululuokan yksikkökustannus tai tuotteen yksikkökustannus. **Ajan** oletusarvo perustuu alkamispäivänä voimassa olevaan sopimusyksikköön liitetyssä projektihinnastossa olevien roolihintarivien hinnoitteludimensioiden arvojen yhdistelmiin. Kulujen oletusarvo perustuun alkamispäivänä voimassa olevaan sopimusyksikköön yhdistetyssä projektihinnastossa olevan kustannushinnaston luokan hintarivin hinnoittelumäärityksiin. Jos tapahtumaluokan hinnoittelutapa ei ole yksikköhinta, oletusarvoa ei ole, ja tämä kenttä jätetään tyhjäksi. Tämän kentän oletusarvo tuotteille perustuu **Hinnaston nimike** -riviin kustannushinnastossa, joka liittyy sopimusyksikköön, joka on voimassa alkamispäivänä.|
| Arvioitu vero | Pikaluonti | Voit syöttää tämän työn tai kulun arvioidun veron manuaalisesti. | Tämä kenttä ei vaikuta loppupään prosessiin. |
| Summa | Pikaluonti | Tähän kenttään voi syöttää tietoja manuaalisesti, jos **Määrä**- ja **Hinta**-kentät jätetään tyhjiksi. Jos nämä kentät eivät ole tyhjiä, tämä kenttä muuttuu vain luku -kentäksi, ja se lasketaan seuraavasti: (Määrä \* Yksikköhinta) + Vero. | Tämä kenttä ei vaikuta loppupään prosessiin. |

## <a name="update-prices-on-quote-line-details"></a>Hintojen päivittäminen tarjousrivin tiedoissa

Jos olet muuttanut tarjoukseen liitetyn projektihinnaston hintoja tai sopimusyksikön kustannushinnastoa, voit valita **Tarjous**-sivulla **Laske uudelleen**, jos haluat päivittää yksittäisten tarjousrivin tietojen hinnat tämän muutoksen mukaisiksi. Kun valitset **Laske uudelleen**, näkyviin tulee varoitus, joka ilmoittaa, että kaikkien tarjouksen tarjousrivien hinnat tarjousriveillä nollataan. Valitse **Kyllä**, jos haluat päivittää sekä myynti- että kustannustarjousrivin tietojen hinnat.

## <a name="access-quote-line-details-for-cost"></a>Kustannuksen tarjousrivin tietojen käyttäminen

Tarjousrivin kustannustietoihin päästään seuraavia vaiheita seuraamalla:

1. Valitse **Tarjousrivin tiedot** -välilehdellä ruudukon rivi ottaaksesi aliruudukon työkalurivin toiminnot käyttöön. 
2. Valitsemalla **Avaa kustannuksen tiedot** saat näkyviin kyseisen tarjousrivin liittyvän kustannushinnan ja määrän.

> [!NOTE]
> Resursointiyksikön, määrän, päivämäärien, roolien tai luokkien arvojen muuttaminen tarjousrivin kustannustiedoissa muuttaa myynnin tarjousrivin tietojen vastaavat arvot.

## <a name="currency-on-quote-line-details-for-cost-and-sales"></a>Tarjousrivin tietojen valuutta kustannuksille ja myynnille

Tarjousrivin tietojen valuutta myynneille saa oletusarvon projektihinnastosta, joka on voimassa tarjousrivin tiedon alkamispäivänä.

Tarjousrivin tietojen valuutta kustannuksille saa oletusarvon tarjousrivin kustannustiedon alkamispäivänä voimassa olevan tarjouksen sopimusyksikön projektihinnastosta.

> [!NOTE]
> Kannattavuuslaskelmat muuntavat tarjousrivin tiedot kustannukselle ja myynnille ympäristön perusvaluuttaan ja ilmoittavat tarjouksen yleisen arvioidun katteen. Valuutan pyöristysvirheitä ja muuttuneita katteita voi esiintyä, koska vaihtokurssien voimassaolopäivä puuttuu. Näitä laskelmia voi käyttää vain projektitarjouksissa, koska ne ovat pyöristyksiä, ja ne eivät ole varsinaisia lakimääräistä tai muuta raportointia, joka edellyttää valuuttakurssien pyöristystarkkuutta ja päivämäärävaikuttavuuden tuntemusta.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
