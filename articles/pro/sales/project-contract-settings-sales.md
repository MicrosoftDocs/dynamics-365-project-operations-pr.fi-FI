---
title: Projektin palvelusopimuksen kentät ja tiedot
description: Tässä aiheessa on tietoja kentistä, jotka vaikuttavat sopimusriveihin, sekä sopimustietoihin, joista on tehty yhteenveto kaikille rivinimikkeille.
author: rumant
manager: Annbe
ms.date: 10/20/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 082292c54682022933a4b46b856f9241078a9067
ms.sourcegitcommit: f8edff6422b82fdf2cea897faa6abb51e2c0c3c8
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/21/2020
ms.locfileid: "4087891"
---
# <a name="project-contract-fields-and-information"></a>Projektin palvelusopimuksen kentät ja tiedot 

_**Käytetään:** Lite-käyttöönotto – kauppa proformalaskutukseen_

Tässä aiheessa on tietoja koko projektisopimusta koskevista kentistä, mukaan lukien asetukset, jotka vaikuttavat kaikkiin sopimusriveihin. Mukana on myös tietoja palvelusopimuksesta, joka on koottu kaikkiin rivikohteisiin projektisopimuksen suorituskykyilmaisimien mukaan.

Seuraavassa taulukossa on esitetty projektisopimuksen kentät, jotka löytyvät vain Dynamics 365 Project Operationsista tai joissa on merkittäviä muutoksia verrattuna myyntisopimuksiin Dynamics 365 Salesissa.

| Field | Sijainti | Relevanssi, tarkoitus ja opastus | Loppupään vaikutus |
| --- | --- | --- | --- |
| Laji | **Yhteenveto** -välilehti (piilotettu) | Tämä on asetuskenttä, jossa on seuraavat vaihtoehdot:</br>- **Työperusteinen** (käytettävissä vain, kun Project Operations on asennettu)</br>- **Nimikepohjainen** (käytettävissä vain, kun Project Operations ja Sales on asennettu)</br>- **Palvelun ylläpitoon perustuva** (käytettävissä, kun Dynamics 365 Field Service on asennettu) | Project Operations -toiminnoissa tämän kentän arvo on oletusarvoisesti **työperusteinen** ja palvelusopimus on luokiteltu projektipohjaiseksi palvelusopimukseksi. Sopimuksen on oltava projektipohjainen, jotta kaikki projektikohtaiset laajennukset ja toiminnot voidaan ottaa käyttöön. |
| Mahdollinen asiakas | **Yhteenveto** -välilehti | Viittaus asiakkaan yritykseen tai asiakastietueeseen. Kun tarjouksesta luodaan sopimus, tämä kenttä kopioidaan tarjoustietueen vastaavasta kentästä. | Projektitarjouksen valuuttana käytetään sopimuksen oletusarvona asiakkaan valuuttaa. Tätä ei voi muuttaa ennen kuin sopimus on tallennettu. |
| Asiakaspäällikkö | **Yhteenveto** -välilehti | Tämä sopimuksen asiakaspäällikön nimi. Kun tarjouksesta luodaan sopimus, tämä kenttä kopioidaan tarjoustietueen vastaavasta kentästä. | Asiakkuuspäällikkö vastaa asiakassuhteen hallinnasta koko projektin elinkaaren ajan. Asiakkuuspäällikköön sidotun varattavan resurssin tietueen perusteella hankintayksikön oletusarvona on projektisopimus. |
| Sopimusyksikkö | **Yhteenveto** -välilehti | Tähän sopimukseen liittyvien projektien toimituksesta vastuussa oleva organisaatioyksikkö. Kun tarjouksesta luodaan sopimus, tämä kenttä kopioidaan tarjoustietueen vastaavasta kentästä. | Sopimusyksikkö on sen yrityksen osasto, joka suorittaa projektit. Jokaisella sopimusyksiköllä on valuutta, ja tätä valuuttaa käytetään projektin aikana arvioitujen ja todellisten kustannusten raportoimiseen. |
| Tuotehinnasto | **Yhteenveto** -välilehti | Tämä on hinnasto, jota käytetään tuotepohjaisten sopimusrivien oletushintoihin. Tämän kentän pudotusvalikkoluettelo näyttää luettelon hinnastoista, joissa hinnaston valuutta vastaa sopimuksen valuuttaa. Kun tarjouksesta luodaan sopimus, tämä kenttä kopioidaan tarjoustietueen vastaavasta kentästä. Projektisopimuksessa tämä kenttä on oletusarvo tilitietueesta, mutta sitä voidaan muuttaa. | Tällä kentällä ei ole merkitystä loppupäässä. |
| Valuutta | **Yhteenveto** -välilehti | Valuutta, jonka avulla ilmoitetaan tämän sopimuksen arvo ja valuutta, jossa asiakas laskutetaan. Kun tarjouksesta luodaan sopimus, tämä kenttä kopioidaan tarjoustietueen vastaavasta kentästä. Projektisopimuksessa tämä kenttä on oletusarvo tilitietueesta, mutta sitä voidaan muuttaa. | Kun sopimus on tallennettu, tätä kenttää ei voi enää muokata. Tätä kenttää käytetään sopimuksen tuote- ja projektihinnastojen oletusarvoihin. Sopimuksen valuutan avulla täsmäytetään hinnaston valuutta. |
| Ei-ylitettävä rajoitus | **Yhteenveto** -välilehti | Tämä kenttä tarkoittaa lopullisen arvo neuvoteltua ylärajaa, jonka asiakas on hyväksynyt tässä sopimuksessa. | Ylärajaa arvioidaan suorituksen aikana, ja sitä voi käyttää kaikissa tähän sopimukseen liittyvissä rivinimikkeissä ja projekteissa. |
| Pyydetty toimituspäivä | **Yhteenveto** -välilehti | Kun projektitarjouksesta luodaan sopimus, tämä kenttä kopioidaan projektitarjouksen vastaavasta kentästä. | Tätä päivämäärää käytetään laskutusaikataulujen luomisen päättymispäivänä. |

