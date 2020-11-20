---
title: Yleisten resurssitarpeiden täyttäminen
description: Tässä aiheessa on tietoja siitä, miten nimettyjä resursseja varataan yleistä resurssitarvetta varten.
author: ruhercul
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 3c4d02fd589d4a5d39380688852377f57fceb05b
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/28/2020
ms.locfileid: "4130303"
---
# <a name="generic-resource-requirement-fulfillment"></a><span data-ttu-id="bc2e8-103">Yleisten resurssitarpeiden täyttäminen</span><span class="sxs-lookup"><span data-stu-id="bc2e8-103">Generic resource requirement fulfillment</span></span>

<span data-ttu-id="bc2e8-104">_**Koskee:** Project Operationsin resurssiin / muuhun kuin resurssiin perustuvia skenaarioita, Lite-käyttöönotto-kaupasta proformalaskutukseen_</span><span class="sxs-lookup"><span data-stu-id="bc2e8-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="bc2e8-105">Voit varata nimetyn resurssin korvaamaan yleisen resurssin, jolla on resurssitarve.</span><span class="sxs-lookup"><span data-stu-id="bc2e8-105">You can book a named resource to replace generic resource that has a resource requirement.</span></span>

1. <span data-ttu-id="bc2e8-106">Valitse **Projektit**-sivulla **Ryhmä**-välilehti.</span><span class="sxs-lookup"><span data-stu-id="bc2e8-106">On the **Projects** page, select the **Team** tab.</span></span>
2. <span data-ttu-id="bc2e8-107">Valitse luettelosta yleinen resurssi, jolla on resurssitarve, ja valitse sitten **Varaa**.</span><span class="sxs-lookup"><span data-stu-id="bc2e8-107">Select the generic resource that has a resource requirement from the list, and then select **Book**.</span></span> <span data-ttu-id="bc2e8-108">Voit myös avata resurssitarpeen ja valita **Varaa**-kohdan.</span><span class="sxs-lookup"><span data-stu-id="bc2e8-108">Or, open the resource requirement and then select **Book**.</span></span>
3. <span data-ttu-id="bc2e8-109">Valitse **Ajoitusavustaja**-sivulla projektiryhmääsi varattava nimetty resurssi ja valitse **Varaa**.</span><span class="sxs-lookup"><span data-stu-id="bc2e8-109">On the **Schedule Assistant** page, select a named resource to book onto your project team and then select **Book**.</span></span>

<span data-ttu-id="bc2e8-110">Kun varaus on valmis ja nimetty resurssi on täyttänyt sen, yleinen resurssi korvataan nimetyllä resurssilla.</span><span class="sxs-lookup"><span data-stu-id="bc2e8-110">When the booking is complete and fulfilled by a named resource, the generic resource is replaced with the named resource.</span></span>

<span data-ttu-id="bc2e8-111">Myös aikataulun kohdennukset päivitetään nimetyllä resurssilla.</span><span class="sxs-lookup"><span data-stu-id="bc2e8-111">The assignments on the schedule are updated with the named resource as well.</span></span>

## <a name="fulfill-a-generic-resource-with-multiple-named-resources"></a><span data-ttu-id="bc2e8-112">Yleisen resurssin täyttäminen useilla nimetyillä resursseilla</span><span class="sxs-lookup"><span data-stu-id="bc2e8-112">Fulfill a generic resource with multiple named resources</span></span>
<span data-ttu-id="bc2e8-113">Yleisen resurssin tarpeen täyttäminen useilla nimetyillä resursseilla vastaa yksittäisen nimetyn resurssin kohdentamista.</span><span class="sxs-lookup"><span data-stu-id="bc2e8-113">Fulfilling a requirement for a generic resource with multiple named resources is similar to assigning a single named resource.</span></span> <span data-ttu-id="bc2e8-114">Otetaan esimerkiksi viisi päivää ja 120 tuntia työtä vaativa tehtävä.</span><span class="sxs-lookup"><span data-stu-id="bc2e8-114">For example, there is a task with a duration of five days and 120 hours of effort.</span></span> <span data-ttu-id="bc2e8-115">Yksittäinen yleensä kahdeksantuntista työpäivää viiden päivän työviikoilla tekevä resurssi ei voi suorittaa tätä tehtävää.</span><span class="sxs-lookup"><span data-stu-id="bc2e8-115">This task can't be completed by one resource that works a typical eight-hour day over a five-day week.</span></span> 

