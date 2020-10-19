---
title: Tarjouksien sulkeminen
description: Tämä aihe tarjoaa tietoja tarjousten sulkemisesta Project Operationsissa.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: cc3b2cdeb1ac46b7d927c1f96e94e9154d3eebf8
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/28/2020
ms.locfileid: "3896187"
---
# <a name="close-quotes"></a>Tarjouksien sulkeminen 

_**Käytetään:** Lite-käyttöönotto – kauppa proformalaskutukseen_

Projektitarjous voidaan sulkea voitettuna tai hävittynä. Tarjousten Aktivoi- ja Tarkista-toimintoja ei tueta Microsoft Dynamics 365 Project Operationsissa, joten tarjousluonnos voidaan sulkea.

## <a name="close-a-quote-as-won"></a>Tarjouksen sulkeminen voitettuna

Projektitarjouksen sulkeminen voitettuna sulkee tarjouksen määrittäen tilaksi Suljettu ja tilan syyksi Voitettu. Kun suljet tarjouksen, projektitarjous on vain luku -muodossa ja luo tarjoustiedot sisältävän projektisopimusluonnoksen. Koska suljettua tarjousta ei voi avata uudelleen, näkyviin tulee vahvistusikkuna ennen muutosten tekemistä – muutokset ovat peruuttamattomia.

Jos tarjous liitetään mahdollisuuteen, kaikki muut mahdollisuuteen liittyvät projektitarjoukset suljetaan automaattisesti hävittyinä.

### <a name="financial-impact-of-closing-a-quote-as-won"></a>Taloudellinen vaikutus, kun tarjous suljetaan voitettuna

Jos projektiin on tallennettu ajan toteutuneita arvoja, kun se on vielä liitetty tarjousluonnokseen, vain ajan tai kulun kustannukset tallennetaan. Kun tarjous on suljettu voitettuna, sovellus määrittää kustannukset uudelleen peruuttaen vanhat toteutuneet kustannukset ja luoden uudelleen uudet toteutuneet kustannukset. Sovellus käsittelee nämä toteutuneet kustannukset liitetyn projektisopimusrivin laskutusmenetelmän mukaan. Jos toteutuneet kustannukset viittaavat aika- ja materiaalisopimusriviin, järjestelmä luo automaattisesti vastaavat laskuttamattomat myynnin toteutuneet arvot, kun tarjous suljetaan ja projektisopimus luodaan. Jos kustannusten todelliset tiedot viittaavat kiinteähintaiseen sopimusriviin, sovellus lopettaa kustannusten uudelleenkäsittelyn projektisopimusasiakkaiden laskutuksen jakamisen sääntöjen perusteella.

## <a name="closing-a-quote-as-lost"></a>Tarjouksen sulkeminen hävittynä:

Jos projektitarjous suljetaan hävittynä, tilaksi tulee Suljettu ja tilan syyksi Hävitty. Kun tarjous suljetaan, projektitarjous siirtyy vain luku -tilaan. Koska suljettua tarjousta ei voi avata uudelleen, ennen kuin suljet tarjouksen, vahvistusikkuna vahvistaa tekemäsi muutokset.

Jos hävittynä suljetulla projektitarjouksella on projekti, johon on viitattu jossakin tarjouksen riveillä, projekti merkitään myös suljetuiksi ja kaikki kyseisestä päivästä eteenpäin tehdyt resurssivaraukset peruutetaan.

> [!NOTE]
> Project Operationsissa tarjouksen sulkeminen voitettuna tai hävittynä ei vaikuta mahdollisuuden tilaan, joka säilyy avoimena, kunnes se suljetaan manuaalisesti.
