---
title: Projektin resurssien aikataulutuksen suorituskyky
description: Tässä aiheessa on tietoja siitä, miten voidaan parantaa resurssien aikatauluttamisen tehokkuutta useissa projekteissa.
author: Yowelle
ms.date: 08/31/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 10.0.14
ms.search.validFrom: 2020-09-01
ms.openlocfilehash: 9dc638a7b2d8e0db45b5acfa5cc9512f356f8b2635028748a1e2c3230605c154
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/06/2021
ms.locfileid: "7007277"
---
# <a name="project-resource-scheduling-performance"></a>Projektin resurssien aikataulutuksen suorituskyky

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]


Resurssiaikataulutukseen liittyviä suorituskykyongelmia voi ilmetä, kun projektien määrä on tuhansia. Resurssien aikataulutuksen tehokkuuden parantamiseksi käytettävissä on toiminto, jonka avulla käyttäjät voivat lyhentää resurssien saatavuuslomakkeen käynnistämiseen kuluvan ajan. Tämä poistaa resurssikapasiteetin koontiprosessin ja nopeuttaa resurssihaun käyttöä **ResProjectResource**-taulukon avulla. Huomaa, että **ResRollup**-taulukkoa ei enää käytetä.

> [!IMPORTANT]
> Jos resurssikapasiteetin koontiprosessissa tai yhteenvetosynkronointiprosessissa on **ResProjectResource**-taulukko, älä käytä tätä ominaisuutta.

## <a name="enable-resource-scheduling-performance-enhancement"></a>Resurssien aikataulutuksen tehokkuuden parantamisen käyttöönotto
Jos haluat ottaa käyttöön resurssien aikataulutuksen tehokkuuden parantamisen, suorita seuraavat vaiheet.

1. Siirry kohtaan **ominaisuuksien hallinta** > **Kaikki** ja etsi ominaisuusluettelosta **Ota käyttöön projektin resurssiajoitussuorituskyvyn parannus** -ominaisuus.
2. Valitse **Ota käyttöön nyt**.

> [!NOTE]
> Jos et löydä ominaisuutta luettelosta, päivitä luettelo valitsemalla **Tarkista päivitykset**.

3. Päivitä selain ja siirry sitten kohtaan **projektinhallinta ja kirjanpito** > **kausittainen** > **Projektiresurssit** > **Synkronoi resurssikalenterit kaikkien yritysten kesken**.
4. Jos haluat poistaa aiemmat tiedot, aseta **Poista nykyiset kapasiteettitietueet** -valinnan arvoksi **Kyllä**. Jos haluat luoda arvon lisätietoja, aseta se arvoksi **Ei**.
5. Valitse **kausikoodi**-kentässä ajanjakso, jolta tiedot on luotava. Jos valitset kausikoodin, aloitus- ja päättymispäivämäärää ei tarvitse määrittää.
6. Jos jätät **kausikoodi**-kentän tyhjäksi, luo tiedot valitsemalla tietyt alkamis- ja päättymispäivämäärät.
7. Valitse **OK**.

 > [!NOTE]
 > Tämä jakaa yleiset tiedot **ResCalendarCapacity**-taulukkoon kaikissa ympäristössäsi olevissa yrityksissä, joten eräajo on suoritettava vain yhdessä yrityksessä. Tämän eräajon tietoja tarvitaan resurssikapasiteetin laskemiseen liitetyn kalenterin kautta.

8. Siirry kohtaan **projektinhallinta ja kirjanpito** > **kausittainen** > **Projektiresurssit** > **Täyttävät projektiresurssit kaikissa yrityksissä**, ja valitse sitten **OK**. Tämä on tietojen päivityskomentosarja yleisille tiedoille, jotka ovat **ResProjectResource**-, **ResCalendarDateTimeRange**- ja **ResEffectiveDateTimeRange**-taulukot. **PSAPRojSchedRole.RootActivity**-kentän arvot päivittyvät myös. Jos tätä ei suoriteta, näyttöön tulee varoitus, kun yrität suorittaa resurssien aikataulutustoimintoja.
 
## <a name="turn-off-resource-scheduling-performance-enhancement"></a>Resurssien aikataulutuksen tehokkuuden parantamisen käytöstä poisto

1. Siirry kohtaan **ominaisuuksien hallinta** > **Kaikki** ja etsi **Ota käyttöön projektin resurssiajoitussuorituskyvyn parannus** -ominaisuus.
2. Valitse toiminto ja valitse sitten **Poista käytöstä** -painike.
3. Päivitä selain.
4. Valitse **Projektinhallinta ja kirjanpito** > **Jaksoittainen** > **Kapasiteetin synkronointi** > **Synkronoi resurssikapasiteettien koonnit**.
5. Voit poistaa aiemmat tiedot määrittämällä **kapasiteetin koonti-synkronointi** -sivulla **Poista nykyiset kapasiteetti tietueet** **Kyllä**-arvoksi. Jos haluat luoda arvon lisätietoja, aseta se arvoksi **Ei**.
6. Valitse **kausikoodi**-kentässä ajanjakso, jolta tiedot on luotava. Jos valitset kausikoodin, aloitus- ja päättymispäivämäärää ei tarvitse määrittää.
7. Jos jätät **kausikoodi**-kentän tyhjäksi, luo tiedot valitsemalla tietyt alkamis- ja päättymispäivämäärät.
8. Valitse **OK**.

> [!NOTE]
> Tämä jakaa yleiset tiedot **ResRollup**-taulukkoon kaikissa ympäristössäsi olevissa yrityksissä, joten eräajo on suoritettava vain yhdessä yrityksessä. Tätä eräajoa tarvitaan kaikissa **resurssin käytettävyys** -näkymissä. Jos tätä eräajoa ei suoriteta, **ResRollup**-tiedot luodaan lennossa, mikä voi viedä aikaa.


[!INCLUDE[footer-include](../includes/footer-banner.md)]