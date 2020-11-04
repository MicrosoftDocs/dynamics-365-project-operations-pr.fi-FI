---
title: Luottokorttitapahtumien tuonti ja ylläpitäminen
description: Tässä aihessa on tietoja kuluun liittyvien luottokorttitapahtumien tuomisesta ja ylläpitämisestä. Nämä tapahtumat voidaan määrittää siten, että ne tuodaan automaattisesti toistuvaan aikatauluun, tai ne voidaan tuoda manuaalisesti tarpeen mukaan.
author: KimANelson
manager: AnnBe
ms.date: 01/12/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TrvPbsMainDataLines
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 274023
ms.assetid: 3605eda1-a7ed-4675-8031-5279c5a8f5e4
ms.search.region: Global
ms.author: suvaidya
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.openlocfilehash: 6cec15e436bc699e361577c970dd5845c6c68908
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/16/2020
ms.locfileid: "4075501"
---
# <a name="import-and-maintain-credit-card-transactions"></a>Luottokorttitapahtumien tuonti ja ylläpitäminen

[!include [banner](../includes/banner.md)]

Kuluihin liittyvät luottokorttitapahtumat voidaan määrittää automaattisesti tuotaviksi toistuvalla aikataululla. Vaihtoehtoisesti tapahtumat voidaan tuoda manuaalisesti tarvittaessa. Luottokorttitapahtumat tuodaan luottokorttitapahtumien tietoentiteetin kautta.

Lisätietoja tietoyksiköistä on kohdassa [Tietoyksiköt](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/data-entities/data-entities).

## <a name="import-credit-card-transactions"></a>Luottokorttitapahtumien tuominen

1. Valitse **Luottokorttitapahtumat** -sivulla **Tuo tapahtumat**. Jos avaat tietojen hallinnan ensimmäisen kerran, järjestelmän on päivitettävä tieto-entiteettiluettelo ennen kuin jatkat.
2. Anna **Nimi** -kenttään tuotavan työn yksilöivä kuvaus.
3. Valitse **Lähdetietojen muoto** -kentässä sen tiedoston muoto, joka sisältää tuotavat luottokorttitapahtumat.
4. Valitse **Lataa** ja etsi sitten tuotava tiedosto.
5. Kun tiedosto on ladattu, tarkista luottokorttitapahtumtiedoston ja luottokorttitapahtumien tietoentiteetin sarakkeiden yhdistämismääritys valitsemalla ruudun **Näytä yhdistämismääritys** -linkki. Jos löytyy yhdistämismääritysvirheitä tai jos yhdistämismääritys on muutettava, tee muutokset **Yhdistämismäärityksen visualisointi** -välilehdessä tai **Yhdistämismäärityksen tiedot** -välilehdessä.
6. Jos haluat automatisoida luottokorttitapahtumia, valitse **Luo toistuva tietotyö**. Tämän jälkeen voit määrittää toistuvuuden, joka määrittää, miten usein luottokorttitapahtumat tuodaan. Kun olet valmis, valitse **OK**.
7. Jos haluat tuoda valitun tiedoston nyt, valitse **Tuo**.
8. Jos tuonnin aikana tapahtuu virheitä, voit tarkastella suorituslokia tai valmistelutietoja ja katsoa korjattavat virheet onnistuneen tuonnin varmistamiseksi.

> [!NOTE]
> Jos sinun täytyy tuoda useita tiedostomuotoja, luo erilliset tuontityöt kullekin muototyypille.

## <a name="reassign-the-credit-card-transactions-for-terminated-employees"></a>Niiden työntekijöiden luottokorttitapahtumien määrittäminen uudelleen, joiden työsuhde on päättynyt

Kun työntekijätietue päätetään, työntekijän Active Directory -toimialueen palveluiden (AD DS) tili poistetaan käytöstä. Aktiivisia luottokorttitapahtumia, jotka on veloitettava ja korvattava, voi kuitenkin yhä olla. **Luottokorttitapahtumat** -sivulla voit määrittää työntekijän uudelleen mihin tahansa luottokorttitapahtumaan, jonka työntekijän työsuhde on päättynyt.

Valitse vähintään yksi luottokorttitapahtuma ja valitse sitten **Määritä tapahtumat uudelleen**. Tämän jälkeen voit valita toisen työntekijän, jolle luottokorttitapahtumat määritetään. Kun luottokorttitapahtumat on määritetty uudelleen, ne voidaan valita kuluraporttia varten ja maksaa kuluraportin korvauksen normaalin prosessin avulla.
