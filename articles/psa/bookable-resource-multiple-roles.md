---
title: Projektin myynnin ja kustannusten arvioiminen, kun varattavissa oleva resurssi täyttää useita rooleja projektissa
description: Tässä aiheessa kerrotaan, miten hinnoitteludimensioita käytetään sellaisen resurssin hinnoittelun ja kustannusten tukemiseen, joka täyttää useita rooleja projektissa.
author: rumant
ms.custom:
- dyn365-projectservice
ms.date: 10/01/2020
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.reviewer: johnmichalak
ms.openlocfilehash: f8b84de740a3d610e49acea8fa13885b977b440c
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/14/2022
ms.locfileid: "8590710"
---
# <a name="estimate-project-sales-and-costs-when-a-bookable-resource-fills-multiple-roles-for-a-project"></a>Projektin myynnin ja kustannusten arvioiminen, kun varattavissa oleva resurssi täyttää useita rooleja projektissa 

[!include [banner](../includes/psa-now-project-operations.md)]

Projektipohjaiset yritykset tarvitsevat usein yhden resurssin täyttämään useita rooleja projektissa. Kukin näistä rooleista voidaan hinnoitella ja kustannuslaskea eri tavalla, mikä tarkoittaa sitä, että saman resurssin aika projektissa voi saada erilaisen talousarvion kunkin roolin laskutus- ja kustannushinnan mukaan. Project Service Automation sallii nimetyn resurssin Ryhmän jäsen -tietueen arvojen määrittämisen ja sallii eri korvaamiset kullekin tehtävälle, johon ryhmän jäsen on delegoitu.

Seuraavassa esimerkissä selitetään, miten tämän arvon yksinkertainen korvaaminen mahdollistaa sen, että resurssilla voi olla useita rooleja projektissa, ja kussakin roolissa eri kustannus- ja laskutushinnat.

## <a name="create-tasks"></a>Tehtävien luominen
Luo kaksi projektitehtävää, jotka ovat 40 tuntia, tehtävä A ja tehtävä B. Valitse tehtävän B edeltäjäksi tehtävä A.

## <a name="set-up-role-and-organization-unit-for-a-generic-project-team-member"></a>Yleisen projektiryhmän jäsenen roolin ja organisaatioyksikön määrittäminen

1. Valitse **Aikataulu**-sivulla tehtävän A **Tehtävä**-rivi. 
2. Valitse **Resurssit**-kentässä avattavasta luettelosta **Luo**.
3. Määritä **Ryhmän jäsenen pikaluonti** -sivulla sen yleisen ryhmän jäsenen määritteet, joka voi suorittaa tämän tehtävän.
4. Valitse haluamasi rooli ja organisaatioyksikkö ja valitse sitten **Tallenna ja sulje**. Yleinen ryhmän jäsen luodaan ja delegoidaan tähän tehtävään. 

Toista nämä vaiheet tehtävän B kohdalla ja varmista, että tehtävään B luodun yleisen ryhmän jäsenen rooli ja organisaatioyksikkö ovat eri kuin tehtävässä A. 

## <a name="set-up-role-and-organization-unit-for-a-project-task"></a>Projektitehtävän roolin ja organisaatioyksikön määrittäminen

1. Kun olet luonut tehtävän A, valitse se ja valitse sitten **Muokkaa tehtävää**.
2. Etsi **Tehtävän tiedot**-sivulla **Rooli**- ja **Organisaatioyksikkö**-kentät ja lisää tämän tehtävän suorittavalta resurssilta vaadittavat arvot. 

  > [!NOTE]
  > Jos olet tekemässä skenaarioita Project Service Automationin esittelytietojen avulla, valitse rooliksi **Consulting Lead** ja **Fabrikam US** organisaatioyksiköksi.

3. Valitse tehtävä B ja valitse sitten **Muokkaa tehtävää**.
4. Etsi **Tehtävän tiedot**-sivulla **Rooli**- ja **Organisaatioyksikkö**-kentät ja lisää tämän tehtävän suorittavalta resurssilta vaadittavat arvot. Varmista, että **Rooli**- ja **Organisaatioyksikkö**-kenttien arvot ovat erilaiset tehtävälle B kuin tehtävälle A. 

  > [!NOTE]
  > Jos olet tekemässä skenaarioita Project Service Automationin esittelytietojen avulla, valitse rooliksi **Network Technician** ja **Fabrikam US** organisaatioyksiköksi.

5. Tallenna ja sulje **Tehtävän tiedot** -sivu. 

## <a name="team-member-and-estimates-behavior"></a>Ryhmän jäsenen ja arvioiden toiminta 

1. Valitse **Tehtävän tiedot** -sivun **Ryhmän jäsen** -kohdassa kaksi yleistä ryhmän jäsentä ja valitse sitten **Luo tarpeet**. 
2. Valitse ryhmän jäsenen rivi **Consulting Lead** ja valitse sitten **Varaa**. Aikataulutaulukko avautuu ja varaa resurssin tälle tarpeelle.
3. Valitse ryhmän jäsenen rivi **Network Technician** ja valitse sitten **Varaa**. Aikataulutaulukko avautuu ja varaa saman resurssin kyseiselle tarpeelle.

### <a name="team-member-grid"></a>Ryhmän jäsen -ruudukko 
Huomaa **Ryhmän jäsen** -ruudukossa, että kaksi yleistä ryhmän jäsenen tietuetta poistetaan ja että ne on korvattu yhdellä resurssilla. Kyseiselle resurssille on määritetty yksi arvojoukko, joka näyttää **Rooli**- ja **Organisaatioyksikkö**-kenttien oletusarvojoukot.
Kun laajennat kyseisen Ryhmän jäsen -tietueen riviä, näet kummallekin tehtävälle erilliset delegoinnit Ryhmän jäsen -tietueessa. Kullakin delegointirivillä on tehtäväkohtaiset arvot kentille **Rooli** ja **Organisaatioyksikkö**. 

### <a name="estimates-grid"></a>Arvioruudukko 
Kun siirryt **Arviot**-ruudukkoon, huomaat, että saman resurssin molemmat delegoinnit hinnoitellaan eri tavalla.
Resurssin delegointi tehtävssä A on hinnoiteltu käyttämällä **Rooli**-määritteen arvoa **Consulting Lead**. Saman resurssin delegointi tehtävssä B on hinnoiteltu käyttämällä **Rooli**-määritteen arvoa **Network Technician**.



[!INCLUDE[footer-include](../includes/footer-banner.md)]
