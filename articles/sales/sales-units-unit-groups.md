---
title: Yksiköt ja yksikköryhmät
description: Tässä aiheessa on tietoja yksiköiden ja yksikköryhmien luomisesta Dynamics 365 Project Operationsissa.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
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
ms.openlocfilehash: ea5399368214a293ca7c10fabf21d82407b5c76f
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/28/2020
ms.locfileid: "3898752"
---
# <a name="units-and-unit-groups"></a>Yksiköt ja yksikköryhmät

_**Koskee:** Project Operationsin resurssiin / muuhun kuin resurssiin perustuvia skenaarioita, Lite-käyttöönotto-kaupasta proformalaskutukseen_

Yksiköt ovat määriä tai mittayksiköitä, joissa tuotteita tai palveluja myydään. Jos esimerkiksi myyt puutarhatarvikkeita, siemenien myyntiyksikkönä voi olla paketti, laatikko tai kuormalava. Yksikköryhmä on näiden yksiköiden kokoelma.

Jos haluat viimeistellä tämän aiheen vaiheet, varmista, että sinulle on annettu järjestelmänvalvojan tai Sales Professionalin esimiehen rooli tai vastaavat käyttöoikeudet.

## <a name="create-a-unit-group"></a>Yksikköryhmän luominen

1. Valitse sivustokartassa **Yksiköt**.
2. Valitse **Uusi** ja syötä **Luo yksikköryhmä** -valintaikkunaan yksikön nimi.
3. Anna **Ensisijainen yksikkö** -kenttään pienin yhteinen mittayksikkö, jossa tuotetta myydään. Voit esimerkiksi syöttää arvon Kappale tai Unssi.
4. Valitse **OK**.

## <a name="add-units-to-a-unit-group"></a>Yksiköiden lisääminen yksikköryhmään

1. Avaa yksikköryhmä ja valitse **Liittyvät**-välilehdessä **Yksiköt**. Ensisijainen yksikkö näkyy jo lisättynä.
2. Valitse **Lisää uusi yksikkö** ja syötä **Pikaluonti: Yksikkö** -sivun **Nimi**-kenttään yksikön nimi.
3. Syötä **Määrä**-kenttään yksikön sisältämä määrä. Jos laatikossa on esimerkiksi kaksi kappaletta, syötä 2. 
4. Valitse **Perusyksikkö**-kentässä perusyksikkö, joka määrittää yksikön pienimmän mittayksikön. Voit valita esimerkiksi Kappale.
5. Valitse **Tallenna**.
