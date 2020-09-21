---
title: Aikamerkintäkalenteri
description: Tässä aiheessa on tietoja aikamerkintäkalenterin käytöstä.
author: rumant
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 05/20/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: cc78d9ae-9f1b-4bd4-8cdf-41406f859ff7
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: ea8c5113b9ba89e2255218e6a53f062c25badc98
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/24/2020
ms.locfileid: "3751216"
---
# <a name="time-entry-calendar"></a><span data-ttu-id="f66e4-103">Aikamerkintäkalenteri</span><span class="sxs-lookup"><span data-stu-id="f66e4-103">Time entry calendar</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="f66e4-104">Voit tarkastella aikamerkintöjä kalenterissa **Aikamerkinnät**-sivulla valitsemalla **Näytä** \> **Kalenteriohjausobjekti**.</span><span class="sxs-lookup"><span data-stu-id="f66e4-104">On the **Time Entries** page, you can view the time entries on the calendar by selecting **Show as** \> **Calendar Control**.</span></span>

## <a name="updated-calendar-control"></a><span data-ttu-id="f66e4-105">Kalenterin päivitetty ohjausobjekti</span><span class="sxs-lookup"><span data-stu-id="f66e4-105">Updated calendar control</span></span>

<span data-ttu-id="f66e4-106">Dynamics 365 Project Service Automation tarjoaa uuden ja laajan ajansyöttökokemuksen.</span><span class="sxs-lookup"><span data-stu-id="f66e4-106">Dynamics 365 Project Service Automation offers a new and extensible time entry experience.</span></span> <span data-ttu-id="f66e4-107">Tämä uusi kokemus korvaa aiemmissa versioissa käytetyn mukautetun kalenterinohjausobjektin.</span><span class="sxs-lookup"><span data-stu-id="f66e4-107">This new experience replaces the Custom Calendar Control that was used in earlier versions.</span></span> <span data-ttu-id="f66e4-108">Voit kuitenkin tarkastella aika merkintöjä vain luku -tilassa olevan kalenteriohjausobjektin avulla, jonka Unified Interface Framework tarjoaa päivittäisille, viikoittaisille ja kuukausittaisille näkymille.</span><span class="sxs-lookup"><span data-stu-id="f66e4-108">However, you can still view time entries through a read-only calendar control that the Unified Interface Framework provides for daily, weekly, or monthly views.</span></span>

<span data-ttu-id="f66e4-109">Kalenteri ei tue yksittäisten kalenterikohteiden toimintoja, etkä voi valita yhtä tai useampaa kalenterikohdetta lähetystä tai poistoa varten.</span><span class="sxs-lookup"><span data-stu-id="f66e4-109">The calendar doesn't support actions on individual calendar items, and you can't select one or more calendar items for submission or deletion.</span></span> <span data-ttu-id="f66e4-110">Valitse sen sijaan kalenterikohde avataksesi **Aikakirjaus**-entiteettisivun, jolla voit suorittaa tarvitsemasi toimenpiteet.</span><span class="sxs-lookup"><span data-stu-id="f66e4-110">Instead, select a calendar item to open the **Time Entry** entity page, where you can complete the required actions.</span></span>

## <a name="extensibility"></a><span data-ttu-id="f66e4-111">Laajennettavuus</span><span class="sxs-lookup"><span data-stu-id="f66e4-111">Extensibility</span></span>

<span data-ttu-id="f66e4-112">Voit lisätä mukautettuja kenttiä, määrittää hakukenttiä ja luoda mukautettuja näkymiä **Aikakirjaukset**-sivulla.</span><span class="sxs-lookup"><span data-stu-id="f66e4-112">On the **Time Entries** page that has the time entry grid, you can add custom fields, set up lookup fields, and create custom views.</span></span> <span data-ttu-id="f66e4-113">Voit myös määrittää mukautetun liiketoimintalogiikan, joka perustuu mukautettuihin kenttiin valittuihin tai kirjoitettuihin arvoihin.</span><span class="sxs-lookup"><span data-stu-id="f66e4-113">You can also set up custom business logic that is based on the values that are selected or entered in custom fields.</span></span>
