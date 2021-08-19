---
title: Alihankinnan keskeiset käsitteet
description: Tässä aiheessa on joitakin tärkeitä käsitteitä, joita sovelletaan Microsoft Dynamics 365 Project Operationsin alihankintasopimuksiin.
author: rumant
ms.date: 08/03/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 01d2e57b99015c346be15e3504440c14cb9a54e24215c0b1c052c5112f4b940a
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/06/2021
ms.locfileid: "6994272"
---
# <a name="key-concepts-in-subcontracting"></a>Alihankinnan keskeiset käsitteet

[!include [banner](../../includes/dataverse-preview.md)]

_**Käytetään:** Lite-käyttöönotto – kauppa proformalaskutukseen_

Seuraavassa aiheessa on joitakin tärkeitä käsitteitä, jotka on syytä tietää, ennen kuin alat käyttää Microsofti Dynamics 365 Project Operationsin alihankkijatoimintoja.

## <a name="contracting-unit-on-the-subcontract"></a>Alihankkijan sopimusyksikkö

Sopimusyksikkö edustaa osastoa tai käytäntöä, joka omistaa mahdollisen projektin toimituksen. Sopimusyksikkö on myös jako, joka tulee sopimussuhteeseen myyjän kanssa.

## <a name="purchase-currency"></a>Ostovaluutta

Project Operationsissa ostovaluutta on valuutta, jossa alihankkija luodaan. Se on myös valuutta, jossa projektin alihankkijakustannukset kirjataan. Ostovaluutta voi erota projektivaluutasta, ja projektin valuutta voi puolestaan olla erilainen kuin myyntivaluutta.

## <a name="billing-methods-on-subcontract-lines"></a>Alihankkijarivien laskutustavat

Projekteihin liittyy yleensä kiinteähintaisia ja osamaksupohjaisia sopimusmalleja. Project Operations tukee näitä laskutusmenetelmiä myynti- ja ostokontekstissa. Oston laskutustavat toimivat seuraavasti:

- **Aika ja materiaali** – Kun alihankkijarivi käyttää **Aika- ja Materiaali**-laskutustapaa, projektiin kirjataan ajan kustannukset alihankkijoina, jotka työskentelevät projektissa ja kirjaavat aikaa. Tämän jälkeen nämä alihankkijoiden kustannustapahtumat vastaavat toimittajan laskujen rivinimikkeitä. Tässä mallissa projektipäälliköt, jotka käyttävät Project Operationsia, voivat yhdistää ja tarkistaa toimittajan laskuriveillä alihankkijan ajan, joka on tallennettu ja hyväksytty. Kun tarkistus on tehty, aiemman kustannuksen toteutuneet summat, jotka on kirjattu hyväksynnän jälkeen, palautetaan ja toimittajalaskuun perustuvat uudet toteutuneet kustannukset luodaan projektille.
- **Kiinteä hinta** – Tässä kiinteän maksun sopimusmallissa toimittajan laskut perustuvat kiinteään välitavoitteeseen. Alihankkijaresurssit voivat kuitenkin myös ilmoittaa ajan. Tämän jälkeen projektipäällikkö tarkistaa ja hyväksyy ajan. Kun se on hyväksytty, Project Operations luo projektiin tilapäisiä toteutuneita kustannuksia. Kun toimittaja on lähettänyt laskun välitavoitteesta, projektipäällikkö voi täsmäyttää aiemmin kirjatut kustannusten toteutuneet summat välitavoitteeseen. Kun tarkistus on tehty, toteutuneet kustannukset palautetaan ja välitavoitteeseen perustuva kustannus kirjataan.

## <a name="project-price-lists-on-subcontracts"></a>Projektihinnastot alihankintasopimuksissa

Projektihinnastot ovat hintoja, joita käytetään aika-, kulu- ja muiden projektiin liittyvien komponenttien ostohintojen määritykseen. Hinnastoja voi olla useita, ja jokaisella voi olla oma päivämäärällinen alihankintasopimus Project Operationsissa. Project Operations ei tue alihankintasopimuksen projektihintojen päällekkäisiä päivämääriä.

## <a name="transaction-classes-on-subcontracts"></a>Alihankkijoiden tapahtumaluokat

Project Operations tukee neljää tapahtumaluokan tyyppiä:

- Aika
- Kulut
- Materiaali
- Maksu

Ostokustannuksia voi arvioida ja aiheutua vain **Aika**-, **Kulu**- ja **Materiaali**-tapahtumaluokissa. **Maksu** on vain myyntituottoa varten käytettävissä oleva tapahtumaluokka, eikä se ole käytettävissä oston sisällössä.

## <a name="purchase-pricing-dimensions"></a>Ostojen hinnoitteludimensiot

Hinnoitteludimensioiden avulla voit määrittää, mitä määritteitä käytetään ostohinnan määrityksessä ja aikatapahtumien oletusarvoissa. Project Operations tukee oston yhteydessä vain kiinteän dimension joukkoja ostohinnan määrityksessä ja oletusarvoissa. Alihankkijoiden rivien ja alihankkijoiden aikatapahtumien ostohinnan määrityksessä ja oletusarvoissa määritteet ovat **Rooli** ja **Varattavissa oleva resurssi**.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]