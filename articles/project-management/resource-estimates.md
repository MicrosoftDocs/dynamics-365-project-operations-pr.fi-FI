---
title: Resurssiarviot
description: Tässä aiheessa on tietoja siitä, miten resurssiarviot lasketaan Project Operationsissa.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 2ebde2b3c5bcfb5faa02ee476065ac34b1953432
ms.sourcegitcommit: f255b2cbf290973ce62fe2c1c121bd1df15a7392
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/01/2020
ms.locfileid: "3928560"
---
# <a name="resource-estimates"></a>Resurssiarviot

_**Koskee:** Project Operationsin resurssiin / muuhun kuin resurssiin perustuvia skenaarioita, Lite-käyttöönotto-kaupasta proformalaskutukseen_

Resurssiarviot tulevat työrakenteessa määritetystä aikajaksotetusta työmäärästä, johon sisältyvät sovellettavat hinnoitteludimensiot. Yleensä laskenta on **hinta/tunti kullekin roolille x tuntia** Kunkin resurssin aikajaksotettu työmäärä tallennetaan resurssin delegointitietueeseen. Hinnoittelu on tallennetaan ennalta määritettyyn hinnastoon. Yksikkömuunnosta käytetään sovellettavan hinnaston perusteella.

![Resurssiarviot](./media/navigation12.png)

## <a name="default-cost-price-and-cost-currency"></a>Kustannushinnan ja kustannusvaluutan oletusarvot

Kustannushinnat määritetään oletusarvona organisaatioyksiköstä.

## <a name="default-bill-rate-and-sales-currency"></a>Laskutushinnan ja myyntivaluutan oletusarvot

Myyntihintoja käytetään kerran sopimusta kohden. Myyntihinnaston hierarkian oletusarvo on seuraava:

1. Organisaatio
2. Asiakas
3. Tarjous/sopimus
