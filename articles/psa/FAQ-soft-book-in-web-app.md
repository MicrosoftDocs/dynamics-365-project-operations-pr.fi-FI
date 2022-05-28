---
title: Miten varaan resursseja alustavasti sovellusversiossa 2.x?
description: Tässä artikkelissa kerrotaan, miten projektiryhmän jäseniä varataan alustavasti Project Service -sovelluksessa.
author: JohnPBurrows
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
ms.reviewer: johnmichalak
ms.openlocfilehash: 472529c146fbb5e7a4540676c880cabd4ab1a32b
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/14/2022
ms.locfileid: "8585190"
---
# <a name="how-do-i-soft-book-resources-in-the-web-app-project-service-app-v2x"></a>Miten varaan resursseja alustavasti verkkosovelluksessa (Project Service -sovelluksen versio 2.x)?

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1.x-2.x](../includes/cc-applies-to-psa-app-1x-2x.md)]

Voit ajoittaa tai varata resurssin alustavasti projektiryhmään, jolloin resurssin projektiin delegoimista koskeva suunnitelma näkyy muille. Alustavat varaukset eivät kuluta resurssin käytettävissä olevaa kapasiteettia. Alustavasti varattuja ryhmän jäseniä ei voi delegoida projektitehtäville. Vain resurssit, joiden tila on Varattu sitovasti ja vahvistustyyppi on Vahvistettu, voidaan delegoida tehtäville (jos niillä on delegoinnin työn vaatima määrä sitovan varauksen tunteja).

Alustavasti varatut projektiryhmän jäsenet näkyvät Ryhmän jäsen -ruudukossa niin, että heidän alustavasti varatut tuntinsa näkyvät Alustava varaus -sarakkeessa. Ne näkyvät myös aikataulutaulukossa. Ne eivät osoita kapasiteetin kulutusta, koska alustava varaus ei kuluta resurssin kapasiteettia.

Project Service -sovelluksen versiossa 2.x ryhmän jäsenen voi varata projektiin alustavasti kolmella eri tavalla. Voit tehdä alustavan varauksen aikataulutaulukossa Ylläpidä varauksia -toiminnon avulla tai luomalla yleisen resurssin. Nämä tavat esitellään alla.

## <a name="soft-book-with-the-schedule-board"></a>Alustava varaus aikataulutaulukon avulla

Voit tehdä alustavan varauksen aikataulutaulukon avulla seuraavasti: 
1. Avaa aikataulutaulukko.
2. Valitse Projekti-välilehden aikataulutaulukon Varaustarpeet-paneeli.
3. Etsi projekti, jonka resurssin haluat varata alustavasti. Jos sinulla on useita projekteja, valitse Projekti-sarakkeen otsikko ja etsi projekti suodattimen avulla.
4. Valitse projekti, vedä se resurssin aikaruudukkoon ja pudota projekti sinne.
5. Oikealla oleva Luo resurssin varaus -paneeli avautuu. Muokkaa alku- ja loppupäivämäärää, valitse varauksen tilaksi ALustava ja määritä tunnit. 
6. Valitse Varaa.
7. Resurssi näkyy nyt projektissa ryhmän jäsenenä, jolla on alustavasti varattuja tunteja Alustava varaus -sarakkeessa.

Huomaa, että et voi delegoida niitä työrakenteen tehtäville, koska resurssit on varattava sitovasti ryhmässä delegointia varten.

## <a name="soft-book-using-the-maintain-bookings-feature"></a>Alustava varaus Ylläpidä varauksia -toiminnon avulla

Voit tehdä alustavan varauksen Ylläpidä varauksia -toiminnon avulla seuraavasti:
1. Valitse ryhmän jäsenen ruudukossa Uusi.
2. Valitse varattavan resurssin roolin alku ja loppu.
3. Valitse kohdistustavaksi jokin seuraavista (tapa ei voi olla Ei mitään):
- Täysi kapasiteetti
- Kapasiteettiprosentti
- Tuntien mukaan – jaa tasaisesti
- Tuntien mukaan – etupainotteinen
4. Valitse Tallenna. Resurssi näkyy ryhmän ruudukossa. Resurssin tunnit näkyvät sitovasti varattuina.
5. Ylläpidä resurssin varauksia valitsemalla Ylläpidä varauksia.
6. Kun aikataulutaulukko avautuu, laajenna resurssia niin, että varaukset näkyvät. Varaus näkyy sitovana varauksena.
7. Napsauta varausta hiiren kakkospainikkeella Muuta tilaa -kohdassa. Valitse Alustava varaus ja sitten Alustava. Varauksen tila on nyt Alustava.
8. Kun aikataulutaulukko suljetaan, näet, että resurssin tuntien varaus on muuttunut sitovasta alustavaksi ryhmän jäsenen ruudukossa.
Huomaa, että jos varaat resurssin sitovasti ryhmälle, delegoit työrakenteen tehtävät ja muutat tilan Ylläpidä varauksia -toiminnon avulla sitovasta alustavaksi, kyseisen resurssin tehtävien delegoinnit poistetaan. Näin tehdään sen vuoksi, että vain sitovasti varattuja resursseja voi delegoida tehtäville.

## <a name="soft-book-by-creating-a-generic-resource"></a>Tee alustava varaus luomalla yleinen resurssi

Voit luoda alustavan varauksen luomalla yleisen resurssin ryhmän jäsenen, täyttämällä aikataulutaulukon tai resurssipyynnön ja muuttamalla tyyppiä varauksen aikana.
Voit tehdä niin seuraavasti:

1. Delegoi roolit projektin työrakenteen niihin tehtäviin, joille haluat luoda yleisen ryhmän jäsenet.
2. Valitse Luo projektiryhmä.
3. Valitse projektiryhmän ruudukossa yleinen resurssi ja valitse sitten Varaa.
4. Valitse aikataulutaulukossa varattava resurssi.
5. Muuta aikataulutaulukon Luo resurssin varaus -paneelissa varauksen tilaksi Alustava.
6. Valitse Varaa tai Varaa ja lopeta.

Kun olet sulkenut aikataulutaulukon, valittu Alustava-tilassa oleva resurssi ja sen delegoidut tunnit näkyvät ryhmässä. Näet myös, että yleinen resurssi on yhä ryhmässä. Se osoittaa, että tehtävät on delegoitu alustavasti varatulle ryhmän jäsenelle.

Kun olet valmis muuttamaan alustavasti varatun ryhmän jäsenen resurssin sitovasti varatuksi ryhmän jäseneksi, jolle voi delegoida tehtäviä, tee seuraavat toiminnot:

1. Valitse resurssi ja valitse sitten Ylläpidä varauksia -kohta.
2. Kun aikataulutaulukko avautuu, laajenna resurssia niin, että varaukset näkyvät. Näkyviin tulee varaus, joka on merkitty alustavaksi.
3. Napsauta varausta hiiren kakkospainikkeella Muuta tilaa -kohdassa. Valitse Sitova varaus ja sitten Sitova. Varauksen tila on nyt Sitova.
4. Kun aikataulutaulukko suljetaan, näet, että resurssin tuntien varaus on muuttunut alustavasta sitovaksi ryhmän jäsenen ruudukossa. Voit nyt delegoida resurssin tehtäville (jos tehtävän sitovasti varatut tunnit ja työtunnit vastaavat toisiaan delegoinnissa). Huomaa, että jos seurasit yleisen resurssin täyttämisen vaiheita ylempänä kohteessa kolme, kun muutit alustavasti varatun resurssin tilan sitovaksi, yleisen ryhmän jäsen poistetaan ryhmästä.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
