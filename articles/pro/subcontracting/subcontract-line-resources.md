---
title: Alihankintarivin resurssit
description: Tässä artikkelissa käsitellään sellaisten erillisten resurssien määrittämistä, jotka toimittaja antaa tietylle alihankinnan aikariville.
author: rumant
ms.date: 08/06/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 84fbbd6e1a82db2b2d998b5f41579396df884ec3
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8924150"
---
# <a name="subcontract-line-resources"></a>Alihankintarivin resurssit

[!include [banner](../../includes/dataverse-preview.md)]

_**Käytetään:** Lite-käyttöönotto – kauppa proformalaskutukseen_

Dynamics 365 Project Operationsissa toimittaja voi määrittää resurssit, joita käytetään resurssikapasiteetin, joka ostetaan alihankinnan aikarivillä, toimittamiseen.

## <a name="create-subcontract-line-resources"></a>Alihankintarivin resurssien luominen

Luodaksesi alihankintarivin resursseja toimi seuraavasti:

1. Valitse siirtymisruudussa **Alihankinnat** ja avaa sitten alihankinta, jota haluat käsitellä.
2. Avaa alihankinnan aikarivi, jolle haluat määrittää toimittajan resursseja.
3. Valitse **Alihankintarivin resurssit** -välilehden aliruudukosta **+ Uusi alihankintarivin resurssi**.
4. Syötä **Uusi alihankintarivin resurssi** -sivulla tarvittavat tiedot ja valitse sitten **Tallenna ja sulje**.

Seuraavassa taulukossa selitetään alihankintarivin resurssin kentät.

| Kenttä | Kuvaus | Toiminnallinen vaikutus |
| ----- | ----------- | ----------------- |
| Varattavissa oleva resurssi | Valitse **Sopimustyöntekijä**-tyyppinen varattava resurssi, jota haluat käyttää resurssina alihankintarivillä.| Jos et ole luonut varattavaa resurssia palvelusopimuksen työntekijälle, jätä tämä kenttä tyhjäksi. Varattava resurssi luodaan, kun tallennat tietueen.  |
| Ota yhteyttä | Voit luoda alihankintarivin resurssin aiemmin luodusta yhteyshenkilöstä. Käytä hakua tarkastellaksesi järjestelmässä olevia aktiivisia yhteyshenkilöitä. Valitse tälle alihankinnalle toimittajan yhteyshenkilö. Jos valitsemasi yhteyshenkilö ei ole alihankinnassa olevan toimittajan kelvollinen yhteyshenkilö, alihankintarivin resurssin tietuetta ei tallenneta.| Jos valitulle yhteyshenkilölle ei ole varattavaa resurssia, järjestelmä luo varattavan resurssin valitulle yhteyshenkilölle ennen kuin alihankintarivin resurssi luodaan. |
| Käyttäjä | Voit luoda alihankintarivin resurssin valitsemalla aktiivisen käyttäjän. Käytä hakua tarkastellaksesi järjestelmässä olevia aktiivisia käyttäjiä.| Jos valitulle käyttäjälle ei ole varattavaa resurssia, järjestelmä luo varattavan resurssin valitulle käyttäjälle ennen kuin alihankintarivin resurssi luodaan. |
| Aloituspäivämäärä | Päivämäärä, jolloin alihankinnan työntekijän työtehtävä alkaa.| Jos tämä resurssi on varattu ajanjaksolle, joka on ennen tätä päivämääräväliä, siitä tulee varoitus. |
| Päättymispäivämäärä | Päivämäärä, jolloin alihankinnan työntekijän työtehtävä loppuu.| Jos tämä resurssi on varattu ajanjaksolle, joka on tämän päivämäärävälin jälkeen, siitä tulee varoitus. |
| Työmäärä | Sopimustyöntekijän tälle alihankintariville tekemien työtuntien kokonaismäärä.| Jos tälle resurssille tehty varaus ylittää tälle alihankinnalle varatun työmäärän, tulee varoitus. |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
