---
title: Ominaisuuksien muutokset Project Service Automationista Project Operationsiin
description: Tässä artikkelissa on yleiskatsaus ominaisuuksien muutoksista Microsoft Dynamics 365 Project Service Automationista Dynamics 365 Project Operationsiin.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 02/03/2022
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.reviewer: johnmichalak
ms.openlocfilehash: 9869b3ad0fb6429484a26f367e06a0996f110ed8
ms.sourcegitcommit: a2d720ac6d7ddb20a0967fe87992a376b2478208
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/04/2022
ms.locfileid: "9621215"
---
# <a name="feature-changes-for-project-service-automation-to-project-operations"></a>Ominaisuuksien muutokset Project Service Automationista Project Operationsiin

Kun projekti on päivitetty Microsoft Dynamics 365 Project Service Automation 3.X:stä Dynamics 365 Project Operations Liteen, projektitehtävien muokkaaminen tehtäväruudukon työrakenteessa (WBS) ei ole mahdollista. Asiakkaat voivat tarkastella tuoterakenteita seurantaruudukossa, johon on lisätty uusia kenttiä antamaan kaikki tehtävään liittyvät tiedot. Jos projekteissa on muokattava tuoterakennetta, soveltuvat projektit voidaan muuntaa uudeksi Project for the web -aikataulutuskokemukseksi.

## <a name="project-conversion-process"></a>Projektin muuntoprosessi

Projekti muunnetaan seuraavasti.

1. Avaa projektin pääsivu ja valitse **Muunna** toimintoruudussa.
1. Aloita projektin muunto valitsemalla vahvistussanomaruudussa **OK**. Tuloksena on seuraavat toiminnot:

    1. Projektin pääsivulla olevassa sanomapalkissa on ilmoitus Projektiaikataulua muunnetaan. Projektiin ei voi tehdä muutoksia, ennen kuin muunto on valmis.
    1. Uudelleenohjaus tehdään projektiluetteloon.

    Kun projektin muunto on valmis, seuraava tapahtuu:

    1. Määritetty projektipäällikkö vastaanottaa ilmoituksen sovelluksen oikealla puolella.
    1. Sanomapalkki, joka ilmaisee muunnon olevan kesken, on poistettu.
    1. **Aikataulu**-välilehti näyttää uuden aikataulutuskokemuksen Project for the webiä käytettäessä. Kuka tahansa käyttäjä, jolla on soveltuvat käyttöoikeudet ja käyttöoikeusroolit, voi muokata tuoterakennetta.
    1. **Ajoitusmoduuli**-kenttä on päivitetty **Project for the web** -ominaisuudeksi.
    1. **Muunna**-painike poistetaan toimintoruudusta.

> [!IMPORTANT]
> Projektien joukkomuuntoa ei sallita. Yrityksiä päivittää suurta määrää projekteja samanaikaisesti rajoitetaan. Tämä rajoitus auttaa varmistamaan, että suorituskyky on hyvä kaikilla asiakkailla.

## <a name="manual-tasks-vs-automatic-tasks"></a>Manuaaliset ja automaattisten tehtävien vertailu

Kun ympäristö päivitetään Project Service Automationista Project Operationsiin, kaikki tuoterakenteen tehtävät katsotaan automaattisesti aikataulutetuiksi. Project for the web ei sisällä manuaalisesti aikataulutettuja tehtäviä. Projekteille voidaan kuitenkin määrittää ensisijainen aikataulutustoimintoa käyttämällä [aikataulutustilaa](/project-management/scheduling-modes.md) uusia projekteja luotaessa.

## <a name="restricted-operations-for-pre-conversion-projects"></a>Valmiiksi muunnettujen projektien rajoitetut toiminnot

Tässä osassa käsitellään toiminnallisia eroja, joita on odotettavissa, kun projekteja ei ole muunnettu.

### <a name="copy-project"></a>Projektin kopiointi

**Kopioi**-toimintoa tuetaan vain muunnetuissa projekteissa. Päivitettyjä projekteja ei voi kopioida ennen muuntoa.

### <a name="move-project"></a>Projektin siirtäminen

Projektin alkamispäivän muutos ei siirry suhteellisesti tehtävien aloittamista, jos projektia ei ole muunnettu.

## <a name="frequently-asked-questions"></a>Usein kysyttyjä kysymyksiä

### <a name="what-are-the-differences-between-converted-projects-and-new-projects-that-are-created-after-the-upgrade-has-been-completed"></a>Mitä eroja on muunnettujen projektien ja päivityksen valmistumisen jälkeen luotujen uusien projektin välillä?

Ympäristön päivityksen jälkeen muunnetuissa projekteissa on merkintä, joka opastaa aikataulutuksen noudattamaan vain projektin kalenteria. Tämä toiminta vastaa Project Service Automationin toimintaa. Merkintää ei kuitenkaan määritä uusille projekteille, jotka on luotu päivityksen jälkeen. Niinpä aikataulu noudattaa resurssien työaikaa tehtävää määritettäessä.

### <a name="what-should-i-do-if-my-project-fails-to-be-converted"></a>Miten toimitaan, jos projektin muunnon epäonnistuu?

Jos projektin muunnos epäonnistuu, ensimmäiseksi on tarkistettava virhelokit ja määritettävä työrakenteeseen liittyvät yleiset ongelmat. Jos lokeista ei ilmene tiettyä virhettä, jota ei voi käsitellä, asiakaspalvelua voi pyytää tarkastelemaan tapausta lisää.

### <a name="how-are-business-closures-handled-in-project-for-the-web"></a>Miten palvelukatkoja käsitellään Project for the webissä?

Project for the web ei noudata yrityksen organisaatiotasolla määrittämiä palvelukatkoja. Se noudattaa kuitenkin muita päivätyyppejä, jotka on määritetty annetussa työtuntimallissa.

### <a name="what-are-the-limitations-of-project-for-the-web"></a>Mitkä ovat Project for the webin rajoitukset?

Lisätietoja on kohdassa [Työrakenteen luominen: projektin rajoitukset](/project-management/create-wbs#project-limitations.md).

### <a name="can-i-expect-changes-to-my-cost-and-sales-estimates"></a>Tuleeko kustannus- ja myyntiarvioihin muutoksia?

Kun resurssien määrityksen jaksotukset joskus harvoin lasketaan uudelleen tai kun niiden päivämääräraja ei ole sama kuin lähdeprojektissa, myynti- ja kustannusarvioissa voi näkyä eroja. Asiakkaiden odotetaan testaavan päivitysprosessin osana projektien näytejoukkoa, sillä tällä tavoin he voivat hahmottaa mahdolliset aikataulumuutokset:
