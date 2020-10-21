---
title: Automaattisen laskun luonnin määrittäminen
description: Tässä aiheessa on tietoja siitä, miten järjestelmä määritetään luomaan laskuja automaattisesti.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 764fd4568619e4f5676ee3cbf7fce14ffb069548
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/28/2020
ms.locfileid: "3898122"
---
# <a name="configure-automated-invoice-creation"></a>Automaattisen laskun luonnin määrittäminen

_**Koskee:** Project Operationsin resurssiin / muuhun kuin resurssiin perustuvia skenaarioita, Lite-käyttöönotto-kaupasta proformalaskutukseen_

Suorita seuraavat vaiheet, jos haluat määrittää Project Operationsille automaattisen laskujen suorittamisen.

1. Siirry kohtaan **Asetukset** \> **Erätyöt**.
2. Luo erätyö ja anna sille nimeksi **Project Operationsin laskujen luominen**. Erätyön nimessä on oltava termi "laskujen luominen".
3. Valitse **Työtyyppi**-kentässä **Ei mitään**. Asetusten **Päivittäin** ja **On aktiivinen** oletusarvo on **Kyllä**.
4. Valitse **Suorita työnkulku**. **Valitse tietue** -valintaikkunassa näkyy kolme työnkulkua:

    - ProcessRunCaller
    - ProcessRunner
    - UpdateRoleUtilization

5. Valitse **ProcessRunCaller** ja sitten **Lisää**.
6. Valitse seuraavassa valintaikkunassa **OK**. **Lepo**-työnkulkua seuraa **Käsittely**-työnkulku.

    Vaiheessa 5 voit myös valita **ProcessRunner**. Kun tämän jälkeen valitset **OK**, **Käsittely**-työnkulkua seuraa **Lepo**-työnkulku.

Työnkulut **ProcessRunCaller** ja **ProcessRunner** luovat laskuja. Työnkulku **ProcessRunCaller** kutsuu työnkulun **ProcessRunner**. **ProcessRunner** on se työnkulku, joka tosiasiassa luo laskut. Se käy läpi kaikki sopimusrivit, joille on luotava lasku, ja luo kyseiset laskut. Työnkulku tarkistaa sopimusrivien laskujen suorituspäiviä määrittääkseen ne sopimusrivit, joille on luotava laskuja. Jos yhteen sopimukseen kuuluvilla sopimusriveillä on sama laskujen suorituspäivä, tapahtumat yhdistetään yhteen laskuun, jolla on kaksi laskutusriviä. Jos laskujen luomista edellyttäviä tapahtumia ei ole, työnkulku ohittaa laskujen luonnin.

Kun **ProcessRunner** on valmis, se kutsuu työnkulun **ProcessRunCaller**, antaa päättymisajan ja sulkeutuu. **ProcessRunCaller**käynnistää sitten ajastimen, joka kestää 24 tuntia määritetystä päättymisajasta eteenpäin. Ajastimen loputtua, **ProcessRunCaller** sulkeutuu.

Laskujen luomisen erätyö on toistuva työ. Jos tämä erätyö suoritetaan useita kertoja, siitä luodaan useita esiintymiä, mikä voi aiheuttaa virheitä. Siksi erätyö kannatta käynnistää vain kerran ja käynnistää uudelleen vain, jos se pysähtyy.

> [!NOTE]
> Erälaskutus suoritetaan vain sellaisille projektisopimusriveille, jotka on määritetty laskun aikataulun mukaan. Jos sopimusrivillä on kiinteähintainen laskutusmenetelmä, sillä on oltava määritettyinä välitavoitteet. Jos projektisopimusrivillä on aika- ja materiaalipohjainen laskutusmenetelmä, sille on määritettävä päivämäärään perustuva laskutusaikataulu. Sama koskee myös projektipohjaista sopimusriviä.     
