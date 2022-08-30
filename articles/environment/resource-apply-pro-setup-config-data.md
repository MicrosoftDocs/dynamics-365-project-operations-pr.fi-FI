---
title: Määritystietojen määrittäminen ja käyttäminen Microsoft Dataversessa
description: Tässä artikkelissa on tietoja määritystietojen määrittämisestä ja käyttöönotosta Project Operationsissa.
author: sigitac
ms.date: 05/10/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: b09d3ea7348082a0467fd7b47918c9e00d1f1e8c
ms.sourcegitcommit: 8edd24201cded2672cec16cd5dc84c6a3516b6c2
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/06/2022
ms.locfileid: "9230233"
---
# <a name="set-up-and-apply-configuration-data-in-the-common-data-service"></a>Määritystietojen määrittäminen ja käyttäminen Common Data Servicessa 

_**Käytetään:** Project Operationsin resursseihin ja ei-varastoitaviin perustuvissa skenaarioissa_



## <a name="prerequisites"></a>edellytykset

Seuraavien edellytysten on täytyttävä ennen tietojen määrittämisen aloittamista Microsoft Dataversessa:

1.  Valmistele Dataverse-ympäristö ja Dynamics 365 Finance -ympäristö Project Operationsille.
2.  Dynamics 365 Financen yritystiedot jaetaan Dataverse-ympäristöön. Tämän vuoksi Dataversen **Yhtiö**-entiteetillä on seuraavat yhtiötietueet:
  - THPM
  - USPM
  - GBPM

## <a name="install-setup-and-configuration-data"></a>Asenna määritys- ja konfiguraatiotiedot

1. Lataa, poista esto ja pura [Asennus- ja määritystietopaketti](https://download.microsoft.com/download/e/2/d/e2da6c98-d5dd-450c-aabe-fd6bf2ba374b/ProjOpsSampleSetupData-%20Integrated%20Latest.zip).
2. Siirry purettuun kansioon ja suorita suoritettava tiedosto *DataMigrationUtility*.
3. Valitse ohjatussa Common Data Service Configuration Migration (CMT) -toiminnossa sivulla 1 **Tuo tiedot** ja sitten **Jatka**.

![Määrityksen siirto.](./media/1ConfigurationMigration.png)

4. Valitse ohjatun CMT-toiminnon sivulla 2 **Microsoft 365** **asennustyypiksi**.
5. Valitse **Näytä käytettävissä olevien organisaatioiden luettelo** ja **Näytä lisäasetukset** -valintaruutu.
6. Valitse vuokraajan alue, anna tunnistetietosi ja valitse **Kirjaudu**.

![Kirjautuminen määritykseen.](./media/2ConfigurationSignin.png)

7. Valitse sivulla 3 vuokraajan organisaatioiden luettelosta organisaatio, johon haluat tuoda esittelytiedot, ja valitse sitten **Kirjaudu**.
8. Valitse sivulla 4 puretusta kansiosta zip-tiedosto *SampleSetupAndConfigData*.

![Zip-tiedoston valinta.](./media/3ZipFile.png)

![Valitse tiedosto.](./media/4SelectAFile.png)

9. Kun zip-tiedosto on valittu, valitse **Tuo tiedot**.

![Tuo tiedot.](./media/5ImportData.png)

10. Tuonti kestää noin 2-10 minuuttia verkon nopeuden mukaan. Kun tuonti on valmis, sulje ohjattu CMT-toiminto. 
11. Tarkista organisaatiosi tiedot seuraavissa 26 entiteetissä:

  - Valuutta
  - Tilikartta
  - Kirjanpitokalenteri
  - Vaihtokurssien tyypit
  - Maksupäivä
  - Maksuaikataulu
  - Maksuehto
  - Organisaatioyksikkö
  - Ota yhteyttä
  - Veroryhmä
  - Asiakasryhmä
  - Toimittajaryhmä
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

![Suorita tuonti.](./media/6CompleteImport.png)

## <a name="update-project-operations-configurations"></a>Project Operations -määritysten päivittäminen

1. Siirry CE-ympäristöön. Löydät sen avaamalla [Power Platform -hallintakeskuksen](https://admin.powerplatform.microsoft.com/environments), valitsemalla ympäristön ja valitsemalla sitten **Avaa ympäristö**. 

![Avaa ympäristö.](./media/7OpenEnvironment.png)

2. Siirry kohtaan **Projektit** > **Resurssit** ja valitse sitten **Uusi**, jos haluat luoda käyttäjälle varattavissa olevan resurssin.

![Varattavissa olevat resurssit.](./media/8BookableResources.png)

3. Valitse **Yleiset**-välilehdessä järjestelmänvalvojakäyttäjä. Tarkista, että aikavyöhyke vastaa sitä, missä olet. 

![Uusi varattava resurssi.](./media/9NewBookableResource.png)

4. Valitse **Aikataulutus**-välilehden **Yritys**-kentässä **USPM**-yritys ja valitse sitten **Tallenna**. 

![Aikataulutus-välilehti.](./media/10SchedulingTab.png)

5. Valitse **Työtunnit**-välilehti.  

![Työaika.](./media/11WorkHours.png)

6. Kaksoisnapsauta mitä tahansa kalenterin arvoa ja valitse sitten **Muokkaa** > **Kaikki sarjan tapahtumat**. 

![Työkalenteri.](./media/12WorkCalendar.png)

7. Vaihda työaika kahdeksan (8) tunnin työpäivään, merkitse viikonloput ei-työpäiviksi ja varmista, että aikavyöhyke omaasi. 
8. Valitse **Tallenna ja sulje**.

![Päivitä kalenteri.](./media/13UpdateCalendar.png)

9. Siirry kohtaan **Asetukset** > **Kalenterimallit** ja valitse **Uusi**.
 
 ![Kalenterimallit.](./media/14CalendarTemplates.png)
 
 10. Kirjoita nimi, valitse luomasi malliresurssi ja valitse sitten **Tallenna**. 
 
 ![Tallenna kalenterimalli.](./media/15SaveCalendarTemplate.png)
 
 11. Siirry kohtaan **Parametrit** ja kaksoisnapsauta tietuetta. 
 
 ![Projektin parametrit.](./media/16ProjectParameters.png)
 
12. Päivitä seuraavat kentät:

 - **Oletusyritys**: USPM
 - **Oletusorganisaatioyksikkö**: Contoso Robotics Global
 - **Laskutustiheys**: seitsemäs ja viimeinen päivä
 - **Työtuntimalli**: Vaihda luomaasi malliin.

13. Valitse **Tallenna**. 

![Päivitetyt projektin parametrit.](./media/17UpdatedProjectParameters.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
