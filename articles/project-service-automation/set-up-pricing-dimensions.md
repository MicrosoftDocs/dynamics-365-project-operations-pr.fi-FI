---
title: Mukautettujen kenttien määrittäminen hinnoitteludimensioiksi
description: Tässä aiheessa on tietoja mukautettujen hinnoitteludimensioiden määrittämisestä.
author: Rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 11/20/2018
ms.topic: article
ms.prod: Project Service
ms.service: business-applications
ms.assetid: d5f59779-a6ed-4854-ab82-2810dace288f
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
ms.openlocfilehash: 8f19254acfc7f03ed7ccca95ed7e2b94cc199d3b
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/24/2020
ms.locfileid: "3751145"
---
# <a name="set-up-custom-fields-as-pricing-dimensions"></a>Mukautettujen kenttien määrittäminen hinnoitteludimensioiksi 

Ennen aloittamista aihe olettaa, että olet suorittanut toimintosarjat aiheissa [Luo mukautettuja kenttiä ja entiteettejä](create-custom-fields-entities.md) ja [Lisää mukautettuja kenttiä hintojen määrittelyyn ja tapahtumaentiteetteihin](field-references.md). Jos et ole suorittanut näitä toimintosarjoja loppuun, palaa niihin ja suorita ne, ja palaa sen jälkeen tähän aiheeseen. 

Tässä aiheessa on tietoja mukautettujen hinnoitteludimensioiden määrittämisestä. Project Servicen verkkoliittymän **Parametrit**-sivulla **Summaperusteiset hinnoitteludimensiot** -välilehdellä näkyvät hinnoitteludimensioentiteettien tietueet. Oletusarvoisesti Project Service -asennus luo kaksi riviä tämän välilehden ruudukkoon:

- **msdyn_resourcecategory** (Rooli)
- **msdyn_OrganizationalUnit** (Organisaatioyksikkö)

> [!IMPORTANT]
> Älä poista näitä rivejä. Jos et kuitenkaan tarvitse niitä, voit poistaa ne käytöstä tietyssä yhteydessä asettamalla asetusten **Sovelletaan kustannuksiin**, **Sovelletaan myyntiin** ja **Sovelletaan ostoihin** arvoiksi **Ei**. Määrittämällä nämä määritearvot arvoksi **Ei** tuottaa saman lopputuloksen kuin se, että näitä kenttiä ei ole hinnoitteludimensioina.

Jotta kentästä tulisi hinnoitteludimensio, sen on oltava:

- Luotu kenttänä **Roolihinta** ja **Roolihinnan hinnankorotus** -entiteeteissä. Lisätietoja on aiheessa [Mukautettujen kenttien lisääminen hinnanmäärittely- ja tapahtumaentiteetteihin](field-references.md).
- Luotu rivinä **Hinnoitteludimensio** -taulukkoon. Voit esimerkiksi lisätä hinnoitteludimension rivejä seuraavan kuvan osoittamalla tavalla. 

![Summaan perustuvat hinnoitteludimensioiden rivit](media/Amt-based-PD.png)

Huomaa, että resurssin työaika (**msdyn_resourceworkhours**) on lisätty hinnankorotuspohjaiseen dimensioon, ja se on lisätty **Hinnankorotuspohjainen hinnoitteludimensio** -välilehden ruudukkoon.

![Hinnankorotukseen perustuvat hinnoitteludimensioiden rivit](media/Markup-based-PD.png)

> [!IMPORTANT]
> Mikä tahansa muutos hinnoitteludimensiotietoihin tässä taulukossa, olemassa oleva tai uusi, kopioidaan Project Servicen hinnoittelun liiketoimintalogiikkaan vasta sitten, kun välimuisti päivitetään. Välimuistin päivitys voi kestää 10 minuuttia. Salli tämän verran aikaa nähdäksesi ne muutokset hintojen oletusarvojen logiikassa, jotka seuraavat muutoksista hinnoitteludimensiotietoihin.


## <a name="attributes-of-the-pricing-dimensions-table"></a>Hinnoitteludimensiot -taulukon määritteet
Seuraavissa osissa on tietoja **Hinnoitteludimensiot**-taulukon eri määritteistä.

### <a name="pricing-dimension-name"></a>Hinnoitteludimension nimi
Tämän arvon on oltava täsmälleen sama kuin sen kentän rakennenimi, joka on lisätty mukautettujen hinnoitteludimensioiden- **Roolihinta**-taulukkoon. Lisätietoja kenttien lisäämisestä **Roolihinta**-taulukkoon on aiheessa [Lisää mukautettuja kenttiä hintojen määrittely- ja tapahtumaentiteetteihin](field-references.md).

