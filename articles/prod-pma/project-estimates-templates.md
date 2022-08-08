---
title: Projektiarvioiden synkronointi suoraan Project Service Automationista talous- ja toimintosovelluksiin
description: Tässä artikkelissa käsitellään malleja ja taustatehtäviä, joilla projektin tunti- ja kuluarviot synkronoidaan suoraan Microsoft Microsoft Dynamics 365 Project Service Automationista Dynamics 365 Financeen.
author: Yowelle
ms.date: 07/20/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: johnmichalak
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.3.0
ms.openlocfilehash: 2a71a2a7ca0c9179ddd5667364d8b5c9e413b917
ms.sourcegitcommit: a798fed5c59e3fefa62cdfa42c852d529b33fd35
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/18/2022
ms.locfileid: "9029801"
---
# <a name="synchronize-project-estimates-directly-from-project-service-automation-to-finance-and-operations"></a>Projektiarvioiden synkronointi suoraan Project Service Automationista talous- ja toimintosovelluksiin

[!include[banner](../includes/banner.md)]

Tässä artikkelissa käsitellään malleja ja taustatehtäviä, joilla projektin tunti- ja kuluarviot synkronoidaan suoraan Microsoft Dynamics 365 Project Service Automationista Dynamics 365 Financeen.

> [!NOTE]
> - Projektitehtävien integrointi, kulutapahtumien luokat, työaika-arviot, kuluarviot ja toimintojen lukitus ovat käytettävissä versiossa 8.0.
> - Toteutuneiden arvojen integrointi on käytettävissä alkaen versiosta 8.0.1 tai myöhempi.

## <a name="data-flow-for-project-service-automation-to-finance"></a>Tietovuo Project Service Automationista Financeen

Project Service Automationin integrointiratkaisua Financeen käyttää tietojen integrointitoimintoa tietojen synkronointiin Project Service Automationin ja Financen eri esiintymien välillä. Tietojen integrointitoiminnossa käytettävissä olevat integrointimallit mahdollistavat projektien työaika-arvioiden ja projektien kuluarvioiden tietovuon Project Service Automationista Financeen.

Seuraavassa kuvassa on esitetty, miten tiedot synkronoidaan Project Service Automationin ja Financen välillä.

[![Tietovuo Project Service Automationin Financeen integroinnissa.](./media/ProjectEstimatesFlow.png)](./media/ProjectEstimatesFlow.png)

## <a name="project-hour-estimates"></a>Projektin työmäärä-arviot

### <a name="template-and-tasks"></a>Malli ja tehtävät

Jos haluat käyttää käytettävissä olevia malleja, valitse Microsoft Power Appsin hallintakeskuksessa **Projektit** ja sitten oikeassa yläkulmassa **Uusi projekti** valitaksesi julkisia malleja.

Seuraavaa mallia ja pohjana olevia tehtäviä käytetään projektien työaika-arvioiden synkronoimiseen Project Service Automationista Financeen:

- **Tietojen integroinnin mallin nimi:** Projektin työaika-arviot (PSA:sta Fin:iin ja Ops:iin)
- **Projektin tehtävien nimet:**

    - Tapahtumasuhteet
    - Kulujen arviot

### <a name="entity-set"></a>Entiteettijoukko

| Project Service Automation | Rahoitus                                       |
|----------------------------|-----------------------------------------------|
| Projektitehtävät              | Projektien työaika-arvioiden integrointientiteetti |

### <a name="entity-flow"></a>Entiteettivuo

Projektien työaika-arvioita hallitaan Project Service Automationissa, ja ne synkronoidaan Financeen työaikaennusteina.

### <a name="prerequisites"></a>Edellytykset

Ennen kuin projektien työaika-arvioita voidaan suorittaa, on synkronoitava projektit, projektitehtävät ja projektien kulutapahtumaluokat.

### <a name="power-query"></a>Power Query

Projektin tuntiarvioiden mallissa on käytettävä Microsoft Power Query for Exceliä seuraavien toimintojen päivittämiseen:

- Määritä sen oletusarvoisen ennustemallin tunnus, jota käytetään, kun integrointi luo uusia työaikaennusteita.
- Suodata kaikki ne tehtävän resurssikohtaiset tietueet, jotka aiheuttavat työaikaennusteisiin integroinnin epäonnistumisen.
- Suodata tyhjät tapahtumaluokkarivit pois. Jos tätä tehtävää ei suoriteta, saattaa esiintyä virheellisiä työaikaennusteita.

#### <a name="set-the-default-forecast-model-id"></a>Määritä oletusarvoisen ennustemallin tunnus

