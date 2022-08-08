---
title: Project Operationsin määritysten ja määritystietojen integrointi
description: Tässä artikkelissa on tietoja Project Operationsin kaksoiskirjoituksen asettamisesta ja määrityksestä.
author: sigitac
ms.date: 4/23/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: d03393de893c39ceb53c06a3031395f765a26f55
ms.sourcegitcommit: a798fed5c59e3fefa62cdfa42c852d529b33fd35
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/18/2022
ms.locfileid: "9029148"
---
# <a name="project-operations-setup-and-configuration-data-integration"></a>Project Operationsin määritysten ja määritystietojen integrointi

_**Käytetään:** Project Operationsin resursseihin ja ei-varastoitaviin perustuvissa skenaarioissa_

Tässä artikkelissa on tietoja Project Operationsin asetuksen ja määritysentiteettien integroinnista käyttämällä kaksoiskirjoitusta.

## <a name="project-contracts-contract-lines-and-projects"></a>Projektisopimukset, projektisopimusrivit ja projektit

Projektisopimukset, sopimusrivit ja projektit luodaan Dataversessa ja synkronoidaan talous- ja toimintosovelluksiin lisälaskentaa varten. Entiteettien tietueita voi luoda ja poistaa vain Dataversessä. Näihin tietueisiin voidaan kuitenkin lisätä kirjanpitomääritteitä, kuten myyntiveroryhmän oletusarvoja ja taloushallinnon dimensioita, talous- ja toimintosovelluksissa.

  ![Projektisopimuksen integrointikäsitteet.](./media/1ProjectContract.jpg)

Myyntiaktiviteettien liidejä, mahdollisuuksia ja tarjouksia seurataan Dataversessa eikä niitä synkronoida talous- ja toimintosovelluksiin, koska tähän aktiviteettiin ei liity kirjanpitoa.

Projektisopimustoiminto Dataversessa luo projektisopimustietueen talous- ja toimintosovelluksissa **Projektisopimusotsikot (salesorders)** -taulukkokartan avulla. Kun projektisopimus tallennetaan Dataversessä, ohjelma luo myös projektisopimusasiakasentiteettitietueen. Tämä tietue synkronoidaan talous- ja toimintosovelluksiin käyttämällä **Projektin rahoituslähde (msdyn\_projectcontractssplitbillingrules)** -taulukkokarttaa. Tämä kartta synkronoi myös projektisopimuksen asiakaslisäykset, päivitykset ja poistot. Projektisopimusasiakkaiden väliset jaetut laskutusprosentit hallitaan vain Dataversessa, eikä niitä synkronoida talous- ja toimintosovelluksiin.

Kun projektisopimus on luotu Dataversessa, projektin kirjanpitäjä voi päivittää tämän projektisopimuksen kirjanpitomääritteet talous- ja toimintosovelluksissa kohdassa **Projektinhallinta ja kirjanpito** > **Projektisopimukset** > **Määritys** > **Näytä oletuskirjanpito**. Kirjanpitäjä voi tarkastella operatiivisia projektisopimusmääritteitä, kuten pyydettyä toimituspäivää ja sopimussummaa, valitsemalla projektisopimuksen tunnuksen talous- ja toimintosovelluksissa, jotka avaavat liittyvän projektisopimustietueen Dataversessa.

Projektientiteetti synkronoidaan talous- ja toimintosovelluksiin käyttämällä **Projektit V2 (msdyn\_projects)** -taulukkokarttaa. Projektin kirjanpitäjä voi:

  - Voit tarkastella talous- ja toimintosovellusten projekteja kohdassa **Projektinhallinta ja kirjanpito** > **Kaikki projektit**. 
  - Päivitä projektin kirjanpitomääritteet talous- ja toimintosovelluksissa valitsemalla **Projektinhallinta ja kirjanpito** > **Kaikki projektit** > **Määritys** > **Näytä oletuskirjanpito**.  
  - Voit tarkastella projektin toiminnallisia määritteitä, kuten arvioituja alkamis- ja päättymispäivämääriä, valitsemalla projektin tunnuksen talous- ja toimintosovelluksissa, jotka avaavat liittyvän projektitietueen Dataversessa.

Projekti liittyy projektisopimukseen **Projektisopimusrivi**-kohteen kautta.

Projektisopimusrivit Dataversessa luovat projektisopimuksen laskutussäännön talous- ja toimintosovelluksissa **Projektisopimusrivit (salesorderdetails)** -taulukkokartan avulla. Laskutustapa määrittää projektisopimuksen laskutussäännön tyypin talous- ja toimintosovelluksissa:

  - Projektisopimusriveillä, joilla on ajan ja materiaalin laskutustapa, luodaan ajan ja materiaalityypin laskutussääntö.
  - Kiinteähintaisten hintojen laskutustavan sopimusriveillä luodaan välitavoitteen laskutussääntö.

