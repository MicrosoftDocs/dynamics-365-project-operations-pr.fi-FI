---
title: Luottokortin integroinnin määrittäminen
description: Tässä artikkelissa käsitellään kuluihin liittyvien luottokorttitapahtumien käsittelemistä.
author: suvaidya
ms.date: 11/17/2021
ms.topic: article
ms.prod: ''
ms.search.form: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.search.region: ''
ms.author: shylaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 4d32754548af67bdd5b9f7345f6363bd6193b36d
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8924472"
---
# <a name="set-up-credit-card-integration"></a>Luottokortin integroinnin määrittäminen

_**Koskee:** Project Operationsin resurssiin / muuhun kuin resurssiin perustuvia skenaarioita, Lite-käyttöönotto-kaupasta proformalaskutukseen_

Kuluihin liittyvät luottokorttitapahtumat voidaan määrittää automaattisesti tuotaviksi toistuvalla aikataululla. Vaihtoehtoisesti tapahtumat voidaan tuoda manuaalisesti tarvittaessa. Luottokorttitapahtumat tuodaan luottokorttitapahtumien tietoentiteetin kautta.

## <a name="import-credit-card-transactions"></a>Luottokorttitapahtumien tuominen

Voit tuoda luottokorttitapahtumia seuraavia vaiheita noudattamalla:

1. Valitse **Luottokorttitapahtumat**-sivulla **Tuo tapahtumat**. Jos avaat tietojen hallinnan ensimmäisen kerran, järjestelmän on päivitettävä tieto-entiteettiluettelo ennen kuin jatkat.
2. Kirjoita **Nimi**-kenttään tuontityön yksilöivä kuvaus.
3. Valitse **Lähdetietojen muoto** -kentässä sen tiedoston muoto, joka sisältää tuotavat luottokorttitapahtumat.
4. Valitse **Lataa** ja etsi sitten tuotava tiedosto.
5. Kun tiedosto on ladattu, tarkista luottokorttitapahtumtiedoston ja luottokorttitapahtumien tietoentiteetin sarakkeiden yhdistämismääritys valitsemalla ruudun **Näytä yhdistämismääritys** -linkki. Jos löytyy yhdistämismääritysvirheitä tai jos yhdistämismääritys on muutettava, tee muutokset **Yhdistämismäärityksen visualisointi** -välilehdessä tai **Yhdistämismäärityksen tiedot** -välilehdessä.
6. Jos haluat automatisoida luottokorttitapahtumia, valitse **Luo toistuva tietotyö**. Tämän jälkeen voit määrittää toistuvuuden, joka määrittää, miten usein luottokorttitapahtumat tuodaan. Kun olet valmis, valitse **OK**.
7. Jos haluat tuoda valitun tiedoston nyt, valitse **Tuo**.
8. Jos tuonnin aikana ilmenee virheitä, voit tarkastella suorituslokia tai väliaikaistietoja nähdäksesi virheet, jotka on korjattava, jotta tuonti onnistuisi.

> [!NOTE]
> Jos haluat tuoda useita tiedostomuotoja, luo erilliset tuontityöt kullekin muototyypille.

## <a name="reassign-the-credit-card-transactions-for-terminated-employees"></a>Niiden työntekijöiden luottokorttitapahtumien määrittäminen uudelleen, joiden työsuhde on päättynyt

Kun työntekijätietue päätetään, työntekijän Active Directory -toimialueen palveluiden (AD DS) tili poistetaan käytöstä. Aktiivisia luottokorttitapahtumia, jotka on veloitettava ja korvattava, voi kuitenkin yhä olla. **Luottokorttitapahtumat**-sivulla voit määrittää työntekijän uudelleen luottokortin tapahtumalle, jonka mukaan liitetty työntekijä on lopetettu.

Valitse vähintään yksi luottokorttitapahtuma ja valitse sitten **Määritä tapahtumat uudelleen**. Tämän jälkeen voit valita toisen työntekijän, jolle luottokorttitapahtumat määritetään. Kun luottokorttitapahtumat on määritetty uudelleen, ne voidaan valita kuluraporttia varten ja maksaa kuluraportin korvauksen normaalin prosessin avulla.

## <a name="delete-credit-card-transactions"></a>Luottokorttitapahtumien poistaminen 

Joskus luottokorttitapahtumien tuonnin jälkeen jotkin tapahtumat on ehkä poistettava. Tämä voi johtuu siitä, että tapahtumat ovat kaksoiskappaleita tai koska tiedot eivät pidä paikkansa. Järjestelmänvalvojat voivat käyttää **Luottokorttitapahtumien poistaminen** -toimintoa valitakseen ja poistaakseen luottokorttitapahtumia, joita **ei ole liitetty** kuluraporttiin. 

1. Siirry kohtaan **Jaksoittaiset tehtävät** > **Poista luottokorttitapahtumia**.
2. Valitse **Suodata** ja anna sisällytettävät tietueet tunnistavat tiedot.
3. Voit poistaa tietueet valitsemalla **OK**. 

## <a name="storing-credit-card-numbers"></a>Tallentaa luottokorttinumeroita

Luottokortin numero voidaan tallentaa kolmella eri tavalla. Luottokortin numerot tallennetaan **Kulunhallinnan parametrit** -sivulle.

- **Kortin numeron syöttämisen estäminen** – luottokorttinumeroita ei tallenneta.
- **Hajautuskoodikortin numerot (myymälän viimeiset 4 numeroa)** – Luottokortin numeroiden neljä viimeistä numeroa tallennetaan salatussa muodossa.
- **Kortin tallennusnumerot** – luottokortin numerot tallennetaan salaamattomaan muotoon. Tämä vaihtoehto ei ole DSS (Payment Card Industry, PCI) Data Security Standard (DSS) -standardin mukainen. Jotta organisaatio olisi PCI DSS -määräysten mukainen, organisaation järjestelmänvalvojien on valittava, että luottokorttinumeroita ei tallenneta tai hajautuskoodikortin numeroita säilytetään.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
