---
title: Ajoitusavustajan yleiskatsaus
description: Tässä aiheessa on tietoja resurssien varaamisesta ajoitusavustajan avulla.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: da551e805f395e466952df1dbb7d193bdddba358
ms.sourcegitcommit: 56c42d7f5995a674426a1c2a81bae897dceb391c
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/01/2020
ms.locfileid: "3908068"
---
# <a name="schedule-assistant-overview"></a><span data-ttu-id="b656e-103">Ajoitusavustajan yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="b656e-103">Schedule assistant overview</span></span>

<span data-ttu-id="b656e-104">_**Koskee:** Project Operationsin resurssiin / muuhun kuin resurssiin perustuvia skenaarioita, Lite-käyttöönotto-kaupasta proformalaskutukseen_</span><span class="sxs-lookup"><span data-stu-id="b656e-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="b656e-105">Ajoitusavustajan avulla voit varata resursseja projektipäällikön määrittämien vaatimusten perusteella.</span><span class="sxs-lookup"><span data-stu-id="b656e-105">The Schedule assistant is used to book resources based on requirements defined by the Project manager.</span></span> <span data-ttu-id="b656e-106">Ajoitusavustaja käyttää resurssitarpeen parametreja löytääkseen resurssin.</span><span class="sxs-lookup"><span data-stu-id="b656e-106">The schedule assistant relies on the parameters provided in the resource requirement to find the resource.</span></span> <span data-ttu-id="b656e-107">Ajoitusavustaja suosittelee resursseja, jotka vastaavat asiaankuuluvia vaatimuksia, kuten aikaikkunoita tai tarvittavia taitoja.</span><span class="sxs-lookup"><span data-stu-id="b656e-107">The Schedule assistant recommends resources that match relevant requirements, like time windows or skills needed.</span></span>

<span data-ttu-id="b656e-108">Kun tarvittavat resurssit on tunnistettu, resurssi- tai projektipäällikkö voi varata resurssin työhön.</span><span class="sxs-lookup"><span data-stu-id="b656e-108">After suitable resources are identified, the Resource or Project manager can book the resource to the work.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="b656e-109">Edellytykset</span><span class="sxs-lookup"><span data-stu-id="b656e-109">Prerequisites</span></span>

<span data-ttu-id="b656e-110">Ajoitusavustaja on osa Universal Resource Scheduling -ratkaisua.</span><span class="sxs-lookup"><span data-stu-id="b656e-110">The Schedule assistant is a part of the Universal Resource Scheduling solution.</span></span> <span data-ttu-id="b656e-111">Tämä ratkaisu sisältyy ja asennetaan Dynamics 365 Project Operationsin, Dynamics 365 Field Servicee ja Dynamics 365 Customer Servicen kanssa.</span><span class="sxs-lookup"><span data-stu-id="b656e-111">This solution is included and installed with Dynamics 365 Project Operations, Dynamics 365 Field Service, and Dynamics 365 Customer Service.</span></span>

## <a name="matching-requirements-and-resources"></a><span data-ttu-id="b656e-112">Vastaavat tarpeet ja resurssit</span><span class="sxs-lookup"><span data-stu-id="b656e-112">Matching requirements and resources</span></span>

<span data-ttu-id="b656e-113">Luotu resurssitarve perustuu esimerkiksi seuraaviin tietoihin:</span><span class="sxs-lookup"><span data-stu-id="b656e-113">A generated resource requirement is based on details such as:</span></span>

-   <span data-ttu-id="b656e-114">Ominaisuudet</span><span class="sxs-lookup"><span data-stu-id="b656e-114">Characteristics</span></span>
-   <span data-ttu-id="b656e-115">Roolit</span><span class="sxs-lookup"><span data-stu-id="b656e-115">Roles</span></span>
-   <span data-ttu-id="b656e-116">Liiketoimintayksiköt</span><span class="sxs-lookup"><span data-stu-id="b656e-116">Business units</span></span>
-   <span data-ttu-id="b656e-117">Resurssin asetukset</span><span class="sxs-lookup"><span data-stu-id="b656e-117">Resource preferences</span></span>
-   <span data-ttu-id="b656e-118">Työmäärän aikaväli</span><span class="sxs-lookup"><span data-stu-id="b656e-118">Effort contours</span></span>
-   <span data-ttu-id="b656e-119">Aikavyöhyke</span><span class="sxs-lookup"><span data-stu-id="b656e-119">Time zone</span></span>

