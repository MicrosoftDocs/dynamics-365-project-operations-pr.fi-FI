---
title: Project Operationsin päivittäminen Finance-ympäristössä
description: Tässä artikkelissa on tietoja Project Operationsin päivittämisestä Dynamics 365 Finance -ympäristössä.
author: ruhercul
ms.date: 12/11/2020
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: aedfd815521054d58944496500aa03a27be9267b
ms.sourcegitcommit: a798fed5c59e3fefa62cdfa42c852d529b33fd35
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/18/2022
ms.locfileid: "9030031"
---
# <a name="update-project-operations-in-your-finance-environment"></a>Project Operationsin päivittäminen Finance-ympäristössä

_**Käytetään:** Project Operationsin resursseihin ja ei-varastoitaviin perustuvissa skenaarioissa_


Tässä artikkelissa on tietoja Dynamics 365 Project Operationsin päivittämisestä Dynamics 365 Finance -ympäristössä. Project Operationsin päivittäminen päivitysversioon 5 (UR5) edellyttää kolmea toimenpidettä:

- [Paketin tuominen esiversioprojektiin](#import)
- [Asenna päivitys](#apply)
- [Dataverse-ympäristön päivittäminen](#update)

## <a name="import-the-package-into-your-lcs-project"></a><a name="import"></a>Paketin tuominen LCS-projektiin

1. Kirjaudu [Lifecycle Servicesiin (LCS)](https://lcs.dynamics.com/) projektin omistajana tai ympäristön ylläpitäjänä.
2. Valitse LCS-projektisi projektiluettelosta.
3. Avaa **Projekti**-sivun **Ympäristöt**-ryhmästä se ympäristö, jonka haluat päivittää.
4. Tarkista, että ympäristö on käytössä. Jos sitä ei ole käynnistetty, käynnistä ympäristö.
5. Valitse **Saatavilla olevat päivitukset** -kohdan alla olevasta **Uusi versio** -kohdasta **Näytä päivitys** versiolle 10.0.15.

![Näytä päivitys -painike.](media/view-update.png)

6. Valitse **Binaaripäivitykset**-sivulla **Tallenna paketti**.
7. Valitse **Tarkista ja tallenna päivitykset**-sivulla **Tallenna paketti**.
8. Kirjoita paketin nimi **Tallenna paketti resurssikirjastoon** -ruutuun ja valitse sitten **Tallenna paketti**.
9. Kun LCS on tallentanut paketin, **Valmis**-painike on käytössä. Valitse **Valmis**. LCS tarkistaa paketin. Tarkistaminen voi kestää muutaman minuutin tai jopa tunnin.


## <a name="apply-the-package-update"></a><a name="apply"></a>Asenna päivityspaketti

1. Valitse LCS:ssä **Ympäristön tiedot** -sivulla **Ylläpidä** > **Ota päivitykset käyttöön**.
2. Valitse luettelosta aiemmin tallennettu paketti ja valitse sitten **Käytä**.
3. Vahvista paketin käyttöönotto valitsemalla **Kyllä**.

![Vahvista paketin käyttöönotto -valintaikkuna.](media/confirm-package-deployment.png)

4. Vahvista sovelluksen päivitys valitsemalla **Kyllä**.

![Vahvista sovelluksen päivitys -valintaikkuna.](media/confirm-application-update.png)

Käyttöönotto ja sovelluspäivitys käynnistyy. 

**Ympäristön tiedot** -sivun oikeassa yläkulmassa ympäristön tilaksi päivittyy **Ylläpito**. Päivitys on valmis noin kahden tunnin kuluttua. Sovelluksen julkaisutiedoiksi päivittyy **Microsoft Dynamics 365 for Finance and Operations 10.0.15)** ja ympäristön tilaksi päivittyy **Otettu käyttöön**.


## <a name="update-your-dataverse-environment"></a><a name="update"></a>Dataverse-ympäristön päivittäminen

1. Kirjaudu [Power Platform -hallintakeskukseen](https://admin.powerplatform.com/).
2. Etsi ja avaa luettelosta ympäristö, jota käytit Project Operationsin asentamiseen.
3. Valitse **Ympäristöt**-sivulla **Resurssi** > **Dynamics 365 -sovellukset**.
4. Etsi luettelosta **Microsoft Dynamics 365 Project Operations** ja valitse **Tila**-sarakkeesta **Päivitys saatavilla**.
5. Valitse **Hyväksyn palveluehdot** -valintaruutu ja valitse sitten **Päivitä**. Ratkaisun uusin versio asennetaan.

Kun asennus on valmis, asennettuna on versio 4.5.0.134.

## <a name="configure-new-features"></a>Uusien ominaisuuksien määrittäminen

### <a name="enable-dual-write-mapping"></a>Ota käyttöön kaksoiskirjoituksen yhdistäminen

Kun olet päivittänyt Finance- ja Dataverse-ympäristöt, voit ottaa käyttöön tarvittavat kaksoiskirjoituksen yhdistämiset. Tee seuraavat toimet kaksoiskirjoituksen yhdistämisen käyttöönottamiseksi.

- [Customer Engagement -ympäristön suojausasetusten päivittäminen](#security)
- [Päivitä tietoentiteetit](#refresh)
- [Kaksoiskirjoituksen yhdistämismääritysten päivittäminen ja suorittaminen](#run)

### <a name="update-security-settings-on-the-dataverse-environment"></a><a name="security"></a>Dataverse-ympäristön suojausasetusten päivittäminen

UR5-päivityksessä tarvitaan seuraavat entiteettien suojausoikeuksien päivitykset.

1. Valitse Dataverse-ympäristössä **Asetukset** ja valitse sitten **Järjestelmä**-ryhmästä **Suojaus**.

![Dataversen ympäristöasetukset.](media/Picture21.png)

2. **Käyttöoikeusroolien** valitseminen
3. Valitse rooliluettelosta **kaksoiskirjoitussovelluksen käyttäjä** ja valitse **Mukautetut entiteetit** -välilehti. 
4. Varmista, että roolilla on **Luku**- ja **Lisää kohteeseen** -oikeudet seuraaville:

      - **Valuuttakurssin tyyppi**
      - **Tilikartta** 
      - **Kirjanpitokalenteri** 
      - **Tapahtumarekisteri**

5. Kun käyttöoikeusrooli on päivitetty, valitse **Asetukset** > **Suojaus** > **Ryhmät**. Tarkista, että **kaksoiskirjoitussovelluksen käyttäjä** -rooli on otettu käyttöön ryhmässä. 

### <a name="refresh-data-entities-from-the-update"></a><a name="refresh"></a>Päivitä tietoentiteetit päivityspaketista

1. Avaa Finance-ympäristössä **Tiedonhallinta**-työtila ja avaa sitten **Framework-parametrit**-sivu.
2. Valitse **Entiteettiasetukset**-välilehdessä **Päivitä entiteettiluettelo**.
3. Vahvista entiteetin päivitys valitsemalla **Sulje**.

 > [!NOTE]
 > Tämän prosessin suorittaminen kestää noin 20 minuuttia. Saat ilmoituksen, kun päivitys on valmis.

### <a name="update-dual-write-mappings"></a><a name="run"></a>Päivitä kaksoiskirjoituksen yhdistämismääritykset

1. Valitse **Tiedonhallinta**-työtilassa **Kaksoiskirjoitus**.
2. Valitse **Ota ratkaisut käyttöön**, valitse molemmat ratkaisut luettelosta ja valitse sitten **Käytä**.
3. Valitse **Kaksoiskirjoitus**-sivulla seuraavat taulukkokartat ja valitse sitten **Lopeta**.

    - **Project Operations -integroinnin todelliset arvot (msdyn_actuals)**
    - **Project Operations -integroinnin projektikululuokat (msdyn_expensecategories)**
    - **Project Operations -integroinnin toteutuneiden projektikulujen vientientiteetti (msdyn_expenses)**

4. Ota **Taulukon yhdistämismäärityksen versio** -sivulla käyttöön määrityksen uusi versio kussakin kolmessa entiteetissä.
5. Käynnistä määritykset uudelleen valitsemalla Suorita **Kaksoiskirjoitus**-sivulla.
6. Valitse määritysluettelosta **Tapahtumarekisteri (msdyn_ledgers)** -määritys ja kaikki edellytykset ja valitse sitten **Ensimmäinen synkronointi** -valintaruutu. 
7. Valitse **Ensimmäisen synkronoinnin pääkohde** -kentässä **talous- ja toimintosovellukset** ja valitse sitten **Suorita**.
 
 ![Kirjanpitomäärityksen synkronointi.](media/DW6.png)
 


[!INCLUDE[footer-include](../includes/footer-banner.md)]