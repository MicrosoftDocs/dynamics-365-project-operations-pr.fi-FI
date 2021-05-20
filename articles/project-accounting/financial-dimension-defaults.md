---
title: Taloushallinnon dimension oletusarvot
description: Tässä aiheessa on tietoja taloushallinnon dimension oletusarvojen määrittämisestä.
author: sigitac
manager: Annbe
ms.date: 10/26/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 0a76447bb1a81a7157fccc0cd58eddd1eb5995de
ms.sourcegitcommit: 3d78338773929121d17ec3386f6cb67bfb2272cc
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/27/2021
ms.locfileid: "5950125"
---
# <a name="financial-dimension-defaults"></a>Taloushallinnon dimension oletusarvot

_**Käytetään:** Project Operationsin resursseihin ja ei-varastoitaviin perustuvissa skenaarioissa_

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Dynamics 365 Project Operations käyttää [Taloushallinnon dimensiot](/dynamics365/finance/general-ledger/financial-dimensions) kehystä Dynamics 365 Financessa antamaan lisää merkityksellisiä tietoja projektin alitapahtumarekisterin ja yleisen tapahtumarekisterin tapahtumista.

Taloushallinnon oletusdimensiot voidaan määrittää asiakkaassa, projektin rajoituslähteessä, välitavoitteessa, projektin sopimusrivillä tai projektissa.

## <a name="define-default-financial-dimensions-for-a-customer"></a>Asiakkaan taloushallinnon oletusdimensioiden määrittäminen

Asiakkaan dimensio-oletukset määritetään Financessa. Määritä dimensio-oletukset suorittamalla seuraavat vaiheet.

1. Valitse **Myyntireskontra** > **Asiakkaat** > **Kaikki asiakkaat**.
2. Määritä tietyn asiakkaan talousdimension arvot **Asiakkaat**-sivun **Taloushallinnon dimensiot** -välilehdessä.

## <a name="define-default-financial-dimensions-for-project-contracts"></a>Projektisopimuksen taloushallinnon oletusdimensioiden määrittäminen

Projektisopimukset luodaan ja niitä ylläpidetään Common Data Servicessa (CDS). Projektisopimusten kirjanpitomääritteet määritetään Financen **Projektinhallinta ja kirjanpito** -moduulissa.

### <a name="set-financial-dimensions-for-a-project-funding-source"></a>Projektin rahoituslähteen taloushallinnon dimensioiden määrittäminen

1. Valitse **Projektinhallinta ja kirjanpito** > **Projektit** > **Projektiyhteyshenkilöt**.
2. Valitse päivitettävä tietue ja valitse sitten **Projektisopimus**-välilehdessä **Näytä oletuskirjanpito**.
3. Laajenna **Liittyvät tiedot** ja valitse **Rahoituslähteet**-välilehti.
4. Määritä taloushallinnon dimension oletusarvot. Huomaa, että taloushallinnon dimensioiden oletusarvo saadaan asiakastililtä.

### <a name="set-financial-dimensions-for-a-project-contract-line"></a>Projektin sopimusrivin taloushallinnon dimensioiden määrittäminen

1. Valitse **Projektinhallinta ja kirjanpito** > **Projektit** > **Projektiyhteyshenkilöt**.
2. Valitse päivitettävä tietue ja valitse sitten **Projektisopimus**-välilehdessä **Näytä oletuskirjanpito**.
3. Laajenna **Liittyvät tiedot** ja valitse **Sopimusrivit**-välilehti.
4. Määritä taloushallinnon dimension oletusarvot. Taloushallinnon dimension oletusarvot ovat käytettävissä, ja niitä voi käyttää vain kiinteähintaisilla (välitavoitteiden) sopimusrivillä.

Näitä oletusarvoja käytetään liittyvien projektien tilitapahtumissa ja laskuriveillä.

## <a name="define-default-financial-dimensions-for-projects"></a>Projektien taloushallinnon oletusdimensioiden määrittäminen

Projektit luodaan ja niitä ylläpidetään ssa (CDS). Projektien kirjanpitomääritteet määritetään Financen **Projektinhallinta ja kirjanpito** -moduulissa.

1. Valitse **Projektinhallinta ja kirjanpito** > **Projektit** > **Kaikki projektit**.
2. Valitse päivitettävä tietue ja valitse sitten **Projekti**-välilehdessä **Näytä oletuskirjanpito**.
3. Laajenna **Liittyvät tiedot** ja valitse **Määritys**-välilehti.
4. Määritä taloushallinnon dimension oletusarvot. Huomaa, että taloushallinnon dimensioiden oletusarvo saadaan asiakastililtä. Jos projekti on liitetty sopimusriviin, jossa on useita projektisopimuksen asiakkaita, ensisijaista asiakasta käytetään taloushallinnon dimensioiden oletusarvona.

Projektin taloushallinnon oletusdimensioita käytetään määrittämään aika-, kulu- ja maksutapahtumien kirjauskansioiden rivin oletusarvot **Project Operationsin integroinnin kirjauskansiossa** ja liittyvillä projektilaskuriveillä.


[!INCLUDE[footer-include](../includes/footer-banner.md)]