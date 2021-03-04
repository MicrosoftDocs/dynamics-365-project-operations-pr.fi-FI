---
title: Kulujen hallinnan työnkulku
description: Tässä aiheessa kerrotaan, miten voit käyttää työnkulkujärjestelmää Microsoft Dynamics 365 Finance -järjestelmässä ja määrittää kuluraporttien tarkistusprosessin kulunhallinnassa.
author: ShylaThompson
manager: AnnBe
ms.date: 09/13/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WorkflowtableListPageRnr
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: bbee90450749c89f643d96e4d41a387c45e9abc5
ms.sourcegitcommit: 9f31b33ed6e7f1b49200a407913201a1337f3401
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/14/2021
ms.locfileid: "4960558"
---
# <a name="expense-management-workflow"></a>Kulujen hallinnan työnkulku

Voit käyttää työnkulkujärjestelmää määrittääksesi kuluraporttien tarkistusprosessin kulunhallinnassa. Voit määrittää työnkulun, joka määrittää seuraavia ehtoja käyttäen, kuka hyväksyy kuluraportit:

- Työntekijöiden raportointihierarkia ja valmiit hyväksyntärajat
- Monitasoinen hyväksyntä, joka tukee väliaikaisia hyväksyjiä ja lopullista hyväksyjää
- Taloushallinnon dimensiot ja projektivastuu
- Delegointi tietyille käyttäjille tai käyttäjäryhmille

Työnkulun hyväksyntöjä voi luoda kuluraportteja, matkustusehdotuksia, käteisennakkoja ja arvonlisäveroa (ALV) varten.

**Esimerkki**

Seuraava prosessi on esimerkki kuluraportin kulunhallinnan työnkulusta.

1. Työntekijä luo ja tallentaa kuluraportin.
2. Työntekijä lähettää kuluraportin hyväksyttäväksi. Hyväksyjä tunnistetaan työnkulun määrittämisen yhteydessä määritettyjen sääntöjen perusteella.
3. Hyväksyjä saa ilmoituksen siitä, että kuluraportti on valmis hyväksyttäväksi. Hyväksyjä tarkistaa kuluraportin ja varmistaa, että seuraavat ehdot täyttyvät:

    - Kulut eivät riko mitään kulukäytäntöjä. Jos kulu rikkoo käytäntöä, hyväksyjä tarkistaa, että kuluraportti sisältää kelvollisen liiketoimintaperusteen.
    - Sähköiset kuitit on liitetty kuluraporttiin.

4. Hyväksyjä hyväksyy kuluraportin.
5. Kuluraportti delegoidaan ostoreskontran koordinaattorille kirjausta varten.
6. Jokin seuraavista vaiheista tapahtuu sen mukaan, onko automaattinen kirjaaminen määritetty:

    - Jos automaattinen kirjaus on määritetty, kuluraportti käsitellään maksua varten ja kuluraportin tila päivittyy.
    - Jos automaattista kirjausta ei määritetä, ostoreskontrakoordinaattori tarkistaa, että kaikki alkuperäiset kuitit on lähetetty ja että vastaanotot on kohdistettu kuluraportin kulujen kanssa. Kaikki kuluraporttiin kirjoitetut verokoodit on myös tarkistettava oikeiksi.

Kun nämä vaatimukset on tarkistettu, kuluraportti kirjataan.

Kun kuluraportti on kirjattu, maksu on sallittu kuluraportille ja työntekijälle hyvitetään.
