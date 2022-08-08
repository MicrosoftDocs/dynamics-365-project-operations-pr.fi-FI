---
title: Poistetut tai vanhentuneet Dynamics 365 Project Operations -ominaisuudet
description: Tässä artikkelissa käsitellään ominaisuuksia, jotka on poistettu tai joiden poistoa Dynamics 365 Project Operationsista suunnitellaan.
author: sigitac
ms.date: 03/16/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: f0fbaed028db11d8fb1551d304a40543faf35b0d
ms.sourcegitcommit: a798fed5c59e3fefa62cdfa42c852d529b33fd35
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/18/2022
ms.locfileid: "9028325"
---
# <a name="removed-or-deprecated-features-in-dynamics-365-project-operations"></a>Poistetut tai vanhentuneet Dynamics 365 Project Operations -ominaisuudet

_**Koskee:** Project Operations resursseihin ja ei-varastoitaviin perustuvissa skenaarioissa, Lite-käyttöönotto – kauppa proformalaskutukseen ja Project Operations varastoitavien ja tuotantopohjaisten skenaarioissa_

Tässä artikkelissa käsitellään ominaisuuksia, jotka on poistettu tai joiden poistoa Dynamics 365 Project Operationsista suunnitellaan.

- *Poistettu* toiminto ei ole enää käytettävissä tuotteessa.
- *Vanhentunut* toiminto ei ole aktiivisessa kehityksessä, ja se voidaan poistaa tulevassa päivityksessä.

Luettelon tarkoituksena on auttaa sinua tarkastelemaan näitä poistoja ja vanhentumisia, jotta voit suunnitella tulevaa.

> [!NOTE]
> Seuraavissa raporteissa on tarkempia tietoja talous- ja toimintosovellusten objekteista: [**Tekniset viitetiedot**](/dynamics/s-e/global/axtechrefrep_61). Voit verrata raporttien eri versioita saadaksesi lisätietoja objekteista, jotka on muutettu tai poistettu kussakin talous- ja toimintosovellusten versiossa.

## <a name="features-removed-or-deprecated-in-the-project-operations-march-2022-release"></a>Poistetut tai vanhentuneet ominaisuudet Project Operationsin maaliskuun 2022 julkaisussa

### <a name="project-management-and-accounting-always-create-adjustment-transaction-parameter"></a>Projektinhallinnan ja kirjanpidon "Luo aina oikaisutapahtuma" -parametri

| &nbsp; | &nbsp; |
|--------|--------|
| **Vanhentumisen/poistamisen syy** | Oikaisutapahtumat ovat pakollisia seurantatarkoituksia varten. Kun poisto on tehty, tämä parametri piilotetaan. Järjestelmä luo aina oikaisutapahtumat, kuten tällä hetkelläkin, kun parametriksi on määritetty **Kyllä**. |
| **Korvataanko toisella ominaisuudella?** | No |
| **Vaikutuksenalaiset tuotealueet** | Sovellus |
| **Käyttöönottovaihtoehto** | Project Operations tuotannon ja varastoitavien skenaarioissa |
| **Tila** | Vanhentunut: 1. maaliskuuta 2023 mennessä piilotamme parametrin ja muutamme järjestelmän toimintaa niin, että oikaisutapahtumat luodaan aina. |

### <a name="project-management-and-accounting-use-adjustment-date-as-new-project-date-parameter"></a>Projektinhallinnan ja kirjanpidon "Käytä oikaisupäivämäärää uutena projektipäivämääränä" -parametri