Seuraavat suorituskykyilmaisimet ovat käytettävissä projektisopimuksen **sopimuksen suorituskyky** -välilehdessä.

| Field | Sijainti | Relevanssi, tarkoitus ja opastus |
| --- | --- | --- |
| Sopimuksen arvo | Koko palvelusopimus | Projektisopimuksen kokonaisarvo. |
| Laskutettu summa | Koko palvelusopimus | Kaikkien tähän palvelusopimukseen kuuluvien laskujen summien summa. |
| Aiheutuneet kulut | Koko palvelusopimus | Kaikkiin palvelusopimukseen yhdistetyille projekteille kirjattujen todellisten kustannusten summa. |
| Käyttökate | Koko palvelusopimus | Laskutettu määrä - kustannukset, jotka ovat syntyneet asti päivä määrä/laskutettu summa |
| Odotettu kate | Koko palvelusopimus | (Sopimuksen arvo – arvioidut kustannukset)/sopimus valueEstimated costs = kaikkien sopimukseen liitettyjen projektien kaikkien arvioitujen kustannusten summa.|
| Sopimuksen arvo | Projektipohjaiset rivit | Sopimusrivin arvo. |
| Laskutettu summa | Projektipohjaiset rivit | Kiinteä hintasopimusrivi: kaikkien laskutettujen myynnin välitavoitteiden summien summa vastaa tätä sopimusriviä eri sopimusta varten laadituissa laskuissa. Ajan ja aineellisen sopimusrivin osalta: Summa kaikista veloitettavista laskutetuista myynneistä toteutuu tämän sopimusrivin kohdalla eri tätä sopimusta varten laadituissa laskuissa. |
| Aiheutuneet kulut | Projektipohjaiset rivit | Kaikkiin palvelusopimusriville yhdistetyille projekteille kirjattujen todellisten kustannusten summa. |
| Käyttökate | Projektipohjaiset rivit | (Laskutettu määrä - kustannukset, jotka ovat syntyneet asti päivä määrä)/laskutettu summa |
| Odotettu kate | Projektipohjaiset rivit | (Sopimusrivin summa perusvaluutassa – sopimusrivin arvioidut kustannukset perusvaluutassa)/sopimusrivin summa perusvaluutassa |
| Aiheutuneet kulut | Projektipohjaisen linjan erittely | Aika: Sopimusriville määritetyn projektin tämän roolin ajankohtaisten kustannusten todellisten arvojen määrä. Kulut: Sopimusriville määritetyn projektin kaikkien tähän luokkaan kirjattujen kustannuskustannusten summa. |
| Kirjattu määrä | Projektipohjaisen linjan erittely | Aika: Tähän sopimusriviin yhdistetyn projektin kokonaiskustannusten määrä toteutuu. Kulut: Kaikki tämän kululuokan määrät projektin tosiasiallisissa kustannuskustannuksissa on yhdistetty tähän sopimusriviin. |
| Laskutettu summa | Projektipohjaisen linjan erittely | Jos kyseessä on kiinteähintainen sopimusrivi, tämä kenttä jätetään tyhjäksi yksityiskohtatasolla, ja se näkyy vain sopimusrivin tasolla. Aika- ja materiaalisopimusrivin laskelmat suoritetaan tiedot-tasolla. Tiedot näyttävät kaikkien laskutettujen myyntituottorivien summan tälle sopimusriville, joka on veloitettavissa. |
| Laskutettu määrä | Projektipohjaisen linjan erittely | Jos kyseessä on kiinteähintainen sopimusrivi, tämä kenttä jätetään tyhjäksi yksityiskohtatasolla, ja se näkyy vain sopimusrivin tasolla. Aika- ja materiaalisopimusrivin laskelmat suoritetaan tiedot-tasolla ajalle ja kuluille. Aika: Tämän roolin kaikkien laskutettavien tulorivien laskutettujen tuntien summa tällä sopimusrivillä. Kulut: Kaikki tämän kululuokan määrät projektin tosiasiallisissa kustannuskustannuksissa on yhdistetty tähän sopimusriviin. |
| Sopimuksen arvo | Tuotepohjaiset rivit | Tämän tuotepohjaisen sopimusrivin sopimusriviarvo. |
| Laskutettu summa | Tuotepohjaiset rivit | Kaikkien laskurivien summien yhteissumma tätä tuotepohjaista sopimusriviä vastaan eri laskuille, jotka on luotu tälle palvelusopimukselle. |
| Aiheutuneet kulut | Tuotepohjaiset rivit | Kaikkien tuotepohjaiseen sopimusriviin kirjattujen kustannustodistusten summa. |
| Käyttökate | Projektipohjaiset rivit | Laskutettu määrä - kustannukset, jotka ovat syntyneet asti päivä määrä/laskutettu summa |
| Odotettu kate | Tuotepohjaiset rivit | (Sopimusrivin arvo - sopimusrivin arvioidut kustannukset)/sopimusrivin arvo |
