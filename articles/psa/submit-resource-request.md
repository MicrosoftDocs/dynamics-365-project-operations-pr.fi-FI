---
title: Resurssipyynnön lähettäminen
description: Tässä aiheessa on tietoja projektiresurssinpyynnön lähettämisestä.
manager: kfend
ms.service: project-operations
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
ms.openlocfilehash: 50f076b89c5ac7fee4866534cbd47d81f92f3ab3
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/28/2020
ms.locfileid: "4131259"
---
# <a name="submitting-a-resource-request"></a><span data-ttu-id="a3942-103">Resurssipyynnön lähettäminen</span><span class="sxs-lookup"><span data-stu-id="a3942-103">Submitting a resource request</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="a3942-104">Voit lähettää luodun resurssivaatimuksen resurssipyyntönä.</span><span class="sxs-lookup"><span data-stu-id="a3942-104">You can submit a generated resource requirement as a resource request.</span></span> <span data-ttu-id="a3942-105">Pyyntö lähetetään sitten resurssipäällikölle toteutusta varten.</span><span class="sxs-lookup"><span data-stu-id="a3942-105">The request is then sent to a resource manager for fulfillment.</span></span>

1. <span data-ttu-id="a3942-106">Napauta Project Service Automation (PSA) **Projektit**-sivulla **Ryhmä**-välilehteä nähdäksesi varattavissa olevat resurssit.</span><span class="sxs-lookup"><span data-stu-id="a3942-106">In Project Service Automation (PSA), on the **Projects** page, click the **Team** tab to view a list bookable resources.</span></span> 
2. <span data-ttu-id="a3942-107">Valitse luettelosta yleinen resurssi, jolla on resurssitarve, ja valitse sitten **Lähetä pyyntö.**</span><span class="sxs-lookup"><span data-stu-id="a3942-107">Select the generic resource that has a resource requirement from the list and then click **Submit Request**.</span></span>

![Resurssipyynnön lähettäminen](media/RM-how-to-18.png)

<span data-ttu-id="a3942-109">Yleisen ryhmän jäsenen pyynnön tila muuttuu tilaksi **Lähetetty**.</span><span class="sxs-lookup"><span data-stu-id="a3942-109">The request status of the generic team member will change to **Submitted**.</span></span>

<span data-ttu-id="a3942-110">Kun resurssipäällikkö on täyttänyt pyynnön, yleinen resurssi korvataan nimetyllä resurssilla, jos resurssipäällikkö täyttää pyynnön nimetyn resurssin varauksella.</span><span class="sxs-lookup"><span data-stu-id="a3942-110">After the request is fulfilled by the resource manager, the generic resource will be replaced by a named resource if the resource manager fulfills the request with the booking of a named resource.</span></span> <span data-ttu-id="a3942-111">Muussa tapauksessa yleinen resurssi säilyy ryhmässä ja pyynnön tilaksi muuttuu **Vaatii tarkistusta**, jos resurssipäällikkö on ehdottanut nimettyä resurssia.</span><span class="sxs-lookup"><span data-stu-id="a3942-111">Otherwise, the generic resource will remain on the team and the request status will change to **Needs Review**, if the resource manager has proposed a named resource.</span></span>
