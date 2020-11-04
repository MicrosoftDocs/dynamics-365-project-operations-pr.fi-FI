---
title: Projektien myyntitilaukset aika- ja materiaaliprojekteille
description: Tässä aiheessa selitetään, miten projektiin perustuvia myyntitilauksia luodaan aika- ja materiaaliprojekteille.
author: Yowelle
manager: AnnBe
ms.date: 04/05/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2019-04-05
ms.dyn365.ops.version: AX 10.0.2
ms.openlocfilehash: 3653a6869dab323be88f1fd0f9fd0f2cb35c456f
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/16/2020
ms.locfileid: "4075333"
---
# <a name="project-sales-orders-for-time-and-material-projects"></a><span data-ttu-id="e01b4-103">Projektien myyntitilaukset aika- ja materiaaliprojekteille</span><span class="sxs-lookup"><span data-stu-id="e01b4-103">Project sales orders for time and material projects</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="e01b4-104">Tässä aiheessa kuvataan, miten projekteille luodaan myyntitilaus.</span><span class="sxs-lookup"><span data-stu-id="e01b4-104">This topic describes how to create a sales order for a project.</span></span> <span data-ttu-id="e01b4-105">Myyntitilauksia voi luoda vain **aika ja materiaali** -tyypin projekteille.</span><span class="sxs-lookup"><span data-stu-id="e01b4-105">Sales orders can only be created for projects of type **time and material**.</span></span>

<span data-ttu-id="e01b4-106">Jos aika-ja materiaali projektin projektisopimuksissa on useita rahoituslähteitä, sinun täytyy ottaa käyttöön **Salli myyntitilaukset projekteille, joilla on useita rahoitus lähteitä** -parametri **Projektinhallinnan ja kirjanpidon parametrit** -sivulla.</span><span class="sxs-lookup"><span data-stu-id="e01b4-106">If a time and material project has multiple funding sources on the project contract, you must enable the **Allow sales orders for projects with multiple funding sources** parameter on the **Project management and accounting parameters** page.</span></span> 

> [!NOTE]
> - <span data-ttu-id="e01b4-107">Tuki projektien myyntitilauksille, joilla on useita rahoituslähteitä, on käytettävissä sovellusversiosta 10.0.2 alkaen.</span><span class="sxs-lookup"><span data-stu-id="e01b4-107">Support for project sales orders with multiple funding sources is available starting with application release 10.0.2 and higher.</span></span>
> - <span data-ttu-id="e01b4-108">Parametri, jolla otetaan käyttöön projektin myyntitilaukset, joilla on useita rahoituslähteitä, poistetaan huhtikuun 2020 julkaisuaallossa, minkä jälkeen toiminto on aina käytössä.</span><span class="sxs-lookup"><span data-stu-id="e01b4-108">The parameter to enable the support for project sales orders with multiple funding sources will be removed in the April 2020 release wave, after which the functionality will always be enabled.</span></span>

<span data-ttu-id="e01b4-109">Voit luoda projektiperusteisia myyntitilauksia kahdella seuraavalla tavalla.</span><span class="sxs-lookup"><span data-stu-id="e01b4-109">You can create project-based sales orders in two ways:</span></span>

- <span data-ttu-id="e01b4-110">Siirry projektiin itseensä.</span><span class="sxs-lookup"><span data-stu-id="e01b4-110">Go to the project itself.</span></span> <span data-ttu-id="e01b4-111">Valitse toimintoruudussa **Hallitse > Nimiketehtävät > Myyntitilaus**.</span><span class="sxs-lookup"><span data-stu-id="e01b4-111">On the Action Pane, select **Manage > Item tasks > Sales order**.</span></span> <span data-ttu-id="e01b4-112">Projektitiedot siirtyvät oletusarvoiksi projektin myyntitilaukseen.</span><span class="sxs-lookup"><span data-stu-id="e01b4-112">The project information will default to the sales order from the project.</span></span> <span data-ttu-id="e01b4-113">Jos projektisopimuksessa on useita rahoituslähteitä, sinun on valittava rahoituslähde, jotta voit määrittää asiakkaan myyntitilaukselle.</span><span class="sxs-lookup"><span data-stu-id="e01b4-113">If the project contract has more than one funding source, you will need to select the funding source to set the customer for the sales order.</span></span> <span data-ttu-id="e01b4-114">Jos projektille on vain yksi rahoituslähde, asiakas määritetään automaattisesti.</span><span class="sxs-lookup"><span data-stu-id="e01b4-114">If there is only one funding source for the project, the customer will be automatically set.</span></span>
- <span data-ttu-id="e01b4-115">Siirry **Kaikki myyntitilaukset** -luettelosivulle ja luo uusi myyntitilaus.</span><span class="sxs-lookup"><span data-stu-id="e01b4-115">Go to the **All sales order** list page and create a new sales order.</span></span> <span data-ttu-id="e01b4-116">Sinun on valittava projekti myyntitilausta varten.</span><span class="sxs-lookup"><span data-stu-id="e01b4-116">You will need to select the project for the sales order.</span></span> <span data-ttu-id="e01b4-117">Kun projekti on valittu, asiakas määritetään rahoituslähteen perusteella tai sinun on valittava rahoituslähde, jos projektisopimuksessa on useita rahoituslähteitä.</span><span class="sxs-lookup"><span data-stu-id="e01b4-117">After the project is selected, the customer will be set from the funding source or you will need to select the funding source if the project contract has multiple funding sources.</span></span>

