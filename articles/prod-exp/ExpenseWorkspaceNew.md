---
title: Uudelleen suunnitellut kuluraportit
description: Tässä aiheessa on tietoja siitä, miten kuluraportin tapahtumien käyttökokemus on uusittu ja suunniteltu uudelleen.
author: ryansandness
ms.date: 06/14/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.region: Global
ms.author: suvaidya
ms.search.validFrom: 2019-6-30
ms.dyn365.ops.version: 10.0.3
ms.openlocfilehash: cad971f3b45faf13dab4cd71ff7439c44b2e7b61
ms.sourcegitcommit: 2c2a5a11d446adec2f21030ab77a053d7e2da28e
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/04/2022
ms.locfileid: "8685650"
---
# <a name="redesigned-expense-reports"></a>Uudelleen suunnitellut kuluraportit

Kuluraporttimerkintä on suunniteltu uudelleen yksinkertaistamaan kuluraporttien täyttämistä ja lyhentämään tarvittavaa aikaa. Tässä ovat uuden kulun käyttökokemuksen tärkeimmät osat:

- Uusi kulujen hallinnan työtila, jonka avulla voit käyttää delegoidun henkilön kuluja.
- Uusi kuitin täsmäytyskokemus, jotta voit paremmin näyttää otsikkotason kuitit ja yksinkertaistaa kuittien liittämistä kuluriveille.
- Uusi vain luku -ruudukko, jonka avulla voit tarkastella useita kulurivejä ja muita tietosarakkeita. Nyt voit nähdä kaikki eritellyt ja jaetut rivit sekä niiden ylätason kulut.
- Yksinkertaistettu ruutu kulujen muokkaamista varten.
- Uudelleen suunnitellut virhe-, varoitus- ja käytäntöviestit takaavat, että sinulla on oikea konteksti ongelman ymmärtämiseen ja sen ratkaisemiseen. Microsoft on poistanut useita viestejä, jotka tulivat näkyviin, ennen kuin käyttäjillä oli mahdollisuus suorittaa tehtävänsä ja käsitellä ongelmia, kuten epätäydellinen erittelysanoma.
- Uusi sivu, joka määrittää organisaation edellyttämät kentät, mitkä kentät ovat valinnaisia ja mitä kenttiä ei pitäisi siepata. Tämä sivu auttaa vähentämään käyttäjien asettamien kenttien määrää.
- Kuluraporttien uusi ulkoasu, jotta raportit eivät enää vaikuta siltä kuin ne olisi suunniteltu kirjanpidon ammattilaisia varten.

Voit ottaa uuden käyttökokemuksen käyttöön ottamalla käyttöön **Kuluraporttien uusi suunnittelu** -ominaisuuden **Ominaisuuksien hallinta**-työtilan avulla. Kun otat tämän ominaisuuden käyttöön, suoritetaan seuraavat toiminnot:

- Aiemmin luotu Kulu-työtila korvataan uudella työtilalla.
- Kulukentän näkyvyydelle lisätään uusi valikon vaihtoehto.
- Kuluraporttien (nykyisen sivun) tai kuluraportin kenttien aiemmin luotuja valikkokohteita ei poisteta.
- Työnkulkujen ja hyväksyntöjen avulla käyttäjä siirretään yhä olemassa olevien kuluraporttien sivulle.

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
| Parempi näkyvyys jaetuille ja eritellyille riveille | Eritellyt ja jaetut rivit lisätään suoraan kululuetteloon näkyvyyden lisäämiseksi, ja niiden avulla voit helposti selvittää, onko käytäntövirheitä tai muita virheitä. |
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


[!INCLUDE[footer-include](../includes/footer-banner.md)]