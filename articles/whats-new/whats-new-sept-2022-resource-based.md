---
title: Uudet ominaisuudet, syyskuu 2022 – Project Operations resursseihin ja ei-varastoitaviin perustuvissa skenaarioissa
description: Tässä artikkelissa on tietoja Microsoft Dynamics 365 Project Operationsin resursseihin ja ei-varastoitaviin perustuvissa skenaarioissa syyskuussa 2022 julkaistussa versiossa saatavilla olevista laatupäivityksistä.
author: ramagadu
ms.date: 09/28/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: ramagadu
ms.openlocfilehash: 04b5f2f8223cdc80028860dd880dde314be244eb
ms.sourcegitcommit: b3a70bc4f2850cff5c2b7114cff7bd61ec298143
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/06/2022
ms.locfileid: "9634801"
---
# <a name="whats-new-september-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>Uudet ominaisuudet, syyskuu 2022 – Project Operations resursseihin ja ei-varastoitaviin perustuvissa skenaarioissa

_**Käytetään:** Project Operationsin resursseihin ja ei-varastoitaviin perustuvissa skenaarioissa_

Tämä artikkeli koskee seuraavia Microsoft Dynamics 365 Project Operationsin osia ja versioita:

- Project Operations Dataversessa ympäristöversio 4.46.0.60
- Projektinhallinta ja kirjanpito Dynamics 365 Finance -ympäristön versiossa 10.0.29

## <a name="features-included-in-this-release"></a>Tähän julkaisuun sisältyvät ominaisuudet

