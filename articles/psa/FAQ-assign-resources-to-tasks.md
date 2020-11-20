---
title: Kohdenna resurssi tehtävälle
description: Tässä aiheessa on tietoja resurssien kohdentamisesta tehtäville.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 9/27/2019
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: b7aef799ec4b90d602a6f3641cbac06264664f00
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/28/2020
ms.locfileid: "4125129"
---
# <a name="assign-a-resource-to-a-task"></a>Kohdenna resurssi tehtävälle

Microsoft Dynamics 365 Project Service Automationissa resursseja voi kohdentaa tehtävälle kolmella eri tavalla.

## <a name="book-a-resource-as-a-team-member-and-then-assign-the-resource-to-a-task"></a>Resurssin varaaminen ryhmän jäseneksi ja resurssin kohdentaminen tehtävälle

Voit lisätä resurssin projektiryhmään ja kohdentaa resurssin projektiaikataulun tehtäville.

1. Lisää uusi ryhmän jäsen **Ryhmän jäsen** -välilehdelle valitsemalla **Uusi**. 

2. Näkyviin tulee **Ryhmän jäsenen pikaluonti** -paneeli, jossa voit valita varattavissa olevan resurssin nimen ja määrittää sen roolin. 

    Valitse jokin seuraavista resurssin varauksen kohdennustavoista:

    - **Täysi kapasiteetti** varaa resurssin täyden kapasiteetin tietyn alku- ja loppupäivämäärän välille.
    - **Kapasiteettiprosentti** varaa resurssin kapasiteettiprosentin perusteella tietyn alku- ja loppupäivämäärän välille.
    - **Tuntien mukaan – jaa tasaisesti** varaa resurssin tietyille tunneille. Tunnit jaetaan tasan päivää kohti tietyn alku- ja loppupäivämäärän väliselle ajalle.
    - **Tuntien mukaan – etupainotteinen** varaa resurssin tietyille tunneille. Päiväkohtaiset tunnit jaetaan etupainotteisesti tietyn alku- ja loppupäivämäärän väliselle ajalle.
    - **Ei mitään** -vaihtoehto lisää ryhmään resurssin, mutta ei luo varauksia, jotka käyttävät resurssin kapasiteettia.

3. Valitse tehtävän **Aikataulut**-ruudukossa resurssin solun **Resurssi**-kuvake ja valitse sitten **Ryhmän jäsenet** -kohdasta juuri lisätty ryhmän jäsen. 

> [!NOTE]
> Resurssin varatut tunnit ja kohdennetut tunnit näkyvät sekä **Ryhmän jäsen**- että **Täsmäytys**-välilehdessä. Tuntien pitäisi olla samat, mutta se ei ole pakollista, koska varaukset ja kohdennukset eivät ole tiiviissä yhteydessä toisiinsa. **Täsmäytys**-välilehti sisältää tietoja, jos tuntien määrät eivät ole samat. Näin voi käydä, jos esimerkiksi resurssille kohdennettuja tunteja on enemmän kuin varattuja tunteja. Tarvittaessa voit korjata tietoja laajentamalla resurssin varauksia tai muuttamalla kohdennusta.

## <a name="create-a-generic-team-member-through-task-assignment"></a>Yleisen ryhmän jäsenen luominen tehtäväkohdennuksen kautta

Kun luot yleisen ryhmän jäsenen tehtäväkohdennuksella, luot ensin paikkamerkin tai yleisen resurssin, joka kuvaa sen nimetyn resurssin ominaisuudet, jonka haluat lopulta suorittavan tehtäviä. Tämän jälkeen voit luoda tarpeen (tai lähettää pyynnön käyttämällä tarvetta), jota käytetään nimetyn resurssin haussa ja varauksessa.

1. Valitse tehtävän **Aikataulut**-ruudukossa **Resurssi**-kuvake resurssin solussa.

2. Kirjoita nimi, joka toimii resurssin nimen paikkamerkkinä. Esimerkiksi ohjelmapäällikkö.

3. Valitse **Luo** ja määritä yleisen resurssin rooli kentässä **Projektiryhmän jäsenen pikaluonti**.

4. Voit jatkaa tehtävien delegoimista tälle paikkamerkin resurssille valitsemalla tehtävälle resurssin **Resurssinvalitsin**-kohdasta. Ne löytyvät **Ryhmän jäsenet** -kohdasta.

5. Kun olet kohdentanut yleisen resurssin, valitse se **Ryhmä**-välilehdessä ja valitse sitten **Luo tarve** luodaksesi resurssitarpeen yleiselle resurssille.

6. Valitse yleisen resurssin **Varaa**-kohta. Tämän jälkeen voit etsiä aikataulutaulukon avulla todellisen resurssin ja varata sen. Voit myös lähettää tarpeen resurssipäällikön tekemälle toteutukselle.

7. Kun yleinen resurssi toteutetaan nimetyn resurssin kanssa, yleinen resurssi poistetaan ryhmästä ja yleisen resurssin tehtävän delegoinnit delegoidaan nimetylle resurssille, joka toteutti yleisen resurssin resurssitarpeen.

## <a name="assign-a-named-resource-from-the-list-of-all-bookable-resources"></a>Nimetyn resurssin kohdentaminen kaikkien varattavissa olevien resurssien luettelosta

**Resurssinvalitsin**-kohdan hakuruudun avulla voit hakea kaikki varattavissa olevat resurssit ja kohdentaa ne tehtävälle.

Tällä tavoin kohdennetut resurssit lisätään ryhmään ilman varauksia. tämä vastaa ryhmän jäsenen lisäämistä ja Ei mitään -kohdennusmenetelmän valitsemista. Resurssi näkyy **Ryhmä**- ja **Täsmäytys**-välilehdessä resurssina, jolla on vain kohdennuksia. Sillä on varausvaje. Varaa ne, jos haluat käyttää niitä.

1. Valitse tehtävän **Aikataulut**-ruudukossa **Resurssi**-kuvake resurssin solussa.

2. Aloita kirjoittamalla nimi. Nimen hakutulokset näkyvät **Muut resurssit**-kohdan kohdassa **Resurssinvalitsin**.

3. Valitse resurssi, jonka haluat kohdentaa tehtävälle.

