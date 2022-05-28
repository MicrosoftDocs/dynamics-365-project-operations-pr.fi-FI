---
title: Projektiryhmän jäsenten alihankintavaihtoehdot
description: Tässä aiheessa selitetään projektiryhmän jäsenten alihankintavaihtoehtoja Microsoft Dynamics 365 Project Operationsissa.
author: rumant
ms.date: 12/03/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: aacd2f97d3120a854c78fe87e512fad1c43b9651
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/14/2022
ms.locfileid: "8600186"
---
# <a name="subcontracting-options-for-project-team-members"></a>Projektiryhmän jäsenten alihankintavaihtoehdot

[!include [banner](../../includes/dataverse-preview.md)]

_**Käytetään:** Lite-käyttöönotto – kauppa proformalaskutukseen_

Microsoft Dynamics 365 Project Operationsissa voit arvioida projektiryhmän jäsenelle tai jäsenille saatavilla olevia alihankintavaihtoehtoja. Käytettävissä olevien alihankintavaihtoehtojen avulla voi:

- Luoda uuden alihankinnan ja/tai luoda uusia rivejä aiemmin luotuun alihankintaan valittuja projektiryhmän jäseniä varten. 
- Tehdä varauksia aiemmin luotua alihankintaa ja alihankintariviä vastaan. 

Voit valita käytössä olevia alihankintavaihtoehtoja yleisiä projektiryhmän jäseniä varten tai valita projektiryhmän jäsenistä, jotka on resursoitu nimetyllä sopimustyöntekijäresurssilla. 

Alihankintavaihtoehtoja ei ole käytettävissä seuraavia varten:

- Projektiryhmän jäsenet, jotka on resursoitu työntekijällä. 
- Projektiryhmän jäsenet, jotka on jo liitetty alihankintaan ja alihankintariviin. 

## <a name="subcontracting-an-unstaffed-project-team-member"></a>Resursoimattoman projektiryhmän jäsenen alihankinta

Kun haluat arvioida ja valita käytössä olevia alihankintavaihtoehtoja yleistä tai resursoimatonta projektiryhmän jäsentä varten, noudata seuraavia vaiheita:

1. Valitse vähintään yksi projektiryhmän jäsentietue, jossa resurssi on yleinen resurssi.
2. Varmista, ettei yksikään valituista projektiryhmän jäsentietueista ole jo alihankittu. 
3. Valitse **Alihankintavaihtoehdot** projektiryhmän jäsenten aliruudukosta. **Alihankintavaihtoehdot**-dialogi avautuu. 
4. Jos olet valinnut vaiheessa 1 vain yhden projektiryhmän jäsentietueen, käytettävissä ovat seuraavat vaihtoehdot:
    - Uusien alihankintarivien luonti. 
    - Varaaminen aiemmin luotua alihankintaa vastaan Jos valitsit vaiheessa 1 useampia projektiryhmän jäsentietueita, ainoa käytössä oleva vaihtoehto on uusien alihankintarivien luominen.
5. Aiemmin luotua alihankintariviä vastaan varaamisen vaihtoehdon avulla voit valita alihankinnan ja alihankintarivin, joita vastaan haluat varata. Kun valitset alihankintarivin kapasiteetin varaamista varten, varmista, että valittu alihankintarivi edustaa aikaa ja että rooli, joka projektiryhmän jäseneltä vaaditaan, vastaa roolia, joka ostettiin alihankintarivillä.
6. Kun valitset uusien alihankintarivien luomisen projektiryhmän jäseniä varten, järjestelmä sallii sinun valita alihankinnan, jonka haluat kyseisten rivien luomista varten. Alihankinnan, johon haluat luoda uusia rivejä, tulee olla **Luonnos**-tilassa. Tätä vaihtoehtoa (uusien alihankintarivien luominen projektiryhmän jäsenille) käytettäessä järjestelmä luo yhden aikaa edustavan alihankintarivin jokaiselle projektiryhmän jäsenelle. Rooli, tunnit ja päivämäärät kopioidaan projektiryhmän jäsenestä jokaiselle luodulle alihankintariville. 
7. Kun yleinen ryhmän jäsen yhdistetään alihankintaan ja alihankintariviin, **Työntekijätyyppi**-kenttä yleisen ryhmän jäsenen rivillä päivitetään muotoon **Sopimustyöntekijä** ja **Alihankinnan voimassaolo** määritetään arvoon **Kelvollinen**.

