---
title: Projektin palvelusopimuksen asetukset
description: Tässä aiheessa on tietoja kentistä, jotka vaikuttavat sopimusriveihin, sekä sopimustietoihin, joista on tehty yhteenveto kaikille rivinimikkeille.
author: rumant
ms.date: 10/20/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: f34d6c6b92f164cc95405147356c34bb03eb127284aba7a92712b8eec42d792f
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/06/2021
ms.locfileid: "6996297"
---
# <a name="header-details-for-project-based-contracts"></a>Projektipohjaisten sopimusten otsikkotiedot

_**Käytetään:** Project Operationsin resursseihin ja ei-varastoitaviin perustuvissa skenaarioissa_

Tässä aiheessa on tietoja koko projektisopimusta koskevista kentistä, mukaan lukien asetukset, jotka vaikuttavat kaikkiin sopimusriveihin. Mukana on myös tietoja palvelusopimuksesta, joka on koottu kaikkiin rivikohteisiin projektisopimuksen suorituskykyilmaisimien mukaan.

Seuraavassa taulukossa on luettelo projektisopimuksen kentistä, jotka ovat yksilöllisiä Dynamics 365 Project Operationsissa tai joiden myyntitilausten toimintatavoissa on tärkeitä muutoksia Dynamics 365 Salesissa.

| Field | Sijainti | Kuvaus | Loppupään vaikutus |
| --- | --- | --- | --- |
| Laji | **Yhteenveto**-välilehti (piilotettu) | Tämä on asetuskenttä, jossa on seuraavat vaihtoehdot:</br>- **Työperusteinen** (käytettävissä vain, kun Project Operations on asennettu)</br>- **Nimikepohjainen** (käytettävissä vain, kun Project Operations ja Sales on asennettu)</br>- **Palvelun ylläpitoon perustuva** (käytettävissä, kun Dynamics 365 Field Service on asennettu) | Project Operations -toiminnoissa tämän kentän arvo on oletusarvoisesti **työperusteinen** ja palvelusopimus on luokiteltu projektipohjaiseksi palvelusopimukseksi. Sopimuksen on oltava projektipohjainen, jotta kaikki projektikohtaiset laajennukset ja toiminnot voidaan ottaa käyttöön. |
| Omistava yritys | **Yhteenveto**-välilehti | Yritys, joka käsittelee tähän hankesopimukseen liittyvistä projekteista kertyneet kustannukset ja tulot. Kun tarjouksesta luodaan sopimus, tämä kenttä kopioidaan tarjoustietueen vastaavasta kentästä. | Omistava yritys vastaa oikeushenkilön käsitettä Project Operationsin **Projektinhallintaja kirjanpito** -moduulissa. Kaikki tästä projektista kertyvät kustannukset ja tuotot kirjataan omistavan yrityksen kirjanpitoon. |
| Asiakas | **Yhteenveto**-välilehti | Viittaus asiakkaan yritykseen tai asiakastietueeseen. Kun tarjouksesta luodaan sopimus, tämä kenttä kopioidaan tarjoustietueen vastaavasta kentästä. | Projektitarjouksen valuuttana käytetään sopimuksen oletusarvona asiakkaan valuuttaa. Valuuttaa voi muuttaa, ennen kuin palvelusopimus tallennetaan. |
| Asiakaspäällikkö | **Yhteenveto**-välilehti | Tämä sopimuksen asiakaspäällikön nimi. Kun tarjouksesta luodaan sopimus, tämä kenttä kopioidaan tarjoustietueen vastaavasta kentästä. | Asiakkuuspäällikkö vastaa asiakassuhteen hallinnasta koko projektin elinkaaren ajan. Asiakkuuspäällikköön sidotun varattavan resurssin tietueen perusteella hankintayksikön oletusarvona on projektisopimus. |
| Sopimusyksikkö | **Yhteenveto**-välilehti | Tähän sopimukseen liittyvien projektien toimituksesta vastuussa oleva organisaatioyksikkö. Kun tarjouksesta luodaan sopimus, tämä kenttä kopioidaan tarjoustietueen vastaavasta kentästä. | Sopimusyksikkö on sen yrityksen osasto, joka suorittaa projektit. Jokaisella sopimusyksiköllä on valuutta, ja tätä valuuttaa käytetään projektin aikana arvioitujen ja todellisten kustannusten raportoimiseen. |
| Tuotehinnasto | **Yhteenveto**-välilehti | Tämä on hinnasto, jota käytetään tuotepohjaisten sopimusrivien oletushintoihin. Tämän kentän pudotusvalikkoluettelo näyttää luettelon hinnastoista, joissa hinnaston valuutta vastaa sopimuksen valuuttaa. Kun tarjouksesta luodaan sopimus, tämä kenttä kopioidaan tarjoustietueen vastaavasta kentästä. Projektisopimuksessa tämä kenttä on oletusarvo tilitietueesta, mutta sitä voidaan muuttaa. | Tällä kentällä ei ole merkitystä loppupäässä. |
| Valuutta | **Yhteenveto**-välilehti | Valuutta, jonka avulla ilmoitetaan tämän sopimuksen arvo ja valuutta, jossa asiakas laskutetaan. Kun tarjouksesta luodaan sopimus, tämä kenttä kopioidaan tarjoustietueen vastaavasta kentästä. Projektisopimuksessa tämä kenttä on oletusarvo tilitietueesta, mutta sitä voidaan muuttaa. | Kun sopimus on tallennettu, tätä kenttää ei voi enää muokata. Tätä kenttää käytetään sopimuksen tuote- ja projektihinnastojen oletusarvoihin. Sopimuksen valuutan avulla täsmäytetään hinnaston valuutta. |
| Ei-ylitettävä rajoitus | **Yhteenveto**-välilehti | Tämä kenttä tarkoittaa lopullisen arvo neuvoteltua ylärajaa, jonka asiakas on hyväksynyt tässä sopimuksessa. | Ylärajaa arvioidaan suorituksen aikana, ja sitä voi käyttää kaikissa tähän sopimukseen liittyvissä rivinimikkeissä ja projekteissa. |
| Pyydetty toimituspäivä | **Yhteenveto**-välilehti | Kun projektitarjouksesta luodaan sopimus, tämä kenttä kopioidaan projektitarjouksen vastaavasta kentästä. | Tätä päivämäärää käytetään laskutusaikataulujen luomisen päättymispäivänä. |

