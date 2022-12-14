---
title: Uudet ominaisuudet marraskuussa 2022 – Project Operations resursseihin ja ei-varastoitaviin perustuvissa skenaarioissa
description: Tässä artikkelissa on tietoja Microsoft Dynamics 365 Project Operationsin resursseihin ja ei-varastoitaviin perustuvissa skenaarioissa marraskuussa 2022 julkaistussa versiossa saatavilla olevista laatupäivityksistä.
author: ryansandness
ms.date: 12/16/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: ryansandness
ms.openlocfilehash: 509e303aeb0567627590fd89c6888b59a414c6f1
ms.sourcegitcommit: 952fcefe33de192ad48f4108c3adbe658fd7b94f
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/08/2022
ms.locfileid: "9831081"
---
# <a name="whats-new-november-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>Uudet ominaisuudet marraskuussa 2022 – Project Operations resursseihin ja ei-varastoitaviin perustuvissa skenaarioissa

_**Käytetään:** Project Operationsin resursseihin ja ei-varastoitaviin perustuvissa skenaarioissa_

Tämä artikkeli koskee seuraavia Microsoft Dynamics 365 Project Operationsin osia ja versioita:

- Project Operations Dataversessa ympäristöversio 4.58.0.119
- Projektinhallinta ja kirjanpito Dynamics 365 Finance -ympäristön versiossa 10.0.30

## <a name="project-operations-dual-write-maps-updates"></a>Project Operationsin kaksoiskirjoituskarttojen päivitys

Tässä versiossa ei ole päivityksiä Project Operationsin kaksoiskirjoituskartoille. Project Operationsin kaksoiskirjoituskarttojen luettelo ja versiot ovat kohdassa [Project Operationsin kaksi kaksoiskirjoituskarttojen versiot](../environment/resource-dual-write-maps.md).

Suorita aina ympäristön kartan uusin versio ja ota käyttöön kaikki taulukkokartat, kun päivität Project Operations Dataverse -ratkaisua ja rahoitusratkaisun versiota. Jotkin ominaisuudet ja toiminnot eivät ehkä toimi oikein, jos kartan uusinta versiota ei ole aktivoitu. Voit tarkastella kartan aktiivista versiota **Kaksoiskirjoitus**-sivun **Versio**-sarakkeessa. Voit aktivoida kartan uuden version valitsemalla **Taulukkokartan versiot**, valitsemalla uusimman version ja tallentamalla sitten valitun version. Jos olet mukauttanut valmista taulukkokarttaa, voit käyttää muutokset uudelleen. Lue lisätietoja kohdasta [Ratkaisun elinkaaren hallinta](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Jos kartan käynnistämisen yhteydessä tulee ongelma, seuraa ohjeita [Puuttuvien taulukkosarakkeiden ongelma kartoissa](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) -osassa kaksoiskirjoituksen vianmääritysoppaassa.

## <a name="quality-updates"></a>Laatupäivitykset

### <a name="project-operations-on-dataverse"></a>Project Operations Dataversessä

| Ominaisuusalue | Viitenumero | Laatupäivitys |
| --- | --- | --- |
| Laskutus ja hinnoittelu | 2781818 | Avainta ei löytynyt -virhe, kun materiaalin käyttölokissa käytetään oletushintaa. |
| Laskutus ja hinnoittelu | 2922373 | Tarjousriviä ei voi linkittää projektiin, joka on suljettu hävittynä tarjouksena. |
| Laskutus ja hinnoittelu | 2943206 | Projekti-entiteetin **Sopimusrivi**-kentän on oltava valinnainen. |
| Laskutus ja hinnoittelu | 2953182 | Paranna korjauslaskujen virhesanomaa.|
| Laskutus ja hinnoittelu | 2959500 | Tarjousriviä ei voi linkittää projektitehtävään, joka on jo liitetty hävittyyn tarjoukseen.|
| Laskutus ja hinnoittelu | 2959560 | "Tämä asiakas on jo projektisopimuksessa" -sanoma vastaanotetaan, kun tarjous suljetaan voitettuna tietyillä kielialueilla. |
| Laskutus ja hinnoittelu | 3031727 | Resurssimääritykset epäonnistuvat ja Pakollinen kenttä "msdyn_Company" puuttuu -virhe. |
| Laskutus ja hinnoittelu | 3036905 | Omistavaa yritystä ei ole koskaan alustettu ProjectTeamMember-kohdassa. |
| Mahdollisuuksien hallinta | 2763519 | Tyhjäarvoinen viittausvirhe EnsureProjectContractAllowsUpdates-kohdassa. |
| Mahdollisuuksien hallinta | 2783798 | Kun tuot projektiarvioita tarjousrivillä, kulujen ja materiaaliarvioiden tehtävien kuvaukset puuttuvat.|
| Mahdollisuuksien hallinta | 2988635 | Paranna virheen kuvausta, kun asiakas poistetaan tarjouksesta. |
| Mahdollisuuksien hallinta | 3001191 | Tarjousta ei voi luoda mahdollisuudesta, jossa laskutustapa on tyhjäarvo. |
| Päivitys | 3012324 | Projektin muuntaminen epäonnistui projektissa, jonka nimessä oli ohjausmerkkejä, kuten sarkainmerkki. || Projektin suunnittelu ja seuranta | 2790384 | Pending OperationSet-aikakatkaisu on liian lyhyt. |
| Projektin suunnittelu ja seuranta | 3044275 | Puuttuva lokalisointi: missingProjectSchedulerErrorMessage. |
| Projektin suunnittelu ja seuranta | 3044277 | Project Recon -ruudukko ei lataudu, kun aikataulutusta ei ole määritetty.|
| Resurssienhallinta | 2943153 | Päivitä seuranta -välilehti, jossa näkyvät keston kaksi desimaalia.|
| Alihankinta | 2932774 | Toimittajan laskurivillä on virheellinen Vain luku -virhe. |
| Alihankinta | 2939556 | Toimittajan laskun otsikon tilaksi ei tulisi asettaa Luonnos, kun rivi poistetaan, jos se ei ole aktiivinen. |
| Aika ja kulu | 2939998 | Uusi TESA-versio on nyt käytössä ProjOpsissa. |


### <a name="project-management-and-accounting-in-finance"></a>Projektinhallinta ja kirjanpito Financessa

Lisätietoja tähän päivitykseen liittyvistä virheenkorjauksista saa kirjautumalla sisään Microsoft Dynamics Lifecycle Servicesiin ja tarkastelemalla [tietokanta-artikkelia](https://fix.lcs.dynamics.com/Issue/Details?bugId=745468).
