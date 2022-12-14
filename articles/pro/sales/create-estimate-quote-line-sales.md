---
title: Projektin tarjousrivin arviointi
description: Tässä artikkelissa on tietoja arvion luomisesta projektin tarjousrivillä.
author: rumant
ms.date: 04/01/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: bac3a3fa2d14c857edfb469a005406c346c8dbf6
ms.sourcegitcommit: e0cbbe7c6f03d4978134405cf04bd8bc1d019f65
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/05/2022
ms.locfileid: "9825983"
---
# <a name="estimate-a-project-quote-line"></a>Projektin tarjousrivin arviointi

_**Koskee:** Lite-käyttöönotto - kaupasta proformalaskutukseen, Project Operationsin resurssiin/ei-varastointiin perustuvia skenaarioita_

Projektipohjaisella tarjousrivillä on tietoja, joiden avulla voidaan arvioida tarjousrivin toimittamiseen liittyvän työn kustannuksia ja mahdollista tuottoa.

Jos haluat arvioida projektipohjaisen tarjousrivin, valitse projektipohjaisellatarjous rivillä **Tarjousrivin tiedot** -väl lehti. Arvio voidaan luoda projektipohjaisella tarjousrivillä kahdella tavalla:

- Luo arvio manuaalisesti suoraan tarjousriville tarjousrivin tietojen avulla. 
- Luo projekti ja projektisuunnitelma ja liitä sitten projekti ja tehtävät projektiin tarjousriville. Prosessi, jossa projektisuunnitelman arviot tuodaan tarjousriville antamiesi tietojen perusteella, otetaan käyttöön.

## <a name="create-estimates-directly-on-a-project-quote-line"></a>Arvioiden luonti suoraan projektin tarjousriville

Jos haluat luoda arvion projektipohjaiselle tarjousriville, valitse **Tarjousrivin tiedot** -välilehti. Tässä välilehdessä luotavaan rivinimikkeeseen tulee yhteenveto tämän tarjousrivin tarjotusta arvosta. 

Luo tarjousrivin tiedot valitsemalla **Uusi tarjousrivin tieto** **Tarjousrivin tiedot** -aliruudukossa. Pikaluonti-liukuruutu avautuu. Seuraavassa taulukossa on tietoja **Tarjousrivin tiedot** -sivun kentistä ja siitä, miten arvot vaikuttavat toiminnallisuuteen.

| **Kenttä** | **Sijainti** | **Kuvaus** | **Loppupään vaikutus** |
| --- | --- | --- | --- |
| Kuvaus | Pikaluonti | Tietyn arvion kuvaus. | Tämä arvo saa oletusarvon, joka on automaattisesti luotu liittyvä tarjousrivin kustannustieto. |
| Tapahtumaluokka | Pikaluonti | Tämä avattava luettelo sisältää projektipohjaisen tarjousrivin **Yleiset**-välilehteen sisältyvät tapahtumaluokat.  | Tämä arvo saa oletusarvon, joka on automaattisesti luotu liittyvä tarjousrivin kustannustieto. |
| Valitse tuote | Pikaluonti | Koskee, kun tapahtumaluokka on **Materiaali**. Voit valinnaisesti määrittää, että tämä arviorivi on **Aiemmin luodulle** (luettelon) tuotteelle tai **Käsin lisättävälle** tuotteelle. | Tämä arvo saa oletusarvon, joka on automaattisesti luotu liittyvä tarjousrivin kustannustieto. |
| Tuote | Pikaluonti | Tuoteluettelon tuotteen tunnus. Tämä kenttä on käytössä vain, jos valitset **Aiemmin luotu** **Valitse tuote** -kentässä. Tunnuksen avulla haetaan myyntihinta tarjouksen projektihinnastosta. | Tämä arvo saa oletusarvon, joka on automaattisesti luotu liittyvä tarjousrivin kustannustieto. |
| Käsin lisätty tuote | Pikaluonti | Tekstiruutu, johon kirjoitetaan tuotteen nimi. Tämä kenttä on käytössä vain, jos valitset **Käsin lisättävä** **Valitse tuote** -kentässä.| Tämä arvo saa oletusarvon, joka on automaattisesti luotu liittyvä tarjousrivin kustannustieto. |
| Rooli | Pikaluonti | Sen henkilön rooli, joka suorittaa nämä työt tai aiheuttaa tämän kulun. | Tämä arvo saa oletusarvon, joka on automaattisesti luotu liittyvä tarjousrivin kustannustieto. |
| Luokka | Pikaluonti | Työn tai kulun luokka. | Tämä arvo saa oletusarvon, joka on automaattisesti luotu liittyvä tarjousrivin kustannustieto. |
| Aloituspäivämäärä | Pikaluonti | Työn alkamispäivämäärä. | Tämä kenttä saa oletusarvon, joka on automaattisesti luotu tarjousrivin kustannustieto. |
| Päättymispäivämäärä | Pikaluonti | Työn päättymispäivämäärä. | Tämä kenttä saa oletusarvon, joka on automaattisesti luotu tarjousrivin kustannustieto. |
| Resursointiyksikkö | Pikaluonti | Resursoiva yksikkö, joka aiheuttaa tämän kustannuksen ja tarjoaa resurssit sen suhteen tehtävään työhön. | Tämä arvo saa oletusarvon, joka on automaattisesti luotu liittyvä tarjousrivin kustannuksen tieto ja jota käytetään kustannushinnan hakemiseen. |
| Yksikön aikataulutus | Pikaluonti | Työn, tuotteen tai kulun yksikköryhmä. Yksiköt kuuluvat yksikköaikatauluun tai yksiköiden ryhmään. Esimerkiksi mailit ja kilometrit ovat etäisyyttä kuvaavaan yksikköryhmään kuuluvia yksiköitä. | Tämä arvo saa oletusarvon, joka on automaattisesti luotu liittyvä tarjousrivin kustannustieto. |
| Yksikkö | Pikaluonti | Työn, tuotteen tai kulun yksikkö. | Tämä arvo saa oletusarvon, joka on automaattisesti luotu liittyvä tarjousrivin kustannustieto. |
| Määrä | Pikaluonti | Työn, tuotteen tai kulun määrä. | Tämä arvo saa oletusarvon, joka on automaattisesti luotu liittyvä tarjousrivin kustannustieto. |
| Yksikköhinta | Pikaluonti |Työn suorittavan roolin laskutushinta, tuotteen yksikkökustannus tai tuote- tai kululuokan myyntihinta. Tämän kentän oletusarvo on **Aika** perustuen alkamispäivänä voimassa olevassa projektihinnastossa olevien roolihintarivien hinnoitteludimensioiden arvojen yhdistelmiin. **Kulujen** oletusarvo on sen projektihinnaston tapahtumaluokan hintamääritys, joka on voimassa alkamispäivänä. Jos tapahtumaluokan hinnoittelutapa ei ole yksikköhinta, oletusarvoa ei ole, ja tämä kenttä jätetään tyhjäksi. Oletusarvo tuotteille perustuu **Hinnaston nimike** -riviin projektihinnastossa, joka on voimassa alkamispäivänä.| Työn suorittavan roolin kustannushinta, kululuokan yksikkökustannus tai tuotteen yksikkökustannus. Tämän kentän oletusarvo on **Aika** perustuen alkamispäivänä voimassa olevassa projektihinnastossa olevien roolihintarivien hinnoitteludimensioiden arvojen yhdistelmiin. **Kulujen** oletusarvo on sen projektihinnaston tapahtumaluokan hintamääritys, joka on voimassa alkamispäivänä. Jos tapahtumaluokan hinnoittelutapa ei ole yksikköhinta, oletusarvoa ei ole, ja tämä kenttä jätetään tyhjäksi. Oletusarvo tuotteille perustuu **Hinnaston nimike** -riviin projektihinnastossa, joka on voimassa alkamispäivänä.|
| Arvioitu vero | Pikaluonti | Voit syöttää tämän työn tai kulun arvioidun veron manuaalisesti. | Tämä kenttä ei vaikuta loppupään prosessiin. |
| Summa | Pikaluonti | Tähän kenttään voi syöttää tietoja manuaalisesti, jos **Määrä**- ja **Hinta**-kentät jätetään tyhjiksi. Jos nämä kentät eivät ole tyhjiä, tämä kenttä muuttuu vain luku -kentäksi, ja se lasketaan seuraavasti: (Määrä \* Yksikköhinta) + Vero. | Tämä kenttä ei vaikuta loppupään prosessiin. |


