---
title: Tuotteiden alihankintarivit
description: Tässä artikkelissa käsitellään sitä, miten voidaan kirjata tuotteiden alihankintarivejä ja kirjata tuoteostot toimittajilta eri kenttien avulla.
author: rumant
ms.date: 08/06/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: b5852df1876eff591ae6a131b229d979eacf5aad
ms.sourcegitcommit: b2224d1f3c0bd4925d647e6ca3960db81a209521
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/11/2022
ms.locfileid: "9262102"
---
# <a name="subcontract-lines-for-products"></a>Tuotteiden alihankintarivit

_**Käytetään:** Lite-käyttöönotto – kauppa proformalaskutukseen_

Alihankinta Dynamics 365 Project Operationsissa voi sisältää tuotteiden alihankintarivejä. Näiden rivien avulla projektipäällikkö voi ostaa toimittajilta tuotteita, joita he voivat käyttää projektitehtävissä.

Luo Project Operationsissa tuotteiden alihankintarivi seuraavien vaiheiden mukaisesti.

1. Valitse siirtymissivulla **Alihankinnat** ja avaa sitten alihankinta, jota haluat käsitellä. 
2. Valitse **Alihankintarivit**-välilehdessä **+ Uusi** luodaksesi uuden alihankintarivin.
3. **Pikaluonti** -sivun **Tapahtumaluokka**-kentässä valitse **Materiaali** ja syötä tai valitse tarvittavat kenttätiedot. 
4. Valitse **Tallenna**.

Seuraavassa taulukossa on tietoa kentistä **Alihankintarivin tiedot** -sivulla ja **Pikaluonti**-sivulla, koska ne ovat oleellisia tuotteiden ostamisessa.

| Kenttä | Kuvaus | Toiminnallinen vaikutus|
| ----- | ----------- | ----------- |
| Nimi | Alihankintarivin nimi tunnistamisen helpottamiseksi. |Tämä näkyy kaikkien hakujen ensimmäisenä sarakkeena alihankintarivien perusteella.
| Kuvaus | Lyhyt kuvaus alihankintarivillä tilatuista tuotteista. | Ei ole |
| Rivityyppi | Tämän kentän oletusarvo on **Määräpohjainen**. |Ei ole |
| Laskutustapa | Tämä on asetusjoukko, joka edustaa kahta pääsopimusmallia, joita Project Operations tukee: **Kiinteä hinta** ja **Aika ja materiaali**. | Valitun laskutustavan perusteella välitavoitteeseen perustuva laskuaikataulu on käytettävissä alihankintariveillä, joilla on kiinteähintainen laskutustapa. |
| Tapahtumaluokka |Tämän kentän oletusarvo on **Aika**. Jos haluat luoda alihankintarivejä tuotteiden ostamista varten, määritä **Tapahtumaluokka**-kenttä arvoon **Materiaali**.  | Tämä osoittaa, että alihankintariviä käytetään projekteissa käytettävien tuotteiden ostojen kirjaamista varten. |
| Valitse tuote | Valitse, ylläpidetäänkö ostettavaa tuotetta tuoteluettelossa vai onko se käsin lisätty tuote. |Ei ole |
| Tuote | Valitse aktiivinen tuote luettelosta. Tämä kenttä on käytettävissä vain, jos **Valitse tuote** on valittuna arvoon **Olemassa**. |**Tuotteen** ja **Yksikön** yhdistelmää käytetään alihankintarivin yksikköhinnan oletusarvona tai laskettuna arvona.
| Käsin lisätty tuote | Syötä käsin lisätyn tuotteen nimi. Tämä kenttä on käytettävissä vain, jos **Valitse tuote** on valittuna arvoon **Käsin lisätty**.  |Ostohintaa ei täytetä automaattisesti käsin lisätyille tuotteille.|
| Pyydetty toimituspäivä | Anna tuotteiden vaadittu toimituspäivä.| Tätä päivämäärää käytetään myös projektin hinnaston valitsemiseen projektin hinnastoista, jotka on liitetty alihankkijaan. Tämän jälkeen alihankintarivillä oleva tuotteen kustannus tulee oletusarvona tästä hinnastosta. |
| Sopimuksessa mainittu toimituspäivä | Anna päivämäärä, jolloin tuotteet on sopimuksen mukaan sovittu toimitettavaksi.  |Ei ole|
| Tilattu määrä | Anna toimittajalta ostettavan tuotteen määrä.| Tätä käytetään varoitusten näyttämiseen, kun projektipäällikkö ylikäyttää tätä määrää.|
| Yksikköryhmä | Tämä arvo on oletusarvo vain luettelotuotteille. |Kun sekä **Tuote** että **Pyydetty toimituspäivä** on valittu, järjestelmä valitsee soveltuvan hinnaston toimituspäivän perusteella. Liittyvän hinnaston nimikkeistä haetaan vastaava tuote. Yksikkö- ja yksikköryhmäarvojen oletusarvot ovat hinnaston nimiketietueen asetuksissa. |
| Yksikkö | Tämä arvo on oletusarvo hinnaston nimikkeen yksikkömääritystä varten. Voit vaihtaa tämän toiseen yksikköön tarpeen mukaan.| Tuotteen ja yksikön yhdistelmää käytetään aiemmin luotujen tuoteluettelotuotteiden yksikköhinnan oletusarvona alihankintarivillä. |
| Yksikköhinta | Yksikköhinnan oletusarvo tulee käyttämällä tuotteen ja yksikön yhdistelmää hintaluettelonimikkeistä, jotka liittyvät projektin hinnastoon, joka soveltuu alihankintarivin pyydettyyn toimituspäivään.  |Ei ole |
| Välisumma | Tämä vain luku -kenttä lasketaan muodossa Määrä x Yksikköhinta, jos molempiin kenttiin on syötetty arvot. Jos **Määrä**-kenttä, **Yksikköhinta**-kenttä tai molemmat ovat tyhjät, voit syöttää arvon manuaalisesti.  |Ei ole |
| Arvonlisävero | Anna arvonlisäveron arvo. |Ei ole |
| Loppusumma | Tässä laskennallisessa kentässä näkyy alihankintarivin kokonaissumma verot mukaan lukien. Tämän kentän arvo lasketaan muodossa välisumma + vero. |Ei ole |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
