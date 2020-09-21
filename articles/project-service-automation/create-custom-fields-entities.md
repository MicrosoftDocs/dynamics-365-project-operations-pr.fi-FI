---
title: Mukautettujen kenttien ja entiteettien luominen
description: Tässä aiheessa selitetään, miten Power Apps-ympäristön omassa ratkaisussasi luodaan asetusjoukkoja ja entiteettejä.
author: Rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 11/26/2018
ms.topic: article
ms.prod: Project Service
ms.service: business-applications
ms.assetid: fb160bfd-e037-4a21-a968-3ff2e6e16481
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
ms.openlocfilehash: 7ee30e3bb6b8034ef226e2e9181195685355011f
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/24/2020
ms.locfileid: "3751240"
---
# <a name="create-custom-fields-and-entities"></a>Mukautettujen kenttien ja entiteettien luominen 

Toimi seuraavasti aina, kun haluat luoda mukautetun asetusjoukon tai entiteetin Power Apps-ympäristössä.  
Tämän aiheen toimintojoukot on tarkoitus suorittaa Project Service Automationin (PSA) verkkoliittymän avulla.

> [!IMPORTANT]
> Suosittelemme kaikkien mukautettujen hinnoitteludimensioiden muutokset erillisessä ratkaisussa. Tämä tärkeä paras käytäntö varmistaa, että muutoksia voidaan myöhemmin päivittää tai poistaa tarpeen mukaan, auttaa työn uudelleenkäytössä ja helpottaa näiden muutosten siirtämistä toiseen esiintymään. Kun olet tehnyt kaikki tarvittavat muutokset, vie tämä ratkaisu muodossa **Hallittu ratkaisu** ja tuo se muihin esiintymiin, jotta voit käyttää hinnoittelumäärityksiäsi uudelleen.


## <a name="create-a-custom-solution-for-pricing-dimensions"></a>Mukautetun ratkaisun luominen hinnoitteludimensioille
1. Napsauta PSA:ssa **Asetukset** > **Ratkaisut** ja luo sitten uusi ratkaisu napsauttamalla **Uusi**. 
2. Anna ratkaisulle nimeksi **\<organisaatiosi nimi > hinnoitteludimensiot**, anna muut tarvittavat tiedot ja napsauta **Tallenna**.

> ![Mukautetun ratkaisun luominen hinnoitteludimensioille](media/Creation-of-custom-pricing-dimension-solution.PNG)
  
## <a name="create-custom-fields-and-option-sets-in-the-pricing-dimension-solution"></a>Mukautettujen kenttien ja asetusjoukkojen luominen hinnoitteludimensioratkaisussa

Hinnoitteludimensio voi olla asetusjoukko tai entiteetti. Molemmat on luotava hinnoitteluratkaisussa. Tämän toimintosarjojen vaiheissa selitetään, miten luodaan entiteettiperusteisia dimensioita ja asetusjoukkoperusteisia dimensioita.

### <a name="entity-based-dimensions"></a>Entiteettiperusteiset dimensiot

1. Napsauta PSA:ssa **Asetukset** > **Ratkaisut** kaksoisnapsauta sitten **\<organisaatiosi nimi>: hinnoitteludimensiot**.
2. Valitse vasemman siirtymisruudun Ratkaisunhallinnassa **Entiteetit**.
3. Napsauta **Uusi**, jos haluat luoda uuden entiteetin nimellä **Vakio-otsikko**. Syötä muut tarvittavat tiedot ja napsauta **Tallenna**.

> ![Vakio-otsikko-entiteetin määritys](media/Standard-Title-entity-definition.png)


### <a name="option-set-based-dimensions"></a>Asetusjoukkoperusteiset dimensiot 
Voit luoda kaksi asetusjoukkoperusteista dimensiota. Käytä asetusjoukkoa **Resurssin työn sijainti** seurataksesi töiden **Koti** ja **Asiakkaan tiloissa** ja käytä kentän **Resurssin työtunnit** arvoja **Tavallinen työ** ja **Ylityö** hinnankorotuksen perusteena, kun työ on valmis.


