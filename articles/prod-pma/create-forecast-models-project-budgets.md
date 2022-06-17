---
title: Ennustemallien luominen projektibudjeteille
description: Tässä artikkelissa käsitellään ennustemallin luomista jäljellä oleville budjeteille.
author: Yowelle
ms.date: 04/24/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: johnmichalak
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: e6b1419c41124d2062595f7346efb7538e50ee33
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8916698"
---
# <a name="create-forecast-models-for-project-budgets"></a>Ennustemallien luominen projektibudjeteille 

[!include [banner](../includes/banner.md)]

Tässä artikkelissa käsitellään ennustemallin luomista jäljellä oleville budjeteille. Budjetinhallinnan kohteena oleva projekti käyttää kahdentyyppisiä budjetteja: alkuperäistä ja jäljellä olevaa projektia. Kun luot projektibudjetin, sinun täytyy määrittää alkuperäiset ja jäljellä olevat budjettiennustemallit, jotka on luotu **ennustemallit**-sivulla. Määritettyihin malleihin perustuvat projektibudjetit luodaan projektibudjetin toteutuksen yhteydessä.

> [!NOTE]
> Budjetinhallinnan ennustemallilla ei voi olla osamallia eikä sitä voi käyttää osamallina.

1. Valitse **projektinhallinta ja kirjanpito** > **asetukset** > **ennusteet**  > **ennustemallit**.
2. Valitse **Uusi**, jos haluat luoda uuden ennustemallin, ja kirjoita sitten mallin tunnusnumero ja nimi uudelle mallille. 
3. Jos haluat estää ennustemallin ennusterivien muuttamisen, aseta **pysäytetty**-asetuksen arvoksi **Kyllä**. 
4. Jos ennusteriveille, joihin malli liittyy, tulisi luoda kassavirtaennusteita pääkirjaan, aseta **Sisällytä kassavirtaennusteisiin** asetukseksi **Kyllä.** 
5. Jos haluat käyttää projektin päivämäärää laskunpäivämääränä, aseta **ennustettu laskun päivämäärä** -kentän arvoksi **Kyllä**. 
6. Valitse **budjetin tyyppi** -kentässä jokin seuraavista mallityypeistä:

   - **Alkuperäinen budjetti**: Käytä alkuperäistä budjettisummaa, joka on sidottu, kun alkuperäinen budjetti luodaan ja hyväksytään.
   - **Jäljellä oleva budjetti**: Käytä jäljellä olevia budjetin summia projektin käyttöiän aikana. Tämän ennustemallin saldosta vähennetään toteutuneita tapahtumia ja niitä korotetaan tai vähennetään budjetin versioissa.
   - **Siirto eteenpäin**: Käytä projektin siirtobudjetin summia. Siirtäminen eteenpäin on valinnainen prosessi, jonka avulla voidaan siirtää käyttämättömät budjettisummat yhdestä tilikaudesta toiseen.

7. Määritä seuraavat asetukset tarpeen mukaan:

   - Jos haluat käyttää projektin päivämäärää laskunpäivämääränä, ota **ennustettu laskun päivämäärä** käyttöön.
   - Ota käyttöön **ennuste, jossa KET** ennustaaksesi keskeneräisen työn (KET) perusteella, ja valitse sitten KET-tyyppi. 
   - Voit säilyttää oletus-**budjettityypiksi** **ei mitään** tai määrittää uuden tyypin. Budjetin tyyppiä ei voi muuttaa, kun muutat tietuetta.     
    > [!NOTE]
    > Jos muutat oletusbudjettityyppiä, kaikki muut asetukset eivät ole käytettävissä päivityksille, etkä voi käyttää tätä ennustemallia uudelleen. 
   


 



[!INCLUDE[footer-include](../includes/footer-banner.md)]