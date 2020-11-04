---
title: Myyntiprosessien yleiskatsaus
description: Tämä aihe sisältää tietoja perustason myyntiprosesseista.
author: rumant
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 09/23/2019
ms.topic: article
ms.prod: ''
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app: ''
ms.openlocfilehash: c70760748c5faa87f6738ab7e2ab593e2df49e41
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/16/2020
ms.locfileid: "4075547"
---
# <a name="sales-processes-overview"></a>Myyntiprosessien yleiskatsaus

Projektiperusteisessa organisaatiossa käytettävät myyntiprosessit eroavat tuoteperusteisessa organisaatiossa käytettävistä myyntiprosesseista. Tämä ero johtuu siitä, että projektiperusteisten organisaatioiden myyntisyklit ovat pidempiä ja edellyttävät mukautettuja arviointimenetelmiä tarjousten analysoimiseksi ja luomiseksi kullekin kaupalle. Dynamics 365 Project Operations käyttää joitakin seuraavia samoja toimintoja kuin myyntiprosessit:

- Myyntiprosessin seurannassa käytetään Liidi-tietuetta.
- Hyväksyttyjä liidejä seurataan mahdollisuuksina.
- Kaikkia mahdollisuuteen liittyviä artefakteja käytetään. Näitä artefakteja ovat esimerkiksi myyntiryhmä, sidosryhmät, todennäköisyys, luokitus, myyntivaiheet ja liiketoimintaprosessit.
- Mahdollisuudelle luodaan useita tarjouksia.
- Myyntitilaus luodaan antamalla tarjouksen tilaksi **Suljettu voitettuna**. Project Operationsissa myyntitarjousta on muokattu, ja sitä kutsutaan projektisopimukseksi.

## <a name="estimate-a-sale"></a>Myynnin arvioiminen
Myynnin arvo voidaan arvioida aiemmin toimitettujen projektien ja projektin monimutkaisuuden perusteella. Jos projektiin liittyy laajennuksia aiempaan projektiin tai projektin toimittajan asiantuntemus on korkeatasoista ja siinä käytetään tuttuja työmalleja, voidaan käyttää yksinkertaisempaa arviointiprosessia. Monimutkaisissa projekteissa ostoprosessi on yleensä pidempi. Siksi myös myynninarviointiprosessissa on enemmän vaiheita. Projektin alussa myyntiryhmä käyttää asiakkuuspäällikköjen ja aihealueen asiantuntijoiden panosta luodakseen ylätason arvioinnin kullekin erilliselle tarjoukseen sisältyvälle työkomponentille. Tarjousrivit edustavat näitä työkomponentteja. 

Vuot luoda tarjoukselle ylätason arvioinnin. Tämä ylätason arviointi korvataan myöhemmin yksityiskohtaisemmalla arvioinnilla, joka perustuu vakioitujen projektimallien avulla luotavaan projektisuunnitelmaan. Näiden mallien avulla voit laatia aikataulun ja määrittää rahallisia arvoja tarjoukselle ja sen komponenteille (tarjousriveille). 

Voit luoda projektille useita tarjouksia ja koota ne yksittäiselle mahdollisuustietueelle. Lopulta jokin tarjouksista asetetaan tilaan **Suljettu voitettuna** ja projektisopimus tai työnkuvaus luodaan. Projektisopimus sisältää sovitun arvon kullekin komponentille (sopimusrivi), jonka asiakas hyväksyy toimitettavaksi. Työnkuvaus luodaan yleensä Microsoft Word -asiakirjana. Kaikki asiakkaalle projektin toimittamisen aikana lähetettävät laskut viittaavat projektisopimukseen tai työnkuvaukseen.

Voit myös luoda vaihtoehtoisia tarjouksia yhdelle mahdollisuustietueelle tai määrittää järjestelmän siten, että projektisopimus luodaan, kun tarjous voitetaan. Tällöin voit liittää projektisopimuksen tietueeseen Word-asiakirjan, joka edustaa työnkuvausta.

