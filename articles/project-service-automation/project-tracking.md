---
title: Projektin edistyminen ja toteutuneet kustannukset
description: Tässä aiheessa on tietoja siitä, miten projektin edistymistä ja kustannusten toteutumista voidaan seurata.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: 0d742164-5469-421d-8917-63160a81f651
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 8aa5814938129f30885d8161a7c86197ab013364
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/24/2020
ms.locfileid: "3751233"
---
# <a name="project-progress-and-cost-consumption"></a>Projektin edistyminen ja toteutuneet kustannukset

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Tarve seurata aikataulun edistymistä vaihtelee toimialoittain. Joillakin toimialoilla seurataan yksityiskohtaisella tasolla, kun taas muilla toimi loilla seurataan korkeammalla tasolla. Tässä aiheessa kerrotaan, miten voit aikatauluttaa oman organisaatiosi tarpeiden mukaan.

## <a name="effort-tracking-view"></a>Työmäärän seurantanäkymä

**Työn seuranta** -näkymä seuraa tehtävien edistymistä aikataulussa. Se vertailee tehtävään käytettyjä toteutuneita työtunteja tehtävälle suunniteltuihin työtunteihin. PSA laskee seurantamittarit seuraavien kaavojen avulla:

- Edistymisprosentti = Todellinen tähän päivämäärään saakka käytetty työmäärä ÷ Tehtävälle suunniteltu työmäärä 
- Valmistumisarvio (ETC) = Suunniteltu työmäärä – Tähän päivämäärään saakka käytetty työmäärä 
- Arvio valmistumisen hetkellä (EAC) = Jäljellä oleva työmäärä + Tähän päivämäärään saakka käytetty työmäärä 
- Ennustettu työmäärän varianssi = Suunniteltu työmäärä – EAC

PSA näyttää tehtävän työmäärän varianssin ennusteen. Jos EAC on suunniteltua työmäärää enemmän, tehtävän ennustetaan vaativan enemmän aikaa kuin alunperin oli suunniteltu. Siksi se on myöhässä. Jos EAC on suunniteltua työmäärää vähemmän, tehtävän ennustetaan vaativan vähemmän aikaa kuin alunperin oli suunniteltu. Siksi se on edellä aikataulusta.

## <a name="re-projecting-effort"></a>Työmäärän uudelleenprojisoiminen

On tavallista, että projektipäällikkö muuttaa tehtävän alkuperäisiä arvioita. Projektin ennusteet ovat projektipäällikön arvioita, joissa otetaan huomioon projektin tämänhetkinen tila. Microsoft ei suosittele perusaikataulun numeroiden muuttamista, koska projektin perusaikataulu on projektin aikataulun ja kustannusarvioiden virallinen lähde, ja projektin kaikki sidosryhmät ovat hyväksyneet sen.

Projektipäällikkö voi projisoida tehtävien työmäärää uudelleen seuraavilla kahdella tavalla:

- Korvaa oletusarvoinen ETC uudella arviolla tehtävän todellisesta jäljellä olevasta työstä. 
- Korvaa oletusarvoinen edistymisprosentti uudella arviolla tehtävän todellisesta edistymisestä.

Kukin näistä lähestymistavoista aiheuttaa tehtävän ETC:n, EAC:n ja edistymisprosentin sekä ennustetun työmäärän varianssin uudelleenlaskennan. Myös yhteenvetotehtävien EAC, ETC ja edistymisprosentti lasketaan uudelleen, ja uusi työmäärän varianssin arvo tuotetaan.

## <a name="re-projection-of-effort-on-summary-tasks"></a>Yhteenvetotehtävien työmäärän uudelleenprojisointi

Yhteenvetotehtävien tai säiliötehtävien työmäärä voidaan projisoida uudelleen. Riippumatta siitä, uudelleenprojisoiko käyttäjä käyttäen yhteenvetotehtävien jäljellä olevaa työmäärää vai edistymisprosenttia, seuraava laskentajoukko aloitetaan:

- EAC, ETC ja tehtävän edistymisprosentti lasketaan.
- Uusi EAC jaetaan alitehtäviin samassa suhteessa kuin alkuperäinen EAC oli tehtävässä.
- Jokaisen yksittäisen tehtävän EAC aina lehtisolmutehtäviin asti lasketaan. 
- Alitehtävien, joihin vaikutus ulottuu lehtisolmuissa, ETC ja edistymisprosentti lasketaan uudelleen EAC:n arvoon perustuen. Tuloksena on uusi projektio tehtävän työmäärän varianssista. 
- Yhteenvetotehtävien EAC:t lasketaan uudelleen aina juurisolmuun asti.

### <a name="cost-tracking-view"></a>Kustannusten seurannan näkymä 

**Kustannusten seuranta** -näkymä vertaa tehtävän toteutuneita kustannuksia tehtävälle suunniteltuihin kustannuksiin. 

> [!NOTE]
> Tämä näkymä näyttää vain työvoimakustannukset, eikä se sisällä kuluarvioiden kustannuksia. 

PSA laskee seurantamittarit seuraavien kaavojen avulla:

- Toteutuneiden kustannusten prosenttiosuus = Toteutuneet kustannukset tähän päivämäärään asti ÷ Tehtävän suunnitellut kustannukset
- Kustannukset valmistuessa (CTC) = Suunnitellut kustannukset – Tähän päivämäärään saakka toteutuneet kustannukset
- EAC = CTC + Toteutuneet kustannukset tähän päivämäärään saakka
- Arvioitujen kustannusten varianssi = Suunnitellut kustannukset – EAC

Kustannusten varianssin ennuste näytetään tehtävässä. Jos EAC on suunniteltuja kustannuksia enemmän, tehtävän ennustetaan maksavan enemmän kuin alunperin oli suunniteltu. Siksi se on suuntautunut budjetin ylittämiseen. Jos EAC on suunniteltuja kustannuksia vähemmän, tehtävän ennustetaan maksavan vähemmän kuin alunperin oli suunniteltu. Siksi se on suuntautunut budjetin alittamiseen.

## <a name="project-managers-re-projection-of-cost"></a>Projektipäällikön kustannusten uudelleenprojektio

Kun työmäärä projektoidaan uudelleen, CTC, EAC, kustannusten toteutumisprosentti ja ennustettu kustannusten varianssi lasketaan kaikki uudelleen **Kustannusten seuranta** -näkymässä.

## <a name="project-status-summary"></a>Projektin tilan yhteenveto

Seurantatiedot **Työmäärän seuranta**- ja **Kustannusten seuranta** -näkymissä näyttävät edistymisen ja toteutuneet kustannukset projektin juurisolmun, yhteenvetotehtävien ja lehtisolmujen tasoilla. **Tila**-osio **Projektikohde**-sivulla näyttää yhteenvedon projektitason tilasta.

## <a name="status-summary-fields"></a>Tilan yhteenvetokentät

**Projektin kokonaistila** -kenttä on muokattava kenttä, joka näyttää projektin kokonaistilan. Se käyttää värikoodausta, kuten vihreää, keltaista ja punaista, osoittamaan lisääntyvää riskiä. **Kommentit** -kentän avulla projektipäällikkö voi syöttää tilaan liittyviä kommentteja. **Tila päivitetty** -kenttää ei voi muokata, ja sen arvo on aik leima, joka ilmaisee, milloin tila on viimeksi päivitetty.

**Aikataulun tehokkuus** - ja **Kustannustehokkuus**-kentät määritetään seurantapäivänä. Kun aikataulun ja kustannusten varianssi juurisolmussa **Työmäärän seuranta** -näkymässä ovat positiivisia, voit asettaa näiden kenttien arvoksi **Edellä**. Kun pääsolmun aikataulun ja kustasten varianssi juurisolmussa on negatiivinen, voit määrittää niiden arvoksi **Jäljessä**.
