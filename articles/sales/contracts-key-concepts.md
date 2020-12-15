---
title: Projektin palvelusopimukset – keskeiset käsitteet
description: Tässä aiheessa on tietoja projektisopimusten avainkonsepteista Project Operationsissa.
author: rumant
manager: Annbe
ms.date: 10/07/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: fa00bd5b4a1179f38d5dfb63a47b39eec69c6ecf
ms.sourcegitcommit: 573be7e36604ace82b35e439cfa748aa7c587415
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/25/2020
ms.locfileid: "4642134"
---
# <a name="project-contracts---key-concepts"></a>Projektin palvelusopimukset – keskeiset käsitteet

_**Käytetään:** Project Operationsin resursseihin ja ei-varastoitaviin perustuvissa skenaarioissa_

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Tämä aihe sisältää tärkeimmät käsitteet, jotka on otettava huomioon, ennen kuin aloitat projektisopimusten käyttämisen Dynamics 365 Project Operationsissa:

## <a name="owning-company"></a>Omistava yritys

Omistava yritys on oikeushenkilö Dynamics 365 Financen Project Operationsin **Projektinhallinta ja kirjanpito** -moduulissa. Omistava yritys edustaa yritystä, joka ottaa huolehtii kustannuksista ja tuotosta, jotka kertyvät sopimuksesta.

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

Monen asiakkaan sopimuksissa on useampi kuin yksi asiakas, jota voi laskuttaa sopimuksesta. Yleisiä esimerkkejä tästä:

- OEM-yritykset ja niiden kumppanit: kumppanit ja jälleenmyyjät myyvät tuotetta joidenkin lisäarvopalvelujen kanssa, joihin liittyy yleensä erityisesti asiakkaan kanssa tehty sopimus. OEM tarjoaa mahdollisuuden rahoittaa osan projektista. 

- Julkisen sektorin projektit: Useat paikallishallinnon osastot suostuvat rahoittamaan hanketta, ja ne laskutetaan aiemmin sovitun jaon mukaisesti. Esimerkiksi koulupiiri ja kaupungin tai paikallishallinnon osasto sopivat rahoittavansa uima-altaan rakentamista.

## <a name="invoice-schedules"></a>Laskutusaikataulut

Laskusuunnitelmat liittyvät kuhunkin sopimusriviin, ja ne tarvitaan, jotta automaattinen laskutus toimisi. Laskutusaikatauluja luodaan tiettyjen alkamis- ja päättymispäivien sekä laskutustiheyden perusteella. Aikatauluja käytetään sopimusvaiheessa, kun automaattinen laskun luontiprosessi määritetään. Kun projektisopimus luodaan tarjouksesta, laskun aikataulu kopioidaan tarjouksen projektisopimukseen.

## <a name="changes-from-dynamics-365-sales-orders"></a>Dynamics 365 Sales -tilausten muutokset

Project Operationsin palvelusopimukset perustuvat Dynamics 365 Sales -tilauksiin. Toiminnoissa on kuitenkin tärkeitä poikkeamia ja eroja. Sopimuksilla on omat lomake- ja käyttöliittymäelementit, liiketoimintasäännöt, laajennusten liiketoimintalogiikka ja asiakaspuolen komentosarjat, jotka tekevät niistä erilaisia kuin tarjoukset. Näistä syistä älä käytä myyntitilausta ja Project Operationsin sopimusta samassa merkityksessä.
