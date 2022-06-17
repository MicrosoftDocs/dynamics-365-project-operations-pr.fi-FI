---
title: Tapahtumaluokan käyttäminen hinnoitteludimensiona
description: Tässä artikkelissa on tietoja tapahtumaluokan käyttämisestä hinnoitteludimensiona.
author: rumant
ms.date: 11/05/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 648933299616a683b19bbe2f1231caac779bd1f8
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8911690"
---
# <a name="use-transaction-category-as-a-pricing-dimension"></a>Tapahtumaluokan käyttäminen hinnoitteludimensiona


_**Koskee:** Project Operationsin resurssiin / muuhun kuin resurssiin perustuvia skenaarioita, Lite-käyttöönotto-kaupasta proformalaskutukseen_


Tässä artikkelissa käsitellään **Tapahtumaluokka**-kentän käyttämistä hinnoitteludimensiona. 

## <a name="prerequisites"></a>edellytykset
Organisaatiolla on oltava uusi hinnoitteludimensioratkaisu, ennen tässä artikkelissa käsiteltyjen toimintosarjojen suorittamista. Jos et ole vielä luonut sellaista, katso kohtaa [Mukautettujen kenttien ja entiteettien luominen hinnoitteludimensioina](create-custom-fields-entities-pricing-dimensions.md).

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