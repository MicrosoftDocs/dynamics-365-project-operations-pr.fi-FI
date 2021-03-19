---
title: Pakollisten mukautettujen kenttien lisääminen hintamääritys- ja tapahtumaentiteetteihin
description: Tässä aihessa on tietoja pakollisten mukautettujen kenttien viittausten lisäämisestä entiteettiin sekä lomakkeisiin ja näkymiin.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 66cd638a3726cb68c0e92d3b0b54de28ff94b2a5
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5275759"
---
# <a name="add-required-custom-fields-to-price-setup-and-transactional-entities"></a>Pakollisten mukautettujen kenttien lisääminen hintamääritys- ja tapahtumaentiteetteihin

_**Koskee:** Project Operationsin resurssiin / muuhun kuin resurssiin perustuvia skenaarioita, Lite-käyttöönotto-kaupasta proformalaskutukseen_

Tässä aiheessa oletetaan, että olet suorittanut aiheen [Mukautettujen kenttien ja entiteettien luominen hinnoitteludimensioita varten](create-custom-fields-entities-pricing-dimensions.md) vaiheet. Jos et ole suorittanut näitä toimintosarjoja loppuun, palaa niihin ja suorita ne, ja palaa sen jälkeen tähän aiheeseen. 

Tämän aiheen vaiheet näyttävät, miten vaadittavat mukautettujen kenttien viitteet lisätään entiteetteihin ja käyttöliittymän (UI) elementteihin, kuten lomakkeisiin ja näkymiin.

## <a name="add-custom-pricing-dimension-fields"></a>Mukautettujen hintadimensiokenttien lisääminen 
Kun mukautettuja kenttiä ja entiteettejä on luotu, seuraavana vaiheena on päivittää hinnanmäärittely- ja tapahtumaentiteetit ottamaan huomioon mukautetut entiteetit tai asetusjoukot luomalla viitekenttiä. Riippuen siitä, sisältääkö hinnoitteludimensioiden luettelo asetusjoukkodimensioita vai entiteettidimensioita vai molempia, noudata tilanteen mukaan vain kohdan **Asetusjoukkoperusteiset mukautetut hinnoitteludimensiot** tai kohdan **Entiteettiperusteiset mukautetut hinnoitteludimensiot** tai niiden molempien ohjeita.

### <a name="option-set-based-custom-pricing-dimensions"></a>Asetusjoukkoperusteiset mukautetut hinnoitteludimensiot
Kun mukautettu hinnoitteludimensio perustuu asetusjoukkoon, lisää se kenttänä keskeisiin entiteetteihin. Seuraavassa menettelyssä arvoja **Resurssin työn sijainti** ja **Resurssin työtunnit** käytetään asetusjoukkoperusteisina hinnoitteludimensioina. Ne on ensin lisättävä kenttinä hinnoitteluentiteetteihin ja arvoihin **Roolin hinta** ja **Roolin hinnankorotus**.

1. Valitse projektin toiminnoissa **Asetukset** > **Ratkaisut** ja kaksoisnapsauta **\<your organization name> hinnoitteludimensioita**. 
2. Valitse vasemman siirtymisruudun Ratkaisunhallinnassa **Entiteetit > Roolin hinta**.
3. Laajenna entiteetti **Roolin hinta** ja valitse **Kentät**.
4. Valitse **Uusi** ja luo kenttä nimeltä **Resurssin työn sijainti**. Valitse kentän tyypiksi **Asetusjoukko**. 
5. Valitse **Käytä olemassa olevaa asetusjoukkoa** ja valitse sitten asetusjoukko **Resurssin työn sijainti**. Valitse lopuksi **Tallenna**.
6. Toista vaiheet 1–5 lisätäksesi tämän kentän entiteettiin **Roolin hinnankorotus**. 
7. Toista vaiheet 1–5 **Resurssin työtunnit** -asetusjoukon osalta.

> [!IMPORTANT]
> Kun lisäät kentän useisiin entiteetteihin, käytä niissä kaikissa samaa kentän nimeä. 

> ![Resurssin työn sijainnin lisääminen Roolin hintaan](media/RWL-Field.png)

