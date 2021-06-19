---
title: Automaattisen laskun luonnin määrittäminen
description: Tässä aiheessa on tietoja siitä, miten järjestelmä määritetään luomaan laskuja automaattisesti.
author: rumant
ms.date: 10/13/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: dffa95c163f7f8d5074e02cd56d6f1ed429a7c72
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/10/2021
ms.locfileid: "6005337"
---
# <a name="configure-automatic-invoice-creation"></a>Automaattisen laskun luonnin määrittäminen

_**Käytetään:** Project Operationsin resursseihin ja ei-varastoitaviin perustuvissa skenaarioissa_


Suorita seuraavat vaiheet, jos haluat määrittää Dynamics 365 Project Operationsille automaattisen laskujen suorittamisen.

1. Siirry kohtaan **Asetukset** > **Erätyöt**.
2. Luo erätyö ja anna sille nimeksi **Project Operationsin laskujen luominen**. Erätyön nimessä on oltava sanat "laskujen luominen".
3. Valitse **Työtyyppi**-kentässä **Ei mitään**. Asetusten **Päivittäin** ja **On aktiivinen** oletusarvo on **Kyllä**.
4. Valitse **Suorita työnkulku**. **Valitse tietue** -valintaikkunassa näkyy kolme työnkulkua:

    - ProcessRunCaller
    - ProcessRunner
    - UpdateRoleUtilization

5. Valitse **ProcessRunCaller** ja sitten **Lisää**.
6. Valitse seuraavassa valintaikkunassa **OK**. **Lepo**-työnkulkua seuraa **Käsittely**-työnkulku.

  > [!NOTE]
  > Vaiheessa 5 voit myös valita **ProcessRunner**. Kun tämän jälkeen valitset **OK**, **Käsittely**-työnkulkua seuraa **Lepo**-työnkulku.

Työnkulut **ProcessRunCaller** ja **ProcessRunner** luovat laskuja. Työnkulku **ProcessRunCaller** kutsuu työnkulun **ProcessRunner**. **ProcessRunner** on se työnkulku, joka tosiasiassa luo laskut. Se käy läpi kaikki sopimusrivit, joille on luotava lasku, ja luo kyseiset laskut. Työnkulku tarkistaa sopimusrivien laskujen suorituspäiviä määrittääkseen ne sopimusrivit, joille on luotava laskuja. Jos yhteen sopimukseen kuuluvilla sopimusriveillä on sama laskujen suorituspäivä, tapahtumat yhdistetään yhteen laskuun, jolla on kaksi laskutusriviä. Jos laskujen luomista edellyttäviä tapahtumia ei ole, työnkulku ohittaa laskujen luonnin.

Kun **ProcessRunner** on valmis, se kutsuu työnkulun **ProcessRunCaller**, antaa päättymisajan ja sulkeutuu. **ProcessRunCaller** käynnistää sitten ajastimen, joka kestää 24 tuntia määritetystä päättymisajasta eteenpäin. Ajastimen loputtua, **ProcessRunCaller** sulkeutuu.

Laskujen luomisen erätyö on toistuva työ. Jos tämä erätyö suoritetaan useita kertoja, siitä luodaan useita esiintymiä, mikä voi aiheuttaa virheitä. Siksi erätyö kannatta käynnistää vain kerran ja käynnistää uudelleen vain, jos se pysähtyy.

> [!NOTE]
> Erälaskutus suoritetaan vain sellaisille projektisopimusriveille, jotka on määritetty laskun aikataulun mukaan. Jos sopimusrivillä on kiinteähintainen laskutusmenetelmä, sillä on oltava määritettyinä välitavoitteet. Jos projektisopimusrivillä on aika- ja materiaalipohjainen laskutusmenetelmä, sille on määritettävä päivämäärään perustuva laskutusaikataulu. Sama koskee myös projektipohjaista sopimusriviä.     


[!INCLUDE[footer-include](../includes/footer-banner.md)]