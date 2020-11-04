---
title: Projektin myynnin ja kustannusten arvioiminen, kun varattavissa oleva resurssi täyttää useita rooleja projektissa
description: Tässä aiheessa on tietoja siitä, miten hinnoitteludimensioita voidaan käyttää sellaisen resurssin hinnoittelun ja kustannuslaskennan tukemiseen, joka täyttää useita rooleja projektissa.
author: rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 10/01/2020
ms.topic: article
ms.service: business-applications
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 8ddc827a4170c5576c0a4350b51e6a119094ac50
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/16/2020
ms.locfileid: "4075400"
---
# <a name="estimate-project-sales-and-costs-when-a-bookable-resource-fills-mulitple-roles-on-a-project"></a>Projektin myynnin ja kustannusten arvioiminen, kun varattavissa oleva resurssi täyttää useita rooleja projektissa 

Projektipohjaiset yritykset tarvitsevat usein yhden resurssin suorittamaan useita rooleja projektissa. Kukin näistä rooleista voidaan hinnoitella ja kustannuslaskea eri tavalla, mikä tarkoittaa sitä, että saman resurssin aika projektissa voi saada erilaisen talousarvion kunkin roolin laskutus- ja kustannushinnan mukaan. Project Service Automation sallii nimetyn resurssin Ryhmän jäsen -tietueen arvojen määrittämisen ja sallii eri korvaamiset kullekin tehtävälle, johon ryhmän jäsen on delegoitu.

Seuraavassa esimerkissä selitetään, miten tämän arvon yksinkertainen korvaaminen mahdollistaa sen, että resurssilla voi olla useita rooleja projektissa, ja kussakin roolissa eri kustannus- ja laskutushinnat.

## <a name="create-tasks"></a>Tehtävien luominen
Luo kaksi projektitehtävää, jotka ovat 40 tuntia, tehtävä A ja tehtävä B. Valitse tehtävän B edeltäjäksi tehtävä A.

## <a name="set-up-role-and-organization-unit-for-a-generic-project-team-member"></a>Yleisen projektiryhmän jäsenen roolin ja organisaatioyksikön määrittäminen

1. Valitse **Aikataulu** -sivulla tehtävän A **Tehtävä** -rivi. 
2. Valitse **Resurssit** -kentässä avattavasta luettelosta **Luo**.
3. Määritä **Ryhmän jäsenen pikaluonti** -sivulla sen yleisen ryhmän jäsenen määritteet, joka voi suorittaa tämän tehtävän.
4. Valitse haluamasi rooli ja organisaatioyksikkö ja valitse sitten **Tallenna ja sulje**. Yleinen ryhmän jäsen luodaan ja delegoidaan tähän tehtävään. 

Toista nämä vaiheet tehtävän B kohdalla ja varmista, että tehtävään B luodun yleisen ryhmän jäsenen rooli ja organisaatioyksikkö ovat eri kuin tehtävässä A. 

## <a name="set-up-role-and-organization-unit-for-a-project-task"></a>Projektitehtävän roolin ja organisaatioyksikön määrittäminen

1. Kun olet luonut tehtävän A, valitse se ja valitse sitten **Muokkaa tehtävää**.
2. Etsi **Tehtävän tiedot** -sivulla **Rooli** - ja **Organisaatioyksikkö** -kentät ja lisää tämän tehtävän suorittavalta resurssilta vaadittavat arvot. 

  > [!NOTE]
  > Jos olet tekemässä skenaarioita Project Service Automationin esittelytietojen avulla, valitse rooliksi **Consulting Lead** ja **Fabrikam US** organisaatioyksiköksi.

3. Valitse tehtävä B ja valitse sitten **Muokkaa tehtävää**.
4. Etsi **Tehtävän tiedot** -sivulla **Rooli** - ja **Organisaatioyksikkö** -kentät ja lisää tämän tehtävän suorittavalta resurssilta vaadittavat arvot. Varmista, että **Rooli** - ja **Organisaatioyksikkö** -kentissä on eri arvot ovat tehtävissä A ja B. 

  > [!NOTE]
  > Jos olet tekemässä skenaarioita Project Service Automationin esittelytietojen avulla, valitse rooliksi **Network Technician** ja **Fabrikam US** organisaatioyksiköksi.

5. Tallenna ja sulje **Tehtävän tiedot** -sivu. 

## <a name="team-member-and-estimates-behaviour"></a>Tiimin jäsenen ja arvioiden käyttäytyminen 

1. Valitse **Tehtävän tiedot** -sivun **Ryhmän jäsen** -kohdassa kaksi yleistä ryhmän jäsentä ja valitse sitten **Luo tarpeet**. Tämä luo resurssitarpeet. 
2. Valitse ryhmän jäsenen rivi **Consulting Lead** ja valitse sitten **Varaa**. Aikataulutaulukko avautuu ja varaa resurssin tälle tarpeelle.
3. Valitse ryhmän jäsenen rivi **Network Technician** ja valitse sitten **Varaa**. Aikataulutaulukko avautuu ja varaa saman resurssin kyseiselle tarpeelle.

### <a name="team-member-grid"></a>Ryhmän jäsen -ruudukko 
Huomaa **Ryhmän jäsen** -ruudukossa, että kaksi yleistä ryhmän jäsenen tietuetta poistetaan ja että ne on korvattu yhdellä resurssilla. Kyseiselle resurssille on määritetty yksi arvojoukko, joka näyttää **Rooli** - ja **Organisaatioyksikkö** -kenttien oletusarvojoukot.
Kun laajennat kyseisen Ryhmän jäsen -tietueen riviä, näet kummallekin tehtävälle erilliset delegoinnit Ryhmän jäsen -tietueessa. Kullakin delegointirivillä on tehtäväkohtaiset arvot kentille **Rooli** ja **Organisaatioyksikkö**. 

### <a name="estimates-grid"></a>Arvioruudukko 
Kun siirryt **Arviot** -ruudukkoon, huomaat, että saman resurssin molemmat delegoinnit hinnoitellaan eri tavalla.
Resurssin delegointi tehtävssä A on hinnoiteltu käyttämällä **Rooli** -määritteen arvoa **Consulting Lead**. Saman resurssin delegointi tehtävssä B on hinnoiteltu käyttämällä **Rooli** -määritteen arvoa **Network Technician**.





