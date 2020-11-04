---
title: Projektin päivittäminen
description: Tässä aiheessa on tietoja projektien päivittämisestä Project Operationsissa.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 5c9cd0c7c6886bd454c5f2ef2ae7f20d1707293f
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/16/2020
ms.locfileid: "4075203"
---
# <a name="update-a-project"></a>Projektin päivittäminen

_**Koskee:** Project Operationsin resurssiin / muuhun kuin resurssiin perustuvia skenaarioita, Lite-käyttöönotto-kaupasta proformalaskutukseen_

Alla on yhteenveto kentistä, jotka voidaan päivittää projektiin sen jälkeen, kun se on luotu, sekä mahdolliset päivitysten vaikutukset.

## <a name="project-detail-fields"></a>Projektin tietokentät

- **Nimi** : Projektin otsikko.
- **Kuvaus** : Projektin yleiskuvaus.
- **Asiakas** : Yritys, jolle projekti toimitetaan.
- **Kalenterimalli** : Projektin työtunnit. Kun tätä kenttää muutetaan, koko aikataulu lasketaan uudelleen.
- **Valuutta** : Projektin valuutta. Tämä kentän oletusarvo on valuutta, joka on määritetty sopimusyksikössä. Kun sopimusyksikkö päivitetään, myös tämä kenttä päivittyy.
- **Sopimusyksikkö** : Organisaatioyksikkö, joka edustaa sitä yrityksen ryhmää tai osastoa, joka on pääasiallisesti vastuussa myynnin parantamisesta ja työn ja palvelujen asiakkaalle toimittamisen hallinnasta. 
- **Projektipäällikkö** : Projektiryhmän jäsen, jolla on valtuudet tarkastella ja hyväksyä aikamerkintöjä ja kuluja.

## <a name="estimate-fields"></a>Arviokentät

- **Arvioitu alkamispäivä** : Päivämäärä, jolloin projekti alkaa. Kun tämä kenttä päivitetään, kaikki projektin tehtävät siirtyvät suhteessa uuteen alkamispäivään.
- **Päättymispäivä** : Päivä määrä, jona projekti on aikataulutettu päättymään.
- **Työmäärä** : Projektin arvioitu työmäärä. Kun projektiin lisätään tehtäviä, tätä kenttää ei enää voi muokata.
- **Arvioitu työvoimakustannus** : Projektin arvioitu työvoimakustannus. Kun projektiin lisätään työnvoimakustannuksia, tätä kenttää ei enää voi muokata.
- **Arvioidut kulut** : Projektin arvioidut kulut. Kun projektiin lisätään kuluja, tätä kenttää ei enää voi muokata.

## <a name="project-actual-fields"></a>Projektin toteutuneiden arvojen kentät
- **Todellinen aloituspäivämäärä** : Päivämäärä, jolloin projekti alkoi.
- **Todellinen päättymispäivä** : Päivitetään, kun projekti on valmis.

## <a name="project-status-fields"></a>Projektin tilakentät

- **Projektin yleinen tila** : Projektipäällikön määrittämä projektin kunto.
- **Kommentit** : Projektipäällikön kirjoittama kuvaus projektin nykyisestä kunnosta.

