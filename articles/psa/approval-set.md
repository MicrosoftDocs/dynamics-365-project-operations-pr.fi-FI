---
title: Hyväksyntäjoukot Project Service Automationissa
description: Tässä artikkelissa on tietoja hyväksyntäjoukoista, pyynnöistä ja näiden toimintojen alijoukoista.
author: stsporen
manager: tfehr
ms.date: 05/28/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: 568815967b909d2a5ee9bf40b4fee97e0ad4d295
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8927048"
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
