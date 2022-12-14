---
title: Projektipohjaisten tarjousten yksilölliset käsitteet
description: Tässä artikkelissa on tietoja projektitarjouksista Microsoft Dynamics 365 Project Operationsissa.
author: rumant
ms.date: 12/02/2022
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: rumant
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 89867cfbe92f47d58b16da40b62d3d9dd6a15b64
ms.sourcegitcommit: e0cbbe7c6f03d4978134405cf04bd8bc1d019f65
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/05/2022
ms.locfileid: "9824323"
---
# <a name="concepts-unique-to-project-based-quotes"></a>Projektipohjaisten tarjousten yksilölliset käsitteet

_**Käytetään:** Project Operationsin resursseihin ja ei-varastoitaviin perustuvissa skenaarioissa_

Seuraavat ovat tärkeimmät käsitteet, jotka on otettava huomioon, ennen kuin aloitat projektitarjousten käyttämisen Microsoft Dynamics 365 Project Operationsissa.

## <a name="owning-company"></a>Omistava yritys

Omistava yritys kuvaa yritystä, joka omistaa projektin toimituksen. Tarjouksen asiakkaan on oltava kelvollinen asiakas tässä yrityksessä rahoitus- ja toimintosovelluksissa. Omistavan yrityksen valuutan ja projektipohjaisesta tarjouksesta valitun sopimusyksikön valuutan on vastattava toisiaan.

## <a name="contracting-unit"></a>Sopimusyksikkö

Sopimusyksikkö tarkoittaa divisioonaa tai käytäntöä, joka omistaa projektitoimituksen. Voit määrittää resurssikustannuksia kullekin sopimusyksikölle. Kun resurssille määritetään resurssikustannukset sopimusyksikössä, voit myös määrittää eri kustannushinnat resursseille, joista tämä sopimusyksikkö lainaa, tai muille yrityksen divisioonille tai käytännöille. Näitä kustannushintoja kutsutaan siirtohinnoiksi, resurssilainoiksi tai vaihtohinnoiksi. Kun määrität muiden osastojen resurssien lainaamisen kustannukset, voit myös määrittää nämä kustannushinnat lainaavan divisioonan valuuttana.

## <a name="cost-currency"></a>Kustannuksen valuutta

Kustannusvaluutta Project Operationsissa on se valuutta, jossa kustannukset raportoidaan. Tämä valuutta johdetaan tarjouksen, palvelusopimuksen ja projektin **Sopimusyksikkö**-kenttään liitetystä valuutasta. Kustannukset voidaan kirjata mihin tahansa valuuttaan projektissa. Valuutan muunnon valuuttakustannukset on kuitenkin kirjattu projektin kustannusvaluuttaan.

Koska Dataverse-ympäristön valuuttakurssit eivät voi olla ajan tasalla, kustannusten näyttösummat voivat muuttua ajan mittaan, jos päivität valuutan vaihtokursseja. Tietokantaan kirjatut kustannukset säilyvät kuitenkin ennallaan, koska summat on tallennettu valuuttana, jossa ne ovat syntyneet.

## <a name="sales-currency"></a>Myynnin valuutta

Project Operationsin myyntivaluutta on valuutta, jossa arvioidut ja toteutuneet myyntisummat tallennetaan ja näytetään. Se on myös valuutta, jossa asiakasta laskutetaan sopimuksesta. Projektitarjouksessa myyntivaluutan oletusarvona on asiakas- tai tilitietue, ja sitä voi muuttaa, kun tarjous luodaan. Kun tarjous on tallennettu, myyntivaluuttaa ei voi muuttaa. Oletusarvoiset uote- ja projektihinnastot perustuvat tarjouksen myyntivaluuttaan.

Toisin kuin kustannukset, myyntiarvot voidaan kirjata **vain** myyntivaluuttana.

## <a name="billing-method"></a>Laskutustapa

Projekteissa on yleensä kiinteät maksut ja kulutussopimusmallit. Project Operationsissa projektin sopimusmallia edustaa laskutustapa. Laskutustavalla on kaksi arvoa: Aika ja materiaali tai Kiinteä hinta.

- **Aika ja materiaali** - Kulutukseen perustuva sopimusmalli, jossa kunkin kustannuksen tukena on vastaava myyntituotto. Kun arvioit tai kerrytät kustannuksia, myös vastaava arvioitu ja toteutunut myynti lisääntyy. Voit määrittää ei-ylittämättömät rajat tarjousriveille, joilla on tämä laskutustapa. Näin voit tallentaa myös todellisen tuoton. Arvioituun myyntituottoon eivät vaikuta ei-ylittämättömät rajat.
- **Kiinteä hinta** - Kiinteän maksun sopimusmalli, joka ilmaisee, että myyntiarvot ovat aiheutuneista kustannuksista riippumattomia. Myyntiarvo on kiinteä eikä muutu, kun arvioit tai kerrytät lisää kustannuksia.

## <a name="project-price-lists"></a>Projektihinnastot

