---
title: Arviot
description: Tässä aiheessa on tietoja arvioista sovelluksessa Dynamics 365 Project Service Automation.
author: rumant
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 1/31/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: 8edb1689-2059-4776-8522-11cf0bb19b7a
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: a17ca814a71b05b0864d3da8f1cdbebe03e65f74
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/24/2020
ms.locfileid: "3751105"
---
# <a name="estimates"></a>Arviot

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Projektiperusteisessa tarjouksessa entiteettiä Tarjousrivin tiedot voidaan käyttää projektin toimittamisen edellyttämän työmäärän arviointiin. Tämä arvio voidaan ilmoittaa asiakkaalle.

Projektiperusteisilla tarjousriveillä ei tarvitse olla tarjousrivin tietoja. Vaihtoehtoisesti niillä voi olla useita tarjousrivin tietoja. Tarjousrivin tietoja käytetään ajan, kulujen tai maksujen arviointiin. PSA ei mahdollista materiaaliarvioita tarjousrivin tietojen perusteella. Näitä kutsutaan tapahtumaluokiksi. Myös arvioidut verosummat voidaan määrittää tapahtumaluokassa.

Tapahtumaluokkien lisäksi tarjousrivin tiedoilla on tapahtumatyyppi. PSA tukee tarjousrivin tiedoissa kahta tapahtumatyyppiä: **Kustannus** ja **Projektisopimus**.

## <a name="estimate-by-using-a-contract"></a>Arvio sopimuksen perusteella

Jos käytit PSA-tarjousta projektiperusteisen sopimuksen luonnin yhteydessä, kunkin tarjouksen tarjousrivin arvio kopioidaan projektisopimukseen. Projektisopimuksen rakenne vastaa projektitarjouksen rakennetta eli siinä on rivejä, rivien tietoja ja laskutusaikatauluja.

Arvioita voidaan tehdä suoraan projektisopimuksessa samalla tavalla kuin projektitarjouksessa. Projektitarjouksen osalta arvio tehdään sopimusrivien ja sopimisrivin tietojen perusteella. Sopimusrivin tietoja voidaan luoda myös alhaalta ylös -arvioinnin avulla luodun projektisuunnitelman perusteella.

Sopimusrivin tietoja voidaan käyttää ajan, kulujen tai maksujen arviointiin. Myös arvioidut verosummat voidaan määrittää sopimusrivin tiedossa.

PSA ei mahdollista materiaaliarvioita sopimusrivin tietojen perusteella.

Projektisopimuksessa tuetut prosessit ovat laskun luominen ja vahvistaminen. Laskun luonnissa luodaan luonnos projektiperusteisesta laskusta, joka sisältää kaikki laskuttamattomat myynnin todelliset arvot kulloiseenkin päivämäärään mennessä.

Vahvistuksen jälkeen sopimusta voidaan vain lukea ja sen tila muuttuu arvosta **Luonnos** arvoon **Vahvistettu**. Tätä toimintoa ei voi perua. Koska toiminto on pysyvä, parhaana käytäntönä on pitää sopimus **Luonnos**-tilassa.

Ainoa ero sopimusluonnosten ja vahvistettujen sopimusten välillä on niiden tila ja se, että sopimusluonnoksia voi muuttaa ja vahvistettuja sopimuksia ei voi muuttaa. Sekä sopimusluonnosten että vahvistettujen sopimusten perusteella voidaan luoda laskuja ja seurata todellisia arvoja.

PSA ei tue muutostilauksia sopimuksissa tai projekteissa.

## <a name="estimating-projects"></a>Projektien arviointi

Voit arvioida projektien aikaa ja kuluja. PSA ei mahdollista projektien materiaalien tai maksujen arviointia.

Aika-arvioita luodaan, kun luot tehtävän ja määrität tehtävän suorittamiseen tarvittavan yleisen resurssin määritteet. Aika-arviot luodaan ajoitettujen tehtävien perusteella. Aika-arvioita ei luoda, jos luot yleisiä ryhmän jäseniä aikataulun kontekstin ulkopuolella.

Kuluarviot syötetään **Arviot** -sivun ruudukkoon.

## <a name="understanding-estimation"></a>Tietoja arvioinnista

Seuraava taulukko sisältää opastuksen arviointivaiheen liiketoimintalogiikkaan.

