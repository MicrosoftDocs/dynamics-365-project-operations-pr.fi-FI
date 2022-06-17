---
title: Arvioiden luominen tarjousrivillä
description: Tässä artikkelissa on tietoja siitä, miten projektin tarjousriville luodaan arvio.
author: rumant
ms.date: 09/18/2020
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
ms.openlocfilehash: 9f606ff2c33c46063f7025e8bc58e704d472061b
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8912558"
---
# <a name="create-estimates-on-a-quote-line"></a>Arvioiden luominen tarjousrivillä

_**Koskee:** Project Operationsin resurssiin / muuhun kuin resurssiin perustuvia skenaarioita, Lite-käyttöönotto-kaupasta proformalaskutukseen_

Projektiperusteisessa tarjouksessa entiteettiä Tarjousrivin tiedot voidaan käyttää projektin toimittamisen edellyttämän työmäärän arviointiin. Tämä arvio voidaan ilmoittaa asiakkaalle.

Projektiperusteisilla tarjousriveillä ei tarvitse olla tarjousrivin tietoja. Vaihtoehtoisesti niillä voi olla useita tarjousrivin tietoja. Tarjousrivin tietoja käytetään ajan, kulujen tai maksujen arviointiin. Dynamics 365 Project Operations ei mahdollista materiaaliarvioita tarjousrivin tietojen perusteella. Näitä kutsutaan tapahtumaluokiksi. Myös arvioidut verosummat voidaan määrittää tapahtumaluokassa.

Tapahtumaluokkien lisäksi tarjousrivin tiedoilla on tapahtumatyyppi. Tarjousrivin tiedoissa on kaksi tapahtumatyyppiä: **Kustannus** ja **Projektisopimus**.

## <a name="estimate-by-using-a-contract"></a>Arvio sopimuksen perusteella

Jos käytit Project Operations -tarjousta projektiperusteisen sopimuksen luonnin yhteydessä, kunkin tarjouksen tarjousrivin arvio kopioidaan projektisopimukseen. Projektisopimuksen rakenne vastaa projektitarjouksen rakennetta eli siinä on rivejä, rivien tietoja ja laskutusaikatauluja.

Arvioita voidaan tehdä suoraan projektisopimuksessa samalla tavalla kuin projektitarjouksessa. Projektitarjouksen osalta arvio tehdään sopimusrivien ja sopimisrivin tietojen perusteella. Sopimusrivin tietoja voidaan luoda myös alhaalta ylös -arvioinnin avulla luodun projektisuunnitelman perusteella.

Sopimusrivin tietoja voidaan käyttää ajan, kulujen tai maksujen arviointiin. Myös arvioidut verosummat voidaan määrittää sopimusrivin tiedossa.

Materiaaliarviot eivät ole sallittuja sopimusrivin tietojen perusteella.

Projektisopimuksessa tuetut prosessit ovat laskun luominen ja vahvistaminen. Laskun luonnissa luodaan luonnos projektiperusteisesta laskusta, joka sisältää kaikki laskuttamattomat myynnin todelliset arvot kulloiseenkin päivämäärään mennessä.

Vahvistuksen jälkeen sopimusta voidaan vain lukea ja sen tila muuttuu arvosta **Luonnos** arvoon **Vahvistettu**. Tätä toimintoa ei voi perua. Koska toiminto on pysyvä, parhaana käytäntönä on pitää sopimus **Luonnos**-tilassa.

Ainoa ero sopimusluonnosten ja vahvistettujen sopimusten välillä on niiden tila ja se, että sopimusluonnoksia voi muuttaa ja vahvistettuja sopimuksia ei voi muuttaa. Sekä sopimusluonnosten että vahvistettujen sopimusten perusteella voidaan luoda laskuja ja seurata todellisia arvoja.

Muutostilauksia ei tueta sopimuksissa tai projekteissa.

## <a name="estimating-projects"></a>Projektien arviointi

Voit arvioida projektien aikaa ja kuluja, mutta et materiaaleja tai maksuja.

Aika-arvioita luodaan, kun luot tehtävän ja määrität tehtävän suorittamiseen tarvittavan yleisen resurssin määritteet. Aika-arviot luodaan ajoitettujen tehtävien perusteella. Aika-arvioita ei luoda, jos luot yleisiä ryhmän jäseniä aikataulun kontekstin ulkopuolella.

Kuluarviot syötetään **Arviot** -sivun ruudukkoon.

## <a name="understand-estimation"></a>Tietoja arviosta

Seuraava taulukko sisältää opastuksen arviointivaiheen liiketoimintalogiikkaan.

