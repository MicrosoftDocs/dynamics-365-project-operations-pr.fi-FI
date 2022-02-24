---
title: Projektien myyntitilaukset aika- ja materiaaliprojekteille
description: Tässä aiheessa selitetään, miten projektiin perustuvia myyntitilauksia luodaan aika- ja materiaaliprojekteille.
author: Yowelle
manager: AnnBe
ms.date: 04/05/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2019-04-05
ms.dyn365.ops.version: AX 10.0.2
ms.openlocfilehash: 3653a6869dab323be88f1fd0f9fd0f2cb35c456f
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/16/2020
ms.locfileid: "4075333"
---
# <a name="project-sales-orders-for-time-and-material-projects"></a>Projektien myyntitilaukset aika- ja materiaaliprojekteille

[!include[banner](../includes/banner.md)]

Tässä aiheessa kuvataan, miten projekteille luodaan myyntitilaus. Myyntitilauksia voi luoda vain **aika ja materiaali** -tyypin projekteille.

Jos aika-ja materiaali projektin projektisopimuksissa on useita rahoituslähteitä, sinun täytyy ottaa käyttöön **Salli myyntitilaukset projekteille, joilla on useita rahoitus lähteitä** -parametri **Projektinhallinnan ja kirjanpidon parametrit** -sivulla. 

> [!NOTE]
> - Tuki projektien myyntitilauksille, joilla on useita rahoituslähteitä, on käytettävissä sovellusversiosta 10.0.2 alkaen.
> - Parametri, jolla otetaan käyttöön projektin myyntitilaukset, joilla on useita rahoituslähteitä, poistetaan huhtikuun 2020 julkaisuaallossa, minkä jälkeen toiminto on aina käytössä.

Voit luoda projektiperusteisia myyntitilauksia kahdella seuraavalla tavalla.

- Siirry projektiin itseensä. Valitse toimintoruudussa **Hallitse > Nimiketehtävät > Myyntitilaus**. Projektitiedot siirtyvät oletusarvoiksi projektin myyntitilaukseen. Jos projektisopimuksessa on useita rahoituslähteitä, sinun on valittava rahoituslähde, jotta voit määrittää asiakkaan myyntitilaukselle. Jos projektille on vain yksi rahoituslähde, asiakas määritetään automaattisesti.
- Siirry **Kaikki myyntitilaukset**-luettelosivulle ja luo uusi myyntitilaus. Sinun on valittava projekti myyntitilausta varten. Kun projekti on valittu, asiakas määritetään rahoituslähteen perusteella tai sinun on valittava rahoituslähde, jos projektisopimuksessa on useita rahoituslähteitä.

