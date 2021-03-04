---
title: Työrakenteen luominen
description: Tässä aiheeessa selostetaan, miten luodaan työrakenne (WBS) sisältäen perusohjausobjektit uudessa aikataulutuksen käyttöliittymässä.
author: ruhercul
manager: tfehr
ms.date: 01/07/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: d7fa645e78d2206e333d9f85fcec0f7a9c213c23
ms.sourcegitcommit: 260ce052fed760bb44c514517806049ca13a5459
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/08/2021
ms.locfileid: "4841331"
---
# <a name="create-a-work-breakdown-structure-wbs"></a>Työrakenteen (WBS) luominen

Projektiaikataulu ilmaisee, mikä työ on suoritettava, mitkä resurssit suorittavat työn, ja aikajakson, jonka puitteissa työn on valmistuttava. Aikataulu kuvastaa kaikkea työtä, joka liittyy projektin toimittamiseen oikeaan aikaan. Dynamics 365 Project Operationsissa voit luoda projektin aikataulun seuraavasti:

  - Työn jakaminen helposti hallittaviksi tehtäviksi.
  - Kunkin tehtävän edellyttämän ajan arvioiminen.
  - Tehtävien riippuvuuksien määrittäminen.
  - Tehtävie kestojen määrittäminen.
  - Tehtävien yleisten resurssien arvioiminen. 

Projektiaikataulu luodaan **Aikataulut**-välilehdessä **Projekti**-sivulla.

## <a name="tasks"></a>Tehtävät

Projektiaikataulun luomisen ensimmäinen vaihe on jakaa työ hallittavissa oleviin osiin. Project Operationsin aikataulu tukee seuraavia toimintoja:

- Yhteenvetotehtävät tai säilössä olevat tehtävät
- Lehtisolmutehtävät

### <a name="summary-tasks"></a>Yhteenvetotehtävät

Yhteenvetotehtäviin voi tallentaa muita yhteenvetotehtäviä tai lehtisolmun tehtäviä. Niillä ei ole omia työmääriä tai kustannuksia. Sen sijaan niiden työmäärät ja kustannukset ovat koosteita niiden säilötehtävien työmääristä ja kustannuksista. Yhteenvetotehtävän alkamispäivä on säiliötehtävien alkamispäivä ja päättymispäivä säiliötehtävien päättymispäivä. Yhteenvetotehtävän nimeä voi muokata, mutta aikataulutusominaisuuksia (kuten työmäärä, päivämäärät, kesto) ei voi muokata. Jos poistat yhteenvetotehtävän, poistat myös kaikki sen säiliötehtävät.

### <a name="leaf-node-tasks"></a>Lehtisolmutehtävät

Lehtisolmutehtävät edustavat projektin yksityiskohtaisinta työtä. Niillä on arvioitu työmäärä, resursseja, suunnitellut alkamis- ja päättymispäivämäärät ja kesto.

## <a name="create-a-task-hierarchy"></a>Luo tehtävähierarkia

### <a name="add-a-task"></a>Lisää tehtävä

Toimi seuraavien vaiheiden mukaisesti yhden tai useamman tehtävän lisäämiseksi.

1. Siirry kohtaan **Projektit** ja valitse ja avaa projektitietue, jolle haluat luoda aikataulun. 
2. Valitse **Tehtävät**-välilehti. 
3. Valitse **Lisää uusi tehtävä**, kirjoita tehtävän nimi ja paina Enter-näppäintä.
2. Kirjoita toinen tehtävän nimi ja paina Enter-näppäintä uudelleen, kunnes saat täydellisen tehtäväluettelon.

### <a name="manage-hierarchy-of-a-task"></a>Tehtävän hierarkian hallinta

Kun tehtävä sisennetään, siitä tulee suoraan sen yläpuolella olevan tehtävän alitehtävä. Tällöin tehtävän aikataulutunnus lasketaan uudelleen siten, että se perustuu uuden päätehtävänsä aikataulutunnukseen ja vastaa monitasoista numerointijärjestelmää. Päätehtävä on nyt yhteenvetotehtävä. Siten siitä tulee alitehtäviensä kooste. Kun tehtävä korotetaan, se ei enää ole päätehtävänsä alitehtävä. Tällöin aikataulutunnus lasketaan uudelleen siten, että se vastaa tehtävän päivitettyä syvyyttä ja sijaintia hierarkiassa. Aiemman päätehtävän työmäärä, kustannukset ja päivämäärät lasketaan sitten uudelleen siten, että ne eivät enää sisällä entistä alitehtävää.

Toimi seuraavien vaiheiden mukaisesti tehtävän sisentämiseksi tai korottamiseksi.

1. Valitse **Projekti**-sivulla **Tehtävät**-välilehdessä **Yhteenvetotehtävät**-kohdan alla kolme pystysuorassa olevaa pistettä ja valitse sitten **Tee alitehtävä**. 
2. Valitse tehtävä, jonka haluat sisentää tai korottaa. Jos haluat valita useita tehtäviä, valitse tehtävä, pidä CTRL-näppäintä alhaalla ja valitse sitten muut tehtävät.
2. Voit myös valita **Sisennä** tai **Korota alitehtävä**, jos haluat siirtää tehtäviä yhteenvetotehtävien alle tai ulos niistä.

