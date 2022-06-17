---
title: Tapahtumayhteydet – eri tapahtumatyyppien toteutuneiden arvojen linkitys
description: Tässä artikkelissa käsitellään sitä, miten tapahtumayhteyttä käytetään erityyppisten toteutuneiden arvojen linkittämiseen kannattavuuden, laskutuksen tehtävälista ja laskutettu vs. laskuttamaton -myyntituottolaskelmien seuraamiseen.
author: rumant
ms.date: 03/25/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 19a78336099f54c5d6b36a963a90b9fd77e3d0af
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8926082"
---
# <a name="transaction-connections---link-actuals-of-different-transaction-types"></a>Tapahtumayhteydet – eri tapahtumatyyppien toteutuneiden arvojen linkitys

_**Koskee:** Project Operationsin resurssiin / muuhun kuin resurssiin perustuvia skenaarioita, Lite-käyttöönotto-kaupasta proformalaskutukseen_

Tapahtumayhteystietueet luodaan, jotta erityyppiset toteutuneet tiedot voidaan linkittää kun ajan, kulun tai materiaalin käyttö siirtyy elinkaaren aikana tarjouksesta tai myyntiä edeltävästä vaiheesta palvelusopimuksen vaiheeseen, hyväksyntöihin ja/tai takaisinvetoihin, laskutukseen sekä mahdollisesti hyvitykseen tai korjaavaan laskutukseen.

Seuraavassa esimerkissä esitellään aikamerkintöjen tyypillinen käsittely Project Operationsissa projektin elinkaaren aikana.

> ![Aikamerkintöjen käsittely Project Operationsissa.](media/basic-guide-17.png)

Aikamerkintöjen käsittely Project Operationsin projektin elinkaaren aikana noudattaa seuraavia vaiheita: 

1. Aikamerkinnän lähettäminen johtaa kahden kirjauskansion rivin luomiseen: yksi kustannuksia ja toinen laskuttamatonta myyntiä varten. 
2. Aikamerkinnän hyväksyminen taas johtaa kahden todellisen arvon luomiseen: yksi kustannuksia ja toinen laskuttamatonta myyntiä varten. Nämä kaksi toteutunutta arvoa linkitetään tapahtumayhteyksien avulla.
3. Kun käyttäjä luo projektilaskun, laskurivitapahtuma luodaan laskuttamattoman myynnin todellisen arvon tietojen perusteella.
4. Kun lasku on vahvistettu, tämä luo kaksi uutta todellista tapahtumaa: laskuttamattoman myynnin palautus ja laskutetun myynnin todellinen arvo. Laskuttamattoman myynnin peruutus ja alkuperäinen laskuttamaton toteutunut myynti yhdistetään käyttämällä peruutustapahtumayhteyksiä. Laskutettu myynti ja alkuperäiset laskuttamattoman myynnin toteutuneet arvot yhdistetään, jotta näytetään linkit siitä, mikä oli kerran tehtävälista tai käynnissä olevan laskutettavan työn tuotto siihen, mikä nyt ja on laskutettua tuottoa.   

Jokainen käsittelytyönkulun tapahtuma käynnistää tietueiden luomisen **Tapahtumayhteys**-taulukkoon. Tämä auttaa luomaan jäljityksen ajankirjaamisen, kirjauskansiorivin, toteutuneiden arvojen ja laskurivin tietojen luomien tietueiden suhteiden välille.

Seuraavassa taulukossa esitetään edeltävässä työnkulussa käytettävän **Tapahtuman yhteys** -entiteetin tietueet.

|Tapahtuma                   |Tapahtuma 1                 |Tapahtuman 1 rooli |Tapahtuman 1 tyyppi       |Tapahtuma 2          |Tapahtuman 2 rooli |Tapahtuman 2 tyyppi |
|------------------------|------------------------------|---------------|-----------------------------|-----------------------------|-------------------|-------------------|
|Aikamerkinnän lähetys   |Kirjauskansion rivin (myynti) GUID     |Laskuttamaton myynti |msdyn_journalline            |Kirjauskansion rivin (kustannus) GUID     |Kustannus            |msdyn_journalline  |
|Ajan hyväksyminen           |Uusien laskuttamattoman myynnin todellisen arvon GUID  |Laskuttamaton myynti |msdyn_actual                 |Kustannuksen todellisen arvon (kustannus) GUID       |Kustannus            |msdyn_actual       |
|Laskun luonti        |Laskurivin tietojen GUID      |Laskutettu myynti   |msdyn_invoicelinetransaction |Uuden laskuttamattoman myynnin todellisen arvon GUID   |Laskuttamaton myynti  |msdyn_actual       |
|Laskun vahvistaminen    |Palauttavan todellisen arvon GUID         |Palauttava      |msdyn_actual                 |Alkuperäisen laskuttamattoman myynnin GUID |Alkuperäinen        |msdyn_actual       |
|                        |Laskutetun myynnin GUID             |Laskutettu myynti   |msdyn_actual                 |Uuden laskuttamattoman myynnin todellisen arvon GUID   |Laskuttamaton myynti  |msdyn_actual       |
|Laskuluonnoksen korjaus |Laskurivin tapahtuman GUID|Korvaava      |msdyn_invoicelinetransaction |Laskutetun myynnin GUID            |Alkuperäinen        |msdyn_actual       |
|Laskun korjauksen vahvistaminen|Laskutetun myynnin palautuksen GUID  |Palauttava      |msdyn_actual                 |Laskutetun myynnin GUID            |Alkuperäinen        |msdyn_actual       |
|                        |Uusi laskuttamaton myynti – GUID |Korvaava            |msdyn_actual                 |Laskutetun myynnin GUID            |Alkuperäinen        |msdyn_actual       |


Seuraavassa kuvassa on esitetty eri tyyppisten toteutuneiden arvojen luodut linkit eri tapahtumille käyttämällä Project Operationsin aikamerkintöjen esimerkkiä.

> ![Miten erityyppiset toteutuneet arvot linkitetään toisiinsa Project Operationsissa.](media/TransactionConnections.png)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