## <a name="subcontracting-a-staffed-project-team-member"></a>Resursoidun projektiryhmän jäsenen alihankinta

Samoin kuin yleisten ja resursoimattomien ryhmän jäsenien kohdalla, alihankintavaihtoehtoja voi tarkastella myös resursoitujen projektiryhmän jäsenten osalta, kunhan resursoitu ryhmän jäsen on sopimustyöntekijä. Kun haluat arvioida ja valita käytössä olevia alihankintavaihtoehtoja resursoitua tai nimettyä projektiryhmän jäsentä varten, noudata seuraavia vaiheita:

1. Valitse vähintään yksi projektiryhmän jäsentietue, jossa resurssi on nimetty sopimustyöntekijä.
2. Varmista, ettei yksikään valituista projektiryhmän jäsentietueista ole jo alihankittu. 
3. Valitse **Alihankintavaihtoehdot** projektiryhmän jäsenten aliruudukosta. **Alihankintavaihtoehdot**-dialogi avautuu. 
4. Jos olet valinnut vaiheessa 1 vain yhden projektiryhmän jäsentietueen, käytettävissä ovat seuraavat vaihtoehdot:
      - Uusien alihankintarivien luonti.
      - Varaa aiemmin luotua alihankintaa vastaan.
  Jos valitsit vaiheessa 1 useampia projektiryhmän jäsentietueita, ainoa käytössä oleva vaihtoehto on uusien alihankintarivien luominen.
5. Aiemmin luotua alihankintariviä vastaan varaamisen vaihtoehdon avulla voit valita alihankinnan ja alihankintarivin, joita vastaan haluat varata. Kun valitset alihankintariviä kapasiteetin varaamista varten, varmista seuraavat asiat:
      - Valittu alihankintarivi edustaa aikaa. 
      - Projektiryhmän jäseneltä vaadittu rooli vastaa roolia, joka ostettiin alihankintarivillä. 
      - Toimittaja, johon sopimustyöntekijä on liitetty, on sama kuin alihankinnan toimittaja.
6. Kun valitset uusien alihankintarivien luomisen projektiryhmän jäseniä varten, järjestelmä sallii sinun valita alihankinnan, jonka haluat kyseisten rivien luomista varten. Tämän vaihtoehdon avulla sinun tulisi varmistaa, että toimittaja, jolle sopimustyöntekijä kuuluu, on sama kuin alihankinnan toimittaja. 
7. Alihankinnan, johon haluat luoda uusia rivejä, tulee olla **Luonnos**-tilassa. Tätä vaihtoehtoa (uusien alihankintarivien luominen projektiryhmän jäsenille) käytettäessä järjestelmä luo yhden aikaa edustavan alihankintarivin jokaiselle projektiryhmän jäsenelle. Rooli, tunnit ja päivämäärät kopioidaan projektiryhmän jäsenestä jokaiselle luodulle alihankintariville.  
8. Kun nimetty ryhmän jäsen yhdistetään alihankintaan ja alihankintariviin, **Työntekijätyyppi**-kenttä nimetyn ryhmän jäsenen rivillä päivitetään muotoon **Sopimustyöntekijä** ja **Alihankinnan voimassaolo** määritetään arvoon **Kelvollinen**.

## <a name="re-costing-subcontractor-assignments"></a>Alihankinnan määritysten uudelleenlaskenta

Kun linkität projektiryhmän jäsenen (yleisen tai nimetyn) alihankintariviin käyttämällä **Alihankintavaihtoehdot**-dialogia, kaikki määritykset tehtäviin, jotka kyseisellä ryhmän jäsenellä on, lasketaan uudelleen perustuen alihankintaan liitettyyn ostohinnastoon. Valitse **Arviot**-välilehti **Projektin tiedot** -sivulla ja valitse **Päivitä hinnat** -painike nähdäksesi päivitetyn hinnoittelun ja/tai laskelman, joka syntyy alihankintapäätöksen tuloksena.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