### <a name="move-tasks-up-and-down"></a>Tehtävien siirtäminen ylöspäin ja alaspäin

Tehtävät voidaan siirtää mille tahansa työrakenteen tasolle kahdella tavalla:

- Valitse yksi tai useampi tehtävä ja vedä ne haluamaasi sijaintiin.
- Valitse vähintään yksi tehtävä, napsauta hiiren kakkospainikkeella ja valitse **Leikkaa**, valitse aikataulun kohdesolu, napsauta hiiren kakkospainikkeella ja valitse **Liitä**.

## <a name="task-attributes"></a>Tehtävän määritteet

Tehtävän nimi kuvaa työtä, joka on suoritettava. Project Operationsissa tehtävään yhdistetyt määritteet kuvaavat tehtävän aikataulua ja henkilöstötarpeita.

## <a name="schedule-attributes"></a>Aikataulun määritteet

Määritteet **Työmäärä**, **Alkamispäivä**, **Päättymispäivä** ja **Kesto** määrittävät tehtävän aikataulun.

Seuraavassa taulukossa on esitetty lisää aikataulun määritteitä.

| **Lopullinen näyttönimi** | **Lopullinen kuvaus** |
| --- | --- |
| Suoritettu työmäärä (tuntia) | Tehtävän suoritettu työmäärä tunteina. |
| Kesto | Näyttää tehtävän keston päivinä. |
| Kokonaistyömäärä | Tehtävän kokonaistyömäärä tunteina. |
| Lopetus | Lopetuspäivä ja ‑aika. |
| % valmiina | Tehtävän valmistumisen prosenttiosuus. |
| Projektin joukko | Tehtävätaulukko voidaan ryhmitellä joukkojen mukaan, jotta kullakin joukolla on oma sarake. |
| Jäljellä oleva työmäärä (tuntia) | Tehtävän jäljellä oleva työmäärä tunteina. |
| Käynnistä | Aloituspäivä ja ‑aika. |
| Nimi | Tehtävän nimi. |
| Tunnus | Näyttää työrakenteen tehtävän tunnuksen. |

## <a name="staffing-attributes"></a>Henkilöstömääritteet

Henkilöstömääritteitä käytetään aikataulun **Resurssit**-kentän kautta. Voit joko hakea olemassa olevaa resurssia tai valita **Luo** ja lisätä projektiryhmän jäsenen uudeksi resurssiksi **Pikaluonti**-ruudussa.

Kenttiä **Rooli**, **Resursointiyksikkö** ja **Toimen nimi** käytetään tehtävän henkilöstötarpeiden kuvaamiseen. Näitä henkilöstömääritteitä käytetään yhdessä tehtävän aikataulun kanssa käytettävissä olevien resurssien hakemiseen tehtävälle.

   - **Rooli**: määritä tehtävän suorittamiseen tarvittava resurssityyppi.
   - **Resursointiyksikkö**: määritä yksikkö, josta tehtävän resurssit kohdennetaan. Tämä määrite vaikuttaa tehtävän kustannus- ja myyntiarvioon, jos resurssin kustannukset ja laskutushinta määritetään resursointiyksikköjen perusteella.
   - **Toimen nimi**: anna ystävällinen nimi sille yleiselle resurssille, joka toimii työn lopulta suorittavan resurssin paikkamerkkinä.

**Resurssit** -kenttä sisältää yleisen resurssin tai lopulta nimetyn resurssin toimen nimen.

**Luokka** -kenttä sisältää arvot, jotka ilmaisevat laajan työtyypin, johon tehtävä voidaan ryhmitellä. Tämä kenttä ei vaikuta aikataulutukseen tai henkilöstöön. Kenttää käytetään sen sijaan vain raportointiin.

## <a name="task-dependencies"></a>Tehtävän riippuvuudet

Voit käyttää Project Operationsin aikataulua luodaksesi edeltäjäsuhteita tehtävien välille. **Edeltäjä**-kentällä on vähintään yksi arvo kuvastamaan tehtäviä, joista toinen tehtävä on riippuvainen. Kun tehtävälle määritetään edeltäjäarvoja, tehtävä voi alkaa vasta, kun kaikki edeltäjätehtävät on suoritettu. Riippuvuuden vuoksi tehtävän suunniteltu alkamispäivä määritetään uudelleen siksi päiväksi, jona edeltäjätehtävät on suoritettu loppuun.

Tämä tehtävätila ei vaikuta edeltävien/riippuvaisten tehtävien alkamis- ja päättymispäiviin tehtäviin päivityksiin.

## <a name="accessibility-and-keyboard-shortcuts"></a>Helppokäyttötoiminnot ja pikanäppäimet

**Aikataulut**-ruudukko on täysin käytettävissä, ja siinä voidaan käyttää näytönlukijoita (esim. Narrator, JAWS tai NVDA). Voit siirtyä ruudukkoalueella nuolinäppäimillä (kuten Microsoft Excelissä), voit käyttää sarkainnäppäintä siirtyäksesi vuorovaikutteisten käyttöliittymäelementtien välillä ja voit käyttää alanuolinäppäintä, Enter-näppäintä tai välilyöntiä valitaksesi ja avataksesi avattavia valikkoja.


[!INCLUDE[footer-include](../includes/footer-banner.md)]