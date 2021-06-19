---
title: Taloushallinnon dimension oletusarvot
description: Tässä aiheessa on tietoja taloushallinnon dimension oletusarvojen määrittämisestä.
author: sigitac
ms.date: 10/26/2020
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: d2509f74d34ac3dce4c6915ca860283750eb50b1
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/10/2021
ms.locfileid: "6013302"
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