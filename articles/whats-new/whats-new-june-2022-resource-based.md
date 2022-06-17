---
title: Kesäkuun 2022 uudet ominaisuudet – Project Operations resurssien/ei-varastoitavien skenaarioissa
description: Tässä artikkelissa on tietoja Microsoft Dynamics 365 Project Operationsin resursseihin ja ei-varastoitaviin perustuvissa skenaarioissa kesäkuussa 2022 julkaistussa versiossa saatavilla olevista laatupäivityksistä.
author: sigitac
ms.date: 06/03/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: fde1f0be42eecfc5ee809cb9b2191d3aeae57131
ms.sourcegitcommit: 51745acac29dfacba43a4003d86baff4d6ca2fb8
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/14/2022
ms.locfileid: "8959419"
---
# <a name="whats-new-june-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>Kesäkuun 2022 uudet ominaisuudet – Project Operations resurssien/ei-varastoitavien skenaarioissa

_**Käytetään:** Project Operationsin resursseihin ja ei-varastoitaviin perustuvissa skenaarioissa_

Tämä artikkeli koskee seuraavia Microsoft Dynamics 365 Project Operationsin osia ja versioita:

- Project Operations Dataversessa ympäristöversio 4.43.0.77
- Projektinhallinta ja kirjanpito Dynamics 365 Finance -ympäristön versiossa 10.0.27

## <a name="project-operations-dual-write-maps-updates"></a>Project Operationsin kaksoiskirjoituskarttojen päivitys

Seuraavassa taulukossa on esitetty Project Operationsin kesäkuun 2022 julkaisuun muutetut tai lisätyt kaksoiskirjoituksen yhdistämismääritykset.

| Entiteetin yhdistämismääritys | Päivitetty versio | Kommentit |
| --- | --- | --- |
| Project Operationsin integrointiprojektin toimittajalaskun vientientiteetti (msdyn_projectvendorinvoices) | 1.0.0.1 | Vanhentunut vanha kenttä yhdistettiin uuteen kenttään toimittajan laskun tilan seurantaa varten. |

Suorita aina ympäristön kartan uusin versio ja ota käyttöön kaikki taulukkokartat, kun päivität Project Operations Dataverse -ratkaisua ja rahoitusratkaisun versiota. Jotkin ominaisuudet ja toiminnot eivät ehkä toimi oikein, jos kartan uusinta versiota ei ole aktivoitu. Voit tarkastella kartan aktiivista versiota **Kaksoiskirjoitus**-sivun **Versio**-sarakkeessa. Voit aktivoida kartan uuden version valitsemalla **Taulukkokartan versiot**, valitsemalla uusimman version ja tallentamalla sitten valitun version. Jos olet mukauttanut valmista taulukkokarttaa, voit käyttää muutokset uudelleen. Lue lisätietoja kohdasta [Ratkaisun elinkaaren hallinta](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Jos kartan käynnistämisen yhteydessä tulee ongelma, seuraa ohjeita [Puuttuvien taulukkosarakkeiden ongelma kartoissa](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) -osassa kaksoiskirjoituksen vianmääritysoppaassa.

## <a name="quality-updates"></a>Laatupäivitykset

### <a name="project-operations-on-dataverse"></a>Project Operations Dataversessä

| Ominaisuusalue | Viitenumero | Laatupäivitys |
| --- | --- | --- |
| Alihankinta | 2708885 | Korjattiin virhesanoma, joka annetaan, kun käyttäjä luo varattavissa olevan resurssin varauksen otsikon, johon ei ole täytetty varattavissa olevaa resurssia. |
| Projektin suunnittelu ja seuranta | 2629441 | Korjattiin työkulun käynnistyslogiikkaa siten, että päättymättömän silmukan syntyminen estetään projektitehtäviä päivitettäessä. |
| Aika ja kulut | 2641209 | Määrityksistä tai varauksista tuotavissa aikamerkinnöissä on säilytettävä varattavissa olevan resurssin viite. |
| Projektin suunnittelu ja seuranta | 2651148 | Projektiasiakirjan otsikon on oltava suojattu.|
| Projektin suunnittelu ja seuranta | 2653145 | Lisättiin tarkistuksia varmistamaan, ettei sellaisen projektitietueen luonti ole mahdollista, jonka nimessä on ei-kelvollisia merkkejä. |
| Aika ja kulut | 2654710 | Korjattiin **Hyväksynnät**-sivun suodatus. |
| Laskutus ja hinnoittelu | 2667805 | Lisättiin tarkistuksia estämään laskutetun toteutuneen myynnin luonti, jos taustalla ei ole laskuttamatonta toteutunutta myyntiä. |
| Laskutus ja hinnoittelu | 2668378 | Lisättiin tarkistukset estämään mukautetun hinnoitteludimension lisääminen, jos loogista nimeä ja kentän nimeä ei ole täytetty. |
| Alihankinta | 2677485 | Päivitettiin toimittajan laskurivien kaksoiskirjoitusmäärityksen kohdeversio. |
| Aika ja kulut | 2700428 | Parannettiin hyväksyntälogiikka varmistamaan, että projektin muut hyväksyntäjoukot voivat käsitellä, vaikka yksi hyväksyntäjoukko jumiutuisi järjestelmätöihin. |

### <a name="project-management-and-accounting-in-finance"></a>Projektinhallinta ja kirjanpito Financessa

Saat lisätietoja tähän päivitykseen liittyvistä virheenkorjauksista kirjautumalla sisään Microsoft Dynamics Lifecycle Services (LCS) -sovellukseen ja tarkastelemalla [Knowledge Base -artikkelia](https://fix.lcs.dynamics.com/Issue/Details?bugId=673271).
