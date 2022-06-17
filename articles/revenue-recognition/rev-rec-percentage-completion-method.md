---
title: Kiinteähintaisen tuoton arviointiprojektit
description: Tässä artikkelissa on tietoja kiinteähintaisesta tuotosta projekteissa.
author: sigitac
ms.date: 11/16/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 3febb22397faa31222015231481d43fb0449d0a2
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8928382"
---
# <a name="fixed-price-revenue-estimate-projects"></a>Kiinteähintaisen tuoton arviointiprojektit 

_**Käytetään:** Project Operationsin resursseihin ja ei-varastoitaviin perustuvissa skenaarioissa_

Kun luot projektisopimusrivin, jolla on seuraavat määritteet Dynamics 365 Project Operationsin Microsoft Dataversessä, järjestelmä luo automaattisesti kiinteähintaisen tuoton arviointiprojektin. Tämän projektin tiedot perustuvat seuraaviin:

  - Kiinteän hinnan laskutusmenetelmä.
  - Liittyvä projekti.
  - Vähintään yksi välitavoite, joka on määritetty **Laskutusaikataulu**-välilehdellä **Projektisopimuksen rivi** -sivulla.

## <a name="review-fixed-price-revenue-estimates-projects"></a>Kiinteähintaisen tuoton arviointiprojektien tarkastelu
Voit tarkastella kiinteähintaisen tuoton arviointiprojekteja suorittamalla seuraavat vaiheet:

1. Siirry Dynamics 365 Finance -ympäristössä kohtaan **Projektinhallinta ja kirjanpito** > **Projektit** > **Kiinteähintaisen arvioidun myyntituoton projektit**.
2. Valitse tarkasteltava projekti ja kaksoisnapsauta **Arviointiprojektin tunnusta** avataksesi tietueen ja tarkastellaksesi projektin tietoja.
3. Laajenna **Projekti**-välilehti. **Valitut projektit** -ruudukossa näkyy yksi projekti. Järjestelmä käyttää tätä oletusprojektina, koska se on projektisopimuksen riviin liittyvä projekti. 
4. Jos haluat muuttaa kytkentää, valitse lisää projekteja ja lisää ne **Valitut projektit**-ruudukkoon. Jos ruudukossa valitaan useita projekteja, projektin valmistumisprosentti- ja tuottoarviot lasketaan yhteen kaikista valituista projekteista.

  Projektikustannukset, tuottoprofiili, kustannusmalli ja kausikoodi voidaan määrittää manuaalisesti. Jos niitä ei ole määritetty manuaalisesti, arvot ovat oletusarvoja, jotka on saatu ensimmäisen arvion laskemisen aikana projektista käyttäen sääntöjä, jotka on määritetty projektin kustannus- ja tuottoprofiileille.



[!INCLUDE[footer-include](../includes/footer-banner.md)]