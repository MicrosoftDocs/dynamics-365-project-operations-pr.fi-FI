---
title: Todelliset arvot
description: Tässä artikkelissa on tietoja Microsoft Dynamics 365 Project Operationsin todellisten arvojen käsittelystä.
author: rumant
ms.date: 02/22/2022
ms.topic: overview
ms.prod: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.assetid: ''
ms.search.region: ''
ms.search.industry: ''
ms.author: rumant
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 2551b7d6d20df170c913e302e734583135265529
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8924794"
---
# <a name="actuals"></a>Todelliset arvot

_**Koskee:** Project Operationsin resurssiin/ei-varastointiin perustuvia skenaarioita, Lite-käyttöönotto - kaupasta proformalaskutukseen_

Toteutuneet arvot edustavat projektin arvioitua ja hyväksyttyä taloudellista ja aikataulun edistymistä. Ne luodaan, kun ajan, kulun ja materiaalinkäytön merkinnät, kirjauskansioviennit ja laskut hyväksytään.

> [!IMPORTANT]
> Toteutuneita tietoja ei pitäisi muokata eikä poistaa järjestelmästä. Muussa tapauksessa taloudellinen yhtenäisyys ja integrointi muiden talous- ja kirjanpitojärjestelmien kanssa saattaa vaurioitua. Microsoft Dynamics 365 Project Operationsin avulla voit palauttaa ja korvata toteutuneita arvoja muokkaamalla toteutuneita arvoja projektien elinkaaren eri vaiheissa.

## <a name="recording-actuals-based-on-project-events"></a>Todellisten arvojen tallentaminen projektitapahtumien perusteella

Project Operations kirjaa toteutuneina arvoina taloushallinnon tapahtumat, jotka tapahtuvat projektitapahtuman elinkaaren aikana. Toteutuneiden arvojen luominen elinkaaren eri tapahtumissa vaihtelee sen mukaan, käyttääkö projektitapahtuma ajan ja materiaalien laskutusmallia vai kiinteähintaista laskutusmallia sekä sen mukaan, onko kyseessä vaihe ennen myyntiä vai onko kyseessä sisäinen projekti.

Seuraavissa artikkeleissa käsitellään eri variaatioiden vaikutusta Toteutuneet-taulukkoon:

- [Toteutuneiden arvojen vaikutus aika- ja materiaaliaktiviteetissa](ActualsonTM.md)
- [Toteutuneiden arvojen vaikutus kiinteähintaisessa aktiviteetissa](ActualonFP.md)
- [Vaikutukset toteutuneisiin vuorovaikutuksen myynnin ennakkovaiheessa](ActualonPreSales.md)
- [Sisäisen projektin todellisten arvojen vaikutus](ActualonInternal.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
