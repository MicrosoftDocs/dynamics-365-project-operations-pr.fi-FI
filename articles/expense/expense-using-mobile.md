---
title: Mobiililaitteen käyttämisen kulu
description: Tässä aiheessa on tietoja Kulujen hallinta -mobiilityötilasta.
author: suvaidya
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: ''
ms.author: shylaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 3185c80c792dfe537f4974fa276eafbd16813131
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/28/2020
ms.locfileid: "3897042"
---
# <a name="expense-using-mobile"></a>Mobiililaitteen käyttämisen kulu

_**Koskee:** Project Operationsin resurssiin / muuhun kuin resurssiin perustuvia skenaarioita, Lite-käyttöönotto-kaupasta proformalaskutukseen_

Tässä aiheessa on tietoja **Kulujen hallinta** -mobiilityötilasta. Tässä työtilassa käyttäjä voi siepata ja ladata kuitin myöhempää kuluraporttiin liittämistä varten. Käyttäjät voivat myös nopeasti luoda kulurivin liitetyn kuitin avulla sekä luoda ja hallinnoida kuluraportteja. Lisäksi hyväksyjät voivat tarkastella heille liitettyjä kuluraportteja **Kulujen hallinta** -mobiilityötilassa sekä hyväksyä tai hylätä kuluraportteja.

Tämä mobiilityötila on tarkoitettu käytettäväksi Dynamics 365 Unified Ops -mobiilisovelluksen kanssa.

Useat organisaatiot edellyttävät, että työntekijän korvausta varten lähettämään matkustukseen tai yrityksen toimintaan liittyvään kuluraporttiin liitetään kopio kuitista. **Kulujen hallinta** -työtilan avulla käyttäjät voivat nopeasti luoda uusia kulurivejä valitsemassaan mobiililaitteessa liitetyn kuitin kuvan avulla. Vaihtoehtoisesti käyttäjät voivat siepata kuvan kuitista ja liittää sen kuluraporttiin myöhemmin. Työntekijät voivat myös luoda ja hallinnoida kuluraportteja sekä lähettää ne mobiililaitteella hyväksyntää ja korvausta varten.

**Kulujen hallinta** -mobiilityötilan avulla käyttäjät voivat siis suorittaa seuraavia tehtäviä:

- valokuvan ottaminen kuitista kuitin kuvan lataaminen ja liittäminen kuluraporttiin myöhemmin
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
Jos organisaatiossasi on otettu käyttöön Finance, järjestelmänvalvojan on julkaistava **Kulujen hallinta** -mobiilityötila. 

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
<li><a href="https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/download-hotfix-lcs">Päivitysten lataaminen Lifecycle Servicesestä</a>.</li>
<li><a href="https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/install-metadata-hotfix-package">Metatietojen hotfix-korjauksen asentaminen</a>.</li>
<li><a href="https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/create-apply-deployable-package">Sellaisen käyttöönotettavan paketin luominen</a>, joka sisältää <strong>ApplicationSuite</strong>- ja <strong>ExpenseMobile</strong>-mallit, ja sitten käyttöönotettavan paketin lataaminen LCS-palveluun.</li>
<li><a href="https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/apply-deployable-package-system">Käyttöönotettavan paketin käyttöönotto</a>.</li>
</ol></td>
</tr>
<tr class="even">
<td>Julkaise <strong>Kulujen hallinta</strong> -mobiilityötila.</td>
<td>Järjestelmänvalvoja</td>
<td>Katso <a href="https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/mobile-apps/publish-mobile-workspace">Mobiilityötilan julkaiseminen </a>.</td>
</tr>
</tbody>
</table>

## <a name="download-and-install-the-dynamics-365-unified-ops-mobile-app"></a>Dynamics 365 Unified Ops -mobiilisovelluksen lataaminen ja asentaminen
Voit ladata asentaa Dynamics 365 Unified Ops -mobiilisovelluksen seuraavasti:

