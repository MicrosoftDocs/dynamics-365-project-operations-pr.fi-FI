---
title: Ei-varastoivien materiaalien tai hankintaluokkien ostaminen odottavan toimittajan laskun avulla
description: Tässä aihe, miten odottavat toimittajan laskut tallennetaan.
author: sigitac
ms.date: 09/13/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: e81f7a54e304ae6fc9a9f2637124579b6e7b54e9
ms.sourcegitcommit: 9916f536a71b6a0078297402564ac79308ec6890
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/18/2022
ms.locfileid: "8612653"
---
# <a name="purchase-non-stocked-materials-or-procurement-categories-using-a-pending-vendor-invoice"></a>Ei-varastoivien materiaalien tai hankintaluokkien ostaminen odottavan toimittajan laskun avulla

_**Käytetään:** Project Operationsin resursseihin ja ei-varastoitaviin perustuvissa skenaarioissa_

Kun yritys hankkii ei-varastoituja materiaaleja tai hankintaluokkia projektille, kustannukset voidaan kirjata projektiin heti. 

Esimerkiksi Contoso Robotics US tekee välineiden uusimisprojektin ja tarvitsee ohjelmistojen käyttöoikeuksia. Nämä käyttöoikeudet hankitaan ulkopuoliselta toimittajalta.  Dynamics 365 Financen avulla ostoreskontran kirjanpitäjä kirjaa odottavan toimittajan laskuasiakirjan ja määrittää käyttöoikeuskustannukset suoraan välineiden uusimisprojektiin. 

> [!IMPORTANT]
> Ennen kuin käytät tässä aiheessa kuvattuja toimintoja, tarkista ja ota käyttöön tarvittavat määritykset. For Lisätietoja on ohjeaiheessa [Ei-varastoitujen materiaalien ja odottavien toimittajan laskujen käyttöönotto](configure-materials-nonstocked.md) ja [Hankintaluokkien käyttö projektin ostotilauksissa ja odottavissa toimittajan laskuissa](configure-procurement-categories.md)

## <a name="post-a-project-related-pending-vendor-invoice"></a>Projektiin liittyvän odottavan toimittajan laskun kirjaaminen 

Odottavat toimittajan laskut voidaan tallentaa **Odottavat toimittajan laskut** -sivulle (**Ostoreskontra** > **laskut** > **odottavat toimittajan laskut**). Kirjaa projektiin liittyvä odottava toimittajan lasku seuraavien vaiheiden mukaisesti:

1. Siirry kohtaan **Ostoreskontra** > **Laskut** ja valitse **Uusi**. 
1. Valitse **Laskutili**-kentässä toimittaja ja kirjoita sitten **Numero**-kenttään toimittajan laskun tunnus.
1. Lisää rivi toimittajan laskuun ja valitse sitten **Nimikenumero**-kentässä toimittajalta ostettu ei-varastoitu nimike. Voit vaihtoehtoisesti valita **Hankintaluokka**-kentässä toimittajalta ostetun hankintaluokan.   
1. Lisää ostettu määrä. Järjestelmä täyttää yksikköhinnan ei-varastoidun nimikkeen hintamäärityksen perusteella. 
1. Tarkista kokonaissumma ja muut rivin pakolliset tiedot.
1. Valitse rivin tiedoissa **Projekti**-välilehdestä sen projektin tunnus, jonne tämä nimike kirjataan.
1. Valinnainen: Valitse aktiviteetin numero ja päivitä projektin luokka ja rivin ominaisuus.
1. Kirjaa odottava toimittajan lasku. Kun lasku kirjataan, järjestelmä kirjaa seuraavat tiedot:
    
    - Toimittajan saldon summa.
    - Arvonlisäveron summa.
    - Projektiin kohdistuvat kustannukset kirjataan integrointia varten integrointitilille.
    - Projektin toteutuneiden kustannusten tapahtuma Dataversessa.  Tätä tapahtumaa käsitellään lisää [Project Operations Integration -kirjauskansion](../project-accounting/project-operations-integration-journal.md) avulla. Tämän kirjauksen kirjaaminen siirtää summan integroinnin lisäkulutililtä projektikustannustilille. 
    - Ostot, jotka laskutetaan projektiasiakkaalta käyttämällä aika ja materiaali -laskutustapaa. Lisäksi ostoille luodaan laskuttamattomat myyntitapahtumat Dataversessa. Dataversessa olevaa tuotehinnastoa käytetään laskuttamattoman myyntitapahtuman myyntihintoja ja määriä varten.
