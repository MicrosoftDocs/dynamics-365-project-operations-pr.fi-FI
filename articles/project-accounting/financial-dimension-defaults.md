---
title: Taloushallinnon dimension oletusarvot
description: Tässä artikkelissa on tietoja taloushallinnon dimension oletusarvojen määrittämisestä.
author: sigitac
ms.date: 12/14/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 10d9e0d739ac1b7681e2e77ec651daf3da8316ff
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8931050"
---
# <a name="financial-dimension-defaults"></a>Taloushallinnon dimension oletusarvot

_**Käytetään:** Project Operationsin resursseihin ja ei-varastoitaviin perustuvissa skenaarioissa_



Dynamics 365 Project Operations käyttää Dynamics 365 Financen [taloushallinnon dimensioiden](/dynamics365/finance/general-ledger/financial-dimensions) kehystä antaakseen lisätietoja projektin alareskontrasta ja kirjanpitotapahtumista.

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
