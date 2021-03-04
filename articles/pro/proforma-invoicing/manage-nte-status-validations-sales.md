---
title: Ei-ylitettävän tilan ja vahvistusten hallinta
description: Tässä aiheessa on tietoja Project Operationsissa suorittavista ei-ylitettävän rajoituksen tarkistuksesta.
author: rumant
manager: Annbe
ms.date: 10/22/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 09dea414e91a365f33bd23089c427b5f63f55c8e
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/28/2020
ms.locfileid: "4129989"
---
# <a name="manage-not-to-exceed-status-and-validations"></a>Ei-ylitettävän tilan ja vahvistusten hallinta 

_**Koskee:** Project Operationsin resurssiin / muuhun kuin resurssiin perustuvia skenaarioita, Lite-käyttöönotto-kaupasta proformalaskutukseen_

## <a name="not-to-exceed-on-approvals"></a>Ei-ylitettävät rajoitukset hyväksynnöissä

Kun aika- tai kulumerkintä lähetetään, hyväksyntätietue luodaan. Jos hyväksyntä on veloitettava ja yhdistetään ajan ja materiaalin sopimusriville, järjestelmä suorittaa ei-ylitettävän vahvistustarkastuksen seuraavilla tasoilla:

  - Tarkistus projektin sopimusrivillä asiakkaalle määritetyn rajan perusteella
  - Tarkistus sopimusrivillä määritetyn rajan perusteella
  - Tarkistus asiakkaalle määritetyn rajan perusteella
  - Tarkistus sopimuksessa määritetyn rajan perusteella

Kullakin tasolla tehtävät tarkistukset varmistavat, että tämän hyväksynnän myyntiarvon summa ei riko ei-ylitettävää rajoitusta kyseisellä tasolla sen jälkeen, kun jo kirjattu keskeneräinen laskutus ja kyseiseen päivämäärään mennessä laskutettu summa on otettu huomioon.

Jos tarkistus läpäistään, hyväksynnän vahvistuksen tila on **Onnistui**.

Jos tarkistusta ei läpäistä, hyväksynnän vahvistuksen tila on **Epäonnistui**. Ei-ylitettävän rajoituksen tarkistuksen tiedot ilmaisevat käyttäjälle, millä tasolla vahvistus epäonnistui.

Jos lähetetty aika- tai kulumerkintä on ei-veloitettava, ei-ylitettävän rajoituksen tarkistuksen tilaksi on määritetty **Ei käytettävissä** ja tarkistuksen tieto on **Ei käytettävissä**.

## <a name="not-to-exceed-on-unbilled-sales-actuals"></a>Laskuttamattomien myynnin todellisten arvojen ei-ylitettävä rajoitus

Kun aika- tai kulumerkintä hyväksytään, kustannusten ja laskuttamattomien myynnin todellisten arvojen tietueet luodaan. Jos luotava laskuttamaton myynnin todellinen arvo on veloitettava ja yhdistetään ajan ja materiaalin sopimusriville, sovellus suorittaa ei-ylitettävän rajoituksen vahvistustarkastuksen seuraavilla tasoilla:

  - Tarkistus projektin sopimusrivin asiakkaalle määritetyn rajan perusteella
  - Tarkistus sopimusrivillä määritetyn rajan perusteella
  - Tarkistus asiakkaalle määritetyn rajan perusteella
  - Tarkistus sopimuksessa määritetyn rajan perusteella

Kullakin tasolla tehtävät tarkistukset varmistavat, että tämän todellisen arvon myyntiarvon summa ei riko ei-ylitettävää rajoitusta kyseisellä tasolla sen jälkeen, kun jo kirjattu keskeneräinen laskutus ja kyseiseen päivämäärään mennessä laskutettu summa on otettu huomioon.

Jos tarkistus läpäistä, laskuttamattoman myynnin todellisen arvon ei-ylitettävän tilaksi annetaan **Vahvistettu**.

Jos tarkistusta ei läpäistä, laskuttamattoman myynnin todellisen arvon ei-ylitettävän rajoituksen tilaksi annetaan **Epäonnistui**. Vahvistuksen tiedot ilmaisevat käyttäjälle, millä tasolla vahvistus epäonnistui.

