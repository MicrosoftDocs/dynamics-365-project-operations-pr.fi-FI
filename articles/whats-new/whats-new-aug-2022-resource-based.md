---
title: Elokuun 2022 uudet ominaisuudet – Project Operations resurssien/ei-varastoitavien skenaarioissa
description: Tässä artikkelissa on tietoja Microsoft Dynamics 365 Project Operationsin resursseihin ja ei-varastoitaviin perustuvissa skenaarioissa elokuussa 2022 julkaistussa versiossa saatavilla olevista laatupäivityksistä.
author: ramagadu
ms.date: 07/19/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: ramagadu
ms.openlocfilehash: 4042dca72a33f48e04e51af2a3cfd2da83146afd
ms.sourcegitcommit: 7ed8e77a92917f2d242988ca02bd7de9571cce5e
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/02/2022
ms.locfileid: "9403852"
---
# <a name="whats-new-august-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>Elokuun 2022 uudet ominaisuudet – Project Operations resurssien/ei-varastoitavien skenaarioissa

_**Käytetään:** Project Operationsin resursseihin ja ei-varastoitaviin perustuvissa skenaarioissa_

Tämä artikkeli koskee seuraavia Microsoft Dynamics 365 Project Operationsin osia ja versioita:

- Project Operations Dataversessa ympäristöversio 4.45.0.53
- Projektinhallinta ja kirjanpito Dynamics 365 Finance -ympäristön versiossa 10.0.28

## <a name="project-operations-dual-write-maps-updates"></a>Project Operationsin kaksoiskirjoituskarttojen päivitys

Tässä versiossa ei ole päivityksiä Project Operationsin kaksoiskirjoituskartoille. Project Operationsin kaksoiskirjoituskarttojen luettelo ja versiot ovat kohdassa [Project Operationsin kaksi kaksoiskirjoituskarttojen versiot](../environment/resource-dual-write-maps.md).

Suorita aina ympäristön kartan uusin versio ja ota käyttöön kaikki taulukkokartat, kun päivität Project Operations Dataverse -ratkaisua ja rahoitusratkaisun versiota. Jotkin ominaisuudet ja toiminnot eivät ehkä toimi oikein, jos kartan uusinta versiota ei ole aktivoitu. Voit tarkastella kartan aktiivista versiota **Kaksoiskirjoitus**-sivun **Versio**-sarakkeessa. Voit aktivoida kartan uuden version valitsemalla **Taulukkokartan versiot**, valitsemalla uusimman version ja tallentamalla sitten valitun version. Jos olet mukauttanut valmista taulukkokarttaa, voit käyttää muutokset uudelleen. Lue lisätietoja kohdasta [Ratkaisun elinkaaren hallinta](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Jos kartan käynnistämisen yhteydessä tulee ongelma, seuraa ohjeita [Puuttuvien taulukkosarakkeiden ongelma kartoissa](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) -osassa kaksoiskirjoituksen vianmääritysoppaassa.

## <a name="quality-updates"></a>Laatupäivitykset

### <a name="project-operations-on-dataverse"></a>Project Operations Dataversessä

| Ominaisuusalue | Viitenumero | Laatupäivitys |
| --- | --- | --- |
|   Mahdollisuuksien hallinta | 2762089 | Virheiden käsittely, kun sopimus suljetaan hävittynä, jos automaattinen tallennus on poistettu organisaatiossa käytöstä.|
|Projektin suunnittelu ja seuranta | 2767841 | Telemetria päivittää projektientiteetin luonti- tai päivitysskenaariot.|
|Laskutus ja hinnoittelu | 2771072 | Tyhjäarvoinen viittauspoikkeuksen käsittely tarjousta voittaessa.|
|Laskutus ja hinnoittelu | 2844181 |Korrelaatiotunnuksen saaminen ja laskun luonnin estämisen epäonnistuminen.|
|Laskutus ja hinnoittelu | 2852836 | Konsernin toteutuneet arvot puuttuvat CE:ssä luoduista ja hyväksytyistä konsernin kuluista.|


### <a name="project-management-and-accounting-in-finance"></a>Projektinhallinta ja kirjanpito Financessa

Saat lisätietoja tähän päivitykseen liittyvistä virheenkorjauksista kirjautumalla sisään Microsoft Dynamics Lifecycle Services (LCS) -sovellukseen ja tarkastelemalla [Knowledge Base -artikkelia](https://fix.lcs.dynamics.com/Issue/Details?bugId=694438).
