---
title: Työn laskutushintojen määrittäminen – lite
description: Tämä aihe sisältää tietoja työvoiman laskutushinnoista Project Operationsissa.
author: rumant
manager: Annbe
ms.date: 10/16/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 733b7c83de8137aba6c084d5f03a2a4cf076a16c
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5274409"
---
# <a name="set-up-labor-bill-rates---lite"></a>Työn laskutushintojen määrittäminen – lite

_**Käytetään:** Lite-käyttöönotto – kauppa proformalaskutukseen_

Jokaisella hinnastolla on joukkoroolien hintoja tai työvoimahintoja, jotka ovat voimassa sen kontekstin ja päivämäärän mukaan, joka sisältyy hinnasto-otsikkoon. Dynamics 365 Project Operationsin laskutushinnat ajan osalta voidaan määrittää vain yhdessä valuutassa, joka on hinnasto-otsikossa käytetty valuutta.

1. Jos haluat määrittää myyntihinnaston työvoimalaskujen hinnat, luo hinnasto-otsikon perusteella hinnasto. 
2. Valitse **roolien hinnat** -välilehden aliruudukossa **+ Uusi roolien hinta**. 
3. Kirjoita **pikaluonti**-ruutuun se roolien ja organisaatioyksiköiden yhdistelmä, jolle haluat määrittää laskun hinnan.

  Seuraavassa taulukossa on sisältää **yleiset**-välilehden kentät ja roolin hintarivin **pikaluontisivu**-ruudun, joka täytyy pitää mielessä, kun luot roolihintoja myyntihinnastossa:

  | Field | Sijainti | Kuvaus | Loppupään vaikutus |
  | --- | --- | --- | --- |
  | Rooli | **Yleiset**-välilehti ja **pikaluonti**-ruutu | Valitse rooli, jolle haluat määrittää laskun hinnan. | Saapuva arvio tai todellinen rooli sovitetaan tämän rivin kanssa roolin oletuslaskutusprosenttiin. |
  | Resursointiyksikkö | **Yleiset**-välilehti ja **pikaluonti**-ruutu | Valitse sen yrityksen organisaatioyksikkö tai osasto, josta osa on peräisin. Kyseessä on esimerkiksi Fabrikam Intian Robotics Divisionin kehittäjä tai Fabrikam USA:n ohjelmisto-osaston kehittäjä. | Saapuvan arvion tai todellisen resurssien tarjoajayksikkö vertaa tätä riviä oletusarvoisesti roolin laskutusprosenttiin. |
  | Hinta | **Yleiset**-välilehti ja **pikaluonti**-ruutu | Määritä roolienresurssointi- ja resursointiyksikön yhdistelmän laskutushinta. Esimerkiksi Fabrikam Intian kehittäjälle on määritetty 100 USD tai Fabrikam USA:n kehittäjän laskutushinta on 150 USD. | Tämä hinta on oletuslaskenta saapuvan arvion tai todellisen rivin yksikköhinnalle aika-tapahtumaluokalle. |
  | Valuutta | **Yleiset**-välilehti ja **pikaluonti**-ruutu| Oletusarvon mukaan tämä valuutta on myyntihinnaston otsikossa oleva valuutta. Myyntihinnastossa valuuttaa ei voi ohittaa. | Tämä valuutta on oletusvaluutta saapuvan varsinaisen myyntirivin yksikköhinnassa aika-tapahtumaluokalle. |
  | Yksikön aikataulutus | **Yleiset**-välilehti ja **pikaluonti**-ruutu | Tämän yksikön aikataulun oletusarvo on aika, eikä sitä voi muuttaa roolihintaentiteetissä, koska sitä käytetään ilmaisemaan hinnat yksiköiden mukaan. | Tämä kenttä ei vaikuta loppupään prosessiin. |
  | Yksikkö | **Yleiset**-välilehti ja **pikaluonti**-ruutu | Yksikköarvo tulee myyntihinnasto-otsikon **Aikayksikkö**-kentästä. Arvoa ei voi ohittaa. Esimerkiksi Fabrikam Intian sovelluskehittäjällä on laskutushinta, joka on 1000 USD per **Intian päivä**. Fabrikam USA:n kehittäjällä on laskutushinta 1500 USD per **USA:n päivä**. | Kun yksikköhinnan oletusarvona on saapuva arvio tai todellinen rivi, järjestelmä käyttää yksiköiden järjestelmää ja muuntamista perusyksikköinä yksikköhinnan laskemiseksi. Esimerkiksi arvio on 10 **Intian päivän** verran työtä kehittäjälle Intiasta, ja Intian päiväyksikkö määritetään 10 tunniksi. Kun arvioriviä hinnoitellaan, sovellus laskee yksikköhinnan arvioon 1 000 USD/10 tuntia = 100 USD tunnissa. |


## <a name="transfer-pricing-or-set-up-bill-rates-for-resources-from-other-organizational-units-or-divisions"></a>Siirrä hinnoittelu tai määritä laskujen hinnat muiden organisaatioyksiköiden tai osastojen resursseille 

Projektipohjaiset yritykset, jotka käyttävät yrityksen eri osastojen työntekijöitä projektien työstöihin. Projektit voidaan suorittaa yhdestä divisioonista samalla, kun työntekijät tai konsultit ovat peräisin samasta eri yrityksen jaoksesta. Hanke voi myös koostua erilaisista eri divisioonien henkilöistä. Project Operationsissa projektin toimituksen omistava yritys on nimeltään **hankintayksikkö**. Kaikkia muita resursseja toimittavien osastojen nimi on **resursointiyksiköt**. Koska työvoimakustannukset vaihtelevat eri maantieteellisillä alueilla ja työmarkkinoilla eri puolilla maailmaa, työntekijöiden laskujen hinnat määritetään eri maantieteellisillä alueilla eri tavoin.

Esimerkiksi Yhdysvalloissa työskentelevä Fabrikam Intian kehittäjä laskuttaa 100 USD tunnissa. Fabrikam US USA -projektin kehittäjä laskuttaa 150 USD tunnissa.

### <a name="example-set-up-a-bill-rate"></a>Esimerkki: laskun hinnan määrittäminen

1. Luo myyntihinnasto, jonka nimi on *Fabrikam US -laskutushinnat*, ja määritä voimassaolopäivämäärä.
2. Kirjoita Myyntihinnasto-lomakkeeseen seuraavat hintatiedot:

    | Rooli | Organisaatioyksikkö | Laskun hinta |
    | --- | --- | --- |
    | Developer | Fabrikam Intia | 100 $ |
    | Developer | Fabrikam Filippiinit | 90 $ |
    | Developer | Fabrikam US | 150 $ |

3. Liitä myyntihinnasto **Fabrikam USA:n laskuhinnat** projektisopimuksen projektihinnastoon tai tietylle tilille.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]