| &nbsp; | &nbsp; |
|--------|--------|
| **Vanhentumisen/poistamisen syy** | Tätä parametria käytettiin alun perin oikaisujen sallimiseen, kun kirjanpitokausi suljettiin. Se ei kuitenkaan ole enää pakollinen, koska tapahtuman kirjanpitopäiväksi voidaan muuttaa avoimen kauden ensimmäinen päivä, jos se on määritetty. Projektin päivämäärää ei saa muuttaa, koska se edustaa tapahtuman esiintymisen päivämäärää. |
| **Korvataanko toisella ominaisuudella?** | No |
| **Vaikutuksenalaiset tuotealueet** | Sovellus |
| **Käyttöönottovaihtoehto** | Project Operations tuotannon ja varastoitavien skenaarioissa |
| **Tila** | Vanhentunut: 1. maaliskuuta 2023 mennessä piilotamme parametrin ja muutamme järjestelmän toimintaa niin, että projektin päivämäärää ei koskaan muuteta oikaisuissa. |

### <a name="resource-request-workflow-in-project-operations-for-stockedproduction-based-scenarios"></a>Resurssipyynnön työnkulku Project Operationsin varastoitavien ja tuotantopohjaisissa skenaarioissa

| &nbsp; | &nbsp; |
|--------|--------|
| **Vanhentumisen/poistamisen syy** | Vanhentunut, koska käyttö on vähäistä ja tapahtumien määrän rajoitusten vuoksi. |
| **Korvataanko toisella ominaisuudella?** | No |
| **Vaikutuksenalaiset tuotealueet** | Sovellus |
| **Käyttöönottovaihtoehto** | Project Operations tuotannon ja varastoitavien skenaarioissa |
| **Tila** | Vanhentunut: 1.3.2023 mennessä käytöstä poistetaan mahdollisuus pyytää resursseja projektia varten työnkulun avulla. |

### <a name="project-invoice-proposal-page-without-header-and-lines-views"></a>Projektilaskuehdotus-sivu ilman Otsikko- ja Rivit-näkymiä

| &nbsp; | &nbsp; |
|--------|--------|
| **Vanhentumisen/poistamisen syy** | Vanhentunut, koska sivuun on tehty parannuksia, jotka on tehty yhdessä **Käytä projektilaskuehdotuksen ja laskukirjauskansion lomakkeita Otsikko- ja Rivit-näkymän kanssa** -ominaisuusavaimen kanssa. |
| **Korvataanko toisella ominaisuudella?** | Kyllä |
| **Vaikutuksenalaiset tuotealueet** | Sovellus |
| **Käyttöönottovaihtoehto** | Project Operations tuotanto/varastoitavat -skenaarioille; Project Operations resurssi/ei-varastoitava -skenaarioille |
| **Tila** | Vanhentunut: 1.3.2023 mennessä aiempi (vanha) sivu poistetaan käytöstä ja otetaan käyttöön **Käytä projektilaskuehdotuksen ja laskukirjauskansion lomakkeita Otsikko- ja Rivit-näkymän kanssa** -ominaisuusavain oletusarvoisesti. |

## <a name="features-removed-or-deprecated-in-the-project-operations-december-2021-release"></a>Poistetut tai vanhentuneet ominaisuudet Project Operationsin joulukuun 2021 julkaisussa

### <a name="collaboration-workspaces"></a>Yhteistyötilat

[Linkin luominen yhteistyötilaan (Projekti)](/dynamicsax-2012/appuser-itpro/create-or-link-to-a-collaboration-workspace-project)

| &nbsp; | &nbsp; |
|--------|--------|
| **Vanhentumisen/poistamisen syy** | Vanhentunut vähäisen käytön vuoksi. Asiakkaat, jotka käyttävät Project Operationsia resurssien ja ei-varastoitavien skenaarioita varten, voivat hyödyntää [Office-ryhmien yhteistyötä](../project-management/collaboration-groups.md). |
| **Korvataanko toisella ominaisuudella?** | No |
| **Vaikutuksenalaiset tuotealueet** | Sovellus  |
| **Käyttöönottovaihtoehto** | Project Operations tuotannon ja varastoitavien skenaarioissa |
| **Tila** | Vanhentunut: 1. joulukuuta 2022 mennessä, yhteistyötilojen tuen jatkamista ei suunnitella. |
