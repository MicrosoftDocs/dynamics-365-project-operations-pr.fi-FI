---
title: Uutuudet ja muutokset Project Service Automation -päivitysjulkaisussa 23, V3
description: Tässä aiheessa on luettelo ominaisuuksista ja korjauksista, jotka ovat käytettävissä Project Service Automation -päivitysjulkaisussa 23, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 08/25/2020
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
ms.openlocfilehash: cc918f1516d4751b3f8e70a93d8fc66058201f22
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/14/2022
ms.locfileid: "8581602"
---
# <a name="project-service-automation-update-release-23-v3"></a>Project Service Automation -päivitysjulkaisu 23, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Meillä on ilo julkistaa Dynamics 365:n Project Service Automation-sovelluksen uusin päivitys. Tämä julkaisu sisältää joitakin tärkeitä parannuksia laatuun, tehokkuuteen ja käytettävyyteen. Tämä versio on yhteensopiva Dynamics 365 -versioiden 9.x kanssa. Jos haluat päivittää tämän julkaisun, avaa Dynamics 365 online -hallintakeskuksen Ratkaisut-sivu ja asenna päivitys. Lisätietoja: [Ensisijaisen ratkaisun asentaminen, päivittäminen tai poistaminen](/power-platform/admin/install-remove-preferred-solution).

Tässä aiheessa on luettelo ominaisuuksista ja korjauksista, jotka ovat uusia tai muuttuneita Project Service Automation V3 -päivitysjulkaisussa 23. Tällä versiolla on koontinumero V3.10.34.30 ja se on ollut yleisesti saatavilla itsepalvelupäivityksenä elokuusta 2020 lähtien.

## <a name="update-release-23"></a>Päivitysjulkaisu 23

### <a name="bug-fixes"></a>Ohjelmavirhekorjauksia

**Aika ja kulu**

Seuraavat ongelmat on korjattu:
- Käsittele reunan palvelupyyntö kohdassa **Projektiryhmän jäsenen poisto**, jotta saat mielekkään poikkeuksen.
- Delegoinnin tuonnin tuloksena on tyhjä poistoruutu.

**Resurssienhallinta**

Seuraavat ongelmat on korjattu:

- **Resurssin käyttöasteruudukon resurssikortissa** näkyy virheellisiä tietoja, kun aika-asteikko on yli viisi päivää.
- Kun asiakkaat luovat varattavissa olevan resurssin, laajennus ei välillä lisää resurssia automaattisesti Microsoft Office 365 -ryhmään.
- **Täsmäytys**-näkymä näyttää manuaaliset muodot virheellisesti **Viikko**- tai **Kuukausi**-näkymässä.

**Projektinhallinta**

Seuraavat ongelmat on korjattu:

- Jos **usersettings-asetuksen RetrieveMultiple** -entiteettejä on liian suuri määrä, se heikentää projektien hyväksyntöjen ja muiden toimintojen suorituskykyä.
- **Tehtävien suunnittelu** -ruudukon resurssivalinta on rajoitettu näyttämään enintään viisi projektiryhmän jäsentä. 
- **Tehtävien suunnittelu** -ruudukon resurssihaku ei suodata passiivisia resursseja.
- Manuaalinen tila ei toimi odotetulla tavalla projektisuunnittelun työrakenteessa.
- **Tehtävien suunnittelu** -ruudukko näyttää **Passiiviset tapahtumaluokat**.
- **Resurssien delegointi** -ruudukko pyöristää virheellisesti, kun tehtävällä on useita varauksia.
- Pyöristysarvot eroavat suunniteltujen kustannusten ja todellisten kustannusten välillä yksittäisessä tehtävässä.

**Sales**

Seuraavat ongelmat on korjattu:

- **Nouda kaikki tapahtumaluokat** -kaksoisnapsautus luo useita rivejä.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
