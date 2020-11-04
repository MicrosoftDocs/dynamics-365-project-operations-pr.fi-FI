---
title: Uutuudet ja muutokset Project Service Automation -päivitysjulkaisussa 20, V3
description: Tässä aiheessa on luettelo ominaisuuksista ja korjauksista, jotka ovat käytettävissä Project Service Automation -päivitysjulkaisussa 20, V3.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom: dyn365-projectservice
ms.date: 06/12/2020
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
ms.openlocfilehash: 12edae76dbc6de63d3e2d36058c4092f80ede77d
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/16/2020
ms.locfileid: "4075297"
---
# <a name="project-service-automation-update-release-20-v3"></a>Project Service Automation -päivitysjulkaisu 20, V3

Meillä on ilo julkistaa Dynamics 365:n Project Service Automation-sovelluksen uusin päivitys. Tämä julkaisu sisältää joitakin tärkeitä parannuksia laatuun, tehokkuuteen ja käytettävyyteen. Tämä versio on yhteensopiva Dynamics 365 -versioiden 9.x kanssa. Jos haluat päivittää tämän julkaisun, avaa Dynamics 365 online -hallintakeskuksen Ratkaisut-sivu ja asenna päivitys. Lisätietoja: [Ensisijaisen ratkaisun asentaminen, päivittäminen tai poistaminen](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).

Tässä aiheessa on luettelo ominaisuuksista ja korjauksista, jotka ovat uusia tai muuttuneita Project Service Automation V3 -päivitysjulkaisussa 20. Tämän version koontiversion numero on V 3.10.31.37, ja se on yleisesti saatavana itsepäivittyvänä kesäkuussa 2020.

## <a name="update-release-20"></a>Päivitysjulkaisu 20

### <a name="bug-fixes"></a>Ohjelmavirhekorjauksia

**Projektinhallinta**

Seuraavat ongelmat on korjattu:

- Kun projektiryhmän jäseniä tuodaan käyttämällä kohdistusmenetelmää, joka edellyttää tunteja, tuloksena on epäselvä virhesanoma, kun määritetyt tunnit ovat nolla.
- Käyttäjät saavat virheellisen virheen, kun projektitehtävän **Kuvaus** -kenttään on syötetty enimmäismäärä merkkejä.
- **Microsoft Dynamics 365 Project Service Automation -laajennuksen lataus** -sivu ohjaa englanninkieliselle lataussivulle, kun käyttäjän kieliasetukseksi on määritetty japani.
- Kun palvelinvirhe ilmenee, **Projektit** -lomakkeen **Aikataulu** -välilehden synkronoinnin selite säilyy joskus.
- Tarpeettomia tehtävien päivityksiä lähetetään palvelimeen, kun tehtävää muokataan.

**Sales**

Seuraavat ongelmat on korjattu:

- Kun kaksoisnapsautat **Palvelusopimus** -lomakkeessa **Luo lasku** -painiketta, se luo kaksi laskua yksittäiselle toteutuneiden arvojen tietueelle.
- Internet Explorer 11 -käyttäjät eivät voi luoda kulumerkintöjä.
- Kulujen peruutusta ja laskuttamattoman myynnin toteutuneita arvoja ei linkitetä.
- **Projekti** -lomakkeen **Päivitä toteutuneet** - painike ei päivitä **tehtävän todellisia tunteja**.
- **PreValidateProjectTeamMemberCreate** -laajennus voi luoda kaksoiskappaleisia yleisiä varattavissa olevia resursseja, kun määritteen **msdyn_isgenericresourceprojectscoped** arvo on **False**.
- **Laske uudelleen** -toiminto tyhjentää tuotepohjaisten tarjousrivien ja sopimusrivin tietojen laskutettavat kustannukset.
- Tietyissä tilanteissa **PostEstimateLineUpdate** -laajennus näyttää null-viittauksen poikkeusvirheen.
- **Kannattavuusanalyysikaavion** ajanjakson kesto ei vastaa kustannusten kestoa tarjouksen kiinteähintaisella tarjousrivillä.
- Yksikkö- ja yksikköryhmäarvot eivät oletusarvon mukaan ole oikein **Sopimusrivin tiedot** - ja **Tarjousrivin tiedot** -lomakkeiden kululuokille.
- **Organisaation yksikkökustannushinta** -luettelot sallivat päivämäärän voimassaolon päällekkäisyydet.
- Käyttäjät eivät voi muuttaa **organisaatioyksikköä** , kun järjestystyyppi ei ole työpohjainen, koska se johtaa null-viittauksen poikkeusvirheeseen.
- Kun yrität siirtyä **Tarjousrivin tiedot** -lomakkeesta takaisin **Tarjous** -välilehteen, lomake päivittyy ja näyttää **Yhteenveto** -välilehden.
