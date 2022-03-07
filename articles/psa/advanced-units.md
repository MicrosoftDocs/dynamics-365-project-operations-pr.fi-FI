---
title: Yksikköryhmät ja yksiköt
description: Tässä aiheessa on tietoja yksikköryhmistä ja yksiköistä.
author: rumant
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/05/2019
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
ms.openlocfilehash: 78f154856acf796f408491c5873cb29da8ac55bb
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/16/2020
ms.locfileid: "4075364"
---
# <a name="unit-groups-and-units"></a>Yksikköryhmät ja yksiköt

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Yksikköryhmät ja yksiköt Microsoft Dynamics 365:n perusentiteettejä. Yksikkö on yksittäinen mittayksikkö ja useita yksikköjä voidaan ryhmitellä yksikköryhmiksi. Yksikköryhmää kutsutaan joskus yksikköaikatauluksi Dynamics 365:n käyttöliittymässä (UI). 

Seuraavassa on esimerkkejä yksiköistä ja yksikköryhmistä:
 
- **Yksikköryhmä**: Etäisyys 
    - **Yksiköt**: Maili, Kilometri jne.
- **Yksikköryhmä**: Aika
    - **Yksiköt**: Tunti, Päivä, Viikko jne. 

Kun useita yksikköjä määritetään yksikköryhmäksi, niiden välille on myös määritettävä muuntokerroin määrittämällä ensimmäinen määritettävä yksikkö yksikköryhmän oletusyksiköksi tai ensisijaiseksi yksiköksi. 

Jos esimerkiksi **Aika**-yksikköryhmässä ensimmäisenä yksikkönä määritetään **Tunti**, järjestelmä määrittää yksikön **Tunti** oletusyksiköksi. Jos seuraavana yksikkönä määritetään **Päivä**, on määritettävä muuntokerroin yksikköjen **Päivä** ja **Tunti** välille. Jos sitten kolmantena yksikkönä määritetään **Viikko**, on määritettävä muuntokerroin yksikköjen **Viikko** ja joko **Päivä** tai **Tunti** välille. 

Seuraavassa kuvassa esitetään esimerkkimääritys yksikölle **Päivä**, jossa **Määrä**-kentässä näkyy päivässä olevien tuntien määrä, ja yksikölle **Viikko**, jossa **Määrä**-kentässä näkyy viikossa olevien päivien määrä.

> ![Yksikköryhmä: tietosivu](media/advanced-2.png)

## <a name="using-units-and-unit-groups"></a>Yksikköjen ja yksikköryhmien käyttö

Dynamics 365 Project Service Automation käyttää yksikköjä ja yksikköryhmiä käsitelläkseen sekä kulujen että ajan arvioiden ja merkintöjen käsittelyyn. 

Kulujen osalta kullakin kululuokalla on oletusarvoinen yksikköryhmänsä ja yksikkönsä. Nämä arvot otetaan oletusarvoiksi kululuokkien hinnastomerkinnöille. 

Sinulla voi olla esimerkiksi **Kilometrikorvaus**-niminen kululuokka. Sillä on **Etäisyys**-niminen yksikköryhmä ja oletusyksikkö nimeltä **Maili**. Jos määrität **Etäisyys**-yksikköryhmän siten, että siinä on kaksi yksikköä (**Maili** ja **Kilometri**), voit määrittää yhden hinnaston **Kilometrikorvaus**-luokalle kaksi hintaa: mailikohtainen hinta ja kilometrikohtainen hinta.

| Kululuokka  | Yksikköryhmä  | Yksikkö      | Hinnoittelutapa  | Yksikköhinta  |
|-------------------|---------------|-----------|-------------------|-------------------|
| Kilometrikorvaus           | Etäisyys      | Maili      | Yksikköhinta    | 10 USD            |
| Kilometrikorvaus           | Etäisyys      | Kilometri | Yksikköhinta    |  6 USD            |

Kun lisäät projektiin kulun, järjestelmä määrittää hinnan kyseisen kulun luokan ja yksikön yhdistelmän perusteella. 

| Kulun kuvaus        | Kululuokka  | Yksikkö  | Määrä  | Yksikköhinta   |
|----------------------------|---------------------|-------|-----------|----------------|
| Asiakkaan toimipaikkaan ajaminen | Kilometrikorvaus             | Maili  | 10        | 10 USD         |

