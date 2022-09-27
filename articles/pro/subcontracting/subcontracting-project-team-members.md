---
title: Alihankintaprojektiryhmän jäsenet
description: Tässä artikkelissa käsitellään alihankintaprojektiryhmän jäseniä Microsoft Dynamics 365 Project Operationsissa.
author: rumant
ms.date: 9/14/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: a2f17d6f270029e3a517e99c7bb518cdb19b8d23
ms.sourcegitcommit: 08eb3be9eda44e9446c43ed9b6aefd58d77927c5
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/15/2022
ms.locfileid: "9522791"
---
# <a name="subcontracting-project-team-members"></a>Alihankintaprojektiryhmän jäsenet

_**Koskee:** Project Operationsin resurssiin / muuhun kuin resurssiin perustuvia skenaarioita, Lite-käyttöönotto-kaupasta proformalaskutukseen_

Microsoft Dynamics 365 Project Operationsissa voi alihankkia resursoimattomia tai resursoituja ryhmän jäseniä.

- Resursoimattomille ryhmän jäsenille on määritetty yleinen resurssi.
- Resursoiduille ryhmän jäsenille on määritetty nimetty resurssi.

Kun linkität projektiryhmän jäsenen alihankintariviin, kaikki määritykset tehtäviin, jotka kyseisellä ryhmän jäsenellä on, lasketaan uudelleen perustuen alihankintaan liitettyyn ostohinnastoon.  Valitse **Arviot**-välilehti **Projektin tiedot** -sivulla ja valitse **Päivitä hinnat** -painike nähdäksesi päivitetyn hinnoittelun ja/tai laskelman, joka syntyy alihankintapäätöksen tuloksena. 

## <a name="subcontracting-an-unstaffed-project-team-member"></a>Resursoimattoman projektiryhmän jäsenen alihankinta
**Ryhmän jäsenen tiedot** -sivulla on alihankinta- ja alihankintarivikentät, joiden avulla projektipäällikkö voi valita, miten alihankinnasta otetaan vaadittua kapasiteettia. Jos haluat tehdä projektiryhmän jäsenen alihankinnan yleisenä resurssina, noudata seuraavia vaiheita:

1.  Valitse alihankinta **Ryhmän jäsenen tiedot** -sivulta.

2.  Voit valita vain alihankintoja, joiden tila on joko **Luonnos** tai **Vahvistettu**. Jos alihankinnan tila on joko **Suljettu** tai **Peruutettu**, sitä ei voi valita. 

3.  **Alihankintarivi**-kenttä tulee näkyviin, kun olet valinnut alihankinnan.

4.  **Alihankintarivi**-kentässä voi valita vain aikaa edustavia alihankintarivejä. Kulujen ja materiaalien alihankintarivejä ei voi valita.

5.  Projektiryhmän jäsentietueen roolin on vastattava alihankintarivin roolia. Tämä varmistaa, että projektissa arvioitu roolin aika vastaa alihankintarivillä ostettua roolia. 

Kun yleinen ryhmän jäsen yhdistetään alihankintaan ja alihankintariviin, **Työntekijätyyppi**-kenttä yleisen ryhmän jäsenen rivillä päivitetään muotoon **Sopimustyöntekijä** ja **Alihankinnan voimassaolo** määritetään arvoon **Kelvollinen**.

## <a name="subcontracting-a-staffed-project-team-member"></a>Resursoidun projektiryhmän jäsenen alihankinta
Kuten yleisten tai resursoimattomien ryhmän jäsenien tapauksessa, projektin vaatiman resursoidun ryhmän jäsenen kapasiteetin voi linkittää alihankintaan. Jos haluat tehdä nimetyn projektiryhmän jäsenen alihankinnan, noudata seuraavia vaiheita:

1.  Varmista, että nimetty resurssi on määritetty varattavan resurssin sopimustyöntekijätyypiksi. Varmista myös, että varattavan resurssin **Toimittaja**-kenttä vastaa valitsemasi alihankinnan toimittajaa. 

2.  Voit valita vain alihankintoja, joiden tila on joko **Luonnos** tai **Vahvistettu**. Jos alihankinnan tila on joko **Suljettu** tai **Peruutettu**, sitä ei voi valita. 

3.  **Alihankintarivi**-kenttä tulee näkyviin, kun olet valinnut alihankinnan.

4.  **Alihankintarivi**-kentässä voi valita vain aikaa edustavia alihankintarivejä. Kulujen ja materiaalien alihankintarivejä ei voi valita.

5.  Projektiryhmän jäsentietueen roolin on vastattava alihankintarivin roolia. Tämä varmistaa, että projektissa arvioitu roolin aika vastaa alihankintarivillä ostettua roolia. 

Nimetyt projektiryhmän jäsenet, joilla ei ole sopimustyöntekijän tyyppiä **Varattava resurssi**, näkyvät alihankinnan voimassaolotilassa **Ei kelvollinen**, jos niitä ei ole linkitetty alihankintaan. Kun nimetty projektiryhmän jäsen yhdistetään alihankintaan ja alihankintariviin, **Työntekijätyyppi**-kenttä ryhmän jäsenen rivillä päivitetään muotoon **Sopimustyöntekijä** ja **Alihankinnan voimassaolo** määritetään arvoon **Kelvollinen**.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
