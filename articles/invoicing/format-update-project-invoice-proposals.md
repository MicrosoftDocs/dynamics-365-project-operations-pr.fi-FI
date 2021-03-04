---
title: Projektin laskuehdotusten hallinta
description: Tässä aiheessa on tietoja asiakkaille suunnattujen laskujen käsittelystä Project Operationsissa resurssi-/ei-varastoitavissa skenaarioissa.
author: sigitac
manager: Annbe
ms.date: 01/29/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 83e5af60d0a3baf0b59da2a97c6b156ef5b2b7ed
ms.sourcegitcommit: b4298ca4729643c1040ef35dde8c67f829461ce7
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/29/2021
ms.locfileid: "5089233"
---
# <a name="manage-project-invoice-proposals"></a>Projektin laskuehdotusten hallinta

_**Käytetään:** Project Operationsin resursseihin ja ei-varastoitaviin perustuvissa skenaarioissa_

Laskutusosasto voi käsitellä projektilaskuehdotuksia, kun seuraavat kaksi ehtoa täyttyvät:

  - Projektipäällikkö vahvistaa proformalaskun Microsoft Dataversessä.
  - Kaikki proformalaskuun sisältyvät ajan ja materiaalin laskuttamattomat myyntitapahtumat kirjataan Dynamics 365:n **Project Operations -integroinnin** kirjauskansioon.

Suorita projektilaskuehdotus seuraavien vaiheiden mukaisesti Dynamics 365 Financessa.

1. Tarkista aika- ja materiaalitapahtumien laskutustiedot ja kirjaa **Project Operations -integroinnin** kirjauskansioon.
2. Tarkista kiinteähintaisten laskutuksen välitavoitteiden laskutustiedot.
3. Projektin laskuehdotusten tarkistaminen ja muotoileminen.
4. Projektin laskujen kirjaaminen ja tulostaminen.

## <a name="manage-billing-information-in-the-project-operations-integration-journal"></a>Laskutustietojen hallinta Project Operationsin integroinnin kirjauskansion avulla

Projektin kirjanpitäjä tarkistaa ja kirjaa Financeen projektin todelliset arvot, jotka luodaan Dataversessä. Lisätietoja integroinnin kirjauskansioiden käyttämisestä on ohjeaiheessa [Project Operationsin integroinnin kirjauskansio](../project-accounting/project-operations-integration-journal.md).

Toteutuneet kustannukset ja laskuttamattomat toteutuneet myyntisummat lisätään integroinnin kirjauskansioon erillisinä riveinä:

  - Toteutuneiden kustannusten yksikkökustannushinta ja kustannussumma saadaan oletuksena Dataversen projektin toteutuneesta kustannustapahtumasta.
  - Laskuttamattomien myyntitapahtumien yksikkökustannushinta ja myyntisumma saadaan oletuksena Dataversen projektin toteutuneesta laskuttamattomasta myyntitapahtumasta.

### <a name="billing-sales-tax"></a>Laskutuksen arvonlisävero

Laskutuksen arvonlisäverolaskelma määräytyy **Laskutuksen arvonlisäveroryhmä**- ja **Laskutusnimikkeen arvonlisäveroryhmä** -kenttien yhdistelmästä laskuttamattomassa myyntitietueessa **Project Operationsin integroinnin** kirjauskansiossa. Järjestelmä määrittää nämä kenttien oletusarvot **Talous**-välilehden asetusten perusteella (**Projektinhallinta- ja kirjanpitoparametrit** -sivulla).

- **Arvonlisäveromenetelmä** määrittää laskutuksen arvonlisäveroryhmän oletuslogiikan:
  
  - **Projekti**: käyttää projektin laskutuksen arvonlisäveroryhmää aina oletusarvona. Voit tarkastella tai muuttaa projektin laskutuksen oletusarvonlisäveroryhmää valitsemalla **Näytä oletuskirjanpito** -vaihtoehdon **Kaikki projektit** -sivulla.
  - **Projektisopimus**: käyttää projektisopimuksen arvonlisäveroryhmää aina oletusarvona. Voit tarkastella tai muuttaa projektisopimuksen oletusarvonlisäveroryhmää valitsemalla **Näytä oletuskirjanpito** -vaihtoehdon **Projektisopimukset**-sivulla.
  - **Asiakas**: käyttää asiakkaan laskutuksen arvonlisäveroryhmää aina oletusarvona.
  - **Haku**: etsii kaikista edellä mainituista entiteeteistä ja valitsee ensimmäisen käytettävissä olevan arvon. Haku alkaa **Projekti**-entiteetistä, sitten **Projektisopimus**-entiteetistä ja lopuksi **Asiakas**-entiteetistä.

