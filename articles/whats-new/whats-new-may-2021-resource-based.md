---
title: Toukokuun 2021 uudet ominaisuudet - Project Operations resursseihin/ei-varastoitaviin perustuvissa skenaarioissa
description: Tässä aiheessa on tietoja Project Operations resursseihin ja ei-varastoitaviin perustuvissa skenaarioissa toukokuun 2021 julkaisussa saatavilla olevista laatupäivityksistä.
author: sigitac
ms.date: 05/11/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 07ae18faef6acb9d64b889bbfdba89de0c96a453
ms.sourcegitcommit: d48dce64f6c5b16db3250096715c9d9f92a81971
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/20/2021
ms.locfileid: "6083922"
---
# <a name="whats-new-may-2021---project-operations-for-resourcenon-stocked-based-scenarios"></a>Toukokuun 2021 uudet ominaisuudet - Project Operations resursseihin/ei-varastoitaviin perustuvissa skenaarioissa

_**Käytetään:** Project Operationsin resursseihin ja ei-varastoitaviin perustuvissa skenaarioissa_

Tämä aihe koskee seuraavia Dynamics 365 Project Operationsin komponentteja ja versioita:

- Project Operations Dynamics 365 Dataverse -ympäristön versiossa 4.10.0.186
- Projektinhallinta ja kirjanpito Finance and Operations -sovellusten ympäristöjen versiossa 10.0.18

## <a name="features-included-in-this-release"></a>Tähän julkaisuun sisältyvät ominaisuudet

Tähän julkaisuun sisältyvät seuraavat ominaisuudet:

- [Aikataulutustilat](../project-management/scheduling-modes.md): Projektipäälliköt voivat määrittää, tulisiko projektia hallita käyttämällä kiinteän keston, kiinteän työmäärän vai kiinteiden yksiköiden aikataulutustilaa.
- [Kilometrikorvausten määrittäminen kilometrikorvaustasoilla](../expense/set-up-mileage.md): Päivitä kilometrikorvaustasot työntekijöiden kuluraportteja varten.

## <a name="project-operations-dual-write-maps-updates"></a>Project Operationsin kaksoiskirjoituskarttojen päivitys

Seuraavassa luettelossa on esitetty kaksoiskirjoituskarttoja, joita on muokattu tai lisätty Project Operationsin toukokuun 2021 julkaisuun.

| Entiteetin yhdistämismääritys | Päivitetty versio | Kommentit |
| --- | --- | --- |
| Projektin rahoituslähde (msdyn\_projectcontractsplitbillingrules) | 1.0.0.2 | Projektisopimuksen asiakkaan maksuehtojen synkronointi. |
| Projektin laskuehdotus V2 (laskut) | 1.0.0.3 | Proformalaskujen maksuehtojen synkronointi. |
| Project Operationsin integrointiprojektin toimittajalaskurivin vientientiteetti (msdyn\_projectvendorinvoicelines) | 1.0.0.1 | Laatupäivitykset |
| Projektit V2 (msdyn\_projects) | 1.0.0.2 | Laatupäivitykset |

Suorita aina kartan uusin versio ympäristössä ja ota käyttöön kaikki asiaan liittyvät taulukkokartat, kun päivität Project Operations Dataverse -ratkaisua ja Finance and Operations -sovellusten ratkaisun versiota. Tietyt ominaisuudet ja toiminnot eivät ehkä toimi oikein, jos kartan uusinta versiota ei ole aktivoitu. Kartan aktiivinen versio näkyy **Kaksoiskirjoitus**-sivun **Versio**-sarakkeessa. Voit aktivoida kartan uuden version valitsemalla **Taulukkokartan versiot**, valitsemalla uusimman version ja tallentamalla sitten valitun version. Jos olet mukauttanut valmiin taulukkokartan, kohdista muutokset uudelleen. Lue lisätietoja kohdasta [Ratkaisun elinkaaren hallinta](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management.md).