- [Android-puhelimille](https://go.microsoft.com/fwlink/?linkid=850662)
- [iPhone-puhelimille](https://go.microsoft.com/fwlink/?linkid=850663)

## <a name="sign-in-to-the-mobile-app"></a>Mobiilisovellukseen kirjautuminen
1. Käynnistä sovellus mobiililaitteessa.
2. Syötä Dynamics 365:n URL-osoite.
4. Kun kirjaudut sisään ensimmäisen kerran, sinulta kysytään käyttäjätunnusta ja salasanaa. Anna tunnistetiedot.
5. Kun olet kirjautunut sisään, näkyviin tulevat yrityksessä käytettävissä olevat työtilat. Jos järjestelmänvalvoja julkaisee uuden työtilan myöhemmin, sinun on päivitettävä mobiilityötilojen luettelo.

## <a name="capture-a-receipt-by-using-the-expense-management-mobile-workspace"></a>Kuitin sieppaaminen Kulujen hallinta -mobiilityötilan avulla

1. Avaa mobiililaitteessa **Kulujen hallinta** -työtila.
2. Valitse **Sieppaa kuitti**.
3. Valitse **Ota valokuva** tai **Valitse kuva**.
4. Valitse jokin seuraavista vaiheista:

   - Jos valitsit **Ota valokuva** -kohdan, toimi seuraavasti:

      1. Mobiililaitteen kamera avautuu ja voit ottaa kuvan kuitista. 
      2. Kun olet ottanut valokuvan, hyväksy se valitsemalla **OK**.
      3. Valinnainen: Anna valokuvalle nimi ja syötä mahdolliset muistiinpanot.

    - Jos valitsit **Valitse kuva** -kohdan, toimi seuraavasti:

        1. Valitse luettelosta kuva.
        2. Valinnainen: Anna kuvalle nimi ja syötä mahdolliset muistiinpanot.

5. Valitse **Valmis**.

## <a name="quickly-enter-expenses-by-using-the-expense-management-mobile-workspace"></a>Kulujen syöttäminen nopeasti Kulujen hallinta -mobiilityötilan avulla

1. Avaa mobiililaitteessa **Kulujen hallinta** -työtila.
2. Valitse **Kulun nopea syöttö**.
3. Valitse kululuokka. Näkyvissä ovat kululuokat, jotka ladataan sovellukseesi offline-käyttöä varten. Oletusarvoisesti ladataan 50 nimikettä, mutta kehittäjä voi muuttaa tätä määrää. Lisätietoja kehittäjille on kohdassa [Mobiiliympäristö](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/mobile-apps/platform/mobile-platform-getting-started). Jos luokkaa ei ole luettelossa, valitse **Hae** online-hakua varten. Hae kululuokan mukaan tai vaihda hakuun kulutyypin perusteella.
4. Anna kulun tapahtumapäivämäärä.
5. Valinnainen: Anna kuluun liittyvä myyjä.
6. Anna kulun summa.
7. Valitse kulun valuutta. Näkyvissä ovat valuuttakoodit, jotka ladataan sovellukseesi offline-käyttöä varten. Oletusarvoisesti ladataan 400 valuuttaa, mutta kehittäjä voi muuttaa tätä määrää. Lisätietoja kehittäjille on kohdassa [Mobiiliympäristö](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/mobile-apps/platform/mobile-platform-getting-started). Jos valuutta ei ole luettelossa, valitse **Hae** online-hakua varten. Hae valuutan mukaan tai vaihda hakuun nimen perusteella.
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
10. Valitse kululle luokka. Näkyvissä ovat kululuokat, jotka ladataan sovellukseesi offline-käyttöä varten. Oletusarvoisesti ladataan 50 nimikettä, mutta kehittäjä voi muuttaa tätä määrää. Lisätietoja kehittäjille on kohdassa [Mobiiliympäristö](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/mobile-apps/platform/mobile-platform-getting-started). Jos luokkaa ei ole luettelossa, valitse **Hae** online-hakua varten. Hae kululuokan mukaan tai vaihda hakuun kulutyypin perusteella.
11. Valinnainen: Anna kuluun liittyvä myyjä.
12. Anna kulun tapahtumapäivämäärä.
13. Anna kulun summa.
14. Valitse kulun valuutta. Näkyvissä ovat valuuttakoodit, jotka ladataan sovellukseesi offline-käyttöä varten. Oletusarvoisesti ladataan 400 valuuttaa, mutta kehittäjä voi muuttaa tätä määrää. Lisätietoja kehittäjille on kohdassa [Mobiiliympäristö](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/mobile-apps/platform/mobile-platform-getting-started). Jos valuutta ei ole luettelossa, valitse **Hae** online-hakua varten. Hae valuutan mukaan tai vaihda hakuun nimen perusteella.
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

            1. Valitse luettelosta vähintään yksi edellinen vieras. Näkyviin tulee sovellukseen offline-tilaa varten ladattuihin edellisiin kuluraportteihin lisättyjen aiempien vieraiden luettelo. Oletusarvoisesti ladataan 50 nimikettä, mutta kehittäjä voi muuttaa tätä määrää. Lisätietoja kehittäjille on kohdassa [Mobiiliympäristö](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/mobile-apps/platform/mobile-platform-getting-started). Jos edellinen vieras ei ole luettelossa, valitse **Hae** online-hakua varten. Hae nimen mukaan tai vaihda hakuun organisaation, maan tai nimikkeen perusteella.
            2. Valitse **Valmis**.

        - Jos valitsit **Työtoverit**-kohdan, toimi seuraavasti:

            1. Valitse luettelosta vähintään yksi työntekijä. Näkyvissä ovat työntekijät, jotka ladataan sovellukseesi offline-käyttöä varten. Oletusarvoisesti ladataan 50 nimikettä, mutta kehittäjä voi muuttaa tätä määrää. Lisätietoja kehittäjille on kohdassa [Mobiiliympäristö](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/mobile-apps/platform/mobile-platform-getting-started). Jos työtoveri ei ole luettelossa, valitse **Hae** online-hakua varten. Hae nimen mukaan tai vaihda hakuun yrityksen tai nimikkeen perusteella.
            2. Valitse **Valmis**.

    3. Valitse **Takaisin**-painike, jos haluat palata kulun tietoihin.

19. Jos yrityskäytäntö edellyttää, että kulu on eriteltävä, valitse **Erittele** ja tee seuraavat toiminnot:

    1. Valitse ensimmäinen päivämäärä, jonka mukaan erittely tehdään.
    2. Valitse **Lisää erittely**.
    3. Valitse kulun erittelylle aliluokka. Näkyvissä ovat kulun aliluokat, jotka ladataan sovellukseesi offline-käyttöä varten. Oletusarvoisesti ladataan 50 nimikettä, mutta kehittäjä voi muuttaa tätä määrää. Lisätietoja kehittäjille on kohdassa [Mobiiliympäristö](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/mobile-apps/platform/mobile-platform-getting-started). Jos aliluokkaa ei ole luettelossa, valitse **Hae** online-hakua varten. Hae kulun aliluokan nimen mukaan.
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
