---
title: Projektin myynnin ja kustannusten arvioiminen, kun varattavissa oleva resurssi täyttää useita rooleja projektissa
description: Tässä aiheessa kerrotaan, miten hinnoitteludimensioita käytetään sellaisen resurssin hinnoittelu- ja kostannusarvioiden tukemiseen, joka täyttää useita rooleja projektissa.
author: rumant
ms.date: 11/16/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 2cc632d43bfcbdd23c1d06ff5203385bccf9926d
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/14/2022
ms.locfileid: "8589146"
---
# <a name="estimate-project-sales-and-costs-when-a-bookable-resource-fills-multiple-roles-on-a-project"></a>Projektin myynnin ja kustannusten arvioiminen, kun varattavissa oleva resurssi täyttää useita rooleja projektissa 

_**Koskee:** Project Operations resursseihin ja ei-varastoitaviin perustuvissa skenaarioissa, Lite-käyttöönotto – kaupasta proformalaskutukseen, Project Operations varastoitavien ja tuotantopohjaisten skenaarioissa_ 

Projektipohjaiset yritykset tarvitsevat usein yhden resurssin täyttämään useita rooleja projektissa. Kukin rooli voi olla hinnoiteltu ja sen kulut laskettu eri tavoin. Tämä tarkoittaa sitä, että saman resurssin aika projektissa voidaan arvioida rahallisesti eri arvoiseksi riippuen kunkin roolin laskutus- ja kustannushinnoittelusta. Voit määrittää nimetyn resurssin ryhmän jäsen tietueen arvot erikseen kullekin tehtävälle, johon ryhmän jäsen on delegoitu.

Seuraavassa esimerkissä kuvataan, miten yksinkertainen arvon ohitus sallii resurssille projektissa useita rooleja, joilla on eri kustannus-ja laskutushinnat.

## <a name="create-tasks"></a>Tehtävien luominen
Jotta voisit luoda tehtäviä, sinun täytyy lisätä tehtäviä sekä yhteenvetotehtäviä, joiden jälkeen tehtävä on delegoitava, ennen kuin lisäät tehtävän keston. 

### <a name="add-tasks-and-summary-tasks"></a>Tehtävien ja yhteenvetotehtävien lisääminen
Toimi seuraavien vaiheiden mukaisesti tehtävän lisäämiseksi.

1. Siirry kohtaan **Projektit** ja avaa projekti, johon haluat lisätä tehtäviä.
2. Valitse **Lisää uusi tehtävä**. Anna tehtävälle nimi ja paina **Enter-näppäintä**.
3. Syötä toinen tehtävän nimi ja paina **Enter-näppäintä**. Toista tätä, kunnes sinulla on täydellinen luettelo tehtävistä.
3. Jos haluat sisentää tehtäviä **Yhteenveto**-tehtävien alla, valitse tehtävän nimen vieressä olevat kolme pystysuorassa olevaa pistettä ja valitse sitten **Tee alitehtävä**. 

  > [!TIP]
  > Jos haluat valita useita tehtäviä, valitse tehtävä, pidä **CTRL-näppäintä** alhaalla, ja valitse toinen tehtävä.
  >
  > Voit myös valita **Korota alitehtävä**, jos haluat siirtää tehtäviä ulos **Yhteenveto**-tehtävistä.

### <a name="assign-tasks"></a>Delegoi tehtäviä

Toimi seuraavien vaiheiden mukaisesti tehtävien delegoimiseksi.

1. Valitse tehtävän  **Delegoitu**-sarakkeesta henkilökuvake.
2. Valitse ryhmän jäsen luettelosta tai syötä tekstiä, jos haluat hakea nimen.

### <a name="add-task-duration-and-columns"></a>Tehtävän keston ja sarakkeiden lisääminen

On usein helpointa aloittaa projektin rakentaminen kestosta. Toimi seuraavien vaiheiden mukaisesti tehtävän keston lisäämiseksi.

1. Kirjoita tehtävän **Kesto**-sarakkeeseen päivien määrä, jonka arvelet tehtävän suorittamiseen kuluvan. Jos haluat käyttää eri aikayksikköä, kirjoita numero sekä sana **tuntia**, **viikkoa** tai **kuukautta**.
2. Jos haluat, että tehtävä näkyy vinoneliön muotoisena välitavoitteena **Aikajana**-näkymässä, syötä **Kesto**-sarakkeeseen **0 päivää** .
3. Paina **Enter-näppäintä**  siirtyäksesi tehtävän **Kesto**-kenttään ja jatka kestojen syöttöä.

  > [!NOTE]
  > Yhteenvetotehtävien kestoa ei voi määrittää.

Voit lisätä projektiin sarakkeita antaaksesi lisätietoja. Voit tehdä tämän valitsemalla **Lisää sarake**. 

