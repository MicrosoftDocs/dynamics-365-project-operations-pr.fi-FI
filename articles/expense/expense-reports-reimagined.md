---
title: Uudistetut matkalaskut
description: Tässä aiheessa on tietoja siitä, miten kuluraportin tapahtumien käyttökokemus on uusittu ja suunniteltu uudelleen.
author: suvaidya
manager: AnnBe
ms.date: 10/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: ''
ms.author: suvaidya
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: cd0d415b9cc85bac91de8fb9427da290ae0c6108
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/28/2020
ms.locfileid: "3897132"
---
# <a name="expense-reports-reimagined"></a>Uudistetut matkalaskut

Kuluraporttimerkintä on uusittu, jotta prosessia voidaan yksinkertaistaa ja raportin valmistumisessa tarvittavaa aikaa lyhentää. Tässä ovat uuden kulun käyttökokemuksen tärkeimmät osat:

- Uusi kulujen hallinnan työtila, jonka avulla voit käyttää delegoidun henkilön kuluja.
- Uusi kuitin täsmäytyskokemus, jotta voit paremmin näyttää otsikkotason kuitit ja yksinkertaistaa kuittien liittämistä kuluriveille.
- Uusi vain luku -ruudukko, jonka avulla voit tarkastella useita kulurivejä ja muita tietosarakkeita. Nyt voit nähdä kaikki eritellyt ja jaetut rivit sekä niiden ylätason kulut.
- Yksinkertaistettu ruutu kulujen muokkaamista varten.
- Uudelleensuunnitellut virhe-, varoitus- ja käytäntösanomat, jotka antavat oikean kontekstin ja tietoja ongelmasta ja sen ratkaisemisesta. Olemme poistaneet useita viestejä, jotka tulivat näkyviin, ennen kuin käyttäjät saattoivat suorittaa tehtävänsä ja käsitellä ongelmia.
- Uusi sivu, joka määrittää pakolliset kentät, valinnaiset kentät ja kentät, joita ei pitäisi sisällyttää. Tämän sivun avulla voit vähentää määritettyjen kenttien määrää.
- Kuluraporttien uusi ulkoasu, jotta raportit eivät enää vaikuta siltä kuin ne olisi suunniteltu kirjanpidon ammattilaisia varten.

Voit ottaa uuden käyttökokemuksen käyttöön ottamalla käyttöön **Kuluraporttien uusi suunnittelu** -ominaisuuden **Ominaisuuksien hallinta**-työtilan avulla. Kun otat tämän ominaisuuden käyttöön, suoritetaan seuraavat toiminnot:

- Aiemmin luotu Kulu-työtila korvataan uudella työtilalla.
- Kulukentän näkyvyydelle lisätään uusi valikon vaihtoehto.
- Kuluraporttien (nykyisen sivun) tai kuluraportin kenttien aiemmin luotuja valikkokohteita ei poisteta.
- Työnkulkujen ja hyväksyntöjen avulla käyttäjä siirretään yhä olemassa olevien kuluraporttien sivulle.

## <a name="getting-started-video-for-new-users"></a>Aloitusvideo uusille käyttäjille

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE2Y7gO]

[Kulujen käyttökokemus Dynamics 365 for Finance and Operations](https://youtu.be/Ocy-MsTvEE0) -video (yllä) [Finance and Operations -toistoluetteloon](https://www.youtube.com/playlist?list=PLcakwueIHoT_SYfIaPGoOhloFoCXiUSyW) YouTubessa.

## <a name="new-features"></a>Uudet ominaisuudet

| Uusi ominaisuus | Kuvaus |
|---|----|
| Kulu-kentän näkyvyys | Uuden asetussivun avulla voit määrittää, mitkä kentät on poistettava käytöstä organisaatiossa, mitkä kentät ovat pakollisia ja mitkä kentät on suositeltavia. |
| Pakolliset kentät | Uuden yksinkertaisen määrityksen avulla voit määrittää tietyt kentät pakolliseksi tarvitsematta käyttää käytäntökehystä. |
| Valinnaiset kentät | Valinnaisten kenttien toinen sivu on lisätty. Näin työntekijät eivät tunne, että heidän täytyy määrittää kentät, mutta kentät ovat yhä helposti käytettävissä. |
| Lisää liittämättömät kuitit | Mahdollisuus lisätä liittämättömiä kuitteja kuluraporttiin on näkyvämpi työtilassa ja kuluraportissa. |
| Parannettu viestintä | On parempi näkyvyys kuluriveille, joilla on varoituksia tai virheitä. |
| Sanomarivin viestien vähentäminen| Infolokin viestien määrää vähennettiin ja yritettiin estää päällekkäisten viestien näkyminen useissa tapauksissa. |
| Yhteen ryhmitellyt yleiset toiminnot | Käyttöliittymä siivottiin lisäämällä uusia toimintopainikkeita useimmille yleisille rivitason toiminnoille ja lisäämällä kolme pistettä sisältävän painikkeen (...) otsikolle ja muille harvemmin suoritettaville toiminnoille. |
| Uusi työtila näkyvyyden lisäämiseksi | Uusi työtila yhdistää ominaisuuksia ja linkkejä, joiden avulla käyttäjät voivat siirtyä eri alueisiin. |
| Lisää aiemmin luodut kulut ja kuitit kulun luonnin aikana | Kun luot kuluraportteja, voit lisätä kaikki tai valitut kulut ja kuitit. |
| Vaihtokurssilaskin | Lisätään valuuttakurssilaskin, jonka avulla voit laskea käteisellä maksettujen monivaluuttatapahtumien valuuttakursseja. |
| Tallenna ja lisää uusia kulurivejä | **Tallenna**- ja **Uusi**-painikkeet ovat käytettävissä, kun uusia kuluja syötetään, joten voit nopeasti syöttää kulurivejä. |
| Parempi näkyvyys jaetuille ja eritellyille riveille | Eritellyt ja jaetut rivit lisätään suoraan kululuetteloon näkyvyyden lisäämiseksi, ja niiden avulla voit helposti selvittää, onko virheitä. |
| Näytä kuitit erittelyn aikana | Kuitit voidaan näyttää erittelyn aikana. |

Alkuperäinen julkaisu keskittyy kulujen syöttämisen skenaarioihin. Kuluraporttien tarkistus- tai hyväksyntäskenaario jatkaa aiemmin luodun kulun syöttösivun käyttämistä.

Nykyisessä sivussa on seuraavat ominaisuudet, mutta ne eivät vielä näy uudella sivulla. Nämä ominaisuudet otetaan uudelleen käyttöön seuraavien useiden versioiden aikana:

- Hyväksynnät
- Ostoreskontran hyväksynnät ja mahdollisuus muokata kirjanpitoa
- Useita aloituskohtia
- Matkustusehdotuksen integraatio
- Kulukentän näkyvyyden tietoentiteetti
- Päivärahakulujen kirjaus
- Rivitason työnkulku
- Väliaikaisen hyväksyjän tuki
- Lisäerittely
