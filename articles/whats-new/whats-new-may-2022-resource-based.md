---
title: Toukokuun 2022 uudet ominaisuudet - Project Operations resursseihin/ei-varastoitaviin perustuvissa skenaarioissa
description: Tässä artikkelissa on tietoja Microsoft Dynamics 365 Project Operationsin resursseihin ja ei-varastoitaviin perustuvissa skenaarioissa toukokuussa 2022 julkaistussa versiossa saatavilla olevista laatupäivityksistä.
author: sigitac
ms.date: 05/02/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: beb75fc4b721d52cddbdaf2d20194218cefced5e
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8921390"
---
# <a name="whats-new-may-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>Toukokuun 2022 uudet ominaisuudet - Project Operations resursseihin/ei-varastoitaviin perustuvissa skenaarioissa

_**Käytetään:** Project Operationsin resursseihin ja ei-varastoitaviin perustuvissa skenaarioissa_

Tämä artikkeli koskee seuraavia Microsoft Dynamics 365 Project Operationsin osia ja versioita:

- Project Operations Dataversessa ympäristöversio 4.42.0.70
- Projektinhallinta ja kirjanpito Dynamics 365 Finance -ympäristön versiossa 10.0.26

## <a name="project-operations-dual-write-maps-updates"></a>Project Operationsin kaksoiskirjoituskarttojen päivitys

Tässä versiossa ei ole päivityksiä Project Operationsin kaksoiskirjoituskartoille. Project Operationsin kaksoiskirjoituskarttojen luettelo ja versiot ovat kohdassa [Project Operationsin kaksi kaksoiskirjoituskarttojen versiot](../environment/resource-dual-write-maps.md).

Suorita aina ympäristön kartan uusin versio ja ota käyttöön kaikki taulukkokartat, kun päivität Project Operations Dataverse -ratkaisua ja rahoitusratkaisun versiota. Jotkin ominaisuudet ja toiminnot eivät ehkä toimi oikein, jos kartan uusinta versiota ei ole aktivoitu. Voit tarkastella kartan aktiivista versiota **Kaksoiskirjoitus**-sivun **Versio**-sarakkeessa. Voit aktivoida kartan uuden version valitsemalla **Taulukkokartan versiot**, valitsemalla uusimman version ja tallentamalla sitten valitun version. Jos olet mukauttanut valmista taulukkokarttaa, voit käyttää muutokset uudelleen. Lue lisätietoja kohdasta [Ratkaisun elinkaaren hallinta](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Jos kartan käynnistämisen yhteydessä tulee ongelma, seuraa ohjeita [Puuttuvien taulukkosarakkeiden ongelma kartoissa](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) -osassa kaksoiskirjoituksen vianmääritysoppaassa.

## <a name="quality-updates"></a>Laatupäivitykset
### <a name="project-operations-on-dataverse"></a>Project Operations Dataversessä

| Ominaisuusalue | Viitenumero | Laatupäivitys |
| --- | --- | --- |
| Resurssien hallinta | 2634019 | Parannetut liiketoimintatarkistuksen sanomat lisättäessä yleisiä ryhmän jäseniä resursseiksi. |
| Projektin suunnittelu ja seuranta | 2648515 | Rajoitetut päivitykset kohtaille **ownerid**, **state** ja **status** aikataulutusentiteetissä. |
| Laskutus ja hinnoittelu | 2653167 | **Arviot**-ruudukon desimaalierottimen on oltava **henkilökohtaisten asetusten** muotoasetusten mukainen. |
| Laskutus ja hinnoittelu| 2662251 | **Korjattu yksikkö**- ja **Yksikköryhmä**-kenttien arvot ovat oletusarvoja luotaessa tietueita materiaaliarvioihin. |
| Laskutus ja hinnoittelu| 2571408 | Laskuttamattomien myyntien toteutuneet arvot leimataan proformalaskutunnuksella luotaessa laskuluonnosta. |

### <a name="project-management-and-accounting-in-dynamics-365-finance"></a>Projektinhallinta ja kirjanpito Dynamics 365 Financessa

Saat lisätietoja tähän päivitykseen liittyvistä virheenkorjauksista kirjautumalla sisään Microsoft Dynamics Lifecycle Services (LCS) -sovellukseen ja tarkastelemalla [Knowledge Base -artikkelia](https://fix.lcs.dynamics.com/Issue/Details?bugId=662864).
