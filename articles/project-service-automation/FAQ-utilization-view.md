---
title: Resurssien veloitettavan käytön katselu
description: Tässä aiheessa on tietoja resurssin käyttönäkymästä.
author: ruhercul
manager: kfend
ms.service: business-applications
ms.custom:
- dyn365-projectservice
ms.date: 9/26/2019
ms.topic: article
ms.prod: Applies to all versions of Project Service
ms.technology: Applies to all versions of Project Service
ms.assetid: 656511ac-6851-42d6-abd4-0c7e77ea5d9c
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 8953015ced24ff10f0bec2570a840cf4e130b01a
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/24/2020
ms.locfileid: "3751123"
---
# <a name="view-chargeable-utilization-for-resources"></a><span data-ttu-id="011e2-103">Resurssien veloitettavan käytön katselu</span><span class="sxs-lookup"><span data-stu-id="011e2-103">View chargeable utilization for resources</span></span>
 
<span data-ttu-id="011e2-104">**Käyttönäkymä** **Project Service -sovelluksen resurssin käyttö** -sivulla näkyy kunkin varattavissa olevan resurssin veloitettava käyttö.</span><span class="sxs-lookup"><span data-stu-id="011e2-104">The **Utilization View** on the **Project Service Resource Utilization** page shows the chargeable utilization for each bookable resource.</span></span> <span data-ttu-id="011e2-105">Koska näkymä perustuu aikataulutaulukkoon, näkymä sisältää useita samoja toimintoja kuin taulukko.</span><span class="sxs-lookup"><span data-stu-id="011e2-105">Because the view is based on the schedule board, you’ll find many of the same functions.</span></span>

> ![Käyttönäkymän näyttökuva](media/FAQ-utilization-1.png)
 

<span data-ttu-id="011e2-107">Veloitettavan käytön laskutoimitus tehdään seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="011e2-107">The chargeable utilization calculation works as follows:</span></span>

   <span data-ttu-id="011e2-108">Veloitettava käyttö = (veloitettavat todelliset tunnit) / (resurssin kapasiteetti)</span><span class="sxs-lookup"><span data-stu-id="011e2-108">Chargeable utilization = (Chargeable actual hours) / (resource capacity)</span></span>

<span data-ttu-id="011e2-109">Solut edustavat näkymän valitun jakson (päivät, viikot tai kuukaudet) laskettua veloitettavaa käyttöä.</span><span class="sxs-lookup"><span data-stu-id="011e2-109">The cells represent the calculated chargeable utilization for the selected period (days, weeks, or months).</span></span>

<span data-ttu-id="011e2-110">Kunkin solun värit näyttävät resurssin veloitettavan käytön verrattuna sen veloitettavaan tavoitekäyttöön.</span><span class="sxs-lookup"><span data-stu-id="011e2-110">The colors in each cell show the chargeable utilization for a resource as compared to their target chargeable utilization.</span></span> 

<span data-ttu-id="011e2-111">Tavoitekäyttö voidaan määrittää joko resurssin oletusroolissa tai yksittäisessä roolissa.</span><span class="sxs-lookup"><span data-stu-id="011e2-111">The target utilization can be set on the resource’s default role or on the individual resource itself.</span></span> <span data-ttu-id="011e2-112">Laskutoimitus käsittelee ensin tavoitteen yksittäisen resurssin ja sitten resurssin oletusroolin.</span><span class="sxs-lookup"><span data-stu-id="011e2-112">The calculation looks at the individual for the target first, and then to the resource’s default role.</span></span>

## <a name="set-target-on-a-resource"></a><span data-ttu-id="011e2-113">Tavoitteen asettaminen resurssille</span><span class="sxs-lookup"><span data-stu-id="011e2-113">Set target on a resource</span></span>

1. <span data-ttu-id="011e2-114">Siirry kohtaan **Resurssit** \> **Resurssit**.</span><span class="sxs-lookup"><span data-stu-id="011e2-114">Go to **Resources** \> **Resources**.</span></span> 
2. <span data-ttu-id="011e2-115">Avaa tietue valitsemalla resurssi.</span><span class="sxs-lookup"><span data-stu-id="011e2-115">Select a resource to open the record.</span></span> 
3. <span data-ttu-id="011e2-116">**Project Service** -välilehdellä voit myös määrittää resurssin tavoitekäytön.</span><span class="sxs-lookup"><span data-stu-id="011e2-116">On the **Project Service** tab, you can set the resource’s target utilization.</span></span>

> ![Näyttökuva Project Service -välilehden käyttämisestä, kun tavoitekäyttöä määritetään](media/FAQ-utilization-2.png)
 