| Ominaisuusalue | Ominaisuuden nimi | Lisätietoja |
| --- | --- | --- |
| Mahdollisuuksien hallinta | **Tarjousten muutokset ja aktivointi**<br>Project Operations tukee kokonaisvaltaisesti myyntiprosessia. Projektitarjoukset voidaan aktivoida ilmaisemaan tila, jossa tarjous on vain luku -muotoinen ja sitä arvioidaan. Aktivoituja tarjouksia voidaan muuttaa luomalla uusia tarjouksia, joissa on lisäävä versionumero. Aktivoidut projektitarjoukset tai tarjouksen muutokset sulkea voitettuna tai hävittynä. | [Projektitarjouksen aktivoiminen ja muuttaminen](/dynamics365/project-operations/sales/activation-and-revision) |
| Laskutus ja hinnoittelu | **Aikavyöhykkeestä riippumaton hinnan oletusarvo**<br>Project Operations ottanut käyttöön aikavyöhykkeestä riippumattoman päivämäärä kaikissa projektin todellisissa arvoissa. Uusi **Tapahtuman päivä** -kenttä on nyt käytettävissä kirjauskansion riveillä ja todellisissa arvoissa. Sen avulla voidaan tallentaa päivämäärä, jolloin tapahtuma tapahtui, ilman kyseisen päivämäärän muuttamista UCT-aikaan. Tätä päivämäärää käytetään alaspäin suuntautuvissa prosesseissa, kuten hinnan oletusarvossa ja laskun luonnissa. | <p>[Projektipohjaisten arvioiden ja toteutuneiden arvojen kustannusten määrittäminen](/dynamics365/project-operations/pricing-costing/cost-price-resolution)</p><p>[Projektipohjaisten arvioiden ja toteutuneiden myyntihintojen määrittäminen](/dynamics365/project-operations/pricing-costing/sales-price-resolution)</p> |
| Laskutus ja hinnoittelu | **Päivämääräperusteiset hinnan ohitukset Project Operationsissa**<br>Päivämääräperusteiset hinnan ohitukset antavat tavan korvata tai muuttaa hinnastossa tiettyjä hintoja. | [Päivämääräperusteiset hinnan ohitukset](/dynamics365/project-operations/pricing-costing/dateffective_price_overrides) |
| Alihankinta | **Alihankinta ja toimittajan laskujen täsmäytys**<br>Tämä ominaisuus antaa asiakkaille mahdollisuuden luoda alihankintasopimuksia resurssin ajan, kululuokkien projektityössä käytettävien materiaalien ostamiseen. Se antaa myös asiakkaille mahdollisuuden tallentaa talous- ja toimintosovelluksiin toimittajan laskuja, jotka ovat projektipääIliköiden tarkistettavissa Dataversessa. | <p>[Alihankinnan hallinta](/dynamics365/project-operations/pro/subcontracting/managing-subcontracts-overview)</p><p>[Toimittajalaskujen luominen](/dynamics365/project-operations/procurement/vendor-invoicing-concept-and-creation)</p> |
| Aika ja kulu | **Yleinen hyväksyjä**<br>Tämä ominaisuus ottaa käyttöön ISV-toimittajien ja keskitetyn hyväksynnän riippumatta siitä, mikä on projektin tai tiimin jäsenen tila projektissa. | [Suojaus ja hyväksynnät](/dynamics365/project-operations/approvals/approvals-security) |
| Kulujen hallinta | **Mahdollisuus kirjata kuluvelka toimittajan valuuttana**<br>Tämä ominaisuus ottaa käyttöön käteismaksutavan toimittajan valuuttana kirjattavat kuluraportit. | [Mahdollisuus kirjata kuluvelka toimittajan valuuttana](/dynamics365/project-operations/expense/posting-expense-reports#enable-the-ability-to-post-expense-liability-in-vendor-currency-for-cash-payment-method-feature) |
| Projektin hankinta | **Toimittajan maksa kun maksettu -maksut**<br>Tämä ominaisuus antaa mahdollisuuden käyttää Maksa kun maksettu (PWP) -ominaisuutta Project Operationsin ei-varastoitavien ympäristöissä. Sen avulla toimittajan maksut voidaan estää tai pidättää pidätysehtojen mukaisesti siihen saakka, että maksu vastaanotetaan asiakkaalta. | [Toimittajan maksa kun maksettu -maksut](/dynamics365/project-operations/procurement/pay-when-paid) |
| Projektin hankinta | **Projektin ostoehdotukset**<br>Tämä ominaisuus antaa käyttäjille mahdollisuuden luoda projektiin liittyviä ostotilauksissa niissä yrityksissä, joissa Project Operationsin Dynamics 365 Customer Engagement -integrointi on otettu käyttöön. Projekti ostotilauksia voidaan käyttää kirjaamaan ei-varastoitavat materiaalihankinnat projektiin hankintaosaston henkilötyypin perusteella. Projektin ostotilauksia ei synkronoida Dataverseen. Virtuaalientiteetin avulla projektin ostotilausrivit voidaan kuitenkin näyttää Dataversessä projektipäällikön tiedoissa. Projektiin liittyvän toimittajan laskun kustannus integroidaan Dataversen Projektin todelliset arvot -entiteettiin. Projektikustannus kirjataan projektin alareskontraan käyttämällä Project Operationsin integrointikirjauskansiota. | |
|Projektin suunnittelu ja seuranta|**Projektiaikataulun ohjelmointirajapintojen käyttö toimintojen suorittamiseen aikataulutusentiteeteillä** </br> </br>Resurssien delegoinnin jaksottumisen muokkausrajapinnan avulla sovelluskehittäjät määrittävät ohjelmoimalla tehtävän vastuullisen henkilön työt kaikilla tuetuilla päivämääräväleillä tarkempaa aikavaiheistetun työmäärän suunnittelua varten.|[Projektiaikataulun ohjelmointirajapintojen käyttö toimintojen suorittamiseen aikataulutusentiteeteillä](/dynamics365/project-operations/project-management/schedule-api-preview)|

## <a name="project-operations-dual-write-maps-updates"></a>Project Operationsin kaksoiskirjoituskarttojen päivitys

Seuraavassa taulukossa on esitetty Project Operationsin syyskuun 2022 julkaisuun muutetut tai lisätyt kaksoiskirjoituksen yhdistämismääritykset.

| Entiteetin yhdistämismääritys | Päivitetty versio | Kommentit |
| -------------- | ------------------- | ------------|
| Project Operations -integroinnin todelliset arvot (msdyn_actuals) | 1.0.0.15 | Tämä määritys tukee alihankintasopimuksen todellisten arvojen käsittelyä Project Operationsin avulla resurssipohjaisissa skenaariossa. |
| Project Operationsin integrointiprojektin toimittajalaskun vientientiteetti (msdyn_projectvendorinvoices) | 1.0.0.2 | Tämä määritys tukee alihankintasopimuksen todellisten arvojen käsittelyä Project Operationsin avulla resurssipohjaisissa skenaariossa. |
| Project Operationsin integrointiprojektin toimittajalaskurivin vientientiteetti (msdyn_projectvendorinvoicelines) | 1.0.0.5 | Tämä määritys tukee alihankintasopimuksen todellisten arvojen käsittelyä Project Operationsin avulla resurssipohjaisissa skenaariossa. |

Suorita aina ympäristön kartan uusin versio ja ota käyttöön kaikki taulukkokartat, kun päivität Project Operations Dataverse -ratkaisua ja rahoitusratkaisun versiota. Jotkin ominaisuudet ja toiminnot eivät ehkä toimi oikein, jos kartan uusinta versiota ei ole aktivoitu. Voit tarkastella kartan aktiivista versiota **Kaksoiskirjoitus**-sivun **Versio**-sarakkeessa. Voit aktivoida kartan uuden version valitsemalla **Taulukkokartan versiot**, valitsemalla uusimman version ja tallentamalla sitten valitun version. Jos olet mukauttanut valmista taulukkokarttaa, voit käyttää muutokset uudelleen. Lue lisätietoja kohdasta [Ratkaisun elinkaaren hallinta](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Jos kartan käynnistämisen yhteydessä tulee ongelma, seuraa ohjeita [Puuttuvien taulukkosarakkeiden ongelma kartoissa](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) -osassa kaksoiskirjoituksen vianmääritysoppaassa.

## <a name="quality-updates"></a>Laatupäivitykset

### <a name="project-operations-on-dataverse"></a>Project Operations Dataversessä

| Ominaisuusalue | Viitenumero | Laatupäivitys |
| --- | --- | --- |
| Laskutus ja hinnoittelu | 2754422 | Materiaali- ja kuluarviot eivät siirry Financeen, kun projektin kopioidaan Dataversessa. |
| Aika ja kulu | 2787409 | Muu kuin hyväksytty hyväksyjä voi hyväksyä muun kuin projektin aikamerkinnän. |
| Mahdollisuuksien hallinta | 2788907 | Päivitetty virhesanoma, joka koskee merkintöjä sisältävien tilausrivien yksilöllisyyden tarkistusta. |
| Aika ja kulu | 2842253 | Aikahyväksynnän tyhjäarvoisen poikkeuksen käsittely. |
| Laskutus ja hinnoittelu | 2844181 | Korrelaatiotunnuksen hakuvirhe estää laskun luonnin. |
| Laskutus ja hinnoittelu | 2876628 | Tarjousrivin tiedot, sopimusrivin tiedot – arvion hinnaston ratkaisussa on käytettävä hinnaston vanhoja päivämäärävälikenttiä. |
| Alihankinta | 2893222 | Jos alihankintariville ei ole määritetty roolia, kyseisen rivin valinnan pitäisi olla mahdollista kaikille ryhmän jäsenille roolista riippumatta. |

### <a name="project-management-and-accounting-in-finance"></a>Projektinhallinta ja kirjanpito Financessa

Lisätietoja tähän päivitykseen liittyvistä virheenkorjauksista saa kirjautumalla sisään Microsoft Dynamics Lifecycle Servicesiin ja tarkastelemalla [tietokanta-artikkelia](https://fix.lcs.dynamics.com/Issue/Details?bugId=726559).

## <a name="features-turned-on-by-default-in-upcoming-release"></a>Tulevassa julkaisussa oletusarvoisesti käytössä olevat ominaisuudet

Seuraavassa taulukossa luetellaan ominaisuudet, jotka ovat oletusarvoisesti käytössä versiossa 10.0.30. Useimmat automaattisesti käyttöön otetut ominaisuudet voi ottaa käyttöön [ominaisuuksienhallinnassa](/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview). Tulevaisuudessa jotkin automaattisesti käyttöönotetut ominaisuudet voidaan poistaa ominaisuuksien hallinnasta, ja niistä tulee pakollisia. Tämä muutos varmistaa, että asiakkaat käyttävät nykyistä toiminnallisuutta. Näin parannukset voidaan ottaa käyttöön nykyisessä toiminnallisuudessa, kun ne lisätään. Ominaisuudet otetaan automaattisesti käyttöön korkeintaan kerran vuodessa, jos niitä ei ole määritetty olennaisiksi.

| Ominaisuuden nimi | Käyttöönottopäivämäärä | Ominaisuuden lisäysajankohta | Ominaisuuden tila | Moduuli |
| --- | --- | --- |--- |--- |
| Asynkronisen toiminnon ottaminen käyttöön, kun käyttäjän vaihdeltava synkronoinnin ja asynkronisten toimintojen välillä | 21. lokakuuta 2022 | 9. huhtikuuta 2021 | Käytössä oletusarvoisesti | Kulujen hallinta |
| Pakollisten kuittien kulukäytännön arviointi | 21. lokakuuta 2022 | 20. joulukuuta 2021 | Käytössä oletusarvoisesti | Kulujen hallinta |
| Työntekijät delegoimalla luotujen kuluraporttien luettelonäkymä | 21. lokakuuta 2022 | 19. helmikuuta 2020 | Käytössä oletusarvoisesti | Kulujen hallinta |
| Kilometrikorvauksen yhteismäärän laskenta tilikauden mukaan | 21. lokakuuta 2022 | 10. toukokuuta 2022 | Käytössä oletusarvoisesti | Kulujen hallinta |
