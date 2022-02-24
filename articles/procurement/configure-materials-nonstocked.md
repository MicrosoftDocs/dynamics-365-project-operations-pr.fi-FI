---
title: Ei-varastoivien materiaalien ja odottavien toimittajan laskujen määrittäminen
description: Tässä aihe, miten varastoimattomia materiaaleja ja odottavia toimittajan laskuja voi ottaa käyttöön.
author: sigitac
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 24418f3aad8356bd209eef7487a47a3870bce10f
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/10/2021
ms.locfileid: "5993907"
---
# <a name="configure-non-stocked-materials-and-pending-vendor-invoices"></a>Ei-varastoivien materiaalien ja odottavien toimittajan laskujen määrittäminen

_**Käytetään:** Project Operationsin resursseihin ja ei-varastoitaviin perustuvissa skenaarioissa_

## <a name="minimum-version-requirement"></a>Version vähimmäisvaatimus

Ei-varastoivien materiaalien ja odottavien toimittajien laskujen käyttäminen Dynamics 365 Project Operations ei-varastoituissa/resurssipohjaissa skenaarioissa edellyttää seuraavia versioita:

Dynamics 365 Dataverse -ratkaisut:

- Project Operations – 4.9.0.221 tai uudempi
- Kaksoiskirjoitussovelluksen orkestrointiratkaisu – 2.2.2.23 tai uudempi

Dynamics 365 Finance:
- 10.0.18 (10.0.793.52) tai uudempi. Varmista, että rahoitusympäristösi on ajan tasalla ja että kaikki laatupäivitykset vastaavat vähimmäisversiovaatimuksia.

## <a name="run-dual-write-maps-for-non-stocked-materials-and-vendor-invoice-integration"></a>Suorita kaksoiskirjoituskarttoja ei-varastoiduille materiaaleille ja toimittajalaskujen integroinnille