## <a name="update-prices-on-quote-line-details"></a>Hintojen päivittäminen tarjousrivin tiedoissa

Jos olet muuttanut hintoja projektihinnastossa, joka liittyy tarjoukseen tai sopimuksen tekevän yksikön kustannushinnastossa, voit valita **Laske uudelleen** sivulla **Tarjous** päivittääksesi yksittäisen tarjousrivin tiedot tämän muutoksen näyttämiseksi. Kun valitset **Laske uudelleen**, näkyviin tulee varoitus, joka ilmoittaa, että kaikkien tarjouksen tarjousrivien hinnat tarjousriveillä nollataan. Valitse **Kyllä**, jos haluat päivittää sekä myynti- että kustannustarjousrivin tietojen hinnat.

## <a name="access-quote-line-details-for-cost"></a>Kustannuksen tarjousrivin tietojen käyttäminen

Valitse **Tarjousrivin tiedot** -välilehden ruudussa rivi, jolloin jotkin aliruudukon työkalurivin toiminnot otetaan käyttöön. Ensimmäinen aliruudukon työkalurivin toiminto tarjousrivin tietoa valittaessa on **Avaa kustannuksen tiedot**. Valitsemalla **Avaa kustannuksen tiedot** saat näkyviin kyseisen tarjousrivin liittyvän kustannushinnan ja määrän.

> [!NOTE]
> Resursointiyksikön, määrän, päivämäärien, roolien tai luokkien arvojen muuttaminen tarjousrivin kustannustiedoissa muuttaa myynnin tarjousrivin tietojen vastaavat arvot.
## <a name="currency-on-quote-line-details-for-cost-and-sales"></a>Tarjousrivin tietojen valuutta kustannuksille ja myynnille

Tarjousrivin tietojen valuutta myynnille tulee oletuksena projektihinnastosta, joka on voimassa tarjousrivin tietojen alkamispäivänä.

Tarjousrivin tietojen valuutta kustannukselle tulee oletuksena tarjouksen sopimusyksikön hinnastosta, joka on voimassa ksutannuksen tarjousrivin tietojen alkamispäivänä.

Kannattavuuslaskelmat muuntavat tarjousrivin tiedot kustannukselle ja myynnille ympäristön perusvaluuttaan ja ilmoittavat tarjouksen yleisen arvioidun katteen.

> [!HUOMAUTUS Valuutan pyöristysvirheitä ja muuttuneita katteita voi esiintyä, koska vaihtokurssien voimassaolopäivä puuttuu. Näitä laskelmia voi käyttää vain projektisopimuksissa, koska ne ovat pyöristyksiä, ja ne eivät ole varsinaisia lakimääräistä tai muuta raportointia, joka edellyttää valuuttakurssien pyöristystarkkuutta ja päivämäärävaikuttavuuden tuntemusta.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
