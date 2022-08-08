---
title: uudet ominaisuudet huhtikuu 2022 – Project Operations resursseihin ja ei-varastoitaviin perustuvissa skenaarioissa
description: Tässä artikkelissa on tietoja Microsoft Dynamics 365 Project Operationsin resursseihin ja ei-varastoitaviin perustuvissa skenaarioissa huhtikuussa 2022 julkaistussa versiossa saatavilla olevista laatupäivityksistä.
author: sigitac
ms.date: 04/08/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 999006b2c2fe2b31d6e47910a3f1a55cab415f0e
ms.sourcegitcommit: 5c971b15295046b3c92ff6638dd1352129f1c390
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 07/01/2022
ms.locfileid: "9110880"
---
# <a name="whats-new-april-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>uudet ominaisuudet huhtikuu 2022 – Project Operations resursseihin ja ei-varastoitaviin perustuvissa skenaarioissa

_**Käytetään:** Project Operationsin resursseihin ja ei-varastoitaviin perustuvissa skenaarioissa_

Tämä artikkeli koskee seuraavia Microsoft Dynamics 365 Project Operationsin osia ja versioita:

- Project Operations Dataversessa ympäristöversio 4.41.0.45
- Projektinhallinta ja kirjanpito Dynamics 365 Finance -ympäristön versiossa 10.0.26

## <a name="features-included-in-this-release"></a>Tähän julkaisuun sisältyvät ominaisuudet

Hankintaluokkia voidaan käyttää projektin ostotilauksissa ja odottavissa toimittajan laskuissa. Lisätietoja: [Hankintaluokkien käyttö projektin ostotilauksissa ja odottavissa toimittajan laskuissa](../procurement/configure-procurement-categories.md).

## <a name="project-operations-dual-write-maps-updates"></a>Project Operationsin kaksoiskirjoituskarttojen päivitys

Seuraavassa taulukossa on esitetty Project Operationsin maaliskuun 2022 julkaisuun muutetut tai lisätyt kaksoiskirjoituksen yhdistämismääritykset.

| Entiteetin yhdistämismääritys | Päivitetty versio | Kommentit |
| -------------- | ------------------- | ------------|
| Project Operationsin integrointiprojektin toimittajalaskurivin vientientiteetti msdyn\_projectvendorinvoicelines | 1.0.0.4 | Tämä yhdistämismääritys tukee hankintaluokkien käyttöä ostotilauksissa ja odottavissa toimittajan laskuissa. |

Suorita aina ympäristön kartan uusin versio ja ota käyttöön kaikki taulukkokartat, kun päivität Project Operations Dataverse -ratkaisua ja rahoitusratkaisun versiota. Jotkin ominaisuudet ja toiminnot eivät ehkä toimi oikein, jos kartan uusinta versiota ei ole aktivoitu. Voit tarkastella kartan aktiivista versiota **Kaksoiskirjoitus**-sivun **Versio**-sarakkeessa. Voit aktivoida kartan uuden version valitsemalla **Taulukkokartan versiot**, valitsemalla uusimman version ja tallentamalla sitten valitun version. Jos olet mukauttanut valmista taulukkokarttaa, voit käyttää muutokset uudelleen. Lue lisätietoja kohdasta [Ratkaisun elinkaaren hallinta](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Jos kartan käynnistämisen yhteydessä tulee ongelma, seuraa ohjeita [Puuttuvien taulukkosarakkeiden ongelma kartoissa](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) -osassa kaksoiskirjoituksen vianmääritysoppaassa.

## <a name="quality-updates"></a>Laatupäivitykset

### <a name="project-operations-on-dataverse"></a>Project Operations Dataversessä

| Ominaisuusalue | Viitenumero | Laatupäivitys |
| ------------ | ---------------- | -------------- |
| Aika ja kulut | 2573900 | **Modernin hyväksynnän** ominaisuuden on oltava oletusarvoisesti käytössä. |
| Laskutus ja hinnoittelu | 2603313 | Korjattu tietueen kaksoiskappalevirhe, joka esti tuotteen sisältävän tarjouksen ja sopimusrivien lisäämisen. |
| Käyttöönotto ja määritys | 2611368 | Asiakkaiden on voitava lisätä ratkaisuun enintään viisi mukautettua entiteettiä uuden sovelluksen suunnitteluohjelman avulla. |
| Aika ja kulut | 2628285 | Korjattu ongelma, joka vaikutti siihen, pystyikö määrittämään oikean resurssiluokan aikamerkinnän tuonnin aikana. |
|   Mahdollisuuksien hallinta| 2628815 | Päivitä tarjousrivin tietokuvauksen merkkirajoitus vastaamaan tehtävän aiheen merkkirajoitusta, jotta tuonti onnistuu tehtäville, joissa aiheessa on yli 100 merkkiä. |
| Aika ja kulut| 2629547 | Projektin hyväksyntöjen **Lähettäjä**-kentän on osoitettava tietueen lähettäneeseen käyttäjään. |
| Aika ja kulut| 2629865 | **Kopioi luokka** -kenttä tehtäville, kun projektit kopioidaan. |
| Aika ja kulut| 2636463 | Korjattu hyväksyntöjen suodattimet uusissa hyväksyntälomakkeissa. |
| Projektin suunnittelu ja seuranta | 2648300 | Korjattu ongelma, joka estää projektin omistajan muuttamisen. |
| Laskutus ja hinnoittelu | 2563000 | Jos valuutta eroaa sopimusvaluutasta, sen laskuttamattoman myynnin kirjauskansiorivejä ei saa sallia. |

### <a name="project-management-and-accounting-in-dynamics-365-finance"></a>Projektinhallinta ja kirjanpito Dynamics 365 Financessa

Saat lisätietoja tähän päivitykseen liittyvistä virheenkorjauksista kirjautumalla sisään Microsoft Dynamics Lifecycle Services (LCS) -sovellukseen ja tarkastelemalla [Knowledge Base -artikkelia](https://fix.lcs.dynamics.com/Issue/Details?bugId=662864).
