---
title: Hyväksyntäjoukot Project Service Automationissa
description: Tässä aiheessa on tietoja hyväksyntäjoukoista, pyynnöistä ja näiden toimintojen alijoukoista.
author: stsporen
manager: tfehr
ms.date: 05/28/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 9a7a9efbd8615f4923c6795a16c9cf98a40362b6
ms.sourcegitcommit: 80aa1e8070f0cb4992ac408fc05bdffe47cee931
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/13/2021
ms.locfileid: "7323547"
---
# <a name="approval-sets-in-project-service-automation"></a>Hyväksyntäjoukot Project Service Automationissa

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Hyväksyntäjoukot ryhmittelevät hyväksyntäpyynnöt pienempiin toimintojen alijoukkoihin. Tämä ryhmittely sallii projektin käsitellä hyväksynnät järjestyksessä, ja se mahdollistaa uudelleen yrittämisen ja sekvensoinnin. Ryhmittely parantaa luotettavuutta ja jäljittämistä, kun hyväksyntöjä käsitellään suuria määriä.

Hyväksyntäjoukot osoittavat niihin liittyvien tietueiden käsittelyn kokonaistilan. Kun hyväksyntätietue käsitellään käyttämällä hyväksyntäjoukkoa, se siirtyy **Lähetetty**-tilasta **Hyväksytty**-tilaan ja irrotetaan hyväksyntäjoukosta. Jos tietue epäonnistuu, kun se lähetetään hyväksyttäväksi, se säilyy **Lähetetty**-tilassa ja hyväksyntäjoukko merkitään epäonnistuneeksi. Hyväksyntäjoukko kirjaa virhesanoman lokiin.

## <a name="processing-approvals-and-approval-sets"></a>Hyväksyntöjen ja hyväksyntäjoukkojen käsittely
Hyväksynnät, jotka on lisätty jonoon käsittelyä varten, näytetään **Käsittelyssä olevat hyväksynnät** -näkymässä. Järjestelmä yrittää käsitellä kaikki merkinnät useita kertoja asynkronisesti ja yrittää hyväksyntää uudelleen, jos aiemmat yritykset epäonnistuvat.

**Hyväksyntäjoukon elinkaari** -kenttä sisältää jäljellä olevien käsittely-yritysten määrän ennen kuin joukko merkitään epäonnistuneeksi.

## <a name="failed-approvals-and-approval-sets"></a>Epäonnistuneet hyväksynnät ja hyväksyntäjoukot
**Epäonnistuneet hyväksynnät** -näkymässä näytetään kaikki hyväksynnät, jotka edellyttävät käyttäjän toimia. Avaa asiaan liittyvät hyväksyntäjoukon lokit selvittääksesi virheen syyn.
Jos valitset **Yritä uudelleen**, hyväksyntäjoukon elinkaaren arvo kasvaa, hyväksyntäjoukko siirtyy takaisin **Käsittely**-tilaan ja jäljellä olevat tietueet yritetään käsitellä uudelleen.

## <a name="configure-approval-sets"></a>Hyväksyntäjoukkojen määrittäminen

###  <a name="enable-the-approval-sets-feature"></a>Hyväksyntäjoukot-ominaisuuden ottaminen käyttöön
Varmista ennen Hyväksyntäjoukot-ominaisuuden ottamista käyttöön, ettei hyväksyntöjä käsitellä tällä hetkellä.

- Siirry **Projektin parametrit** -sivulle ja valitse **Ominaisuuden ohjausobjekti** > **Ota modernit hyväksynnät käyttöön**.

### <a name="turn-off-the-approval-sets-feature"></a>Hyväksyntäjoukot-ominaisuuden poistaminen käytöstä
Varmista ennen Hyväksyntäjoukot-ominaisuuden käytöstä poistamista, ettei hyväksyntöjä käsitellä tällä hetkellä.

- Siirry **Projektin parametrit** -sivulle ja valitse **Ominaisuuden ohjausobjekti** > **Poista modernit hyväksynnät käytöstä**.

### <a name="configuring-the-asynchronous-threshold"></a>Asynkronisen kynnysarvon määrittäminen 
Kun hyväksyntäjoukkoja luodaan, käsittely siirtyy taustalle, kun hyväksyttäväksi valittujen tietueiden määrä ylittää määritetyn kynnysarvon. Käytä **Asynkroninen kynnysarvo** -kenttää määrittääksesi, milloin hyväksyntöjen käsittely tulisi suorittaa synkronisesti tai asynkronisesti.
Kelvolliset arvot ovat:

  - Nolla: Kaikki pyynnöt tulisi käsitellä asynkronisesti. 
  - Nollaa suuremmat arvot: Hyväksynnät käsitellään asynkronisesti vain, kun lähetettyjen hyväksyntöjen määrä ylittää tämän arvon.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
