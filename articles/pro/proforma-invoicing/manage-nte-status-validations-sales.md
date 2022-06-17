---
title: Ei-ylitettävän tilan ja vahvistusten hallinta
description: Tässä artikkelissa on tietoja Project Operationsissa suorittavista ei-ylitettävän rajoituksen tarkistuksesta.
author: rumant
ms.date: 04/05/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: d10a88305339a84b36d8606631ea9761806098a1
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8932752"
---
# <a name="manage-not-to-exceed-status-and-validations"></a>Ei-ylitettävän tilan ja vahvistusten hallinta 

_**Koskee:** Project Operationsin resurssiin / muuhun kuin resurssiin perustuvia skenaarioita, Lite-käyttöönotto-kaupasta proformalaskutukseen_

## <a name="not-to-exceed-on-approvals"></a>Ei-ylitettävät rajoitukset hyväksynnöissä

Kun ajan, kulun tai materiaalin käytön merkintä lähetetään, luodaan hyväksyntätietue. Jos hyväksyntä on veloitettava ja yhdistetään ajan ja materiaalin sopimusriville, järjestelmä suorittaa ei-ylitettävän vahvistustarkastuksen seuraavilla tasoilla:

  - Tarkistus projektin sopimusrivillä asiakkaalle määritetyn rajan perusteella
  - Tarkistus sopimusrivillä määritetyn rajan perusteella
  - Tarkistus asiakkaalle määritetyn rajan perusteella
  - Tarkistus sopimuksessa määritetyn rajan perusteella

Kullakin tasolla tehtävät tarkistukset varmistavat, että tämän hyväksynnän myyntiarvon summa ei riko ei-ylitettävää rajoitusta kyseisellä tasolla sen jälkeen, kun jo kirjattu keskeneräinen laskutus ja kyseiseen päivämäärään mennessä laskutettu summa on otettu huomioon.

Jos tarkistus läpäistään, hyväksynnän vahvistuksen tila on **Onnistui**.

Jos tarkistusta ei läpäistä, hyväksynnän vahvistuksen tila on **Epäonnistui**. Ei-ylitettävän rajoituksen tarkistuksen tiedot ilmaisevat käyttäjälle, millä tasolla vahvistus epäonnistui.

Kun lähetettyä aikaa, kulua tai materiaalin käyttöä ei katsota laskutettavaksi, ei-ylitettävän vahvistuksen tilaksi määritetään **Ei käytettävissä** ja tarkistustiedot ovat **Ei käytettävissä**.

## <a name="not-to-exceed-on-unbilled-sales-actuals"></a>Laskuttamattomien myynnin todellisten arvojen ei-ylitettävä rajoitus

Kun ajan, kulun tai materiaalin käyttötapahtuma hyväksytään, luodaan kustannukset ja laskuttamattomat myynnin toteutuneiden arvojen tietueet. Jos luotava laskuttamaton myynnin todellinen arvo on veloitettava ja yhdistetään ajan ja materiaalin sopimusriville, sovellus suorittaa ei-ylitettävän rajoituksen vahvistustarkastuksen seuraavilla tasoilla:

  - Tarkistus projektin sopimusrivin asiakkaalle määritetyn rajan perusteella
  - Tarkistus sopimusrivillä määritetyn rajan perusteella
  - Tarkistus asiakkaalle määritetyn rajan perusteella
  - Tarkistus sopimuksessa määritetyn rajan perusteella

Kullakin tasolla tehtävät tarkistukset varmistavat, että tämän todellisen arvon myyntiarvon summa ei riko ei-ylitettävää rajoitusta kyseisellä tasolla sen jälkeen, kun jo kirjattu keskeneräinen laskutus ja kyseiseen päivämäärään mennessä laskutettu summa on otettu huomioon.

Jos tarkistus läpäistä, laskuttamattoman myynnin todellisen arvon ei-ylitettävän tilaksi annetaan **Vahvistettu**.

Jos tarkistusta ei läpäistä, laskuttamattoman myynnin todellisen arvon ei-ylitettävän rajoituksen tilaksi annetaan **Epäonnistui**. Vahvistuksen tiedot ilmaisevat käyttäjälle, millä tasolla vahvistus epäonnistui.

