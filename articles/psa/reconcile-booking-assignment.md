---
title: Täsmäytä varaukset ja tehtävät
description: Tässä aiheessa on tietoja nykyarvoista.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 11/27/2019
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 9528bd983e6e18197138f0720abccdc6d6fa1ed5
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/10/2021
ms.locfileid: "5147919"
---
# <a name="reconcile-bookings-and-assignments"></a>Täsmäytä varaukset ja tehtävät

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Projektiryhmän jäsenen projektivaraukset ja projektitehtävien kohdennukset on kytketty löyhästi. Siksi resurssilla voi olla tehtäväkohdennuksia, jotka eivät vastaa varauksia ja varauksia, jotka eivät vastaa tehtäväkohdennuksia. Ihannetapauksessa projektivaraukset ja kohdennukset ovat samoja, jotta resurssit ovat sitoutuneet suorittamaan kohdennettuja tehtäviään. Tosiasia on kuitenkin se, että varaukset voivat tapahtua saatavuuden mukaan, ja tehtävien ajoitus voi muuttua, kun projekti kulkee elinkaarensa läpi. Siksi löyhä kytkös mahdollistaa joustavuuden.

Löyhän kytkennän ansiosta projektivarausten ja tehtävien kohdennuksen välillä **Täsmäytys** -välilehti sisältyy Projekti-entiteettiin. Tämän välilehden avulla projektipäälliköt voivat täsmäyttää ryhmänsä jäsenten varaukset ja kohdennukset.

Kunkin nimetyn ryhmän jäsenen **Täsmäytys**-välilehti näyttää varaukset ja kohdennukset yksittäisten tehtävien kohdennuksiin asti. Se näyttää tunnit soluissa, jotka voivat edustaa aikajaksoja kuukausista päiviin asti.

Voit valita **Aikajana**-kentässä **Kuukauden**, **Viikon** tai **Päivän**. Oletusarvoisesti **Viikko** on valittuna. Voit kuitenkin muuttaa oletusarvoa valitsemalla **Asetukset**-painikkeen. Kun **Täsmäytys**-välilehti avautuu, se näyttää kuluvan päivän päivämäärän, mutta kalenteriohjausobjektin avulla voit siirtyä ajassa eteenpäin tai taaksepäin. Kun projektin alkamispäivä on tulevaisuudessa, välilehdellä näkyy avattaessa kyseinen päivämäärä. Kalenteriohjausobjektissa on myös vaihtoehtoja, joiden avulla voit siirtyä projektin alkamis- ja päättymispäivään.

Voit käyttää laajennusohjausobjekteja jokaisessa resurssissa näyttämään resurssin varausten tiedot. Voit myös laajentaa kunkin resurssin kohdennukset yksittäisen tehtävän tasolle.

**Täsmäytys**-välilehden alaosassa näkyy projektin kokonaissumma, ja välilehdellä on myös summasarake. Välilehti näyttää eron kunkin resurssin varausten ja tämän projektiryhmän jäsenen kohdennettujen tehtävien välillä projektissa. Ihannetapauksessa eron pitäisi olla 0 (nolla). Resurssin varausten ja sen kohdennettujen tehtävien välillä ei siis pitäisi olla eroa. Mahdolliset erot ilmaistaan väreillä ja sävytyksellä, jotta voidaan osoittaa kaksi tilannetta:

- **Varauspula** – varauspulaa tapahtuu, kun resurssilla on enemmän kohdennuksia kuin varauksia. Koska tätä kapasiteettia ei ole varattu, projektipäällikkö voi korjata tämän tilanteen laajentamalla resurssin varauksia kattamaan puutteen.
- **Ylimääräiset varaukset** – ylimääräisiä varauksia tapahtuu, kun resurssi on kirjattu projektiin, mutta sitä ei ole kohdennettu tehtäviin. Tämä tilanne voi olla hyväksyttävä, jos resurssi on esimerkiksi varattu ennen tehtävän kohdennuksen tekemistä. Muissa tapauksissa resurssia ei kuitenkaan ehkä ole tarkoitus kohdentaa. Näissä tapauksissa projektipäällikön tulisi harkita resurssin varausten peruuttamista, jotta kapasiteettia voidaan käyttää toisessa projektissa.

> [!NOTE]
> Näiden tilanteiden selite on ehkä piilotettu, jotta ruudukolle jäisi enemmän tilaa. Tällöin voit tuoda selitteen näkyviin valitsemalla **Asetukset**-painikkeen.

Joissakin tapauksissa, kun **Aikajana**-kenttä on asetettu korkeammalle tasolle kuin **Päivä**, erojen arvoksi voi olla laskettu 0 (nolla). Esimerkiksi **Kuukauden** tasolla resurssin nettoero voi olla 0 (nolla), joka osoittaa, että varaukset ovat yhtä suuria kuin kohdennukset. Kuintenkin **Viikko**-tason tarkastelussa voidaan nähdä, että kohdennuksia on 0 (nolla) tuntia, ja varauksia 40 tuntia kuukauden ensimmäisellä viikolla, ja 40 tuntia kohdennuksia ja 0 (nolla) tuntia varauksia kuukauden toisella viikolla. Vaikka kuukauden varaukset ja kohdennukset ovat samat, ne eroavat viikon mukaan.

Korkeammilla aikatasoilla tarkasteltaessa **Tasmäytys**-välilehti näyttää soluilmaisimen, joka ilmoittaa, että alemmilla aikatasoilla on eroja. Esimerkiksi seuraavassa kuvassa solun ilmaisin näkyy 2018 lokakuun solussa resurssille nimeltä Liisa Järvinen. Siten on nähtävissä, että vaikka resurssin varaukset ja kohdennukset ovat yhtä suuria, kun ne kootaan **Kuukauden** tasolla, ne eivät täsmää alemmilla tasoilla.

