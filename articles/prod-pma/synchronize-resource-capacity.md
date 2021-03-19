---
title: Resurssin kapasiteetin synkronointi
description: Tässä aiheessa on tietoja resurssin kapasiteetin synkronoimisesta eri kalentereissa ja projekteissa.
author: Yowelle
manager: AnnBe
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e6b63ccb5b0f04dedb8a942e22d6e1993204dc20
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5288555"
---
# <a name="synchronize-resource-capacity"></a>Resurssin kapasiteetin synkronointi

[!include [banner](../includes/banner.md)]

Resurssisynkronoinnin prosessit auttavat sen varmistamisessa, että kalenterin ja peruskalenterin tiedot kopioidaan projektin resurssiaikataulutukseen. Jos kalenteria muutetaan, prosessit tekevät tarvittavat päivitykset projektiresurssien aikataulutukseen. Prosessit auttavat myös parantamaan tehokkuutta, koska kalenterin resurssitiedot synkronoidaan etukäteen. Siksi päivitykset resurssiaikataulutustietoihin tapahtuvat nopeammin. Suosittelemme prosessien aikatauluttamista erissä sen sijaan, että ne aikataulutettaisiin yksi kerrallaan. Muussa tapauksessa on vaarana, että joku on unohtanut mukana olevat päivämäärät, kun tiedot on viimeksi synkronoitu. Jos mukana olevia päivämääriä ei käytetä, päivämäärän synkronoinnissa voi esiintyä aukkoja.

![Kalenterin synkronointi](./media/projectresourcing04-1024x471.jpg)

## <a name="synchronize-resource-capacity-roll-ups"></a>Resurssikapasiteettien koontien synkronointi

Synkronointiprosessi on suunniteltu synkronoimaan kaikki resurssikalenterin tiedot. Näihin tietoihin kuuluvat peruskalenterin tiedot kaikista muutoksista projektin resurssikalenterin kapasiteettitaulukkoon. Jos projektiin lisätään uusia resursseja, synkronointi auttaa varmistamaan, että päivitetyt kalenteritiedot ovat käytettävissä. Synkronoinnin vois suorittaa milloin tahansa.

On suositeltavaa synkronoida erissä. Asetukset ovat käytettävissä kapasiteettivarausten synkronoinnin yhteydessä.

1. Valitse **Projektinhallinta ja kirjanpito** &gt; **Jaksoittainen** &gt; **Kapasiteetin synkronointi** &gt; **Synkronoi resurssikapasiteettien koonnit**.
2. Määritä seuraavan taulukon asetukset.

    | Asetus      | Kuvaus |
    |-------------|-------------|
    | Jaksokoodi | Voit myös valita pääkirjan päivämäärävälin koodin määrittääksesi resurssikapasiteettien koontien synkronointiprosessin alkamis- ja päättymispäivät. |
    | Alkamispäivä  | Syötä resurssikapasiteettien koontien synkronointiprosessin alkamispäivä. |
    | Päättymispäivä    | Syötä resurssikapasiteettien koontien synkronointiprosessin päättymispäivä. |

[![Synkronointiprosessi](./media/projectresourcing09.jpg)](./media/projectresourcing09.jpg)


[!INCLUDE[footer-include](../includes/footer-banner.md)]