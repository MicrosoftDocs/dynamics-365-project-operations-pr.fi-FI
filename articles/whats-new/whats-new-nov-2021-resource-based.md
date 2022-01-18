---
title: Uudet ominaisuudet marraskuussa 2021 – Project Operations resursseihin ja ei-varastoitaviin perustuvissa skenaarioissa
description: Tässä aiheessa on tietoja Project Operationsin resursseihin ja ei-varastoitaviin perustuvissa skenaarioissa -palvelun marraskuussa 2021 julkaistussa versiossa saatavilla olevista laatupäivityksistä.
author: sigitac
ms.date: 11/09/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: fb9dad5b04ef2933ed8a8d8211f888f13df5ba40
ms.sourcegitcommit: 9d20e7738cce195d344f5925a115741a1ce3ca36
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/21/2021
ms.locfileid: "7942881"
---
# <a name="whats-new-november-2021---project-operations-for-resourcenon-stocked-based-scenarios"></a>Uudet ominaisuudet marraskuussa 2021 – Project Operations resursseihin ja ei-varastoitaviin perustuvissa skenaarioissa

*Käytetään: Project Operationsin resursseihin ja ei-varastoitaviin perustuvissa skenaarioissa*

Tämä aihe koskee seuraavia Microsoft Dynamics 365 Project Operationsin osia ja versioita:

- Project Operations Dataversessa ympäristöversio version 4.26.0.145, 4.26.0.148, 4.26.0.150, 4.26.0.155
- Projektinhallinta ja kirjanpito Dynamics 365 Finance -ympäristöversiossa 10.0.22

## <a name="features-included-in-this-release"></a>Tähän julkaisuun sisältyvät ominaisuudet

Tähän julkaisuun sisältyvät seuraavat ominaisuudet:

- Projektien aikataulutussovelluksen ohjelmointirajapinnat (API:t) tukevat nyt projektisäilöjen luontia ja poistoa.

## <a name="project-operations-dual-write-maps-updates"></a>Project Operationsin kaksoiskirjoituskarttojen päivitys

Tässä versiossa ei ole päivityksiä Project Operationsin kaksoiskirjoituskartoille. Project Operationsin kaksoiskirjoituskarttojen luettelo ja versiot ovat kohdassa [Project Operationsin kaksi kaksoiskirjoituskarttojen versiot](/dynamics365/project-operations/environment/resource-dual-write-maps).

