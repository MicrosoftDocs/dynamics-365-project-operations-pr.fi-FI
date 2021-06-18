---
title: Tarjouksen sulkeminen
description: Tämä aihe tarjoaa tietoja tarjousten sulkemisesta Project Operationsissa.
author: rumant
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 3f46bf61bc3e492a648d65e86750a25609d5ab7a
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/10/2021
ms.locfileid: "5995932"
---
# <a name="close-a-quote"></a>Tarjouksen sulkeminen

_**Käytetään:** Project Operationsin resursseihin ja ei-varastoitaviin perustuvissa skenaarioissa_

Projektitarjous voidaan sulkea voitettuna tai hävittynä. Voit sulkea tarjousluonnoksen, koska Microsoft Dynamics 365 Project Operations ei tue tarjousten Aktivoi- ja Muuta-toimintoja.

## <a name="close-a-quote-as-won"></a>Tarjouksen sulkeminen voitettuna

Projektitarjouksen sulkeminen voitettuna sulkee määrittää tilaksi **Suljettu** ja tilan syyksi **Voitettu**. Kun suljet tarjouksen, projektitarjous on vain luku -muodossa ja luo kaikki tarjoustiedot sisältävän projektisopimusluonnoksen. Koska suljettua tarjousta ei voi avata uudelleen, ennen kuin suljet tarjouksen, vahvistusikkuna vahvistaa tekemäsi muutokset.

Projektitarjouksesta luotu projektisopimus on myös käytettävissä Project Operationsin Projektinhallinta ja kirjanpito -moduulissa. Jos projektisopimusta ei ole yhdistetty projektiin millään sen rivillä, tämä projektisopimus on käytettävissä passiivisena projektisopimuksena, ja se aktivoituu heti, kun projekti on yhdistetty vähintään yhteen sen sopimusriveistä.

Jos tarjous liitetään mahdollisuuteen, kaikki muut mahdollisuuteen liittyvät projektitarjoukset suljetaan automaattisesti hävittyinä.

### <a name="financial-impact-of-closing-a-quote-as-won"></a>Taloudellinen vaikutus, kun tarjous suljetaan voitettuna

Jos projektiin on tallennettu ajan toteutuneita arvoja, kun se on vielä liitetty tarjousluonnokseen, vain ajan tai kulun kustannukset tallennetaan. Kun tarjous on suljettu voitettuna, sovellus määrittää kustannukset uudelleen peruuttaen vanhat toteutuneet kustannukset ja luoden uudelleen uudet toteutuneet kustannukset. Sovellus käsittelee nämä toteutuneet kustannukset liitetyn projektisopimusrivin laskutusmenetelmän mukaan. Jos toteutuneet kustannukset viittaavat aika- ja materiaalisopimusriviin, järjestelmä luo automaattisesti vastaavat laskuttamattomat myynnin toteutuneet arvot, kun tarjous suljetaan ja projektisopimus luodaan. Jos kustannusten todelliset tiedot viittaavat kiinteähintaiseen sopimusriviin, sovellus lopettaa kustannusten uudelleenkäsittelyn projektisopimusasiakkaiden laskutuksen jakamisen sääntöjen perusteella.

Kaikki uudelleenkäsitellyt todelliset arvot ovat käytettävissä Projektinhallinta ja kirjanpito -moduulissa, jotta projektin kirjanpitäjä voi tarkastella, päivittää ja kirjata kirjanpitoon. 

## <a name="close-a-quote-as-lost"></a>Tarjouksen sulkeminen hävittynä

Jos projektitarjous suljetaan hävittynä, tilaksi tulee **Suljettu** ja tilan syyksi **Hävitty**. Kun tarjous suljetaan, se on vain luku -tilassa. Koska suljettua tarjousta ei voi avata uudelleen, ennen kuin suljet tarjouksen, vahvistusikkuna vahvistaa tekemäsi muutokset.

Jos hävittynä suljetulla projektitarjouksella on projekti, johon on viitattu jossakin tarjouksen riveillä, projekti merkitään myös suljetuiksi ja kaikki kyseisestä päivästä eteenpäin tehdyt resurssivaraukset peruutetaan.

> [!NOTE]
> Project Operationsissa tarjouksen sulkeminen voitettuna tai hävittynä ei vaikuta mahdollisuuden tilaan, joka säilyy avoimena, kunnes se suljetaan manuaalisesti.


[!INCLUDE[footer-include](../includes/footer-banner.md)]