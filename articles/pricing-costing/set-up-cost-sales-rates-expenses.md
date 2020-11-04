---
title: Kulujen kustannus- ja myyntihintojen määrittäminen
description: Tässä aiheessa on tietoja kustannusten ja myyntihintojen määrittämisestä tapahtuma- ja kululuokille.
author: rumant
manager: Annbe
ms.date: 10/13/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: e5a2402a2c1059ff11dbe1a331a028da77958235
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/16/2020
ms.locfileid: "4075267"
---
# <a name="set-up-cost-and-sales-rates-for-expenses"></a>Kulujen kustannus- ja myyntihintojen määrittäminen

_**Koskee:** Project Operationsin resurssiin / muuhun kuin resurssiin perustuvia skenaarioita, Lite-käyttöönotto-kaupasta proformalaskutukseen_

Voit määrittää tapahtumaluokkien kustannus- ja myyntihinnat Dynamics 365 Project Operationsissa. Koska kustannus- ja myyntihinnat on suunniteltu kuluja varten, kukin näitä sisältävä tapahtumaluokka on määritettävä myös kululuokaksi. Tämä määritys varmistaa, että loppupään toiminnot ovat tarkkoja. Tapahtumaluokkien kustannus- ja myyntihinnat voidaan luetella vain yhdessä valuutassa, jonka on oltava hintaluettelon otsikon valuutta.

Voit määrittää tapahtumaluokkien kustannukset ja myyntihinnat tekemällä seuraavat toimet. 

1. Hinnaston otsikkoon perustuvan hinnaston luominen. 
2. Valitse **luokan hinnat** -kohdan aliruudukon valikosta **+ Uusi luokkahinta**. 
3. Kirjoita **pikaluontisivulle** tapahtumaluokka ja yksikkö, jolle luot uuden hinnan.

Seuraavassa taulukossa on lueteltu **yleiset** -välilehden kentät ja luokan hintarivin **pikaluontisivu** , joka kannattaa pitää mielessä, kun luot luokkahintoja myynti- tai kustannushinnastossa.

| Field | Sijainti | Relevanssi, tarkoitus ja opastus | Loppupään vaikutus |
| --- | --- | --- | --- |
| Tapahtumakategoria | **Yleiset** -välilehti ja **pikaluonti** -sivut | Valitse tapahtumaluokka, jolle olet luomassa myynti- tai kustannushintaa. | Saapuvan arvion tai todellisen kulun tapahtumaluokka kohdistetaan tähän riviin siten, että se määrittää oletusarvon mukaan tapahtumaluokan kustannuksen tai myyntihinnan. |
| Yksikön aikataulutus | **Yleiset** -välilehti ja **pikaluonti** -sivut | Yksikkö aikatauluttaa oletukset tapahtumaluokan yksikköaikataulusta. | Tämä kenttä ei vaikuta loppupään prosessiin. |
| Yksikkö | **Yleiset** -välilehti ja **pikaluonti** -sivut | Valitse yksikkö, jolle hinnat määritetään. | Saapuvan arvion tai todellisen yksikön yksikkö vastaa tällä rivillä olevaa yksikköä ja määrittää kuluarvion tai todellisen hinnan oletusarvoksi. |
| Hinnoittelutapa | **Yleiset** -välilehti ja **pikaluonti** -sivut | **Hinnoittelutapa** -kentän mahdolliset arvot ovat **yksikköhinta** , **kustannus** ja **hinnankorotus**. | Hinnan määrittämisen aikana valitaan **yksikköhinta** , joka lukitsee **prosentti** -kentän luokan hintarivillä. Jos **kustannukset** valitaan, **hinta** - ja **prosentti** -kentät lukitaan myyntihinnastoon. Kun **hinnankorotus** on valittu se **lukitsee** myyntihinnaston hintakentän. Kun kyseessä on saapuvan postin todellinen rivi, **kustannus** tai **merkintäkustannusten** hinnoittelumenetelmä johtaa vastaavaan laskuttamattomaan myyntiriviin, jolle on määritetty hinta, joka on sama kuin hinnan todellinen hinta tai laskettu hinnan merkintänä. |
| Hinta | **Yleiset** -välilehti ja **pikaluonti** -sivut | Määritä tapahtumaluokalle ja yksikköyhdistelmälle yksikkökohtainen hinta. Esimerkiksi matkahinta on 10 USD mailia kohti ja 8 USD kilometriä kohti. | Matkahinta on hinta, joka oletusarvona on yksikkökohtaisen hinnan tai kulutapahtumaluokan saapuvan tai todellisen rivin hinta.|
| Prosentti | **Yleiset** -välilehti ja **pikaluonti** -sivut | Määritä prosenttiosuus kustannuksista tapahtumaluokalle ja yksiköiden yhdistelmälle. Esimerkiksi lentolippujen myyntihinnaksi on merkitty 10 prosenttia aiheutuneista kustannuksista. | Tämä prosenttiosuus kustannuksista on voimassa vain myyntihinnastoissa, kun valittu hinnoittelutapa on **Hinnankorotus hinnan yli**. |
| Valuutta | **Yleiset** -välilehti ja **pikaluonti** -sivut | Oletusarvon mukaan tämä arvo on hinnaston otsikossa oleva valuutta. Tapahtumaluokan hinnoittelussa valuuttaa ei voi ohittaa. | Tämä valuutta on oletusarvoisesti saapuvan varsinaisen rivin yksikköhinta kustannustapahtumaluokalle kustannusten ja myynnin osalta. |

