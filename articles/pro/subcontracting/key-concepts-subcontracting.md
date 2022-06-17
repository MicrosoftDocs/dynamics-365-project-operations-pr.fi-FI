---
title: Alihankinnan keskeiset käsitteet
description: Tässä artikkelissa on joitakin tärkeitä käsitteitä, joita käytetään Microsoft Dynamics 365 Project Operationsin alihankintasopimuksissa.
author: rumant
ms.date: 08/03/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 0ac84d132a2d62528d97ed3776a78062a589a380
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8927692"
---
# <a name="key-concepts-in-subcontracting"></a>Alihankinnan keskeiset käsitteet

[!include [banner](../../includes/dataverse-preview.md)]

_**Käytetään:** Lite-käyttöönotto – kauppa proformalaskutukseen_

Artikkelissa käsitellään joitakin tärkeitä käsitteitä, jotka on syytä tietää, ennen kuin Microsoft Dynamics 365 Project Operationsin alihankkijatoimintojen käyttö aloitetaan.

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
