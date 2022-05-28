---
title: Projektihinnastojen hallinta tarjouksessa
description: Tässä aiheessa on tietoja projektin hinnastoentiteetistä.
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
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: d77f66d3311f3aa5ee720a05ea7da149d2a4362b
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/14/2022
ms.locfileid: "8601014"
---
# <a name="manage-project-price-lists-on-a-quote"></a>Projektihinnastojen hallinta tarjouksessa

_**Koskee:** Project Operationsin resurssiin / muuhun kuin resurssiin perustuvia skenaarioita, Lite-käyttöönotto-kaupasta proformalaskutukseen_

Dynamics 365 Project Operations laajentaa Dynamics 365 Salesin Hinnasto-entiteettiä. 

## <a name="key-entities"></a>Avainentiteetit

Hinnasto sisältää neljästä eri entiteetistä peräisin olevia tietoja:

- **Hinnasto**: Tähän entiteettiin tallennetaan tietoja kontekstista, valuutasta, päivämäärävälistä ja ajan hinnoittelun aikayksiköstä. Konteksti ilmaisee, esitetäänkö hinnasto kustannushintoina vai myyntihintoina. 
- **Valuutta**: Tämä entiteetti sisältää hinnaston hintojen valuutan. 
- **Päivämäärä**: Tätä entiteettiä käytetään, kun järjestelmä yrittää määrittää tapahtumalle oletushinnan. Valitaan hinnasto, jonka päivämääräväli kattaa tapahtuman päivämäärän. Jos löydetään useita hinnastoja, jotka pätevät asianomaiseen tarjoukseen, sopimukseen tai organisaatioyksikköön tapahtuman päivämääränä, oletushintaa ei määritetä. 
- **Aika**: Tämä entiteetti sisältää hintojen aikayksikön (esim. päivä- tai tuntihinnat). 

Hinnasto-entiteetillä on kolme toisiinsa liittyvää hintoja sisältävää taulukkoa:

  - **Roolin hinta**: Tämä taulukko sisältää hinnan roolin ja organisaatioyksikön arvojen yhdistelmälle, ja sitä käytetään rooliperusteisten hintojen määrittämiseen henkilöresursseille.
  - **Tapahtumaluokan hinta**: Tämä taulukko sisältää tapahtumaluokkakohtaisia hintoja, ja sitä käytetään määrittämään kululuokkien hintoja.
  - **Hinnaston nimikkeet**: Tämä taulukko sisältää luettelotuotteiden hintoja.
 
Hinnasto on ilmoitushinnasto. Ilmoitushinnasto on yhdistelmä Hintaluettelo-entiteetistä ja siihen liittyvistä riveistä taulukoissa Roolin hinta, Tapahtumaluokan hinta ja Hinnaston nimikkeet.

## <a name="resource-roles"></a>Resurssiroolit

Termi *resurssirooli* viittaa joukkoon taitoja, osaamista ja sertifikaatteja, jotka henkilöllä on oltava, jotta hän voisi suorittaa tietyn tehtäväjoukon projektissa.

Henkilöresurssien ajan hinta perustuu siihen rooliin, joka resurssilla on tietyssä projektissa. Henkilöresurssin kustannuslaskenta ja laskutus perustuvat resurssirooliin. **Aika**-yksikköryhmässä aika voidaan hinnoitella missä tahansa yksikössä.

**Aika**-yksikköryhmä luodaan Project Operations -sovelluksen asentamisen yhteydessä. Sen oletusyksikkönä on **Tunti**. **Aika**-yksikköryhmän tai **Tunti**-yksikön määritteitä ei voi poistaa, nimetä uudelleen eikä muokata. **Aika**-yksikköryhmään voi kuitenkin lisätä muita yksikköjä. Jos yrität poistaa **Aika**-yksikköryhmää tai **Tunti**-yksikköä, liiketoimintalogiikassa voi aiheutua virheitä.
 
