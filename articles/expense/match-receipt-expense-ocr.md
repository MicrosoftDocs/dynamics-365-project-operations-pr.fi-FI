---
title: Kuitin ja kulun täsmäyttäminen OCR-tunnistuksella
description: Tässä aiheessa on tietoja kuittien optisesta merkintunnistuksesta (OCR).
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
ms.openlocfilehash: 02c1bafbe907a657689b610ae792f88085320903
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/28/2020
ms.locfileid: "3896997"
---
# <a name="match-a-receipt-to-an-expense-using-ocr"></a>Kuitin ja kulun täsmäyttäminen OCR-tunnistuksella

_**Koskee:** Project Operationsin resurssiin / muuhun kuin resurssiin perustuvia skenaarioita, Lite-käyttöönotto-kaupasta proformalaskutukseen_

Kulun syöttöä on parannettu kuittien optisen merkintunnistuksen (OCR) käsittelyn avulla. Tämä toiminto on suunniteltu parantamaan kuluraporttien luomisen käyttökokemusta.

## <a name="key-features"></a>Tärkeimmät ominaisuudet

- Järjestelmä poimii myyjän nimen, päivämäärän ja kokonaissumman kuiteista.
- Järjestelmä yrittää määrittää liittämättömät kuitit liittämättömiin kulutapahtumiin.
- Voit luoda manuaalisesti syötettyjä kulutapahtumia kuiteista.

## <a name="attach-receipts-to-an-expense-report"></a>Kuittien liittäminen kuluraportteihin

Jos haluat liittää kuluraportin luomisen yhteydessä automaattisesti luottokorttitapahtumia sisältävät kuitit, suorita seuraavat vaiheet.

  1. Avaa **Kulun hallinta** -työtila.
  2. Tarkista **Kuitit**-välilehdessä, että liitetyt kuitit ovat olemassa. Voit myös ladata kuitit **Kuitit**-välilehteen.
  3. Tarkista **Kulut**-välilehdessä, että liitetyt kulut ovat olemassa. Yleensä kulujen järjestelmänvalvoja tuo nämä kulut luottokortin myöntäjältä.
  4. Valitse **Uusi kuluraportti**. Huomaa, että voit lisätä kuluja ja kuitteja myös nyt, kun luot kuluraportin. Jos lisäät sekä kuluja että kuitteja, järjestelmä käynnistää kuittausten automaattisen täsmäytyksen kuluihin.

## <a name="create-or-match-receipts-to-an-expense-report"></a>Kuittien luominen tai liittäminen kuluraportteihin
Jos haluat luoda kulun tai määrittää kuitin kulun vastaavuuden, tee seuraavat vaiheet.

  1. Liitä kuluraportin **Kuitit**-välilehteen kuitti valitsemalla **Lisää kuitteja**.
  2. Huomaa kuitin ladatun kuvan alla olevat **Luo**- ja **Määritä vastaavuus** -vaihtoehdot.

      - Valitse **Luo**, jos haluat luoda manuaalisesti syötetyn kulutapahtuman ja täyttää arvot, jotka on poimittu kuitista.
      - Jos valitset **Määritä vastaavuus**, järjestelmä yrittää määrittää olemassa olevan kulun ja kuitin vastaavuuden.

## <a name="installation"></a>Asennus

Jos haluat käyttää kulujen lisäominasuuksia, asenna Microsoft Dynamics 365 Financen kulujen hallintapalvelun apuohjelma ja ota toiminnot käyttöön esiintymässä. Voit käyttää Microsoft Dynamics Lifecycle Services (LCS) -sovelluksen projektin apuohjelmaa.

1. Kirjaudu sisään LCS-sovellukseen ja avaa haluamasi ympäristö.
2. Siirry kohtaan **Täydelliset tiedot**.
3. Valitse **Ylläpidä** tai siirry **Ympäristön apuohjelmat** -pikavälilehteen virittämällä.
4. Valitse **Asenna uusi apuohjelma**.
5. Valitse **Kulujen hallintapalvelu**.
6. Seuraa asennusopasta ja hyväksy ehdot.
7. Valitse **Asennus**.

Ota **Ominaisuuksien hallinta** -työtilassa käyttöön seuraavat ominaisuudet:

- Uudistetut kuluraportit
- Automaattinen vastaavuus ja kulun luominen kuitista

Kun otat nämä ominaisuudet käyttöön, suoritetaan seuraavat toiminnot:

- Aiemmin luotu **Kulun hallinta** -työtila korvataan uudella työtilalla.
- Kulukentän näkyvyydelle lisätään uusi valikon vaihtoehto.
- Voit yhä avata aiemman **Kuluraportit**-sivun siirtymällä kohtaan **Kulujen hallinta > Omat kulut > Kuluraportit**.
- Työnkulkujen ja hyväksyntöjen avulla käyttäjä siirretään yhä olemassa olevien kuluraporttien sivulle.
- Microsoft Azure Cognitive Services -sovellus käsittelee kuitit ja metatiedot puretaan ja lisätään.
- Järjestelmä lisää vaihtoehdon sellaisen kuluraportin luomista varten, joka sisältää liittämättömiä kuitteja, joiden vastaavuutta ei ole määritetty.
- Kuluraportteihin lisättävän vaihtoehdon avulla voit luoda kulurivin kuitista tai yrittää määrittää olemassa olevan kuitin ja olemassa olevan kulurivin vastaavuuden.

## <a name="frequently-asked-questions"></a>Usein kysyttyjä kysymyksiä

**Käyttääkö Microsoft tietojani malleissa?**

Ei. Microsoft on rakentanut yleisen koneoppiminen mallin kuittien käsittelypalvelua varten. Tämä malli ei perustu kuitteihin, joita käyttäjä lataa.

**Missä tämä toiminto on käytettävissä ja missä sitä käsitellään?**

Tällä hetkellä tuetaan käyttöä Yhdysvalloissa.

**Minne kuitit siirretään?**

Finance ottaa yhteyttä Cognitive Services -sovellukseen ja purkaa kentän tiedot. Cognitive Services -sovellus säilyttää kuittikopion käsittelyn ajan, mutta enintään 24 tuntia. Kun käsittely on valmis, Cognitive Services poistaa kuitin. Kuitit tallennetaan edelleen Finance-sovellukseen.

Lisätietoja on kohdassa [Lisätietoja kuiteista lomakkeen tunnistustoiminnon uuden ominaisuuden avulla](https://azure.microsoft.com/blog/enable-receipt-understanding-with-form-recognizer-s-new-capability/).
