---
title: Myyntiprosessit
description: Tämä aihe sisältää tietoja perustason myyntiprosesseista.
author: rumant
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 2561a54af6bdb9764a318f012fdc53f7b3298893
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/10/2021
ms.locfileid: "5145174"
---
# <a name="sales-processes"></a>Myyntiprosessit

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Projektiperusteisessa organisaatiossa käytettävät myyntiprosessit eroavat tuoteperusteisessa organisaatiossa käytettävistä myyntiprosesseista. Tämä ero johtuu siitä, että projektiperusteisten organisaatioiden myyntisyklit ovat pidempiä ja edellyttävät mukautettuja arviointimenetelmiä tarjousten analysoimiseksi ja luomiseksi kullekin kaupalle. Dynamics 365 Project Service Automationissa käytetään joitakin samoja toimintoja kuin Dynamics 365 Salesin myyntiprosesseissa. Seuraavassa on joitakin esimerkkejä.

- Myyntiprosessin seurantaan käytetään Liidi-entiteettiä.
- Hyväksyttyjä liidejä seurataan mahdollisuuksina. Myyntiprosessi voi alkaa myös mahdollisuudesta.
- Kaikkia mahdollisuuteen liittyviä artefakteja käytetään. Näitä artefakteja ovat esimerkiksi myyntiryhmä, sidosryhmät, todennäköisyys, luokitus, myyntivaiheet ja liiketoimintaprosessit.
- Mahdollisuudelle luodaan useita tarjouksia.
- Myyntitilaus luodaan asettamalla tarjouksen tilaksi **Suljettu voitettuna**. PSA:ssa myyntitarjous on muokattu, ja sitä kutsutaan projektisopimukseksi.

Seuraavassa kuvassa näkyy projektiperusteisen organisaation tyypillinen myyntiprosessi.

> ![Myyntiprosessi projektiperusteisessa organisaatiossa](media/basic-guide-1.png)

## <a name="estimating-a-sale"></a>Myynnin arviointi
Myynnin arvo voidaan arvioida aiemmin toimitettujen projektien ja projektin monimutkaisuuden perusteella. Jos projektiin liittyy laajennuksia aiempaan projektiin tai projektin toimittajan asiantuntemus on korkeatasoista ja siinä käytetään tuttuja työmalleja, voidaan käyttää yksinkertaisempaa arviointiprosessia. Monimutkaisissa projekteissa ostoprosessi on yleensä pidempi. Siksi myös myynninarviointiprosessissa on enemmän vaiheita. Projektin alussa myyntiryhmä käyttää asiakkuuspäällikköjen ja aihealueen asiantuntijoiden panosta päästäkseen alkuun ylätason arvioinnin luomisessa kullekin erilliselle tarjoukseen sisältyvälle työkomponentille. Tarjousrivit edustavat näitä työkomponentteja. 

Vuot luoda tarjoukselle ylätason arvioinnin. Tämä ylätason arviointi korvataan myöhemmin yksityiskohtaisemmalla arvioinnilla, joka perustuu vakioitujen projektimallien avulla luotavaan projektisuunnitelmaan. Näiden mallien avulla voit laatia aikataulun ja määrittää rahallisia arvoja tarjoukselle ja sen komponenteille (tarjousriveille). 

Voit luoda projektille useita tarjouksia ja koota ne yksittäisen mahdollisuusentiteettityypin alle. Lopulta jokin näistä tarjouksista asetetaan tilaan **Suljettu voitettuna** ja projektisopimus tai työnkuvaus luodaan. Projektisopimus sisältää sovitun arvon kullekin komponentille (sopimusrivi), jonka asiakas hyväksyy toimitettavaksi. Työnkuvaus luodaan yleensä Microsoft Word -asiakirjana. Kaikki asiakkaalle projektin toimittamisen aikana lähetettävät laskut viittaavat projektisopimukseen tai työnkuvaukseen.

Voit myös luoda vaihtoehtoisia tarjouksia yhden mahdollisuusentiteettityypin alle tai määrittää järjestelmän siten, että projektisopimus luodaan, kun tarjous voitetaan. Tällöin voit liittää projektisopimuksen tietueeseen Word-asiakirjan, joka edustaa työnkuvausta.

![Tarjouksen sulkeminen projektisopimuksen luomista varten](media/basic-guide-2.png)

## <a name="configuring-the-sales-process"></a>Myyntiprosessin määrittäminen
Voit määrittää myyntiprosessisi käyttämällä Microsoft Dynamics 365:n liiketoimintaprosesseja. Liiketoimintaprosessit tarjoavat myyntihenkilöstölle opastetun visuaalisen liittymän, jota se voi käyttää siirtääkseen kauppoja yrityksellesi tyypillisten vaiheiden läpi.

Yrityksen myyntiprosessissa voi olla esimerkiksi seuraavat kuusi vaihetta:

1. Hyväksy
2. Arvio
3. Sisäinen arviointi
4. Palvelusopimus
5. Toimita
6. Sulje

Nuolenkärkipainikkeet (\>), jotka valitaan laajennettavaksi kussakin luotavassa mahdollisuusentiteettityypissä, edustavat näitä kuutta vaihetta.

![Liiketoimintaprosessien määritys Dynamics 365:ssä](media/basic-guide-3.png)
 
