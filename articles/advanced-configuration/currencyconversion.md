---
title: Määritä valuutan muuntaminen myyntihintojen laskemiseksi kustannusprosenteista
description: Tässä artikkelissa selostetaan valuuttamuunnoskäyttäytymistä, jota käytetään Microsoft Dynamics 365 Project Operationsissa, kun myyntitapahtumia luodaan kustannustapahtumista.
author: rumant
ms.date: 11/01/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 3fa8077deb18f1a54e7f0f5e6dc4491a830df45b
ms.sourcegitcommit: 95e52fcf012a51229f3f6ae7dbf7b0fa56072a85
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/01/2022
ms.locfileid: "9816664"
---
# <a name="set-up-currency-conversion-to-calculate-sales-prices-from-cost-rates"></a>Määritä valuutan muuntaminen myyntihintojen laskemiseksi kustannusprosenteista

_**Käytetään:** Project Operationsin resursseihin ja ei-varastoitaviin perustuvissa skenaarioissa_

Microsoft Dynamics 365 Project Operationsissa kululuokkien myyntihinnat voidaan määrittää numeerisiksi arvoiksi, tai ne voidaan määrittää laskettavaksi syntyvien kustannusten perusteella.

Kun ne on määritetty laskettaviksi aiheutuneen kustannuksen perusteella, käytettävissä ovat seuraavat vaihtoehdot:

- Kustannusten mukaan
- Kustannukset ylittävä voitto

Skenaarioissa, joissa kulukustannus aiheutuu valuuttana, joka eroaa projektisopimuksen myyntivaluutasta, valuutan muuntaminen on pakollinen, jotta myyntihinta lasketaan kustannuksen perusteella.

## <a name="currency-conversion-behavior-that-uses-native-dataverse-exchange-rates"></a>Alkuperäisiä Dataverse-valuuttakursseja käyttävä valuutan muuntotapa  

Project Operations käyttää oletusarvoisesti valuuttakursseja, jotka on tallennettu Valuutta-taulukkoon Dataversessa. Jos haluat määrittää Project Operationsin käyttämään alkuperäisiä valuuttakurssit myyntihintojen laskemiseksi kustannuksista, toimi seuraavasti.

1. Siirry kohtaan **Project Operations \> Asetukset \> Parametrit**.
1. Avaa **Projektiparametrit**-tietosivu.
1. Aseta **Valuutan muuntologiikka** -kenttään tyhjä arvo.

## <a name="currency-conversion-behavior-that-uses-exchange-rates-from-finance-and-operations-apps"></a>Valuutan muuntaminen, joka käyttää rahoitus- ja toimintosovellusten valuuttakursseja

Valuuttataulukon valuuttakurssit, jotka ovat alkuperäisessä muodossa käytettävissä Dataversessa, eivät ole voimassa. Siksi niitä ei ehkä aina skaalata vaatimuksiin, joita sinulla on myyntihintojen laskemiseen kustannushinnoista.

Rahoitus- ja toimintaympäristön valuuttakurssien avulla voit laskea myyntivaluutan myyntihinnan kustannusvaluutan kustannusvaluutasta. Voit määrittää valuuttamuunnoskäyttäytymistä seuraavasti.

1. Lisää **Projektiparametrit**-sivulla  **Valuutan muuntologiikka** - kenttä. Tallenna ja julkaise mukautus.
1. Siirry kohtaan **Project Operations \> Asetukset \> Parametrit**.
1. Avaa **Projektiparametrit**-tietosivu. 
1. Määritä **Valuutan muuntotapa** -kentän arvoksi **Laajennettu ja vara-arvoksi oletusarvo**.
1. Anna  **Kaksoiskirjoitussovelluksen käyttävä** -käyttöoikeusroolille **Luku**-oikeus seuraaviin taulukoihin:

    - msdyn\_currencyexchangerates
    - msdyn\_currencyexchangeratepairs
    - msdyn\_exchangeratetypes

1. Suorita rahoitus- ja toimintaympäristössä seuraavat kaksoiskirjauskartat ensimmäisen synkronoinnin yhteydessä:

    - Vaihtokurssin tyyppi (msdyn\_exchangeratetypes)
    - Vaihtokurssin valuuttapari (msdyn\_currencyexchangeratepairs)
    - CDS-vaihtokurssit (msdyn\_currencyexchangerates)

Kun nämä muutokset on tehty, kaksoiskirjoitus saattaa valuuttakurssit rahoitus- ja toimintaympäristöstä käytettäviksi Dataversessä. Tämän jälkeen Project Operations käyttää näitä valuuttakursseja kustannushintojen muuntamiseen sopimuksen myyntivaluutaksi.

> [!NOTE]
> Tämä valuutan muuntotapa koskee vain kustannusprosentin myyntihintojen laskentaa. Sitä ei käytetä perusvaluutan arvojen laskemiseen yleisesti. Perusvaluutan arvot käyttävät alkuperäisiä Dataverse-vaihtokursseja huolimatta siitä, suoritatko tämän menettelyn.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
