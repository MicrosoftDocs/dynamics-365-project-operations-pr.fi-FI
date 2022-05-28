---
title: Projektin vaihetyypit
description: Tässä aiheessa on tietoja projektin vaiheista.
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 06/19/2020
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.reviewer: johnmichalak
ms.openlocfilehash: 7f893b5429dd61ae45ad9d536420c96b2f58605b
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/14/2022
ms.locfileid: "8586846"
---
# <a name="project-stage-types"></a>Projektin vaihetyypit 

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Projektin vaiheet suunnitellaan vastaamaan projektin tilaa sen edetessä. Mukautusten avulla vaiheet voidaan päivittää automaattisesti käyttämällä liiketoimintaprosesseja, Power Automatea tai laajennuksia.

Seuraavat vaiheet määritetään oletusarvoisessa BPF:ssä:

- Uusi
- Tarjous
- Suunnittelu
- Toimitus
- Valmistuminen
- Sulje 

## <a name="new"></a>Uusi

Kun luot projektin, projektin vaiheeksi on määritetty **Uusi**. Jos projekti on luotu mallista, siinä voi olla aikataulu, arvio ja ryhmän tiedot. Muussa tapauksessa se on vain luonnos projektista, ja muut osat on syötettävä.

## <a name="quote"></a>Tarjous

Kun liität projektin tarjoukseen tai luot sen tarjouksesta, projektivaiheeksi on määritetty **Tarjous**, ja arvioidut aloitus- ja päättymispäivät päivitetään myös. Kun projekti on **Tarjous**-vaiheessa, **Myynti**-välilehti **Projektikohde**-sivulla näyttää tarjouksen tiedot.

## <a name="plan"></a>Suunnittelu

Kun projektiin liittyvä tarjous voittaa ja valmistelu etenee **Sopimus**-vaiheeseen, päivitetään projektin vaiheeksi **Suunnittelu**. Kun projekti on **Suunnittelu**-vaiheessa, **Projektikohde**-sivulla näytetään sopimuksen tiedot.

## <a name="deliver"></a>Toimitus

Kun projektisuunnitelma valmistuu ja olet valmis aloittamaan projektin, projektipäällikön on päivitettävä projekti vaihe **Toimitettavaksi** osoittamaan, että projekti on käynnistynyt.

## <a name="complete"></a>Valmistuminen 

Kun projektin työ on valmis, projektipäällikkö voi päivittää vaiheen **valmistuneeksi**. Kun projektipäällikkö päivittää projektin vaiheen **valmiiksi**, se osoittaa, että työ on 100 prosenttisesti valmiina, mutta että projekti on avoinna niin, että odottavat aika- tai kulukirjaukset voidaan kirjata.

## <a name="close"></a>Sulje

Kun kaikki tapahtumat on kirjattu projektille, projektipäällikkö voi päivittää vaiheen **suljetuksi**. Tässä vaiheessa tapahtumia ei voi tallentaa, ja projekti on määritetty vain luku -tilaan.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
