---
title: Toimittajalaskutuksen integrointi
description: Tässä artikkelissa on tietoja toimittajalaskujen integroinnista Project Operationsissa.
author: sigitac
ms.date: 04/27/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: d1e41638b6fe827e9e577860a78a84a9948053e4
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8912052"
---
# <a name="vendor-invoice-integration"></a>Toimittajalaskutuksen integrointi

_**Käytetään:** Project Operationsin resursseihin ja ei-varastoitaviin perustuvissa skenaarioissa_

Projektiin liittyvät alennukset Dynamics 365 Project Operationsissa voidaan kirjata valitsemalla **Ostoreskontralaskut** > **Laskut** > **Odottavat toimittajan laskut** ja käyttämällä odottavaa toimittajan laskuasiakirjaa. Lisätietoja on ohjeaiheessa [Ei-varastoivien materiaalien ostaminen odottavien toimittajan laskun avulla](../procurement/pending-vendor-invoices.md).

> [!IMPORTANT]
> Ennen kuin tässä artikkelissa kuvattuja toimintojen käytetään, pakolliset määritykset on tarkistettava ja niitä on käytettävä: Lisätietoja on ohjeaiheessa [Ei-varastoivien materiaalien ja odottavien toimittajan laskujen ottaminen käyttöön](../procurement/configure-materials-nonstocked.md).

Project Operationsissa projektiin liittyvät toimittajalaskut kirjataan käyttämällä erityisiä kirjaussääntöjä:

- Projektiin liittyvää kustannusta (mukaan lukien ei-palautettavissa oleva vero) ei kirjata heti projektin kustannustilille pääkirjaan. Kustannus kirjataan sen sijaan **Hankintojen integrointitilille**, jossa se voidaan integroida. Tämä asiakas on määritetty kohdassa **Projektinhallinta ja kirjanpito** > **Määrittäminen** > **Projektinhallinta- ja kirjanpitoparametrit**, **Project Operations Dynamics 365 Customer engagement** -välilehdellä.
- Kaksoiskirjoitus synkronoi toimittajan laskun tiedot Microsoft Dataverseen käyttämällä seuraavia taulukkokarttoja:

     - **Project Operationsin integrointi projektin toimittajan laskun vientientiteetti (msdyn_projectvendorinvoices)**: Tämä taulukkokartta synkronoi toimittajan laskun otsikkotiedot. Vain toimittajalaskut, joilla on vähintään yhden projektitunnuksen sisältävä rivi, synkronoidaan Dataverseen.
     - **Project Operationsin integrointi projektin toimittajan laskun vientientiteetti (msdyn_projectvendorinvoicelines)**: Tämä taulukkokartta synkronoi toimittajan laskun rivitiedot. Vain rivit, jotka sisältävät projektitunnuksen, synkronoidaan Dataverseen.

     > [!NOTE]
     > Toimittajan laskun tietoja Dataversessä ei voi muokata.

Verojen alareskontra, toimittajan alareskontra ja muut taloudelliset kirjaukset kirjataan asianmukaisesti Dynamics 365 Financeen, kun toimittajan lasku kirjataan.

![Toimittajalaskutuksen integrointi.](media/DW7VendorInvoice.png)

Kun tietueet kirjoitetaan **Toimittajan lasku** -entiteettiin Dataversessä, tietueiden automaattinen hyväksyntäprosessi alkaa. Jos tarpeen, automaattisen hyväksyntäprosessin tilan voi tarkistaa Dataversessä kohdassa **Lisäasetukset** > **Järjestelmä** > **Järjestelmätyöt**. Kun hyväksyntä on valmis, järjestelmä luo materiaalitapahtumien luokkatietueet **Toteutuneet**-entiteettiin.

Tämän jälkeen materiaaleihin liittyvät toteutuneet tiedot käsitellään käyttämällä **Project Operationsin integrointien toteutuneet (msdyn_actuals)** -kaksoiskirjoitustaulukkokarttaa. Lisätietoja on aiheissa [Projektin arviot ja todelliset kulut](resource-dual-write-estimates-actuals.md).

Jaksottainen prosessi, **Tuonti valmistelusta** luo toimittajalaskuun liittyvät Project Operationsin integrointikirjausrivit. Siirtymätilin oletusarvona on hankintojen integrointitili. Kun integrointikirjaus on julkaistu, kulutapahtuman tilisaldo tyhjennetääntoimittajan laskutapahtumalle ja rivisumma siirretään projektin kustannustilille. Projektin alareskontratapahtumat luodaan myös loppupään laskutusta ja tuottojen kirjaamista varten.
