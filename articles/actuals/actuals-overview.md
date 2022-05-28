---
title: Todelliset arvot
description: Tässä aiheessa on tietoja Microsoft Dynamics 365 Project Operationsin todellisten arvojen käsittelystä.
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
ms.openlocfilehash: 3f0cb8c478e2ce6fba589d51d95649f53f62e883
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/14/2022
ms.locfileid: "8581280"
---
# <a name="actuals"></a>Todelliset arvot

_**Koskee:** Project Operationsin resurssiin/ei-varastointiin perustuvia skenaarioita, Lite-käyttöönotto - kaupasta proformalaskutukseen_

Toteutuneet arvot edustavat projektin arvioitua ja hyväksyttyä taloudellista ja aikataulun edistymistä. Ne luodaan, kun ajan, kulun ja materiaalinkäytön merkinnät, kirjauskansioviennit ja laskut hyväksytään.

> [!IMPORTANT]
> Toteutuneita tietoja ei pitäisi muokata eikä poistaa järjestelmästä. Muussa tapauksessa taloudellinen yhtenäisyys ja integrointi muiden talous- ja kirjanpitojärjestelmien kanssa saattaa vaurioitua. Microsoft Dynamics 365 Project Operationsin avulla voit palauttaa ja korvata toteutuneita arvoja muokkaamalla toteutuneita arvoja projektien elinkaaren eri vaiheissa.

## <a name="recording-actuals-based-on-project-events"></a>Todellisten arvojen tallentaminen projektitapahtumien perusteella

Project Operations kirjaa toteutuneina arvoina taloushallinnon tapahtumat, jotka tapahtuvat projektitapahtuman elinkaaren aikana. Toteutuneiden arvojen luominen elinkaaren eri tapahtumissa vaihtelee sen mukaan, käyttääkö projektitapahtuma ajan ja materiaalien laskutusmallia vai kiinteähintaista laskutusmallia sekä sen mukaan, onko kyseessä vaihe ennen myyntiä vai onko kyseessä sisäinen projekti.

Seuraavissa aiheissa selitetään eri variaatioiden vaikutus Toteutuneet-taulukkoon:

- [Toteutuneiden arvojen vaikutus aika- ja materiaaliaktiviteetissa](ActualsonTM.md)
- [Toteutuneiden arvojen vaikutus kiinteähintaisessa aktiviteetissa](ActualonFP.md)
- [Vaikutukset toteutuneisiin vuorovaikutuksen myynnin ennakkovaiheessa](ActualonPreSales.md)
- [Sisäisen projektin todellisten arvojen vaikutus](ActualonInternal.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
