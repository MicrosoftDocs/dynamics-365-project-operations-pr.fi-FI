---
title: Hinnastojen aktivoinnin poistaminen
description: Tässä aiheessa kerrotaan, miten voit poistaa käyttämättömien, vanhojen hinnastojen aktivoinnin tai poistaa ne käytöstä.
author: rumant
ms.date: 03/19/2021
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Professional Service industries
ms.author: rumant
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: ab790764f7a99118fd42bc76934105389173ff88
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/14/2022
ms.locfileid: "8596879"
---
# <a name="deactivate-price-lists"></a>Hinnastojen aktivoinnin poistaminen 

_**Koskee:** Project Operationsin resurssiin / muuhun kuin resurssiin perustuvia skenaarioita, Lite-käyttöönotto-kaupasta proformalaskutukseen_

Jos haluat poistaa vanhoja tai käyttämättömiä hinnastoja Dynamics 365 Project Operationsista, suorita seuraavat kaksi vaihetta. 

1. Hinnaston poistaminen tai sen poistaminen tietyiltä sivuilta.
2. Poista hinnaston aktivointi tai poista se aktiivisista hinnastoista **Hinnastot**-sivulla.

>[!IMPORTANT]
> Molemmat vaiheet on suoritettava hinnaston poistamiseksi täysin. Ei riitä, että vain vaihe 2, jossa hinnasto poistetaan tai sen aktivointi poistetaan aktiivisten hinnastojen näkymästä, suoritetaan. On myös poistettava tämän hinnaston suhde kaikista paikoista, jotka on mainittu vaiheessa 1.

## <a name="delete-the-price-list-from-specific-pages"></a>Hinnaston poistaminen tietyiltä sivuilta
1. Jos haluat poistaa hinnaston Project Operationsista, siirry seuraaville sivuille:  

      - **Projektiparametrit**-sivu > **Hinnastot**-välilehti
      - **Organisaatioyksikkö**-sivu > **Hinnastot**-ruudukko
      - **Tilit**-sivu > **Projektihinnastot**-ruudukko
      - **Projektitarjoukset**-sivu > **Projektihinnastot** -ruudukko: Tämä koskee kaikkia aktiivisia projektitarjouksia.
      - **Projektisopimukset**-sivu > **Projektihinnastot** -ruudukko: Tämä koskee kaikkia aktiivisia projektisopimuksia.

 2. Valitse kullakin sivulla poistettava hinnasto ja valitse sitten **Poista**. 
 
## <a name="delete-or-deactivate-the-price-list-from-the-price-lists-page"></a>Poista hinnasto tai poista sen aktivointi Hinnastot-sivulla
 
1. Jos haluat poistaa hinnaston aktiivisista hinnastoista, siirry kohtaan **Myynti** > **Asiakkaat** > **Hinnastot**. 
2. Valitse poistettava hinnasto ja valitse sitten **Poista**. Jos hinnastoon viitataan aiemmin luoduissa tapahtumissa, et voi poistaa sitä. Jos tämä tapahtuu, voit poistaa hinnaston aktivoinnin niin, että se ei näy missään näkymissä. 
3. Jos haluat poistaa hinnastosta aktivoinnin, valitse hinnasto uudelleen ja valitse sitten **Poista aktivointi**.   
