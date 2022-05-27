---
title: Projektien hinnoittelu
description: Tässä aiheessa on tietoja hinnoittelusta Dynamics 365 Project Service Automationissa.
author: rumant
ms.custom:
- dyn365-projectservice
ms.date: 03/11/2019
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.reviewer: johnmichalak
ms.openlocfilehash: c9a5e1ef52eec99ee580258b5dd6db9823cdb4cb
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/14/2022
ms.locfileid: "8576450"
---
# <a name="project-pricing"></a>Projektien hinnoittelu 

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Dynamics 365 Project Service Automation laajentaa Dynamics 365 Salesin Hinnasto-entiteettiä. 

## <a name="key-entities"></a>Avainentiteetit

Hinnasto sisältää neljästä eri entiteetistä peräisin olevia tietoja:

- **Hinnasto** – Tähän entiteettiin tallennetaan tietoja kontekstista, valuutasta, päivämäärävälistä ja ajan hinnoittelun aikayksiköstä. Konteksti ilmaisee, esitetäänkö hinnasto kustannushintoina vai myyntihintoina. 
- **Valuutta** – Tämä entiteetti sisältää hinnaston hintojen valuutan. 
- **Päivämäärä** – tätä entiteettiä käytetään, kun järjestelmä yrittää määrittää tapahtumalle oletushinnan. PSA:n hinnoittelu valitsee hinnaston, jonka päivämääräväli kattaa tapahtuman päivämäärän. Jos PSA:n hinnoittelussa löydetään useita hinnastoja, jotka pätevät asianomaiseen tarjoukseen, sopimukseen tai organisaatioyksikköön tapahtuman päivämääränä, oletushintaa ei määritetä. 
- **Aika** – Tämä entiteetti sisältää hintojen aikayksikön (esim. päivä- tai tuntihinnat). 

Hinnasto-entiteetillä on kolme toisiinsa liittyvää hintoja sisältävää taulukkoa:

  - **Roolin hinta** – Tämä taulukko sisältää hinnan roolin ja organisaatioyksikön arvojen yhdistelmälle, ja sitä käytetään rooliperusteisten hintojen määrittämiseen henkilöresursseille.
  - **Tapahtumaluokan hinta** –Tämä taulukko sisältää tapahtumaluokkakohtaisia hintoja, ja sitä käytetään määrittämään kululuokkien hintoja.
  - **Hinnaston nimikkeet** – Tämä taulukko sisältää luettelotuotteiden hintoja.

> ![Hintojen määrittäminen hinnaston avulla.](media/basic-guide-12.png)
 
Hinnasto on ilmoitushinnasto. Ilmoitushinnasto on yhdistelmä Hintaluettelo-entiteetistä ja siihen liittyvistä riveistä taulukoissa Roolin hinta, Tapahtumaluokan hinta ja Hinnaston nimikkeet.

## <a name="resource-roles"></a>Resurssiroolit

Termi *resurssirooli* viittaa joukkoon taitoja, osaamista ja sertifikaatteja, jotka henkilöllä on oltava, jotta hän voisi suorittaa tietyn tehtäväjoukon projektissa.

Henkilöresurssien ajan hinta perustuu yleensä siihen rooliin, joka resurssilla on tietyssä projektissa. Henkilöresurssin ajan osalta PSA tukee resurssirooliin perustuvaa kustannuslaskentaa ja laskutusta. **Aika**-yksikköryhmässä aika voidaan hinnoitella missä tahansa yksikössä.

**Aika**-yksikköryhmä luodaan PSA:n asennuksen yhteydessä. Sen oletusyksikkönä on **Tunti**. **Aika**-yksikköryhmän tai **Tunti**-yksikön määritteitä ei voi poistaa, nimetä uudelleen eikä muokata. **Aika**-yksikköryhmään voi kuitenkin lisätä muita yksikköjä. Jos yrität poistaa **Aika**-yksikköryhmää tai **Tunti**-yksikköä, PSA:n liiketoimintalogiikassa voi aiheutua virheitä.

> ![Hintojen määrittäminen roolien mukaan.](media/basic-guide-13.png)
 