<span data-ttu-id="bc2e8-116">Tarpeena on 120 tuntia robotiikkasuunnittelua viiden päivän aikana eli 24 tuntia päivässä.</span><span class="sxs-lookup"><span data-stu-id="bc2e8-116">The requirement is for 120 hours of robotics engineering over five days, which is 24 hours per day.</span></span>

<span data-ttu-id="bc2e8-117">Tämä on esimerkki siitä, että useita nimettyjä resursseja tarvitaan täyttämään yleinen resurssipyyntö.</span><span class="sxs-lookup"><span data-stu-id="bc2e8-117">This is an example of when multiple named resources are needed to fulfill a generic resource request.</span></span> <span data-ttu-id="bc2e8-118">Sinun on varattava useita resursseja täyttämään tarve.</span><span class="sxs-lookup"><span data-stu-id="bc2e8-118">You will need to book multiple resources to fulfill the requirement.</span></span>

<span data-ttu-id="bc2e8-119">Suurin ero tässä skenaariossa on, että yleinen resurssi pysyy ryhmässä tehtävälle kohdistettuna ja että varattuja nimettyjä ryhmän jäseniä ei kohdenneta osana asemaa.</span><span class="sxs-lookup"><span data-stu-id="bc2e8-119">The main difference in this scenario is that the generic resource remains on the team assigned to the task, and the booked named resource team members are not assigned as part of the position.</span></span> <span data-ttu-id="bc2e8-120">Projektipäällikkö voi kohdentaa työn nimetyille resursseille harkintansa mukaan.</span><span class="sxs-lookup"><span data-stu-id="bc2e8-120">The project manager can assign the work as appropriate to the named resources.</span></span> <span data-ttu-id="bc2e8-121">**Täsmäytys**-näkymä voi auttaa projektipäällikköä jakamaan varaukset tehtäväkohdennuksiksi useille resursseille.</span><span class="sxs-lookup"><span data-stu-id="bc2e8-121">The **Reconciliation** view can assist a project manager in breaking up the bookings across multiple resources to task assignments.</span></span> <span data-ttu-id="bc2e8-122">Tämä ei tapahdu automaattisesti, koska yllä esitettyä monimutkaisemmissa skenaarioissa, kuten siinä tapauksessa, jossa on joukko tehtäviä, jotka muodostavat tarpeen, järjestelmän on otettava huomioon, miten projektipäällikkö haluaa toteuttaa kohdennukset.</span><span class="sxs-lookup"><span data-stu-id="bc2e8-122">This is not done automatically because in any scenario more complicated than the simple example above, such as where you have a bundle of tasks making up the requirement or the intent of how the project manager wants to assign, needs to be assumed by the system.</span></span> <span data-ttu-id="bc2e8-123">Koska järjestelmä ei ymmärrä tarkoitusta, oletukset ovat todennäköisesti erilaisia kuin tarkoitus, ja tuloksena syntyy virheellinen tai arvaamaton tulos.</span><span class="sxs-lookup"><span data-stu-id="bc2e8-123">Because the system can't understand intent, it's likely that the assumptions will be different than intended and an incorrect or unpredictable result will occur.</span></span> <span data-ttu-id="bc2e8-124">Ennustettava tulos on se, että yleinen resurssi säilyy määritettynä, kunnes projektipäällikkö luo tietoisesti kohdennuksia **Täsmäytys**-näkymän avulla.</span><span class="sxs-lookup"><span data-stu-id="bc2e8-124">The predictable outcome is that the generic resource remains assigned until the project manager deliberately creates assignments, with the assistance of the **Reconciliation** view.</span></span>


