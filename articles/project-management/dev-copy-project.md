---
title: Projektimallien kehittäminen kopiointiprojektin avulla
description: Tässä aiheessa on tietoja siitä, miten projektimalleja luodaan kopioi projekti -mukautetun toiminnon avulla.
author: stsporen
manager: Annbe
ms.date: 10/07/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: cb49109e8c199bc4569702ae844a19985534294d
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/16/2020
ms.locfileid: "4075288"
---
# <a name="develop-project-templates-with-copy-project"></a><span data-ttu-id="c73ff-103">Projektimallien kehittäminen kopiointiprojektin avulla</span><span class="sxs-lookup"><span data-stu-id="c73ff-103">Develop project templates with Copy Project</span></span>

<span data-ttu-id="c73ff-104">_**Koskee:** Project Operationsin resurssiin / muuhun kuin resurssiin perustuvia skenaarioita, Lite-käyttöönotto-kaupasta proformalaskutukseen_</span><span class="sxs-lookup"><span data-stu-id="c73ff-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="c73ff-105">Dynamics 365 Project Operations tukee mahdollisuutta kopioida projekti ja palauttaa tehtävät takaisin roolia edustaville yleisille resursseille.</span><span class="sxs-lookup"><span data-stu-id="c73ff-105">Dynamics 365 Project Operations supports the ability to copy a project and revert any assignments back to the generic resources that represent the role.</span></span> <span data-ttu-id="c73ff-106">Tämän toiminnon avulla asiakkaat voivat luoda perusprojektimalleja.</span><span class="sxs-lookup"><span data-stu-id="c73ff-106">Customers can use this functionality to build basic project templates.</span></span>

<span data-ttu-id="c73ff-107">Kun valitset **Kopioi projekti** , kohdeprojektin tila päivittyy.</span><span class="sxs-lookup"><span data-stu-id="c73ff-107">When you select **Copy Project** , the status of the target project is updated.</span></span> <span data-ttu-id="c73ff-108">**Tilan syyn** avulla voit määrittää, milloin kopiointitoiminto on valmis.</span><span class="sxs-lookup"><span data-stu-id="c73ff-108">Use **Status Reason** to determine when the copy action is complete.</span></span> <span data-ttu-id="c73ff-109">Jos valitset **Kopioi projekti** , myös projektin alkamispäiväksi tulee nykyinen alkamispäivä, jos kohdeprojektientiteetissä ei havaita tavoitepäivämäärää.</span><span class="sxs-lookup"><span data-stu-id="c73ff-109">Selecting **Copy Project** also updates the start date of the project to the current start date if no target date is detected in the target project entity.</span></span>

## <a name="copy-project-custom-action"></a><span data-ttu-id="c73ff-110">Kopioi projektin mukautettu toiminto</span><span class="sxs-lookup"><span data-stu-id="c73ff-110">Copy Project custom action</span></span> 

### <a name="name"></a><span data-ttu-id="c73ff-111">Nimi</span><span class="sxs-lookup"><span data-stu-id="c73ff-111">Name</span></span> 

<span data-ttu-id="c73ff-112">**msdyn_CopyProjectV2**</span><span class="sxs-lookup"><span data-stu-id="c73ff-112">**msdyn_CopyProjectV2**</span></span>

### <a name="input-parameters"></a><span data-ttu-id="c73ff-113">Syöteparametrit</span><span class="sxs-lookup"><span data-stu-id="c73ff-113">Input parameters</span></span>
<span data-ttu-id="c73ff-114">Syöttöparametreja on kolme:</span><span class="sxs-lookup"><span data-stu-id="c73ff-114">There are three input parameters:</span></span>

