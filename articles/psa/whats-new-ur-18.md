---
title: Uutuudet ja muutokset Project Service Automation -päivitysjulkaisussa 18, V3
description: Tässä artikkelissa on luettelo ominaisuuksista ja korjauksista Project Service Automationin päivitysjulkaisussa 18, V3.
author: ruhercul
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
ms.reviewer: johnmichalak
ms.openlocfilehash: e8d423c550d9aa09c9cbb7d4f7c277c43bbe10ae
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8918860"
---
# <a name="project-service-automation-update-release-18-v3"></a>Project Service Automation -päivitysjulkaisu 18, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Meillä on ilo julkistaa Dynamics 365:n Project Service Automation-sovelluksen uusin päivitys. Tämä julkaisu sisältää joitakin tärkeitä parannuksia laatuun, tehokkuuteen ja käytettävyyteen. Tämä versio on yhteensopiva Dynamics 365 -versioiden 9.x kanssa. Jos haluat päivittää tämän julkaisun, avaa Dynamics 365 online -hallintakeskuksen Ratkaisut-sivu ja asenna päivitys. Lisätietoja: [Ensisijaisen ratkaisun asentaminen, päivittäminen tai poistaminen](/power-platform/admin/install-remove-preferred-solution).

Tässä artikkelissa on luettelo ominaisuuksista ja korjauksista, jotka ovat uusia tai muuttuneita Project Service Automation V3:n päivitysjulkaisussa 18. Tämän version koontiversion numero on V 3.10.8.12, ja se on yleisesti saatavana itsepäivittyvänä huhtikuussa 2020.

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
