---
title: Projektin kopioiminen
description: Tässä aiheessa on tietoja projektien kopioinnista Dynamics 365 Project Operationsissa.
author: ruhercul
manager: AnnBe
ms.date: 10/07/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: cf80f2a1cd27aae33d123e45dee70d94ea4d01a9
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/16/2020
ms.locfileid: "4075289"
---
# <a name="copy-a-project"></a>Projektin kopioiminen

_**Koskee:** Project Operationsin resurssiin / muuhun kuin resurssiin perustuvia skenaarioita, Lite-käyttöönotto-kaupasta proformalaskutukseen_

Dynamics 365 Project Operationsissa voit luoda nopeasti uusia projekteja valitsemalla **Kopioi projekti** **Projektit** -lomakkeessa. Jos haluat kopioida projektin, avaa kopioitava projekti ja valitse sitten **Kopioi projekti**. Toiminto kopioi:

- Projektin ominaisuudet
- Työrakenne
- Projektiryhmän jäsenet
- Projektin arviot
- Projektin kuluarviot

## <a name="project-properties"></a>Projektin ominaisuudet

Kun projekti kopioidaan, seuraavien kenttien arvot kopioidaan:

- Nimi
- Kuvaus
- Asiakas
- Kalenterimalli
- Valuutta
- Sopimusyksikkö
- Projektipäällikkö
- Tila
- Koko projektin tila
- Kommentit
- Arviot
- Arvioitu aloituspäivä
- Lopetuspäivä
- Työmäärä (tuntia)
- Arvioidut työvoimakustannukset
- Arvioidut kulujen kustannukset

## <a name="work-breakdown-structure"></a>Työrakenne

Kun projekti kopioidaan, koko resursseillä täytetty työrakenne kopioidaan. Nimetyt resurssit korvataan yleisillä resursseilla. Jos nimettyjen resurssien työaika ei ole sama kuin yleisellä resurssilla, aikataulu lasketaan uudelleen ja tehtävien kestot voivat muuttua.

## <a name="project-team-members"></a>Projektiryhmän jäsenet

Kun projektiryhmä kopioidaan lähdeprojektista, yleiset resurssit kopioidaan. Yleisten resurssien kohdennukset myös säilytetään sellaisina, kuin ne olivat lähdeprojektissa. Nimetyt resurssit muunnetaan yleisiksi ryhmän jäseniksi.

## <a name="estimates"></a>Arviot

Kun projekti kopioidaan, sekä resurssin että kulun arviorivit kopioidaan lähdeprojektista. 

Lisätietoja projektin kopioinnin ohjelmallisesta käyttämisestä on ohjeaiheessa [Projektimallien kehittäminen projektin kopioinnin avulla](dev-copy-project.md).