| <span data-ttu-id="c73ff-115">Parametri</span><span class="sxs-lookup"><span data-stu-id="c73ff-115">Parameter</span></span>          | <span data-ttu-id="c73ff-116">Laji</span><span class="sxs-lookup"><span data-stu-id="c73ff-116">Type</span></span>   | <span data-ttu-id="c73ff-117">Arvot</span><span class="sxs-lookup"><span data-stu-id="c73ff-117">Values</span></span>                                                   | 
|--------------------|--------|----------------------------------------------------------|
| <span data-ttu-id="c73ff-118">ProjectCopyOption</span><span class="sxs-lookup"><span data-stu-id="c73ff-118">ProjectCopyOption</span></span>  | <span data-ttu-id="c73ff-119">String</span><span class="sxs-lookup"><span data-stu-id="c73ff-119">String</span></span> | <span data-ttu-id="c73ff-120">**{"removeNamedResources":true}** tai **{"clearTeamsAndAssignments":true}**</span><span class="sxs-lookup"><span data-stu-id="c73ff-120">**{"removeNamedResources":true}** or **{"clearTeamsAndAssignments":true}**</span></span> |
| <span data-ttu-id="c73ff-121">SourceProject</span><span class="sxs-lookup"><span data-stu-id="c73ff-121">SourceProject</span></span>      | <span data-ttu-id="c73ff-122">Entiteettiviittaus</span><span class="sxs-lookup"><span data-stu-id="c73ff-122">Entity Reference</span></span> | <span data-ttu-id="c73ff-123">Lähdeprojekti</span><span class="sxs-lookup"><span data-stu-id="c73ff-123">Source Project</span></span> |
| <span data-ttu-id="c73ff-124">Kohde</span><span class="sxs-lookup"><span data-stu-id="c73ff-124">Target</span></span>             | <span data-ttu-id="c73ff-125">Entiteettiviittaus</span><span class="sxs-lookup"><span data-stu-id="c73ff-125">Entity Reference</span></span> | <span data-ttu-id="c73ff-126">Kohdeprojekti</span><span class="sxs-lookup"><span data-stu-id="c73ff-126">Target Project</span></span> |


- <span data-ttu-id="c73ff-127">**{"clearTeamsAndAssignments":true}** : Kolme oletuskäyttäytyminen web-projektille ja poistaa kaikki varaukset ja ryhmän jäsenet.</span><span class="sxs-lookup"><span data-stu-id="c73ff-127">**{"clearTeamsAndAssignments":true}** : Thee default behavior for Project for the Web, and will remove all assignments and team members.</span></span>
- <span data-ttu-id="c73ff-128">**{"removeNamedResources":true}** Oletustoiminta Project Operationsille ja palauttaa varaukset yleisiin resursseihin.</span><span class="sxs-lookup"><span data-stu-id="c73ff-128">**{"removeNamedResources":true}** The default behavior for Project Operations, and will revert assignments to generic resources.</span></span>

<span data-ttu-id="c73ff-129">Lisätietoja oletustoiminnoista on kohdassa [Verkko-ohjelmointirajapintojen toimintojen käyttö](https://docs.microsoft.com/powerapps/developer/common-data-service/webapi/use-web-api-actions)</span><span class="sxs-lookup"><span data-stu-id="c73ff-129">For more defaults on actions, see [Use Web API actions](https://docs.microsoft.com/powerapps/developer/common-data-service/webapi/use-web-api-actions)</span></span>

## <a name="specify-fields-to-copy"></a><span data-ttu-id="c73ff-130">Kopioitavien kenttien määrittäminen</span><span class="sxs-lookup"><span data-stu-id="c73ff-130">Specify fields to copy</span></span> 
<span data-ttu-id="c73ff-131">Kun toimintoa kutsutaan, **Kopioi projekti** näyttää projektinäkymän **Kopioi projekti sarakkeet** , kun haluat määrittää, mitkä kentät kopioidaan projektin kopioinnin yhteydessä.</span><span class="sxs-lookup"><span data-stu-id="c73ff-131">When the action is called, **Copy Project** will look at the project view **Copy Project Columns** to determine which fields to copy when the project is copied.</span></span>
