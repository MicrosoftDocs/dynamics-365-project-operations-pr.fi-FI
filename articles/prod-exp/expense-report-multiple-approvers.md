---
title: Matkalaskun monta hyväksyjää
description: Tässä aiheessa on tietoja kuluraporteista, jotka vaativat usean henkilön hyväksynnän.
author: saraschi2
manager: AnnBe
ms.date: 02/23/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TrvExpensesReportList
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9b6d07f00fd6c1ba2d860787665d95f95f7b1a89
ms.sourcegitcommit: 9f31b33ed6e7f1b49200a407913201a1337f3401
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/14/2021
ms.locfileid: "4960603"
---
# <a name="multiple-approvers-on-an-expense-report"></a>Matkalaskun monta hyväksyjää

Organisaation kulujen hyväksyntäkäytännöt voivat edellyttää, että työntekijän lähettämä kuluraportti vaatii usean henkilön hyväksynnän. Kun määrität työnkulkuprosessin kuluraportin hyväksynnälle, voit lisätä tehtäviä tai vaiheita sisältäviä työnkulkuelementtejä yhdelle tai usealle kuluraportin hyväksyjälle. Voit esimerkiksi edellyttää, että ensin työntekijän esimiehen ja sitten ostoreskontran koordinaattorin on hyväksyttävä kaikki kuluraportit.

Jos päätät vaatia kuluraportille useita hyväksyjiä, voit lisätä työnkulkuelementit jollakin seuraavista tavoista:

- Lisää yksi hyväksyntäelementti, jossa on yksi vaihe. Vaihe voi edellyttää esimerkiksi, että kuluraportti on määritettävä käyttäjäryhmälle ja että käyttäjäryhmän jäsenistä 50 prosentin on hyväksyttävä se.
- Lisää yksi hyväksyntäelementti, jossa on useita vaiheita. Hyväksyntäelementillä voi olla esimerkiksi seuraavat vaiheet:

    1. Kuluraportin lähettäneen työntekijän esimies hyväksyy raportin.
    2. Ostoreskontran virkailija tarkistaa kuitit ja kuluraportin nimikkeet.
    3. Budjetin omistaja hyväksyy kuluraportin.

- Lisää useita hyväksyntäelementtejä, joista jokaisessa on yksi vaihe. Voit esimerkiksi lisätä erillisen hyväksyntäelementin kullekin seuraavista vaiheista:

    1. Työntekijän esimies hyväksyy kuluraportin.
    2. Budjetin omistaja hyväksyy kuluraportin.
