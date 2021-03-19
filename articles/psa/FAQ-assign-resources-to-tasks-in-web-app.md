---
title: Miten delegoin varattavissa olevan resurssin tehtävälle verkkosovelluksessa
description: Yleiskatsaus tapoihin, joilla varattavissa olevia resursseja voidaan delegoida.
author: JohnPBurrows
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 8/21/2018
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: b4296837cabd4c6f7e2d2924079658e45ce8b87c
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5286289"
---
# <a name="how-do-i-assign-a-bookable-resource-to-a-task-in-the-web-app-project-service-app-v2x"></a>Miten delegoin varattavissa olevan resurssin tehtävälle verkkosovelluksessa (Project Service -sovelluksen versio 2.x)?

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1.x-2.x](../includes/cc-applies-to-psa-app-1x-2x.md)]

Resurssin voi delegoida tehtävälle kahdella eri tavalla Project Service -sovelluksessa. Voit varata resurssin ryhmän jäsenenä ja delegoida sen sitten tehtävälle. Vaihtoehtoisesti voit luoda yleisen ryhmän jäsenen roolin tehtävän delegointien kautta, luoda sitten ryhmän ja täyttää taustalla olevat tarpeet nimetyn resurssin avulla.

Huomaa, että jos haluat delegoida varattavissa olevan resurssin tehtävälle, varattavissa olevan resurssin ryhmän jäsenellä on oltava riittävästi käytettävissä olevia varauksia. Varauksen tilan vahvistustyypin on oltava Sitova varaus ja tilan on oltava Vahvistettu. Jos resurssilla ei ole riittävästi varauksia, Project Service poistaa delegoinnin ja näyttää seuraavan virhesanoman:

*Resurssia ei voi delegoida tehtävälle - Seuraaville resursseille ei ole varattu riittävästi tunteja projektissa*

## <a name="book-a-resource-as-a-team-member-and-then-assign-the-resource-to-a-task"></a>Varaa resurssi ryhmän jäsenenä ja delegoi resurssi sitten tehtävälle.

Kun tämä tapa on käytössä resurssi lisätään projektiryhmään. Tämän jälkeen delegoidaan tehtävät projektiaikataulun resurssille. Tämä tehdään seuraavasti:
1.  Lisää uusi ryhmän jäsen ryhmän jäsenen ruudukkoon valitsemalla **Uusi**.
2.  Valitse ryhmän jäsenen pikaluontinäytössä varattavissa olevan resurssin nimi ja määritä rooli.
3.  Valitse **alku**- ja **loppupäivämäärät**.

    > [!div class="mx-imgBorder"] 
    > ![Kuvakaappaus ryhmän jäsenen lisäämisestä](media/FAQ-Resources-to-Tasks2-1.png "Kuvakaappaus ryhmän jäsenen lisäämisestä")
 
4.  Valitse jokin seuraavista resurssin varauksen kohdistustavoista:
    - **Täysi kapasiteetti** varaa resurssin täyden kapasiteetin tietyn alku- ja loppupäivämäärän välille.
    - **Kapasiteettiprosentti** varaa resurssin kapasiteettiprosentin perusteella tietyn alku- ja loppupäivämäärän välille.
    - **Tuntien mukaan – jaa tasaisesti** varaa resurssin tietyille tunneille. Aika jaetaan tasan päivää kohti tietyn alku- ja loppupäivämäärän väliselle ajalle.
    - **Tuntien mukaan – etupainotteinen** varaa resurssin tietyille tunneille. Päiväkohtaiset tunnit jaetaan etupainotteisesti tietyn alku- ja loppupäivämäärän väliselle ajalle.

    Älä valitse **Ei mitään** -tapaa, koska se lisää resurssin ryhmään, mutta ei luo varauksia, jotka käyttävät resurssin kapasiteettia.
5.  Valitse **Tallenna**.

    Huomaa, että varauksen tunteja on oltava riittävästi, jotta ne kattavat työtunnit ja sen tehtävän päivämäärävälit, jolle tämä resurssi delegoidaan. Jos ne eivät vastaa toisiaan, et voi delegoida resurssia tehtävälle.

6.  Valitse tehtävän työrakenteessa resurssin solun avattava luettelo. Tee seuraavaksi näin: 

    1. Valitse **Lisää**.
    2. Valitse **Resurssit**-kohdan alla oleva avattava luettelo ja valitse aiemmin lisäämäsi ryhmän jäsen.
    3. Valitse **OK**. Ryhmän jäsen on nyt delegoitu tehtävälle.

    > [!div class="mx-imgBorder"] 
    > ![Näyttökuva resurssien lisäämisestä työrakenteen avulla](media/FAQ-Resources-to-Tasks2-2.png "Näyttökuva resurssien lisäämisestä työrakenteen avulla")
 
Ryhmän jäsenen ruudukon Delegoidut tunnit -kohdassa on resurssin delegoitujen tuntien kooste. Se on yhtä suuri tai pienempi kuin resurssin varatut tunnit. 