Kun laskuttamattoman myynnin todellinen arvo on ei-veloitettava tai ilmainen ja jos millekään neljällä tasolle ei ole määritetty ei-ylitettävää rajoitusta tai luotava todellinen arvo on kustannus, ennakkomaksu, resursointityksikkö tai konsernin sisäinen myynti, **Ei-ylitettävän rajoituksen tila**- ja **Ei-ylitettävän rajoituksen tarkistuksen tiedot** -kenttien arvoksi on määritettävä **Ei käytettävissä**.

## <a name="reset-the-not-to-exceed-status"></a>Ei-ylitettävän rajoituksen tilan nollaaminen

Ei-ylitettävän rajoituksen voi nollata joukkotoiminnolla. Tällä tavoin projektipäälliköt voivat muokata ei-ylitettävän rajoituksen tarkistusta ja priorisoida tietyn työn, ajan tai kulujen laskutusta muiden käytettävissä olevasta ei-ylitettävästä rajoitussummasta jo vahvistettujen ohitse.

Kun laskuttamattomien myynnin todellisten arvojen ei-ylitettävien rajoitusten tila nollataan, vahvistettua summaa pienennetään. Projektipäällikkö voi valita toisen työn, ajan tai kulun, joka ei aiemmin läpäissyt ei-ylitettävän rajoituksen tarkistusta, ja arvioida ne uudelleen. Kun vahvistettu summa pienenee, nämä todelliset arvot läpäisevät nyt vahvistuksen. Tällä tavoin projektipäällikkö voi hallita tarkemmin kyseisen kauden laskutettavissa olevia tapahtumia.

Voit nollata ei-ylitettävän rajoituksen tilan valitsemalla vähintään yhden todellisen arvon **Keskeneräiset ajan ja materiaalin laskutukset**- tai **Todelliset arvot** -näkymässä ja valitse sitten **Nollaa ei-ylitettävän rajoituksen tila**.

Kaikkien soveltuvien todellisten arvojen ei-ylitettävän rajoituksen tilaksi nollataan **Ei arvioitu**. Todelliset arvot, joiden ei-ylitettävän rajoituksen tila nollataan, ovat laskuttamattomia myynnin todellisia arvoja, joita ei ole vielä laskutettu, jotka eivät ole laskuluonnoksia ja jotka on merkitty veloitettavaksi. Kaikki muut valitut todelliset arvot ohitetaan.

## <a name="reevaluate-not-to-exceed-status"></a>Ei-ylitettävän rajoituksen tila uudelleenarviointi

Ei-ylitettävän rajoituksen voi arvioida uudelleen joukkotoiminnolla. Ei-ylitettävän rajoituksen tilan uudelleenarvioinnista on hyötyä seuraavissa tilanteissa:

  - Ei-ylitettävät rajoitukset neuvoteltiin uudelleen asiakkaan kanssa ja todelliset arvot on arvioitava uudelleen.
  - Projektipäällikkö haluaa tarkentaa laskuttamattoman myynnin keskeneräistä laskutusta priorisoimalla tiettyjä töitä.

Voit arvioida ei-ylitettävän rajoituksen tilan uudelleen valitsemalla vähintään yhden todellisen arvon **Keskeneräiset ajan ja materiaalin laskutukset**- tai **Todelliset arvot** -näkymässä ja valitse sitten **Arvioi ei-ylitettävän rajoituksen tila uudelleen**.

Kaikki soveltuvat todelliset arvot, joissa on ei-ylitettävä rajoitus, arvioidaan ei-ylitettävien rajoitusten asetusten perusteella. Todelliset arvot, jotka liittyvät ei-ylitettävän rajoituksen tila uudelleenarviointiin, ovat laskuttamattomia myynnin todellisia arvoja, joita ei ole laskutettu, jotka eivät ole laskuluonnoksia ja jotka on merkitty veloitettavaksi. Kaikki muut valitut todelliset arvot ohitetaan.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]