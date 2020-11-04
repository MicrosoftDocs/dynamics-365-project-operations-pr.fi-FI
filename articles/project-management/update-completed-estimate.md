---
title: Valmistumisen kustannusarvion päivittäminen
description: Tässä aiheessa on tietoja projektin työn arvion päivittämisestä.
author: ruhercul
manager: AnnBe
ms.date: 09/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 16393133a5de17308caceb069d7bca670caa04c8
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/16/2020
ms.locfileid: "4075531"
---
# <a name="update-estimate-at-completion"></a><span data-ttu-id="a74c3-103">Valmistumisen kustannusarvion päivittäminen</span><span class="sxs-lookup"><span data-stu-id="a74c3-103">Update estimate at completion</span></span>

<span data-ttu-id="a74c3-104">_**Koskee:** Project Operationsin resurssiin / muuhun kuin resurssiin perustuvia skenaarioita, Lite-käyttöönotto-kaupasta proformalaskutukseen_</span><span class="sxs-lookup"><span data-stu-id="a74c3-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="a74c3-105">On tavallista, että projektipäällikkö muuttaa tehtävän alkuperäisiä arvioita.</span><span class="sxs-lookup"><span data-stu-id="a74c3-105">It's common for a project manager to revise the original estimates on a task.</span></span> <span data-ttu-id="a74c3-106">Projektin uudelleenprojisoinnit ovat projektipäällikön arvioita, joissa otetaan huomioon projektin tämänhetkinen tila.</span><span class="sxs-lookup"><span data-stu-id="a74c3-106">Project reprojections are a project manager's perception of estimates, given the current state of a project.</span></span> <span data-ttu-id="a74c3-107">Microsoft ei suosittele perusaikataulun numeroiden muuttamista, koska projektin perusaikataulu on projektin aikataulun ja kustannusarvioiden virallinen lähde, ja projektin kaikki sidosryhmät ovat hyväksyneet sen.</span><span class="sxs-lookup"><span data-stu-id="a74c3-107">However, we don't recommend that project managers change the baseline numbers, because the project baseline represents the established source of truth for the project's schedule and cost estimate, and all project stakeholders have agreed to it.</span></span>

<span data-ttu-id="a74c3-108">Projektipäällikkö voi projisoida tehtävien työmäärää uudelleen seuraavilla kahdella tavalla:</span><span class="sxs-lookup"><span data-stu-id="a74c3-108">There are two ways that a project manager can reproject effort on tasks:</span></span>

- <span data-ttu-id="a74c3-109">Korvaa oletusvalmistumisarvion tehtävän uudella todellisen jäljellä olevan työn arvolla.</span><span class="sxs-lookup"><span data-stu-id="a74c3-109">Override the default estimate to complete (ETC) with a new estimate of the actual remaining effort on the task.</span></span> 
- <span data-ttu-id="a74c3-110">Korvaa oletusarvoinen edistymisprosentti uudella arviolla tehtävän todellisesta edistymisestä.</span><span class="sxs-lookup"><span data-stu-id="a74c3-110">Override the default progress percentage with a new estimate of the true progress on the task.</span></span>

<span data-ttu-id="a74c3-111">Kukin näistä lähestymistavoista aiheuttaa tehtävän valmistumisarvion, valmistumisen kustannusarvion ja edistymisprosentin sekä ennustetun työmäärän varianssin uudelleenlaskennan.</span><span class="sxs-lookup"><span data-stu-id="a74c3-111">Each of these approaches cause a recalculation of the task's ETC, estimate at complete (EAC), and progress percentage, and the projected effort variance on a task.</span></span> <span data-ttu-id="a74c3-112">Myös yhteenvetotehtävien valmistumisen kustannusarvio, valmistumisarvio ja edistymisprosentti lasketaan uudelleen. Näin saadaan uusi työmäärän varianssin arvio.</span><span class="sxs-lookup"><span data-stu-id="a74c3-112">The EAC, ETC, and progress percentage on the summary tasks are recalculated, and produce a new projection of effort variance.</span></span>