| Skenaario                                                                                                                                                                                                                                                                                                                                          | Entiteettitietue                                                                                                                                                                                                       | Tapahtumatyyppi | Tapahtumaluokka | Lisätiedot                                                            |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------|-------------|-----------------------------------------------------------------------------------|
| Kun tarjouksen ajan myyntiarvo on arvioitava                                                                                                                                                                                                                                                                                    | Tarjousrivin tietojen tietue luodaan                                                                                                                                                                               | Projektisopimus | Time        | Tarjousrivin tietojen myyntipuolen Tapahtuman alkuperä -kenttä viittaa kustannuspuolen tarjousrivin tietoihin |
|                                                                                                                                                                                                                                                                                     | Järjestelmä luo toisen tarjousrivin tietojen tietueen vastaavia kustannusarvoja varten. Järjestelmä kopioi kaikki muut kuin rahamuotoiset kentät myynnin tarjousrivin tiedoista kustannuksen tarjousrivin tietoihin.                                                                                                                                                                               | Kustannus | Time        | Tarjousrivin tietojen myyntipuolen Tapahtuman alkuperä -kenttä viittaa kustannuspuolen tarjousrivin tietoihin |
| Kun sopimuksen ajan myyntiarvo on arvioitava                                                                                                                                                                                                                                                                                 | Projektisopimusrivin tietojen tietue luodaan                                                                                                                                                                    | Projektisopimus | Time        | Projektisopimusrivin tietojen myyntipuolen Tapahtuman alkuperä -kenttä viittaa kustannuspuolen projektisopimusrivin tietoihin      |
|                                                                                                                                                                                                                                                                                  | Järjestelmä luo toisen projektisopimusrivin tietojen tietueen vastaavia kustannusarvoja varten. Järjestelmä kopioi kaikki muut kuin rahamuotoiset kentät myynnin projektisopimusrivin tiedoista kustannuksen projektisopimusrivin tietoihin.                                                                                                                                                                    | Kustannus | Time        | Projektisopimusrivin tietojen myyntipuolen Tapahtuman alkuperä -kenttä viittaa kustannuspuolen projektisopimusrivin tietoihin      |
| Kun käyttäjä kuvaa resurssia projektitehtävässä                                                                                                                                                                                                                                                                                            | Arviorivitietue tehtävän myyntiarvoa varten luodaan, kun tehtävä luodaan kaikkine tarvittavine hinnoitteludimensioineen. Rooli ja organisaatioyksiköt ovat hinnoitteludimensiot | Projektin palvelusopimus | Aika        |                                                                                   |
|     | Arviorivitietue tehtävän kustannusarvoa varten luodaan, kun tehtävä luodaan kaikkine tarvittavine hinnoitteludimensioineen. Järjestelmä kopioi kaikki muut kuin rahamuotoiset kentät myynnin arvioriviltä kustannuksen arvioriville. Rooli ja organisaatioyksikkö ovat hinnoitteludimensiot sekä kustannus- että laskutushinnoille.                                                                                                                                                                                                                | Kustannus             | Aika           |                                                                                   |



## <a name="customize-the-quote-line-detail-and-contract-line-detail-entities"></a>Tarjousrivin tietojen ja sopimusrivin tietojen entiteettien mukauttaminen

Jos olet lisännyt muokatun kentän tarjousrivin tietoihin ja haluat järjestelmän syöttävän kyseisen kentän arvon sen luoman vastaavan kustannusrivin oletusarvoksi, voit käyttää rekisteröintityökalujen laajennuksia PreOperationContractLineDetailUpdate ja PreOperationQuoteLineDetailUpdate. Nämä laajennukset on rekisteröitävä uudelleen, kun tarjousrivin tietoja tai sopimusrivin tietoja on muutettu. Suorita prosessi loppuun seuraavasti.

1. Avaa PluginRegistrationTool ja muodosta yhteys online-esiintymään.
2. Valitse **Hae** ja etsi päivitettävä laajennus.
3. Valitse laajennus ja valitse sitten pääsivulla **Valitse**.
4. Valitse päivitettävän laajennuksen vaihe, napsauta hiiren kakkospainiketta ja valitse sitten **Päivitä**.
5. Valitse kolme pistettä sisältävä painike **(...)** valintaikkunan **Päivitä aiemmin luotu vaihe** kentästä **Suodatusmääritteet**:
6. Valitse **Valitse määritteet** -valintaikkunassa mukautettujen määritteiden valintaruudut.
7. Sulje valintaikkuna valitsemalla **OK** ja valitse sitten **Päivitä vaihe**.
8. Toista vaiheet 1–7 toisen laajennuksen osalta.
9. Sulje PluginRegistrationTool.


[!INCLUDE[footer-include](../includes/footer-banner.md)]