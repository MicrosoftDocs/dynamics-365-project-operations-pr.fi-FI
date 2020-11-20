---
title: Osaamisalueiden ja pätevyyksien määrittäminen
description: Tässä aiheessa on tietoja pätevyysmallien määrittämisestä resurssien arvioimiseksi.
author: ruhercul
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
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
ms.openlocfilehash: 8738a4743554704ef76807c81fdefcd74e668e1b
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/28/2020
ms.locfileid: "4124769"
---
# <a name="define-skills-and-proficiencies"></a><span data-ttu-id="aa3c1-103">Osaamisalueiden ja pätevyyksien määrittäminen</span><span class="sxs-lookup"><span data-stu-id="aa3c1-103">Define skills and proficiencies</span></span>

<span data-ttu-id="aa3c1-104">_**Koskee:** Project Operationsin resurssiin / muuhun kuin resurssiin perustuvia skenaarioita, Lite-käyttöönotto-kaupasta proformalaskutukseen_</span><span class="sxs-lookup"><span data-stu-id="aa3c1-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="aa3c1-105">Taidot ovat resurssien ominaisuuksia, jotka on jaettu Dynamics 365 Project Operationsin ja mahdollisesti käytössä olevan Dynamics 365 Field Servicen välillä.</span><span class="sxs-lookup"><span data-stu-id="aa3c1-105">Skills are resource characteristics that are shared between Dynamics 365 Project Operations and if present, Dynamics 365 Field Service.</span></span> 

- <span data-ttu-id="aa3c1-106">Ylläpidä taitosäilöä Project Operationsissa siirtymällä kohtaan **Resurssit** \> **Resurssien taidot**.</span><span class="sxs-lookup"><span data-stu-id="aa3c1-106">To maintain the repository of skills in Project Operations, go to **Resources** \> **Resource Skills**.</span></span> 

## <a name="use-proficiency-models-to-rate-resources"></a><span data-ttu-id="aa3c1-107">Pätevyysmallien käyttäminen resurssien tasojen määrittelyyn</span><span class="sxs-lookup"><span data-stu-id="aa3c1-107">Use proficiency models to rate resources</span></span>

<span data-ttu-id="aa3c1-108">Resurssien taidot on luokiteltu pätevyysmallien mukaan.</span><span class="sxs-lookup"><span data-stu-id="aa3c1-108">Skills for resources are rated by proficiency models.</span></span> <span data-ttu-id="aa3c1-109">Yksittäiset luokitukset ovat pätevyysmallissa.</span><span class="sxs-lookup"><span data-stu-id="aa3c1-109">The individual ratings are in a proficiency model.</span></span> 

1. <span data-ttu-id="aa3c1-110">Luodaksesi pätevyysmallin siirry kohtaan **Resurssit** \> **Pätevyysmallit** ja valitse sitten **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="aa3c1-110">To create a proficiency model, go to **Resources** \> **Proficiency Models**, and then select **New**.</span></span>
2. <span data-ttu-id="aa3c1-111">Määritä uudessa luokitusmallissa pienin luokitusarvo, suurin luokitusarvo ja entiteetti, jota luokitellaan.</span><span class="sxs-lookup"><span data-stu-id="aa3c1-111">In the new rating model, specify the minimum rating value, the maximum rating value, and the entity that is being rated.</span></span>
3. <span data-ttu-id="aa3c1-112">**Luokitusarvot**-aliruudukossa voi määrittää eri luokitusarvot vähimmäisarvosta suurimpaan arvoon.</span><span class="sxs-lookup"><span data-stu-id="aa3c1-112">In the **Rating Values** subgrid, you can define the different rating values, from the minimum to the maximum.</span></span>


<span data-ttu-id="aa3c1-113">Nämä luokitusarvot näytetään **Resurssivaatimukset**, **Aikataulutaulukko** ja **Aikatauluavustaja** -suodattimissa.</span><span class="sxs-lookup"><span data-stu-id="aa3c1-113">These rating values are shown on the **Resource Requirements**, **Schedule Board**, and **Schedule Assistant** filters.</span></span>
