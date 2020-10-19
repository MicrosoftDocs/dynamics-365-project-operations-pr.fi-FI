---
title: Projektin seurannan yleiskatsaus
description: Tässä aiheessa on tietoja siitä, miten projektin edistymistä ja kustannusten toteutumista voidaan seurata.
author: ruhercul
manager: AnnBe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: c998addbbdbbea8fe69c95f65e58a24146f394c8
ms.sourcegitcommit: 56c42d7f5995a674426a1c2a81bae897dceb391c
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/01/2020
ms.locfileid: "3907359"
---
# <a name="project-tracking-overview"></a>Projektin seurannan yleiskatsaus

_**Koskee:** Project Operationsin resurssiin / muuhun kuin resurssiin perustuvia skenaarioita, Lite-käyttöönotto-kaupasta proformalaskutukseen_

Tarve seurata aikataulun edistymistä vaihtelee toimialoittain. Joillakin toimialoilla seurataan yksityiskohtaisella tasolla, kun taas muilla toimialoilla seurataan korkeammalla tasolla. Tässä aiheessa kerrotaan, miten voit aikatauluttaa oman organisaatiosi tarpeiden mukaan.

## <a name="effort-tracking-view"></a>Työmäärän seurantanäkymä

**Työmäärän seuranta**  -näkymä seuraa aikataulun tehtävien edistymistä vertaamalla tehtävään ajoitettua todellista työmäärää tehtävän suunniteltuun työmäärään (tunteihin). Dynamics 365 Project Operations laskee seurantamittarit seuraavien kaavojen avulla:

- **Edistymisprosentti**: Tähän päivämäärään saakka käytetty työmäärä ÷ Arvio valmistumisen hetkellä (EAC) 
- **Valmistumisarvio (ETC)**: Suunniteltu työmäärä – Tähän päivämäärään saakka käytetty työmäärä 
- **EAC**: Jäljellä oleva työmäärä + Tähän päivämäärään saakka käytetty työmäärä 
- **Ennustettu työmäärän varianssi**: Suunniteltu työmäärä – EAC

Project Operations näyttää tehtävän työmäärän varianssin ennusteen. Jos valmistumisen kustannusarvio on suunniteltua työmäärää suurempi, tehtävän ennustetaan vaativan enemmän aikaa kuin alun perin oli suunniteltu, ja se on perässä aikataulusta. Jos valmistumisen kustannusarvio on suunniteltua työmäärää pienempi, tehtävän ennustetaan vaativan vähemmän aikaa kuin alun perin oli suunniteltu, ja se on edellä aikataulua.

## <a name="reprojecting-effort"></a>Työmäärän uudelleenprojisoiminen

Projektipäälliköt usein muuttavat tehtävän alkuperäisiä arvioita. Projektin uudelleenprojisoinnit ovat projektipäällikön arvioita, joissa otetaan huomioon projektin tämänhetkinen tila. Emme kuitenkaan suosittele, että projektipäälliköt muuttavat perustason numeroita. Tämä siksi, koska projektin perusaikataulu on projektin aikataulun ja kustannusarvioiden virallinen lähde, ja projektin kaikki sidosryhmät ovat hyväksyneet sen.

Projektipäällikkö voi projisoida tehtävien työmäärää uudelleen seuraavilla kahdella tavalla:

- Korvaa oletusarvoinen ETC uudella arviolla tehtävän todellisesta jäljellä olevasta työstä. 
- Korvaa oletusarvoinen edistymisprosentti uudella arviolla tehtävän todellisesta edistymisestä.

Kukin näistä lähestymistavoista aiheuttaa tehtävän ETC:n, EAC:n, edistymisprosentin ja ennustetun työmäärän varianssin uudelleenlaskennan. Myös yhteenvetotehtävien EAC, ETC ja edistymisprosentti lasketaan uudelleen, ja uusi työmäärän varianssin arvo tuotetaan.

## <a name="reprojection-of-effort-on-summary-tasks"></a>Yhteenvetotehtävien työmäärän uudelleenprojisointi

Yhteenvetotehtävien tai säiliötehtävien työmäärä voidaan projisoida uudelleen. Riippumatta siitä, uudelleenprojisoiko käyttäjä käyttäen yhteenvetotehtävien jäljellä olevaa työmäärää vai edistymisprosenttia, seuraava laskentajoukko aloitetaan:

