---
title: Huhtikuun 2021 - Project Operations lite -käyttöönotto
description: Tässä aiheessa on tietoja Project Operations lite -käyttöönoton huhtikuussa 2021 julkaistussa versiossa saatavilla olevista laatupäivityksistä.
author: sigitac
manager: tfehr
ms.date: 04/07/2021
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: bd6fbe8d75fbe9157a97d2edd38d40a97395c924
ms.sourcegitcommit: 8ff9fe396db6dec581c21cd6bb9acc2691c815b0
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/07/2021
ms.locfileid: "5868034"
---
# <a name="whats-new-april-2021---project-operations-lite-deployment"></a>Huhtikuun 2021 - Project Operations lite -käyttöönotto

_Käytetään: Lite-käyttöönotto – kauppa proformalaskutukseen_

Tämä aihe koskee seuraavia Dynamics 365 Project Operationsin komponentteja ja versioita:

  - Project Operations Dataverse-ympäristön versiossa 4.9.0.221 

## <a name="features-included-in-this-release"></a>Tähän julkaisuun sisältyvät ominaisuudet

Tähän julkaisuun sisältyvät seuraavat ominaisuudet:

- Projektien ei-varastoitava materiaali. Tärkeitä ominaisuuksia ovat seuraavat:
  - Ei-varastoitavien materiaalien arviointi ja hinnoittelu projektin myyntikierron aikana. Lisätietoja on kohdassa [Luettelotuotteiden kustannus- ja myyntihintojen määrittäminen – lite](../pricing-costing/set-up-cost-sales-rates-catalog-products.md).
  - Ei-varastoitavien materiaalien käytön seuranta projektin toimituksen aikana. Lisätietoja on kohdassa [Materiaalikäytön kirjaaminen projekteihin ja projektitehtäviin](../../material/material-usage-log.md).
  - Laskutuksessa käytettiin ei-varastoitavan materiaalin kustannuksia. Lisätietoja on kohdassa [Laskutuksen jonon hallinta – lite](../proforma-invoicing/manage-billing-backlog-sales.md#product-billing-backlog).
  - Uudet ohjelmointirajapinnat Dynamics 365 Dataversessä sallivat toimintojen luomisen, päivittämisen ja poistamisen **Aikataulutusentiteettien** avulla. Lisätietoja on kohdassa [Aikataulutuksen ohjelmointirajapintojen käyttö toimintojen suorittamiseen ajoitusentiteeteillä](../../project-management/schedule-api-preview.md).

## <a name="quality-updates"></a>Laatupäivitykset

| **Ominaisuusalue** | **Viitenumero** | **Laatupäivitys** |
| --- | --- | --- |
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
