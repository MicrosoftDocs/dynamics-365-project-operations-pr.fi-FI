---
title: Uutuudet ja muutokset Project Service Automation -päivitysjulkaisussa 19, V3
description: Tässä aiheessa on luettelo ominaisuuksista ja korjauksista, jotka ovat käytettävissä Project Service Automation -päivitysjulkaisussa 19, V3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 05/05/2020
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
ms.openlocfilehash: 0137d0241238ff96de406884dd05a5d7f023c318
ms.sourcegitcommit: 3d78338773929121d17ec3386f6cb67bfb2272cc
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/27/2021
ms.locfileid: "5949135"
---
# <a name="project-service-automation-update-release-19-v3"></a>Project Service Automation -päivitysjulkaisu 19, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Meillä on ilo julkistaa Dynamics 365:n Project Service Automation-sovelluksen uusin päivitys. Tämä julkaisu sisältää joitakin tärkeitä parannuksia laatuun, tehokkuuteen ja käytettävyyteen. Tämä versio on yhteensopiva Dynamics 365 -versioiden 9.x kanssa. Jos haluat päivittää tämän julkaisun, avaa Dynamics 365 online -hallintakeskuksen Ratkaisut-sivu ja asenna päivitys. Lisätietoja: [Ensisijaisen ratkaisun asentaminen, päivittäminen tai poistaminen](/power-platform/admin/install-remove-preferred-solution).

Tässä aiheessa on luettelo ominaisuuksista ja korjauksista, jotka ovat uusia tai muuttuneita PSA V3 -päivitysjulkaisussa 19. Tämän version koontiversion numero on V3.10.30.41, ja se on yleisesti saatavana itsepäivittyvänä toukokuussa 2020.

## <a name="update-release-19"></a>Päivitysjulkaisu 19

### <a name="bug-fixes"></a>Ohjelmavirhekorjauksia

**Aika ja kulu**

Seuraavat ongelmat on korjattu: 

- Aikamerkintöjen tuonneisrta johdetut virheet eivät näy oikein.
- Ajansyöttöruudukko ei tue **Vain päivämäärä** -kentän toimintaa.
- Projektiresurssit eivät voi luoda kuluja projektiin.

**Projektinhallinta**

Seuraavat ongelmat on korjattu: 

-  Alitason alitason tehtävä aiheuttaa virheellisen työmääräarvion valmistumisen laskennan (EAC) aikana.

**Sales**

Seuraavat ongelmat on korjattu: 

- **Laske uudelleen** -toiminto ei toimi kulusopimusrivin tai tarjousrivin tietojen kanssa.
- Kuluarvioista puuttuu **Päivitä hinnat**.
-  Asiakkaat eivät voi valita mukautettuja palvelusopimuksen tilan syitä **Projektisopimus**-sivulla.
- Asiakkaat kokevat heikentyneen suorituskyvyn luotaessa mukautettua hinnastoa tarjouksesta.
- Asiakkaat kokevat epäjohdonmukaisuutta **Tarjousrivin tiedot**- ja **Sopimusrivin tiedot** -sivujen **yksiköiden** oletusarvojen kanssa.
- Jos lisäät ei-laskutettavan tapahtumaluokan nimikkeitä laskutettavaan sopimusriviin, toiminta ei noudata tapahtumaluokan **Ei-laskutettava**-laskutustyyppiä.
- Asiakkaat eivät voi käyttää aiemmin luotujen palvelusopimusten juuri lisättyjä rooleja ja luokkia.
- Asiakkaat kokevat heikentyneen suorituskyvyn tarpeettomasssa kohteen PreValidateProjectTeamMemberUpdate.cs noudossa
- Jos roolit on määritetty ei-laskutettaviksi **Resurssiluokat**-luettelossa, ne on lisättävä **Laskutettavat roolit** -välilehteen projektisopimusriville arvolla **Ei-laskutettava**.
- Asiakkaat saattavat kokea heikentyneen suorituskyvyn luodessaan projektia, koska **GetBookableResourceIdFromUser** hakee varattavissa olevien resurssien kaikki sarakkeet pelkän ensisijaisen tunnuksen sijaan.
- **TransactionType**-entiteetistä puuttuu esivahtistuken päivityslaajennus, joka estää käyttäjiä syöttämästä **yksiköitä** ja **yksikköryhmiä**, jotka eivät ole kelvollisia tapahtumatyypeille.
- **Poista**-vaihe ei toimi aikamerkintöjen tuonnissa.


[!INCLUDE[footer-include](../includes/footer-banner.md)]