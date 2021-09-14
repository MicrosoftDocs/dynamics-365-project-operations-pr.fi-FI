---
title: Tuotteiden alihankintarivit
description: Tässä aiheessa selitetään, miten voidaan kirjata tuotteiden alihankintarivejä ja kirjata tuoteostot toimittajilta eri kenttien avulla.
author: rumant
ms.date: 08/06/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: c0ddc39638ae9830eacc57f3e1def75aa36e6553
ms.sourcegitcommit: 80aa1e8070f0cb4992ac408fc05bdffe47cee931
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/13/2021
ms.locfileid: "7323682"
---
# <a name="subcontract-lines-for-products"></a>Tuotteiden alihankintarivit

[!include [banner](../../includes/dataverse-preview.md)]

_**Käytetään:** Lite-käyttöönotto – kauppa proformalaskutukseen_

Alihankinta Dynamics 365 Project Operationsissa voi sisältää tuotteiden alihankintarivejä. Näiden rivien avulla projektipäällikkö voi ostaa toimittajilta tuotteita, joita he voivat käyttää projektitehtävissä.

Luo Project Operationsissa tuotteiden alihankintarivi seuraavien vaiheiden mukaisesti.

1. Valitse siirtymissivulla **Alihankinnat** ja avaa sitten alihankinta, jota haluat käsitellä. 
2. Valitse **Alihankintarivit**-välilehdessä **+ Uusi** luodaksesi uuden alihankintarivin.
3. **Pikaluonti** -sivun **Tapahtumaluokka**-kentässä valitse **Materiaali** ja syötä tai valitse tarvittavat kenttätiedot. 
4. Valitse **Tallenna**.

Seuraavassa taulukossa on tietoa kentistä **Alihankintarivin tiedot** -sivulla ja **Pikaluonti**-sivulla, koska ne ovat oleellisia tuotteiden ostamisessa.

| Kenttä | Kuvaus |
| ----- | ----------- |
| Nimi | Alihankintarivin nimi. |
| Kuvaus | Lyhyt kuvaus alihankintarivillä tilatuista tuotteista. |
| Rivityyppi | Tämän kentän oletusarvo on **Määräpohjainen**. |
| Laskutustapa |  Alihankintarivin laskutustapa. Kiinteähintaisia laskutusmenetelmiä varten on käytettävissä välitavoitteeseen perustuva laskuaikataulu. |
| Tapahtumaluokka | Tämän kentän oletusarvo on **Aika**. Jos haluat luoda alihankintarivejä tuotteiden ostamista varten, valitse **Tapahtumaluokka**-kentässä **Materiaali**. Tämä valinta osoittaa, että alihankintarivillä tallennetaan projekteissa käytettävät tuotteet. |
| Valitse tuote | Valitse, ylläpidetäänkö ostettavaa tuotetta tuoteluettelossa vai onko se käsin lisätty tuote. |
| Tuote | Valitse aktiivinen tuote luettelosta. Tämä kenttä on käytettävissä vain, jos **Valitse tuote** on valittuna arvoon **Olemassa**. |
| Käsin lisätty tuote | Syötä käsin lisätyn tuotteen nimi. Tämä kenttä on käytettävissä vain, jos **Valitse tuote** on valittuna arvoon **Käsin lisätty**.  |
| Pyydetty toimituspäivä | Valitse tuotteiden vaadittu toimituspäivä. Tätä päivämäärää käytetään myös projektin hinnaston valitsemiseen projektin hinnastoista, jotka on liitetty alihankkijaan. Tämän jälkeen alihankintarivillä oleva tuotteen kustannus tulee oletusarvona tästä hinnastosta. |
| Sopimuksessa mainittu toimituspäivä | Valitse päivämäärä, jolloin tuotteet on sovittu toimitettavaksi.  |
| Tilattu määrä | Anna toimittajalta ostettavan tuotteen määrä. Jos projektipäällikkö ylittää tämän määrän, siitä tulee varoitus. |
| Yksikköryhmä | Tämä arvo on oletusarvo vain luettelotuotteille. Kun sekä **Tuote** että **Pyydetty toimituspäivä** on valittu, järjestelmä valitsee soveltuvan hinnaston toimituspäivän perusteella. Liittyvän hinnaston nimikkeistä haetaan vastaava tuote. Yksikkö- ja yksikköryhmäarvojen oletusarvot ovat hinnaston nimiketietueen asetuksissa. |
| Yksikkö | Tämä arvo käyttää hinnaston nimiketietueen yksikköasetusten oletusarvoa. Voit vaihtaa tämän toiseen yksikköön tarpeen mukaan. Tuotteen ja yksikön yhdistelmää käytetään aiemmin luotujen tuoteluettelotuotteiden yksikköhinnan oletusarvona alihankintarivillä. |
| Yksikköhinta | Yksikköhinnan oletusarvo tulee käyttämällä tuotteen ja yksikön yhdistelmää hintaluettelonimikkeistä, jotka liittyvät projektin hinnastoon, joka soveltuu alihankintarivin pyydettyyn toimituspäivään.  |
| Välisumma | Tämä vain luku -kenttä lasketaan muodossa Määrä x Yksikköhinta, jos molempiin kenttiin on syötetty arvot. Jos **Määrä**-kenttä, **Yksikköhinta**-kenttä tai molemmat ovat tyhjät, voit syöttää arvon manuaalisesti.  |
| Arvonlisävero | Anna arvonlisäveron arvo. |
| Loppusumma | Tässä laskennallisessa kentässä näkyy alihankintarivin kokonaissumma verot mukaan lukien. Tämän kentän arvo lasketaan muodossa välisumma + vero. |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
