---
title: Resurssipyynnön lähettäminen
description: Voit lähettää luodun resurssivaatimuksen resurssipyyntönä. Pyyntö lähetetään sitten resurssipäällikölle toteutusta varten.
author: ruhercul
manager: Annbe
ms.date: 10/04/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 94cf0f0d88e9be2522936b45122ed0037434d4f3
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/16/2020
ms.locfileid: "4075242"
---
# <a name="submit-a-resource-request"></a><span data-ttu-id="a1db5-104">Resurssipyynnön lähettäminen</span><span class="sxs-lookup"><span data-stu-id="a1db5-104">Submit a resource request</span></span>

<span data-ttu-id="a1db5-105">_**Koskee:** Project Operationsin resurssiin / muuhun kuin resurssiin perustuvia skenaarioita, Lite-käyttöönotto-kaupasta proformalaskutukseen_</span><span class="sxs-lookup"><span data-stu-id="a1db5-105">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="a1db5-106">Voit lähettää luodun resurssivaatimuksen resurssipyyntönä.</span><span class="sxs-lookup"><span data-stu-id="a1db5-106">You can submit a generated resource requirement as a resource request.</span></span> <span data-ttu-id="a1db5-107">Pyyntö lähetetään sitten resurssipäällikölle toteutusta varten.</span><span class="sxs-lookup"><span data-stu-id="a1db5-107">The request is then sent to a resource manager for fulfillment.</span></span>

1. <span data-ttu-id="a1db5-108">Valitse Dynamics 365 Project Operationsissa **Projektit** -sivulla **Ryhmä** -välilehteä nähdäksesi varattavissa olevat resurssit.</span><span class="sxs-lookup"><span data-stu-id="a1db5-108">In Dynamics 365 Project Operations, on the **Projects** page, select the **Team** tab to view a list of bookable resources.</span></span> 
2. <span data-ttu-id="a1db5-109">Valitse luettelosta yleinen resurssi, jolla on resurssitarve, ja valitse sitten **Lähetä pyyntö**.</span><span class="sxs-lookup"><span data-stu-id="a1db5-109">Select the generic resource that has a resource requirement from the list, and then click **Submit Request**.</span></span>

<span data-ttu-id="a1db5-110">Yleisen ryhmän jäsenen pyynnön tila muuttuu tilaksi **Lähetetty**.</span><span class="sxs-lookup"><span data-stu-id="a1db5-110">The request status of the generic team member will change to **Submitted**.</span></span>

<span data-ttu-id="a1db5-111">Kun pyyntö on täytetty, yleinen resurssi korvataan nimetyllä resurssilla, jos resurssipäällikkö täyttää pyynnön nimetyn resurssin varauksella.</span><span class="sxs-lookup"><span data-stu-id="a1db5-111">After the request is fulfilled, the generic resource is replaced by a named resource if the resource manager fulfills the request by booking a named resource.</span></span> <span data-ttu-id="a1db5-112">Muussa tapauksessa yleinen resurssi säilyy ryhmässä ja pyynnön tilaksi muuttuu **Vaatii tarkistusta** , jos resurssipäällikkö on ehdottanut nimettyä resurssia.</span><span class="sxs-lookup"><span data-stu-id="a1db5-112">Otherwise, if the resource manager proposes a named resource, the generic resource remains on the team and the request status will change to **Needs Review**.</span></span>
