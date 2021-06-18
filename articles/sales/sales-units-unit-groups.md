---
title: Yksiköt ja yksikköryhmät
description: Tässä aiheessa on tietoja yksikköjen ja yksikköryhmien luomisesta Dynamics 365 Project Operationsissa.
author: rumant
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 646e20189efb4aab56972f01a52b1bff19f2e79f
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/10/2021
ms.locfileid: "5996067"
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


[!INCLUDE[footer-include](../includes/footer-banner.md)]