- **Nimikkeen arvonlisäveromenetelmä** määrittää laskutusnimikkeen arvonlisäveroryhmän oletuslogiikan:
  
  - Aika-, kulu- ja maksutapahtumatyypeissä laskutusnimikkeen arvonlisäveroryhmä tulee aina oletusarvona **Projektiluokka**-entiteetistä.
  - Materiaalitapahtumatyypeissä laskutusnimikkeen arvonlisäveroryhmä tulee oletuksena **Nimikkeen arvonlisäveromenetelmä** -asetuksesta, joka määritetään kohdassa **Projektinhallinta- ja kirjanpitoparametrit**. Nimikenumero tulee oletuksena **Julkaistu tuote** -entiteetin nimikkeen arvonlisäveroveroryhmästä. Luokkaa tulee oletuksena **Projektiluokka**-entiteetin nimikkeen arvonlisäveroveroryhmästä.

### <a name="financial-dimensions"></a>Taloushallinnon dimensiot

The financial dimensions for unbilled sales records in the **Project Operations -integroinnin** -kirjauskansion laskuttamattoman myynnin tietueiden talousdimensiot tulevat oletuksena **Projekti** -entiteetistä. Talousdimensioita voi tarkastella ja muuttaa valitsemalla **Jaa summat**. Jos laskuttamattoman myyntitietueen talousdimensioita on muutettava integroinnnin kirjauskansion kirjaamisen jälkeen, mutta ennen kuin proformalasku vahvistetaan, valitse **Kaikki projektit** > **Hallitse** > **Kirjatut tapahtumat**, valitse tapahtuma ja valitse sitten **Prosessi** > **Kirjanpidon oikaisu**.

### <a name="exchange-rates"></a>Valuuttakurssit

Laskuttamattoman tapahtuman valuuttaa Dataversessä käytetään tapahtumavaluuttana Financessa, ja se muunnetaan yrityksen kirjanpitovaluutaksi käyttämällä Financessa määritettyjä valuuttakursseja.


## <a name="manage-the-financial-attributes-of-billing-milestones"></a>Laskutuksen välitavoitteiden taloudellisten määritteiden hallinta 

