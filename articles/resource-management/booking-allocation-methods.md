---
title: Varauksen kohdistusmenetelmät
description: Tässä aiheessa on tietoja siitä, miten varauksen kohdistusmenetelmät toimivat Project Operationsissa.
author: ruhercul
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: ruhercul
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 74f8889022e42a7bbd37879df870401c0e103446
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/28/2020
ms.locfileid: "3897672"
---
# <a name="booking-allocation-methods"></a>Varauksen kohdistusmenetelmät

_**Koskee:** Project Operationsin resurssiin / muuhun kuin resurssiin perustuvia skenaarioita, Lite-käyttöönotto-kaupasta proformalaskutukseen_

Voit käyttää muutamaa erilaista varausten kohdistustapaa, kun lisäät ryhmän jäsenen suoraan projektiin **Ryhmä**-välilehdessä tai varaat resurssin projektille tai tarpeelle aikataulutaulukossa. Tässä aiheessa kerrotaan, miten kukin tapa toimii ja mitkä tavat voivat johtaa resurssien ylivaraukseen.

## <a name="booking-allocation-methods"></a>Varauksen kohdistusmenetelmät

Voit käyttää seuraavaa kuutta varauksen kohdistusmenetelmää.

- [Täysi kapasiteetti](#full)
- [Jäljellä oleva kapasiteetti](#remaining)
- [Kapasiteettiprosentti](#percentage)
- [Jaa tunnit tasaisesti](#evenly)
- [Etupainotteiset tunnit](#front)
- [Ei ole](#none)

### <a name="full-capacity"></a><a name="full"></a>Täysi kapasiteetti 
Täysi kapasiteetti -menetelmä varaa resurssin täyden kapasiteetin tietyn alku- ja loppupäivämäärän välille. Jos resurssin kalenteriin on määritetty esimerkiksi kahdeksan tunnin työpäivä viitenä päivänä viikossa, viisi työpäivää kattavan alku- ja loppupäivämäärän määrittäminen varaa resurssin 40 tunniksi. Varaus on tehty ilman, että resurssin jäljellä olevaa kapasiteettia otetaan huomioon. Jos resurssi on jo varattu muille projekteille tuona aikana, 40 tuntia varataan lisätunteina. Tämä voi aiheuttaa ylivarauksia.

### <a name="remaining-capacity"></a><a name="remaining"></a>Jäljellä oleva kapasiteetti
Jäljellä oleva kapasiteetti -menetelmä on käytettävissä vain, jos varaus tehdään suoraan projektiin aikataulutaulukon avulla. Tämä tapa varaa resurssin käytettävän kapasiteetin tiettynä ajanjaksona. Jos resurssin kapasiteetti on esimerkiksi 40 tuntia viikossa ja resurssi on jo varattu 10 tunnille, kyseiseltä viikolta varataan jäljellä olevat 30 tuntia.

### <a name="percentage-capacity"></a><a name="percentage"></a>Kapasiteettiprosentti
Kapasiteettiprosentti-menetelmä varaa resurssin kapasiteettiprosentin perusteella tietyn alku- ja loppupäivämäärän välille. Jos resurssin kalenteriin on määritetty esimerkiksi kahdeksan tunnin työpäivä viitenä päivänä viikossa, viisi työpäivää 50 prosentin kapasiteetilla kattavan alku- ja loppupäivämäärän määrittäminen varaa resurssin 20 tunniksi. Päivän yksittäiset varaukset jaetaan tasaisesti ajanjaksolle. Tässä esimerkissä päivää kohti tulee neljä tuntia. Varaus on tehty ilman, että resurssin jäljellä olevaa kapasiteettia otetaan huomioon. Jos resurssi on jo varattu muille projekteille tuona aikana, 20 tuntia varataan lisätunteina. Tämä voi aiheuttaa ylivarauksia.

### <a name="evenly-distribute-hours"></a><a name="evenly"></a>Jaa tunnit tasaisesti
Jaa tunnit tasaisesti -menetelmä varaa resurssin tietyille tunneille. Tunnit jaetaan tasan päivää kohti tietyn alku- ja loppupäivämäärän väliselle ajalle. Jos esimerkiksi varaat resurssin 20 tunnin ajalle viiden päivän jaksolla, tämä menetelmä jakaa 20 tuntia tasan niin, että päivää kohti tulee neljä tuntia. Varaus on tehty ilman, että resurssin jäljellä olevaa kapasiteettia otetaan huomioon. Jos resurssi on jo varattu muille projekteille tuona aikana, 20 tuntia varataan lisätunteina. Tämä voi aiheuttaa ylivarauksia.

### <a name="front-load-hours"></a><a name="front"></a>Etupainotteiset tunnit
Etupainotteiset tunnit -menetelmä varaa resurssin tietyille tunneille. Päiväkohtaiset tunnit jaetaan etupainotteisesti tietyn alku- ja loppupäivämäärän väliselle ajalle. Etupainotteisuus kuluttaa resurssin käytettävissä olevaa kapasiteettia niin, että ensin tullut resurssi kulutetaan ensin. Jos resurssin työaikataulu on esimerkiksi kahdeksan tuntia päivässä ja viisi päivää viikossa, eikä resurssilla ole tällä hetkellä varauksia, resurssin varaaminen 20 tunniksi viiden työpäivän ajaksi aiheuttaa seuraavan päivittäisen varauskaavan: 

|                           |    Päivä 1    |    Päivä 2    |    Päivä 3    |    Päivä 4    |    Päivä 5    |    Yhteensä    |
|---------------------------|-------------|-------------|-------------|-------------|-------------|-------------|
|    **Aiemmin luodut varaukset**    |    0        |    0        |    0        |    0        |    0        |    0        |
|    **Uusi varaus**          |    8        |    8        |    4        |    0        |    0        |    20       |

Etupainotteinen tapa ottaa huomioon aiemmin luodut varaukset ja käytettävissä olevan kapasiteetin. Jos samalla resurssilla on jo esimerkiksi 20 tunnin varaus työviikolla, uudet varaukset kuluttavat jäljellä olevaa kapasiteettia seuraavasti:

|                     | Päivä 1 | Päivä 2 | Päivä 3 | Päivä 4 | Päivä 5 | Yhteensä |
|---------------------|-------|-------|-------|-------|-------|-------|
| **Aiemmin luodut varaukset** | 8     | 8     | 4     | 0     | 0     | 20    |
| **Uusi varaus**       | 0     | 0     | 4     | 8     | 8     | 20    |

Koska käytettävissä oleva kapasiteetti otetaan huomioon, näyttöön voi tulla virhesanoma, jos resurssilla ei ole jäljellä olevaa kapasiteettia varausta varten. Kun tämä tapa on käytössä, ylivaraus ei ole mahdollista.

### <a name="none"></a><a name="none"></a>Ei ole
Ei ole -menetelmä on käytettävissä vain, jos projektin varaukset tehdään **Ryhmä**-välilehdessä. Tämä tapa lisää resurssin projektiin ryhmän jäsenenä, mutta ei luo varauksia, jotka käyttävät resurssin kapasiteettia. Tätä tapaa käytetään, kun projektipäällikön ryhmän oletusjäsen lisätään projektin luomisen yhteydessä. Projektin luonut projektipäällikkökäyttäjä lisätään projektiin oletusarvoisesti. Tällöin projektin entiteettitietueella on omistaja ja projektissa on yksi hyväksyjä. Nykyisellä käyttäjällä ei ole varauksia. Jos haluat varata resurssin, voit poistaa resurssin ja lisätä sen uudelleen eri kohdistustavan avulla tai lisätä resurssin tehtäviin ja luoda sitten delegoinneille varauksia **Täsmäytys**-välilehden **Laajenna varaukset** -kohdan avulla.

## <a name="allocation-methods-that-lead-to-overbooking"></a>Ylivaraukseen johtavat kohdistustavat
Seuraavat kohdistustavat johtavat ylivaraukseen, jos resurssi on jo vahvistettu muissa projekteissa (tai muissa työtilauksissa tai aikataulutettavissa entiteeteissä):

- Täysi kapasiteetti
- Kapasiteettiprosentti
- Jaa tunnit tasaisesti

Kun käytössä on jokin näistä kolmesta kohdistustavasta, resurssin ylivarauksesta ei ilmoiteta. Voit korjata ylivarauksen aikataulutaulukon avulla.
