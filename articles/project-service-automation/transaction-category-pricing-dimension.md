---
title: Käytä tapahtumaluokkaa hinnoitteludimensiona
description: Tässä aiheessa on tietoja tapahtumaluokan käyttämisestä hinnoitteludimensiona.
author: Rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 11/19/2018
ms.topic: article
ms.prod: Project Service
ms.service: business-applications
ms.assetid: 64b81ca7-e2db-4e4a-a202-aae0eb235ffd
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
ms.openlocfilehash: a36e0578b8d77a0ed1ea61134453aa064771760f
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/24/2020
ms.locfileid: "3751245"
---
# <a name="use-transaction-category-as-a-pricing-dimension"></a>Käytä tapahtumaluokkaa hinnoitteludimensiona
Tässä aiheessa kerrotaan tapahtumaluokan käyttämisestä hinnoitteludimensiona. Ennen kuin aloitat, jos et ole vielä luonut hinnoitteludimensioratkaisua, sinun on luotava uusi. Jos sinulla on jo hinnoitteludimensioratkaisu, voit tehdä siihen muutoksia. Jos et ole luonut organisaatiolle uutta hinnoitteludimensioratkaisua, suorita toimintosarjat aiheessa [Luo mukautettuja kenttiä ja entiteettejä](create-custom-fields-entities.md).

## <a name="add-transaction-category-to-forms-and-views"></a>Lisää tapahtumaluokka lomakkeisiin ja näkymiin
Jos haluat tehdä tapahtumaluokasta näkyvän hinnoitteludimensioratkaisun käyttöliittymässä, sinun täytyy käydä läpi kaikki lomakkeet ja näkymät avainentiteeteissä ja lisätä nämä kentät lomakkeisiin ja näkymiin kyseisissä entiteeteissä.
Seuraavassa taulukossa on kattava luettelo niistä valmiina olevista lomakkeista ja näkymistä lueteltuina entiteetin mukaan, jotka tulee päivittää uusilla kentillä. Jos olet mukauttanut näitä entiteettejä uusilla näkymillä tai lomakkeilla, lisää uudet kentät myös niihin.

|  Entiteetti        | Lomakkeet     |Näkymät        |
| ------------------------------|---------------------------------|----------------------------------|
|  Roolin hinta|• Tiedot |• Aktiiviset resurssiluokan hinnat<br> • Resurssiluokan hintojen liitetty näkymä|
|  Roolin hinnankorotus|• Tiedot|• Aktiivisen roolin hinnankorotukset<br>• Roolin hinnankorotuksen liitetty näkymä|
|  Tarjousrivin tiedot|• Projektin tiedot<br>• Projektin pikaluonti|• Aktiiviset tarjousrivin tiedot<br>• Yhdistetyt tarjousrivin tiedot<br>• Tarjousrivin tietojen liitetty näkymä|
|  Projektin sopimusrivin tiedot|• Projektin tiedot<br>• Projektin pikaluonti|• Yhdistetyt sopimusrivin tiedot<br>• Aktiiviset sopimusrivin tiedot<br>• Sopimusrivien yksityiskohtien liitetty näkymä|
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
