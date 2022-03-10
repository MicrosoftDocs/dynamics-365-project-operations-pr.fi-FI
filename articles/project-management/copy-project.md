---
title: Projektin kopioiminen
description: Tässä aiheessa on tietoja projektien kopioimisesta Dynamics 365 Project Operationsissa.
author: ruhercul
ms.date: 05/21/2021
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: fe76f59b315fd0f46b25e1d116acde1f6b2864d1753e01d6311ea93ae7d116fc
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/06/2021
ms.locfileid: "7007187"
---
# <a name="copy-a-project"></a>Projektin kopioiminen

_**Koskee:** Project Operationsin resurssiin / muuhun kuin resurssiin perustuvia skenaarioita, Lite-käyttöönotto-kaupasta proformalaskutukseen_

Dynamics 365 Project Operationsin avulla voit nopeasti luoda uusia projekteja valitsemalla **Projektit**-lomakkeessa **Kopioi projekti**. Jos haluat kopioida projektin, avaa kopioitava projekti ja valitse sitten **Kopioi projekti**. Toiminto kopioi seuraavat tiedot:

- Projektin ominaisuudet 
- Työrakenne
- Projektiryhmän jäsenet
- Projektin arviot
- Projektin kuluarviot
- Projektin materiaaliarviot

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
- Arvioitu aloituspäivä: Tämä on päivämäärä, jolloin projekti luodaan kopiosta.
- Arvioitu päättymispäivä: Tätä päivämäärää säädetään kopiosta luodun uuden projektin aloituspäivän perusteella.
- Työmäärä (tuntia)
- Arvioidut työvoimakustannukset
- Arvioidut kulujen kustannukset
- Arvioidut materiaalikustannukset

> [!NOTE]
> Projektin kopiointi on pitkäkestoinen toiminto. Myös projektitietueet, niihin liittyvät määritteet ja monet asiaan liittyvät entiteetit kopioidaan. Koska toiminto on pitkäkestoinen, kohdeprojektin sivu lukitaan kopioinnin alkamisen jälkeen muokkausten estämiseksi, kunnes kopiointitoiminto on valmis.

## <a name="work-breakdown-structure"></a>Työrakenne

Kun projekti kopioidaan, koko resursseillä täytetty työrakenne kopioidaan. Nimetyt resurssit korvataan yleisillä resursseilla. Jos nimettyjen resurssien työaika ei ole sama kuin yleisellä resurssilla, aikataulu lasketaan uudelleen ja tehtävien kestot voivat muuttua.

## <a name="project-team-members"></a>Projektiryhmän jäsenet

Kun projektiryhmä kopioidaan lähdeprojektista, yleiset resurssit kopioidaan. Yleisten resurssien kohdennukset myös säilytetään sellaisina, kuin ne olivat lähdeprojektissa. Nimetyt resurssit muunnetaan yleisiksi ryhmän jäseniksi.

## <a name="estimates"></a>Arviot

Kun projekti kopioidaan, resurssien, kulujen ja materiaaliarvioiden rivit kopioidaan lähdeprojektista. 

Lisätietoja projektin kopioinnin ohjelmallisesta käyttämisestä on ohjeaiheessa [Projektimallien kehittäminen projektin kopioinnin avulla](dev-copy-project.md).


[!INCLUDE[footer-include](../includes/footer-banner.md)]
