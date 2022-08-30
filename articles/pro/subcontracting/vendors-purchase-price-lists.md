---
title: Toimittaja- ja ostohinnastojen hallinta Project Operationsissa
description: Tässä artikkelissa on tietoja, joiden avulla voidaan luoda ja ylläpitää toimittajatietoja sekä ostohintaluetteloita alihankkijoita varten.
author: rumant
ms.date: 08/02/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 3cd883fed8a59f1c54c39e2d051b9748833ba692
ms.sourcegitcommit: b2224d1f3c0bd4925d647e6ca3960db81a209521
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/11/2022
ms.locfileid: "9261883"
---
# <a name="vendor-and-purchase-price-list-management-in-project-operations"></a>Toimittaja- ja ostohinnastojen hallinta Project Operationsissa


_**Käytetään:** Lite-käyttöönotto – kauppa proformalaskutukseen_

## <a name="vendors-in-project-operations"></a>Project Operationsin toimittajat

Microsoft Dynamics 365 Project Operationsissa toimittajatilien suhdetyyppi on **Toimittaja** tai **Alihankkija**. Voit valita vain asiakastietueen, jolla on jokin näistä suhdetyypeistä, alihankintasopimuksen toimittajaksi.

Voit liittää toimittajatietueeseen yhden tai useamman ostohinnaston. Jokaisella toimittajatietueeseen liittyvällä ostohinnastolla on kuitenkin oltava selkeä voimaantulopäivä. Project Operations ei tue ostohintojen päivämäärien päällekkäisyyttä.

Seuraavia toimittajatietueen kenttiä ja käsitteitä käytetään oletusarvoisesti alihankkijoissa, jotka luodaan toimittajalle:

- Maksuehdot
- Lasku yhteyshenkilölle
- Ensisijainen yhteyshenkilö

    > [!NOTE]
    > Oletusarvoisesti toimittajan ensisijaista yhteyshenkilöä käytetään alihankkijan toimittajan asiakaspäällikkönä.

- Valuutta
- Nykyiset ostohinnastot

## <a name="purchase-price-lists-in-project-operations"></a>Ostohinnastot Project Operationsissa

Hinnastoa, jossa **Konteksti**-kentän arvoksi on määritetty **Osto**, pidetään ostohinnastona. Ostohinnastot voidaan määrittää kuvaamaan ajan, kulujen ja materiaalien ostohintojen luetteloa. Ostohinnastot muistuttavat Project Operationsin kustannus- ja myyntihintaluetteloita. Seuraavat käsitteet koskevat ostohinnastoita samalla tavalla kuin kustannus- ja myyntihintaluetteloita:

- **Päivämäärävaikutus** – Ostohinnastoilla on päivämäärävaikutus. Päivämäärävaikutusta edustavat kunkin hinnastossa olevat alkamis- ja päättymispäiväkentät. Alkamis- ja päättymispäivän välinen aika on voimassaolojakso.
- **Valuutta** – Hinnaston otsikon valuuttaa käytetään valuuttana, jossa ostohinnat on ilmaistu luettelossa olevien työvoima-, kululuokkien ja tuotteiden osalta.
- **Oletusaikayksikkö** – Oletusaikayksikkö ilmaisee ostojen työvoimahinnat. Hinnastossa käytettävää aikayksikkökenttää käytetään vain oletusarvona. Arvoa voi muuttaa yksittäisten roolien hintariveillä.

Ostohinnastot voidaan liittää toimittajatietueisiin liitoksina, joita kutsutaan projektihintaluetteloksi. Näiden hinnastojen avulla voidaan määrittää alihankkijoiden rivien oletushinnat. Kun toimittajatietueeseen liitetään oletusarvon mukaan useita ostohinnastoja, nykyistä hinnastoa käytetään alihankkijoissa, jotka on luotu toimittajalle. Vain hinnastot, joissa **Konteksti**-kentän arvo on **Osto**, voidaan liittää toimittajatietueisiin.

### <a name="subcontract-specific-purchase-price-lists"></a>Alihankkijakohtaiset ostohintaluettelot

Ostohinnastot voidaan liittää myös alihankintasopimuksiin liitoksina, joita kutsutaan projektien hinnastoiksi. Näiden hinnastojen avulla voidaan määrittää alihankkijoiden rivien oletushinnat. Kun alihankkijaan liitetään oletusarvoisesti useita ostohinnastoja, kullakin on oltava selkeä voimaantulopäivämäärä. Project Operations ei tue ostohintojen päivämäärien päällekkäisyyttä. Vain hinnastot, joissa **Konteksti**-kentän arvo on **Osto**, voidaan liittää alihankkijasopimuksiin.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