Organisaatiossasi saatetaan käyttää eri entiteettejä edustamaan samaa kauppaa sen muuttuessa. Aikaisin myyntiprosessissa kauppaa edustaa Mahdollisuus-entiteetti. Ajan myötä ja kaupan tarkentuessa saatetaan käyttää ylätason arvioita yhden tai useamman tarjouksen luomiseen. Jos sisäiset ja asiakkaan sidosryhmät tarkistavat yhden näistä tarjouksista, kauppaa edustaa Tarjous-entiteetti. Kun asiakas on hyväksynyt tarjouksen, kauppaa edustaa projektisopimus tai työnkuvaus. Näiden toimintojen tukemiseksi jokainen prosessin vaihe on liiketoimintaprosessien rakenteessa linkitetty eri tietokantataulukkoon.

Myyntiprosessin **Hyväksy**-vaihetta voidaan tukea Mahdollisuus-entiteetillä. Vaiheita **Arvio** ja **Sisäinen arviointi** voidaan tukea Tarjous-entiteetillä. Vaiheita **Sopimus**, **Toimitus** ja **Sulkeminen** voidaan tukea Projektisopimus-entiteetillä.

Kun siirrät kauppoja vaiheiden läpi, järjestelmä pyytää sinua luomaan asianmukaisen entiteettitietueen auttamaan ja opastamaan sinua prosessissa. Vaiheet voivat olla ehdollisia. Jos esimerkiksi tarvitset tarjoukselle sisäisen arvioinnin vain, kun tarjouksessa käytetään mukautettua hinnastoa, voit määrittää kyseisen ehdon vastaavassa liiketoimintaprosessin vaiheessa. **Sisäinen arviointi** -vaihe näkyy tällöin vain sellaisten tarjousten osalta, joissa käytetään mukautettua hinnastoa. Kaikissa muissa kaupoissa ja tarjouksissa **Arvio** -vaihetta seuraa **Sopimus**-vaihe.

> [!NOTE]
> PSA:ssa on omat sivunsa entiteeteille Mahdollisuus, Tarjous, Tilaus ja Lasku. Sinun on luotava projektipalvelun mahdollisuuksia, tarjouksia, tilauksia ja laskuja käyttämällä näiden entiteettien projektitietosivuja. Jos käytät tietueen luonnissa muuta sivua, et voi avata tietuetta **Projektitiedot**-sivun kautta. Jos haluat avata tietueen **Projektitiedot**-sivulta, sinun on poistettava tietue ja luotava se uudelleen käyttäen **Projektitiedot**-sivua. **Projektitiedot**-sivulla näiden entiteettityyppien liiketoimintalogiikat varmistavat, että tietueen **Tyyppi**-kenttä määritetään oikein ja että kaikki pakolliset konseptit alustetaan asianmukaisesti.

> ![Uuden tilauksen projektitiedot](media/basic-guide-4.png)
 
## <a name="differences-between-project-service-automation-and-sales"></a>Erot Project Service Automationin ja Salesin välillä
Vaikka PSA:n myyntiprosessissa käytetään Salesin myyntiprosessin perusominaisuuksia, niiden välillä on keskeisiä eroja projektiperusteisten organisaatioiden liiketoimintakäytännöissä esiintyvien vaihteluiden vuoksi. Seuraavassa on joitakin esimerkkejä.

- **Projektitarjoukset** – Project Service Automationissa tarjous suljetaan, kun tarjouksesta on luotu projektisopimus. Salesissa tarjous voidaan pitää avoimena, kun se on voitettu. Syynä tähän eroon, että tarjouksen ja projektisopimuksen vastaavuus sopii paremmin projektiperusteiselle organisaatiolle. 
- **Aktivoinnit ja muutokset** – PSA ei tue projektitarjousten aktivointeja ja muutoksia. Salesissa tarjous voidaan lukita muokkauksen estämiseksi.
- **Tarjouksen sulkeminen hävittynä tai voitettuna** – Kun projektitarjous suljetaan voitettuna tai hävittynä, mahdollisuus pysyy PSA:ssa avoimena. Kaikki muut mahdollisuuden tarjoukset suljetaan hävittynä. Kun tarjous suljetaan voitettuna tai hävittynä Salesissa, käyttäjää pyydetään toimimaan mahdollisuuden osalta. Taustalla oleva mahdollisuus suljetaan tai jätetään avoimeksi käyttäjän valinnan perusteella.

## <a name="tracking-revisions-to-quotes-and-project-plans-in-the-sales-cycle"></a>Muutosten jäljittäminen tarjouksiin ja projektisuunnitelmiin myyntisyklin aikana
PSA:ssa tarjoukseen tehtyjä muutoksia ei voi jäljittää. Sen sijaan kulloisenkin tarjouksen tilaksi on asetettava **Suljettu hävittynä** ja sen jälkeen luotava uusi tarjous. PSA:n avulla tarjous voidaan kopioida tai projektiperusteinen tarjous kloonata.

## <a name="tracking-comments-and-approvals-of-quotes-and-project-contracts"></a>Tarjousten ja projektisopimusten kommenttien ja hyväksyntöjen seuraaminen
Voit hallita tarjousten ja projektisopimusten arviointia ja hyväksymistä tietueseinän ja viestien avulla. Organisaatiosi voi luoda mukautettuja työnkulkuja ja laajennuksia kohdentamaan, uudelleenohjaamaan ja hallitsemaan arvioinnin ja hyväksynnän työkohteiden ilmoituksia.
