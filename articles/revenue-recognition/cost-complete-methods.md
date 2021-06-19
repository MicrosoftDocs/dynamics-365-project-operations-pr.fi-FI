---
title: Valmistumiskustannusten menetelmät
description: Tässä aiheessa on tietoja menetelmistä, joita käytetään projektin valmistumiskustannusten laskemiseen.
author: sigitac
ms.date: 11/16/2020
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: c6d3cd6056466be686f15c9f332c8274aeb0ac19
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/10/2021
ms.locfileid: "6013932"
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