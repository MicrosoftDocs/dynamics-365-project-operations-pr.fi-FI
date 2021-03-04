---
title: Näytetietojen asennus
description: Tässä aiheessa on tietoja näytetietojen asentamisesta Project Service Automationin avulla.
ms.custom: dyn365-projectservice
ms.date: 11/08/2018
ms.service: project-operations
ms.reviewer: kfend
ms.suite: ''
applies_to: Dynamics 365 Project Service Automation
author: ruhercul
ms.author: ruhercul
search.audienceType: IT Pro, Developer
search.app: ''
ms.openlocfilehash: aaeb4163c7ace1c3bf4db61f1a10a13cfbdc4fc2
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/10/2021
ms.locfileid: "5144499"
---
# <a name="sample-data-installation-for-the-project-service-application"></a>Näytetietojen asennus Project Service -sovelluksessa

[!include [banner](../includes/psa-now-project-operations.md)]

Jos haluat luoda omia esittely-ympäristöjä, voit käyttää Microsoftin ladattavissa olevia näytetietopaketteja, joissa esitellään sovellustesi ominaisuuksia. Näytetietopaketteja on kahta tyyppiä:
- viite- ja asetustiedot
- esittelytiedot (viite- ja asetustiedot ja liiketapahtumatiedot, kuten työtilaukset ja projektit)

**Viitteiden** näytetietopaketit ovat ladattavissa kolmessa erillisessä paketissa. Voit siis asentaa vain Project Service- tai vain Field Service -sovelluksen näytetiedot tai molempien sovellusten näytetiedot kerralla.

Asetus- ja viitetietojen näytetietopaketit:

