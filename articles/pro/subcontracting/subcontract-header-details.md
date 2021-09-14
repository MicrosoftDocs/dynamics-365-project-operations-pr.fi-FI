---
title: Alihankintojen otsikkotiedot
description: Tässä aiheessa on tietoja Project Operationsin alihankintaotsikoiden tarjoamista toiminnoista.
author: rumant
ms.date: 08/05/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 49158af1a430033db3a5db57a840512c45bc17e2
ms.sourcegitcommit: 80aa1e8070f0cb4992ac408fc05bdffe47cee931
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/13/2021
ms.locfileid: "7323637"
---
# <a name="header-details-for-subcontracts"></a>Alihankintojen otsikkotiedot

[!include [banner](../../includes/dataverse-preview.md)]

_**Käytetään:** Lite-käyttöönotto – kauppa proformalaskutukseen_

Tässä aiheessa on tietoja Dynamics 365 Project Operationsin alihankintaotsikoiden tarjoamista toiminnoista.

Projektipäällikkö voi suunnitellessaan ja toteuttaessaan projekteja käyttää alihankkijoita ja ostaa tuotteita ja palveluita toimittajilta. Kun projektipäällikön on ostettava tuotteita tai palveluita, hän voi luoda alihankinnan Project Operationsissa.

Luodaksesi alihankinnan toimi seuraavasti:

1. Valitse siirtymisruudusta **Alihankinnat** ja valitse **Alihankinta**-sivulla **Uusi**.
2. Syötä tarvittavat tiedot ja valitse **Tallenna**.

    Seuraavassa taulukossa on tietoja Alihankinta-otsikkosivun kentistä.

    | **Kenttä** | **Kuvaus** |
    | --- | --- | 
    | Nimi | Alihankinnan nimi. |
    | Kuvaus | Lyhyt kuvaus alihankintarivillä ostettavista palveluista ja tuotteista. |
    | Toimittaja | Yrityksen, jolta tuotteet ja palvelut ostetaan, nimi. Tämän tilitietueen suhdetyyppi on **Toimittaja** tai **Alihankkija**. |
    | Alihankinnan päivämäärä | Päivämäärä, jona alihankinta luodaan. |
    | Tilan syy | Alihankinnan tila. |
    | Valuutta | Valuutta, jossa tuotteet ja palvelut ostetaan. Tämän kentän arvo on toimittajatilin oletusarvo, mutta sitä voidaan muuttaa. Projektihinnastojen, joita käytetään alihankinnan tuotteiden ja palveluiden hinnoitteluun, tulisi olla tässä valuutassa. Muissa valuutoissa olevia hinnastoja ei voi liittää alihankintaan. Tästä alihankinnasta aiheutuvat tuotteiden ja palveluiden kustannukset kirjataan projektiin tässä valuutassa. |
    | Sopimusyksikkö | Yrityksen osasto, joka on tekemässä ostosopimusta tai alihankintaa toimittajan kanssa. |
    | Maksuehdot | Tälle alihankinnalle luotujen toimittajan laskujen maksuehdot. Tämän kentän arvo on toimittajatilin tietueen oletusarvo. |
    | Maksuosoite | Osoite, johon toimittajan laskujen maksu lähetetään. Tämän kentän arvo on toimittajatilin tietueen oletusarvo. |
    | Laskutusosoitteen nimi | Laskun lähettävän henkilön tai osaston nimi toimittajan yrityksessä. Tämän kentän arvo on toimittajatilin tietueen oletusarvo, ja sitä käytetään toimittajalaskujen ensisijaisen yhteyshenkilön nimenä tässä alihankinnassa. |
    | Laskutusosoite | Osoite, jota käytetään tämän toimittajan laskuissa. Tämän kentän arvo on toimittajatilin tietueen oletusarvo. Osoitetta käytetään myös saapuvien laskujen osoitteena toimittajan laskuissa, jotka on luotu tälle alihankinnalle. |
    | Välisumma | Jos alihankinnassa ei ole rivejä, kirjoita tähän kenttään arvo, joka osoittaa tilauksen välisumman ennen veroja. Jos alihankinnassa on rivejä, tämä kenttä on vain luku -tyyppinen. Näytettävä summa on alihankinnan kaikkien rivien välisumma. |
    | Vero yhteensä | Jos alihankinnassa ei ole rivejä, kirjoita tähän kenttään arvo, joka osoittaa tämän alihankinnan veroja. Jos alihankinnassa on rivejä, tämä kenttä on vain luku -tyyppinen. Näytettävä summa on alihankinnan kaikkien rivien verojen summa. |
    | Loppusumma |  Tässä laskennallisessa kentässä näkyy alihankintarivin kokonaissumma verot mukaan lukien.  |
    | Vahvistuspäivä | Päivämäärä, jona alihankinta vahvistettiin.  |
    | Pyytänyt | Tämän kentän arvo on oletusarvoisesti käyttäjän nimi, joka loi tämän alihankinnan. Tätä arvoa voi muuttaa se henkilö, joka loi alihankinnan, jotta voidaan ilmaista henkilö, jonka puolesta hän loi alihankinnan.  |
    | Toimittajatilin päällikkö | Toimittajatilin ensisijaisen yhteyshenkilön nimi. Tämän kentän arvo on toimittajatilin tietueen oletusarvo. Käyttäjä voi muuttaa tämän kentän arvoa, jos hän haluaa valita toisen yhteyshenkilön toimittajan asiakaspäälliköksi kyseisessä alihankinnassa. Yhteyshenkilö voi määrittää ja lähettää sähköposti-ilmoitukset ja hintaneuvottelut. |


