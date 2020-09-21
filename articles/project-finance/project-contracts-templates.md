---
title: Synkronoi projektisopimuksia ja projekteja suoraan Project Service Automationista Finance and Operationsiin
description: Tässä aiheessa kuvataan malli ja sen pohjana olevat tehtävät, joita käytetään projektisopimusten ja projektien synkronoimiseen suoraan Microsoft Dynamics 365 Project Service Automationista Dynamics 365 Financeen.
author: KimANelson
manager: AnnBe
ms.date: 09/09/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: 57fe4ae8-6ee9-442d-9933-d525b5415db8
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2017-12-13
ms.dyn365.ops.version: AX 7.3.0
ms.openlocfilehash: b914a56b306639253a8cd3b7caa754da175b6df2
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/24/2020
ms.locfileid: "3751125"
---
# <a name="synchronize-project-contracts-and-projects-directly-from-project-service-automation-to-finance-and-operations"></a>Synkronoi projektisopimuksia ja projekteja suoraan Project Service Automationista Finance and Operationsiin

[!include[banner](../includes/banner.md)]

Tässä aiheessa kuvataan malli ja sen pohjana olevat tehtävät, joita käytetään projektisopimusten ja projektien synkronoimiseen suoraan Dynamics 365 Project Service Automationista Dynamics 365 Financeen.

> [!NOTE] 
> Jos käytössäsi on Enterprise Edition 7.3.0, sinun täytyy asentaa tietokanta 4074835.

## <a name="data-flow-for-project-service-automation-to-finance"></a>Tietovuo Project Service Automationista Financeen

> [!NOTE]
> Ennen kuin voit käyttää Project Service Automationin integrointiratkaisua Financeen, sinun on tunnettava Dynamics 365:n tietojen integrointitoiminto.

Project Service Automationin integrointiratkaisua Financeen käyttää tietojen integrointitoimintoa tietojen synkronointiin Project Service Automationin ja Financen eri esiintymien välillä. Tietojen integrointitoiminnossa käytettävissä oleva integrointimalli mahdollistaa projektisopimusten, projektien, projektisopimuksen rivien ja projektisopimuksen rivien välitavoitteiden tietovuon Project Service Automationista Financeen.

Seuraavassa kuvassa on esitetty, miten tiedot synkronoidaan Project Service Automationin ja Financen välillä.

[![Tietovuo Project Service Automationin Financeen integroinnissa](./media/ProjectsAndContractsFlow_upd.JPG)](./media/ProjectsAndContractsFlow.JPG)

## <a name="templates-and-tasks"></a>Mallit ja tehtävät

Jos haluat käyttää käytettävissä olevia malleja, valitse Microsoft Power Appsin hallintakeskuksessa **Projektit** ja sitten oikeassa yläkulmassa **Uusi projekti** valitaksesi julkisia malleja.

Seuraavia malleja ja pohjana olevia tehtäviä käytetään projektisopimusten ja projektien synkronoimiseen Project Service Automationista Financeen:

### <a name="integrating-with-dynamics-365-project-service-automation-v2x"></a>Integrointi Dynamics 365 Project Service Automationin versioon v2.x
- **Tietojen integroinnin mallin nimi:** Projektit ja sopimukset (PSA:sta Fin:iin ja Ops:iin)
- **Projektin tehtävien nimet:**

    - Projektisopimukset PSA:sta Fin:iin ja Ops:iin
    - Projektit PSA:sta Fin:iin ja Ops:iin
    - Projektisopimuksen rivit PSA:sta Fin:iin ja Ops:iin
    - Projektisopimuksen rivien välitavoitteet PSA:sta Fin:iin ja Ops:iin
  
### <a name="integrating-with-dynamics-365-project-service-automation-v3x"></a>Integrointi Dynamics 365 Project Service Automationin versioon v3.x
Project Service Automationissa on rakennemuutos, joka vaikuttaa projektisopimuksen rivien välitavoitemalliin, ja mallin v2-version käyttöä tarvitaan Project Service Automationin version v3.x integroimiseksi Dynamics 365:een.

- **Tietojen integroinnin mallin nimi:** Projektit ja sopimukset (PSA 3.x:stä Fin:iin ja Ops:iin) – v2
- **Projektin tehtävien nimet:**

    - Projektisopimukset PSA:sta Fin:iin ja Ops:iin
    - Projektit PSA:sta Fin:iin ja Ops:iin
    - Projektisopimuksen rivit PSA:sta Fin:iin ja Ops:iin
    - Projektisopimuksen rivien välitavoitteet PSA:sta Fin:iin ja Ops:iin