Kun laskuttamattoman myynnin todellinen arvo on ei-veloitettava tai ilmainen ja jos millekään neljällä tasolle ei ole määritetty ei-ylitettävää rajoitusta tai luotava todellinen arvo on kustannus, ennakkomaksu, resursointityksikkö tai konsernin sisäinen myynti, **Ei-ylitettävän rajoituksen tila**- ja **Ei-ylitettävän rajoituksen tarkistuksen tiedot** -kenttien arvoksi on määritettävä **Ei käytettävissä**.

## <a name="reset-the-not-to-exceed-status"></a>Ei-ylitettävän rajoituksen tilan nollaaminen

Ei-ylitettävän rajoituksen voi nollata joukkotoiminnolla. Projektipäälliköt voivat oikaista ei-ylitettävää tarkistusta, jotta tietyn työ-, aika-, kulu- tai materiaalikäytön laskutus voidaan priorisoida muiden suhteen, jotka on jo käytetty saatavilla olevasta summasta, jota ei saa ylittää.

Kun laskuttamattomien myynnin todellisten arvojen ei-ylitettävien rajoitusten tila nollataan, vahvistettua summaa pienennetään. Projektipäällikkö voi valita toisen työ-, aika-, kulu- tai materiaalikäyttömerkinnän, joka ei ole aiemmin läpäissyt ei-ylitettävää vahvistusta, ja arvioida sen uudelleen. Kun sidottu summa on pienentynyt, nämä toteutuneet summat ohittavat nyt oikeellisuustarkistuksen, mikä auttaa projektipäällikköä hallitsemaan enemmän laskutettavia tapahtumia kyseiseltä jaksolta.

Voit nollata ei-ylitettävän rajoituksen tilan valitsemalla vähintään yhden todellisen arvon **Keskeneräiset ajan ja materiaalin laskutukset**- tai **Todelliset arvot** -näkymässä ja valitse sitten **Nollaa ei-ylitettävän rajoituksen tila**.

Kaikkien soveltuvien todellisten arvojen ei-ylitettävän rajoituksen tilaksi nollataan **Ei arvioitu**. Todelliset arvot, joiden ei-ylitettävän rajoituksen tila nollataan, ovat laskuttamattomia myynnin todellisia arvoja, joita ei ole vielä laskutettu, jotka eivät ole laskuluonnoksia ja jotka on merkitty veloitettavaksi. Kaikki muut valitut todelliset arvot ohitetaan.

## <a name="reevaluate-not-to-exceed-status"></a>Ei-ylitettävän rajoituksen tila uudelleenarviointi

Ei-ylitettävän rajoituksen voi arvioida uudelleen joukkotoiminnolla. Ei-ylitettävän rajoituksen tilan uudelleenarvioinnista on hyötyä seuraavissa tilanteissa:

  - Ei-ylitettävät rajoitukset neuvoteltiin uudelleen asiakkaan kanssa ja todelliset arvot on arvioitava uudelleen.
  - Projektipäällikkö haluaa tarkentaa laskuttamattoman myynnin keskeneräistä laskutusta priorisoimalla tiettyjä töitä.

Voit arvioida ei-ylitettävän rajoituksen tilan uudelleen valitsemalla vähintään yhden todellisen arvon **Keskeneräiset ajan ja materiaalin laskutukset**- tai **Todelliset arvot** -näkymässä ja valitse sitten **Arvioi ei-ylitettävän rajoituksen tila uudelleen**.

Kaikki soveltuvat todelliset arvot, joissa on ei-ylitettävä rajoitus, arvioidaan ei-ylitettävien rajoitusten asetusten perusteella. Todelliset arvot, jotka liittyvät ei-ylitettävän rajoituksen tila uudelleenarviointiin, ovat laskuttamattomia myynnin todellisia arvoja, joita ei ole laskutettu, jotka eivät ole laskuluonnoksia ja jotka on merkitty veloitettavaksi. Kaikki muut valitut todelliset arvot ohitetaan.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
