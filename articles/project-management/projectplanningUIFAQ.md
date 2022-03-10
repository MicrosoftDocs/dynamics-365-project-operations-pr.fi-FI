---
title: Tehtäväruudukossa työskentelyn vianmääritys
description: Tässä aihe sisältää vianmääritystietoja, joita tarvitaan tehtäväruudukossa.
author: ruhercul
ms.date: 09/22/2021
ms.topic: article
ms.product: ''
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 67136229d84a09886fffe9677b10f671aea3c393
ms.sourcegitcommit: 74a7e1c9c338fb8a4b0ad57c5560a88b6e02d0b2
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/23/2021
ms.locfileid: "7547195"
---
# <a name="troubleshoot-working-in-the-task-grid"></a>Tehtäväruudukossa työskentelyn vianmääritys 


_**Koskee seuraavaa:** Project Operations resursseihin/ei-varastoitaviin perustuville skenaarioille, lite-käyttöönotto - tarjouksesta proformalaskutukseen, Project for the web_

Tehtäväruudukko Dynamics 365 Project Operationsissa on isännöity iFrame Microsoft Dataversessa. Tämän käytön vuoksi tiettyjen vaatimusten on täytyttävä, jotta todentaminen ja valtuutus toimivat oikein. Tässä aihessa kuvataan seikkoja, jotka voivat vaikuttaa ruudukon hahmontamiseen tai tehtävien hallintaan työrakenteessa (work breakdown structure, WBS).

Joitakin yleisiä ongelmia:

- **Tehtävä**-välilehti tehtäväruudukossa on tyhjä.
- Projektia avattaessa projekti ei lataudu ja käyttöliittymä juuttuu hyrräkuvakkeeseen.
- **Project for the Web** -oikeuksien hallinta.
- Muutoksia ei tallenneta, kun luot, päivität tai poistat tehtävän.

## <a name="issue-the-task-tab-is-empty"></a>Ongelma: Tehtävä-välilehti on tyhjä

### <a name="mitigation-1-enable-cookies"></a>Korjaavat toimet 1: Ota evästeet käyttöön

Project Operations edellyttää, että kolmannen osapuolen evästeet on otettu käyttöön työrakenteen hahmontamista varten. Kun kolmannen osapuolen evästeitä ei ole otettu käyttöön, tehtävien sijaan näet tyhjän sivun, kun valitset **Tehtävät**-välilehden **Projekti**-sivulla.

Seuraavissa ohjeissa kerrotaan, miten selainasetus päivitetään kolmannen osapuolen evästeiden käyttöönottamiseksi Microsoft Edge- ja Google Chrome -selaimissa.

#### <a name="microsoft-edge"></a>Microsoft Edge

1. Avaa Edge-selain.
2. Valitse oikeasta yläkulmasta **kolme pistettä** (...) ja valitse sitten **Asetukset**.
3. Valitse **Evästeet ja sivuston oikeudet** -kohdasta **Evästeet ja sivustotiedot**.
4. Poista käytöstä **Estä kolmansien osapuolten evästeet**.
5. Päivitä selain. 

#### <a name="google-chrome"></a>Google Chrome

1. Avaa Chrome-selain.
2. Valitse oikeasta yläkulmasta kolme pystysuuntaista pistettä ja valitse sitten **Asetukset**.
3. Valitse **Tietosuoja ja turvallisuus** -kohdasta **Evästeet ja muut sivuston tiedot**.
4. Valitse **Salli kaikki evästeet**.
5. Päivitä selain. 

> [!NOTE]
> Jos estät kolmansien osapuolten evästeet, kaikki muiden sivustojen evästeet ja sivustotiedot estetään, vaikka sivusto olisi sallittu poikkeusluettelossasi.

### <a name="mitigation-2-validate-the-pex-endpoint-has-been-correctly-configured"></a>Korjaavat toimet 2: Tarkista, että PEX-päätepiste on määritetty oikein