<span data-ttu-id="b656e-120">Ajoitusavustaja käyttää näitä tietoja resurssien suodattamiseen.</span><span class="sxs-lookup"><span data-stu-id="b656e-120">The Schedule assistant uses these details to filter resources.</span></span>

## <a name="launch-the-schedule-assistant"></a><span data-ttu-id="b656e-121">Ajoitusavustajan käynnistäminen</span><span class="sxs-lookup"><span data-stu-id="b656e-121">Launch the Schedule assistant</span></span>

<span data-ttu-id="b656e-122">Ajoitusavustaja voidaan käynnistää kahdella tavalla.</span><span class="sxs-lookup"><span data-stu-id="b656e-122">There are two ways in which the schedule assistant is launched.</span></span> <span data-ttu-id="b656e-123">Jos käytät hybriditilaa, voit valita Ryhmän jäsen -ruudukossa minkä tahansa ryhmän jäsenen, jonka resurssitarve on täyttämättä, ja valita sitten **Varaa**.</span><span class="sxs-lookup"><span data-stu-id="b656e-123">If you're using the hybrid mode, in the team member grid you can select any team member with an unfulfilled resource requirement, and then select **Book**.</span></span> <span data-ttu-id="b656e-124">Jos käytät keskitettyä tilaa, resurssipäällikkö etsii ja valitsee resurssin.</span><span class="sxs-lookup"><span data-stu-id="b656e-124">If you're using the central mode, the Resource manager finds and selects the resource.</span></span>

## <a name="schedule-assistant-filters"></a><span data-ttu-id="b656e-125">Ajoitusavustajan suodattimet</span><span class="sxs-lookup"><span data-stu-id="b656e-125">Schedule assistant filters</span></span>

<span data-ttu-id="b656e-126">Kun ajoitusavustaja on suoritettu, resurssitarpeen tiedot näkyvät vasemmanpuoleisessa ruudussa suodatettuina arvoina.</span><span class="sxs-lookup"><span data-stu-id="b656e-126">After the Schedule assistant runs, the details from the resource requirement are displayed as filtered values in the left pane.</span></span> <span data-ttu-id="b656e-127">Resurssipäällikkö tai projektiäällikkö voi hienosäätää tuloksia säätämällä suodattimia vastaamaan aikataulutuksen tarpeita.</span><span class="sxs-lookup"><span data-stu-id="b656e-127">The Resource manager or the Project manager can fine-tune results by adjusting filters to meet the scheduling needs.</span></span>

<span data-ttu-id="b656e-128">Suodatusruudussa näkyvät työhön liittyvät asetukset, kuten seuraavat:</span><span class="sxs-lookup"><span data-stu-id="b656e-128">The filter pane shows work-related options, including:</span></span>

-   <span data-ttu-id="b656e-129">Työn aloitus- ja päättymisajat</span><span class="sxs-lookup"><span data-stu-id="b656e-129">Work start and end</span></span>
-   <span data-ttu-id="b656e-130">Ominaisuudet</span><span class="sxs-lookup"><span data-stu-id="b656e-130">Characteristics</span></span>
-   <span data-ttu-id="b656e-131">Roolit</span><span class="sxs-lookup"><span data-stu-id="b656e-131">Roles</span></span>
-   <span data-ttu-id="b656e-132">Organisaatioyksiköt</span><span class="sxs-lookup"><span data-stu-id="b656e-132">Organizational units</span></span>
-   <span data-ttu-id="b656e-133">Resursoiva yritys</span><span class="sxs-lookup"><span data-stu-id="b656e-133">Resourcing company</span></span>
-   <span data-ttu-id="b656e-134">Resurssityypit</span><span class="sxs-lookup"><span data-stu-id="b656e-134">Resource types</span></span>
-   <span data-ttu-id="b656e-135">Ensisijaiset resurssit</span><span class="sxs-lookup"><span data-stu-id="b656e-135">Preferred resources</span></span>
