---
title: Uudet ominaisuudet, lokakuu 2022 – Project Operations resursseihin ja ei-varastoitaviin perustuvissa skenaarioissa
description: Tässä artikkelissa on tietoja Microsoft Dynamics 365 Project Operationsin resursseihin ja ei-varastoitaviin perustuvissa skenaarioissa lokakuussa 2022 julkaistussa versiossa saatavilla olevista laatupäivityksistä.
author: ramagadu
ms.date: 11/17/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: ramagadu
ms.openlocfilehash: 392a12d6954c2390e5bad8e8e36cf58b7a1d0749
ms.sourcegitcommit: 1f162707ac342343fb5390fb9ae335e4cea4f3f2
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/29/2022
ms.locfileid: "9806606"
---
# <a name="whats-new-october-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>Uudet ominaisuudet, lokakuu 2022 – Project Operations resursseihin ja ei-varastoitaviin perustuvissa skenaarioissa

_**Käytetään:** Project Operationsin resursseihin ja ei-varastoitaviin perustuvissa skenaarioissa_

Tämä artikkeli koskee seuraavia Microsoft Dynamics 365 Project Operationsin osia ja versioita:

- Project Operations Dataversessa ympäristöversio 4.57.0.176
- Projektinhallinta ja kirjanpito Dynamics 365 Finance -ympäristön versiossa 10.0.30

## <a name="features-included-in-this-release"></a>Tähän julkaisuun sisältyvät ominaisuudet

| Ominaisuusalue | Ominaisuuden nimi | Lisätietoja |
| --- | --- | --- |
| Projektin suunnittelu ja seuranta | **Project Operationsin ulkoinen aikataulutus**<br>Ulkoisen aikataulutustilan avulla voit natiivisti luoda, päivittää ja poistaa entiteettejä, jotka liittyvät työrakenteisiin (WBS) käyttämällä Dataversen luonnollisia ohjelmointirajapintoja, mutta ilman Microsoft Project for the Webin pakottamia nykyisiä rajoituksia. | [Ulkoinen aikataulutus](/dynamics365/project-operations/project-management/external-scheduling) |
| Käyttöönotto ja määritys | <p>**Salli asiakkaiden valita käyttöönottotyyppi**<br>Project Operationsin tuotepohjaisten päivitysten (PDU) avulla Project Operationsin kaksoiskirjoitusratkaisu asennetaan automaattisesti, kun kaksiosaiset ydinratkaisut ja orkestrointiratkaisut asennetaan ympäristöön.</p><p>Tämä ominaisuus esittelee projektiparametreissa uuden **Ratkaisun päivityksen käyttäytyminen** -parametrin. Kun tämän parametrin arvo on **vain Lite**, PUD:it eivät enää asenna Project Operationsin kaksoiskirjoitusratkaisua automaattisesti, vaikka kaksoiskirjoituksen ydin- ja orkestrointiratkaisut on asennettu ympäristöön. Tästä käyttäytymisestä on hyötyä asiakkaille, jotka haluavat käyttää kaksoiskirjoitusratkaisuja integroidakseen myyntitilaukset rahoitus- ja toimintosovelluksiin, mutta haluavat käyttää Project Operationsia Lite-tilassa (integroimatta niitä rahoitus- ja toimintosovelluksiin).</p> | |
| Laskutus ja hinnoittelu | <p>**Valuutan muuntaminen kulujen laskuttamattomaan myyntitapahtumaan integroiduissa ympäristöissä**<br>Jos asiakas käyttää Project Operationsia, joka on integroitu rahoitus- ja toimintosovelluksiin (resurssi- tai ei-varastoidussa käyttöönottotyypissä), valuuttakurssit hallitaan yleensä rahoitus- ja toimintasovelluksissa. Jos kululuokka on kuitenkin hinnoitettava käyttämällä asiakasta laskutessa hintaa "kustannuksilla" tai "hankintakuluilla", valuuttakurssi, jossa myyntisumma lasketaan, käyttää Dataversen vaihtokurssia, ei rahoitus- ja toimintasovellusten valuuttakurssia.</p><p>Tämä ominaisuus esittelee projektiparametreissa uuden **Valuutanvaihdon käyttäytyminen** -parametrin. Kun parametriksi on määritetty **Laajennettu varatoiminnolla**, kulutapahtumien laskuttamattomat myyntisummat lasketaan käyttämällä rahoitus- ja toimintasovellusten valuuttakursseja.</p> | |

## <a name="project-operations-dual-write-maps-updates"></a>Project Operationsin kaksoiskirjoituskarttojen päivitys

Tässä versiossa ei ole päivityksiä Project Operationsin kaksoiskirjoituskartoille. Project Operationsin kaksoiskirjoituskarttojen luettelo ja versiot ovat kohdassa [Project Operationsin kaksi kaksoiskirjoituskarttojen versiot](../environment/resource-dual-write-maps.md).

