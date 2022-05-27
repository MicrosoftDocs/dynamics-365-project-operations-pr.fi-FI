---
title: Moderneihin hyväksyntöihin liittyviä näkökohtia päivittämistä varten
description: Tämä aihe kattaa seikat, jotka järjestelmänvalvojien on otettava huomioon, kun he mahdollistivat modernien hyväksyntöjen toiminnan.
author: stsporen
ms.date: 01/31/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: a3757f057a801318feccde9be3e49c7b40fa8fcb
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/14/2022
ms.locfileid: "8578382"
---
# <a name="upgrade-considerations-for-modern-approvals"></a>Moderneihin hyväksyntöihin liittyviä näkökohtia päivittämistä varten 

_**Koskee:** Project Operationsin resurssiin / muuhun kuin resurssiin perustuvia skenaarioita, Lite-käyttöönotto-kaupasta proformalaskutukseen_

Osana huhtikuun 2022 aallon 1 julkaisua modernit hyväksynnät ovat oletusarvoisesti käytössä. Tämä toiminto parantaa hyväksyntälogiikan luotettavuutta ja varmistaa, että hyväksyntälogiikan mahdollisen epäonnistumisen syy voidaan määrittää.

Osana tätä muutosta projektin hyväksyntöjen tilamuutokset päivitetään. Tila siirtyy nyt suoraan **Lähetetty**-tilasta **Hyväksytty**-tilaan. **Odottaa**-tila ei ole enää hyväksyntöjen tila. Voit selvittää, onko hyväksyntä odottamassa, tarkistamalla, että hyväksyntä kuuluu hyväksyntäjoukkoon, ja tarkistamalla liitetyn hyväksyntäjoukon tilan.

## <a name="before-you-upgrade"></a>Ennen päivitystä

Varmista ennen moderneihin hyväksyntöihin päivittämistä, ettei sinulla ole odottavia hyväksyntöjä. Modernit hyväksynnät eivät käytä **Odottaa**-tilaa. Siksi kaikkia hyväksyntöjä, jotka on vielä merkitty **Odottaa**-tilaan päivityksen jälkeen, ei käsitellä.

## <a name="after-you-upgrade"></a>Päivityksen jälkeen

Kun olet päivittänyt moderneihin hyväksyntöihin, järjestelmänvalvojan on tarkistettava, että hyväksyntöjä käsittelevä pilvityönkulku on otettu käyttöön.

1. Kirjaudu sisään osoitteessa [flow.microsoft.com](https://flow.microsoft.com)
2. Vaihda ympäristöksi päivitetty ympäristö sivun oikeassa yläkulmassa.
3. Valitse **Ratkaisut**, jos haluat luetteloida ympäristöön asennetut ratkaisut.
4. Valitse ratkaisuluettelosta **Project Operations** tai **Project Service**.
5. Vaihda suodatin **Kaikki**-arvosta **Pilvityönkulut**-arvoksi.
6. Tarkista, että **Project Service – Aikatauluta projektin hyväksyntäjoukot toistuvasti** -asetuksena on **Käytössä**. Jos se ei ole, valitse työnkulku ja valitse sitten **Ota käyttöön**.
7. Tarkista, että käsittely tapahtuu viiden minuutin välein, tarkistamalla **Järjestelmätyöt**-luettelon **Asetukset**-alueessa.

## <a name="short-term-rollback"></a>Lyhyen aikavälin palautus

Jos et voi ottaa muutoksia käyttöön tai kohtaat tämän ominaisuuden vakavan ongelman, voit palata alkuperäiseen hyväksyntätyönkulkuun väliaikaisesti suorittamalla seuraavat vaiheet:
1. Kirjaudu ympäristöön ja tarkista, että odottavia hyväksyntöjä ei ole.
2. Siirry kohtaan **Asetukset** > **Projektiparametrit**.
3. Valitse **Ominaisuuksien hallinta** ja poista toiminto käytöstä valitsemalla **Modernit hyväksynnät**.

## <a name="removing-the-feature-flag"></a>Toimintomerkinnän poistaminen

Lokakuun 2022 aallon 2 päivityksessä mahdollisuus poistaa tämä ominaisuus käytöstä poistetaan.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
