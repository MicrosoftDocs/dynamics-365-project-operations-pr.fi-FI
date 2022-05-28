---
title: Ominaisuuksien muutokset Project Service Automationista Project Operationsiin
description: Tässä aihe on yleiskatsaus ominaisuuksien muutoksista Project Service Automationista Dynamics 365 Project Operationsiin.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 02/03/2022
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.reviewer: johnmichalak
ms.openlocfilehash: 7e41b381d6da267f58174305f33fc229c66cd7b7
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/14/2022
ms.locfileid: "8595402"
---
# <a name="feature-changes-from-project-service-automation-to-project-operations"></a>Ominaisuuksien muutokset Project Service Automationista Project Operationsiin

Päivitys Dynamics 365 Project Service Automationista Dynamics 365 Project Operations Liteen toimitetaan kolmessa vaiheessa. Tässä aiheessa on tietoja tärkeimmistä muutoksista, jotka päivityksen valmistuessa ovat odotettavissa.

| Päivityksen toimitus | Vaihe 1 <br>(Tammikuu 2022) | Vaihe 2 <br>(Huhtikuun aalto 2022) | Vaihe 3  |
|------------------|------------------------|---------------------------|---------------------------|
| Ei riippuvuutta projektien työrakenteesta (WBS). | :heavy_check_mark: | :heavy_check_mark: | :heavy_check_mark: |
| WBS sisältyy Project Operationsin tällä hetkellä tuettuihin rajoihin. | &nbsp; | :heavy_check_mark: | :heavy_check_mark: |
| WBS Project Operationsin tällä hetkellä tuettujen rajojen ulkopuolella, mukaan lukien Project Desktop Client -tuki. | &nbsp; | &nbsp; | :heavy_check_mark: |

## <a name="project-management"></a>Projektinhallinta

