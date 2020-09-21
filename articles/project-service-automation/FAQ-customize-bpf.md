---
title: Miten voin mukauttaa Projektin vaiheet -liiketoimintaprosessin?
description: Yleiskatsaus Projektin vaiheet -liiketoimintaprosessin mukauttamiseen.
manager: kfend
ms.service: business-applications
ms.custom:
- dyn365-projectservice
ms.date: 10/11/2018
ms.topic: article
ms.prod: ''
ms.technology: Dynamics 365 Project Service Automation 3.x
author: JohnPBurrows
ms.assetid: 36f7df9e-117d-4f85-af4b-d842e93321bd
ms.author: john.burrows
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: d4b99f67e929ebcd1a684bcd1124756140107d17
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/24/2020
ms.locfileid: "3751130"
---
# <a name="how-do-i-customize-the-project-stages-business-process-flow"></a>Miten voin mukauttaa Projektin vaiheet -liiketoimintaprosessin?
[!INCLUDE[cc-applies-to-psa-app-2-4x-9-0-platform](../includes/cc-applies-to-psa-app-2-4x-9-0-platform.md)]
[!INCLUDE[cc-applies-to-psa-app-1x-8-2-platform](../includes/cc-applies-to-psa-app-1x-8-2-platform.md)]

Project Service -sovelluksen aiemmissa versioissa on rajoitus, jonka vuoksi Projektin vaiheet -liiketoimintaprosessin vaiheiden nimien on vastattava täsmälleen englanninkielisiä nimiä (**Quote**, **Plan**, **Close**). Muussa tapauksessa englanninkielisiin vaiheiden nimiin tukeutuva liiketoimintalogiikka ei toimi odotetulla tavalla. Tämän vuoksi projektilomakkeessa ei ole tuttuja toimintoja, kuten **Vaihda prosessia** tai **Muokkaa prosessia**, eikä liiketoimintaprosessin mukautusta suositella. 

Tämä rajoitus on otettu huomioon versiossa 2.4.5.48 ja sitä uudemmissa versioissa. Tämä artikkeli sisältää ehdotetut ratkaisut sitä varten, että aiempien versioiden oletusliiketoimintaprosessia on mukautettava.  

## <a name="business-logic-requires-an-exact-match-with-english-stage-names"></a>Liiketoimintalogiikkaa varten on annettava englanninkielisten vaiheiden nimien täsmälliset vastineet

Projektin vaiheet -liiketoimintaprosessi sisältää liiketoimintalogiikan, joka ohjaa sovelluksen seuraavaa toimintaa:
- Kun projekti on liitetty tarjoukseen, koodi määrittää liiketoimintaprosessin vaiheeksi **Quote**.
- Kun projekti on liitetty sopimukseen, koodi määrittää liiketoimintaprosessin vaiheeksi **Plan**.
- Kun liiketoimintaprosessi on edennyt **Close**-vaiheeseen, projektitietueen aktivointi poistetaan. Kun projektin aktivointi poistetaan, projektilomake ja työrakenne määritetään Vain luku -tilaan, nimetyt resurssin varaukset vapautetaan ja kaikkien liittyvien hinnastojen aktivoinnit poistetaan.

Tämä liiketoimintalogiikka edellyttää englanninkielisiä nimiä projektin vaiheissa. Riippuvuus englanninkielisistä vaiheiden nimistä on pääsyy sille, miksi Projektin vaiheet -liiketoimintaprosessin mukauttamista ei suositella. Se on syy myös siihen, miksi projektin entiteetissä ei näy yleisiä liiketoimintaprosessien toimintoja, kuten **Vaihda prosessia** tai **Muokkaa prosessia**.

## <a name="what-happens-if-the-stage-names-dont-match-the-english-names"></a>Mitä tapahtuu, jos vaiheiden nimet eivät vastaa englanninkelisiä nimiä?

Jos Project Service -sovelluksen versiossa 1.x ympäristössä 8.2 liiketoimintaprosessin vaiheiden nimet eivät vastaa täysin englanninkielisiä vaiheiden nimiä, liiketoimintalogiikka, joka määrittää tarjousten ja sopimusten oikean vaiheen ja sulkee projektin, ohitetaan. Virhesanomia ei näytetä. Tämän vuoksi vaikuttaa siltä, että Projektin vaiheet -liiketoimintaprosessin mukauttaminen toimii. Automaattiset prosessit eivät kuitenkaan toimi tarjouksissa, sopimuksissa ja projektin sulkemisessa.

Project Service -sovelluksen versiossa 2.4.4.30 tai aiemmassa versiossa ympäristössä 9.0 oli merkittävä arkkitehtuurimuutos liiketoimintaprosesseissa. Muutoksen vuoksi liiketoimintaprosessin liiketoimintalogiikka piti kirjoittaa uudelleen. Jos projektin vaiheiden nimet eivät vastaa odotettuja englanninkielisiä nimiä, virhesanomaa ei näytetä. 

Jos siis haluat mukauttaa projektin entiteetin Projektin vaiheet -liiketoimintaprosessia, voit lisätä vain aivan uusia vaiheita projektin entiteetin oletusliiketoimintaprosessiin. **Quote**-, **Plan**- ja **Close**-vaiheita ei saa muuttaa. Rajoitus varmistaa sen, että liiketoimintaprosessi ei aiheuta virheitä. Liiketoimintaprosessi vaatii englanninkieliset vaiheiden nimet.

Tässä artikkelissa kuvattu liiketoimintalogiikka on poistettu versiossa 2.4.5.48 tai sitä uudemmissa versioissa projektin entiteetin oletusliiketoimintaprosessista. Kun otat käyttöön kyseisen version tai myöhemmän version, voit mukauttaa oletusliiketoimintaprosessia tai korvata sen omalla prosessilla. 