Project Operations edellyttää, että projektiparametri viittaa PEX-päätepisteeseen. Tämän päätepisteen on oltava yhteydessä palveluun, jonka avulla työrakenne hahmonnetaan. Jos parametria ei ole otettu käyttöön, näyttöön tulee seuraava virhe: "Projektiparametri on virheellinen". Voit päivittää PEX-päätepisteen seuraavasti.

1. Lisää **PEX-päätepiste**-kenttä **Projektiparametrit**-sivulle.
2. Määritä tuotetyyppi, jota käytät. Tätä arvoa käytetään, kun PEX-päätepiste on määritetty. Noudettaessa tuotetyyppi on jo määritetty PEX-päätepisteeseen. Säilytä tämä arvo.
3. Päivitä kenttään seuraava arvo: `https://project.microsoft.com/<lang>/?org=<cdsServer>#/taskgrid?projectId=<id>&type=2`. Seuraavassa taulukossa on esitetty tyyppiparametri, jota tulisi käyttää tuotetyypin mukaan.

      | **Tuotetyyppi**                     | **Syötä parametri** |
      |--------------------------------------|--------------------|
      | Project for the Web oletusorganisaatiossa   | laji=0             |
      | Project for the Web CDS-nimetyssä organisaatiossa | laji=1             |
      | Project Operations                   | laji=2             |

4. Poista kenttä **Projektiparametrit**-sivulta.

## <a name="issue-the-project-doesnt-load-and-the-ui-is-stuck-on-the-spinner"></a>Ongelma: Projekti ei lataudu ja käyttöliittymä juuttuu hyrräkuvakkeeseen

Todentamista varten ponnahdusikkunat on otettava käyttöön, jotta tehtäväruudukko latautuu. Jos ponnahdusikkunoita ei ole otettu käyttöön, näyttö juuttuu latauksen hyrräkuvakkeeseen. Seuraavassa kuvassa näkyvät URL-osoite, osoiterivillä estetyn ponnahdusikkunan selite ja lataamisen yhteydessä aiheutunut juuttunut hyrräkuvake. 

   ![Juuttunut hyrräkuvake ja ponnahdusikkunoiden esto.](media/popupsblocked.png)

### <a name="mitigation-1-enable-pop-ups"></a>Korjaavat toimet 1: Ota ponnahdusikkunat käyttöön

Kun projekti juuttuu hyrräkuvakkeeseen, ponnahdusikkunoita ei ehkä ole sallittu.

#### <a name="microsoft-edge"></a>Microsoft Edge

Ponnahdusikkunat voi ottaa käyttöön Edge-selaimessa kahdella tavalla.

1. Valitse ilmoitus Edge-selaimen oikeasta yläkulmasta.
2. Valitse **Salli aina ponnahdusikkunat ja uudelleenohjaukset** tietystä Dataverse-ympäristöstä.
 
     ![Ponnahdusikkunat estetty -ikkuna.](media/enablepopups.png)

Vaihtoehtoisesti voit toimia myös seuraavasti:

1. Avaa Edge-selain.
2. Valitse oikeasta yläkulmasta **kolme pistettä** (...) ja valitse sitten **Asetukset** > **Sivuston oikeudet** > **Ponnahdusikkunat ja uudelleenohjaukset**.
3. Vaihda **Ponnahdusikkunat ja uudelleenohjaukset** pois päältä estääksesi ponnahdusikkunat tai vaihda se päälle salliaksesi ponnahdusikkunat laitteessasi.
4. Kun olet sallinut ponnahdusikkunat, päivitä selain. 

#### <a name="google-chrome"></a>Google Chrome
1. Avaa Chrome-selain.
2. Siirry sivulle, jossa ponnahdusikkunat on estetty.
3. Valitse osoiterivillä **Ponnahdusikkuna estetty**.
4. Valitse linkki siihen ponnahdusikkunaan, jonka haluat nähdä.
5. Kun olet sallinut ponnahdusikkunat, päivitä selain. 