### <a name="type-of-dimension"></a>Dimension tyyppi
Hinnoitteludimensioita on kahta tyyppiä:
  
  - **Summiin perustuvat dimensiot**: Syötekontekstin dimension arvot on sovitettu yhteen **Roolihinta**-rivillä olevien dimension arvojen kanssa, ja hinta/kustannus saadaan oletusarvoisesti suoraan **Roolihinta** -taulukosta.
  - **Hinnankorotuspohjaiset dimensiot**: Nämä ovat dimensioita, joissa Project Service ottaa käyttöön 3-vaiheisen prosessin hinnan/kustannusten saamiseksi.
 
    1. Project Service yhdistää hinnankorotukseen perustumattomat dimensioarvot syötekontekstista Roolihinta-riviin saadakseen perushinnan.
    2. Project Service yhdistää kaikki dimensioarvot syötekontekstista **Roolihinnan korotus**-riviin saadakseen korotusprosentin.
    3. Project Service soveltaa toisen vaiheen korotusprosenttia perushintaan, joka saatiin **Roolihinta**-taulukosta ensimmäisessä vaiheessa laskeakseen lopullisen hinnan/kustannuksen.
   
   Seuraavassa taulukossa on esitetty hinnankorotusten laskeminen.
  
| Rooli        | Organisaatioyksikkö    |Työn sijainti      |Vakio-otsikko      |Resurssin työtunnit      |  Hinnankorotus|
| ------------|-------------|-------------------|--------------------|-------------------------|--------:|
|             | Contoso India|Asiakkaan tiloissa            |                    |Ylityö                 |15     |
|             | Contoso India|Paikallinen             |                    |Ylityö                 |10     |
|             | Contoso US   |Paikallinen             |                    |Ylityö                 |20     |


Jos resurssi Contoso Indialta, jonka perushinta on 100 US-dollaria työskentelee asiakkaan tiloissa, ja hän merkitsee 8 tuntia tavallista työaikaa ja 2 tuntia ylityötä aikamerkintäänsä, Project Servicen hinnoittelumoottori käyttää perushintaa 100 kahdelsalle tunnille ja tallentaa 800 USD. Kahdelle ylityötunnille käytetään 15 % hinnankorotusta, joka lasketaan perushinnalle 100, jotta saadaan yksikköhinta 115 US-dollaria, ja kokonaiskustannukseksi tallennetaan 230 US-dollaria.

### <a name="applicable-to-cost"></a>Sovelletaan kustannuksiin 
Jos tämän arvo on **Kyllä**, se osoittaa, että dimension arvoa syötekontekstista tulisi käyttää yhdistämään **Roolihinta** ja **Roolihinnan korotus**, kun haetaan kustannuksia ja hinnankorotusten arvoja.

### <a name="applicable-to-sales"></a>Sovelletaan myyntiin
Jos tämän arvo on **Kyllä**, se osoittaa, että dimension arvoa syötekontekstista tulisi käyttää yhdistämään **Roolihinta** ja **Roolihinnan korotus**, kun haetaan laskutuksen ja hinnankorotusten arvoja.

### <a name="applicable-to-purchase"></a>Sovelletaan ostoihin
Jos tämän arvo on **Kyllä**, se osoittaa, että dimension arvoa syötekontekstista tulisi käyttää yhdistämään **Roolihinta** ja **Roolihinnan korotus**, kun haetaan ostohintaa. Tällä hetkellä Project Service ei tue alihankintaskenaarioita, joten tätä kenttää ei käytetä. 

### <a name="priority"></a>Prioriteetti
Dimension prioriteetin määrittäminen auttaa Project Servicen hinnoittelua tuottamaan hinnan jopa silloin, kun se ei löydä tarkkaa yhteyttä syötedimension arvojen ja **Roolihinta** tai **Roolihinnan korotus** -taulujen väliltä. Tässä skenaariossa Project Service käyttää null-arvoja yhteensovittamattomille dimensioarvoille painottamalla dimensioita niiden prioriteettien mukaan.

- **Kustannusprioriteetti**: dimension kustannusprioriteetin arvo osoittaa kyseisen dimension painon, kun sitä verrataan kustannushintojen asetuksiin. **Kustannusprioriteetin** arvon tulee olla yksilöivä niissä dimensioissa, joita **Sovelletaan kustannuksiin**.
- **Myyntiprioriteetti**: dimension myyntiprioriteetin arvo osoittaa kyseisen dimension painon, kun sitä verrataan myyntihintojen tai laskutushintojen asetuksiin. **Myyntiprioriteetin** arvon tulee olla yksilöivä niissä dimensioissa, joita **Sovelletaan myyntiin**.
