---
title: Yksiköt ja yksikköryhmät
description: Tässä artikkelissa on tietoja yksikköjen ja yksikköryhmien luomisesta Dynamics 365 Project Operationsissa.
author: rumant
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: a46b7d182d3d7fc77c1275c108f5dc569ffebff1
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8921436"
---
# <a name="units-and-unit-groups"></a>Yksiköt ja yksikköryhmät

_**Koskee:** Project Operationsin resurssiin / muuhun kuin resurssiin perustuvia skenaarioita, Lite-käyttöönotto-kaupasta proformalaskutukseen_

Yksiköt ovat määriä tai mittayksiköitä, joissa tuotteita tai palveluja myydään. Jos esimerkiksi myyt puutarhatarvikkeita, siemenien myyntiyksikkönä voi olla paketti, laatikko tai kuormalava. Yksikköryhmä on näiden yksiköiden kokoelma.

Jos haluat viimeistellä tämän artikkelin vaiheet, varmista, että sinulle on annettu järjestelmänvalvojan tai Sales Professionalin esimiehen rooli tai vastaavat käyttöoikeudet.

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