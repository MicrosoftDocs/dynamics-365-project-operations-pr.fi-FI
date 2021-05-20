---
title: Kulujen hallinnan mobiilityötila
description: Tässä aiheessa on tietoja Kulujen hallinta -mobiilityötilasta. Tässä työtilassa käyttäjä voi siepata ja ladata kuitin myöhempää kuluraporttiin liittämistä varten. Käyttäjät voivat myös nopeasti luoda kulurivin liitetyn kuitin avulla sekä luoda ja hallinnoida kuluraportteja.
author: suvaidya
manager: AnnBe
ms.date: 12/01/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 274023
ms.assetid: 3605eda1-a7ed-4675-8031-5279c5a8f5e4
ms.search.region: Global
ms.author: suvaidya
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.openlocfilehash: cc19297131937949fe6f7eed00ee66fb5e3bff13
ms.sourcegitcommit: 3d78338773929121d17ec3386f6cb67bfb2272cc
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/27/2021
ms.locfileid: "5950475"
---
# <a name="expense-management-mobile-workspace"></a>Kulujen hallinnan mobiilityötila

Tässä aiheessa on tietoja **Kulujen hallinta** -mobiilityötilasta. Tässä työtilassa käyttäjä voi siepata ja ladata kuitin myöhempää kuluraporttiin liittämistä varten. Käyttäjät voivat myös nopeasti luoda kulurivin liitetyn kuitin avulla sekä luoda ja hallinnoida kuluraportteja. Lisäksi hyväksyjät voivat tarkastella heille liitettyjä kuluraportteja **Kulujen hallinta** -mobiilityötilassa sekä hyväksyä tai hylätä kuluraportteja.


Tämä mobiilityötila on tarkoitettu käytettäväksi Dynamics 365 Unified Ops -mobiilisovelluksen kanssa.


## <a name="overview"></a>Yleiskuvaus

Useat organisaatiot edellyttävät, että työntekijän korvausta varten lähettämään matkustukseen tai yrityksen toimintaan liittyvään kuluraporttiin liitetään kopio kuitista. **Kulujen hallinta** -työtilan avulla käyttäjät voivat nopeasti luoda uusia kulurivejä valitsemassaan mobiililaitteessa liitetyn kuitin kuvan avulla. Vaihtoehtoisesti käyttäjät voivat siepata kuvan kuitista ja liittää sen kuluraporttiin myöhemmin. Työntekijät voivat myös luoda ja hallinnoida kuluraportteja sekä lähettää ne mobiililaitteella hyväksyntää ja korvausta varten.


**Kulujen hallinta** -mobiilityötilan avulla käyttäjät voivat siis suorittaa seuraavia tehtäviä:

- Ota valokuva kuitista ja lataa se Dynamics 365 Financeen. Voit liittää valokuvan myöhemmin kuluraporttiin.
- tiedoston lataaminen siepattuna kuittina. Voit liittää tiedoston myöhemmin kuluraporttiin.
- Luo uusi kulurivi liitetyn kuitin avulla. Tämän jälkeen voit lisätä rivinimikkeen matkaraporttiin myöhemmin ja lähettää sen hyväksyntää ja korvausta varten.

Voit käyttää myös seuraavia toimintoja:

- Luo uusi kuluraportti.
- Liitä luottokorttitapahtumia ja muita äskettäin luotuja kuluja kuluraporttiin.
- Luo kuluraporttiin uusia kuluja.
- Liitä kuitti kuluraporttiin ottamalla kuitista kuva tai lataamalla tiedosto siepattuna kuittina.
- Voit lisätä vierasluettelon kuluun, jos yrityksen kulukäytännöt sallivat sen.
- Erittele kulut yrityksen kulukäytännön mukaisesti.
- Lähetä kuluraportti hyväksyntää ja korvausta varten.
- Hyväksy tai hylkää kuluraportit, joiden hyväksyjäksi sinut on määritetty.

## <a name="prerequisites"></a>Edellytykset
Edellytykset vaihtelevat organisaatiossa käyttöön otetun version mukaan.

