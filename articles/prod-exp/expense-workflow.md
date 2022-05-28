---
title: Kulujen hallinnan työnkulku
description: Tässä ohjeaiheessa kerrotaan, miten Microsoft Dynamics 365 Financen työnkulkujärjestelmää käytetään kuluraporttien tarkastusprosessien luomiseen kulujenhallinnassa.
author: ShylaThompson
ms.date: 09/13/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WorkflowtableListPageRnr
audience: Application User
ms.reviewer: johnmichalak
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3eb4d57194ce2dd7f80d75c2c765f1cfa48b0348
ms.sourcegitcommit: 2c2a5a11d446adec2f21030ab77a053d7e2da28e
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/04/2022
ms.locfileid: "8684270"
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


[!INCLUDE[footer-include](../includes/footer-banner.md)]