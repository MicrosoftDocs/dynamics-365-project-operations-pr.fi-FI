---
title: Projektiarvioiden ja toteutuneiden kustannusten integrointi
description: Tässä aiheessa on tietoja Project Operationsin kuluarvioiden ja toteutuneiden kulujen integroinnista käyttämällä kaksoiskirjoitusta.
author: sigitac
ms.date: 4/26/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: d8aa1541a3560db175acead1d000895312b299db
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/10/2021
ms.locfileid: "6000027"
---
# <a name="project-estimates-and-actuals-integration"></a>Projektiarvioiden ja toteutuneiden kustannusten integrointi

_**Käytetään:** Project Operationsin resursseihin ja ei-varastoitaviin perustuvissa skenaarioissa_

Tässä aiheessa on tietoja Project Operationsin kuluarvioiden ja toteutuneiden kulujen integroinnista käyttämällä kaksoiskirjoitusta.

## <a name="project-estimates"></a>Projektin arviot

Projektityö-, kulu- ja materiaaliarviot luodaan ja ylläpidetään Microsoft Dataversessä ja synkronoidaan Finance and Operations -sovelluksiin kirjanpitoa varten. Finance and Operations -sovellusten avulla ei tueta luonti-, päivitys- ja poistotoimintoja.

Arvioiden luominen edellyttää projektille kelvollista kirjanpitomääritystä. Sopimusriveihin liittyvillä projekteilla on oltava voimassa oleva projekti- ja tuottoprofiili, joka on määritelty projektin kustannus- ja tuottoprofiilisäännöissä. Lisätietoja on ohjeaiheessa [Laskutettavien projektien kirjanpidon määrittäminen](../project-accounting/configure-accounting-billable-projects.md#configure-project-cost-and-revenue-profile-rules).

## <a name="labor-estimates"></a>Työvoima-arviot

Projektipäällikkö tai henkilöstöpäällikkö luo työvoima-arviot, ja he myös delegoivat projektitehtävälle yleisen tai nimetyn resurssin. Resurssin määritystietueita voi tarkastella **Resurssimääritykset**-välilehden **Projektin tiedot** -sivulla Dataversessä. Resurssimääritykset Dataversessä luovat tuntiennustetietueet Finance and Operations -sovelluksissa, joissa käytetään **Project Operationsin integrointientiteettiä tuntiarvioita varten (msdyn\_resourceassignments)**.

   ![Työvoima-arvioiden integrointi](./Media/DW4LaborEstimates.png)

Kaksoiskirjoitus synkronoi resurssien määritystietueet väliaikaiseen taulukkoon (**ProjCDSEstimateHoursImport**) kanssa ja käyttää sitten liiketoimintalogiikkaa tuntiennustetietueiden luomiseen ja päivittämiseen (**ProjForecastEmpl**).

Projektin kirjanpitäjä arvioi Finance and Operations -sovelluksissa luodut tuntitietueet valitsemalla **Projektinhallinta ja kirjanpito** > **Kaikki projektit** > **Suunnittele** > **Tuntiennusteet**.

## <a name="expense-estimates"></a>Kulujen arviot

Projektipäällikkö luo kuluarviot **Projektin tiedot** -sivun **Kuluarviot**-välilehdessä Dataversessä. Kuluarviotietueet tallennetaan **arviorivin** entiteettiin Dataversessä. Näillä arviotietueilla on tapahtumaluokka, **kulu** ja ne synkronoidaan Finance and Operations -sovellusten kuluennustetietueisiin käyttämällä **Project Operationsin integrointientiteettiä kuluarvioille (msdyn\_estimatelines)**.

   ![Kuluarvioiden integrointi](./Media/DW4ExpenseEstimates.png)

Kaksoiskirjoitus synkronoi kuluarviotietueet väliaikaiseen taulukkoon (**ProjCDSEstimateExpenseImport**) kanssa ja käyttää sitten liiketoimintalogiikkaa kuluennustetietueiden luomiseen ja päivittämiseen (**ProjForecastCost**). Arvioriveillä säilytetään myyntiarvio- ja kustannusarviotietueet erikseen. Finance and Operations -sovellusten liiketoimintalogiikka täyttää yhden kuluennustetietueen käyttämällä tätä erittelyä valmistelutaulukossa.

Projektin kirjanpitäjä voi arvioida Finance and Operations -sovelluksissa luodut kulutietueet valitsemalla **Projektinhallinta ja kirjanpito** > **Kaikki projektit** > **Suunnittele** > **Kuluennusteet**.

## <a name="material-estimates"></a>Materiaaliarviot

Projektipäällikkö luo materiaaliarviot **Projektin tiedot** -sivun **Materiaaliarviot**-välilehdessä Dataversessä. Materiaaliarviotietueet tallennetaan **arviorivin** entiteettiin Dataversessä. Näillä arviotietueilla on tapahtumaluokka, **materiaali** ja ne synkronoidaan Finance and Operations -sovellusten nimike-ennustetietueisiin käyttämällä **Projektin integrointitaulukkoa materiaaliarvioille (msdyn\_estimatelines)**.

   ![Materiaaliarvioiden integrointi](./Media/DW4MaterialEstimates.png)

Kaksoiskirjoitus synkronoi materiaaliarviotietueet väliaikaiseen taulukkoon **ProjForecastSalesImpor** kanssa ja käyttää sitten liiketoimintalogiikkaa nimike-ennustetietueiden luomiseen ja päivittämiseen (**ForecastSales**). Arvioriveillä säilytetään myyntiarvio- ja kustannusarviotietueet erikseen. Finance and Operations -sovellusten liiketoimintalogiikka täyttää yhden nimike-ennustetietueen käyttämällä tätä erittelyä valmistelutaulukossa.

Projektin kirjanpitäjä voi arvioida Finance and Operations -sovelluksissa luodut nimike-tietueet valitsemalla **Projektinhallinta ja kirjanpito** > **Kaikki projektit** > **Suunnittele** > **Nimike-ennusteet**.

## <a name="project-actuals"></a>Projektin todelliset arvot

Toteutuneet projektit luodaan Dataversessä ajan, kulun, materiaalin ja laskutusaktiviteetin perusteella. Kaikki näiden tapahtumien toiminnalliset määritteet, kuten määrä, kustannushinta, myyntihinta ja projekti, tallennetaan tähän Dataverse-entiteettiin. Lue lisätietoja kohdasta [Todelliset arvot](../actuals/actuals-overview.md). Todelliset tiedot synkronoidaan Finance and Operations -sovelluksiin käyttämällä kaksoiskirjoitustaulukkokarttaa **Project Operationsin integrointien toteutuneet (msdyn\_actuals)** loppupään kirjanpitoa varten.

   ![Todellisten kustannusten integrointi](./Media/DW4Actuals.png)

**Projektitoimintojen integroinnin toteutuneet** -taulukkokartta synkronoi kaikki tietueet **Toteutuneet kustannukset** -entiteetistä Dataversessä ja määritteen **Ohita synkronointi (vain sisäiseen käyttöön)** arvoksi on määritetty **Epätosi**. Tämä määritteen arvo määritetään Dataversessä automaattisesti, kun tietue luodaan. Esimerkkejä, joissa määritteen arvoksi on määritetty **Tosi**:

  - Konsernin sisäisten tapahtumien toteutuneet projektikustannukset. Lisätietoja on ohjeaiheessa [Konsernin sisäisten tapahtumien luominen](../project-accounting/create-intercompany-transactions.md). Nämä tietueet ohitetaan, koska järjestelmä luo projektin kustannuksen uudelleen Finance and Operations -sovelluksissa, kun konsernin toimittajan lasku on julkaistu.
  - Negatiiviset laskuttamattomat myyntitietueet, jotka luodaan proformalaskun vahvistuksen yhteydessä. Nämä tietueet ohitetaan, koska Finance and Operations -sovellusten projektin alareskontra ei palauta laskuttamatonta myyntitietuetta laskutuksessa, vaan tilaksi tulee kokonaan laskutettu.

Kaksoiskirjoitustaulukkopöytä synkronoi toteutuneet tietueet väliaikaista taulukkoa, **ProjCDSActualsImport** varten. Nämä tietueet käsitellään jaksottaisen prosessin **Tuo valmistelutaulukosta** luotaessa Project Operationsin integrointikirjausrivejä ja projektin laskuehdotusrivejä. Lisätietoja on kohdassa [Integrointikirjauskansio Project Operationsissa](../project-accounting/project-operations-integration-journal.md).

Dataverse sisältää myös projektin toteutuneiden tapahtumien väliset linkit **Tapahtumayhteys** entiteettiin. Lisätietoja on ohjeaiheessa [Toteutuneiden kustannusten linkitäminen alkuperäisiin tietueisiin](../actuals/linkingactuals.md). Myös todellisten tapahtumien väliset linkit synkronoidaan Finance and Operations -sovelluksiin käyttämällä kaksoiskirjoitustaulukkokarttaa **Projektitapahtumasuhteiden integrointientiteetit (msdyn\_transactionconnections)**. Näitä tietueita käytetään jaksottaisen prosessin **Tuo valmistelutaulukosta** luotaessa Project Operationsin integrointikirjausrivejä ja projektin laskuehdotusrivejä.

Projektitoimintojen integrointikirjauksen ja projektilaskun ehdotuksen lähettäminen käynnistää päivityksen väliaikaista taulukkoa vastaaviin tietueisiin, **IntegraCDSActualsImport**-tietueeseen. Järjestelmä kerää ja kirjaa seuraavat toteutuneiden tapahtumien kirjanpitomääritteet:

- Kirjanpidon valuuttamäärä
- Valuuttakurssi
- Tositenumero
- Arvonlisäveron summa

**Project Operationsin integroinnin toteutuneet** -taulukko päivittää toteutuneet tietueet Dataversessä näiden tietojen avulla.