Käyttökokemuksen merkittävimmät muutokset ovat projektisuunnittelun alue. Project Operations omaksuu uuden nykyaikaisen käyttökokemuksen työrakenteen hallintaan hyödyntämällä [Project for the Webin](https://support.microsoft.com/en-us/office/what-is-project-for-the-web-c19b2421-3c9d-4037-97c6-f66b6e1d2eb5) aikataulutusominaisuuksia.

## <a name="differences-in-the-scheduling-experience"></a>Aikataulutuskokemuksen erot

Seuraavassa taulukossa on yhteenveto Project Service Automationin ja Project Operationsin aikataulutuseroista.

|  Aikataulutus     |   Project Operations   |   PSA   |
|-----------------|------------------------|---------|
| Projektimallit – mahdollisuus määrittää ja ottaa käyttöön projektimalleja projektia luotaessa  |  &nbsp;    | :heavy_check_mark: |
| Projektin työrakenteen (WBS) integrointi pöytätietokoneen asiakasohjelman kanssa   |    &nbsp;  | :heavy_check_mark: |
| Rajoitukset – aloita aikaisintaan, lopeta viimeistään  | :heavy_check_mark: |   &nbsp;  |
| Välitavoitteet – tehtävät, joiden kesto on nolla   | :heavy_check_mark:  |  &nbsp;  |
| Resurssipohjaiset tehtävät noudattavat määritettyjen resurssien käytettävyyttä   | :heavy_check_mark: |  &nbsp;    |
| Aikavaiheistettu muokkaaminen – suunnitelmien muokkaaminen ja työstäminen päivittäin   |   &nbsp;  | :heavy_check_mark: |
| Automaattinen/manuaalinen aikataulutus – Aikatauluta tehtäviä automaattisesti tai manuaalisesti projektin aikataulutusmoduulin avulla |  &nbsp; | :heavy_check_mark:  |
| Suurten projektien muokkaaminen suoraan käyttöliittymässä: Muokattavissa olevia suunnitelmia ei ole rajoitettu  | 500 tehtävän rajoitus  | :heavy_check_mark:       |
| Valmistumisprosentti – merkitse tehtävän edistyminen   | :heavy_check_mark:  |  &nbsp;  |
| [Projektin aikataulutustilat](../project-management/scheduling-modes.md) – määritä projekti kiinteäksi yksiköiksi, kiinteäksi työmääräksi tai kiinteäksi kestoksi | :heavy_check_mark: | &nbsp; |
| Aikajana – Luo ja mukauta aikajananäkymää, jotta voit visualisoida aikataulun tietoja ja olla yhteydessä sidosryhmien kanssa. | :heavy_check_mark:  | &nbsp; |
| Työmäärään perustuvat tehtävät – aikataulutusmoduulin tuki tehtävän aikatauluttamiseksi työmäärän perusteella  | :heavy_check_mark:  | &nbsp; |
| **Tehtävän tiedot** -valintaikkuna – Tallenna tehtävän tiedot valintaikkunan avulla | :heavy_check_mark:  |  &nbsp;  |
| Vedä ja pudota – valitse useita tehtäviä ja muokkaa niiden sijaintia WBS:ssä | :heavy_check_mark: | &nbsp;  |
| Joustavat pysyvät näkymät – tehtävämääritteiden tarkempien näkymien määrittäminen   | :heavy_check_mark:  | &nbsp; |
| Lajittele ja suodata WBS:ää  | :heavy_check_mark:  | &nbsp; |
| Ei-vesiputousmalli -projektin toimituksen taulunäkymä  | :heavy_check_mark:   | &nbsp; |
| Aikajananäkymä – vuorovaikutteinen Gantt-kaavio, jonka avulla WBS:ää voidaan visualisoida ja muokata   | :heavy_check_mark:  | &nbsp; |
| Pikanäppäimet – pikanäppäinten käyttäminen yleisille toiminnoille, kuten sisennykseen tai lisäämiseen  | :heavy_check_mark:  |  &nbsp; |
| Monitasoinen kumoaminen – suorita entä jos -analyysi, jotta saat kokonaiskäsityksen muutosten vaikutuksista peruuttamalla koko toimintojoukon ja ottamalla se uudelleen käyttöön | :heavy_check_mark: | &nbsp; |
| Leikkaa/kopioi/liitä – Tee aikataulujen kehittämisessä yhteistyötä kopioimalla ja liittämällä aikataulutietoja sovellusten välillä  | :heavy_check_mark: | &nbsp; |
| Tehtävien tarkistusluettelot – Lisää enintään 20 tarkistusluettelokohdetta tehtävää kohti   | :heavy_check_mark: | &nbsp; |

## <a name="project-planning"></a>Projektin suunnittelu

Project Operationsin **Projekti**-sivulla on merkittäviä eroja Project Service Automationin **Projekti**-sivuun verrattuna.

Vaiheen 1 päivityksen yhteydessä **Projektit**-sivulta on poistettu seuraavat toiminnot:

  - **Avaa MS Projectissa**
  - **Luo malli**
  - **Poista projektin linkitys MS Projectista**

Project Operationsin **Projekti**-sivu sisältää seuraavat uudet välilehdet.

- **Materiaaliarviot**
- **Tehtävän laskutuksen asetukset**

**Tila**-välilehti on poistettu ja **Tila**-kenttä on nyt **Yhteenveto**-välilehdessä projektin aikataulutustilassa.

   ![Projekti-sivun päivitykset.](media/projectform.png)

**Aikataulu**-välilehti on nimetty uudelleen **Tehtävä**-välilehdeksi, ja siinä on uusi projektisuunnittelukokemus ja Project for the Web.

   ![Uusi Projektitehtävät-välilehti.](media/tasktab.png)

## <a name="scheduling-modes"></a>Aikataulutustilat

Project Operations on ottanut käyttöön uuden ominaisuuden, [aikataulutustilat](../project-management/scheduling-modes.md). Kaikkien aiemmin luotujen Project Service Automation -projektien oletuskestoksi tulee Project Operationsissa **Kiinteä kesto**. Uusien projektien oletusarvoa voidaan kuitenkin hallita valitsemalla **Asetukset** > **Parametrit** > **Parametri** > **Aikataulutustila**.

   ![Projektiparametrien asetukset aikataulutustilaa varten.](media/projectparameter.png)

## <a name="project-planning-limits"></a>Projektin suunnittelun rajat

Project Operationsin kaikki projektin aikataulutustoiminnot perustuvat Project for The Webiin. Project for the Web hallitsee työrakennetta seuraavan taulukon rajoitusten mukaisesti.

| **Field**                                          | **Raja**             |
|----------------------------------------------------|-----------------------|
| Projektin tehtävien enimmäismäärä                  | 500                   |
| Projektin keston enimmäismäärä               | 3650 päivää (10 vuotta)  |
| Projektin resurssien enimmäismäärä              | 300                   |
| Projektin linkkien enimmäismäärä (vain seuraaja) | 600                   |
| Projektin mukautettujen linkkien enimmäismäärä          | 10                    |
| Hierarkian enimmäistaso                            | 10 tasoa             |
| Linkkien enimmäismäärä (seuraaja + edeltäjä)            | 20                    |
| Lehtitehtävän enimmäiskesto                      | 1250 päivää             |
| Yhteenvetotehtävän enimmäiskesto                 | 3650 päivää (10 vuotta)  |
| Tehtävään kohdennettujen resurssien enimmäismäärä               | 20 resurssia          |
| Tehtävän tuettu päivämääräväli                    | 1.1.2000 - 31.12.2149 |
| Tarkistusluettelon kohdat                                    | 20                    |

## <a name="project-planning-extensibility-and-development"></a>Projektisuunnittelun laajennettavuus ja kehittäminen

Kun olet päivittänyt Project Operationsiin, sinun täytyy projektien aikataulutuksen ohjelmointirajapintojen avulla käyttää luonti-, päivitys- ja poistotoimintoja seuraaville entiteeteille:

|   Entiteetin nimi           |   Entiteetin looginen nimi       |
|-------------------------|-----------------------------|
| Project                 | msdyn_project               |
| Projektin tehtävä            | msdyn_projecttask           |
| Projektitehtävän riippuvuus | msdyn_projecttaskdependency |
| Resurssien delegointi     | msdyn_resourceassignment    |
| Projektin joukko          | msdyn_projectbucket         |
| Projektiryhmän jäsen     | msdyn_projectteam           |

Jos sinulla on mukautuksia, joihin liittyy näitä entiteettejä, katso toteutusohjeet: [Projektiaikataulun ohjelmointirajapintojen käyttö toimintojen suorittamiseen aikataulutusentiteettien kanssa](../project-management/schedule-api-preview.md).

## <a name="data-model-changes"></a>Tietomallin muutokset

Osana päivitysvaihetta 1 tietomalliin on tehty muutoksia. Nämä muutokset ovat pääasiassa kenttien muutoksia aiemmin luotuihin entiteetteihin. Vaiheessa 1 entiteetit, **msydn_project** ja **msdyn_projectteam** ovat mukautusten refaktorointeja. 

> [!IMPORTANT]
> Tähän osaan päivitetään lisäentiteettejä, kun tulevat päivitysvaiheet ovat valmiit.

Seuraavat kentät on korvattu uusilla kentillä.

|   Entity          |   Vanha looginen nimi   |   Uusi looginen nimi    |
|-------------------|----------------------|-----------------------|
| msdyn_project     | msdyn_actualhours    | msdyn_effortcompleted |
| msdyn_project     | msdyn_plannedhours   | msdyn_effort          |
| msdyn_project     | msdyn_remaininghours | msdyn_effortremaining |
| msdyn_project     | msdyn_scheduledend   | msdyn_finish          |
| msdyn_project     | msdyn_wbsduration    | msdyn_duration        |
| msdyn_projectteam | msdyn_assignedhours  | msdyn_effort          |
| msdyn_projectteam | msdyn_from           | msdyn_start           |
| msdyn_projectteam | msdyn_to             | msdyn_finish          |

Seuraavat kentät on lisätty.

|   Entity          |   Looginen nimi                               |   Description |
|-------------------|----------------------------------------------|---------------|
| msdyn_project     | msdyn_actualfeesales                         | Näyttää projektin toteutuneen palkkiomyynnin koonnin. Käytettäväksi vain Project Service Automationissa. |
| msdyn_project     | msdyn_actualmaterialcost                     | Näyttää projektin toteutuneiden materiaalikustannusten koonnin. Käytettäväksi vain Project Service Automationissa. |
| msdyn_project     | msdyn_actualmaterialsales                    | Näyttää projektin toteutuneiden materiaalimyynnin koonnin. Käytettäväksi vain Project Service Automationissa. |
| msdyn_project     | msdyn_businesscase                           |                |
| msdyn_project     | msdyn_contractlineproject                    | Tähän projektiin liittyvä sopimusrivi. |
| msdyn_project     | msdyn_copyprojectcorrelationid               | Tämä on sisäinen järjestelmäkenttä, jota käytetään korrelaatiotunnukseen liittyvässä **Kopioi projekti** -toiminnossa. Käytettäväksi vain Project Service Automationissa. |
| msdyn_project     | msdyn_copyprojectsessionid                   | Tämä on sisäinen järjestelmäkenttä, jota käytetään istuntotunnukseen liittyvässä **Kopioi projekti** -toiminnossa. Käytettäväksi vain Project Service Automationissa. |
| msdyn_project     | msdyn_globalrevisiontoken                    | xRM Global Revision Token -tunnuksen viimeisin synkronointi projektin aikataulutuspalvelusta. |
| msdyn_project     | msdyn_msprojectdocument                      | Projektiin kuuluva Microsoft Project -asiakirja. |
| msdyn_project     | msdyn_plannedmaterialcost                    | Projektin suunnitellun materiaalikustannuksen kooste. Käytettäväksi vain Project Service Automationissa. |
| msdyn_project     | msdyn_plannedmaterialsales                   | Projektin suunnitellun materiaalimyynnin kooste. Käytettäväksi vain Project Service Automationissa. |
| msdyn_project     | msdyn_program                                | Ohjelma, johon tämä projekti liittyy. |
| msdyn_project     | msdyn_quotelineproject                       | Tähän projektiin liittyvä tarjousrivi. |
| msdyn_project     | msdyn_replaylogheader                        | Uudelleentoiston lokien yläviite. |
| msdyn_project     | msdyn_schedulemode                           | Projektin kaikissa tehtävissä käytettävä oletusaikataulutila.  |
| msdyn_project     | msdyn_taskearlieststart                      | Projektin tehtävien aikaisin alkamispäivämäärä.  |
| msdyn_project     | msdyn_valuestatement                         |                |
| msdyn_projectteam | msdyn_copiedfromprojectteammember            | Projektiryhmän jäsen, josta tämä projektiryhmän jäsen kopioitiin. |
| msdyn_projectteam | msdyn_creategenericteammemberwithrequirement | Ilmaisee, luodaanko juuri luodun yleisen ryhmän jäsenen resurssitarve.  |
| msdyn_projectteam | msdyn_deletestatus                           | Seurattavan ryhmän jäsenen poistamisen tila, eli onko lähetetty poistamispyyntö projektin aikataulutuspalveluun ja onko se lähettänyt onnistuneesti vastauksen odotetun aikaikkunan sisällä. |
| msdyn_projectteam | msdyn_effortcompleted                        | Seuraa ryhmän jäsenen toimeksiantoihin käyttämää työmäärää. |
| msdyn_projectteam | msdyn_effortremaining                        | Seuraa ryhmän jäsenen toimeksiantojen vielä suoritettavaa työmäärää. |
| msdyn_projectteam | msdyn_markedfordeletiontimer                 | Odotusaika siitä, milloin ryhmän jäsen lähettää poistopyynnön projektin aikataulutuspalveluun, kunnes ryhmän jäsen todellisuudessa poistetaan Microsoft Dataversesta.|
| msdyn_projectteam | msdyn_markedfordeletiontimestamp             | Aikaleima, joka tallennetaan, kun ryhmän jäsenen poistamispyyntö lähetetään projektin aikataulutuspalveluun. |
| msdyn_projectteam | msdyn_copiedfromprojectteammember            | Näyttää projektiryhmän jäsenen, josta tämä projektiryhmän jäsen kopioitiin.  |

## <a name="project-templates"></a>Projektimallit

Project Operations ei tue projektimalleja. [Projektin kopioinnin ohjelmointirajapinnan](../project-management/dev-copy-project.md) avulla voit kuitenkin replikoida monet ydintoiminnot.

## <a name="desktop-add-in-support"></a>Desktop-apuohjelman tuki

Microsoft Project Desktop -apuohjelman tuki ei ole käytettävissä päivityksen kahdessa ensimmäisessä vaiheessa. Vaiheessa 3 asiakkaat, joiden projektit ovat suurempia kuin tällä hetkellä tuetut Project for the Web-rajoitukset, voivat käyttää Desktop-apuohjelmaa.

## <a name="editing-resource-assignment-contours"></a>Resurssien määrityksen jaksotuksen muokkaaminen

Resurssin määrityksen jaksotuksen muokkaus on mahdollista, kun päivityksen 2. vaihe on käytettävissä.

## <a name="billing-and-pricing"></a>Laskutus ja hinnoittelu

Project Operationsiin on lisätty seuraavat uudet ominaisuudet. Nämä ominaisuudet ovat luonnostaan lisääviä, eivätkä ne vaikuta Project Service Automation -tietomalliin.

- [Materiaalikäytön kirjaaminen projekteihin ja projektitehtäviin](../material/material-usage-log.md)
- [Alihankinnan hallinta](../pro/subcontracting/managing-subcontracts-overview.md)
- [Ennakkomaksut ja ennakkomaksuun perustuvat palvelusopimukset](../pro/sales/set-up-advances-retainer-based-contracts-sales.md)
- [Sopimuksen ei-ylitettävä tila ja vahvistus](../pro/proforma-invoicing/manage-nte-status-validations-sales.md)
- [Tehtäväpohjainen laskutus](../pro/sales/mapping-projects-tasks-quote-line-sales.md)

## <a name="deprecated-components"></a>Vanhentuneet osat

Seuraavissa taulukoissa on dokumentoitu kaikki vanhentuneet kentät, jotka on siirretään vanhentuneen komponentin ratkaisuun päivityksen jälkeen. Lisätietoja ja linkki ratkaisuun on kohdassa [Dynamics 365 Project Service Automation 3x:stä Project Operations 4x:ään – vanhentuneet osat](https://github.com/microsoft/Dynamics365-Project-Operations-PowerApps/tree/main/3x-4x-deprecated-solution).

### <a name="invoicedetail"></a>invoicedetail

| Kentät                                                    |
|-----------------------------------------------------------------------------------------------|
|invoicedetail.msdyn_contractline    |

### <a name="msdyn_actual"></a>msdyn_actual

| Kentät                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_actual.msdyn_salescontractline                                                          |

### <a name="msdyn_characteristicreqforteammember"></a>msdyn_characteristicreqforteammember

| Kentät                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_characteristicreqforteammember.msdyn_characteristic                                     |
| msdyn_characteristicreqforteammember.msdyn_characteristicreqforteammemberid                   |
| msdyn_characteristicreqforteammember.msdyn_characteristictype                                 |
| msdyn_characteristicreqforteammember.msdyn_name                                               |
| msdyn_characteristicreqforteammember.msdyn_ratingvalue                                        |
| msdyn_characteristicreqforteammember.msdyn_resourcerequirementid                              |

### <a name="msdyn_contractlineinvoiceschedule"></a>msdyn_contractlineinvoiceschedule

| Kentät                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_contractlineinvoiceschedule.msdyn_contractline                                          |
| msdyn_contractlinescheduleofvalue.msdyn_contractline                                          |
 
### <a name="msdyn_dataexport"></a>msdyn_dataexport

| Kentät                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_dataexport.msdyn_dataexportid                                                           |
| msdyn_dataexport.msdyn_datatoken                                                              |
| msdyn_dataexport.msdyn_entityname                                                             |
| msdyn_dataexport.msdyn_exportedrecordcount                                                    |
| msdyn_dataexport.msdyn_exportstatus                                                           |
| msdyn_dataexport.msdyn_linkedentitydata                                                       |
| msdyn_dataexport.msdyn_name                                                                   |
| msdyn_dataexport.msdyn_pagingdata                                                             |

### <a name="msdyn_fact"></a>msdyn_fact

| Kentät                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_fact.msdyn_salescontractline                                                            |

### <a name="msdyn_findworkevent"></a>msdyn_findworkevent

| Kentät                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_findworkevent.msdyn_bookableresource                                                    |
| msdyn_findworkevent.msdyn_findworkeventid                                                     |
| msdyn_findworkevent.msdyn_name                                                                |
| msdyn_findworkevent.msdyn_timestamp                                                           |
| msdyn_findworkevent.msdyn_type                                                                |
| msdyn_findworkevent.msdyn_value                                                               |
| msdyn_findworkevent.msdyn_work                                                                |

### <a name="msdyn_invoicelinetransaction"></a>msdyn_invoicelinetransaction

| Kentät                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_invoicelinetransaction.msdyn_invoiceline                                                |
| msdyn_invoicelinetransaction.msdyn_salescontractline                                          |

### <a name="msdyn_journalline"></a>msdyn_journalline

| Kentät                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_journalline.msdyn_salescontractline                                                     |

### <a name="msdyn_opportunitylineresourcecategory"></a>msdyn_opportunitylineresourcecategory

| Kentät                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_opportunitylineresourcecategory.msdyn_billingtype                                       |
| msdyn_opportunitylineresourcecategory.msdyn_description                                       |
| msdyn_opportunitylineresourcecategory.msdyn_opportunitylineresourcecategoryid                 |
| msdyn_opportunitylineresourcecategory.msdyn_opportunitylinetransactionclassification          |
| msdyn_opportunitylineresourcecategory.msdyn_resourcecategory                                  |

### <a name="msdyn_opportunitylinetransaction"></a>msdyn_opportunitylinetransaction

| Kentät                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_opportunitylinetransaction.msdyn_accountcustomer                                        |
| msdyn_opportunitylinetransaction.msdyn_accountingdate                                         |
| msdyn_opportunitylinetransaction.msdyn_accountvendor                                          |
| msdyn_opportunitylinetransaction.msdyn_amount                                                 |
| msdyn_opportunitylinetransaction.msdyn_amount_base                                            |
| msdyn_opportunitylinetransaction.msdyn_amountmethod                                           |
| msdyn_opportunitylinetransaction.msdyn_basisamount                                            |
| msdyn_opportunitylinetransaction.msdyn_basisamount_base                                       |
| msdyn_opportunitylinetransaction.msdyn_basisprice                                             |
| msdyn_opportunitylinetransaction.msdyn_basisprice_base                                        |
| msdyn_opportunitylinetransaction.msdyn_basisquantity                                          |
| msdyn_opportunitylinetransaction.msdyn_billingtype                                            |
| msdyn_opportunitylinetransaction.msdyn_bookableresource                                       |
| msdyn_opportunitylinetransaction.msdyn_contactcustomer                                        |
| msdyn_opportunitylinetransaction.msdyn_contactvendor                                          |
| msdyn_opportunitylinetransaction.msdyn_customertype                                           |
| msdyn_opportunitylinetransaction.msdyn_description                                            |
| msdyn_opportunitylinetransaction.msdyn_documentdate                                           |
| msdyn_opportunitylinetransaction.msdyn_enddatetime                                            |
| msdyn_opportunitylinetransaction.msdyn_exchangeratedate                                       |
| msdyn_opportunitylinetransaction.msdyn_opportunityline                                        |
| msdyn_opportunitylinetransaction.msdyn_opportunitylinetransactionid                           |
| msdyn_opportunitylinetransaction.msdyn_percent                                                |
| msdyn_opportunitylinetransaction.msdyn_price                                                  |
| msdyn_opportunitylinetransaction.msdyn_price_base                                             |
| msdyn_opportunitylinetransaction.msdyn_pricelist                                              |
| msdyn_opportunitylinetransaction.msdyn_product                                                |
| msdyn_opportunitylinetransaction.msdyn_project                                                |
| msdyn_opportunitylinetransaction.msdyn_quantity                                               |
| msdyn_opportunitylinetransaction.msdyn_resourcecategory                                       |
| msdyn_opportunitylinetransaction.msdyn_resourceorganizationalunitid                           |
| msdyn_opportunitylinetransaction.msdyn_startdatetime                                          |
| msdyn_opportunitylinetransaction.msdyn_task                                                   |
| msdyn_opportunitylinetransaction.msdyn_transactioncategory                                    |
| msdyn_opportunitylinetransaction.msdyn_transactionclassification                              |
| msdyn_opportunitylinetransaction.msdyn_transactiontypecode                                    |
| msdyn_opportunitylinetransaction.msdyn_unit                                                   |
| msdyn_opportunitylinetransaction.msdyn_unitschedule                                           |
| msdyn_opportunitylinetransaction.msdyn_vendortype                                             |

### <a name="msdyn_opportunitylinetransactioncategory"></a>msdyn_opportunitylinetransactioncategory

| Kentät                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_opportunitylinetransactioncategory.msdyn_billingtype                                    |
| msdyn_opportunitylinetransactioncategory.msdyn_description                                    |
| msdyn_opportunitylinetransactioncategory.msdyn_opportunitylinetransactioncategoryid           |
| msdyn_opportunitylinetransactioncategory.msdyn_opportunitylinetransactionclassification       |
| msdyn_opportunitylinetransactioncategory.msdyn_transactioncategory                            |

### <a name="msdyn_opportunitylinetransactionclassificatio"></a>msdyn_opportunitylinetransactionclassificatio

| Kentät                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_opportunitylinetransactionclassificatio.msdyn_billingtype                               |
| msdyn_opportunitylinetransactionclassificatio.msdyn_description                               |
| msdyn_opportunitylinetransactionclassificatio.msdyn_include                                   |
| msdyn_opportunitylinetransactionclassificatio.msdyn_opportunityline                           |
| msdyn_opportunitylinetransactionclassificatio.msdyn_opportunitylinetransactionclassificatioid |
| msdyn_opportunitylinetransactionclassificatio.msdyn_transactionclassification                 |

### <a name="msdyn_orderlineresourcecategory"></a>msdyn_orderlineresourcecategory

| Kentät                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_orderlineresourcecategory.msdyn_contractline                                            |

### <a name="msdyn_orderlinetransaction"></a>msdyn_orderlinetransaction

| Kentät                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_orderlinetransaction.msdyn_salescontractline                                            |
| msdyn_orderlinetransactioncategory.msdyn_contractline                                         |

### <a name="msdyn_orderlinetransactionclassification"></a>msdyn_orderlinetransactionclassification

| Kentät                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_orderlinetransactionclassification.msdyn_contractline                                   |

### <a name="msdyn_project"></a>msdyn_project

| Kentät                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_project.msdyn_actualdurationminutes                                                     |
| msdyn_project.msdyn_actualhours                                                               |
| msdyn_project.msdyn_istemplate                                                                |
| msdyn_project.msdyn_plannedhours                                                              |
| msdyn_project.msdyn_projecttemplate                                                           |
| msdyn_project.msdyn_remaininghours                                                            |
| msdyn_project.msdyn_scheduleddurationminutes                                                  |
| msdyn_project.msdyn_scheduledend                                                              |
| msdyn_project.msdyn_stagename                                                                 |
| msdyn_project.msdyn_wbsduration                                                               |


### <a name="msdyn_projecttask"></a>msdyn_projecttask

| Kentät                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_projecttask.msdyn_actualdurationminutes                                                 |
| msdyn_projecttask.msdyn_actualeffort                                                          |
| msdyn_projecttask.msdyn_aggregationdirection                                                  |
| msdyn_projecttask.msdyn_assignedresources                                                     |
| msdyn_projecttask.msdyn_assignedteammembers                                                   |
| msdyn_projecttask.msdyn_autoscheduling                                                        |
| msdyn_projecttask.msdyn_costestimatecontour                                                   |
| msdyn_projecttask.msdyn_effortcontour                                                         |
| msdyn_projecttask.msdyn_islinetask                                                            |
| msdyn_projecttask.msdyn_numberofresources                                                     |
| msdyn_projecttask.msdyn_remaininghours                                                        |
| msdyn_projecttask.msdyn_resourceutilization                                                   |
| msdyn_projecttask.msdyn_salesestimatecontour                                                  |
| msdyn_projecttask.msdyn_scheduledhours                                                        |
| msdyn_projecttask.msdyn_wbsid                                                                 |

### <a name="msdyn_projecttaskstatususer"></a>msdyn_projecttaskstatususer

| Kentät                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_projecttaskstatususer.msdyn_bookableresource                                            |
| msdyn_projecttaskstatususer.msdyn_description                                                 |
| msdyn_projecttaskstatususer.msdyn_expectedcompletiondate                                      |
| msdyn_projecttaskstatususer.msdyn_expectedhourstocomplete                                     |
| msdyn_projecttaskstatususer.msdyn_iscompleted                                                 |
| msdyn_projecttaskstatususer.msdyn_name                                                        |
| msdyn_projecttaskstatususer.msdyn_percentcomplete                                             |
| msdyn_projecttaskstatususer.msdyn_projecttaskid                                               |
| msdyn_projecttaskstatususer.msdyn_projecttaskstatusindicator                                  |
| msdyn_projecttaskstatususer.msdyn_projecttaskstatususerid                                     |

### <a name="msdyn_projectteam"></a>msdyn_projectteam

| Kentät                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_projectteam.msdyn_applicantcount                                                        |
| msdyn_projectteam.msdyn_applicantsavailable                                                   |
| msdyn_projectteam.msdyn_assignedhours                                                         |
| msdyn_projectteam.msdyn_description                                                           |
| msdyn_projectteam.msdyn_from                                                                  |
| msdyn_projectteam.msdyn_hoursrequested                                                        |
| msdyn_projectteam.msdyn_membershipstatus                                                      |
| msdyn_projectteam.msdyn_number                                                                |
| msdyn_projectteam.msdyn_to                                                                    |

### <a name="msdyn_projectteammembersignup"></a>msdyn_projectteammembersignup

| Kentät                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_projectteammembersignup.msdyn_bookableresource                                          |
| msdyn_projectteammembersignup.msdyn_membershipstatus                                          |
| msdyn_projectteammembersignup.msdyn_name                                                      |
| msdyn_projectteammembersignup.msdyn_projectteammembersignupid                                 |
| msdyn_projectteammembersignup.msdyn_teammembership                                            |

### <a name="msdyn_projecttransactioncategory"></a>msdyn_projecttransactioncategory

| Kentät                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_projecttransactioncategory.msdyn_billingtype                                            |
| msdyn_projecttransactioncategory.msdyn_name                                                   |
| msdyn_projecttransactioncategory.msdyn_project                                                |
| msdyn_projecttransactioncategory.msdyn_projecttransactioncategoryid                           |
| msdyn_projecttransactioncategory.msdyn_transactioncategory                                    |

### <a name="msdyn_quotelineinvoiceschedule"></a>msdyn_quotelineinvoiceschedule

| Kentät                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_quotelineinvoiceschedule.msdyn_quoteline                                                |
| msdyn_quotelineresourcecategory.msdyn_quoteline                                               |
| msdyn_quotelinescheduleofvalue.msdyn_quoteline                                                |
| msdyn_quotelinetransaction.msdyn_quoteline                                                    |
| msdyn_quotelinetransactioncategory.msdyn_quoteline                                            |
| msdyn_quotelinetransactionclassification.msdyn_quoteline                                      |

### <a name="msdyn_resourceassignment"></a>msdyn_resourceassignment

| Kentät                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_resourceassignment.msdyn_hours                                                          |
| msdyn_resourceassignment.msdyn_fromdate                                                       |
| msdyn_resourceassignment.msdyn_msprojectclientid                                              |
| msdyn_resourceassignment.msdyn_todate                                                         |
| msdyn_resourceassignmentdetail.msdyn_duration                                                 |
| msdyn_resourceassignmentdetail.msdyn_from                                                     |
| msdyn_resourceassignmentdetail.msdyn_name                                                     |
| msdyn_resourceassignmentdetail.msdyn_resourceassignmentdetailid                               |
| msdyn_resourceassignmentdetail.msdyn_resourceassignmentid                                     |

### <a name="salesorderdetail"></a>salesorderdetail

| Kentät                                                    |
|-----------------------------------------------------------------------------------------------|
| salesorderdetail.msdyn_quoteline                                                              |

