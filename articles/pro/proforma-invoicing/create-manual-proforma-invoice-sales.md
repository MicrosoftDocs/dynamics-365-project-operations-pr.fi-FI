---
title: Manuaalisen proformalaskun luominen – lite
description: Tämä aihe tarjoaa tietoja Project Operationsin manuaalisen proformalaskun luomisesta.
author: rumant
manager: Annbe
ms.date: 10/19/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 87ef090454b2a7ab997e7c21d8d10badc31c8235
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/30/2020
ms.locfileid: "4176382"
---
# <a name="create-a-manual-proforma-invoice---lite"></a>Manuaalisen proformalaskun luominen – lite

_**Käytetään:** Lite-käyttöönotto – kauppa proformalaskutukseen_

Dynamics 365 Project Operationsissa voidaan luoda proformalaskuja manuaalisesti tarpeen mukaan. Voit luoda proformalaskun manuaalisesti **Projektisopimuksen** luettelosivulta tai **Projektisopimuksen** tiedot-sivulta.

##  <a name="project-contracts-list-page"></a>Projektisopimusten luettelosivu

Valitse **projektisopimusten** luettelosivulta vähintään yksi projektisopimus ja luo laskut kaikille valituille tietueille.

Järjestelmä tarkistaa, mikä valituista projektisopimuksista on **valmis laskutukseen**, joka on päivätty ennen kuluvan päivän päivämäärää. Näistä palvelusopimuksista järjestelmä luo luonnokset proformalaskuiksi. Jos projektisopimuksessa on useita asiakkaita, asiakasta kohden voi olla yksi lasku ja useita laskuja projektisopimusta kohden.

Kaikki luodut projektilaskut ovat käytettävissä **Myynti**-alueen **laskutus**-osan **lasku**-sivulla.

## <a name="project-contract-details-page"></a>Projektisopimuksen tiedot-sivu

Proformalasku voidaan luoda myös **Projekti sopimuksen** tiedot-sivulla, joka luo laskun kyseisestä projektisopimuksesta. Järjestelmä varmistaa, että projektisopimuksella on **valmis laskutukseen** -varaus, joka on päivätty ennen kuluvan päivän päivämäärää. Näistä palvelusopimuksista järjestelmä luo proformalaskujen luonnokset kunkin sopimusrivin asiakkaiden määrän perusteella.

Kun luodaan yksittäinen proformalasku, näkyviin tulee **lasku**-sivu. Jos kyseiselle projektisopimukselle on luotu useita laskuja, näkyviin tulee **laskut**-luettelosivu, jossa näkyvät kaikki luodut laskut.
