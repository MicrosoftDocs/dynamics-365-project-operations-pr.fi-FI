---
title: Työn kustannushintojen määrittäminen – lite
description: Tämä aihe sisältää tietoja siitä, miten työvoimakustannukset määritetään Project Operationsissa.
author: rumant
ms.date: 10/12/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 01e3b41ca5c8fcc9146186873e0f44daad020c6c
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/14/2022
ms.locfileid: "8575668"
---
# <a name="set-up-labor-cost-rates---lite"></a>Työn kustannushintojen määrittäminen – lite

_**Käytetään:** Lite-käyttöönotto – kauppa proformalaskutukseen_

Jokaisessa hinnastossa on joukko työvoimaprosentteja (roolihinnat), jotka vastaavat hinnaston sisältöä ja päivämäärän vaikuttavuutta.

1. Luo hinnasto ja valitse **Roolin hinta** -välilehden aliruudukossa **Uusi rooli**.
2. Valitse **pikaluontisivulla** roolit ja organisaatioyksiköt.
3. Kirjoita tarvittavat tiedot kenttiin.

Seuraavassa taulukossa on joitakin kenttiä, jotka ovat tärkeitä luotaessa työvoimahintoja kustannushinnastoon.

| Field | Sijainti | Kuvaus | Loppupään vaikutus |
| --- | --- | --- | --- |
| Rooli | **Yleiset**-välilehti ja **pikaluonti**-sivut | Valitse rooli, jota kustannushinta koskee. | Saapuva arvio tai todellinen rooli sovitetaan tämän rivin kanssa roolin oletuskuluun. |
| Resursointiyksikkö | **Yleiset**-välilehti ja **pikaluonti**-sivut | Valitse sen yrityksen organisaatioyksikkö tai osasto, jossa roolia käytetään. Kyseessä on esimerkiksi Fabrikam Intian Robotics Divisionin kehittäjä tai Fabrikam USA:n ohjelmisto-osaston kehittäjä. | Saapuvan arvion tai todellisen resurssien tarjoajayksikkö vertaa tätä riviä oletusarvoisesti roolin kuluprosenttiin. |
| Hinta | **Yleiset**-välilehti ja **pikaluonti**-sivut | Määritä kustannukset roolille, resursseja tuottavalle yritykselle ja resurssiyksikköyhdistelmälle. Esimerkiksi Fabrikam Intian kehittäjä maksaa 1 000 INR tai Fabrikam USA:n kehittäjä maksaa 150 UDS. | Hinta on kustannusnopeus, joka oletusarvoisesti laskee saapuvan estimaatin tai todellisen rivin **Aika**-tapahtumaluokan yksikkökustannukset. |
| Valuutta | **Yleiset**-välilehti ja **pikaluonti**-sivut | Oletusarvon mukaan tämä valuutta on kuluhinnaston otsikossa oleva valuutta, mutta se voidaan ohittaa. Esimerkiksi Fabrikam Intian sovelluskehittäjä maksaa 1 000 INR. Fabrikam USA:n kehittäjä maksaa 150 USD. | Tämä valuutta on oletuksena saapuvan todellisen kustannusrivin yksikköhinnassa **aika**-tapahtumaluokalle. Projektiarvion valuutta-arvo muunnetaan projektivaluutaksi ja näytetään arvion aika-vaiheittaisessa näkymässä. |
| Yksikön aikataulutus | **Yleiset**-välilehti ja **pikaluonti**-sivut | Yksikön aikataulun oletusarvo on aika, eikä sitä voi muuttaa roolihintaentiteetissä, koska sitä käytetään ilmaisemaan hinnat yksiköiden mukaan. | Tämä ei vaikuta loppupään toimintaan. |
| Yksikkö | **Yleiset**-välilehti ja **pikaluonti**-sivut | Oletusarvoisesti arvo tulee **Aikayksikkö**-kentästä kustannushintaluettelon otsikossa. Arvo voidaan ohittaa. Esimerkiksi Fabrikam Intian sovelluskehittäjällä on hinta, joka on 1000 INR per **Intian päivä**. Fabrikam USA:n kehittäjä maksaa 150 USD per **US:n päivä**. | Järjestelmä käyttää yksikkö- ja muunnosjärjestelmää perusyksiköissä yksikkökustannusten laskemiseksi laskemaan oletushintayksikköä kohti tulevassa arviossa tai todellisessa rivissä. Esimerkiksi arvio on 10 **Intian päivän** verran työtä kehittäjälle Intiasta, ja **Intian päiväyksikkö** määritetään 10 tunniksi. Kun arviorivi lasketaan, sovellus laskee yksikkökustannuksen arviosta seuraavasti: 1000 INR/10 tuntia = 100 INR tunnissa, joka muunnetaan USD:ksi ja näytetään yksikkökustannuksena **Projektiarviot**-sivulla. |

