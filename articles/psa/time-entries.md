---
title: Luo aikamerkintöjä
description: Tässä aiheessa on tietoja aikamerkintöjen luomisesta.
author: rumant
ms.custom:
- dyn365-projectservice
ms.date: 05/20/2019
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: bc8e52fef0aa02505e412c746343ce1410c40ac3
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/10/2021
ms.locfileid: "5999262"
---
# <a name="create-time-entries"></a>Luo aikamerkintöjä

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Aiemmissa Dynamics 365 Project Service Automation-versioissa aikamerkinnät on syötetty viikoittain. Project Service Automationin versiossa 3 aikamerkinnät syötetään päivittäin. Voit kuitenkin luoda tai kopioida aikamerkintöjä useita kerrallaan sen jälkeen, kun muutama aikamerkintä on luotu.

## <a name="create-a-time-entry"></a>Luo aikamerkintä

Luo aikamerkintä seuraavien vaiheiden mukaisesti:

1. Valitse **Aikamerkinnät**-sivulla **Uusi**.
2. Kirjoita **Pikaluonti: aikamerkintä** -valintaikkunaan aikamerkinnän kesto minuutteina, tunteina tai päivinä. Kesto on ilmoitettava seuraavassa muodossa: *x* minuuttia, *x* tuntia tai *x* päivää. Tunnit ja päivät voidaan ilmoittaa myös desimaalilukuina, kuten *x.x* tuntia tai *x.x* päivää.
3. Valitse aikamerkinnän tyyppi ja projekti, jolle olet syöttämässä aikamerkintää.
4. Etsi **Projektitehtävä**-kentässä tämän aikamerkinnän tehtävä.

    > [!NOTE]
    > Jos olet luomassa aikamerkintää tehtävälle, jota ei ole kohdennettu käyttäjälle **Projektitehtävä**-kentässä, valitse **Etsi**-painike, valitse **Muuta näkymää** ja valitse sen jälkeen **Kaikki aktiiviset projektitehtävät** nähdäksesi listan tehtävistä.

5. Kirjoita kuvaus, jos kuvaus on pakollinen, ja valitse sitten **Tallenna ja sulje**.

Kun aikamerkintä on luotu ja tallennettu, voit muokata sitä ajansyöttöruudukossa. Ajansyöttöruudukko tukee kahta muotoa:

- Voit kirjoittaa aikamerkinnät muodossa **hh:mm**. Tämä muoto muunnetaan sitten tunneiksi ja murtoluvuiksi.
- Voit määrittää tunnit ja murtoluvut suoraan.

Huomaa, että tunnin murto-osat eivät ole minuutteja. 1,5 tunnin osuus on siis 1 tunti ja 30 minuuttia. Sama sääntö koskee päivien murto-osia. Yksi päivä on 24 tuntia, ja 0,5 päivää on 12 tuntia.

## <a name="bulk-create-time-entries"></a>Luo useita aikamerkintöjä kerralla

Sen jälkeen, kun muutama aikamerkintä on luotu, voit kopioida niitä luodaksesi kerralla useita aikamerkintöjä.

1. Valitse **Aikamerkinnät**-sivulla **Kopioi viikko**.
2. Määritä **Lähdejakso** -kenttäryhmässä **Alkamispäivä** ja **Päättymispäivä** -kentissä päivämääräväli, jolta aikamerkinnät kopioidaan.
3. Määritä **Kohdejakso** -kenttäryhmässä **Alkamispäivä**-kentässä päivämäärä, jolle luodaan aikamerkintöjä.
4. Valitse **Kopioi**, jos haluat luoda kopion aikakiertauksista, jotka vastaavat sitä viikonpäivää, joka on määritelty **Kohdejakso**-kenttäryhmässä. Esimerkiksi edellisen viikon maanantain aikakirjaus kopioidaan sen viikon maanantaille, joka on määritetty **Kohdejakso**-kenttäryhmässä.

## <a name="import-data-for-time-entries"></a>Aikamerkintöjen tuontitiedot

Voit tuoda tietoja projektin varauksista ja kohdennuksista. Kun tuot tietoja, voit määrittää tuotavien varausten päivämäärävälin ja valita sitten erikseen varaukset, jotka luodaan **Luonnos**-tyyppisinä aikakirjauksina.

## <a name="group-by-sort-search-and-filter-capabilities"></a>Ryhmittely-, lajittelu-, haku- ja suodatusominaisuudet

Voit ryhmitellä ja suodattaa aikakirjauksia sarakkeissa määritettyjen dimensioiden mukaan. Valitse **Ryhmittelyperuste**-kentässä aikamerkintöjen suodatuksessa käytettävä dimensio. Voit myös lajitella aikamerkintätietueita nousevaan tai laskevaan järjestykseen käyttämällä sarakeotsikoiden lajittelunuolta. Lisäksi voit näyttää tai piilottaa kirjauksia valitsemalla sarakeotsikoista **Suodatin**-painikkeen ja kirjoittamalla sitten **Haku**-ruutuun tekstin, jota käytetään haettaessa aikamerkintöjä projektin nimen, projektitehtävän, aikakirjauksen tai resurssin perusteella.


[!INCLUDE[footer-include](../includes/footer-banner.md)]