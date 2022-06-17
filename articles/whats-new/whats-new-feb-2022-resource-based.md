---
title: Helmikuun 2022 uudet ominaisuudet Project Operationsin resursseihin ja ei-varastoitaviin perustuvissa skenaarioissa
description: Tässä artikkelissa on tietoja Project Operationsin resursseihin ja ei-varastoitaviin perustuvissa skenaarioissa helmikuussa 2022 julkaistussa versiossa saatavilla olevista laatupäivityksistä.
author: sigitac
ms.date: 01/27/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: b036c0a3c39c52cb15277293679ef88906cae2c4
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8932982"
---
# <a name="whats-new-february-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>Helmikuun 2022 uudet ominaisuudet Project Operationsin resursseihin ja ei-varastoitaviin perustuvissa skenaarioissa

*Käytetään: Project Operationsin resursseihin ja ei-varastoitaviin perustuvissa skenaarioissa*

Tämä artikkeli koskee seuraavia Microsoft Dynamics 365 Project Operationsin osia ja versioita:

- Project Operations Dataversessa ympäristöversio 4.28.0.120
- Projektinhallinta ja kirjanpito Dynamics 365 Finance -ympäristön versiossa 10.0.24

## <a name="features-included-in-this-release"></a>Tähän julkaisuun sisältyvät ominaisuudet

