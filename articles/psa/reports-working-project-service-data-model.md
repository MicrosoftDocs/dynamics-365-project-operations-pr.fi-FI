---
title: Project Service Automation -tietomallin käsitteleminen
description: Tässä aiheessa on tietoja tietomallin käyttämisestä.
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 37c7b15daa75cc3ba53ff6a3bcc0ab54717aa62d
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/10/2021
ms.locfileid: "6008802"
---
# <a name="working-with-the-project-service-automation-data-model"></a>Project Service Automation -tietomallin käsitteleminen

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]
[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Dynamics 365 Project Service Automation laajentaa muita sovelluskokonaisuuksia ja tuo käyttöön omat Common Data Service -tietomallin kohteensa. Tässä aiheessa kuvataan joitakin tyypillisissä PSA-raportoinnin skenaarioissa kohtaamiasi entiteettejä.

## <a name="reporting-on-opportunities"></a>Mahdollisuuksista raportointi

Project Service Automation laajentaa Dynamics 365 Sales **Mahdollisuus** -entiteettiä lisäämällä kenttiä, jotka mahdollistavat projektipohjaiset skenaariot. Nämä kentät on määritetty rakennenimellä, jonka etuliite on **msdyn\_**. Yksi uusi kenttä, joka on tärkeä PSA-mahdollisuuksien raportoinnissa, **Tilaustyyppi**. Tämän kentän arvo **Työperusteinen** osoittaa, että mahdollisuus on PSA-mahdollisuus. Muita entiteettiin lisättyjä kenttiä ovat **Sopimusorganisaatio**, johon tallennetaan organisaatio, jolle mahdollisuus kuuluu, ja **Asiakkuuspäällikkö**, johon tallennetaan mahdollisuudesta vastuussa olevan asiakkuuspäällikön nimi.

**Mahdollisuusrivi** -entiteetti sisältää myös kenttiä, jotka liittyvät Project Service -palveluun. **Laskutusmenetelmä** osoittaa, laskutetaako mahdollisuusrivi ajan ja materiaalin perusteella vai kiinteähintaisena, ja **Projekti** tallentaa sen projektin nimen, joka tukee mahdollisuutta. Muihin kenttiin, joista voidaan raportoida, tallennetaan kustannus- ja asiakkaan budjettisummat rivinimikkeittäin.

## <a name="reporting-on-quotes"></a>Tarjousten raportointi

PSA laajentaa myynnin **Tarjous**-entiteettiä lisäämällä projektiin liittyviä kenttiä. **Tilaustyyppi** erottaa PSA-tarjoukset muista kuin PSA-tarjouksista. Tämän kentän arvo **Työperusteinen** osoittaa, että tarjous on PSA-tarjous. Muut kentät, joilla voi olla merkitystä PSA-tarjousten raportoinnissa sisältävät summakenttiä, kuten **Laskutettavat kustannukset**, **Ei-laskutettavat kustannukset**, **Käyttökate**, **Arviot** ja **Budjetti**. Muut hyödylliset kentät ilmaisevat, tuottaako tarjous voittoa, valmistuuko se aikataulussa, ja täyttääkö se asiakkaan odotukset budjetista.

PSA laajentaa myös myynnin **Tarjousrivi**-entiteettiä. Eräs kenttä, jonka PSA lisää on **Laskutustapa**, joka osoittaa, kuinka tarjousrivi laskutetaan (ajan ja materiaalien perusteella vai kiinteähintaisesti). Muihin entiteettiin lisättyihin kenttiin tallennetaan tarjousrivin taustalla oleva projekti, laskutus, kustannukset ja budjetti.

PSA lisää myös uusia tarjoukseen liittyviä entiteettiä Dynamics 365- tietomalliin. Seuraavassa on joitakin esimerkkejä.

- **Tarjousrivin tiedot** – tämä entiteetti sisältää tarjousrivin projektiarvion tiedot. Siinä on kaksi tietuetta kutakin tarjousriviä kohti. Yksi tietue tallentaa tarjousrivin kustannukset ja kustannustiedot, ja toinen tietue sisältää tarjousrivin myyntisumman ja myyntitiedot.
- **Tarjousrivin laskutusaikataulu** – tämä entiteetti sisältää tarjousrivin laskutusaikataulun. Tämä aikataulu luodaan tarjousriville määritetyn laskutusvälin perusteella.
- **Tarjousrivin välitavoite** – tämä entiteetti sisältää laskutuksen välitavoitteet kiinteähintaisille tarjousriveille.
- **Tarjousrivin analytiikan yksityiskohdat** – tämä entiteetti sisältää tarjousrivin taloudelliset tiedot. Nämä tiedot voivat olla hyödyllisiä myyntitarjouksista ja arvioiduista kustannuksista raportointia varten useiden dimensioiden mukaan.

Muita entiteettejä, joita PSA lisää tarjouksiin, ovar **Tarjousrivin projektihinnasto**, **Tarjousrivin resurssiluokka** ja **Tarjousrivin tapahtumaluokka**.

![Kaavio, jossa näkyvät tarjous, tarjousrivi ja projektisuhteet](media/PS-Reporting-image2.png "Kaavio, jossa näkyvät tarjous, tarjousrivi ja projektisuhteet")

## <a name="reporting-on-project-contracts"></a>Projektisopimuksista raportointi

PSA laajentaa myynnin **Tilaus**-entiteettiä, jota käytetään, kun projektisopimuksia tallennetaan. Se lisää tärkeän uuden kentän, **Tilaustyypin**, joka osoittaa, että sopimus on PSA-projektisopimus eikä myyntitilaus. Tämän kentän arvo **Työperusteinen** osoittaa, että tilaus on PSA-projektisopimus. Muut uudet kentät, jotka on lisätty **Tilaus**-entiteettiin säilyttävät tietoja kustannuksista, PSA-sopimuksen tilasta ja organisaatiosta, jolle sopimus kuuluu.

PSA laajentaa myös **Myyntitilausrivi**-entiteettiä. Niiden kenttien joukkoon, jotka se lisää, kuuluu kenttiä, joissa säilytetään laskutustapaa (ajan ja materiaalin perusteella tai kiinteähintaisesti), asiakkaan budjettisummat, ja taustaprojekti.

PSA lisää myös uusia entiteettejä, jotka on suunniteltu projektisopimuksia varten. Seuraavassa on joitakin esimerkkejä.

- **Projektisopimusrivin tiedot** – tämä entiteetti sisältää rivikohtaiset tiedot, jotka on koottu sopimusrivisummaan. Ne voivat olla yhtä yksityiskohtaisia kuin rivinimikkeet, jotka luodaan projektiaikataulusta tehtävätasolla.
- **Sopimusrivin laskutusaikataulu** – tämä entiteetti sisältää laskutusaikataulun, joka on luotu sen laskutusvälin perusteella, joka sopimusriville on määritetty.
- **Sopimuksen välitavoite** – tämä entiteetti sisältää laskutuksen välitavoitteet sellaisille sopimusriveille, joilla on kiinteähintainen laskutustapa.

Muita entiteettejä, joita PSA lisää sopimuksiin, ovat **Projektisopimusrivin projektihinnasto**, **Projektisopimusrivin resurssiluokka** ja **Projektisopimusrivin tapahtumaluokka**.

![Kaavio, jossa näkyvät tilaus, tilausrivi ja projektisuhteet](media/PS-Reporting-image3.png "Kaavio, jossa näkyvät tilaus, tilausrivi ja projektisuhteet")

## <a name="reporting-on-projects"></a>Projekteista raportointi

**Projektit** -entiteetti ja siihen liittyvät entiteetit ovat vain PSA-kohteita. **Projekti** on ylätason entiteetti, jonka avulla tallennetaan toimintoihin liittyvä työ ja kustannukset. Seuraavassa on luettelo liittyvistä kohteista:

- **Projektiryhmän jäsen** – tämä entiteetti sisältää tietoja projektiin liitetyistä varattavista resursseista. Nämä resurssit voivat olla yleisiä varattavissa olevia resursseja, tai ne voivat olla nimettyjä varattavia resursseja, joka projektipäällikkö syöttää, tai jotka luodaan projektiaikataulusta.
- **Projektitehtävä** – tämä kohde sisältää tehtävät, jotka muodostavat projektisuunnitelman tai -aikataulun.
- **Resurssien kohdentaminen** – tämä kohde sisältää varattavissa olevan resurssin tehtäväkohdennuksen.
- **Resurssitarve** – tämä kohde sisältää vaatimukset mahdollisille yleisille resurssiryhmän jäsenille.
- **Arvio** ja **Arviorivi** – näillä entiteeteillä on otsikko/rivi-suhde, ja ne sisältävät kuluarvioita projektille. Tehtävien arviot tallennetaan **Resurssiarvio**-entiteettiin.

![Kaavio, jossa näkyvät resurssitarve ja projektisuhteet](media/PS-Reporting-image4.png "Kaavio, jossa näkyvät resurssitarve ja projektisuhteet")

## <a name="reporting-on-resources"></a>Resursseista raportointi

Projektiresurssit käyttävät **Varattava resurssi** entiteettejä kohteesta Universal Resource Scheduling (URS) , jotka jaetaan muiden sovellusten, kuten Microsoft Dynamics 365 Field Service -sovelluksen kanssa. Tässä on luettelo entiteeteistä, joita voi olla tarpeen käyttää raportoitaessa projektin resursseista:

- **Varattava resurssi** – tämä entiteetti edustaa käyttäjää, yhteyshenkilöä, yleistä resurssia, tiliä, ryhmää tai välineistöä, jota käytetään projektitiimissä.
- **Varattavan resurssin ominaisuudet** – tämä entiteetti sisältää resurssin taidot, sertifikaatit tai koulutuksen. Ominaisuuksilla voi olla luokitusarvoja, jotka määritellään luokitusmallissa.
- **Varattavan resurssin luokka** – tämä entiteetti edustaa varattavan resurssin roolia.
- **Varattavan resurssin varaukset** – tämä entiteetti edustaa aikaa, joka on varattu projekteihin tälle resurssille. Jokaisella varauksella on sekä otsikkoentiteetti että rivientiteettejä, ja jokaisella rivillä on tila, joka edustaa varauksen tilaa.

![Kaavio, jossa näkyvät varattavien resurssien ominaisuuksien suhteet](media/PS-Reporting-image5.png "Kaavio, jossa näkyvät varattavien resurssien ominaisuuksien suhteet")

## <a name="reporting-on-actual-transactions"></a>Todellisten tapahtumien raportointi

Kun hyväksyt tuntilomakkeen tai kulun tai laskutat palvelusopimuksen PSA:N kautta, liike tapahtuma tallennetaan **Todellisessa** entiteetissä. Tämä entiteetti voi olla pohjana lähes kaikille PSA:N rahoitukseen liittyville raporteille. **Todellinen** entiteetti tallentaa liiketoimintatapahtuman kustannus- ja myynti tapahtumat. Se sisältää myös monia olennaisia määritteitä.

Kun käsittelet **Todellista** entiteettiä, on tärkeää, että ymmärrät, mitä transaktioita tai tapahtumia kirjataan entiteettiin ja milloin tapahtumat kirjataan. Tässä on tyypillinen virtaus, kun käytät aika merkintöjä (kulutapahtumien virtaus on samankaltainen):

1. Kun aikamerkintä tallennetaan, **Todelliseen** entiteettiin ei luoda tietueita.
2. Kun aikamerkintä lähetetään, **Todelliseen** entiteettiin ei luoda tietueita.
3. Kun aikamerkintä on hyväksytty, **Todelliseen** entiteettiin luodaan yksi tietue ja myös toinen tietue voidaan luoda. Ensimmäiseen tietueeseen tallennetaan aikasyötteen kustannukset. Toinen tietue sisältää aikasyötteen laskuttamattomat myyntisummat. Toinen tietue on riippuvainen projektista, jolle on kohdennettu joko asiakas, tarjous tai sopimusrivi.

    | Asiakirjan päivämäärä | Tapahtumatyyppi | Tapahtumaluokka | Asiakas         | Palvelusopimus   | Resurssi     | Resurssin rooli | Laskutustyyppi | Määrä | Yksikköhinta | Summa |
    |---------------|------------------|-------------------|------------------|------------|--------------|---------------|--------------|----------|------------|--------|
    | 2/3/18        | Kustannus             | Time              | Alpine ski house | Alpine CRM | Aurora Harila | Projektipäällikkö   | Veloitettava   | 8.0      | 50.00      | 400.00 |
    | 2/3/18        | Laskuttamaton myynti   | Time              | Alpine ski house | Alpine CRM | Aurora Harila | Projektipäällikkö   | Veloitettava   | 8.0      | 100.00     | 800.00 |

    Nämä kaksi tietuetta ovat erillisiä, mutta toisiinsa liittyviä tietueita. Ne eivät ole veloituksia tai hyvityksiä.

4. Jos projektiin liittyy sopimus, kun aikakirjaus on laskutettu, **Todelliseen** entiteettiin luodaan kaksi tietuetta lisää. Ensimmäiseksi luodaan laskuttamattomien myyntitietueiden negatiivinen summa. Tämä tietue kumoaa laskuttamattoman myyntitiedon. Seuraavaksi luodaan laskutettavan myynnin tapahtuma. Nämä tietueet ovat jälleen erillisiä, mutta toisiinsa liittyviä tietueita, eivät veloituksia ja hyvityksiä.

    | Asiakirjan päivämäärä | Tapahtumatyyppi | Tapahtumaluokka | Asiakas         | Palvelusopimus   | Resurssi     | Resurssin rooli | Laskutustyyppi | Määrä | Yksikköhinta | Summa   |
    |---------------|------------------|-------------------|------------------|------------|--------------|---------------|--------------|----------|------------|----------|
    | 2/4/18        | Laskuttamaton myynti   | Time              | Alpine ski house | Alpine CRM | Aurora Harila | Projektipäällikkö   | Veloitettava   | - 8,0    | 100.00     | - 800,00 |
    | 2/4/18        | Laskutettu myynti     | Time              | Alpine ski house | Alpine CRM | Aurora Harila | Projektipäällikkö   | Veloitettava   | 8.0      | 100.00     | 800.00   |

**Tapahtuman alkuperä** -entiteetti tallentaa **Todellisen** tietueen alkuperän, ja **Tapahtuman yhteys** -entiteetti tallentaa liittyvät tietueet **Todelliselle** tietueelle. Lisäksi **Todellinen** tietue sisältää viittauksia projektiin, projektisopimukseen (tilaus), varattavissa olevaan resurssiin ja asiakkaaseen.

![Kaavio, jossa näkyvät tapahtuman yhteys, alkuperä ja toteutuneet suhteet](media/PS-Reporting-image6.png "Kaavio, jossa näkyvät tapahtuman yhteys, alkuperä ja toteutuneet suhteet")


[!INCLUDE[footer-include](../includes/footer-banner.md)]