Projektin sopimusrivejä voi tarkastella projektin kirjanpitäjä talous- ja toimintosovelluksissa kohdassa **Projektinhallinta ja kirjanpito** > **Projektisopimukset** > **Määritys** > **Näytä oletuskirjanpito** ja tarkistamalla tiedot **Sopimusrivit**-välilehdessä. Kirjanpitäjä voi myös määrittää taloushallinnon oletusdimensiot kiinteän hinnan laskutustavan sopimusriveille tässä välilehdessä.

## <a name="billing-milestones"></a>Laskutuksen välitavoitteet

Kiinteähintaista laskutustapaa käyttävät projektisopimusrivit laskutetaan laskutuksen välitavoitteiden kautta. Laskutuksen välitavoitteet synkronoidaan projektin ennakkotapahtumiin talous- ja toimintosovelluksissa käyttämällä **Project Operations -integraation sopimusrivin välitavoitteet (msdyn\_contractlinescheduleofvalues)** -taulukkokarttaa.

  ![Laskutuksen välitavoitteiden integrointi.](./media/2Milestones.jpg)

Kirjanpitäjä voi tarkastella tilitapahtumia ja oikaista näiden tapahtumien kirjanpitomääritteitä valitsemalla **Projektinhallinta ja kirjanpito** > **Projektisopimukset** > **Ylläpidä** > **Kirjanpitotapahtumat** tai **Projektinhallinta ja kirjanpito** > **Kaikki projektit** > **Ylläpidä** > **Kirjanpitotapahtumat**.

Kun luot laskutuksen välitavoitteen ensimmäiseksi projektisopimusriville, järjestelmä luo automaattisesti kiinteähintaista myyntituottoa arvioivaa projektia varten, joka liittyy tähän sopimusriviin. Kiinteähintaiset tuottoarvioprojektit voidaan tarkistaa siirtymällä kohtaan **Projektinhallinta ja kirjanpito** > **Kiinteähintaiset tuottoarvioprojektit**.

### <a name="project-tasks"></a>Projektitehtävät

Projektitehtävät synkronoidaan talous- ja toimintosovelluksiin **Projektitehtävät (msdyn\_projecttasks)** -taulukkokartan kautta vain viitteeksi. Talous- ja toimintosovellukset eivät tue luomista, päivittämistä ja poistamista.

  ![Projektitehtävien integrointi.](./media/3Tasks.jpg)

## <a name="project-resources"></a>Projektien resurssit

**Projektiresurssiroolit**-entiteetti synkronoidaan talous- ja toimintosovelluksiin käyttämällä **Kaikkien yritysten projektiresurssiroolit (bookableresourcecategories)** -taulukkokarttaa vain viitteenä. Koska resurssiroolit Dataversessa eivät ole yrityskohtaisia, järjestelmä luo automaattisesti vastaavat yrityskohtaiset resurssiroolitietueet talous- ja toimintosovelluksissa automaattisesti kaikille kaksoiskirjoituksen integroinnin vaikutusalueeseen sisällytetyille yrityksille.

![Resurssiroolien integrointi.](./media/5Resources.jpg)

Project Operationsin projektiresursseja ylläpidetään Dataversessa ja niitä ei synkronoida talous- ja toimintosovelluksiin.

### <a name="transaction-categories"></a>Tapahtumaluokat

Tapahtumaluokkia ylläpidetään Dataversessa ja synkronoidaan talous- ja toimintosovelluksiin käyttämällä **Projektitapahtumien luokat (msdyn\_transactioncategories)** -taulukkokarttaa. Kun tapahtumaluokkatietue on synkronoitu, järjestelmä luo automaattisesti neljä jaettua luokkatietuetta. Kukin tietue vastaa talous- ja toimintosovellusten tapahtumatyyppiä ja linkittää ne tapahtumaluokkatietueeseen.

![Tapahtumaluokkien integrointi.](./media/4TransactionCategories.jpg)

Arvioitujen ja toteutuneiden luokkien käyttäminen edellyttää, että projektin kirjanpitäjä tai järjestelmänvalvoja luo vastaavat projektiluokat kaikkiin juridisiin entiteetteihin. Lisätietoja on ohjeaiheessa [Projektiluokkien määrittäminen](../project-accounting/configure-project-categories.md).
