---
title: Miksi en voi poistaa Todelliset arvot -entiteetin tietueita?
description: Tässä aiheessa on tietoja siitä, miksi Todelliset arvot -entiteetistä ei voi poistaa tietueita.
author: JPBurrows
manager: kfend
ms.service: business-applications
ms.custom:
- dyn365-projectservice
ms.date: 11/6/2018
ms.topic: article
ms.prod: Project Service
ms.technology: Applies to all versions of Project Service
ms.assetid: ff504c34-7337-474f-89e8-d8afdd1e0a98
ms.author: Jburrows
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 5817940933c161dccac0fe549fabacbe57e7077a
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/24/2020
ms.locfileid: "3751128"
---
# <a name="why-cant-i-delete-records-from-the-actuals-entity"></a><span data-ttu-id="8e7f0-103">Miksi en voi poistaa Todelliset arvot -entiteetin tietueita?</span><span class="sxs-lookup"><span data-stu-id="8e7f0-103">Why can’t I delete records from the Actuals entity?</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="8e7f0-104">Project Service Automation (PSA) ei salli todellisten arvojen poistamista, koska ne toimivat virallisena tietolähteenä tapahtumille, joilla on taloudellisia vaikutuksia jäljempänä sijaitseviin järjestelmiin, kuten pääkirjaan.</span><span class="sxs-lookup"><span data-stu-id="8e7f0-104">Project Service Automation (PSA) doesn't allow you to delete actuals because they serve as the source of truth for transactions that have financial implications to downstream systems, such as the general ledger.</span></span> <span data-ttu-id="8e7f0-105">Jos todellisia arvoja voisi poistaa, tilinpäätösraportoinnin eheys voitaisi kyseenalaistaa.</span><span class="sxs-lookup"><span data-stu-id="8e7f0-105">If actuals could be deleted, the integrity of the financial reporting transactions could be questioned.</span></span> <span data-ttu-id="8e7f0-106">Kirjausketjun luomista varten asiakkaiden pitäisi käyttää kirjauskansioita luodakseen kompensoivia tapahtumia.</span><span class="sxs-lookup"><span data-stu-id="8e7f0-106">To establish an audit trail, customers should use journals to create compensating transactions.</span></span>

