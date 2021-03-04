---
title: Varattavissa olevan resurssin käyttäminen hinnoitteludimensiona
description: Tässä aiheessa on tietoja varattavissa olevan resurssin käyttämisestä hinnoitteludimensiona.
author: Rumant
manager: tfehr
ms.date: 11/18/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: b0c5cb85f7c43f7b2fd9c367d7f7ac9c3250e0a1
ms.sourcegitcommit: 573be7e36604ace82b35e439cfa748aa7c587415
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/25/2020
ms.locfileid: "4643079"
---
# <a name="use-a-bookable-resource-as-a-pricing-dimension"></a>Varattavissa olevan resurssin käyttäminen hinnoitteludimensiona

 _**Koskee:** Project Operationsin resurssiin / muuhun kuin resurssiin perustuvia skenaarioita, Lite-käyttöönotto-kaupasta proformalaskutukseen_ 

Tässä aiheessa on tietoja varattavissa olevan resurssin käyttämisestä hinnoitteludimensiona. Jos hinnoittelustrategiasi on määritetty siten, että kullakin varattavissa olevalla resurssilla on oltava tiettyhinta tai kustannushinta, käytä varattavissa olevaa resurssia hinnoitteludimensiona.

## <a name="prerequisites"></a>Edellytykset
Ennen kuin suoritat tämän aiheen kuvailemat toimintosarjat, organisaatiolla on oltava uusi hinnoitteludimensioratkaisu. Jos et ole vielä luonut sellaista, katso kohtaa [Mukautettujen kenttien ja entiteettien luominen](../pricing-costing/create-custom-fields-entities-pricing-dimensions.md).

## <a name="add-the-bookable-resource-field-to-forms-and-views"></a>Varattavissa olevan resurssin kentän lisääminen lomakkeisiin ja näkymiin
Jotta **Varattavissa oleva resurssi** -kenttä näkyisi hinnoitteludimensioratkaisussa, kenttä on lisättävä kaikkiin lomakkeisiin ja näkymiin entiteettinä.

Seuraavassa taulukossa on luettelo kaikista sisällytetyistä lomakkeista ja näkymistä entiteeteitäin. Uusi kenttä on myös lisättävä mukautettujen entiteettien muihin lomakkeisiin tai näkymiin.

|   Entity        | Lomakkeet   |Näkymät        |
| ------------------------------|---------------------------------|----------------------------------|
|  Roolin hinta| Tietoja | - Aktiiviset resurssiluokan hinnat<br> - Liitetty resurssiluokan hinta |
|  Roolin hinnankorotus| Tietoja| - Aktiivisen roolin hinnankorotus<br>- Liitetty roolin hinnankorotus |
|  Tarjousrivin tiedot| - Projektin tiedot<br>- Projektin pikaluonti| - Aktiivisen tarjousrivin tiedot<br>- Yhdistetyt tarjousrivin tiedot<br>- Liittyvä tarjousrivin tieto |
|  Projektin sopimusrivin tiedot| - Projektin tiedot<br>- Projektin pikaluonti| - Yhdistetyt sopimusrivin tiedot<br>- Aktiivisen sopimusrivin tiedot<br>- Liittyvä sopimusrivin tieto |
|  Projektin tehtävä| - Tiedot<br>- Uusi lomake| &nbsp; |
|  Projektiryhmän jäsen| - Tiedot<br>- Uusi lomake| - Aktiiviset projektiryhmän jäsenet<br>- Projektiryhmän jäsenet<br>- Liitetyt projektiryhmän jäsenet |
|  Aikamerkintä| - Tiedot<br>- Luo aikamerkintä| - Omat aikamerkinnät päivämäärän mukaan<br>- Omat aikamerkinnät tällä viikolla<br>- Hyväksyttävät aikamerkinnät|
|  Kirjauskansion rivi| - Tiedot<br>- Pikaluonti| - Aktiiviset kirjauskansion rivit<br>- Liitetty kirjauskansion rivi |
|  Laskurivin tiedot| - Tiedot<br>- Pikaluonti| - Aktiivisen laskurivin tiedot<br>- Veloitettavat laskutapahtumat<br>- Ilmaiset laskutapahtumat<br>- Liitetty laskurivin tieto <br>- Ei-veloitettavat laskutapahtumat|
|  Todellinen| - Tiedot<br>- Aktiiviset todelliset arvot| Liittyvät todelliset |

## <a name="set-up-a-bookable-resource-as-a-pricing-dimension"></a>Varattavissa olevan resurssin määritys hinnoitteludimensiona
Määritä varattavissa oleva resurssi hinnoitteludimensioksi suorittamalla seuraavat vaiheet:

1. Siirry kohtaan **Asetukset** > **Parametrit**. 
2. Varmista **Parametri**-sivun **Määrään perustuvat hinnoitteludimensiot** -välilehdellä, että ruudukko näyttää tietueet **Hinnoitteludimensiot**-entiteetissä. 
2. Lisää **varattavissa oleva resurssi** tähän hinnoitteludimensioiden listaan muodossa **msdyn_bookableresource**. 
3. Valitse arvo kohdissa **Sovelletaan kustannuksiin** ja **Sovelletaan myynteihin**.
4. Valitse **Dimensiotyyppi**-kohdassa **Määrään perustuva**. 
5. Valitse varattavissa olevan resurssin kustannus- ja myyntiprioriteetti. Yleensä varattavissa olevan resurssin prioriteetti on suurin, kun se sisällytetään hinnoitteludimensioon. Määritä prioriteetin arvoksi **1** (tai **0** riippuen siitä, kuinka lasket prioriteetin) tämän toiminnallisuuden varmistamiseksi.

## <a name="set-up-pricing-dimension-field-names"></a>Hinnoitteludimension kenttien nimien määritys

Kun **Roolin hinta** -taulukossa olevan hinnoitteludimension kentän nimi eroaa sen kentän nimestä jossakin muussa entiteetissä, jossa oletushintaa käytetään, hinnoitteludimensiotietueelle on ilmoitettava nimien eroista.  

Varattavissa olevan resurssin **Projektiryhmän jäsenet** -entiteetillä on hieman eri nimi kuin **Roolihinta**-entiteetissä: 

 - **Projektiryhmän jäsenet** -entiteetti = **msdyn_bookableresourceid**
 - **Roolihinta**-entiteetti = **msdyn_bookableresource**

Hinnoitteludimensiotietueelle koskien kohdetta **msydn_bookableresource** on ilmoitettava tästä erosta.

1. Kaksoisnapauta riviä **Hinnoitteludimensiot**-ruudukossa avataksesi dimensiosivun kohteelle **msdyn_bookableresource**.
2. Valitse dimensiosivun **Liittyvät**-välilehdellä **Hinnoitteludimension kenttänimet**.

  ![Hinnoitteludimension kenttien nimet](media/PD-fieldname.png)

3. Valitse aukeavassa näkymässä **Lisää uusi hinnoitteludimension kentän nimi**.

  ![Uusien hinnoitteludimension kentän nimien lisääminen](media/Add-NewPD-fieldname.png)

  Näkyviin tulee **msdyn_bookableresource**-kentän **Uusi hinnoitteludimension kentän nimi** -sivu 

4. Lisää **Uusi hinnoitteludimension kentän nimi** -sivulla **msdyn_projectteam** kohtaan **Entiteetin looginen nimi**.
5. Lisää **msdyn_bookableresourceid** **Kentän nimeen**.

 ![Uuden hinnoitteludimension kentän nimen lomake](media/PD-fieldname-Added.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]