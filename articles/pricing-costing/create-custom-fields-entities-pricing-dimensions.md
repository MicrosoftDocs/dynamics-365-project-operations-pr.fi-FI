---
title: Mukautettujen kenttien ja entiteettien luominen hinnoitteludimensioina
description: Tässä aiheessa on tietoja mukautetun asetusjoukon tai mukautettujen entiteettien luomisesta.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
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
ms.openlocfilehash: 2000f7e710267560fe2bd52b0e33024617d108ea
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/28/2020
ms.locfileid: "3898257"
---
# <a name="create-custom-fields-and-entities-as-pricing-dimensions"></a>Mukautettujen kenttien ja entiteettien luominen hinnoitteludimensioina

_**Koskee:** Project Operationsin resurssiin / muuhun kuin resurssiin perustuvia skenaarioita, Lite-käyttöönotto-kaupasta proformalaskutukseen_

Toimi seuraavasti aina, kun haluat luoda mukautetun asetusjoukon tai entiteetin.

> [!IMPORTANT]
> Suosittelemme kaikkien mukautettujen hinnoitteludimensioiden muutokset erillisessä ratkaisussa. Tämä tärkeä paras käytäntö varmistaa, että muutoksia voidaan myöhemmin päivittää tai poistaa tarpeen mukaan, auttaa työn uudelleenkäytössä ja helpottaa näiden muutosten siirtämistä toiseen esiintymään. Kun olet tehnyt kaikki tarvittavat muutokset, vie tämä ratkaisu muodossa **Hallittu ratkaisu** ja tuo se muihin esiintymiin, jotta voit käyttää hinnoittelumäärityksiäsi uudelleen.


## <a name="create-a-custom-solution-for-pricing-dimensions"></a>Mukautetun ratkaisun luominen hinnoitteludimensioille
1. Siirry kohtaan **Asetukset** > **Ratkaisut** ja luo uusi ratkaisu valitsemalla **Uusi**. 
2. Anna ratkaisulle nimeksi **organisaation \<your organization name> hinnoitteludimensiot**, anna muut tarvittavat tiedot ja valitse **Tallenna**.
  
## <a name="create-custom-fields-and-option-sets-in-the-pricing-dimension-solution"></a>Mukautettujen kenttien ja asetusjoukkojen luominen hinnoitteludimensioratkaisussa

Hinnoitteludimensio voi olla asetusjoukko tai entiteetti. Molemmat on luotava hinnoitteluratkaisussa. Tämän toimintosarjojen vaiheissa selitetään, miten luodaan entiteettiperusteisia dimensioita ja asetusjoukkoperusteisia dimensioita.

### <a name="entity-based-dimensions"></a>Entiteettiperusteiset dimensiot

1. Siirry kohtaan **Asetukset** > **Ratkaisut** ja kaksoisnapsauta **organisaation \<your organization name> hinnoitteludimensio** -kohtaa.
2. Valitse vasemman siirtymisruudun Ratkaisunhallinnassa **Entiteetit**.
3. Valitse **Uusi**, jos haluat luoda uuden entiteetin nimellä **Vakio-otsikko**. 
4. Syötä muut tarvittavat tiedot ja valitse **Tallenna**.


### <a name="option-set-based-dimensions"></a>Asetusjoukkoperusteiset dimensiot 
Voit luoda kaksi asetusjoukkoperusteista dimensiota. Käytä asetusjoukkoa **Resurssin työn sijainti** seurataksesi töiden **Koti** ja **Asiakkaan tiloissa** ja käytä kentän **Resurssin työtunnit** arvoja **Tavallinen työ** ja **Ylityö** hinnankorotuksen perusteena, kun työ on valmis.


1. Siirry kohtaan **Asetukset** > **Ratkaisut** ja kaksoisnapsauta **organisaation \<your organization name> hinnoitteludimensio** -kohtaa. 
2. Valitse vasemman siirtymisruudun Ratkaisunhallinnassa **Asetusjoukot**. 
3. Valitse **Uusi** luodaksesi uuden asetusjoukon. Syötä muut tarvittavat tiedot ja valitse **Tallenna**.

## <a name="create-data-for-entity-based-dimensions"></a>Tietojen luominen entiteettiperusteisia dimensioita varten

Voit luoda tietoja entiteettiperusteisille dimensioille manuaalisesti tai käyttämällä Microsoft Excelin tuontia tai palvelukutsuja. Luo tämän toimintosarjan vaiheiden avulla kaksi vakionimekettä eli **Järjestelmäinsinööri** ja **Vanhempi järjestelmäinsinööri** entiteettiperusteisen dimension **Vakionimike** perusteella. Jos haluamasi tietomäärä on vähäinen, kuten seuraavassa esimerkissä, voit käyttää vakiolomaketta.

1. Valitse **Erikoishaku**, valitse entiteetin **Vakio-otsikko** ja valitse sitten **Tulokset**. Näkyviin tulevat kaikki **Vakionimike**-entiteetin rivit.
2. Valitse **Uusi** ja syötä **Nimi**-kenttään Järjestelmäinsinööri. Valitse sitten **Tallenna**.
3. Sulje lomake. 
4. Luo toinen vakionimike Vanhemmalle järjestelmäinsinöörille toistamalla vaiheet 1–3.

## <a name="add-all-required-entities-and-related-components-to-the-pricing-dimension-solution"></a>Kaikkien tarvittavien entiteettien ja niihin liittyvien komponenttien lisääminen hinnoitteludimensioratkaisuun
Sinun on lisättävä seuraavat entiteetit hinnoitteluratkaisuusi. Tee tämän toimintosarjan vaiheiden avulla tärkeitä rakennemuutoksia hinnoitteluratkaisuun, jotta entiteetit ottavat uudet hinnoitteludimensiot huomioon.

1. Valitse **Asetukset** > **Ratkaisut** ja kaksoisnapsauta **organisaation \<your organization name> hinnoitteludimensio** -kohtaa. 
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


> [!NOTE]
> Varmista, että lisäät kaikkien valittujen entiteettien kaikki lomakkeet ja näkymät.

4. Kun sinua pyydetään lisäämään yllä valituista entiteeteistä riippuvaisia entiteettejä, valitse **Ei**.

