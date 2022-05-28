---
title: uudet ominaisuudet huhtikuu 2021 – Project Operations resursseihin ja ei-varastoitaviin perustuvissa skenaarioissa
description: Tässä aiheessa on tietoja Project Operations resursseihin ja ei-varastoitaviin perustuvissa skenaarioissa huhtikuun 2021 julkaisussa saatavilla olevista laatupäivityksistä.
author: sigitac
ms.date: 04/22/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 07622ed798fd8d70e0ce5cc42297bd5056402474
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/14/2022
ms.locfileid: "8589100"
---
# <a name="whats-new-april-2021---project-operations-for-resourcenon-stocked-based-scenarios"></a>uudet ominaisuudet huhtikuu 2021 – Project Operations resursseihin ja ei-varastoitaviin perustuvissa skenaarioissa

_**Käytetään:** Project Operationsin resursseihin ja ei-varastoitaviin perustuvissa skenaarioissa_

Tämä aihe koskee seuraavia Dynamics 365 Project Operationsin komponentteja ja versioita:

- Project Operations Dataverse-ympäristön versiossa 4.9.0.221
- Projektinhallinta ja kirjanpito Dynamics 365 Finance -ympäristön versiossa 10.0.17

## <a name="features-included-in-this-release"></a>Tähän julkaisuun sisältyvät ominaisuudet

Tähän julkaisuun sisältyvät seuraavat ominaisuudet:

- Projektien ei-varastoitava materiaali. Tärkeitä ominaisuuksia ovat seuraavat:
  - Ei-varastoitavien materiaalien arviointi ja hinnoittelu projektin myyntikierron aikana. Lisätietoja on kohdassa [Luettelotuotteiden kustannus- ja myyntihintojen määrittäminen – lite](../pro/pricing-costing/set-up-cost-sales-rates-catalog-products.md).
  - Ei-varastoitavien materiaalien käytön seuranta projektin toimituksen aikana. Lisätietoja on kohdassa [Materiaalikäytön kirjaaminen projekteihin ja projektitehtäviin](../material/material-usage-log.md).
  - Laskutuksessa käytettiin ei-varastoitavan materiaalin kustannuksia. Lisätietoja on kohdassa [Laskutuksen jonon hallinta](../proforma-invoicing/manage-billing-backlog.md).
  - Tietoja tämän ominaisuuden määrittämisestä on aihessa [Ei-varastoivien materiaalien ja odottavien toimittajan laskujen määrittäminen](../procurement/configure-materials-nonstocked.md)
- Tehtäväpohjainen laskutus: Lisäsi mahdollisuuden liittää projektitehtäviä projektisopimusriveille ja siten käyttää samaa laskutustapaa, laskutusväliä ja asiakkaita kuin sopimusrivillä. Tämä liitos varmistaa tarkan laskutuksen, kirjanpidon sekä myyntituoton arvioinnin ja kirjaamisen, jotta se toimisi tämän projektitehtävien määritysten mukaisesti.
- Uudet ohjelmointirajapinnat Dynamics 365 Dataversessä sallivat toimintojen luomisen, päivittämisen ja poistamisen **Aikataulutusentiteettien** avulla. Lisätietoja on kohdassa [Aikataulutuksen ohjelmointirajapintojen käyttö toimintojen suorittamiseen ajoitusentiteeteillä](../project-management/schedule-api-preview.md).

## <a name="project-operations-dual-write-maps-updates"></a>Project Operationsin kaksoiskirjoituskarttojen päivitys

Seuraavassa luettelossa on esitetty kaksoiskirjoituskarttoja, joita on muokattu tai lisätty Project Operationsin huhtikuussa 2021 julkaistuun julkaisuun.

| **Entiteetin yhdistämismääritys** | **Päivitetty versio** | **Kommentit** |
| --- | --- | --- |
| Project Operations -integroinnin todelliset arvot (msdyn\_actuals) | 1.0.0.14 | Kartta on muokattu synkronoimaan materiaaliprojektien toteutuneet kulut. |
| Project Operations -integrointikohde kuluarvioita varten (msdyn\_estimateslines) | 1.0.0.2 | Lisätty projektisopimusrivin synkronointi talous- ja toimintosovelluksiin tehtäväpohjaisen laskutuksen tuen osalta. |
| Project Operations -integrointikohde tuntiarvioita varten (msdyn\_resourceassignments) | 1.0.0.5 | Lisätty projektisopimusrivin synkronointi talous- ja toimintosovelluksiin tehtäväpohjaisen laskutuksen tuen osalta. |
| Project Operationsin materiaaliarvioiden integrointitaulukko (msdyn\_estimatelines) | 1.0.0.0 | Uusi taulukkokartta, joka synkronoi materiaaliarviot Dataversesta talous- ja toimintosovelluksiin. |
| Project Operationsin integrointiprojektin toimittajalaskun vientientiteetti (msdyn\_projectvendorinvoices) | 1.0.0.0 | Uusi taulukkokartta, joka synkronoi toimittajan laskun otsikot talous- ja toimintosovelluksista Dataverseen. |
| Project Operationsin integrointiprojektin toimittajalaskurivin vientientiteetti (msdyn\_projectvendorinvoicelines) | 1.0.0.0 | Uusi taulukkokartta, joka synkronoi toimittajan laskun rivit talous- ja toimintosovelluksista Dataverseen. |

