---
title: Tarjouksen keskeiset käsitteet – lite
description: Tämä aihe tarjoaa tietoja Project Operationsin projektitarjousten käyttämisestä.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: e86f1a5a7b2859df5bf9569ee9ca306c6dcc6293
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/30/2020
ms.locfileid: "4178002"
---
# <a name="quotes---key-concepts---lite"></a>Tarjouksen keskeiset käsitteet – lite

_**Käytetään:** Lite-käyttöönotto – kauppa proformalaskutukseen_


Seuraavassa on tärkeitä käsitteitä, jotka kannattaa tietää ennen projektitarjousten käytön aloittamista Dynamics 365 Project Operationsissa:

## <a name="contracting-unit"></a>Sopimusyksikkö

Sopimusyksikkö tarkoittaa divisioonaa tai käytäntöä, joka omistaa projektitoimituksen. Voit määrittää resurssikustannuksia kullekin sopimusyksikölle. Kun resurssille määritetään resurssikustannukset sopimusyksikössä, voit myös määrittää eri kustannushinnat resursseille, joista tämä sopimusyksikkö lainaa, tai muusta yrityksen divisioonasta tai toiminnosta. Näitä kutsutaan siirtohinnoiksi, resurssilainoiksi tai vaihtohinnoiksi. Kun määrität muiden osastojen resurssien lainaamisen kustannukset, voit myös määrittää nämä kustannushinnat lainaavan divisioonan valuuttana.

## <a name="cost-currency"></a>Kustannuksen valuutta

Kustannusvaluutta Project Operationsissa on se valuutta, jossa kustannukset raportoidaan. Tämä valuutta johdetaan tarjouksen, palvelusopimuksen ja projektin **Sopimusyksikkö**-kenttään liitetystä valuutasta. Kustannukset voidaan kirjata mihin tahansa valuuttaan projektissa. Valuutan muunnon valuuttakustannukset on kuitenkin kirjattu projektin kustannusvaluuttaan.

Koska CDS-ympäristön valuuttakurssit eivät voi olla ajan tasalla, kustannusten näyttösummat voivat muuttua ajan mittaan, jos päivität valuutan vaihtokursseja. Tietokantaan kirjatut kustannukset säilyvät kuitenkin ennallaan, koska summat on tallennettu valuuttana, jossa ne ovat syntyneet.

## <a name="sales-currency"></a>Myynnin valuutta

Project Operationsin myyntivaluutta on valuutta, jossa arvioidut ja toteutuneet myyntisummat tallennetaan ja näytetään. Se on myös valuutta, jossa asiakasta laskutetaan sopimuksesta. Projektitarjouksessa myyntivaluutan oletusarvona on asiakas- tai asiakkuustietue, ja sitä voi muuttaa, kun tarjous luodaan. Kun tarjous on tallennettu, myyntivaluuttaa ei voi muuttaa. Tuote- ja projektihinnastot perustuvat oletusarvon mukaan tarjouksen myyntivaluuttaan.

Toisin kuin kustannukset, myyntiarvot voidaan kirjata vain myyntivaluuttana.

## <a name="billing-method"></a>Laskutustapa

Projekteissa on yleensä kiinteät maksut ja kulutussopimusmallit. Tämä on esitetty Project Operationsissa l **askutusmenetelmänä** ja siinä on kaksi arvoa, Aika ja materiaali sekä Kiinteä hinta.

- **Aika ja materiaali:** Tämä on kulutukseen perustuva sopimusmalli, jossa kunkin kustannuksen tukena on vastaava myyntituotto. Kun arvioit tai kerrytät kustannuksia, myös vastaava arvioitu ja toteutunut myynti lisääntyy. Voit määrittää ei-ylittämättömät rajat tarjousriveille, joilla on tämä laskutustapa. Tämä leikkaa varsinaisen myyntituoton. Arvioituun myyntituottoon eivät vaikuta ei-ylittämättömät rajat.
- **Kiinteä hinta:** Tämä on kiinteän maksun sopimusmalli, joka ilmaisee, että myyntiarvot ovat aiheutuneista kustannuksista riippumattomia. Myyntiarvo on kiinteä eikä muutu, kun arvioit tai kerrytät lisää kustannuksia.