- [**V902PSMasterData** - vain Project Service -sovelluksen versio 3.x](https://go.microsoft.com/fwlink/?linkid=2026540&clcid=0x409)

- [**V902FSMasterData** - vain Field Service -sovelluksen versio 8.x](https://go.microsoft.com/fwlink/?linkid=2026536&clcid=0x409)

- [**V902FPSMasterData** - Field Service -sovelluksen versio 8.x ja Project Service -sovelluksen versio 3.x](https://go.microsoft.com/fwlink/?linkid=2026041&clcid=0x409)

Uusin **esittelytietojen** tietopaketti:

 - [**FPSDemoData** - Field Service 8.x ja Project Service 3.x](https://aka.ms/fpsdemodatapackage)

   Asennusohjeet poikkeavat hieman sen mukaan, luoko vai määrittääkö käyttäjä osan, mutta muuten ohjeet ovat samat kuin edellisessä [**blogikirjoituksessa**](https://aka.ms/fpsdemodatablog). Tässä paketissa on rajoitettu esittelytietojoukko, ja sen asentaminen kestää noin 3 tuntia.

Nämä näytetietopaketit ovat saatavana vain englanninkielisinä.

> [!IMPORTANT]
> **Näytetietojen asennusta ei voi peruuttaa.** Nämä paketit tulee asentaa vain esittely-, arviointi-, koulutus- tai testijärjestelmiin. Huomaa myös, että yksittäisen paketin asennuksen jälkeen toisen yksittäisen paketin asennusta ei tueta. (Toisin sanoen et voi asentaa **FSMasterData**-pakettia ja sen jälkeen **PSMasterData**-pakettia tai päin vastoin) Jos tarvitset jossakin vaiheessa molempien sovellusten näytetietoja, asennettavan paketin tulee olla **v902FPSMasterData**.

Kun asennat jonkin näytetietopaketin, asennusprosessi suorittaa seuraavat toiminnot:

- Luo tai määrittää oletusparametrit, joiden avulla käytetään Project Service- tai Field Service -sovellusta tai molempia sovelluksia (jos käytettävissä).

- Tuo sovellusten näytetiedot, kuten varattavat resurssit, sovelluskohtaiset roolit, myynti- ja kustannushinnastot, organisaatioyksiköt, myyntiprosessitietueet ja muut entiteetit, joiden avulla esitellään tärkeimpiä ominaisuuksia.  

**Esittelytietopaketti** sisältää edellä olevat ja lisää liiketapahtumatietoja, kuten työtilauksia ja projekteja.

Haluatko tietää, millaisia ominaisuuksia voit esitellä näytetietojen kanssa? Katso kuvitteellinen Fabrikam Robotics -skenaario [teknisissä huomautuksissa](#technical-notes).

Jos sinulla on näiden näytetietopakettien asentamiseen liittyviä kysymyksiä, [lähetä sähköpostiviesti osoitteeseen fpsdemodata@microsoft.com](mailto:fpsdemodata@microsoft.com).

## <a name="requirements"></a>Vaatimukset

Asennustoiminnoissa edellytetään, että kohdeilmentymä (organisaatio) täyttää seuraavat vaatimukset:

- Peruskieli on englanti ja perusvaluutta Yhdysvaltain dollari (USD,$).

- Organisaatiolla ei ole Project Service- tai Field Service -tietoja tai sillä on vain oletustiedot, jotka tulevat minkä tahansa uuden organisaation mukana.

- Yrityssovelluksen oikea versio on jo asennettu:
       
    - **FPSDemoData tai v902FPSMasterData:** Organisaatioon on asennettu Field Service -sovelluksen versio 8.x ja Project Service -sovelluksen versio 3.x.

    - **v902PSMasterData:** Organisaatioon on asennettu Project Service -sovelluksen versio 3.x.

    - **v902FSMasterData:** Organisaatioon on asennettu Field Service -sovelluksen versio 8.x.

> [!NOTE]
> Jos näytetiedot on asennettava olemassa olevan Project Service- tai Field Service -kokeilu- tai esittely-ympäristöön, jossa on jo tietoja (ei suositella), asennusohjelman suorittamat turvallisuuteen liittyvät esitarkistukset on poistettava käytöstä tilapäisesti. Lisätietoja on alla olevissa teknisissä huomautuksissa.

## <a name="prepare-for-installation"></a>Asennuksen valmisteleminen

Asennusohjelma on suoritettava tietokoneella, jossa on käytössä Windowsin uusin versio (Windows 10 on suositeltu versio).

Tietokoneessa on oltava verkkoyhteys. **Asennus- tai viitetietojen** asentaminen voi kestää **tunnin**. (Yleensä **FPSMasterData**-paketin asennus kestää noin 30 minuuttia. Paketti sisältää kummankin sovelluksen mallitiedot.) **FPSDemoData**-paketin asennus kestää noin **3 tuntia**.

Tietokoneen näytönsäästäjätoiminto tulee poistaa käytöstä. Muussa tapauksessa asennuksen istunnon tunnistetiedot menetetään, kun näytönsäästäjä menee päälle (ellet pidä istuntoa aktiivisena koko ajan).

> [!div class="mx-imgBorder"]
> ![Näytönsäästäjän asetusten näyttökuva, jossa näytönsäästäjä on poistettu käytöstä](media/sample-data-1.png)

## <a name="download-and-unpack"></a>Lataaminen ja paketin purkaminen

Project Service- ja Field Service -näytetietojen asennusohjelma jaetaan automaattisesti purkautuvana suoritettavana tiedostona. Tiedostojen nimet voivat vaihdella näytetietopaketin mukaan. Vaiheet ovat kuitenkin samat asennettavasta paketista riippumatta.

Kun paketti on ladattu, suorita .exe-tiedosto ja hyväksy pakatun zip-tiedoston purkamisen ehdot. Tämän jälkeen tiedoston sisältö puretaan tietokoneen kansioon.

Käyttöjärjestelmästä ja suojausasetuksista riippuen zip-tiedoston purkamisen jälkeen on suoritettava seuraavat vaiheet:

1. Etsi **FPSDemoData.dll**-tiedosto **v902FPSMasterData** / **PackageDeployer_FPSDemoData**-kansiossa ja kaksoisnapsauta sitä.

2. Valitse **Poista esto**.

3. Valitse **Käytä**.

4. Valitse **OK**.


## <a name="create-or-configure-users"></a>Käyttäjien luominen tai määrittäminen

**FPSDemoData**-paketti edellyttää kuutta käyttäjää, kun taas **FPSMasterData**-paketit edellyttävät yhtä käyttäjää. Viittaa oikeaan, näytetietopaketille tarkoitettuun versioon.

## <a name="create-or-configure-users---setupreference-data-packages"></a>Käyttäjien luominen tai määrittäminen – asetus- ja viitetietopaketit

**FPSMasterData**-paketti on suunniteltu niin, että se asentaa yhden käyttäjän, jonka nimi on Spencer Low, sekä tässä kuvatut asetukset. Jotta paketti asentuu oikein, ympäristöösi on luotava käyttäjät (tai käyttäjät on nimettävä uudelleen tilapäisesti), jotta ne vastaavat näytetietojen määritystä.

Voit luoda tai määrittää käyttäjiä siirtymällä kohtaan **Asetukset** > **Suojaus** > **Käyttäjät** ja tekemällä seuraavat toimet:

1. Määritä UserFullname="Spencer Low" ja käyttäjätunnukseksi "spencerl" (**pienet kirjaimet**) projektipäällikön ja käytäntöpäällikön rooleihin.

2. Valitse käyttäjäksi **Spencer Low** ja valitse sitten **Hallitse rooleja**. Etsi **järjestelmänvalvojan** rooli ja valitse se. Myönnä Spencer Low'lle täydet järjestelmänvalvojan oikeudet valitsemalla **OK**. Tämän vaihe on välttämätön, koska siinä varmistetaan, että näytetiedot luodaan oikean käyttäjän omistuksen kanssa. Näin näkymien täyttäminen tapahtuu oikein.

3. Päivitä ladatun paketin tietojen yhdistämisen tiedostoon oletuskäyttäjän sähköpostiosoitteet. Avaa **PkgFolder**, etsi **ImportUserMapFile.xml** -tiedosto ja avaa se Muistiossa (tai Visual Studiossa tai toisessa XML-editorissa). Määritä **DefaultUserToMapTo=**-kenttään käyttäjän Spencer Low sähköpostiosoite.

4. Jos et käytä Spencer Low'n käyttäjätunnusta **spencerl**, sinun on päivitettävä toinen tiedosto. Avaa **DemoDataPreImportConfig.xml**-tiedosto ja etsi **userstocreateandconfigure**-tunniste. Päivitä **\<login\>**-tunnisteeksi käyttäjän Spencer Low käyttäjätunnus. Lisätietoja on [teknisissä huomautuksissa](#technical-notes).

## <a name="create-or-configure-users---demo-data-package"></a>Käyttäjien luominen tai muokkaaminen – esittelytietopaketti

Esittelytietopakettia varten tarvitaan kuusi käyttäjää. Paketti asennetaan oikein seuraavasti:

 1. Luo käyttäjiä tai vaihda väliaikaisesti käyttäjien nimet vastaamaan saapuvaa mallitietomääritystä valitsemalla **Asetukset** > **Suojaus** > **Käyttäjät**.
 
    Näitä rooleja tarvitaan vain henkilöpohjaisissa esittelyissä.  
    - Käytä kenttätyöntekijänä käyttäjää Fullname="David So"   
    - Käytä asiakaspalvelijana ja kenttäpalvelun aikatauluttajana käyttäjää Fullname="Jamie Reding"   
    - Käytä asiakaspäällikkönä käyttäjää Fullname="Molly Clark"   
    - Käytä käytäntö- ja projektipäällikkönä käyttäjää Fullname="Spencer Low"  
    - Käytä tiimin jäsenenä käyttäjää Fullname="Veronica Quek"   
    - Käyttäjä Fullname="William Contoso"
  
2. Määritä edellä mainituille kuudelle käyttäjälle järjestelmänvalvojan rooli esittelytietojen tuontia varten, jotta näytetiedot tuodaan oikein. 

3. Avaa **PkgFolder** ja etsi ja avaa sitten **ImportUserMapFile.xml**. Päivitä **New=**-kentät järjestelmän käyttäjiä vastaaviksi sähköpostiosoitteiksi.

   > [!div class="mx-imgBorder"]
   > ![Näyttökuva UserMapFile-tiedostosta](media/sample-data-7.png)

4. Jos "Spencer Low" -nimisen käyttäjän koko nimellä on eri käyttäjätunnus kuin **"spencerl"**, myös lisätiedosto on päivitettävä. Avaa **DemoDataPreImportConfig.xml** ja etsi **userstocreateandconfigure**-tunniste. Päivitä loginId (kirjainkoolla on merkitystä) **\<login\>**-tunnisteeseen. 

5. Ensimmäisen käyttäjän kalenterin (joka on **userstocreateandconfigure**-tunnisteessa) avulla lisätään kaikkien varattavien resurssien työtunnit esittelytietoja tuotaessa. Valitse **Asetukset** > **Suojaus** > **Käyttäjät**, etsi käyttäjä Spencer Low ja avaa Työtunnit-asetus. Muokkaa nykyisiä työtunteja valitsemalla **Koko viikoittain toistuva aikataulu alusta loppuun** -asetus. Varmista, että **työtunneiksi on määritetty 8.00–17.00 (9 tuntia) maanantaista perjantaihin ja aikavyöhykkeeksi on määritetty Tyynenmeren normaaliaika (USA ja Kanada)**. Tällä tavoin varmistaa, että projekti- ja aikataulutaulukko näkyvät odotetusti.

**Suositus:** Organisaatiolle kannattaa luoda varmuuskopio nyt siltä varalta, että asennuksessa on palattava aloituskohtaan. Näin saattaa käydä, jos näytetietojen asennuksen aikana tapahtuu virhe. Lisätietoja on kohdassa [Ilmentymien varmuuskopiointi ja palautus](https://docs.microsoft.com/dynamics365/customer-engagement/admin/backup-restore-instances).

## <a name="run-the-package-deployer"></a>Suorita Package Deployer

1. Etsi ja suorita **PackageDeployer.exe**. Se on **v902FPSMasterData**- TAI **PackageDeployer_FPSDemoData**-kansiossa.

2. Hyväksy ehdot.

3. Seuraava ikkuna:

   a. Valitse **Office 365**:n käyttöönottotyyppi.

   b. Käytä järjestelmänvalvojalle Käyttäjien luominen tai määrittäminen -kohdassa luotua käyttäjää ja salasanaa (Spencer Low ja käyttäjätunnus spencerl).

   c. Varmista, että **Näytä käytettävissä olevien organisaatioiden luettelo** on valittu.

      > [!div class="mx-imgBorder"]
      > ![Näyttökuva Package Deployer -ikkunasta, jossa on valittu Näytä käytettävissä olevien organisaatioiden luettelo](media/sample-data-2.png)

4. Valitse organisaatio, johon haluat asentaa näytetiedot.

5. Valitse **Seuraava** niin kauan, kunnes näkyviin tulee **Esittelytietojen asetukset** -valintaikkuna.

   > [!div class="mx-imgBorder"]
   > ![Esittelytietojen asennusohjelman tilaikkunan näyttökuva](media/sample-data-3.png)

6. Ennen kuin jatkat, ota huomioon, että näytetietojen asentaminen voi kestää jopa tunnin (yleensä se kestään noin 10 minuuttia). Varmista, että tietokone on päällä, verkkoyhteys säilyy asennusprosessin ajan ja että istunto pysyy aktiivisena.   

7. Kun olet valmis, valitse **Seuraava** ja aloita näytetietojen asennusprosessi. Kun näytetiedot on ladattu, valitse **Valmis**.

## <a name="verify-the-sample-data-installation"></a>Näytetietojen asennuksen tarkistaminen

Tarkista, että Fabrikam Robotics -yrityksen kuvitteellisen skenaarion tietueet ja entiteettityypit näkyvät halutulla tavalla.

Kun näytetiedot on ladattu kokonaan, kirjaudu sisään käyttäjänä Spencer Low ja vahvista seuraavat kohdat:

- Jos Project Service -sovellus on asennettu, siirry kohtaan **Project Service** > **Asetukset** > **Hinnastot**. Vahvista, että tietojoukon jokaiselle maalle/alueelle on määritetty laskutus- ja kustannushinnat soveltuvassa valuutassa.

- Jos Project Service -sovellus on asennettu, siirry kohtaan **Universal Resource Scheduling** > **Asetukset** > **Organisaatioyksiköt**. Vahvista, että jokaiseen organisaatioyksikköön (lukuun ottamatta kaupunkikirjauksia) on liitetty soveltuvassa valuutassa oleva kustannushinnasto. Jos joku puuttuu, etsi oikea kustannushinnasto ja liitä se.

- Jos Field Service -sovellus on asennettu, siirry kohtaan **Project Service** > **Asetukset** > **Hinnastot** Varmista, että laskutus- ja kustannushinnat on määritetty. Siirry kohtaan **Field Service** > **Asetukset** > **Hinnastot** ja tarkista, että tietojoukon jokaiselle maalle/alueelle on määritetty laskutus- ja kustannushinnat soveltuvassa valuutassa.

  > [!div class="mx-imgBorder"]
  > ![Aktiivisten hinnastojen näyttökuva](media/sample-data-4.png)

  > [!div class="mx-imgBorder"]
  > ![Aktiivisten organisaatioyksiköiden näyttökuva](media/sample-data-5.png)

## <a name="technical-notes"></a>Tekniset huomautukset

Alla on lisää näiden tietojen asennukseen liittyviä teknisiä tietoja.

### <a name="installing-sample-data-on-top-of-existing-data-not-recommended"></a>Näytetietojen asentaminen aiemmin luotujen tietojen päälle (ei suositella)

Jos näytetiedot on asennettava olemassa olevan Field Service- tai Project Service -kokeilu- tai esittely-ympäristöön, jossa on jo tietoja, asennusohjelman suorittamat turvallisuuteen liittyvät esitarkistukset on poistettava käytöstä tilapäisesti.

Jos haluat tehdä niin, siirry **PkgFolder**-kansioon, etsi **DemoDataPreImportConfig.xml**-tiedosto ja avaa se Muistiolla (tai toisella XML-editorilla).

Etsi seuraava arvo ja muuta Tosi-arvo Epätosi-arvoksi:

```alias
<TerminateOnPreCheckFailure>true</TerminateOnPreCheckFailure>
```

Tämän muutoksen vuoksi asennusohjelma ohittaa joitakin tärkeitä turvallisuustarkistuksia, esimerkiksi seuraavat:

- Vahvistetaan, että aktiivisia **organisaatioyksikkötietueita** on vain yksi, ja annetaan sen nimeksi **Fabrikam US**.

- Vahvistetaan, että aktiivisia **työmallitietueita** on vain yksi.

- Vahvistetaan, että aktiivisia **projektiparametritietueita** on vain yksi, ja annetaan sen nimeksi **Parametrit**.

### <a name="configuration-components"></a>Määrityksen komponentit

Tässä tuontia edeltävässä määritystiedostossa on useita muita määrityksen komponentteja. Teknisille käyttäjille tiedoksi, että niitä ovat esimerkiksi seuraavat:

- **\<RequiredSolutions\>** määrittää ratkaisun edellyttämät asennukset ja niiden versionumerot.

- **\<InstallSampleData\>** määrittää, onko sovellusten valmiit näytetiedot asennettu.

    - epätosi - ohittaa näiden oletustietojen asennuksen (poistettavissa)

    - tosi - asentaa oletustiedot yhdessä FS- ja PSA-näytetietojen asennuksen kanssa

- **\<PreImportDataCollection\>** määrittää vakiotiedoston tietokartat ja liittyvät tietueet, jotka tuodaan ennen päänäytetietojen asennusta.

- **\<EntitiesToEnableScheduling\>** määrittää, mitkä entiteetit otetaan käyttöön varaukselle Microsoft Dynamics Schedulingissa (eli Universal Resource Schedulingissa).

- **\<UsersToCreateAndConfigure\>** määrittää varattavissa olevat resurssit, jotka luodaan (jos niitä ei jo ole) ennen näytetietojen tuontia. Ota huomioon, että lähdejärjestelmän näytetietojen varattavissa oleva resurssi vastaa kohdejärjestelmän varattavissa olevan resurssin tietueita FullName-kohdassa ja kunkin resurssin sisäänkirjauksessa. Tämän vuoksi esimääritystiedoston nimiä EI voi muuttaa, ennen kuin näytetiedot on tuotu kohdejärjestelmään käyttämällä näitä nimiä, varattavissa olevat resurssit ja aktivoitujen käyttäjien tietueet on nimetty uudelleen ja tiedot viety uudelleen tuontia varten lopulliseen kohdejärjestelmään (samalla päivitetään vastaavasti **ImportUserMapFile.xml**-tiedoston vanhat ja uudet merkinnät).

- **\<PluginsToDisable\>** määrittää nimikkeen laajennukset, jotka on poistettava käytöstä näytetietojen tuonnin aikana. Tämän jälkeen ne otetaan uudelleen käyttöön.

### <a name="fabrikam-robotics-fictitious-scenario"></a>Fabrikam Robotics -yrityksen kuvitteellinen skenaario

Field Service- ja Project Service -viitetietojen näytetietopaketit asentavat **Fabrikamin valmistuksen perustiedot (v3.0.0.0) -ratkaisun** sekä noin 4 000 tietuetta ja 40 eri entiteettiä. Field Service- ja Project Service -sovelluksen erilliset näytetietopaketit sisältävät kyseisen sovelluksen **v902FPSMasterData**-näytetietojen alijoukon. **Esittelytietopaketti** asentaa **Fabrikamin valmistuksen perustiedot (v3.0.0.7) -ratkaisun**, jossa on noin 22 000 tietuetta 148 entiteetissä.

Kuvitteellinen Fabrikam Robotics -yritys valmistaa elektronisten laitteiden kokoonpanolinjan robotteja. Yritys on tunnettu tuotteiden laadusta, innovoinnista ja hyvästä asiakaspalvelusta. Siihen kuuluvat esimerkiksi asennuksen suunnittelu, käyttöönotto ja jatkuva ylläpito. Fabrikamin pääkonttori on Yhdysvalloissa (Fabrikam US). Sillä on projektikohtaisia palvelutoimintoja Ranskassa, Intiassa, Isossa-Britanniassa ja Sveitsissä.

Kenttäpalvelutoiminnot on keskitetty Yhdysvaltoihin ja siellä enimmäkseen Seattlen alueelle. Yritys hyödyntää esineiden internetiä (IoT), jonka avulla on mahdollista seurata asiakasresurssien suorituskykyä ja tarjota entistäkin proaktiivisempaa asiakaspalvelua asiakkaan tiloissa.

Näytetietojen korkean tason yleiskatsaus on seuraava:

- Yleiset näytetietoelementit (kuuluvat kumpaankin sovellukseen)

    - 1 käyttäjä

    - 71 asiakasta

    - 137 yhteyshenkilöä

    - Erilaisia tapahtumatyyppejä ja -luokkia

    - 50 tuotetta ja 1 tuotehinnasto

    - 14 hintaa/kustannushinnastot

    - 31 ominaisuutta (resurssin osaamisaluetta) 2 luokitusmallissa ja 3 tasolla (luokitusarvot)

- Project Service

    - 8 organisaatioyksikköä

    - 6 roolikohtaisia käyttötasoa

    - 2,8 k + roolihinnan määritykset

- Field Service

    - 4 aluetta

    - 5 työtilaustyyppiä

    - 22 asiakasresurssia

    - 9 tapauksen tyyppiä ja liittyviä resurssin ominaisuuksia (9), palveluita (13) ja palvelutehtäviä (13)
   
**Esittelytietopaketti** asentaa noin 179 työtilausta, 12 projektia ja liitetyt liiketapahtumatiedot. 

### <a name="change-the-work-hours-for-sample-resources"></a>Näyteresurssien työtuntien muuttaminen

Kaikilla varattavissa olevilla resursseilla on 24 työtunnin oletuskalenteri.

Jos haluat muuttaa varattavissa olevien näyteresurssien työtunteja, siirry kohtaan **Universal Resource Scheduling** > **Aikataulutus** > **Resurssit**.

Valitse käyttäjä (esimerkiksi Spencer Low) ja muuta käyttäjän työtunnit. Tätä asetusta käytetään useilla käyttäjillä. Siirry kohtaan **Universal Resource Scheduling** > **Asetukset** > **Työtuntimallit** ja muokkaa **Oletustyömalli**-tietuetta. Valitse **Malliresurssi**-kentässä käyttäjä, jonka työtunnit haluat ottaa käyttöön muissa resursseissa. Siirry kohtaan **Universal Resource Scheduling** > **Aikataulutus** > **Resurssit** > **Aktiiviset varattavissa olevat resurssit**. Valitse muutettavat resurssit ja valitse sitten **Määritä kalenteri**. Valitse avattavasta **Työmalli**-luettelosta **Oletustyötunti**-malli tai toinen malli, jossa on oikea malliresurssi. Nyt aikataulutaulukossa pitäisi näkyä resurssien päivitetyt työtunnit.

> [!div class="mx-imgBorder"]
> ![Aktiivisten varattavissa olevien resurssien näyttökuva](media/sample-data-6.png)
