---
title: Luo resurssien delegoinnit
description: Tässä aiheessa on tietoja yleisten ja nimettyjen resurssien delegointien luomisesta.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 20eb3880b17fb1f765ad79bd720520b0c8004c0a
ms.sourcegitcommit: a0f80d024a5d3112a39781815bd31d0c05ddaf6f
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/30/2020
ms.locfileid: "3906141"
---
# <a name="create-resource-assignments"></a>Luo resurssien delegoinnit

_**Koskee:** Project Operationsin resurssiin / muuhun kuin resurssiin perustuvia skenaarioita, Lite-käyttöönotto-kaupasta proformalaskutukseen_


Resurssin delegointi on suora yhteys projektitiimin jäsenestä lehtisolmutehtävään. Tässä aiheessa on tietoja eri tavoista delegoida resursseja.

## <a name="create-a-generic-team-member-through-task-assignment"></a>Yleisen ryhmän jäsenen luominen tehtäväkohdennuksen kautta


Kun luot yleisen ryhmän jäsenen tehtävän delegoinnin avulla, luot paikkamerkin tai yleisen resurssin. Tämä yleinen resurssi kuvaa sen nimetyn resurssin ominaisuudet, jonka haluat suorittavan tehtävät. Tämän jälkeen voit luoda tarpeen (tai lähettää pyynnön käyttämällä tarvetta), jota käytetään nimetyn resurssin haussa ja varauksessa.

1. Valitse tehtävän Aikataulut-ruudukossa Resurssi-kuvake **Resurssi**-solussa.
2. Kirjoita nimi, joka toimii resurssin nimen paikkamerkkinä. Esimerkiksi ohjelmapäällikkö.
3. Valitse **Luo** ja määritä yleisen resurssin rooli kentässä **Projektiryhmän jäsenen pikaluonti**.
4. Delegoi tarpeen mukaan tehtäviä tälle paikkamerkkiresurssille valitsemalla tehtävälle resurssi **Resurssinvalitsin**-kohdasta. Resurssit löytyvät **Ryhmän jäsenet** -kohdasta.
5. Kun olet kohdentanut yleisen resurssin, valitse se **Ryhmä**-välilehdessä, valitse yleinen resurssi ja valitse sitten **Luo tarve** luodaksesi resurssitarpeen yleiselle resurssille.
6. Valitse yleisen resurssin **Varaa**-kohta. Tämän jälkeen voit etsiä todellisen resurssin ja varata sen aikataulutaulukon avulla. Voit myös lähettää tarpeen resurssipäällikön tekemälle toteutukselle.
7. Kun yleinen resurssi on kokonaan täytetty (osittainen resurssitarpeen täyttäminen ei johda resurssin delegointiin) nimetyn resurssin kanssa, yleinen resurssi poistetaan ryhmästä. Yleisen resurssin tehtävien delegoinnit delegoidaan nimetylle resurssille, joka täytti yleisen resurssin resurssitarpeen.

## <a name="assign-a-named-resource-from-the-list-of-all-bookable-resources"></a>Nimetyn resurssin kohdentaminen kaikkien varattavissa olevien resurssien luettelosta

**Resurssinvalitsin**-kohdan hakuruudun avulla voit hakea kaikki aktiiviset varattavissa olevat resurssit ja kohdentaa ne mille tahansa lehtisolmutehtävälle. Tällä tavoin kohdennetut resurssit lisätään ryhmään ilman varauksia. tämä vastaa ryhmän jäsenen lisäämistä ja **Ei mitään** -kohdennusmenetelmän valitsemista. Resurssi näkyy **Ryhmä**, **Resurssin delegointi**- ja **Täsmäytys**-välilehdessä resurssina, jolla on vain delegointeja ja varausvaje. Varaa ne, jos haluat käyttää niitä.

1. Siirry tehtävän ruudukkoon, taulukoon tai aikajanaan ja soluun **Vastuuhenkilö**.
2. Ala kirjoittaa nimeä hakuruutuun. Nimen hakutulokset näkyvät **Muut resurssit**-kohdan kohdassa **Resurssinvalitsin**.
3. Valitse resurssi, jonka haluat delegoida tehtävälle, tai valitse resurssin nimi kohdassa **Muut ryhmän resurssit**.
