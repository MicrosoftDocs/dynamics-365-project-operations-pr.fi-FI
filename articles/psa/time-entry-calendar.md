---
title: Aikamerkintäkalenteri
description: Tässä aiheessa on tietoja aikamerkintäkalenterin käytöstä.
author: rumant
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 05/20/2019
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 413aba735a5011a9b40c1d5b0bf43c6771db0f7b
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/28/2020
ms.locfileid: "4131171"
---
# <a name="time-entry-calendar"></a><span data-ttu-id="37260-103">Aikamerkintäkalenteri</span><span class="sxs-lookup"><span data-stu-id="37260-103">Time entry calendar</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="37260-104">Voit tarkastella aikamerkintöjä kalenterissa **Aikamerkinnät**-sivulla valitsemalla **Näytä** \> **Kalenteriohjausobjekti**.</span><span class="sxs-lookup"><span data-stu-id="37260-104">On the **Time Entries** page, you can view the time entries on the calendar by selecting **Show as** \> **Calendar Control**.</span></span>

## <a name="updated-calendar-control"></a><span data-ttu-id="37260-105">Kalenterin päivitetty ohjausobjekti</span><span class="sxs-lookup"><span data-stu-id="37260-105">Updated calendar control</span></span>

<span data-ttu-id="37260-106">Dynamics 365 Project Service Automation tarjoaa uuden ja laajan ajansyöttökokemuksen.</span><span class="sxs-lookup"><span data-stu-id="37260-106">Dynamics 365 Project Service Automation offers a new and extensible time entry experience.</span></span> <span data-ttu-id="37260-107">Tämä uusi kokemus korvaa aiemmissa versioissa käytetyn mukautetun kalenterinohjausobjektin.</span><span class="sxs-lookup"><span data-stu-id="37260-107">This new experience replaces the Custom Calendar Control that was used in earlier versions.</span></span> <span data-ttu-id="37260-108">Voit kuitenkin tarkastella aika merkintöjä vain luku -tilassa olevan kalenteriohjausobjektin avulla, jonka Unified Interface Framework tarjoaa päivittäisille, viikoittaisille ja kuukausittaisille näkymille.</span><span class="sxs-lookup"><span data-stu-id="37260-108">However, you can still view time entries through a read-only calendar control that the Unified Interface Framework provides for daily, weekly, or monthly views.</span></span>

<span data-ttu-id="37260-109">Kalenteri ei tue yksittäisten kalenterikohteiden toimintoja, etkä voi valita yhtä tai useampaa kalenterikohdetta lähetystä tai poistoa varten.</span><span class="sxs-lookup"><span data-stu-id="37260-109">The calendar doesn't support actions on individual calendar items, and you can't select one or more calendar items for submission or deletion.</span></span> <span data-ttu-id="37260-110">Valitse sen sijaan kalenterikohde avataksesi **Aikakirjaus**-entiteettisivun, jolla voit suorittaa tarvitsemasi toimenpiteet.</span><span class="sxs-lookup"><span data-stu-id="37260-110">Instead, select a calendar item to open the **Time Entry** entity page, where you can complete the required actions.</span></span>

## <a name="extensibility"></a><span data-ttu-id="37260-111">Laajennettavuus</span><span class="sxs-lookup"><span data-stu-id="37260-111">Extensibility</span></span>

<span data-ttu-id="37260-112">Voit lisätä mukautettuja kenttiä, määrittää hakukenttiä ja luoda mukautettuja näkymiä **Aikakirjaukset**-sivulla.</span><span class="sxs-lookup"><span data-stu-id="37260-112">On the **Time Entries** page that has the time entry grid, you can add custom fields, set up lookup fields, and create custom views.</span></span> <span data-ttu-id="37260-113">Voit myös määrittää mukautetun liiketoimintalogiikan, joka perustuu mukautettuihin kenttiin valittuihin tai kirjoitettuihin arvoihin.</span><span class="sxs-lookup"><span data-stu-id="37260-113">You can also set up custom business logic that is based on the values that are selected or entered in custom fields.</span></span>