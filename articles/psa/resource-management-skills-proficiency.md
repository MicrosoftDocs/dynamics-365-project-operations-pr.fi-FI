---
title: Taidot ja pätevyysmallit
description: Tässä aiheessa on tietoja taitojen ja pätevyysmallien käyttämisestä.
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 03/13/2019
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 976650cc71b0cdb75d5ce2d7532cd78bd91d3670
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/10/2021
ms.locfileid: "6008667"
---
# <a name="skills-and-proficiency-models"></a><span data-ttu-id="846d5-103">Taidot ja pätevyysmallit</span><span class="sxs-lookup"><span data-stu-id="846d5-103">Skills and proficiency models</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="846d5-104">Taidot ovat resurssien ominaisuuksia, jotka on jaettu Dynamics 365 Project Service Automationin ja, jos käytössä, Dynamics 365 Field Servicen välillä.</span><span class="sxs-lookup"><span data-stu-id="846d5-104">Skills are resource characteristics that are shared between Dynamics 365 Project Service Automation and if present, Dynamics 365 Field Service.</span></span> 

<span data-ttu-id="846d5-105">Ylläpitääksesi taitovarastoa sovelluksessa Project Service Automation, siirry kohtaan **Resurssit** \> **Resurssien taidot**.</span><span class="sxs-lookup"><span data-stu-id="846d5-105">To maintain the repository of skills in Project Service Automation, go to **Resources** \> **Resource Skills**.</span></span> 

> ![Resurssin taidot](media/Resource-Management-image84.png)

## <a name="use-proficiency-models-to-rate-resources"></a><span data-ttu-id="846d5-107">Pätevyysmallien käyttäminen resurssien tasojen määrittelyyn</span><span class="sxs-lookup"><span data-stu-id="846d5-107">Use proficiency models to rate resources</span></span>

<span data-ttu-id="846d5-108">Resurssien taidot on luokiteltu pätevyysmallien mukaan.</span><span class="sxs-lookup"><span data-stu-id="846d5-108">Skills for resources are rated by proficiency models.</span></span> <span data-ttu-id="846d5-109">Yksittäiset luokitukset ovat pätevyysmallissa.</span><span class="sxs-lookup"><span data-stu-id="846d5-109">The individual ratings are in a proficiency model.</span></span> 

1. <span data-ttu-id="846d5-110">Luodaksesi pätevyysmallin siirry kohtaan **Resurssit** \> **Pätevyysmallit** ja valitse sitten **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="846d5-110">To create a proficiency model, go to **Resources** \> **Proficiency Models**, and then select **New**.</span></span>
2. <span data-ttu-id="846d5-111">Määritä uudessa luokitusmallissa pienin luokitusarvo, suurin luokitusarvo ja entiteetti, jota luokitellaan.</span><span class="sxs-lookup"><span data-stu-id="846d5-111">In the new rating model, specify the minimum rating value, the maximum rating value, and the entity that is being rated.</span></span>
3. <span data-ttu-id="846d5-112">**Luokitusarvot**-aliruudukossa voi määrittää eri luokitusarvot vähimmäisarvosta suurimpaan arvoon.</span><span class="sxs-lookup"><span data-stu-id="846d5-112">In the **Rating Values** subgrid, you can define the different rating values, from the minimum to the maximum.</span></span>

> ![Vähimmäis-ja enimmäisluokitukset määritetty](media/Resource-Management-image85.png)

<span data-ttu-id="846d5-114">Nämä luokitusarvot näytetään **Resurssivaatimukset**, **Aikataulutaulukko** ja **Aikatauluavustaja** -suodattimissa.</span><span class="sxs-lookup"><span data-stu-id="846d5-114">These rating values are shown on the **Resource Requirements**, **Schedule Board**, and **Schedule Assistant** filters.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]