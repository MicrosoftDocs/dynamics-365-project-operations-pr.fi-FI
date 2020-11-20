---
title: Projektipohjaisen sopimusrivin veloitettavien komponenttien määrittäminen
description: Tässä ohjeaiheessa on tietoja sisällytetyistä, laskutettavista ja ei-laskutettavista komponenteista sopimusriveillä.
author: rumant
manager: Annbe
ms.date: 10/12/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: d6f67d5dc6b94148d437b3399229c1235c702c6a
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/28/2020
ms.locfileid: "4128684"
---
# <a name="configure-chargeable-components-of-a-project-based-contract-line"></a>Projektipohjaisen sopimusrivin veloitettavien komponenttien määrittäminen

_**Käytetään:** Project Operationsin resursseihin ja ei-varastoitaviin perustuvissa skenaarioissa_

Projektipohjaisella sopimusrivillä on sisällytettyjen, laskutettavien ja ei-laskutettavien osien käsitteet.

Sisällytettyinä oleviin komponentteihin sovelletaan laskutustapaa, asiakasjakoja, ylittämättömiä rajoja ja laskun toistumisväliasetuksia, jotka on määritetty projektipohjaisella sopimusrivillä.

Sisällytettyjen komponenttien alijoukko voidaan merkitä laskutettaviksi päivittämällä **Laskutustyyppi**-kenttä.

Laskutettavat komponentit voidaan määrittää rooleille ja tapahtumaluokille.

Projektisopimusrivillä roolille määritetty maksuvalmius koskee vain **Ajan** tapahtumaluokkaa. Jos **Sisällytä aika** -asetus on **Ei** projektisopimusrivillä, **Veloitettavat roolit** -välilehti ei ole käytettävissä.

Projektisopimusrivin tapahtumakategorioihin määritetty maksuvalmius koskee vain **Kulu** tapahtumaluokkaa. Jos **Sisällytä kulut** -asetus on **Ei** projektisopimusrivillä, **Veloitettavat luokat** -välilehti ei ole käytettävissä.

### <a name="update-a-role-to-be-chargeable-or-non-chargeable"></a>Roolin päivittäminen laskutettavaksi tai ei-laskutettavaksi

Tietyn projektipohjaisen sopimusrivin rooli voi olla laskutettava tai ei-laskutettava.

Päivitä roolin laskutustyyppi projektipohjaisen sopimusrivin **Veloitettavat roolit** -välilehden **Veloitettavat luokat** -aliruudukon **Laskutustyyppi**-kentässä.

### <a name="update-a-transaction-category-to-be-chargeable-or-non-chargeable"></a>Päivitä tapahtumaluokka laskutettavaksi tai ei-laskutettavaksi

Tietyn projektipohjaisen sopimusrivin tapahtumaluokka voi olla laskutettava tai ei-laskutettava.

Päivitä tapahtuman laskutustyyppi projektipohjaisen sopimusrivin **Veloitettavat luokat** -välilehden **Veloitettavat luokat** -aliruudukon **Laskutustyyppi**-kentässä.

### <a name="resolve-chargeability"></a>Selvitä verosaatavan syntyminen

Arviota tai todellista luontiaikaa voidaan pitää veloitettavissa vain, jos sopimusriville on lisätty aika ja jos rooli on määritetty laskutettaviksi sopimusrivillä.

Arviota tai todellista kulua voidaan pitää veloitettavissa vain, jos sopimusriville on lisätty kulu ja jos tehtäväluokka on määritetty laskutettaviksi sopimusrivillä.

| Sisältää ajan | Sisältää kulun | Rooli | Luokka | Tehtävä |
| --- | --- | --- | --- | --- |
| Kyllä | Kyllä | Veloitettava | Veloitettava | Laskutus toteutuneesta ajasta: Laskutettava </br>Laskutustyyppi tosiasiallisesta kustannuksesta: Laskutettava |
| Kyllä | Kyllä | Ei veloitettava | Veloitettava | Laskutus toteutuneesta ajasta: Ei veloitettava </br>Laskutustyyppi tosiasiallisesta kustannuksesta: Laskutettava |
| Kyllä | Kyllä | Ei veloitettava | Ei veloitettava | Laskutus toteutuneesta ajasta: Ei veloitettava </br>Laskutustyyppi tosiasiallisesta kustannuksesta: Ei veloitettava |
| No | Kyllä | Ei voida määrittää | Veloitettava | Laskutus toteutuneesta ajasta: Ei saatavilla </br>Laskutustyyppi tosiasiallisesta kustannuksesta: Laskutettava |
| No | Kyllä | Ei voida määrittää | Ei veloitettava | Laskutus toteutuneesta ajasta: Ei saatavilla </br>Laskutustyyppi tosiasiallisesta kustannuksesta: Ei veloitettava |
| Kyllä | No | Veloitettava | Ei voida määrittää | Laskutus toteutuneesta ajasta: Laskutettava </br>Laskutustyyppi tosiasiallisesta kustannuksesta: Ei saatavilla |
| Kyllä | No | Ei veloitettava | Ei voida määrittää | Laskutus toteutuneesta ajasta: Ei veloitettava </br> Laskutustyyppi tosiasiallisesta kustannuksesta: Ei saatavilla |
