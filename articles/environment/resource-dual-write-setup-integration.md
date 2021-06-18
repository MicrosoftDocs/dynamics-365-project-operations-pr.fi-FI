---
title: Project Operationsin määritysten ja määritystietojen integrointi
description: Tässä aiheessa on tietoja Project Operationsin kaksoiskirjoituksen asettamisesta ja määrityksestä.
author: sigitac
ms.date: 4/23/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 1e9ca9407404274648f359be42d350137775ae55
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/10/2021
ms.locfileid: "6001062"
---
# <a name="project-operations-setup-and-configuration-data-integration"></a>Project Operationsin määritysten ja määritystietojen integrointi

_**Käytetään:** Project Operationsin resursseihin ja ei-varastoitaviin perustuvissa skenaarioissa_

Tässä aiheessa on tietoja Project Operationsin asetuksen ja määritysentiteettien integroinnista käyttämällä kaksoiskirjoitusta.

## <a name="project-contracts-contract-lines-and-projects"></a>Projektisopimukset, projektisopimusrivit ja projektit

Projektisopimukset, sopimusrivit ja projektit luodaan Dataversessä ja synkronoidaan Finance and Operations -sovelluksiin lisälaskentaa varten. Entiteettien tietueita voi luoda ja poistaa vain Dataversessä. Finance and Operations -sovellusten näihin tietueisiin voidaan kuitenkin lisätä kirjanpitomääritteitä, kuten arvonlisäveroryhmän oletusarvoja ja taloushallinnon dimensioita.

  ![Projektisopimuksen integrointikäsitteet](./media/1ProjectContract.jpg)

Myyntiaktiviteettien liidejä, mahdollisuuksia ja tarjouksia seurataanDataversessä eikä niitä synkronoida Finance and Operations -sovelluksille, koska tähän aktiviteettiin ei liity kirjanpitoa.

Dataversen projektisopimustoiminto luo Finance and Operations -sovelluksiin projektisopimustietueen **Projektisopimusotsikoiden (salesorders)** taulukkokartan avulla. Kun projektisopimus tallennetaan Dataversessä, ohjelma luo myös projektisopimusasiakasentiteettitietueen. Tämä tietue synkronoidaan Finance and Operations -sovelluksiin käyttämällä **Projektin rahoituslähde (msdyn\_projectcontractssplitbillingrules)** -taulukkokarttaa. Tämä kartta synkronoi myös projektisopimuksen asiakaslisäykset, päivitykset ja poistot. Projektisopimusasiakkaille jaetut laskutusprosentit hallitaan vain Dataversessä, eikä niitä synkronoida Finance and Operations -sovelluksiin.

Kun projektisopimus on luotu Dataversessä, projektin kirjanpitäjä voi päivittää tämän projektisopimuksen kirjanpitomääritteet Finance and Operations -sovelluksissa valitsemalla **Projektinhallinta- ja kirjanpito** > **Projektisopimukset** > **Määritä** > **Näytä oletuskirjanpito**. Kirjanpitäjä voi tarkastella projektisopimusmääritteitä, kuten pyydettyä toimituspäivää ja palvelusopimuksen summaa, valitsemalla projektisopimuksen tunnuksen Finance and Operations -sovelluksissa, jotka avaavat liittyvän projektisopimustietueen Dataversestä.

Projektientiteetti synkronoidaan Finance and Operations -sovelluksiin käyttämällä **Projektit V2 (msdyn\_projektit)** -taulukkokarttaa. Projektin kirjanpitäjä voi:

  - Tarkistaa Finance and Operations -sovellusten projektit valitsemalla **Projektinhallinta ja kirjanpito** > **Kaikki projektit**. 
  - Päivitä projektin kirjanpitomääritteet Finance and Operations -sovelluksissa valitsemalla **Projektinhallinta ja kirjanpito** > **Kaikki projektit** > **Määritä** > **Näytä oletuskirjanpito**.  
  - Voit tarkastella projektin toiminnallisia määritteitä, kuten arvioituja alkamis- ja päättymispäivämääritteitä, valitsemalla niiden Finance and Operations -sovellusten projektitunnuksen, jotka avaavat liittyvän projektitietueen Dataversessä.

Projekti liittyy projektisopimukseen **Projektisopimusrivi**-kohteen kautta.

