---
title: Resurssien hallintatilojen yleiskatsaus
description: Tässä aiheessa on tietoja resurssienhallinnan toiminnosta Dynamics 365 Project Operationsissa.
author: ruhercul
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 94db65a2ddbdc6a7226c70907bcce4c45b4a3923
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/10/2021
ms.locfileid: "6000882"
---
# <a name="resource-management-modes-overview"></a><span data-ttu-id="c49d3-103">Resurssien hallintatilojen yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="c49d3-103">Resource management modes overview</span></span>

<span data-ttu-id="c49d3-104">_**Koskee:** Project Operationsin resurssiin / muuhun kuin resurssiin perustuvia skenaarioita, Lite-käyttöönotto-kaupasta proformalaskutukseen_</span><span class="sxs-lookup"><span data-stu-id="c49d3-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="c49d3-105">Dynamics 365 Project Operations tukee kahta tilaa, jotta voit suorittaa yleisen varaustyönkulun.</span><span class="sxs-lookup"><span data-stu-id="c49d3-105">Dynamics 365 Project Operations supports two modes in order for you to execute the overall booking flow.</span></span> <span data-ttu-id="c49d3-106">Hallintatapa määritetään projektiparametrina, ja sitä voi muokata, jos yrityksen tarpeet muuttuvat.</span><span class="sxs-lookup"><span data-stu-id="c49d3-106">The mode of management is defined as a project parameter and can be modified if your business needs change.</span></span>    

## <a name="central-mode"></a><span data-ttu-id="c49d3-107">Keskitetty tila</span><span class="sxs-lookup"><span data-stu-id="c49d3-107">Central mode</span></span>
<span data-ttu-id="c49d3-108">Jos kyseessä on organisaatio, joka keskittää resurssien kohdistuksen projekteihin, keskitetyn tilan avulla voit varmistaa, että projektipäälliköt voivat määrittää resurssitarpeet projektitasolla.</span><span class="sxs-lookup"><span data-stu-id="c49d3-108">For organizations who centralize the allocation for resources to projects, the Central mode provides a way to ensure Project managers can define resource requirements at the project level.</span></span> <span data-ttu-id="c49d3-109">Resurssitarpeiden täyttäminen delegoidaan resurssipäällikölle.</span><span class="sxs-lookup"><span data-stu-id="c49d3-109">Fulfillment of the resource requirements is delegated to a Resource manager.</span></span> <span data-ttu-id="c49d3-110">Projektipäälliköt voivat hyväksyä tai hylätä resurssipäällikön ehdottamat resurssit.</span><span class="sxs-lookup"><span data-stu-id="c49d3-110">Project managers can accept or reject resources that are proposed by the Resource manager.</span></span>

![Keskitetty tila](./media/resource-management-central.png)

<span data-ttu-id="c49d3-112">Jos haluat hallita resursseja keskitetyn tilan avulla, katso:</span><span class="sxs-lookup"><span data-stu-id="c49d3-112">To manage resources with the Central mode, see:</span></span>

- [<span data-ttu-id="c49d3-113">Yleisten varattavissa olevien resurssien delegointi tehtävään ja resurssitarpeiden luominen</span><span class="sxs-lookup"><span data-stu-id="c49d3-113">Assign generic bookable resources to a task and generate resource requirements</span></span>](/dynamics365/project-service/assign-generic-bookable-resource)
- [<span data-ttu-id="c49d3-114">Nimettyjen resurssien varaaminen resurssitarpeista</span><span class="sxs-lookup"><span data-stu-id="c49d3-114">Book named resources from resource requirements</span></span>](/dynamics365/project-service/book-named-resource)
- [<span data-ttu-id="c49d3-115">Resurssipyynnön lähettäminen</span><span class="sxs-lookup"><span data-stu-id="c49d3-115">Submit a resource request</span></span>](/dynamics365/project-service/submit-resource-request)
- [<span data-ttu-id="c49d3-116">Resurssipyyntöjen täyttäminen</span><span class="sxs-lookup"><span data-stu-id="c49d3-116">Fulfill a resource request</span></span>](/dynamics365/project-service/resource-management-fulfill-requests)
- [<span data-ttu-id="c49d3-117">Ehdotetun projektiresurssin hyväksyminen tai hylkääminen resurssipyynnöstä</span><span class="sxs-lookup"><span data-stu-id="c49d3-117">Accept or reject a proposed project resource from a resource request</span></span>](/dynamics365/project-service/accept-reject-proposed-resource)

## <a name="hybrid-mode"></a><span data-ttu-id="c49d3-118">Hybriditila</span><span class="sxs-lookup"><span data-stu-id="c49d3-118">Hybrid mode</span></span>
<span data-ttu-id="c49d3-119">Organisaatioille, jotka tarvitsevat resurssien kohdentamisen joustavuutta, hybriditilan avulla sekä projekti päälliköt että resurssipäälliköt voivat varata resursseja.</span><span class="sxs-lookup"><span data-stu-id="c49d3-119">For organizations who require flexibility in the allocation of resources, the hybrid mode enables both Project managers and Resource managers the ability to book resources.</span></span>

![Hybriditila](./media/resource-management-hybrid.png)

<span data-ttu-id="c49d3-121">Tuetun keskitetyn tilan prosessin lisäksi voit hallita kaikkia muita tuettuja varaustyönkulkuja hybriditilassa seuraavien aiheiden ohjeiden mukaisesti:</span><span class="sxs-lookup"><span data-stu-id="c49d3-121">In addition to the supported Central mode process, see the following topics to manage all other supported booking flows in the Hybrid mode:</span></span>

<span data-ttu-id="c49d3-122">Resurssin varaaminen suoraan projektiin:</span><span class="sxs-lookup"><span data-stu-id="c49d3-122">Book a resource directly to a project:</span></span>
- [<span data-ttu-id="c49d3-123">Nimettyjen varattavissa olevien resurssien varaaminen projektiryhmälle ja tehtävien kohdennus</span><span class="sxs-lookup"><span data-stu-id="c49d3-123">Book named bookable resources to a project team and assign tasks</span></span>](/dynamics365/project-service/assign-named-bookable-resource)

<span data-ttu-id="c49d3-124">Resurssien varaaminen resurssitarpeesta:</span><span class="sxs-lookup"><span data-stu-id="c49d3-124">Book a resource from a resource requirement:</span></span>
- [<span data-ttu-id="c49d3-125">Yleisten varattavissa olevien resurssien delegointi tehtävään ja resurssitarpeiden luominen</span><span class="sxs-lookup"><span data-stu-id="c49d3-125">Assign generic bookable resources to a task and generate resource requirements</span></span>](/dynamics365/project-service/assign-generic-bookable-resource)
- [<span data-ttu-id="c49d3-126">Nimettyjen resurssien varaaminen resurssitarpeista</span><span class="sxs-lookup"><span data-stu-id="c49d3-126">Book named resources from resource requirements</span></span>](/dynamics365/project-service/book-named-resource)


[!INCLUDE[footer-include](../includes/footer-banner.md)]