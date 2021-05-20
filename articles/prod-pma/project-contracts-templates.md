---
title: Synkronoi projektisopimukset ja projektit suoraan Project Service Automationista Financeen
description: Tässä aiheessa kuvataan malli ja sen pohjana olevat tehtävät, joita käytetään projektisopimusten ja projektien synkronoimiseen suoraan Microsoft Dynamics 365 Project Service Automationista Dynamics 365 Financeen.
author: Yowelle
manager: AnnBe
ms.date: 12/17/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2017-12-13
ms.dyn365.ops.version: AX 7.3.0
ms.openlocfilehash: 85722f61a672cc55cd2b511dc80ebfbe4807b957
ms.sourcegitcommit: 3d78338773929121d17ec3386f6cb67bfb2272cc
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/27/2021
ms.locfileid: "5950395"
---
# <a name="synchronize-project-contracts-and-projects-directly-from-project-service-automation-to-finance"></a>Synkronoi projektisopimukset ja projektit suoraan Project Service Automationista Financeen 

[!include[banner](../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

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
- **Mallin nimi tietojen integroinnissa:** Projektit ja sopimukset (Project Service Automationista Financeen)
- **Projektin tehtävien nimet:**

    - Projektisopimukset Project Service Automationista Financeen
    - Projektit Project Service Automationista Financeen
    - Projektisopimusrivit Project Service Automationista Financeen
    - Projektisopimusrivien välitavoitteet Project Service Automationista Financeen
  
### <a name="integrating-with-dynamics-365-project-service-automation-v3x"></a>Integrointi Dynamics 365 Project Service Automationin versioon v3.x
Project Service Automationissa on rakennemuutos, joka vaikuttaa projektisopimuksen rivien välitavoitemalliin, ja mallin v2-version käyttöä tarvitaan Project Service Automationin version v3.x integroimiseksi Dynamics 365:een.

- **Mallin nimi tietojen integroinnissa:** Projektit ja sopimukset (Project Service Automation 3.x -versiosta Financeen) - v2
- **Projektin tehtävien nimet:**

    - Projektisopimukset Project Service Automationista Financeen
    - Projektit Project Service Automationista Financeen
    - Projektisopimusrivit Project Service Automationista Financeen
    - Projektisopimusrivien välitavoitteet Project Service Automationista Financeen

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

Aika-, materiaali- ja kiinteähintaisia projekteja hallitaan Project Service Automationissa, ja ne synkronoidaan Financeen projekteina. Osana malli-integrointia voit määrittää projektin integrointilähteen Financessa. Tällä hetkellä tuetaan vain aika- ja materiaali- sekä kiinteähintaisia projekteja.


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
- Lisää yhteysjoukkoosi integrointiavaimen kenttämääritys kohteelle **msdyn\_organizationalunits** to **msdyn\_name \[Nimi\]**. Sinun täytyy ehkä ensin lisätä projekti yhteysjoukkoon. Lisätietoja [Tietojen integrointi Common Data Serviceen sovelluksille](/powerapps/administrator/data-integrator).
- Lisää yhteysjoukkoosi integrointiavaimen kenttämääritys kohteelle **msdyn\_projects** to **msdynce\_projectnumber \[Projektinumero\]**. Sinun täytyy ehkä ensin lisätä projekti yhteysjoukkoon. Lisätietoja [Tietojen integrointi Common Data Serviceen sovelluksille](/powerapps/administrator/data-integrator).
- **SourceDataID**, jotta projektisopimukset ja projektit voidaan päivittää eri arvoon tai poistaa yhdistämismäärityksestä. Mallin oletusarvo on **Project Service Automation**.
- **PaymentTerms**-yhdistämismääritys on päivitettävä vastaamaan kelvollisia maksuehtoja Financessa. Voit myös poistaa yhdistämismäärityksen projektitehtävästä. Oletusarvon yhdistämismäärityksissä on esittelytietojen oletusarvoja. Seuraavassa taulukossa esitetään arvot Project Service Automationissa.

    | Value | Kuvaus   |
    |-------|---------------|
    | 1     | Netto 30 pv        |
    | 2     | 10 pv 2 %, 30 pv netto |
    | 3     | Netto 45 pv        |
    | 4     | Netto 60 pv        |

## <a name="power-query"></a>Power Query

Microsoft Power Query for Excelin avulla voit suodattaa tietoja, jos seuraavat ehdot täyttyvät:

- Sinulla on myyntitilauksia Dynamics 365 Salesissa.
- Sinulla on useita organisaatioyksiköitä Project Service Automationissa, ja nämä organisaatioyksiköt yhdistetään useisiin oikeushenkilöihin Financessa.

Jos sinun on käytettävä Power Queryä, noudata seuraavia ohjeita:

- Projektien ja sopimusten (PSA:sta Fin:iin ja Ops:iin) mallissa on oletussuodatin, joka sisältää vain tyypin **Työkohde (msdyn\_ordertype = 192350001)** myyntitilauksia. Tämän suodattimen avulla voidaan varmistaa, että myyntitilauksille ei luoda projektisopimuksia Financessa. Jos luot oman mallin, tämä suodatin on lisättävä.
- Luo Power Query -suodatin, joka sisältää vain sopimusorganisaatiot, jotka synkronoidaan integroinnin yhteysjoukon yritykseen. Esimerkiksi projektisopimukset, joiden organisaatioyksikkö on Contoso US, on synkronoitava USSI-yritykseen, mutta projektisopimukset, jotka sinulla on Contoso Globalin sopimusorganisaatioyksikön kanssa, synkronoidaan USMF-yritykseen. Jos et lisää tätä suodatinta tehtävien yhdistämismääritykseen, kaikki projektisopimukset synkronoidaan yhteysjoukolle määritettyyn oikeushenkilöön sopimusorganisaatioyksiköstä riippumatta.

## <a name="template-mapping-in-data-integration"></a>Mallien yhdistämismääritys tietojen integroinnissa

> [!NOTE] 
> Kentät **CustomerReference**, **AddressCity**, **AddressCountryRegionID**, **AddressDescription**, **AddressLine1**, **AddressLine2**, **AddressState** ja **AddressZipCode** eivät ole mukana projektisopimusten oletusarvoisessa yhdistämismäärityksessä. Voit lisätä yhdistämismääritykset, jos nämä tiedot on synkronoitava projektisopimuksissa.
>
> Kentät **Description**, **ParentID**, **ProjectGroup**, **ProjectManagerPersonnelNumber** ja **ProjectType** eivät ole mukana projektisopimusten oletusarvoisessa yhdistämismäärityksessä. Voit lisätä yhdistämismääritykset, jos nämä tiedot on synkronoitava projekteissa.

Seuraavissa kuvissa on esimerkkejä mallitehtävien yhdistämismäärityksestä tietojen integroinnissa. Yhdistämismäärityksessä näytetään kenttätiedot, jotka synkronoidaan Project Service Automationista Financeen.

[![Palvelusopimusmallin yhdistäminen](./media/ProjectContractTemplateMapping.JPG)](./media/ProjectContractTemplateMapping.JPG)

[![Projektimallin yhdistäminen](./media/ProjectTemplateMapping.JPG)](./media/ProjectTemplateMapping.JPG)

[![Palvelusopimusrivimallien yhdistäminen](./media/ProjectContractLinesMapping.JPG)](./media/ProjectContractLinesMapping.JPG)

[![Palvelusopimusrivivälitavoitemallin yhdistäminen](./media/ProjectContractLineMilestonesMapping.JPG)](./media/ProjectContractLineMilestonesMapping.JPG)

#### <a name="project-contract-line-milestone-mapping-in-the-projects-and-contracts-psa-3x-to-dynamics---v2-template"></a>Projektisopimusten rivien välitavoitteiden yhdistämismääritys Projektit ja sopimukset -mallissa (PSA 3.x:stä Dynamicsiin) – v2-malli:

[![Palvelusopimusrivivälitavoitemallin yhdistäminen version kaksi mallilla](./media/ProjectContractLineMilestoneMapping_v2.jpg)](./media/ProjectContractLineMilestoneMapping_v2.jpg)


[!INCLUDE[footer-include](../includes/footer-banner.md)]