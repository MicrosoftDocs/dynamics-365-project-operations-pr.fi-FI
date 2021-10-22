---
title: Elokuun 2021 uudet ominaisuudet – Project Operations resurssien/ei-varastoitavien skenaarioissa
description: Tässä aiheessa on tietoja laatupäivityksistä, jotka ovat käytettävissä Project Operationsin elokuussa 2021 julkaistussa versiossa resurssi- tai ei-varastopohjaisiin skenaarioihin.
author: sigitac
ms.date: 08/11/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 26861472d3af20c58b3d01142b834d535cf99715
ms.sourcegitcommit: 083e3d219cd5126eecb74debb1b70b361680b1f6
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/18/2021
ms.locfileid: "7501367"
---
# <a name="whats-new-august-2021---project-operations-for-resourcenon-stocked-based-scenarios"></a>Elokuun 2021 uudet ominaisuudet – Project Operations resurssien/ei-varastoitavien skenaarioissa

*Käytetään: Project Operationsin resursseihin ja ei-varastoitaviin perustuvissa skenaarioissa*

Tämä aihe koskee seuraavia Dynamics 365 Project Operationsin komponentteja ja versioita:

   - Project Operations Microsoft Dataversessä ympäristöversio 4.13.0.152.
   - Projektinhallinta ja kirjanpito Dynamics 365 Finance -ympäristön versiossa 10.0.20.

## <a name="features-included-in-this-release"></a>Tähän julkaisuun sisältyvät ominaisuudet

Tähän julkaisuun sisältyvät seuraavat ominaisuudet:

- **Hyväksyntäjoukot**: Hyväksyntäjoukot ryhmittelevät ajan, kulujen ja materiaalikäytön hyväksyntäpyynnöt yhteen pienemmiksi toimintoalijoukoiksi. Tämä ryhmittely sallii hyväksyntöjen käsittelemisen tietyssä järjestyksessä projektikohtaisesti ja sallii uudelleenyrittämisen ja jaksotuksen. Pyyntöjen ryhmitteleminen parantaa suurten hyväksyntämäärien käsittelyn luotettavuutta ja seurattavuutta. Lisätietoja: [Hyväksyntäjoukot](../approvals/approval-sets.md).

## <a name="project-operations-dual-write-maps-updates"></a>Project Operationsin kaksoiskirjoituskarttojen päivitys

Tässä versiossa ei ole päivityksiä Project Operationsin kaksoiskirjoituskartoille.

Project Operationsin kaksoiskirjoituskarttojen luettelo ja versiot ovat kohdassa [Project Operationsin kaksi kaksoiskirjoituskarttojen versiot](../environment/resource-dual-write-maps.md).