Kiinteähintaista laskutustapaa käyttävät projektisopimusrivit laskutetaan [kiinteähintaisten välitavoitteiden](../sales/invoice-schedules-contract-line.md#create-a-fixed-price-invoice-schedule-for-a-contract-line) kautta. Projektin kirjanpitäjä voi tarkistaa laskutuksen välitavoitteet Financessa valitsemalla **Projektinhallinta ja kirjanpito** > **Kaikki projektit** > **Hallitse** > **Tilitapahtumat**.

### <a name="billing-sales-tax"></a>Laskutuksen arvonlisävero

**Arvonlisäveroryhmä**- ja **Nimikkeen arvonlisäveroryhmä** -arvojen oletusarvot saadaan asetuksista, kun uusi laskutuksen välitavoite luodaan Dataversessä. Järjestelmä määrittää nämä kenttien oletusarvot **Talous**-välilehden asetusten perusteella (**Projektinhallinta- ja kirjanpitoparametrit** -sivulla).

- **Arvonlisäveromenetelmä** määrittää **laskutuksen arvonlisäveroryhmän** oletuslogiikan:

    - **Projekti** käyttää projektin laskutuksen arvonlisäveroryhmää aina oletusarvona. Voit tarkastella tai muuttaa projektin oletusarvonlisäveroryhmää valitsemalla **Näytä oletuskirjanpito** -vaihtoehdon **Kaikki projektit** -sivulla.
    - **Projektisopimus** käyttää projektisopimuksen arvonlisäveroryhmää aina oletusarvona. Voit tarkastella tai muuttaa projektisopimuksen oletusarvonlisäveroryhmää valitsemalla **Näytä oletuskirjanpito** -vaihtoehdon **Projektisopimukset**-sivulla.
    - **Asiakas** käyttää asiakkaan laskutuksen arvonlisäveroryhmää aina oletusarvona.
    - **Haku**: etsii kaikista tämän luettelon entiteeteistä ja valitsee ensimmäisen käytettävissä olevan arvon. Haku alkaa **Projekti**-entiteetistä, sitten **Projektisopimus**-entiteetistä ja sitten **Asiakas**-entiteetistä.

- **Kiinteähintaisen välitavoitteen nimikkeen arvonlisäveroryhmää** käytetään **Nimikkeen arvonlisäveroryhmä** -kentän oletusarvona.

### <a name="financial-dimensions"></a>Taloushallinnon dimensiot

Kiinteähintaisen laskutuksen välitavoitteen taloushallinnon oletusdimensiot määritetään projektisopimusriveillä. Siirry kohtaan **Projektisopimukset** > **Näytä oletuskirjanpito** ja valitse **Sopimusrivit**-välilehdessä **hinnan sopimusrivi**, ja määritä sitten taloushallinnon dimensioarvot, joita haluat käyttää oletusarvoina.

Projektin kirjanpitäjä voi muokata laskun välitavoitteiden arvonlisäveron ja taloushallinnon dimensiotietoja, kunnes projektilaskuehdotus on luotu.


## <a name="create-project-invoice-proposals"></a>Projektin laskuehdotusten luominen

Projektilaskuehdotuksia voi tarkastella **Projektinhallinta ja kirjanpito** -moduulin kohdassa **Projektilaskut** > **Projektilaskuehdotukset**.

Projektilaskuehdotuksen otsikko luodaan Financessa, kun proformalasku vahvistetaan Dataversessä. Täsmäytyksen helpottamiseksi järjestelmä määrittää Financen projektilaskun ehdotusnumeroksi saman numeron kuin proformalaskun tunnus Dataversessä. Koska proformalaskuja ei välttämättä vahvisteta samassa järjestyksessä kuin ne on luotu, projektilaskuehdotusten numerojärjestyksen Financessa on mahdollistettava numerojen muuttaminen pienemmäksi tai suuremmaksi. Määritä numerojärjestykset seuraavien vaiheiden mukaisesti:

1. Siirry Financessa kohtaan **Organisaation hallinta** > **Numerojärjestykset** > **Numerojärjestykset**.
2. Valitse **Alue**-suodattimessa **Projektit**.
3. Valitse **Viite**-suodattimesta **Laskuehdotus**.
4. Käytä **Yritys**-kenttää suodattaaksesi jokaisen yrityksen, jolla on käytössä Project Operations Dataverse -integrointi.
5. Avaa **Numerojärjestyksen tiedot** ja tee seuraavat asetukset **Yleiset**-välilehdessä:

    - **Salli käyttäjän muutokset: numeron pienentäminen** = **Kyllä**
    - **Salli käyttäjän muutokset: numeron suurentaminen** = **Kyllä**

Järjestelmä lisää projektilaskun ehdotusrivit käyttämällä kausittaista prosessia **Tuo valmistelutaulukosta** (**Projektinhallinta ja kirjanpito** > **Kausittainen** > **Project Operations -integrointi** > **Tuo valmistelutaulukosta**). Voit tehdä tämän joko manuaalisesti tai kausittaisen aikataulun avulla. Järjestelmä ei lisää rivejä laskuehdotusasiakirjaan, ennen kuin kaikki rivit ovat valmiita laskutettavaksi. Aika- ja materiaalitapahtumat ovat valmiita laskutettaviksi vain, jos ne kirjataan **Project Operationsin integroinnin** kirjauskansiolla.

## <a name="format-and-print-invoice-proposals"></a>Laskuehdotusten muotoileminen ja tulostaminen

Projektin kirjanpitäjä voi mukauttaa projektin laskun tulostetta käyttämällä **Laskuehdotuksen muotoilu** -sivua ja tulostushallintaominaisuuksia.

### <a name="format-invoice-proposals"></a>Laskuehdotusten muotoilu

**Laskuehdotusten muotoilu** -sivu mahdollistaa mukautettujen tapahtumaryhmien näyttämisen asiakkaan projektilaskussa.

1. Valitse **Projektilaskuehdotus**-sivulla **Tulosta** > **Laskuehdotuksen muotoilu**.
2. Valitse **Uusi**, jos haluat luoda uuden ryhmittelyn projektilaskun tulostetta varten.
3. Valitse **Erittely/yhteenveto**-kentässä ryhmittelyasetukset:

    - Valitse **Erittely**, jos haluat tulostaa asiakaslaskun tapahtuman tarkat tiedot.
    - Valitse **Yhteenveto**, jos haluat tulostaa asiakaslaskun tapahtuman yhteenvedon.

> [!NOTE]
> **Erittely/yhteenveto**-kentässä **Laskuehdotuksen muotoilu** -sivulla tehty valinta laskun erittelyn tai yhteenvedon tulostamisesta korvaa **Laskun muoto** -kentässä **Laskuehdotukset**-sivulla tehdyn valinnan.

- Valitse tähän osaan sisällytettävät tapahtumarivit **Käytettävissä olevat tapahtumat** -välilehdessä ja valitse sitten **Sisällytä tapahtumat** siirtääksesi ne **Valitut tapahtumat** -välilehteen.
- Voit muuttaa osien järjestystä valitsemalla **Siirrä ylöspäin** ja **Siirrä alaspäin**.
- Valitse **Tulostuksen esikatselu**, jos haluat esikatsella muotoiltua laskua.

### <a name="print-management"></a>Tulostuksen hallinta

Tulostuksen hallinta käyttää erilaisia raporttitiedostoja laskun tulostamiseen, kohteiden määrittämiseen ja laskun alatunnistetekstin mukauttamiseen. Tulostuksen hallinnan voi määrittää moduulitasolla, mutta nämä asetukset voidaan ohittaa tietylle asiakkaalle, palvelusopimukselle tai laskuehdotukselle. Jos haluat käyttää tätä toimintoa **Projektilaskuehdotus**-sivulla, valitse **Tulosta** > **Tulostuksen hallinta**.

Tulostuksen hallinnan asetukset näkyvät puunäkymänä, jossa jokaisella solmutasolla näkyy muutettavissa olevat asiakirjat. Voit delegoida mukautettuja tulosteita moduuli-, asiakas-, palvelusopimus- tai laskuehdotusasiakirjatasolla. Jos haluat muokata alkuperäistä asiakirjan tulostetta, laajenna haluamasi solmu ja valitse **Alkuperäinen nimike**. Valitse **Raportin muoto** -kentässä tulostuksessa käytettävä raportin muoto. Voit käyttää mukautettuja raportin muotoja [Business Document Management -kehyksen](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/analytics/er-business-document-management) avulla.

## <a name="post-invoice-proposals"></a>Laskuehdotusten kirjaus

Kun lasku on tarkistettu ja muokattu ja laskuehdotuksen rivit ovat hyväksyttävät, tarkista laskun kokonaissummat ja arvonlisävero. Valitse **Tiedot**-ryhmästä **Summat** ja kirjaa sitten lasku valitsemalla **Kirjaa**.

Jos haluat tarkastella laskua ennen kirjausta, poista **Kirjaus**-valintaruudun valinta. **Proforma** tulostetaan laskuun merkkinä esimerkkilaskusta. Tulosta lasku valitsemalla **Tulosta lasku** -valintaruutu.

**Laskuehdotus**-sivun lisäksi laskuehdotukset voi kirjata myös suorittamalla kausittaisen työn **Laskuehdotusten kirjaus**. Tämä työ löytyy kohdasta **Projektinhallinta ja kirjanpito** > **Kausittainen** > **Projektilaskut** > **Laskuehdotusten kirjaus**.

Tällä sivulla näkyvät kaikki laskuehdotukset, jotka ovat valmiita kirjattaviksi. Voit aikatauluttaa laskuehdotusten kirjauksen valitsemalla **Erä**. Aseta **erän käsittelyparametriksi** **Kyllä** ja määritä erän käsittelyn toistuminen valitsemalla **Toistuminen**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]