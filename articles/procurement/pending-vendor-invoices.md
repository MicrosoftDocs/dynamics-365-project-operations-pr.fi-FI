---
title: Ei-varastoivien materiaalien ostaminen käyttämällä odottavaa toimittajan laskua
description: Tässä aihe, miten odottavat toimittajan laskut tallennetaan.
author: sigitac
ms.date: 09/13/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: e95f7dabe597968707fdd2dead40bfb93d7f1f95
ms.sourcegitcommit: 74a7e1c9c338fb8a4b0ad57c5560a88b6e02d0b2
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/23/2021
ms.locfileid: "7547285"
---
# <a name="purchase-non-stocked-materials-using-a-pending-vendor-invoice"></a>Ei-varastoivien materiaalien ostaminen käyttämällä odottavaa toimittajan laskua

_**Käytetään:** Project Operationsin resursseihin ja ei-varastoitaviin perustuvissa skenaarioissa_

Kun yritys hankkii ei-varastoitavaa materiaalia projektia varten, kustannukset voidaan kirjata projektiin heti. 

Esimerkiksi Contoso Robotics US tekee välineiden uusimisprojektin ja tarvitsee ohjelmistojen käyttöoikeuksia. Nämä käyttöoikeudet hankitaan ulkopuoliselta toimittajalta.  Dynamics 365 Financen avulla ostoreskontra kirjaa odottavan toimittajan laskuasiakirjan ja määrittää käyttöoikeuskustannukset suoraan välineiden uusimisprojektiin. 

> [!IMPORTANT]
> Ennen kuin käytät tässä aiheessa kuvattuja toimintoja, tarkista ja ota käyttöön tarvittavat määritykset. Lisätietoja on ohjeaiheessa [Ei-varastoivien materiaalien ja odottavien toimittajan laskujen ottaminen käyttöön](configure-materials-nonstocked.md). 

## <a name="post-a-project-related-pending-vendor-invoice"></a>Projektiin liittyvän odottavan toimittajan laskun kirjaaminen 

Odottavat toimittajan laskut voidaan tallentaa **Odottavat toimittajan laskut** -sivulle (**Ostoreskontra** > **laskut** > **odottavat toimittajan laskut**). Kirjaa projektiin liittyvä odottava toimittajan lasku seuraavien vaiheiden mukaisesti:

1. Siirry kohtaan **Ostoreskontra** > **laskut** ja valitse **Uusi**. 
2. Valitse **Laskutili**-kentässä toimittaja ja kirjoita **Numero**-kenttään toimittajan laskun tunnus.
3. Lisää rivi toimittajan laskuun ja valitse **Nimikenumero**-kentässä toimittajalta ostettu ei-varastoitu nimike. 

    > [!NOTE]
    > Projektiin ei voi kirjata toimittajan laskun rivejä, jotka perustuvat hankintaluokkaan. 
    
5. Lisää ostettu määrä. Järjestelmä täyttää yksikköhinnan ei-varastoidun yksikköhinnan määrityksen perusteella. 
6. Tarkista kokonaissumma ja muut rivin pakolliset tiedot.
7. Valitse rivin tiedoista **Projekti**-välilehdestä sen projektin tunnus, jonne tämä kohde tallennetaan.
8. Voit myös valita aktiviteetin numeron ja päivittää projektin luokan ja rivin ominaisuuden.
9. Kirjaa odottava toimittajan lasku. Kun lasku kirjataan, järjestelmä kirjaa seuraavat tiedot:
    
    - Toimittajan saldon summa.
    - Arvonlisäveron summa.
    - Projektiin kohdistuvat kustannukset kirjataan integrointia varten integrointitilille.
    - Projektin toteutuneiden kustannusten tapahtuma Dataversessa.  Tätä tapahtumaa käsitellään lisää [Project Operations Integration -kirjauskansion](../project-accounting/project-operations-integration-journal.md) avulla. Tämän kirjauksen kirjaaminen siirtää summan integroinnin lisäkulutililtä projektikustannustilille. 
    - Ostot, jotka laskutetaan projektiasiakkaalta käyttämällä aika ja materiaali -laskutustapaa. Lisäksi ostoille luodaan laskuttamattomat myyntitapahtumat Dataversessa. Dataversessa olevaa tuotehinnastoa käytetään laskuttamattoman myyntitapahtuman myyntihintoja ja määriä varten.
