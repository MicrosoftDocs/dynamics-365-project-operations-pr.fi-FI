---
title: Ennakkomaksut ja ennakkomaksuun perustuvat palvelusopimukset
description: Tässä aiheessa on tietoja siitä, miten tietoa pidätyspohjaisista sopimusmalleista ja ennakoista Project Operationsissa.
author: rumant
manager: Annbe
ms.date: 10/20/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 5ccf8ff4fa52fa6ff9fe534dfbe6736afc24ffba
ms.sourcegitcommit: f8edff6422b82fdf2cea897faa6abb51e2c0c3c8
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/21/2020
ms.locfileid: "4087889"
---
# <a name="advances-and-retainer-based-contracts"></a>Ennakkomaksut ja ennakkomaksuun perustuvat palvelusopimukset 


_**Käytetään:** Lite-käyttöönotto – kauppa proformalaskutukseen_

Dynamics 365 Project Operations tukee pidätykseen perustuvia palvelusopimuksia. Pidätykseen perustuva sopimus on neuvoteltu joukko yhtä hajautettuja maksuja, joista asiakasta laskutetaan projektin koko keston ajan. Tämäntyyppistä palvelusopimusta käytetään yleensä aika- ja materiaali- tai kulutuspohjaisissa laskutusmalleissa, joissa asiakkaalle on annettava ennustettavissa oleva lasku ja maksuaikataulu. Kunkin kauden kertyneet tuoton toteutuneet tuotot täsmäytetään asiakkaalta kauden alussa saadun maksun perusteella. Aika- ja materiaalilaskutusmallin käsitteen mukaisesti kullakin jaksolla kertyneet tuottoarvot voivat vaihdella kulujen mukaan. Jos kertynyt tuotto on suurempi kuin kauden alussa saatu summa, projektin toimitus yritys voi:

- Laskuttaa asiakasta vain ylimääräisestä 
- Siirtää tuoton täsmäyttämisen seuraavalle laskutusjaksolle ja tehdä viimeinen laskun projektin päättyessä jäljellä olevaan täsmäyttämättömään tuottoon

Perussopimuspohjaisen hankintamallin ja kiinteähintaisen sopimusmallin välinen suurin ero Project Operationsissa on se, että kiinteän hinnan sopimusmallissa laskun summa ei ole linkitetty tai sidottu aiheutuviin kustannuksiin. Laskutuksessa noudatetaan välitavoitteeseen perustuvaa lähestymistapaa, joka on kohdistettu kyseisellä jaksolla toteutuneista kustannuksista. Jos kyseessä on maksupalvelusopimus, laskutettava tuotto kirjataan sopimusrivin laskutusmenetelmän perusteella. Kun laskutustapa on aika ja materiaali, laskutettava myyntituotto on sidottu tiettynä ajan jaksona toteutuneista kustannuksista, ja se voi vaihdella kaudesta toiseen. Asiakkaalta laskutetaan kuitenkin vain kausittaisen maksun summa. Järjestelmä määrittää kauden lopussa toisen laskun täsmäyttäen kauden aikana kirjatun myyntituoton sen määrän perusteella, josta asiakasta on laskutettu kauden alussa.

Tämän menetelmän etuna on se, että asiakkaan kustannukset ovat ennustettavissa maksuaikataulussa toisin kuin tyypillisessä aika- ja materiaalimallissa. Projektin toimittajaorganisaatiolla on myös joitakin mahdollisuuksia periä kustannukset, jotka aiheutuvat siitä, että ne ovat nousseet pois siitä, että kiinteä hintamalli ei olisi sallinut niitä.

Kausittaisen ajankäyttösuunnitelman lisäksi Project Operations voi kirjata asiakkaalle kertaennakon ja täsmäyttää sen projektikustannusten eri osien perusteella.

Project Operationsin pidätys ei ole käytettävissä, ennen kuin se laskutetaan asiakkaalta. Tämä ilmaistaan seuraavissa aliruudukon kentissä ennakoina ja pidätyksinä.

| Field | Relevanssi, tarkoitus ja opastus | Loppupään vaikutus |
| --- | --- | --- |
| Käytettävissä oleva summa | Summa, joka on käytettävissä maksu- tai ennakkotietueessa. | Sitä ei voi käyttää, ennen kuin ennakko tai maksu on laskutettu, joten käytettävissä oleva summa on nolla. |
| Käytetty summa | Summa, joka on jo käytetty pidätyksissä tai ennakoissa. | Ennakko tai pidätys voidaan täsmäyttää laskuun, jolla on todelliset kustannukset ja jonka osa on merkitty jo käytetyksi tai kulutetuksi. Muu ennakko tai maksun summa on käytettävissä, jotta tulevaan laskuun voidaan täsmäyttää todelliset kustannukset. |
