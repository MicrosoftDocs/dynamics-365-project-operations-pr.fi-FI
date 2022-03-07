---
title: Varattavissa olevan resurssin käyttäminen hinnoitteludimensiona
description: Tässä aiheessa on tietoja varattavissa olevan resurssin käyttämisestä hinnoitteludimensiona.
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
ms.openlocfilehash: c551673708ae2d965979136e92326be98252304a601964c1fbc52a329c592712
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/06/2021
ms.locfileid: "6988962"
---
# <a name="use-bookable-resource-as-a-pricing-dimension"></a>Varattavissa olevan resurssin käyttäminen hinnoitteludimensiona

[!include [banner](../includes/psa-now-project-operations.md)]

Tässä aiheessa on tietoja varattavissa olevan resurssin käyttämisestä hinnoitteludimensiona. Ennen kuin aloitat, jos et ole vielä luonut hinnoitteludimensioratkaisua, sinun on luotava uusi. Jos sinulla on jo hinnoitteludimensioratkaisu, voit tehdä siihen muutoksia. Jos et ole luonut organisaatiolle uutta hinnoitteludimensioratkaisua, suorita toimintosarjat aiheessa [Luo mukautettuja kenttiä ja entiteettejä](create-custom-fields-entities.md).

## <a name="add-bookable-resource-to-forms-and-views"></a>Varattavissa olevan resurssin lisääminen lomakkeisiin ja näkymiin
Jos haluat tehdä kentistä näkyvän hinnoitteludimensioratkaisun käyttöliittymässä, sinun täytyy käydä läpi kaikki lomakkeet ja näkymät keskeisissä Project Service -entiteeteissä ja lisätä nämä kentät lomakkeisiin ja näkymiin kyseisissä entiteeteissä.
Seuraavassa luettelossa esitetään kattava entiteettiperusteinen luettelo niistä valmiina olevista lomakkeista ja näkymistä, jotka on päivitettävä. Jos olet mukauttanut näitä entiteettejä uusilla näkymillä tai lomakkeilla, lisää uudet kentät myös niihin.
Avaa hinnoitteludimensioratkaisun Ratkaisunhallinta ja napsauta **Julkaise kaikki mukautukset**.


|   Entiteetti        | Lomakkeet   |Näkymät        |
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

## <a name="set-up-bookable-resource-as-a-pricing-dimension"></a>Varattavissa olevan resurssin määritys hinnoitteludimensiona

1. Siirry verkkokäyttöliittymässä kohtaan **Project Service** > **Asetukset** > **Parametrit**. Huomaa **Parametrit**-sivun **Summaperusteiset hinnoitteludimensiot** -välilehdellä, että välilehden ruudukko näyttää Hinnoitteludimensiot-entiteetin tietueet. 
2. Lisää **varattavissa oleva resurssi** tähän hinnoitteludimensioiden listaan muodossa **msdyn_bookableresource**. 
3. Määritä yhteys, jossa varattavissa oleva resurssi toimii hinnoitteludimensiona, ja määritä arvot **Sovelletaan kustannuksiin** ja **Sovelletaan myyntiin**.
4. Valitse **Dimensiotyyppi**-kentässä **Summaperusteinen**. 
5. Valitse varattavissa olevan resurssin kustannus- ja myyntiprioriteetti. Yleensä hinnoitteludimensioksi lisätyllä varattavissa olevalla resurssilla on korkein prioriteetti, joten prioriteetin määrittäminen arvoksi **1** (tai **0** riippuen prioriteetin laskemistavasta) varmistaa tämän toimintatavan.

## <a name="set-up-pricing-dimension-field-names"></a>Hinnoitteludimension kenttien nimien määritys

Kun **Roolin hinta** -taulukossa olevan hinnoitteludimension kentän nimi eroaa sen kentän nimestä jossakin muussa entiteetissä, jossa oletushintojen määrityksen on toimittava, hinnoitteludimension tietue on päivitettävä ottamaan huomioon tämä ero nimissä.    
Varattavissa olevan resurssin **Projektiryhmän jäsenet** -entiteetin kentän nimi (**msdyn_bookableresourceid**) eroaa sen nimestä **Roolin hinta** -entiteetissä (**msdyn_bookableresource**). **msydn_bookableresource**-kentän hinnoitteludimensiotietue on päivitettävä ottamaan tämä huomioon. 
1. Tämä tehdään kaksoisnapsauttamalla riviä **Pricing Dimensions**-ruudukossa, jotta **msdyn_bookableresource**-kentän dimensiosivu aukeaa.
2. Napsauta **Liittyvät**-välilehdellä **Hinnoitteludimension kenttien nimet**.

 ![Hinnoitteludimension kenttien nimet.](media/PD-fieldname.png)

4. Napsauta aukeavassa näkymässä **Lisää uusi hinnoitteludimension kentän nimi**.

 ![Uusien hinnoitteludimension kentän nimien lisääminen.](media/Add-NewPD-fieldname.png)


Näkyviin tulee **msdyn_bookableresource**-kentän **Uusi hinnoitteludimension kentän nimi** -sivu 

5. Lisää **msdyn_projectteam** kenttään **Entiteetin looginen nimi** ja **msdyn_bookableresourceid** kenttään **Kentän nimi**. Tallenna tietue.

 ![Uuden hinnoitteludimension kentän nimen lomake.](media/PD-fieldname-Added.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]