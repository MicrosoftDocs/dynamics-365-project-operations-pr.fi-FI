---
title: Toimittajalaskutuksen integrointi
description: Tässä aiheessa on tietoja toimittajalaskujen integroinnista Project Operationsissa.
author: sigitac
ms.date: 04/27/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 538a2694591f1d0d368ee0ffeed9bdf12cb47420c3d0571f75185fe433f23436
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/06/2021
ms.locfileid: "6986487"
---
# <a name="vendor-invoice-integration"></a>Toimittajalaskutuksen integrointi

_**Käytetään:** Project Operationsin resursseihin ja ei-varastoitaviin perustuvissa skenaarioissa_

Projektiin liittyvät alennukset Dynamics 365 Project Operationsissa voidaan kirjata valitsemalla **Ostoreskontralaskut** > **Laskut** > **Odottavat toimittajan laskut** ja käyttämällä odottavaa toimittajan laskuasiakirjaa. Lisätietoja on ohjeaiheessa [Ei-varastoivien materiaalien ostaminen odottavien toimittajan laskun avulla](../procurement/pending-vendor-invoices.md).

> [!IMPORTANT]
> Ennen kuin käytät tässä aiheessa kuvattuja toimintoja, tarkista ja ota käyttöön tarvittavat määritykset. Lisätietoja on ohjeaiheessa [Ei-varastoivien materiaalien ja odottavien toimittajan laskujen ottaminen käyttöön](../procurement/configure-materials-nonstocked.md).

Project Operationsissa projektiin liittyvät toimittajalaskut kirjataan käyttämällä erityisiä kirjaussääntöjä:

- Projektiin liittyvää kustannusta (mukaan lukien ei-palautettavissa oleva vero) ei kirjata heti projektin kustannustilille pääkirjaan. Kustannus kirjataan sen sijaan **Hankintojen integrointitilille**, jossa se voidaan integroida. Tämä asiakas on määritetty kohdassa **Projektinhallinta ja kirjanpito** > **Määrittäminen** > **Projektinhallinta- ja kirjanpitoparametrit**, **Project Operations Dynamics 365 Customer engagement** -välilehdellä.
- Kaksoiskirjoitus synkronoi toimittajan laskun tiedot Microsoft Dataverseen käyttämällä seuraavia taulukkokarttoja:

     - **Project Operationsin integrointi projektin toimittajan laskun vientientiteetti (msdyn_projectvendorinvoices)**: Tämä taulukkokartta synkronoi toimittajan laskun otsikkotiedot. Vain toimittajalaskut, joilla on vähintään yhden projektitunnuksen sisältävä rivi, synkronoidaan Dataverseen.
     - **Project Operationsin integrointi projektin toimittajan laskun vientientiteetti (msdyn_projectvendorinvoicelines)**: Tämä taulukkokartta synkronoi toimittajan laskun rivitiedot. Vain rivit, jotka sisältävät projektitunnuksen, synkronoidaan Dataverseen.

     > [!NOTE]
     > Toimittajan laskun tietoja Dataversessä ei voi muokata.

Verojen alareskontra, toimittajan alareskontra ja muut taloudelliset kirjaukset kirjataan Dynamics 365 Financeen, kun toimittajalasku julkaistaan.

![Toimittajalaskutuksen integrointi.](media/DW7VendorInvoice.png)

Kun tietueet kirjoitetaan **Toimittajan lasku** -entiteettiin Dataversessä, tietueiden automaattinen hyväksyntäprosessi alkaa. Jos tarpeen, automaattisen hyväksyntäprosessin tilan voi tarkistaa Dataversessä kohdassa **Lisäasetukset** > **Järjestelmä** > **Järjestelmätyöt**. Kun hyväksyntä on valmis, järjestelmä luo materiaalitapahtumien luokkatietueet **Toteutuneet**-entiteettiin.

Tämän jälkeen materiaaleihin liittyvät toteutuneet tiedot käsitellään käyttämällä **Project Operationsin integrointien toteutuneet (msdyn_actuals)** -kaksoiskirjoitustaulukkokarttaa. Lisätietoja on aiheissa [Projektin arviot ja todelliset kulut](resource-dual-write-estimates-actuals.md).

Jaksottainen prosessi, **Tuonti valmistelusta** luo toimittajalaskuun liittyvät Project Operationsin integrointikirjausrivit. Siirtymätilin oletusarvona on hankintojen integrointitili. Kun integrointikirjaus on julkaistu, kulutapahtuman tilisaldo tyhjennetääntoimittajan laskutapahtumalle ja rivisumma siirretään projektin kustannustilille. Projektin alareskontratapahtumat luodaan myös loppupään laskutusta ja tuottojen kirjaamista varten.