Suorita aina ympäristön kartan uusin versio ja ota käyttöön kaikki taulukkokartat, kun päivität Project Operations Dataverse -ratkaisua ja rahoitusratkaisun versiota. Tietyt ominaisuudet ja toiminnot eivät ehkä toimi oikein, jos kartan uusinta versiota ei ole aktivoitu. Kartan aktiivinen versio näkyy **Kaksoiskirjoitus**-sivun **Versio**-sarakkeessa. Aktivoi kartan uusi versio valitsemalla **Taulukkokarttaversiot**, valitsemalla uusin versio ja tallentamalla valittu versio. Jos olet mukauttanut valmiin taulukkokartan, kohdista muutokset uudelleen. Lue lisätietoja kohdasta [Ratkaisun elinkaaren hallinta](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Jos kartan käynnistämisessä on ongelma, noudata kohdan [Puutuvat sarakkeet -ongelma kartoissa](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) ohjeita kaksoiskirjoituksen vianmääritysoppaassa.

## <a name="quality-updates"></a>Laatupäivitykset

### <a name="project-operations-on-dataverse"></a>Project Operations Dataversessä

| **Ominaisuusalue** | **Viitenumero** | **Laatupäivitys** |
| --- | --- | --- |
| Laskutus ja hinnoittelu | 2295625 | Välitavoitteen nimi on kopioitava laskuaikataulusta laskurivin tietoihin. |
| Laskutus ja hinnoittelu | 2316323 | Proformalaskussa alennuksen ei pitäisi olla muokattavissa Project Operationsin resurssipohjaisissa skenaarioissa. |
|   Mahdollisuuksien hallinta | 2338619 | **Mahdollisuus** ja **Tarjous**-liiketoimintasäännöt saa käynnistää vain sivuilla. |
| Resurssien hallinta | 2316523 | Kun käytetään **Lähetä pyyntö** -kohdetta resurssivaatimuksesta, jossa on liitetty rooli, ei pitäisi tulla virhettä. |
| Resurssien hallinta | 2326885 | Jos luot resurssivaatimuksen projektin kautta, projektin ei tulisi näyttää virhettä. |
| Aika ja kulut | 2335584 | Vanhentuneet tehtävätyönkulut aikamerkinnässä. |
| Aika ja kulut | 2336884 | **Kopioi viikko** -aikamerkintäpainikkeen on toimittava laajemmin kuin vain nykyiselle käyttäjälle. |


### <a name="project-management-and-accounting-on-dynamics-365-finance"></a>Dynamics 365 Financen projektinhallinta ja kirjanpito

| Ominaisuusalue | Viitenumero | Laatupäivitys |
| --- | --- | --- |
| Matka ja kulut | [4618082](https://fix.lcs.dynamics.com/Issue/Details?kb=4618082&amp;bugId=583101&amp;dbType=3&amp;qc=9c85ac8ca1e5e9cd07fac9e9aa2cb0914724e28b86ad3339dacf7741f554c605) | Virheelliset toimittajan tapahtumien ja arvonlisäveron tapahtumien määrät kirjataan, kun kulu luodaan luottokorttitapahtumasta. |
| Matka ja kulut | [4620366](https://fix.lcs.dynamics.com/Issue/Details?kb=4620366&amp;bugId=579485&amp;dbType=3&amp;qc=e864789bd95505ea624c537d585bf113c2de60b97c88439d44693dbd85aa8e92) | Väärät selvitykset ovat rivejä, jotka luodaan, kun maksukirjauskansio luodaan. |
| Matka ja kulut | [4618082](https://fix.lcs.dynamics.com/Issue/Details?kb=4618082&amp;bugId=583101&amp;dbType=3&amp;qc=9c85ac8ca1e5e9cd07fac9e9aa2cb0914724e28b86ad3339dacf7741f554c605) | Virheelliset arvonlisäveron tapahtumien määrät kirjataan, kun kulu luodaan luottokorttitapahtumasta. |
| Matka ja kulut | [4621765](https://fix.lcs.dynamics.com/Issue/Details?kb=4621765&amp;bugId=587306&amp;dbType=3&amp;qc=6fbfad0123d4e95eaf8d5a5a2f6c354577c991b7905c852ab02d1f94e728a876) | Kulurivin poistaminen voi kestää kauan. |
| Projektin kirjanpito | [4623737](https://fix.lcs.dynamics.com/Issue/Details?kb=4623737&amp;bugId=598109&amp;dbType=3&amp;qc=4101fc5865201e21815299f2ff11ae46d5d5370510868df86c25ee09a8ca1a0c) | Järjestelmä ei tue numeroiden jatkuvan jaksotuksen määrittämistä, kun kirjaat arvion sen jälkeen, kun tietokanta 4619395 on käytetty. |
| Projektin kirjanpito | [4623332](https://fix.lcs.dynamics.com/Issue/Details?kb=4623332&amp;bugId=586034&amp;dbType=3&amp;qc=2f64bb1977c4a9c9dd2ce9de7e72230b86eca14b6295c5bbfb614ea97ad81caf) | Toimittajan laskun kirjaus voi epäonnistua ja näyttöön voi tulla seuraava virhesanoma: "Tositteen tapahtumat eivät täsmää päivämäärällä 17.5.2021. (kirjanpitovaluutta: 0,00 – raportointivaluutta: 0,01)" |
