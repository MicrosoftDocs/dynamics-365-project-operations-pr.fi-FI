---
title: Tehtäväruudukossa työskentelyn vianmääritys
description: Tässä aihe sisältää vianmääritystietoja, joita tarvitaan tehtäväruudukossa.
author: ruhercul
manager: tfehr
ms.date: 01/19/2021
ms.topic: article
ms.product: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: dedd989cc7c959d9ea97a0abfb13f8f1b2150a56
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5286559"
---
# <a name="troubleshoot-working-in-the-task-grid"></a>Tehtäväruudukossa työskentelyn vianmääritys 

_**Koskee:** Project Operationsin resurssiin / muuhun kuin resurssiin perustuvia skenaarioita, Lite-käyttöönotto-kaupasta proformalaskutukseen_

Tässä aiheessa kuvataan, miten Cost Managementin käytössä mahdollisesti kohtaamiasi ongelmia ratkaistaan.

## <a name="enable-cookies"></a>Ota evästeet käyttöön

Project Operations edellyttää, että kolmannen osapuolen evästeet on otettu käyttöön, jotta työrakenne voidaan hahmontaa. Kun kolmannen osapuolen evästeitä ei ole otettu käyttöön, tehtävien sijaan näet tyhjän sivun, kun valitset **Tehtävät**-välilehden **Projekti**-sivulla.

![Tyhjä välilehti, kun kolmannen osapuolen evästeitä ei ole otettu käyttöön](media/blankschedule.png)


### <a name="workaround"></a>Ratkaisutapa
Seuraavissa ohjeissa kerrotaan, miten selainasetus päivitetään kolmannen osapuolen evästeiden käyttöönottamiseksi Microsoft Edge- ja Google Chrome -selaimissa.

#### <a name="microsoft-edge"></a>Microsoft Edge

1. Avaa Edge-selain.
2. Valitse oikeasta yläkulmasta **kolme pistettä** (...) ja valitse sitten **Asetukset**.
3. Valitse **Evästeet ja sivuston oikeudet** -kohdasta **Evästeet ja sivustotiedot**.
4. Poista käytöstä **Estä kolmansien osapuolten evästeet**.

#### <a name="google-chrome"></a>Google Chrome

1. Avaa Chrome-selain.
2. Valitse oikeasta yläkulmasta kolme pystysuuntaista pistettä ja valitse sitten **Asetukset**.
3. Valitse **Tietosuoja ja turvallisuus** -kohdasta **Evästeet ja muut sivuston tiedot**.
4. Valitse **Salli kaikki evästeet**.

> [!IMPORTANT]
> Jos estät kolmansien osapuolten evästeet, kaikki muiden sivustojen evästeet ja sivustotiedot estetään, vaikka sivusto olisi sallittu poikkeusluettelossasi.

## <a name="pex-endpoint"></a>PEX-päätepiste

Project Operations edellyttää, että projektiparametri viittaa PEX-päätepisteeseen. Tämän päätepisteen on oltava yhteydessä palveluun, jota käytetään työrakenteen hahmontamiseen. Jos parametria ei ole otettu käyttöön, näyttöön tulee seuraava virhe: "Projektiparametri on virheellinen". 

### <a name="workaround"></a>Ratkaisutapa
 ![PEX-päätepiste-kenttä projektiparametrissa](media/projectparameter.png)

1. Lisää **PEX-päätepiste**-kenttä **Projektiparametrit**-sivulle.
2. Päivitä kenttään seuraava arvo: `https://project.microsoft.com/<lang>/?org=<cdsServer>#/taskgrid?projectId=\<id>&type=2`
3. Poista kenttä **Projektiparametrit**-sivulta.

## <a name="privileges-for-project-for-the-web"></a>Projektin verkko-oikeudet

Project Operations luottaa ulkoiseen aikataulutuspalveluun. Palvelu edellyttää, että käyttäjälle on delegoitu useita rooleja työrakenteeseen liittyvien entiteettien lukemista ja kirjoittamista varten. Näitä entiteettejä ovat projektitehtävät, resurssimääritykset ja tehtävien riippuvuudet. Jos käyttäjä ei voi hahmontaa työrakennetta, kun hän siirtyy **Tehtävät**-välilehteen, se johtuu luultavasti siitä, että Project Operationsin projektia ei ole otettu käyttöön. Käyttäjä voi saada joko käyttöoikeusroolivirheen tai käytönestoon liittyvän virheen.


## <a name="workaround"></a>Ratkaisutapa

1. Valitse **Asetus > Suojaus > Käyttäjät > Sovelluksen käyttäjät**.  

   ![Sovelluslukija](media/applicationuser.jpg)
   
2. Tarkista seuraavat seikat kaksoisnapsauttamalla sovelluksen käyttäjätietuetta:

 - Käyttäjällä on projektin käyttöoikeus. Tarkistus tehdään yleensä varmistamalla, että käyttäjällä on **projektipäällikön** käyttöoikeusrooli.
 - Microsoft Project -sovelluksen käyttäjä on olemassa ja määritetty oikein.
 
3. Jos käyttäjää ei ole, voit luoda uuden käyttäjätietueen. Valitse **Uudet käyttäjät**. Vaihda syöttölomakkeeksi **Sovelluksen käyttäjä** ja lisää sitten **sovellustunnus**.

   ![Sovelluksen käyttäjän tiedot](media/applicationuserdetails.jpg)

4. Tarkista, että käyttäjälle on määritetty oikea käyttöoikeus ja että palvelu on otettu käyttöön käyttöoikeuden palvelusuunnitelmissa.
5. Tarkista, että käyttäjä voi avata osoitteen project.microsoft.com.
6. Tarkista projektiparametrien kautta, että järjestelmä osoittaa oikeaan projektin päätepisteeseen.
7. Tarkista, että projektisovelluksen käyttäjä on luotu.
8. Ota käyttäjälle käyttöön seuraavat käyttöoikeusroolit:

  - Dataverse -palvelun käyttäjä
  - Project Operations -järjestelmä
  - Projektijärjestelmä

## <a name="error-when-updating-the-work-breakdown-structure"></a>Virhe päivitettäessä työrakennetta

Kun vähintään yksi päivitys tehdään työrakenteeseen, muutokset epäonnistuvat lopulta eikä niitä tallenneta. Aikatauluruudukossa tapahtuu virhe, jonka mukaan "Äskettäin tehtyä muutosta ei voi tallentaa".

### <a name="workaround"></a>Ratkaisutapa

1. Tarkista, että käyttäjälle on määritetty oikea käyttöoikeus ja että palvelu on otettu käyttöön käyttöoikeuden palvelusuunnitelmissa.
2. Tarkista, että käyttäjä voi avata osoitteen project.microsoft.com.
3. Tarkista, että järjestelmä osoittaa oikeaan projektin päätepisteeseen.
4. Tarkista, että projektisovelluksen käyttäjä on luotu.
5. Ota käyttäjälle käyttöön seuraavat käyttöoikeusroolit:
  
  - Dataverse-käyttäjä tai peruskäyttäjä
  - Project Operations -järjestelmä
  - Projektijärjestelmä
  - Project Operationsin kaksoiskirjoitusjärjestelmä (tämä rooli on pakollinen, jos otat käyttöön Project Operationsin resursseihin ja ei-varastoitaviin perustuvissa skenaarioissa).


[!INCLUDE[footer-include](../includes/footer-banner.md)]