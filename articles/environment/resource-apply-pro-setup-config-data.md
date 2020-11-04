---
title: Aseta määritystiedot ja ota ne käyttöön Common Data Service for Project Operationsissa
description: Tässä aiheessa on tietoja määritystietojen määrittämisestä ja käyttöönotosta Project Operationsissa.
author: sigitac
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 5e72b88a4dae1eb89859fdfd55f6d5e6ee5befcd
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/16/2020
ms.locfileid: "4075221"
---
# <a name="set-up-and-apply-configuration-data-in-the-common-data-service-for-project-operations"></a>Aseta määritystiedot ja ota ne käyttöön Common Data Service for Project Operationsissa

_**Käytetään:** Project Operationsin resursseihin ja ei-varastoitaviin perustuvissa skenaarioissa_

## <a name="install-setup-and-configuration-data"></a>Asenna määritys- ja konfiguraatiotiedot

1. Lataa, poista esto ja pura [Asennus- ja määritystietopaketti](https://download.microsoft.com/download/1/3/4/1349369c-6209-42b7-b3b4-5be0e67cacd8/ProjOpsSampleSetupData-%20Integrated%20UR1.zip).
2. Siirry purettuun kansioon ja suorita suoritettava tiedosto *DataMigrationUtility*.
3. Valitse ohjatussa Common Data Service Configuration Migration (CMT) -toiminnossa sivulla 1 **Tuo tiedot** ja sitten **Jatka**.

![Määrityksen siirto](./media/1ConfigurationMigration.png)

4. Valitse ohjatun CMT-toiminnon sivulla 2 **Microsoft 365** **Käyttöönottotyypiksi**.
5. Valitse **Näytä käytettävissä olevien organisaatioiden luettelo** ja **Näytä lisäasetukset** -valintaruutu.
6. Valitse vuokraajan alue, anna tunnistetietosi ja valitse **Kirjaudu**.

![Kirjautuminen määritykseen](./media/2ConfigurationSignin.png)

7. Valitse sivulla 3 vuokraajan organisaatioiden luettelosta organisaatio, johon haluat tuoda esittelytiedot, ja valitse sitten **Kirjaudu**.
8. Valitse sivulla 4 puretusta kansiosta zip-tiedosto *SampleSetupAndConfigData*.

![Zip-tiedoston valinta](./media/3ZipFile.png)

![Valitse tiedosto](./media/4SelectAFile.png)

9. Kun zip-tiedosto on valittu, valitse **Tuo tiedot**.

![Tuo tiedot](./media/5ImportData.png)

10. Tuonti kestää noin 2-10 minuuttia verkon nopeuden mukaan. Kun tuonti on valmis, sulje ohjattu CMT-toiminto. 
11. Tarkista organisaatiosi tiedot seuraavissa 19 entiteetissä:

  - Valuutta
  - Organisaatioyksikkö
  - Ota yhteyttä
  - Veroryhmä
  - Asiakasryhmä
  - Yksikkö
  - Yksikköryhmä
  - Hinnasto
  - Projektin parametrin hinnasto
  - Laskutustiheys
  - Varattavissa olevan resurssin luokka
  - Tapahtumakategoria
  - Kululuokka
  - Roolin hinta
  - Tapahtumaluokan hinta
  - Ominaisuus
  - Varattavissa oleva resurssi
  - Varattavissa olevan resurssin luokkaliitos
  - Varattavissa olevan resurssin ominaisuus

![Suorita tuonti](./media/6CompleteImport.png)

## <a name="update-project-operations-configurations"></a>Project Operations -määritysten päivittäminen

1. Siirry CE-ympäristöön. Löydät sen avaamalla [Power Platform -hallintakeskuksen](https://admin.powerplatform.microsoft.com/environments), valitsemalla ympäristön ja valitsemalla sitten **Avaa ympäristö**. 

![Avaa ympäristö](./media/7OpenEnvironment.png)

2. Siirry kohtaan **Projektit** > **Resurssit** ja valitse sitten **Uusi** , jos haluat luoda käyttäjälle varattavissa olevan resurssin.

![Varattavissa olevat resurssit](./media/8BookableResources.png)

3. Valitse **Yleiset** -välilehdessä järjestelmänvalvojakäyttäjä. Tarkista, että aikavyöhyke vastaa sitä, missä olet. 

![Uusi varattava resurssi](./media/9NewBookableResource.png)

4. Valitse **Aikataulutus** -välilehden **Yritys** -kentässä **USPM** -yritys ja valitse sitten **Tallenna**. 

![Aikataulutus-välilehti](./media/10SchedulingTab.png)

5. Valitse **Työtunnit** -välilehti.  

![Työaika](./media/11WorkHours.png)

6. Kaksoisnapsauta mitä tahansa kalenterin arvoa ja valitse sitten **Muokkaa** > **Kaikki sarjan tapahtumat**. 

![Työkalenteri](./media/12WorkCalendar.png)

7. Vaihda työaika kahdeksan (8) tunnin työpäivään, merkitse viikonloput ei-työpäiviksi ja varmista, että aikavyöhyke omaasi. 
8. Valitse **Tallenna ja sulje**.

![Päivitä kalenteri](./media/13UpdateCalendar.png)

9. Siirry kohtaan **Asetukset** > **Kalenterimallit** ja valitse **Uusi**.
 
 ![Kalenterimallit](./media/14CalendarTemplates.png)
 
 10. Kirjoita nimi, valitse luomasi malliresurssi ja valitse sitten **Tallenna**. 
 
 ![Tallenna kalenterimalli](./media/15SaveCalendarTemplate.png)
 
 11. Siirry kohtaan **Parametrit** ja kaksoisnapsauta tietuetta. 
 
 ![Projektin parametrit](./media/16ProjectParameters.png)
 
12. Päivitä seuraavat kentät:

 - **Oletusyritys** : USPM
 - **Oletusorganisaatioyksikkö** : Contoso Robotics Global
 - **Laskutustiheys** : seitsemäs ja viimeinen päivä
 - **Työtuntimalli** : Vaihda luomaasi malliin.

13. Valitse **Tallenna**. 

![Päivitetyt projektin parametrit](./media/17UpdatedProjectParameters.png)
