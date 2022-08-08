---
title: Project Operationsin integroinnin kirjauskansio
description: Tässä artikkelissa on tietoja integroinnin kirjauskansioiden käyttämisestä Project Operationsissa.
author: sigitac
ms.date: 06/29/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: d6f1709c4bf44cfd45516d9ac74b30d4817bb653
ms.sourcegitcommit: a5a1d81d2fe0a6f684e79859fcddf45e913d76bc
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 07/01/2022
ms.locfileid: "9106271"
---
# <a name="integration-journal-in-project-operations"></a>Project Operationsin integroinnin kirjauskansio

_**Käytetään:** Project Operationsin resursseihin ja ei-varastoitaviin perustuvissa skenaarioissa_

Aika-, kulu-, maksu- ja materiaalimerkinnät luovat **todellisia** tapahtumia, ja nämä tapahtumat ovat operatiivinen näkymä projektin perusteella suoritetusta työstä. Dynamics 365 Project Operationsin avulla kirjanpitäjät saavat työkalun, jolla he voivat tarkistaa tapahtumia ja oikaista kirjanpitomääritteitä tarvittaessa. Kun tarkistus ja oikaisut on tehty, tapahtumat kirjataan projektin alakirjanpitoon ja pääkirjanpitoon. Kirjanpitäjä voi suorittaa näitä aktiviteetteja käyttämällä **Project Operationsin integraatio** -kirjauskansiota (**Dynamics 365 Finance** > **Projektinhallinta ja kirjanpito** > **Kirjauskansiot** > **Project Operations -integraatio** -kirjauskansio.

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

Integrointikirjauskansion rivejä voi poistaa. Vaikka integrointikirjauskansion rivejä voi poistaa, kirjaamattomat rivit lisätään kuitenkin kirjauskansioon uudelleen, kun kausittainen **Tuo valmistelusta** -prosessi suoritetaan uudelleen.

### <a name="post-the-project-operations-integration-journal"></a>Project Operations -sovelluksen integrointikirjauskansion kirjaaminen

Kun integroinnin kirjauskansio kirjataan, projektin alakirjanpito- ja kirjanpitotapahtumat luodaan. Niitä käytetään myöhemmin asiakkaan laskutuksessa, tuloutuksessa ja taloushallinnon raportoinnissa.

Valittu Project Operationsin integrointikirjauskansio voidaan kirjata käyttämällä Project Operationsin integrointikirjauskansion sivun **Kirjaa**-kohtaa. Kaikki kirjauskansiot voidaan kirjata automaattisesti suorittamalla prosessi kohdassa **Jaksoittaiset** > **Project Operationsin integrointi** > **Kirjaa Project Operationsin integrointikirjauskansio**.

Kirjaus voidaan tehdä vuorovaikutteisesti tai eränä. Huomaa, että kaikki kirjauskansiot, joissa on yli 100 riviä, kirjataan automaattisesti eränä. Jos useita rivejä sisältävät kirjauskansiot on kirjattu eränä hyvän suorituskyvyn takaamiseksi, ota käyttöön **Kirjaa Project Operationsin integrointikirjauskansio käyttämällä useita erätehtäviä** -ominaisuus **Ominaisuuksien hallinta** -kohdassa. 

#### <a name="transfer-all-lines-that-have-posting-errors-to-a-new-journal"></a>Kaikkien kirjausvirheitä sisältävien rivien siirto uuteen kirjauskansioon

> [!NOTE]
> Jos haluat käyttää tätä ominaisuutta, ota käyttöön **Siirrä kaikki kirjausvirheitä sisältävät rivit uuteen Project Operationsin integrointikirjauskansioon** -ominaisuutta **Ominaisuuksien hallinta** -työtilassa.

Kun Project Operationsin integrointikirjauskansioon kirjataan, järjestelmä tarkistaa kirjauskansion jokaisen rivin. Järjestelmä kirjaa kaikki virheettömät rivit ja luo uuden kirjauskansion kaikille riveille, joissa on kirjausvirheitä. Jos haluat tarkastella kirjauskansioita, joissa on kirjausvirheitä sisältäviä rivejä, siirry kohtaan **Projektinhallinta ja kirjanpito** > **Kirjauskansiot** > **Project Operationsin integrointikirjauskansio** ja suodata kirjauskansiot käyttämällä **Alkuperäinen kirjauskansio** -kenttää.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
