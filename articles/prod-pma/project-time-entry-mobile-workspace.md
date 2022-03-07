---
title: Project Time Entry -mobiilityötila
description: Tässä aiheessa on tietoja Project Time Entry -mobiilityötilasta. Tämän työtilan avulla käyttäjät voivat kirjata ja tallentaa aikaa projektiin mobiililaitteellaan.
author: Yowelle
ms.date: 12/01/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 272101
ms.assetid: 4505f021-b9bb-4b87-be24-6bf0bd88ee60
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.openlocfilehash: 04024cc005b67b8f4e5821b22be65cfd1822b2414c85e1fbb75c3b2ac4339dc4
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/06/2021
ms.locfileid: "6989547"
---
# <a name="project-time-entry-mobile-workspace"></a>Project Time Entry -mobiilityötila

[!include [banner](../includes/banner.md)]

Tässä aiheessa on tietoja **Project Time Entry** -mobiilityötilasta. Tämän työtilan avulla käyttäjät voivat kirjata ja tallentaa aikaa projektiin mobiililaitteellaan.

Tämä mobiilityötila on tarkoitettu käytettäväksi Dynamics 365 Unified Ops -mobiilisovelluksen kanssa. 

## <a name="overview"></a>Yleiskatsaus
Osana päivittäistä työtään projektiresurssit ovat usein asiakkaan tiloissa tai matkustamassa. **Project Time Entry** -mobiilityötilan avulla käyttäjät voivat määrittää laskutettavat ja ei-laskutettavat työtuntinsa projektissa valitsemallaan mobiililaitteella. Siksi projektiresurssit voivat kirjata työaikoja milloin ja missä tahansa. He voivat myös tarkastella jo kirjattuja aikamerkintöjä. 

Tarkat tehtävät, joita käyttäjät voivat suorittaa **Project Time Entry** -mobiilityötilassa:

-   Tiettyyn tehtävään käytettyjen työtuntien kirjaaminen mille tahansa päivämäärälle.
-   Projektien haku työaikojen kirjausta varten projektin nimen tai asiakkaan perusteella.
-   Käytetäyn ajan luokan ja aktiviteetin määrittäminen.
-   Ajan kirjaaminen projektiin laskutettavaksi tai ei-laskutettavaksi.
-   Vaihtoehtoiesesti ulkoisten tai sisäisten kommenttien lisääminen.

## <a name="prerequisites"></a>Edellytykset
Edellytykset vaihtelevat organisaatiossa käyttöön otetun Microsoft Dynamics 365 -version mukaan.

### <a name="prerequisites-if-you-use-dynamics-365-finance"></a>Edellytykset käytettäessä Dynamics 365 Financea
Jos organisaatiossasi on otettu käyttöön Finance, järjestelmänvalvojan on julkaistava **Project Time Entry** -mobiilityötila. Ohjeet [Mobiilityötilan julkaiseminen ](/dynamics365/fin-ops-core/dev-itpro/mobile-apps/publish-mobile-workspace).

### <a name="prerequisites-if-you-use-version-1611-with-platform-update-3-or-later"></a>Edellytykset, jos käytössä on versio 1611 ja Platform Update 3 tai uudempi
Jos organisaatiossasi on otettu käyttöön versio 1611, jossa on Platform Update 3 tai uudempi, järjestelmänvalvoja on täytettävä seuraavat edellytykset. 

<table>
<thead>
<tr class="header">
<th>Edellytykset</th>
<th>Rooli</th>
<th>Kuvaus</th>
</tr>
</thead>
<tbody>
<tr class="odd">

<td>Tietokannan 4018050 käyttöönotto.</td>
<td>Järjestelmänvalvoja</td>
<td>Tietokanta 4018050 on X++-päivitys tai metatietojen hotfix-korjaus, joka sisältää <strong>Project Time Entry</strong> -mobiilityötilan. Tietokannan 4018050 käyttöönottoa varten järjestelmänvalvojasi on suoritettava seuraavat vaiheet.
<ol>
<li><a href="/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/download-hotfix-lcs">Metatietojen hotfix-korjauksen lataaminen Microsoft Dynamics Lifecycle Services (LCS) palveluista</a>.</li>
<li><a href="/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/install-metadata-hotfix-package">Metatietojen hotfix-korjauksen asentaminen</a>.</li>
<li><a href="/dynamics365/fin-ops-core/dev-itpro/deployment/create-apply-deployable-package">Sellaisen käyttöönotettavan paketin luominen</a>, joka sisältää mallit <strong>ApplicationSuite</strong> ja <strong>ProjectMobile</strong>, ja sitten käyttöönotettavan paketin lataaminen LCS-palveluun.</li>
<li><a href="/dynamics365/fin-ops-core/dev-itpro/deployment/apply-deployable-package-system">Käyttöönotettavan paketin käyttöönotto</a>.</li>

