---
title: Projektin kopioiminen
description: Tässä aiheessa on tietoja projektien kopioimisesta Dynamics 365 Project Operationsissa.
author: ruhercul
manager: AnnBe
ms.date: 02/22/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: af1942e81691d9e13fdcbbf68599c1a8a4004582
ms.sourcegitcommit: 24528bb9c0ef8898077cb3bc672daa211c0e73aa
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/04/2021
ms.locfileid: "5479515"
---
# <a name="copy-a-project"></a>Projektin kopioiminen

_**Koskee:** Project Operationsin resurssiin / muuhun kuin resurssiin perustuvia skenaarioita, Lite-käyttöönotto-kaupasta proformalaskutukseen_

Dynamics 365 Project Operationsin avulla voit nopeasti luoda uusia projekteja valitsemalla **Projektit**-lomakkeessa **Kopioi projekti**. Jos haluat kopioida projektin, avaa kopioitava projekti ja valitse sitten **Kopioi projekti**. Toiminto kopioi:

- Projektin ominaisuudet (arvioitu alkamispäivä kopioidaan lähdeprojektista)
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


[!INCLUDE[footer-include](../includes/footer-banner.md)]
