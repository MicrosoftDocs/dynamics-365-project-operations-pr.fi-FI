---
title: Tarjouksen sulkeminen – lite
description: Tämä aihe tarjoaa tietoja tarjousten sulkemisesta Project Operationsissa.
author: rumant
ms.date: 10/01/2020
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: bde4794c19dd69b6dd77abf5483c674cd7503d23
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/14/2022
ms.locfileid: "8574702"
---
# <a name="close-a-quote---lite"></a>Tarjouksen sulkeminen – lite

_**Käytetään:** Lite-käyttöönotto – kauppa proformalaskutukseen_

Projektitarjous voidaan sulkea voitettuna tai hävittynä. Tarjousluonnos voidaan sulkea, koska Microsoft Dynamics 365 Project Operations ei tue tarjousten Aktivoi- ja Muuta-toimintoja.

## <a name="close-a-quote-as-won"></a>Tarjouksen sulkeminen voitettuna

Kun suljet projektitarjouksen voitettuna, sen tilaksi tulee Suljettu ja tilan syy on Voitettu. Kun suljet tarjouksen, projektitarjous on vain luku -muodossa ja luo tarjoustiedot sisältävän projektisopimusluonnoksen. Suljettua tarjousta ei voi avata uudelleen, joten vahvistusikkuna vahvistaa tekemäsi muutokset.

Jos tarjous liitetään mahdollisuuteen, kaikki muut mahdollisuuteen liittyvät projektitarjoukset suljetaan automaattisesti hävittyinä.

### <a name="financial-impact-of-closing-a-quote-as-won"></a>Taloudellinen vaikutus, kun tarjous suljetaan voitettuna

Jos projektissa on vielä toteutuneita aikatietoja, jotka on vielä liitetty tarjousluonnokseen, vain ajan tai kulujen kustannukset tallennetaan. Kun tarjous on suljettu voitettuna, sovellus määrittää kustannukset uudelleen peruuttaen vanhat toteutuneet kustannukset ja luoden uudelleen uudet toteutuneet kustannukset. Sovellus käsittelee nämä toteutuneet kustannukset liitetyn projektisopimusrivin laskutusmenetelmän mukaan. Jos toteutuneet kustannukset liittyvät ajan ja materiaalin sopimusriviin, vastaavat laskuttamattomat toteutuneet myynnit luodaan, kun tarjous suljetaan ja projektisopimus luodaan. Jos toteutuneet kustannukset liittyvät kiinteän hinnan sopimusriviin, sovellus lopettaa sellaisten toteutuneiden kustannusten uudelleenkäsittelyn, jotka perustuvat projektisopimusasiakkaita koskevien jaetun laskutuksen sääntöihin.

## <a name="closing-a-quote-as-lost"></a>Tarjouksen sulkeminen hävittynä:

Kun suljet projektitarjouksen hävittynä, sen tilaksi tulee Suljettu ja tilan syy on Hävitty. Kun tarjous suljetaan, projektitarjous siirtyy vain luku -tilaan. Koska suljettua tarjousta ei voi avata uudelleen, ennen kuin suljet tarjouksen, vahvistusikkuna vahvistaa tekemäsi muutokset.

Jos hävittynä suljettu projektitarjous viittaa projektiin riveillään, myös se projekti merkitään suljetuksi. Kaikki kyseisestä päivästä eteenpäin tehdyt varaukset peruutetaan.

> [!NOTE]
> Project Operationsissa tarjouksen sulkeminen voitettuna tai hävittynä ei vaikuta mahdollisuuden tilaan, joka säilyy avoimena, kunnes se suljetaan manuaalisesti.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]