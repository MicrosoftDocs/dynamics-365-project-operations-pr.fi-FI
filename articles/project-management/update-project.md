---
title: Projektin luominen ja päivittäminen
description: Tässä aiheessa on tietoja projektien päivittämisestä Project Operationsissa.
author: ruhercul
ms.date: 10/20/2021
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: d0847b5343cf3e353b91eae04c94509f14213ba5
ms.sourcegitcommit: 51224cb3bf7cdeae6614d39fc8d899c83dbad5f2
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/23/2021
ms.locfileid: "7678345"
---
# <a name="create-and-update-a-project"></a>Projektin luominen ja päivittäminen

_**Koskee:** Project Operationsin resurssiin / muuhun kuin resurssiin perustuvia skenaarioita, Lite-käyttöönotto-kaupasta proformalaskutukseen_

Seuraavassa on yhteenveto kentistä, jotka voidaan päivittää projektissa sen luomisen jälkeen. Tähän sisältyvät myös näihin päivityksiin liittyvät vaikutukset.

## <a name="project-detail-fields"></a>Projektin tietokentät

- **Nimi**: Projektin otsikko.
- **Kuvaus**: Projektin yleiskuvaus.
- **Asiakas**: Yritys, jolle projekti toimitetaan.
- **Kalenterimalli**: Projektin työtunnit. Kun tätä kenttää muutetaan, koko aikataulu lasketaan uudelleen.
- **Valuutta**: Projektin valuutta. Tämän kentän oletusarvo perustuu palvelusopimuksessa määritettyyn valuuttaan. Kun sopimusyksikkö päivitetään, myös tämä kenttä päivittyy.
- **Sopimusyksikkö**: Organisaatioyksikkö, joka edustaa sitä yrityksen ryhmää tai osastoa, joka on pääasiallisesti vastuussa myynnin parantamisesta ja työn ja palvelujen asiakkaalle toimittamisen hallinnasta.  Kun projektipäällikön organisaatioyksikköä ei ole määritetty, tämän kentän oletusarvo on projektin parametreissa määritetty arvo.
- **Projektipäällikkö**: Projektiryhmän jäsen, jolla on valtuudet tarkastella ja hyväksyä aikamerkintöjä ja kuluja.

## <a name="estimate-fields"></a>Arviokentät

- **Arvioitu alkamispäivä**: Päivämäärä, jolloin projekti alkaa. Kun tämä kenttä päivitetään, kaikki projektin tehtävät siirtyvät suhteessa uuteen alkamispäivään.
- **Päättymispäivä**: Päivä määrä, jona projekti on aikataulutettu päättymään.
- **Työmäärä**: Projektin arvioitu työmäärä. Kun projektiin lisätään tehtäviä, tätä kenttää ei enää voi muokata.
- **Arvioitu työvoimakustannus**: Projektin arvioitu työvoimakustannus. Kun projektiin lisätään työnvoimakustannuksia, tätä kenttää ei enää voi muokata.
- **Arvioidut kulut**: Projektin arvioidut kulut. Kun projektiin lisätään kuluja, tätä kenttää ei enää voi muokata.

## <a name="project-actual-fields"></a>Projektin toteutuneiden arvojen kentät
- **Todellinen aloituspäivämäärä**: Päivämäärä, jolloin projekti alkoi.
- **Todellinen päättymispäivä**: Päivitetään, kun projekti on valmis.

## <a name="project-status-fields"></a>Projektin tilakentät

- **Projektin yleinen tila**: Projektipäällikön määrittämä projektin kunto.
- **Kommentit**: Projektipäällikön kirjoittama kuvaus projektin nykyisestä kunnosta.



[!INCLUDE[footer-include](../includes/footer-banner.md)]