Dataversen projektisopimusrivit luovat Finance and Operations -sovelluksiin projektisopimuslaskutussäännön **Projektisopimusrivien (salesorderdetails)** taulukkokartan avulla. Laskutustapa määrittää projektisopimuksen laskutussäännön tyypin Finance and Operations -sovelluksissa:

  - Projektisopimusriveillä, joilla on ajan ja materiaalin laskutustapa, luodaan ajan ja materiaalityypin laskutussääntö.
  - Kiinteähintaisten hintojen laskutustavan sopimusriveillä luodaan välitavoitteen laskutussääntö.

Projektin sopimusrivejä voi tarkistaa Finance and Operations -sovellusten projektinpitäjän valitsemalla **Projektinhallinta- ja kirjanpito** > **Projektisopimukset** > **Määritä** > **Näytä oletuskirjanpito** ja tarkistamalla **Sopimusrivit**-välilehden tiedot. Kirjanpitäjä voi myös määrittää tämän välilehden kiinteähintaisen laskutustavan sopimusriveille taloushallinnon oletusdimensiot.

## <a name="billing-milestones"></a>Laskutuksen välitavoitteet

Kiinteähintaista laskutustapaa käyttävät projektisopimusrivit laskutetaan laskutuksen välitavoitteiden kautta. Laskutuksen välitavoitteet synkronoidaan Finance and Operations -sovellusten projektien tilitapahtumiin käyttämällä **Project Operationsin integrointisopimusrivin välitavoitteet (msdyn\_contractlinescheduleofvalues)** -taulukkokarttaa.

  ![Laskutuksen välitavoitteiden integrointi](./media/2Milestones.jpg)

Kirjanpitäjä voi tarkastella tilitapahtumia ja oikaista näiden tapahtumien kirjanpitomääritteitä valitsemalla **Projektinhallinta ja kirjanpito** > **Projektisopimukset** > **Ylläpidä** > **Kirjanpitotapahtumat** tai **Projektinhallinta ja kirjanpito** > **Kaikki projektit** > **Ylläpidä** > **Kirjanpitotapahtumat**.

Kun luot laskutuksen välitavoitteen ensimmäiseksi projektisopimusriville, järjestelmä luo automaattisesti kiinteähintaista myyntituottoa arvioivaa projektia varten, joka liittyy tähän sopimusriviin. Kiinteähintaiset tuottoarvioprojektit voidaan tarkistaa siirtymällä kohtaan **Projektinhallinta ja kirjanpito** > **Kiinteähintaiset tuottoarvioprojektit**.

### <a name="project-tasks"></a>Projektitehtävät

Projektitehtävät synkronoidaan Finance and Operations -sovelluksiin **projektitehtävien (msdyn\_projektien)** taulukkokartan kautta vain viitteeksi. Luonti-, päivitys- ja poistotoimintoja ei tueta Finance and Operations -sovellusten avulla.

  ![Projektitehtävien integrointi](./media/3Tasks.jpg)

## <a name="project-resources"></a>Projektien resurssit

**Projektiresurssiroolit**-kohde synkronoidaan Finance and Operations -sovelluksiin käyttämällä **Kaikkien yritysten projektiresurssiroolit (bookableresourcecategories)** -taulukkokarttaa vain tiedoksi. Koska resurssiroolit Dataversessä eivät ole yrityskohtaisia, järjestelmä luo automaattisesti sovelluksiin vastaavat yrityskohtaiset resurssiroolitietueet Finance and Operations -sovelluksissa automaattisesti kaikille kaksoiskirjoitusintegroinnin vaikutusalueeseen sisällytetyille juridisille entiteeteille.

![Resurssiroolien integrointi](./media/5Resources.jpg)

Project Operationsin projektiresursseja ylläpidetään Dataversessä ja niitä ei synkronoida Finance and Operations -sovelluksiin.

### <a name="transaction-categories"></a>Tapahtumaluokat

Tapahtumaluokkia ylläpidetään Dataversessä ja synkronoidaan Finance and Operations -sovelluksiin käyttämällä **projektitapahtumien luokkien (msdyn\_transactioncategories)** taulukkokarttaa. Kun tapahtumaluokkatietue on synkronoitu, järjestelmä luo automaattisesti neljä jaettua luokkatietuetta. Jokainen tietue vastaa sovellusten tapahtumatyyppiä Finance and Operationsissa ja linkittää ne tapahtumaluokkatietueeseen.

![Tapahtumaluokkien integrointi](./media/4TransactionCategories.jpg)

Arvioitujen ja toteutuneiden luokkien käyttäminen edellyttää, että projektin kirjanpitäjä tai järjestelmänvalvoja luo vastaavat projektiluokat kaikkiin juridisiin entiteetteihin. Lisätietoja on ohjeaiheessa [Projektiluokkien määrittäminen](../project-accounting/configure-project-categories.md).
