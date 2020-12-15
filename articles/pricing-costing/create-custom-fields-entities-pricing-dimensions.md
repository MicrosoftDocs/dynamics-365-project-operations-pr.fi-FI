---
title: Mukautettujen kenttien ja entiteettien luominen hinnoitteludimensioina
description: Tässä aiheessa on tietoja mukautetun asetusjoukon tai mukautettujen entiteettien luomisesta.
author: rumant
manager: AnnBe
ms.date: 11/18/2020
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
ms.openlocfilehash: fc5917856b8f28d36dc55593a68eba7823a00b36
ms.sourcegitcommit: 573be7e36604ace82b35e439cfa748aa7c587415
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/25/2020
ms.locfileid: "4642809"
---
# <a name="create-custom-fields-and-entities-as-pricing-dimensions"></a>Mukautettujen kenttien ja entiteettien luominen hinnoitteludimensioina

_**Koskee:** Project Operationsin resurssiin / muuhun kuin resurssiin perustuvia skenaarioita, Lite-käyttöönotto-kaupasta proformalaskutukseen_

Suorita seuraavat vaiheet, kun haluat luoda mukautetun asetusjoukon tai entiteetin sen käyttämiseksi hinnoitteludimensiona. Katso lisätietoja kohdasta [Hinnoitteludimensioiden yleiskatsaus](pricing-dimensions-overview.md).  

> [!IMPORTANT]
> Suosittelemme kaikkien mukautettujen hinnoitteludimensioiden muutokset erillisessä ratkaisussa. Tämä tärkeä parhaaksi todettu käytäntö tarjoaa joustavulla tulevaisuudessa tarvittavia päivityksiä ja poistoja varten. Tämä auttaa myös tehdyn työn uudelleenkäyttämisessä, ja helpottaa näiden muutosten siirrossa toiseen esiintymään. Kun kaikki tarvittavat muutokset on tehty, vie tämä ratkaisu muodossa **Hallittu ratkaisu** ja tuo se toisiin esiintymiin hinnoittelumääritysten uudelleenkäyttöä varten.

  
## <a name="create-custom-fields-and-option-sets-in-the-pricing-dimension-solution"></a>Mukautettujen kenttien ja asetusjoukkojen luominen hinnoitteludimensioratkaisussa

Hinnoitteludimensio voi olla asetusjoukko tai entiteetti. Molemmat on luotava hinnoitteluratkaisussa. Tämän toimintosarjojen vaiheissa selitetään, miten luodaan entiteettiperusteisia dimensioita ja asetusjoukkoperusteisia dimensioita.

### <a name="entity-based-dimensions"></a>Entiteettiperusteiset dimensiot
Voit luoda entiteettipohjaisia dimensioita seuraamalla näitä vaiheita:

1. Siirry kohtaan **Asetukset** > **Ratkaisut** ja kaksoisnapsauta **organisaation \<your organization name> hinnoitteludimensio** -kohtaa.
2. Valitse vasemman siirtymisruudun Ratkaisunhallinnassa **Entiteetit**.
3. Valitse **Uusi**, jos haluat luoda uuden entiteetin nimellä **Vakio-otsikko**. 
4. Syötä muut tarvittavat tiedot ja valitse **Tallenna**.

> ![Vakio-otsikko-entiteetin määritys](media/Standard-Title-entity-definition.png)

### <a name="option-set-based-dimensions"></a>Asetusjoukkoperusteiset dimensiot 
Voit luoda kaksi asetusjoukkoperusteista dimensiota. 

- **Resurssien työsijainnin** avulla voit seurata **Koti**-sijainnin työn ja **Asiakkaan tiloissa** tapahtuvan työn hintaa. 
- Käytä **Resurssin työaikaa** arvoilla **Normaali** ja **Ylityö**, jos haluat korottaa hintaa, kun työ on valmis.

Seuraavassa kuvassa on **Resurssin työsijainti** -dimension näkymä. 

> ![Asetusjoukkoperusteinen hinnoitteludimensio nimeltään Resurssin työn sijainti](media/Option-set-PD-called-Resource-Work-Location.png)

Seuraavassa kuvassa on **Resurssin työtunnit** -dimension näkymä. 

> ![Asetusjoukkoperusteinen hinnoitteludimensio nimeltään Resurssin työntunnit](media/Option-set-PD-called-Resource-Work-Hours.png)

1. Siirry kohtaan **Asetukset** > **Ratkaisut** ja kaksoisnapsauta **organisaation \<your organization name> hinnoitteludimensio** -kohtaa. 
2. Valitse vasemman siirtymisruudun Ratkaisunhallinnassa **Asetusjoukot**. 
3. Valitse **Uusi** luodaksesi uuden asetusjoukon. Syötä muut tarvittavat tiedot ja valitse **Tallenna**.

## <a name="create-data-for-entity-based-dimensions"></a>Tietojen luominen entiteettiperusteisia dimensioita varten

Voit luoda tietoja entiteettiperusteisille dimensioille manuaalisesti tai käyttämällä Microsoft Excelin tuontia tai palvelukutsuja. Luo tämän toimintosarjan vaiheiden avulla kaksi vakionimekettä eli **Järjestelmäinsinööri** ja **Vanhempi järjestelmäinsinööri** entiteettiperusteisen dimension **Vakionimike** perusteella. Jos haluamasi tietomäärä on vähäinen, kuten seuraavassa esimerkissä, voit käyttää vakiolomaketta.

1. Valitse **Erikoishaku**.
2. Valitse entiteetti **Vakionimike** ja valitse sitten **Tulokset**. Näkyviin tulevat kaikki **Vakionimike**-entiteetin rivit.
3. Valitse **Uusi** ja syötä **Nimi**-kenttään Järjestelmäinsinööri. Valitse sitten **Tallenna**.
4. Sulje sivu. 
5. Luo toinen vakionimike Vanhemmalle järjestelmäinsinöörille toistamalla vaiheet 1–3.

> ![Esimerkkitietoja Vakionimike-entiteetille](media/ST-data.png)
