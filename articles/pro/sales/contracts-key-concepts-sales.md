---
title: Projektin palvelusopimusten keskeiset käsitteet – lite
description: Tässä aiheessa on tietoja projektitarjousten avainkonsepteista.
author: rumant
manager: Annbe
ms.date: 10/07/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: ce37c9dd18fd01e599e8766389e42c066e182547
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/30/2020
ms.locfileid: "4177057"
---
# <a name="project-contracts---key-concepts---lite"></a>Projektin palvelusopimusten keskeiset käsitteet – lite

_**Käytetään:** Lite-käyttöönotto – kauppa proformalaskutukseen_

Tässä aiheessa on avainkäsitteitä, jotka kannattaa tietää ennen projektisopimusten käytön aloittamista Dynamics 365 Project Operationsissa:

## <a name="contracting-unit"></a>Sopimusyksikkö

Sopimusyksikkö tarkoittaa divisioonaa tai käytäntöä, joka omistaa projektin toimituksen. Voit määrittää resurssikustannuksia kullekin sopimusyksikölle. Kun määrität resurssille resurssin kustannukset, voit myös määrittää resursseille eri kustannushinnat. Tämä hankintayksikkö lainaa nämä resurssit yrityksen muista divisioonista tai käytännöistä. Resurssien kustannuksia kutsutaan siirtohinnoiksi, resurssilainoiksi tai vaihtohinnoiksi. Kun määrität muiden osastojen resurssien lainaamisen kustannuskurssit, käytä lainaavan divisioonan valuuttaa.

## <a name="cost-currency"></a>Kustannuksen valuutta

Kustannusvaluutta on se valuutta, jossa kustannukset raportoidaan ruudulla. Tämä valuutta johdetaan palvelusopimuksen ja projektin **Sopimusyksikkö**-kenttään liitetystä valuutasta. Kustannukset voidaan kirjata mihin tahansa valuuttaan projektissa. Valuutan muunnon valuuttakustannukset on kuitenkin kirjattu projektin kustannusvaluuttaan, kun ne näytetään ruudulla.

Koska Common Data Service (CDS) -ympäristön valuuttakurssit eivät voi olla ajan tasalla, kustannusten näyttösummat voivat muuttua ajan mittaan, jos päivität valuutan vaihtokursseja. Tietokantaan kirjatut kustannukset säilyvät kuitenkin ennallaan, koska summat on tallennettu valuuttana, jossa ne ovat syntyneet.

## <a name="sales-currency"></a>Myynnin valuutta

Project Operationsin myyntivaluutta on valuutta, jossa arvioidut ja toteutuneet myyntisummat tallennetaan ja näytetään. Se on myös myyntivaluutta, jossa asiakasta laskutetaan sopimuksesta. Projektisopimuksessa myyntivaluutan oletusarvona on asiakas- tai asiakkuustietue, ja sitä voi muuttaa, samalla kun sopimus luodaan. Kun palvelusopimus luodaan sulkemalla tarjous voitettuna, palvelusopimuksen valuutan oletusarvona on tarjouksen valuutta.

Kun luot projektisopimuksen alusta alkaen, **myyntivaluutta**-kenttää ei voi muokata. Tuote- ja projektihinnastot perustuvat oletusarvon mukaan sopimuksen valuuttaan.

Toisin kuin kustannukset, myyntiarvot voidaan kirjata vain myyntivaluuttana.

## <a name="billing-method"></a>Laskutustapa

Projekteissa on tyypillisesti kahden tyyppisiä sopimusmalleja, kiinteät maksut ja kulutussopimusmallit. Nämä mallit on esitetty Project Operationsissa laskutusmenetelminä, joissa on kaksi mahdollista arvoa:

- Aika ja materiaali: Kulutukseen perustuva sopimusmalli, jossa kunkin kustannuksen tukena on vastaava myyntituotto. Kun arvioit tai kerrytät kustannuksia, myös vastaava arvioitu ja toteutunut myynti lisääntyy. Määritä ei-ylitettävät raja-arvot sopimusriveille, joilla on tämä laskutustapa, joka sulkee pois varsinaisen myyntituoton. Arvioituun myyntituottoon eivät vaikuta ei-ylittämättömät rajat.
- Kiinteä hinta: Tämä on kiinteän maksun sopimusmalli, joka ilmaisee, että myyntiarvot ovat aiheutuneista kustannuksista riippumattomia. Myyntiarvo on kiinteä eikä muutu, kun arvioit tai kerrytät lisää kustannuksia.

