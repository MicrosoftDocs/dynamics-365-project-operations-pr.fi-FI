---
title: Projektien resurssiajan taloudelliset arviot
description: Tässä aiheessa on tietoja siitä, miten ajan taloudelliset arviot lasketaan.
author: rumant
ms.date: 03/19/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: e4be4c8087005ae66a54d40ac88017df591c56eca64f04b00cf34b0e5a8a09ce
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/06/2021
ms.locfileid: "6998682"
---
# <a name="financial-estimates-for-resource-time-on-projects"></a>Projektien resurssiajan taloudelliset arviot

_**Koskee:** Project Operationsin resurssiin / muuhun kuin resurssiin perustuvia skenaarioita, Lite-käyttöönotto-kaupasta proformalaskutukseen_

Ajan taloudelliset arviot lasketaan kolmen tekijän perusteella: 

- Projektisuunnitelman jokaiselle solmutehtävälle määritetty yleisen tai nimetyn ryhmän jäsenen tyyppi. 
- Työn tyyppi tai monimutkaisuus.
- Resurssin tehtävän määrityksen työmäärän jakautuminen. 

Kaksi ensimmäistä tekijää vaikuttavat resurssin tehtävän yksikkökustannukseen tai laskutusprosenttiin. Resurssin delegoinnissa yksikkökustannus tai laskutusprosentti määräytyy resurssin määritteiden mukaan. Nämä määritteet sisältävät organisaatioyksikön, johon resurssi kuuluu, ja resurssin vakioroolin. Voit myös lisätä yrityksesi kannalta merkityksellisiä mukautettuja määritteitä resurssille, kuten vakionimike- tai kokemustason, ja määrittää ne vaikuttamaan tehtävän yksikkökustannuksiin tai laskuprosenttiin.
Resurssin määritteiden lisäksi työn määritteet, kuten tehtävä, voivat vaikuttaa myös tehtävän yksikkölaskutusprosenttiin tai kustannusprosenttiin. Jos esimerkiksi tietyt tehtävät ovat monimutkaisempia, resurssin kyseisille tehtäville määrittäminen johtaa siihen, että yksikkökustannus tai laskutusaste on suurempi kuin tehtävillä, jotka ovat vähemmän monimutkaisia.   

Kolmas tekijä antaa tähän tuntien lukumäärän tällä hinnalla. Jos tehtävä kattaa kaksi hintajaksoa, on todennäköistä, että resurssin tehtävän ensimmäinen osa saa kustannukset ja hinnoitellaan eri tavalla kuin toinen osa tehtävästä. Kunkin resurssin tehtävän työmääräarvio on monitasoinen arvo, joka tallennetaan työmäärän jakautumiseen päiville.

Yksityiskohtaiset ohjeet työn ja resurssien mukautettujen määritteiden määrittämisestä hinnoittelu- ja kustannusdimensioiksi on ohjeaiheessa [Hinnoitteludimensioiden yleiskatsaus](../pricing-costing/pricing-dimensions-overview.md).

Kunkin resurssin määrityksen taloudellinen arvio lasketaan tehtävän **työn hinta/t kerrottuna tuntien lukumäärällä.**  Työmäärän arvion tavoin kunkin resurssimäärityksen kustannus- ja tuottoarvio on monitasoinen arvo, joka tallennetaan rahasumman jakautumiseen päiville. 

## <a name="summarizing-financial-estimates-for-time"></a>Ajan taloudellisten arvioiden yhteenveto
Ajan taloudellinen arvio lehtisolmussa on kyseisen tehtävän taloudellisten arvioiden summa kaikista resurssimäärityksistä.

Ajan taloudellinen arvio yhteenveto- tai ylätason tehtävässä on kyseisen tehtävän taloudellisten arvioiden summa kaikista sen alitehtävistä. Tämä on projektin arvioitu työvoimakustannus. 

![Resurssiarviot.](./media/navigation12.png)

## <a name="default-cost-price-and-cost-currency"></a>Kustannushinnan ja kustannusvaluutan oletusarvot

Oletuskustannushinta tulee projektin sopimusyksikköön liitetystä hinnastosta. Projektin kustannusvaluutta on aina projektin sopimusyksikön valuutta. Kun resurssi on määritetty, kustannuksen taloudellinen arvio tallennetaan projektin kustannusvaluuttana. Joskus valuutta, jossa kustannushinta määritetään hinnastossa, eroaa projektin kustannusvaluutasta. Tällöin sovellus muuntaa valuutan, jossa kustannushinta on määritetty, projektin valuutaksi. **Arviot**-ruudukossa näkyvät kaikki kustannusarviot ja niiden yhteenveto projektin kustannusvaluuttana. 

## <a name="default-bill-rate-and-sales-currency"></a>Laskutushinnan ja myyntivaluutan oletusarvot

Oletusmyyntihinta tulee projektihinnastoista, jotka on liitetty liittyvään projektisopimukseen, jos sopimus on voitettu, tai liittyvästä projektitarjouksesta, jos kauppa on vielä myyntiä edeltävässä vaiheessa. Projektin myyntivaluutta on aina projektin tarjouksen tai sopimuksen valuutta. Kun resurssi on määritetty, myynninn taloudellinen arvio tallennetaan projektin myyntivaluuttana. Toisin kuin kustannus, hinnastossa määritetty myyntihinta ei voi olla koskaan eri kuin projektin myyntivaluutta. Ei ole skenaariota, jossa valuutan muuntamista tarvittaisiin. **Arviot**-ruudukossa näkyvät kaikki myyntiarviot ja niiden yhteenveto projektin myyntivaluuttana. 

[!INCLUDE[footer-include](../includes/footer-banner.md)]
