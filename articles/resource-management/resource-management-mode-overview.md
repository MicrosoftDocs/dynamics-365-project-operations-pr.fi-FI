---
title: Resurssien hallintatilojen yleiskatsaus
description: Tässä aiheessa on tietoja resurssienhallinnan toiminnosta Dynamics 365 Project Operationsissa.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 872f4f2878f474e16674932f23fe192c6a8de6eb
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5279449"
---
# <a name="resource-management-modes-overview"></a><span data-ttu-id="c9f91-103">Resurssien hallintatilojen yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="c9f91-103">Resource management modes overview</span></span>

<span data-ttu-id="c9f91-104">_**Koskee:** Project Operationsin resurssiin / muuhun kuin resurssiin perustuvia skenaarioita, Lite-käyttöönotto-kaupasta proformalaskutukseen_</span><span class="sxs-lookup"><span data-stu-id="c9f91-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="c9f91-105">Dynamics 365 Project Operations tukee kahta tilaa, jotta voit suorittaa yleisen varaustyönkulun.</span><span class="sxs-lookup"><span data-stu-id="c9f91-105">Dynamics 365 Project Operations supports two modes in order for you to execute the overall booking flow.</span></span> <span data-ttu-id="c9f91-106">Hallintatapa määritetään projektiparametrina, ja sitä voi muokata, jos yrityksen tarpeet muuttuvat.</span><span class="sxs-lookup"><span data-stu-id="c9f91-106">The mode of management is defined as a project parameter and can be modified if your business needs change.</span></span>    

## <a name="central-mode"></a><span data-ttu-id="c9f91-107">Keskitetty tila</span><span class="sxs-lookup"><span data-stu-id="c9f91-107">Central mode</span></span>
<span data-ttu-id="c9f91-108">Jos kyseessä on organisaatio, joka keskittää resurssien kohdistuksen projekteihin, keskitetyn tilan avulla voit varmistaa, että projektipäälliköt voivat määrittää resurssitarpeet projektitasolla.</span><span class="sxs-lookup"><span data-stu-id="c9f91-108">For organizations who centralize the allocation for resources to projects, the Central mode provides a way to ensure Project managers can define resource requirements at the project level.</span></span> <span data-ttu-id="c9f91-109">Resurssitarpeiden täyttäminen delegoidaan resurssipäällikölle.</span><span class="sxs-lookup"><span data-stu-id="c9f91-109">Fulfillment of the resource requirements is delegated to a Resource manager.</span></span> <span data-ttu-id="c9f91-110">Projektipäälliköt voivat hyväksyä tai hylätä resurssipäällikön ehdottamat resurssit.</span><span class="sxs-lookup"><span data-stu-id="c9f91-110">Project managers can accept or reject resources that are proposed by the Resource manager.</span></span>

![Keskitetty tila](./media/resource-management-central.png)

<span data-ttu-id="c9f91-112">Jos haluat hallita resursseja keskitetyn tilan avulla, katso:</span><span class="sxs-lookup"><span data-stu-id="c9f91-112">To manage resources with the Central mode, see:</span></span>

- [<span data-ttu-id="c9f91-113">Yleisten varattavissa olevien resurssien delegointi tehtävään ja resurssitarpeiden luominen</span><span class="sxs-lookup"><span data-stu-id="c9f91-113">Assign generic bookable resources to a task and generate resource requirements</span></span>](https://docs.microsoft.com/dynamics365/project-service/assign-generic-bookable-resource)
- [<span data-ttu-id="c9f91-114">Nimettyjen resurssien varaaminen resurssitarpeista</span><span class="sxs-lookup"><span data-stu-id="c9f91-114">Book named resources from resource requirements</span></span>](https://docs.microsoft.com/dynamics365/project-service/book-named-resource)
- [<span data-ttu-id="c9f91-115">Resurssipyynnön lähettäminen</span><span class="sxs-lookup"><span data-stu-id="c9f91-115">Submit a resource request</span></span>](https://docs.microsoft.com/dynamics365/project-service/submit-resource-request)
- [<span data-ttu-id="c9f91-116">Resurssipyyntöjen täyttäminen</span><span class="sxs-lookup"><span data-stu-id="c9f91-116">Fulfill a resource request</span></span>](https://docs.microsoft.com/dynamics365/project-service/resource-management-fulfill-requests)
- [<span data-ttu-id="c9f91-117">Ehdotetun projektiresurssin hyväksyminen tai hylkääminen resurssipyynnöstä</span><span class="sxs-lookup"><span data-stu-id="c9f91-117">Accept or reject a proposed project resource from a resource request</span></span>](https://docs.microsoft.com/dynamics365/project-service/accept-reject-proposed-resource)

## <a name="hybrid-mode"></a><span data-ttu-id="c9f91-118">Hybriditila</span><span class="sxs-lookup"><span data-stu-id="c9f91-118">Hybrid mode</span></span>
<span data-ttu-id="c9f91-119">Organisaatioille, jotka tarvitsevat resurssien kohdentamisen joustavuutta, hybriditilan avulla sekä projekti päälliköt että resurssipäälliköt voivat varata resursseja.</span><span class="sxs-lookup"><span data-stu-id="c9f91-119">For organizations who require flexibility in the allocation of resources, the hybrid mode enables both Project managers and Resource managers the ability to book resources.</span></span>

![Hybriditila](./media/resource-management-hybrid.png)

<span data-ttu-id="c9f91-121">Tuetun keskitetyn tilan prosessin lisäksi voit hallita kaikkia muita tuettuja varaustyönkulkuja hybriditilassa seuraavien aiheiden ohjeiden mukaisesti:</span><span class="sxs-lookup"><span data-stu-id="c9f91-121">In addition to the supported Central mode process, see the following topics to manage all other supported booking flows in the Hybrid mode:</span></span>

<span data-ttu-id="c9f91-122">Resurssin varaaminen suoraan projektiin:</span><span class="sxs-lookup"><span data-stu-id="c9f91-122">Book a resource directly to a project:</span></span>
- [<span data-ttu-id="c9f91-123">Nimettyjen varattavissa olevien resurssien varaaminen projektiryhmälle ja tehtävien kohdennus</span><span class="sxs-lookup"><span data-stu-id="c9f91-123">Book named bookable resources to a project team and assign tasks</span></span>](https://docs.microsoft.com/dynamics365/project-service/assign-named-bookable-resource)

<span data-ttu-id="c9f91-124">Resurssien varaaminen resurssitarpeesta:</span><span class="sxs-lookup"><span data-stu-id="c9f91-124">Book a resource from a resource requirement:</span></span>
- [<span data-ttu-id="c9f91-125">Yleisten varattavissa olevien resurssien delegointi tehtävään ja resurssitarpeiden luominen</span><span class="sxs-lookup"><span data-stu-id="c9f91-125">Assign generic bookable resources to a task and generate resource requirements</span></span>](https://docs.microsoft.com/dynamics365/project-service/assign-generic-bookable-resource)
- [<span data-ttu-id="c9f91-126">Nimettyjen resurssien varaaminen resurssitarpeista</span><span class="sxs-lookup"><span data-stu-id="c9f91-126">Book named resources from resource requirements</span></span>](https://docs.microsoft.com/dynamics365/project-service/book-named-resource)


[!INCLUDE[footer-include](../includes/footer-banner.md)]