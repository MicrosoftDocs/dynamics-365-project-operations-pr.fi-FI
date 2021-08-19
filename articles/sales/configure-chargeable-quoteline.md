---
title: Projektiin perustuvan tarjousrivin laskutettavien komponenttien määrittäminen
description: Tässä aiheessa on tietoja projektiin perustuvien tarjousrivien sisällytetyistä, laskutettavista ja ei-laskutettavista komponenteista.
author: rumant
ms.date: 11/18/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 251d0013b445d2f7d17fbe1908f0db2e05cfc2670ac667deb363c98f608a2aef
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/06/2021
ms.locfileid: "7003992"
---
# <a name="configure-the-chargeable-components-of-a-project-based-quote-line"></a>Projektiin perustuvan tarjousrivin laskutettavien komponenttien määrittäminen

_**Käytetään:** Project Operationsin resursseihin ja ei-varastoitaviin perustuvissa skenaarioissa_

Projektiin perustuva tarjousrivi voi sisältää sisällytettyjä komponentteja ja laskutettavia osia.

Sisällytettyihin komponentteihin sovelletaan laskutustapaa, asiakasjakoja, ylittämättömiä rajoja ja laskutusväliasetuksia, jotka on määritetty projektipohjaisella tarjousrivillä.
Sisällytettyjen komponenttien alijoukko voidaan merkitä laskutettaviksi **Laskutustyypin** avulla. Voit valita jonkin seuraavista vaihtoehdoista **Laskutustyyppi**-kentässä tarjousrivin kontekstissa:

   - Veloitettava
   - Ei veloitettava

Laskutettavat komponentit voidaan määrittää rooleille ja tapahtumaluokille.

Projekti tarjousrivin rooleille määritetty laskutettavuus koskee vain **Aika**-tapahtumaluokkaa. Jos projektin tarjousrivi sisältää **Sisällytä aika** = **Ei**, **Laskutettavat roolit** -välilehti ei ole käytettävissä.

Projektin tarjousrivin tapahtumaluokille määritetty laskutettavuus koskee vain **Kulu**-tapahtumaluokkaa. Jos projektin tarjousrivi sisältää **Sisällytä kulut** = **Ei**, **Laskutettavat luokat** -välilehti ei ole käytettävissä.

## <a name="update-a-role-to-be-chargeable-or-non-chargeable"></a>Roolin päivittäminen laskutettavaksi tai ei-laskutettavaksi
Rooli voi olla laskutettava tai ei-laskutettava projektiin perustuvalla tarjousrivillä. Roolin laskutus tyyppi voidaan määrittää projektiin perustuvan tarjousrivin **Laskutettavat roolit** -välilehdessä. Se tehdään päivittämällä **Laskutustyyppi** **Veloitettavat roolit** -aliruudukossa. 

## <a name="update-a-transaction-category-to-be-chargeable-or-non-chargeable"></a>Päivitä tapahtumaluokka laskutettavaksi tai ei-laskutettavaksi
Tapahtumaluokka voi olla laskutettava tai ei-laskutettava projektiin perustuvalla tarjousrivillä. Tapahtuman laskutustyyppi voidaan määrittää projektiin perustuvan tarjousrivin **Laskutettavat luokat** -välilehdessä. Se tehdään päivittämällä **Laskutustyyppi**-kenttä **Veloitettavat luokat** -aliruudukossa. 

## <a name="resolve-chargeability"></a>Selvitä verosaatavan syntyminen

Arvioitu tai toteutunut aika voi olla laskutettava ainoastaan, jos aika on sisällytetty tarjousriviin ja rooli on määritetty laskutettavaksi.
Arvioitu tai toteutunut kulu voi olla laskutettava ainoastaan, jos kulu on sisällytetty tarjousriviin ja tapahtumaluokka on määritetty laskutettavaksi tarjousrivillä. Seuraavassa taulukossa on esitetty, kuinka laskutettavuuden oletusarvot määritetään kullekin toteutuneelle arvolle. Oletusarvot perustuvat sisällytettyihin komponentteihin ja laskutustyyppiin, joka on määritetty tarjousrivillä.

| Sisältää ajan | Sisältää kulun | Rooli | Luokka | Tehtävä |
| --- | --- | --- | --- | --- |
| Kyllä | Kyllä | Veloitettava | Veloitettava | Laskutus toteutuneesta ajasta: Laskutettava </br>Laskutustyyppi tosiasiallisesta kustannuksesta: Laskutettava |
| Kyllä | Kyllä | Ei veloitettava | Veloitettava | Laskutus toteutuneesta ajasta: Ei veloitettava </br>Laskutustyyppi tosiasiallisesta kustannuksesta: Laskutettava |
| Kyllä | Kyllä | Ei veloitettava | Ei veloitettava | Laskutus toteutuneesta ajasta: Ei veloitettava </br>Laskutustyyppi tosiasiallisesta kustannuksesta: Ei veloitettava |
| No | Kyllä | Ei voida määrittää | Veloitettava | Laskutus toteutuneesta ajasta: Ei saatavilla </br>Laskutustyyppi tosiasiallisesta kustannuksesta: Laskutettava |
| No | Kyllä | Ei voida määrittää | Ei veloitettava | Laskutus toteutuneesta ajasta: Ei saatavilla </br>Laskutustyyppi tosiasiallisesta kustannuksesta: Ei veloitettava |
| Kyllä | No | Veloitettava | Ei voida määrittää | Laskutus toteutuneesta ajasta: Laskutettava </br>Laskutustyyppi tosiasiallisesta kustannuksesta: Ei saatavilla |
| Kyllä | No | Ei veloitettava | Ei voida määrittää | Laskutus toteutuneesta ajasta: Ei veloitettava </br> Laskutustyyppi tosiasiallisesta kustannuksesta: Ei saatavilla |


[!INCLUDE[footer-include](../includes/footer-banner.md)]