</ol></td>
</tr>
<tr class="even">
<td><strong>Project Time Entry</strong> -mobiilityötilan julkaiseminen.</td>
<td>Järjestelmänvalvoja</td>
<td>Katso <a href="/dynamics365/fin-ops-core/dev-itpro/mobile-apps/publish-mobile-workspace">Mobiilityötilan julkaiseminen </a>.</td>
</tr>
</tbody>
</table>

## <a name="download-and-install-the-mobile-app"></a>Mobiilisovelluksen lataaminen ja asennus

Lataa ja asenna Finance and Operations -mobiilisovellus:

-   [Android-puhelimille](https://go.microsoft.com/fwlink/?linkid=850662)
-   [iPhone-puhelimille](https://go.microsoft.com/fwlink/?linkid=850663)

## <a name="sign-in-to-the-mobile-app"></a>Mobiilisovellukseen kirjautuminen
1.  Käynnistä sovellus mobiililaitteessa.
2.  Syötä Dynamics 365:n URL-osoite.
3.  Kun kirjaudut sisään ensimmäisen kerran, sinulta kysytään käyttäjätunnusta ja salasanaa. Anna tunnistetiedot.
4.  Kun olet kirjautunut sisään, näkyviin tulevat yrityksessä käytettävissä olevat työtilat. Huomaa, että jos järjestelmänvalvoja julkaisee uuden työtilan myöhemmin, sinun on päivitettävä mobiilityötilojen luettelo.

[![Päivittäminen vetämällä.](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)

## <a name="enter-time-by-using-the-project-time-entry-mobile-workspace"></a>Ajan kirjaaminen käyttämällä Project Time Entry -mobiilityötilaa
1.  Valitse mobiililaitteessa **Project Time Entry** -työtila.
2.  Valitse **Aikamerkintä**. Näkyviin tulevat kuluvan viikon kalenteripäivät.
3.  Valitse valitulle päivämäärälle **toiminnot** &gt; **Uusi merkintä**.
4.  Syötä tallennettavien tuntien määrä.
5.  Valitse aikamerkinnän projekti. Luettelossa näkyvät projektit, jotka ladataan sovellukseesi offline-käyttöä varten. Oletusarvoisesti ladataan 50 nimikettä, mutta kehittäjä voi muuttaa tätä määrää. Lisätietoja: [Mobiiliympäristö](/dynamics365/fin-ops-core/dev-itpro/mobile-apps/mobile-app-home-page).
6.  Jos projektia ei ole luettelossa, valitse **Hae**. Hae nimen mukaan tai vaihda hakuun projektin nimen tai asiakkaan perusteella.
7.  Valitse luokka . Luettelossa näkyvät luokat, jotka ladataan sovellukseesi offline-käyttöä varten. Oletusarvoisesti ladataan 50 nimikettä, mutta kehittäjä voi muuttaa tätä määrää. Lisätietoja: [Mobiiliympäristö](/dynamics365/fin-ops-core/dev-itpro/mobile-apps/mobile-app-home-page).
8.  Jos luokkaa ei ole luettelossa, valitse **Hae**. Hae luokan mukaan tai vaihda hakuun luokan nimen perusteella.
9.  Valitse aktiviteetti. Luettelossa näkyvät aktiviteetit, jotka ladataan sovellukseesi offline-käyttöä varten. Oletusarvoisesti ladataan 50 nimikettä, mutta kehittäjä voi muuttaa tätä määrää. Lisätietoja: [Mobiiliympäristö](/dynamics365/fin-ops-core/dev-itpro/mobile-apps/mobile-app-home-page).
10. Jos aktiviteettia ei ole luettelossa, valitse **Hae**. Hae aktiviteetin numeron mukaan tai vaihda hakuun tarkoituksen mukaan.

11. Valitse riviominaisuus.
12. Valinnaista: Lisää ulkoisia ja sisäisiä kommentteja.
13. Valitse **Valmis**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]