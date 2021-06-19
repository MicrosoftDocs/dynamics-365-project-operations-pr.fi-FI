---
title: Kustannuslaskennan tuotepohjaiset tarjousrivit
description: Tässä aiheessa on tietoja kustannushinnan käyttämisestä tuotepohjaisella tarjousrivillä.
author: ruhercul
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 1fa7896e249abfefd3e93cba4bad789e67e14f31
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/10/2021
ms.locfileid: "6003447"
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