## <a name="transaction-categories-and-expense-categories"></a>Tapahtuma- ja kululuokat

Matka- ja muut kulut, jotka aiheutuvat projektin konsulteille, laskutetaan asiakkaalta. Kululuokkien hinnoittelu viimeistellään hinnastojen avulla. Lentoliput, hotellit ja autojen vuokraukset ovat esimerkkejä kululuokista. Kukin kulujen hinnastorivi määrittää tietyn kululuokan hinnoittelun. Hinnan kululuokkissa käytetään seuraavia kolmea menetelmää:

- **Kustannusten mukaan**: Kulujen kustannus veloitetaan asiakkaalta ilman hinnankorotusta.
- **Hinnankorotusprosentti**: Asiakkaalta laskutettava todellisen kustannuksen ylittävä prosenttiosuus. 
- **Yksikköhinta**: Kullekin kululuokan yksikölle määritetään laskutushinta. Asiakkaalta laskutettava summa lasketaan konsultin ilmoittamien kuluyksikköjen määrän perusteella. Kilometrikorvauksessa käytetään yksikkökohtaista hinnoittelutapaa. Kilometrikorvausten kululuokan hinnaksi voidaan määrittää esimerkiksi 30 Yhdysvaltojen dollaria (USD) päivää kohden tai 2 USD mailia kohden. Kun konsultti ilmoittaa projektin kilometrikorvaukset, laskutettava summa lasketaan konsultin ilmoittamien mailien perusteella.
 
## <a name="project-sales-pricing-and-overrides"></a>Projektien myyntihinnoittelu ja hintojen korvaaminen

Projektihinnastolla on projektitarjousten ja -sopimusten osalta erilainen korvausmalli kuin tuotehinnastolla. Tuoteluetteloperusteisella tarjousrivillä tarjousrivin hinta voidaan korvata suoraan roolien ja luokkien hinnoilla, koska kukin tarjousrivi viittaa tasan yhteen luettelonimikkeeseen. Projektiperusteisella tarjousrivillä tarjousrivin hintaa sen sijaan ei voida korvata suoraan roolien ja luokkien hinnoilla. Käytä projektihinnastoa tukemaan kahta erillistä korvausmallia.

> [!NOTE]
> Suosittelemme erillistä hinnastoa projektiresursseille ja luettelonimikkeille, koska ne toimivat eri tavoilla hinnoittelua korvattaessa.

Kullakin seuraavista entiteeteistä voi olla yksi tai useampi kohdennettu myyntihinnasto projektihinnoittelua varten:

- Asiakas (tili) 
- Mahdollisuus 
- Tarjous 
- Projektisopimus

Näiden entiteettien kohdennukset hinnastoille ilmaistaan projektin hinnastoissa. Myyntientiteeteille Asiakas, Mahdollisuus, Tarjous ja Projektisopimus voidaan kohdentaa yksi tai useampi hinnasto.

Asiakkaan tietueeseen ei lisätä oletusarvoista projektihinnastoa. Voit kuitenkin liittää projektihinnaston manuaalisesti asiakkaan tietueeseen. Manuaalista liittämistä pitäisi kuitenkin käyttää vain, kun asiakkaan kanssa on tehty mukautettu hinnoittelusopimus. 

Kun projektihinnasto liitetään myyntientiteettiin, seuraavat tiedot tarkistetaan:

- Hinnaston konteksti on **Myynti**. 
- Hinnaston valuutta vastaa asiakkaan hinnastoa. 

Projektisopimuksen liittyvien projektihinnastojen automaattisessa määrityksessä on seuraava ensisijaisuusjärjestys:

1. Tarjous
2. Mahdollisuus
3. Asiakas 
4. Yleiset asetukset 

Kun projektihinnasto määritetään oletusarvoisesti, järjestelmä tarkistaa, että valuutta vastaa asiakkaan valuuttaa ja että määritetyillä oletushinnastoilla on **Myynti**-konteksti.

