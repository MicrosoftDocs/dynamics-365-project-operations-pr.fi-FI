---
title: Alihankintarivin resurssit
description: Tässä aiheessa selitetään, miten määritetään erilliset resurssit, jotka toimittaja tarjoaa tietylle alihankinnan aikariville.
author: rumant
ms.date: 08/06/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 48440f82170bde7f0a0a45f8f9849d688b232949
ms.sourcegitcommit: 80aa1e8070f0cb4992ac408fc05bdffe47cee931
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/13/2021
ms.locfileid: "7323367"
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
4. Syötä **Uusi alihankintarivin välitavoite** -sivulla tarvittavat tiedot ja valitse sitten **Tallenna ja sulje**.

Seuraavassa taulukossa selitetään alihankintarivin resurssin kentät.

| Kenttä |  Kuvaus |
| ----- | ------------ |
| Varattavissa oleva resurssi | Valitse "Sopimustyöntekijä"-tyyppinen varattava resurssi, jota haluat käyttää resurssina alihankintarivillä. Jos et ole vielä luonut varattavaa resurssia sopimustyöntekijälle, jätä tämä kenttä tyhjäksi. Kun tallennat tietueen, ohjelma luo varattavan resurssin.  |
| Ota yhteyttä | Jos **Varattava resurssi** -kenttä on tyhjä, voit luoda alihankintarivin resurssin aiemmin luodusta yhteyshenkilöstä. Käytä hakua tarkastellaksesi järjestelmässä olevia aktiivisia yhteyshenkilöitä. Valitse tälle alihankinnalle toimittajan yhteyshenkilö. Yhteyshenkilö, jonka valitsit, tarkistetaan tietueen tallentamisen yhteydessä. Jos valitsemasi yhteyshenkilö ei ole kelvollinen yhteyshenkilö, tietuettasi ei tallenneta. Jos valitulle yhteyshenkilölle ei ole varattavaa resurssia, järjestelmä luo varattavan resurssin valitulle yhteyshenkilölle ennen kuin alihankintarivin resurssi luodaan. |
| Käyttäjä | Jos **Varattava resurssi** -kenttä on tyhjä, voit luoda alihankintarivin resurssin valitsemalla aktiivisen käyttäjän. Käytä hakua tarkastellaksesi järjestelmässä olevia aktiivisia käyttäjiä. Jos valitulle käyttäjälle ei ole varattavaa resurssia, järjestelmä luo varattavan resurssin valitulle käyttäjälle ennen kuin alihankintarivin resurssi luodaan. |
| Aloituspäivämäärä | Päivämäärä, jolloin alihankinnan työntekijän työtehtävä alkaa. Jos tämä resurssi on varattu ajanjaksolle, joka on ennen tätä päivämääräväliä, siitä tulee varoitus. |
| Päättymispäivämäärä | Päivämäärä, jolloin alihankinnan työntekijän työtehtävä loppuu. Jos tämä resurssi on varattu ajanjaksolle, joka on tämän päivämäärävälin jälkeen, siitä tulee varoitus. |
| Työmäärä | Työtuntien yhteismäärä, jonka alihankinnan työntekijä käyttää tällä alihankintarivillä. Jos tämä resurssi varataan tässä alihankinnassa varattua suuremmalle työmäärälle, siitä tulee varoitus. |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
