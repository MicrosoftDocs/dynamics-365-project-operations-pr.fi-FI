---
title: Kustannusten tuotepohjaiset sopimusrivit – lite
description: Tässä aiheessa on tietoja siitä, kuinka luodaan
author: rumant
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 3def4c330dc9aadbf5ff806ef7682fbfd1072e4b
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/14/2022
ms.locfileid: "8599266"
---
# <a name="cost-product-based-contract-lines---lite"></a>Kustannusten tuotepohjaiset sopimusrivit – lite

_**Käytetään:** Lite-käyttöönotto – kauppa proformalaskutukseen_


Tuotepohjaiset sopimusrivit Dynamics 365 Project Operationsissa sisältävät **Kustannushinta**-kentän, jossa on tuotteen kustannushinta kannattavuuslaskelmia varten.

Kun tuotepohjainen sopimusrivi luodaan luettelotuotteelle, rivin hinta on oletusarvon mukaan tuoteluettelon **Vakiokustannus**-kentän mukainen. Tuoteluettelon **Vakiokustannus**-kenttä määritetään organisaation perusvaluuttana. Kun yksikkökustannuksen oletusarvo on sopimusrivillä, se muunnetaan palvelusopimuksen myyntivaluutaksi.

## <a name="unit-cost-on-a-product-based-contract-line"></a>Yksikkökustannus tuotepohjaisella sopimusrivillä

Yksikkökustannusten ottaminen tuotepohjaiseen sopimusriviin sallii eri tuotekustannukset jokaiselle yksikön myynnille. Vaikka ei olekaan aina tarpeen, on tiettyjä tilanteita, joissa toimittaja voi diskontata tuotteen hintaa. Esimerkkitilanne:

Fabrikam Robotics asentaa robottikäsiä Adatum Corporationin kokoonpanolinjoilla. Fabrikam tarjoaa asennuspalvelut, mutta robottikädet ovat peräisin Trey Researchilta. Jos robottikäsien asennus Adatum Corporationissa avaa uuden toimialayksikön, Treyn Researchille, he voivat tarjota Fabrikamille erikoisalennuksen tästä sopimuksesta. Tässä tapauksessa Fabrikam luo tuotepohjaisen sopimusrivin robottikäsille. Tähän palvelusopimukseen syötetään yksikkökustannus. Kustannus eroaa Trey Researchin robottikäsien kustannuksesta.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]