## <a name="set-target-utilization-on-a-role"></a><span data-ttu-id="011e2-118">Tavoitekäytön määritys roolille</span><span class="sxs-lookup"><span data-stu-id="011e2-118">Set target utilization on a role</span></span>

1. <span data-ttu-id="011e2-119">Siirry kohtaan **Resurssit** \> **Resurssin roolit**.</span><span class="sxs-lookup"><span data-stu-id="011e2-119">Go to **Resources** \> **Resource Roles**.</span></span> 
2. <span data-ttu-id="011e2-120">Valitsemalla rooli ja avaa tietue.</span><span class="sxs-lookup"><span data-stu-id="011e2-120">Select a role and open the record.</span></span> 
3. <span data-ttu-id="011e2-121">Määritä roolin tavoitekäyttö.</span><span class="sxs-lookup"><span data-stu-id="011e2-121">Set the target utilization for the role.</span></span>

> ![Näyttökuva resurssin roolien käyttämisestä, kun tavoitekäyttöä määritetään](media/FAQ-utilization-3.png)
 
## <a name="calculate-chargeable-utilization-for-a-resource"></a><span data-ttu-id="011e2-123">Resurssin veloitettavan käytön laskeminen</span><span class="sxs-lookup"><span data-stu-id="011e2-123">Calculate chargeable utilization for a resource</span></span>

<span data-ttu-id="011e2-124">Jos haluat resurssin laskea veloitettavan käytön, sinun on täytettävä tietyt edellytykset.</span><span class="sxs-lookup"><span data-stu-id="011e2-124">To calculate chargeable utilization for a resource, you will need to complete some pre-requisites.</span></span> 

### <a name="set-default-role-for-individual-resource"></a><span data-ttu-id="011e2-125">Oletusroolin määrittäminen yksittäiselle resurssille</span><span class="sxs-lookup"><span data-stu-id="011e2-125">Set default role for individual resource</span></span>

<span data-ttu-id="011e2-126">Ensin on määritettävä tavoitekäyttö joko yksittäiselle resurssille tai resurssin rooleille.</span><span class="sxs-lookup"><span data-stu-id="011e2-126">First, the target utilization must be set on either the individual resource or on resource roles.</span></span> <span data-ttu-id="011e2-127">Jos käytössä on tavoitteiden resurssin roolit, jokaisella yksittäisellä resurssilla on oltava oletusrooli.</span><span class="sxs-lookup"><span data-stu-id="011e2-127">If you are using resource roles for targets, each individual resource must have a default role.</span></span> 

1. <span data-ttu-id="011e2-128">Tee tämä siirtymällä kohtaan **Resurssit** \> **Resurssit**.</span><span class="sxs-lookup"><span data-stu-id="011e2-128">To set this, go to **Resources** \> **Resources**.</span></span> 
2. <span data-ttu-id="011e2-129">Valitse resurssi, avaa tietue ja valitse sitten **Project Service** -välilehti.</span><span class="sxs-lookup"><span data-stu-id="011e2-129">Select a resource, open the record, and then select the **Project Service** tab.</span></span> 
3. <span data-ttu-id="011e2-130">Varmista **Resurssin rooli** -ruudukossa, että resurssille on vain yksi rooli ja että kohdan **On oletus** arvoksi on määritetty **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="011e2-130">In the **Resource Role** grid, make sure there’s one role for the resource and **Is Default** is set to **Yes**.</span></span>
 
### <a name="change-billing-type-for-resource-role"></a><span data-ttu-id="011e2-131">Resurssin roolin laskutustyypin muuttaminen</span><span class="sxs-lookup"><span data-stu-id="011e2-131">Change billing type for resource role</span></span>

<span data-ttu-id="011e2-132">Resurssin roolien laskutustyypiksi on määritettävä **Veloitettava**.</span><span class="sxs-lookup"><span data-stu-id="011e2-132">The resource roles must be set to have a billing type of **Chargeable**.</span></span> 

1. <span data-ttu-id="011e2-133">Siirry kohtaan **Resurssit** \> **Resurssin roolit**.</span><span class="sxs-lookup"><span data-stu-id="011e2-133">Go to **Resources** \> **Resource Roles**.</span></span> 
2. <span data-ttu-id="011e2-134">Avaa tietue, jota haluat päivittää ja määritä sitten laskutustyypin oletusarvoksi **Veloitettava**.</span><span class="sxs-lookup"><span data-stu-id="011e2-134">Open the record you want to update, and then set the billing type default to **Chargeable**.</span></span>

### <a name="set-working-hours-for-resource-role"></a><span data-ttu-id="011e2-135">Työtuntien määrittäminen resurssin roolille</span><span class="sxs-lookup"><span data-stu-id="011e2-135">Set working hours for resource role</span></span>
 
