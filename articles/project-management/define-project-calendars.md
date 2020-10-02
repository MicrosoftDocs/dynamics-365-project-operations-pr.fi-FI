---
title: Projektikalenterien määrittäminen
description: Tässä aiheessa on tietoja projektikalenterin käyttämisestä projektin aikataulun seuraamisessa.
author: ruhercul
manager: AnnBe
ms.date: 09/18/2020
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
ms.openlocfilehash: 1d44a2d0d8c13fb9e93b9a6da15fb3a7ce8d764c
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/28/2020
ms.locfileid: "3897987"
---
# <a name="define-project-calendars"></a><span data-ttu-id="c9999-103">Projektikalenterien määrittäminen</span><span class="sxs-lookup"><span data-stu-id="c9999-103">Define project calendars</span></span>

<span data-ttu-id="c9999-104">_**Koskee:** Project Operationsin resurssiin / muuhun kuin resurssiin perustuvia skenaarioita, Lite-käyttöönotto-kaupasta proformalaskutukseen_</span><span class="sxs-lookup"><span data-stu-id="c9999-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="c9999-105">Määritä projektin aikataulun luomista varten projektikalenteri, joka määrittää päivittäisten työtuntien määrän ja mahdolliset yrityksen kiinnioloajat.</span><span class="sxs-lookup"><span data-stu-id="c9999-105">To create a project schedule, you create a project calendar template that defines the number of working hours per day and any business closures.</span></span> <span data-ttu-id="c9999-106">Projektikalenterimallin luomiseksi työmalli liitetään projektin **Kalenterimalli**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="c9999-106">To create a project calendar template, you associate a work template with the **Calendar template** field for the project.</span></span> <span data-ttu-id="c9999-107">Luo työmalli seuraavien vaiheiden mukaisesti.</span><span class="sxs-lookup"><span data-stu-id="c9999-107">Follow these steps to create a work template.</span></span>

1. <span data-ttu-id="c9999-108">Valitse siirtymisruudun **Resurssit**.</span><span class="sxs-lookup"><span data-stu-id="c9999-108">In the left navigation pane, select **Resources**.</span></span> 
2. <span data-ttu-id="c9999-109">Avaa **Resurssit**-listaussivulla käyttäjän tietue, ja valitse sitten **Näytä työtunnit**.</span><span class="sxs-lookup"><span data-stu-id="c9999-109">On the **Resources** list page, open a user record, and then select **Show Work Hours**.</span></span>

  > [!NOTE]
  > <span data-ttu-id="c9999-110">Varmista, että ponnahdusikkunat on sallittu selaimen sivulla.</span><span class="sxs-lookup"><span data-stu-id="c9999-110">Make sure that you allow pop-ups on the browser page.</span></span> <span data-ttu-id="c9999-111">Näin näet resurssille määritetyt työtunnit.</span><span class="sxs-lookup"><span data-stu-id="c9999-111">This lets you see the work hours set for the resource.</span></span>
  
3. <span data-ttu-id="c9999-112">Valitse **Kuukausinäkymä**-välilehdessä **Määritä**.</span><span class="sxs-lookup"><span data-stu-id="c9999-112">On the **Monthly View** tab, select **Set Up**.</span></span> <span data-ttu-id="c9999-113">Kolme vaihtoehtoa sisältävä lista tulee näkyviin:</span><span class="sxs-lookup"><span data-stu-id="c9999-113">A list of three options appears:</span></span> 

  - <span data-ttu-id="c9999-114">Uusi viikkoaikataulu</span><span class="sxs-lookup"><span data-stu-id="c9999-114">New Weekly Schedule</span></span>
  - <span data-ttu-id="c9999-115">Yhden päivän työaikataulu</span><span class="sxs-lookup"><span data-stu-id="c9999-115">Work Schedule for One Day</span></span>
  - <span data-ttu-id="c9999-116">Poissaolo</span><span class="sxs-lookup"><span data-stu-id="c9999-116">Time Off</span></span>

4. <span data-ttu-id="c9999-117">Valise **Uusi viikkoaikataulu**, ja määritä sen jälkeen tiedot tälle resurssiaikataululle.</span><span class="sxs-lookup"><span data-stu-id="c9999-117">Select **New Weekly Schedule**, and then set the options for this resource schedule.</span></span> <span data-ttu-id="c9999-118">Voit määrittää toistuvan viikoittaisen aikataulun, päivittäiset tuntiparametrit, yrityksen kiinnioloajat ja muita seikkoja.</span><span class="sxs-lookup"><span data-stu-id="c9999-118">You can set a recurring weekly schedule, daily hour parameters, business closures, and more.</span></span>
5. <span data-ttu-id="c9999-119">Määritä päivämääräväli, valitse **Tallenna**, ja valitse sen jälkeen **Sulje**.</span><span class="sxs-lookup"><span data-stu-id="c9999-119">Set the date range, select **Save**, and then select **Close**.</span></span> 
6. <span data-ttu-id="c9999-120">Palaa **Resurssit**-luettelosivulle ja valitse resurssi, jolle määrität työtunnit.</span><span class="sxs-lookup"><span data-stu-id="c9999-120">Go back to the **Resources** list page, and select the resource that you set the work hours for.</span></span> 
7. <span data-ttu-id="c9999-121">Valitse **Määritä kalenteri** määrittääksesi työmallin.</span><span class="sxs-lookup"><span data-stu-id="c9999-121">Select **Set Calendar As** to set the work template.</span></span> 
8. <span data-ttu-id="c9999-122">Syötä **Työmalli**-dialogilaatikossa työmallin nimi, ja valitse sen jälkeen **Käytä**.</span><span class="sxs-lookup"><span data-stu-id="c9999-122">In the **Work Template** dialog box, enter a name for the work template, and then select **Apply**.</span></span> 

<span data-ttu-id="c9999-123">Voit nyt liittää työmallin projektin kalenterimalliin.</span><span class="sxs-lookup"><span data-stu-id="c9999-123">You can now associate the work template with a project calendar template.</span></span>