### <a name="prerequisites-if-you-use-dynamics-365-finance"></a>Edellytykset käytettäessä Dynamics 365 Financea 
Jos organisaatiossasi on otettu käyttöön Finance, järjestelmänvalvojan on julkaistava **Kulujen hallinta** -mobiilityötila. Katso ohjeet kohdasta [Mobiilityötilojen julkaiseminen](/dynamics365/fin-ops-core/dev-itpro/mobile-apps/publish-mobile-workspace).

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
<td>Tietokannan 4019015 käyttöönotto.</td>
<td>Järjestelmänvalvoja</td>
<td>Tietokanta 4019015 on X++-päivitys tai metatietojen hotfix-korjaus, joka sisältää <strong>Kulujen hallinta</strong> -mobiilityötilan. Tietokannan 4019015 käyttöönottoa varten järjestelmänvalvojasi on suoritettava seuraavat vaiheet.
<ol>
<li><a href="/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/install-metadata-hotfix-package#download-the-hotfix-from-lcs">Metatietojen hotfix-korjauksen lataaminen Microsoft Dynamics Lifecycle Services (LCS) palveluista</a>.</li>
<li><a href="/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/install-metadata-hotfix-package#install-the-metadata-hotfix-package">Metatietojen hotfix-korjauksen asentaminen</a>.</li>
<li><a href="/dynamics365/fin-ops-core/dev-itpro/deployment/create-apply-deployable-package">Sellaisen käyttöönotettavan paketin luominen</a>, joka sisältää <strong>ApplicationSuite</strong>- ja <strong>ExpenseMobile</strong>-mallit, ja sitten käyttöönotettavan paketin lataaminen LCS-palveluun.</li>
<li><a href="/dynamics365/fin-ops-core/dev-itpro/deployment/apply-deployable-package-system">Käyttöönotettavan paketin käyttöönotto</a>.</li>
</ol></td>
</tr>
<tr class="even">
<td>Julkaise <strong>Kulujen hallinta</strong> -mobiilityötila.</td>
<td>Järjestelmänvalvoja</td>
<td>Katso <a href="/dynamics365/fin-ops-core/dev-itpro/mobile-apps/publish-mobile-workspace">Mobiilityötilan julkaiseminen </a>.</td>
</tr>
</tbody>
</table>

## <a name="download-and-install-the-dynamics-365-for-operations-mobile-app"></a>Lataa ja asenna Dynamics 365 for Operations -mobiilisovellus
Voit ladata asentaa Dynamics 365 Unified Ops -mobiilisovelluksen seuraavasti:

