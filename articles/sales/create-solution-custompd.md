---
title: Ratkaisun luominen mukautetuille hinnoitteludimensioille
description: Tässä aiheessa on tietoja mukautettujen hinnoitteludimensioiden luomisesta.
author: Rumant
ms.date: 11/09/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 82593d3d00b008c1922d70c508bc77624aeb46b3
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/14/2022
ms.locfileid: "8601106"
---
# <a name="create-a-solution-for-custom-pricing-dimensions"></a>Ratkaisun luominen mukautetuille hinnoitteludimensioille

 _**Koskee:** Project Operationsin resurssiin / muuhun kuin resurssiin perustuvia skenaarioita, Lite-käyttöönotto-kaupasta proformalaskutukseen_ 

>[!IMPORTANT]
>Kaikkien mukautettujen hinnoitteludimension muutosten on oltava erillisessä ratkaisussa. Tämä tärkeä paras käytäntö tarjoaa joustavuutta, jonka avulla voidaan myöhemmin päivittää tai poistaa muutoksia tarpeen mukaan, auttaa työn uudelleenkäytössä ja helpottaa näiden muutosten siirtämistä toiseen esiintymään. Kun olet tehnyt kaikki tarvittavat muutokset, vie tämä ratkaisu muodossa **Hallittu** ratkaisu ja tuo se sitten muihin esiintymiin, jotta voit käyttää sitä uudelleen.

## <a name="create-a-solution-for-custom-pricing-dimensions"></a>Ratkaisun luominen mukautetuille hinnoitteludimensioille

1.  Valitse **Asetukset** > **Ratkaisut** ja valitse sitten **Uusi**.
2.  Anna ratkaisulle nimeksi *\<your organization name\> hinnoitteludimensiot*.
3. Syötä muut tarvittavat tiedot ja valitse **Tallenna**.

  ![Mukautetun hinnoitteludimensioratkaisun luominen.](./media/Creation-of-custom-pricing-dimension-solution.png)
 
## <a name="add-all-required-entities-and-related-components-to-the-pricing-dimension-solution"></a>Kaikkien tarvittavien entiteettien ja niihin liittyvien komponenttien lisääminen hinnoitteludimensioratkaisuun

Lisää hinnoitteluratkaisuun seuraavat Project Service -entiteetit, jotta voit tehdä hinnoitteluratkaisuun tärkeitä rakennemuutoksia. Kun olet suorittanut tämän toiminpiteen, entiteetit tunnistavat uudet hinnoitteludimensiot.

1.  Valitse **Asetukset** > **Ratkaisut** ja kaksoisnapauta sen jälkeen **<*organisaatiosi nimen*> hinnoitteludimensioita**.
2.  Valitse vasemman siirtymisruudun Ratkaisunhallinnassa **Lisää aiemmin luoto** > **Entiteetit**.
3.  Valitse **Ratkaisun osat** -valintaikkunassa seuraavat entiteetit:
 
   - **Todellinen**
   - **Varattavissa oleva resurssi**
   - **Arviorivi**
   - **Projektin tehtävä**
   - **Laskurivin tiedot**
   - **Kirjauskansion rivi**
   - **Projektin sopimusrivin tiedot**
   - **Projektiryhmän jäsen**
   - **Tarjousrivin tiedot**
   - **Roolin hinnankorotus**
   - **Roolin hinta**
   - **Aikamerkintä**
 
   ![Aiemmin luotujen entiteettien lisääminen mukautettuun hinnoitteludimensioratkaisuun.](./media/Existing-entities-to-PD-solution.png)
 
 4. Tarkista kunkin entiteetin osalta lisättävät komponentit ja kunkin yhteisön lopullinen resurssiluettelo. 

   >[!NOTE]
   > Lisää kaikkien valittujen entiteettien kaikki lomakkeet ja näkymät.

  ![Lisätyt entiteetit.](./media/solution-component-selection.png)


5.  Kun sinua pyydetään sisällytämään valituista entiteeteistä riippuvaisia entiteettejä, valitse **Ei, älä sisällytä pakollisia komponentteja.**

    ![Sisältäen riippuvaiset entiteetit.](./media/Do-not-include-required.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]