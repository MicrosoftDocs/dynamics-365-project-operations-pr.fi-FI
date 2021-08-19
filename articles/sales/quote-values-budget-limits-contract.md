---
title: Projektitarjouksen asetukset
description: Tässä aiheessa on tietoja projektitarjouksiin vaikuttavista tiedoista ja asetuksista.
author: rumant
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 3f11188a47c6f0c7de9fb591fd3be3e22f8f7d842fb6d075c1f43d9baea4d225
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/06/2021
ms.locfileid: "6993462"
---
# <a name="header-details-for-project-based-quotes"></a>Projektipohjaisten tarjousten otsikkotiedot

_**Käytetään:** Project Operationsin resursseihin ja ei-varastoitaviin perustuvissa skenaarioissa_


Tässä artikkelissa selitetään projektitarjousta koskevat tiedot. Tämä sisältää kaikkiin tarjousriveihin vaikuttavat asetukset sekä tiedot tarjouksesta, joka on koottu yhteen kaikkien rivinimikkeiden kanssa, jotta projektitarjouksen suorituskykyilmaisimia voidaan tuottaa.

Seuraavassa taulukossa on luettelo projektitarjouksen yhteenvetotietokentistä, jotka ovat yksilöllisiä Dynamics 365 Project Operationsissa tai joiden toimintatavoissa on tärkeitä muutoksia Dynamics 365 Salesin tarjouksista.

| **Kenttä** | **Sijainti** | **Kuvaus** | **Loppupään vaikutus** |
| --- | --- | --- | --- |
| Laji | Yhteenveto-välilehti (piilotettu) | Tässä asetusjoukkokentässä on seuraavat vaihtoehdot:</br>– Työperusteinen (käytettävissä vain, kun Project Operations on asennettu)</br>– Nimikepohjainen (käytettävissä vain, kun Project Operations ja Sales on asennettu)</br>– Palvelun ylläpitoon perustuva (käytettävissä, kun Dynamics 365 Field Service on asennettu) | Kun käytät Project Operations -sovellusta, tämän kentän arvoksi määritetään automaattisesti **Työperusteinen**. Tämä luokittelee tarjouksen projektipohjaksi tarjoukseksi. Tarjouksen on oltava projektipohjainen, jotta kaikki projektikohtaiset laajennukset ja toiminnot voidaan ottaa käyttöön. |
| Omistava yritys | Yhteenveto | Oikeushenkilö, joka vastaa tähän tarjoukseen liittyvän projektin / liittyvien projektien kertyvistä kustannuksista ja tuotosta. Kun mahdollisuudesta luodaan tarjous, tämä kenttä kopioidaan mahdollisuuden vastaavasta kentästä. | Omistava yritys vastaa oikeushenkilön käsitettä Project Operationsin **Projektinhallintaja kirjanpito** -moduulissa. Kaikki tästä projektista kertyvät kustannukset ja tuotot kirjataan omistavan yrityksen kirjanpitoon. |
| Mahdollinen asiakas | Yhteenveto-välilehti | Viittaus asiakkaan yritykseen tai asiakastietueeseen. Projektitarjouksesessa viitattava kelvollinen asiakas täytyy määrittää asiakkaaksi tarjouksen omistavassa yrityksessä. Omistava yritys näyttää oikeushenkilöiden luettelon ja nämä määritetään Project Operationsin **Projektinhallintaja kirjanpito** -moduulissa. Kun mahdollisuudesta luodaan tarjous, tämä kenttä kopioidaan mahdollisuuden vastaavasta kentästä. | Projektitarjouksen valuuttana käytetään oletusarvona asiakkaan valuuttaa. Tätä ei voi kuitenkaan muuttaa ennen kuin tarjous on tallennettu. |
| Asiakaspäällikkö | Yhteenveto-välilehti | Tämä sopimuksen asiakaspäällikön nimi. Kun mahdollisuudesta luodaan tarjous, tämä kenttä kopioidaan mahdollisuuden vastaavasta kentästä. | Asiakkuuspäällikkö vastaa asiakassuhteen hallinnasta koko projektin elinkaaren ajan. Asiakkuuspäällikköön sidotun varattavan resurssin tietueen perusteella sopimusyksikön oletusarvona on projektitarjous.|
| Sopimusyksikkö | Yhteenveto-välilehti | Organisaatioyksikkö, joka on vastuussa tähän tarjoukseen liittyvän projektin tai liittyvien projektien toimituksesta. Kun mahdollisuudesta luodaan tarjous, tämä kenttä kopioidaan mahdollisuuden vastaavasta kentästä. | Sopimusyksikkö on sen yrityksen osasto, joka suorittaa projektit, kun sopimus on tehty. Jokaisella sopimusyksiköllä on valuutta, ja tätä valuuttaa käytetään projektin toteutuksen aikana arvioitujen ja todellisten kustannusten raportoimiseen. |
| Tuotehinnasto | Yhteenveto-välilehti | Tämä on hinnasto, jota käytetään tuotepohjaisten tarjousrivien oletushintoihin. Tämän kentän asetusluettelo näyttää hinnastojen luettelon, jossa hinnaston valuutta vastaa tarjouksen valuuttaa. Kun mahdollisuudesta luodaan tarjous, tämä kenttä kopioidaan mahdollisuuden vastaavasta kentästä. Tämän mahdollisuuden kentän oletusarvona on asiakastietue, mutta sitä voi muuttaa. | Kun tarjous on voitettu, kentän arvo kopioidaan luotuun projektisopimukseen. |
| Valuutta | Yhteenveto-välilehti | Tämä ilmaisee valuutan, jota käytetään tämän sopimuksen arvon raportoinnissa. Se on myös valuutta, jossa asiakasta laskutetaan sopimuksesta, jos sopimus voitetaan. Kun mahdollisuudesta luodaan tarjous, tämä kenttä kopioidaan mahdollisuuden vastaavasta kentästä. Tämän mahdollisuuden kentän oletusarvona on asiakastietue, mutta käyttäjä voi muuttaa sitä.  | Kun tarjous on tallennettu, tätä kenttää ei voi enää muokata. Tätä käytetään tarjouksen tuote- ja projektihinnastojen oletusarvoihin. Tarjouksen valuutan avulla täsmäytetään hinnaston valuutta. |
| Ei-ylitettävä rajoitus | Yhteenveto-välilehti | Tämä tarkoittaa lopullisen arvo neuvoteltua ylärajaa, jonka asiaks hyväksyy tässä sopimuksessa. | Tätä ylärajaa arvioidaan suorituksen aikana, ja sitä voi käyttää kaikissa tähän sopimukseen liittyvissä rivinimikkeissä ja projekteissa. |
| Pyydetty toimituspäivä | Yhteenveto-välilehti | Kun mahdollisuudesta luodaan tarjous, tämä kenttä kopioidaan mahdollisuuden vastaavasta kentästä. | Tätä päivämäärää käytetään laskutusaikataulujen luomisen päättymispäivänä. |