Projektihinnastot ovat hinnastoja, joita käytetään ajan, kulujen ja muihin projektiin liittyvien komponenttien oletushintojen syöttämiseen, ei kustannushintoihin. Hinnastoja voi olla useita, ja kullakin hinnastolla voi olla omat voimassaoloajat kunkin projektitarjouksen osalta. Project Operations ei tue projektin hinnastojen päivämäärien päällekkäisyyttä.

## <a name="product-price-lists"></a>Tuotehinnastot

Tuotehinnastot ovat hinnastoja, joita käytetään tarjouksen tuotepohjaisten rivien oletushintojen syöttämiseen, ei kustannushintoihin. Tarjouksessa on vain yksi tuotehinnasto.

## <a name="transaction-classes"></a>Tapahtumaluokat

Project Operations tukee neljää tapahtumaluokan tyyppiä:

- Aika
- Kulu
- Materiaali
- Maksu

Kustannusten ja myynnin arvot voidaan arvioida ja ne voidaan kerryttää **Aika**-, **Kulu**- ja **Materiaali**-tapahtumaluokissa. **Maksu** on vain myyntituoton tapahtumaluokka.

## <a name="work-entities-and-billing-entities"></a>Työkohteet ja laskutuskohteet

Projektit ja tehtävät ovat työtä edustavia entiteettejä. Tarjousrivit ja sopimusrivit ovat laskutusta edustavia entiteettejä. Voit linkittää erilaisia työkohteita laskutusasetuksiin liittämällä ne tarjous- tai sopimusriveihin.

## <a name="multi-customer-deals"></a>Monen asiakkaan tarjoukset

Monen asiakkaan tarjouksia tapahtuu silloin, kun laskutettavana on useampi kuin yksi asiakas laskua kohti. Seuraavassa on joitakin tyypillisiä esimerkkejä:

- **Alkuperäiset laitteiden valmistajayritykset (OEM) ja niiden kumppanit** – Kumppanit ja jälleenmyyjät myyvät tuotteen, joka sisältää lisäarvoa tuottavia palveluita. Asiakkaan kaupan aikana OEM rahoittaa tavallisesti osan projektista.
- **Julkisen sektorin projektit** - Useat paikallishallinnon osastot suostuvat rahoittamaan hanketta, ja niitä laskutetaan aiemmin sovitun jaon mukaisesti. Esimerkiksi koulupiiri ja kaupungin tai paikallishallinnon osasto sopivat rahoittavansa uima-altaan rakentamista.

## <a name="invoice-schedules"></a>Laskutusaikataulut

Kullakin tarjousrivillä on oma laskutusaikataulu ja se on myös valinnainen. Laskutusaikatauluja luodaan tiettyjen alkamis- ja päättymispäivien sekä laskutustiheyden perusteella. Niitä käytetään sopimusvaiheessa, kun automaattinen laskun luontiprosessi määritetään. Tarjousvaiheessa aikataulut ovat valinnaisia. Kun laskutussuunnitelmat luodaan tarjousvaiheessa, ne kopioidaan projektisopimukseen, joka luodaan, kun projektitarjous on voitettu.

## <a name="differences-from-dynamics-365-sales-quotes"></a>Erot Dynamics 365 Sales -tarjouksiin

Project Operationsin tarjoukset perustuvat Dynamics 365 Sales -tarjouksiin. Toiminnossa on kuitenkin joitakin tärkeitä eroja, jotka kannattaa tietää:

- Project Operationsin tarjouksilla on kaksi erityyppistä riviä: yksi projekteille ja toinen tuotteille.
- Project Operations -tarjouksilla on omat sivunsa ja lomake- ja käyttöliittymäelementtinsa, liiketoimintasäännöt, laajennusten liiketoimintalogiikka ja asiakaspuolen komentosarjat, jotka tekevät niistä erilaisia kuin Sales-tarjouksista.
- Voit liittää Salesissa useita tilauksia yhteen myyntitarjoukseen. Project Operationsissa projektitarjoukseen voi liittää vain yhden projektisopimuksen.
- Kun voitat myyntitarjouksen, siihen liittyvä mahdollisuus voi säilyä avoimena. Kun projektitarjous on voitettu, siihen liittyvä mahdollisuus suljetaan.
- Myyntitarjous ei sisällä kaikkia projektitarjouksessa olevia kenttiä ja konsepteja. Kenttiä ovat esimerkiksi **Sopimusyksikkö**, **Asiakaspäällikkö** ja **Laskutusyhteyshenkilön nimi**.
- Myynti- ja projektitarjouksille määritetään myös asetusjoukkoperusteinen kenttä **Tyyppi**. Myyntitarjouksessa tällä kentällä on arvo **Nimikepohjainen**. Projektitarjouksessa sen arvo on **Työpohjainen**.

Näiden erojen vuoksi emme suosittele käyttämään Salesin ja Project Operationsin tarjouksia toistensa vaihtoehtoina.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
