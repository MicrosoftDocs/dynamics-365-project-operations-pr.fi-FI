---
title: Kulujen hallintaintegraatio
description: Tässä aiheessa on tietoja kuluraporttien integroinnista Project Operationsissa käyttämällä kaksoiskirjoitusta.
author: sigitac
ms.date: 04/28/2021
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 8c347f14f3a479eb4aec951cfe4094c5581bce32
ms.sourcegitcommit: 02f00960198cc78a5e96955a9e4390c2c6393bbf
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/28/2021
ms.locfileid: "5955741"
---
# <a name="expense-management-integration"></a>Kulujen hallintaintegraatio

_**Käytetään:** Project Operationsin resursseihin ja ei-varastoitaviin perustuvissa skenaarioissa_

Tässä aiheessa on tietoja kuluraporttien integroinnista Project Operationsissa [täysi kustannusten käyttöönotto](../expense/expense-overview.md) käyttämällä kaksoiskirjoitusta.

## <a name="expense-categories"></a>Kululuokat

Täydellisessä kulujen käyttöönotossa kululuokat luodaan ja ylläpidetään Finance and Operations -sovelluksissa. Jos haluat luoda uuden kululuokan, toimi seuraavasti:

1. Luo **tapahtuma**-luokka Microsoft Dataversessä. Kaksoiskirjoitusintegrointi synkronoi tämän tapahtumaluokan Finance and Operations -sovelluksiin. Lisätietoja on ohjeaiheessa [Projektiluokkien määrittäminen](/dynamics365/project-operations/project-accounting/configure-project-categories) ja [Projektitoimintojen määritysten ja määritystietojen integrointi](resource-dual-write-setup-integration.md). Tämän integroinnin tuloksena järjestelmä luo neljä jaettua luokkatietuetta Finance and Operations -sovelluksiin.
2. Siirry Financessa kohtaan **Kulujen hallinta** > **Määritys** > **Jaetut luokat** ja valitse jaettu luokka, jolla on **Kulu**-tapahtumaluokka. Määritä **Voi käyttää kuluissa** -parametrin arvoksi **Tosi** ja määritä käytettävä kulutyyppi.
3. Luo tämän jaetun luokkatietueen avulla uusi kululuokka menemällä kohtaan **Kulujen hallinta** > **Määritys** > **Kululuokat** ja valitsemalla **Uusi**. Kun tietue tallennetaan, kaksoiskirjoitus käyttää taulukkokarttaa **Project Operationsin integrointiprojektin kululuokkien vientientiteetti (msdyn\_expensecategories)** tämän tietueen synkronoimiseen Dataverseen.

  ![Kululuokkien integrointi](./media/DW6ExpenseCategories.png)

Finance and Operations -sovellusten kululuokat ovat yritys- tai oikeushenkilökohtaisia. Dataversessä on erilliset, vastaavat oikeushenkilökohtaiset tietueet. Kun projektipäällikkö arvioi kuluja, hän ei voi valita kululuokkia, jotka on luotu projektille, jonka omistaa eri yritys kuin se yritys, joka omistaa projektin, jota hän käyttää. 

## <a name="expense-reports"></a>Kuluraportit

Kuluraportit luodaan ja hyväksytään Finance and Operations -sovelluksissa. Lisätietoja on kohdassa [Kuluraporttien luominen ja käsitteleminen Dynamics 365 Project Operationsissa](/learn/modules/create-process-expense-reports/). Kun projektipäällikkö on hyväksynyt kuluraportin, se kirjataan pääkirjanpitoon. Project Operationsissa projektiin liittyvät kuluraporttirivit kirjataan käyttämällä erityisiä kirjaussääntöjä:

  - Projektiin liittyvää kustannusta (mukaan lukien ei-palautettavissa oleva vero) ei kirjata heti projektin kustannustilille pääkirjaan, vaan se kirjataan kulujen integrointitilille. Tämä asiakas on määritetty **Projektinhallinta ja kirjanpito** > **Määrittäminen** > **Projektinhallinta- ja kirjanpitoparametrit**, **Project Operations Dynamics 365 Customer engagementissa** -välilehdellä.
  - Kaksoiskirjoitus synkronoi Dataverseen käyttämällä **Project Operations -integrointiprojektin kulujen vientientiteetti (msdyn\_kulujen)** -taulukkokartan kanssa.
  - Verojen alareskontra, toimittajan alareskontra ja muut taloudelliset kirjaukset kirjataan kuluraporttien kirjausten yhteydessä soveltuvin osin.

  ![Matkalaskujen integrointi](./media/DW6ExpenseReports.png)

Kun tietue kirjoitetaan **Kulu**-kohteeseen Dataverse -järjestelmässä, järjestelmä käynnistää tietueen automaattisen hyväksyntäprosessin. Jos tarpeen, automaattisen hyväksyntäprosessin tilan voi tarkistaa Dataversessä kohdassa **Lisäasetukset** > **Järjestelmä** > **Järjestelmätyöt**. Kun hyväksyntä on valmis, kulutapahtumien luokkatietueet luodaan **Toteutuneet**-entiteettiin.

Tämän jälkeen kuluihin liittyvät toteutuneet tiedot käsitellään käyttämällä **Project Operationsin integrointien toteutuneet (msdyn\_actuals)** -kaksoiskirjoitustaulukkokarttaa. Lisätietoja on aiheissa [Projektin arviot ja todelliset kulut](resource-dual-write-estimates-actuals.md).

Jaksottainen prosessi, **Tuonti valmistelusta** luo kuluraporttiin liittyvät kirjausrivit Project Operationsin integrointi -kirjauskansioon. Siirtymätilin oletusarvona on kulujen integrointitili. Integrointikirjauksen julkaisu tyhjentää kulutapahtuman tilisaldon ja siirtää kulusumman projektin kustannustilille. Järjestelmä luo myös projektin alareskontratapahtumia laskutusta ja tuottojen kirjaamista varten.
