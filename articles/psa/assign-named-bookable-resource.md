---
title: Nimettyjen varattavissa olevien resurssien varaaminen projektiryhmälle ja tehtävien kohdennus
description: Tässä aiheessa on tietoja miten nimetyt resurssit varataan projektiryhmille ja miten ne kohdennetaan tehtäville.
author: JohnPBurrows
ms.custom:
- dyn365-projectservice
ms.date: 11/28/2018
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.reviewer: johnmichalak
ms.openlocfilehash: cdbcd84d2277ba1c8e68270d5b1f8ca45c17f05e
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/14/2022
ms.locfileid: "8575346"
---
# <a name="book-named-bookable-resources-to-a-project-team-and-assign-tasks"></a>Nimettyjen varattavissa olevien resurssien varaaminen projektiryhmälle ja tehtävien kohdennus 

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Voit lisätä nimetyn resurssin projektiryhmään varaamalla sen suoraan ryhmään. Toimi seuraavien vaiheiden mukaisesti.

1. Siirry Project Service Automationissa kohtaan **Projektit** ja avaa projekti, jota varten teet varausta.
2. Napsauta **Projekti**-sivun **Tyhmä**-välilehdessä **Uusi**. 

![Ryhmän jäsenen lisääminen ryhmävälilehdestä.](media/RM-how-to-1.png)

3. Valitse varattavissa oleva resurssi **Projektiryhmän jäsenen pikaluonti** -valintaikkunassa. **Rooli**-kenttä täytetään resurssin oletusroolilla, jos sillä sellainen on. Voit muuttaa roolia tarvittaessa. 
4. Valitse alkamis- ja päättymispäivä resurssin tarpeelle ja valitse resurssin kapasiteetin kohdennustapa. 
5. Jos haluat ryhmän jäsenen olevan projektin hyväksyjä, valitse **Projektin hyväksyjä** -kentässä **Kyllä**. Tämä tarkoittaa, että ryhmän jäsen voi tässä projektissa hyväksyä toimitettuja aika- ja kulumerkintöjä. 
6. Valitse **Tallenna**.

![Ryhmän jäsenen lisääminen pikaluontilomakkeessa.](media/RM-how-to-2.png)


Voit nyt kohdentaa varatun resurssin projektin tehtäville. Napsauta **Projekti** -sivulla **Aikataulut**-välilehteä kohdentaaksesi tehtäviä uudelle resurssille. Tehtäväruudukon **Resurssit**-kentästä käynnistettävä resurssinvalitsin näyttää ne ryhmän jäsenet, jotka voidaan valita.

![Ryhmän jäsenen kohdentaminen aikataulutaulukossa olevalle tehtävälle.](media/RM-how-to-3.png)

Project Service Automationin (PSA) versiossa 3 resurssivaraukset ja tehtäväkohdennukset eivät ole tiiviissä yhteydessä toisiinsa. Tämä tarkoittaa, että voit aikataulun resurssinvalitsinta käyttäessäsi kohdentaa ryhmän jäsenille tehtäviä, joiden tuntimäärä ylittää heidän varaustensa projektissa kattaman tuntimäärän.
Voit tarkastella ryhmän jäsenen varausten ja kohdennusten välisiä eroja **Ryhmä**- tai **Resurssin täsmäytys** -välilehdellä. Voit myös täsmäyttää resurssien varauksia ja kohdennuksia yksityiskohtaisemmalla tasolla.

![Resurssin täsmäytys -välilehti.](media/RM-how-to-4.png)

Voit myös käyttää **Aikataulut**-välilehden resurssinvalitsinta etsiäksesi ja valitaksesi varattavissa olevia resursseja, jotka eivät vielä kuulu projektiryhmään. Nämä näkyvät resurssinvalitsimessa nimellä **Muut resurssit**.

![Ryhmään kuulumattoman resurssin kohdentaminen tehtävälle.](media/RM-how-to-5.png)

Kun teet näin, resurssi lisätään projektiryhmään ja se kohdennetaan tehtävällä, mutta varauksia ei luoda.

![Ryhmän jäsen, jolla on kohdennuksia muttei varauksia.](media/RM-how-to-6.png)

Voit käyttää **Täsmäytys**-välilehden varauksenlaajennustoimintoa tai kohtaa **aikataulutaulukko** varataksesi resurssin kapasiteettia projektille.

![Ryhmän jäsenen varausten laajentaminen resurssin täsmäyksen välilehdessä.](media/RM-how-to-7.png)

Kun ryhmän jäsen on varattu projektillesi, voit käyttää niiden varausten hallitsemiseen varausten ylläpitoa tai aikataulutaulukkoa.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