## <a name="transaction-categories-and-expense-categories"></a>Tapahtuma- ja kululuokat

Matka- ja muut kulut, jotka aiheutuvat projektin konsulteille, laskutetaan yleensä asiakkaalta. PSA tukee kululuokkien hinnoittelua hinnastojen avulla. Lentoliput, hotellit ja autojen vuokraukset ovat esimerkkejä kululuokista. Kukin kulujen hinnastorivi määrittää tietyn kululuokan hinnoittelun. Kululuokkien hinnoittelun osalta PSA tukee kolmea seuraavaa hinnoittelutapaa:

- **Kustannusten mukaan** – Kulujen kustannus veloitetaan asiakkaalta ilman hinnankorotusta.
- **Hinnankorotusprosentti** – Asiakkaalta laskutettava todellisen kustannuksen ylittävä prosenttiosuus. 
- **Yksikköhinta** – Kullekin kululuokan yksikölle määritetään laskutushinta. Asiakkaalta laskutettava summa lasketaan konsultin ilmoittamien kuluyksikköjen määrän perusteella. Kilometrikorvauksessa käytetään yksikkökohtaista hinnoittelutapaa. Kilometrikorvausten kululuokan hinnaksi voidaan määrittää esimerkiksi 30 Yhdysvaltojen dollaria (USD) päivää kohden tai 2 USD mailia kohden. Kun konsultti ilmoittaa projektin kilometrikorvaukset, laskutettava summa lasketaan konsultin ilmoittamien mailien perusteella.

> ![Kululuokkien hinnoittelun määritys.](media/basic-guide-14.png)
 
## <a name="project-sales-pricing-and-overrides"></a>Projektien myyntihinnoittelu ja hintojen korvaaminen

Projektihinnastolla on projektitarjousten ja -sopimusten osalta erilainen korvausmalli kuin tuotehinnastolla. Tuoteluetteloperusteisella tarjousrivillä tarjousrivin hinta voidaan korvata suoraan roolien ja luokkien hinnoilla, koska kukin tarjousrivi viittaa tasan yhteen luettelonimikkeeseen. Projektiperusteisella tarjousrivillä tarjousrivin hintaa sen sijaan ei voida korvata suoraan roolien ja luokkien hinnoilla. Näiden erilaisten korvausmallien tukemista varten PSA:ssa on otettu käyttöön uusi hinnasto eli projektihinnasto.

> [!NOTE]
> Suosittelemme erillistä hinnastoa projektiresursseille ja luettelonimikkeille, koska ne toimivat eri tavoilla hinnoittelua korvattaessa.

Kullakin seuraavista entiteeteistä voi olla yksi tai useampi kohdennettu myyntihinnasto projektihinnoittelua varten:

- Asiakas (tili) 
- Mahdollisuus 
- Tarjous 
- Projektisopimus

Näiden entiteettien kohdennukset hinnastoille ilmaistaan projektin hinnastoissa. Myyntientiteeteille Asiakas, Mahdollisuus, Tarjous ja Projektisopimus voidaan kohdentaa yksi tai useampi hinnasto.

Asiakkaan tietueeseen ei lisätä oletusarvoista projektihinnastoa. Voit kuitenkin liittää projektihinnaston manuaalisesti asiakkaan tietueeseen. Manuaalista liittämistä pitäisi kuitenkin käyttää vain, kun asiakkaan kanssa on tehty mukautettu hinnoittelusopimus. 

Kun projektihinnasto liitetään myyntientiteettiin, PSA tarkistaa seuraavat tiedot:

- Hinnasto **Myynti**-entiteetin kontekstina. 
- Hinnaston valuutta vastaa asiakkaan hinnastoa. 

PSA käyttää projektisopimukseen liittyvien projektihinnastojen automaattisessa määrityksessä seuraavaa ensisijaisuusjärjestystä:

1. Tarjous
2. Mahdollisuus
3. Asiakas 
4. PSA:n yleiset asetukset

Kun projektihinnasto määritetään oletusarvoisesti, PSA tarkistaa, että valuutta vastaa asiakkaan valuuttaa ja että määritetyillä oletushinnastoilla on **Myynti**-konteksti.

