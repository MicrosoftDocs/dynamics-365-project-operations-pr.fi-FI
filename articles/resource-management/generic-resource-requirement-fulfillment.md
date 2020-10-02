---
title: Yleisten resurssitarpeiden täyttäminen
description: Tässä aiheessa on tietoja nimettyjen resurssien varaamisesta yleistä resurssitarvetta varten.
author: ruhercul
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: ruhercul
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 76dd47fa2451b5cb61298ff332d77bae646a288a
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/28/2020
ms.locfileid: "3897582"
---
# <a name="generic-resource-requirement-fulfillment"></a><span data-ttu-id="f860c-103">Yleisten resurssitarpeiden täyttäminen</span><span class="sxs-lookup"><span data-stu-id="f860c-103">Generic resource requirement fulfillment</span></span>

<span data-ttu-id="f860c-104">_**Koskee:** Project Operationsin resurssiin / muuhun kuin resurssiin perustuvia skenaarioita, Lite-käyttöönotto-kaupasta proformalaskutukseen_</span><span class="sxs-lookup"><span data-stu-id="f860c-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="f860c-105">Voit varata nimetyn resurssin korvaamaan yleisen resurssin, jolla on resurssitarve.</span><span class="sxs-lookup"><span data-stu-id="f860c-105">You can book a named resource to replace generic resource that has a resource requirement.</span></span>

1. <span data-ttu-id="f860c-106">Valitse **Projektit**-sivulla **Ryhmä**-välilehti.</span><span class="sxs-lookup"><span data-stu-id="f860c-106">On the **Projects** page, select the **Team** tab.</span></span>
2. <span data-ttu-id="f860c-107">Valitse luettelosta yleinen resurssi, jolla on resurssitarve, ja valitse sitten **Varaa**.</span><span class="sxs-lookup"><span data-stu-id="f860c-107">Select the generic resource that has a resource requirement from the list, and then select **Book**.</span></span> <span data-ttu-id="f860c-108">Voit myös avata resurssitarpeen ja valita **Varaa**-kohdan.</span><span class="sxs-lookup"><span data-stu-id="f860c-108">Or, open the resource requirement and then select **Book**.</span></span>
3. <span data-ttu-id="f860c-109">Valitse **Ajoitusavustaja**-sivulla projektiryhmääsi varattava nimetty resurssi ja valitse **Varaa**.</span><span class="sxs-lookup"><span data-stu-id="f860c-109">On the **Schedule Assistant** page, select a named resource to book onto your project team and then select **Book**.</span></span>

<span data-ttu-id="f860c-110">Kun varaus on valmis ja nimetty resurssi on täyttänyt sen, yleinen resurssi korvataan nimetyllä resurssilla.</span><span class="sxs-lookup"><span data-stu-id="f860c-110">When the booking is complete and fulfilled by a named resource, the generic resource is replaced with the named resource.</span></span>

<span data-ttu-id="f860c-111">Myös aikataulun kohdennukset päivitetään nimetyllä resurssilla.</span><span class="sxs-lookup"><span data-stu-id="f860c-111">The assignments on the schedule are updated with the named resource as well.</span></span>

## <a name="fulfill-a-generic-resource-with-multiple-named-resources"></a><span data-ttu-id="f860c-112">Yleisen resurssin täyttäminen useilla nimetyillä resursseilla</span><span class="sxs-lookup"><span data-stu-id="f860c-112">Fulfill a generic resource with multiple named resources</span></span>
<span data-ttu-id="f860c-113">Yleisen resurssin tarpeen täyttäminen useilla nimetyillä resursseilla vastaa yksittäisen nimetyn resurssin kohdentamista.</span><span class="sxs-lookup"><span data-stu-id="f860c-113">Fulfilling a requirement for a generic resource with multiple named resources is similar to assigning a single named resource.</span></span> <span data-ttu-id="f860c-114">Otetaan esimerkiksi viisi päivää ja 120 tuntia työtä vaativa tehtävä.</span><span class="sxs-lookup"><span data-stu-id="f860c-114">For example, there is a task with a duration of five days and 120 hours of effort.</span></span> <span data-ttu-id="f860c-115">Yksittäinen yleensä kahdeksantuntista työpäivää viiden päivän työviikoilla tekevä resurssi ei voi suorittaa tätä tehtävää.</span><span class="sxs-lookup"><span data-stu-id="f860c-115">This task can't be completed by one resource that works a typical eight-hour day over a five-day week.</span></span> 

