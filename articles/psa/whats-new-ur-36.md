---
title: Uutuudet ja muutokset Project Service Automation -päivitysjulkaisussa 36, V3
description: Tässä aiheessa on lueteltu ominaisuudet ja korjaukset, jotka ovat saatavissa Microsoft Dynamics 365 Project Service Automation -päivityksessä 36, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 10/06/2021
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
ms.openlocfilehash: 9b85aed79acb7e7784a23f54a2e9af1cc83f5f4d
ms.sourcegitcommit: 6d9fc4dc851814664bf71729904ab4bedd85fe70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/06/2021
ms.locfileid: "7606749"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-36-v3"></a>Uutuudet ja muutokset Project Service Automation -päivitysjulkaisussa 36, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Meillä on ilo esitellä Microsoft Dynamics 365 Project Service Automation -sovelluksen uusin päivitys. Tämä julkaisu sisältää joitakin tärkeitä parannuksia laatuun, tehokkuuteen ja käytettävyyteen. Se on yhteensopiva Dynamics 365 9.x -version kanssa. Päivitä tähän versioon asentamalla päivitys Dynamics 365 -hallintakeskuksen online-ratkaisujen sivulta. Lisätietoja: [Ensisijaisen ratkaisun asentaminen, päivittäminen tai poistaminen](/power-platform/admin/install-remove-preferred-solution).

Tässä aiheessa on luettelo ominaisuuksista ja korjauksista, jotka ovat uusia tai muuttuneita Project Service Automationin Päivitysjulkaisussa 36, V3. Tällä versiolla on koontinumero V3.10.57.152 ja se on ollut yleisesti saatavilla itsepalvelupäivityksenä lokakuusta 2021 lähtien.

## <a name="update-release-36"></a>Päivitysjulkaisu 36

### <a name="bug-fixes"></a>Ohjelmavirhekorjauksia

Seuraavat ongelmat on korjattu.

**Yhteiset**
- **Oletustyötuntimalli**-kentän nimi on käännetty väärin **Projektin parametrit**-sivulla.
- Asynkroniset laajennukset eivät käsittele **SharedVariableService**-palveluun liittyviä poikkeuksia oikein.

**Aika ja kulu**
- Kun kirjauskansion rivit puuttuvat tai käyttäjällä ei ole kirjauskansion rivien lukuoikeutta, tapahtuu virhe, kun projektin hyväksynnät peruutetaan.
- Käyttäjät eivät voi peruuttaa hyväksyntää, jos kuluun tai aikamerkintään on liitetty enemmän kuin yksi projektihyväksyntä.
- Kohdat **Poissaolo** ja **Loma** on käännetty väärin kiinan kielelle **Aikamerkintä**-pikaluontisivun haussa.

**Resurssien hallinta**
- Käyttäjä ei voi hakea resursseja **Ajoitusavustajasta**, kun näyttötilaksi on määritetty **Päivä**, **Viikko** tai **Kuukausi**.
- Yleiset resurssit saavat virheellisesti tyhjiä toimen nimiä. 
- Sopimuksen sulkeminen hävittynä ei peruuta tulevia varauksia.

**Myynti**
- Kun ympäristössä on paljon tuotteita, suorituskyky heikentyy **Materiaaliarvio**-ruudukossa.
- Kun projekti luodaan mallista, projektivaluutta ei oletusarvoisesti vastaa projektipäällikön sopimusyksikköä.
- Todelliset summat eivät aina vastaa sitä, mitä projektin määräajassa näkyy tai määristä tulee negatiivisia tietyissä palautusskenaarioissa.
- Tapahtuu virhe, kun liität projektimallista luodun projektin sopimusriviin.
- Käyttäjät voivat poistaa sopimusrivin, jolla on välitavoitteet **Valmis laskuttamista varten** ja **Lasku luotiin**. Tämän ei pitäisi olla sallittua.
- Kun projektista tuodaan arvioita, tarjousrivin tietojen laskutettavuus määritetään virheellisesti, kun tehtäväpohjainen laskutus on otettu käyttöön tarjousrivillä.
- Kun lisäät kiinteähintaisen laskutuksen välitavoitteen, välitavoite näkyy välitavoitteen aliruudukossa vasta, kun sivu on päivitetty.
- Tyhjän viittauksen poikkeus muodostetaan, kun luot projektisopimuksen, jonka tarjouksen nimi on tyhjä.
- Manuaaliset tilatehtävät, joissa projektivaluutta on eri kuin resurssin valuutta, johtavat virheellisiin hinta-arvioihin.
- Käyttäjät eivät voi palauttaa tapahtumaa, joka on korjattu onnistuneesti korjauslaskulla.
- Käytöstä poistetut tapahtumaluokat näkyvät **Kuluarviot**-ruudukossa.



