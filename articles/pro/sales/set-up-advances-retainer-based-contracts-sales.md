---
title: Ennakkomaksut ja ennakkomaksuun perustuvat palvelusopimukset
description: Tässä aiheessa on tietoja siitä, miten tietoa pidätyspohjaisista sopimusmalleista ja ennakoista Project Operationsissa.
author: rumant
ms.date: 10/20/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 87e275cb72f1edc5a2a9913b4aa47d461d1f3d3d9bf177bf0ffba8b463f4ce01
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/06/2021
ms.locfileid: "6994407"
---
# <a name="advances-and-retainer-based-contracts"></a>Ennakkomaksut ja ennakkomaksuun perustuvat palvelusopimukset


_**Koskee:** Project Operationsin resurssiin / muuhun kuin resurssiin perustuvia skenaarioita, Lite-käyttöönotto-kaupasta proformalaskutukseen_

Dynamics 365 Project Operations tukee ennakkomaksuun perustuvia sopimuksia. Pidätykseen perustuva sopimus on neuvoteltu joukko yhtä hajautettuja maksuja, joista asiakasta laskutetaan projektin koko keston ajan. Tämäntyyppistä palvelusopimusta käytetään yleensä aika- ja materiaali- tai kulutuspohjaisissa laskutusmalleissa, joissa asiakkaalle on annettava ennustettavissa oleva lasku ja maksuaikataulu. Kunkin kauden kertyneet tuoton toteutuneet tuotot täsmäytetään asiakkaalta kauden alussa saadun maksun perusteella. Aika- ja materiaalilaskutusmallin käsitteen mukaisesti kullakin jaksolla kertyneet tuottoarvot voivat vaihdella kulujen mukaan. Jos kertynyt tuotto on suurempi kuin kauden alussa saatu summa, projektin toimitus yritys voi:

- Laskuttaa asiakasta vain ylimääräisestä 
- Siirtää tuoton täsmäyttämisen seuraavalle laskutusjaksolle ja tehdä viimeinen laskun projektin päättyessä jäljellä olevaan täsmäyttämättömään tuottoon

Perussopimuspohjaisen hankintamallin ja kiinteähintaisen sopimusmallin välinen suurin ero Project Operationsissa on se, että kiinteän hinnan sopimusmallissa laskun summa ei ole linkitetty tai sidottu aiheutuviin kustannuksiin. Laskutuksessa noudatetaan välitavoitteeseen perustuvaa lähestymistapaa, joka on kohdistettu kyseisellä jaksolla toteutuneista kustannuksista. Jos kyseessä on maksupalvelusopimus, laskutettava tuotto kirjataan sopimusrivin laskutusmenetelmän perusteella. Kun laskutustapa on aika ja materiaali, laskutettava myyntituotto on sidottu tiettynä ajan jaksona toteutuneista kustannuksista, ja se voi vaihdella kaudesta toiseen. Asiakkaalta laskutetaan kuitenkin vain kausittaisen maksun summa. Järjestelmä määrittää kauden lopussa toisen laskun täsmäyttäen kauden aikana kirjatun myyntituoton sen määrän perusteella, josta asiakasta on laskutettu kauden alussa.

Tämän menetelmän etuna on se, että asiakkaan kustannukset ovat ennustettavissa maksuaikataulussa toisin kuin tyypillisessä aika- ja materiaalimallissa. Projektin toimittajaorganisaatiolla on myös joitakin mahdollisuuksia periä kustannukset, jotka aiheutuvat siitä, että ne ovat nousseet pois siitä, että kiinteä hintamalli ei olisi sallinut niitä.

Kausittaisen ajankäyttösuunnitelman lisäksi Project Operations voi kirjata asiakkaalle kertaennakon ja täsmäyttää sen projektikustannusten eri osien perusteella.

Project Operationsin pidätys ei ole käytettävissä, ennen kuin se laskutetaan asiakkaalta. Tämä ilmaistaan seuraavissa aliruudukon kentissä ennakoina ja pidätyksinä.

| Field | Kuvaus | Loppupään vaikutus |
| --- | --- | --- |
| Käytettävissä oleva summa | Summa, joka on käytettävissä maksu- tai ennakkotietueessa. | Sitä ei voi käyttää, ennen kuin ennakko tai maksu on laskutettu, joten käytettävissä oleva summa on nolla. |
| Käytetty summa | Summa, joka on jo käytetty pidätyksissä tai ennakoissa. | Ennakko tai pidätys voidaan täsmäyttää laskuun, jolla on todelliset kustannukset ja jonka osa on merkitty jo käytetyksi tai kulutetuksi. Muu ennakko tai maksun summa on käytettävissä, jotta tulevaan laskuun voidaan täsmäyttää todelliset kustannukset. |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]