<span data-ttu-id="f860c-116">Tarpeena on 120 tuntia robotiikkasuunnittelua viiden päivän aikana eli 24 tuntia päivässä.</span><span class="sxs-lookup"><span data-stu-id="f860c-116">The requirement is for 120 hours of robotics engineering over five days, which is 24 hours per day.</span></span>

<span data-ttu-id="f860c-117">Tämä on esimerkki siitä, että useita nimettyjä resursseja tarvitaan täyttämään yleinen resurssipyyntö.</span><span class="sxs-lookup"><span data-stu-id="f860c-117">This is an example of when multiple named resources are needed to fulfill a generic resource request.</span></span> <span data-ttu-id="f860c-118">Sinun on varattava useita resursseja täyttämään tarve.</span><span class="sxs-lookup"><span data-stu-id="f860c-118">You will need to book multiple resources to fulfill the requirement.</span></span>

<span data-ttu-id="f860c-119">Suurin ero tässä skenaariossa on, että yleinen resurssi pysyy ryhmässä tehtävälle kohdistettuna ja että varattuja nimettyjä ryhmän jäseniä ei kohdenneta osana asemaa.</span><span class="sxs-lookup"><span data-stu-id="f860c-119">The main difference in this scenario is that the generic resource remains on the team assigned to the task, and the booked named resource team members are not assigned as part of the position.</span></span> <span data-ttu-id="f860c-120">Projektipäällikkö voi kohdentaa työn nimetyille resursseille harkintansa mukaan.</span><span class="sxs-lookup"><span data-stu-id="f860c-120">The project manager can assign the work as appropriate to the named resources.</span></span> <span data-ttu-id="f860c-121">**Täsmäytys**-näkymä voi auttaa projektipäällikköä jakamaan varaukset tehtäväkohdennuksiksi useille resursseille.</span><span class="sxs-lookup"><span data-stu-id="f860c-121">The **Reconciliation** view can assist a project manager in breaking up the bookings across multiple resources to task assignments.</span></span> <span data-ttu-id="f860c-122">Tämä ei tapahdu automaattisesti, koska yllä esitettyä monimutkaisemmissa skenaarioissa, kuten siinä tapauksessa, jossa on joukko tehtäviä, jotka muodostavat tarpeen, järjestelmän on otettava huomioon, miten projektipäällikkö haluaa toteuttaa kohdennukset.</span><span class="sxs-lookup"><span data-stu-id="f860c-122">This is not done automatically because in any scenario more complicated than the simple example above, such as where you have a bundle of tasks making up the requirement or the intent of how the project manager wants to assign, needs to be assumed by the system.</span></span> <span data-ttu-id="f860c-123">Koska järjestelmä ei ymmärrä tarkoitusta, oletukset ovat todennäköisesti erilaisia kuin tarkoitus, ja tuloksena syntyy virheellinen tai arvaamaton tulos.</span><span class="sxs-lookup"><span data-stu-id="f860c-123">Because the system can't understand intent, it's likely that the assumptions will be different than intended and an incorrect or unpredictable result will occur.</span></span> <span data-ttu-id="f860c-124">Ennustettava tulos on se, että yleinen resurssi säilyy määritettynä, kunnes projektipäällikkö luo tietoisesti kohdennuksia **Täsmäytys**-näkymän avulla.</span><span class="sxs-lookup"><span data-stu-id="f860c-124">The predictable outcome is that the generic resource remains assigned until the project manager deliberately creates assignments, with the assistance of the **Reconciliation** view.</span></span>


