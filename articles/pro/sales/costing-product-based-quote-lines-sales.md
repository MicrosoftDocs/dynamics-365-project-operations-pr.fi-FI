---
title: Kustannuslaskennan tuotepohjaiset tarjousrivit
description: Tässä artikkelissa on tietoja kustannushinnan käyttämisestä tuotepohjaisella tarjousrivillä.
author: ruhercul
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: 23eb3d29081769347d62098534a9863fd28fa90c
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8932568"
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