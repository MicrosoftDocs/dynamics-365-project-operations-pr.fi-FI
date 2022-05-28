---
title: Taloudellista arviointia koskevat käsitteet
description: Tässä aiheessa on tietoja projektien taloudellisista arvioista Project Operationsissa.
author: rumant
ms.date: 03/22/2021
ms.topic: overview
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 338d2924f0e2a4a7fb943686eaad421a892dce70
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/14/2022
ms.locfileid: "8597748"
---
# <a name="financial-estimation-concepts"></a>Taloudellista arviointia koskevat käsitteet

_**Koskee:** Project Operationsin resurssiin / muuhun kuin resurssiin perustuvia skenaarioita, Lite-käyttöönotto-kaupasta proformalaskutukseen_

Dynamics 365 Project Operationsissa projektit voidaan arvioida kahdessa vaiheessa: 
1. Myyntiä edeltävässä vaiheessa ennen sopimuksen voittamista. 
2. Sen jälkeen, kun projektisopimus on luotu, suoritusvaiheessa. 

Projektipohjaiselle työlle voi luoda talousarvion seuraavilla kolmella sivulla:
- **Tarjousrivi**-sivulla käyttäen tarjousrivin tietoja.  
- **Projektisopimus**-sivulla käyttäen projektisopimuksen tietoja. 
- **Projekti**-sivulla käyttäen **Tehtävät** tai **Kuluarviot**-välilehtisivuja.

## <a name="use-a-project-quote-to-create-an-estimate"></a>Arvion luominen projektitarjouksen avulla
Projektiperusteisessa tarjouksessa entiteettiä **Tarjousrivin tiedot** voidaan käyttää projektin toimittamisen edellyttämän työmäärän arviointiin. Tämä arvio voidaan ilmoittaa asiakkaalle.

Projektiperusteisilla tarjousriveillä voi olla paljon tarjousrivin tietoja tai ei yhtään. Tarjousrivin tietoja käytetään ajan, kulujen tai maksujen arviointiin. Microsoft Dynamics 365 Project Operations ei mahdollista materiaaliarvioita tarjousrivin tietojen perusteella. Näitä kutsutaan tapahtumaluokiksi. Myös arvioidut verosummat voidaan määrittää tapahtumaluokassa.

Tapahtumaluokkien lisäksi tarjousrivin tiedoilla on tapahtumatyyppi. Tarjousrivin tiedoissa on kaksi tapahtumatyyppiä: **Kustannus** ja **Projektisopimus**.

## <a name="use-a-project-contract-to-create-an-estimate"></a>Arvion luominen projektisopimuksen avulla

Jos käytit tarjousta projektiperusteisen sopimuksen luonnin yhteydessä, kunkin tarjouksen tarjousrivin arvio kopioidaan projektisopimukseen. Projektisopimuksen rakenne vastaa projektitarjouksen rakennetta eli siinä on rivejä, rivien tietoja ja laskutusaikatauluja.

Arvioita voidaan tehdä suoraan projektisopimuksessa samalla tavalla kuin projektitarjouksessa. Projektitarjouksen osalta arvio tehdään sopimusrivien ja sopimisrivin tietojen perusteella. Sopimusrivin tietoja voidaan luoda myös alhaalta ylös -arvioinnin avulla luodun projektisuunnitelman perusteella.

Sopimusrivin tietoja voidaan käyttää ajan, kulujen tai maksujen arviointiin. Myös arvioidut verosummat voidaan määrittää sopimusrivin tiedossa.

Materiaaliarviot eivät ole sallittuja sopimusrivin tietojen perusteella.

## <a name="use-a-project-to-create-an-estimate"></a>Arvion luominen projektin avulla 

Voit arvioida projektien aikaa ja kuluja. Project Operations ei tue projektien materiaalien tai maksujen arvioita.

Aika-arvioita luodaan, kun luot tehtävän ja määrität tehtävän suorittamiseen tarvittavan yleisen resurssin määritteet. Aika-arviot luodaan ajoitettujen tehtävien perusteella. Aika-arvioita ei luoda, jos luot yleisiä ryhmän jäseniä aikataulun kontekstin ulkopuolella.

Kuluarviot syötetään **Kuluarviot**-sivun ruudukkoon.

Projektin arvion luomista pidetään parhaina käytäntönä, koska kullekin projektisuunnitelman tehtävälle voidaan luoda yksityiskohtaisia alhaalta ylöspäin -arvioita työvoimaa tai aikaa ja kuluja varten. Tämän yksityiskohtaisen arvion avulla voidaan sitten luoda arvioita kullekin tarjousriville ja luoda asiakkaalle entistä luotettavampi tarjous. Kun tuot tai luot tarjousrivillä yksityiskohtaisen arvion projektisuunnitelman avulla, Project Operations tuo näiden arvioiden myyntiarvot ja kustannusarvot. Tuonnin jälkeen voit tarkastella projektin tarjouksessa kannattavuutta, katteita ja soveltuvuusmittareita.

