---
title: Projektiaikataulut
description: Tässä artikkelissa on tietoja aikataulun luomisesta.
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 3/01/2019
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.reviewer: johnmichalak
ms.openlocfilehash: f0d052efda1b78161feed1c1e4cd70a31f3c4dea
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8915870"
---
# <a name="project-schedules"></a>Projektiaikataulut 

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Projektiaikataulu ilmaisee, mikä työ on suoritettava, mitkä resurssit suorittavat työn, ja aikajakson, jonka puitteissa työ on suoritettava. Se kuvastaa kaikkea työtä, joka liittyy projektin oikea-aikaiseen toimittamiseen. Dynamics 365 Project Service Automationissa projektiaikataulu luodaan jakamalla työ hallittavissa oleviin tehtäviin, arvioimalla kunkin tehtävän edellyttämä aika, määrittämällä tehtäväriippuvuuksia ja tehtävien kestoja sekä arvioimalla yleiset resurssit, jotka suorittavat tehtävät. Projektiaikataulu luodaan projektisivun **Aikataulut**-välilehdessä.
 
## <a name="tasks"></a>Tehtävät

Projektiaikataulun luomisen ensimmäinen vaihe on jakaa työ hallittavissa oleviin osiin. PSA:ssa oleva aikataulu tukee seuraavia toimintoja:

- Projektin pääsolmu
- Yhteenvetotehtävät tai säilössä olevat tehtävät
- Lehtisolmutehtävät

### <a name="project-root-node"></a>Projektin pääsolmu

Projektin pääsolmu on projektin ylätason yhteenvetotehtävä. Kaikki muut projektitehtävät luodaan sen alaisuuteen. Pääsolmun nimenä on aina projektin nimi. Pääsolmun työmäärä, päivämäärä ja kesto vedetään yhteen sen alapuolella hierarkiassa olevien arvojen perusteella. Pääsolmun ominaisuuksia ei voi muokata. Pääsolmua ei myöskään voi poistaa.

### <a name="summary-or-container-tasks"></a>Yhteenvetotehtävät tai säilössä olevat tehtävät 

Yhteenvetotehtävien alapuolella on alitehtäviä tai säiliötehtäviä. Niillä ei ole omia työmääriä tai kustannuksia. Sen sijaan niiden työmäärät ja kustannukset ovat koosteita niiden säilötehtävien työmääristä ja kustannuksista. Yhteenvetotehtävän alkamispäivä on säiliötehtävien alkamispäivä ja päättymispäivä säiliötehtävien päättymispäivä. Yhteenvetotehtävän nimeä voi muokata, mutta aikataulutusominaisuuksia (työmäärä, päivämäärät, kesto) ei voi muokata. Jos poistat yhteenvetotehtävän, poistat myös kaikki sen säiliötehtävät.

### <a name="leaf-node-tasks"></a>Lehtisolmutehtävät

Lehtisolmutehtävät edustavat projektin yksityiskohtaisinta työtä. Niillä on arvioitu työmäärä, resursseja, suunnitellut alkamis- ja päättymispäivämäärät ja kesto.
 
## <a name="creating-a-task-hierarchy"></a>Tehtävähierarkian luominen

Tehtävähierarkian luomisen vaihtoehdot:

- **Lisää ryhmä** -painike
- **Sisennä tehtävä** -painike
- **Ulonna tehtävä** -painike
- **Siirrä ylöspäin** ja **Siirrä alaspäin** -painikkeet.
- Helppokäyttötoiminnot ja pikanäppäimet

### <a name="add-task"></a>Tehtävän lisääminen

**Lisää tehtävä** -painikkeen avulla voit luoda hierarkiaan uuden tehtävän. Jos et valitse paikkaa, uusi tehtävä lisätään loppuun. 

Kullekin tehtävälle määritetään aikataulutustunnus. Aikataulutunnus edustaa tehtävän syvyyttä ja sijaintia hierarkiassa. Siinä käytetään monitasoista numerointia. Ensimmäisellä projektin pääsolmun alla olevalla tasolla sijaitsevissa tehtävissä käytetään numerointia 1, 2, 3 jne. Ensimmäisen projektin pääsolmun alla olevan tason alla käytetään numerointia 1.1, 1.2, 1.3 jne.

### <a name="indent-task"></a>Tehtävän sisennys