## <a name="transfer-pricing-and-costs-for-resources-outside-of-your-division-or-legal-entity"></a>Siirrä hinnoittelu ja kustannukset resursseille, jotka eivät kuulu jaostoosi tai oikeushenkilöösi

Projektipohjaisissa yrityksissä on tavallista käyttää projektiin eri oikeushenkilöiden tai osastojen työntekijöitä. Projektin voi toteuttaa yksi oikeushenkilö, mutta projektissa työskentelevät työntekijät tai konsultit voivat tulla samalta oikeushenkilöltä tai toiselta, tai molemmat voivat olla yhdistettyjä. Dynamics 365 Project Operationsissa projektin toimituksen omistava yritys on **Omistava yritys** ja toimituksen omistava yritys on **Sopimusyksikkö**. Muita resursseja toimittavien oikeushenkilöiden nimenä on **resursointiyritys**, ja resursseja tuottavia osastoja kutsutaan **resursointiyksiköiksi**. Useimmissa maissa yritysten on varmistettava, että resurssipäällikkö tai -osasto veloittaa omistettavaa yritystä ja hankintayksikköä resurssien käytöstä.

Esimerkiksi Fabrikam Corporationin on varmistettava, että Fabrikam Intia-Robotics on neuvotellut kustannushintakortin Fabrikam US-Roboticsin tai Fabrikam UK-Roboticsin kanssa.

Fabrikam Intia-Roboticin kehittäjä veloittaa 100 $ lainattaessa Fabrikam US-Roboticsille ja 150 $, kun lainataan Fabrikam U-Roboticsille.

### <a name="set-up-costs-for-outside-resources"></a>Ulkoisten resurssien kustannusten määrittäminen

1. Luo kustannushinnasto nimeltä *Fabrikam US-Robotics-kustannushinnat* ja määritä voimassaoloalue.
2. Määritä kustannushinnastossa hinnat käyttämällä seuraavan taulukon tietoja. 

| Rooli | Resursoiva yritys | Resursointiyksikkö | Kustannushinta |
| --- | --- | --- | --- |
| Developer | Fabrikam Intia | Fabrikam Intia-Robotics | 100 $ |
| Developer | Fabrikam Filippiinit | Fabrikam Filippiinit-Robotics | 90 $ |
| Developer | Fabrikam US | Fabrikam US-Robotics | 150 $ |

3. Liitä tämä kustannushintaluettelo Fabrikam US-Robotics-organisaatioyksikköön.

### <a name="set-up-transfer-pricing-for-a-resource-in-the-appropriate-currency"></a>Resurssin siirtohinnoittelun määrittäminen sopivaan valuuttaan 

Project Operationsissa resurssin hinnoittelu voidaan määrittää missä tahansa valuutassa. Valuutan oletusarvona on, mitä hinnaston otsikossa on, mutta sitä voi muuttaa.

Tietojensiirtohinnan määrittämisen esimerkin avulla tiedot voidaan muuttaa:

Fabrikam Corporationin on varmistettava, että Fabrikam Intia-Robotics on neuvotellut kustannushinnan Fabrikam US-Roboticsin tai Fabrikam UK-Roboticsin kanssa.

Fabrikam Intia-Roboticin kehittäjä maksaa 5 000 INR lainattaessa Fabrikam US-Roboticsille ja 5 500 INR, kun lainataan Fabrikam UK-Roboticsille.

Fabrikam US-Roboticsin kustannushinnastossa kustannushinnat voidaan ilmaista seuraavasti:

| Rooli | Resursoiva yritys | Kustannus |
| --- | --- | --- |
| Developer | Fabrikam Intia | 5 000 INR |
| Developer | Fabrikam US | 115 USD |

Fabrikam UK-Roboticsin kustannushinnastossa kustannushinnat voidaan ilmaista seuraavasti:

| Rooli | Resursoiva yritys | Kustannus |
| --- | --- | --- |
| Developer | Fabrikam Intia | 5 500 INR |
| Developer | Fabrikam UK | 115 GBP |

Kustannushinnastossa voi olla työvoimahinnat useissa valuutoissa. Kun projektin kustannusarvio luodaan, Project Operations muuntaa nämä kustannusprosentit projektivaluuttaan ja näyttää ne käyttäjälle. Kun ajankohta on hyväksytty ja todellinen kustannus luodaan, todellinen kustannushinta on hinnoiteltu vastaavan roolihintarivin valuutassa kustannushinnastossa. Yksittäisen projektin kustannusten toteutuneet kustannukset voidaan kirjata useina valuuttoina. Kun kuitenkin kootaan tai tiivistetään todelliset työvoimakustannukset projektitasolla, Project Operations muuntaa kaikki työvoimakustannussummat projektin valuutaksi, jonka käyttäjä voi tarkastella.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]