---
title: Kustannuslaskennan tuotepohjaiset tarjousrivit
description: Tässä aiheessa on tietoja kustannushinnan käyttämisestä tuotepohjaisella tarjousrivillä.
author: ruhercul
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: d9c03fa1a8f43cc110565efbafd7f5aba69f65f96bec7f15f2bd492123f639c7
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/06/2021
ms.locfileid: "7001877"
---
# <a name="costing-product-based-quote-lines"></a>Kustannuslaskennan tuotepohjaiset tarjousrivit

_**Koskee:** Project Operationsin resurssiin / muuhun kuin resurssiin perustuvia skenaarioita, Lite-käyttöönotto-kaupasta proformalaskutukseen_


Dynamics 365 Project Operationsin tuotepohjaisissa tarjousriveissä on myös **Kustannushinta**-kenttä. Tämän kentän avulla seurataan tuotteen kustannushintaa tarjousrivillä ja tehdään prosessin loppupään kannattavuuslaskelmia.

Kun tuotepohjainen tarjousrivi luodaan luettelotuotteelle, tuotepohjaisen tarjousrivin kustannuksen oletusarvona on tuoteluettelon **Vakiokustannus**-kenttä. Tuoteluettelon Vakiokustannus -kenttä määritetään organisaation perusvaluuttana. Tuotepohjaisen tarjousrivin oletusyksikkökustannus muunnetaan tarjouksen myyntivaluutaksi.

## <a name="unit-cost-on-a-product-based-quote-line"></a>Yksikkökustannus tuotepohjaisella tarjousrivillä

Yksikkökustannuksen tarkoitus tuotepohjaisella tarjousrivillä on sallia tuotteelle eri kustannukset eri myyntitilanteisiin. Tämä ei ole tyypillinen skenaario, mutta joskus toimittaja voi alentaa tuotteen kustannusta myynnin loppuasiakkaan mukaan.

Esimerkkejä:

Fabrikam Robotics asentaa robottikäsiä Datum Corporationin kokoonpanolinjoilla. Fabrikam tarjoaa asennuspalveluita, mutta robottikädet hankitaan Trey Robotics -yrityksestä. Jos robottikäsien asennus Datum Corporationissa avaa uuden toimialayksikön, Treyn robottikäsille, Trey voi antaa Fabrikamille erikoisalennuksen tästä sopimuksesta.

Tässä tapauksessa Fabrikam luo tuotepohjaisen tarjousrivin Robotic Armsille ja syöttää tälle tarjoukselle erityisen yksikkökustannuksen. Tämä kustannus poikkeaa Trey Robotic Armsin vakiokustannuksista.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]