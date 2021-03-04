---
title: Project Operationsin integroinnin kirjauskansio
description: Tässä aiheessa on tietoja integroinnin kirjauskansioiden käyttämisestä Project Operationsissa.
author: sigitac
manager: Annbe
ms.date: 10/27/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: ffe3373184c8cd776bf3705fd674bedf221d9b77
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/28/2020
ms.locfileid: "4133326"
---
# <a name="integration-journal-in-project-operations"></a>Project Operationsin integroinnin kirjauskansio

_**Käytetään:** Project Operationsin resursseihin ja ei-varastoitaviin perustuvissa skenaarioissa_

Aika- ja kulumerkinnät luovat **todellisia** tapahtumia, ja nämä tapahtumat ovat operatiivinen näkymä projektin perusteella suoritetusta työstä. Dynamics 365 Project Operationsin avulla kirjanpitäjät saavat työkalun, jolla he voivat tarkistaa tapahtumia ja oikaista kirjanpitomääritteitä tarvittaessa. Kun tarkistus ja oikaisut on tehty, tapahtumat kirjataan projektin alakirjanpitoon ja pääkirjanpitoon. Kirjanpitäjä voi tehdä näitä toimintoja **Project Operationsin integroinnin** kirjauskansiossa (**Dynamics 365 Finance** > **Projektinhallinta ja kirjanpito** > **Kirjauskansiot** > **Project Operationsin integroinnin** kirjauskansio.

![Työnkulku integroinnin kirjauskansiossa](./media/IntegrationJournal.png)

### <a name="create-records-in-the-project-operations-integration-journal"></a>Tietueiden luominen Project Operationsin integroinnin kirjauskansiossa

Project Operationsin integroinnin kirjauskansion tietueet luodaan kausittaisella **Tuo valmistelutaulukosta** -prosessilla. Tämä prosessi suoritetaan valitsemalla **Dynamics 365 Finance** > **Projektinhallinta ja kirjanpito** > **Kausittainen** > **Project Operationsin Integrointi** > **Tuo valmistelutaulukosta**. Prosessin voi suorittaa vuorovaikutteisesti tai sen voi määrittää suoritettavaksi taustalla tarpeen mukaan.

Jaksottaisen prosessin suorittamisen aikana löydetään sellaiset todelliset arvot, joita ei ole vielä lisätty Project Operationsin integroinnin kirjauskansioon. Kullekin todelliselle tapahtumalla luodaan kirjauskansion rivi.
Järjestelmä ryhmittelee kirjauskansion rivit erillisiin kirjauskansioihin **Project Operationsin integroinnin kirjauskansion kausiyksikkö** -kentässä valitun arvon perusteella (**Finance** > **Projektinhallinta ja kirjanpito** > **Määritys** > **Projektinhallinnan ja kirjanpidon parametrit**, **Project Operations Dynamics 365 Customer Engagementissa** _ -välilehti). Tämän kentän mahdollisia arvoja:

  - _*Päivät**: Todelliset arvot ryhmitetään tapahtumapäivän mukaan. Kullekin päivälle luodaan oma kirjauskansio.
  - **Kuukaudet**: Todelliset arvot ryhmitetään kalenterikuukauden mukaan. Kullekin kuukaudelle luodaan oma kirjauskansio.
  - **Vuodet**: Todelliset arvot ryhmitetään kalenterivuoden mukaan. Kullekin vuodelle luodaan oma kirjauskansio.
  - **Kaikki**: Kaikki todelliset tapahtuvat sisältyvät samaan integroinnin kirjauskansioon. Jos kirjauskansio ei käytettävissä, kun kausittainen prosessi suoritetaan, esimerkiksi sen vuoksi, että kirjauskansio on kirjaamassa tapahtumia, uusi kirjauskansio luodaan.

Kirjauskansion rivit luodaan projektin todellisten arvojen perusteella. Seuraavassa luettelossa on muutamia tärkeitä oletus- ja muunnossääntöjä:

  - Kullakin projektin todellisella tapahtumalla on rivi Project Operationsin integroinnin kirjauskansiossa. Ajan ja materiaalin laskutustyypin kustannukset ja laskuttamattomat myyntitapahtumat näytetään erillisillä riveillä.
  - **Päivämäärä**-kenttä ilmaisee tapahtumapäivän. **Kirjanpitopäivämäärä**-kenttä ilmaisee päivämäärän, jolloin tapahtuma kirjattiin kirjanpitoon. Jos kirjanpitopäivämäärä on [suljetulla tilikaudella](https://docs.microsoft.com/dynamics365/finance/general-ledger/close-general-ledger-at-period-end) ja parametri **Määritä kirjauspäivä automaattisesti avoimeen kirjanpidon kauteen** on määritetty **Projektinhallinnan ja kirjanpidon parametrit** -sivun **Rahoitustoiminta**-välilehdessä, järjestelmä oikaisee tapahtumapäivämäärän seuraavan avoimen kirjanpitokauden ensimmäiseen päivään.
  - **Tosite**-kentässä on jokaisen todellisen tapahtuman tositenumero. Tositenumerosarja määritetään **Projektinhallinnan ja kirjanpidon parametrit** -sivun **Numerosarjat**-välilehdessä. Kullekin riville määritetään uusi numero. Kun tosite on kirjattu, kustannusten ja laskuttamattoman myyntitapahtuman suhdetta voi tarkastella valitsemalla **Liittyvät tositteet** **Tositetapahtuma**-sivulla.
  - **Luokka**-kenttä ilmaisee projektitapahtuman ja oletusarvot liittyvän projektin todellisen arvon tapahtumaluokan perusteella.
    - Jos **Tapahtumaluokka** määritetään projektin todellisessa arvossa ja annetussa yrityksessä on liittyvä **projektiluokka**, luokan oletusarvona on tämä projektiluokka.
    - Jos **tapahtumaluokkaa** ei ole määritetty projektin todellisessa arvossa, järjestelmää käyttää **Projektinhallinnan ja kirjanpidon parametrit** -sivun **Dynamics 365 Customer Engagementin Project Operations** -välilehden **Projektiluokan oletusarvot** -kentän arvoa.
  - **Resurssi**-kenttä ilmaisee tähän tapahtumaan liittyvän projektiresurssin. Resurssia käytetään viitteenä projektin laskuehdotuksissa asiakkaille.
  - **Vaihtokurssi**-kenttä saa oletusarvon Dynamics 365 Financessa määritetystä **valuutan vaihtokurssista**. Jos vaihtokurssimääritys puuttuu kausittainen **Tuo valmistelusta** -prosessi ei lisää tietuetta kirjauskansioon ja työn suorituslokiin lisätään virhesanoma.
  - **Rivin ominaisuus** -kenttä ilmaisee laskutustyypin projektin todellisissa arvoissa. Rivin ominaisuuden ja laskutustyypin yhdistäminen määritetään **Projektinhallinnan ja kirjanpidon parametrit** -sivun **Dynamics 365 Customer Engagementin Project Operations** -välilehdessä.

Project Operationsin integroinnin kirjauskansion riveillä voidaan päivittää vain seuraavat kirjanpitomääritteet:

- **Laskutuksen arvonlisäveroryhmä** ja **Laskutusnimikkeen arvonlisäveroryhmä**
- **Taloushallinnon dimensiot** (**Jaa summat** -toimintoa käytettäessä)

Vaikka integroinnin kirjauskansion rivejä voi poistaa, kirjaamattomat rivit lisätään kuitenkin kirjauskansioon uudelleen, kun kausittainen **Tuo valmistelusta** -prosessi suoritetaan uudelleen.

Kun integroinnin kirjauskansio kirjataan, projektin alakirjanpito- ja kirjanpitotapahtumat luodaan. Niitä käytetään myöhemmin asiakkaan laskutuksessa, tuloutuksessa ja taloushallinnon raportoinnissa.


[!INCLUDE[footer-include](../includes/footer-banner.md)]