Suorita aina ympäristön kartan uusin versio ja ota käyttöön kaikki taulukkokartat, kun päivität Project Operations Dataverse -ratkaisua ja rahoitusratkaisun versiota. Jotkin ominaisuudet ja toiminnot eivät ehkä toimi oikein, jos kartan uusinta versiota ei ole aktivoitu. Voit tarkastella kartan aktiivista versiota **Kaksoiskirjoitus**-sivun **Versio**-sarakkeessa. Voit aktivoida kartan uuden version valitsemalla **Taulukkokartan versiot**, valitsemalla uusimman version ja tallentamalla sitten valitun version. Jos olet mukauttanut valmista taulukkokarttaa, voit käyttää muutokset uudelleen. Lue lisätietoja kohdasta [Ratkaisun elinkaaren hallinta](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Jos kartan käynnistämisen yhteydessä tulee ongelma, seuraa ohjeita [Puuttuvien taulukkosarakkeiden ongelma kartoissa](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) -osassa kaksoiskirjoituksen vianmääritysoppaassa.

## <a name="quality-updates"></a>Laatupäivitykset

### <a name="project-operations-in-dataverse"></a>Project Operations Dataversessä

| Ominaisuusalue | Viitenumero | Laatupäivitys |
| --- | --- | --- |
| Laskutus ja hinnoittelu | 2240080 | **Maksuehdot**-kenttää ei saa monistaa proformalaskussa. |
| Laskutus ja hinnoittelu | 2358236 | Laskun korjauksen on sallittava korjaukset, joissa on nollahintarivejä. |
| Resurssienhallinta | 2410072 | Salli tehtävään projektipäällikkönä määritetyn resurssin määrittäminen. |
| Laskutus ja hinnoittelu | 2430234 | Korjaa kustannustehokkuuden laskutoimitukseen liittyvät ongelmat. |
| Aika ja kulu | 2436978 | Salli ajan syöttäminen hh:mm-muodossa. |
| Laskutus ja hinnoittelu | 2448623 | Salli hinnastojen päivittäminen sen jälkeen, kun ne on liitetty organisaatioyksikköön. |
| Aika ja kulu | 2460396 | Salli aikamerkinnän poistaminen tyhjentämällä solu. |
| Laskutus ja hinnoittelu | 2467386 | Salli, että projekti, jolla on tehtävä, voidaan poistaa, vaikka tehtävä liittyisi voitettuun tarjoukseen. |
| Aika ja kulu | 2461744 | **Omat epäonnistuneet hyväksynnät** -näkymä sisältää vain projektin **Lähetetty**-tilassa olevat hyväksynnät. |
| Aika ja kulu | 2464082 | Poista linkki projektin hyväksynnistä hyväksyntäjoukkoon, kun kohdetila on hyväksytty. |
| Aika ja kulu | 2468108 | Aikataulutyö ei saa määrittää hyväksyntäjoukon **Käsittely**-tilaa. |
| Aika ja kulu | 2471503 | Poista seitsemän päivää vanhat hyväksyntäjoukot. |
| Laskutus ja hinnoittelu | 2480687 | Tarjousrivin viittausta ei saa poistaa, kun tarjousrivin välitavoite luodaan. |

### <a name="project-management-and-accounting-in-finance"></a>Projektinhallinta ja kirjanpito Financessa

| Ominaisuusalue | Viitenumero | Laatupäivitys |
| --- | --- | --- |
| Projektinhallinta ja kirjanpito | [584732](https://fix.lcs.dynamics.com/Issue/Details/?bugId=584732) | Projektikulutapahtumien edelliset toimittajasummat eivät näy tapahtumaluettelossa. |
| Projektinhallinta ja kirjanpito | [593068](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593068) | Konsernin sisäinen toimittajan lasku katkesi, kun toimittajan laskun integrointi on käytössä. |
| Projektinhallinta ja kirjanpito | [593382](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593382) | Projektilaskujen maksuehdot eivät toimi odotetusti. |
| Projektinhallinta ja kirjanpito | [596263](https://fix.lcs.dynamics.com/Issue/Details/?bugId=596263) | Kun toimittajan säilyttäminen julkaistaan, tositteen kirjauksen lisärivit ovat virheellisiä. |
| Projektinhallinta ja kirjanpito | [598758](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598758) | Kun Project Operationsin integrointi -kirjaus kirjataan, se epäonnistuu, koska sen tilin, jota ei julkaista, dimensiot puuttuvat. |
| Projektinhallinta ja kirjanpito | [602650](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602650) | **Projekti**-välilehteä ei voi muokata odottavassa toimittajan laskussa, kun nimikkeelle on määritetty lisäluokka. |
| Projektinhallinta ja kirjanpito | [605121](https://fix.lcs.dynamics.com/Issue/Details/?bugId=605121) | Siirtymisruutu puuttuu, jos et ole kirjautunut Project Operations Dataverseen. |
| Projektinhallinta ja kirjanpito | [602728](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602728) | Kun kirjaat tuottoa projektilaskusta kohdistettuun etuustapaukseen, ilmenee ongelma, koska tositteen tapahtumat eivät täsmää. |
| Projektinhallinta ja kirjanpito | [603624](https://fix.lcs.dynamics.com/Issue/Details/?bugId=603624) | Kun arvio luodaan laskun ehdotuksen julkaisemisen jälkeen, korjausrivit voidaan estää tuonnista. |
| Projektinhallinta ja kirjanpito | [606083](https://fix.lcs.dynamics.com/Issue/Details/?bugId=606083) | Kokonaan laskutettavan välitavoitetietueen muokkaaminen ei pitäisi olla mahdollista. |
| Matka ja kulut | [575305](https://fix.lcs.dynamics.com/Issue/Details/?bugId=575305) | Kaikki kuluraportit näkyvät, kun haet luokkaa Kulu-mobiilisovelluksessa. |
| Matka ja kulut | [583101](https://fix.lcs.dynamics.com/Issue/Details/?bugId=583101) | Toimittaja- ja arvonlisäverotapahtumien virheelliset summat kirjataan kulusta, joka on luotu luottokorttitapahtumasta. |
| Matka ja kulut | [583760](https://fix.lcs.dynamics.com/Issue/Details/?bugId=583760) | Jos päivität **kuluraportti**-sivun, näyttöön tulee epäolennainen varoitus. |
| Matka ja kulut | [598656](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598656) | Väärää väliaikaista hyväksyjää käytetään, kun poistat väliaikaisen hyväksyjän ja lähetät kuluraportin uudelleen työnkulun kautta. |
| Matka ja kulut | [612742](https://fix.lcs.dynamics.com/Issue/Details/?bugId=612742) | Näkyviin tulee kilometrien asennukseen liittyvä kirjausvirhe. |
