---
title: Nimettyjen resurssien varaaminen resurssitarpeista.
description: Tässä aiheessa on tietoja nimettyjen resurssien varaamisesta yleistä resurssitarvetta varten.
author: JohnPBurrows
manager: kfend
ms.service: project-operations
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
ms.openlocfilehash: d7ff58ec08661adc702867c6c26805a74a3637c9
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/28/2020
ms.locfileid: "4125894"
---
# <a name="book-named-resources-from-resource-requirements"></a><span data-ttu-id="15dac-103">Nimettyjen resurssien varaaminen resurssitarpeista.</span><span class="sxs-lookup"><span data-stu-id="15dac-103">Book named resources from resource requirements</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="15dac-104">Voit varata nimetyn resurssin korvaamaan yleisen resurssin, jolla on resurssitarve.</span><span class="sxs-lookup"><span data-stu-id="15dac-104">You can book a named resource to replace generic resource that has a resource requirement.</span></span>

1. <span data-ttu-id="15dac-105">Napsauta Project Service Automationin (PSA:n) **Projektit** -sivulla **Ryhmä** -välilehteä.</span><span class="sxs-lookup"><span data-stu-id="15dac-105">In Project Service Automation (PSA), on the **Projects** page, click the **Team** tab.</span></span>
2. <span data-ttu-id="15dac-106">Valitse luettelosta yleinen resurssi, jolla on resurssitarve, ja valitse sitten **Varaa**.</span><span class="sxs-lookup"><span data-stu-id="15dac-106">Select the generic resource that has a resource requirement from the list and then click **Book**.</span></span> <span data-ttu-id="15dac-107">Voit myös avata resurssitarpeen ja napsauttaa **Varaa**.</span><span class="sxs-lookup"><span data-stu-id="15dac-107">Or, open the resource requirement and then click **Book**.</span></span>


![Yleisen ryhmän jäsenen varaus](media/RM-how-to-14.png)


3. <span data-ttu-id="15dac-109">Valitse **Ajoitusavustaja**-sivulla projektiryhmääsi varattava nimetty resurssi ja napsauta **Varaa**.</span><span class="sxs-lookup"><span data-stu-id="15dac-109">On the **Schedule Assistant** page, select a named resource to book onto your project team and then click **Book**.</span></span>

![Yleisen ryhmän jäsenen varaaminen ajoitusavustajalla](media/RM-how-to-15.png)

<span data-ttu-id="15dac-111">Kun varaus on valmis ja nimetty resurssi on täyttänyt sen, yleinen resurssi korvataan nimetyllä resurssilla.</span><span class="sxs-lookup"><span data-stu-id="15dac-111">When the booking is complete and fulfilled by a named resource, the generic resource is replaced with the named resource.</span></span>

![Nimetty ryhmän jäsen korvaa yleisen ryhmän jäsenen](media/RM-how-to-16.png)

<span data-ttu-id="15dac-113">Myös aikataulun kohdennukset päivitetään nimetyllä resurssilla.</span><span class="sxs-lookup"><span data-stu-id="15dac-113">The assignments on the schedule are updated with the named resource as well.</span></span>

![Nimetty ryhmän jäsen kohdennettuna projektitehtäville](media/RM-how-to-17.png)

## <a name="fulfill-a-generic-resource-with-multiple-named-resources"></a><span data-ttu-id="15dac-115">Yleisen resurssin täyttäminen useilla nimetyillä resursseilla</span><span class="sxs-lookup"><span data-stu-id="15dac-115">Fulfill a generic resource with multiple named resources</span></span>
<span data-ttu-id="15dac-116">Yleisen resurssin tarpeen täyttäminen useilla nimetyillä resursseilla vastaa yksittäisen nimetyn resurssin kohdentamista.</span><span class="sxs-lookup"><span data-stu-id="15dac-116">Fulfilling a requirement for a generic resource with multiple named resources is similar to assigning a single named resource.</span></span> <span data-ttu-id="15dac-117">Otetaan esimerkiksi viisi päivää ja 120 tuntia työtä vaativa tehtävä.</span><span class="sxs-lookup"><span data-stu-id="15dac-117">For example, there is a task with a duration of five days and 120 hours of effort.</span></span> <span data-ttu-id="15dac-118">Yksittäinen yleensä kahdeksantuntista työpäivää viiden päivän työviikoilla tekevä resurssi ei voi suorittaa tätä tehtävää.</span><span class="sxs-lookup"><span data-stu-id="15dac-118">This task can't be completed by one resource that works a typical eight-hour day over a five day week.</span></span> 