Seuraavat suorituskykyilmaisimet ovat käytettävissä projektisopimuksen **sopimuksen suorituskyky** -välilehdessä.

| Field | Sijainti | Kuvaus |
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
| Kirjattu määrä | Projektipohjaisen linjan erittely | Aika: kaikki tähän sopimusriviin liitetyn projektin roolille määritetty ajan kustannusten todellisten arvojen määrä. Kulut: Kaikki tämän kululuokan määrät projektin tosiasiallisissa kustannuskustannuksissa on yhdistetty tähän sopimusriviin. |
| Laskutettu summa | Projektipohjaisen linjan erittely | Jos kyseessä on kiinteähintainen sopimusrivi, tämä kenttä jätetään tyhjäksi yksityiskohtatasolla, ja se näkyy vain sopimusrivin tasolla. Aika- ja materiaalisopimusrivin laskelmat suoritetaan tiedot-tasolla. Tiedot näyttävät kaikkien laskutettujen myyntituottorivien summan tälle sopimusriville, joka on veloitettavissa. |
| Laskutettu määrä | Projektipohjaisen linjan erittely | Jos kyseessä on kiinteähintainen sopimusrivi, tämä kenttä jätetään tyhjäksi yksityiskohtatasolla, ja se näkyy vain sopimusrivin tasolla. Aika- ja materiaalisopimusrivin laskelmat suoritetaan tiedot-tasolla ajalle ja kuluille. Aika: Tämän roolin kaikkien laskutettavien tulorivien laskutettujen tuntien summa tällä sopimusrivillä. Kulut: Kaikki tämän kululuokan määrät projektin tosiasiallisissa kustannuskustannuksissa on yhdistetty tähän sopimusriviin. |
| Sopimuksen arvo | Tuotepohjaiset rivit | Tämän tuotepohjaisen sopimusrivin sopimusriviarvo. |
| Laskutettu summa | Tuotepohjaiset rivit | Kaikkien laskurivien summien yhteissumma tätä tuotepohjaista sopimusriviä vastaan eri laskuille, jotka on luotu tälle palvelusopimukselle. |
| Aiheutuneet kulut | Tuotepohjaiset rivit | Kaikkien tuotepohjaiseen sopimusriviin kirjattujen kustannustodistusten summa. |
| Käyttökate | Projektipohjaiset rivit | Laskutettu määrä - kustannukset, jotka ovat syntyneet asti päivä määrä/laskutettu summa |
| Odotettu kate | Tuotepohjaiset rivit | (Sopimusrivin arvo - sopimusrivin arvioidut kustannukset)/sopimusrivin arvo |


[!INCLUDE[footer-include](../includes/footer-banner.md)]