## <a name="configure-the-sales-process"></a>Myyntiprosessin määrittäminen
Voit määrittää myyntiprosessit käyttämällä liiketoimintaprosesseja. Nämä prosessit sisältävät ohjatun visualisoidun liittymän, jonka avulla kaupat etenevät myyntiprosessin vaiheissa.

Yrityksen myyntiprosessissa voi olla esimerkiksi seuraavat kuusi vaihetta:

1. Hyväksy
2. Arvio
3. Sisäinen arviointi
4. Sopimus
5. Toimita
6. Sulje
 
Organisaatiossasi saatetaan käyttää eri entiteettejä edustamaan samaa kauppaa sen muuttuessa. Aikaisin myyntiprosessissa kauppaa edustaa Mahdollisuus-entiteetti. Ajan myötä ja kaupan tarkentuessa saatetaan käyttää ylätason arvioita yhden tai useamman tarjouksen luomiseen. Jos sisäiset ja asiakkaan sidosryhmät tarkistavat yhden näistä tarjouksista, kauppaa edustaa Tarjous-entiteetti. Kun asiakas on hyväksynyt tarjouksen, kauppaa edustaa projektisopimus tai työnkuvaus. Näiden toimintojen tukemiseksi jokainen prosessin vaihe on liiketoimintaprosessien rakenteessa linkitetty eri tietokantataulukkoon.

Myyntiprosessin **Hyväksy** -vaihetta voidaan tukea Mahdollisuus-entiteetillä. Vaiheita **Arvio** ja **Sisäinen arviointi** voidaan tukea Tarjous-entiteetillä. Vaiheita **Sopimus** , **Toimitus** ja **Sulkeminen** voidaan tukea Projektisopimus-entiteetillä.

Kun siirrät kauppoja vaiheiden läpi, järjestelmä pyytää sinua luomaan asianmukaisen entiteettitietueen auttamaan ja opastamaan sinua prosessissa. Vaiheet voivat olla ehdollisia. Jos esimerkiksi tarvitset tarjoukselle sisäisen arvioinnin vain, kun tarjouksessa käytetään mukautettua hinnastoa, voit määrittää kyseisen ehdon vastaavassa liiketoimintaprosessin vaiheessa. **Sisäinen arviointi** -vaihe näkyy tällöin vain sellaisten tarjousten osalta, joissa käytetään mukautettua hinnastoa. Kaikissa muissa kaupoissa ja tarjouksissa **Arvio** -vaihetta seuraa **Sopimus** -vaihe.

> [!NOTE]
> Project Operationsissa on omat sivut mahdollisuus-, tarjous-, tilaus- ja laskuentiteettitietueille. Nämä tietueet on luotava näiden entiteettien projektitietosivujen avulla. Muussa tapauksessa et voi avata tietueita **Projektin tiedot** -sivulla. Jos haluat avata tietueen **Projektin tiedot** -sivulla, poista tietue ja luo se uudelleen käyttämällä **Projektin tiedot** -sivua, jossa näiden entiteettityyppien liiketoimintalogiikka varmistaa, että tietueen **Tyyppi** -kenttä on määritetty oikein ja että kaikki pakolliset käsitteet on alustettu oikein.


## <a name="track-revisions-to-quotes-and-project-plans-in-the-sales-cycle"></a>Muutosten jäljittäminen tarjouksiin ja projektisuunnitelmiin myyntisyklin aikana
Project Operationsissa tarjoukseen tehtyjä muutoksia ei voi jäljittää. Sen sijaan kulloisenkin tarjouksen tilaksi on asetettava **Suljettu hävittynä** ja sen jälkeen luotava uusi tarjous. Tarjous voidaan kopioida tai projektiperusteinen tarjous kloonata.

## <a name="track-comments-and-approvals-of-quotes-and-project-contracts"></a>Tarjousten ja projektisopimusten kommenttien ja hyväksyntöjen seuraaminen
Voit hallita tarjousten ja projektisopimusten arviointia ja hyväksymistä tietueseinän ja viestien avulla. Organisaatiosi voi luoda mukautettuja työnkulkuja ja laajennuksia kohdentamaan, uudelleenohjaamaan ja hallitsemaan arvioinnin ja hyväksynnän työkohteiden ilmoituksia.
