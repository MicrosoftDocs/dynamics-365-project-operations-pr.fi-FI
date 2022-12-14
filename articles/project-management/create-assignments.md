---
title: Luo resurssien delegoinnit
description: Tässä artikkelissa on tietoja yleisten ja nimettyjen resurssien delegointien luomisesta.
author: ruhercul
ms.date: 11/22/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: 42dd2906ce8db8844bf4dea232f24aca58a5d951
ms.sourcegitcommit: 9b1136d95f19cc039d675a4a1b0962ca3ec61646
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/30/2022
ms.locfileid: "9811989"
---
# <a name="create-resource-assignments"></a>Luo resurssien delegoinnit

_**Koskee:** Project Operationsin resurssiin / muuhun kuin resurssiin perustuvia skenaarioita, Lite-käyttöönotto-kaupasta proformalaskutukseen_


Resurssin delegointi on suora yhteys projektitiimin jäsenestä lehtisolmutehtävään. Tässä artikkelissa on tietoja eri tavoista delegoida resursseja.

## <a name="create-a-generic-team-member-through-task-assignment"></a>Yleisen ryhmän jäsenen luominen tehtäväkohdennuksen kautta


Kun luot yleisen ryhmän jäsenen tehtävän delegoinnin avulla, luot paikkamerkin tai yleisen resurssin. Tämä yleinen resurssi kuvaa sen nimetyn resurssin ominaisuudet, jonka haluat suorittavan tehtävät. Tämän jälkeen voit luoda tarpeen tai lähettää pyynnön käyttämällä tarvetta, jota käytetään nimetyn resurssin haussa ja varauksessa.

1. Valitse tehtävän Aikataulut-ruudukossa Resurssi-kuvake **Resurssi**-solussa.
2. Kirjoita nimi, joka toimii resurssin nimen paikkamerkkinä. Esimerkiksi ohjelmapäällikkö.
3. Valitse **Luo** ja määritä yleisen resurssin rooli kentässä **Projektiryhmän jäsenen pikaluonti**.
4. Delegoi tarpeen mukaan tehtäviä tälle paikkamerkkiresurssille valitsemalla tehtävälle resurssi **Resurssinvalitsin**-kohdasta. Resurssit löytyvät **Ryhmän jäsenet** -kohdasta.
5. Kun olet kohdentanut yleisen resurssin, valitse se **Ryhmä**-välilehdessä, valitse yleinen resurssi ja valitse sitten **Luo tarve** luodaksesi resurssitarpeen yleiselle resurssille.
6. Valitse yleisen resurssin **Varaa**-kohta. Tämän jälkeen voit etsiä todellisen resurssin ja varata sen aikataulutaulukon avulla. Voit myös lähettää tarpeen resurssipäällikön tekemälle toteutukselle.
7. Kun yleinen resurssi on täytetty nimetyllä resurssilla, yleinen resurssi poistetaan ryhmästä. (Osittainen resurssitarpeen täyttäminen ei johda resurssin delegointiin.) Yleisen resurssi tehtävät delegoidaan nimetylle resurssille, joka täytti yleisen resurssin resurssitarpeen.

## <a name="assign-a-named-resource-from-the-list-of-all-bookable-resources"></a>Nimetyn resurssin kohdentaminen kaikkien varattavissa olevien resurssien luettelosta

**Resurssinvalitsin**-kohdan hakuruudun avulla voit hakea kaikki aktiiviset varattavissa olevat resurssit ja kohdentaa ne mille tahansa lehtisolmutehtävälle. Tällä tavoin kohdennetut resurssit lisätään ryhmään ilman varauksia. tämä vastaa ryhmän jäsenen lisäämistä ja **Ei mitään** -kohdennusmenetelmän valitsemista. Resurssi näkyy **Ryhmä**, **Resurssin delegointi**- ja **Täsmäytys**-välilehdessä resurssina, jolla on vain delegointeja ja varausvaje. Varaa ne, jos haluat käyttää niitä.

