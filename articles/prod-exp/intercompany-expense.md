---
title: Konsernin sisäiset kulut
description: Tässä artikkelissa on tietoja siitä, miten konsernin sisäisiä kuluja käytetään työntekijän kulujen kohdistamiseksi sille yritykselle, jolle työ on tehty.
author: suvaidya
ms.date: 07/08/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TrvParameters
audience: Application User
ms.reviewer: johnmichalak
ms.search.region: Global
ms.author: suvaidya
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1c58fb1510c9ba75bc81a4dc07b91f1b6a60355d
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8932384"
---
# <a name="intercompany-expenses"></a>Konsernin sisäiset kulut

Työntekijä, joka on yhden yrityksen palveluksessa organisaatiossa, voi suorittaa työn toiselle saman organisaation yritykselle. Voit käyttää konsernin sisäisiä kuluja työntekijän kulujen kohdistamiseksi sille yritykselle, jolle työ on tehty. Yritystä, jonka palveluksessa työntekijä on, kutsutaan lainaavaksi yritykseksi. Yritystä, jolle työntekijästä aiheutuu kuluja, kutsutaan lainaavaksi yritykseksi. 

Ennen kuin työntekijä voi luoda ja lähettää konsernin sisäisiä kuluja, sinun on otettava käyttöön konsernin sisäisten kulujen rivit. Valitse lainan myöntävän yrityksen **Kulujen hallintaparametrit** -sivulta **Salli konsernin sisäisten kulujen rivit**. 

## <a name="tax-posting-for-intercompany-expenses"></a>Konsernin sisäisten kulujen verokirjaus

[!include [banner](../includes/banner.md)]

Ennen kuin voit käyttää lainan myöntävään (lähde) yritykseen liittyviä veroryhmiä lainan ottavan (kohde) yrityksen sijaan kuluraportissa, sinun on otettava käyttöön toiminto pääkirjan arvonlisäveroasetuksissa. Kun **Yritys konsernin sisäistä verokirjausta varten** -parametriksi on asetettu **Lähde** ja **Käytä arvonlisäveron verotussääntöjä** -asetukseksi on valittu **Ei**, lainan myöntävän yrityksen veroyhdistelmää käytetään. Kun sama parametri on asetettu **kohteeseen**, käytetään lainaavan yrityksen veroyhdistelmää. Jos kyseessä on Yhdysvaltalainen yritys, kun parametrin arvoksi on määritetty **lähde**, **arvonlisäverosaatavat**-kentän asetukset on määritettävä myös uuden **kirjanpidon kirjausryhmät** -sivulla. Kirjanpitomoduuli käyttää tämän kentän tietoja veroihin liittyvään kirjanpitomerkintään.   
Toiminta on yhdenmukainen projektin kanssa tai ei-kirjattujen kulurivien kanssa.  

## <a name="new-expense-expression-builder"></a>Uusi kululausekkeen muodostin

Uusi kustannuslausekkeen muodostin käsittelee ongelmia, jotka liittyvät projekteja käyttäviin yritysten välisiin kuluskenaarioihin. Tämä ominaisuus varmistaa, että kun luot konsernin kulun, kulukäytäntö tarkistetaan oikein kulurivillä valittua projektia vastaan, ja että kuluraportin voi lähettää onnistuneesti.

Jotta kululausekkeen muodostintoiminto toimisi, se on otettava käyttöön. Lisäksi on määritettävä kulukäytäntö, jolla on projektitunnus.

Jos olet jo määrittänyt käytäntöjä, jotka tarkistavat projektin tunnuksen kulurivillä, nämä käytännöt on otettava pois käytöstä. Tämän jälkeen voit ottaa ominaisuuden käyttöön ja määrittää käytännöt uudelleen.

Voit ottaa toiminnon käyttöön seuraavien ohjeiden mukaisesti.

1. Siirry kohtaan **Työtilat** \> **Ominaisuuksien hallinta**.
2. Valitse luettelosta **Uusi kustannusilmoituksen rakennustyökalu, joka käsittelee projekteja käyttävien yritysten välisten kuluskenaarioiden ongelmia.** Valitse sitten **Ota käyttöön nyt**.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
