---
title: Työrakenteen päivitykseen liittyvät seikat
description: Tässä aihe on tietoja työrakenteen päivittämisestä Project Service Automation 2.x:n ja 3.x:n välillä.
ms.custom:
- dyn365-projectservice
ms.date: 10/18/2019
ms.topic: article
author: ruhercul
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
ms.openlocfilehash: 5258813410c3cea015775898cc72ba1574549edd8ee0c8b7aad8c94943eb5a60
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/06/2021
ms.locfileid: "6992337"
---
# <a name="upgrade-considerations-for-the-work-breakdown-structure"></a>Työrakenteen päivitykseen liittyvät seikat

[!include [banner](../includes/psa-now-project-operations.md)]

Tässä aihe on tietoja työrakenteen päivittämisestä Project Service Automation 2.x:n ja 3.x:n välillä. Tämä aihe määrittää project Service Automation (PSA) -projektin terveen tilan, jota päivityksen onnistuminen edellyttää. Siinä on myös tietoja yleisistä estoehdoista, jotka aiheuttavat päivityksen epäonnistumisen. Lisätietoja projektitehtävien ja niiden toimintojen määrittämisestä projektiaikataulussa on aiheessa [Projektiaikataulut](project-creating.md).

## <a name="key-entities"></a>Avainentiteetit
Seuraavat entiteetit vaaditaan tarkkaa työrakennetta varten, jossa on jo resursseja:

- [Projekti](/dynamics365/customerengagement/on-premises/developer/entities/msdyn_project)
- [Projektiryhmä](/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projectteam)
- [Projektin tehtävä](/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projecttask)
- [Resurssimääritykset](/dynamics365/customerengagement/on-premises/developer/entities/msdyn_resourceassignment)
- [Projektitehtävän riippuvuus](/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projecttaskdependency)
- [Varattavissa olevat resurssit](/dynamics365/customerengagement/on-premises/developer/entities/bookableresource)

Voit määrittää työrakenteen, jossa on resurssit, tekemällä seuraavat toimet:

1. Luo uusi projekti. Lisätietoja uuden projektin luomisesta on aiheessa [msdyn_project](/dynamics365/customerengagement/on-premises/developer/entities/msdyn_project).
2. Luo yksi tai useampia tehtäviä. Lisätietoja tehtävän luomisesta on aiheessa [msdyn_projecttask](/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projecttask).
3. Määritä tehtäväriippuvuudet. Lisätietoja on kohdassa [projektitehtävien riippuvuus](/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projecttaskdependency).
4. Kohdenna projektiryhmän jäsenet projektiin. Lisätietoja on aiheessa [msdyn_projectteam](/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projectteam).
5. Kohdenna projektiryhmän jäsenet tehtäviin. Lisätietoja on aiheessa [msdyn_resourceassignment](/dynamics365/customerengagement/on-premises/developer/entities/msdyn_resourceassignment).

## <a name="project-team-relationships"></a>Projektiryhmän suhteet

Onnistuneen päivityksen varmistamiseksi seuraavat suhteet on säilytettävä oikein:
- Kaikkien projektiryhmän jäsenten on oltava liitettyinä varattavissa olevaan resurssiin.
- Kaikkien projektiryhmän jäsenten on oltava liitettyinä samaan projektiin. 

## <a name="project-task-relationships"></a>Projektitehtävän suhteet
Onnistuneen päivityksen varmistamiseksi seuraavat suhteet on säilytettävä oikein:

- Liittyvät tehtävät on liitettävä samaan projektiin.
- Jokaisella rivitehtävällä on oltava päätehtävä.
- Jokaisella tehtävällä on oltava projekti.

### <a name="valid-conditions"></a>Kelvolliset ehdot

- Kaikkien tehtävien keston on oltava suurempi tai yhtä suuri kuin (> =) 1 tunti ja alle 1 800 000 minuuttia (1 250 päivää). *
- Kaikilla tehtävillä on oltava alkamispäivä aikaisintaan 2000/01/01. *
- Kaikilla tehtävillä on oltava alkamispäivä viimeistään 17 vuoden kuluttua nykyisestä päivästä. *
- Kaikkien tehtävien alkamispäivän on oltava aiemmin tai samana päivänä kuin niiden päättymispäivä.
- Kaikilla tapahtumatyypeillä luokissa (Kulu, Materiaali, Vero ja Aika) on oltava arvot **Oletusyksikkö** ja **Yksikköryhmä**.
- Päivämäärämuotoja, joissa on kirjaimia, on vältettävä.

### <a name="potential-mitigation-steps"></a>Mahdolliset korjaavien toimien vaiheet
- Erikoishaku-toiminnon avulla voit määrittää projektitehtävät, jotka eivät sisällä projektitunnusta.
- Erikoishaku-toiminnon avulla voit määrittää projektitehtävät, joiden ajoitettu kesto on suurempi kuin 1 800 000.
- Ennen kuin teet muutoksia tietoihin, tutki entiteettiin liittyviä mukautuksia, jotka ovat voineet saada tiedot huonoon tilaan. Nämä mukautukset on selvitettävä, ennen kuin jatkat mitään tietoihin liittyviä päivityksiä.
- Jos tunnistetut tehtävät on määritetty orvoiksi, harkitse näiden tehtävien poistamista, jos niitä ei tarvita, tai niiden liitettämistä oikeaan pääprojektiin.
- Jos tehtävän kesto on suurempi kuin 1 250 päivää, kannattaa lisätä useita tehtäviä, jotka kuvaavat kokonaiskestoa, jos mahdollista.

> [!NOTE]
> Tähdellä (\*) merkityt kohteet sisältävät rajoituksia, jotka johtuvat siitä, että customer relationship management (CRM) tukee vain 7 320 toistuvuuslaajennusta. Sinun täytyy pysyä tämän rajan alapuolella.

## <a name="resource-assignment-relationships"></a>Resurssien kohdentamisen suhteet
Onnistuneen päivityksen varmistamiseksi seuraavat suhteet on säilytettävä oikein:

- Kaikkien työrakenteen resurssikohdennusten on liityttävä samaan projektiin.
- Kaikkien työrakenteen resurssikohdennusten on liityttävä projektiryhmän jäseniin samassa projektissa.

### <a name="potential-mitigation-steps"></a>Mahdolliset korjaavien toimien vaiheet
- Määritä kaikki tehtävät, jotka eivät kuulu edellä mainittuihin ehtoihin.  
- Kaikki resurssivaraukset, jotka eivät ole enää kelvollisia, on poistettava.

## <a name="project-task-dependency-relationships"></a>Projektitehtävän riippuvuuksien suhteet
Onnistuneen päivityksen varmistamiseksi seuraavat suhteet on säilytettävä oikein:

- Kaikkien projektitehtäväriippuvuuksien on liityttävä samaan projektiin.
- Samaan tehtävän riippuvuuteen ei voi viitata useammin kuin kerran.


[!INCLUDE[footer-include](../includes/footer-banner.md)]