Kun tehtävä sisennetään, siitä tulee suoraan sen yläpuolella olevan tehtävän alitehtävä. Tällöin tehtävän aikataulutunnus lasketaan uudelleen siten, että se perustuu uuden päätehtävänsä aikataulutunnukseen ja vastaa monitasoista numerointijärjestelmää. Päätehtävä on nyt yhteenvetotehtävä tai säiliötehtävä. Siten siitä tulee alitehtäviensä kooste.

### <a name="outdent-task"></a>Tehtävän ulontaminen 

Kun tehtävä ulonnetaan, se ei enää ole päätehtävänsä alitehtävä. Tällöin aikataulutunnus lasketaan uudelleen siten, että se vastaa tehtävän päivitettyä syvyyttä ja sijaintia hierarkiassa. Aiemman päätehtävän työmäärä, kustannukset ja päivämäärät lasketaan sitten uudelleen siten, että ne eivät enää sisällä entistä alitehtävää.

### <a name="move-up-and-move-down"></a>Ylöspäin ja alaspäin siirtäminen 

Painikkeet **Siirrä ylöspäin** ja **Siirrä alaspäin** muuttavat tehtävän sijaintia sen päätehtävän sisällä. Tällaiset muutokset eivät vaikuta tehtävän työmäärään, kustannuksiin päivämääriin tai kestoon. Vain tehtävän aikataulutunnus muuttuu. Tällöin aikataulutunnus lasketaan uudelleen siten, että se vastaa tehtävän uutta sijaintia päätehtävän alitehtäväluettelossa.

### <a name="accessibility-and-keyboard-shortcuts"></a>Helppokäyttötoiminnot ja pikanäppäimet

**Aikataulut**-ruudukko on täysin käytettävissä, ja siinä voidaan käyttää näytönlukijoita (esim. Narrator, JAWS tai NVDA). Voit siirtyä ruudukkoalueella nuolinäppäimillä (kuten Microsoft Excelissä), voit käyttää sarkainnäppäintä siirtyäksesi vuorovaikutteisten käyttöliittymäelementtien välillä ja voit käyttää alanuolinäppäintä, Enter-näppäintä tai välilyöntiä valitaksesi ja käyttääksesi avattavia valikkoja. Myös sarakeotsikot ovat vuorovaikutteisia. Voit piilottaa ja ottaa näkyviin sarakkeita, siirtyä sarakeotsikoiden välillä sarkainnäppäimen ja nuolinäppäinten avulla ja käyttää työkalurivin toimintopainikkeita. Lisäksi voit käyttää seuraavia pikanäppäimiä:

- **Päivitä**: ALT + VAIHTO + F5
- **Lisää**: ALT + VAIHTO + INSERT
- **Poista**: ALT + VAIHTO + DELETE
- **Siirrä ylös/alas**: ALT + VAIHTO + ylä-/alanuoli
- **Sisennä/ulonna**: ALT_SHIFT + vasen/oikea nuoli
- **Laajenna/kutista hierarkiat**: ALT + VAIHTO + plus-/miinusnäppäin

## <a name="task-attributes"></a>Tehtävän määritteet

Tehtävän nimi kuvaa työtä, joka on suoritettava. PSA:ssa tehtävään yhdistetyt määritteet kuvaavat tehtävän aikataulua ja henkilöstötarpeita.

> ![Tehtävän määritteet.](media/project-2.png)
 
### <a name="schedule-attributes"></a>Aikataulun määritteet

Määritteet **Työmäärä**, **Alkamispäivä**, **Päättymispäivä** ja **Kesto** määrittävät tehtävän aikataulun.

Muita aikataulumääritteitä ovat esimerkiksi:

- **Työtunnit**: anna arvio tunneista, jotka tehtävän suorittaminen vaatii. 
- **Kesto**: määritä tehtävän suorittamisen vaatima työpäivämäärä.
- **Aikataulutunnus**: tätä automaattisesti luotavaa tunnusta käytetään tehtävien järjestämiseen hierarkiassa. Riippuvuudet tehtävien välillä hallitsevat todellista järjestystä, jossa tehtävät suoritetaan.
 
### <a name="staffing-attributes"></a>Henkilöstömääritteet

Henkilöstömääritteitä käytetään aikataulun **Resurssit**-kentän kautta. Voit joko hakea olemassa olevaa resurssia tai napsauttaa **Luo** ja lisätä projektiryhmän jäsenen uudeksi resurssiksi **Pikaluonti**-ruudussa.

