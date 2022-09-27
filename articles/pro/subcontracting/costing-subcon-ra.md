---
title: Alihankittujen resurssimääritysten kustannusarvio
description: Tässä artikkelissa käsitellään Microsoft Dynamics 365 Project Operationsin tapaa laskea alihankittujen resurssimääritysten kustannusarvio.
author: rumant
ms.date: 09/14/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 9fded1baa63d2defc134994c858dfc6c09f75082
ms.sourcegitcommit: 08eb3be9eda44e9446c43ed9b6aefd58d77927c5
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/15/2022
ms.locfileid: "9522650"
---
# <a name="cost-estimation-of-subcontracted-resource-assignments"></a>Alihankittujen resurssimääritysten kustannusarvio

_**Koskee:** Project Operationsin resurssiin / muuhun kuin resurssiin perustuvia skenaarioita, Lite-käyttöönotto-kaupasta proformalaskutukseen_

Alihankittujen projektiryhmän jäsenten määritykset lasketaan käyttämällä **ostohinnastoa**, joka on liitetty alihankintaan liittyvässä ryhmän jäsenen tietueessa. Tämä eroaa työntekijän resurssimäärityksien laskemisesta siinä, että työntekijän resurssien tehtävämääritykset lasketaan käyttämällä **kustannushinnastoa**, joka on liitetty projektin sopimusyksikköön. 

Alihankittujen yleisten projektiryhmän jäsenten osalta määritykset lasketaan käyttämällä roolipohjaista hintamäärittelyä alihankintaan liitetyssä ostohinnastossa. Ostohinnat voidaan määrittää myös erikseen kullekin resurssille. Näille resurssikohtaisille hinnoille annetaan prioriteetti, kun lasketaan nimettyjen projektiryhmän jäsenten ja sopimustyöntekijöiden määrityksiä. 

Roolikohtaisen ja resurssikohtaisen ostohinnan käyttämisen välisen prioriteetin määrää hinnoitteludimension prioriteetin määritys kohdassa **Parametrit > Summaperusteiset hinnoitteludimensiot**.

Tämä toiminto, jossa hinnat johdetaan dynaamisesti perustuen alihankkijoiden ostohintojen dimensiomääritykseen, on samanlainen kuin toiminto, jossa kustannus- ja laskutushinnat johdetaan kokoaikaisille työntekijöille. 

## <a name="creating-task-assignments-for-getting-cost-estimates-of-subcontractor-resources"></a>Tehtävien määritysten luominen alihankkijaresurssien kustannusarvioiden saamista varten

Alihankkijoiden tehtävämääritykset voidaan luoda kahdella tavalla: 
- Käyttämällä **Tehtävät**-välilehteä.
- Käyttämällä **Ryhmä**-välilehteä.

### <a name="creating-resources-assignments-using-the-tasks-tab"></a>Resurssimäärityksien luominen käyttämällä Tehtävät-välilehteä
Käyttämällä **Resurssit**-luetteloa **Tehtävät**-välilehdessä tiettyä tehtävää varten voit luoda tehtävämäärityksen nimetylle resurssille tai yleiselle resurssille. Jos valitset nimetyn resurssin avattavasta **Määritetyt resurssit**-luettelosta tehtävässä ja resurssi on sopimustyöntekijä, määritetään nimetty resurssi tehtävään ja luodaan vastaava projektiryhmän jäsentietue, jossa työntekijätyyppi on **Sopimustyöntekijä** ja **Voimassaolo** on **Pätemätön**. Avaa seuraavaksi projektiryhmän jäsentietue ja valitse alihankinta ja alihankintarivi. Tämä päivittää tehtävän määrityksen niin, että siinä on viittaus alihankintaan ja alihankintariviin, ja myös ryhmän jäsenen tilaksi tulee **Kelvollinen**.

Jos päätät luoda yleisen ryhmän jäsenen avattavasta **Määritetyt resurssit** -luettelosta tehtävässä, **Yleisen ryhmän jäsenen luonti** -dialogin avulla voit valita alihankinnan ja alihankintarivin. Kun yleinen resurssi on määritetty tehtävään ja vastaava projektiryhmän jäsentietue on luotu, huomaat, että projektiryhmän jäsentietueessa työntekijätyyppi on **Sopimustyöntekijä** ja **Voimassaolo** on **Kelvollinen**.

### <a name="creating-project-team-members-using-the-team-tab"></a>Projektiryhmän jäsenten luominen käyttämällä Ryhmä-välilehteä
Projektin Ryhmä-välilehden avulla voit luoda yleisen tai nimetyn ryhmän jäsenen. Luodessasi ryhmän jäsentä voit valita alihankinnan ja alihankintarivin. Kun ryhmän jäsen on luotu, sinun on määritettävä ryhmän jäsen tehtävään käyttämällä avattavaa **Määritetyt resurssit** -luetteloa tehtävässä. 

## <a name="updating-estimates"></a>Arvioiden päivittäminen
Kun olet delegoinut tehtävät ryhmän jäsenille, on siirryttävä projektin **Arviot**-välilehteen ja valittava **Päivitä hinnat**, jotta varmistetaan, että alihankkijan resurssimäärityksien kustannushinnat päivitetään alihankintaan liitetyn ostohinnaston mukaisesti. Delegoimattomia tehtäviä varten ei muodosteta arvioita Microsoft Dynamics 365 Project Operationsissa. Tämän vuoksi sinun täytyy luoda projektissa tehtävämääritykset eri hinnoittelu- ja laskemistehtäviä varten. 

> [HUOMAUTUS!] Projektiryhmän jäsenet, joiden **Työntekijätyyppi** on **Sopimustyöntekijä**, mutta joilla ei ole alihankintaviitettä, merkitään muotoon **Pätemätön** **Projektiryhmän jäsenet** -ruudukossa. Jos on projektiryhmän jäseniä, joilla on tämä tila, avaa projektiryhmän jäsentietue ja päivitä alihankinta- ja alihankintarivikentät manuaalisesti niin, että kustannusarvio vastaa tarkasti alihankkijan kustannusta **Arviot**-välilehdessä. 


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