Tilit on synkronoitava, ennen kuin projektisopimuksia ja projekteja voi esiintyä.

## <a name="entity-set"></a>Entiteettijoukko

| Project Service Automation       | Rahoitus                                                |
|----------------------------------|--------------------------------------------------------|
| Tilaukset                           | Projektisopimuksen integroinnin entiteetti                |
| Projektit                         | Projektin integroinnin entiteetti                         |
| Tilausrivit                      | Projektisopimuksen rivin integroinnin entiteetti           |
| Projektisopimusrivien välitavoitteet | Projektisopimuksen rivien välitavoitteiden integroinnin entiteetti |

## <a name="entity-flow"></a>Entiteettivuo

Projektisopimuksia hallitaan Project Service Automationissa, ja ne synkronoidaan Financeen projektisopimuksina. Voit määrittää projektisopimuksen integroinnin lähteen Financessa osana integrointimallia.

Aika- ja materiaaliprojekteja ja kiinteähintaisia projekteja hallitaan Project Service Automationissa, ja ne synkronoidaan Financeen projekteina. Voit määrittää projektin integroinnin lähteen Financessa osana integrointimallia.

Projektisopimuksen rivejä hallitaan Project Service Automationissa, ja ne synkronoidaan Financeen sopimuksen laskutussääntöinä. Jos laskutustapa poikkeaa oletusarvoisesta projektityypistä, synkronointi päivittää sopimusrivi projektin ja projektiryhmän projektityypin.

Projektisopimuksen rivejä hallitaan Project Service Automationissa, ja ne synkronoidaan Financeen sopimuksen laskutussääntöjen välitavoitteina.

## <a name="project-service-automation-to-finance-integration-solution"></a>Project Service Automationista Financeen integroinnin ratkaisu

**Projektisopimuksen tunnus** -kenttä on käytettävissä **Projektisopimukset**-sivulla. Tämä kenttä on tehty luonnolliseksi ja yksilölliseksi avaimeksi integroinnin tukemiseksi.

Kun uusi projektisopimus luodaan eikä **Projektisopimuksen tunnus** -arvoa vielä ole olemassa, se luodaan automaattisesti numerosarjan avulla. Arvo alkaa kirjaimilla **ORD**, joiden perässä on kasvava numerosarja ja sitten kuuden merkin jälkiliite. Esimerkki: **ORD-01022-Z4M9Q0**.

**Projektinumero**-kenttä on käytettävissä **Projektit**-sivulla. Tämä kenttä on tehty luonnolliseksi ja yksilölliseksi avaimeksi integroinnin tukemiseksi.

Kun uusi projekti luodaan eikä **Projektinumero** -arvoa vielä ole olemassa, se luodaan automaattisesti numerosarjan avulla. Arvo alkaa kirjaimilla **PRJ**, joiden perässä on kasvava numerosarja ja sitten kuuden merkin jälkiliite. Esimerkki: **PRJ-01049-CCNID0**.

Kun käytetään Project Service Automationin Finenceen integroinnin ratkaisua, päivityskomentosarja määrittää **Projektisopimuksen tunnus** -kentän olemassa oleville projektisopimuksille sekä **Projektinumero**-kentän Project Service Automationissa oleville projekteille.

## <a name="prerequisites-and-mapping-setup"></a>Edellytykset ja yhdistämismääritykset