Entiteeteille Asiakas, Mahdollisuus, Tarjous ja Projektisopimus voidaan kohdentaa useita projektihinnastoja. Tämä ominaisuus tukee päivämääräkohtaisia oletushintoja pitkäaikaisessa projektisopimuksessa, joka voi edellyttää useita hinnastoja inflaatiosta johtuvien hintapäivitysten mahdollistamista varten. Jos entiteetille Asiakas, Mahdollisuus, Tarjous tai Projektisopimus kohdennetuilla hinnastoilla kuitenkin on päällekkäisiä päivämäärävälejä, oletushinnat voivat olla virheellisiä. Tämän vuoksi on varmistettava, että kyseisille entiteeteille ei kohdenneta päällekkäisiä päivämäärävälejä sisältäviä projektihinnastoja.

### <a name="deal-specific-price-overrides"></a>Kauppakohtaiset hintojen korvaamiset

Voit luoda kauppakohtaisia korvaavuuksia tietyille projektihinnastojen hinnoille, jotka määritetään oletusarvoisesti tarjoukseen tai projektisopimukseen.

Oletusarvoisesti projektisopimukseen lisätään aina jäljennös päämyyntihinnastosta sen sijaan, että käytettäisiin linkkiä siihen. Tämä auttaa sen varmistamisessa, että asiakkaan kanssa tietyn työnkuvauksen osalta sovitut hinnat eivät muutu, jos päähinnasto muuttuu.

Tarjouksessa kuitenkin voidaan käyttää päähinnastoa. Vaihtoehtoisesti voit kopioida päähintaluettelon ja muuttaa sen muokatuksi hinnastoksi, joka pätee vain kulloiseenkin tarjoukseen. Voit luoda uuden tarjouskohtaisen hinnaston valitsemalla **Tarjous**-sivulla **Luo mukautettu hinnoittelu**. Kauppakohtaista projektihinnastoa voidaan käyttää vain tarjouksesta käsin. 

Kun luot mukautetun projektihinnaston, ainoastaan hinnaston projektikomponentit kopioidaan. Toisin sanoen uusi hinnasto luodaan kopiona tarjoukseen liitetystä projektihinnastosta, ja tässä uudessa hinnastossa on vain liittyviä roolin hintoja ja tapahtumaluokan hintoja.
  
## <a name="tracking-costs"></a>Kustannusten seuranta

Project Operations seuraa projekteissa henkilöresurssien käytöstä aiheutuvia kustannuksia. Se seuraa myös muita projektin aikana aiheutuvia kuluja, kuten matkakuluja.

Laskutushintojen lailla myös henkilöresurssien kustannushinnat määritetään hinnastoilla. Tässä ovat keskeisimmät erot kustannushinnaston ja myyntihinnaston välillä:

- Resurssin kustannushintaa ei voi korvata tietyssä projektissa, sopimuksessa tai tarjouksessa. Laskutushintoja voidaan kuitenkin korvata kauppakohtaisesti, jos tehdään kaupan luonteelle ominaisia muutoksia. 

- Kustannushinnaston laskemisessa käytetään seuraavaa järjestystä:

    1. Organisaatioyksikköön liitetty kustannushinnasto.
    2. Project Operationsin parametreihin liitetty kustannushinnasto. Koska parametreihin voidaan liittää kustannushinnastoja monissa eri valuutoissa, projektin, sopimuksen tai tarjouksen sopimusorganisaatioyksikön valuutan ja kustannushinnaston valuuttojen vastaavuus määritetään.
    3. Kulujen osalta hinnoittelutapoja kustannusten mukaan ja hinnankorotus prosentteina kustannuksista ei voi käyttää kustannushinnastoissa. Vaikka näitä hinnoittelutapoja käytettäisiin kustannushinnaston riveillä tapahtumaluokan kustannusten määrittämiseen, järjestelmä jättää ne huomioimatta eikä oletusarvoista kustannushintaa määritetä.


[!INCLUDE[footer-include](../includes/footer-banner.md)]