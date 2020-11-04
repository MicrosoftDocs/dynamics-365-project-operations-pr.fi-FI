---
title: Manuaalisen proformalaskun luominen
description: Tämä aihe tarjoaa tietoja Project Operationsin manuaalisen proformalaskun luomisesta.
author: rumant
manager: Annbe
ms.date: 10/19/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: d5e93206737507bf6698a9746815c790d3dfc904
ms.sourcegitcommit: 3a0c18823a7ad23df5aa3de272779313abe56c82
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/20/2020
ms.locfileid: "4075577"
---
# <a name="creating-a-manual-proforma-invoice"></a>Manuaalisen proformalaskun luominen

_**Käytetään:** Lite-käyttöönotto – kauppa proformalaskutukseen_

Dynamics 365 Project Operationsissa voidaan luoda proformalaskuja manuaalisesti tarpeen mukaan. Voit luoda proformalaskun manuaalisesti **Projektisopimuksen** luettelosivulta tai **Projektisopimuksen** tiedot-sivulta.

##  <a name="project-contracts-list-page"></a>Projektisopimusten luettelosivu

Valitse **projektisopimusten** luettelosivulta vähintään yksi projektisopimus ja luo laskut kaikille valituille tietueille.

Järjestelmä tarkistaa, mikä valituista projektisopimuksista on **valmis laskutukseen** , joka on päivätty ennen kuluvan päivän päivämäärää. Näistä palvelusopimuksista järjestelmä luo luonnokset proformalaskuiksi. Jos projektisopimuksessa on useita asiakkaita, asiakasta kohden voi olla yksi lasku ja useita laskuja projektisopimusta kohden.

Kaikki luodut projektilaskut ovat käytettävissä **Myynti** -alueen **laskutus** -osan **lasku** -sivulla.

## <a name="project-contract-details-page"></a>Projektisopimuksen tiedot-sivu

Proformalasku voidaan luoda myös **Projekti sopimuksen** tiedot-sivulla, joka luo laskun kyseisestä projektisopimuksesta. Järjestelmä varmistaa, että projektisopimuksella on **valmis laskutukseen** -varaus, joka on päivätty ennen kuluvan päivän päivämäärää. Näistä palvelusopimuksista järjestelmä luo proformalaskujen luonnokset kunkin sopimusrivin asiakkaiden määrän perusteella.

Kun luodaan yksittäinen proformalasku, näkyviin tulee **lasku** -sivu. Jos kyseiselle projektisopimukselle on luotu useita laskuja, näkyviin tulee **laskut** -luettelosivu, jossa näkyvät kaikki luodut laskut.