Suorita aina ympäristön kartan uusin versio ja ota käyttöön kaikki taulukkokartat, kun päivität Project Operations Dataverse -ratkaisua ja talous- ja toimintosovellusratkaisun versiota. Tietyt ominaisuudet ja toiminnot eivät ehkä toimi oikein, jos kartan uusinta versiota ei ole aktivoitu. Kartan aktiivinen versio näkyy **Kaksoiskirjoitus**-sivun **Versio**-sarakkeessa. Voit aktivoida kartan uuden version valitsemalla **taulukkokartan versiot**, valitsemalla uusimman ja tallentamalla valitun version. Jos olet mukauttanut valmiin taulukkokartan, kohdista muutokset uudelleen. Lue lisätietoja kohdasta [Ratkaisun elinkaaren hallinta](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Jos kartan käynnistykssä ilmenee ongelmia, noudata kaksoiskirjoituksen vianmääritysoppaan ohjeita kohdasta [Karttojen puuttuvat taulukkosarakkeet -ongelma](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps).

## <a name="quality-updates"></a>Laatupäivitykset

### <a name="project-operations-in-dynamics-365-dataverse"></a>Project Operations Dynamics 365 Dataversessä

| **Ominaisuusalue** | **Viitenumero** | **Laatupäivitys** |
| --- | --- | --- |
| Laskutus ja hinnoittelu | 2124532 | **Korjaa lasku** -painike näkyy proformalaskussa, kun ennakkomaksun summa tai käytetty ennakkomaksun summa on alkuperäisessä laskussa. Painike näkyy vain ympäristöissä, joissa on Finance-versio 10.0.19 tai uudempi. |
| Laskutus ja hinnoittelu | 2224568 | Lisätty logiikka, jonka avulla voidaan ottaa käyttöön mukautuksia, joihin liittyy laskun vahvistuslaajennus. |
| Laskutus ja hinnoittelu | 2101098 | Parannettiin proformalaskun oletuskenttien logiikkaa: **Laskutusosoitteen**, **Maksun saajan nimen** ja **Maksuehtojen** logiikka saavat nyt oletusarvot vastaavasta projektisopimuksen asiakastietueesta. |
| Laskutus ja hinnoittelu | 2021413 | Päivitettiin **Todelliset kustannukset** -ja **Myynti**-kenttä **Tehtävä**-entiteetissä sisältämään myynnin arvot tehtävien laskuttamattomista ja laskutetuista kuluista. |
| Laskutus ja hinnoittelu | 2182110 | Kun kopioit projektisopimuksen, sopimusrivin tunnus luodaan uudelleen kohdeprojektisopimuksessa, jotta se olisi yksilöivä. |
| Mahdollisuuksien hallinta | 2186741 | Lisätyt vahvistukset varmistavat, että **Alkuperä**-kenttää ja **Tapahtumatyyppiä** ei voi päivittää aiemmin luoduissa tarjousrivin tiedoissa. |
| Mahdollisuuksien hallinta | 2191353 | Välitavoitteita ei saa luoda ajan ja materiaalin sopimusrivillä. |
| Mahdollisuuksien hallinta | 2216956 | **Hintojen päivityksen** ongelmat on korjattu. |
| Suunnittelu ja seuranta | 2182979 | Projektin kopiointitoimintoa on parannettu, jotta kuluarviorivit kopioidaan alkuperäisestä projektista. |
| Suunnittelu ja seuranta | 2184144 | Projektin kopiointitoimintoa on parannettu, jotta resurssin työtehtävän nimi kopioidaan alkuperäisestä projektista. |
| Suunnittelu ja seuranta | 2184799 | Projektikopio: Kiristetty hallintaa sen varmistamiseksi, että arvioitua alkamispäivää ei voi muuttaa kopioinnin aikana. |
| Suunnittelu ja seuranta | 2185134 | Projektikopio: Kohdeprojektin arvioiduksi alkamispäiväksi on määritetty kuluva päivä. |
| Suunnittelu ja seuranta | 2196373 | Projektikopio: Varmista, että projektipäällikkö- ja ryhmän jäsen -tietueet eivät ole kahdentuneet projektiryhmässä. |
| Suunnittelu ja seuranta | 2211833 | Projektikopio: Resurssimääritykset kopioidaan lähdeprojektin tehtävästä kohdeprojektiin. |
| Suunnittelu ja seuranta | 2186541 | **Arviot**-ruudukon ongelmat resurssin mukaan ryhmiteltäessä on korjattu. |
| Suunnittelu ja seuranta | 2166906 | Tehtävän tapahtumaluokka on kopioittava **Resurssin määritys** -entiteettiin. |
| Resurssienhallinta | 2125362 | Korjattiin ongelmat, jotka liittyivät yleisen ryhmän jäsenen luomiseen tuntipohjaisella kohdistusmenetelmällä. |
| Aika ja kulu | 2113603 | Korjattiin mukautusongelma, joka liittyi määritteiden poistamiseen **Ajan syöttö** -sivulta. Järjestelmä tarkistaa nyt, onko määrite sivulla, ennen kuin sitä voi käyttää komentosarjan avulla. |
| Aika ja kulu | 2204377 | Kopioidut työaikaraportit näkyvät automaattisesti, kun valitaan **Kopioi viikko** aikaa syötettäessä. |
| Aika ja kulu | 2209059 | **Tila**-kenttää voi muokata Dynamics 365 Field Servicen aikakirjauksia varten. |

### <a name="project-management-and-accounting-in-dynamics-365-finance"></a>Projektinhallinta ja kirjanpito Dynamics 365 Financessa

| **Ominaisuusalue** | **Viitenumero** | **Laatupäivitys** |
| --- | --- | --- |
| Projektinhallinta ja kirjanpito | [491941](https://fix.lcs.dynamics.com/Issue/Details/?bugId=491941) | Käänteisen arvion poistaminen ei toimi **Kausittainen**-osassa.  |
| Projektinhallinta ja kirjanpito | [509773](https://fix.lcs.dynamics.com/Issue/Details/?bugId=509773) | **Kirjanpidon oikaisu** -toiminto luo ongelman kirjanpitotileille, joille on valittu **Älä salli manuaalista syöttöä**. |
| Projektinhallinta ja kirjanpito | [510728](https://fix.lcs.dynamics.com/Issue/Details/?bugId=5109728) | Lisätty liiketoimintalogiikka korjauslaskujen, mukaan lukien ennakkomaksun summan tai käytetyn ennakkomaksun summan, käsittelemiseen. |
| Projektinhallinta ja kirjanpito | [514364](https://fix.lcs.dynamics.com/Issue/Details/?bugId=514364) | KET-myyntiarvon kirjaaminen yritysten välisessä projektilaskutuksessa poimii odottamattoman tilin. |
| Projektinhallinta ja kirjanpito | [521807](https://fix.lcs.dynamics.com/Issue/Details/?bugId=521807) | Kun työstät ennakkomaksuja Project Operationsissa, sopimuksen oletusprojektin muuttaminen sen jälkeen, kun ennakkomaksut on laskutettu, aiheuttaa ongelmia saapuvien vähennysten kanssa. |
| Projektinhallinta ja kirjanpito | [527319](https://fix.lcs.dynamics.com/Issue/Details/?bugId=527319) | Project Operationsissa projektin poistamisen sopimuksesta tulisi palauttaa tarvittaessa sopimuksen oletusprojekti. |
| Projektinhallinta ja kirjanpito | [528212](https://fix.lcs.dynamics.com/Issue/Details/?bugId=528212) | Project Operations näyttää vääriä kulurivejä yritysten välisen laskun **Lisää rivi** -luettelossa. |
| Projektinhallinta ja kirjanpito | [543968](https://fix.lcs.dynamics.com/Issue/Details/?bugId=543968) | Project Operationsissa **Ostosopimus**-sivua ei näy Project Operationsiin integroiduissa Finance-yrityksissä. |
| Projektinhallinta ja kirjanpito | [545878](https://fix.lcs.dynamics.com/Issue/Details/?bugId=545878) | Dataverse-integrointivirheen johdosta tarjousta ei voida muuttaa voitetuksi Project Operationsissa. |
| Projektinhallinta ja kirjanpito | [547440](https://fix.lcs.dynamics.com/Issue/Details/?bugId=547440) | **ProjCDSProjectContractEntity** voi määrittää rahoituslähteen laskun osoitteen toiselta asiakkaalta.  |
| Projektinhallinta ja kirjanpito | [557376](https://fix.lcs.dynamics.com/Issue/Details/?bugId=557376) | Dimensioita ei valita Project Operationsissa, kun tapahtumalle luodaan kirjauslasku. |
| Matkustus ja kulut | [441256](https://fix.lcs.dynamics.com/Issue/Details/?bugId=441256) | Käteisennakkosaldoa ei päivitetä kuluraportissa, jos se on hyväksytty ja kirjattu rivi riviltä. |
| Matka ja kulut | [482041](https://fix.lcs.dynamics.com/Issue/Details/?bugId=482041) | Eriteltyjen yritysten välisten kuluraporttien veroja ei lasketa oikein. |
| Matka ja kulut | [483469](https://fix.lcs.dynamics.com/Issue/Details/?bugId=483469) | Projekteihin liittyvät lisäkentät näkyvät uudelleen suunnitellulla **yritysten välisten kuluraporttien** sivulla. |
| Matka ja kulut | [486592](https://fix.lcs.dynamics.com/Issue/Details/?bugId=486592) | Kuluraporttien otsikkokuittauksissa näkyy virheellinen virhesanoma. |
| Matka ja kulut | [487971](https://fix.lcs.dynamics.com/Issue/Details/?bugId=487971) | Kuluraportti on kirjattu virheellisesti yritysten välisessä skenaariossa, jos arvonlisävero on kirjattu kohdeyritykseen. |
| Matka ja kulut | [505696](https://fix.lcs.dynamics.com/Issue/Details/?bugId=505696) | Raportin lähetyspäivämääriä ei tulosteta hyväksyttyihin kuluraportteihin. |
| Matka ja kulut | [508726](https://fix.lcs.dynamics.com/Issue/Details/?bugId=508726) | **Hyväksymispäivä** - ja **Hylkäyspäivä** -kentät eivät täyty, kun kulu hyväksytään. |
| Matka ja kulut | [509913](https://fix.lcs.dynamics.com/Issue/Details/?bugId=509913) | Yhdelle työntekijälle luotua matkustuspyyntöä voi käyttää toisen työntekijän kuluraportissa. |
| Matka ja kulut | [518186](https://fix.lcs.dynamics.com/Issue/Details/?bugId=518186) | Kululuokat lukitaan, kun uusi kulurivi lisätään. |
| Matka ja kulut | [520914](https://fix.lcs.dynamics.com/Issue/Details/?bugId=520914) | Jos kuluraporttirivit on jo jaettu ja se jaetaan nimikkeisiin, ostoreskontra\kirjanpitotosite kirjataan puutteellisesti ja laskentalähteen hallinta katkeaa, koska **TRVEXPTRANS. SOURCEDOCUMENTLINE** on kaksoiskappale. |
| Matka ja kulut | [521943](https://fix.lcs.dynamics.com/Issue/Details/?bugId=521943) | Matkustuspyyntökäytäntö ei toimi odotetulla tavalla. |
| Matka ja kulut | [522567](https://fix.lcs.dynamics.com/Issue/Details/?bugId=522567) | Toimittajan tilin nimi ei näy kuluraporttien kirjatuissa projektitapahtumissa. |
| Matka ja kulut | [525106](https://fix.lcs.dynamics.com/Issue/Details/?bugId=525106) | Aikaa ei voi hyväksyä Project Operationsissa tehtävälle, joka liittyy yritysten väliseen projektiin. |
| Matka ja kulut | [526336](https://fix.lcs.dynamics.com/Issue/Details/?bugId=526336) | Käteisennakkopalautusluokka ei päivitä käteisennakkosaldoja, kun se kirjataan. |
| Matka ja kulut | [527218](https://fix.lcs.dynamics.com/Issue/Details/?bugId=527218) | Myyntihinta lasketaan väärin kuluraporteissa, jotka on luotu ulkomaisena valuuttana käyttämällä tuotuja luottokorttitapahtumia ja jotka on liitetty projektiin. |
| Matka ja kulut | [542927](https://fix.lcs.dynamics.com/Issue/Details/?bugId=542927) | Peruutettiin **TrvRequisitionLine**-tietoentiteetti ja siihen liittyvä yksilöllinen indeksi. |
| Matka ja kulut | [543239](https://fix.lcs.dynamics.com/Issue/Details/?bugId=543239) | Lisätty instrumentointi **SOURCEDOCUMENTLINE**-luontiin. |
| Matka ja kulut | [544323](https://fix.lcs.dynamics.com/Issue/Details/?bugId=544323) | Väärä alikirjanpidon kirjauskansio näytetään yritysten välisessä skenaariossa, jos arvonlisävero on kirjattu kohdeyritykseen. |
| Matka ja kulut | [546877](https://fix.lcs.dynamics.com/Issue/Details/?bugId=546877) | Kuluarvioita ei poisteta Project Operationsissa Financesta, kun ne poistetaan Dataversestä. |
| Matka ja kulut | [550575](https://fix.lcs.dynamics.com/Issue/Details/?bugId=550575) | Kun kululuokka on muu kuin projektiluokka, **Kulu**-sivulla valittuja taloushallinnon dimensioita ei kopioida kuluraporttiin. |
