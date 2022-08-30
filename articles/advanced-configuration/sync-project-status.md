---
title: Projektin tilan synkronoiminen suljettujen projektien merkinnän estämiseksi
description: Tässä artikkelissa selostetaan, miten projektin tila synkronoidaan, jotta merkintöjä ei voi tehdä passiivisiin tai suljettuihin projekteihin.
author: ryansandnessMSFT
ms.date: 08/09/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ryansandnessMSFT
ms.openlocfilehash: 7a306da164235f36d9ed5e69196508dce6d257de
ms.sourcegitcommit: 6b6c2bfd04e3e613ed1f38355c7cd47c3a56748d
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/24/2022
ms.locfileid: "9348022"
---
# <a name="sync-project-status-to-prevent-entry-against-closed-projects"></a>Projektin tilan synkronoiminen suljettujen projektien merkinnän estämiseksi

_**Käytetään:** Project Operationsin resursseihin ja ei-varastoitaviin perustuvissa skenaarioissa_

## <a name="scenario"></a>Skenaario

Contoso on julkaissut Microsoft Dynamics 365 Project Operationsin resurssi/ei-varastoitu-skenaarioille. Osana normaaleja liiketoiminta-aktiviteetteja projektit voidaan merkitä valmiiksi tai asettaa pitoon. Voit poistaa projektin käytöstä, jos haluat varmistaa, ettei kuluja tai laskuja luoda.

## <a name="solution"></a>Ratkaisu

### <a name="prerequisites"></a>edellytykset

-   Microsoft Dynamics 365 Finance 10.0.29 tai uudempi on oltava asennettuna.
-   Kaksoiskirjoituskartta 1.0.0.3 Projektille V2 (msdyn\_projects) on oltava asennettuna tai manuaalisesti määritettynä alla kuvatulla tavalla.

### <a name="create-an-updated-version-of-the-project-operations-integration-projects-v2-dual-write-map"></a>Luo päivitetty versio Project Operations -integroinnin Projektit V2 -kaksoiskirjoituskartasta

Päivitä Project Operations Projektit V2 -kaksoiskirjoituskartta seuraavasti:

1. Siirry kohtaan **Tiedonhallinta**-työtilassa ja valitse **Kaksoiskirjoitus**.
2. Valitse **Kaksoiskirjoitus**-ruutu
3. T **Taulukon yhdistämismääritys** -sarakkeessa, paikallista ja valitse **Projekti V2 (msdyn\_projects)** ja valitse sitten Pysäytä.
4. Avaa kartta valitsemalla kartan nimi ja valitse sitten **[Ei mitään]**.
5. Valitse Valitse sarake -valintaikkunassa **statecode \[Projektin tila\]** ja valitse sitten OK. Luetteloa voi tarkentaa kirjoittamalla **tila** suodattimen arvoksi.
6.  Muokkaa muunnosta valitsemalla **Lisää muunnos tai muokkaa sitä** **yhdistämismäärityksen tyyppi** -sarakkeessa.
7.  Valitse **Muunnostyyppi**-kentässä **ValueMap**.
8.  Valitse **Lisää arvon yhdistämismääritys** ja lisää sitten seuraavat **avaimet** ja **arvot**:

   Key       | Arvo 
   ----------|-------
   InProcess | 0     
   Valmis | 1     

![Näyttökuvassa kaksoiskirjoituksen yhdistäminen](media/projectstage-dw-mapping.png)

9. Valitse **Tallenna**.
10. Valitse **Kaksoiskirjoitus > Projektit V2 (msdyn_projects)** -sivun yläosassa **Tallenna nimellä**.
11. Valitse **Lisää taulukko** -kohdan **Julkaisija**-kentässä **CDS oletusjulkaisija**.
12. Määritä **Versio**-kentän arvoksi 1.0.0.3.
13. Kirjoita **kuvaus** ja valitse sitten **Tallenna**.
14. Aloita yhdistämismääritys valitsemalla **Kaksoiskirjoitus > Projektit V2 (msdyn_projects)** -sivun yläosassa **Suorita** ja valitse **Kyllä**, jos vahvistusta pyydetään ennen suorittamista. 

### <a name="close-a-newly-completed-project"></a>Äskettäin valmistuneen projektin sulkeminen

Dynamics 365 Finance erottelee **projektin vaihe** -kentän avulla, onko projekti **keskeneräinen** vai **valmis**. **Valmiit** projektit eivät aiheuta kuluja eikä niitä voi laskuttaa asiakkailta.

1. Avaa projekti, jonka aktivoinnin haluat poistaa.
2. Valitse nauhasta **Poista aktivointi**.

> [!NOTE]
> Voit joko poistaa projektin aktivoinnin tai sulkea sen, sillä kumpikin toimii samalla tavalla Finance-yhteydessä.

3. Avaa Financessa **Kaikki projektit** -luettelosivu.
4. Vahvista, että projekti, jonka aktivointi on poistettu, ei näy luettelossa.
5. Muuta arvo **näytä projektit** -suodattimessa luettelon yläpuolella arvosta **Aktiiviset** arvoksi **Kaikki**.
6. Nyt näet projektin, jonka aktivointi on poistettu.

Jos yrität kirjata aikaa tai kuluja tähän projektiin Financeissa, projektia ei pitäisi näkyä valittavana. Jos syötät projektin numeron manuaalisesti kuluun, näet viestin, kuten "Projektin vaihe valmis ei salli projektin tallentamista". Laskutuksen ja muiden laskutustoimintojen on oltava poissa käytöstä, koska ne liittyvät suljettuun projektiin.

