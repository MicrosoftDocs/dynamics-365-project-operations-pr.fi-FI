---
title: Mukautettujen kenttien määrittäminen hinnoitteludimensioiksi
description: Tässä aiheessa on tietoja hinnoitteludimensioiden määrittämisestä mukautettujen kenttien avulla.
author: rumant
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: rumant
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 41c65d6bf64d8a81759239f2a31f3a68953181c8
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/14/2022
ms.locfileid: "8599404"
---
# <a name="set-up-custom-fields-as-pricing-dimensions"></a>Mukautettujen kenttien määrittäminen hinnoitteludimensioiksi

_**Koskee:** Project Operationsin resurssiin / muuhun kuin resurssiin perustuvia skenaarioita, Lite-käyttöönotto-kaupasta proformalaskutukseen_

Ennen aloittamista aihe olettaa, että olet suorittanut toimintosarjat aiheissa [Luo mukautettuja kenttiä ja entiteettejä](create-custom-fields-entities-pricing-dimensions.md) ja [Lisää vaadittuja mukautettuja kenttiä hintojen määrittelyyn ja tapahtumaentiteetteihin](add-custom-fields-price-setup-transactional-entities.md). Jos et ole suorittanut näitä toimintosarjoja loppuun, palaa niihin ja suorita ne, ja palaa sen jälkeen tähän aiheeseen. 

Tässä aiheessa on tietoja mukautettujen hinnoitteludimensioiden määrittämisestä. **Parameterit**-sivun **Summaperusteiset hinnoitteludimensiot** -välilehdessä ovat hinnoitteludimensioentiteettien tietueet. Tämän välilehden ruudukossa on oletusarvoisesti seuraavat kaksi riviä:

- **msdyn_resourcecategory** (Rooli)
- **msdyn_OrganizationalUnit** (Organisaatioyksikkö)

> [!IMPORTANT]
> Älä poista näitä rivejä. Jos et kuitenkaan tarvitse niitä, voit poistaa ne käytöstä tietyssä yhteydessä asettamalla asetusten **Sovelletaan kustannuksiin**, **Sovelletaan myyntiin** ja **Sovelletaan ostoihin** arvoiksi **Ei**. Määrittämällä nämä määritearvot arvoksi **Ei** tuottaa saman lopputuloksen kuin se, että näitä kenttiä ei ole hinnoitteludimensioina.

Jotta kentästä tulisi hinnoitteludimensio, sen on oltava:

- Luotu kenttänä **Roolihinta** ja **Roolihinnan hinnankorotus** -entiteeteissä. Lisätietoja on aiheessa [Mukautettujen kenttien lisääminen hinnanmäärittely- ja tapahtumaentiteetteihin](add-custom-fields-price-setup-transactional-entities.md).

- Luotu rivinä **Hinnoitteludimensio** -taulukkoon. Voit esimerkiksi lisätä hinnoitteludimension rivejä seuraavan kuvan osoittamalla tavalla. 

![Summaan perustuvat hinnoitteludimensioiden rivit.](media/Amt-based-PD.png)

Tesurssin työaika (**msdyn_resourceworkhours**) on lisätty hinnankorotuspohjaiseen dimensioon, ja se on lisätty **Hinnankorotuspohjainen hinnoitteludimensio** -välilehden ruudukkoon.

![Hinnankorotukseen perustuvat hinnoitteludimensioiden rivit.](media/Markup-based-PD.png)


> [!IMPORTANT]
> Mikä tahansa muutos hinnoitteludimensiotietoihin tässä taulukossa, olemassa oleva tai uusi, kopioidaan hinnoittelun liiketoimintalogiikkaan vasta sitten, kun välimuisti päivitetään. Välimuistin päivitys voi kestää 10 minuuttia. Salli tämän verran aikaa nähdäksesi ne muutokset hintojen oletusarvojen logiikassa, jotka seuraavat muutoksista hinnoitteludimensiotietoihin.


## <a name="attributes-of-the-pricing-dimensions-table"></a>Hinnoitteludimensiot -taulukon määritteet
Seuraavissa osissa on tietoja **Hinnoitteludimensiot**-taulukon eri määritteistä.

### <a name="pricing-dimension-name"></a>Hinnoitteludimension nimi
Tämän arvon on oltava täsmälleen sama kuin sen kentän rakennenimi, joka on lisätty mukautettujen hinnoitteludimensioiden- **Roolihinta**-taulukkoon. Lisätietoja kenttien lisäämisestä **Roolihinta**-taulukkoon on aiheessa [Lisää mukautettuja kenttiä hintojen määrittely- ja tapahtumaentiteetteihin](add-custom-fields-price-setup-transactional-entities.md).

