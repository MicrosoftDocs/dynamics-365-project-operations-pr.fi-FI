---
title: Project Operations -kaksoiskirjoituksen karttaversiot
description: Tässä aiheessa on luettelo kaksoiskirjoituskartoista, joita tarvitaan Dynamics 365 Project Operationsissa.
author: sigitac
ms.date: 04/22/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 385893e8ecdb29f4dc411c233b9ae19bb2448dfd
ms.sourcegitcommit: 9916f536a71b6a0078297402564ac79308ec6890
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/18/2022
ms.locfileid: "8612746"
---
# <a name="project-operations-dual-write-map-versions"></a>Project Operations -kaksoiskirjoituksen karttaversiot

_**Käytetään:** Project Operationsin resursseihin ja ei-varastoitaviin perustuvissa skenaarioissa_

Käytettäessä Dynamics 365 Project Operationsia resurssi-/varastoimattomissa skenaarioissa, joukon kaksoiskirjoituskarttoja on oltava käynnissä ympäristössä. 

## <a name="prerequisite-maps-dual-write-orchestration-solution"></a>Vaadittavat kartat: Kaksoiskirjoituksen orkestrointiratkaisu

Project Operations -ratkaisun edellytykset ovat seuraavat kartat. Suorita seuraavassa taulukossa luetellut kartat ja ympäristöön liittyvät taulukkokartat.

| Taulukon yhdistämismääritys | Ensimmäinen synkronointi |
| --- | --- |
| Tapahtumarekisteri (msdyn_ledgers) | Edellyttää tietojen alustavaa synkronointia taulukkokartalle ja kaikille edellytyksille. Ensimmäisen synkronoinnin pääkohde on talous- ja toimintosovellukset. |
| Yritykset (cdm_companies) | Ei pakollinen. Järjestelmä täyttää tämän entiteetin automaattisesti, kun ympäristöt linkitetään kaksoiskirjoituksen avulla. |
| Asiakkaat V3 (tilit) | Ei vaadita valmistelua varten. |
| Toimittajat V2 (msdyn_vendors) | Ei vaadita valmistelua varten. |

1. Valitse määritysluettelosta Tapahtumarekisteri **(msdyn\_ledgers)** -määritys ja kaikki edellytykset ja valitse sitten **Ensimmäinen synkronointi** -valintaruutu. Valitse **Ensimmäisen synkronoinnin pääkohde** -kentässä sekä kirjanpitokartan että kaikkien edellytettyjen karttojen kohdalla **talous- ja toimintosovellukset**. Valitse **Suorita**.

![Kirjanpitomäärityksen synkronointi.](media/DW6.png)

2. Noudata edellä olevassa taulukossa mainittuja muita taulukkokarttoja samojen vaiheiden mukaisesti. Älä valitse **Ensimmäinen synkronointi** -valintaruutua, kun käytät näitä karttoja.

## <a name="project-operations-dual-write-maps"></a>Project Operationsin kaksoiskirjoituskartat

Project Operations -ratkaisun edellytyksenä ovat seuraavat kartat. Kaksoiskirjoituksen karttaversiot on kuvattu luettelossa alkaen toukokuun 2021 Project Operations -päivityksen versiosta 4.10.0.186.