1. Napsauta PSA:ssa **Asetukset** > **Ratkaisut** ja kaksoisnapsauta sitten **\<organisaatiosi nimi>: hinnoitteludimensiot**. 
2. Valitse vasemman siirtymisruudun Ratkaisunhallinnassa **Asetusjoukot**. 
3. Napsauta **Uusi** luodaksesi uuden asetusjoukon, syötä muut tarvittavat tiedot ja napsauta **Tallenna**.

> ![Asetusjoukkoperusteinen hinnoitteludimensio nimeltään Resurssin työn sijainti ](media/Option-set-PD-called-Resource-Work-Location.png)

> ![Asetusjoukkoperusteinen hinnoitteludimensio nimeltään Resurssin työntunnit ](media/Option-set-PD-called-Resource-Work-Hours.PNG)


## <a name="create-data-for-entity-based-dimensions"></a>Tietojen luominen entiteettiperusteisia dimensioita varten

Voit luoda tietoja entiteettiperusteisille dimensioille manuaalisesti tai käyttämällä Microsoft Excelin tuontia tai palvelukutsuja. Luo tämän toimintosarjan vaiheiden avulla kaksi vakionimekettä eli **Järjestelmäinsinööri** ja **Vanhempi järjestelmäinsinööri** entiteettiperusteisen dimension **Vakionimike** perusteella. Jos haluamasi tietomäärä on vähäinen, kuten seuraavassa esimerkissä, voit käyttää vakiolomaketta.

1. Napsauta PSA:ssa **Erikoishaku**. Valitse entiteetti **Vakionimike** ja napsauta sitten **Tulokset**. Näkyviin tulevat kaikki **Vakionimike**-entiteetin rivit.
2. Valitse **Uusi**. Syötä **Nimi**-kenttään "Järjestelmäinsinööri" ja napsauta **Tallenna**.
3. Sulje lomake. 
4. Luo toinen vakionimike Vanhemmalle järjestelmäinsinöörille toistamalla vaiheet 1–3.

> ![Esimerkkitietoja Vakionimike-entiteetille ](media/ST-data.png)

## <a name="add-all-required-psa-entities-and-related-components-to-the-pricing-dimension-solution"></a>Kaikkien tarvittavien PSA-entiteettien ja niihin liittyvien komponenttien lisääminen hinnoitteludimensioratkaisuun
Sinun on lisättävä seuraavat Project Service -entiteetit hinnoitteluratkaisuusi. Tee tämän toimintosarjan vaiheiden avulla tärkeitä rakennemuutoksia hinnoitteluratkaisuun, jotta entiteetit ottavat uudet hinnoitteludimensiot huomioon.

1. Napsauta PSA:ssa **Asetukset** > **Ratkaisut** kaksoisnapsauta sitten **\<organisaatiosi nimi>: hinnoitteludimensiot**. 
2. Valitse vasemman siirtymisruudun Ratkaisunhallinnassa **Lisää aiemmin luoto** > **Entiteetit**.
3. Valitse **Ratkaisun osat** -valintaikkunassa seuraavat entiteetit:

- Todellinen
- Varattava resurssi
- Arviorivi
- Laskurivin tiedot
- Kirjauskansion rivi
- Projektin sopimusrivin tiedot
- Projektiryhmän jäsen
- Tarjousrivin tiedot
- Roolin hinnankorotus
- Roolin hinta 
- Aikamerkintä 

> ![Aiemmin luotujen entiteettien lisääminen hinnoitteludimensioratkaisuun](media/Existing-entities-to-PD-solution.png)

> ![Valitse ratkaisun osat](media/Dimension-Components.png)

> [!NOTE]
> Varmista, että lisäät kaikkien valittujen entiteettien kaikki lomakkeet ja näkymät.

4. Kun sinua pyydetään lisäämään yllä valituista entiteeteistä riippuvaisia entiteettejä, valitse **Ei**.

> ![Älä lisää kaikkia liittyviä komponentteja.](media/Do-not-include-required.png)