Alla on projektitarjouksessa käytettävissä olevat välilehdet ja suorituskykyilmaisimet, jotka löytyvät vain Project Operationsista tai joissa on merkittäviä muutoksia verrattuna Salesin tarjouksiin:

| **Kenttä** | **Sijainti** | **Kuvaus** |
| --- | --- | --- |
| Kannattavuusanalyysi | Tarjouksen välilehti | Välilehedessä näkyvät seuraavat mittarit:</br>– Veloitettavat kokonaiskustannukset</br></br>– Ei-veloitettavat kokonaiskustannukset</br>– Kokonaistuotto</br>– Kokonaistuotto (perusvaluutta)</br>– Käyttökate</br>– Muutettu käyttökate|
| Vertailu asiakasodotuksiin | Tarjouksen välilehti | Tässä välilehedessä näkyvät seuraavat mittarit:</br>– Arvioitu valmistuminen</br>– Pyydetty valmistuminen</br>– Asiakasbudjetti</br>– Tarjouksen arvo |
| Tarjousanalyysi | Tarjouksen välilehti | Tässä välilehdessä on yhteenveto projektitarjouksen tärkeimmistä suorituskykyilmaisimista</br>– Asiakkaiden odotusten vertailu budjettiin ja aikatauluun</br>– Käyttökate</br>– Muutettu käyttökate |


[!INCLUDE[footer-include](../includes/footer-banner.md)]