Tässä osassa on tietoja ei-varastoituitujen materiaalien ja toimittajalaskujen edellyttämistä kartoista. Tarkista, että [Valmistele uusi ympäristö](../environment/resource-provision-new-environment.md#run-project-operations-dual-write-maps) -aiheessa luetellut tarvittavat kartat ovat käytössä ympäristössä.

1. Siirry Lifecycle Services (LCS) -sivulle, siirry LCS-projektiin ja siirry **Ympäristön tiedot** -sivulle.
2. Valitse **Common Data Service -ympäristön tiedot** -osassa **Linkitä CDS for Appsiin**. Kun olet valinnut linkin, sinut ohjataan yhdistämismääritysten entiteettiluetteloon.
3. Varmista, että seuraavat kartat ovat käytössä. Jos ne eivät ole käynnissä, käynnistä ne ja liitä mukaan kaikki liittyvät taulukkokartat.

    - CDS julkaisi erillisiä tuotteita (tuotteita)
    - Toimittajat v2 (msdyn_vendors)
    - Project Operationsin materiaaliarvioiden taulukko (msdyn_estimatelines)
    - Project Operationsin integrointiprojektin toimittajalaskun vientientiteetti (msdyn_projectvendorinvoices)
    - Project Operationsin integrointiprojektin toimittajalaskurivin vientientiteetti (msdyn_projectvendorinvoicelines)
    - Project Operations -integroinnin todelliset arvot (msdyn_actuals). Varmista, että käytössä oleva versio on 1.0.0.14 tai uudempi. Kartan aktiivinen versio näkyy **Kaksoiskirjoitus**-sivun **Versio**-sarakkeessa. Voit aktivoida kartan uuden version valitsemalla **taulukkokartan version** ja tallentamalla valitun version.

Jos käytät vakiomuotoista esittelytietoa, sinun täytyy ehkä pysäyttää ja käynnistää uudelleen myös seuraavat entiteettikartat ensimmäisen synkronoinnin yhteydessä:
  - Maksupäivät CDS V2 (msdyn_paymentdays)
  - Maksuaikataulu (msdyn_paymentschedules)
  - Maksuehdot (msdyn_paymentterms)
  - Toimittajaryhmät (msdyn_vendorgroups)
  - Yksiköt (uom)

> [!NOTE]
> Toimittajaryhmien ja yksiköiden ensimmäinen synkronointi voi epäonnistua muutamista aiemmin luodun demostietojoukon tietueista johtuen. Voit ohittaa epäonnistuneet toiminnot, koska ne eivät estä demotietojen käyttöä Project Operationsissa.

## <a name="configure-prerequisites-in-dataverse"></a>Edellytysten määrittäminen Dataversessä

### <a name="activate-workflow-to-create-accounts-based-on-vendor-entity"></a>Työnkulun aktivoiminen toimittajaentiteettiin perustuvien tilien luontia varten

Kaksoiskirjoitusorkestrointiratkaisu mahdollistaa [toimittajien pääintegroinnin](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/vendor-mapping.md). Tämän ominaisuuden edellytyksenä on, että toimittajan tiedot luodaan **Asiakkaat**-entiteetissä. Aktivoi mallin työnkulkuprosessi ja luo toimittajat **Asiakkaat**-taulukossa kohdassa [Toimittajan mallien vaihtaminen](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/vendor-switch.md#use-the-extended-vendor-design-for-vendors-of-the-organization-type) kuvatulla tavalla.

### <a name="set-products-to-be-created-as-active"></a>Määritä luotavat tuotteet aktiivisiksi

Varastoimattomat materiaalien arvoksi on määritettävä Financessa **Julkaistut tuotteet**. Kaksoiskirjoitusorkestrointiratkaisu sisältää valmiin [Julkaistujen tuotteiden integraation Dataverseen -tuoteluettelon](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/product-mapping.md). Oletusarvon mukaan Financen tuotteet synkronoidaan Dataverseen luonnostilassa. Jos haluat synkronoida tuotteen aktiiviseen tilaan, jotta sitä voidaan käyttää suoraan materiaalin käyttöasiakirjoissa tai odottavassa toimittajan laskussa, siirry kohtaan **Järjestelmä** > **Hallinta** > **Järjestelmänvalvoja** > **Järjestelmäasetukset**- ja määritä **Myynti**-välilehdessä **Luo tuotteet aktiivisessa tilassa** -arvoksi **Kyllä**.

## <a name="configure-prerequisites-in-finance"></a>Edellytysten määrittäminen Financessa

### <a name="enable-the-feature-key-for-pending-vendor-invoices"></a>Ota ominaisuusavain käyttöön odottavia toimittajan laskuja varten

Suorita seuraavat vaiheet ottaaksesi toiminnallisuuden käyttöön lisätäksesi projektin tietoja odottaviin toimittajan laskuihin.

1. Siirry Financessa **Ominaisuuksien hallinta** -työtilaan.
2. Etsi ominaisuusluettelosta **Ota käyttöön odottavat toimittajan laskut Project Operations -kohdassa resurssipohjaisia tai ei-varastoituja skenaarioita varten** ja valitse **Ota käyttöön**.

### <a name="define-category-groups-and-project-categories-for-items"></a>Kohteiden luokkaryhmien ja projektiluokkien määrittäminen

Määritä **nimikkeen** tapahtumatyypille vähintään yksi luokkaryhmä ja vähintään yksi projektiluokka tämän ryhmän avulla. Lisätietoja on ohjeaiheessa [Projektiluokkien määrittäminen](../project-accounting/configure-project-categories.md#category-groups).

Tarkista projektin kustannus- ja tuottoprofiilit ja määritä nimiketapahtumien kirjausasetukset. Lisätietoja on ohjeaiheessa [Laskutettavien projektien kirjanpidon määrittäminen](../project-accounting/configure-accounting-billable-projects.md).

### <a name="set-up-a-write-in-product"></a>Määritä käsin lisätty tuote

Project Operationsissa voit kirjata materiaaliarvioita ja käyttöä luettelotuotteille, jotka on määritetty julkaistuun tuoteluetteloon ja tuotteisiin, jotka on lisätty käsin. Käsin lisättyjen tuotteiden käyttäminen edellyttää yhtä Financessa tätä varten määritettyä julkaistua tuotetta. Määritä käsin lisätty tuote seuraavien vaiheiden mukaisesti. Toista nämä vaiheet jokaisessa yrityksessä, joka käyttää Project Operationsia resurssi- tai ei-varastoiduissa skenaarioissa.

1. Siirry Financessa kohtaan **Tuotetietojen hallinta** > **Tuotteet** > **Julkaistut tuotteet**, ja valitse **Uusi**.
2. Valitse **Tuotetyyppi**-kentässä **Nimike** ja valitse sitten **Tuotteen alatyyppi** -kentässä **Tuote**.
3. Anna tuotenumero (WRITEIN) ja tuotteen nimi (käsin lisätty tuote).
4. Valitse nimikemalliryhmä. Varmista, että valitussa nimikemalliryhmässä **Varastokäytännön varastotuote**-kentän arvo on **Epätosi**.
5. Valitse arvot **Nimikeryhmästä**, **Tallennustilan dimensioryhmästä** ja **Seurantadimensioryhmä**-kentistä. Käytä vain **sivuston** **tallennustiladimensiota**, älä määritä seurantadimensioita.
6. Valitse arvot **Varastoyksikkö**-, **Ostoyksikkö** ja **Myyntiyksikkö**-kentässä ja tallenna muutokset.
7. Määritä **Suunnitelma**-välilehdessä oletustilausasetukset ja määritä sitten **Varasto**-välilehdessä oletussijainti ja varasto.
8. Siirry kohteeseen **Projektinhallinta ja kirjanpito** > **Määrittäminen** > **Projektinhallinta- ja kirjanpitoparametrit** sekä avaa **Project Operations Dynamics 365 Dataversessä**. 
9. Valitse **Materiaalit**-välilehden **Käsin lisätty tuote** -kentässä luomasi tuote.
10. Avaa Dataverse-ympäristön sivustokartassa **Tuotteet**-entiteetti ja etsi käsin lisätty tuotetietue. 
11. Avaa tietueen tiedot ja määritä tuotteen tilaksi **Vanhentunut**. Tämä tuotetila estää ketään vahingossa käyttämästä tätä tietuetta suoraan materiaaliarvioissa ja käyttöasiakirjoissa.

### <a name="set-up-a-procurement-integration-account"></a>Hankintojen integrointitilin luominen

Hankintojen integrointitiliä käytetään selvitystilinä kirjattaessa odottavaa toimittajan laskua, jonka rivit on määritetty projektiin.

Kun järjestelmä kirjaa odottavan toimittajan laskun, tiliä käytetään projektin kustannussummana. Toimittajan laskun tiedot käsitellään Dataversessä ja vastaava projektin todellinen arvo luodaan. Projektin toteutuneiden tietojen määrä lisätään Project Operationsin integrointi -kirjauskansioon. Kun julkaiset integrointipäiväkirjan, summa poistetaan hankintojen integrointitililtä ja kirjataan projektin kustannuksiin.

1. Määrittääksesi hankintojen integrointitilin, siirry kohteeseen **Projektinhallinta ja kirjanpito** > **Määrittäminen** > **Projektinhallinta- ja kirjanpitoparametrit** sekä avaa **Project Operations Dynamics 365 Dataversessä**. 
2. Valitse **Materiaalit**-välilehti ja valitse arvo **Hankintojen integrointitili** -kentässä.

#### <a name="set-up-project-category-defaults-for-an-item"></a>NImikkeen projektiluokkaoletusarvojen määrittäminen

1. Siirry Financessa kohteeseen **Projektinhallinta ja kirjanpito** > **Määrittäminen** > **Projektinhallinta- ja kirjanpitoparametrit** sekä avaa **Project Operations Dynamics 365 Dataversessä**. 
2. Valitse arvo **Projektiluokan oletusarvot**-välilehden **Nimike**-kentässä. Tätä projektiluokkaa käytetään materiaalitapahtumista, jos projektin luokkaa ei ole määritetty projektin toteutuneiden kustannusten tietueelle.