Kenttiä **Rooli**, **Resursointiyksikkö** ja **Toimen nimi** käytetään tehtävän henkilöstötarpeiden kuvaamiseen. Näitä henkilöstömääritteitä käytetään yhdessä tehtävän aikataulun kanssa käytettävissä olevien resurssien hakemiseen tehtävälle.

**Rooli** – määritä tehtävän suorittamiseen tarvittava resurssityyppi.

**Resursointiyksikkö** – määritä yksikkö, josta tehtävän resurssit kohdennetaan. Tämä määrite vaikuttaa tehtävän kustannus- ja myyntiarvioon, jos resurssin kustannukset ja laskutushinta määritetään resursointiyksikköjen perusteella.

**Toimen nimi** – anna ystävällinen nimi sille yleiselle resurssille, joka toimii työn lopulta suorittavan resurssin paikkamerkkinä.

**Resurssit** -kenttä sisältää yleisen resurssin tai lopulta nimetyn resurssin toimen nimen.

**Luokka** -kenttä sisältää arvot, jotka ilmaisevat laajan työtyypin, johon tehtävä voidaan ryhmitellä. Tämä kenttä ei vaikuta aikataulutukseen tai henkilöstöön. Sitä käytetään vain raportointiin.

### <a name="task-dependencies"></a>Tehtävän riippuvuudet 

Voit käyttää PSA:n aikataulua luodaksesi edeltäjäsuhteita tehtävien välille. **Tehtävät**-arvon alla olevalla **Edeltäjä**-kentällä on vähintään yksi arvo kuvastamaan tehtäviä, joista toinen tehtävä on riippuvainen. Kun tehtävälle määritetään edeltäjäarvoja, tehtävä voi alkaa vasta, kun kaikki edeltäjätehtävät on suoritettu. Riippuvuuden vuoksi tehtävän suunniteltu alkamispäivä määritetään uudelleen siksi päiväksi, jona edeltäjätehtävät on suoritettu loppuun.

Tämä tehtävätila ei vaikuta edeltävien/riippuvaisten tehtävien alkamis- ja päättymispäiviin tehtäviin päivityksiin.

## <a name="task-mode"></a>Tehtävätila 

Tehtävätila määrittää lehtisolmutehtävien aikataulutuksen. PSA tukee kunkin tehtävän kahta tehtävätilaa: automaattinen aikataulutus ja manuaalisen aikataulutus.

### <a name="auto-scheduling"></a>Automaattinen aikataulutus 
 
Kun tehtävätilan arvoksi määritetään **Automaattisesti aikataulutettu**, ajoitusmoduuli käyttää ajoitussääntöjä tehtävän määritteisiin määrittäessään tehtävän ajoitusta.

#### <a name="scheduling-rules"></a>Ajoitussäännöt

Oletusarvoisesti lehtisolmutehtävän alkamispäiväksi määritetään projektin aikataulun mukainen alkamispäivä, jos tehtävällä ei ole edeltäjiä. Lehtisolmutehtävän kesto vastaa aina alkamis- ja päättymispäivämäärien välisten työpäivien lukumäärää. Kun tehtävä ajoitetaan automaattisesti, aikataulutusmoduuli noudattaa seuraavia sääntöjä:

- Tehtävän alkamis- ja päättymispäivien on aina oltava projektin ajoituskalenterin mukaisia työpäiviä. 
- Tehtävillä, joilla on edeltäjätehtäviä, alkamispäiväksi määritetään automaattisesti sen edeltäjien myöhäisin päättymispäivä.
- Työmäärä lasketaan seuraavalla kaavalla: Henkilömäärä × Kesto × Normaalin työpäivän tuntimäärä projektikalenterissa.

### <a name="manual-scheduling"></a>Manuaalinen aikataulutus

Jos automaattisen aikataulutuksen säännöt eivät vastaa tarpeitasi, voit määrittää tehtävätilaksi **Manuaalisesti aikataulutettu**. Tämä asetus estää aikataulutusmoduulia laskemasta muiden ajoitusmääritteiden arvoja. Tehtävätilasta riippumatta edeltäjän määrittäminen tehtävälle vaikuttaa aina riippuvaisen tehtävän alkamispäivään.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
