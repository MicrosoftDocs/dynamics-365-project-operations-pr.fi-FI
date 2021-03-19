---
title: Resurssipyynnön lähettäminen
description: Voit lähettää luodun resurssivaatimuksen resurssipyyntönä. Pyyntö lähetetään sitten resurssipäällikölle toteutusta varten.
author: ruhercul
manager: Annbe
ms.date: 10/04/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: bc97af1ec90e60417c502eb329a85004e769e05b
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5279134"
---
# <a name="submit-a-resource-request"></a><span data-ttu-id="ec550-104">Resurssipyynnön lähettäminen</span><span class="sxs-lookup"><span data-stu-id="ec550-104">Submit a resource request</span></span>

<span data-ttu-id="ec550-105">_**Koskee:** Project Operationsin resurssiin / muuhun kuin resurssiin perustuvia skenaarioita, Lite-käyttöönotto-kaupasta proformalaskutukseen_</span><span class="sxs-lookup"><span data-stu-id="ec550-105">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="ec550-106">Voit lähettää luodun resurssivaatimuksen resurssipyyntönä.</span><span class="sxs-lookup"><span data-stu-id="ec550-106">You can submit a generated resource requirement as a resource request.</span></span> <span data-ttu-id="ec550-107">Pyyntö lähetetään sitten resurssipäällikölle toteutusta varten.</span><span class="sxs-lookup"><span data-stu-id="ec550-107">The request is then sent to a resource manager for fulfillment.</span></span>

1. <span data-ttu-id="ec550-108">Valitse Dynamics 365 Project Operationsin **Projektit**-sivulla **Ryhmä**-välilehteä nähdäksesi varattavissa olevat resurssit.</span><span class="sxs-lookup"><span data-stu-id="ec550-108">In Dynamics 365 Project Operations, on the **Projects** page, select the **Team** tab to view a list of bookable resources.</span></span> 
2. <span data-ttu-id="ec550-109">Valitse luettelosta yleinen resurssi, jolla on resurssitarve, ja valitse sitten **Lähetä pyyntö**.</span><span class="sxs-lookup"><span data-stu-id="ec550-109">Select the generic resource that has a resource requirement from the list, and then click **Submit Request**.</span></span>

<span data-ttu-id="ec550-110">Yleisen ryhmän jäsenen pyynnön tila muuttuu tilaksi **Lähetetty**.</span><span class="sxs-lookup"><span data-stu-id="ec550-110">The request status of the generic team member will change to **Submitted**.</span></span>

<span data-ttu-id="ec550-111">Kun pyyntö on täytetty, yleinen resurssi korvataan nimetyllä resurssilla, jos resurssipäällikkö täyttää pyynnön nimetyn resurssin varauksella.</span><span class="sxs-lookup"><span data-stu-id="ec550-111">After the request is fulfilled, the generic resource is replaced by a named resource if the resource manager fulfills the request by booking a named resource.</span></span> <span data-ttu-id="ec550-112">Muussa tapauksessa yleinen resurssi säilyy ryhmässä ja pyynnön tilaksi muuttuu **Vaatii tarkistusta**, jos resurssipäällikkö on ehdottanut nimettyä resurssia.</span><span class="sxs-lookup"><span data-stu-id="ec550-112">Otherwise, if the resource manager proposes a named resource, the generic resource remains on the team and the request status will change to **Needs Review**.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]