Jos kartan käynnistyksessä ilmenee ongelmia, noudata kaksoiskirjoituksen vianmääritysoppaan ohjeita kohdasta [Karttojen puuttuvat taulukkosarakkeet -ongelma](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades.md#missing-table-columns-issue-on-maps).

## <a name="quality-updates"></a>Laatupäivitykset

### <a name="project-operations-on-dataverse"></a>Project Operations Dataversessä

| **Ominaisuusalue** | **Viitenumero** | **Laatupäivitys** |
| --- | --- | --- |
| Laskutus ja hinnoittelu | 2227635 | **Yksikköryhmä**- ja **Yksikkö**-kenttien arvot saadaan oletusarvoisesti **Materiaaliarviot**-ruudukon tuotteesta. |
| Laskutus ja hinnoittelu | 2234127 | **Tehtävän tunnus** -kenttä integroituu nyt oikein Dataverse-projektin todellisiin arvoihin, kun toimittajan lasku kirjataan. |
| Laskutus ja hinnoittelu | 2235564 | Kirjauskansion rivin tallentaminen varmistaa, että kirjauskansion rivillä näkyvä valuutta vastaa rivin oletusvaluuttaa tallennuksen jälkeen. |
| Laskutus ja hinnoittelu | 2246671 | Tapahtuman muuttaminen ei-veloitettavaksi laskutuksen aikana kumoaa alkuperäisen laskuttamattoman myyntitietueen ja luo uuden ei-veloitettavan laskuttamattoman myyntitietueen. |
| Laskutus ja hinnoittelu | 2264042 | Kelvollista laskun korjausta ei saa estää, jos laskun korjauksen tiedot eivät ole kelvollisia ympäristössä. |
| Laskutus ja hinnoittelu | 2146367 | Projektin laskun ylätunnisteen kaksoiskirjoituksen kartoitusta laajennettiin sisältämään maksuehdot. |
|   Mahdollisuuksien hallinta | 2086888 | Älä lisää rooleja ja luokkia, joiden aktivointi on kumottu ennen tarjouksen kopioimista, uuden kopioidun tarjouksen laskutettaviin rooleihin ja luokkiin. |
|   Mahdollisuuksien hallinta | 2234376 | Vain luku -kentät näkyvät harmaana **Materiaaliarviot**-ruudukossa. |
|   Mahdollisuuksien hallinta | 2238337 | Yhteyshenkilöön perustuvan tarjouksen voi tallentaa, vaikka sitä ei olisi liitetty projektin hinnastoon. |
|   Mahdollisuuksien hallinta | 2239810 | Kun tarjous suljetaan hävittynä, myös siihen liittyvä projekti suljetaan ja mahdolliset varaukset peruutetaan. |
| Projektin suunnittelu ja seuranta | 2099559 | Lisätty järjestelmän kuntoa koskevia lisätarkistuksia, jotka suoritetaan ennen kuin **Projektitehtävät**-ruudukko avautuu. |
| Projektin suunnittelu ja seuranta | 2178987 | Korjattiin tilapäinen virhe, joka ilmeni, kun **Projekti**-sivulta valittiin **Seuraava vaihe**. |
| Resurssienhallinta | 2224817 | Varausten laajentamisen toimintatapa käyttää oletusarvoisesti oikeaa varauksen tilaa. |
| Aikamerkintä | 2202476 | **Aikamerkintä**-sivu käyttää nyt reaktioruudukon ohjausobjektia ja korjaa ongelmia, kuten ruudukon virheellinen tasaus. |
| Aikamerkintä | 2223377 | Aikamerkintä on piilotettu **Varattavissa oleva resurssi** -sivun **Liittyvä**-osiosta käytettävyyteen liittyvien epäselvyyksien välttämiseksi. |

### <a name="project-management-and-accounting-in-dynamics-365-finance"></a>Dynamics 365 Financen projektinhallinta ja kirjanpito

| Ominaisuusalue | Viitenumero | Laatupäivitys |
| --- | --- | --- |
| Projektinhallinta ja kirjanpito | [545878](https://fix.lcs.dynamics.com/Issue/Details/?bugId=545878) | Project Operations resursseihin perustuvissa skenaarioissa: Tarjousta ei voi muuntaa voitetuksi integrointivirheen vuoksi. |
| Projektinhallinta ja kirjanpito | [546604](https://fix.lcs.dynamics.com/Issue/Details/?bugId=546604) | Project Operations: Päällekkäisten sopimusrivien ja tapahtumatyyppien tarkistus aiheuttaa virheen, kun yrität liittää sopimusriviä projektin tunnukseen. |
| Projektinhallinta ja kirjanpito | [547440](https://fix.lcs.dynamics.com/Issue/Details/?bugId=547440) | **ProjCDSProjectContractEntity** määrittää rahoituslähteen laskun osoitteen toiselta asiakkaalta. |
| Matka ja kulut | [480451](https://fix.lcs.dynamics.com/Issue/Details/?bugId=480451) | Kilometrikorvausten määrityksiin liittyvä kirjausvirhe saattaa tapahtua. |
| Matka ja kulut | [522084](https://fix.lcs.dynamics.com/Issue/Details/?bugId=522084) | **Jaa henkilökohtaiseksi** -toiminto ei toimi ulkomaalaisia valuuttoja käyttäville kulutapahtumille. |
| Matka ja kulut | [523938](https://fix.lcs.dynamics.com/Issue/Details/?bugId=523938) | Kululuokkien avattavan valikon arvot näyttävät edustajille virheelliset luokat riippumatta siitä, ovatko edustajat resursseja. |
| Matka ja kulut | [539266](https://fix.lcs.dynamics.com/Issue/Details/?bugId=539266) | Konsernin kuluraporttia ei voi tallentaa **resurssin/luokan tarkistuksen** virheen takia. |
| Matka ja kulut | [532610](https://fix.lcs.dynamics.com/Issue/Details/?bugId=532610) | Kuluraportin kirjauksen väärällä kilometrimaksun laskutoimituksella on jaettuja rivejä. |
| Matka ja kulut | [537404](https://fix.lcs.dynamics.com/Issue/Details/?bugId=537404) | Konsernin kuluraporttia ei voi kirjata, kun arvonlisävero sisällytetään ja maksutavan vastatilin tyyppi on **Työntekijä**. |
| Matka ja kulut | [542927](https://fix.lcs.dynamics.com/Issue/Details/?bugId=542927) | Palautuksen **TrvRequisitionLine**-tietoentiteetti ja yksilöllinen indeksi on liitetty toisiinsa. |
| Matka ja kulut | [543239](https://fix.lcs.dynamics.com/Issue/Details/?bugId=543239) | Kuluraportti tukee lähdeasiakirjan rivien luomista ja päivittämistä. |
| Matka ja kulut | [544323](https://fix.lcs.dynamics.com/Issue/Details/?bugId=544323) | Konserniskenaariossa näytetään väärä alareskontran kirjauskansio, jos arvonlisävero kirjataan kohdeyritykseen. |
| Matka ja kulut | [546877](https://fix.lcs.dynamics.com/Issue/Details/?bugId=546877) | Project Operations: Kuluarviota ei poisteta Financesta, kun se poistetaan Dataversestä. |
| Matka ja kulut | [550575](https://fix.lcs.dynamics.com/Issue/Details/?bugId=550575) | Kun kululuokka on muu kuin projektiluokka, **Kulut**-sivulla valittuja taloushallinnon dimensioita ei kopioida kuluraporttiin. |
