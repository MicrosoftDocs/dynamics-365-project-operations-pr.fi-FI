---
title: Määritä alihankkijat varattavissa olevina resursseina
description: Tässä aiheessa selostetaan, miten käyttäjiltä ja yhteyshenkilöitä järjestelmässä luodut alihankkijaresurssit voidaan määrittää ja ylläpitää, jotta ne voidaan liittää Microsoft Dynamics 365 Project Operationsin alihankkijoihin.
author: rumant
ms.date: 07/28/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: c765e3c423e440f092c92f9bab75304914b0609447f1dc1c014f98801561b7a6
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/06/2021
ms.locfileid: "6994182"
---
# <a name="set-up-subcontractors-as-bookable-resources"></a>Määritä alihankkijat varattavissa olevina resursseina

[!include [banner](../../includes/dataverse-preview.md)]

_**Käytetään:** Lite-käyttöönotto – kauppa proformalaskutukseen_

Seuraavien vaiheiden avulla voit määrittää alihankkijat Microsoft Dynamics 365 Project Operationsin varattavissa oleviksi resursseiksi.

1. Siirry kohtaan **Projekti** \> **Resurssit** ja valitse **Uusi**.
2. Valitse **Uusi varattava resurssi** -sivun **Resurssityyppi**-kentässä jokin seuraavista vaihtoehdoista:

    - **Käyttäjä** – Valitse tämä resurssityyppi, jos alihankkijan on käytettävä Project Operationsia ajan tai kulujen lisäämiseen. Jos valitset **Käyttäjä**, alihankkija tarvitsee kelvollisen käyttöoikeuden järjestelmän käyttöön.
    - **Yhteyshenkilö** tai **Asiakas** – Valitse jokin näistä resurssityypeistä, jos alihankkija ei tarvitse Project Operationsin käyttöä, mutta sen on oltava käytettävissä projektien tehtävämäärityksiä tai varauksia varten. Kumpikaan näistä resurssityypeistä ei ole järjestelmän käytettävissä. Valitse **Tili**, jos haluat esittää toimittajan yrityksen varattavissa olevana resurssina. Valitse **Yhteyshenkilö**, jos haluat esittää toimittajan yksittäiset työntekijät.

3. Järjestelmä pyytää valitsemaan vastaavan käyttäjä-, asiakas- tai yhteyshenkilötietueen valitsemasi resurssityypin mukaan.
4. Valitse **Työntekijätyyppi**-kentässä Sopimustyöntekijä, jos haluat määrittää alihankkijan varattavaksi resurssiksi.

    > [!NOTE]
    > Jos jätät **Työntekijätyyppi**-kentän tyhjäksi, varattavissa oleva resurssi katsotaan työntekijäksi.

5. Jos olet valinnut työntekijän tyypiksi **Palvelusopimustyö**, valitse toimittaja, jolle resurssi työskentelee.
6. Valitse resurssin aikavyöhyke ja valitse sitten **Tallenna**. Jos haluat delegoida työtuntimallin varattavissa olevalle resurssille, valitse **Varattavissa oleva resurssi** -luettelosivulta **Määritä kalenteri**.

Jotta varattava resurssi voidaan liittää alihankintariviin, sen on täytettävä seuraavat ehdot:

- Varattavissa olevan resurssin on oltava palvelusopimustyöntekijä.
- **Yhteyshenkilö**-resurssityypin varattavissa oleva resurssi on liityttävä toimittajan tiliin yhteyshenkilönä. **Käyttäjä**-resurssityypin varattavissa olevan resurssin ei tarvitse liittyä toimittajan tiliin yhteyshenkilönä.
- Varattavan resurssin **Toimittaja**-kentän arvon on vastattava alihankkijan **Toimittaja**-kentän arvoa.

## <a name="update-the-type-of-worker-and-vendor-mapping-for-bookable-resources"></a>Varattavissa olevia resursseja varten tarvittavien työntekijän ja toimittajan yhdistämismääritysten tyyppien päivittäminen

Varattavan resurssin **Työntekijätyyppi**-kenttä määrittää, onko varattavissa oleva resurssi sopimustyöntekijä vai työntekijä. **Toimittaja**-kenttä määrittää toimittajatilin, johon varattavissa oleva resurssi liittyy. Liittämällä varattavan resurssin yhteyshenkilönä toimittajaan osoitat, että yhteyshenkilö on toimittajayrityksen työntekijä.

Jos varattavan resurssin **Työntekijätyyppi**- ja **Toimittaja**-kenttiä muutetaan, muutokset vaikuttavat varattavissa olevan resurssin luomien uusien tietueiden, kuten aikamerkintöjen, tuleviin vahvistuksiin. Muutokset eivät kuitenkaan mitätöi olemassa olevia tietueita.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