- Tilit on synkronoitava, ennen kuin projektisopimuksia ja projekteja voi esiintyä.
- Lisää yhteysjoukkoosi integrointiavaimen kenttämääritys kohteelle **msdyn\_organizationalunits** to **msdyn\_name \[Nimi\]**. Sinun täytyy ehkä ensin lisätä projekti yhteysjoukkoon. Lisätietoja [Tietojen integrointi Common Data Serviceen sovelluksille](https://docs.microsoft.com/powerapps/administrator/data-integrator).
- Lisää yhteysjoukkoosi integrointiavaimen kenttämääritys kohteelle **msdyn\_projects** to **msdynce\_projectnumber \[Projektinumero\]**. Sinun täytyy ehkä ensin lisätä projekti yhteysjoukkoon. Lisätietoja [Tietojen integrointi Common Data Serviceen sovelluksille](https://docs.microsoft.com/powerapps/administrator/data-integrator).
- **SourceDataID**, jotta projektisopimukset ja projektit voidaan päivittää eri arvoon tai poistaa yhdistämismäärityksestä. Mallin oletusarvo on **Project Service Automation**.
- **PaymentTerms**-yhdistämismääritys on päivitettävä vastaamaan kelvollisia maksuehtoja Financessa. Voit myös poistaa yhdistämismäärityksen projektitehtävästä. Oletusarvon yhdistämismäärityksissä on esittelytietojen oletusarvoja. Seuraavassa taulukossa esitetään arvot Project Service Automationissa.

    | Value | Kuvaus   |
    |-------|---------------|
    | 1     | Netto 30 pv        |
    | 2     | 10 pv 2 %, 30 pv netto |
    | 3     | Netto 45 pv        |
    | 4     | Netto 60 pv        |

## <a name="power-query"></a>Power Query

Sinun on käytettävä Microsoft Power Query for Excel -isäosaa suodattamaan tietoja, jos seuraavat ehdot täyttyvät:

- Sinulla on myyntitilauksia Dynamics 365 Salesissa.
- Sinulla on useita organisaatioyksiköitä Project Service Automationissa, ja nämä organisaatioyksiköt yhdistetään useisiin oikeushenkilöihin Financessa.

Jos sinun on käytettävä Power Queryä, noudata seuraavia ohjeita:

- Projektien ja sopimusten (PSA:sta Fin:iin ja Ops:iin) mallissa on oletussuodatin, joka sisältää vain tyypin **Työkohde (msdyn\_ordertype = 192350001)** myyntitilauksia. Tämän suodattimen avulla voidaan varmistaa, että myyntitilauksille ei luoda projektisopimuksia Financessa. Jos luot oman mallin, tämä suodatin on lisättävä.
- Sinun täytyy luoda Power Query -suodatin, joka sisältää vain ne sopimusorganisaatiot, jotka on synkronoitava integroinnin yhteysjoukon oikeushenkilöön. Esimerkiksi projektisopimukset, jotka sinulla on Contoso US:n sopimusorganisaatioyksikön kanssa, pitäisi synkronoida USSI-oikeushenkilöön, mutta projektisopimukset, jotka sinulla on Contoso Globalin sopimusorganisaatioyksikön kanssa, pitäisi synkronoida USMF-oikeushenkilöön. Jos et lisää tätä suodatinta tehtävien yhdistämismääritykseen, kaikki projektisopimukset synkronoidaan yhteysjoukolle määritettyyn oikeushenkilöön sopimusorganisaatioyksiköstä riippumatta.

## <a name="template-mapping-in-data-integration"></a>Mallien yhdistämismääritys tietojen integroinnissa

> [!NOTE] 
> Kentät **CustomerReference**, **AddressCity**, **AddressCountryRegionID**, **AddressDescription**, **AddressLine1**, **AddressLine2**, **AddressState** ja **AddressZipCode** eivät ole mukana projektisopimusten oletusarvoisessa yhdistämismäärityksessä. Voit lisätä yhdistämismääritykset, jos nämä tiedot on synkronoitava projektisopimuksissa.
>
> Kentät **Description**, **ParentID**, **ProjectGroup**, **ProjectManagerPersonnelNumber** ja **ProjectType** eivät ole mukana projektisopimusten oletusarvoisessa yhdistämismäärityksessä. Voit lisätä yhdistämismääritykset, jos nämä tiedot on synkronoitava projekteissa.

Seuraavissa kuvissa on esimerkkejä mallitehtävien yhdistämismäärityksestä tietojen integroinnissa. Yhdistämismäärityksessä näytetään kenttätiedot, jotka synkronoidaan Project Service Automationista Financeen.

[![Yhdistelmämääritysmalli](./media/ProjectContractTemplateMapping.JPG)](./media/ProjectContractTemplateMapping.JPG)

[![Yhdistelmämääritysmalli](./media/ProjectTemplateMapping.JPG)](./media/ProjectTemplateMapping.JPG)

[![Yhdistelmämääritysmalli](./media/ProjectContractLinesMapping.JPG)](./media/ProjectContractLinesMapping.JPG)

[![Yhdistelmämääritysmalli](./media/ProjectContractLineMilestonesMapping.JPG)](./media/ProjectContractLineMilestonesMapping.JPG)

#### <a name="project-contract-line-milestone-mapping-in-the-projects-and-contracts-psa-3x-to-dynamics---v2-template"></a>Projektisopimusten rivien välitavoitteiden yhdistämismääritys Projektit ja sopimukset -mallissa (PSA 3.x:stä Dynamicsiin) – v2-malli:

[![Yhdistelmämääritysmalli](./media/ProjectContractLineMilestoneMapping_v2.jpg)](./media/ProjectContractLineMilestoneMapping_v2.jpg)
