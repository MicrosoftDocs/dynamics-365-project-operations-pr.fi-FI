---
title: Mukautettujen ratkaisujen luominen hinnoitteludimensioille
description: Tässä artikkelissa käsitellään mukautetun ratkaisun luontia mukautettuja hinnoitteludimensioita luotaessa.
author: Rumant
ms.custom:
- dyn365-projectservice
ms.date: 10/01/2020
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.reviewer: johnmichalak
ms.openlocfilehash: 0df6728634b169c8a1a128aba1555d79fee5719f
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8929026"
---
# <a name="create-custom-solutions-for-pricing-dimensions"></a>Mukautettujen ratkaisujen luominen hinnoitteludimensioille

[!include [banner](../includes/psa-now-project-operations.md)]

> [!IMPORTANT]
> Kaikkien mukautettujen hinnoitteludimension muutosten on oltava erillisessä ratkaisussa. Tämä tärkeä paras käytäntö varmistaa, että muutoksia voidaan myöhemmin päivittää tai poistaa tarpeen mukaan, auttaa työn uudelleenkäytössä ja helpottaa näiden muutosten siirtämistä toiseen esiintymään. Kun olet tehnyt kaikki tarvittavat muutokset, vie tämä ratkaisu muodossa **Hallittu ratkaisu** ja tuo se muihin esiintymiin, jotta voit käyttää hinnoittelumäärityksiäsi uudelleen.

1. Valitse **Asetukset** > **Ratkaisut** ja valitse sitten **Uusi**. 
2. Anna ratkaisulle nimeksi **organisaation \<your organization name> hinnoitteludimensiot**, anna muut tarvittavat tiedot ja valitse **Tallenna**.

> ![Mukautetun ratkaisun luominen hinnoitteludimensioille.](media/Creation-of-custom-pricing-dimension-solution.PNG)
  
## <a name="add-all-required-entities-and-related-components-to-the-pricing-dimension-solution"></a>Kaikkien tarvittavien entiteettien ja niihin liittyvien komponenttien lisääminen hinnoitteludimensioratkaisuun
Sinun on lisättävä seuraavat Project Service -entiteetit hinnoitteluratkaisuusi. Tämän toimintosarjan vaiheet suorittamalla voit tehdä tärkeitä rakennemuutoksia hinnoitteluratkaisuun, jotta entiteetit ottavat uudet hinnoitteludimensiot huomioon.

1. Valitse **Asetukset** > **Ratkaisut** ja kaksoisnapsauta **\<your organization name> hinnoitteludimensioita**. 
2. Valitse vasemman siirtymisruudun Ratkaisunhallinnassa **Lisää aiemmin luoto** > **Entiteetit**.
3. Valitse **Ratkaisun osat** -valintaikkunassa seuraavat entiteetit:

- Todellinen
- Varattavissa oleva resurssi
- Arviorivi
- Projektin tehtävä
- Laskurivin tiedot
- Kirjauskansion rivi
- Projektin sopimusrivin tiedot
- Projektiryhmän jäsen
- Tarjousrivin tiedot
- Roolin hinnankorotus
- Roolin hinta 
- Aikamerkintä 

> ![Aiemmin luotujen entiteettien lisääminen hinnoitteludimensioratkaisuun.](media/Existing-entities-to-PD-solution.png)

> ![Valitse ratkaisun osat.](media/Dimension-Components.png)

> [!NOTE]
> Varmista, että lisäät kaikkien valittujen entiteettien kaikki lomakkeet ja näkymät.

4. Kun sinua pyydetään lisäämään yllä valituista entiteeteistä riippuvaisia entiteettejä, valitse **Ei**.

> ![Älä lisää kaikkia liittyviä komponentteja.](media/Do-not-include-required.png)




[!INCLUDE[footer-include](../includes/footer-banner.md)]