### <a name="type-of-dimension"></a>Dimension tyyppi
Hinnoitteludimensioita on kahta tyyppiä:
  
  - **Summiin perustuvat dimensiot**: Syötekontekstin dimension arvot on sovitettu yhteen **Roolihinta**-rivillä olevien dimension arvojen kanssa, ja hinta/kustannus saadaan oletusarvoisesti suoraan **Roolihinta** -taulukosta.
  - **Hinnankorotuspohjaiset dimensiot**: Nämä ovat dimensioita, joissa käytetään seuraavaa kolmevaiheista prosessia hinnan/kustannusten saamiseksi:
 
    1. Hinnankorotukseen perustumattomat dimensioarvot syötekontekstista täsmäytetään Roolihinta-rivin kanssa, jotta saadaan perushinta.
    2. Dimensioarvot syötekontekstista täsmäytetään **Roolihinnan korotus**-rivin kanssa, jotta saadaan korotusprosentti.
    3. Toisen vaiheen korotusprosentti kohdistetaan perushintaan, joka saatiin **Roolihinta**-taulukosta ensimmäisessä vaiheessa. Näin lasketaan lopullinen hinta/kustannus.
   
   Seuraavassa taulukossa on esitetty hinnankorotusten laskeminen.
  
| Rooli        | Organisaatioyksikkö    |Työn sijainti      |Vakio-otsikko      |Resurssin työtunnit      |  Hinnankorotus|
| ------------|-------------|-------------------|--------------------|-------------------------|--------:|
|             | Contoso India|Asiakkaan tiloissa            |                    |Ylityö                 |15     |
|             | Contoso India|Paikallinen             |                    |Ylityö                 |10     |
|             | Contoso US   |Paikallinen             |                    |Ylityö                 |20     |


Jos resurssi Contoso Indialta, jonka perushinta on 100 US-dollaria työskentelee asiakkaan tiloissa, ja hän merkitsee 8 tuntia tavallista työaikaa ja 2 tuntia ylityötä aikamerkintäänsä, hinnoittelumoottori käyttää perushintaa 100 kahdeksalle tunnille ja tallentaa 800 USD. Kahdelle ylityötunnille käytetään 15 % hinnankorotusta, joka lasketaan perushinnalle 100, jotta saadaan yksikköhinta 115 US-dollaria, ja kokonaiskustannukseksi tallennetaan 230 US-dollaria.

### <a name="applicable-to-cost"></a>Sovelletaan kustannuksiin 
Jos tämän arvo on **Kyllä**, se osoittaa, että dimension arvoa syötekontekstista tulisi käyttää yhdistämään **Roolihinta** ja **Roolihinnan korotus**, kun haetaan kustannuksia ja hinnankorotusten arvoja.

### <a name="applicable-to-sales"></a>Sovelletaan myyntiin
Jos tämän arvo on **Kyllä**, se osoittaa, että dimension arvoa syötekontekstista tulisi käyttää yhdistämään **Roolihinta** ja **Roolihinnan korotus**, kun haetaan laskutuksen ja hinnankorotusten arvoja.

### <a name="applicable-to-purchase"></a>Sovelletaan ostoihin
Jos tämän arvo on **Kyllä**, se osoittaa, että dimension arvoa syötekontekstista tulisi käyttää yhdistämään **Roolihinta** ja **Roolihinnan korotus**, kun haetaan ostohintaa. Alihankintaskenaarioita ei tueta, joten tätä kenttää ei käytetä. 

### <a name="priority"></a>Prioriteetti
Dimension prioriteetin määrittäminen auttaa hinnoittelua tuottamaan hinnan jopa silloin, kun se ei löydä tarkkaa yhteyttä syötedimension arvojen ja **Roolihinta** tai **Roolihinnan korotus** -taulujen väliltä. Tässä skenaariossa käytetään null-arvoja yhteensovittamattomille dimensioarvoille painottamalla dimensioita niiden prioriteettien mukaan.

- **Kustannusprioriteetti**: dimension kustannusprioriteetin arvo osoittaa kyseisen dimension painon, kun sitä verrataan kustannushintojen asetuksiin. **Kustannusprioriteetin** arvon tulee olla yksilöivä niissä dimensioissa, joita **Sovelletaan kustannuksiin**.
- **Myyntiprioriteetti**: dimension myyntiprioriteetin arvo osoittaa kyseisen dimension painon, kun sitä verrataan myyntihintojen tai laskutushintojen asetuksiin. **Myyntiprioriteetin** arvon tulee olla yksilöivä niissä dimensioissa, joita **Sovelletaan myyntiin**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]