- EAC, ETC ja tehtävän edistymisprosentti lasketaan.
- Uusi EAC jaetaan alitehtäviin samassa suhteessa kuin alkuperäinen EAC oli tehtävässä.
- Jokaisen yksittäisen tehtävän valmistumisen kustannusarvio lasketaan lehtisolmutehtäviin asti. 
- Alitehtävien, joihin vaikutus ulottuu lehtisolmuissa, ETC ja edistymisprosentti lasketaan uudelleen EAC:n arvoon perustuen. Tuloksena on uusi projektio tehtävän työmäärän varianssista. 
- Yhteenvetotehtävien EAC:t lasketaan uudelleen aina juurisolmuun asti.

### <a name="cost-tracking-view"></a>Kustannusten seurannan näkymä 

**Kustannusten seuranta** -näkymä vertaa tehtävän toteutuneita kustannuksia tehtävälle suunniteltuihin kustannuksiin. 

> [!NOTE]
> Tämä näkymä näyttää vain työvoimakustannukset, eikä se sisällä kuluarvioiden kustannuksia. Project Operations laskee seurantamittarit seuraavien kaavojen avulla:

- **Toteutuneiden kustannusten prosenttiosuus**: Toteutuneet kustannukset tähän päivämäärään asti ÷ Arvioidut kustannukset valmistuessa
- **Kustannukset valmistuessa (CTC)** = Suunnitellut kustannukset – Tähän päivämäärään saakka toteutuneet kustannukset
- **Valmistumisen kustannusarvio**: jäljellä oleva kustannus + toteutunut kustannus kuluvaan päivään saakka
- **Arvioitujen kustannusten varianssi**: Suunnitellut kustannukset – EAC

Kustannusten varianssin ennuste näytetään tehtävässä. Jos EAC on suunniteltuja kustannuksia enemmän, tehtävän ennustetaan maksavan enemmän kuin alunperin oli suunniteltu. Siksi se on suuntautunut budjetin ylittämiseen. Jos EAC on suunniteltuja kustannuksia vähemmän, tehtävän ennustetaan maksavan vähemmän kuin alunperin oli suunniteltu. Siksi se on suuntautunut budjetin alittamiseen.

## <a name="project-managers-reprojection-of-cost"></a>Projektipäällikön kustannusten uudelleenprojektio

Kun työmäärä projisoidaan uudelleen, kustannukset valmistuessa, valmistumisen kustannusarvio, kustannusten toteutumisprosentti ja ennustettu kustannusten varianssi lasketaan kaikki uudelleen **Kustannusten seuranta** -näkymässä.

## <a name="project-status-summary"></a>Projektin tilan yhteenveto

Seurantatiedot **Työmäärän seuranta**- ja **Kustannusten seuranta** -näkymissä näyttävät edistymisen ja toteutuneet kustannukset projektin juurisolmun, yhteenvetotehtävien ja lehtisolmujen tasoilla. **Tila**-osio **Projektikohde**-sivulla näyttää yhteenvedon projektitason tilasta.

## <a name="status-summary-fields"></a>Tilan yhteenvetokentät

**Projektin kokonaistila** -kenttä on muokattava kenttä, joka näyttää projektin kokonaistilan. Se käyttää värikoodausta, kuten vihreää, keltaista ja punaista, osoittamaan lisääntyvää riskiä. **Kommentit** -kentän avulla projektipäällikkö voi syöttää tilaan liittyviä kommentteja. **Tila päivitetty** -kenttää ei voi muokata, ja sen arvo on aik leima, joka ilmaisee, milloin tila on viimeksi päivitetty.

**Aikataulun tehokkuus** - ja **Kustannustehokkuus**-kentät määritetään seurantapäivänä. Kun aikataulun ja kustannusten varianssi juurisolmussa **Työmäärän seuranta** -näkymässä ovat positiivisia, voit asettaa näiden kenttien arvoksi **Edellä**. Kun pääsolmun aikataulun ja kustasten varianssi juurisolmussa on negatiivinen, voit määrittää niiden arvoksi **Jäljessä**.