Suorita aina ympäristön kartan uusin versio ja ota käyttöön kaikki taulukkokartat, kun päivität Project Operations Dataverse -ratkaisua ja rahoitusratkaisun versiota. Jotkin ominaisuudet ja toiminnot eivät ehkä toimi oikein, jos kartan uusinta versiota ei ole aktivoitu. Voit tarkastella kartan aktiivista versiota **Kaksoiskirjoitus**-sivun **Versio**-sarakkeessa. Voit aktivoida kartan uuden version valitsemalla **Taulukkokartan versiot**, valitsemalla uusimman version ja tallentamalla sitten valitun version. Jos olet mukauttanut valmista taulukkokarttaa, voit käyttää muutokset uudelleen. Lue lisätietoja kohdasta [Ratkaisun elinkaaren hallinta](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Jos kartan käynnistämisen yhteydessä tulee ongelma, seuraa ohjeita [Puuttuvien taulukkosarakkeiden ongelma kartoissa](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) -osassa kaksoiskirjoituksen vianmääritysoppaassa.

## <a name="quality-updates"></a>Laatupäivitykset

### <a name="project-operations-on-dataverse"></a>Project Operations Dataversessä

| Ominaisuusalue | Viitenumero | Laatupäivitys |
| --- | --- | --- |
| Laskutus ja hinnoittelu | 2316317 | Järjestelmän avulla voidaan luoda lasku, jolla ei ole laskutettavia tapahtumia. |
| Laskutus ja hinnoittelu | 2737300 | Tarkista, onko **Asiakas**-kentän käytettävyys tarkistettu, ennen kuin lomaketta käytetään. |
| Laskutus ja hinnoittelu | 2744948 | Lisää laskutustavan tyhjäarvotarkistus. |
| Laskutus ja hinnoittelu | 2763515 | Tyhjäviittauksen virhekahva, kun laskun myyntisopimus puuttuu. |
| Laskutus ja hinnoittelu | 2844301 | Erälaskun luonti epäonnistuu virheen takia. |
| Laskutus ja hinnoittelu | 2845869 | Organisaatiopalvelun virheellinen tallennus. |
| Laskutus ja hinnoittelu | 2853729 | Rooli- ja hintatiedot päivitetään, kun laskutustyyppiä muokataan. |
| Laskutus ja hinnoittelu | 2940350 | Kun toteutuneet hinnat hinnoitetaan, vain aktiiviset hinnastot tulisi syöttää automaattisesti. |
| Käyttöönotto ja määritys | 3001206 | Entiteetti msdyn\_replaylogheader estää asiakasorganisaatioiden päivityksen. |
| Mahdollisuuksien hallinta | 2755582 | Split Billing Rule Helper -ohjeen tyhjäarvoisia viittauspoikkeuksia käsittelevä kahva. |
| Mahdollisuuksien hallinta | 2761477 | Kun käytetään jaettua laskutusta, välitavoitteen (otsikon) poistaminen jättää orpotavoitteet. |
| Mahdollisuuksien hallinta | 2767595 | Kun materiaalin käyttötietue avataan päälomakkeessa, tietueen varattavissa oleva resurssi muuttuu tällä hetkellä kirjautuneena olevaksi käyttäjäksi. |
| Projektin suunnittelu ja seuranta | 2790384 | Pending OperationSet-aikakatkaisu on liian lyhyt. |
| Projektin suunnittelu ja seuranta | 2957840 | Tehtäviä ei voi tallentaa eikä sarakkeita voi lisätä Integrated Project Operationsin **Tehtävät-sivulle**. |
| Resurssienhallinta | 2751560 | Resurssivaatimuksen ensisijaiset organisaatioyksiköt ovat epäyhtenäisiä. |
| Alihankinta | 2853245 | Toimittajan laskurivin toteutunut vastaavuus ei päivitä tarkistuksen tilaa, jos sopimusrivi on jo linkitetty toimittajan laskuriviin. |
| Alihankinta | 2907231 | Toimittajan laskujen prosessivaihe ei voi tehdä ennakkoa. |
| Aika ja kulu | 2867363 | Tietueet eivät poistu Poissaolot/lomat hyväksyttäviksi -näkymästä, kun ne asetetaan jonoon hyväksyttäviksi. |
| Aika ja kulu | 2894405 | TESA: Käyttämätön POC-hakemisto aiheuttaa yhteensopivuusongelmia. |

### <a name="project-management-and-accounting-in-finance"></a>Projektinhallinta ja kirjanpito Financessa

Lisätietoja tähän päivitykseen liittyvistä virheenkorjauksista saa kirjautumalla sisään Microsoft Dynamics Lifecycle Servicesiin ja tarkastelemalla [tietokanta-artikkelia](https://fix.lcs.dynamics.com/Issue/Details?bugId=745468).
