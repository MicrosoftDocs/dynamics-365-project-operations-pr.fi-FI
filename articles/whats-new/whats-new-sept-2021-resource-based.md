---
title: Uudet ominaisuudet, syyskuu 2021 – Project Operations resursseihin ja ei-varastoitaviin perustuvissa skenaarioissa
description: Tässä aiheessa on tietoja Project Operationsin resursseihin ja ei-varastoitaviin perustuvissa skenaarioissa -palvelun syyskuussa 2021 julkaistussa versiossa saatavilla olevista laatupäivityksistä.
author: sigitac
ms.date: 09/12/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 842ea95892fa4f7a29a778cfd2c33a66e84f676c
ms.sourcegitcommit: 74a7e1c9c338fb8a4b0ad57c5560a88b6e02d0b2
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/23/2021
ms.locfileid: "7547150"
---
# <a name="whats-new-september-2021---project-operations-for-resourcenon-stocked-based-scenarios"></a>Uudet ominaisuudet, syyskuu 2021 – Project Operations resursseihin ja ei-varastoitaviin perustuvissa skenaarioissa

*Käytetään: Project Operationsin resursseihin ja ei-varastoitaviin perustuvissa skenaarioissa*

Tämä aihe koskee seuraavia Dynamics 365 Project Operationsin komponentteja ja versioita:

   - Project Operations Microsoft Dataversessä ympäristöversio 4.14.0.99.
   - Projektinhallinta ja kirjanpito Dynamics 365 Finance -ympäristön versiossa 10.0.20.

## <a name="project-operations-dual-write-maps-updates"></a>Project Operationsin kaksoiskirjoituskarttojen päivitys

Tässä versiossa ei ole päivityksiä Project Operationsin kaksoiskirjoituskartoille. Project Operationsin kaksoiskirjoituskarttojen luettelo ja versiot ovat kohdassa [Project Operationsin kaksi kaksoiskirjoituskarttojen versiot](../environment/resource-dual-write-maps.md).

Suorita aina ympäristön kartan uusin versio ja ota käyttöön kaikki taulukkokartat, kun päivität Project Operations Dataverse -ratkaisua ja rahoitusratkaisun versiota. Tietyt ominaisuudet ja toiminnot eivät ehkä toimi oikein, jos kartan uusinta versiota ei ole aktivoitu. Kartan aktiivinen versio näkyy **Kaksoiskirjoitus**-sivun **Versio**-sarakkeessa. Voit aktivoida kartan uuden version valitsemalla **Taulukkokartan versiot**, valitsemalla uusimman version ja tallentamalla sitten valitun version. Jos olet mukauttanut valmiin taulukkokartan, kohdista muutokset uudelleen. Lue lisätietoja kohdasta [Ratkaisun elinkaaren hallinta](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Jos kartan käynnistämisen yhteydessä tulee ongelma, seuraa ohjeita [Puuttuvien taulukkosarakkeiden ongelma kartoissa](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) -osassa kaksoiskirjoituksen vianmääritysoppaassa.

## <a name="quality-updates"></a>Laatupäivitykset

### <a name="project-operations-on-dataverse"></a>Project Operations Dataversessä

| **Ominaisuusalue** | **Viitenumero** | **Laatupäivitys** |
| --- | --- | --- |
| Aika ja kulut | 1811407 | Kulumerkinnän hyväksynnän projektihyväksyjän käyttöoikeusrooli oikaistu. |
| Aika ja kulut | 1811438 | Aikamerkinnän hyväksynnän peruutuksen projektihyväksyjän käyttöoikeusrooli oikaistu. |
| Aika ja kulut | 2370126 | Päivitetty **Projektitehtävä**- ja **Rooli**-kuvakkeet **Aikamerkintä**-entiteetissä. |
| Aika ja kulut | 2379879 | Korjattu aikamerkinnän **Kopioi viikko** -funktio käytettäessä Dynamics 365:n puhelinversiota. |
| Laskutus ja hinnoittelu | 2371906 | Proformalaskun kokonaissumma ei saa olla säädettävä Project Operations resurssipohjaisissa käyttöönotoissa -palvelussa. |
| Laskutus ja hinnoittelu | 2385802 | Korjattiin virhe, joka ilmeni, kun toteutuneet tunnit ovat negatiiviset projektin kokonaissummia päivitettäessä. |
| Laskutus ja hinnoittelu | 2389675 | Proformalaskun vahvistamisen toimintaa parannettu. Pitkäkestoisten töiden entiteetin on otettava huomioon aktiviteetti, jota tarvitaan vahvistustulosten kirjoittamisessa kirjanpitoa varten. |

### <a name="project-management-and-accounting-in-dynamics-365-finance"></a>Dynamics 365 Financen projektinhallinta ja kirjanpito

| Ominaisuusalue | Viitenumero | Laatupäivitys |
| --- | --- | --- |
| Matka ja kulut | [4618082](https://fix.lcs.dynamics.com/Issue/Details?kb=4618082&amp;bugId=583101&amp;dbType=3&amp;qc=9c85ac8ca1e5e9cd07fac9e9aa2cb0914724e28b86ad3339dacf7741f554c605) | Määrät toimittaja- ja arvonlisäverotapahtumissa, jotka kirjattiin kulusta, joka luotiin luottokorttitapahtumasta, ovat virheellisiä. |
| Matka ja kulut | [4620366](https://fix.lcs.dynamics.com/Issue/Details?kb=4620366&amp;bugId=579485&amp;dbType=3&amp;qc=e864789bd95505ea624c537d585bf113c2de60b97c88439d44693dbd85aa8e92) | Väärät tilitysrivit luodaan, kun maksukirjauskansio muodostetaan. |
| Matka ja kulut | [4618082](https://fix.lcs.dynamics.com/Issue/Details?kb=4618082&amp;bugId=583101&amp;dbType=3&amp;qc=9c85ac8ca1e5e9cd07fac9e9aa2cb0914724e28b86ad3339dacf7741f554c605) | Määrät arvonlisäverotapahtumissa, jotka kirjattiin kulusta, joka luotiin luottokorttitapahtumasta, ovat virheellisiä. |
| Matka ja kulut | [4621765](https://fix.lcs.dynamics.com/Issue/Details?kb=4621765&amp;bugId=587306&amp;dbType=3&amp;qc=6fbfad0123d4e95eaf8d5a5a2f6c354577c991b7905c852ab02d1f94e728a876) | Kulurivin poistaminen voi kestää kauan. |
| Projektin kirjanpito | [4623737](https://fix.lcs.dynamics.com/Issue/Details?kb=4623737&amp;bugId=598109&amp;dbType=3&amp;qc=4101fc5865201e21815299f2ff11ae46d5d5370510868df86c25ee09a8ca1a0c) | Kun käytät KB 4619395:n, numerojärjestyksen muuttamista muotoon **Jatkuva** ei tueta, ja kun kirjaat arvion, tulee seuraava virhe: "Järjestelmä ei tue Proj_X:n numerojärjestyksen määritystä 'jatkuva'." |
| Projektin kirjanpito | [4623332](https://fix.lcs.dynamics.com/Issue/Details?kb=4623332&amp;bugId=586034&amp;dbType=3&amp;qc=2f64bb1977c4a9c9dd2ce9de7e72230b86eca14b6295c5bbfb614ea97ad81caf) | Toimittajan laskun kirjaaminen voi epäonnistua ja näyttöön voi tulla seuraava virhesanoma: "Tositteen tapahtumat eivät täsmää per 17.5.2021. (kirjanpitovaluutta: 0,00 – raportointivaluutta: 0,01)." |