> [!NOTE]
> Jos haluat nähdä sivuston ponnahdusikkunat aina, valitse **Salli aina ponnahdusikkunat ja uudelleenohjaukset sivustosta [sivusto]** ja valitse sitten **Valmis**.

## <a name="issue-3-administration-of-privileges-for-project-for-the-web"></a>Ongelma 3: Project for the Web -oikeuksien hallinta.

Project Operations luottaa ulkoiseen aikataulutuspalveluun. Palvelu edellyttää, että käyttäjälle on delegoitu useita rooleja, joiden avulla hänellä on luku- ja kirjoitusoikeudet WBS:ään liittyviin entiteetteihin. Näitä entiteettejä ovat projektitehtävät, resurssimääritykset ja tehtävien riippuvuudet. Jos käyttäjä ei voi hahmontaa WBS:ää siirtyessään **Tehtävät**-välilehteen, syy on todennäköisesti se, ettei **Projektia** **Project Operations** issa ole otettu käyttöön. Käyttäjä voi saada joko käyttöoikeusroolivirheen tai käytönestoon liittyvän virheen.

### <a name="mitigation-1-validate-the-application-user-and-end-user-security-roles"></a>Korjaavat toimet 1: Tarkista sovelluksen käyttäjän ja loppukäyttäjän käyttöoikeusroolit

1. Siirry kohtaan **Asetus** > **Suojaus** > **Käyttäjät** > **Sovelluksen käyttäjät**.  

   ![Sovelluslukija.](media/applicationuser.jpg)
   
2. Kaksoisnapsauta sovelluksen käyttäjätietuetta tarkistaaksesi, että:

     - Käyttäjällä on projektin käyttöoikeus. Voit tehdä tämän tarkistamalla, että käyttäjällä on **Projektipäällikkö**-käyttöoikeusrooli.
     - Microsoft Project -sovelluksen käyttäjä on olemassa ja määritetty oikein.
 
3. Jos tätä käyttäjää ei ole olemassa, luo uusi käyttäjätietue. 
4. Valitse **Uudet käyttäjät**, muuta merkintälomake muotoon **Sovelluksen käyttäjä**  ja lisää sitten **Sovelluksen tunnus**.

   ![Sovelluksen käyttäjän tiedot.](media/applicationuserdetails.jpg)


## <a name="issue-4-changes-arent-saved-when-you-create-update-or-delete-a-task"></a>Ongelma 4: Muutoksia ei tallenneta, kun luot, päivität tai poistat tehtävän

Kun teet WBS:ään yhden tai useamman päivityksen, muutokset epäonnistuvat eikä niitä tallenneta. Aikatauluruudukossa tapahtuu virhe ja näyttöön tulee seuraava sanoma: "Viimeksi tehtyä muutosta ei voi tallentaa".

### <a name="mitigation-1-validate-the-license-assignment"></a>Korjaavat toimet 1: Tarkista käyttöoikeuden määritys

1. Tarkista, että käyttäjälle on määritetty oikea käyttöoikeus ja että palvelu on otettu käyttöön käyttöoikeuden palvelusuunnitelmissa.  
2. Tarkista, että käyttäjä voi avata osoitteen **project.microsoft.com**.
    
### <a name="mitigation-2-validation-configuration-of-the-project-application-user"></a>Korjaavat toimet 2: Projektin sovelluksen käyttäjän vahvistusmääritykset
1. Tarkista, että projektisovelluksen käyttäjä on luotu.
2. Ota käyttäjälle käyttöön seuraavat käyttöoikeusroolit:
  
  - Dataverse-käyttäjä tai peruskäyttäjä
  - Project Operations -järjestelmä
  - Projektijärjestelmä
  - Project Operationsin kaksoiskirjoitusjärjestelmä. Tämä rooli vaaditaan Project Operationsin resursseihin ja ei-varastoitaviin perustuvien skenaarioiden käyttöönottoon.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
