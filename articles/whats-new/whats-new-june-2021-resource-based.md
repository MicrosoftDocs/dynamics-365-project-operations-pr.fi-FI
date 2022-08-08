---
title: Kesäkuun 2021 uudet ominaisuudet – Project Operations resurssien/ei-varastoitavien skenaarioissa
description: Tässä artikkelissa on tietoja Project Operationsin resursseihin ja ei-varastoitaviin perustuvissa skenaarioissa kesäkuun 2021 julkaisussa saatavilla olevista laatupäivityksistä.
author: sigitac
ms.date: 06/14/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: fd745107fa6d50882ebea302d3d2ae0de21b79ad
ms.sourcegitcommit: a798fed5c59e3fefa62cdfa42c852d529b33fd35
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/18/2022
ms.locfileid: "9028171"
---
# <a name="whats-new-june-2021---project-operations-for-resourcenon-stocked-based-scenarios"></a>Kesäkuun 2021 uudet ominaisuudet – Project Operations resurssien/ei-varastoitavien skenaarioissa

_**Käytetään:** Project Operationsin resursseihin ja ei-varastoitaviin perustuvissa skenaarioissa_

Tämä artikkeli koskee seuraavia Dynamics 365 Project Operationsin komponentteja ja versioita:

- Project Operations Dynamics 365 Dataverse -ympäristön versiossa 4.11.0.156 or 4.11.0.164.
- Projektinhallinta ja kirjanpito talous- ja toimintosovellusten ympäristön versiossa 10.0.19.

## <a name="features-included-in-this-release"></a>Tähän julkaisuun sisältyvät ominaisuudet

Tähän julkaisuun sisältyvät seuraavat ominaisuudet:

- Mahdollisuus poistaa [projektilaskun ehdotusrivejä oikaisuskenaarioita](../invoicing/correct-project-invoice-proposals.md) varten.
- Eritetyt kulurivit heijastavat kuluraportin alaluokkien nimiäkuluraportissa [Uudelleen suunnitellut kuluraportit uusilla ominaisuuksilla](../expense/expense-reports-reimagined.md#new-features).
- Maksutapa on käytettävissä uudessa kuluruudussa uutta kulua luotaessa.
- Projektiaikataulun ohjelmointirajapintojen yleinen käytettävyys. Tämän uuden toiminnon avulla asiakkaat voivat suorittaa ohjelmallisesti projektitehtävien, resurssivarausten, tehtävien riippuvuuksien ja projektiryhmän jäsentietueiden luonti-, päivitys- ja poistotoimintoja. Lisätietoja on ohjeaiheessa [Projektiaikataulun ohjelmointirajapintojen käyttö toimintojen suorittamiseen aikataulutusentiteettien kanssa](../project-management/schedule-api-preview.md).

## <a name="project-operations-dual-write-maps-updates"></a>Project Operationsin kaksoiskirjoituskarttojen päivitys

Tässä versiossa ei ole päivityksiä Project Operationsin kaksoiskirjoituskartoille. 

Project Operationsin kaksoiskirjoituskarttojen luettelo ja versiot ovat kohdassa [Project Operationsin kaksi kaksoiskirjoituskarttojen versiot](../environment/resource-dual-write-maps.md).

Suorita aina ympäristön kartan uusin versio ja ota käyttöön kaikki taulukkokartat, kun päivität Project Operations Dataverse -ratkaisua ja talous- ja toimintosovellusratkaisun versiota. Tietyt ominaisuudet ja toiminnot eivät ehkä toimi oikein, jos kartan uusinta versiota ei ole aktivoitu. Kartan aktiivinen versio näkyy **Kaksoiskirjoitus**-sivun **Versio**-sarakkeessa. Aktivoi kartan uusi versio valitsemalla **Taulukkokarttaversiot**, valitsemalla uusin versio ja tallentamalla valittu versio. Jos olet mukauttanut valmiin taulukkokartan, kohdista muutokset uudelleen. Lue lisätietoja kohdasta [Ratkaisun elinkaaren hallinta](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Jos kartan käynnistämisessä on ongelma, noudata kohdan [Puutuvat sarakkeet -ongelma kartoissa](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) ohjeita kaksoiskirjoituksen vianmääritysoppaassa.

## <a name="quality-updates"></a>Laatupäivitykset

### <a name="project-operations-on-dataverse"></a>Project Operations Dataversessä

| **Ominaisuusalue** | **Viitenumero** | **Laatupäivitys** |
| --- | --- | --- |
| Laskutus ja hinnoittelu | 2281417 | Korjattiin laskun automaattisen luontitoiminnon epäonnistuminen laskuaikataulun kautta. |
| Laskutus ja hinnoittelu | 2287835 | Laskun vahvistuksen suorituskyvyn parantaminen. |
| Mahdollisuuksien hallinta | 2222555 | Materiaaliarvioiden laskutettävyys on kopioitava oikein tarjousrivin tietoihin, kun käytetään **tuomista projektiarviosta**. |
| Mahdollisuuksien hallinta | 2223427 | Mukautukset ovat nyt sallittuja toimintoa varten, **GenerateRetainersFromRetainerScheduleOptions**. |
| Mahdollisuuksien hallinta | 2277528 | Korjattiin kiinteä laskutuksen välitavoitteen arvon laskenta projektisopimusriveille, joilla on useita asiakkaita. |
| Projektin suunnittelu ja seuranta | 2226110 | Korjattiin jaksottainen ongelma **Luo vaatimus**-funktiossa **Projektiryhmä**-ruudukossa. |
| Projektin suunnittelu ja seuranta | 2208109 | Käyttäjät eivät voi luoda projektia yhdessä valuutassa, jos siihen liittyvät tehtävät ovat toisessa valuutassa. |
| Projektin suunnittelu ja seuranta | 2258228 | Luettelo kentistä, joiden avulla **Aikataulutus**-entiteettejä voi muokata aikataulutuksen ohjelmointirajapinnan avulla, on päivitetty. |
| Projektin suunnittelu ja seuranta | 2293989 | Oikeat kieli- ja aluekohtaiset asetukset on välitettävä **Projektitehtävät**-ruudukkoon. |
| Resurssienhallinta | 2220493 | Korjattiin **Tehtävä**-ruudukon käyttökokemus, kun resurssipyyntö merkitään nopeasti valmiiksi. |
| Resurssienhallinta | 2330496 | Korjasi **aikataulutaulukoiden** latausongelman. (Laatupäivitys on saatavilla versiossa 4.11.0.164) |
| Aika ja kulu | 2194431 | **Ajansyöttö**-ruudukon on käytettävä viikon alkua, joka on määritetty **Järjestelmäasetuksissa**. |
| Aika ja kulu | 2277311 | Kun olet poistanut arvon **Ajansyöttö**-ruudukon solusta, kohdistin säilyy ruudukossa. |

### <a name="project-management-and-accounting-on-dynamics-365-finance"></a>Projektinhallinta ja kirjanpito Dynamics 365 Financessa

| Ominaisuusalue | Viitenumero | Laatupäivitys |
| --- | --- | --- |
| Projektinhallinta ja kirjanpito | [552976](https://fix.lcs.dynamics.com/Issue/Details/?bugId=552976) | **Lomakemuistiinpanot** ja **Lomakeasetukset** eivät ole näkyvissä **Projektinhallinnan asetuksissa** taloushallinnon yrityksissä, jotka on integroitu Project Operationsin kanssa. |
| Projektinhallinta ja kirjanpito | [527970](https://fix.lcs.dynamics.com/Issue/Details/?bugId=527970) | Arvonlisäveron oletuskuvaus on tyhjä, kun **Kirjaustyyppi** = **Arvonlisävero** projektilaskujen tositteille. |
| Projektinhallinta ja kirjanpito | [565089](https://fix.lcs.dynamics.com/Issue/Details/?bugId=565089) | Kaksinkertaiset tapahtumat kirjataan, kun tehtäväpohjainen laskutus on käytössä Dataversessa Project Operations -integroinnissa. |
| Projektinhallinta ja kirjanpito | [566869](https://fix.lcs.dynamics.com/Issue/Details/?bugId=566869) | Valmistumisprosentti on virheellinen tuoton tunnistuksessa Käytettäessä Project Operations -integrointia. |
| Projektinhallinta ja kirjanpito | [568107](https://fix.lcs.dynamics.com/Issue/Details/?bugId=568107) | Tuottojen jaksotus kaksinkertaistuu odottavan toimittajan laskulle Project Operationsin integroidussa skenaariossa. |
| Projektinhallinta ja kirjanpito | [572370](https://fix.lcs.dynamics.com/Issue/Details/?bugId=572370) | Integrointikirjauskansiota ei voi kirjata, kun tuottoprofiilin säännöksi on määritetty **Ryhmä**-asetukset. |
| Projektinhallinta ja kirjanpito | [573596](https://fix.lcs.dynamics.com/Issue/Details/?bugId=573596) | Ostolaskua ei voi kirjata projektin ostotilauksille, joiden riveillä on useita mittayksiköitä. |
| Projektinhallinta ja kirjanpito | [573637](https://fix.lcs.dynamics.com/Issue/Details/?bugId=573637) | Projektin taloushallinnon oletusdimensiota ei voi päivittää projektien **V2**-tietoentiteetissä. |
| Projektinhallinta ja kirjanpito | [577211](https://fix.lcs.dynamics.com/Issue/Details/?bugId=577211) | Projektin arvioiden luomisen eräprosessi kestää liian kauan. |
| Projektinhallinta ja kirjanpito | [582329](https://fix.lcs.dynamics.com/Issue/Details/?bugId=582329) | Palvelusopimuksen poistaminen poistaa myös asiakkaaseen liittyvän osoitteen. |
| Matka ja kulut | [514930](https://fix.lcs.dynamics.com/Issue/Details/?bugId=514930) | Kuluraportin hyväksynnän työnkulun ehtoa ei arvioida oikein. |
| Matka ja kulut | [519304](https://fix.lcs.dynamics.com/Issue/Details/?bugId=519304) | Kuluraporttikäytäntö ei arvioi projektitunnusta oikein. |
| Matka ja kulut | [522463](https://fix.lcs.dynamics.com/Issue/Details/?bugId=522463) | Toiminto, **Jaa konsernin kulutapahtumista henkilökohtaiseksi**, ei toimi oikein. |
| Matka ja kulut | [534702](https://fix.lcs.dynamics.com/Issue/Details/?bugId=534702) | Kuluraporttirivin syyt poistetaan vahingossa, kun tietyt matkustusehdotukset poistetaan. Näin tapahtuu, kun kuluraportin recID ja matkustuspyyntö ovat samat. |
| Matka ja kulut | [544368](https://fix.lcs.dynamics.com/Issue/Details/?bugId=544368) | Kulu-mobiilisovelluksessa on ongelma, kun kuluraporttikäytäntöjen **Projektitunnus**-kenttä on pakollinen. |
| Matka ja kulut | [545331](https://fix.lcs.dynamics.com/Issue/Details/?bugId=545331) | Projektiin liittyviä yritysten välisiä kuluja ei voi muokata. Sen sijaan näyttöön tulee seuraava virhesanoma: "Objektiviittausta ei ole määritetty objektin esiintymään". |
| Matka ja kulut | [548659](https://fix.lcs.dynamics.com/Issue/Details/?bugId=548659) | Kun kuluraportti on julkaistu, pankin alareskontrassa näkyy väärä valuutta ja summa. |
| Matka ja kulut | [558336](https://fix.lcs.dynamics.com/Issue/Details/?bugId=558336) | *Luottokorttitapahtumien poisto* -toimintoon on tehty parannuksia.  |
| Matka ja kulut | [525070](https://fix.lcs.dynamics.com/Issue/Details/?bugId=525070) | Kuluraporttiin sisältyvää arvonlisäveroa ei lasketa johdonmukaisesti, kun eri raportointivaluutta on määritetty yrityksessä. |
| Matka ja kulut | [527779](https://fix.lcs.dynamics.com/Issue/Details/?bugId=527779) | Uuden käteismatkakulun lisääminen vaikuttaa suorituskykyyn. |
| Matka ja kulut | [537841](https://fix.lcs.dynamics.com/Issue/Details/?bugId=537841) | Kulukäytännön säännöt eivät käynnisty kuluraportille. |
| Matka ja kulut | [566386](https://fix.lcs.dynamics.com/Issue/Details/?bugId=566386) | Kun uusi jaettu luokka ladataan Data Management Frameworkin avulla, kaikki jaettujen luokkien aliluokat poistetaan. |
| Matka ja kulut | [574131](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574131) | Kun luot kulurivin ja valitset sitten luokan, näyttöön tulee seuraava virhesanoma: "Yhdistelmä arvonlisäveroryhmän DOM ja nimikkeen arvonlisäveroryhmän STD ei ole kelvollinen". |
| Matka ja kulut | [574900](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574900) | Kulu-mobiilisovelluksessa on synkronointiongelmia. |