> [!div class="mx-imgBorder"] 
> ![Resurssin delegoitujen tuntien näyttökuva](media/FAQ-Resources-to-Tasks2-3.png "Resurssin delegoitujen tuntien näyttökuva")
 
Jos tehtävä, jota yrität delegoida resurssille, alkaa resurssin varausten loppupäivämäärän jälkeen, resurssi ei näy avattavassa luettelossa.

Huomaa, että voit delegoida resurssin varattujen tunteja useammille tunneille, jos resurssilla on jäljellä delegoimatonta kapasiteettia. Tässä tapauksessa resurssi on vain osittain delegoitu varausten perusteella. Näet jäljellä olevat delegoimattomat tehtävän tunnit, kun lisäät työrakenteeseen Resursoimattomat tunnit -sarakkeen.

Jos resurssit on delegoitu niiden varatuille tunneille (varattuja tunteja on yhtä paljon kuin delegoituja tunteja), näkyviin tulee seuraava virhesanoma, kun yrität delegoida niille uusia tehtäviä:

*Resurssia ei voi delegoida tehtävälle - Seuraaville resursseille ei ole varattu riittävästi tunteja projektissa.*

Lisäksi projektipäällikön ryhmän oletusjäsen, joka on lisätty ryhmään projektin luomisen yhteydessä, on lisätty ilman varauksia. Hänelle ei voi delegoida tehtäviä. Ne eivät näy resurssin tehtävien avattavassa luettelossa.

Jos haluat delegoida tämän resurssin, poista se ryhmästä ja lisää uudelleen käyttämällä jotain muuta kohdistustapaa kuin Ei mitään. Jäsenet lisätään ryhmään projektin luontivaiheessa siksi, että projektissa on oletusarvoisesti vähintään yksi projektin hyväksyjä.

## <a name="create-a-generic-team-member-through-role-assignment-on-tasks"></a>Yleisen ryhmän jäsenen luominen roolin delegoinnin kautta tehtävissä

Tämä tapa varmistaa sen, että resursseilla on riittävästi tehtävien varauksia. Luo ensin paikkamerkki tai yleinen resurssi, joka kuvaa sen nimetyn resurssin ominaisuudet, jota haluat käsitellä tehtävissä. Tämä tapahtuu luomalla ryhmä sen jälkeen, kun tehtäville on delegoitu roolit. Tämä tehdään seuraavasti:

1. Valitse työrakenteessa tehtävä.
2. Valitse resurssin solun avattavan **Delegoitu rooli** -luettelon kuvake.
3. Valitse avattava **Rooli**-luettelo ja valitse yleisen resurssin rooli.
4. Valitse **OK**.

    > [!div class="mx-imgBorder"] 
    > ![Näyttökuva resurssin lisäämisestä työrakenteen avulla](media/FAQ-Resources-to-Tasks2-4.png "Näyttökuva resurssin lisäämisestä työrakenteen avulla")
 
Kun roolit on delegoitu tehtäville työrakenteessa, valitse **Luo projektiryhmä**. Project Service luo vähimmäismäärän yleisen ryhmän jäseniä näiden roolien, resursointiorganisaation yksiköiden ja projektikalenterin perusteella yhdistämällä tehtävien delegoinnit.

> [!div class="mx-imgBorder"] 
> ![Kuvakaappaus projektiryhmän luomisesta](media/FAQ-Resources-to-Tasks2-5.png "Kuvakaappaus projektiryhmän luomisesta")
 
Ryhmän jäsenen ruudukossa näkyvät yleisen resurssityypin resurssit ja niiden rooli sekä sijainnin nimi. Jos roolissa on oltava kaksi resurssia, jotta työ voidaan tehdä valmiiksi, Luo ryhmä -toiminto luo kaksi ryhmän jäsentä ja erottelee ne toisistaan sijainnin nimen avulla.

> [!div class="mx-imgBorder"] 
> ![Näyttökuva kahden yleisen resurssin lisäämisestä](media/FAQ-Resources-to-Tasks2-6.png "Näyttökuva kahden yleisen resurssin lisäämisestä")
 
Voit avata yleisen ryhmän jäsenen taustalla olevan resurssitarpeen valitsemalla Resurssitarve-kohdan alla olevan linkin.

> [!div class="mx-imgBorder"] 
> ![Näyttökuva taustalla olevan resurssitarpeen avaamisesta](media/FAQ-Resources-to-Tasks2-7.png "Näyttökuva taustalla olevan resurssitarpeen avaamisesta")

Valitse yleisen resurssin **Varaa**-kohta. Tämän jälkeen voit etsiä todellisen resurssin ja varata sen aikataulutaulukon avulla. Voit myös lähettää tarpeen resurssipäällikön tekemälle toteutukselle valitsemalla **Lähetä pyyntö**.

Kun yleinen resurssi toteutetaan nimetyn resurssin kanssa, yleinen resurssi poistetaan ryhmästä ja yleisen resurssin tehtävän delegoinnit delegoidaan nimetylle resurssille, joka toteutti yleisen resurssin resurssitarpeen.
 



[!INCLUDE[footer-include](../includes/footer-banner.md)]