## <a name="project-price-lists"></a>Projektihinnastot

Projektihinnastoja käytetään ajan, kulujen ja muihin projektiin liittyvien komponenttien oletushintoihin, ei kustannushintoihin. Hinnastoja voi olla useita. Jokaisella hinnastolla on oma voimaantulopäivämäärä kullekin projektisopimukselle. Projekti hinnastojen päällekkäisiä voimassaolopäivämääriä ei tueta Project Operationsissa.

Kun projektisopimus luodaan voittamalla projektitarjous, projektihinnastot kopioidaan sopimuksen nimen ja päivämäärän mukaan. Näiden tietojen kopioiminen muodostaa tämän projektisopimuksen projektikomponenttien mukautetun hinnoittelun.

## <a name="product-price-lists"></a>Tuotehinnastot

Tuotehinnastoja käytetään sopimuksen tuotepohjaisten rivien oletushintoihin, ei kustannushintoihin. Sopimuksessa on vain yksi tuotehinnasto.

## <a name="transaction-classes"></a>Tapahtumaluokat

Project Operations tukee neljää tapahtumaluokan tyyppiä:

- Aika
- Kulu
- Materiaali
- Maksu

Kustannusten ja myynnin arvot voidaan arvioida ja ne voidaan kerryttää Aika-, Kulu- ja Materiaali-tapahtumaluokissa. Maksu on vain myyntituoton tapahtumaluokka.

## <a name="work-entities-and-billing-entities"></a>Työkohteet ja laskutuskohteet

Töitä edustavat kohteet ovat projekteja ja tehtäviä. Laskutusta edustavat kohteet ovat laskutusseikkoja ja sopimusrivejä. Voit sitoa erilaisia työkohteita laskutusasetuksiin sitomalla ne sopimusriveihin.

## <a name="multi-customer-deals"></a>Monen asiakkaan tarjoukset

Monen asiakkaan sopimuksissa on useampi kuin yksi asiakas, jota voi laskuttaa sopimuksesta. Tavallisia esimerkkejä ovat mm. seuraavat:

- OEM-yritykset ja niiden kumppanit: kumppanit ja jälleenmyyjät myyvät tuotetta joidenkin lisäarvopalvelujen kanssa, joihin liittyy yleensä erityisesti asiakkaan kanssa tehty sopimus. OEM tarjoaa mahdollisuuden rahoittaa osan projektista. 

- Julkisen sektorin projektit: Useat paikallishallinnon osastot suostuvat rahoittamaan hanketta, ja ne laskutetaan aiemmin sovitun jaon mukaisesti. Esimerkiksi koulupiiri ja kaupungin tai paikallishallinnon osasto sopivat rahoittavansa uima-altaan rakentamista.

## <a name="invoice-schedules"></a>Laskutusaikataulut

Laskusuunnitelmat liittyvät kuhunkin sopimusriviin, ja ne tarvitaan, jotta automaattinen laskutus toimisi. Laskutusaikatauluja luodaan tiettyjen alkamis- ja päättymispäivien sekä laskutustiheyden perusteella. Aikatauluja käytetään sopimusvaiheessa, kun automaattinen laskun luontiprosessi määritetään. Kun projektisopimus luodaan tarjouksesta, laskun aikataulu kopioidaan tarjouksen projektisopimukseen.

## <a name="changes-from-the-dynamics-365-sales-contract"></a>Muutokset Dynamics 365 Sales -sopimuksessa

Project Operationsin palvelusopimukset perustuvat Dynamics 365 Sales -sopimuksiin. Toiminnossa on kuitenkin joitakin tärkeitä poikkeuksia ja eroja, jotka kannattaa tietää:

- Project Operationsin palvelusopimuksilla on kaksi erityyppistä riviä, yksi projekteille ja toinen tuotteille.
- Project Operations -sopimuksilla on omat lomake- ja käyttöliittymäelementit, liiketoimintasäännöt, laajennusten liiketoimintalogiikka ja asiakaspuolen komentosarjat, jotka tekevät niistä erilaisia kuin Sales-sopimuksista.

Näistä syistä sinun ei tule käyttää myyntitilausta ja Project Operationsin sopimusta samassa merkityksessä.
