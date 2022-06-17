---
title: Työn laskutushintojen määrittäminen
description: Tässä artikkelissa on tietoja työvoiman laskutushintojen määrittämisestä Project Operationsissa.
author: rumant
ms.date: 04/07/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 0ad83e899030be480baed95597e1ccfc0e560e24
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8924334"
---
# <a name="set-up-labor-bill-rates"></a>Työn laskutushintojen määrittäminen

**Käytetään**: Project Operationsin resursseihin ja ei-varastoitaviin perustuvissa skenaarioissa

Jokaisella hinnastolla on joukkoroolien hintoja tai työvoimahintoja, jotka ovat voimassa sen kontekstin ja päivämäärän mukaan, joka sisältyy hinnasto-otsikkoon. Dynamics 365 Project Operationsin laskutushinnat ajan osalta voidaan määrittää vain yhdessä valuutassa, joka on hinnasto-otsikossa käytetty valuutta.

1. Voit määrittää työvoiman laskutushinnat myyntihinnastolle siirtymällä kohtaan **Myynti** > **Asiakkaat** > **Hinnastot** ja valitsemalla **Uusi** hinnaston luomiseksi. 
2. Valitse **Roolien hinnat** -välilehden aliruudukossa **Uusi roolihinta**. 
3. Kirjoita **pikaluonti**-ruutuun se roolien ja organisaatioyksiköiden yhdistelmä, jolle haluat määrittää laskun hinnan.

   Seuraavassa taulukossa on sisältää **yleiset**-välilehden kentät ja roolin hintarivin **pikaluontisivu**-ruudun, joka täytyy pitää mielessä, kun luot roolihintoja myyntihinnastossa:

    | Field | Sijainti | Kuvaus | Loppupään vaikutus |
    | --- | --- | --- | --- |
    | Rooli | **Yleiset**-välilehti ja **pikaluonti**-ruutu | Valitse rooli, jolle haluat määrittää laskun hinnan. | Saapuva arvio tai todellinen rooli sovitetaan tämän rivin kanssa roolin oletuslaskutusprosenttiin. |
    | Resursoiva yritys | **Yleiset**-välilehti ja **pikaluonti**-ruutu | Valitse yritys tai oikeushenkilö, josta rooli on peräisin. Kyseessä on esimerkiksi Fabrikam Intian kehittäjä tai Fabrikam USA:n kehittäjä. | Saapuvan arvion tai todellisen resurssien tarjoajayritys vertaa tätä riviä oletusarvoisesti roolin laskutusprosenttiin. |
    | Resursointiyksikkö | **Yleiset**-välilehti ja **pikaluonti**-ruutu | Valitse sen yrityksen organisaatioyksikkö tai osasto, josta osa on peräisin. Kyseessä on esimerkiksi Fabrikam Intian Robotics Divisionin kehittäjä tai Fabrikam USA:n ohjelmisto-osaston kehittäjä. | Saapuvan arvion tai todellisen resurssien tarjoajayksikkö vertaa tätä riviä oletusarvoisesti roolin laskutusprosenttiin. |
    | Hinta | **Yleiset**-välilehti ja **pikaluonti**-ruutu | Määritä roolienresurssointi- ja resursointiyksikön yhdistelmän laskutushinta. Esimerkiksi Fabrikam Intian kehittäjälle on määritetty 100 USD tai Fabrikam USA:n kehittäjän laskutushinta on 150 USD. | Tämä hinta on oletuslaskenta saapuvan arvion tai todellisen rivin yksikköhinnalle aika-tapahtumaluokalle. |
    | Valuutta | **Yleiset**-välilehti ja **pikaluonti**-ruutu| Oletusarvon mukaan tämä valuutta on myyntihinnaston otsikossa oleva valuutta. Myyntihinnastossa valuuttaa ei voi ohittaa. | Tämä valuutta on oletusvaluutta saapuvan varsinaisen myyntirivin yksikköhinnassa aika-tapahtumaluokalle. |
    | Yksikön aikataulutus | **Yleiset**-välilehti ja **pikaluonti**-ruutu | Tämän yksikön aikataulun oletusarvo on aika, eikä sitä voi muuttaa roolihintaentiteetissä, koska sitä käytetään ilmaisemaan hinnat yksiköiden mukaan. | Tämä kenttä ei vaikuta loppupään prosessiin. |
    | Yksikkö | **Yleiset**-välilehti ja **pikaluonti**-ruutu | Yksikköarvo tulee myyntihinnasto-otsikon **Aikayksikkö**-kentästä. Arvoa ei voi ohittaa. Esimerkiksi Fabrikam Intian sovelluskehittäjällä on laskutushinta, joka on 1000 USD per **Intian päivä**. Fabrikam USA:n kehittäjällä on laskutushinta 1500 USD per **USA:n päivä**. | Kun yksikköhinnan oletusarvona on saapuva arvio tai todellinen rivi, järjestelmä käyttää yksiköiden järjestelmää ja muuntamista perusyksikköinä yksikköhinnan laskemiseksi. Esimerkiksi arvio on 10 **Intian päivän** verran työtä kehittäjälle Intiasta, ja Intian päiväyksikkö määritetään 10 tunniksi. Kun arvioriviä hinnoitellaan, sovellus laskee yksikköhinnan arvioon 1 000 USD/10 tuntia = 100 USD tunnissa. |