Aikaa varten jokaisella hinnasto-otsikolla on **Oletusaikayksikkö**-kenttä. Arvo määritetään, kun hinnasto-otsikko luodaan. Tämän jälkeen kyseistä yksikköä käytetään kaikkien hinnaston rooliperusteisten hintojen määrittämisessä.

**Tarjouksen aika** -kentän arviorivit voidaan ilmaista missä tahansa aikayksikössä. Projektien arvioriveissä ja projektien merkinnöissä kuitenkin voidaan käyttää vain **Tunti**-aikayksikköä. Jos aikamerkinnän tai arviorivin yksikkö ei vastaa hinnaston yksikköä kyseistä roolia varten, järjestelmä muuntaa hinnan niiksi yksiköiksi, jotka on määritetty projektiarviossa tai projektin todellisessa tapahtumassa.

Seuraavassa esimerkissä esitetään, miten PSA käyttää yksikköryhmiä, yksikköjä ja muuntokertoimia.
- Yksiköt

   - **Yksikköryhmä**: Aika 
   - **Yksiköt**: Tunti 
    
    - **Päivä** – Muuntokerroin: 8 tuntia       
    - **Viikko** – Muuntokerroin: 40 tuntia  
        
- Projektin A hinnastomääritys:

    - **Nimi**: UK:n myyntihinnat 2016 
    - **Oletusaikayksikkö**: Päivä 
    - **Valuutta**: GBP

| Rooli      | Yksikköryhmä | Yksikkö | Organisaatioyksikkö | Hinta   |
|-----------|------------|------|---------------------|---------|
| Kehittäjä | Time       | Day  | Contoso UK          | 800 GBP |

### <a name="time-entry"></a>Aikamerkintä

Seuraavassa taulukossa esitetään kolmen tunnin projektin tuloksena oleva PSA:n luoma myyntipuolen tapahtuma.


| Projekti   | Tehtävä    | Rooli      | Määrä | Yksikkö  | Yksikköhinta | Laskuttamattoman myynnin summa |
|-----------|---------|-----------|----------|-------|------------|-----------------------|
| Projekti A | Suunnittele  | Kehittäjä | 3        | Hour  | 100 GBP    | 300 GBP               |

## <a name="time-unit-faq"></a>Aikayksikön usein kysytyt kysymykset

### <a name="does-psa-convert-to-different-units-in-the-case-of-expenses"></a>Muuntaako PSA kulut eri yksiköiksi?
Ei. Yksikköjen muuntaminen toimii vain ajan osalta. Jos järjestelmä ei kulujen osalta löydä hintaa kululuokan ja yksikön yhdistelmälle, hinnan oletusarvo on 0,00.

### <a name="why-does-psa-convert-time-units"></a>Miksi PSA muuntaa aikayksikköjä?
Joissakin maissa tai tietyillä alueilla laskutushinnat on lakisääteisesti ilmaistava päivissä. Tarjousmenettelyn aikana hintaneuvottelut ja alennukset toteutetaan käyttämällä kunkin laskutettavan roolin päivähintoja. Aikatauluarvio ja aikamerkintä toteutetaan tunneissa. PSA muuntaa aikayksikköjä tukeakseen tätä eroa.

### <a name="can-time-units-be-changed-on-project-estimates"></a>Voidaanko projektiarvioiden aikayksikköjä muuttaa?
Ei. Projektiarviot on tällä hetkellä rajoitettu tunteihin eikä tähän voi tehdä muutoksia.

### <a name="can-units-and-unit-groups-be-edited-deleted-and-added"></a>Voiko yksikköjä ja yksikköryhmiä muokata, poistaa ja lisätä?
Kyllä. **Aika**-yksikköryhmää ja **Tunti**-yksikköä lukuun ottamatta kaikkia yksikköjä voi poistaa tai muokata ja uusia yksikköjä voi lisätä. PSA:ssa **Aika**-yksikköryhmää ja **Tunti**-yksikköä ei voi poistaa. Niitä voidaan kuitenkin päivittää **Nimi**-kenttää varten käännetyllä tekstillä.
