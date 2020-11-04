---
title: Resurssien hallintatilojen yleiskatsaus
description: Tämä aihe tarjoaa tietoja Dynamics 365 Project Operationsin uusista resurssinhallintatoiminnosta.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 4a8e605109e48b50da68abeee989f8ac8d3d659c
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/16/2020
ms.locfileid: "4075236"
---
# <a name="resource-management-modes-overview"></a><span data-ttu-id="e4938-103">Resurssien hallintatilojen yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="e4938-103">Resource management modes overview</span></span>

<span data-ttu-id="e4938-104">_**Koskee:** Project Operationsin resurssiin / muuhun kuin resurssiin perustuvia skenaarioita, Lite-käyttöönotto-kaupasta proformalaskutukseen_</span><span class="sxs-lookup"><span data-stu-id="e4938-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="e4938-105">Dynamics 365 Project Operations tukee kahta tilaa, jotta voit suorittaa varaustyönkulun kokonaisuudessaan.</span><span class="sxs-lookup"><span data-stu-id="e4938-105">Dynamics 365 Project Operations supports two modes in order for you to execute the overall booking flow.</span></span> <span data-ttu-id="e4938-106">Hallintatapa määritetään projektiparametrina, ja sitä voi muokata, jos yrityksen tarpeet muuttuvat.</span><span class="sxs-lookup"><span data-stu-id="e4938-106">The mode of management is defined as a project parameter and can be modified if your business needs change.</span></span>    

## <a name="central-mode"></a><span data-ttu-id="e4938-107">Keskitetty tila</span><span class="sxs-lookup"><span data-stu-id="e4938-107">Central mode</span></span>
<span data-ttu-id="e4938-108">Jos kyseessä on organisaatio, joka keskittää resurssien kohdistuksen projekteihin, keskitetyn tilan avulla voit varmistaa, että projektipäälliköt voivat määrittää resurssitarpeet projektitasolla.</span><span class="sxs-lookup"><span data-stu-id="e4938-108">For organizations who centralize the allocation for resources to projects, the Central mode provides a way to ensure Project managers can define resource requirements at the project level.</span></span> <span data-ttu-id="e4938-109">Resurssitarpeiden täyttäminen delegoidaan resurssipäällikölle.</span><span class="sxs-lookup"><span data-stu-id="e4938-109">Fulfillment of the resource requirements is delegated to a Resource manager.</span></span> <span data-ttu-id="e4938-110">Projektipäälliköt voivat hyväksyä tai hylätä resurssipäällikön ehdottamat resurssit.</span><span class="sxs-lookup"><span data-stu-id="e4938-110">Project managers can accept or reject resources that are proposed by the Resource manager.</span></span>

![Keskitetty tila](./media/resource-management-central.png)

<span data-ttu-id="e4938-112">Jos haluat hallita resursseja keskitetyn tilan avulla, katso:</span><span class="sxs-lookup"><span data-stu-id="e4938-112">To manage resources with the Central mode, see:</span></span>

- [<span data-ttu-id="e4938-113">Yleisten varattavissa olevien resurssien delegointi tehtävään ja resurssitarpeiden luominen</span><span class="sxs-lookup"><span data-stu-id="e4938-113">Assign generic bookable resources to a task and generate resource requirements</span></span>](https://docs.microsoft.com/dynamics365/project-service/assign-generic-bookable-resource)
- [<span data-ttu-id="e4938-114">Nimettyjen resurssien varaaminen resurssitarpeista</span><span class="sxs-lookup"><span data-stu-id="e4938-114">Book named resources from resource requirements</span></span>](https://docs.microsoft.com/dynamics365/project-service/book-named-resource)
- [<span data-ttu-id="e4938-115">Resurssipyynnön lähettäminen</span><span class="sxs-lookup"><span data-stu-id="e4938-115">Submit a resource request</span></span>](https://docs.microsoft.com/dynamics365/project-service/submit-resource-request)
- [<span data-ttu-id="e4938-116">Resurssipyyntöjen täyttäminen</span><span class="sxs-lookup"><span data-stu-id="e4938-116">Fulfill a resource request</span></span>](https://docs.microsoft.com/dynamics365/project-service/resource-management-fulfill-requests)
- [<span data-ttu-id="e4938-117">Ehdotetun projektiresurssin hyväksyminen tai hylkääminen resurssipyynnöstä</span><span class="sxs-lookup"><span data-stu-id="e4938-117">Accept or reject a proposed project resource from a resource request</span></span>](https://docs.microsoft.com/dynamics365/project-service/accept-reject-proposed-resource)

## <a name="hybrid-mode"></a><span data-ttu-id="e4938-118">Hybriditila</span><span class="sxs-lookup"><span data-stu-id="e4938-118">Hybrid mode</span></span>
<span data-ttu-id="e4938-119">Organisaatioille, jotka tarvitsevat resurssien kohdentamisen joustavuutta, hybriditilan avulla sekä projekti päälliköt että resurssipäälliköt voivat varata resursseja.</span><span class="sxs-lookup"><span data-stu-id="e4938-119">For organizations who require flexibility in the allocation of resources, the hybrid mode enables both Project managers and Resource managers the ability to book resources.</span></span>

![Hybriditila](./media/resource-management-hybrid.png)

<span data-ttu-id="e4938-121">Tuetun keskitetyn tilan prosessin lisäksi voit hallita kaikkia muita tuettuja varaustyönkulkuja hybriditilassa seuraavien aiheiden ohjeiden mukaisesti:</span><span class="sxs-lookup"><span data-stu-id="e4938-121">In addition to the supported Central mode process, see the following topics to manage all other supported booking flows in the Hybrid mode:</span></span>

<span data-ttu-id="e4938-122">Resurssin varaaminen suoraan projektiin:</span><span class="sxs-lookup"><span data-stu-id="e4938-122">Book a resource directly to a project:</span></span>
- [<span data-ttu-id="e4938-123">Nimettyjen varattavissa olevien resurssien varaaminen projektiryhmälle ja tehtävien kohdennus</span><span class="sxs-lookup"><span data-stu-id="e4938-123">Book named bookable resources to a project team and assign tasks</span></span>](https://docs.microsoft.com/dynamics365/project-service/assign-named-bookable-resource)

<span data-ttu-id="e4938-124">Resurssien varaaminen resurssitarpeesta:</span><span class="sxs-lookup"><span data-stu-id="e4938-124">Book a resource from a resource requirement:</span></span>
- [<span data-ttu-id="e4938-125">Yleisten varattavissa olevien resurssien delegointi tehtävään ja resurssitarpeiden luominen</span><span class="sxs-lookup"><span data-stu-id="e4938-125">Assign generic bookable resources to a task and generate resource requirements</span></span>](https://docs.microsoft.com/dynamics365/project-service/assign-generic-bookable-resource)
- [<span data-ttu-id="e4938-126">Nimettyjen resurssien varaaminen resurssitarpeista</span><span class="sxs-lookup"><span data-stu-id="e4938-126">Book named resources from resource requirements</span></span>](https://docs.microsoft.com/dynamics365/project-service/book-named-resource)