Lisätietoja on kohdassa [Projektin luominen](https://support.microsoft.com/en-us/office/create-a-project-a5b5e823-fb2e-45fd-be00-7d84422d9749).

## <a name="set-up-the-role-and-organization-unit-for-a-generic-project-team-member"></a>Määritä yleisen projektiryhmän jäsenen rooli ja organisaatioyksikkö
Suorita seuraavat vaiheet määrittääksesi roolin ja organisaatioyksikön yleiselle projektiryhmän jäsenelle.

1. Valitse **Tehtävät**-sivulla **Tehtävä**-rivi tehtävälle **Tehtävä A**. 
2. Valitse **Delegoitu**-kohdasta **Lisää yleinen resurssi**. Tämä avaa **Ryhmän jäsenen pikaluonti** -sivun.
3. Määritä **Ryhmän jäsenen pikaluonti** -sivulla sen yleisen ryhmän jäsenen määritteet, joka voi suorittaa tämän tehtävän.
4. Valitse haluamasi rooli ja organisaatioyksikkö ja valitse sitten **Tallenna ja sulje**. Yleinen ryhmän jäsen luodaan ja delegoidaan tähän tehtävään. 
5. Toista vaiheet 1-4 tehtävälle **Tehtävä B**. Tehtävällä **Tehtävä B** on kuitenkin oltava eri rooli ja eri organisaatioyksikkö delegoituna yleiseen ryhmään kuin tehtävällä **Tehtävä A**. 

## <a name="set-up-the-role-and-organization-unit-for-a-project-task"></a>Määritä projektitehtävän rooli ja organisaatioyksikkö
Suorita seuraavat vaiheet määrittääksesi roolin ja organisaatioyksikön tehtävälle.

1. Kun olet luonut **Tehtävän A**, valitse se ja valitse sitten **i**-kuvake **Tehtävän tiedot**-ruudun avaamiseksi. 
2. Siirry **Tehtävän tiedot**-ruudun alaosaan ja valitse **Näytä tiedot** avataksesi **Tehtävän tiedot** -sivun.
3. Lisää tämän tehtävän suorittamisen resurssilta vaatimat arvot **Tehtävän tiedot**-sivulla kohdissa **Rooli** ja **Organisaatioyksikkö**. 

  > [!NOTE]
  > Jos suoritat tämän skenaarion käyttämällä Project Operationsin esittelytietoja, valitse rooliksi **Consulting Lead** ja organisaatioyksiköksi **Fabrikam US**.

4. Valitse **Tehtävä B** ja valitse sitten tehtävä.
5. Valitse **i**-kuvake avataksesi **Tehtävän tiedot**-ruudun. 
6. Siirry **Tehtävän tiedot**-ruudun alaosaan ja valitse **Näytä tiedot** avataksesi **Tehtävän tiedot** -sivun.
7. Lisää tämän tehtävän suorittavalta resurssilta vaaditut arvot **Tehtävän tiedot**-sivulla kohdissa **Rooli** ja **Organisaatioyksikkö**. Arvojen kohdissa **Rooli** ja **Organisaatioyksikkö** tehtävälle **Tehtävä B** on oltava eri arvoja kuin arvojen tehtävälle **Tehtävä A**. 

  > [!NOTE]
  > Jos suoritat tämän skenaarion käyttämällä Project Operationsin esittelytietoja, valitse rooliksi **Network Technician** ja organisaatioyksiköksi **Fabrikam US**.

8. Tallenna ja sulje **Tehtävän tiedot** -sivu. 

## <a name="team-member-and-estimates-behavior"></a>Ryhmän jäsenen ja arvioiden toiminta 
Jos haluat ymmärtää **Ryhmän jäsen**-ruudukon ja arvioiden toimintaa, suorita seuraavat vaiheet.

1. Valitse **Ryhmän jäsen**-ruudukossa kaksi yleistä ryhmän jäsentä ja valitse sitten **Luo vaatimukset**. Tämä luo resurssitarpeet. 
2. Valitse ryhmän jäsenen rivi **Consulting Lead** ja valitse sitten **Varaa**. Aikataulutaulukko avautuu, ja siinä on resurssiluettelo. Valitse resurssi ja sen jälkeen **Varaa** varataksesi resurssin kyseiselle vaatimukselle.
3. Valitse ryhmän jäsenen rivi **Network Technician** ja valitse sitten **Varaa**. Aikataulutaulukko avautuu, ja siinä on resurssiluettelo. Valitse sama resurssi kuin yllä ja sen jälkeen **Varaa** varataksesi resurssin kyseiselle vaatimukselle.

### <a name="team-member-grid"></a>Ryhmän jäsen -ruudukko 

Kaksi yleistä ryhmän jäsen -tietuetta poistetaan **Ryhmän jäsen** -ruudukosta ja korvataan vain yhdellä resurssilla. Resurssilla on yksi arvojoukko, joka on **Roolien** ja **Organisaatioyksiköiden** oletusarvojoukko.

Kun laajennat kyseisen ryhmän jäsen tietueen riviä, voit nähdä ryhmän jäsen -tietueessa erilliset varaukset kummallekin tehtävälle. Kullakin delegointirivillä on tehtäväkohtaiset arvot kentille **Rooli** ja **Organisaatioyksikkö**. 

### <a name="estimates-grid"></a>Arvioruudukko 

**Arviot**-ruudukossa saman resurssin eri määritykset hinnoitellaan eri tavalla. Resurssin varaus tehtävässä **Tehtävä A** on hinnoiteltu käyttäen **Rooli**-määritteen arvoa **Consulting Lead**. Saman resurssin varaus tehtävässä **Tehtävä B** on hinnoiteltu käyttäen **Rooli**-määrityksen arvoa **Network Technician**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]