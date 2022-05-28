---
title: Hankintaluokkien käyttö projektin ostotilauksissa ja odottavissa toimittajan laskuissa
description: Tässä aiheessa kerrotaan, miten määritetään hankintaluokkia, joita voidaan käyttää projektin ostotilauksissa ja odottavassa toimittajan laskussa.
author: sigitac
ms.date: 04/07/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: ee68d7906cb0c887c19a32363ec7fda547cb74bd
ms.sourcegitcommit: 9916f536a71b6a0078297402564ac79308ec6890
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/18/2022
ms.locfileid: "8613261"
---
# <a name="use-procurement-categories-with-project-purchase-orders-and-pending-vendor-invoices"></a>Hankintaluokkien käyttö projektin ostotilauksissa ja odottavissa toimittajan laskuissa

_**Käytetään:** Project Operationsin resursseihin ja ei-varastoitaviin perustuvissa skenaarioissa_

Hankintahenkilöstö voi luoda ja ylläpitää luetteloita nimikkeistä ja palveluista, joita voi käyttää projektin ostotilauksissa ja odottavissa toimittajalaskuissa. [Hankintaluettelot](/dynamics365/supply-chain/procurement/procurement-catalogs) ovat helppo tapa luokitella ostoja tarvitsematta määrittää ja käyttää julkaistua tuoteluetteloa. Jokainen hankintaluokka voidaan yhdistää projektiluokkaan aika-, kulu- tai nimiketapahtumia varten. Kun odottava toimittajan lasku, joka käyttää hankintaluokkaa, on julkaistu, järjestelmä luo ajan, kulujen tai materiaalin projektin toteutuneet, projektitapahtumat ja alareskontran merkinnät.

## <a name="minimum-version-requirements"></a>Vähimmäisversiovaatimukset

Seuraavia versioita edellytetään käytettäessä hankintaluokkia projektin ostotilauksissa Microsoft Dynamics 365 Project Operationsin ei-varastoitu/resurssi-pohjaisissa skenaarioissa:

- Project Operations Dataverse -ratkaisun versio 4.41.0.45 tai uudempi
- Talous- ja toimintosovellusten ympäristön versio 10.0.26 tai uudempi

## <a name="run-dual-write-maps-for-procurement-category-support"></a>Suorita kaksoiskirjoituksen määritykset hankintaluokan tukea varten

Varmista, että **Project Operations -integrointiprojektin toimittajan laskun rivin vientientiteetti msdyn\_projectvendorinvoicelines** käyttää versiota 1.0.0.4 tai uudempaa.

## <a name="enable-the-feature-key-for-procurement-categories"></a>Ota ominaisuusavain käyttöön hankintaluokille

Seuraavien vaiheiden avulla voit ottaa käyttöön toiminnot, joiden avulla projektien ostotilauksiin voi käyttää hankintaluokkia.

1. Avaa Dynamics 365 Financessa **Ominaisuuksien hallinta** -työtila.
1. Hae ja valitse ominaisuusluettelosta ominaisuus **Käytä hankintaluokkia Project Operations resurssiin/ei-varastoitaviin perustuvissa skenaarioissa** -ominaisuus ja valitse **Ota käyttöön**.

> [!IMPORTANT]
> Edellytyksenä on otettava käyttöön myös **Ota odottavat toimittajalaskut käyttöön Project Operationsin resurssiin/ei-varastoitaviin perustuvissa skenaarioissa** -ominaisuus.

## <a name="map-project-categories-in-the-procurement-category-hierarchy"></a>Yhdistä projektiluokat hankintaluokkahierarkiaan

Seuraavien vaiheiden avulla voit yhdistää projektiluokat hankintaluokkiin **Hankintaluokka**-hierarkiassa:

1. Valitse **Hankinta \> Hankintaluokat**.
1. Valitse **Muokkaa luokkahierarkiaa**.
1. Valitse haluamasi luokkahierarkian solmu ja liitä sitten **Delegoi projektiluokat** -välilehdessä solmu projektiluokkaan **Aika**-, Kulu- tai **Nimikeprojekti**-luokka (siis **Oletusaika**- tai **Oletuskulut**-luokka).
1. Valitse **Tallenna**.
1. Sulje sivu.

> [!NOTE]
> Hankintaluokan yhdistäminen projektiluokkaan on valinnaista. Jos luokkaa, jota ei ole yhdistetty, järjestelmä käyttää **Projektiluokan oletukset** -kohdan **Nimike**-kentässä määritettyä arvoa **Project Operations – Dynamics 365 Customer Engagement**-välilehdessä **Projektinhallinnan ja kirjanpidon parametrit** -sivulla.