Projektin myynti- ja arviointivaiheissa arvioita työmäärästä, joka tarvitaan töiden **Paikallinen** ja **Asiakkaan tiloissa** suorittamiseen arvoissa **Tavalliset työtunnit** ja **Ylityötunnit**, käytetään tarjouksen/projektin arvon arviointiin. Kentät **Resurssin työn sijainti** ja **Resurssin työtunnit** lisätään arviointientiteetteihin **Tarjousrivin tiedot**, **Sopimusrivin tiedot**, **Projektiryhmän jäsen** ja **Arviorivi**.

1. Valitse projektin toiminnoissa **Asetukset** > **Ratkaisut** ja kaksoisnapsauta **\<your organization name> hinnoitteludimensioita**. 
2. Valitse vasemman siirtymisruudun Ratkaisunhallinnassa **Entiteetit > Tarjousrivin tiedot**.
3. Laajenna **Tarjousrivin tiedot** -entiteetti ja valitse **Kentät**.
4. Valitse **Uusi** ja luo kenttä nimeltä **Resurssin työn sijainti**. Valitse kentän tyypiksi **Asetusjoukko**. 
5. Valitse **Käytä olemassa olevaa asetusjoukkoa** ja **Resurssin työn sijainti** ja valitse sitten **Tallenna**.
6. Toista vaiheet 1–5 lisätäksesi tämän kentän entiteetteihin **Projektin sopimusrivin tiedot**, **Projektiryhmän jäsen** ja **Arviorivi**.
7. Toista vaiheet 1–6 **Resurssin työtunnit** -asetusjoukon osalta. 

> ![Resurssin työn sijainnin lisääminen Arvioriviin](media/RWL-Default-Value.png)

Toimitusta ja laskutusta varten suoritettu työ on hinnoiteltava oikein, jotta projektin todellisissa arvoissa voidaan valita suoritettiinko se arvolla **Paikallinen** vai **Asiakkaan tiloissa** ja arvolla **Tavalliset työtunnit** vai **Ylityötunnit**. Kentät **Resurssin työn sijainti** ja **Resurssin työtunnit** pitäisi lisätä entiteetteihin **Aikamerkintä**, **Todellinen arvo**, **Laskurivin tiedot** ja **Kirjauskansion rivi**.

1. Valitse **Asetukset** > **Ratkaisut** ja kaksoisnapsauta **\<your organization name> hinnoitteludimensioita**.
2. Valitse vasemman siirtymisruudun Ratkaisunhallinnassa **Entiteetit > Aikamerkintä**.
3. Laajenna **Tarjousrivin tiedot** -entiteetti ja valitse sitten **Kentät**.
4. Valitse **Uusi** ja luo kenttä nimeltä **Resurssin työn sijainti**. Valitse kentän tyypiksi **Asetusjoukko**. 
5. Valitse **Käytä olemassa olevaa asetusjoukkoa** ja valitse sitten asetusjoukko **Resurssin työn sijainti**. Valitse lopuksi **Tallenna**.
6. Toista vaiheet 1–5 lisätäksesi tämän kentän entiteetteihin **Todellinen arvo**, **Laskurivin tiedot** ja **Kirjauskansion rivi**.
7. Toista vaiheet 1–6 **Resurssin työtunnit** -asetusjoukon osalta. 

> ![Resurssin työn sijainnin lisääminen Aikamerkintään](media/RWL-time-entry.png)

Tämä täydentää asetusjoukkoperusteisiin mukautettuihin dimensioihin vaadittavat rakennemuutokset.

## <a name="entity-based-custom-pricing-dimensions"></a>Entiteettiperusteiset mukautetut hinnoitteludimensiot

Kun mukautettu hinnoitteludimensio on entiteetti, lisäät 1:N-suhteita dimensioentiteetin ja keskeisten entiteettien välille. Kun käytetään yllä esitettyä Vakionimike-esimerkkiä on syytä olettaa, että jokaiselle työntekijälle määritetään vakionimike. Tämän surauksena tarvitset 1:N-suhteen Vakionimikkeestä Varattavissa olevaan resurssiin tai N:1-suhteen, jos se luodaan Varattavissa olevasta resurssista Vakionimikkeeseen.

1. Valitse projektin toiminnoissa **Asetukset** > **Ratkaisut** ja kaksoisnapsauta **\<your organization name> hinnoitteludimensioita**. 
2. Valitse vasemman siirtymisruudun Ratkaisunhallinnassa **Entiteetit > Vakionimike**.
3. Laajenna entiteetti **Vakionimike** ja valitse **1:N-suhteet**.
4. Valitse **Uusi** ja luo uusi 1:N-suhde nimellä **Varattavissa olevan resurssin vakio-otsikko**. Syötä tarvittavat tiedot ja valitse **Tallenna**.

