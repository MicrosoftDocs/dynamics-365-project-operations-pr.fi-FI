---
title: Resurssipyynnön lähettäminen
description: Tässä aiheessa on tietoja projektiresurssinpyynnön lähettämisestä.
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 12/1/2018
ms.topic: article
author: JohnPBurrows
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
ms.openlocfilehash: bcea3d640d7e9ee2b071c55bff9ade3268edb319
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/16/2020
ms.locfileid: "4075441"
---
# <a name="submitting-a-resource-request"></a>Resurssipyynnön lähettäminen

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Voit lähettää luodun resurssivaatimuksen resurssipyyntönä. Pyyntö lähetetään sitten resurssipäällikölle toteutusta varten.

1. Napauta Project Service Automation (PSA) **Projektit** -sivulla **Ryhmä** -välilehteä nähdäksesi varattavissa olevat resurssit. 
2. Valitse luettelosta yleinen resurssi, jolla on resurssitarve, ja valitse sitten **Lähetä pyyntö.**

![Resurssipyynnön lähettäminen](media/RM-how-to-18.png)

Yleisen ryhmän jäsenen pyynnön tila muuttuu tilaksi **Lähetetty**.

Kun resurssipäällikkö on täyttänyt pyynnön, yleinen resurssi korvataan nimetyllä resurssilla, jos resurssipäällikkö täyttää pyynnön nimetyn resurssin varauksella. Muussa tapauksessa yleinen resurssi säilyy ryhmässä ja pyynnön tilaksi muuttuu **Vaatii tarkistusta** , jos resurssipäällikkö on ehdottanut nimettyä resurssia.
