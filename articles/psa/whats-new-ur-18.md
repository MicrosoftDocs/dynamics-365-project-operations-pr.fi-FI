---
title: Uutuudet ja muutokset Project Service Automation -päivitysjulkaisussa 18, V3
description: Tässä aiheessa on luettelo ominaisuuksista ja korjauksista, jotka ovat käytettävissä Project Service Automation -päivitysjulkaisussa 18, V3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 04/27/2020
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
ms.openlocfilehash: d6e0bb669513185ca266858ea9b8a89ed6dd4408
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/10/2021
ms.locfileid: "5147199"
---
# <a name="project-service-automation-update-release-18-v3"></a>Project Service Automation -päivitysjulkaisu 18, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Meillä on ilo julkistaa Dynamics 365:n Project Service Automation-sovelluksen uusin päivitys. Tämä julkaisu sisältää joitakin tärkeitä parannuksia laatuun, tehokkuuteen ja käytettävyyteen. Tämä versio on yhteensopiva Dynamics 365 -versioiden 9.x kanssa. Jos haluat päivittää tämän julkaisun, avaa Dynamics 365 online -hallintakeskuksen Ratkaisut-sivu ja asenna päivitys. Lisätietoja: [Ensisijaisen ratkaisun asentaminen, päivittäminen tai poistaminen](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).

Tässä aiheessa on luettelo ominaisuuksista ja korjauksista, jotka ovat uusia tai muuttuneita Project Service Automation V3 -päivitysjulkaisussa 18. Tämän version koontiversion numero on V 3.10.8.12, ja se on yleisesti saatavana itsepäivittyvänä huhtikuussa 2020.

## <a name="update-release-18"></a>Päivitysjulkaisu 18

### <a name="bug-fixes"></a>Ohjelmavirhekorjauksia

**Aika ja kulu**

- Korjattu: **Palautus**-, **Pyyntö**- ja **Peruuta hyväksyntä** -työnkulut aiheuttavat poikkeuksen, joiden virhesanoma on epäselvä.
- Korjattu: kun **Peruuta hyväksyntä** epäonnistuu kulun osalta, se ei aiheuta siihen liittyvää poikkeusta.
- Korjattu: Aikamerkintä-ruudukko käsittelee Australian muut kuin työpäivät virheellisesti lokakuussa tapahtuvan talviaikaan siirtymisen jälkeen.
- Korjattu: virheellinen oletuslogiikka estää kulujen lähettämisen.
- Korjattu: kun aikamerkinnän hyväksyntä epäonnistuu, hyväksyntä pysyy **Odottaa**-tilana.
- Korjattu: joukkohyväksymisten SQL-virheet (lukkiutuminen/aikakatkaisu).
- Korjattu: ryhmän jäsenten päivittäminen aikamerkintöjä hyväksyttäessä aiheuttaa merkittäviä käyttökokemuksen suorituskykyongelmia.

**Projektinhallinta**

- Korjattu: aikavyöhykeilmoitus siirrettiin **Täsmäytys**-näkymästä **Projekti**-päälomakkeeseen.
- Korjattu: kalenterimallissa ei käytetä oikeita oletusarvoja, kun uusi projektilomake avautuu.
- Korjattu: chromium-pohjaisten selainten käyttäjillä ei ole helppoa tapaa valita poistettavia edeltäjän tehtäviä.
- Korjattu: kun **projektin tyhjää mallia** käytetään luontiin tai kopiointiin, noudettavat tehtävät eivät liity siihen.
- Korjattu: joissakin reunan palvelupyynnöissä uuden määrityksen luonti tehtäväruudukossa aiheuttaa tietueiden kaksoiskappaleiden luonnin.
- Korjattu: käyttäjät eivät voi päivittää manuaalisessa tilassa tehtävän alkamispäiviä nykyistä tallennettua päivämäärää myöhäisemmäksi.

**Resurssienhallinta**

- Korjattu: **Täsmäytys**-näkymän välisummarivi laskee varausten eron virheellisesti varausten laajennusten jälkeen.
- Korjattu: **Täsmäytys**-näkymä näyttää resurssimääritykset virheellisesti, kun varattavissa olevalla resurssilla on kalenteri, joka ei vastaa projektikalenteria.

**Sales**

- Korjattu: kun aikamerkinnät hyväksytään uudelleen (**Hyväksy > Peruuta >** hyväksyntä uudelleen), todellisen ei-veloitettavan kaksoiskappale luodaan.


[!INCLUDE[footer-include](../includes/footer-banner.md)]