- Tässä versiossa yhteen projektiin voi lisätä enintään 300 ryhmän jäsentä. Aiemmin ryhmän jäsenmäärärajoitus oli 150. Lisätietoja on kohdassa [Projektin rajoitukset](../project-management/create-wbs.md#project-limitations).

## <a name="project-operations-dual-write-map-updates"></a>Project Operations -kaksoiskirjoituksen yhdistämismäärityksen päivitykset

Seuraavassa luettelossa on esitetty Project Operationsin helmikuun 2022 julkaisuun muutetut tai lisätyt kaksoiskirjoituksen yhdistämismääritykset.

| Entiteetin yhdistämismääritys | Päivitetty versio | Kommentit |
| --- | --- | --- |
| Project Operations -integroinnin projektikulujen vientientiteetti (msdyn\_expenses) | 1.0.0.3 | Laajennettu projektiaktiviteetin synkronoinnille Dataverseen. |

Project Operationsin kaksoiskirjoituksen yhdistämismääritysten luettelot ja versiot ovat ohjeaiheessa [Project Operationsin kaksoiskirjoituksen yhdistämismääritysten versiot](../environment/resource-dual-write-maps.md).

Suorita aina ympäristön kartan uusin versio ja ota käyttöön kaikki taulukkokartat, kun päivität Project Operations Dataverse -ratkaisua ja rahoitusratkaisun versiota. Jotkin ominaisuudet ja toiminnot eivät ehkä toimi oikein, jos kartan uusinta versiota ei ole aktivoitu. Voit tarkastella kartan aktiivista versiota **Kaksoiskirjoitus**-sivun **Versio**-sarakkeessa. Voit aktivoida kartan uuden version valitsemalla **Taulukkokartan versiot**, valitsemalla uusimman version ja tallentamalla sitten valitun version. Jos olet mukauttanut valmista taulukkokarttaa, voit käyttää muutokset uudelleen. Lue lisätietoja kohdasta [Ratkaisun elinkaaren hallinta](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Jos kartan käynnistämisen yhteydessä tulee ongelma, seuraa ohjeita [Puuttuvien taulukkosarakkeiden ongelma kartoissa](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) -osassa kaksoiskirjoituksen vianmääritysoppaassa.

## <a name="quality-updates"></a>Laatupäivitykset

### <a name="project-operations-on-dataverse"></a>Project Operations Dataversessä

| Ominaisuusalue | Viitenumero | Laatupäivitys |
| --- | --- | --- |
| Laskutus ja hinnoittelu | 2415109 | **Toimintojen maksuehdot** -kentän oletusarvon on oltava projektisopimuksen asiakastietue ja proformalaskutietue. |
| Laskutus ja hinnoittelu | 2497369 | Materiaalin korjauksen on noudatettava **Korjaus**-parametrien päivämääräarvoa. |
| Laskutus ja hinnoittelu | 2498697 | Parannettiin **aikamerkinnän palautuksen** suojausmäärityksiä. |
| Laskutus ja hinnoittelu | 2513824 | Resurssipohjaisissa skenaarioissa tapahtumaluokan tunnus saa olla enintään 28 merkkiä Project Operationsissa. |
| Laskutus ja hinnoittelu | 2517455 | **Päivitä laskurivin tapahtumat** -toiminto ei saa käynnistyä useita kertoja samaan aikaan samalle laskulle. |
| Laskutus ja hinnoittelu | 2517465 | **Poista laskurivin tietojen aktivointi** - toiminto on estetty, koska sitä ei tueta. |
| Laskutus ja hinnoittelu | 2556660 | Korjattiin projektiparametritietueeseen liitetylle hinnastolle tehty päivämäärien voimassaolon tarkistus. |
|   Mahdollisuuksien hallinta | 2369202 | Korjattiin liiketoimintalogiikka, joka tarkistaa, että samaan projektisopimukseen voidaan liittää hinnastot, joissa on päällekkäisiä voimassaolopäiviä. |
|   Mahdollisuuksien hallinta | 2385965 | Korjattu toimintatapa **Projektisopimus**-sivun **Asiakkaat**-välilehdessä, kun valitset **Tallenna ja sulje**. |
| Aika ja kulut | 2538503 | Projektitehtävän on oltava käytettävissä **Projektin toteutuneet arvot** -entiteetissä sen jälkeen, kun kuluraportti on kirjattu. |

### <a name="project-management-and-accounting-on-dynamics-365-finance"></a>Projektinhallinta ja kirjanpito Dynamics 365 Financessa

| Ominaisuusalue | Viitenumero | Laatupäivitys |
| --- | --- | --- |
| Projektinhallinta ja kirjanpito | [615496](https://fix.lcs.dynamics.com/Issue/Details/?bugId=615496) | Toimittajan hyvityslaskujen tuonnin aikana tapahtuu virhe. Virhesanomassa näkyy: "Ennakkomaksun summa ei voi olla suurempi kuin jäljellä oleva nettosumma". |
| Projektinhallinta ja kirjanpito | [619391](https://fix.lcs.dynamics.com/Issue/Details/?bugId=619391) | Jos laskuehdotuksessa on nollasummamaksutapahtumia, jotka ovat laskuttamattoman myynnin toteutuneita arvoja, laskutusta ei voi tehdä. |
| Projektinhallinta ja kirjanpito | [624423](https://fix.lcs.dynamics.com/Issue/Details/?bugId=624423) | Julkaistu kustannus ei ole oikea, kun ostohinta on päivitetty ja **Aktivoi muutosten hallinta** on otettu käyttöön.|
| Projektinhallinta ja kirjanpito | [628386](https://fix.lcs.dynamics.com/Issue/Details/?bugId=628386) | Kiinteähintaista projektia varten tehty kirjausarvio käyttää virheellistä valuuttaa ja summaa arviotositteessa, vaikka **Ota projektin sopimusvaluutta käyttöön arvion laskemista varten** -ominaisuus on otettu käyttöön. |
| Projektinhallinta ja kirjanpito | [629239](https://fix.lcs.dynamics.com/Issue/Details/?bugId=629239) | Kohteen **ProjDMFDataPopulation\_Extension** ei pitäisi tehdä kutsua, joka ottaa käyttöön muutosten seurannan ottamatta kiinni poikkeuksia entiteeteille, joilla on määritysavaimia, jotka eivät ole käytössä. |
| Projektinhallinta ja kirjanpito | [623818](https://fix.lcs.dynamics.com/Issue/Details/?bugId=623818) | Erätyö korjataan, kun kirjataan useita edistyneitä kirjauskansioita ja tapahtuu virhe. |
| Matka ja kulut | [616805](https://fix.lcs.dynamics.com/Issue/Details/?bugId=616805) | Kuluraporttien käteisennakkoihin liittyvän tilitysongelman vuoksi verosummaa ei kateta käteisennakon osana. |
| Matka ja kulut | [616959](https://fix.lcs.dynamics.com/Issue/Details/?bugId=616959) | ALV-tiedot eivät sisälly **Kulu - Kirjatut tapahtumat** -raporttiin. |
| Matka ja kulut | [618943](https://fix.lcs.dynamics.com/Issue/Details/?bugId=618943) | **Kuitit vaaditaan** -kulukäytäntörikkomus näyttää virheellisesti varoituksen kuluraporteissa. |
| Matka ja kulut | [633470](https://fix.lcs.dynamics.com/Issue/Details/?bugId=633470) | Projektitapahtuma ei sisällytä ei-palautettavaa arvonlisäveroa kokonaismyyntisummaan, kun tapahtuma on kilometrikulun tulos. |
| Matka ja kulut | [642979](https://fix.lcs.dynamics.com/Issue/Details/?bugId=642979) | Kun kohdistetulla rivillä on veroa, et voi muuttaa kohdistusrivin päivämäärää ja tapahtuu lähdeasiakirjan tilavirhe. |

## <a name="removed-and-deprecated-features"></a>Poistetut ja vanhentuneet ominaisuudet

Artikkelissa [Project Operationsin poistetut tai vanhentuneet ominaisuudet](removed-depreciated-features-project.md) käsitellään ominaisuuksia, jotka on poistettu tai vanhentuneet Dynamics 365 Project Operationsissa.

- Poistettu toiminto ei ole enää käytettävissä tuotteessa.
- Vanhentunutta ominaisuutta ei enää kehitetä aktiivisesti ja se voidaan poistaa tulevassa päivityksessä.

Vanhentumisilmoitus näkyy artikkelissa [Project Operationsin poistetut tai vanhentuneet toiminnot](removed-depreciated-features-project.md) 12 kuukautta ennen ominaisuuden poistoa tuotteesta.

Jos muutokset vaikuttavat vain käännösaikaan, mutta ne ovat binaarisesti yhteensopivia Sandbox- ja tuotantoympäristön kanssa, vanhentumisaika on lyhyempi kuin 12 kuukautta. Yleensä nämä muutokset ovat toiminnallisia päivityksiä, jotka on tehtävä kääntäjään.