Entiteeteille Asiakas, Mahdollisuus, Tarjous ja Projektisopimus voidaan kohdentaa useita projektihinnastoja. Tämä ominaisuus tukee päivämääräkohtaisia oletushintoja pitkäaikaisessa projektisopimuksessa, joka voi edellyttää useita hinnastoja inflaatiosta johtuvien hintapäivitysten mahdollistamista varten. Jos entiteetille Asiakas, Mahdollisuus, Tarjous tai Projektisopimus kohdennetuilla hinnastoilla kuitenkin on päällekkäisiä päivämäärävälejä, oletushinnat voivat olla virheellisiä. Tämän vuoksi on varmistettava, että kyseisille entiteeteille ei kohdenneta päällekkäisiä päivämäärävälejä sisältäviä projektihinnastoja.

### <a name="deal-specific-price-overrides"></a>Kauppakohtaiset hintojen korvaamiset

PSA:ssa voidaan luoda kauppakohtaisia korvaavuuksia tietyille projektihinnastojen hinnoille, jotka määritetään oletusarvoisesti tarjoukseen tai projektisopimukseen.

Oletusarvoisesti projektisopimukseen lisätään aina jäljennös päämyyntihinnastosta sen sijaan, että käytettäisiin linkkiä siihen. Tämä auttaa sen varmistamisessa, että asiakkaan kanssa tietyn työnkuvauksen osalta sovitut hinnat eivät muutu, jos päähinnasto muuttuu.

Tarjouksessa kuitenkin voidaan käyttää päähinnastoa. Vaihtoehtoisesti voit kopioida päähintaluettelon ja muuttaa sen muokatuksi hinnastoksi, joka pätee vain kulloiseenkin tarjoukseen. Voit luoda uuden tarjouskohtaisen hinnaston valitsemalla **Tarjous**-sivulla **Luo mukautettu hinnoittelu**. Kauppakohtaista projektihinnastoa voidaan käyttää vain tarjouksesta käsin. 

Kun luot mukautetun projektihinnaston, ainoastaan hinnaston projektikomponentit kopioidaan. Toisin sanoen uusi hinnasto luodaan kopiona tarjoukseen liitetystä projektihinnastosta, ja tässä uudessa hinnastossa on vain liittyviä roolin hintoja ja tapahtumaluokan hintoja.

> ![Projektisopimuksen mukautetun hinnoittelun tarkastelu ja määritys.](media/basic-guide-15.png)
  
## <a name="tracking-costs"></a>Kustannusten seuranta

PSA seuraa projekteissa henkilöresurssien käytöstä aiheutuvia kustannuksia. Se seuraa myös muita projektin aikana aiheutuvia kuluja, kuten matkakuluja.

Laskutushintojen lailla myös henkilöresurssien kustannushinnat määritetään hinnastoilla. Tässä ovat keskeisimmät erot kustannushinnaston ja myyntihinnaston välillä:

- Resurssin kustannushintaa ei voi korvata tietyssä projektissa, sopimuksessa tai tarjouksessa. Laskutushintoja voidaan kuitenkin korvata kauppakohtaisesti, jos tehdään kaupan luonteelle ominaisia muutoksia. 

- Kustannushinnaston laskemisessa käytetään seuraavaa järjestystä:

    1. Organisaatioyksikköön liitetty kustannushinnasto.
    2. Projektin palveluparametreihin liitetty kustannushinnasto. Koska projektin palveluparametreihin voidaan liittää kustannushinnastoja monissa eri valuutoissa, PSA täsmäyttää projektin, sopimuksen tai tarjouksen sopimusorganisaatioyksikön valuutan ja kustannushinnaston valuutan.
    3. Kulujen osalta hinnoittelutapoja kustannusten mukaan ja hinnankorotus prosentteina kustannuksista ei voi käyttää kustannushinnastoissa. Vaikka näitä hinnoittelutapoja käytettäisiin kustannushinnaston riveillä tapahtumaluokan kustannusten määrittämiseen, järjestelmä jättää ne huomioimatta eikä oletusarvoista kustannushintaa määritetä.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
