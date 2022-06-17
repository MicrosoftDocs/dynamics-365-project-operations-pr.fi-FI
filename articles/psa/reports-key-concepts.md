---
title: Keskeiset käsitteet
description: Tässä artikkelissa on tietoja Project Service Automationin resurssienhallinnan keskeisistä käsitteistä.
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 03/28/2019
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
ms.reviewer: johnmichalak
ms.openlocfilehash: 41b13000ca17ec3a5d86fdb17885f09692d6f0c0
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8921712"
---
# <a name="key-concepts"></a>Keskeiset käsitteet

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Seuraavassa taulukossa on määritetty Dynamics 365 Project Service Automation -sovelluksessa käytettävät keskeiset käsitteet.

| Käsite                    | Määritelmä |
|----------------------------|------------|
| Projektiryhmän jäsen        | Projektiryhmän jäsen osana projektiryhmää voi olla nimetty resurssi, jolla on varauksia, nimetty resurssi, jolla ei ole varauksia, tai yleinen resurssi. Yleisillä resursseilla ei ole varauksia, ne ovat paikallisia projektissa, eikä niillä ole kapasiteettirajoituksia projektien välillä. |
| Projektin yleinen resurssi   | Resurssin paikkamerkki, jonka avulla voit muodostaa ryhmän ja luoda henkilöstön projektisuunnitelmaan ilman, että sinun tarvitsee tietää nimettyä resurssia. Projektikalenteria käytetään yleisen resurssin kalenterina. Yleisiä resursseja voidaan lisätä projektiryhmään ja kohdentaa tehtäviin. |
| Varatut tunnit               | Resurssitunnit kirjataan sitovasti projektiin, jotta voidaan varmistaa, että projektityö valmistuu. Varatut tunnit kulutetaan resurssin kokonaiskapasiteetista. Varauksia tehdään vain nimetyille resursseille, ei yleisille resursseille. |
| Kohdennetut tunnit             | Resurssitunnit kohdennetaan projektiaikataulun tehtäville. Kohdennukset voivat koskea joko nimettyjä resursseja tai yleisiä resursseja. Kohdennukset voivat olla riippumattomia varauksista. |
| Vaaditut tunnit             | Kapasiteetti, joka tarvitaan, mutta jota ei vielä ole täytetty nimetyllä resurssilla. Vaaditut tunnit liittyvät vain yleisiin ryhmän jäseniin, joilla on luotuja resurssitarpeita. |
| Kysyntä                     | Nykyinen ja saapuva työmäärä. Project Service Automationissa kysyntä näkyy resurssivaatimuksien tai resurssipyyntöjen muodossa. |
| Resurssitarve       | Entiteetti, jota käytetään tallentamaan vaaditut tunnit, alku- ja loppupäivämäärät, maantieteelliset seikat ja muita hinnoitteludimensioita vaadituille resursseille. Resurssivaatimukset luodaan joko projektiryhmän jäsenistä tai ne luodaan yksitellen. |
| Resurssipyyntö           | Entiteetti, jota käytetään "kirjekuorena", joka kuljettaa resurssivaatimuksia, jotka resurssipäällikön tulee täyttää. |
| Resurssin oletusrooli      | Rooli, jonka alle resurssi on ryhmitelty käyttöasteen laskentaa varten. Resurssilla oletetaan olevan roolille tarvittavat taidot ja saavuttavan tavoitekäyttöastetta tälle roolille. |
| Resurssiorganisaatioyksikkö | Organisaatioyksikkö, jolle resurssi on kohdennettu. |
| Muoto                    | Tehtävän, vaatimuksen tai kohdennuksen tunnit jaettuina päivittäin. Esimerkiksi viiden päivän ja 40 tunnin tehtävä voidaan määrittää kahdeksaan tuntiin päivässä viiden päivän kuluessa. |
| Täsmäytysnäkymä        | Näkymä, jossa näkyvät kunkin projektiryhmän jäsenen varaukset ja kohdennukset. Tämä näkymä mahdollistaa sen, että projektipäällikkö voi hakea varauksien ja kohdennusten välisiä eroja ja tehdä korjaavia toimenpiteitä, jos ilmenee ristiriitoja. |
| Työaika                 | Entiteetti, jonka avulla tunnistetaan resurssikapasiteetti sekä työtunnit ja ei-työtunnit. Tätä entiteettiä kutsutaan myös resurssikalenteriksi. |


[!INCLUDE[footer-include](../includes/footer-banner.md)]