## <a name="project-price-lists"></a>Projektihinnastot

Projektihinnastot ovat hinnastoja, joita käytetään ajan, kulujen ja muihin projektiin liittyvien komponenttien oletushintoihin, ei kustannushintoihin. Hinnastoja voi olla useita, ja kullakin hinnastolla voi olla omat voimassaoloajat kunkin projektitarjouksen osalta. Projekti hinnastojen päällekkäisiä voimassaolopäivämääriä ei tueta Project Operationsissa.

## <a name="product-price-lists"></a>Tuotehinnastot

Tuotehinnastot ovat hinnastoja, joita käytetään tarjouksen tuotepohjaisten rivien oletushintoihin, ei kustannushintoihin. Tarjouksessa on vain yksi tuotehinnasto.

## <a name="transaction-classes"></a>Tapahtumaluokat

Project Operations tukee neljää tapahtumaluokan tyyppiä:

- Aika
- Kulu
- Materiaali
- Maksu

Kustannusten ja myynnin arvot voidaan arvioida ja ne voidaan kerryttää Aika-, Kulu- ja Materiaali-tapahtumaluokissa. Maksu on vain myyntituoton tapahtumaluokka.

## <a name="work-entities-and-billing-entities"></a>Työkohteet ja laskutuskohteet

Töitä edustavat kohteet ovat projekteja ja tehtäviä. Laskutusta edustavat kohteet ovat tarjousrivejä ja sopimusrivejä. Voit linkittää erilaisia työkohteita laskutusasetuksiin liittämällä ne tarjous- tai sopimusriveihin.

## <a name="multi-customer-deals"></a>Monen asiakkaan tarjoukset

Monen asiakkaan tarjouksia tapahtuu silloin, kun laskutettavana on useampi kuin yksi asiakas. Yleisiä esimerkkejä tästä:

- **OEM-yritykset ja niiden yhteistyökumppanit:** Kumppanit ja jälleenmyyjät myyvät tuotetta lisäarvopalveluilla. Tämä on yleensä skenaario, jossa asiakkaan tietyn kaupan aikana OEM-valmistaja rahoittaa osan projektista. 

- **Julkisen sektorin projektit:** Useat paikallishallinnon osastot suostuvat rahoittamaan hanketta, ja ne laskutetaan aiemmin sovitun jaon mukaisesti. Esimerkiksi koulupiiri ja kaupungin tai paikallishallinnon osasto sopivat rahoittavansa uima-altaan rakentamista.

## <a name="invoice-schedules"></a>Laskutusaikataulut

Kullakin tarjousrivillä on oma laskutusaikataulu ja se on myös valinnainen. Laskutusaikatauluja luodaan tiettyjen alkamis- ja päättymispäivien sekä laskutustiheyden perusteella. Laskutusaikatauluja käytetään sopimusvaiheessa, kun automaattinen laskun luontiprosessi määritetään. Tarjousvaiheessa aikataulut ovat valinnaisia. Kun laskutussuunnitelmat luodaan **Tarjous**-vaiheessa, ne kopioidaan projektisopimukseen, joka luodaan, kun projektitarjous on voitettu.

## <a name="changes-from-dynamics-365-sales-quote"></a>Dynamics 365 Sales -tarjouksen muutokset:

Project Operationsin tarjoukset perustuvat Dynamics 365 Sales -tarjouksiin. Toiminnossa on kuitenkin joitakin tärkeitä eroja, jotka kannattaa tietää:

- **Muokkaa**- tai **Aktivoi**-toimintoja ei tueta.
- Project Operations -tarjouksilla on kaksi erityyppistä riviä. Yksi on projekteille ja toinen tuotteille.
- Project Operations -tarjouksilla on omat lomake- ja käyttöliittymäelementit, liiketoimintasäännöt, laajennusten liiketoimintalogiikka ja asiakaspuolen komentosarjat, jotka tekevät niistä erilaisia kuin Sales-tarjouksista.

Näistä syistä ei ole suositeltavaa käyttää Sales-tarjousta ja Project Operations -tarjousta yhtäläisinä.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]