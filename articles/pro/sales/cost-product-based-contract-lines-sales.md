---
title: Kustannusten tuotepohjaiset sopimusrivit – lite
description: Tässä aiheessa on tietoja siitä, kuinka luodaan
author: rumant
manager: Annbe
ms.date: 10/19/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 0e961bcf32a5dd662b7cd27a23eb5f664c45c292
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/30/2020
ms.locfileid: "4177237"
---
# <a name="cost-product-based-contract-lines---lite"></a>Kustannusten tuotepohjaiset sopimusrivit – lite

_**Käytetään:** Lite-käyttöönotto – kauppa proformalaskutukseen_


Dynamics 365 Project Operationsin tuotepohjaiset sopimusrivit sisältävät **kustannushinta**-kentän, joka tallentaa tuotteen kustannushinnan loppupään kannattavuuden laskentaan.

Kun tuotepohjainen sopimusrivi luodaan luettelotuotteelle, tuotepohjaisen sopimusrivin kustannuksen oletusarvona on tuoteluettelon **Vakiokustannus**-kenttä. Tuoteluettelon **Vakiokustannus**-kenttä määritetään organisaation perusvaluuttana. Kun yksikkökustannuksen oletusarvo on sopimusrivillä, se muunnetaan palvelusopimuksen myyntivaluutaksi.

## <a name="unit-cost-on-a-product-based-contract-line"></a>Yksikkökustannus tuotepohjaisella sopimusrivillä

Yksikkökustannusten ottaminen tuotepohjaiseen sopimusriviin sallii eri tuotekustannukset jokaiselle yksikön myynnille. Vaikka ei olekaan aina tarpeen, on tiettyjä tilanteita, joissa toimittaja voi diskontata tuotteen hintaa. Esimerkkitilanne:

Fabrikam Robotics asentaa robottikäsiä Adatum Corporationin kokoonpanolinjoilla. Fabrikam tarjoaa asennuspalveluita, mutta robottikädet hankitaan Trey Research -yrityksestä. Jos robottikäsien asennus Adatum Corporationissa avaa uuden toimialayksikön, Treyn Researchille, he voivat tarjota Fabrikamille erikoisalennuksen tästä sopimuksesta. Tässä tapauksessa Fabrikam luo tuotepohjaisen sopimusrivin robottikäsille ja syöttää tämän sopimuksen yksikkökustannukset, jotka poikkeavat Trey Researchin vakiokustannuksista.
