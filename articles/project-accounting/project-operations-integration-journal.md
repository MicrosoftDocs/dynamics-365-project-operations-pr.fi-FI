---
title: Project Operationsin integroinnin kirjauskansio
description: Tässä aiheessa on tietoja integroinnin kirjauskansioiden käyttämisestä Project Operationsissa.
author: sigitac
ms.date: 10/27/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 5e1a455d055fe562a1946cc3b90c8274ef1a4b12
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/14/2022
ms.locfileid: "8582430"
---
# <a name="integration-journal-in-project-operations"></a>Project Operationsin integroinnin kirjauskansio

_**Käytetään:** Project Operationsin resursseihin ja ei-varastoitaviin perustuvissa skenaarioissa_

Aika- ja kulumerkinnät luovat **todellisia** tapahtumia, ja nämä tapahtumat ovat operatiivinen näkymä projektin perusteella suoritetusta työstä. Dynamics 365 Project Operationsin avulla kirjanpitäjät saavat työkalun, jolla he voivat tarkistaa tapahtumia ja oikaista kirjanpitomääritteitä tarvittaessa. Kun tarkistus ja oikaisut on tehty, tapahtumat kirjataan projektin alakirjanpitoon ja pääkirjanpitoon. Kirjanpitäjä voi suorittaa näitä aktiviteetteja käyttämällä **Project Operationsin integraatio** -kirjauskansiota (**Dynamics 365 Finance** > **Projektinhallinta ja kirjanpito** > **Kirjauskansiot** > **Project Operations -integraatio** -kirjauskansio.

![Työnkulku integroinnin kirjauskansiossa.](./media/IntegrationJournal.png)

### <a name="create-records-in-the-project-operations-integration-journal"></a>Tietueiden luominen Project Operationsin integroinnin kirjauskansiossa

Project Operationsin integroinnin kirjauskansion tietueet luodaan kausittaisella **Tuo valmistelutaulukosta** -prosessilla. Voit suorittaa tämän prosessin valitsemalla **Dynamics 365 Finance** > **Projektinhallinta ja kirjanpito** > **Kausittaiset** > **Project Operationsin integraatio** > **Tuo väliaikaisesta taulusta**. Prosessin voi suorittaa vuorovaikutteisesti tai sen voi määrittää suoritettavaksi taustalla tarpeen mukaan.

Jaksottaisen prosessin suorittamisen aikana löydetään sellaiset todelliset arvot, joita ei ole vielä lisätty Project Operationsin integroinnin kirjauskansioon. Kullekin todelliselle tapahtumalla luodaan kirjauskansion rivi.
Järjestelmä ryhmittelee kirjauskansiorivit erillisiin kirjauskansioihin, jotka perustuvat **Kausiyksikkö Project Operationsin integraatiokirjauskansio** -kentässä valittuun arvoon (**Finance** > **Projektinhallinta ja kirjanpito** > **Määritys** > **Projektinhallinta ja kirjanpitoparametrit**, **Project Operations – Dynamics 365 Customer Engagement** -välilehti). Tämän kentän mahdollisia arvoja:

  - **Päivät**: Todelliset arvot ryhmitetään tapahtumapäivän mukaan. Kullekin päivälle luodaan oma kirjauskansio.
  - **Kuukaudet**: Todelliset arvot ryhmitetään kalenterikuukauden mukaan. Kullekin kuukaudelle luodaan oma kirjauskansio.
  - **Vuodet**: Todelliset arvot ryhmitetään kalenterivuoden mukaan. Kullekin vuodelle luodaan oma kirjauskansio.
  - **Kaikki**: Kaikki todelliset tapahtuvat sisältyvät samaan integroinnin kirjauskansioon. Jos kirjauskansio ei käytettävissä, kun kausittainen prosessi suoritetaan, esimerkiksi sen vuoksi, että kirjauskansio on kirjaamassa tapahtumia, uusi kirjauskansio luodaan.

Kirjauskansion rivit luodaan projektin todellisten arvojen perusteella. Seuraavassa luettelossa on muutamia tärkeitä oletus- ja muunnossääntöjä:

  - Kullakin projektin todellisella tapahtumalla on rivi Project Operationsin integroinnin kirjauskansiossa. Ajan ja materiaalin laskutustyypin kustannukset ja laskuttamattomat myyntitapahtumat näytetään erillisillä riveillä.
  - **Päivämäärä**-kenttä ilmaisee tapahtumapäivän. **Kirjanpitopäivämäärä**-kenttä ilmaisee päivämäärän, jolloin tapahtuma kirjattiin kirjanpitoon. Jos kirjanpitopäivämäärä on [suljetulla tilikaudella](/dynamics365/finance/general-ledger/close-general-ledger-at-period-end) ja parametri **Määritä kirjauspäivä automaattisesti avoimeen kirjanpidon kauteen** on määritetty **Projektinhallinnan ja kirjanpidon parametrit** -sivun **Rahoitustoiminta**-välilehdessä, järjestelmä oikaisee tapahtumapäivämäärän seuraavan avoimen kirjanpitokauden ensimmäiseen päivään.
  - **Tosite**-kentässä on jokaisen todellisen tapahtuman tositenumero. Tositenumerosarja määritetään **Projektinhallinnan ja kirjanpidon parametrit** -sivun **Numerosarjat**-välilehdessä. Kullekin riville määritetään uusi numero. Kun tosite on kirjattu, kustannusten ja laskuttamattoman myyntitapahtuman suhdetta voi tarkastella valitsemalla **Liittyvät tositteet** **Tositetapahtuma**-sivulla.
  - **Luokka**-kenttä ilmaisee projektitapahtuman ja oletusarvot liittyvän projektin todellisen arvon tapahtumaluokan perusteella.
    - Jos **Tapahtumaluokka** määritetään projektin todellisessa arvossa ja annetussa yrityksessä on liittyvä **projektiluokka**, luokan oletusarvona on tämä projektiluokka.
    - Jos **tapahtumaluokkaa** ei ole määritetty projektin toteutuneissa arvoissa, järjestelmä käyttää **Projektiluokan oletukset** -kentässä määritettyä arvoa **Project Operations – Dynamics 365 Customer Engagement**-välilehdessä **Projektinhallinnan ja kirjanpidon parametrit** -sivulla.
  - **Resurssi**-kenttä ilmaisee tähän tapahtumaan liittyvän projektiresurssin. Resurssia käytetään viitteenä projektin laskuehdotuksissa asiakkaille.
  - **Valuuttakurssi**-kentän oletusarvo on Dynamics 365 Financessa määritetty **valuutan vaihtokurssi**. Jos vaihtokurssimääritys puuttuu kausittainen **Tuo valmistelusta** -prosessi ei lisää tietuetta kirjauskansioon ja työn suorituslokiin lisätään virhesanoma.
  - **Rivin ominaisuus** -kenttä ilmaisee laskutustyypin projektin todellisissa arvoissa. Rivin ominaisuuden ja laskutustyypin yhdistämismääritys määritetään **Project Operations – Dynamics 365 Customer Engagement** -välilehdessä **Projektinhallinta ja kirjanpitoparametrit** -sivulla.

Project Operationsin integroinnin kirjauskansion riveillä voidaan päivittää vain seuraavat kirjanpitomääritteet:

- **Laskutuksen arvonlisäveroryhmä** ja **Laskutusnimikkeen arvonlisäveroryhmä**
- **Taloushallinnon dimensiot** (**Jaa summat** -toimintoa käytettäessä)

Vaikka integroinnin kirjauskansion rivejä voi poistaa, kirjaamattomat rivit lisätään kuitenkin kirjauskansioon uudelleen, kun kausittainen **Tuo valmistelusta** -prosessi suoritetaan uudelleen.

Kun integroinnin kirjauskansio kirjataan, projektin alakirjanpito- ja kirjanpitotapahtumat luodaan. Niitä käytetään myöhemmin asiakkaan laskutuksessa, tuloutuksessa ja taloushallinnon raportoinnissa.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
