---
title: Kustannusten tuotepohjaiset sopimusrivit – lite
description: Tässä aiheessa on tietoja siitä, kuinka luodaan
author: rumant
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 9458a57863244a68359f57185325c03a46bd6569
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/10/2021
ms.locfileid: "6003537"
---
# <a name="cost-product-based-contract-lines---lite"></a>Kustannusten tuotepohjaiset sopimusrivit – lite

_**Käytetään:** Lite-käyttöönotto – kauppa proformalaskutukseen_


Tuotepohjaiset sopimusrivit Dynamics 365 Project Operationsissa sisältävät **Kustannushinta**-kentän, jossa on tuotteen kustannushinta kannattavuuslaskelmia varten.

Kun tuotepohjainen sopimusrivi luodaan luettelotuotteelle, rivin hinta on oletusarvon mukaan tuoteluettelon **Vakiokustannus**-kentän mukainen. Tuoteluettelon **Vakiokustannus**-kenttä määritetään organisaation perusvaluuttana. Kun yksikkökustannuksen oletusarvo on sopimusrivillä, se muunnetaan palvelusopimuksen myyntivaluutaksi.

## <a name="unit-cost-on-a-product-based-contract-line"></a>Yksikkökustannus tuotepohjaisella sopimusrivillä

Yksikkökustannusten ottaminen tuotepohjaiseen sopimusriviin sallii eri tuotekustannukset jokaiselle yksikön myynnille. Vaikka ei olekaan aina tarpeen, on tiettyjä tilanteita, joissa toimittaja voi diskontata tuotteen hintaa. Esimerkkitilanne:

Fabrikam Robotics asentaa robottikäsiä Adatum Corporationin kokoonpanolinjoilla. Fabrikam tarjoaa asennuspalvelut, mutta robottikädet ovat peräisin Trey Researchilta. Jos robottikäsien asennus Adatum Corporationissa avaa uuden toimialayksikön, Treyn Researchille, he voivat tarjota Fabrikamille erikoisalennuksen tästä sopimuksesta. Tässä tapauksessa Fabrikam luo tuotepohjaisen sopimusrivin robottikäsille. Tähän palvelusopimukseen syötetään yksikkökustannus. Kustannus eroaa Trey Researchin robottikäsien kustannuksesta.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]