## <a name="transfer-pricing-or-set-up-bill-rates-for-resources-from-other-organizational-units-or-divisions"></a>Siirrä hinnoittelu tai määritä laskujen hinnat muiden organisaatioyksiköiden tai osastojen resursseille 

Projektipohjaiset yritykset käyttävät usein eri juridisten entiteettien työntekijöitä ja erilaisia juridisen entiteetin osastoja projektitöihin. Projektit voidaan suorittaa jostakin tietystä juridisesta entiteetistä ja jaostosta, kun taas projekteissa työskentelevät työntekijät tai konsultit voivat olla peräisin samasta juridisesta entiteetistä ja jaostosta tai muusta. Hanke voi myös koostua erilaisista eri yritysten tai divisioonien henkilöistä. Projektitoiminnoissa oikeushenkilöä, joka omistaa projektin toimituksen, kutsutaan **omistajayritykseksi** ja jaosta, joka omistaa toimituksen, kutsutaan **sopimusyksiköksi**. Kaikkia muita resursseja toimittavien oikeushenkilöiden nimenä on **resursointiyritys**, ja resursseja tuottavia osastoja kutsutaan **resursointiyksiköiksi**. Koska työvoimakustannukset vaihtelevat eri maantieteellisillä alueilla ja työmarkkinoilla eri puolilla maailmaa, työntekijöiden laskujen hinnat määritetään eri maantieteellisillä alueilla eri tavoin.

Esimerkiksi Yhdysvalloissa työskentelevä Fabrikam Intian Robotics-osaston kehittäjä laskuttaa 100 USD tunnissa. Fabrikam USA:n Robotics-osaston kehittäjä, joka työskentelee Yhdysvaltain projektissa, laskuttaa 150 USD tunnissa. 

### <a name="example-set-up-a-bill-rate"></a>Esimerkki: laskun hinnan määrittäminen 

1. Luo myyntihinnasto, jonka nimi on *Fabrikam US -laskutushinnat*, ja määritä voimassaolopäivämäärä.
2. Kirjoita Myyntihinnasto-lomakkeeseen seuraavat hintatiedot:

    | Rooli | Resursoiva yritys | Resursointiyksikkö | Laskun hinta |
    | --- | --- | --- | --- |
    | Developer | Fabrikam Intia | Fabrikam Intia - Robotics | 100 $ |
    | Developer | Fabrikam Filippiinit | Fabrikam Filippiinit - Robotics | 90 $ |
    | Developer | Fabrikam US | Fabrikam US - Robotics | 150 $ |

3. Liitä myyntihinnasto **Fabrikam USA:n laskuhinnat** projektisopimuksen projektihinnastoon tai tietylle tilille.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