![Tehtävä vaatii 120 työtuntia viiden päivän aikana](media/RM-how-to-21.png)

<span data-ttu-id="15dac-120">Tarpeena on 120 tuntia robotiikkasuunnittelua viiden päivän aikana eli 24 tuntia päivässä.</span><span class="sxs-lookup"><span data-stu-id="15dac-120">The requirement is for 120 hours of robotics engineering over five days, which is 24 hours per day.</span></span>

![Päiväkohtainen tarve](media/RM-how-to-22.png)

<span data-ttu-id="15dac-122">Tämä on esimerkki siitä, että useita nimettyjä resursseja tarvitaan täyttämään yleinen resurssipyyntö.</span><span class="sxs-lookup"><span data-stu-id="15dac-122">This is an example of when multiple named resources are needed to fulfill a generic resource request.</span></span> <span data-ttu-id="15dac-123">Sinun on varattava useita resursseja täyttämään tarve.</span><span class="sxs-lookup"><span data-stu-id="15dac-123">You will need to book multiple resources to fulfill the requirement.</span></span>

![Useiden resurssien varaaminen täyttämään tarve](media/RM-how-to-23.png)

<span data-ttu-id="15dac-125">Suurin ero tässä skenaariossa on, että yleinen resurssi pysyy ryhmässä tehtävälle kohdistettuna ja että varattuja nimettyjä ryhmän jäseniä ei kohdenneta osana asemaa.</span><span class="sxs-lookup"><span data-stu-id="15dac-125">The main difference in this scenario is that the generic resource remains on the team assigned to the task, and the booked named resource team members are not assigned as part of the position.</span></span> <span data-ttu-id="15dac-126">Projektipäällikkö voi kohdentaa työn nimetyille resursseille harkintansa mukaan.</span><span class="sxs-lookup"><span data-stu-id="15dac-126">The project manager can assign the work as appropriate to the named resources.</span></span> <span data-ttu-id="15dac-127">**Täsmäytys**-näkymä voi auttaa projektipäällikköä jakamaan varaukset tehtäväkohdennuksiksi useille resursseille.</span><span class="sxs-lookup"><span data-stu-id="15dac-127">The **Reconciliation** view can assist a project manager in breaking up the bookings across multiple resources to task assignments.</span></span> <span data-ttu-id="15dac-128">Tämä ei tapahdu automaattisesti, koska yllä esitettyä monimutkaisemmissa skenaarioissa, kuten siinä tapauksessa, jossa on joukko tehtäviä, jotka muodostavat tarpeen, järjestelmän on otettava huomioon, miten projektipäällikkö haluaa toteuttaa kohdennukset.</span><span class="sxs-lookup"><span data-stu-id="15dac-128">This is not done automatically because in any scenario more complicated than the simple example above, such as where you have a bundle of tasks making up the requirement, the intent of how the project manager wants to assign, needs to be assumed by the system.</span></span> <span data-ttu-id="15dac-129">Koska järjestelmä ei ymmärrä tarkoitusta, oletukset eroavat todennäköisesti tarkoituksesta, ja tuloksena on virheellinen tai arvaamaton tulos.</span><span class="sxs-lookup"><span data-stu-id="15dac-129">Because the system can't understand intent, chances are that the assumptions will be different than intended and an incorrect or unpredictable result will happen.</span></span> <span data-ttu-id="15dac-130">Ennustettava tulos on se, että yleinen resurssi säilyy määritettynä, kunnes projektipäällikkö luo tietoisesti kohdennuksia **Täsmäytys**-näkymän avulla.</span><span class="sxs-lookup"><span data-stu-id="15dac-130">The predictable outcome is that the generic resource remains assigned until the project manager deliberately creates assignments, with the assistance of the **Reconciliation** view.</span></span>


