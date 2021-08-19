---
title: Valmistumiskustannusten menetelmät
description: Tässä aiheessa on tietoja menetelmistä, joita käytetään projektin valmistumiskustannusten laskemiseen.
author: sigitac
ms.date: 11/16/2020
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: fe42ea0e1a5c562ec648fbf2a2924648af80381b9db8ffe0c209cb5247bb2ba2
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/06/2021
ms.locfileid: "6997962"
---
# <a name="cost-to-complete-methods"></a>Valmistumiskustannusten menetelmät

_**Käytetään:** Project Operationsin resursseihin ja ei-varastoitaviin perustuvissa skenaarioissa_

Tässä aiheessa on tietoja menetelmistä, joita käytetään projektin valmistumiskustannusten laskemiseen. Projektin valmistumiskustannusten laskentaan on olemassa useita tapoja. 

Kun luot arvion projektia varten, voit valita **Luo arvio** -sivun **Valmistumiskustannusten menetelmä** -kentässä yhden seuraavista valmistumiskustannusten menetelmistä.

| Valmistumiskustannusten menetelmä    | Kuvaus                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Kokonaiskustannukset-todelliset            | Syötä arvioidut kustannukset manuaalisesti **Kokonaiskustannukset**- tai **Kokonaismäärä**-kenttiin käyttäen **Kustannusarvio**-painiketta **Arviosivulla**. Järjestelmä vähentää todelliset kustannukset syöttämistäsi loppusummista. Kokonaissumma on projektin valmistumiskustannukset. Tämä menetelmä ei käytä kuluarvioita eikä resurssivarauksia, jotka on syötetty Microsoft Dataversen avulla rakennettuun Project Operationsiin. Kokonaiskustannukset tai kokonaismäärä voidaan päivittää manuaalisesti tarpeen mukaan.  |
| Kokonaisennuste-todellinen        | Resurssivarauksia ja kuluarvioita käytetään määrittämään projektin kokonaisennustesummaa. Toteutuneita kustannuksia verrataan tähän ennusteeseen valmistumiskustannusten laskemista varten.                                                                                                                                                                                                                                                                          |
| Edellisen arvion mukaan         | Tässä käytetään samoja arviointimenetelmiä, joita käytettiin edellisellä kaudella. Tämä menetelmä edellyttää ennustemallia, jos edellisellä jaksolla on vaadittu ennustemallia.                                                                                                                                                                                                                                                                                                                           |
| Määritä kustannukset valmiiksi nollaksi | Tätä menetelmää käytetään yleensä ennen arviointiprojektin poistamista, ja se liittää kokonaisarviot kirjattuihin todelliseen tapahtumiin ja tyhjentää **Valmistumiskustannukset**-sarakkeen. Valmistumisen jälkeen tuloksena on aina 100 prosenttia. Minkään luotavan kustannus rivin **Ennuste**-valintaruutu ei ole valittuna ja kokonaisarvio kopioidaan edellisestä kustannusarviosta. Arviokauden todellinen kulutus vähennetään projektin valmistumiseen liittyvistä kustannuksista.              |
| Kustannusmallista           | Valittuun projektiin liittyvässä kustannusmallissa määritetty valmistumiskustannusmenetelmä.                                                                                                                                                                                                                                                                                                                                                                          |


[!INCLUDE[footer-include](../includes/footer-banner.md)]