## <a name="workarounds-for-earlier-versions"></a>Aiempien versioiden ratkaisuehdotukset

Jos version päivittäminen ei ole vaihtoehto, voit mukauttaa projektin entiteetin Projektin vaiheet -liiketoimintaprosessin jommallakummalla seuraavista tavoista:

1. Lisää oletusmääritykseen vaiheita samalla, kun säilytät englanninkieliset nimet **Quote**-, **Plan**- ja **Close**-vaiheille.

   > [!div class="mx-imgBorder"] 
   > ![Oletusmäärityksen vaiheiden lisäämisen näyttökuva](media/FAQ-Customize-BPF-1.png)
 
2. Luo oma liiketoimintaprosessi ja tee siitä projektin entiteetin ensisijainen liiketoimintaprosessi. Tällöin voit antaa vaiheille haluamasi nimet. Jos kuitenkin haluat käyttää samoja projektin vakiovaiheita eli **Quote**-, **Plan**- ja **Close**-vaiheita, sinun on tehtävä joitakin mukautuksia, jotka saadaan mukautetuista vaiheiden nimistä. Projektin sulkeminen sisältää monimutkaisempaa logiikkaa. Voit kuitenkin käynnistää sen poistamalla projektitietueen aktivoinnin.

   > [!div class="mx-imgBorder"] 
   > ![Liiketoimintaprosessin mukautuksen näyttökuva](media/FAQ-Customize-BPF-2.png)

### <a name="additional-considerations-for-project-service-app-version-24430-or-earlier-on-platform-90"></a>Erityisiä huomioita Project Service -sovelluksen versiosta 2.4.4.30 tai aiemmista versioista ympäristössä 9.0

Mukautetun liiketoimintaprosessin omaavassa Project Service -versiossa 2.4.4.30 tai aiemmassa versiossa ympäristössä 9.0 projektin entiteetin **Vaiheen nimi** -kenttä, jota käytetään **Projekti vaiheen mukaan** -kaaviossa ja projektiluettelonäkymissä, ei päivity, koska se on yhdistetty Projektin vaiheet -oletusliiketoimintaprosessiin. Tämä ongelma voidaan ratkaista seuraavien vaiheiden avulla:

- Lisää mukautettu kenttä, joka sieppaa nykyisen liiketoimintaprosessin vaiheen, joka päivitetään samalla kun käyttäjä siirtyy mukautetussa liiketoimintaprosessissa.

- Muokkaa **Projekti vaiheen mukaan** kaaviota niin, että sitä voi käyttää mukautetun kentän kanssa oletusmäärityksen sijaan.

### <a name="steps-to-create-your-own-business-process-flow-for-the-project-entity"></a>Vaiheet, joiden avulla luodaan oma liiketoimintaprosessi projektin entiteettiä varten

Voit luoda oman liiketoimintaprosessin projektin entiteettiä varten seuraavasti:

1. Siirry kohtaan **Asetukset** > **Prosessikeskus**. Älä kopioi Projektin vaiheet -liiketoimintaprosessia, koska silloin myös Project Service -sovelluksen liiketoimintalogiikka kopioidaan.

   > [!div class="mx-imgBorder"] 
   > ![Liiketoimintaprosessin mukautuksen näyttökuva](media/FAQ-Customize-BPF-3.png)

2. Luo haluamasi vaiheiden nimet prosessin suunnitteluohjelman avulla. Jos haluat samat toiminnot kuin **Quote**-, **Plan**- ja **Close**-oletusvaiheissa on, luonnin on perustuttava mukautetun liiketoimintaprosessin vaiheiden nimiin.

   > [!div class="mx-imgBorder"] 
   > ![Liiketoimintaprosessin mukautuksessa käytettävän prosessin suunnitteluohjelman näyttökuva](media/FAQ-Customize-BPF-4.png) 

3. Tee mukautetusta liiketoimintaprosessista projektin entiteetin ensisijainen liiketoimintaprosessi valitsemalla prosessin suunnitteluohjelmassa **Prosessin järjestys** -kohta. Siirrä projektin entiteetti Projektin vaiheet -liiketoimintaprosessin yläpuolelle luettelon yläosaan.

   > [!div class="mx-imgBorder"] 
   > ![Prosessin järjestyksen käyttämisen näyttökuva](media/FAQ-Customize-BPF-5-720.png)

### <a name="the-following-steps-apply-to-project-service-app-24430-or-earlier-on-the-90-platform"></a>Seuraavat vaiheet koskevat Project Service -sovelluksen versiota 2.4.4.30 tai aiempaa versiota ympäristössä 9.0

4. Lisää uusi mukautettu kenttä projektin entiteettiin ja sieppaa mukautetut vaiheet mukautettuun liiketoimintaprosessiin. Lisää liiketoimintalogiikka (laajennus/työnkulku) ja päivitä tämä kenttä, kun mukautetun liiketoimintaprosessin vaihe päivitetään.

   > [!div class="mx-imgBorder"] 
   > ![Projektin entiteetin mukautuksen näyttökuva](media/FAQ-Customize-BPF-6-720.png)

5. Muokkaa **Projekti vaiheen mukaan** -kaaviota, kun haluat käyttää vaiheiden uutta mukautettua kenttää.

   > [!div class="mx-imgBorder"] 
   > ![Projekti vaiheen mukaan -kaavion käyttämisen näyttökuva](media/FAQ-Customize-BPF-7-720.png)

6. Muokkaa projektin entiteetin näkymiä ja sisällytä vaiheiden uusi mukautettu kenttä.

   > [!div class="mx-imgBorder"] 
   > ![Projektin entiteetin näkymien muokkaamisen näyttökuva](media/FAQ-Customize-BPF-8-720.png)

