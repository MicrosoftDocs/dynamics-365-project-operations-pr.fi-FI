---
title: Tapahtumaluokan käyttäminen hinnoitteludimensiona
description: Tässä aiheessa on tietoja tapahtumaluokan käyttämisestä hinnoitteludimensiona.
author: rumant
ms.date: 11/05/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: d956545e1ad38fb09660f107e085f38d099c2207
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/10/2021
ms.locfileid: "6004437"
---
# <a name="use-transaction-category-as-a-pricing-dimension"></a>Tapahtumaluokan käyttäminen hinnoitteludimensiona


_**Koskee:** Project Operationsin resurssiin / muuhun kuin resurssiin perustuvia skenaarioita, Lite-käyttöönotto-kaupasta proformalaskutukseen_


Tässä aiheessa kerrotaan **Tapahtumaluokka**-kentän käyttämisestä hinnoitteludimensiona. 

## <a name="prerequisites"></a>Edellytykset
Ennen kuin suoritat tämän aiheen kuvailemat toimintosarjat, organisaatiolla on oltava uusi hinnoitteludimensioratkaisu. Jos et ole vielä luonut sellaista, katso kohtaa [Mukautettujen kenttien ja entiteettien luominen hinnoitteludimensioina](create-custom-fields-entities-pricing-dimensions.md).

## <a name="add-the-transaction-category-field-to-forms-and-views"></a>Lisää tapahtumaluokka-kenttä lomakkeisiin ja näkymiin
Jotta **Tapahtumaluokka**-kenttä näkyisi hinnoitteludimensioratkaisussa, kenttä on lisättävä kaikkiin lomakkeisiin ja näkymiin entiteettinä.

Seuraavassa taulukossa on luettelo kaikista sisällytetyistä lomakkeista ja näkymistä entiteeteitäin. Uusi kenttä on myös lisättävä mukautettujen entiteettien muihin lomakkeisiin tai näkymiin.

|  Entity        | Lomakkeet     |Näkymät        |
| ------------------------------|---------------------------------|----------------------------------|
|  Roolin hinta| Tietoja |- Aktiiviset resurssiluokan hinnat<br> - Liitetty resurssiluokan hinta |
|  Roolin hinnankorotus| Tietoja|- Aktiivisen roolin hinnankorotus<br>- Liitetty roolin hinnankorotus |
|  Tarjousrivin tiedot|- Projektin tiedot<br>- Projektin pikaluonti| - Aktiivisen tarjousrivin tiedot<br>- Yhdistetyt tarjousrivin tiedot<br>- Liittyvä tarjousrivin tieto |
|  Projektin sopimusrivin tiedot|- Projektin tiedot<br>- Projektin pikaluonti|- Yhdistetyt sopimusrivin tiedot<br>- Aktiivisen sopimusrivin tiedot<br>- Liittyvä sopimusrivin tieto |
|  Projektin tehtävä|- Tiedot<br>- Uusi lomake| &nbsp; |
|  Projektiryhmän jäsen|- Tiedot<br>- Uusi lomake|- Aktiiviset projektiryhmän jäsenet<br>- Projektiryhmän jäsenet<br>- Liitetyt projektiryhmän jäsenet |
|  Aikamerkintä|- Tiedot<br>- Luo aikamerkintä|- Omat aikamerkinnät päivämäärän mukaan<br>- Omat aikamerkinnät tällä viikolla<br>- Hyväksyttävät aikamerkinnät|
|  Kirjauskansion rivi|- Tiedot<br>- Pikaluonti|- Aktiiviset kirjauskansion rivit<br>- Liitetty kirjauskansion rivi|
|  Laskurivin tiedot|- Tiedot<br>- Pikaluonti|- Aktiivisen laskurivin tiedot<br>- Veloitettavat laskutapahtumat<br>- Ilmaiset laskutapahtumat<br>- Liitetty laskurivin tieto <br>- Ei-veloitettavat laskutapahtumat|
|  Todellinen|- Tiedot<br>- Aktiiviset todelliset arvot| Liittyvät todelliset |

## <a name="set-up-the-transaction-category-field-as-a-pricing-dimension"></a>Määritä Tapahtumaluokka-kenttä hinnoitteludimensioksi

1. Siirry kohtaan **Asetukset** > **Parametrit**. 
2. Varmista **Parametrit**-sivun **Määrään perustuvat hinnoitteludimensiot** -välilehdellä, että ruudukko näyttää tietueet **Hinnoitteludimensiot**-entiteetissä.
3. Lisää tähän luetteloon **Tapahtumaluokka** ja aseta **Sovelletaan kustannuksiin** ja **Sovelletaan myyntiin** -kenttien arvoksi **Kyllä**.
4. Valitse **Dimensiotyyppi**-kentässä **Määrään perustuva**, ja valitse sitten **Tapahtumaluokan** prioriteetti kustannuksiin ja myynteihin liittyen.


[!INCLUDE[footer-include](../includes/footer-banner.md)]