- [Android-puhelimille](https://go.microsoft.com/fwlink/?linkid=850662)
- [iPhone-puhelimille](https://go.microsoft.com/fwlink/?linkid=850663)

## <a name="sign-in-to-the-mobile-app"></a>Mobiilisovellukseen kirjautuminen
1. Käynnistä sovellus mobiililaitteessa.
2. Syötä Dynamics 365:n URL-osoite.
4. Kun kirjaudut sisään ensimmäisen kerran, sinulta kysytään käyttäjätunnusta ja salasanaa. Anna tunnistetiedot.
5. Kun olet kirjautunut sisään, näkyviin tulevat yrityksessä käytettävissä olevat työtilat. Huomaa, että jos järjestelmänvalvoja julkaisee uuden työtilan myöhemmin, sinun on päivitettävä mobiilityötilojen luettelo.


[![Päivittäminen vetämällä](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)

## <a name="capture-a-receipt-by-using-the-expense-management-mobile-workspace"></a>Kuitin sieppaaminen Kulujen hallinta -mobiilityötilan avulla

1. Avaa mobiililaitteessa **Kulujen hallinta** -työtila.
2. Valitse **Sieppaa kuitti**.
3. Valitse **Ota valokuva** tai **Valitse kuva**.
4. Valitse jokin seuraavista vaiheista:

    - Jos valitsit **Ota valokuva** -kohdan, toimi seuraavasti:

        1. Mobiililaitteen kamera avautuu ja voit ottaa kuvan kuitista. Kun olet ottanut valokuvan, hyväksy se valitsemalla **OK**.
        2. Valinnainen: Anna valokuvalle nimi ja syötä mahdolliset muistiinpanot.

    - Jos valitsit **Valitse kuva** -kohdan, toimi seuraavasti:

        1. Valitse luettelosta kuva.
        2. Valinnainen: Anna kuvalle nimi ja syötä mahdolliset muistiinpanot.

5. Valitse **Valmis**.

## <a name="quickly-enter-expenses-by-using-the-expense-management-mobile-workspace"></a>Kulujen syöttäminen nopeasti Kulujen hallinta -mobiilityötilan avulla
1. Avaa mobiililaitteessa **Kulujen hallinta** -työtila.
2. Valitse **Kulun nopea syöttö**.
3. Valitse kululle luokka. Näkyvissä ovat kululuokat, jotka ladataan sovellukseesi offline-käyttöä varten. Oletusarvoisesti ladataan 50 nimikettä, mutta kehittäjä voi muuttaa tätä määrää. Lisätietoja kehittäjille on kohdassa [Mobiiliympäristö](/dynamics365/fin-ops-core/dev-itpro/mobile-apps/platform/mobile-platform-home-page). Jos luokkaa ei ole luettelossa, valitse **Hae** online-hakua varten. Hae kululuokan mukaan tai vaihda hakuun kulutyypin perusteella.
4. Anna kulun tapahtumapäivämäärä.
5. Valinnainen: Anna kuluun liittyvä myyjä.
6. Anna kulun summa.
7. Valitse kulun valuutta. Näkyvissä ovat valuuttakoodit, jotka ladataan sovellukseesi offline-käyttöä varten. Oletusarvoisesti ladataan 400 valuuttaa, mutta kehittäjä voi muuttaa tätä määrää. Lisätietoja kehittäjille on kohdassa [Mobiiliympäristö](/dynamics365/fin-ops-core/dev-itpro/mobile-apps/platform/mobile-platform-home-page). Jos valuutta ei ole luettelossa, valitse **Hae** online-hakua varten. Hae valuutan mukaan tai vaihda hakuun nimen perusteella.
8. Valitse **Ota valokuva** tai **Valitse kuva**.
9. Valitse jokin seuraavista vaiheista:

    - Jos valitsit **Ota valokuva**, mobiililaitteen kamera avautuu ja voit ottaa kuvan kuitista. Kun olet ottanut valokuvan, hyväksy se valitsemalla **OK**.
    - Jos valitsit **Valitse kuva**, voit valita kuvan luettelosta.

10. Valitse **Valmis**.

## <a name="approve-an-expense-report-by-using-the-expense-management-mobile-workspace-if-you-use-the-july-2017-update"></a>Hyväksy kuluraportti Kulun hallinta -mobiilityötilan avulla (jos käytössä on heinäkuun 2017 päivitys)
1. Avaa mobiililaitteessa **Kulujen hallinta** -työtila.
2. **Kulujen hyväksynnät** näyttää sinulle hyväksyttäväksi delegoitujen kuluraporttien määrän. Määrä päivitetään noin 30 minuutin välein. Valitse **Kulun hyväksynnät**.

    Näkyviin tulee sinulle hyväksyttäväksi delegoitujen kuluraporttien määrä.
    
3. Valitse kuluraportti, jonka kulun tietoja haluat tarkastella.
4. Valitse kulu, jonka tietoja haluat tarkastella. Näkyvissä olevia kulun tietoja ovat kaikki kuitin, vieraan ja erittelyn tiedot.
5. Siirry takaisin **Kuluraportti**-sivulle ja valitse kuluraportin hyväksyntä tai hylkäys.
6. Anna mahdolliset hyväksyntätoimintoa koskevat kommentit.
7. Valitse **Valmis**.

## <a name="create-a-new-expense-report-and-submit-it-for-approval-by-using-the-expense-management-mobile-workspace-if-you-use-the-july-2017-update"></a>Luo uusi kuluraportti ja lähetä se hyväksyttäväksi Kulun hallinta -mobiilityötilan avulla (jos käytössä on heinäkuun 2017 päivitys)
1. Avaa mobiililaitteessa **Kulujen hallinta** -työtila.
2. Valitse **Kulun syöttö**.
3. Valitse **Uusi raportti** tai valitse aiemmin luotu kuluraportti luettelosta.
4. Syötä uusille kuluraporteille tarkoitus ja mahdolliset lisätiedot. Nämä tiedot vaihtelevat sen mukaan, miten kulujen hallinta on määritetty yrityksessä.
5. Valitse **Valmis**.
6. Jos haluat lisätä kuluraporttiin olemassa olevia kuluja, kuten luottokorttitapahtumia, valitse **Liitä**.
7. Valitse luettelosta vähintään kulu.
8. Valitse **Valmis**.
9. Jos haluat lisätä kuluraporttiin uuden kulun, valitse **Uusi kulu**.
10. Valitse kululle luokka. Näkyvissä ovat kululuokat, jotka ladataan sovellukseesi offline-käyttöä varten. Oletusarvoisesti ladataan 50 nimikettä, mutta kehittäjä voi muuttaa tätä määrää. Lisätietoja kehittäjille on kohdassa [Mobiiliympäristö](/dynamics365/fin-ops-core/dev-itpro/mobile-apps/platform/mobile-platform-home-page). Jos luokkaa ei ole luettelossa, valitse **Hae** online-hakua varten. Hae kululuokan mukaan tai vaihda hakuun kulutyypin perusteella.
11. Valinnainen: Anna kuluun liittyvä myyjä.
12. Anna kulun tapahtumapäivämäärä.
13. Anna kulun summa.
14. Valitse kulun valuutta. Näkyvissä ovat valuuttakoodit, jotka ladataan sovellukseesi offline-käyttöä varten. Oletusarvoisesti ladataan 400 valuuttaa, mutta kehittäjä voi muuttaa tätä määrää. Lisätietoja kehittäjille on kohdassa [Mobiiliympäristö](/dynamics365/fin-ops-core/dev-itpro/mobile-apps/platform/mobile-platform-home-page). Jos valuutta ei ole luettelossa, valitse **Hae** online-hakua varten. Hae valuutan mukaan tai vaihda hakuun nimen perusteella.
15. Valitse **Valmis**.
16. Jos haluat lisätä kuluja koskevia tietoja, valitse **Lisää tietoja**. Käytettävissä olevat kentät määräytyvät yrityksen kulujen hallinnan määrityksen mukaan.
17. Jos yrityskäytäntö edellyttää kululle kuitin, valitse **Kuitit** ja tee seuraavat toiminnot:

    1. Valitse **Sieppaa kuitti** tai **Liitä kuitti**.
    2. Valitse jokin seuraavista vaiheista:

        - Jos valitsit **Sieppaa kuitti** -kohdan, toimi seuraavasti:

            1. Valitse **Ota valokuva** tai **Valitse kuva**.
            2. Valitse jokin seuraavista vaiheista:

                - Jos valitsit **Ota valokuva** -kohdan, toimi seuraavasti:

                    1. Mobiililaitteen kamera avautuu ja voit ottaa kuvan kuitista. Kun olet ottanut valokuvan, hyväksy se valitsemalla **OK**.
                    2. Valinnainen: Anna valokuvalle nimi ja syötä mahdolliset muistiinpanot.

                - Jos valitsit **Valitse kuva** -kohdan, toimi seuraavasti:

                    1. Valitse luettelosta kuva.
                    2. Valinnainen: Anna kuvalle nimi ja syötä mahdolliset muistiinpanot.

            3.  Valitse **Valmis**.

        - Jos valitsit **Liitä kuitti** -kohdan, toimi seuraavasti:

            1.  Valitse luettelosta vähintään yksi kuva.
            2.  Valitse **Valmis**.

    3. Valitse **Takaisin**-painike, jos haluat palata kulun tietoihin.

18. Jos yrityskäytäntö edellyttää kululle vieraat, valitse **Vieraat** ja tee seuraavat toiminnot:

    1. Valitse **Vieras**, **Edelliset vieraat** tai **Työtoverit**.
    2. Valitse jokin seuraavista vaiheista:

        - Jos valitsit **Vieras**-kohdan, toimi seuraavasti:

            1. Kirjoita vieraan nimi.
            2. Valinnainen: Anna vieraalle organisaatio ja/tai maa.
            3. Valinnainen: Kirjoita vieraan nimike.
            4. Valitse **Valmis**.

        - Jos valitsit **Edelliset vieraat** -kohdan, toimi seuraavasti:

            1. Valitse luettelosta vähintään yksi edellinen vieras. Näkyviin tulee sovellukseen offline-tilaa varten ladattuihin edellisiin kuluraportteihin lisättyjen aiempien vieraiden luettelo. Oletusarvoisesti ladataan 50 nimikettä, mutta kehittäjä voi muuttaa tätä määrää. Lisätietoja kehittäjille on kohdassa [Mobiiliympäristö](/dynamics365/fin-ops-core/dev-itpro/mobile-apps/platform/mobile-platform-home-page). Jos edellinen vieras ei ole luettelossa, valitse **Hae** online-hakua varten. Hae nimen mukaan tai vaihda hakuun organisaation, maan tai nimikkeen perusteella.
            2. Valitse **Valmis**.

        - Jos valitsit **Työtoverit**-kohdan, toimi seuraavasti:

            1. Valitse luettelosta vähintään yksi työntekijä. Näkyvissä ovat työntekijät, jotka ladataan sovellukseesi offline-käyttöä varten. Oletusarvoisesti ladataan 50 nimikettä, mutta kehittäjä voi muuttaa tätä määrää. Lisätietoja kehittäjille on kohdassa [Mobiiliympäristö](/dynamics365/fin-ops-core/dev-itpro/mobile-apps/platform/mobile-platform-home-page). Jos työtoveri ei ole luettelossa, valitse **Hae** online-hakua varten. Hae nimen mukaan tai vaihda hakuun yrityksen tai nimikkeen perusteella.
            2. Valitse **Valmis**.

    3. Valitse **Takaisin**-painike, jos haluat palata kulun tietoihin.

19. Jos yrityskäytäntö edellyttää, että kulu on eriteltävä, valitse **Erittele** ja tee seuraavat toiminnot:

    1. Valitse ensimmäinen päivämäärä, jonka mukaan erittely tehdään.
    2. Valitse **Lisää erittely**.
    3. Valitse kulun erittelylle aliluokka. Näkyvissä ovat kulun aliluokat, jotka ladataan sovellukseesi offline-käyttöä varten. Oletusarvoisesti ladataan 50 nimikettä, mutta kehittäjä voi muuttaa tätä määrää. Lisätietoja kehittäjille on kohdassa [Mobiiliympäristö](/dynamics365/fin-ops-core/dev-itpro/mobile-apps/platform/mobile-platform-home-page). Jos aliluokkaa ei ole luettelossa, valitse **Hae** online-hakua varten. Hae kulun aliluokan nimen mukaan.
    4. Kirjoita erittelyn tapahtuman summa.
    5. Muokkaa tapahtumapäivämäärää, jos se on pakollinen.
    6. Valitse **Valmis**.
    7. Toista edelliset vaiheet, kunnes olet lisännyt kaikki valitun päivämäärän erittelyt.
    8. Voit kopioida erittelyitä seuraavaan päivään lisäpäiviä varten valitsemalla **Kopioi seuraavaan päivään** -kohdan. Vaihtoehtoisesti voit valita päivämäärän, joka eritellään, ja lisätä sitten erittelyn kuten ensimmäisen päivämäärän kohdalla.
    9. Kun olet lopettanut kulun erittelyn, valitse **Takaisin**-painike ja palaa kulun tietoihin.

20. Valitse **Takaisin**-painike, jos haluat palata **Kuluraportti**-sivulle.
21. Toista edelliset vaiheet, kunnes olet lisännyt kaikki kulut.
22. Valitse **Lähetä**.
23. Anna mahdolliset hyväksyjää koskevat kommentit.
24. Valitse **Valmis**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]