<span data-ttu-id="011e2-136">Resurssilla on oltava työtunteja kapasiteetin laskentaa varten.</span><span class="sxs-lookup"><span data-stu-id="011e2-136">The resource must have working hours for the capacity calculation.</span></span> 

1. <span data-ttu-id="011e2-137">Siirry kohtaan **Resurssit** \> **Resurssit**.</span><span class="sxs-lookup"><span data-stu-id="011e2-137">Go to **Resources** \> **Resources**.</span></span> 
2. <span data-ttu-id="011e2-138">Avaa tietue valitsemalla resurssi. Valitse sitten **Näytä työtunnit**.</span><span class="sxs-lookup"><span data-stu-id="011e2-138">Select a resource to open the record, and then select **Show Work Hours**.</span></span> 
3. <span data-ttu-id="011e2-139">Voit joukkopäivittää resurssiluettelon valitsemalla **Resurssiluettelo**-näkymästä arvon kohdalle **Työtuntimalli**.</span><span class="sxs-lookup"><span data-stu-id="011e2-139">You can bulk-update the list of resources by applying a **Work Hour Template** from the **Resource List** view.</span></span>

## <a name="troubleshooting-chargeable-actual-hours"></a><span data-ttu-id="011e2-140">Veloitettavien todellisten tuntien vianmääritys</span><span class="sxs-lookup"><span data-stu-id="011e2-140">Troubleshooting chargeable actual hours</span></span>

<span data-ttu-id="011e2-141">Veloitettavat todelliset tunnit saadaan **Todelliset arvot** -entiteetistä.</span><span class="sxs-lookup"><span data-stu-id="011e2-141">The chargeable actual hours are sourced from the **Actuals** entity.</span></span> <span data-ttu-id="011e2-142">Todelliset arvot, joiden laskutustyyppi on **Veloitettava**, sisällytetään laskelmaan. Tämän vuoksi tarvitaan projekteja, joiden todelliset arvot ovat veloitettavia.</span><span class="sxs-lookup"><span data-stu-id="011e2-142">Actuals with a billing type of **Chargeable** are included in the calculation and, for this reason, you must have projects where the actuals that are chargeable.</span></span>

<span data-ttu-id="011e2-143">Tarkista seuraavat kohdat, jos et löydä veloitettavaa käyttöä:</span><span class="sxs-lookup"><span data-stu-id="011e2-143">If you are not seeing chargeable utilization, here are some things you can check:</span></span>

- <span data-ttu-id="011e2-144">Resurssin kapasiteetille on määritetty työtunteja.</span><span class="sxs-lookup"><span data-stu-id="011e2-144">The resource has working hours defined for capacity.</span></span>
- <span data-ttu-id="011e2-145">Resurssilla on joko yksittäinen määritetty käytön tavoite tai sille on delegoitu oletusrooli.</span><span class="sxs-lookup"><span data-stu-id="011e2-145">The resource has either an individually defined utilization target or has a default role assigned to it.</span></span> <span data-ttu-id="011e2-146">Roolille on määritetty käytön tavoite.</span><span class="sxs-lookup"><span data-stu-id="011e2-146">The role has a utilization target defined for it.</span></span>
- <span data-ttu-id="011e2-147">Todellisten arvojen laskutustyyppi on **Veloitettava** sen jakson aikana, jolle odotat käytön laskentaa.</span><span class="sxs-lookup"><span data-stu-id="011e2-147">Actuals have a billing type of **Chargeable** for the period you are expecting a utilization calculation for.</span></span> <span data-ttu-id="011e2-148">Tarkista seuraavat kohdat, jos löydät todellisia arvoja, joiden laskutustyyppi on jokin muu kuin Veloitettava:</span><span class="sxs-lookup"><span data-stu-id="011e2-148">Check the following if you are seeing actuals with billing types other than chargeable:</span></span>

  - <span data-ttu-id="011e2-149">Todellisessa arvossa käytetyn roolin laskutustyyppi on jokin muu kuin Veloitettava.</span><span class="sxs-lookup"><span data-stu-id="011e2-149">The role used on the actual has a default billing type of something other than chargeable.</span></span>
  - <span data-ttu-id="011e2-150">Projektin taustalla olevan projektisopimusrivin rooliksi on määritetty Ei-veloitettava.</span><span class="sxs-lookup"><span data-stu-id="011e2-150">The role on the project contract line backing the project has been set to non-chargeable.</span></span>
  - <span data-ttu-id="011e2-151">Projektiin ei ole liitetty sopimusriviä.</span><span class="sxs-lookup"><span data-stu-id="011e2-151">The project does not have an associated contract line.</span></span>

