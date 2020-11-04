---
title: Matkalaskut ja monta hyväksyjää
description: Tässä aiheessa on tietoja kuluraporteista, jotka vaativat usean henkilön hyväksynnän.
author: suvaidya
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: ''
ms.author: shylaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 548673541cee5ce598721f94415c0444995c8325
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/16/2020
ms.locfileid: "4075351"
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
