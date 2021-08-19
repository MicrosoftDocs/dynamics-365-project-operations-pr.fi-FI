---
title: Miksi en voi poistaa Todelliset arvot -entiteetin tietueita?
description: Tässä aiheessa on tietoja siitä, miksi Todelliset arvot -entiteetistä ei voi poistaa tietueita.
author: JPBurrows
ms.custom:
- dyn365-projectservice
ms.date: 11/6/2018
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
ms.openlocfilehash: d60a3586fd1f0f688bcd2626d039ebc1aa6b0925c90d676f0e716400d8e8d6dd
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/06/2021
ms.locfileid: "7002867"
---
# <a name="why-cant-i-delete-records-from-the-actuals-entity"></a>Miksi en voi poistaa Todelliset arvot -entiteetin tietueita?

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Project Service Automation (PSA) ei salli todellisten arvojen poistamista, koska ne toimivat virallisena tietolähteenä tapahtumille, joilla on taloudellisia vaikutuksia jäljempänä sijaitseviin järjestelmiin, kuten pääkirjaan. Jos todellisia arvoja voisi poistaa, tilinpäätösraportoinnin eheys voitaisi kyseenalaistaa. Kirjausketjun luomista varten asiakkaiden pitäisi käyttää kirjauskansioita luodakseen kompensoivia tapahtumia.



[!INCLUDE[footer-include](../includes/footer-banner.md)]