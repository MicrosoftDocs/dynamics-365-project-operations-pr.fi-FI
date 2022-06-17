---
title: Hyväksyntäjoukot
description: Tässä artikkelissa käsitellään näiden toimintojen hyväksyntäjoukkojen, pyyntöjen ja alijoukkojen käsittelyä.
author: stsporen
ms.date: 02/01/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: 5e030c1aa4a41b428a0f4541fd204a7a3deaba08
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8918078"
---
# <a name="approval-sets"></a>Hyväksyntäjoukot

_**Koskee:** Project Operationsin resurssiin / muuhun kuin resurssiin perustuvia skenaarioita, Lite-käyttöönotto-kaupasta proformalaskutukseen_

Hyväksyntäjoukot ryhmittelevät hyväksyntäpyynnöt pienempiin toimintojen alijoukkoihin. Tämä ryhmittely sallii hyväksyntöjen käsittelemisen projektissa, tietyssä järjestyksessä ja sallii uudelleenyrittämisen ja jaksotuksen. Hyväksyntäpyyntöjen ryhmitteleminen yhteen parantaa suurten hyväksyntämäärien käsittelyn luotettavuutta ja seurattavuutta.

Hyväksyntäjoukot osoittavat niihin liittyvien tietueiden käsittelyn kokonaistilan. Kun hyväksyntätietue käsitellään hyväksyntäjoukon avulla, tietue siirtyy tilasta **Lähetetty** tilaan **Hyväksytty**, eikä se enää linkity hyväksyntäjoukkoon. Jos tietue epäonnistuu, kun se lähetetään hyväksyttäväksi, se säilyy **Lähetetty**-tilassa ja hyväksyntäjoukko merkitään epäonnistuneeksi. Hyväksyntäjoukko kirjaa virhesanoman lokiin.

## <a name="processing-approvals-and-approval-sets"></a>Hyväksyntöjen ja hyväksyntäjoukkojen käsittely
Hyväksynnät, jotka on lisätty jonoon käsittelyä varten, näytetään **Käsittelyssä olevat hyväksynnät** -näkymässä. Järjestelmä käsittelee kaikki merkinnät useita kertoja asynkronisesti, muun muassa yrittää hyväksyntää uudelleen, jos aiemmat yritykset epäonnistuivat.

**Hyväksyntäjoukon elinkaari** -kenttä sisältää jäljellä olevien käsittely-yritysten määrän ennen kuin joukko merkitään epäonnistuneeksi.

Hyväksyntäjoukot käsitellään jaksottaisen aktivoinnin kautta perustuen **pilvityönkulkuun** nimeltä **Project Service - Aikatauluta projektin hyväksyntäjoukot toistuvasti**. Tämä löytyy **Project Operations** -nimisestä **ratkaisusta**. 

Varmista, että työnkulku on aktivoitu seuraavien vaiheiden mukaisesti.

1. Kirjaudu järjestelmänvalvojana sisään osoitteeseen [flow.microsoft.com](https://powerautomate.microsoft.com).
2. Siirry oikeassa yläkulmassa ympäristöön, jossa käytössäsi on Dynamics 365 Project Operations.
3. Valitse **Ratkaisut**, jos haluat luetteloida ympäristöön asennetut ratkaisut.
4. Valitse ratkaisuluettelossa **Project Operations**.
5. Vaihda suodatin **Kaikki**-arvosta **Pilvityönkulut**-arvoksi.
6. Tarkista, että **Project Service – Aikatauluta projektin hyväksyntäjoukot toistuvasti** -työnkulku on **Käytössä**. Jos se ei ole, valitse työnkulku ja valitse sitten **Ota käyttöön**.
7. Tarkista, että käsittely tapahtuu viiden minuutin välein, tarkistamalla Project Operationsin Dataverse-ympäristön **Asetukset**-alueen **Järjestelmätyöt**-luettelo.

## <a name="failed-approvals-and-approval-sets"></a>Epäonnistuneet hyväksynnät ja hyväksyntäjoukot
**Epäonnistuneet hyväksynnät** -näkymä luetteloi kaikki hyväksynnät, jotka vaativat käyttäjän toimia. Avaa asiaan liittyvät hyväksyntäjoukon lokit selvittääksesi virheen syyn.
Jos valitset **Yritä uudelleen**, hyväksyntäjoukon elinkaaren arvo kasvaa, hyväksyntäjoukko siirtyy takaisin **Käsittely**-tilaan ja jäljellä olevat tietueet yritetään käsitellä uudelleen.

## <a name="configure-approval-sets"></a>Hyväksyntäjoukkojen määrittäminen

### <a name="enable-the-approval-sets-feature"></a>Hyväksyntäjoukot-ominaisuuden ottaminen käyttöön
Varmista ennen Hyväksyntäjoukot-ominaisuuden ottamista käyttöön, ettei hyväksyntöjä käsitellä tällä hetkellä.

- Siirry **Projektin parametrit** -sivulle ja valitse **Ominaisuuden ohjausobjekti** > **Ota modernit hyväksynnät käyttöön**.

### <a name="turn-off-the-approval-sets-feature"></a>Hyväksyntäjoukot-ominaisuuden poistaminen käytöstä
Varmista ennen Hyväksyntäjoukot-ominaisuuden käytöstä poistamista, ettei hyväksyntöjä käsitellä tällä hetkellä.

- Siirry **Projektin parametrit** -sivulle ja valitse **Ominaisuuden ohjausobjekti** > **Poista modernit hyväksynnät käytöstä**.

### <a name="configuring-the-asynchronous-threshold"></a>Asynkronisen kynnysarvon määrittäminen 
Kun hyväksyntäjoukkoja luodaan, käsittely siirtyy taustalle, kun hyväksyttäväksi valittujen tietueiden määrä ylittää määritetyn kynnysarvon. Käytä **Asynkroninen kynnysarvo** -kenttää määrittääksesi, milloin hyväksyntöjen käsittely tulisi suorittaa synkronisesti tai asynkronisesti. Valitse yksi seuraavista arvoista:

  - Nolla: Kaikki pyynnöt tulisi käsitellä asynkronisesti. 
  - Nollaa suuremmat arvot: Hyväksynnät käsitellään asynkronisesti vain, kun lähetettyjen hyväksyntöjen määrä ylittää tämän arvon.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