> ![Vakionimikkeen lisääminen viitekentäksi Varattavissa olevaan resurssiin](media/ST-BR.png)

Vakionimike on lisättävä myös hinnoitteluentiteetteihin **Roolin hinta** ja **Roolin hinnankorotus**. Tämä toteutetaan myös käyttämällä 1:N-suhteita entiteettien **Vakionimike** ja **Roolihinta** ja entiteettien **Vakionimike** ja **Roolin hinnankorotus** välillä.

1. Valitse vasemman siirtymisruudun Ratkaisunhallinnassa **Entiteetit > Vakionimike**.
2. Laajenna entiteetti **Vakionimike** ja valitse **1:N-suhteet**.
3. Valitse **Uusi** ja luo uusi 1:N-suhde nimellä **Roolin hinnan vakio-otsikko**. Syötä tarvittavat tiedot ja valitse **Tallenna**.
4. Toista vaiheet 1–4 luodaksesi 1:N-suhteita entiteettien **Vakionimike** ja **Roolin hinnankorotus** välille,

Projektin myynti- ja arviointivaiheissa tarjouksen/projektin hinnoittelua varten kullekin vakionimikkeelle tarvitaan arviot työmäärästä. Tämä tarkoittaa, että vakio-otsikosta tarvitaan 1:N-suhteita jokaiseen näistä arviointientiteeteistä: 

- **Tarjousrivin tiedot**
- **Projektin sopimusrivin tiedot**
- **Projektiryhmän jäsen**
- **Arviorivi**

5. Toista vaiheet 1–5 luodaksesi 1:n-suhteita arvosta **Vakionimike** entiteetteihin **Tarjousrivin tiedot**, **Projektin sopimusrivin tiedot**, **Projektiryhmän jäsen** ja **Arviorivi**.

> ![Vakionimikkeen lisääminen viitekentäksi Arvioriviin](media/ST-Estimate-Line.png)

  Toimitus- ja laskutusvaiheissa kunkin vakionimikkeen suorittama työ on hinnoiteltava oikein projektin todellisissa arvoissa. Tämä tarkoittaa, että tarvitaan 1:N-suhteita arvosta **Vakionimike** entiteetteihin **Aikamerkintä**, **Todellinen arvo**, **Laskurivin tiedot** ja **Kirjauskansion rivi**.

6. Toista vaiheet 1–6 luodaksesi 1:N-suhteita arvosta **Vakionimike** entiteetteihin **Aikamerkintä**, **Todellinen arvo**, **Laskurivin tiedot** ja **Kirjauskansion rivi**.

> ![Vakionimikkeen lisääminen viitekentäksi Aikamerkintään](media/ST-Mapping.png)

### <a name="set-up-dimension-value-defaulting-using-the-mappings-features-of-the-platform"></a>Dimension arvon vakioinnin määritys ympäristön yhdistämismääritystoimintojen avulla
Aikamäärityksen osalta olisi hyödyllistä, jos järjestelmä hakee aikamerkinnän vakionimikkeen oletusarvon aikamerkinnän tekevästä varattavissa olevasta resurssista. Noudata seuraavia vaiheita lisätäksesi kenttien yhdistämismäärityksiä 1:N-suhteeseen arvosta **Varattavissa oleva resurssi** arvoon **Aikamerkintä**.

1. Valitse vasemman siirtymisruudun Ratkaisunhallinnassa **Entiteetit > Vakionimike**.
2. Laajenna entiteetti **Vakionimike** ja valitse **1:N-suhteet**.
3. Kaksoisnapsauta **Varattavissa olevasta resurssista Aikamerkintään**. Valitse **Suhde**-sivulla **Käytä kenttien yhdistämismäärityksiä**. 
4. Valitse **Uusi** ja luo uusi kenttien yhdistämismääritys **Varattavissa oleva resurssi** -entiteetin **Vakio-otsikko**-kentän ja **Aikamerkintä**-entiteetin **Vakio-otsikko**-viitekentän välille. 

