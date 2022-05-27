---
title: Projektiarvioiden ja toteutuneiden kustannusten integrointi
description: Tässä aiheessa on tietoja Project Operationsin kuluarvioiden ja toteutuneiden kulujen integroinnista käyttämällä kaksoiskirjoitusta.
author: sigitac
ms.date: 4/26/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 5aaa59020427438fa6ebab3789fbb70c5b86e272
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/14/2022
ms.locfileid: "8577186"
---
# <a name="project-estimates-and-actuals-integration"></a>Projektiarvioiden ja toteutuneiden kustannusten integrointi

_**Käytetään:** Project Operationsin resursseihin ja ei-varastoitaviin perustuvissa skenaarioissa_

Tässä aiheessa on tietoja Project Operationsin kuluarvioiden ja toteutuneiden kulujen integroinnista käyttämällä kaksoiskirjoitusta.

## <a name="project-estimates"></a>Projektin arviot

Projektityö-, kulu- ja materiaaliarviot luodaan ja niitä ylläpidetään Microsoft Dataversessa ja synkronoidaan talous- ja toimintosovelluksiin kirjanpitoa varten. Talous- ja toimintosovellukset eivät tue luomista, päivittämistä ja poistamista.

Arvioiden luominen edellyttää projektille kelvollista kirjanpitomääritystä. Sopimusriveihin liittyvillä projekteilla on oltava voimassa oleva projekti- ja tuottoprofiili, joka on määritelty projektin kustannus- ja tuottoprofiilisäännöissä. Lisätietoja on ohjeaiheessa [Laskutettavien projektien kirjanpidon määrittäminen](../project-accounting/configure-accounting-billable-projects.md#configure-project-cost-and-revenue-profile-rules).

## <a name="labor-estimates"></a>Työvoima-arviot

Projektipäällikkö tai henkilöstöpäällikkö luo työvoima-arviot, ja he myös delegoivat projektitehtävälle yleisen tai nimetyn resurssin. Resurssin määritystietueita voi tarkastella **Resurssimääritykset**-välilehden **Projektin tiedot** -sivulla Dataversessä. Resurssin määritystietueet Dataversessa luovat tuntiennustetietueita talous- ja toimintosovelluksissa käyttämällä kohdetta **Project Operationsin integraatioentiteetti tuntiarvioille (msdyn\_resourceassignments)**.

   ![Työvoima-arvioiden integrointi.](./Media/DW4LaborEstimates.png)

Kaksoiskirjoitus synkronoi resurssien määritystietueet väliaikaiseen taulukkoon (**ProjCDSEstimateHoursImport**) kanssa ja käyttää sitten liiketoimintalogiikkaa tuntiennustetietueiden luomiseen ja päivittämiseen (**ProjForecastEmpl**).

Projektinkirjan pitäjä tarkistaa talous- ja toimintosovelluksissa luotujen tuntitietue-ennusteet kohdassa **Projektinhallinta ja kirjanpito** > **Kaikki projektit** > **Suunnitelma** > **Tuntiennusteet**.

## <a name="expense-estimates"></a>Kulujen arviot

Projektipäällikkö luo kuluarviot **Projektin tiedot** -sivun **Kuluarviot**-välilehdessä Dataversessä. Kuluarviotietueet tallennetaan **arviorivin** entiteettiin Dataversessä. Näillä arviotietueilla on tapahtumaluokka **Kulu** ja ne synkronoidaan talous- ja toimintosovellusten kuluennustetietueisiin käyttämällä kohdetta **Project Operationsin integraatioentiteetti kuluarvioille (msdyn\_estimatelines)**.

   ![Kuluarvioiden integrointi.](./Media/DW4ExpenseEstimates.png)

Kaksoiskirjoitus synkronoi kuluarviotietueet väliaikaiseen taulukkoon (**ProjCDSEstimateExpenseImport**) kanssa ja käyttää sitten liiketoimintalogiikkaa kuluennustetietueiden luomiseen ja päivittämiseen (**ProjForecastCost**). Arvioriveillä säilytetään myyntiarvio- ja kustannusarviotietueet erikseen. Talous- ja toimintosovellusten liiketoimintalogiikka täyttää yhden kuluennustetietueen käyttämällä tätä tietoa väliaikaisessa taulukossa.

Projektin kirjanpitäjä voi tarkistaa talous- ja toimintosovelluksissa kuluennusteen kohdassa **Projektinhallinta ja kirjanpito** > **Kaikki projektit** > **Suunnitelma** > **Kuluennusteet**.

## <a name="material-estimates"></a>Materiaaliarviot

Projektipäällikkö luo materiaaliarviot **Projektin tiedot** -sivun **Materiaaliarviot**-välilehdessä Dataversessä. Materiaaliarviotietueet tallennetaan **arviorivin** entiteettiin Dataversessä. Näillä arviotietueilla on tapahtumaluokka **Materiaali** ja ne synkronoidaan talous- ja toimintosovellusten nimike-ennustetietueisiin käyttämällä kohdetta **Project Operationsin integraatiotaulu materiaaliarvioille (msdyn\_estimatelines)**.

   ![Materiaaliarvioiden integrointi.](./Media/DW4MaterialEstimates.png)

Kaksoiskirjoitus synkronoi materiaaliarviotietueet väliaikaiseen taulukkoon **ProjForecastSalesImpor** kanssa ja käyttää sitten liiketoimintalogiikkaa nimike-ennustetietueiden luomiseen ja päivittämiseen (**ForecastSales**). Arvioriveillä säilytetään myyntiarvio- ja kustannusarviotietueet erikseen. Talous- ja toimintosovellusten liiketoimintalogiikka täyttää yhden nimike-ennustetietueen käyttämällä tätä tietoa väliaikaisessa taulukossa.

Projektin kirjanpitäjä voi tarkistaa talous- ja toimintosovelluksissa nimike-ennusteen kohdassa **Projektinhallinta ja kirjanpito** > **Kaikki projektit** > **Suunnitelma** > **Nimike-ennusteet**.

## <a name="project-actuals"></a>Projektin todelliset arvot

Toteutuneet projektit luodaan Dataversessä ajan, kulun, materiaalin ja laskutusaktiviteetin perusteella. Kaikki näiden tapahtumien toiminnalliset määritteet, kuten määrä, kustannushinta, myyntihinta ja projekti, tallennetaan tähän Dataverse-entiteettiin. Lue lisätietoja kohdasta [Todelliset arvot](../actuals/actuals-overview.md). Toteutuneet tietueet synkronoidaan talous- ja toimintosovelluksiin käyttämällä kaksoiskirjoitustaulukkokarttaa **Project Operations -integroinnin toteutuneet arvot (msdyn\_actuals)** myöhempää kirjanpitoa varten.

   ![Todellisten kustannusten integrointi.](./Media/DW4Actuals.png)

**Projektitoimintojen integroinnin toteutuneet** -taulukkokartta synkronoi kaikki tietueet **Toteutuneet kustannukset** -entiteetistä Dataversessä ja määritteen **Ohita synkronointi (vain sisäiseen käyttöön)** arvoksi on määritetty **Epätosi**. Tämä määritteen arvo määritetään Dataversessä automaattisesti, kun tietue luodaan. Esimerkkejä, joissa määritteen arvoksi on määritetty **Tosi**:

  - Konsernin sisäisten tapahtumien toteutuneet projektikustannukset. Lisätietoja on ohjeaiheessa [Konsernin sisäisten tapahtumien luominen](../project-accounting/create-intercompany-transactions.md). Nämä tietueet ohitetaan, koska järjestelmä luo projektin toteutuneen kustannuksen uudelleen talous- ja toimintosovelluksissa, kun konsernin sisäisen toimittajan lasku kirjataan.
  - Negatiiviset laskuttamattomat myyntitietueet, jotka luodaan proformalaskun vahvistuksen yhteydessä. Nämä tietueet ohitetaan, koska talous- ja toimintosovellusten projektin alareskontra ei peruuta laskuttamatonta myyntitietuetta laskutuksessa, vaan tilaksi tulee kokonaan laskutettu.

Kaksoiskirjoitustaulukkopöytä synkronoi toteutuneet tietueet väliaikaista taulukkoa, **ProjCDSActualsImport** varten. Nämä tietueet käsitellään jaksottaisen prosessin **Tuo valmistelutaulukosta** luotaessa Project Operationsin integrointikirjausrivejä ja projektin laskuehdotusrivejä. Lisätietoja on kohdassa [Integrointikirjauskansio Project Operationsissa](../project-accounting/project-operations-integration-journal.md).

Dataverse sisältää myös projektin toteutuneiden tapahtumien väliset linkit **Tapahtumayhteys** entiteettiin. Lisätietoja on ohjeaiheessa [Toteutuneiden kustannusten linkitäminen alkuperäisiin tietueisiin](../actuals/linkingactuals.md). Toteutuneiden tapahtumien väliset linkit synkronoidaan myös talous- ja toimintosovelluksiin käyttämällä kaksoiskirjoitustaulukkokarttaa **Integraatioentiteetti projektitapahtumien suhteille (msdyn\_transactionconnections)**. Näitä tietueita käytetään jaksottaisen prosessin **Tuo valmistelutaulukosta** luotaessa Project Operationsin integrointikirjausrivejä ja projektin laskuehdotusrivejä.

Projektitoimintojen integrointikirjauksen ja projektilaskun ehdotuksen lähettäminen käynnistää päivityksen väliaikaista taulukkoa vastaaviin tietueisiin, **IntegraCDSActualsImport**-tietueeseen. Järjestelmä kerää ja kirjaa seuraavat toteutuneiden tapahtumien kirjanpitomääritteet:

- Kirjanpidon valuuttamäärä
- Valuuttakurssi
- Tositenumero
- Arvonlisäveron summa

**Project Operationsin integroinnin toteutuneet** -taulukko päivittää toteutuneet tietueet Dataversessä näiden tietojen avulla.
