---
title: Lokakuun 2022 uudet toiminnot – Project Operationsin lite-käyttöönotto
description: Tässä artikkelissa on tietoja Microsoft Dynamics 365 Project Operations Lite -käyttöönoton lokakuussa 2022 julkaistussa versiossa saatavilla olevista laatupäivityksistä.
author: ramagadu
ms.date: 11/17/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: ramagadu
ms.openlocfilehash: b6975e1f8645721fc03239b355b117eb664785f0
ms.sourcegitcommit: 1f162707ac342343fb5390fb9ae335e4cea4f3f2
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/29/2022
ms.locfileid: "9806611"
---
# <a name="whats-new-october-2022---project-operations-lite-deployment"></a>Lokakuun 2022 uudet toiminnot – Project Operationsin lite-käyttöönotto

_**Käytetään:** Lite-käyttöönotto – kauppa proformalaskutukseen_

Tämä artikkeli koskee seuraavia Microsoft Dynamics 365 Project Operationsin osia ja versioita:

- Project Operations Dataversessa ympäristöversio 4.57.0.176

## <a name="features-included-in-this-release"></a>Tähän julkaisuun sisältyvät ominaisuudet

| Ominaisuusalue | Ominaisuuden nimi | Lisätietoja |
| --- | --- | --- |
| Projektin suunnittelu ja seuranta | **Project Operationsin ulkoinen aikataulutus**<br>Ulkoisen aikataulutustilan avulla voit natiivisti luoda, päivittää ja poistaa entiteettejä, jotka liittyvät työrakenteisiin (WBS) käyttämällä Dataversen luonnollisia ohjelmointirajapintoja, mutta ilman Microsoft Project for the Webin pakottamia nykyisiä rajoituksia. | [Ulkoinen aikataulutus](/dynamics365/project-operations/project-management/external-scheduling) |
| Käyttöönotto ja määritys | <p>**Salli asiakkaiden valita käyttöönottotyyppi**<br>Project Operationsin tuotepohjaisten päivitysten (PDU) avulla Project Operationsin kaksoiskirjoitusratkaisu asennetaan automaattisesti, kun kaksiosaiset ydinratkaisut ja orkestrointiratkaisut asennetaan ympäristöön.</p><p>Tämä ominaisuus esittelee projektiparametreissa uuden **Ratkaisun päivityksen käyttäytyminen** -parametrin. Kun tämän parametrin arvo on **vain Lite**, PUD:it eivät enää asenna Project Operationsin kaksoiskirjoitusratkaisua automaattisesti, vaikka kaksoiskirjoituksen ydin- ja orkestrointiratkaisut on asennettu ympäristöön. Tästä käyttäytymisestä on hyötyä asiakkaille, jotka haluavat käyttää kaksoiskirjoitusratkaisuja integroidakseen myyntitilaukset rahoitus- ja toimintosovelluksiin, mutta haluavat käyttää Project Operationsia Lite-tilassa (integroimatta niitä rahoitus- ja toimintosovelluksiin).</p> | |

## <a name="quality-updates"></a>Laatupäivitykset

| Ominaisuusalue | Viitenumero | Laatupäivitys |
| --- | --- | --- |
| Laskutus ja hinnoittelu | 2316317 | Järjestelmän avulla voidaan luoda lasku, jolla ei ole laskutettavia tapahtumia. |
| Laskutus ja hinnoittelu | 2737300 | Tarkista, onko Asiakas-kentän käytettävyys tarkistettu, ennen kuin lomaketta käytetään. |
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
| Resurssienhallinta | 2751560 | Resurssivaatimuksen ensisijaiset organisaatioyksiköt ovat epäyhtenäisiä. |
| Alihankinta | 2907231 | Toimittajan laskujen prosessivaihe ei voi tehdä ennakkoa. |
| Aika ja kulu | 2867363 | Tietueet eivät poistu Poissaolot/lomat hyväksyttäviksi -näkymästä, kun ne asetetaan jonoon hyväksyttäviksi. |
| Aika ja kulu | 2894405 | TESA: Käyttämätön POC-hakemisto aiheuttaa yhteensopivuusongelmia. |