> ![Kenttien yhdistämismääritysten luominen sen mahdollistamiseksi, että kentän Vakionimike oletusarvoiseksi yhdistämismääritykseksi otetaan Varattavissa olevasta resurssista Aikamerkintään](media/ST-Mapping2.png)

Tämä täydentää entiteettiperusteisiin mukautettuihin dimensioihin vaadittavat rakennemuutokset.

##  <a name="add-custom-fields-to-forms-views-and-business-rules"></a>Muokattujen kenttien lisääminen lomakkeisiin, näkymiin ja liiketoimintasääntöihin

Kun olet tehnyt kaikki vaadittavat rakennemuutokset, seuraavana vaiheena on tehdä kentät näkyviksi käyttöliittymässä lisäämällä kentät lomakkeisiin ja näkymiin.

1. Avaa lomake tai näkymä. Valitse kenttä oikeanpuoleisessa siirtymisruudussa ja vedä se lomakekaavioon. 
2. Jos muokkaat näkymää, käytä oikeanpuoleista siirtymäruutua, valitse **Lisää kenttiä**, valitse **Kenttäluettelo**-valintaikkunassa tarvitsemasi kentät ja valitse sitten **OK**.

Seuraavassa luettelossa esitetään kattava entiteettiperusteinen luettelo niistä valmiina olevista lomakkeista ja näkymistä, jotka on päivitettävä uusilla kentillä. Jos olet mukauttanut näitä entiteettejä uusilla näkymillä tai lomakkeilla, lisää uudet kentät myös niihin.

| Entity        | Uutta kenttää edellyttävät lomakkeet   |Uutta kenttää edellyttävät näkymät      |
| ------------------------------|---------------------------------|----------------------------------|
|  Roolin hinta|• Tiedot |• Aktiiviset resurssiluokan hinnat<br> • Resurssiluokan hintojen liitetty näkymä|
|  Roolin hinnankorotus|• Tiedot|• Aktiivisen roolin hinnankorotukset<br>• Roolin hinnankorotuksen liitetty näkymä|
|  Tarjousrivin tiedot|• Projektin tiedot<br>• Projektin pikaluonti|• Aktiiviset tarjousrivin tiedot<br>• Yhdistetyt tarjousrivin tiedot<br>• Tarjousrivin tietojen liitetty näkymä|
|  Projektin sopimusrivin tiedot|• Projektin tiedot<br>• Projektin pikaluonti|• Yhdistetyt sopimusrivin tiedot<br>• Aktiiviset sopimusrivin tiedot<br>• Sopimusrivin tietojen liitetty näkymä|
|  Projektiryhmän jäsen|• Tiedot<br>• Uusi lomake|• Aktiiviset projektiryhmän jäsenet<br>• Projektiryhmän jäsenet<br>• Projektiryhmän jäsenten liitetty näkymä|
|  Aikamerkintä|• Tiedot<br>• Luo aikamerkintä|• Omat aikamerkinnät päivämäärän mukaan<br>• Omat aikamerkinnät tällä viikolla<br>• Aikamerkinnät hyväksyttäväksi|
|  Kirjauskansion rivi|• Tiedot<br>• Pikaluonti|• Aktiiviset kirjauskansion rivit<br>• Kirjauskansion rivin liitetty näkymä|
|  Laskurivin tiedot|• Tiedot<br>• Pikaluonti|• Aktiiviset laskurivin tiedot<br>• Laskun veloitettavat tapahtumat<br>• Laskun ilmaiset tapahtumat<br>• Laskurivin tietojen liitetty näkymä<br>• Laskun ei-veloitettavat tapahtumat|
|  Todellinen|• Tiedot<br>• Aktiiviset todelliset arvot|• Todellisten arvojen liitetty näkymä|

Mukautettuja kenttiä voi määrityksistäsi riippuen olla tarpeen lisätä myös liiketoimintasääntöihin. Yksi valmis esimerkki on liiketoimintasääntöä **Aikamerkinnän muokattavuus tilan perusteella** varten. Tämä sääntö määrittää, mitkä kentät on lukittava, kun Aikamerkintä-tila on tilassa, jota ei voi muokata, kuten **Hyväksytty**. Lisää kenttiä tähän liiketoimintasääntöön, jotta kenttiä ei voi muokata, kun Aikamerkinnän tila on muu kuin **Luonnos** tai **Palautettu**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]