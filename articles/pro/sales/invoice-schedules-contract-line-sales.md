---
title: Laskutusaikataulujen luominen projektipohjaisella sopimusrivillä – lite
description: Tässä aiheessa on tietoja laskutuksen aikataulujen ja välitavoitteiden luomisesta.
author: rumant
ms.date: 10/26/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: dc0cf92ed7af0353baa0f93fc7fb69e02905f805eb04a7b4c7bc99cfe59da62a
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/06/2021
ms.locfileid: "7006062"
---
# <a name="create-invoice-schedules-on-a-project-based-contract-line---lite"></a>Laskutusaikataulujen luominen projektipohjaisella sopimusrivillä – lite

_**Käytetään:** Lite-käyttöönotto – kauppa proformalaskutukseen_

Laskutusaikataulun voi liittää projektipohjaiseen sopimusriviin. Laskutus on mahdollista vasta, kun sopimus voitettu ja projektisopimus luodaan. Laskutusaikatauluissa on mahdollista luoda projektipohjaisen sopimusrivin laskuluonnos automaattisesti. Jos laskut on tarkoitus luoda aina manuaalisesti, projektipohjaisen sopimusrivin tai sopimusrivin laskuaikataulujen luominen voidaan ohittaa.

## <a name="create-a-time-and-material-invoice-schedule-for-a-project-based-contract-line"></a>Projektipohjaisen sopimusrivin ajan ja materiaalin laskutusaikataulun luominen

Kun projektipohjaisella sopimusrivillä on aika- ja materiaalilaskutapa, voit luoda päivämäärään perustuvan laskuaikataulun. Jos haluat luoda päivämäärään perustuvan laskutusaika taulun automaattisesti, tee seuraavat toimet.

1. Määritä laskutustiheys valitsemalla **Asetukset** > **Laskutustiheys**.
2. Avaa projektisopimus ja määritä pyydetty toimituspäivä **Yhteenveto**-välilehdessä.
3. Avaa se ajan ja materiaalin sopimusrivi, jolle haluat luoda päivämäärään perustuvan laskutusaikataulun. 
4. Valitse **Laskutusaikataulu**-välilehdessä laskutuksen alkamispäivä ja laskutustiheys. 
5. Valitse aliruudukossa **Luo laskutusaikataulu**.

    Järjestelmä luo laskutusaikataulun, jonka kentissä on seuraavat tiedot:

    - **Laskun suorituspäivä** -arvoksi määritetään laskutustiheyteen perustuva päivämäärä.
    - **Tapahtuman katkaisupäivä** -arvoksi määritetään **Laskun suorituspäivä** -arvoa edeltävä päivä.
    - **Suorituksen tila** -arvoksi määritetään automaattisesti **Ei suoritettu**. Kun automaattisen laskun luontityö suoritetaan tietylle **laskun suorituspäivälle**, kentän arvoksi päivitetään joko **Suoritus onnistui** tai **Suoritus epäonnistui**.

## <a name="create-a-fixed-price-invoice-schedule-for-a-project-based-contract-line"></a>Projektipohjaisen sopimusrivin kiinteähintaisen laskutusaikataulun luominen

Jos projektipohjaisen sopimusrivin laskutustapa on kiinteähintainen, laskutusaikataulu voidaan luoda välitavoitteiden perusteella. Seuraavilla ohjeilla luodaan automaattisesti välitavoitteeseen perustuva laskutusaikataulu sellaiselle kiinteälle välitavoitejoukolle, joka jakautuu tasaisesti kalenterijaksolle.

1. Määritä laskutustiheys valitsemalla **Asetukset** > **Laskutustiheys**.
2. Avaa projektisopimus ja määritä pyydetty toimituspäivä **Yhteenveto**-välilehdessä.
3. Avaa se kiinteähintainen sopimusrivi, jolle on luotava välitavoiteaikataulu. 
4. Valitse **Laskutusaikataulu (laskutuksen välitavoitteet)**-välilehdessä laskutuksen alkamispäivä ja laskutustiheys. 
5. Valitse aliruudukossa **Luo jaksoittaiset välitavoitteet**.

    Järjestelmä luo laskutusaikataulun, jonka kentissä on seuraavat välitavoitetiedot:

    - **Välitavoitteen nimi** -arvoksi on määritetty laskutustiheyteen perustuva päivämäärä.
    - **Välitavoitteen päivämäärä** -arvoksi on määritetty laskutustiheyteen perustuva päivämäärä.
    - **Välitavoitteen** lasketaan jakamalla projektipohjaisen sopimusrivin sopimussumma tiheyteen sekä laskutuksen alkamis- ja pyydettyyn toimituspäivään perustuvien välitavoitteiden määrällä.
    - Jos sopimusrivin **Arvioitu verosumma** -kentässä on arvo, myös tämä kenttä jaetaan tasan kullekin välitavoitteelle kausittaisia välitavoitteita luotaessa.

Laskutuksen välitavoitteiden on oltava yhtä suuri kuin projektipohjaisen sopimusrivin sopimusarvo. Jos ne eivät ole yhtä suuri, tapahtuu virhe. Virheen voi korjata varmistamalla, että laskutuksen välitavoitteiden yhteissumma on sama kuin rivin sopimusarvo. Tämä voidaan tehdä luomalla, muokkaamalla tai poistamalla välitavoitteita. Kun muutokset on tehty, päivitä sivu.

### <a name="manually-create-milestones"></a>Luo välitavoitteet manuaalisesti

Kiinteähintaiset välitavoitteet voidaan luoda manuaalisesti, kun niitä ei ole jaettu kausittain. Välitavoite luodaan manuaalisesti seuraavien ohjeiden mukaisesti.

1. Avaa se kiinteähintainen sopimusrivi, johon haluat luoda välitavoitteen. 
2. Valitse **Laskutusaikataulu**-välilehden aliruudukossa **+ Luo uusi sopimusrivin välitavoite**.
3. Anna **Välitavoitteen luonti** -lomakkeessa tarvittavat tiedot seuraavan taulukon perusteella. 

| Field | Sijainti | Kuvaus | Loppupään vaikutus |
| --- | --- | --- | --- |
| Välitavoitteen nimi | Pikaluonti | Välitavoitteen nimen tekstikenttä. | Tämä kenttä sisältyy projektisopimusrivin välitavoitteeseen ja laskuun. |
| Projektin tehtävä | Pikaluonti | Jos välitavoite on sidottu projektitehtävään, lisää mukautettu logiikka tämän viittauksen avulla ja määritä välitavoitteen tila tehtävän tilan perusteella. | Tämä viittaus ei vaikuta myöhemmin tehtävään. |
| Välitavoitteen päivämäärä | Pikaluonti | Päivämäärä, jolloin automaattisen luontiprosessin on etsittävä tämän välitavoitteen tilaa mahdollista laskutusta varten. | Se sisältyy projektisopimusrivin välitavoitteeseen ja laskuun. |
| Laskun tila | Pikaluonti | Kun välitavoite on luotu, tämä tila on aina **Ei valmis laskutukseen** tai **Ei aloitettu**. | Se sisältyy projektisopimusrivin välitavoitteeseen ja laskuun. |
| Rivisumma | Pikaluonti | Asiakkaalta laskutettavan välitavoitteen summa tai arvo. | Tämä kenttä sisältyy projektisopimusrivin välitavoitteeseen ja laskuun. |
| Vero | Pikaluonti | Välitavoitteessa käytetty verosumma. | Se sisältyy projektisopimusrivin välitavoitteeseen ja laskuun. |

4. Valitse **Tallenna ja sulje**.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]