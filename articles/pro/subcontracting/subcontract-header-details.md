---
title: Alihankintojen otsikkotiedot
description: Tässä artikkelissa on tietoja Project Operationsin alihankintaotsikoiden tarjoamista toiminnoista.
author: rumant
ms.date: 09/14/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 85649d08228b16178eb8d6be9af5a6731def74bf
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8914168"
---
# <a name="header-details-for-subcontracts"></a>Alihankintojen otsikkotiedot

[!include [banner](../../includes/dataverse-preview.md)]

_**Käytetään:** Lite-käyttöönotto – kauppa proformalaskutukseen_

Tässä artikkelissa on tietoja Dynamics 365 Project Operationsin alihankintaotsikoiden tarjoamista toiminnoista.

Projektipäällikkö voi suunnitellessaan ja toteuttaessaan projekteja käyttää alihankkijoita ja ostaa tuotteita ja palveluita toimittajilta. Kun projektipäällikön on ostettava tuotteita tai palveluita, hän voi luoda alihankinnan Project Operationsissa.

Luodaksesi alihankinnan toimi seuraavasti:

1. Valitse siirtymisruudusta **Alihankinnat** ja valitse **Alihankinta**-sivulla **Uusi**.
2. Syötä tarvittavat tiedot ja valitse **Tallenna**.

    Seuraavassa taulukossa on tietoja **Alihankinnan otsikko** -sivun kentistä.

    | Kenttä | Kuvaus |Toiminnallinen vaikutus |
    |---|------|---| 
    | Nimi | Alihankinnan nimi. | Kaikissa avattavissa alihankinnan luetteloissa alihankinnan nimi näkyy ensimmäisessä sarakkeessa, mikä auttaa tunnistamaan alihankinnat. | 
    | Kuvaus | Lyhyt kuvaus alihankintarivillä ostettavista palveluista ja tuotteista. | Ei ole |
    | Toimittaja | Yrityksen, jolta tuotteet ja palvelut ostetaan, nimi. Tämän tilitietueen suhdetyyppi on **Toimittaja** tai **Alihankkija**. | Oletusarvot syötetään automaattisesti seuraaviin kenttiin valitun toimittajan mukaan:<br/> **• Valuutta** </br> **• Hinnastot** </br> **• Maksuehdot**</br> **• Maksuosoite**</br> **• Laskutusosoite**</br> **• Laskutusosoitteen nimi** </br>**• Toimittajatilin päällikkö**|
    | Alihankinnan päivämäärä | Päivämäärä, jona alihankinta on luotu. | Alihankinnan päivämäärää käytetään oikean ostohinnaston valitsemiseen joko liittyvään toimittajaan liitetyistä hinnastoista tai projektin parametreista. |
    | Tilan syy | Alihankinnan tila. | Tila määrittää, missä liiketoimintaprosessissa alihankinta on ja voiko sitä muokata. <br/>Arvoihin kuuluvat:<br>• **Luonnos**: Alihankintaa voi muokata. Voit muokata vain alihankintoja, joiden tila on **Luonnos**.<br/>• **Vahvistettu**: Neuvottelu toimittajan kanssa on valmis ja alihankinta on hyväksytty toimitusta varten. <br/>• **Suljettu**: Alihankinnan toimitus on valmis.<br/>• **Peruutettu**: Alihankinta on peruutettu eikä toimitusta suunnitella.  | 
    | Valuutta | Valuutta, jossa tuotteet ja palvelut ostetaan. Oletusarvo syötetään automaattisesti toimittajatililtä, mutta sitä voi muuttaa. | Alihankinnan valuuttaa käytetään oikean ostohinnaston valitsemiseen joko liittyvään toimittajaan liitetyistä hinnastoista tai projektin parametreista. Toisessa valuutassa olevia hinnastoja ei voi liittää alihankintaan. Aika-, kulu- ja materiaalikustannukset, jotka toimittajaresurssit tuottavat tästä alihankinnasta, kirjataan projektiin tässä valuutassa. Kun alihankintatietue on tallennettu, alihankinnan valuuttaa ei voi muuttaa.|
    | Sopimusyksikkö | Yrityksen osasto, joka on tekemässä ostosopimusta tai alihankintaa toimittajan kanssa. | Ei ole |
    | Maksuehdot | Tälle alihankinnalle luotujen toimittajan laskujen maksuehdot. Oletusarvo syötetään automaattisesti toimittajatilin tietueesta. | Alihankinnan maksuehdot kopioidaan kaikkiin toimittajan laskuihin, jotka liittyvät tähän alihankintaan. Maksuehtoja voidaan päivittää, jos alihankinnan tilana on **Luonnos**. | 
    | Maksuosoite | Osoite sille toimittajalle, jolle maksut on lähetettävä. Oletusarvo syötetään automaattisesti toimittajatilin tietueesta. | Alihankinnan maksuosoite kopioidaan maksuosoitteeksi kaikkiin tälle alihankinnalle luotuihin toimittajan laskuihin. Maksuosoitetta voidaan päivittää, jos alihankinnan tilana on **Luonnos**.|
    | Laskutusosoitteen nimi | Laskun lähettävän henkilön tai osaston nimi toimittajan yrityksessä. Oletusarvo syötetään automaattisesti toimittajatilin tietueesta. | Alihankinnan **Laskutusasiakkaan nimi** -arvo kopioidaan kaikkiin toimittajan laskuihin, jotka liittyvät tähän alihankintaan. Tätä kenttää voidaan päivittää, jos alihankinnan tilana on **Luonnos**.|
    | Laskutusosoite | Osoite, jota käytetään toimittajalta tulleissa laskuissa. Oletusarvo syötetään automaattisesti toimittajatilin tietueesta. | Tämä osoite on "lasku kohteesta" -osoite toimittajan laskuissa, jotka on luotu tälle alihankinnalle. |
    | Välisumma | Jos alihankinnalla ei ole rivejä, syötä tilauksen välisumma ennen veroja. Jos alihankinnassa on rivejä, tämä kenttä on vain luku -tyyppinen. Näytetyssä summassa on alihankinnan kaikkien rivien välisumma. | Ei ole |
    | Vero yhteensä | Jos alihankinnalla ei ole rivejä, syötä tämän alihankinnan verojen kokonaissumma. Jos alihankinnassa on rivejä, tämä kenttä on vain luku -tyyppinen. Näytetyssä summassa on alihankinnan kaikkien rivien verojen kokonaissumma. | Ei ole |
    | Loppusumma | Tässä laskennallisessa kentässä näkyy alihankintarivin kokonaissumma verot mukaan lukien. | Ei ole |
    | Vahvistuspäivä | Päivämäärä, jona alihankinta vahvistettiin. | Ei ole |
    | Pyytänyt | Tämä kenttä määritetään oletusarvoisesti sille käyttäjänimelle, joka luo alihankinnan. Alihankinnan tekijä voi kuitenkin muuttaa arvoa ilmaistakseen henkilön, jonka puolesta hän luo alihankinnan. | Ei ole |
    | Toimittajatilin päällikkö | Toimittajatilin ensisijaisen yhteyshenkilön nimi. Oletusarvo syötetään automaattisesti toimittajatilin tietueesta. Voit valita toisen yhteyshenkilön alihankinnan toimittajan asiakaspäälliköksi. | Voit määrittää sähköposti-ilmoitukset, jotka ilmoittavat yhteyshenkilölle, kun alihankintaan tehdään muutoksia hintaneuvottelujen tuloksena. |
