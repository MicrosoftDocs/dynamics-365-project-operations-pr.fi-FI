---
title: Myyntihinnaston määrittäminen
description: Tämä aihe tarjoaa tietoja projektin hinnoittelun myyntihinnastoista.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: eb8dfa61a2d17ba644daf1552889cbcde0f1e47a
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/30/2020
ms.locfileid: "4176247"
---
# <a name="set-up-a-sales-price-list"></a>Myyntihinnaston määrittäminen

_**Koskee:** Project Operationsin resurssiin / muuhun kuin resurssiin perustuvia skenaarioita, Lite-käyttöönotto-kaupasta proformalaskutukseen_

Projektihinnastolla on projektitarjousten ja -sopimusten osalta erilainen korvausmalli kuin tuotehinnastolla. Tuoteluetteloperusteisella tarjousrivillä tarjousrivin hinta voidaan korvata suoraan roolien ja luokkien hinnoilla, koska kukin tarjousrivi viittaa tasan yhteen luettelonimikkeeseen. Projektiperusteisella tarjousrivillä tarjousrivin hintaa sen sijaan ei voida korvata suoraan roolien ja luokkien hinnoilla. Käytä projektihinnastoa kahden erillisen korvausmallin kanssa.

> [!NOTE]
> Suosittelemme erillistä hinnastoa projektiresursseille ja luettelonimikkeille, koska ne toimivat eri tavoilla hinnoittelua korvattaessa.

Kullakin seuraavista entiteeteistä voi olla yksi tai useampi kohdennettu myyntihinnasto projektihinnoittelua varten:

- Asiakas (tili) 
- Mahdollisuus 
- Tarjous 
- Projektisopimus

Näiden entiteettien kohdennukset hinnastoille ilmaistaan projektin hinnastoissa. Myyntientiteeteille Asiakas, Mahdollisuus, Tarjous ja Projektisopimus voidaan kohdentaa yksi tai useampi hinnasto.

Asiakkaan tietueeseen ei lisätä oletusarvoista projektihinnastoa. Voit kuitenkin liittää projektihinnaston manuaalisesti asiakkaan tietueeseen. Manuaalista liittämistä pitäisi kuitenkin käyttää vain, kun asiakkaan kanssa on tehty mukautettu hinnoittelusopimus. 

Kun projektihinnasto liitetään myyntientiteettiin, seuraavat tiedot tarkistetaan:

- Hinnaston konteksti on **Myynti**. 
- Hinnaston valuutta vastaa asiakkaan hinnastoa. 

Projektisopimuksen liittyvien projektihinnastojen automaattisessa määrityksessä on seuraava ensisijaisuusjärjestys:

1. Tarjous
2. Mahdollisuus
3. Asiakas 
4. Yleiset asetukset 

Kun projektihinnasto määritetään oletusarvoisesti, järjestelmä tarkistaa, että valuutta vastaa asiakkaan valuuttaa ja että määritetyillä oletushinnastoilla on **Myynti**-konteksti.

Entiteeteille Asiakas, Mahdollisuus, Tarjous ja Projektisopimus voidaan kohdentaa useita projektihinnastoja. Tämä ominaisuus tukee päivämääräkohtaisia oletushintoja pitkäaikaisessa projektisopimuksessa, joka voi edellyttää useita hinnastoja inflaatiosta johtuvien hintapäivitysten mahdollistamista varten. Jos entiteetille Asiakas, Mahdollisuus, Tarjous tai Projektisopimus kohdennetuilla hinnastoilla kuitenkin on päällekkäisiä päivämäärävälejä, oletushinnat voivat olla virheellisiä. Tämän vuoksi on varmistettava, että kyseisille entiteeteille ei kohdenneta päällekkäisiä päivämäärävälejä sisältäviä projektihinnastoja.
