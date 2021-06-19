---
title: Resurssipyynnön lähettäminen
description: Voit lähettää luodun resurssivaatimuksen resurssipyyntönä. Pyyntö lähetetään sitten resurssipäällikölle toteutusta varten.
author: ruhercul
ms.date: 10/04/2020
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 6ac0044a27d1e506c9c62c477014017fd0ca06cb
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/10/2021
ms.locfileid: "6014022"
---
# <a name="submit-a-resource-request"></a><span data-ttu-id="2439c-104">Resurssipyynnön lähettäminen</span><span class="sxs-lookup"><span data-stu-id="2439c-104">Submit a resource request</span></span>

<span data-ttu-id="2439c-105">_**Koskee:** Project Operationsin resurssiin / muuhun kuin resurssiin perustuvia skenaarioita, Lite-käyttöönotto-kaupasta proformalaskutukseen_</span><span class="sxs-lookup"><span data-stu-id="2439c-105">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="2439c-106">Voit lähettää luodun resurssivaatimuksen resurssipyyntönä.</span><span class="sxs-lookup"><span data-stu-id="2439c-106">You can submit a generated resource requirement as a resource request.</span></span> <span data-ttu-id="2439c-107">Pyyntö lähetetään sitten resurssipäällikölle toteutusta varten.</span><span class="sxs-lookup"><span data-stu-id="2439c-107">The request is then sent to a resource manager for fulfillment.</span></span>

1. <span data-ttu-id="2439c-108">Valitse Dynamics 365 Project Operationsin **Projektit**-sivulla **Ryhmä**-välilehteä nähdäksesi varattavissa olevat resurssit.</span><span class="sxs-lookup"><span data-stu-id="2439c-108">In Dynamics 365 Project Operations, on the **Projects** page, select the **Team** tab to view a list of bookable resources.</span></span> 
2. <span data-ttu-id="2439c-109">Valitse luettelosta yleinen resurssi, jolla on resurssitarve, ja valitse sitten **Lähetä pyyntö**.</span><span class="sxs-lookup"><span data-stu-id="2439c-109">Select the generic resource that has a resource requirement from the list, and then click **Submit Request**.</span></span>

<span data-ttu-id="2439c-110">Yleisen ryhmän jäsenen pyynnön tila muuttuu tilaksi **Lähetetty**.</span><span class="sxs-lookup"><span data-stu-id="2439c-110">The request status of the generic team member will change to **Submitted**.</span></span>

<span data-ttu-id="2439c-111">Kun pyyntö on täytetty, yleinen resurssi korvataan nimetyllä resurssilla, jos resurssipäällikkö täyttää pyynnön nimetyn resurssin varauksella.</span><span class="sxs-lookup"><span data-stu-id="2439c-111">After the request is fulfilled, the generic resource is replaced by a named resource if the resource manager fulfills the request by booking a named resource.</span></span> <span data-ttu-id="2439c-112">Muussa tapauksessa yleinen resurssi säilyy ryhmässä ja pyynnön tilaksi muuttuu **Vaatii tarkistusta**, jos resurssipäällikkö on ehdottanut nimettyä resurssia.</span><span class="sxs-lookup"><span data-stu-id="2439c-112">Otherwise, if the resource manager proposes a named resource, the generic resource remains on the team and the request status will change to **Needs Review**.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]