---
title: Projektin vaiheet
description: Tässä aiheessa on tietoja projektin vaiheista.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: 983c25a0-ed21-4151-a109-b385a88285fa
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 70aa057e127df7ba925e84f5d056a06a4cc8833e
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/24/2020
ms.locfileid: "3751149"
---
# <a name="project-stages"></a>Projektin vaiheet 

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Project-vaiheet päivitetään vastaamaan projektin tilaa sen edetessä. Oletusarvoinen liiketoimintaprosessi päivittää automaattisesti joitakin projektin vaiheista, kun taas toiset projektipäällikkö päivittää manuaalisesti. 

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
