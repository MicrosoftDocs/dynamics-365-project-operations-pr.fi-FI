---
title: Miksi en voi poistaa Todelliset arvot -entiteetin tietueita?
description: Tässä aiheessa on tietoja siitä, miksi Todelliset arvot -entiteetistä ei voi poistaa tietueita.
author: JPBurrows
manager: kfend
ms.service: project-operations
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
ms.openlocfilehash: e3122c5d9495b3ff9a683f477e719ce0c228a84d
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5286064"
---
# <a name="why-cant-i-delete-records-from-the-actuals-entity"></a>Miksi en voi poistaa Todelliset arvot -entiteetin tietueita?

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Project Service Automation (PSA) ei salli todellisten arvojen poistamista, koska ne toimivat virallisena tietolähteenä tapahtumille, joilla on taloudellisia vaikutuksia jäljempänä sijaitseviin järjestelmiin, kuten pääkirjaan. Jos todellisia arvoja voisi poistaa, tilinpäätösraportoinnin eheys voitaisi kyseenalaistaa. Kirjausketjun luomista varten asiakkaiden pitäisi käyttää kirjauskansioita luodakseen kompensoivia tapahtumia.



[!INCLUDE[footer-include](../includes/footer-banner.md)]