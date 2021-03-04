---
title: Uuden ympäristön valmisteleminen
description: Tässä aiheessa on tietoja siitä, miten uuden Project Operations -ympäristön voi valmistella.
author: sigitac
manager: Annbe
ms.date: 12/11/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 09af2a7693c45d1d0b9c75420d018cc50d2cc0fa
ms.sourcegitcommit: 04c446746aad97fc3f4c3d441983c586b918a3a6
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/11/2020
ms.locfileid: "4727786"
---
# <a name="provision-a-new-environment"></a>Uuden ympäristön valmisteleminen

_**Käytetään:** Project Operationsin resursseihin ja ei-varastoitaviin perustuvissa skenaarioissa_

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Tässä aiheessa on tietoja uuden Dynamics 365 Project Operations -ympäristön valmistelusta resurssi/ei-varastoitava -pohjaisille skenaarioille.

## <a name="enable-project-operations-automated-provisioning-in-an-lcs-project"></a>Project Operationsin automaattisen valmistelun käyttöönotto LCS-projektissa

Käytä seuraavia vaiheita, kun haluat ottaa käyttöön Project Operationsin automatisoidun valmistelutyönkulun LCS-projektillesi.

1. Siirry [LCS:sään](https://lcs.dynamics.com/v2) ja valitse **Esiversio-ominaisuuksien hallinta** -ruutu.
2. Valitse **Esiversio-ominaisuus** -luettelosta **Project Operations -ominaisuus** ja ota sitten Project Operations käyttöön valitsemalla **Esiversio-ominaisuus käytössä**.

> [!NOTE]
> Tämä vaihe suoritetaan vain kerran LCS-projektia kohden.

## <a name="provision-a-project-operations-environment"></a>Project Operations -ympäristön tarjoaminen

1. Avaa uusi Dynamics 365 Finance [-esittely-ympäristön](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) tai [eristys-/tuotantoympäristön](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deployenvironment-newinfrastructure) käyttöönotto. 
2. Suorita ohjatun **Ympäristön valmistelu** -toiminnon vaiheet. 

> [!IMPORTANT]
> Varmista, että valittu sovellusversio on 10.0.13 tai uudempi.

3. Jos haluat valmistella Project Operationsi, valitse **Lisäasetukset**-kohdassa **Common Data Service**. 
4. Ota **Common Data Service -asetukset** käyttöön valitsemalla **Kyllä** ja kirjoitramalla tiedot pakollisiin kenttiin:

  - Nimi
  - Alue
  - Language
  - Valuutta
 
5. Valitse **Common Data Service -malli** -kentässä **Project Operations** 

6. Valitse käyttöönoton ympäristötyyppi. Tilauspohjaisen kokeiluversion avulla voit käyttää CDS-ympäristöä 30 päivän ajan. 

![Käyttööntoton asetukset](./media/1DeploymentSettings.png)

> [!IMPORTANT]
> Valitse **Hyväksy**, kun hyväksyt palveluehdot, ja palaa sitten käyttöönottoasetuksiin valitsemalla **Valmis**.

![Käyttöönoton suostumus](./media/2DeploymentConsent.png)

7. Valinnainen - Käytä esittelytietoja ympäristössä. Valitse **Lisäasetukset**, valitse **Mukauta SQL-tietokannan määrityksiä** ja aseta **Määritä sovellustietokannan tietojoukko** -asetukseksi **Esittely**.

8. Täytä loput pakolliset kentät ohjatussa toiminnossa ja vahvista asennus. Ympäristön valmisteluaika vaihtelee ympäristötyypin mukaan. Valmistelu voi kestää jopa kuusi tuntia.

  Kun käyttöönotto on valmis, ympäristö näkyy tilassa **Otettu käyttöön**.

9. Voit varmistaa, että ympäristön käyttöönotto onnistui, valitsemalla **Kirjaudu sisään** ja kirjautumalla ympäristöön.

![-ympäristön tiedot](./media/3EnvironmentDetails.png)

## <a name="apply-updates-to-the-finance-environment"></a>Ota päivitykset käyttöön Finance-ympäristössä

Project Operations edellyttää Finance-ympäristöä, jossa on sovellusversio **10.0.13 (10.0.569.20009)** tai uudempi.

Sinun täytyy ehkä ottaa käyttöön laatupäivityksiä Finance-ympäristössäsi, jotta saat tämän version.

1. Valitse LCS:n **Ympäristön tiedot** -sivun **Saatavilla olevat päivitykset** -kohdassa **Näytä päivitys**.

![Näytä päivitykset](./media/5ViewUpdates.png)

2. Valitse **Binaaripäivitykset**-sivulla **Tallenna paketti.**

![Tallenna paketti](./media/6SavePackage.png)

3. Valitse **Valitse kaikki** ja sitten **Tallenna paketti**.

![Päivitysten tarkistaminen ja tallentaminen](./media/7ReviewAndSaveUpdates.png)

4. Kirjoita paketin nimi ja kuvaus ja valitse sitten **Tallenna**. Internet-yhteydestä riippuen tämä prosessi voi kestää jonkin aikaa.

![Lataa paketti Resurssit-kirjastoon](./media/8UploadPackageToAssetsLibrary.png)

5. Kun paketti on tallennettu, valitse **Valmis** ja tallenna paketti LCS-projektin Resurssit-kirjastoon.

Paketin tallentaminen ja tarkistaminen voi kestää noin 15 minuuttia.

6. Voit ottaa päivityksen käyttöön siirtymällä LCS:n **Ympäristön tiedot** -sivulle ja valitsemalla **Ylläpidä** > **Ota päivitykset käyttöön**.

![Ympäristöjen ylläpito](./media/9MaintainEnvironment.png)

7. Valitse päivitysluettelosta luomasi paketti ja valitse sitten **Käytä**.

![Päivitysten ottaminen käyttöön](./media/10ApplyUpdates.png)

Ympäristön huolto kestää jonkin aikaa. Kun ympäristö on valmis, se palaa käyttöön otettuun tilaan.

![Ympäristö otettu käyttöön](./media/11EnvironmentDeployed.png)

## <a name="establish-a-dual-write-connection"></a>Kaksinkertaisen kirjoituksen yhteyden muodostaminen 

1. Siirry LCS-projektissa **Ympäristön tiedot** -sivulle.
2. **Common Data Service -ympäristön tiedot** -kohdassa **Linkitä CDS for Appsiin**.
3. Kun linkki on valmis, valitse uudelleen **Linkitä CDS for Appsiin**. Sinut ohjataan Financen kaksoiskirjoitukseen.

![Linkitä CDS:ään](./media/12LinktoCDS.png)

4. Valitse **Käytä ratkaisua**, kun haluat käyttää entiteettejä, jotkan yhdistetään integrointiin.

![Ota ratkaisut käyttöön](./media/13ApplySolutions.png)

5. Valitse molemmat ratkaisut, **Dynamics 365 Finance and Operations Kaksoiskirjoitusentiteetin yhdistämismääritys** ja **Dynamics 365 Project Operations Kaksoiskirjoitusentiteettien yhdistämismääritykset** ja valitse sitten **Käytä**.

![Ratkaisujen vahvistaminen](./media/14ConfirmSolutions.png)

Kun ratkaisut on otettu käyttöön, kaksoiskirjoituskohteet otetaan käyttöön ympäristössä.

![Ratkaisujen käyttöönotto](./media/15ApplyingSolutions.png)

Kun entiteetit otetaan käyttöön, kaikki käytettävissä olevat yhdistämismääritykset näkyvät ympäristössä.

![Kaksoiskirjoituksen yhdistämismääritykset](./media/15DWMappings.png)

## <a name="refresh-the-data-entities-after-the-update"></a>Päivitä tietoentiteetit päivityksen jälkeen

1. Siirry Financessa **Tietojen hallinta** -työtilaan.

![Tietojen hallinnan työtila](./media/16DataManagement.png)

2. Valitse **Kehyksen parametrit** -ruutu.

![Kehyksen parametrit](./media/17FrameworkParameters.png)

3. Valitse **Entiteetin asetukset** -sivulla **Päivitä entiteettiluettelo**.

![Päivitä entiteettiluettelo](./media/18RefreshEntityList.png)

Päivitys kestää noin 20 minuuttia. Saat ilmoituksen, kun se on valmis.

![Päivityksen vahvistus](./media/19RefreshConfirmation.png)

## <a name="update-security-settings-on-project-operations-on-dataverse"></a>Suojausasetusten päivittäminen Dataversen Project Operationsissa

1. Siirry Project Operationsiin Dataverse-ympäristössä. 
2. Valitse **Asetukset** > **Suojaus** > **Käyttöoikeusroolit**. 
3. Valitse **Käyttöoikeusroolit**-sivun rooliluettelosta **kaksoiskirjoitussovelluksen käyttäjä** ja valitse **Mukautetut entiteetit** -välilehti.  
4. Varmista, että roolilla on **Luku**- ja **Lisää kohteeseen** -oikeudet seuraaville:
      
      - **Valuuttakurssin tyyppi**
      - **Tilikartta**
      - **Kirjanpitokalenteri**
      - **Tapahtumarekisteri**

5. Kun käyttöoikeusrooli on päivitetty, siirry kohtaan **Asetukset** > **Suojaus** > **Ryhmät** ja valitse oletusryhmä **Oman yksikön omistaja** -ryhmänäkymässä.
6. Valitse **Hallitse rooleja** ja varmista, että **kaksoiskirjoitussovelluksen käyttäjä** -käyttöoikeus on käytössä tässä ryhmässä.

## <a name="run-project-operations-dual-write-maps"></a>Suorita Project Operationsin kaksoiskirjoituksen yhdistämismääritykset

1. Siirry LCS-projektissa **Ympäristön tiedot** -sivulle.
2. Valitse **Common Data Service -ympäristön tiedot** -kohdassa **Linkitä CDS for Appsiin.** Kun olet valinnut linkin, sinut ohjataan yhdistämismääritysten entiteettiluetteloon.
3. Käynnistä yhdistäm,ismääritykset seuraavassa taulukossa kuvatulla tavalla. Varmista, että seuraat järjestystä luettelossa.

| **Entiteetin yhdistämismääritys** | **Päivitä entiteetti** | **Ensimmäinen synkronointi** | **Ensimmäisen synkronoinnin pääkohde** | **Suorita edellytykset** | **Edellytysten ensimmäinen synkronointi** |
| --- | --- | --- | --- | --- | --- |
| **Kaikkien yritysten projektiresurssiroolit (bookableresourcecategories)** | No | Kyllä | Common Data Service | No | – |
| **Yritykset (cdm\_companies)** | No | Kyllä | Finance and Operations -sovellukset | No | – |
| **Tapahtumarekisteri (msdyn_ledgers)** | No | Kyllä | Finance and Operations -sovellukset | Kyllä | Kyllä, Finance and Operations -sovellukset |
| **Project Operations -integroinnin todelliset arvot (msdyn\_actuals)** | No | No | – | Kyllä | No |
| **Projektin sopimusrivit (salesorderdetails)** | No | No | – | No | No |
| **Projektitapahtuman integrointikohdesuhteet (msdyn\_transactionconnections)** | No | No | – | No | – |
| **Project Operations -integroinnin sopimusrivin välitavoitteet (msdyn\_contractlinesscheduleofvalues)** | No | No | – | No | – |
| **Project Operations -integrointikohde kuluarvioita varten (msdyn\_estimateslines)** | No | No | – | No | – |
| **Project Operations -integroinnin projektikululuokkien vientientiteetti (msdyn\_expensecategories)** | No | No | – | No | – |
| **Project Operations -integroinnin projektikulujen vientientiteetti (msdyn\_expenses)** | Kyllä | No | – | No | – |
| **Project Operations -integrointikohde tuntiarvioita varten (msdyn\_resourceassignments)** | Kyllä | No | – | No | – |


4. Jos haluat päivittää entiteetin, valitse yhdistämismäärityksen nimi ja valitse sitten **Päivitä entiteetit**. 


![Päivitä yhdistämismääritys](./media/20RefreshMapping.png)

5. Suorita yhdistämismääritys, kun päivitys on valmis. Ennen kuin otat seuraavan yhdistämismäärityksen käyttöön, tarkista, että taulukon yhdistämismääritys on tilassa **Käynnissä**. Sellaisten yhdistämismääritysten suorittaminen, joissa on paljon edellytyksiä, voi kestää jonkin aikaa.

Jos haluat suorittaa yhdistämismääritys ja edellytykset, ota käyttöön **Näytä liittyvät entiteetin yhdistämismääritykset** -valintapainike. Jos taulukko osoittaa **Edellytyksen ensimmäinen synkronointi** -kohdaas arvo **Ei**, tarkista, että **Ensimmäinen synkronointi** -merkintä on **Ei käytössä** kaikissa edellytysyhdistämismäärityksissä, ennen kuin suoritat sen.

![Suorita yhdistämismääritys](./media/21RunMap.png)

6. Tarkista, että kaikki projektiin liittyvät yhdistämismääritykset ovat Käynnissä-tilassa.

![Kaikki yhdistämismääritykset käynnissä](./media/22AllMapsRunning.png)


## <a name="apply-configuration-data-in-cds-for-project-operations-optional"></a>Määritystietojen ottaminen käyttöön Project Operationsin CDS:ssä (valinnainen)

Jos olet käyttänyt esittelytietoja Finance-ympäristössä, lisätietoja esittelytietojen käyttämisestä CDS-ympäristössä on kohdassa [Määritystietojen määrittäminen ja käyttäminen Project Operationsin Common Data Servicessa](resource-apply-pro-setup-config-data.md).


Project Operations -ympäristö on nyt valmisteltu ja määritetty. 


[!INCLUDE[footer-include](../includes/footer-banner.md)]