| Skenaario                                                                                                                                                                                                                                                                                                                                          | Entiteettitietue                                                                                                                                                                                                       | Tapahtumatyyppi | Tapahtumaluokka | Lisätiedot                                                            |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------|-------------|-----------------------------------------------------------------------------------|
| Kun tarjouksen ajan myyntiarvo on arvioitava                                                                                                                                                                                                                                                                                    | Tarjousrivin tietojen tietue luodaan                                                                                                                                                                               | Projektisopimus | Time        | Tarjousrivin tietojen myyntipuolen Tapahtuman alkuperä -kenttä viittaa kustannuspuolen tarjousrivin tietoihin |
|                                                                                                                                                                                                                                                                                     | Järjestelmä luo toisen tarjousrivin tietojen tietueen vastaavia kustannusarvoja varten. Järjestelmä kopioi kaikki muut kuin rahamuotoiset kentät myynnin tarjousrivin tiedoista kustannuksen tarjousrivin tietoihin.                                                                                                                                                                               | Kustannus | Time        | Tarjousrivin tietojen myyntipuolen Tapahtuman alkuperä -kenttä viittaa kustannuspuolen tarjousrivin tietoihin |
| Kun sopimuksen ajan myyntiarvo on arvioitava                                                                                                                                                                                                                                                                                 | Projektisopimusrivin tietojen tietue luodaan                                                                                                                                                                    | Projektisopimus | Time        | Projektisopimusrivin tietojen myyntipuolen Tapahtuman alkuperä -kenttä viittaa kustannuspuolen projektisopimusrivin tietoihin      |
|                                                                                                                                                                                                                                                                                  | Järjestelmä luo toisen projektisopimusrivin tietojen tietueen vastaavia kustannusarvoja varten. Järjestelmä kopioi kaikki muut kuin rahamuotoiset kentät myynnin projektisopimusrivin tiedoista kustannuksen projektisopimusrivin tietoihin.                                                                                                                                                                    | Kustannus | Time        | Projektisopimusrivin tietojen myyntipuolen Tapahtuman alkuperä -kenttä viittaa kustannuspuolen projektisopimusrivin tietoihin      |
| Kun käyttäjä kuvaa resurssia projektitehtävässä                                                                                                                                                                                                                                                                                            | Arviorivitietue tehtävän myyntiarvoa varten luodaan, kun tehtävä luodaan kaikkine tarvittavine hinnoitteludimensioineen. Rooli ja organisaatioyksiköt ovat Project Servicen valmiit hinnoitteludimensiot | Projektisopimus | Time        |                                                                                   |
|     | Arviorivitietue tehtävän kustannusarvoa varten luodaan, kun tehtävä luodaan kaikkine tarvittavine hinnoitteludimensioineen. Järjestelmä kopioi kaikki muut kuin rahamuotoiset kentät myynnin arvioriviltä kustannuksen arvioriville. Rooli ja organisaatioyksikkö ovat PSA:n valmiit hinnoitteludimensiot sekä kustannus- että laskutushinnoille.                                                                                                                                                                                                                | Kustannus             | Time           |                                                                                   |



## <a name="customizing-the-quote-line-detail-and-contract-line-detail-entities"></a>Entiteettien Tarjousrivin tiedot ja Sopimusrivin tiedot mukauttaminen

Jos olet lisännyt muokatun kentän tarjousrivin tietoihin ja haluat järjestelmän syöttävän kyseisen kentän arvon sen luoman vastaavan kustannusrivin oletusarvoksi, voit käyttää rekisteröintityökalujen laajennuksia PreOperationContractLineDetailUpdate ja PreOperationQuoteLineDetailUpdate. Nämä laajennukset on rekisteröitävä uudelleen, kun tarjousrivin tietoja tai sopimusrivin tietoja on muutettu. Suorita prosessi loppuun seuraavasti.

1. Avaa PluginRegistrationTool ja muodosta yhteys online-esiintymään.
2. Valitse **Hae** ja etsi päivitettävä laajennus.

    ![Haun puuvalintaikkuna](media/basic-guide-19.png)

3. Valitse laajennus ja valitse sitten pääsivulla **Valitse**.
4. Valitse päivitettävän laajennuksen vaihe, napsauta hiiren kakkospainiketta ja valitse sitten **Päivitä**.

    ![Vaiheen valitseminen laajennuksessa](media/basic-guide-20.png)

5. Valitse kolme pistettä sisältävä painike **(...)** valintaikkunan **Päivitä aiemmin luotu vaihe** kentästä **Suodatusmääritteet**:
 
    ![Päivitä aiemmin luotu vaihe -valintaikkuna](media/basic-guide-21.png)

6. Valitse **Valitse määritteet** -valintaikkunassa mukautettujen määritteiden valintaruudut.

    ![Valitse määritteet -valintaikkuna](media/basic-guide-22.png)

7. Sulje valintaikkuna valitsemalla **OK** ja valitse sitten **Päivitä vaihe**.
 
    ![Päivitä vaihe -painike](media/basic-guide-23.png)

8. Toista vaiheet 1–7 toisen laajennuksen osalta.
9. Sulje PluginRegistrationTool.