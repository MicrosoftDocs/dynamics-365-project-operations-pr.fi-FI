---
title: Toukokuun 2021 uudet ominaisuudet - Project Operations lite -käyttöönotto
description: Tässä aiheessa on tietoja Project Operations lite -käyttöönoton toukokuussa 2021 julkaistussa versiossa saatavilla olevista laatupäivityksistä.
author: sigitac
ms.date: 05/17/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 14ff7f1f7374ffe885c511fd693cda5b7023c5beb53adb45042ddda1e932c93d
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/06/2021
ms.locfileid: "7005972"
---
# <a name="whats-new-may-2021---project-operations-lite-deployment"></a>Toukokuun 2021 uudet ominaisuudet - Project Operations lite -käyttöönotto

_Käytetään: Lite-käyttöönotto – kauppa proformalaskutukseen_

Tämä aihe koskee seuraavia Dynamics 365 Project Operationsin komponentteja ja versioita:

   - Project Operations Dataverse-ympäristön versiossa 4.10.0.186.

## <a name="features-included-in-this-release"></a>Tähän julkaisuun sisältyvät ominaisuudet

Tähän julkaisuun sisältyvät seuraavat ominaisuudet:

- [Aikataulutustilat](../../project-management/scheduling-modes.md): Projektipäälliköt voivat nyt määrittää, tulisiko projektia hallita käyttämällä kiinteän keston, kiinteän työmäärän vai kiinteiden yksiköiden aikataulutustilaa.

## <a name="quality-updates"></a>Laatupäivitykset

| **Ominaisuusalue** | **Viitenumero** | **Laatupäivitys** |
| --- | --- | --- |
| Laskutus ja hinnoittelu | 2224568 | Lisätty logiikka, jonka avulla voidaan ottaa käyttöön mukautuksia, joihin liittyy laskun vahvistuslaajennus. |
| Laskutus ja hinnoittelu | 2101098 | Proformalaskun oletuskenttien logiikkaa parannettu. Näihin kenttiin sisältyy **Laskutusosoite**, **Laskutusosoitteen nimi** ja **Maksuehdot**. Kentät saadaan nyt oletusarvoisesti vastaavasta projektisopimuksen asiakastietueesta. |
| Laskutus ja hinnoittelu | 2021413 | **Tehtävä**-entiteetin **Todelliset kustannukset**- ja **Myynti**-kentät päivitettiin sisältämään myyntiarvot tehtävien laskuttamattomista ja laskutetuista kuluista. |
| Laskutus ja hinnoittelu | 2182110 | Kun kopioit projektisopimuksen, sopimusrivin tunnus luodaan uudelleen kohdeprojektisopimuksessa, jotta se olisi yksilöivä. |
| Mahdollisuuksien hallinta | 2186741 | Lisätyt vahvistukset varmistavat, että **Alkuperä**-kenttää tai tapahtumatyyppiä ei voi päivittää aiemmin luoduissa tarjousrivin tiedoissa. |
| Mahdollisuuksien hallinta | 2191353 | Välitavoitteiden luontia ei voi sallia ajan ja materiaalin sopimusrivillä. |
| Mahdollisuuksien hallinta | 2216956 | **Hintojen päivityksen** ongelmat on korjattu. |
| Suunnittelu ja seuranta | 2182979 | Projektin kopiointitoimintoa on parannettu, jotta kuluarviorivit kopioidaan alkuperäisestä projektista. |
| Suunnittelu ja seuranta | 2184144 | Projektin kopiointitoimintoa on parannettu, jotta resurssin työtehtävän nimi kopioidaan alkuperäisestä projektista. |
| Suunnittelu ja seuranta | 2184799 | Projektin kopioinnin aikaista hallintaa tiukennettiin siten, ettei arvioitua aloituspäivää voi muuttaa kopioinnin aikana. |
| Suunnittelu ja seuranta | 2185134 | Kun projektia kopioidaan, kohdeprojektin arvioiduksi aloituspäiväksi määritetään tämänhetkinen päivämäärä. |
| Suunnittelu ja seuranta | 2196373 | Varmista, että projektipäällikön ja ryhmän jäsenten tietueista ei synny identtisiä kopioita, kun projekti kopioidaan. |
| Suunnittelu ja seuranta | 2211833 | Resurssimääritykset kopioidaan lähdeprojektin tehtävästä kohdeprojektiin. |
| Suunnittelu ja seuranta | 2186541 | Korjattu **Arviot**-ruudukon ongelmat, kun ryhmittelyehto on **Resurssi**. |
| Suunnittelu ja seuranta | 2166906 | Tehtävän tapahtumaluokka on kopioittava **Resurssin määritys** -entiteettiin. |
| Resurssienhallinta | 2125362 | Korjattiin ongelmat, jotka liittyivät yleisen ryhmän jäsenen luomiseen tuntipohjaisella kohdistusmenetelmällä. |
| Aika ja kulu | 2113603 | Korjattiin mukautusongelma, joka liittyi määritteiden poistamiseen **Aikamerkintä**-sivulta. Järjestelmä tarkistaa, onko määrite olemassa sivulla, ennen kuin se käyttää määritettä komentosarjan avulla. |
| Aika ja kulu | 2204377 | Kopioidut tuntiraportit näkyvät automaattisesti, kun valitset **Kopioi viikko**. |
| Aika ja kulu | 2209059 | Dynamics 365 Field Servicen aikamerkintöjen **Tila**-kenttää voi muokata. |
