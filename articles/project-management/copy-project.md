---
title: Projektin kopioiminen
description: Tässä aiheessa on tietoja projektien kopioimisesta Dynamics 365 Project Operationsissa.
author: ruhercul
ms.date: 03/07/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: e9b637d2d282d123dfacb8a295292ea06549aa1e
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/14/2022
ms.locfileid: "8574426"
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
- Projektin tarkistusluettelot
- Projektin joukot

## <a name="project-properties"></a>Projektin ominaisuudet

Kun projekti kopioidaan, seuraavien kenttien arvot kopioidaan.

| Field | Project Operations ei-varastoitaville materiaaleille | Project Operations Lite | Project for the Web |
|-------|------------------------------------------|-------------------------|---------------------|
| Name | :heavy_check_mark: | :heavy_check_mark: | :heavy_check_mark: |
| Description | :heavy_check_mark: | :heavy_check_mark: | |
| asiakas | :heavy_check_mark: | :heavy_check_mark: | |
| Kalenterimalli | :heavy_check_mark: | :heavy_check_mark: | :heavy_check_mark: |
| Valuutta | :heavy_check_mark: | :heavy_check_mark: | |
| Sopimusyksikkö | :heavy_check_mark: | :heavy_check_mark: | |
| Omistava yritys | :heavy_check_mark: | | |
| Projektipäällikkö | :heavy_check_mark: | :heavy_check_mark: | :heavy_check_mark: |
| Status | :heavy_check_mark: | :heavy_check_mark: | |
| Koko projektin tila | :heavy_check_mark: | :heavy_check_mark: | |
| Kommentit | :heavy_check_mark: | :heavy_check_mark: | |
| Arviot | :heavy_check_mark: | :heavy_check_mark: | |
| <p>Arvioitu aloituspäivä</p><p><strong>Huomautus:</strong> Tämä kenttä määrittää päivämäärän, jolloin projekti luodaan kopiosta. | :heavy_check_mark: | :heavy_check_mark: | |
| <p>Arvioitu päättymispäivä</p><p><strong>Huomautus:</strong> Tämän kentän päivämäärää muutetaan kopiosta tehdyn uuden projektin aloituspäivän perusteella.</p> | :heavy_check_mark: | :heavy_check_mark: | |
| Työmäärä (tuntia) | :heavy_check_mark: | :heavy_check_mark: | |
| Arvioidut työvoimakustannukset | :heavy_check_mark: | :heavy_check_mark: | |
| Arvioidut kulujen kustannukset | :heavy_check_mark: | :heavy_check_mark: | |
| Arvioidut materiaalikustannukset | | :heavy_check_mark: | |

> [!NOTE]
> Projektin kopiointi on pitkäkestoinen toiminto. Myös projektitietueet, niihin liittyvät määritteet ja monet asiaan liittyvät entiteetit kopioidaan. Koska toiminto on pitkäkestoinen, kohdeprojektin sivu lukitaan kopioinnin alkamisen jälkeen muokkausten estämiseksi, kunnes kopiointitoiminto on valmis.

## <a name="work-breakdown-structure"></a>Työrakenne

Kun projekti kopioidaan, koko resursseillä täytetty työrakenne kopioidaan. Nimetyt resurssit korvataan yleisillä resursseilla. Jos nimetyillä resursseilla ei ole samaa työaikaa kuin yleisellä resurssilla, aikataulu lasketaan uudelleen ja tehtävien kestot voivat muuttua.

## <a name="project-team-members"></a>Projektiryhmän jäsenet

Kun projektiryhmä kopioidaan lähdeprojektista, yleiset resurssit kopioidaan. Yleisten resurssien kohdennukset myös säilytetään sellaisina, kuin ne olivat lähdeprojektissa. Nimetyt resurssit muunnetaan yleisiksi ryhmän jäseniksi.

> [!NOTE]
> Ryhmän jäseniä ja tehtäviä ei kopioida Project for the Webissä.

## <a name="estimates"></a>Arviot

Kun projekti kopioidaan, resurssien, kulujen ja materiaaliarvioiden rivit kopioidaan lähdeprojektista. 

Lisätietoja projektin kopioinnin ohjelmallisesta käyttämisestä on ohjeaiheessa [Projektimallien kehittäminen projektin kopioinnin avulla](dev-copy-project.md).

## <a name="quotes-and-contracts"></a>Tarjoukset ja sopimukset

Tarjouksia ja palvelusopimuksia ei linkitetä kohdeprojektiin.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