| Entiteetin yhdistämismääritys | Viimeisin versio | Ensimmäinen synkronointi | Pakollinen Dynamics 365 Finance -versio |
| --- | --- | --- | --- |
| Projektitapahtuman integrointikohdesuhteet (msdyn\_transactionconnections) | 1.0.0.0 | Ei vaadita valmistelua varten. ||
| Projektisopimusotsikot (myyntitilaukset) | 1.0.0.1 | Ei vaadita valmistelua varten. ||
| Projektin sopimusrivit (salesorderdetails) | 1.0.0.0 | Ei vaadita valmistelua varten. ||
| Projektin rahoituslähde (msdyn_projectcontractsplitbillingrules) | 1.0.0.2 | Ei vaadita valmistelua varten. ||
| Project Operationsin materiaaliarvioiden integrointitaulukko (msdyn\_estimatelines) | 1.0.0.0 | Ei vaadita valmistelua varten. ||
| Projektin laskuehdotukset V2 (laskut) | 1.0.0.3 | Ei vaadita valmistelua varten. ||
| Project Operations -integroinnin todelliset arvot (msdyn_actuals) | 1.0.0.14 | Ei vaadita valmistelua varten. ||
| Project Operations -integraation sopimusrivien välitavoitteet (msdyn_contractlinescheduleofvalues) | 1.0.0.4 | Ei vaadita valmistelua varten. ||
| Project Operations -integraation entiteetti kuluarvioita varten (msdyn_estimatelines) | 1.0.0.2 | Ei vaadita valmistelua varten. ||
| Project Operations -integrointikohde tuntiarvioita varten (msdyn_resourceassignments) | 1.0.0.5 | Ei vaadita valmistelua varten. ||
| Project Operations -integroinnin projektikululuokkien vientientiteetti (msdyn_expensecategories) | 1.0.0.1 | Ei vaadita valmistelua varten. ||
| Project Operations -integroinnin projektikulujen vientientiteetti (msdyn_expenses) | 1.0.0.3 | Ei vaadita valmistelua varten. ||
| Project Operationsin integrointiprojektin toimittajalaskun vientientiteetti (msdyn_projectvendorinvoices) | 1.0.0.0 | Ei vaadita valmistelua varten. ||
| Project Operationsin integrointiprojektin toimittajalaskurivin vientientiteetti (msdyn_projectvendorinvoicelines) | 1.0.0.4 | Ei vaadita valmistelua varten. | 10.0.26 tai uudempi |
| Kaikkien yritysten projektiresurssiroolit (bookableresourcecategories) | 1.0.0.1 | Edellyttää taulukon kartan ensimmäistä synkronointia, jotta Dynamics 365 Dataverse -ympäristössä valmistelun aikana täytetään Projektipäällikkö- ja Ryhmän jäsen -resurssiroolit. Dataverse on ensimmäisen synkronoinnin päälähde. ||
| Projektitehtävät (msdyn_projecttasks) | 1.0.0.4 | Ei vaadita valmistelua varten. ||
| Projektin tapahtumaluokat (msdyn_transactioncategories) | 1.0.0.0 | Ei vaadita valmistelua varten. ||
| Projektit V2 (msdyn_projects) | 1.0.0.2 | Ei vaadita valmistelua varten. ||

Suorita luettelossa olevat kartat seuraavien vaiheiden mukaisesti.

1. Ota projektiresurssiroolit käyttöön **kaikissa yrityksissä (bookableresourcecategories)** -taulukkokartassa, koska tämä kartta edellyttää ensimmäistä synkronointia. Valitse **Perusmuoto synkronoitavaksi** -kentässä **Common data service**. 

 ![Resurssiroolitaulukkokartan synkronointi.](media/6ResourceInitialSync.jpg)

 Odota, kunnes kartan tila on **Käynnissä**, ennen kuin siirryt seuraavaan vaiheeseen.

2. Valitse kaikki jäljellä olevat pakolliset kartat. Voit suodattaa ne kaksoiskirjoituskartan luettelossa käyttämällä avainsanaa **Projekti** oikean yläkulman hakuruudussa. Voit valita useita karttoja ja suorittaa sen jälkeen. Lisätietoja on ohjeaiheessa [Useiden taulukkokarttojen hallinta](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/multiple-entity-maps). Ota myös käyttöön ja suorita liittyvät entiteettikartat.

### <a name="project-operations-dual-write-map-versions"></a>Project Operations -kaksoiskirjoituksen karttaversiot

Suorita aina ympäristön kartan uusin versio. Tietyt ominaisuudet ja toiminnot eivät ehkä toimi oikein seuraavissa tilanteissa:

- Karttaa ei aktivoida.
- Kartan uusinta versiota ei ole aktivoitu. 
- Liittyviä taulukkokarttoja ei aktivoida.

Voit tarkastella kartan aktiivista versiota **Kaksoiskirjoitus**-sivun **Versio**-sarakkeessa. Voit aktivoida kartan uuden version valitsemalla **taulukkokartan versiot**, valitsemalla uusimman ja tallentamalla valitun version. Jos olet mukauttanut valmiin taulukkokartan, muutokset täytyy kohdistaa uudelleen. Lue lisätietoja kohdasta [Ratkaisun elinkaaren hallinta](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).
