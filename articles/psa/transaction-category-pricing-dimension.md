---
title: Käytä tapahtumaluokkaa hinnoitteludimensiona
description: Tässä artikkelissa on tietoja tapahtumaluokan käyttämisestä hinnoitteludimensiona.
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
ms.openlocfilehash: 1a1c2dc17c2092e5364d90e7efc1f13aee80703e
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8915732"
---
# <a name="use-transaction-category-as-a-pricing-dimension"></a>Käytä tapahtumaluokkaa hinnoitteludimensiona

[!include [banner](../includes/psa-now-project-operations.md)]

Tässä artikkelissa käsitellään tapahtumaluokan käyttämisestä hinnoitteludimensiona. Ennen kuin aloitat, jos et ole vielä luonut hinnoitteludimensioratkaisua, sinun on luotava uusi. Jos sinulla on jo hinnoitteludimensioratkaisu, voit tehdä siihen muutoksia. Jos et ole luonut organisaatiolle uutta hinnoitteludimensioratkaisua, suorita artikkelin [Mukautettujen kenttien ja entiteettien luominen](create-custom-fields-entities.md) toimintosarjat.

## <a name="add-transaction-category-to-forms-and-views"></a>Lisää tapahtumaluokka lomakkeisiin ja näkymiin
Jos haluat tehdä tapahtumaluokasta näkyvän hinnoitteludimensioratkaisun käyttöliittymässä, sinun täytyy käydä läpi kaikki lomakkeet ja näkymät avainentiteeteissä ja lisätä nämä kentät lomakkeisiin ja näkymiin kyseisissä entiteeteissä.
Seuraavassa taulukossa on kattava luettelo niistä valmiina olevista lomakkeista ja näkymistä lueteltuina entiteetin mukaan, jotka tulee päivittää uusilla kentillä. Jos olet mukauttanut näitä entiteettejä uusilla näkymillä tai lomakkeilla, lisää uudet kentät myös niihin.

|  Entiteetti        | Lomakkeet     |Näkymät        |
| ------------------------------|---------------------------------|----------------------------------|
|  Roolin hinta|• Tiedot |• Aktiiviset resurssiluokan hinnat<br> • Resurssiluokan hintojen liitetty näkymä|
|  Roolin hinnankorotus|• Tiedot|• Aktiivisen roolin hinnankorotukset<br>• Roolin hinnankorotuksen liitetty näkymä|
|  Tarjousrivin tiedot|• Projektin tiedot<br>• Projektin pikaluonti|• Aktiiviset tarjousrivin tiedot<br>• Yhdistetyt tarjousrivin tiedot<br>• Tarjousrivin tietojen liitetty näkymä|
|  Projektin sopimusrivin tiedot|• Projektin tiedot<br>• Projektin pikaluonti|• Yhdistetyt sopimusrivin tiedot<br>• Aktiiviset sopimusrivin tiedot<br>• Sopimusrivien yksityiskohtien liitetty näkymä|
|  Projektin tehtävä|• Tiedot<br>• Uusi lomake||
|  Projektiryhmän jäsen|• Tiedot<br>• Uusi lomake|• Aktiiviset projektiryhmän jäsenet<br>• Projektiryhmän jäsenet<br>• Projektiryhmän jäsenten liitetty näkymä|
|  Aikamerkintä|• Tiedot<br>• Luo aikamerkintä|• Omat aikamerkinnät päivämäärän mukaan<br>• Omat aikamerkinnät tällä viikolla<br>• Aikamerkinnät hyväksyttäväksi|
|  Kirjauskansion rivi|• Tiedot<br>• Pikaluonti|• Aktiiviset kirjauskansion rivit<br>• Kirjauskansion rivin liitetty näkymä|
|  Laskurivin tiedot|• Tiedot<br>• Pikaluonti|• Aktiiviset laskurivin tiedot<br>• Laskun veloitettavat tapahtumat<br>• Laskun ilmaiset tapahtumat<br>• Laskurivin tietojen liitetty näkymä<br>• Laskun ei-veloitettavat tapahtumat|
|  Todellinen|• Tiedot<br>• Aktiiviset todelliset arvot|• Todellisten arvojen liitetty näkymä|

## <a name="set-up-transaction-category-as-a-pricing-dimension"></a>Aseta tapahtumaluokka hinnoitteludimensioksi

1. Siirry verkkokäyttöliittymässä kohtaan **Project Service** > **Asetukset** > **Parametrit**. 
2. Huomaa **Parametrit**-sivun **Summaperusteiset hinnoitteludimensiot** -välilehdellä, että välilehden ruudukko näyttää **Hinnoitteludimensiot** -entiteetin tietueet.
3. Lisää tähän luetteloon **Tapahtumaluokka** ja aseta **Sovelletaan kustannuksiin** ja **Sovelletaan myyntiin** -kenttien arvoksi **Kyllä**.
4. Valitse **Dimensiotyyppi**-kentässä **Summaperusteinen**, ja valitse sitten **Tapahtumaluokan** prioriteetti kustannuksiin ja myynteihin liittyen.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