## <a name="understanding-estimates"></a>Tietoja arvioista

Seuraava taulukko sisältää opastuksen arviovaiheen liiketoimintalogiikkaan.

| Skenaario                                                                                                                                                                                                                                                                                                                                          | Entiteettitietue                                                                                                                                                                                                       | Tapahtumatyyppi | Tapahtumaluokka | Lisätiedot                                                            |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------|-------------|-----------------------------------------------------------------------------------|
| Kun tarjouksen ajan myyntiarvo on arvioitava                                                                                                                                                                                                                                                                                    | Tarjousrivin tietojen tietue luodaan                                                                                                                                                                               | Projektisopimus | Time        | Tarjousrivin tietojen myyntipuolen Tapahtuman alkuperä -kenttä viittaa kustannuspuolen tarjousrivin tietoihin |
|                                                                                                                                                                                                                                                                                     | Järjestelmä luo toisen tarjousrivin tietojen tietueen vastaavia kustannusarvoja varten. Järjestelmä kopioi kaikki muut kuin rahamuotoiset kentät myynnin tarjousrivin tiedoista kustannuksen tarjousrivin tietoihin.                                                                                                                                                                               | Kustannus | Time        | Tarjousrivin tietojen myyntipuolen Tapahtuman alkuperä -kenttä viittaa kustannuspuolen tarjousrivin tietoihin |
| Kun sopimuksen ajan myyntiarvo on arvioitava                                                                                                                                                                                                                                                                                 | Projektisopimusrivin tietojen tietue luodaan                                                                                                                                                                    | Projektisopimus | Time        | Projektisopimusrivin tietojen myyntipuolen Tapahtuman alkuperä -kenttä viittaa kustannuspuolen projektisopimusrivin tietoihin      |
|                                                                                                                                                                                                                                                                                  | Järjestelmä luo toisen projektisopimusrivin tietojen tietueen vastaavia kustannusarvoja varten. Järjestelmä kopioi kaikki muut kuin rahamuotoiset kentät myynnin projektisopimusrivin tiedoista kustannuksen projektisopimusrivin tietoihin.                                                                                                                                                                    | Kustannus | Time        | Projektisopimusrivin tietojen myyntipuolen Tapahtuman alkuperä -kenttä viittaa kustannuspuolen projektisopimusrivin tietoihin      |
| Kun käyttäjä kuvaa resurssia projektitehtävässä                                                                                                                                                                                                                                                                                            | Arviorivitietue tehtävän myyntiarvoa varten luodaan, kun tehtävä luodaan kaikkine tarvittavine hinnoitteludimensioineen. Rooli ja organisaatioyksiköt ovat hinnoitteludimensiot | Projektin palvelusopimus | Aika        |                                                                                   |
|     | Arviorivitietue tehtävän kustannusarvoa varten luodaan, kun tehtävä luodaan kaikkine tarvittavine hinnoitteludimensioineen. Järjestelmä kopioi kaikki muut kuin rahamuotoiset kentät myynnin arvioriviltä kustannuksen arvioriville. Rooli ja organisaatioyksikkö ovat hinnoitteludimensiot sekä kustannus- että laskutushinnoille.                                                                                                                                                                                                                | Kustannus             | Aika           |                                                                                   |



## <a name="customize-the-quote-line-detail-and-contract-line-detail-entities"></a>Tarjousrivin tietojen ja sopimusrivin tietojen entiteettien mukauttaminen

Jos olet lisännyt muokatun kentän tarjousrivin tietoihin ja haluat järjestelmän syöttävän kyseisen kentän arvon sen luoman vastaavan kustannusrivin oletusarvoksi, voit käyttää rekisteröintityökalujen laajennuksia **PreOperationContractLineDetailUpdate** ja **PreOperationQuoteLineDetailUpdate**. Nämä laajennukset on rekisteröitävä uudelleen, kun tarjousrivin tietoja tai sopimusrivin tietoja on muutettu. Suorita prosessi loppuun seuraavasti.

1. Avaa PluginRegistrationTool ja muodosta yhteys online-esiintymään.
2. Valitse **Hae** ja etsi päivitettävä laajennus.
3. Valitse laajennus ja valitse sitten pääsivulla **Valitse**.
4. Valitse päivitettävän laajennuksen vaihe, napsauta hiiren kakkospainiketta ja valitse sitten **Päivitä**.
5. Valitse kolme pistettä sisältävä painike **(...)** valintaikkunan **Päivitä aiemmin luotu vaihe** kentästä **Suodatusmääritteet**:
6. Valitse **Valitse määritteet** -valintaikkunassa mukautettujen määritteiden valintaruudut.
7. Sulje valintaikkuna valitsemalla **OK** ja valitse sitten **Päivitä vaihe**.
8. Toista vaiheet 1–7 toisen laajennuksen osalta.
9. Sulje **PluginRegistrationTool**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
