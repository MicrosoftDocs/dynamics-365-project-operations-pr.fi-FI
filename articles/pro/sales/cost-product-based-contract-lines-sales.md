---
title: Kustannusten tuotepohjaiset sopimusrivit – lite
description: Tässä artikkelissa on tietoja luonnista
author: rumant
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: a63ad12c081d19efde02303bf626184f8586d4a2
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8922908"
---
# <a name="cost-product-based-contract-lines---lite"></a>Kustannusten tuotepohjaiset sopimusrivit – lite

_**Käytetään:** Lite-käyttöönotto – kauppa proformalaskutukseen_


Tuotepohjaiset sopimusrivit Dynamics 365 Project Operationsissa sisältävät **Kustannushinta**-kentän, jossa on tuotteen kustannushinta kannattavuuslaskelmia varten.

Kun tuotepohjainen sopimusrivi luodaan luettelotuotteelle, rivin hinta on oletusarvon mukaan tuoteluettelon **Vakiokustannus**-kentän mukainen. Tuoteluettelon **Vakiokustannus**-kenttä määritetään organisaation perusvaluuttana. Kun yksikkökustannuksen oletusarvo on sopimusrivillä, se muunnetaan palvelusopimuksen myyntivaluutaksi.

## <a name="unit-cost-on-a-product-based-contract-line"></a>Yksikkökustannus tuotepohjaisella sopimusrivillä

Yksikkökustannusten ottaminen tuotepohjaiseen sopimusriviin sallii eri tuotekustannukset jokaiselle yksikön myynnille. Vaikka ei olekaan aina tarpeen, on tiettyjä tilanteita, joissa toimittaja voi diskontata tuotteen hintaa. Esimerkkitilanne:

Fabrikam Robotics asentaa robottikäsiä Adatum Corporationin kokoonpanolinjoilla. Fabrikam tarjoaa asennuspalvelut, mutta robottikädet ovat peräisin Trey Researchilta. Jos robottikäsien asennus Adatum Corporationissa avaa uuden toimialayksikön, Treyn Researchille, he voivat tarjota Fabrikamille erikoisalennuksen tästä sopimuksesta. Tässä tapauksessa Fabrikam luo tuotepohjaisen sopimusrivin robottikäsille. Tähän palvelusopimukseen syötetään yksikkökustannus. Kustannus eroaa Trey Researchin robottikäsien kustannuksesta.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]