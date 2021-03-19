---
title: Kiinteähintaisen tuoton arviointiprojektit
description: Tässä aiheessa on tietoja kiinteähintaisesta tuotosta projekteissa.
author: sigitac
manager: Annbe
ms.date: 11/16/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 7cf4d7853f7fedaeeeba99bc589f39989b924423
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5278909"
---
# <a name="fixed-price-revenue-estimate-projects"></a>Kiinteähintaisen tuoton arviointiprojektit 

_**Käytetään:** Project Operationsin resursseihin ja ei-varastoitaviin perustuvissa skenaarioissa_

Kun luot projektisopimusrivin, jolla on seuraavat määritteet Dynamics 365 Project Operationsin Microsoft Dataversessä, järjestelmä luo automaattisesti kiinteähintaisen tuoton arviointiprojektin. Tämän projektin tiedot perustuvat seuraaviin:

  - Kiinteän hinnan laskutusmenetelmä.
  - Liittyvä projekti.
  - Vähintään yksi välitavoite, joka on määritetty **Laskutusaikataulu**-välilehdellä **Projektisopimuksen rivi** -sivulla.

## <a name="review-fixed-price-revenue-estimates-projects"></a>Kiinteähintaisen tuoton arviointiprojektien tarkastelu
Voit tarkastella kiinteähintaisen tuoton arviointiprojekteja suorittamalla seuraavat vaiheet:

1. Siirry Dynamics 365 Finance -ympäristössä kohtaan **Projektinhallinta ja kirjanpito** > **Projektit** > **Kiinteähintaisen tuoton arviointiprojektit**.
2. Valitse tarkasteltava projekti ja kaksoisnapsauta **Arviointiprojektin tunnusta** avataksesi tietueen ja tarkastellaksesi projektin tietoja.
3. Laajenna **Projekti**-välilehti. **Valitut projektit** -ruudukossa näkyy yksi projekti. Järjestelmä käyttää tätä oletusprojektina, koska se on projektisopimuksen riviin liittyvä projekti. 
4. Jos haluat muuttaa kytkentää, valitse lisää projekteja ja lisää ne **Valitut projektit**-ruudukkoon. Jos ruudukossa valitaan useita projekteja, projektin valmistumisprosentti- ja tuottoarviot lasketaan yhteen kaikista valituista projekteista.

  Projektikustannukset, tuottoprofiili, kustannusmalli ja kausikoodi voidaan määrittää manuaalisesti. Jos niitä ei ole määritetty manuaalisesti, arvot ovat oletusarvoja, jotka on saatu ensimmäisen arvion laskemisen aikana projektista käyttäen sääntöjä, jotka on määritetty projektin kustannus- ja tuottoprofiileille.



[!INCLUDE[footer-include](../includes/footer-banner.md)]