Päivitä oletusarvoisen ennustemallin tunnus mallissa avaamalla yhdistämismäärityksen valitsemalla **Yhdistämismääritys**-nuoli. Valitse sitten **Tarkka kysely ja suodatus** -linkki.

- Jos käytät oletusarvoisten projektien työaika-arvioiden (PSA:sta Fin:iin ja Ops:iin) mallia, valitse **Sovelletut vaiheet** -luettelossa **Lisätty ehto**. Korvaa **Toiminto**-kirjauksessa **O\_forecast** sen ennustemallin tunnuksella, jota käytetään integroinnissa. Oletusmallilla on esittelytiedoista peräisin oleva ennustemallin tunnus.
- Jos olet luomassa uutta mallia, tämä sarake on lisättävä. Valitse Power Queryssä **Lisää ehtosarake** ja anna uudelle sarakkeelle nimi, kuten **Mallin tunnus**. Kirjoita sarakkeen ehto, silloin jos projektitehtävä ei ole tyhjäarvo, sitten \<enter the forecast model ID\>; muuten tyhjäarvo.

#### <a name="filter-out-resource-specific-records"></a>Resurssikohtaisten tietueiden pois suodattaminen

Projektien työaikaennusteiden (PSA:sta Fin:iin ja Ops:iin) mallissa on oletussuodatin, joka poistaa kaikki resurssikohtaiset tietueet. Jos luot oman mallin, tämä suodatin on lisättävä. Valitse **Tarkka kysely ja suodatus** -linkki suodattaaksesi **msdyn\_islinetask**-saraketta siten, että vain tietueet, joiden arvo on **Epätosi** ovat mukana.

#### <a name="filter-out-empty-transaction-category-rows"></a>Tyhjien tapahtumaluokkarivien pois suodattaminen

Sinun on lisättävä suodatin poistaaksesi kaikki rivit, joilla on tyhjiä tapahtumaluokkia. Tämä tehtävä on pakollinen riippumatta siitä, käytätkö oletusmallia vai luotko oman mallin. Tämä suodatin poistaa Project Service Automationista kaikki yhteenvetorivit, jotka saattavat aiheuttaa virheitä Financen työaikaennusteissa. Valitse **Tarkka kysely ja suodatus**-linkki suodattaaksesi tyhjät tietueet sarakkeessa **msdyn\_transactioncategory\_value**.

### <a name="template-mapping-in-data-integration"></a>Mallien yhdistämismääritys tietojen integroinnissa

Seuraavassa kuvissa on esimerkki mallitehtävien yhdistämismäärityksissä tietojen integroinnissa. Yhdistämismäärityksessä näytetään kenttätiedot, jotka synkronoidaan Project Service Automationista Financeen.

[![Mallitehtävän yhdistämismääritys tietojen integroinnissa.](./media/ProjectHourEstimatesMapping.jpg)](./media/ProjectHourEstimatesMapping.jpg)

## <a name="project-expense-estimates"></a>Projektin kuluarviot

### <a name="template-and-tasks"></a>Malli ja tehtävät

Seuraavaa mallia ja pohjana olevia tehtäviä käytetään projektien kuluarvioiden synkronoimiseen Project Service Automationista Financeen:

- **Tietojen integroinnin mallin nimi:** Projektin kuluarviot (PSA:sta Fin:iin ja Ops:iin)
- **Projektin tehtävien nimet:**

    - Tapahtumasuhteet 
    - Kulujen arviot

### <a name="entity-set"></a>Entiteettijoukko

| Project Service Automation | Rahoitus                                                  |
|----------------------------|----------------------------------------------------------|
| Tapahtuman yhteydet    | Projektitapahtuman integrointikohdesuhteet |
| Arviorivit             | Projektien kuluarvioiden integrointientiteetti         |

### <a name="entity-flow"></a>Entiteettivuo

Projektien kuluarvioita hallitaan Project Service Automationissa, ja ne synkronoidaan Financeen kuluennusteina.

### <a name="prerequisites"></a>Edellytykset

Ennen kuin projektien kuluarvioita voidaan suorittaa, on synkronoitava projektit, projektitehtävät ja projektien kulutapahtumaluokat.

### <a name="power-query"></a>Power Query

Projektin kuluarviomallissa on käytettävä Power Queryfor Exceliä seuraavien toimintojen päivittämiseen:

- Suodatus siten, että mukana on vain kuluarviorivitietueita.
- Määritä sen oletusarvoisen ennustemallin tunnus, jota käytetään, kun integrointi luo uusia työaikaennusteita.
- Laskutustyyppien muuntaminen.
- Tapahtumatyyppien muuntaminen.

