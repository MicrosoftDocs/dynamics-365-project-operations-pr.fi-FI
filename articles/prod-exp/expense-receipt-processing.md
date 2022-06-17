---
title: Kulukuittien käsittely
description: Tässä artikkelissa on tietoja kuittien optisesta merkintunnistuksesta (OCR). Tämä ominaisuus on suunniteltu parantamaan käyttökokemusta, kun luodaan kuluraportteja Microsoft Dynamics 365 Financessa.
author: stsporen
ms.date: 05/14/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.region: Global
ms.author: stsporen
ms.search.validFrom: 2019-11-20
ms.dyn365.ops.version: 10.0.8
ms.openlocfilehash: 5a72802e3c52b6a9e55ac779aa36c32072dc8b8b
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8911408"
---
# <a name="expense-receipt-processing"></a>Kulukuittien käsittely

Kulun syöttöä on parannettu kuittien optisen merkintunnistuksen (OCR) käsittelyn avulla. Tämä ominaisuus on suunniteltu parantamaan luotujen kuluraporttien käyttökokemusta.

## <a name="key-features"></a>Tärkeimmät ominaisuudet

- Myyjän nimi, päivämäärä ja kokonaissumma poimitaan kuiteista.
- Ominaisuus yrittää määrittää liittämättömät kuitit liittämättömiin kulutapahtumiin.
- Käyttäjät voivat luoda manuaalisesti syötettyjä kulutapahtumia kuiteista.

## <a name="usage-examples"></a>Käyttöesimerkkejä

Jos haluat liittää kuluraportin luomisen yhteydessä automaattisesti luottokorttitapahtumia sisältävät kuitit, tee seuraavat vaiheet:

  1. Avaa **Kulun hallinta** -työtila.
  2. Tarkista **Kuitit**-välilehdessä, että liitetyt kuitit ovat olemassa. Voit myös ladata kuitit **Kuitit**-välilehteen.
  3. Tarkista **Kulut**-välilehdessä, että liitetyt kulut ovat olemassa. Yleensä kulujen järjestelmänvalvoja tuo nämä kulut luottokortin myöntäjältä.
  4. Valitse **Uusi kuluraportti**. Huomaa, että voit lisätä kuluja ja kuitteja myös nyt, kun luot kuluraportin. Jos lisäät sekä kuluja että kuitteja, järjestelmä käynnistää kuittausten automaattisen täsmäytyksen kuluihin.

Jos haluat luoda kulun tai määrittää kuitin kulun vastaavuuden, tee seuraavalla tavalla:

  1. Liitä kuluraportin **Kuitit**-välilehteen kuitti valitsemalla **Lisää kuitteja**.
  2. Huomaa kuitin ladatun kuvan alla olevat **Luo**- ja **Määritä vastaavuus** -vaihtoehdot.

      - Valitse **Luo**, jos haluat luoda manuaalisesti syötetyn kulutapahtuman ja täyttää arvot, jotka on poimittu kuitista.
      - Jos valitset **Määritä vastaavuus**, järjestelmä yrittää määrittää olemassa olevan kulun ja kuitin vastaavuuden.

## <a name="installation"></a>Asennus

Tämä ominaisuus toimii yhdessä **uudelleen suunniteltujen kuluraporttien** kanssa, mikä helpottaa kulukokemusta. Tämä ominaisuus on käytettävissä vain Tier 2+-ympäristöissä, jotka ovat eritys- ja tuotantoympäristö.

Jos haluat käyttää näitä kehittyneitä kuluominaisuuksia, asenna Microsoft Dynamics 365 Financen kulujenhallintapalvelu ja ota ominaisuudet käyttöön esiintymässäsi. Voit käyttää Microsoft Dynamics Lifecycle Services (LCS) -sovelluksen projektin apuohjelmaa.

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

Lisätietoja kuluraporttien uudelleenkuvioitavista ominaisuuksista on kohdassa [Uudelleen suunnitellut kuluraportit](ExpenseWorkspaceNew.md).

## <a name="frequently-asked-questions"></a>Usein kysyttyjä kysymyksiä

**Käyttääkö Microsoft tietojani malleissa?**

Ei. Microsoft on rakentanut yleisen koneoppiminen mallin kuittien käsittelypalvelua varten. Tämä malli ei perustu kuitteihin, joita käyttäjä lataa.

**Missä tämä toiminto on käytettävissä ja missä sitä käsitellään?**

Tällä hetkellä tuetaan käyttöä Yhdysvalloissa.

**Minne kuitit siirretään?**

Finance ottaa yhteyttä Cognitive Services -sovellukseen ja purkaa kentän tiedot. Cognitive Services -sovellus säilyttää kuittikopion käsittelyn ajan, mutta enintään 24 tuntia. Kun käsittely on valmis, Cognitive Services poistaa kuitin. Kuitit tallennetaan edelleen Finance-sovellukseen.

Lisätietoja on kohdassa [Lisätietoja kuiteista lomakkeen tunnistustoiminnon uuden ominaisuuden avulla](https://azure.microsoft.com/blog/enable-receipt-understanding-with-form-recognizer-s-new-capability/).


[!INCLUDE[footer-include](../includes/footer-banner.md)]