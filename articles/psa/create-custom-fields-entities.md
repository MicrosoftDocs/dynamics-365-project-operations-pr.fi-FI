---
title: Mukautettujen kenttien ja entiteettien luominen
description: Tässä artikkelissa käsitellään sitä, miten Power Apps-ympäristön omassa ratkaisussa luodaan asetusjoukkoja ja entiteettejä.
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
ms.openlocfilehash: 3b6f675d604f3b6a6f2465c413ceff3d16815e12
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8926910"
---
# <a name="create-custom-fields-and-entities"></a>Mukautettujen kenttien ja entiteettien luominen 

[!include [banner](../includes/psa-now-project-operations.md)]

Toimi seuraavasti aina, kun haluat luoda mukautetun asetusjoukon tai entiteetin Power Apps-ympäristössä.  
Tämän artikkelin toimintosarjat tarkoitus suorittaa Project Service Automationin (PSA) verkkoliittymässä.

> [!IMPORTANT]
> Suosittelemme kaikkien mukautettujen hinnoitteludimensioiden muutokset erillisessä ratkaisussa. Tämä tärkeä paras käytäntö varmistaa, että muutoksia voidaan myöhemmin päivittää tai poistaa tarpeen mukaan, auttaa työn uudelleenkäytössä ja helpottaa näiden muutosten siirtämistä toiseen esiintymään. Kun olet tehnyt kaikki tarvittavat muutokset, vie tämä ratkaisu muodossa **Hallittu ratkaisu** ja tuo se muihin esiintymiin, jotta voit käyttää hinnoittelumäärityksiäsi uudelleen.

  
## <a name="create-custom-fields-and-option-sets-in-the-pricing-dimension-solution"></a>Mukautettujen kenttien ja asetusjoukkojen luominen hinnoitteludimensioratkaisussa

Hinnoitteludimensio voi olla asetusjoukko tai entiteetti. Molemmat on luotava hinnoitteluratkaisussa. Tämän toimintosarjojen vaiheissa selitetään, miten luodaan entiteettiperusteisia dimensioita ja asetusjoukkoperusteisia dimensioita.

### <a name="entity-based-dimensions"></a>Entiteettiperusteiset dimensiot

1. Valitse PSA:ssa **Asetukset** > **Ratkaisut** ja kaksoisnapsauta **\<your organization name> hinnoitteludimensiot**.
2. Valitse vasemman siirtymisruudun Ratkaisunhallinnassa **Entiteetit**.
3. Napsauta **Uusi**, jos haluat luoda uuden entiteetin nimellä **Vakio-otsikko**. Syötä muut tarvittavat tiedot ja napsauta **Tallenna**.

> ![Vakio-otsikko-entiteetin määritys.](media/Standard-Title-entity-definition.png)


### <a name="option-set-based-dimensions"></a>Asetusjoukkoperusteiset dimensiot 
Voit luoda kaksi asetusjoukkoperusteista dimensiota. Käytä asetusjoukkoa **Resurssin työn sijainti** seurataksesi töiden **Koti** ja **Asiakkaan tiloissa** ja käytä kentän **Resurssin työtunnit** arvoja **Tavallinen työ** ja **Ylityö** hinnankorotuksen perusteena, kun työ on valmis.


1. Valitse PSA:ssa **Asetukset** > **Ratkaisut** ja kaksoisnapsauta **\<your organization name> hinnoitteludimensioita**. 
2. Valitse vasemman siirtymisruudun Ratkaisunhallinnassa **Asetusjoukot**. 
3. Napsauta **Uusi** luodaksesi uuden asetusjoukon, syötä muut tarvittavat tiedot ja napsauta **Tallenna**.

> ![Asetusjoukkoperusteinen hinnoitteludimensio nimeltään Resurssin työn sijainti.](media/Option-set-PD-called-Resource-Work-Location.png)

> ![Asetusjoukkoperusteinen hinnoitteludimensio nimeltään Resurssin työntunnit.](media/Option-set-PD-called-Resource-Work-Hours.PNG)


## <a name="create-data-for-entity-based-dimensions"></a>Tietojen luominen entiteettiperusteisia dimensioita varten

Voit luoda tietoja entiteettiperusteisille dimensioille manuaalisesti tai käyttämällä Microsoft Excelin tuontia tai palvelukutsuja. Luo tämän toimintosarjan vaiheiden avulla kaksi vakionimekettä eli **Järjestelmäinsinööri** ja **Vanhempi järjestelmäinsinööri** entiteettiperusteisen dimension **Vakionimike** perusteella. Jos haluamasi tietomäärä on vähäinen, kuten seuraavassa esimerkissä, voit käyttää vakiolomaketta.

1. Napsauta PSA:ssa **Erikoishaku**. Valitse entiteetti **Vakionimike** ja napsauta sitten **Tulokset**. Näkyviin tulevat kaikki **Vakionimike**-entiteetin rivit.
2. Valitse **Uusi**. Syötä **Nimi**-kenttään "Järjestelmäinsinööri" ja napsauta **Tallenna**.
3. Sulje lomake. 
4. Luo toinen vakionimike Vanhemmalle järjestelmäinsinöörille toistamalla vaiheet 1–3.

> ![Esimerkkitietoja Vakionimike-entiteetille.](media/ST-data.png)




[!INCLUDE[footer-include](../includes/footer-banner.md)]
