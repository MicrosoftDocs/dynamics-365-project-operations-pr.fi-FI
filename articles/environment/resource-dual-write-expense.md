---
title: Kulujen hallintaintegraatio
description: Tässä artikkelissa on tietoja kuluraporttien integroinnista Project Operationsissa käyttämällä kaksoiskirjoitusta.
author: sigitac
ms.date: 04/28/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: da37adcf63a10b9f245283d377e70fd08b3aa9c5
ms.sourcegitcommit: 385081ecc839d7d4a557eda2bb1578ca073f7e41
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/19/2022
ms.locfileid: "9527983"
---
# <a name="expense-management-integration"></a>Kulujen hallintaintegraatio

_**Käytetään:** Project Operationsin resursseihin ja ei-varastoitaviin perustuvissa skenaarioissa_

Tässä artikkelissa on tietoja kuluraporttien integroinnista Project Operationsin [täydessä kustannusten käyttöönotossa](../expense/expense-overview.md) käyttämällä kaksoiskirjoitusta.

## <a name="expense-categories"></a>Kululuokat

Täydellisessä kulujen käyttökokemuksessa kululuokat luodaan ja ylläpidetään talous- ja toimintosovelluksissa. Jos haluat luoda uuden kululuokan, toimi seuraavasti:

1. Luo **tapahtuma**-luokka Microsoft Dataversessä. Kaksoiskirjoitusintegrointi synkronoi tämän tapahtumaluokan talous- ja toimintosovelluksiin. Lisätietoja on ohjeaiheessa [Projektiluokkien määrittäminen](/dynamics365/project-operations/project-accounting/configure-project-categories) ja [Projektitoimintojen määritysten ja määritystietojen integrointi](resource-dual-write-setup-integration.md). Tämän integroinnin tuloksena järjestelmä luo neljä jaettua luokkatietuetta talous- ja toimintosovelluksissa.
2. Siirry Financessa kohtaan **Kulujen hallinta** > **Määritys** > **Jaetut luokat** ja valitse jaettu luokka, jolla on **Kulu**-tapahtumaluokka. Määritä **Voi käyttää kuluissa** -parametrin arvoksi **Tosi** ja määritä käytettävä kulutyyppi.
3. Luo tämän jaetun luokkatietueen avulla uusi kululuokka menemällä kohtaan **Kulujen hallinta** > **Määritys** > **Kululuokat** ja valitsemalla **Uusi**. Kun tietue tallennetaan, kaksoiskirjoitus käyttää taulukkokarttaa **Project Operationsin integrointiprojektin kululuokkien vientientiteetti (msdyn\_expensecategories)** tämän tietueen synkronoimiseen Dataverseen.

  ![Kululuokkien integrointi.](./media/DW6ExpenseCategories.png)

Talous- ja toimintosovellusten kululuokat ovat oikeushenkilö- tai yrityskohtaisia. Dataversessä on erilliset, vastaavat oikeushenkilökohtaiset tietueet. Kun projektipäällikkö arvioi kuluja, hän ei voi valita kululuokkia, jotka on luotu projektille, jonka omistaa eri yritys kuin se yritys, joka omistaa projektin, jota hän käyttää. 

## <a name="expense-reports"></a>Kuluraportit

Kuluraportit luodaan ja hyväksytään talous- ja toimintosovelluksissa. Lisätietoja on kohdassa [Kuluraporttien luominen ja käsitteleminen Dynamics 365 Project Operationsissa](/training/modules/create-process-expense-reports/). Kun projektipäällikkö on hyväksynyt kuluraportin, se kirjataan pääkirjanpitoon. Project Operationsissa projektiin liittyvät kuluraporttirivit kirjataan käyttämällä erityisiä kirjaussääntöjä:

  - Projektiin liittyvää kustannusta (mukaan lukien ei-palautettavissa oleva vero) ei kirjata heti projektin kustannustilille pääkirjaan, vaan se kirjataan kulujen integrointitilille. Tämä asiakas on määritetty **Projektinhallinta ja kirjanpito** > **Määrittäminen** > **Projektinhallinta- ja kirjanpitoparametrit**, **Project Operations Dynamics 365 Customer engagementissa** -välilehdellä.
  - Kaksoiskirjoitus synkronoi Dataverseen käyttämällä **Project Operations -integrointiprojektin kulujen vientientiteetti (msdyn\_kulujen)** -taulukkokartan kanssa.
  - Verojen alareskontra, toimittajan alareskontra ja muut taloudelliset kirjaukset kirjataan kuluraporttien kirjausten yhteydessä soveltuvin osin.

  ![Matkalaskujen integrointi.](./media/DW6ExpenseReports.png)

Kun tietue kirjoitetaan **Kulu**-kohteeseen Dataverse -järjestelmässä, järjestelmä käynnistää tietueen automaattisen hyväksyntäprosessin. Jos tarpeen, automaattisen hyväksyntäprosessin tilan voi tarkistaa Dataversessä kohdassa **Lisäasetukset** > **Järjestelmä** > **Järjestelmätyöt**. Kun hyväksyntä on valmis, kulutapahtumien luokkatietueet luodaan **Toteutuneet**-entiteettiin.

Tämän jälkeen kuluihin liittyvät toteutuneet tiedot käsitellään käyttämällä **Project Operationsin integrointien toteutuneet (msdyn\_actuals)** -kaksoiskirjoitustaulukkokarttaa. Lisätietoja on aiheissa [Projektin arviot ja todelliset kulut](resource-dual-write-estimates-actuals.md).

Jaksottainen prosessi, **Tuonti valmistelusta** luo kuluraporttiin liittyvät kirjausrivit Project Operationsin integrointi -kirjauskansioon. Siirtymätilin oletusarvona on kulujen integrointitili. Integrointikirjauksen julkaisu tyhjentää kulutapahtuman tilisaldon ja siirtää kulusumman projektin kustannustilille. Järjestelmä luo myös projektin alareskontratapahtumia laskutusta ja tuottojen kirjaamista varten.
