---
title: Yleisten varattavissa olevien resurssien kohdentaminen tehtävälle ja projektiryhmälle
description: Tässä aiheessa on tietoja yleisten resurssien varaamisesta tehtäville ja projektiryhmille.
author: JohnPBurrows
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 12/11/2018
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
ms.openlocfilehash: ca0999ae5413d824dd1384fe2262e5226695a5f8
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/16/2020
ms.locfileid: "4075363"
---
# <a name="assign-generic-bookable-resources-to-a-task-and-generate-resource-requirements"></a>Yleisten varattavissa olevien resurssien kohdennus tehtävälle ja resurssitarpeiden luominen 

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Nimettyjen tai todellisten resurssien projektillesi varaamisen ja kohdentamisen lisäksi voit kohdentaa yleisiä resursseja projektitehtäville. Tämä resurssit voivat toimia nimettyjen resurssien paikkamerkkeinä, kunnes olet valmis täyttämään projektisi nimetyillä resursseilla. 

1. Avaa Project Service Automationissa (PSA:ssa) **Projekti** -sivu ja kirjoita yleisen resurssin toimen nimi **Aikataulut** -välilehden **Resurssi** -soluun. Voit myös valita solun **Resurssi** -solun avataksesi resurssinvalitsimen ja kirjoittaa nimen yleiselle resurssille, jonka haluat luoda.

![Yleisen ryhmän jäsenen luominen ja kohdennus](media/RM-how-to-9.png)

Näkyviin tulee **Pikaluonti: projektiryhmän jäsen** -paneeli. 

2. Kirjoita yleisen ryhmän jäsenen rooli ja napsauta **Tallenna**.

![Yleisen ryhmän jäsenen pikaluonti](media/RM-how-to-10.png)

3. Kun olet luonut uuden yleisen ryhmän jäsenen, se kohdennetaan tehtävälle. Voit jatkaa kyseisen yleisen resurssin kohdentamista muille tehtäväaikataulun tehtäville.

![Yleisten ryhmän jäsenten kohdentaminen tehtäville](media/RM-how-to-11.png)

4. Kun olet kohdentanut yleisen resurssin, voit luoda resurssitarpeen ja täyttää sen suoralla varaamisella tai lähettämällä resurssipyynnön resurssipäällikölle.

![Yleisen ryhmän jäsenen tarpeen luominen](media/RM-how-to-12.png)

Ryhmän jäsenten ruudukossa voit resurssinvalitsimen yllä mainitulla tavalla käyttämisen lisäksi lisätä suoraan yleisiä resursseja. Lisättävillä resurssilla on resurssitarve, joka perustuu **Pikaluonti: projektiryhmän jäsen** -paneelissa määritettyihin alkamis- ja päättymispäiviin ja kohdennustapaan.

Voit nähdä eron, jos lisäät yleisen ryhmän jäsenen suoraan ja kohdennat yleiselle resurssille tehtävämäärän, joka ylittää niiden tarvittujen tuntien määrän, jotka sen on katettava. Valitse **Luo tarve** , jos haluat luoda tarpeen uudelleen tasapainottaaksesi tarvittavat tunnit ja kohdennukset.

Voit myös napsauttaa ryhmäruudukon **Resurssitarve** -linkkiä avataksesi tarpeen ja lisätäksesi osaamisalueita, ensisijaisia resursseja jne.

![Resurssitarve](media/RM-how-to-13.png)

