---
title: Resurssipyynnön lähettäminen
description: Tässä aiheessa on tietoja projektiresurssinpyynnön lähettämisestä.
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
ms.openlocfilehash: acdd228a9eb9d6c6c56f126ccca416613332a838
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/10/2021
ms.locfileid: "6013167"
---
# <a name="submitting-a-resource-request"></a><span data-ttu-id="1bc59-103">Resurssipyynnön lähettäminen</span><span class="sxs-lookup"><span data-stu-id="1bc59-103">Submitting a resource request</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="1bc59-104">Voit lähettää luodun resurssivaatimuksen resurssipyyntönä.</span><span class="sxs-lookup"><span data-stu-id="1bc59-104">You can submit a generated resource requirement as a resource request.</span></span> <span data-ttu-id="1bc59-105">Pyyntö lähetetään sitten resurssipäällikölle toteutusta varten.</span><span class="sxs-lookup"><span data-stu-id="1bc59-105">The request is then sent to a resource manager for fulfillment.</span></span>

1. <span data-ttu-id="1bc59-106">Napauta Project Service Automation (PSA) **Projektit**-sivulla **Ryhmä**-välilehteä nähdäksesi varattavissa olevat resurssit.</span><span class="sxs-lookup"><span data-stu-id="1bc59-106">In Project Service Automation (PSA), on the **Projects** page, click the **Team** tab to view a list bookable resources.</span></span> 
2. <span data-ttu-id="1bc59-107">Valitse luettelosta yleinen resurssi, jolla on resurssitarve, ja valitse sitten **Lähetä pyyntö.**</span><span class="sxs-lookup"><span data-stu-id="1bc59-107">Select the generic resource that has a resource requirement from the list and then click **Submit Request**.</span></span>

![Resurssipyynnön lähettäminen](media/RM-how-to-18.png)

<span data-ttu-id="1bc59-109">Yleisen ryhmän jäsenen pyynnön tila muuttuu tilaksi **Lähetetty**.</span><span class="sxs-lookup"><span data-stu-id="1bc59-109">The request status of the generic team member will change to **Submitted**.</span></span>

<span data-ttu-id="1bc59-110">Kun resurssipäällikkö on täyttänyt pyynnön, yleinen resurssi korvataan nimetyllä resurssilla, jos resurssipäällikkö täyttää pyynnön nimetyn resurssin varauksella.</span><span class="sxs-lookup"><span data-stu-id="1bc59-110">After the request is fulfilled by the resource manager, the generic resource will be replaced by a named resource if the resource manager fulfills the request with the booking of a named resource.</span></span> <span data-ttu-id="1bc59-111">Muussa tapauksessa yleinen resurssi säilyy ryhmässä ja pyynnön tilaksi muuttuu **Vaatii tarkistusta**, jos resurssipäällikkö on ehdottanut nimettyä resurssia.</span><span class="sxs-lookup"><span data-stu-id="1bc59-111">Otherwise, the generic resource will remain on the team and the request status will change to **Needs Review**, if the resource manager has proposed a named resource.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]