#### <a name="filter-to-include-only-expense-estimate-lines"></a>Suodatus siten, että mukana on vain kuluarviorivejä

Projektin kuluarvioiden (PSA:sta Fin:iin ja Ops:iin) -mallissa on oletussuodatin, jonka ansiosta integroinnissa on mukana vain kulurivejä. Jos luot oman mallin, tämä suodatin on lisättävä. Valitse **Tapahtumasuhteet**-tehtävä ja avaa siten yhdistämismääritys valitsemalla **Yhdistämismääritys**-nuoli. Valitse **Tarkka kysely ja suodatus** -linkki. Suodata **msdyn\_transactiontype1**-saraketta siten, että se sisältää vain **msdyn\_estimateline**-kohteita.

#### <a name="set-the-default-forecast-model-id"></a>Määritä oletusarvoisen ennustemallin tunnus

Päivitä oletusarvoisen ennustemallin tunnus mallissa valitsemalla **Kuluarviot**-tehtävä ja avaamalla sitten yhdistämismääritys valitsemalla **Yhdistämismääritys**-nuoli. Valitse **Tarkka kysely ja suodatus** -linkki.

- Jos käytät projektin kuluarvioiden oletusmallia (PSA:sta Fin and Opsiin), Power Queryssä, valitse ensimmäinen **Lisätty ehto** **Käytetyt vaiheet** -osassa. Korvaa **Toiminto**-kirjauksessa **O\_forecast** sen ennustemallin tunnuksella, jota käytetään integroinnissa. Oletusmallilla on esittelytiedoista peräisin oleva ennustemallin tunnus.
- Jos olet luomassa uutta mallia, tämä sarake on lisättävä. Valitse Power Queryssä **Lisää ehtosarake** ja anna uudelle sarakkeelle nimi, kuten **Mallin tunnus**. Kirjoita sarakkeen ehto, silloin jos arviorivitunnus ei ole tyhjäarvo, sitten \<enter the forecast model ID\>; muuten tyhjäarvo.

#### <a name="transform-the-billing-types"></a>Laskutustyyppien muuntaminen

Projektin kuluarviot (PSA:sta Fin:iin ja Ops:iin) -mallissa on ehdollinen sarake, jonka avulla voidaan muuntaa laskutustyyppejä, jotka vastaanotetaan Project Service Automationista integroinnin aikana. Jos luot oman mallin, tämä ehdollinen sarake on lisättävä. Valitse **Tarkka kysely ja suodatus** -linkki ja valitse sitten **Lisää ehdollinen sarake**. Syötä uudelle sarakkeelle nimi, kuten **Laskutustyyppi**. Syötä sitten seuraava ehto:

If **msdyn\_billingtype** = 192350000, then **NonChargeable**  
else if **msdyn\_billingtype** = 192350001, then **Chargeable**  
else if **msdyn\_billingtype** = 192350002, then **Complimentary**  
else **NotAvailable**

#### <a name="transform-the-transaction-types"></a>Tapahtumatyyppien muuntaminen

Projektin kuluarviot (PSA:sta Fin:iin ja Ops:iin) -mallissa on ehdollinen sarake, jonka avulla voidaan muuntaa tapahtumatyyppejä, jotka vastaanotetaan Project Service Automationista integroinnin aikana. Jos luot oman mallin, tämä ehdollinen sarake on lisättävä. Valitse **Tarkka kysely ja suodatus** -linkki ja valitse sitten **Lisää ehdollinen sarake**. Syötä uudelle sarakkeelle nimi, kuten **Tapahtumatyyppi**. Syötä sitten seuraava ehto:

If **msdyn\_transactiontypecode** = 192350000, then **Cost**  
else if **msdyn\_transactiontypecode** = 192350005, then **Sales**  
else **null**

### <a name="template-mapping-in-data-integration"></a>Mallien yhdistämismääritys tietojen integroinnissa

Seuraavissa kuvissa on esimerkkejä mallitehtävien yhdistämismäärityksestä tietojen integroinnissa. Yhdistämismäärityksessä näytetään kenttätiedot, jotka synkronoidaan Project Service Automationista Financeen.

[![Kuluarviotapahtumien mallin yhdistäminen.](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)

[![Kuluarvioiden mallin yhdistäminen.](./media/ExpenseEstimatesMapping.jpg)](./media/ExpenseEstimatesMapping.jpg)


[!INCLUDE[footer-include](../includes/footer-banner.md)]