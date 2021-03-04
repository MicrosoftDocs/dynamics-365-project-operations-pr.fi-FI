---
title: Resurssin käytön yleiskatsaus
description: Tässä aiheessa on tietoja resurssin käytöstä Project Operationsissa.
author: ruhercul
manager: Annbe
ms.date: 11/05/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 8b85464dbb68523b122116225a604f67e7236f3e
ms.sourcegitcommit: 14aa380759214713d9bf560f5a7f619b7f4bd5b8
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/05/2020
ms.locfileid: "4401372"
---
# <a name="resource-utilization-overview"></a>Resurssin käytön yleiskatsaus

_**Koskee:** Project Operationsin resurssiin / muuhun kuin resurssiin perustuvia skenaarioita, Lite-käyttöönotto-kaupasta proformalaskutukseen_

Resursseilla voi olla tavoite laskutettavalle käytölle. Tämä tavoitekäyttö määritetään resurssin oletusroolin määritteeksi tai se määritetään yksittäisen varattavan resurssin tietueessa. Käytön laskennat perustuvat todellisiin tunteihin, jotka resurssit ovat raportoineet hyväksyttyjen aikakirjausten kautta.

Käytön laskennassa käytetään seuraavia kaavoja:

  - Lakutettava käyttö = Laskutettavat todelliset tunnit ÷ Resurssin kapasiteetti
  - Ei-laskutettava käyttö = Todellinen aika, jonka laskutustyyppi ID = Ei-laskutettava, Täydentävä tai Ei käytettävissä ÷ Resurssin kapasiteetti
  - Sisäinen = Todellinen aika ilman myyntisopimusta ÷ Resurssin kapasiteetti
  - Resurssin kapasiteetti = Resurssin työtunnit – Poissa toimistosta – Muut kuin työpäivät

**Resurssien käyttöaste** -näkymä on **Resurssit**-ruudussa.

Kukin ruudukon solu kuvaa resurssin laskutettavaa käyttöprosenttia kauden, esimerkiksi päivän, viikon tai kuukauden, aikana. Solujen värittämiseen käytetään seuraavia kaavoja:

  - **Vihreä**: laskutettava käyttö > = resurssin tavoitekäyttö
  - **Keltainen**: tavoitekäyttö - 20 <= laskutettava käyttö < tavoitekäyttö
  - **Punainen**: laskutettava käyttö < tavoitekäyttö - 20

Koska **Resurssien käyttöaste** -näkymä perustuu aikataulutaulutaulukkoon, voit suodattaa tuloksia käyttämällä aikataulutaulukon suodatustoimintoja.

Ruudukko edellyttää, että määrität kohteen käytön joko roolille tai yksittäiselle resurssille. Tämä määritys tehdään valitsemalla **Resurssit** > **Resurssiroolit**.

Lisäksi jokaiselle varattavissa olevalle resurssille on määritettävä oletusrooli. Valitse **Resurssit** > **Resurssit**. Varmista **Project Service** -välilehdessä, että resurssin rooli on määritetty ja että **Onko oletus** -kentän arvo on **Kyllä**. Voit lisätä muita rooleja, joiden **Onko oletus** = **Ei**. Roolia, jossa **Onko oletus** = **Kyllä** käytetään määrittämään resurssin käyttöaste tavoitteen mukaisesti.

**Project Service** -välilehdellä voit myös määrittää yksittäisen tavoitekäytön resurssille. Käytön laskenta käyttää sen jälkeen tätä tavoitekäyttöastetta määrittääkseen resurssin tavoitteen resurssin oletusroolin tavoitteen asemesta.

Resurssin käyttöaste näytetään ainoastaan, jos resurssilla on hyväksyttyä laskutettavaa aikaa sen jakson aikana, joka näkyy ruudukossa.


[!INCLUDE[footer-include](../includes/footer-banner.md)]