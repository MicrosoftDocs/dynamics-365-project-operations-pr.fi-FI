---
title: Osaamisalueiden ja pätevyyksien määrittäminen
description: Tässä aiheessa on tietoja pätevyysmallien määrittämisestä resurssien arvioimiseksi.
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
ms.openlocfilehash: 9376e0b268a3ab682716da604ceecfa1e878da68
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/28/2020
ms.locfileid: "3897627"
---
# <a name="define-skills-and-proficiencies"></a><span data-ttu-id="f2af3-103">Osaamisalueiden ja pätevyyksien määrittäminen</span><span class="sxs-lookup"><span data-stu-id="f2af3-103">Define skills and proficiencies</span></span>

<span data-ttu-id="f2af3-104">_**Koskee:** Project Operationsin resurssiin / muuhun kuin resurssiin perustuvia skenaarioita, Lite-käyttöönotto-kaupasta proformalaskutukseen_</span><span class="sxs-lookup"><span data-stu-id="f2af3-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="f2af3-105">Taidot ovat resurssien ominaisuuksia, jotka on jaettu Dynamics 365 Project Operationsin ja mahdollisesti käytössä olevan Dynamics 365 Field Servicen välillä.</span><span class="sxs-lookup"><span data-stu-id="f2af3-105">Skills are resource characteristics that are shared between Dynamics 365 Project Operations and if present, Dynamics 365 Field Service.</span></span> 

- <span data-ttu-id="f2af3-106">Ylläpidä taitosäilöä Project Operationsissa siirtymällä kohtaan **Resurssit** \> **Resurssien taidot**.</span><span class="sxs-lookup"><span data-stu-id="f2af3-106">To maintain the repository of skills in Project Operations, go to **Resources** \> **Resource Skills**.</span></span> 

## <a name="use-proficiency-models-to-rate-resources"></a><span data-ttu-id="f2af3-107">Pätevyysmallien käyttäminen resurssien tasojen määrittelyyn</span><span class="sxs-lookup"><span data-stu-id="f2af3-107">Use proficiency models to rate resources</span></span>

<span data-ttu-id="f2af3-108">Resurssien taidot on luokiteltu pätevyysmallien mukaan.</span><span class="sxs-lookup"><span data-stu-id="f2af3-108">Skills for resources are rated by proficiency models.</span></span> <span data-ttu-id="f2af3-109">Yksittäiset luokitukset ovat pätevyysmallissa.</span><span class="sxs-lookup"><span data-stu-id="f2af3-109">The individual ratings are in a proficiency model.</span></span> 

1. <span data-ttu-id="f2af3-110">Luodaksesi pätevyysmallin siirry kohtaan **Resurssit** \> **Pätevyysmallit** ja valitse sitten **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="f2af3-110">To create a proficiency model, go to **Resources** \> **Proficiency Models**, and then select **New**.</span></span>
2. <span data-ttu-id="f2af3-111">Määritä uudessa luokitusmallissa pienin luokitusarvo, suurin luokitusarvo ja entiteetti, jota luokitellaan.</span><span class="sxs-lookup"><span data-stu-id="f2af3-111">In the new rating model, specify the minimum rating value, the maximum rating value, and the entity that is being rated.</span></span>
3. <span data-ttu-id="f2af3-112">**Luokitusarvojen** aliruudukossa voit määrittää eri luokitusarvot vähimmäisarvosta suurimpaan.</span><span class="sxs-lookup"><span data-stu-id="f2af3-112">In the **Rating Values** sub-grid, you can define the different rating values, from the minimum to the maximum.</span></span>


<span data-ttu-id="f2af3-113">Nämä luokitusarvot näytetään **Resurssivaatimukset**, **Aikataulutaulukko** ja **Aikatauluavustaja** -suodattimissa.</span><span class="sxs-lookup"><span data-stu-id="f2af3-113">These rating values are shown on the **Resource Requirements**, **Schedule Board**, and **Schedule Assistant** filters.</span></span>