1. Siirry tehtävän ruudukkoon, taulukoon tai aikajanaan ja soluun **Vastuuhenkilö**.
2. Ala kirjoittaa nimeä hakuruutuun. Nimen hakutulokset näkyvät **Muut resurssit**-kohdan kohdassa **Resurssinvalitsin**.
3. Valitse resurssi, jonka haluat delegoida tehtävälle, tai valitse resurssin nimi kohdassa **Muut ryhmän resurssit**.

## <a name="editing-resource-assignment-contours"></a>Resurssien määrityksen jaksotuksen muokkaaminen

Kun resurssit on delegoitu aikataulussa tehtävään, työtehtävät jakautuvat oletusarvoisesti lineaarisesti kullekin resurssille resurssin työajan ja projektin aikataulutilan mukaan. Projektipäällikkö voi tarkentaa resurssin delegointiruudukon avulla kunkin yhdelle tai usealle tehtävälle eri aika-asteikolla määritetyn resurssin työmääräarvioita. Tämän ominaisuuden avulla projektipäälliköt voivat laatia tarkkoja kustannus- ja myyntiarvioita, jotka perustuvat resurssin delegoinnissa tehtyihin resurssin määritystoimintoihin, jotka luodaan resurssin delegoinnin yhteydessä tehtävään. Lisäksi projektipäälliköt voivat helpommin heijastaa resurssin tarvetta, jota tarvitaan kysynnän luomiseen resurssitarpeessa.

### <a name="navigation"></a>Siirtyminen

Projektipäällikkö valitsee resurssiruudukon käyttöä varten ensin **Tehtävät**-välilehden projektin aloitussivulla ja sitten **Kohdennukset**-välilehden.

![Projektin pääsivun Tehtävät-välilehden Määritykset-välilehti.](media/AssignmentGrid.png)

Ruudukko tukee kahta ryhmittelymenetelmää: ryhmitteleminen  **resurssin mukaan** ja **tehtävän mukaan**. Toisin kuin ruudukkonäkymässä, sarakkeita ei voi määrittää. Ainoat näkyvät sarakkeet ovat **Delegoitu henkilölle**, **Tehtävän nimi**, **Delegoinnin alku**, **Delegoinnin loppu** ja **Delegoinnin työmäärä**.

Kun ruudukko hahmonnetaan alustavasti, se alkaa varhaisimmasta tehtävästä. Jos aikataulussasi ei ole työtehtäviä, ruudukko on tyhjä eikä siinä hahmonneta mitään.

![Tyhjä määritysruudukko.](media/emptyassignmentgrid.png)

Jos haluat tarkastella tehtäviä ja eri aika-asteikkoja, käytettävissä ovat myös vain luku - resurssin määritysruudukko ja resurssien täsmäytysruudukko.

### <a name="resource-calendars"></a>Resurssikalenterit

Resurssikalenterissa näkyvät resurssin työpäivät säätelevät kykyä muokata tietyn päivän tehtävää. Jos tietyn resurssin solu on poistettu käytöstä, resurssilla ei ole kyseisenä ajanjaksona työpäiviä.

Resurssin aikarajat voivat olla delegoitujen tehtävien nykyisten alkamis- ja päättymispäivämäärien ulkopuolella. Jos tehtävää päivitetään niin, että se on tehtävän viimeisen päättymispäivän tai tehtävän varhaisimman alkamispäivän jälkeen, tehtävän päättymispäivää tai alkamispäivää muutetaan tarpeen mukaan. Jos päivitys kuitenkin tehdään niin, että se on vanhempi kuin edeltävään tehtävään linkitetyn tehtävän alkamispäivä, päivitys epäonnistuu, koska määritys käynnistää tehtävän, ennen kuin sen edeltäjä on valmis, ja tätä toimintaa ei tällä hetkellä tueta.

### <a name="co-authoring"></a>Sisällön tuottaminen yhdessä

Resurssien määritysruudukkoon tehdyt muutokset näkyvät automaattisesti kaikissa liitetyissä näkymissä, kuten kaavio-, aikajana-, taulukko- ja ruudukkonäkymissä. Jos useat käyttäjät tarkastelevat projektia samanaikaisesti, yhden käyttäjän tekemät muutokset näkyvät ruudukossa. Vastaavasti resurssin määritysruudukossa tehdyt muutokset näytetään kaikille muille käyttäjille, jotka tarkastelevat projektia samassa istunnossa.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