## <a name="pricing-methods-for-expenses"></a>Kulujen hinnoittelutavat

Kun määrität luokkahintoja, jotka ovat merkityksellisiä vain kulujen hinnoittelun kontekstissa, voit käyttää jotakin seuraavista kolmesta hinnoittelutavasta:

- **Yksikköhinta**
- **Kustannusten mukaan**
- **Hinnankorotus**

### <a name="price-per-unit"></a>Yksikköhinta
Kun tämä hinnoittelutapa valitaan luokan hintarivillä, joka on linkitetty myyntihinnastoon, luokan ja yksikköyhdistelmän hintaoletukset sekä arviossa että toteutuessa. Arviolla tarkoitetaan kustannusarvioihin liittyviä projektiarvioita, tarjousrivin yksityiskohtia ja kustannusrivin yksityiskohtia.

### <a name="at-cost"></a>Kustannusten mukaan
Kun tämä hinnoittelumenetelmä valitaan luokan hintarivillä, joka on yhdistetty myyntihintaluetteloon, hinta on oletusarvoisesti luokan ja yksikköyhdistelmän osalta tosiasiallisten kulujen osalta. Esimerkki: kulutapahtumaluokan laskuttamattomat myynnin todelliset arvot. Yksikköhinta määritetään laskuttamattomien myyntien toteutuneesta myynnistä kyseisen kulun kustannuksesta toteutuneesta yksikköhinnasta. Kustannuksiin perustuvia hintoja ei tehdä kulujen kustannus- tai tarjousrivin ja sopimusrivin tietojen perusteella.

### <a name="markup-over-cost"></a>Hinnankorotus
Kun tämä hinnoittelumenetelmä valitaan luokan hintarivillä, joka on yhdistetty myyntihintaluetteloon, hinta on oletusarvoisesti luokan ja yksikköyhdistelmän osalta tosiasiallisten kulujen osalta. Esimerkki: kulutapahtumaluokan laskuttamattomat myynnin todelliset arvot. Tämä yksikköhinta asetetaan laskuttamattomalle myynnille tosiasialliseksi laskennalliseksi arvoksi kyseisen hinnan tosiasiallisista kustannuksista sen jälkeen, kun määritelty merkintäprosentti on sovellettu. Kustannuksiin perustuvia hintoja ei tehdä kulujen kustannus- tai tarjousrivin ja sopimusrivin tietojen perusteella.