![Varaukset ja tehtävät eivät täsmää kuukausitasolla](media/reconcile-assignments-01.JPG)

Kaksoisnapsauttamalla solua voit lähentää seuraavalle alemmalle tasolle ja tarkastella eroa. Esimerkiksi jos kaksoisnapsautat lokakuun 2018 eroa Liisa Järviselle, poraudut alas **Viikko**-tasolle. Tämän jälkeen on nähtävissä, että resurssilla on 16 tuntia varauksia mutta ei kohdennuksia lokakuun kahden ensimmäisen viikon aikana ja 16 tuntia kohdennuksia, mutta ei varauksia lokakuun kolmannella viikolla.

![Varaukset ja tehtävät eivät täsmää viikkotasolla](media/reconcile-assignments-02.JPG)

Voit loitontaa seuraavaa ylemmälle tasolle napsauttamalla solua hiiren kakkospainikkeella. Voit myös poistaa solun ilmaisimen käytöstä valitsemalla **Asetukset**-painikkeen. 

Voit myös käyttää **Edellinen**- ja **Seuraava**-painiketta ruudukon yläpuolella selataksesi projektisi mahdollisia eroja. Jos haluat käyttää näitä painikkeita, valitse ensin resurssi. Valitse **Seuraava** siirtyäksesi seuraavaan eroon varausten ja kohdennusten välillä tälle resurssille. Valitse **Edellinen** siirtyäksesi edelliseen eroon.

Tilanteissa, joissa resurssille on kohdennuksia mutta ei varauksia, voit valita varauksen puutteen ja valita sitten **Laajenna varausta**. Tämän jälkeen näkyviin tulee varaus, joka tarvitaan resurssin puutteen korjaamiseksi. Voit myös tarkastella resurssin varauksia nykyisessä projektissa ja muissa projekteissa. Valitse **OK**, jos haluat luoda resurssille varauksen ottamatta huomioon sen nykyistä saatavuutta. Projektipäällikkö tai resurssipäällikkö voi sitten käyttää aikataulutustaulua hallitakseen tilanteita, joissa resurssin varaukset ylittävät kapasiteetin, koska sen varauksia on laajennettu.

## <a name="managing-with-time-zones"></a>Aikavyöhykkeiden hallinta
Jotta voidaan varmistaa tarkat ja ennakoitavat tulokset, kun käytetään Laajenna varausta -toimintoa, on kaksi tärkeää edellytystä, jotka on täytettävä:  

- Käyttäjän on määritettävä laitteen aikavyöhyke vastaamaan järjestelmän mukautusasetuksissa määritettyä aikavyöhykettä.
 
  ![Aikavyöhykeasetukset Windows 10:ssä](media/reconcile-assignments-03.png)

  ![Aikavyöhykeasetukset mukautusasetuksissa](media/reconcile-assignments-04.png)
 
- Varattavissa olevalla resurssilla on oltava vähintään yksi minuutti työaikaa, joka on päällekkäinen pyydetyn laajennuksen määrittämiseen käytettävien tietojen kanssa. Seuraavassa on esimerkiksi tarkistusresurssit, joiden työaika on 9.00–19.00. 

  ![Resurssien muotojen vertailu](media/reconcile-assignments-05.png)

Seuraavassa taulukossa näkyy:

- Projektin kalenterimalli.
- Resurssi A: Tällä resurssilla on sama kalenteri ja se on samassa aikavyöhykkeessä kuin projekti. Varausten alkamisaika on 9.00.
- Resurssi B: Tämä resurssi sijaitsee eri aikavyöhykkeellä kuin projekti, ja resurssi aloittaa klo 7.00 omalla aikavyöhykkeellään. Varaukset alkavat kuitenkin alkaen klo 9.00, koska se on määritysmallin varhaisin alkamisaika.
- Resurssit C ja D: Resurssit sijaitsevat myös eri aikavyöhykkeillä, jotka eroavat toisistaan ja projektista, ja niiden varaukset alkavat aikaisintaan niiden käytettävissä olevan alkamisajan mukaan.

|Entiteetti  |Kalenteri  |
|-|-|
|Projektin kalenterimalli   | ![projektikalenteri](media/reconcile-assignments-06.png) |
|Resurssi A  | ![Resurssin A kalenteri](media/reconcile-assignments-06.png) |
|Resurssi B  |  ![Resurssin B kalenteri](media/reconcile-assignments-07.png) |
|Resurssi C  |  ![Resurssin C kalenteri](media/reconcile-assignments-08.png) |
|Resurssi D  | ![Resurssin D kalenteri](media/reconcile-assignments-09.png)  |
 
Kun siirryt täsmäytysnäkymään, resurssivaraukset ja niihin liittyvät varauspuutteet tulevat näkyviin.
 ![Täsmäytysnäkymä ennen laajentamista](media/reconcile-assignments-10.png)

Kun Laajenna varausta -toiminto on suoritettu jokaisessa resurssissa, varauksia on laajennettu kullekin resurssille. Tämä johtuu siitä, että kunkin resurssin työaika on päällekkäinen tarpeen rajojen kanssa.
 ![Täsmäytysnäkymä varauksen laajentamisen jälkeen](media/reconcile-assignments-11.png) 

Varauksen yksityiskohdissa huomataan kuitenkin eroja varasuten aloitusajoissa. Varaukset alkavat aikaisintaan varauksen rajojen alkamishetkellä ja aikaisintaan resurssin käytettävissä olevana alkamisaikana.
 ![Resurssien uudet varaukset aikataulutaulukossa](media/reconcile-assignments-12.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]