---
title: Luottokortin integroinnin määrittäminen
description: Tässä aihessa on tietoja kuluun liittyvien luottokorttitapahtumien tuomisesta ja ylläpitämisestä.
author: suvaidya
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: ''
ms.author: shylaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 483775e1334a281026dbfaf214d06d235255f13e
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/28/2020
ms.locfileid: "3896817"
---
# <a name="set-up-credit-card-integration"></a>Luottokortin integroinnin määrittäminen

_**Koskee:** Project Operationsin resurssiin / muuhun kuin resurssiin perustuvia skenaarioita, Lite-käyttöönotto-kaupasta proformalaskutukseen_

Kuluihin liittyvät luottokorttitapahtumat voidaan määrittää automaattisesti tuotaviksi toistuvalla aikataululla. Vaihtoehtoisesti tapahtumat voidaan tuoda manuaalisesti tarvittaessa. Luottokorttitapahtumat tuodaan luottokorttitapahtumien tietoentiteetin kautta.

## <a name="import-credit-card-transactions"></a>Luottokorttitapahtumien tuominen

1. Valitse **Luottokorttitapahtumat**-sivulla **Tuo tapahtumat**. Jos avaat tietojen hallinnan ensimmäisen kerran, järjestelmän on päivitettävä tieto-entiteettiluettelo ennen kuin jatkat.
2. Anna **Nimi**-kenttään tuotavan työn yksilöivä kuvaus.
3. Valitse **Lähdetietojen muoto** -kentässä sen tiedoston muoto, joka sisältää tuotavat luottokorttitapahtumat.
4. Valitse **Lataa** ja etsi sitten tuotava tiedosto.
5. Kun tiedosto on ladattu, tarkista luottokorttitapahtumtiedoston ja luottokorttitapahtumien tietoentiteetin sarakkeiden yhdistämismääritys valitsemalla ruudun **Näytä yhdistämismääritys** -linkki. Jos löytyy yhdistämismääritysvirheitä tai jos yhdistämismääritys on muutettava, tee muutokset **Yhdistämismäärityksen visualisointi** -välilehdessä tai **Yhdistämismäärityksen tiedot** -välilehdessä.
6. Jos haluat automatisoida luottokorttitapahtumia, valitse **Luo toistuva tietotyö**. Tämän jälkeen voit määrittää toistuvuuden, joka määrittää, miten usein luottokorttitapahtumat tuodaan. Kun olet valmis, valitse **OK**.
7. Jos haluat tuoda valitun tiedoston nyt, valitse **Tuo**.
8. Jos tuonnin aikana tapahtuu virheitä, voit tarkastella suorituslokia tai valmistelutietoja ja katsoa korjattavat virheet onnistuneen tuonnin varmistamiseksi.

> [!NOTE]
> Jos sinun täytyy tuoda useita tiedostomuotoja, luo erilliset tuontityöt kullekin muototyypille.

## <a name="reassign-the-credit-card-transactions-for-terminated-employees"></a>Niiden työntekijöiden luottokorttitapahtumien määrittäminen uudelleen, joiden työsuhde on päättynyt

Kun työntekijätietue päätetään, työntekijän Active Directory -toimialueen palveluiden (AD DS) tili poistetaan käytöstä. Aktiivisia luottokorttitapahtumia, jotka on veloitettava ja korvattava, voi kuitenkin yhä olla. **Luottokorttitapahtumat**-sivulla voit määrittää työntekijän uudelleen mihin tahansa luottokorttitapahtumaan, jonka työntekijän työsuhde on päättynyt.

Valitse vähintään yksi luottokorttitapahtuma ja valitse sitten **Määritä tapahtumat uudelleen**. Tämän jälkeen voit valita toisen työntekijän, jolle luottokorttitapahtumat määritetään. Kun luottokorttitapahtumat on määritetty uudelleen, ne voidaan valita kuluraporttia varten ja maksaa kuluraportin korvauksen normaalin prosessin avulla.
