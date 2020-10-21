---
title: Matkalaskut ja monta hyväksyjää
description: Tässä aiheessa on tietoja kuluraporteista, jotka vaativat usean henkilön hyväksynnän.
author: suvaidya
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: ''
ms.author: shylaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 818092dd631d07cc0a7d63c9eec51eeff4f67ffe
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/28/2020
ms.locfileid: "3897087"
---
# <a name="expense-reports-and-multiple-approvers"></a>Matkalaskut ja monta hyväksyjää

_**Koskee:** Project Operationsin resurssiin / muuhun kuin resurssiin perustuvia skenaarioita, Lite-käyttöönotto-kaupasta proformalaskutukseen_

Organisaation kulujen hyväksyntäkäytännöt voivat edellyttää, että lähetetty kuluraportti vaatii usean henkilön hyväksynnän. Kun määrität työnkulkuprosessin kuluraportin hyväksynnälle, voit lisätä tehtäviä tai vaiheita sisältäviä työnkulkuelementtejä yhdelle tai usealle kuluraportin hyväksyjälle. Voit esimerkiksi edellyttää, että kahden henkilön on hyväksyttävä kaikki kuluraportit. Henkilöt voivat olla raportin lähettäneen työntekijän esimies ja ostoreskontran koordinaattori.

Jos päätät vaatia kuluraportille useita hyväksyjiä, voit lisätä työnkulkuelementit jollakin seuraavista tavoista:

- Lisää yksi hyväksyntäelementti, jossa on yksi vaihe. Vaihe voi edellyttää esimerkiksi, että kuluraportti on määritettävä käyttäjäryhmälle ja että käyttäjäryhmän jäsenistä 50 prosentin on hyväksyttävä se.
- Lisää yksi hyväksyntäelementti, jossa on useita vaiheita. Hyväksyntäelementillä voi olla esimerkiksi seuraavat vaiheet:

    1. Kuluraportin lähettäneen työntekijän esimies hyväksyy raportin.
    2. Ostoreskontran virkailija tarkistaa kuitit ja kuluraportin nimikkeet.
    3. Budjetin omistaja hyväksyy kuluraportin.

- Lisää useita hyväksyntäelementtejä, joista jokaisessa on yksi vaihe. Voit esimerkiksi lisätä erillisen hyväksyntäelementin kullekin seuraavista vaiheista:

    1. Työntekijän esimies hyväksyy kuluraportin.
    2. Budjetin omistaja hyväksyy kuluraportin.
