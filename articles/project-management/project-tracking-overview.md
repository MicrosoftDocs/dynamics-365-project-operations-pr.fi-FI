---
title: Projektin työmäärän seuranta
description: Tässä aiheessa on tietoja siitä, miten projektin työmäärää ja työn edistymistä voidaan seurata.
author: ruhercul
ms.date: 03/22/2021
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.custom: intro-internal
ms.openlocfilehash: 0df357eaf662816107fbc1777ebae030c93bd199756e78a1c3d59155dc64d38f
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/06/2021
ms.locfileid: "6993957"
---
# <a name="project-effort-tracking"></a>Projektin työmäärän seuranta

_**Koskee:** Project Operationsin resurssiin / muuhun kuin resurssiin perustuvia skenaarioita, Lite-käyttöönotto-kaupasta proformalaskutukseen_

Tarve seurata aikataulun edistymistä vaihtelee toimialoittain. Joillakin toimialoilla seurataan yksityiskohtaisella tasolla, kun taas muilla toimialoilla seurataan korkeammalla tasolla. Tässä aiheessa kerrotaan, miten voit aikatauluttaa oman organisaatiosi tarpeiden mukaan.

## <a name="effort-tracking-view"></a>Työmäärän seurantanäkymä

**Työmäärän seuranta**  -näkymä seuraa aikataulun tehtävien edistymistä vertaamalla tehtävään ajoitettua todellista työmäärää tehtävän suunniteltuun työmäärään (tunteihin). Dynamics 365 Project Operations laskee seurantamittarit seuraavien kaavojen avulla:

- **Edistymisprosentti**: Tähän päivämäärään saakka käytetty työmäärä ÷ Arvio valmistumisen hetkellä (EAC) 
- **Jäljellä oleva työmäärä**: Arvioitu työmäärä valmistumishetkellä - Tähän päivämäärään saakka käytetty työmäärä 
- **EAC**: Jäljellä oleva työmäärä + Tähän päivämäärään saakka käytetty työmäärä 
- **Ennustettu työmäärän varianssi**: Suunniteltu työmäärä – EAC

Project Operations näyttää tehtävän työmäärän varianssin ennusteen. Jos valmistumisen kustannusarvio on suunniteltua työmäärää suurempi, tehtävän ennustetaan vaativan enemmän aikaa kuin alun perin oli suunniteltu, ja se on perässä aikataulusta. Jos valmistumisen kustannusarvio on suunniteltua työmäärää pienempi, tehtävän ennustetaan vaativan vähemmän aikaa kuin alun perin oli suunniteltu, ja se on edellä aikataulua.

## <a name="reprojecting-effort-on-leaf-node-tasks"></a>Työmäärän uudelleen ennustaminen lehtisolmujen tehtävissä

Projektipäälliköt usein muuttavat tehtävän alkuperäisiä arvioita. Projektin uudelleenprojisoinnit ovat projektipäällikön arvioita, joissa otetaan huomioon projektin tämänhetkinen tila. Projektipäälliköitä ei kuitenkaan suositella muuttamaan suunniteltuja työmäärälukuja. Tämä johtuu siitä, että projektin suunniteltu työmäärä on projektin aikataulun ja kustannusarvion todennäköinen lähde, ja kaikki projektin sidosryhmät ovat hyväksyneet sen.

Projektipäällikkö voi ennustaa tehtävien työmäärän uudelleen päivittämällä **Jäljellä olevan työmäärän** arvion tehtävässä. Tämä päivitys aiheuttaa tehtävän valmistumisen ajankohdan arvion (EAC) valmistumisprosentin ja ennustetun työmäärän varianssin uudelleenlaskennan. Myös yhteenvetotehtävien EAC, ETC ja edistymisprosentti lasketaan uudelleen, ja uusi työmäärän varianssin arvo tuotetaan.

## <a name="reprojection-of-effort-on-summary-tasks"></a>Yhteenvetotehtävien työmäärän uudelleenprojisointi

Yhteenvetotehtävien tai säiliötehtävien työmäärä voidaan projisoida uudelleen. Projektipäälliköt voivat päivittää yhteenvetotehtävien jäljellä olevan työmäärän. Kun jäljellä oleva työmäärä päivitetään, sovellus käynnistää seuraavat laskutoimitukset:

- EAC ja tehtävän edistymisprosentti lasketaan.
- Uusi EAC jaetaan alitehtäviin samassa suhteessa kuin alkuperäinen EAC oli tehtävässä.
- Jokaisen yksittäisen tehtävän valmistumisen kustannusarvio lasketaan lehtisolmutehtäviin asti. 
- Alitehtävien, joihin vaikutus ulottuu lehtisolmuissa, jäljellä oleva työmäärä ja edistymisprosentti lasketaan uudelleen EAC:n arvoon perustuen. Tuloksena on uusi projektio tehtävän työmäärän varianssista. 
- Yhteenvetotehtävien EAC:t lasketaan uudelleen aina juurisolmuun asti.


## <a name="project-status-summary"></a>Projektin tilan yhteenveto

Seurantatiedot **Työmäärän seuranta**- ja **Kustannusten seuranta** -näkymissä näyttävät edistymisen ja toteutuneet kustannukset projektin juurisolmun, yhteenvetotehtävien ja lehtisolmujen tasoilla. **Tila**-osio **Projektikohde**-sivulla näyttää yhteenvedon projektitason tilasta.

## <a name="status-summary-fields"></a>Tilan yhteenvetokentät

**Projektin kokonaistila** -kenttä on muokattava kenttä, joka näyttää projektin kokonaistilan. Se käyttää värikoodausta, kuten vihreää, keltaista ja punaista, osoittamaan lisääntyvää riskiä. **Kommentit** -kentän avulla projektipäällikkö voi syöttää tilaan liittyviä kommentteja. **Tila päivitetty** -kenttää ei voi muokata, ja sen arvo on aik leima, joka ilmaisee, milloin tila on viimeksi päivitetty.

**Aikataulun tehokkuus** - ja **Kustannustehokkuus**-kentät määritetään seurantapäivänä. Kun aikataulun ja kustannusten varianssi juurisolmussa **Työmäärän seuranta** -näkymässä ovat positiivisia, voit asettaa näiden kenttien arvoksi **Edellä**. Kun pääsolmun aikataulun ja kustasten varianssi juurisolmussa on negatiivinen, voit määrittää niiden arvoksi **Jäljessä**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
