---
title: Syyskuun 2022 uudet toiminnot – Project Operationsin lite-käyttöönotto
description: Tässä artikkelissa on tietoja Microsoft Dynamics 365 Project Operations Lite -käyttöönoton syyskuussa 2022 julkaistussa versiossa saatavilla olevista laatupäivityksistä.
author: ramagadu
ms.date: 09/28/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: ramagadu
ms.openlocfilehash: 2cce7ae25f05258e8bf0bab9430324bc9b30e329
ms.sourcegitcommit: a2d720ac6d7ddb20a0967fe87992a376b2478208
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/04/2022
ms.locfileid: "9621251"
---
# <a name="whats-new-september-2022---project-operations-lite-deployment"></a>Syyskuun 2022 uudet toiminnot – Project Operationsin lite-käyttöönotto

_**Käytetään:** Lite-käyttöönotto – kauppa proformalaskutukseen_

Tämä artikkeli koskee seuraavia Microsoft Dynamics 365 Project Operationsin osia ja versioita:

- Project Operations Dataversessa ympäristöversio 4.46.0.60

## <a name="features-included-in-this-release"></a>Tähän julkaisuun sisältyvät ominaisuudet

| Ominaisuusalue | Ominaisuuden nimi | Lisätietoja |
| --- | --- | --- |
| Mahdollisuuksien hallinta | **Tarjousten muutokset ja aktivointi**<br>Project Operations tukee kokonaisvaltaisesti myyntiprosessia. Projektitarjoukset voidaan aktivoida ilmaisemaan tila, jossa tarjous on vain luku -muotoinen ja sitä arvioidaan. Aktivoituja tarjouksia voidaan muuttaa luomalla uusia tarjouksia, joissa on lisäävä versionumero. Aktivoidut projektitarjoukset tai tarjouksen muutokset sulkea voitettuna tai hävittynä. | [Projektitarjouksen aktivoiminen ja muuttaminen](/dynamics365/project-operations/sales/activation-and-revision) |
| Laskutus ja hinnoittelu | **Aikavyöhykkeestä riippumaton hinnan oletusarvo**<br>Project Operations ottanut käyttöön aikavyöhykkeestä riippumattoman päivämäärä kaikissa projektin todellisissa arvoissa. Uusi **Tapahtuman päivä** -kenttä on nyt käytettävissä kirjauskansion riveillä ja todellisissa arvoissa. Sen avulla voidaan tallentaa päivämäärä, jolloin tapahtuma tapahtui, ilman kyseisen päivämäärän muuttamista UCT-aikaan. Tätä päivämäärää käytetään alaspäin suuntautuvissa prosesseissa, kuten hinnan oletusarvossa ja laskun luonnissa. | <p>[Projektipohjaisten arvioiden ja toteutuneiden arvojen kustannusten määrittäminen](/dynamics365/project-operations/pro/pricing-costing/cost-price-resolution-sales)</p><p>[Projektipohjaisten arvioiden ja toteutuneiden myyntihintojen määrittäminen](/dynamics365/project-operations/pro/pricing-costing/sales-price-resolution-sales)</p> |
| Laskutus ja hinnoittelu | **Päivämääräperusteiset hinnan ohitukset Project Operationsissa**<br>Päivämääräperusteiset hinnan ohitukset antavat tavan korvata tai muuttaa hinnastossa tiettyjä hintoja. | [Päivämääräperusteiset hinnan ohitukset](/dynamics365/project-operations/pricing-costing/dateffective_price_overrides) |
| Aika ja kulu | **Yleinen hyväksyjä**<br>Tämä ominaisuus ottaa käyttöön ISV-toimittajien ja keskitetyn hyväksynnän riippumatta siitä, mikä on projektin tai tiimin jäsenen tila projektissa. | [Suojaus ja hyväksynnät](/dynamics365/project-operations/approvals/approvals-security) |

## <a name="quality-updates"></a>Laatupäivitykset

| Ominaisuusalue | Viitenumero | Laatupäivitys |
| --- | --- | --- |
| Laskutus ja hinnoittelu | 2754422 | Materiaali- ja kuluarviot eivät siirry Dynamics 365 Financeen, kun projekti kopioidaan Dataversessa. |
| Aika ja kulu | 2787409 | Muu kuin hyväksytty hyväksyjä voi hyväksyä muun kuin projektin aikamerkinnän. |
| Mahdollisuuksien hallinta | 2788907 | Päivitetty virhesanoma, joka koskee merkintöjä sisältävien tilausrivien yksilöllisyyden tarkistusta. |
| Aika ja kulu | 2842253 | Aikahyväksynnän tyhjäarvoisen poikkeuksen käsittely. |
| Laskutus ja hinnoittelu | 2844181 | Korrelaatiotunnuksen hakuvirhe estää laskun luonnin. |
| Laskutus ja hinnoittelu | 2876628 | Tarjousrivin tiedot, sopimusrivin tiedot – arvion hinnaston ratkaisussa on käytettävä hinnaston vanhoja päivämäärävälikenttiä. |
| Alihankinta | 2893222 | Jos alihankintariville ei ole määritetty roolia, kyseisen rivin valinnan pitäisi olla mahdollista kaikille ryhmän jäsenille roolista riippumatta. |
